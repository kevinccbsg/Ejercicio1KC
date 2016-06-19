
# Preguntas Ejercicio 1

### ¿Qué comando utilizaste en el paso 11? ¿Por qué?

```git reset HEAD~1 --hard```

Porque con git reset movemos el putero de la rama ademas del de HEAD. Además el HEAD~1 quiere decir que nos referimos al commit anterior por lo que si estamos moviendo el puntero de rama al commit anterior estamos desaciendo el commit. Luego el --hard quiere decir que descartamos los cambios que quedarían en el working copy.

### ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

```git reflog```

Este comando lo uso para recuperar el identificador del commit que en mi caso es 427f666. Con lo que luego puedo hacer:

```git reset 427f666 --hard```

Es decir muevo el puntero de mi rama styled además de head a dicho commit recuperandolo. El --hard para añadirlo al repo sin tener que hacer el proceso de añadirlo al staging area y luego al repo.

### El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?

No, causa un Already up-to-date ya que el commit de styled es posterior y el contenido de master ya lo tenia en su primer commit por lo que al estar más avanzado en el grafo está ya actualizado.

### El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?

Si, hay conflictos. Porque en ambas ramas se modificaron las mismas lineas del archivo git-nuestro.md provocando conflicto.

### El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?

No, no ha habido conflicto ya que el puntero de la rama master está contenido en la rama styled y por lo tanto solo avancamos el de la rama master al final del styled haciendo un merge fast forward sin causar ningún conflicto solo actualizando el contenido de master.

### ¿Qué comando o comandos utilizaste en el paso 25?

git graph (Porque tengo un alias pero el comando que use fue el siguiente)

```git log --graph --all --format=format:'%C(bold blue)%h%C(reset) - %C(bold cyan)%aD%C(reset) %C(bold green)(%ar)%C(reset)%C(bold yellow)%d%C(reset)%n'' %C(white)%s%C(reset) %C(bold white)— %an%C(reset)' --abbrev-commit```

### El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?


Si, ya que la rama title genero un commit a partir del último de la rama master y la master no genero otro por lo que el puntero de la rama master solo tendría que avanzar hasta el de title realizando un merge fast-forward


### ¿Qué comando o comandos utilizaste en el paso 27?

```git reset HEAD~1```


### ¿Qué comando o comandos utilizaste en el paso 28?

```git checkout -- git-nuestro.md```

### ¿Qué comando o comandos utilizaste en el paso 29?

```git branch -D title```

### ¿Qué comando o comandos utilizaste en el paso 30?

```git branch title```

```git checkout title```

```git reflog```

```git reset f548c81 --hard```

```git checkout master```

```git merge title --no-ff```


### ¿Qué comando o comandos usaste en el paso 32?

```git log``` - Para localizar el identificador del primer commit

```git checkout ba7d4bd31e328939f3485322d901c406ef0d0d66``` - Para moverme a ese commit

### ¿Qué comando o comandos usaste en el punto 33?

```git checkout master```
