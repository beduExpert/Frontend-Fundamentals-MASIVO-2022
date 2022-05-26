# Grid con 3 columnas iguales

## Objetivo
- Utilizar las propiedades CSS para definir columnas con Grid.
## Requisitos
- Tener instalado Visual Studio Code
- Tener conocimientos de CSS (Grid)

## Instrucciones

Queremos indicar que nuestra grid va a contener 3 columnas del mismo ancho
relativo al espacio disponible en la pantalla. ¿Cómo lo lograrías usando la
función `repeat(cantidad, tamaño)`?

<details>
  <summary>Posible Solución</summary>

```css
.features {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
```

</details>
<br/>

[Siguiente](../reto-02/README.md)