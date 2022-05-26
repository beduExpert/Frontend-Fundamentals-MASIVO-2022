# Ej. 03 - Agregando segunda columna del blog

## Objetivos
- Utilizar estilos y elementos de Bootstrap.
- Completar la sección Blog de nuestro proyecto.

---
<br/>

## Requisitos
- Tener instalado Visual Studio Code.
- Conocer estilos de Bootstrap.
- Conocer el patrón de diseño de Bootstrap para contenedores.

---
<br/>

## Desarrollo

Para agregar la segunda columna que viene a ser un post del blog, usaremos un
componente de Bootstrap llamado [card](https://getbootstrap.com/docs/4.4/components/card/).
Al igual que en la sesión de frameworks, agarraremos el código de ejemplo como
base y luego iremos modificando. Sin más, empecemos:

```html
<section class="container blog">
  <div class="row">
    <div class="col">
      <!-- Aquí va la columna de descripción -->
    </div>
    <div class="col">
      <div class="card" style="width: 18rem;">
        <img src="..." class="card-img-top" alt="..." />
        <div class="card-body">
          <h5 class="card-title">Card title</h5>
          <p class="card-text">
            Some quick example text to build on the card title and make up the
            bulk of the card's content.
          </p>
          <a href="#" class="btn btn-primary">Go somewhere</a>
        </div>
      </div>
    </div>
    <div class="col"></div>
  </div>
</section>
```

<br/>

Ahora empecemos a cambiar el contenido por lo que necesitamos en la web de
Matcha:

<br/>

<br/>


```html
<section class="container blog">
  <div class="row">
    <div class="col">
      <!-- Aquí va la columna de descripción -->
    </div>
    <div class="col">
      <div class="card">
        <img
          src="https://getmatcha.com/wp-content/uploads/2019/03/david-marcu-114194-1052x699.jpg"
          class="card-img-top"
          alt="Ecommerce Blogging: The 2020 Guide for Online Stores and DTC Brands"
        />
        <div class="card-body">
          <h5 class="card-title">
            Ecommerce Blogging: The 2020 Guide for Online Stores and DTC Brands
          </h5>
          <p class="metadata">
            <strong class="category">Performance Blogging </strong>
            <strong class="read-time">• 21 mins read</strong>
          </p>
          <p class="card-text">
            Table of ContentsWhy Ecommerce Businesses Need a Blog in
            2020Document Your Ecommerce Blog StrategyPublication: How to Create
            High-Performing Blog ContentDistribution:...
            <span class="read-more">+ <a>Read More</a></span>
          </p>
          <div class="author">
            <img
              src="https://secure.gravatar.com/avatar/b1c37d9c6b3a36a5eb64d7112bf71ca4?s=96&d=retro&r=g"
              alt="Shauna Ward"
            />
            <p>Shauna Ward</p>
          </div>
        </div>
      </div>
    </div>
    <div class="col"></div>
  </div>
</section>
```

<br/>

Con esta estructura nuestro post va tomando forma. Ahora es momento de
personalizar su apariencia con cambios en Sass.

<br/>

[Siguiente](../reto-01/README.md)