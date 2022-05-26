# Ej. 07 - Agregando una navbar al proyecto

## Introducción
Los elementos de Bootstrap (componentes) son muy sencillos de utilizar, y agilizan en mucho la construcción de una página web. Aprenderemos cómo utilizar uno de los componentes más utilizados por los desarrolladores.

## Objetivo

1. Utilizar Bootstrap para insertar componentes prediseñados y reutilizables.

## Requisitos
- Tener instalado Visual Studio Code

## Desarrollo

Comencemos por comentar la barra de navegación que actualmente tenemos para
evitar que se mezcle con la barra de navegación de Bootstrap.

```html
<body>
  <!-- Esto es lo que se verá en el navegador web -->
  <!-- <section class="fixed-header">
    <header class="header">
      <a href="/" class="logo">
        <img
          src="https://getmatcha.com/wp-content/themes/getmatcha/img/footer_logo.svg"
          alt="Matcha"
        />
      </a>
      <nav class="navbar">
        <ul class="menu">
          <li class="menu-item">Platform</li>
          <li class="menu-item">Pricing</li>
          <li class="menu-item">Customers</li>
          <li class="menu-item">Resources</li>
          <li class="menu-item">About</li>
        </ul>
      </nav>
      <div class="actions">
        <a>Sign In</a>
        <button>Start free trial</button>
      </div>
    </header>
  </section> -->
</body>
```

Ahora, agregaremos [barra de navegación de ejemplo](https://getbootstrap.com/docs/5.1/components/navbar/#supported-content)
que nos da Bootstrap y la modificaremos a lo que nosotros necesitamos:

```html
<body>
  <!-- Nuestra barra de navegación comentada va aquí -->
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">Navbar</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
          <li class="nav-item">
            <a class="nav-link active" aria-current="page" href="#">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Link</a>
          </li>
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">
              Dropdown
            </a>
            <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
              <li><a class="dropdown-item" href="#">Action</a></li>
              <li><a class="dropdown-item" href="#">Another action</a></li>
              <li><hr class="dropdown-divider"></li>
              <li><a class="dropdown-item" href="#">Something else here</a></li>
            </ul>
          </li>
          <li class="nav-item">
            <a class="nav-link disabled">Disabled</a>
          </li>
        </ul>
        <form class="d-flex">
          <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
          <button class="btn btn-outline-success" type="submit">Search</button>
        </form>
      </div>
    </div>
  </nav>
</body>
```

Debería verse algo similar a:

![Barra de navegación de ejemplo de Bootstrap agregada](../assets/bootstrap-default-navbar.png)

¡Vamos a adaptarla a lo que necesitamos!

[Siguiente](../reto-05/README.md)
