# Ej. 03 - Agregando una nueva página

## Objetivos
1. Crear otra página con contenido dentro del proyecto.
2. Enlazar esta nueva página con la primera para que se pueda navegar entre ellas.
3. Utilizar más componentes de Bootstrap.

## Requisitos
- Tener instalado Visual Studio Code.

## Instrucciones

Hasta este momento, solo tenemos una página: `index.html`. Este es el archivo que el navegador buscará cuando entre a nuestra aplicación web, pero necesitamos más elementos para que  nuestro proyecto sea más funcional. Vamos a crear un nuevo archivo en el que agregaremos código y utilizaremos algunos estilos que ya hemos aplicado en `index.html`.

Empecemos por crear un nuevo archivo para el HTML y otro para sus estilos en la
carpeta principal del proyecto:

```sh
$ pwd # asegúrate que sea la carpeta del proyecto
/ruta/al/proyecto
$ touch pricing.html
$ ls
index.html   pricing.html   style.css
$ touch pricing.css
index.html   pricing.html   style.css   pricing.css
```
Tenemos que "avisar" a nuestra página principal que ya agregamos nuestra nueva sección. ¿Recuerdas que en nuestro Navbar tenemos la opción de otras secciones? Agreguemos en nuestro código de `index.html` el enlace a la nueva sección **Pricing**.

```html
  <!-- Archivo index.html -->

  <!-- Aquí va el contenido del Navbar -->
    <li class="nav-item">
      <a class="nav-link" href="pricing.html">Pricing</a>
    </li>

```
¡Eso es todo! Nuestra página principal tiene ya establecido el enlace, con lo que al hacer clic en el Navbar en la opción **Pricing**, nuestro navegador cambiará la página que está mostrando de `index.html` a `pricing.html`.

>EXTRA Trata de agregar en pricing.html una referencia a la página principal, tanto al hacer clic en el navbar al texto correspondiente, como al hacer clic en la imagen de Matcha. Es el mismo procedimiento que hicimos al cambiar la referencia de pricing en la página principal.

Ahora, crearemos el código HTML y le agregaremos la configuración de Bootstrap:

```html
<!-- pricing.html -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta
      name="viewport"
      content="width=device-width,initial-scale=1.0,user-scalable=no"
    />
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
    <title>Matcha - Pricing</title>
    <!-- Agregamos la nueva página de estilos -->
    <link rel="stylesheet" type="text/css" href="./pricing.css" />
  </head>
  <body>

    <!-- Aquí agregaremos el nuevo contenido -->

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ka7Sk0Gln4gmtz2MlQnikT1wXgYsOg+OMhuP+IlRH9sENBO0LRn5q+8nbTov4+1p" crossorigin="anonymous"></script>
  </body>
</html>
```

La barra de navegación debe ser igual a la del archivo `index.html`. Para ello, solo copiamos ese elemento en `pricing.html` y agregamos a `pricing.css` los estilos correspondientes:

```html
<!-- pricing.html -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta
      name="viewport"
      content="width=device-width,initial-scale=1.0,user-scalable=no"
    />
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
    <title>Matcha - Pricing</title>
    <link rel="stylesheet" type="text/css" href="./pricing.css" />
  </head>

  <body>

    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-light fixed-top">
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
              <a class="nav-link active" aria-current="page" href="./platform.html">Platform</a>
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

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ka7Sk0Gln4gmtz2MlQnikT1wXgYsOg+OMhuP+IlRH9sENBO0LRn5q+8nbTov4+1p" crossorigin="anonymous"></script>
  </body>
</html>
```
Estos son los estilos de nuestra navbar:

```css
/** pricing.css */
  @import url("https://fonts.googleapis.com/css?family=Alegreya:900|Open+Sans|Slabo+27px&display=swap");

  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body {
    background-color: #fffbf7;
    font-family: "Open Sans", sans-serif;
  }

  .navbar {
    background-color: #fffbf7;
  }

  .navbar-light .nav-item .nav-link {
    color: #025157;
  }

  .navbar-light .navbar-toggler {
    border-color: #025157;
  }

  .navbar-light .navbar-toggler-icon {
    background-image: url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' width='30' height='30' viewBox='0 0 30 30'%3e%3cpath stroke='rgb(3, 81, 77)' stroke-linecap='round' stroke-miterlimit='10' stroke-width='2' d='M4 7h22M4 15h22M4 23h22'/%3e%3c/svg%3e");
  }

  .actions {
    text-align: right;
    font-weight: 600;
    font-size: 14px;
  }

  .actions > * {
    margin-right: 10px;
    margin-left: 10px;
  }

  .actions a {
    color: #67b54b;
  }

  .actions button {
    color: white;
    background-color: #67b54b;
    padding-left: 14px;
    padding-right: 14px;
    padding-top: 12px;
    padding-bottom: 12px;
    border: 0;
    border-radius: 5px;
  }

```

Con estos estilos y estructura extraídas de nuestro `index.html` obtenemos la
misma barra de navegación, pero ahora en `pricing.html`.

[Siguiente](../reto-04/README.md)