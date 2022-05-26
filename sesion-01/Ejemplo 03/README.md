# Ej. 03 - Agregando el home de Matcha
## Objetivos
1. Agregar el primer contenido a tu proyecto usando HTML.
2. Aprender como usar las etiquetas de HTML.

---
<br/>

## Requisitos
- Tener Visual Studio Code instalado.
- Conocer estructura básica de las etiquetas HTML.

---
<br/>

## Instrucciones

Siguiendo el diseño del sitio original de [`Matcha`](https://bedu-fef.netlify.app/),
podemos ver que lo primero que aparece son textos de diferentes tamaños y
colores además de un formulario y una imagen.

Para agregar el texto principal podríamos usar un párrafo (etiqueta `<p></p>`).
Sin embargo, este texto quiere mostrar lo que nos permite realizar el servicio
de `Matcha` y darle un mayor énfasis y diferenciarlo de los demás textos.

Para lograr este efecto _semántico_ en nuestro sitio web, podemos usar los
_headings_ (encabezados). Estos nos ayudan a dar un énfasis jerárquico de
acuerdo al número que nosotros utilicemos, siendo posible usar del 1 al 6,
con 1 como el de mayor peso jerárquico y 6 el menor.

En este caso, queremos el texto inicial es el de mayor peso jerárquico por lo
que usaremos el heading de peso 1, y esto lo indicamos haciendo uso de la
etiqueta `<h1></h1>`.

Aplicalo a nuestro código existente:

```html
<!DOCTYPE html>
<html>
  <head>
    <!-- Aquí va información importante pero no visible dentro del navegador -->
    <title>Matcha</title>
  </head>
  <body>
    <!-- Esto es lo que se verá en el navegador web -->
    <h1>Build your blog. Build your business.</h1>
  </body>
</html>
```

Abre este archivo en tu navegador y mira el resultado. ¡Tu primera página web!
Claro, solo es un texto, pero ¡es un gran primer paso!

<br/>

[Siguiente](../reto-01/README.md)