# Ej. 04 - Manejando el responsive de la sección de publicidad

## Introducción
El layout de los elementos, la manera en que los acomodamos dentro de la pantalla, debe ajustarse para las dimensiones de pantalla que podrían presentar nuestro contenido. Esto lo logramos con media-queries, pero aprenderemos cómo modificar la distribución de contenido usando flexbox.

## Objetivos
1. Aprender a utilizar flexbox para acomodar adecuadamente los elementos en diferentes resoluciones de pantalla.
2. Aplicar los media queries de manera correcta.

## Requisitos
- Tener instalado Visual Studio Code
- Tener conocimientos de CSS Flexbox

## Desarrollo

Si hacemos un poco de scroll hacia la parte inferior de la página, nos daremos
cuenta que las siguientes secciones están desbordadas y no se ven bien ya que
incluso generan un scroll horizontal (debido al desborde en mención). Iremos
corrigiendo esto sección por sección. Empecemos por la sección de publicidad que
está estructurada con propiedades de **Flexbox**.

El motivo de desborde en esta sección es que nosotros esperamos que la pantalla
se divida en lo horizontal en 2 partes iguales para que en un lado se
muestre el video y en el otro el _call-to-action_ de publicidad. Sin embargo, el
ancho del video es muy grande como para que alcance el texto a su lado. Debido
a esto, lo que haremos será cambiar la dirección del flujo de nuestra sección.
Es decir, actualmente nuestro _flex container_ tiene la propiedad por defecto
de `flex-direction: row;` que lo alínea uno al lado del otro, lo cambiaremos por
un `flex-direction:column;` para que vaya uno debajo del otro, ajustaremos el
ancho de tal forma que no haya un desborde y reduciremos el tamaño de la fuente
para tener una jerarquía correctamente organizada.

Teniendo en cuenta nuestra estructura:

```html
<section class="promo">
  <article class="explanatory-video">
    <video
      controls
      poster="https://cdn.videvo.net/videvo_files/video/premium/video0036/thumbnails/computer_code00_small.jpg"
    >
      <source
        type="video/webm"
        src="https://cdn.videvo.net/videvo_files/video/premium/video0036/small_watermarked/computer_code00_preview.webm"
      />
      <source
        type="video/mp4"
        src="https://cdn.videvo.net/videvo_files/video/premium/video0036/small_watermarked/computer_code00_preview.mp4"
      />
    </video>
    <img
      src="https://getmatcha.com/wp-content/themes/getmatcha/img/see_how_it_works.png"
      alt="See how it works"
    />
  </article>
  <article class="publish">
    <h3>Publish to your blog in minutes, not hours.</h3>
    <p>
      Your blog is your most powerful asset to build, engage, and retain a loyal
      audience. But you don’t have hours to create content that may or may not
      work. With Matcha, instantly publish from our library of 10,000+
      professionally written articles and build your email list faster with our
      powerful conversion tool.
    </p>
    <form>
      <p>Start publishing today:</p>
      <div>
        <input type="text" placeholder="Enter email" />
        <button>Start My Trial</button>
      </div>
    </form>
  </article>
</section>
```

Empecemos por cambiar la dirección de nuestro contenedor en dispositivos
pequeños:

```css
@media (max-width: 575px) {
  /** Media queries previos al banner **/
  .promo {
    flex-direction: column;
  }
}
```

Con este simple cambio nuestro texto de _call-to-action_ se movió a la parte
inferior del video, y si inspeccionamos los estilos que este contiene,
notaremos que tiene un `max-width: 70%;` que nos ayudaba a poner un margen a los
lados parar que se vea centrado. En la experiencia móvil, si bien deseamos
mantener un margen, no es conveniente que sea tan grande dado que contamos con menos
espacio por lo que lo moveremos a un `90%` y ajustaremos el ancho del video para
que respete este ancho también.

```css
@media (max-width: 575px) {
  /** Media queries previos al banner **/
  .promo {
    flex-direction: column;
    max-width: 90%;
  }

  .explanatory-video > video {
    width: 100%;
  }
}
```

Ahora ajustaremos el tamaño de la fuente del título promocional para que se
ajuste a la jerarquía de información que tenemos en nuestra página:

```css
@media (max-width: 575px) {
  /** Media queries previos al banner **/
  .promo {
    flex-direction: column;
    max-width: 90%;
  }

  .explanatory-video > video {
    width: 100%;
  }

  .publish {
    margin-top: 10px;
  }

  .publish > h3 {
    font-size: 25px;
    line-height: 1.2;
  }
}
```

> TIP: El valor que hemos asignado a la propiedad `line-height` no tiene una medida, te recomendamos averiguar cómo se calcula el valor final de esta propiedad.
> Puedes consultar la [documentación de MDN](https://developer.mozilla.org/es/docs/Web/CSS/line-height).


<br/>

Adicionalmente, cambiamos el margen superior para agregar una separación entre
el video y el texto, y también fue necesario cambiar la propiedad `line-height`
ya que el tamaño fijo que esta contenía era mucho para el nuevo tamaño.

Por último, nos falta editar el formulario de registro.

<br/>

[Siguiente](../reto-04/README.md)