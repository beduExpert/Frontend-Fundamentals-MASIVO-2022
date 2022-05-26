## Reto 05 - Cambia los colores
## Objetivos
1. Usar propiedades de CSS para dar estilo a varios componentes de texto.
2. Aprender a usar CSS para centrar elementos en la página.

## Desarrollo

Los colores que van a aplicar son los siguientes:

- Texto que va debajo del título: `#46484c`
- Texto promocional: `#8b8b8bcc`
- Texto del botón: `#fff`

<br/>

Ahora te toca buscar en Google, ¿cómo puedes agregar una hoja de estilos a tu proyecto? ¿Qué propiedad usarías para cambiar el color de fondo? ¿Qué selector usarías para cambiar el color de fondo de toda la página?

- Color de fondo de la página: `#fffbf7`
- Color de fondo del botón: `#025157`

<br/>

<details><summary>Posible solución</summary>
<p>

Debes crear un archivo denominado `styles.css`, en la misma carpeta donde encuentras `index.html`. Recuerda usar `touch` para crear este archivo.

Al abrir el archivo con VSCode, observarás que está vacío. Vamos a llenarlo con algunas cosas, según los cambios de color y alineación del texto que necesitas:

```css
        body {
            background-color: #fffbf7;
        }

        h1 {
            color: #46484c;
            text-align: center;
        }

        p {
            color: #8b8b8bcc;
            font-family: verdana;
            font-size: 20px;
        }

        button {
            color: #fff;
            background-color: #025157;
        }
```
Ahora, debemos referenciar la hoja de estilos que está en `styles.css` en nuestro index.html, para que los estilos se apliquen. También debemos borrar la etiqueta `<style>` y su contenido, por lo que el contenido de `<head>` quedará así:

```html
    <head>
        <title>Matcha</title>
        <link rel="stylesheet" href="styles.css">
    </head>
    <body>
        <!-- aqui va el contenido html -->
    </body>
```

¡Listo! Ahora has cambiado con éxito los colores de varios elementos en tu página web.

</p>
</details>

<br/>

[Siguiente](../Ejemplo%2006/README.md)