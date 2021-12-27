# git

## Manejo de ramas

- `git checkout -b NOMBRE`(por si quieres hacer una rama, te coloca en ella de una, o sea
digamos que quieres probar algo mientras Chang está trabajando en el mismo componente,
hace la rama, probas mientras Chang sigue en lo suyo y si miras que ya está le avisas y
ya le podes hacer merge).

- `git checkout NOMBRE` para saltar entre ramas, por ejemplo estás en la rama que
creaste, podes regresar a la **main** con `git checkout main`

- `git merge NOMBRE -m 'Mensaje del merge'` fusiona la rama que tienes seleccionada
con NOMBRE, si no es posible te lo notifica (te toca reparar manualmente), ya te deja
listo para sólo hacer `git push` sin necesidad de hacer `git add` y `git commit`.

## Aquí van unos extras:
si se te olvida en que rama estás xD, porque puede pasar, usa:

- `git branch --list` Lista las ramas.

- `git branch -v` Lista las ramas, pero también muestra el último commit.

- `git branch -a` todas las ramas hasta los que no tienen descargadas
(hacer primero [update de las ramas](#para-github))

- `git show-branch` esta es más compacta xD.

- `git branch -d NOMBRE` elimina la rama por si sólo la usaste un momento,
te la podes clavar con eso.

- `git branch -D NOMBRE` elimina la rama no importando si existe algún problema (cuidado).

## Útiles

- `git add [ARCHIVO1 ARCHIVO2 ...]` agrega los archivos a los cambios, también
se puede colocar por ejemplo `.` para indicar que agregue todos los cambios en
el directorio actual.

- `git add -A` agrega todo sin importar en que path dentro del repositorio se esté.

- `git commit -m 'mensaje'` agrega el trabajo añadido por add a los cambios aprobados (local).
Si no se agrega el -m, se abre un editor para la estructuración de un commit, esto
es bueno ya que permite usar la estructura completa de un commit.

```
Breve descripción (título)

[cuerpo del commit (opcional)]

[footers (opcional)]
```

También es recomendado ver [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/),
que es un estándar que actualmente está siendo usado.


- `git push REMOTO RAMA` si clonaron el repo el REMOTO sería `origin`
y la RAMA depende donde estén, si crearon una nueva rama si es obligatorio
el nombre, sino pueden sólo poner `git push REMOTO` (realmente si está
configurada la rama default), también se pueden hacer configuraciones
para dejar por defecto y seguir usando la versión corta `git push`.


- `git pull REMOTO RAMA` extrae los cambios desde un remote y los fusiona con la rama
actual.

- `git log` les muestra todos los commits que se han hecho, presionen **q** para salir
(si les abre una pantalla nueva), pueden copiar el número de commit
y darle checkout, para visitar lo que que se tenía en ese commit.

- `git checkout COMMIT_HASH .` para regresar la rama actual a cierto commit.

- `git restore NOMBRE` para restaurar un archivo que no ha sido agregado
con `git add`, si ya ha sido agregado ejecute `git reset [ARCHIVO (opcional)]` (vea a bajo),
se puede pasar `.` para restaurar todo el directorio (recuerde que no deben estar en el
espacio de trabajo), es decir `NOMBRE` puede ser, por decirlo de una manera un path relativo.

- `git reset [ARCHIVO (opcional)]` lo quita del espacio de trabajo
(añadido con `git add`), sin argumento para quitar todos los archivos
del espacio del espacio de trabajo.

## Para Github
- `git push —delete NOMBRERAMA` para eliminar ramas en Github (nuestro repositorio
de código).

- `git remote update REMOTO --prune` actualizar las ramas locales.

- `git fetch REMOTO` traer desde el remoto todo lo que no se tenga.

## SSH
Puede ser útil agregar una clave SSH para no tener que estar generando PATs para
pushear al remoto, vea [agregar una clave SSH](https://docs.github.com/es/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account).

- Como bonus, puede ocurrir que tenga más de una cuenta, para usar diferentes claves
SSH, puede cambiar la configuración local del repositorio de esta forma:
`git config core.sshcommand "ssh -i ~/.ssh/SU_CLAVE"`, cabe mencionar que lo que
está cambiando es el comando así que verifique que sea válido.
