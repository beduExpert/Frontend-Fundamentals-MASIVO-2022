## Ej. 01 - Creando nuestras Ramas para versiones de nuestro proyecto

## Objetivos
- Aprender cómo obtener cambios desde un repositorio en GitHub.
- Aprender cómo integrar esos cambios en nuestra rama de trabajo.

---
<br/>

## Instrucciones

1. Escribimos `git branch` para saber en que rama estoy y cuantas ramas tengo
2. Escribimos `git branch [Nombre de rama] `para crear nuestras.
3. Escribimos `git checkout [Nombre de la rama] `para cambiarnos de rama.

---
<br/>

## Desarrollo
<br/>

### Obteniendo cambios con git `git pull`  `git fetch` y `git merge`

1. Escribiremos `git fetch` para traer los cambios que se realizaron desde otro
   ordenador, ya sea cambios que tu hiciste o que alguien te mandó un Pull Request
   y terminaste aceptando.

   ```bash
   $ git fetch # Este comando arrojará algo similar a las siguientes líneas
   remote: Enumerating objects: 12, done.
   remote: Counting objects: 100% (12/12), done.
   remote: Compressing objects: 100% (7/7), done.
   remote: Total 7 (delta 3), reused 0 (delta 0), pack-reused 0
   Unpacking objects: 100% (7/7), 1.66 KiB | 1.66 MiB/s, done.
   From https://github.com/<nombre-de-usuario>/<nombre-de-repo>
   * [new branch]      <nombre-rama> -> origin/<nombre-rama>
     5626041..5b6fd55  master           -> origin/master
   ```

   Lo que nos dice este comando es que trajo cambios desde Github, cambios en la
   rama original (master en el ejemplo) y cambios en nuevas ramas en caso de
   existir. Adicionalmente, nos indica que la nueva rama ha sido almacenada en
   algo llamado `origin/<nombre-rama>` y los cambios que se hicieron en la rama
   master se encuentran `origin/master`. ¿Logras ver el patrón? Cualquier cambio
   lo encontrarás en una _rama_ llamada `origin/<nombre-de-rama>`.

2. Ahora que ya tenemos nuestros cambios en nuestra computadora, aun estos no se
   verán reflejados en nuestro código, esto debido a que `git fetch` solo se
   encarga de _descargar_ los cambios. Para poder juntar los cambios descargados
   con lo que nosotros tenemos en nuestro proyecto se usa `git merge`, checa el
   ejemplo:

   ```bash
   # En este caso queremos combinar los cambios que se hicieron a la rama master.
   # Si tu quisieras obtener cambios de otra rama, podrías cambiar `master` por
   # la rama que desees.
   $ git merge origin/master
   Updating 5626041..5b6fd55
   Fast-forward
    ruta/al/archivo/modificado.html | 277 ------------------------------------
    1 file changed, 277 deletions(-)
   ```

   En el ejemplo, el _merge_ causó que se obtengan 277 cambios (borrado de
   código para este caso) y se juntaron sin generar ningún conflicto entre los
   cambios que estaban en el proyecto antes de unir los cambios que descargamos.

   Esto variará dependiendo de los cambios que hayas realizado, si agregaste
   código, salrá los archivos que se modifcaron y cuántas líneas se alteraron,
   de igual forma con alguna actualización o eliminación.

   <br/>

   > Tip: En ocasiones, se modificó algo en Github, pero al mismo tiempo tu
   > también hiciste modificaciones en la misma ubicación (archivo) y tocaron
   > líneas de código similares. Cuando esto sucede, git no sabe qué cambios se
   > deberían preservar, si los cambios que hiciste en tu computadora o los que
   > está por juntar, a esto se le llaman `conflictos` y dependiendo de los
   > cambios, puede llegar a ser tedioso de corregir. Si te llegara a pasar,
   > puedes consultar [este enlace](https://help.github.com/es/enterprise/2.19/user/github/collaborating-with-issues-and-pull-requests/resolving-a-merge-conflict-using-the-command-line)
   > de Github no bien traducido al español pero con buena y simple información
   > de cómo solucionarlo, si te trabas, no dudes en consultarlo durante la
   > sesión :wink:.


<br/>

[Siguiente](../reto-01/README.md)