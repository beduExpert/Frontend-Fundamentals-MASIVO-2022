# Ej. 02 - Agregando un carrusel

## Objetivo
1. Configurar en nuestro proyecto uno de los elementos más populares de esta librería: el carrusel.

## Requisitos
- Tener instalado Visual Studio Code.

## Desarrollo
Vamos a insertar un carrousel en nuestra sección de historias de éxito, y crearemos unas nuevas tarjetas dentro del carrusel. También ajustaremos algunas clases con Bootstrap para mejorar la respuesta en pantallas pequeñas.

Primero, observa cómo la documentación nos indica qué cosas componen nuestro [carrusel](https://getbootstrap.com/docs/5.1/components/carousel/). El tipo de carrusel que insertaremos en el proyecto es el denominado "[with indicators](https://getbootstrap.com/docs/5.1/components/carousel/#with-indicators)".

Primer paso: vamos a comentar el código previo. Este es el que habías propuesto para una de las tarjetas de historias de éxito.

```html
<article class="stories-carousel">
  <!-- <div class="card">
    <div class="card-media">
      <figure>
        <img
          src="https://getmatcha.com/wp-content/uploads/2019/05/profile-headshot-square.png"
          alt="Everly worker"
        />
      </figure>
      <div class="company">
        <img
          src="https://getmatcha.com/wp-content/uploads/2019/05/everly_logo_blue_v3_x60@2x.png"
          alt="Everly"
        />
      </div>
    </div>
    <div class="card-body">
      <h4>Everly</h4>
      <h3>
        Early-Stage CPG Brand Increases Lead Conversion 20x, Ecommerce
        Revenue 20%
      </h3>
      <div class="results">
        <img
          src="https://getmatcha.com/wp-content/themes/getmatcha/img/icon_cart.png"
          alt="Cart icon"
        />
        <p>22% of monthly revenue influenced by content</p>
      </div>
    </div>
    <div class="card-footer">
      <button>See Case Study</button>
    </div>
  </div> -->
</article>
```
Segundo: agrega el código del carrusel que copiaste de la documentación de Bootstrap, dentro de la etiqueta `<article>`, y en este punto agregaremos unas clases de Bootstrap a la sección, lo que nos permitirá mejorar la interacción en pantallas pequeñas.

```html
<section class="card-container">
    <div class="container">
      <div class="row p-2">
        <!-- Agrega estas clases de Bootstrap -->
        <article class="col-12 col-md-8 comments">
          <!-- Este es el contenido de texto de esta sección-->
        </article>

        <!-- Agrega estas clases de Bootstrap -->
        <article class="col-12 col-md-4 success-stories">
          <!-- Aqui insertamos el carrusel -->
          <div id="carouselExampleIndicators" class="carousel slide" data-bs-ride="carousel">
            <div class="carousel-indicators">
              <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
              <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1" aria-label="Slide 2"></button>
              <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2" aria-label="Slide 3"></button>
            </div>
            <div class="carousel-inner">
              <div class="carousel-item active">
                <img src="..." class="d-block w-100" alt="...">
              </div>
              <div class="carousel-item">
                <img src="..." class="d-block w-100" alt="...">
              </div>
              <div class="carousel-item">
                <img src="..." class="d-block w-100" alt="...">
              </div>
            </div>
            <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="prev">
              <span class="carousel-control-prev-icon" aria-hidden="true"></span>
              <span class="visually-hidden">Previous</span>
            </button>
            <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="next">
              <span class="carousel-control-next-icon" aria-hidden="true"></span>
              <span class="visually-hidden">Next</span>
            </button>
          </div>
        </article>
      </div>
    </div>
  </section>
```

Buscando entender el contenido del HTML de Bootstrap para este carrusel, podemos comentar algunas cosas sobre este código:

**1.** Tres elementos `<button>` dentro del `<div class="carousel-indicators">`. Estos son los
indicadores (líneas) que nos muestran en qué sección estamos por el momento y cuántas secciones hay dentro del carrusel.

**2.** Encontramos `<div class="carousel-inner">` que contiene 3 divs con clase `carousel-item`. Estos `<div>` contienen cada uno de los elementos que queremos mostrar en nuestra página (en este caso las
etiquetas `<img />`). Por esa razón, este es el lugar perfecto donde insertaremos las tarjetas.

**3.** Dos `<button>` que representan las flechas que
se sobreponen sobre los elementos del carousel para controlar manualmente si
queremos avanzar o retroceder en el carousel. Estos no los vamos a usar, así que puedes eliminarlos del código.

<br/>

[Siguiente](../reto-02/README.md)