# Práctica Git

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://github.com/eglogis/KeepCodingPracticaGit)
#### ¿Qué comando utilizaste en el paso 11? ¿Por qué?

```sh
git reset --hard HEAD~1 
```
Con el comando git reset reseteamos los cambios al *commit* que queramos, en este caso reseteamos a **HEAD~1** que es el ultimo que hemos realizado. Con **--hard** estamos diciendo que queremos resetearlos perdiendo los cambios del **Working copy**

#### ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

```sh
git reflog
git reset —hard <referencia_del_commit>
```
Con **git reflog** podemos ver los registros de referencia que crea git cada vez que hacemos una actualizacion de git en ese repositorio. Con esto podemos coger la referencia del commit donde actualizamos el fichero *git-nuestro*. Con el comando **git reset** reseteamos los cambios al *commit* que queramos, en este caso a la referencia del **commit** que hemos buscado anteriormente.

#### El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
No causó ningún conflicto, porque en la rama **master** no hemos hecho ningun *commit* cambiando el contenido de fichero git-nuestro. Por lo que no ha habido ninguna bifurcacion en los *commit* con la que pueda haber conflicto. Es un merge *Fast Forward*

#### El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
Si causó conflictos porque hemos cambiado las mismas lineas en el mismo fichero, en este caso del finchero git-nuestro, por lo que git te pide que eligas los cambios con los que quieres quedarte, ya sea los de la rama **styled**, los de **htmlify** o una mezcla de ambos. En este caso no se puede hacer un merge *fast forward* porque ha habido una bifurcacion en el grafo de *commits*.

#### El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
No casuó ningun conflicto porque en la rama **master** no hemos hecho ningun *commit* cambiando el contenido de fichero git-nuestro que si se ha cambiado en la rama **styled**.

#### ¿Qué comando o comandos utilizaste en el paso 25?
```sh
git log --oneline --graph
```

#### El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
Si puede ser fast forward, ya que no ha habido ninguna bifucarción en el grafo de *commit* de **title** con respecto a **master**, Es decir, en **master** no hemos hecho ningun *commit* nuevo después de crear la rama **title** que pueda afectar al grafo.

#### ¿Qué comando o comandos utilizaste en el paso 27?
```sh
git reset HEAD~1 
```

#### ¿Qué comando o comandos utilizaste en el paso 28?
```sh
git restore <nombre_del_fichero>
```

#### ¿Qué comando o comandos utilizaste en el paso 29?
```sh
git branch -D <nombre_de_la_rama>
```

#### ¿Qué comando o comandos utilizaste en el paso 30?
```sh
git reflog
git reset --hard <referencia_del_merge>
```

#### ¿Qué comando o comandos usaste en el paso 32?
```sh
git reflog
git checkout <referencia_del_primer_commit>
```

#### ¿Qué comando o comandos usaste en el punto 33?
```sh
git reflog
git checkout <referencia_del_ultimo_commit>
```
