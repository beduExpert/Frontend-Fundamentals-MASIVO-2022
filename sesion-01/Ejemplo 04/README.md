# Ej. 04 - Agregando un formulario

## Objetivos
1. Aprender a usar elementos interactivos de un formulario de HTML: `<input>`

---
<br/>

## Requisitos
- Tener Visual Studio Code instalado.

---
<br/>

## Instrucciones

Los formularios en HTML hacen uso de etiquetas particulares para denotar el tipo
de _control_ (caja de texto, botones, etc) que se va a usar en el formulario.

La mayoría de cajas de texto se definen con la etiqueta `<input />` y su
comportamiento por defecto depende del uso del valor de un atributo, llamado
`type`. Esta etiqueta no lleva contenido dentro de la misma, por lo que la
manera de cerrar la etiqueta es automática usando `/>` en vez de `</input>`.

El `input` más común usado en los formularios es:

```html
<input type="text" />
```

Usando este tipo de _input_, la web mostrará una caja de texto que permitirá
ingresar cualquier tipo de texto (números, letras, caracteres especiales, etc),
mientras que usando otros tipos podemos agregar algunas validaciones por defecto
que tenga el navegador. En este formulario, tenemos necesitamos obtener un
correo electrónico del usuario. Para este caso, usaremos el tipo `email`.

```html
<input type="email" />
```

Para terminar el formulario necesitamos agregar un botón, y eso lo logramos a
través de la etiqueta `<button></button>`. Debido a que el texto del botón se
pone entre las etiquetas, el cerrado de la etiqueta no es automático. Además del
texto es importante indicar el tipo de acción que realizará cuando se le de
click al botón. En este caso queremos que el formulario envíe el correo que el
usuario ingresa y por ende el tipo de botón a usar es `submit`.

Un detalle importante es que los controles de formulario deben estar
dentro de una etiqueta `<form></form>`. Nuestro HTML del formulario quedaría así:

```html
<body>
  <!-- Aquí va el código anterior-->
  <form>
    <input type="email" />
    <button type="submit">
      Try it now &rarr;
    </button>
  </form>
</body>
```

Este formulario por si solo no hará ninguna acción, por el momento solo
dejaremos que esté visible, la funcionalidad la dejaremos para después.

<br/>

[Siguiente](../reto-03/README.md)