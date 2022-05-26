# Reto 03 - Agregar las dos tarjetas restantes

## Objetivos
1. Concluir la personalización del componente Carrusel
2. Usar el componente Tarjeta para presentar información de casos de éxito del producto.

## REQUISITOS
- Tener Visual Studio Code instalado

## INSTRUCCIONES

- Inserta las otras dos tarjetas, si ya las tienes listas, o constrúyelas leyendo el código en la página de ejemplo.

<details>
  <summary>Posible Solución</summary>

  - Inserta el contenido de la segunda y tercera tarjeta en los elementos `<img src="..." class="d-block w-100" alt="...">` correspondientes.
  - El código ahora debe verse así...

```html

    <article class="col-12 col-md-4 success-stories">
      <div id="carouselExampleIndicators" class="carousel slide" data-bs-ride="carousel">
        <div class="carousel-indicators selectores">
          <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active"
            aria-current="true" aria-label="Slide 1"></button>
          <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1"
            aria-label="Slide 2"></button>
          <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2"
            aria-label="Slide 3"></button>
        </div>
        <div class="carousel-inner">
          <div class="carousel-item active">
            <!-- Tarjeta 1: Everly -->
            <div class="card">
              <img src="https://getmatcha.com/wp-content/uploads/2019/05/profile-headshot-square.png"
                class="card-img-top" alt="Everly">
              <div class="card-body">
                <div class="card-circle everly">
                  <img src="https://getmatcha.com/wp-content/uploads/2019/05/everly_logo_blue_v3_x60@2x.png"
                    alt="Everly">
                </div>
                <h4>Everly</h4>
                <h3>
                  Early-Stage CPG Brand Increases Lead Conversion 20x,
                  Ecommerce Revenue 20%
                </h3>
                <div class="results">
                  <img src="https://getmatcha.com/wp-content/themes/getmatcha/img/icon_cart.png" alt="Cart icon">
                  <p>22% of monthly revenue influenced by content</p>
                </div>
              </div>
              <div class="card-footer">
                <button>See Case Study</button>
              </div>
            </div>
          </div>

          <!-- Tarjeta 2: Sea to Summit -->
          <div class="carousel-item">
            <div class="card">
              <img src="https://getmatcha.com/wp-content/uploads/2019/08/0.jpg" class="card-img-top" alt="Everly">
              <div class="card-body">
                <div class="card-circle summit">
                  <img src="https://getmatcha.com/wp-content/uploads/2019/08/SeatoSummitLogo.png" alt="Summit">
                </div>
                <h4>Sea to Summit</h4>
                <h3>
                  Sea to Summit’s Ecommerce Site Traffic Climbs 189%, New
                  Subscribers 820%
                </h3>
                <div class="results">
                  <img src="https://getmatcha.com/wp-content/themes/getmatcha/img/icon_target.png" alt="Cart icon">
                  <p>+327% more popup conversions at a 60% lower cost</p>
                </div>
              </div>
              <div class="card-footer">
                <button>See Case Study</button>
              </div>
            </div>
          </div>

          <!-- Tarjeta 3: Mambe -->
          <div class="carousel-item">
            <div class="card">
              <img src="https://getmatcha.com/wp-content/uploads/2019/06/matt-and-margaret_headshot.png"
                class="card-img-top" alt="Everly">
              <div class="card-body">
                <div class="card-circle mambe">
                  <img src="https://getmatcha.com/wp-content/uploads/2019/06/mambe-logo-1.png" alt="Mambe">
                </div>
                <h4>Mambe Waterproof Blankets</h4>
                <h3>
                  How Mambe Increased Conversions by 327%, Reduced CPL by 60%
                </h3>
                <div class="results">
                  <img src="https://getmatcha.com/wp-content/themes/getmatcha/img/icon_target.png" alt="Cart icon">
                  <p>+327% more popup conversions at a 60% lower cost</p>
                </div>
              </div>
              <div class="card-footer">
                <button>See Case Study</button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </article>

```
Y los estilos de CSS quedarían así, agregando las modificaciones de las dos tarjetas.

  ```css

    .success-stories .card .card-body .card-circle.everly {
      background-color: #f9da73;
      border: 5px solid #f9da73;
    }

    .success-stories .card .card-body .card-circle.summit {
      background-color: #81d742;
      border: 5px solid #81d742;
    }

    .success-stories .card .card-body .card-circle.mambe {
      background-color: #ef7179;
      border: 5px solid #ef7179;
    }

    .success-stories .card .card-body .card-circle.everly img,
    .success-stories .card .card-body .card-circle.summit img,
    .success-stories .card .card-body .card-circle.mambe img {
      object-fit: contain;
      width: 100%;
    }
  ```

</details>

<br/>

[Siguiente](../Ejemplo-03/README.md)
