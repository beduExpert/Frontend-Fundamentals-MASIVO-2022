# Reto 01 - Fijando la barra de navegación a la parte superior de la pantalla

## Objetivos
1. Agregar posicionamiento estático a la barra de navegación.
## Requisitos
- Tener instalado Visual Studio Code
- Saber que es responsive design

## Instrucciones

Recuerdas que la barra de navegación tenía un posicionamiento fijo en la parte superior aún y cuando estemos haciendo scroll. ¿Has notado que este comportamiento ya no está presente? ¿Puedes solucionarlo?

:::tip

Al ser este un caso común, Bootstrap tiene clases utilitarias que pueden ayudar
a lograr este comportamiento. Revisa [esta sección de navbar de la documentación](https://getbootstrap.com/docs/5.1/components/navbar/#placement) para que te des una idea de qué podrías usar.

:::

<details>
  <summary>Posible solución</summary>

La clase `fixed-top` de Bootstrap nos ayuda a solucionar este problema:

```html
<nav class="navbar navbar-expand-lg navbar-light fixed-top">
  <!-- Contenido de la barra de navegación -->
</nav>
```

Si bien nuestra barra se posiciona como queremos, al momento de hacer scroll nos
damos cuenta que no tiene un color de fondo porque el texto se mezcla con el
resto del contenido de la página. Para esto, podemos agregarle un color de fondo
a la clase `.navbar` que tenemos declarada en nuestros estilos:

```css
.navbar {
  background-color: #fffbf7;
  text-align: center;
  color: #025157;
  font-weight: 500;
}
```
</details>


<br/>

[Siguiente](../Ejemplo-02/README.md)