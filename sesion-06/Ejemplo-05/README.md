# Ej. 05 - Agregando una sección de preguntas frecuentes

## Objetivos
1. Utilizar el patrón de diseño básico de Bootstrap
2. Insertar y configurar un nuevo elemento de Bootstrap: Acordeón.

Vamos a agregar una sección de preguntas frecuentes, pero lo haremos en dos columnas y con otro elemento de Bootstrap, el [Acordeón](https://getbootstrap.com/docs/5.1/components/accordion/#example).

Primero, armemos los contenedores, que este es el patrón de diseño básico de Bootstrap.

```html
  <section class="faq">
    <div class="container">
      <div class="row">
        <div class="col">
          <!-- Aqui insertaremos el contenido de la primera columna -->
        </div>
        <div class="col">
          <!-- Aqui insertaremos el contenido de la segunda columna -->
        </div>
      </div>
    </div>
  </section>
```

Segundo, ya con la estructura establecida, armemos el primer acordeón:


```html
  <section class="faq">
    <div class="container">
      <div class="row">
        <div class="col">
          <div class="accordion" id="accordionExample">
            <div class="accordion-item">
              <h2 class="accordion-header" id="headingOne">
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                  data-bs-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                  How can I get started?
                </button>
              </h2>
              <div id="collapseOne" class="accordion-collapse collapse" aria-labelledby="headingOne"
                data-bs-parent="#accordionExample">
                <div class="accordion-body">
                  Getting started is easy! Simply
                  <a href="#">create a free account</a> to start using the Platform and
                  exploring the library. Want to start publishing? When you click the
                  “Publish” button on a piece of licensed content, you’ll be prompted to
                  input your credit card information before continuing. Questions?
                  <a href="#">Reach out to our customer support team for assistance!</a>
                </div>
              </div>
            </div>

            <div class="accordion-item">
              <h2 class="accordion-header" id="headingOne">
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                  data-bs-target="#collapseTwo" aria-expanded="true" aria-controls="collapseOne">
                  What is licensed content?
                </button>
              </h2>
              <div id="collapseTwo" class="accordion-collapse collapse" aria-labelledby="headingOne"
                data-bs-parent="#accordionExample">
                <div class="accordion-body">
                  Licensed content, sometimes called syndicated content, is content
                  produced by a professional publisher that can be legally licensed for
                  use on your own website with no SEO penalty.
                  <a href="#">Learn more</a>. The Matcha library leverages licensed
                  content to provide you with a low-cost supply of professionally
                  written articles that are proven to be engaging. It eliminates the
                  headache and time of producing your own blog articles, allowing you to
                  get back to more pressing matters. When we say, “professional
                  publishers”, we mean it. Currently, our library includes articles from
                  the following publishers: Oxygen Magazine, Better Nutrition, Popular
                  Science, Field & Stream, Coach, RootsRated, Business2Community,
                  MoneyNing, YourMoneyGeek Working Mother, Clean Eating, and Healthy
                  Moms Magazine.
                </div>
              </div>
            </div>

            <div class="accordion-item">
              <h2 class="accordion-header" id="headingOne">
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                  data-bs-target="#collapseThree" aria-expanded="true" aria-controls="collapseOne">
                  What is the Matcha content library?
                </button>
              </h2>
              <div id="collapseThree" class="accordion-collapse collapse" aria-labelledby="headingOne"
                data-bs-parent="#accordionExample">
                <div class="accordion-body">
                  Matcha offers a library of more than 10,000 articles with photography
                  and written by high-quality third-party publishers. You can publish an
                  article from the library to your blog in a matter of minutes. In 2018
                  alone, our articles garnered 8.9 million website visits for our
                  customers. The data shows that readers find the articles engaging and
                  perform as well or better than custom articles. You can see the study
                  <a href="#">here</a>. Every week, we are bringing in hundreds of new
                  articles to our library. Our library publishers include: Oxygen
                  Magazine, Better Nutrition, Popular Science, Field & Stream, Coach,
                  RootsRated, Business2Community, MoneyNing, YourMoneyGeek Working
                  Mother, Clean Eating, and Healthy Moms Magazine.
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="col">
          <!-- Aqui insertaremos el contenido de la segunda columna -->
        </div>
      </div>
    </div>
  </section>
```

Como siempre, debemos considerar estilos para que el contenido se visualice correctamente.

```css
  .faq {
    margin-top: 50px;
    padding-bottom: 120px;
  }

  .faq h2 {
    color: #025157;
    font-family: "Alegreya", serif;
  }

  .faq .card-header {
    background-color: white;
    border-left: 1px solid rgba(0, 0, 0, 0.125);
  }

  .faq h2 > button {
    color: #025157;
    font-size: 28px;
    font-weight: 900;
  }

  .faq .card .card-body a {
    color: #6abf4b;
  }
```

¡Se nota que vamos avanzando!



<br/>

[Siguiente](../reto-05/README.md)