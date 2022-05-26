# Reto 05 - Recuperando el contenido de tu NavBar

## Objetivos
1. Aprender cómo modificar los componentes de Bootstrap en cuanto a contenido
2. Estructurar correctamente un componente para que se ajuste a nuestras necesidades

## Requisitos
- Tener Visual Studio Code instalado

## Instrucciones

Cambia el texto usado en el navbar por defecto al contenido que actualmente
tenemos en nuestra página.

<details>
  <summary>Posible solución</summary>

```html
<body>
  <!-- Nuestra barra de navegación comentada va aquí -->
  <nav class="navbar navbar-expand-lg navbar-light" style="background-color: #fffbf7;">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">
        <img src="https://getmatcha.com/wp-content/themes/getmatcha/img/footer_logo.svg" />
      </a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav mx-auto mb-2 mb-lg-0">
          <li class="nav-item">
            <a class="nav-link" aria-current="page" href="#">Platform</a>
          </li>

          <li class="nav-item">
            <a class="nav-link" href="#">Pricing</a>
          </li>

          <li class="nav-item">
            <a class="nav-link" href="#">Customers</a>
          </li>

          <li class="nav-item">
            <a class="nav-link" href="#">Resources</a>
          </li>

          <li class="nav-item">
            <a class="nav-link" href="#">About us</a>
          </li>

        </ul>
        <div class="actions">
          <a href="#">Sign In</a>
          <button>Start Free Trial</button>
        </div>
      </div>
    </div>
  </nav>
  <!-- Nuestro contenido va aquí-->
</body>
```

Viéndose algo como:

![Barra de navegación de Bootstrap con contenido](../assets/bootstrap-default-navbar-with-content.png)

</details>



[Siguiente](../reto-06/README.md)