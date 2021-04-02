# git

## Manejo de ramas

```git checkout -b NOMBRE```(por si querés hacer una rama y te coloca en ella o sea digamos que querés probar algo mientras chang está trabajando en el  mismo componente hace la rama probas mientras chang sigue en lo suyo y si mira que ya está le avisas y ya le podes hacer merge)

```git checkout NOMBRE``` para salta entre ramas o se si estás en la que creaste pordes regresar a la master con git checkout master

```git merge NOMBRE -m 'Mensaje del merge'``` fusiona la rama que tenés seleccionada con NOMBRE o sea que pega lo que pueda en la rama actual ya te dja listo para sólo hacer git push sin necesidad de hacer git add y git commit

## Aquí van unos extras:
si se te olvida en que rama estás jajajaj porque puede pasar usa

```git branch --list```

```git branch -a``` todas las ramas hasta los que no tienen descargadas (hacer primero update de las ramas)

```git show-branch``` esta es más copacta jajaja

```git branch -d NOMBRE``` elimina la rama por si sólo la usaste un momento te la podes clavar con eso.

```git branch -D NOMBRE``` elimina la rama no importando si existe algún problema (cuidado).

## Útiles

```git add .``` agrega el directorio actual a los cambios

```git commit -m 'mensaje'``` agrega el trabajo añadido por add a los cambios aprobados (local)

```git push -u REMOTO RAMA``` si clonaron el repo el remoto sería origin y la rama depende donde estén si crearon una nueva rama si es obligatorio el nombre sino pueden sólo poner ```git push``` 
(agrega los cambios al repo del github)

```git pull REMOTO RAMA``` como me imagino que van a estar en la rama que es y sólo un remoto porque no le veo porque tener más jajaj nunca he usado más de uno entonces  pueden usar sólo ```git pull```
(se webea los cambios jajaj)

```git log``` les muestra todos los commits que se han hecho, presionen **q** para salir, pueden copiar el número de commit y darle checkout, para visitar lo que que se tenía en ese commit 

```git checkout COMMITID .``` para regresar la rama actual a cierto commit.

```git restore NOMBRE_ARCHIVO``` para restaurar un archivo que no ha sido agregado con git add, si ya ha sido agregado ejecute el siguiente, se puede pasar ```.``` para restaurar todo el directorio (recuerde que no deben estar en el espacio de trabajo).

```git reset ARCHIVO``` lo quita del espacio de trabajo (añadido con git add), sin argumento para quitar todos los archivos del espacio del espacio de trabajo.

## Para Github
```git push —delete NOMBRERAMA``` para eliminar ramas en Github y no sólo localmente.

```git remote update REMOTO --prune``` actualizar las ramas locales.

```git fetch REMOTO``` traer desde el remoto todo lo que no se tenga localmente.


