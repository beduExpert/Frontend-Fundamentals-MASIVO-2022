# Reto 01 - Etiquetas semánticas para barra de navegación
## Objetivos
- Utilizar etiquetas semánticas en la barra de navegación.
- Agregar los estilos correctos para ajustar el posicionamiento de la barra de navegación.

---
<br/>

### REQUISITOS
- Tener conocimientos básicos de HTML y CSS

---
<br/>

### INSTRUCCIONES

Viendo la barra de navegación del sitio original de [Matcha](https://getmatcha.com),
¿qué etiquetas semánticas consideras que serían buenas usar?

Tomando en cuenta el contenido actual de nuestra web, ¿consideras bueno que se
ponga dentro de un contenedor? Si tu respuesta es positiva, ¿qué contenedor
semántico usarías?

<br/>

Teniendo en cuenta lo siguiente:

- El link de la imagen del logo es: `https://getmatcha.com/wp-content/themes/getmatcha/img/footer_logo.svg`
- El menú de navegación se puede lograr con una lista desordenada que en HTML se
  representa a través de la etiqueta [`<ul></ul>`](https://developer.mozilla.org/es/docs/Web/HTML/Elemento/ul).
- La acción `Sign In` es un link que apunta a la dirección `/login` y la acción
  de `Start free trial` es un botón.

¿Cómo agregarías el contenido de la barra de navegación?

> Ten en cuenta que no se verá igual que la página, y eso está bien, ya que nos
> estamos enfocando solo en la estructura y luego le daremos los estilos
> necesarios para darle la apariencia esperada.

<br/>

<details><summary>Posible solución</summary>
<p>

```html

<header class="header">
  <!-- Logo con link a la página principal -->
  <a href="/">
    <img src="https://getmatcha.com/wp-content/themes/getmatcha/img/footer_logo.svg" alt="Matcha"/>
  </a>
  <!-- Menú de navegación -->
  <nav>
    <ul>
      <li>Platform</li>
      <li>Pricing</li>
      <li>Customers</li>
      <li>Resources</li>
      <li>About</li>
    </ul>
  </nav>
  <!-- Contenedor de acciones de usuario -->
  <div>
    <a>Sign In</a>
    <button>Start free trial</button>
  </div>
</header>

```

</p>
</details>

<br/>

### NOTA:
Vemos que la barra de navegación en la página original no está pegada al borde superior del navegador. En cambio, esta se encuentra a una distancia fija y el contenido de igual manera se encuentra a una distancia específica de la barra de navegación.

Para agregar este tipo de espaciados, podemos usar la propiedad margin, que nos permite poner un margen de separación entre elementos, ya sea en cualquiera de los 4 lados de la caja (arriba, derecha, abajo e izquierda).

Para el caso de la barra de navegación agregaremos un margen superior de 40px y un margen a cada lado de 20px. Ya que este margen queremos dárselo a toda la barra, se lo aplicaremos al elemento header. Para evitar que en caso agreguemos algún otro header en alguna sección de la página, vamos a agregarle un atributo de clase a la etiqueta header y aplicar el estilo a dicha etiqueta a través del selector de clase:

```html
<header class="header">
  <!-- Contenido del header -->
</header>
```

```css
.header {
  margin-top: 40px;
  margin-left: 20px;
  margin-right: 20px;
}
```

[Siguiente](../Ejemplo%2002/README.md)