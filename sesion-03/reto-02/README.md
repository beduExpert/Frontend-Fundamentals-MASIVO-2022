# Reto 2.1 - Agregando controles de reproducción al video
## Objetivos
- Configurar el elemento de video para que muestre controles de reproducción.
- Agregar una imagen para que el video muestre una pre-visualización del contenido.

---
<br/>

## Requisitos
- Tener Git Bash si usas Windows.
- Tener conocimientos básicos de HTML y CSS
- Tener instalado Visual Studio Code


---
<br/>

## Instrucciones

Resulta que por defecto el navegador no agrega controles de reproducción al video,
¿puedes buscar cómo agregárselo?

> TIP: Lo que buscas es un atributo de la etiqueta `<video></video>`.

<br/>

<details>
  <summary>Posible solución</summary>

Agrega el atributo `controls` a la etiqueta `<video></video>`.

```html
<body>
  <!-- Contenido previo -->
  <!-- ... -->

  <!-- Contenedor de video -->
  <section>
    <video
      controls
      src="https://cdn.videvo.net/videvo_files/video/premium/video0036/small_watermarked/computer_code00_preview.mp4"
    ></video>
  </section>
</body>
```

</details>

<br/>
<br/>

Bien, nuestro videos ya cuenta con controles de reproducción, además soporta más
de un formato para optimizar la experiencia de nuestros usuarios. Sin embargo,
sería genial poder definir la imagen que queremos que se vea antes de que se
reproduzca el video. ¿Nos ayudas a agregar esta funcionalidad?

> TIP: Esta funcionalidad también se logra a través de un atributo de la etiqueta
`<video></video>`.

<details>
  <summary>Posible solución</summary>

Agrega el atributo `poster` a la etiqueta `<video></video>`, asignándole el link
de la imagen de portada como valor.

```html
<section>
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
</section>
```

</details>

<br/>

[Siguiente](../Ejemplo-03/README.md)