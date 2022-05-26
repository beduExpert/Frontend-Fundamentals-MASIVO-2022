# Ej. 01 - Crear la estructura final del proyecto
## Introducción
Nuestro proyecto ya casi está concluido. Ahora es momento de agregarle algunos elementos qué permitirán hacer de este un sitio atractivo y con cierta interactividad.

Como lo viste durante el prework, las transiciones y animaciones dan "vida" a nuestra página, sin necesidad todavía de usar Javascript. CSS tiene algunos trucos bajo la manga que hacen más interesante la presentación de tu página. Si bien deben usarse con cuidado, las transiciones y aniumaciones son casi obligadas en todos los desarrollos web modernos.

## Objetivo
1. Crear una nueva página de nuestro proyecto.
2. Maquetar la nueva página usando un diseño establecido.

## Requisitos
- Tener instalado Visual Studio Code.

## Desarrollo

¡Manos a la obra, entonces! Vamos a crear una nueva página en nuestro proyecto donde podamos agregar nuestras animaciones y transiciones de manera clara, para así poder ejercitarnos en CSS y comprender el proceso para crear estos efectos especiales, como les hemos llamado en esta sección.

Vamos a crear una nueva página, "About us", partiendo del diseño de la página Matcha al momento de crear esta documentación.

## Nuevas propiedades que utilizaremos en esta sesión

Las nuevas propiedades que utilizaremos hoy son `transition` y `animation`. Usaremos también la regla `@keyframes`, que define cómo se desarrollará una animación en nuestra página.

Como vimos en el pre-work, `transition` normalmente viene asociado con **pseudo-elementos** de CSS, como son `:hover` o `:focus`, para que se detecte el estado desde donde arranca la transición.

Las animaciones usan la propiedad `animation`, en conjunto con la regla `@keyframes`, donde podemos definir todos los estados que necesitemos durante una animación para que se desarrolle como lo deseamos. En particular, `animation` es una versión abreviada de varias propiedades de CSS relacionadas, como son `animation-duration` o `animation-name`. Esas diferentes propiedades nos permiten mantener el control entre todos los estados que necesitemos y definir exactamente cómo queremos que la animación se desarrolle.

## Elementos de Matcha a copiar en nuestro proyecto

[Ejemplo de elemento en la página de Matcha](../assets/topFeaturesMatcha.png)

Estos elementos hay que insertarlos en una nueva página. Para ello, recordemos nuestra estructura:


```text
matcha/
    └── scss/main.scss
    └── index.html
    └── pricing.html
```

Vamos a agregar nuestros archivos. Aprovecharemos que ya hemos trabajado con SASS en la sesión anterior, y utilizaremos sus bondades.

Debemos crear nuestros archivos. Simplemente abrimos una terminal y nos ubicamos en nuestro directorio de trabajo (/matcha).


```text
> pwd
/Users/bedu/matcha

> touch aboutUs.html
> ls
index.html pricing.html style.css output.css aboutUs.html

> cd scss
> touch aboutUs.scss
> ls
main.scss _global.scss _aboutUs.scss #puedes tener más archivos, según hayas decidido hacer más partials.
```

Ahora, nuestra estructura debe ser la siguiente:

```text
matcha/
    └── scss/
          └── main.scss
          └── aboutUs.scss
    └── index.html
    └── pricing.html
    └── aboutUs.html
    └── style.css
    └── output.css
```

[Siguiente](../reto-01/README.md)