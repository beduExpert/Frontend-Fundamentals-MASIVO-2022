# Ej. 02 - Cambiando el modelo de caja del menú de navegación

## Objetivo
- Identificar elementos de bloque y de línea.
- Usar etiquetas semánticas para mejor legibilidad del código.
- Definir conjunto de propiedades de CSS para alinear correctamente el contenido de la barra de navegación.

---
<br/>

## Requisitos
- Tener instalado Visual Studio Code
- Conocer la diferencia entre elemento de bloque y elemento de línea

---
<br/>

## Desarrollo

En este punto ya tenemos las separaciones deseadas entre los bloques más grandes
de contenido, sin embargo nuestro menú de navegación aun no tiene la apariencia
del sitio original, ya que se muestran de forma vertical (uno debajo del otro),
mientras que el diseño original lo muestra horizontalmente.

## Concepto: Display `block` vs `inline`

¿Por qué se muestra por defecto uno debajo de otro? Esto es debido a los estilos
que las etiquetas tienen asignadas por defecto, y este comportamiento está
relacionado a la propiedad `display`. El navegador asigna a las etiquetas de HTML
la propiedad `display` con valores `block` o `inline`. Los elementos con
`display: block;` usan todo el ancho disponible de su contenedor, es decir, si
nosotros creamos 4 etiquetas `<p></p>`, una seguida de la otra, vamos a ver que
cada texto que pongamos se mostrará uno debajo de otro porque por defecto su
ancho será del 100%. Mientras que los elementos con `display: inline;` usan solo
el espacio necesario para mostrar su contenido.

Algunos ejemplos de elementos con display `block` son: `div`, `p`, `ul`, `h1`,
`header`, `section`, `aside`, `nav`, y muchos más.

Y algunos ejemplos de elementos con display `inline` son: `img`, `a`, `span`,
`strong`, entre otros.

Teniendo en cuenta esta información, nuestro menú de navegación está basado de
las etiquetas `ul` y `li` que tienen display `block` y `list-item` (se comporta
como display `block` si no hay un valor especificado, puedes leer más al respecto
[aquí](https://developer.mozilla.org/en-US/docs/Web/CSS/display-listitem))
respectivamente.

Una solución podría ser reemplazar el display de los `li` a `inline`.

```css
li {
  display: inline;
}
```

Si aplicamos este estilo, nuestro menú se verá ahora de manera horizontal, pero
se seguirían viendo 3 filas: una para el logo, otra para el menú y la última
para las acciones de usuario.

Para evitar las 3 filas, tendríamos que poner a cada elemento contenedor (`a`,
`nav` y `div`) el display `inline`, sin embargo, al cambiar a este valor de
`display` nos encontramos que perdemos ciertas propiedades como `margin-top`,
`margin-bottom`, `height`, es decir, por más que le pongamos un valor, este no
se ve reflejado, y este es el comportamiento correcto que se define para los
elemento scon `display: inline;`. Ante esto, podemos usar otro valor llamado
`inline-block` que mezcla lo mejor de `block` e `inline`, permitiendo cambiar
el layout a un comporamiento como el `inline` pero permitiendo cambiar los
márgenes verticales y la altura como cualquier elemento con display `block`.

Pongamos a prueba este nuevo display, asignándolo a todos los hijos directos de
la etiqueta header:

```css
.header > * {
  display: inline-block;
}
```

¡Muy bien! Con esto conseguimos que estén alineados. ¿Qué tal si le damos un poco
de espacio a cada parte de la barra de navegación? Si tomamos el contenedor (la
etiqueta `header` para la barra de navegación) como un todo equivalente al 100%
y a cada uno de sus hijos les damos un porcentaje de ancho. Podríamos decir que
el logo va a usar un 15% del tamaño de su contenedor, el menú de navegación un
70% y las acciones de usuario el 15% restante. Para aplicar estos estilos podemos
ponerle atributos de clase para que sean más fáciles de identificar:

```html
<header class="header">
  <!-- Logo con link a la página principal -->
  <a href="/" class="logo"></a>
  <!-- Menú de navegación -->
  <nav class="navbar"></nav>
  <!-- Contenedor de acciones de usuario -->
  <div class="actions"></div>
</header>
```

```css
.logo {
  width: 15%;
}

.navbar {
  width: 70%;
}

.actions {
  width: 15%;
}
```

¿Viste lo que pasó? Las acciones de usuario se fueron debajo de los demás
elementos de la barra de navegación. ¿Por qué te imaginas que esto pasó? ¿Serán
nuestras matemáticas (15 + 75 + 15 = 100) :thinking:?

Tranquilxs, esto se debe a que cuando le dijimos que le ponga el `display: inline-block`
a cada uno de los hijos del `header`, los espacios entre cada etiqueta tomaron
un tamaño también, sí, leíste bien, los espacios, aquellas teclas ENTER que
presionamos para que nuestro código se vea más bonito, puedes hacer la prueba
quitando las separaciones:

```html
<header class="header">
  <!-- Logo con link a la página principal -->
  <a href="/" class="logo"></a
  ><!-- Menú de navegación -->
  <nav class="navbar"></nav>
  <!-- Contenedor de acciones de usuario -->
  <div class="actions"></div>
</header>
```

Resulta que al darle un display `inline-block` a los espacios de nuestro código
le damos la posibilidad de tener un tamaño porque al final representan un texto
vacío, el tamaño variará dependiendo del tamaño de fuente que tenga su contenedor.
Si bien, quitando los espacios entre cada etiqueta soluciona el problema, no es
una solución escalable, puesto que si agregamos algo más dentro de la etiqueta
`header` tendríamos el mismo problema y terminaríamos con una sola línea de
código muy larga. [Otras soluciones](https://css-tricks.com/fighting-the-space-between-inline-block-elements/)
implican agregarle son utilizar comentarios entre los saltos de línea, poner un
margin negativo a cada elemento, quitar la etiqueta de cierre y demás.

En nuestro caso usaremos el _hack_ del `font-size`, resulta que si lo que le da
tamaño a los espacios en blanco es el tamaño de la fuente, podemos darle un
tamaño de fuente 0 al contenedor y luego asignar el tamaño de fuente correcto
en cada elemento hijo. Hagamos una prueba, teniendo en cuenta que el tamaño de
la fuente será de 16px para el menú de navegación:

```css
.header {
  margin-top: 40px;
  margin-left: 20px;
  margin-right: 20px;
  font-size: 0;
}

.header > * {
  display: inline-block;
  font-size: 16px;
}
```

¡Eso es magia! En realidad no, es sufrir con CSS :sweat:.

<br/>

# Alineamiento vertical

Resulta que para alinear al centro verticalmente, debemos hacer uso de la
propiedad `vertical-align: middle`, sin embargo, si aplicamos solo esta propiedad
no nos quedará centrado correctamente, esto debido a que cada elemento tiene un
tamaño diferente. Para solucionar esto, podemos sacar provecho que el contenedor
tiene un tamaño fijo (`.header` con `height:45px;`) y podemos decir que cada hijo
del elemento `header` tenga un height del `100%`. Por último, después de aplicar
ambas propiedades nos daremos con la sorpresa de que no queda verticalmente
centrado ya que a pesar que los elementos tienen el mismo tamaño, no comparten
el mismo espacio que el texto debería ocupar, para esto existe la propiedad
`line-height` que nos permite indicar cuánto es el tamaño de altura que ocupará
cada línea de texto, en este caso debería ser igual al tamaño del contenedor
(45px), quedando así:

```css
.header > * {
  display: inline-block;
  font-size: 16px;
  vertical-align: middle;
  height: 100%;
  line-height: 45px;
}
```

Con esto quedaría centrado nuestro menú de navegación, pero si somos
perfeccionistas, nos daremos cuenta que el logo no está centrado verticalmente,
lo podemos solucionar agrandando su altura al 100% del contendor:

```css
.logo > img {
  height: 100%;
}
```

El último de los detalles sería cambiar el peso de la fuente en los textos del
menú de navegación y los botones ya que aunque no parezcan son distintos en la
web original:

```css
.navbar {
  width: 70%;
  text-align: center;
  color: #025157;
  font-weight: 500;
}

.actions {
  width: 15%;
  text-align: right;
  font-size: 14px;
  font-weight: 600;
}
```

Wohoo!! Finalmente hemos terminado nuestra barra de navegación. ¿Qué te pareció?
Interesante todo lo que tienes que hacer para poder darle la forma que deseas,
¿no?. Como mencionado anteriormente, existen otras técnicas que hacen esto de
una manera mucho más sencilla pero la discutiremos en su momento. No olvides
subir tus cambios a Github y revisar que se vean los cambios reflejados en tu
página alojada en GitHub Pages.

<br/>

[Siguiente](../reto-02/README.md)