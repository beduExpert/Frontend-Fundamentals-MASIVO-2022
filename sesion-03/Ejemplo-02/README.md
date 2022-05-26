# Ej. 02 - Agregando la etiqueta video de HTML5

## Objetivo
- Agregar un elemento de video a tu proyecto.
- Configurar automáticamente el video según el tamaño de pantalla o dispositivo usado para visualizar la página de tu proyecto.

---
<br/>

## Requisitos
- Tener Visual Studio Code instalado.

---
<br/>

## Desarrollo

¡Manos a la obra! Antes de agregar el video, debemos de saber qué video vamos a
utilizar en nuestra web, si inspeccionamos la web de Matcha, encontraremos que
usa un video que está almacenado en una plataforma externa llamada Wistia, en
este caso, dicha plataforma provee una forma diferente de agregar el video, por
lo cual usaremos nuestro propio video y una manera más estándar de agregarlo.

Los recursos que usaremos serán:

- [Portada](https://cdn.videvo.net/videvo_files/video/premium/video0036/thumbnails/computer_code00_small.jpg),
  cuando el video no haya sido reproducido, mostrará una imagen de portada.
- [Video en formato Webm](https://cdn.videvo.net/videvo_files/video/premium/video0036/small_watermarked/computer_code00_preview.webm),
  este es el video que se reproducirá cuando el navegador soporte la codificación
  de videos con formato `webm`.
- [Video en formato MP4](https://cdn.videvo.net/videvo_files/video/premium/video0036/small_watermarked/computer_code00_preview.mp4),
  este video es el más común y probablemente con mayor soporte, por lo que será
  nuestra opción por defecto en caso el navegador que usamos no soporte
  codificación de otros formatos.

>TIP: El video que estamos usando en el ejemplo fue obtenido de un repositorio de videos
> gratis para usar sin fines de uso comercial. Si en caso, deseas usar otro video
diferente al de los ejemplos, eres libre de hacerlo. Solo considera que deberás
contar con la imagen de portada y el video en al menos un formato que funcione
en tu navegador.
>La web desde la que fue obtenido el video en mención es [Videvo](https://www.videvo.net/).

> TIP
>La página comentada en el tip anterior solo da la opción de descargar el video,
si quieres obtener el link del video que usa esa página, puede ser un buen momento
para que le preguntes al mentor de la sesión _¿cómo usar el devtools del navegador?_.

Una vez con los recursos a usar definidos, empecemos. Como el video junto con
un texto promocional irán alineados de manera distinta al contenido que tenemos
actualmente en nuestra web, vamos a agruparlos en un contenedor. Por lo tanto,
luego del contenedor que actualmente tenemos para la pantalla inicial de nuestra
web, agregaremos:

```html
<body>
  <!-- Contenido previo -->
  <!-- ... -->

  <!-- Contenedor de video -->
  <section>
    <video></video>
  </section>
</body>
```

Para indicarle a la etiqueta `<video></video>` qué video queremos ver, se puede
usar de 2 maneras:

1. A través de un atributo `src` en la etiqueta.
2. Agregando una etiqueta `<source />` dentro de la etiqueda de video.

¿Cuándo usamos qué opción?

Bueno, la primera es usada cuando solo tenemos un formato de video, ya que el
atributo `src` solo se puede definir una vez dentro de la etiqueta. En cambio,
la segunda opción nos permite usar varias etiquetas `<source />` dentro de la
etiqueta video, lo cual nos permite agregar diferente tipos de formato tomando
el orden en que se agregaron como orden para intentar mostra el video.

Empecemos por agregar el video con el atributo `src`:

```html
<body>
  <!-- Contenido previo -->
  <!-- ... -->

  <!-- Contenedor de video -->
  <section>
    <video
      src="https://cdn.videvo.net/videvo_files/video/premium/video0036/small_watermarked/computer_code00_preview.mp4"
    ></video>
  </section>
</body>
```

Esto nos mostrará el video en el navegador, pero, ¿te diste cuenta que no lo
podemos reproducir?


<br/>

[Siguiente](../reto-02/README.md)
