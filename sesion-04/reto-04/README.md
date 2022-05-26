# Reto 04 - Agregando el contenido de las tarjetas
## Objetivo
- Interpretar la máqueta disponible para incluir los elementos HTML más adecuados para la acción que se requiere en el Front End.
- Generar elementos repetibles de código que puedan ser utilizados en más lugares del código del proyecto.

---
<br/>

## Requisitos
- Tener instalado Visual Studio Code.
- Tener conocimientos de CSS (Flexbox).
- Tener conocimientos de CSS (Grid).

---
<br/>

## Instrucciones

¡Es hora de poner en práctica lo aprendido hasta ahora! Agrega el contenido
interno de cada tarjeta a excepción de la animación que se genera al poner el
mouse sobre la imagen de la derecha de cada tarjeta (si deseas averiguar cómo
lograr ese efecto, genial, solo recuerda que no es la prioridad de este
challenge).

> TIP:
> * Recuerda que puedes obtener el link de las imágenes, inspeccionando la página
  con el Dev Tools del navegador.
> * Para posicionar la imagen de la forma que está en la página, puedes jugar con
  las propiedades de _position_.
> * El contenido interno de las tarjetas pueden ser estructurado con cualquier
  técnica que has conocido hasta el momento, no necesariamente con CSS Grid.

<br/>

<details>
  <summary>Posible Solución</summary>

Esta solución, usa Flexbox para estructurar el contenido interno de las tarjetas
y `position: relative` para lograr la apariencia de la imagen. Recuerda usar las propiedades de default de HTML/CSS. Por ejemplo, puedes utilizar elementos de línea para textos que necesiten un  arreglo en pantalla particular, uno encima del otro. También puedes usar otros estilos como position: absolute o position: relative para que sea más sencillo manipularlo.

Este es el código completo.

```html
<section class="features">
  <article class="feature-card">
    <div class="feature-content">
      <figure>
        <img
          src="https://getmatcha.com/wp-content/themes/getmatcha/img/icon_publish.png"
          alt="Publish icon"
        />
      </figure>
      <h3>Fill your blog with engaging articles.</h3>
      <p>
        Publish to your blog in less time than it takes to drink your
        morning coffee.
      </p>
      <a href="">Publish instantly →</a>
    </div>
    <div class="feature-image">
      <figure>
        <img
          src="https://getmatcha.com/wp-content/themes/getmatcha/img/image_publish.png"
          alt="Publish example"
        />
      </figure>
    </div>
  </article>
  <article class="feature-card">
    <div class="feature-content">
      <figure>
        <img
          src="https://getmatcha.com/wp-content/themes/getmatcha/img/icon_site_traffic.png"
          alt="Site traffic icon"
        />
      </figure>
      <h3>Attract and engage more website visitors.</h3>
      <p>
        Enhance your email, social media channels, and paid ads with content
        from Matcha.
      </p>
      <a href="">Get more site traffic →</a>
    </div>
    <div class="feature-image">
      <figure>
        <img
          src="https://getmatcha.com/wp-content/themes/getmatcha/img/image_site_traffic.png"
          alt="Site traffic example"
        />
      </figure>
    </div>
  </article>
  <article class="feature-card">
    <div class="feature-content">
      <figure>
        <img
          src="https://getmatcha.com/wp-content/themes/getmatcha/img/icon_capture.png"
          alt="Capture icon"
        />
      </figure>
      <h3>Capture more emails with locked content.</h3>
      <p>
        Convert 10x more of your traffic into subscribers and nurture them
        to a sale.
      </p>
      <a href="">Grow your email list faster →</a>
    </div>
    <div class="feature-image">
      <figure>
        <img
          src="https://getmatcha.com/wp-content/themes/getmatcha/img/image_capture.png"
          alt="Capture example"
        />
      </figure>
    </div>
  </article>
  <article class="feature-card">
    <div class="feature-content">
      <figure>
        <img
          src="https://getmatcha.com/wp-content/themes/getmatcha/img/icon_roi.png"
          alt="ROI icon"
        />
      </figure>
      <h3>Optimize your blog’s performance.</h3>
      <p>
        See what content delivers the most traffic, engagement, email
        subscribers, and sales.
      </p>
      <a href="">See content’s ROI →</a>
    </div>
    <div class="feature-image">
      <figure>
        <img
          src="https://getmatcha.com/wp-content/themes/getmatcha/img/image_roi.png"
          alt="ROI example"
        />
      </figure>
    </div>
  </article>
</section>
```

```css
.features {
  background-color: #025157;
  padding: 5% 10%;
  display: grid;
  grid-template: repeat(2, 330px) / repeat(2, 1fr);
}

.features .feature-card {
  margin-bottom: 30px;
  margin-left: 15px;
  margin-right: 15px;
  background-color: #fff;
  border: 1px solid #dadada;
  border-radius: 5px;
  display: flex;
  align-items: center;
  overflow: hidden;
}

.features .feature-card .feature-content {
  padding: 30px 20px 40px 40px;
  flex: 2;
}

.features .feature-card .feature-content > * {
  margin-bottom: 1rem;
  margin-top: 0;
}

.features .feature-card .feature-content img {
  width: 50px;
}

.features .feature-card .feature-content h3 {
  font-size: 24px;
  color: #343434;
  font-weight: 400;
}

.features .feature-card .feature-content p {
  font-size: 16px;
  color: #7e7e7e;
  font-weight: 400;
}

.features .feature-card .feature-content a {
  font-size: 16px;
  color: #67b54b;
  font-weight: 600;
  text-decoration: none;
}

.features .feature-card .feature-image {
  flex: 1;
  width: 40%;
  position: relative;
  right: -50px;
  height: 80%;
}

.features .feature-card .feature-image figure,
.features .feature-card .feature-image img {
  margin-top: 0;
  height: 100%;
}
```

</details>

<br/>

[Siguiente](../postwork/README.md)