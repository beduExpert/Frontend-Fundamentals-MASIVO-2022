# Ej. 02 - Transiciones y pseudo-elementos

## Introducción
Las transiciones se utiliza cuando queremos resaltar un elemento. Podríamos hacerlo de manera directa con el evento *:hover*, pero es provoca que el efecto se vea brusco o "duro", mientras que una transición te permite implementar la velocidad de cambio que necesites. Ahora, vamos a insertar nuestra primera transición. Esta la haremos dentro de un elemento de texto, para que veamos cómo funcionan.

### Estados de la transición

El primer estado de la transición que vamos a fijar es el estado "base", es decir, el que tiene el elemento al momento de que es mostrado en pantalla por el navegador.

El segundo estado que utilizaremos es cuando el puntero del ratón pasa por encima del elemento de texto, lo que desencadena un evento en la página que se denomina **hover**. CSS está preparado para detectar este evento, utilizando el selector **:hover** que se aplica a la clase o elemento donde se definen las propiedades base.

---
<br/>

## Objetivos
1. Utilizar transiciones en los elementos `<button>` de la nueva página.
2. Aprender el uso del pseudo selector `:hover`.

---
<br/>

## Desarrollo

Seleccionamos el elemento de texto justo por debajo de las fotografías. Como todos tienen la misma clase, con que hagamos el cambio una sola vez en el código nos permitirá cambiar también los otros dos textos.

::Pro-tip DRY es una filosofía de diseño de software, y es un acrónimo de "Don't Repeat Yourself" (DRY), que indica que el código que escribas debe ser, en lo posible, único en toda la extensión de tu desarrollo. El usar una sola clase para varios elementos que deben tener las mismas propiedades de estilo se ajusta a la filosofía DRY: un solo cambio en el código hace cambios en todos los elementos que tengan esa clase.

```css

.feature__title__anchor {
  text-decoration: none;
  color: inherit;
  font-weight: 500;
  font-size: 24px;

  .feature__title {
    margin-top: 50px;
    font-weight: 500;
    font-size: 24px;
    font-family: 'Open Sans',sans-serif;
    margin-bottom: 35px;
    text-decoration: none;
    text-shadow: #025157 1px 1px 2px;
    transition: color .3s ease-in-out;

      /* Agrega este selector para activar la transición en el evento :hover */
    &:hover {
      color:#67b54b;
    }
  }
}

```

Ahora expliquemos que hace `transition`. 

La propiedad `transition` es un atajo que permite escribir en una sola línea las propiedades siguientes:
- `transition-property`
- `transition-duration`
- `transition-timing-function`
- `transition-delay`

En nuestro caso, `transition: color 0.3s ease-in-out;` 
- Modifica la propiedad **color** del elemento. 
- Con una duración de transición desde el estado base al estado :hover en 0.3 segundos
- Con una curva de velocidad **ease-in-out**, que significa que empieza y termina a una velocidad lenta.

Nuestro elemento de texto debe observarse ahora como:

![Elemento base](../assets/elementoBase.png)

Cuando hacemos *hover* con el ratón y se observa que cambia el color del texto de manera gradual, en un tiempo relativamente corto.

![Elemento con hover](../assets/elementoHover.png)

<br/>

[Siguiente](../reto-02/README.md)