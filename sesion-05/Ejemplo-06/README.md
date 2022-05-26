# Ej. 06 - Configurando Bootstrap al proyecto

## Introducción
Ahora que ya hemos manejado los elementos de CSS que nos ayudan a obtener un diseño responsive, ahora instalaremos en nuestro proyecto el CSS framework que se llama Bootstrap, uno de los más sencillos de aprender y aplicar a nuestros proyectos.

## Objetivo
1. Instalar y configurar Bootstrap en nuestro proyecto
2. Agregar el código necesario en nuestro proyecto para usar los elementos de CSS de Bootstrap.

## Requisitos
- Tener instalado Visual Studio Code.

## Desarrollo

Para usar un framework, es necesario agregarlo a nuestro proyecto. En el caso de Bootstrap, podemos descargarlo y configurarlo dentro de nuestro proyecto, aunque recientemente los desarrolladores de Bootstrap ofrecen la modalidad de importar los estilos desde la nube a través de CDN's. (Aquí encuentras una explicación de lo que es un [CDN](https://developer.mozilla.org/es/docs/Glossary/CDN)).

La forma mas directa de agregar Boostrap es a través de links externos que hacen referencia
a un archivo de CSS y algunos archivos de **JavaScript**. Este término puede que
sea nuevo o tal vez lo recuerdes desde el prework de la primera sesión. En
cualquier caso, JavaScript es el único lenguaje de programación que el navegador
soporta nativamente, y es el lenguaje que nos permite agregar interacción y
funcionalidad a nuestra web. En este curso, no estaremos programando en
JavaScript, pero lo usaremos a través del framework sin que nosotros necesariamente tengamos que programar en ese lenguaje.

Empecemos agregando solo el CSS, para esto, debemos ingresar a la sección de
[empezar con Bootstrap](https://getbootstrap.com/docs/5.1/getting-started/introduction/#css),
en el apartado de `CSS` encontraremos una etiqueta `<link />` con una sintaxis similar a la que nosotros usamos para indicarle a nuestro HTML dónde encontrar los estilos de nuestra web. Vamos a copiar toda esa línea de código y la vamos a pegar en nuestro `index.html`. El orden en la cual lo peguemos es importante. Ya que `CSS` es un lenguaje **en-cascada**, en caso de que los nombres de clase se repitan en alguna de las hojas de estilos, la última hoja declarada siempre es la de mayor importancia. Por ello Bootstrap recomienda que su hoja de estilos sea siempre la primera en declararse en el HTML, y que nuestra hoja de estilos sea la última declarada. Así, si se repite un nombre de clase, los estilos que prevalecerán serán los que nosotros definamos en el proyecto.

Por lo tanto, nosotros queremos aprovechar la mayoría de estilos que Bootstrap nos trae consigo (alineación, espaciado, agrupación de elementos), pero en caso de que algo no esté alineado con nuestro diseño, lo deberemos personalizarlo.

Para nuestro proyecto actual, pondremos primero el `<link />` de Bootstrap seguido por el nuestro, quedando algo como:

```html
<head>
  <!-- Aquí van las otras etiquetas del head -->
  <link
    rel="stylesheet"
    href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css"
    integrity="sha384-Vkoo8x4CGsO3+Hhxv8T/Q5PaXtkKtu6ug5TOeNV6gBiFeWPGFN9MuhOf23Q9Ifjh"
    crossorigin="anonymous"
  />
  <link rel="stylesheet" type="text/css" href="./styles.css" />
</head>
```

[Siguiente](../Ejemplo-07/README.md)
