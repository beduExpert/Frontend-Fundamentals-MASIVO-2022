# Reto 02 - Aplica el margen utilizando el atajo de la propiedad `margin`
## Objetivos
- Utilizar las propiedades abreviadas ("shortcuts") de margen.

---
<br/>

## Requisitos
- Tener Git Bash si usas Windows.
- Tener conocimientos básicos de HTML y CSS

---
<br/>

## Instrucciones

¿Sabías que la propiedad `margin` puede asignar el valor de los 4 lados en una
sola línea? Si es la primera vez que escuchas esto, no dudes en _googleaerlo_ y
experimentar cambiando las 3 propiedades que hemos escrito previamente por una
sola. Luego imagina, pregunta e investiga que otras propiedades tienen el mismo
atajo.

<br/>

El contenido que agregamos en la sesión anterior también tiene una separación de
la barra de navegación. Esto podríamos solucionarlo agregando un margen a la
primera etiqueta de nuestro contenido (que sería el `h1`), sin embargo, esto no
sería óptimo porque si en algún momento insertáramos algo antes del `h1` nuestro
margen no funcionaría como deseamos. Para evitar esto, podemos usar un contenedor
que englobe a todo nuestro contenido y aplicar el margen a dicho contenedor.


<br/>

<details><summary>Posible solución</summary>

```html

<!-- Aquí va la barra de navegación -->
 <section class="main">
    <h1>Build your blog. Build your business.</h1>

    <h4>Instantly publish articles, drive more traffic, grow your email list, and see your blog’s impact on sales.</h4>

    <form>
      <input type="email">
      <button type="submit" class="texto-boton">
        Try it now &rarr;
      </button>
    </form>

    <p class="texto-promocional">Start publishing today with a <strong>free 7-day trial.</strong></p>
    <p class="texto-promocional"><strong>No credit card</strong> required.</p>

    <img src="https://getmatcha.com/wp-content/themes/getmatcha/img/capterra.png" alt="Captcha de Capterra">
  </section>

```

<br/>

Ahora agregaremos el CSS que necesitamos.
<br/>
Para nuestro `<header>`, una clase `.header`. Nota que estamos usando una versión abreviada (atajo) de la propiedad `margin`, ahora de tres números:

```css
    .header {
        margin: 40px 20px 0;
        font-size: 0;
    }
```
<br/>

Este es el estilo y margen para el contenedor `<section>` con clase `.main`:

```css
    .main {
    margin-top: 140px;
    text-align: center;
    }
```

Con este cambio en el CSS, así como incorporando un **contenedor** en nuestra sección inicial, logramos un mejor control de nuestros elementos en pantalla.

</details>

<br/>

[Siguiente](../reto-03/README.md)