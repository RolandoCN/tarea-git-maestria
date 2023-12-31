# Controlador Versiones
## Tarea maestria

Git es un sistema de control de versiones que nos permite mantener ordenado las diferentes versiones que hagamos en nuestro proyecto, ademas de poder acceder a nuestro codigo fuente desde cualquier parte del mundo con acceso a internet, trabajar con varios colaboradores, asi como tambien poder volver a un cambio anterior en caso de que la situacion lo amerite.

A continuacion detallamos alguno de los comandos.

### git config --global 
Como primer punto debemos realizar la configuracion del git en la maquina en la cual estamos trabajando para ello debemos asociar la cuenta git a una cuenta de usuario y email.

### git config --global user.name "..."
Este comando permitira asociar a git a la cuenta RolandoCN dentro de la PC.

![Alt text](image.png)

### git config --global user.email "..."
Este comando permitira asociar a git a la cuenta email juan.roland@outlook.es, dentro de la PC.

![Alt text](image-1.png)

### git config --list
Mediante este comando podemos visualizar la informacion de la configuracion de git en la pc que estamos trabajando, como por ejemplo ver a que correo y cuenta de usuario de git esta asociada

![Alt text](image-2.png)

### git init
El comado git init permite inicializar o agregar git a un proyecto en desarrollo, es decir que si tenemos un proyecto y deseamos agregarlo a un repositorio de git, debemos primeramente instalar y configurar git, y posteriormente dirigirnos a la carpeta del proyecto abrir la consola y escribir el comando git init.

![Alt text](image-3.png)

### git add 
Una vez inicializado git dentro de proyecto si deseamos agregar ya sean carpetas, archivos o cambios al repositorio debemos escribir el comando git add, el cual nos permite dos opciones que se detallan a continuacion.

- git add .  
Permite agregar todos los nuevos cambios del proyecto.

   ![Alt text](image-4.png)

- git add test.js
Permite agregar el cambio del archivo escrito, en este ejemplo solo estamos agregando el cambio del archivo, test.js.

   ![Alt text](image-5.png)

### git status
Nos permite ver los nuevos cambios realizados dentro del proyecto.

![Alt text](image-6.png)

### git commit
Permite asignar de manera descriptiva mediante un nombre o mensaje al cambio realizado y guardarlo en el repositorio de manera local.

![Alt text](image-7.png)

### git log
Con este comando podemos visualizar cada uno de los commit relizados dentro de la rama que nos encontremos trabajando.

![Alt text](image-8.png)

### git diff
Permite comparar las diferencia entre los cambios realizados ya sea entre ramas o commit, a continuacion el siguiente ejemplo muestro la difrencia de dos commit.

![Alt text](image-9.png)

### git branch
Permite trabajar con ramas dentro de git, por defecto git nos provee la rama main o master pero podemos agregar mas ramas, asi como tambien eliminar dichas ramas

### git branch desarrollo
Si deseamos crear una rama debemos escribir git branch mas el nombre de la rama que deseamos crear, para este ejemplo he creado la rama desarrollo con el siguiente comando.

![Alt text](image-10.png)

### git checkout desarrollo
Si deseamos movernos a la rama que acabamos de crear debemos escribir el comando git checkout mas el nombre de  la rama en este caso quedaria asi.

![Alt text](image-11.png)

Si deseamos movernos a otra rama debemos escribir el comando git checkout mas el nombre la rama que desamos movernos, en este caso voy a volver a la rama master, con el siguiente comando.

![Alt text](image-12.png)

### git branch -b produccion
Si deseamos crear una rama y movernos a ella directamente, debemos usar el comando git branch -b mas el nombre la rama, en este ejemplo creare una rama produccion y me movere a ella directamente.

![Alt text](image-13.png)

### git merge
Permite fusionar o unir los cambios de dos ramas en una sola es decir, que si deseo obtener los cambios de la rama desarrollo a la de produccion debeo hacer un merge entre ambas, a continuacion se muestra el codigo.

![Alt text](image-16.png)

### git show
Permite visualizar de manera detalla y descriptiva cada una de los cambios realizados del proyecto con git ya sea las ramas creadas, los commit generados, entre otros.

![Alt text](image-15.png)

### hooks
Los hooks son script que se ejecutan despues de un evento dentro de git, como por ejemplo podemos crear una funcion que se ejecute cada vez que realicemos un commit, para lo cual se debe editar el archivo pre-commit.

En el siguiente ejemplo hemos configurado el archivo pre-commit que lo que hara es ejecutar un mensaje por pantalla

![Alt text](image-50.png)

El mensaje que mostrara por pantalla cada vez que hagamos commit sera "vamos hacer un commit"

![Alt text](image-51.png)

Si queremos omitir la funcion o mensaje creada en el precommit debemos agregar al final de cada commit -m

### git ignore
Es un archivo donde podemos colocar los archivos y carpetas que sea ignoradas al momento de subir un cambio es decir que si tenemos un proyecto con informacion estatica o confidencial y deseamos que no sean subidas al hacer un commit debemos agregar el nombre de la misma dentro de este directorio.

![Alt text](image-52.png)
### git rebase
Con este comando podemos mejorar la organizacion de los commit realizados, permitiendonos opciones como traer los cambios de una rama a otro similara al git merge, asi como tambien renombrar nuestro commit realizados, fusionar commit, y fusionar commit y registrarlo con un nombre mas representativo.
A continuacion se muestra los cambios realizado en la rama main, que fue la funcion de validar campos.

![Alt text](image-17.png)

Ahora realizaremos cambios en la rama desarrollo, la cual la denominaremos, calcularTotal2.

![Alt text](image-20.png)

Ahora realizamos git rebase para obtener los cambios en la rama desarrollo de lo realizado en main
![Alt text](image-18.png)

Teniendo como resultado

![Alt text](image-21.png)

### git rebase -i
Permite renombrar un commit en especifico

![Alt text](image-26.png)

Una vez ingresado el comando git rebase -i mas el id del commit saldra la siguiente ventana donde colocaremos la letra r para renombrar dicho commit y despues guardamos 

![Alt text](image-23.png)

Posteriormente saldra la siguiente ventana donde colocaremos el nuevo nombre de nuestro commit y guardamos

![Alt text](image-24.png)

Verificamos que la operacion se realizao exitosamente

![Alt text](image-25.png)

### git rebase -s
Permite unir dos commit manteniendo la descripcion de ambos, escribimos el siguiente comando que nos traera los ultimos dos commit

![Alt text](image-30.png)

Nos mostrara la siguiente ventana. Escribimos la letra s en el segundo commit lo que permitira unir ambos commit

![Alt text](image-32.png)

A continuacion saldra la siguiente ventana y lo que haremos en guardar los cambios

![Alt text](image-33.png)

Por ultimo vemos el resultado en el log

![Alt text](image-34.png)


### git rebase -f
Permite unir dos commit manteniendo solo el nombre del primer commit

![Alt text](image-35.png)

En este ejemplo uniremos los dos commit de la imagen anterior, pero mantendra el nombre del primer commit 

![Alt text](image-36.png)

### git rebase -r git rebase -f
Con este uniremos dos commit y lo renombraremos con algo mas descriptivo

![Alt text](image-37.png)

En este ejemplo hemos usado dos commit como son multiplicacion y division y lo hemos renombrado como operaciones

![Alt text](image-39.png)

### git stash
Permite almacenar de manera temporal los cambios realizados sin necesidad de usar el git commit

![Alt text](image-40.png)

### git stash list
Con este comando podemos visualizar el listado de cambios temporales almacenado 

![Alt text](image-41.png)

### git stash pop
Permite aplicar los cambios y quitarlos de la pila de almacenamiento

![Alt text](image-42.png)

### git stash apply stash@{0}
Con este comando podemos aplicar los cambios de un stash en especifico, y nos deja una copia en la memoria temporal

![Alt text](image-43.png)

### git stash pop stash@{0}
Con este comando podemos aplicar los cambios de un stash en especifico pero no deja copia del stash seleccionado en memoria

![Alt text](image-44.png)

### git cherry-pick
Permite obtener los cambios de un commit de una rama a otra sin necesidad de hacer git-merge.
En este ejemplo crearemos una funcion denominada temporal en la rama desarrollo, la cual le pondremos de nombre cambio temporal en el commit

![Alt text](image-45.png)

Luego volveremos a la rama main y traeremos ese cambio de ese commit a esta rama con el comando git cherry-pick mas el id del commit

![Alt text](image-46.png)

### git revert <<commit>>
Permite revertir cambios en caso de problemas o errores al momento de subir cambios. En este ejemplo hemos subido un cambio y al commit le hemos denominado ejemplo revertir2

![Alt text](image-48.png)

Si deseamos revertir o quitar ese cambio debemos usar git revert mas el id del commit

![Alt text](image-49.png)

![Alt text](image-47.png)



Si deseamos volver a obtener el cambio revertido debemos revertir dicha reversion

### Repositorio remoto
Una vez creada nuestra cuenta de git hub creamos un nuevo repositorio, para lo cual abrimos la pagina de git hub y creamos un nuevo repositorio, para este ejemplo le pondremos repo_maestria y lo pondremos tipo publico

![Alt text](image-53.png)

![Alt text](image-54.png)

### git remote
Para este ejemplo vamos a usar un repositorio existente y lo subiremos a git hub, para lo cual usaremos el comando git remote add origin mas la direccion del repositorio creado en el paso anterior

![Alt text](image-55.png)

### git remote -v
Permite ver si el paso anterior se realizo correctamente, ya que nos permite visualizar si el repositorio local fue vinculado al repositorio remoto.

### git branch -M main
Ahora nos cambiaremos a la rama main, con el comando git branch -M main

![Alt text](image-56.png)

### git push -u origin main
Por ultimo subimos los cambios al repositorio remoto en la rama principal main

![Alt text](image-57.png)

Con esto ya podemos visualizar y tener nuestro codigo en la nube, dentro del repositorio de git hub

### git clone
Con este comando podemos clonar un repositorio remoto existente en nuestra computadora de trabajo y empezar a trabajar en el, a continuacion vemos un ejemplo.

![Alt text](image-58.png)
