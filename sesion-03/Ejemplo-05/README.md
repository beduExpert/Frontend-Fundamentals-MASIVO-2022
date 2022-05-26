# Ej. 05 - Aplicando `position:fixed`

## Objetivos
- Colocar la barra de navegación siempre en la parte superior mediante CSS.
- Utilizar estilos para ajustar la barra de navegación a los nuevos requerimientos.

---
<br/>

## Requisitos
- Tener Visual Studio Code instalado.
---
<br/>

## Desarrollo

Ya que nuestra barra de navegación tiene estilos y está funcionando, vamos a
envolverla en un contenedor en el cual podamos agregar esta propiedad y así no
realizar muchos cambios a lo que tenemos actualmente.

```html
<body>
  <!-- Este es el contenedor que envuelve a la barra de navegación -->
  <section class="fixed-header">
    <header class="header"></header>
  </section>
  <!-- HTML restante -->
  <!-- ... -->
</body>
```

Una vez agregado el contenedor, procedemos a agregar la propiedad `position` con
valor `fixed`.

```css
.fixed-header {
  position: fixed;
}
```

¿Qué pasó? ¿Viste que nuestra barra de navegación se rompió? No te preocupes,
ahora lo solucionamos, como lo mencionamos anteriormente, se salió del flujo de
la web y por ende se puso en una posición distinta sin importarle el resto de
contenido de la web. Apliquemos las propiedades que nos permiten controlar su
posición:

```css
.fixed-header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
}
```

¡Uff! Con esto ya se ve como antes, ¿pero qué está sucediendo? Las propiedades
que hemos agregado nos permite decirle al navegador dónde queremos que se ubique
el contenido. Primero le decimos que se coloque en la parte superior del
navegador (`top: 0`), luego le pedimos que se coloque al borde izquierdo de la
pantalla (`left: 0`) y por último, para que ocupe todo el ancho de la pantalla,
le decimos que se extienda hasta el borde derecho del navegador (`right: 0`).

¿Has probado hacer scroll? ¡La barra de navegación nos acompaña! Sin embargo,
no se ve bien cuando pasa a través de un contenido, porque se ve como si
estuviera encimado el texto de la barra de navegación :thinking:.

Esto podemos solucionar, poniéndole el mismo color de fondo que tiene todo el
documento, pero solo al contenedor que acabamos de crear:

```css
.fixed-header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  background-color: #fffbf7;
}
```

!Ahora sí! Nuestra barra de navegación quedó fija al borde superior de la
pantalla mientras hacemos scroll y no se encima el contenido. Dependiendo de que
tan observador seas, te podrás haber percatado que el título principal de la
página se subió, esto debido a que la barra de navegación se salió del flujo y
el espacio que ocupaba quedó rezagado, por ende, el título se subió, lo que
podemos hacer es ponerle un margen (o agregarle en caso que lo tenga) del tamaño
que ocupaba la barra de navegación.

Actualmente, nuestro contenido principal, tiene un margen superior de `200px`, y
la barra de navegación tiene un alto de `45px` y adicionalmente cuenta con un
margen superior de `40px`. Por lo que a nuestro contenido principal, deberíamos
de poner ahora un margen superior de `285px` para conservar el aspecto que tenía
antes de volver nuestra barra de navegación fija.

```css
main {
  margin-top: 285px;
  text-align: center;
}
```

<br/>

[Siguiente](../postwork/README.md)