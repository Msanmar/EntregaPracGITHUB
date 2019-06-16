# EntregaPracGITHUB
## Entrega Práctica de GIT Mónica Sanmartín Gregorio


**Qué comando utilizaste en el paso 11? ¿Por qué?**

Se nos pide deshacer el último commit, para ello uso el siguiente comando:
`git reset --hard HEAD~1`
Nos permite retroceder al commit anterior al que nos encontramos y descartar los cambios realizados en el working copy (tal como se pide en este paso)


**¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?**
 
Se nos pide rehacer el último commit (el deshecho en el paso anterior), para ello usamos el comando:
`git reflog => para ver el SHA del commit a recuperar /
git reset -hard "idcommit_a_recuperar", en este caso (d4fd3bd) /
git log`

**El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?**

No hay conflictos pero el merge arroja el mensaje de "Already up to date", puesto que en el paso 13 se nos pide que "styled" aborba a "master", y en estos momentos ya lo está haciendo.
 

**El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?**

`git checkout styled / 
git merge htmlify`
Sí, causó conflictos porque estamos intentando hacer un merge de dos ramas que tienen un fichero con distinto contenido en varias líneas.
Nos quedamos con el contenido de la rama styled y volvemos a intentar mergear, ya con éxito:
nano git-nuestro.md => modificamos fichero quedándonos con contenido de styled
`git add git-nuestro.md /
git commit -m "Deshacemos conflicto al mergear htmlify sobre styled" / 
git log`


**El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?**

En este paso no hay conflictos, puesto que "master" puede absorber a "styled" simplemente moviendo el puntero al principio (FF) y no hay ficheros con diferente contenido en alguna misma línea.
`git checkout master / 
git merge styled /
git log /
git branch`


**¿Qué comando o comandos utilizaste en el paso 25?**
`git log --graph`


**El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?**

Se pide realizar un merge NO FF, lo cual se hace con git merge --no-ff title (desde master)
`git branch (para asegurarnos de que estamos en master) /
git merge --no-ff title`
Podría ser un merge FF perfectamente, ya que los commits forman una lista y con un merge FF simplemente se avanzaría el puntero HEAD, de forma que master englobase el trabajo de title. Hacer el merge como FF implicaría no tener un commit "extra"



**¿Qué comando o comandos utilizaste en el paso 27?**
`git status /
git log /
git reset HEAD~1 /
git status /
git log`


**¿Qué comando o comandos utilizaste en el paso 28?**
`git status /
git checkout -- git-nuestro.md /
git log`


**¿Qué comando o comandos utilizaste en el paso 29?**
(desde la rama master)
`git branch -D title /
git branch`


**¿Qué comando o comandos utilizaste en el paso 30?**
Se nos pide recuperar el merge del paso 26:
`git reflog (obtenemos id del commit donde pusimos el titulo - 6dfc937) /
git checkout 6dfc937 /
git branch title /
git checkout title /
git log /
git branch`


**¿Qué comando o comandos usaste en el paso 32?**
`git branch
git reflog / 
git checkout 45b6e47 (SHA del primer commit)/
git log`

**¿Qué comando o comandos usaste en el punto 33?**
`git reflog
git branch /
git checkout title /
git log`
