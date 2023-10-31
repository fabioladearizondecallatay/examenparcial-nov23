# examenparcial-nov23

Fabiola de Arizon de Callataÿ
link del repositorio : https://github.com/fabioladearizondecallatay/examenparcial-nov23.git 


1. Un pull request es cuando un programador decide hacer un fork de un repositorio a su cuenta, es decir copiar un repositorio de otra cuenta a su propia cuenta Github donde va a poder modificar, operar en el repositorio copiado sin modificar el inicial. La pull request es para cuando el programador quiere hacer un merge, es decir poner en comun lo que ha hecho desde su repositorio copiado al inicial, entonce va a crear una pull request donde hace una demanda al repositorio inicial y envia los cambios que desea hacer al repositorio inicial. Luego el programador del repositorio inicial puede decidir si acepta los cambios propuestos y mergea las ramas o los ficheros con los nuevos cambios.

2. Un conflicto de fusion, es cuando uno quiere hacer un merge entre dos ramas o un pull, fetch, push con el repositorio remoto, pero las ramas que se quieren fusionar o actualizar no pueden porque hay una diferencia dentro de unos ficheros. Por ejemplo el read.me, el license o un fichero.html. Para resolverlo hay que modificar los ficheros para que lo que crea conflicto sea identico.

3. Para poder fusionar dos ramas diferentes, se deberia primero desde la rama examen_parcial hacer un "git merge main" para primero fusionarlo todo desde la rama examen_parcial y despues si el merge se hace corectamente y no hay que resolver conflictos, se hace un "git switch main" para ir a la rama main y desde ahi hacer de nuevo un "git merge examen_parcial" para asegurarse que todos los cambios de la rama examen_parcial se realizan en la rama main igualmente.

4. Para revertir un commit, lo mas simple es primero hacer "git log --oneline --graph --all" para ver el grapho de commits de manera clara y encontrar el numero de identificacion del commit al que se quiere volver. El numero de identificacion es una cadena de entre 7 y 8 caracteres que luego se va a copiar para usarla en el commando " git reset "XXXXXXXXX" ". Eso permite volver a ese commit en el proyecto pero no elimina los cambios porque no se ha hecho un "git reset hard" que eso si que los eliminaria.

5. Un fork es cuando un programador va al repositorio publico de otro programador y decide copiarlo a su cuenta personal github. Para eso se encuentra un boton "fork" arriva a la derecha del dicho repositorio y al usarlo, se crea entonces una copia del repositorio a su cuenta personal. Esa accion se usa comunmente para las personnas que quieren o 1) usar lo que se ha realizado ya en otro repositorio para un uso personal o 2) trabajar en equipo con un mismo repositorio y poder hacer cambios sin interferir con el repositorio inicial y luego fusionar los dos repositorios con un pull request (como explicado en la pregunta 1).

6. a) Primero al estar en el directorio raiz vamos a ir al directorio fabiola haciendo un "cd fabiola", cd siendo "cambio de directorio". Una vez en el directorio fabiola hacemos un "cd Universidad" para ir al directorio Universidad. Desde el directorio Universidad hacemos otro "cd UAX" para llegar al directorio UAX. Una vez ahi, podemos hacer "ls" para obtener una lista de todos los archivos que se encuentran en el directorio UAX donde deberia de aparecer archivo.txt. Para ver el archivo podemos hacer "cat archivo.txt" y entramos en el archivo para ver lo que hay dentro. Tambien se pueden usar otros comandos como "git open archivo.txt" o "git show archivo.txt" etc.
   Ese trayecto que hemos hecho para aceder al archivo se ha hecho por la ruta absoluta porque hemos salido desde el directorio raiz.

   b) Desde el directorio Universidad habria que hacer "cd UAX" y luego como explicado antes "ls" para verificar que el archivo este en el directorio UAX y abrirlo con alguno de los comandos explicados arriba. Ese trayecto se ha hecho por una ruta relativa porque es una ruta que empieza desde un directorio que no es el directorio raiz.

7. 1) b) git clone
   2) a) git branch
   3) c) git checkout
   4) b) git add
   5) b) git commit
   6) b) git push
   7) c) git pull
   8) d) git merge
   9) a) git reset --hard
   10) c) git log

8. Para que las integraciones desde las ramas matematicas y Diseno UX no se mezclen y modifiquen la rama developp, lo mas simple seria que se haga primero la integracion de la rama matematicas y luego la integracion de la rama Diseno UX.
   Los collaboradores de la rama matematica hacen un "git merge -m "Integrate matematicas en developp" developp" desde la rama matematicas,
   donde, si no hay conflictos, se fusionan los cambios de la rama matematicas en la rama developp y viene con un commit con mensaje "Integrate matematicas    en developp".
   Luego, los collaboradores de la rama Diseno UX, una vez el merge hecho harian un "git diff developp Diseno UX" para ver todos los cambios que se han        hecho con el merge de matematicas y ver si no tienen que modificar algun fichero que se haya modificado desde el merge para evitar conflictos (con el    nano seguido de "git add . " y de un commit para hacer una instantanea de la version de la rama.
   Una vez que este todo en orden, ellos haran un "git merge -m "Integrate Diseno UX en developp" developp" desde la rama Diseno UX, donde si no hay     conflictos, se hace un auto-merge y se fusionan los nuevos cambios de la rama Diseno UX a la rama developp que debe de tener ya los cambios de la rama    matematica.
Al final, desde la rama developp se podria hacer un "git log" para verificar que los merge aparecen en el historial de commits y que se pueden hacer unos "git diff "codigo de commits"" para ver los nuevos cambios realizados.

9. B) Clonaste el repositorio remoto, hiciste cambios en el archivo "index.html" en una rama secundaria, y luego hiciste un pull request a la rama principal (master).



Perdon por las faltas de ortografia, escribo con un teclado belga lo que me impide usar las tildes.
