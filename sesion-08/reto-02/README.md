# Reto 02 - Agregando otra transición a la actual

## Objetivos
1. Agregar una transición adicional a la vigente
2. Aprender la secuencia de propiedades que permite tener más de una transición en un elemento.

---
<br/>

## Requisitos
- Tener Visual Studio Code instalado

---
<br/>

## Instrucciones


¡Genial! Ahora que ya hemos visto como modificar el color del texto, el reto consiste en que cambies la transición para que ahora logres hacer un cambio de color y un cambio de tamaño del texto, para que resalte todavía más nuestro elemento. Ambas transiciones deben tener un timing diferente. Investiga en Google o en [w3schools](https://www.w3schools.com/css/css3_transitions.asp) por si necesitas algunos tips.

<br/>

<details>
  <summary>Posible solución</summary>

  <br/>

La solución consiste en agregar a la propiedad `transition` la propiedad que necesitamos modificar.

Vamos a agregar esas propiedades extra en nuestro código:

```css
  .feature__title {
    margin-top: 50px;
    font-weight: 500;
    font-size: 24px;
    font-family: 'Open Sans',sans-serif;
    margin-bottom: 35px;
    text-decoration: none;
    text-shadow: #025157 1px 1px 2px;
    transition: color .3s ease-in-out;

    &:hover {
      color:#67b54b;
    }
  }
```

::Pro-tip ¿Puedes agregar más transiciones en una sola línea? Intenta hacerlo con más propiedades en la línea de `transition`, pero puedes usar `transition: all ...` si el intervalo de tiempo es el mismo para todas las transiciones.

<br/>
</details>

<br/>

[Siguiente](../reto-03/README.md)