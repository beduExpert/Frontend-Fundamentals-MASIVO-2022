# Reto 01 - Cambiando la fuente de nuestro título principal

## Objetivos
1. Adaptar contenido de texto a una pantalla más pequeña.
## Requisitos
- Tener Git Bash si usas Windows.
- Tener conocimientos básicos de CSS (Flexbox)
- Tener conocimientos básicos de CSS (Grid)

<br/>

## Instrucciones

El título de nuestra página está tomando demasiado espacio y no se ve bien, esto
se debe a que tiene una fuente fija de `60px` para el ejemplo que usamos en esta
guía. ¿Cómo harías para cambiarle de fuente a una que funcione mejor? 

<br/>

> Nota: En nuestro caso, terminaremos usando una fuente de 30px pero puedes usar el tamaño que prefieras.

<br/>

<details>
  <summary>Posible Solución</summary>

```css
@media (max-width: 575px) {
  .navbar,
  .actions {
    display: none;
  }

  h1 {
    font-size: 30px;
  }
}
```

</details>

<br/>

[Siguiente](../reto-02/README.md)