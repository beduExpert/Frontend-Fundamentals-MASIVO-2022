# Ej. 05 - Haciendo responsive la sección de características principales

## Introducción
No solo los elementos que usan flexbox necesitan cambios para ajustarseal tamaño de la pantalla. También los elementos que usan CSS Grid deben ajustarse para que nuestro diseño sea visible en las pantallas pequeñas o grandes, según queramos que se presente nuestro contenido.
## Objetivo
1. Aplicar técnicas de diseño responsive a elementos con CSS Grid.
## Requisitos
- Tener instalado Visual Studio Code.
- Tener conocimiento de CSS Grid.

## Desarrollo

De momento ya tenemos de manera responsive nuestra portada inicial,
adicionalmente acabamos de cambiar el flujo de nuestra sección publicitaria
que usa Flexbox. La siguiente sección que corresponde a la de publicidad no se
desborda del ancho del dispositivo pero debido a que está estructurada con Grid
CSS, está manteniendo la cantidad de columnas y filas que definimos cuando estaba
en un dispositivo más grande. Para solucionar este problema, es necesario cambiar
la relación de filas y columnas. En este caso, sería bueno mantener cuatro filas
y una columna, para que cada tarjeta vaya debajo una de la otra.

Tomando en consideración la estructura:

```html
<section class="features">
  <article class="feature-card"></article>
  <article class="feature-card"></article>
  <article class="feature-card"></article>
  <article class="feature-card"></article>
</section>
```

Podemos cambiar el CSS para dispositivos pequeños:

```css
@media (max-width: 575px) {
  /** Estilos para la sección principal y de publicidad */
  .features {
    grid-template: repeat(4, 1fr) / 1fr;
  }
}
```

<br/>

Bien, con esto ya logramos posicionar las tarjetas en un flujo vertical, sin
embargo faltan 2 cosas, quitar el espacio a los lados y quitar la imagen que no
es necesaria mostrarla en la experiencia móvil.

<br/>

[Siguiente](./reto-04/README.md)