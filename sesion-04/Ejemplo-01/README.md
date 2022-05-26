# Ej. 01  Obteniendo cambios con `git pull`

## Objetivos
- Utilizar el comando `pull` de git para obtener los cambios hechos por otras personas desde nuestro repositorio.

## Requisitos
- Tener Git instalado.
- Tener Visual Studio Code instalado.
- Tener una terminal de sistema disponible.

## Desarrollo

Como siempre que queremos aplicar cambios relacionados con Git, es necesario que
nos movamos en la terminal hacia la carpeta de nuestro proyecto. Una vez dentro,
vamos a realizar los siguientes pasos:

1. Escribiremos `git pull <nombre-remoto> <nombre-rama>` para traer los cambios
   que se realizaron desde otro ordenador, ya sea cambios que tu hiciste o que
   alguien te mandó un Pull Request y terminaste aceptando. Ten en cuenta que
   normalmente por defecto el nombre del remoto es `origin` (lo puedes verificar
   ejecutando `git remote -v`) y si no creaste ninguna rama, tu nombre de la
   rama será `master`.

   En caso de que no tengamos ningún cambio realizado en Github, nos mostrará
   algo similar a:

   ```bash
   # Este comando arrojará algo similar a las siguientes líneas
   $ git pull origin master
   From github.com:<nombre-usuario>/<nombre-repositoio>
    * branch            master    -> FETCH_HEAD
   Already up to date.
   ```

   Mientras que si tenemos algún cambio que no está en nuestra computadora, se
   verá algo como:

   ```bash
   # Este comando arrojará algo similar a las siguientes líneas
   $ git pull origin master
   remote: Enumerating objects: 74, done.
   remote: Counting objects: 100% (74/74), done.
   remote: Compressing objects: 100% (2/2), done.
   remote: Total 135 (delta 72), reused 72 (delta 72), pack-reused 61
   Receiving objects: 100% (135/135), 250.44 KiB | 1.41 MiB/s, done.
   Resolving deltas: 100% (82/82), completed with 35 local objects.
   From github.com:<nombre-usuario>/<nombre-rerpositorio>
    * branch              master        -> FETCH_HEAD
      58454bc1..00197cd7  master        -> origin/master
   Updating 58454bc1..00197cd7
   Fast-forward
    ruta/al/archivo/modificado.html          |    6 +-
   ```

[Siguiente](../Ejemplo-02/README.md)