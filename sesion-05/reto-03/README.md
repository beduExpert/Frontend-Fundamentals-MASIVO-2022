# Reto 03 - Cambiando el flujo del formulario de registro en la sección de publicidad

## Objetivo
1. Usar Flexbox para controlar la orientación y acomodo del contenido.

## Requisitos
- Tener instalado Visual Studio Code

<br/>

## Instrucciones

El formulario está siendo desbordado debido a que está alineado en un flujo 
horizontal (`row`), para mejorar esta experiencia es necesario volverlo vertical.
¿Cómo hacemos?

<br/>

> TIP: El contenedor del formulario usa Flexbox.

<br/>

<details>
  <summary>Posible Solución</summary>

```css
@media (max-width: 575px) {
  .publish > form {
    flex-direction: column;
  }

  .publish > form > div {
    height: 50px;
    margin-top: 10px;
  }

  .publish > form > div > input {
    width: 65%;
  }
}
```

Adicionalmente agregamos algunos estilos para mejorar la apariencia y ancho de
nuestro formulario.

</details>

<br/>

[Siguiente](../Ejemplo-04/README.md)