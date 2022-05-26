# Reto 02 - Quitando separación superior del título

## Objetivos

1. Aprender a ocultar elementos no necesarios en ciertas resoluciones.
## Requisitos
- Tener instalado Visual Studio Code.

<br/>

## Instrucciones

Si nos fijamos en la página original, el título no queda tan seeparado del borde
superior, esto se debe a la misma razón que el caso anterior, ¿cómo harías para
mejorar su apariencia?

<br/>

<details>
  <summary>Posible Solución</summary>

```css
@media (max-width: 575px) {
  .navbar,
  .actions {
    display: none;
  }

  main {
    margin-top: 130px;
  }

  h1 {
    font-size: 30px;
  }
}
```

</details>

<br/>

[Siguiente](../Ejemplo-03/README.md)