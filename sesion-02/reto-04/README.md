# Reto 04 - Agregando estilos restantes
## Objetivos
- Agregar clases y estilos a la barra de navegación.
- Subir los cambios a GitHub

---
<br/>

## Requisitos
- Tener Git Bash si usas Windows.

---
<br/>

## Instrucciones

A continuación completa los siguientes requerimientos:

1. Todos los textos dentro de la barra de navegación deben usar la fuente
   `sans-serif` y el alto de la barra debe ser de `45px`.
2. El texto del menú de navegación debe tener una separación a los costados de
   `25px`, además debe ser del color `#025157`.
3. El tamaño de fuente para las acciones debe ser de `14px` y cada una de las
   acciones debe tener una separación hacia los lados de `10px`. El color del
   texto `Sign In` debe ser `#67b54b` y el botón de `Start free trial` debe tener
   color de texto blanco, color de fondo `#67b54b`, un  relleno de `14px` hacia
   los costados y `12px` en la parte inferior y superior. Por último el botón
   no debe tener borde, pero un radio de borde de `5px` para tener esquinas
   redondeadas.

<br/>

<details>
  <summary>Posible solución</summary>

  ### Posible solución

  ```css
  .header {
    margin-top: 40px;
    margin-left: 20px;
    margin-right: 20px;
    font-size: 0;
    height: 45px;
    font-family: sans-serif;
  }

  .navbar {
    width: 70%;
    text-align: center;
    color: #025157;
  }

  .menu-item {
    display: inline;
    margin-right: 25px;
    margin-left: 25px;
  }

  .actions {
    width: 15%;
    text-align: right;
    font-size: 14px;
  }

  .actions > * {
    margin-right: 10px;
    margin-left: 10px;
  }

  .actions a {
    color: #67b54b;
  }

  .actions button {
    color: white;
    background-color: #67b54b;
    padding-left: 14px;
    padding-right: 14px;
    padding-top: 12px;
    padding-bottom: 12px;
    border: 0;
    border-radius: 5px;
  }
  ```
</details>

<br/>

No olvides subir tus cambios a Github y revisar que se vean los cambios reflejados en tu página alojada en GitHub Pages.

<br/>

[Postwork](../postwork/README.md)
