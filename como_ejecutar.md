Acá está todo sobre como ejecutar un juego.

Depende de qué necesita el juego, si el juego necesita cosas del lado del
servidor uno va a necesitar un servidor de PHP y no se qué mas.

Pero si el juego es uno simple, que funciona solamente con Javascript uno
necesita un servidor web bien simple.

Para juegos simples
===================

Lo unico que habría que hacer es abrir un ```.html``` con un navegador (haciendo
doble click). Pero por seguridad, la mayoría de los navegadores no te permiten
cargar imágenes desde el disco duro, entonces no se puede.

Lo que hay que hacer es correr un servidor web simple en la PC y abrir el juego
desde ahí

Para correr el servidor
-----------------------

Hay que iniciar un servidor web en la carpeta principal del repositorio (donde
está este README)

### En Windows

Yo ya puse en los repositorios de los juegos a _Mongoose_ que crea un servidor
web en la carpeta donde esté el programa. Entonces lo único que hay que hacer
es hacer doble click al programa

### En Linux

No hace falta ningún programa, hay que abrir una terminal en la carpeta y
hacer:

~~~~~~~~~~~~~~~~~~~~
python3 -m http.server 8080
~~~~~~~~~~~~~~~~~~~~

Para correr el juego
--------------------

Hay que abrir un navegador y abrir nuestra IP usando puerto 8080, o sea, hay
que ir a ```127.0.0.1:8080``` o a ```localhost:8080```.

Desde ahí te podés mover y seleccionar el ```.html``` que querés abrir.

Para juegos con servidor
========================

Creo que hay dos formas, haciendo un servidor completo en tu PC con PHP, MySQL,
ets. O se puede correr el mismo servidor simple para el juego, y para las cosas
del lado del servidor usar el mío.

Pero si uno está probando cosas con PHP y eso creo que si o si hay que correr
un servidor, sino hay que actualizar el mío a cada rato (que tambien puede ser)
