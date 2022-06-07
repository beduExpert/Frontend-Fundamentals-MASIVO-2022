# Ej. 02 - Agregando un carrusel

## Objetivo
- Configurar en nuestro proyecto uno de los elementos más populares de esta librería: el carrusel.

## Requisitos
- Tener instalado Visual Studio Code.

## Desarrollo
Vamos a insertar un carrousel en nuestra sección de historias de éxito, y crearemos unas nuevas tarjetas dentro del carrusel. También ajustaremos algunas clases con Bootstrap para mejorar la respuesta en pantallas pequeñas.

Primero, observa cómo la documentación nos indica qué cosas componen nuestro [carrusel](https://getbootstrap.com/docs/5.1/components/carousel/). El tipo de carrusel que insertaremos en el proyecto es el denominado "[with indicators](https://getbootstrap.com/docs/5.1/components/carousel/#with-indicators)".

Primero agrega la sección de historias de éxito:

```html
<section class="success-stories">
  <article class="overview">
    <h2>Growing ecommerce brands rely on Matcha.</h2>
    <p>
      Are you tired of wasting time publishing blog articles to only see a
      trickle of traffic and no impact on sales? Join hundreds of business
      owners and ecommerce marketers who rely on Matcha for quality content
      and consistent performance from their blogs.
    </p>
    <button>
      Who Uses Matcha?
    </button>
    <figure>
      <img src="https://getmatcha.com/wp-content/uploads/2019/09/brands_group.png" alt="Brands">
    </figure>
  </article>
  <article class="stories-carousel">
  </article>
</section>
```

```css
.success-stories {
  background-color: #a1d683;
  padding: 5% 15%;
  display: flex;
  align-items: center;
  justify-content: space-around;
}

.success-stories .overview {
  flex: 2;
  padding-right: 100px;
}

.success-stories .overview h2 {
  font-family: "Alegreya", serif;
  font-size: 51px;
  line-height: 61px;
  color: #025157;
}

.success-stories .overview p {
  color: #343434;
  font-size: 18px;
  line-height: 1.5;
  margin-bottom: 1rem;
}

.success-stories .overview button {
  font-size: 14px;
  padding: 12px 12px 6px 12px;
  border-radius: 8px;
  height: 45px;
  font-weight: 600;
  margin-left: 0;
}

.success-stories .overview img {
  width: 500px;
  max-width: 100%;
}
```

Segundo agrega el código del carrusel que copiaste de la documentación de Bootstrap, dentro de `<article class="stories-carousel">`, y en este punto agregaremos unas clases de Bootstrap a la sección, lo que nos permitirá mejorar la interacción en pantallas pequeñas.

```html
<section class="card-container">
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