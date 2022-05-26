# Reto 01 - Creando nuestras ramas
## Objetivos
- Crear una rama donde trabajaremos

---
<br/>

## Requisitos
- Tener Git Bash si usas Windows.
- Tener instalado Visual Studio Code.


---
<br/>

## Instrucciones

 1. Crea una rama que se llame **develop**
 2. De la rama develop crea una rama que llamaremos `task/001/changeBckcolor`
 3. Cambia el color de tu `background-color` del proyecto de la sesión anterior
 4. Sube los cambios a github de esta rama
 5. Jala los cambios con `git pull` de la rama `task/001/changeBkcolor` a develop
 6. Sube tus cambios a Github

<br/>

<details>
  <summary>Posible solución</summary>

```console

 git checkout -b develop

 git push -u origin develop

 git checkout -b task/001/changeBckcolor

```

 Aplicar cambios al CSS

```console

 git add .

 git commit -m "Cambiar backgroundColor"

 git push

 git checkout develop

 git merge task/001/changeBckcolor

 git push


```

 Vamos a GitHub y comprobamos que los cambios se aplicaron correctamanente

</details>

<br/>

[Siguiente](../Ejemplo-02/README.md)
