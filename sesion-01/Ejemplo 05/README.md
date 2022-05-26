# Ej. 05 - Agregando color al texto principal

## Objetivos
1. Aprender a usar propiedades de CSS para definir estilos.

---
<br/>

## Requisitos
- Tener Visual Studio Code instalado.

---
<br/>

## Instrucciones

La primera propiedad que veremos en CSS será la de `color`, y la usaremos para cambiar
el color de los textos que hemos agregado.

Los valores de los colores pueden ser expresados de diversas maneras, en este
caso usaremos el formato hexadecimal. El texto de la página original usa el
color `#025157`, y este color debemos aplicarlo al elemento `h1`. Como hay muchos elementos HTML dentro de la etiqueta `<body>`, nuestro CSS debe seleccionar el elemento correcto al que le aplicará los estilos que queremos. Para ello, CSS utiliza selectores,
que en nuestro caso será el de la etiqueta `<h1>`. En ese caso, nuestro CSS quedará así:

```html
<head>
  <style>
    h1 {
      color: #025157;
    }
  </style>
  <!-- aqui va el código que hemos escrito -->
</head>
```

Recarga tu navegador para que puedas ver los cambios reflejados. ¡Ahora ya tienes
tu texto con color!

<br/>

[Siguiente](../reto-04/README.md)