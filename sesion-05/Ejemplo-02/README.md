# Ej. 02 - Ocultando la barra de navegación en móviles

## Introducción
Debemos usar algunos "trucos" al momento de ajustar nuestro contenido a pantallas de distintos tamaños, ya que no todo el contenido se ajusta bien en una pantalla pequeña. Aprenderemos en esta sección como usar los media queries y otras técnicas.

## Objetivos

1. Aprender a utilizar media-queries en CSS.
## Requisitos
1. Tener instalado Visual Studio Code.

## Desarrollo

Lo primero que podemos notar es que nuestra barra de navegación se distorsiona
y termina viéndose mal, debido a muchos factores, tal vez el más importante que
es mucho contenido para el tamaño de nuestros dispositivos. ¿Qué tal si lo
ocultamos para que no se puedan visualizar mientras estemos en dispositivos
móviles?

## Concepto: Media queries

Una forma de agregar condiciones de estilos en base a tamaño de dispositovos es
a través de la característica de CSS llamada `media queries`. Esta característica
nos permite sobreescribir diferentes estilos en base a condiciones (breakpoints)
que nosotros podemos definir.

Veamos un ejemplo de la sintaxis:

```css
@media (breakpoint) {
  /** Aplica estilos particulares para este tamaño */
}
```

Los breakpoints son las condiciones que nosotros establecemos, normalmente en
base al ancho de un dispositivo, también se pueden agrupar un conjunto de
condiciones en un mismo _media query_.

```css
@media (max-width: 575px) {
  body {
    background-color: yellow;
  }
}
```

En el ejemplo estamos diciendo que todos los dispositivos que tengan un ancho
máximo de `575px` tendrá un color de fondo amarillo, si puebas esto en tu
proyecto, verás que en una vista móvil el fondo será amarilla, pero si sales del
emulador, tu página volverá a tener el colo de fondo que tenía antes. Este es el
pode que los _media queries_ te dan. Nosotros trabajaremos con los siguientes
breakpoints para personalizar nuestros estilos:

```css
/** dispositivos móviles en vista viewport (vertical) */
@media (max-width: 575px) {
  ...;
}

/** dispositivos pequeños en vista landscape (horizontal) */
@media (min-width: 576px and max-width: 767px) {
  ...;
}

/** dispositivos medianos (tablets) */
@media (min-width: 768px and max-width: 991px) {
  ...;
}

/** dispositivos grandes (desktops) */
@media (min-width: 992px and max-width: 1199px) {
  ...;
}

/** dispositivos extra grandes (monitores grandes, tvs) */
@media (min-width: 1200px) {
  ...;
}
```

### Ocultando menú de navegación

Ahora que ya sabemos que los _media queries_ nos ayudarán a lograr esto,
pongámoslo en práctica. Primero debemos identificar qué selector usar para
encontrar solo el menú de navegación, ya que el logo si se logra visualizar
correctamente.

En la estructura que seguimos en el ejemplo, encontramos lo siguiente:

```html
<section class="fixed-header">
  <header class="header">
    <a href="/" class="logo">
      <img
        src="https://getmatcha.com/wp-content/themes/getmatcha/img/footer_logo.svg"
        alt="Matcha"
      />
    </a>
    <nav class="navbar">
      <ul class="menu">
        <li class="menu-item">Platform</li>
        <li class="menu-item">Pricing</li>
        <li class="menu-item">Customers</li>
        <li class="menu-item">Resources</li>
        <li class="menu-item">About</li>
      </ul>
    </nav>
    <div class="actions">
      <a>Sign In</a>
      <button>Start free trial</button>
    </div>
  </header>
</section>
```

Para este caso, el contenido a ocultar son los que podemos acceder a través
de `.navbar` y `.actions`. Procedamos a cambiar su display.

```css
@media (max-width: 575px) {
  .navbar,
  .actions {
    display: none;
  }
}
```

!Gran trabajo! Ya hemos ocultado nuestro menú de navegación manteniendo el logo
visible, y ya no se ve tan mal dicha sección. En la siguiente sesión veremos
como recuperar este contenido con una experiencia diferente.

<br/>

[Siguiente](../reto-01/README.md)