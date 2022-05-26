# Reto 03.  Grid con 2 filas y 2 columnas
## Objetivos
- Definir con Grid un arreglo bidimensional.
- Utilizar las propiedades CSS correctas para lograr una arreglo de filas y columnas.

---
<br/>

## Requisitos
- Tener conocimientos de CSS (Grid).
- Conocer el modelo de caja.
- Tener instalado Visual Studio Code.


---
<br/>

## Instrucciones

Como en la mayoría de propiedades de CSS, existen muchos atajos para poner
propiedades relacionadas en una sola. Las columnas y filas de CSS Grid no son la
excepción, por lo cual, este reto consiste en obtener el mismo resultado de las
columnas y filas del grid usando la propiedad de atajo.


<details>
  <summary>Posible Solución</summary>

```css
.features {
  display: grid;
  grid-template: repeat(2, 1fr) / repeat(2, 330px);
}
```

</details>


<br/>

[Siguiente](../reto-04/README.md)