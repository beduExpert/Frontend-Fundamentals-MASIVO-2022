# Reto 02. Grid 2 filas con alto de `330px`

## Objetivo
- Configurar el elemento Grid para una altura específica.
- Utilizar las propiedades Grid para acomodar el contenido de manera adecuada.

---
<br/>

## Requisitos
- Tener conocimientos de CSS (Grid)
- Conocer el modelo de caja.
- Tener instalado Visual Studio Code.

---
<br/>

## Instrucciones

Regresa la cantidad de columnas a las que realmente necesitamos (2) y agrega
la cantidad de filas que usaremos (2) teniendo en cuenta que el alto será de
`330px`. Una vez logrado, ¿cómo se te ocurre que podrías usar la unidad de `fr`
para indicar el alto de las filas?

<details>
  <summary>Posible Solución</summary>

```css
.features {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-template-rows: repeat(2, 330px);
}
```

Una forma de poder usar la unidad `fr` para asignar el alto de las filas sería
indicando un tamaño fijo al elemento contenedor, en nuestro caso, podríamos 
hacer:

```css
.features {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  height: 660px;
  grid-template-rows: repeat(2, 1fr);
}
```

</details>


[Siguiente](../reto-03/README.md)