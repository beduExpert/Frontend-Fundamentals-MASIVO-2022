# Ej. 2  Agregando características principales de Matcha

## Objetivos
- Utilizar CSS Grid para acomodar  nuestro contenido.
- Combinar las diferentes propiedades de CSS Grid al practicar para acomodar el contenido.

---
<br/>

## Requisitos

- Tener instalado Visual Studio Code

---
<br/>

## Desarrollo

¡Empecemos! Vamos a trabajar en la sección de características principales de
nuestra web.

![Características principales](../assets/features.png)

Aprovechando que su apariencia puede ser construida a partir del uso de filas y
columnas, haremos uso de Grid CSS para llevar a cabo esta parte de la web.

## Definiendo el contenedor

En Grid CSS, al igual que en flexbox existe una diferencia entre el _grid container_
y los _grid items_. Esto hace refencia a que el contenedor (al que aplicaremos
la propiedad de CSS `display` con valor `grid`) será el _grid container_,
mientras que los elementos que estén contenidos en él, serán los _grid items_.

Definiendo nuestro contenido se verá algo así:

```html
<!-- Contenido de publicidad viene antes de esta sección -->
<section class="features"></section>
<!-- Contenido de casos de éxito vienen después -->
```

```css
.features {
  display: grid;
}
```

De esta manera, lograremos crear la sección inicial donde pondremos nuestra
primera grid que contendrá a las características principales de nuestro sitio.

## Agregando los grid items

En nuestro web, contamos con 4 características principales, distribuidas en 2
columnas y 2 filas, comencemos por definir dichos elementos.

```html
<!-- Contenido de publicidad viene antes de esta sección -->
<section class="features">
  <article>Característica 1</article>
  <article>Característica 2</article>
  <article>Característica 3</article>
  <article>Característica 4</article>
</section>
<!-- Contenido de casos de éxito vienen después -->
```

Si solo agregamos los contenedores de nuestras características, estas se
mostrarán sin ninguna apariencia en particular (como si el `display: grid` que
agregamos no funcionara) y en realidad es el resutlado esperado, puesto que,
es necesario indicar cómo se van a distribuir los elementos en la grid.

Para esto, podemos usar las propiedades `grid-template-columns` y `grid-template-rows`,
dichas propiedades nos permite especificar la cantidad y tamaño de cada una de
las columnas y filas respectivamente. Veamos un ejemplo, necesitamos definir que
tenemos 2 columnas, imaginemos que sean de `300px`:

```css
.features {
  display: grid;
  grid-template-columns: 300px 300px;
}
```

:::tip

Como tal vez te habrás percatado, la propiedad `grid-template-columns` está
siendo aplicada al _grid container_ y no a cada _grid item_. Similar a como
vimos en Flexbox, es necesario saber que la apariencia general del contenido la
definimos en los estilos del contenedor.

Adicionalmente, hemos definimos 2 veces `300px` para indicar que tendremos 2
columnas de `300px` y de esta manera el contenido toma forma similar a la que
deseamos.

:::

Probablemente te preguntarás, ¿qué pasaría si tuviéramos 5 columnas en vez de 2
del mismo tamaño, tendríamos que escribir 5 veces `300px`? Para esto, CSS nos
provee de una función llamada `repeat(cantidad, tamaño)` que podemos usar para
definir cuántas veces queremos repetir un mismo tamaño:

```css
.features {
  display: grid;
  grid-template-columns: repeat(2, 300px);
}
```

Hasta aquí todo bien, sin embargo, estamos de acuerdo que no siempre vamos a
utilizar un tamaño fijo para indicar el ancho que nuestras columnas van a ocupar.
Si bien, podemos usar las unidades relativas como `%`, `em/rem`, `vw/vh`, etc.,
CSS Grid nos provee con una unidad llamada `fr` (fracción) que se encarga de
calcular dinámicamente el espacio disponible y dividirlo entre los diversos
elementos. Veamos algunos ejemplos:

```css
.features {
  display: grid;
  grid-template-columns: 500px 1fr;
}
```

En este caso, estamos definiendo 2 columnas, la primera con un ancho fijo de
`500px` y la segunda columna con el resto de espacio disponible en la pantalla.
¿Qué pasa si quisiéramos divisiones que ocupen el mismo espacio?

```css
.features {
  display: grid;
  grid-template-columns: 1fr 1fr;
}
```

Declarando que cada columna ocupe _una fracción_ del espacio disponible, hacemos
que cada una ocupe la mitad del espacio disponible, de esta manera si tuviéramos
cuatro columnas cada una con el ancho de `1fr`, cada columna estará tomando un
ancho del 25% del espacio disponible o 1/4 (depende de que notación les guste y
entiendan mejor).

[Siguiente](../reto-01/README.md)