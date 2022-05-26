# Ej. 04 - Alineamiento horizontal con flexbox

## Objetivos
- Utilizar flexbox para alinear correctamente el contenido
- Reconocer la diferencia entre Felxbox container y flex-items.

---
<br/>

## Requisitos
-Tener instalado Visual Studio Code

---
<br/>

## Desarrollo

Para llevar esto a cabo, revisemos nuestra estructura actual, probablemente se
vea algo así:

```html
<!-- Contenedor -->
<section>
  <!-- Video -->
  <video></video>
  <!-- Contenido de publicidad -->
  <article></article>
</section>
```

> TIP: No interesa si tienes un `div` en vez del `section` o `article`, pero si
> es importante que tengas un contenedor de display `block` por defecto.

Ya que tenemos claro la estructura, debemos de definir quién va a ser el _flex container_
y quiénes los _flex items_. Para nuestro caso, el `section` sería nuestro flex
container ya que es quien va a controlar la alineación del video y el contenido
publicitario. Por ende, aplicaremos una clase y le agregaremos la propiedad de
`display: flex`.

```html
<!-- Contenedor -->
<section class="promo">
  <!-- Video -->
  <video></video>
  <!-- Contenido de publicidad -->
  <article></article>
</section>
```

```css
.promo {
  display: flex;
}
```

Con solo agregar esta propiedad verás que el contenido publicitario se puso al
lado del video. Sin embargo, notaremos 2 cosas principalmente:

- El video y contenido publicitario abarcan todo el ancho del navegador.
- Están muy apegados a la imagen que la precede y al borde inferior del navegador.
- El contenido publicitario no está alineado al centro del alto del video.

Resolvamos cada uno de estos problemas en orden. Empecemos, por limitar el ancho
que abarca esta nueva sección. Esto lo podemos hacer especificando un ancho
menor al del que tiene actualmente (100%) y para no poner una medida exacta que
funcione solo para un tamaño de pantalla, podemos usar la unidad de `%` para
hacerlo relativo. ¿Qué tal si probamos con un 70%?

```css
.promo {
  display: flex;
  width: 70%;
}
```

Esto acortó el texto pero del lado derecho, sin embargo, nosotros queremos que
el contenido se centre, de tal forma que quede el mismo espacio a cada lado.
Esto lo podríamos lograr poniendo un `margin-left` pero calcular la medida nos
podría resultar tal vez un poco inexacta. Un _hack_ común cuando quieres lograr
un centrado horizontal en elementos que son contenedores es usando `margin: auto`.
Esta propiedad lo que hace es calcular un margen automático a cada uno de los
lados dependiendo del espacio que tenga libre. Por lo tanto, como nosotros hemos
indicado que nuestro contenedor tiene un ancho de 70% sobre una pantalla que
equivale al 100%, le quedan 30% para repartir en el margen y como el valor a
aplicar a cada lado es el mismo (_auto_), el navegador reparte la misma
proporción a cada uno de los extremos (15% en nuestro caso).

```css
.promo {
  display: flex;
  width: 70%;
  margin: auto;
}
```

¡Eso es magia! En realidad, es CSS :sweat_smile:.

Bien, ahora agreguemos un poco de separación entre la imagen superior y el borde
inferior del navegador, lo cual podríamos lograrlo usando un `margin-top` y
`margin-bottom`. Espera, pero ya le hemos dicho que el margen sea automático,
¿cómo hacemos? Esto lo podemos lograr indicando que el contenedor tendrá un
margen superior e inferior de 100px por ejemplo y que a los costados mantendrá
un margen automático.

```css
.promo {
  display: flex;
  width: 70%;
  margin: 100px auto;
}
```

Esto ya va tomando forma, es momento de volver a Flexbox y comenzar a alinear
a los _flex items_. Primero, vamos a alinear verticalmente al centro para que
nuestro contenido publicitario no se vea con espacio en blanco en la parte
inferior.

```css
.promo {
  display: flex;
  width: 70%;
  margin: 100px auto;
  align-items: center;
}
```

Bien, de esta manera el contenido publicitario ya queda alineado verticalmente
al centro respecto del video. Sin embargo, ¿parece que falta una separación entre
el video y el contenido, no? No te preocupes, esto lo vamos a solucionar
definiendo el tamaño que van a ocupar cada uno de ellos más adelante.

<br/>

[Siguiente](../reto-04/README.md)