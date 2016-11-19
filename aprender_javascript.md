Para aprender Javascript
========================

Vean el resumen de javascript que hice primero, a lo mejor con eso les basta.

Pueden buscar cualquier tutorial, la mayoría te enseña relacionado a HTML y CSS,
pero no hace falta. Lo importante es entender:

- Como se escribe (comentarios, if, else, for)
- Variables (numeros, Strings, arrays)
- Estructuras de control (if, else, for, while)
- Funciones
- Objetos

http://www.genbeta.com/herramientas/ocho-webs-y-canales-de-youtube-para-aprender-javascript-desde-0-hasta-nivel-experto 

Cualquiera de esos, el de KhanAcademy no me gusta que te hable, pero está la
trasncripción también. Sino otros que vi:

https://www.codecademy.com/learn/learn-javascript (Se necesita registrarse)

http://www.w3schools.com/js/js_intro.asp (Para buscar algunas cosas, no para
hacer en orden)

Después, nosotros vamos usar un JavaScript más nuevo. Lo que cambia es:
- En vez de ```var``` usamos ```let```
- En vez de crear los objetos usando ```prototype``` usamos ```class```

Igual es casi lo mismo, cambia como se escribe nomas.

Cómo funcionan las páginas web:
===============================

Las páginas web para funcionar tienen varias partes, algunas cosas se hacen
del lado del servidor y otras se hacen en la PC que está mirando la página web.

Del lado del servidor
---------------------

No se bien del todo como es, lo que sé que hay es:

* Servidor web: Es un programa que se encarga de mandar las páginas al cliente,
  es la base de todo lo que se hace en el servidor. Manda los HTML, Javascripts
  y CSS, si hace falta le pide a PHP que ejecute cosas antes de mandar todo.

* PHP: Es un lenguaje de programación que se usa para hacer cosas en el
  servidor, por ejemplo sirve para recibir y guardar los puntajes en una base de
  datos. Es para hacer programas que funcionan en el servidor, puede hacer
  cualquier cosa.

* Base de datos: Por ejemplo MySQL. Son solamente tablas en donde podés guardar
  o mirar cosas. Para usarla generalmente se usa PHP, pero creo que se puede
  usar Javascript también.

Del lado del cliente
--------------------

Al cliente le llegan tres cosas, HTML, CSS y Javascript. Puede venir todo junto
en un solo archivo (podés meter CSS y Javascript adentro del HTML pero es más
desprolijo), pero normalmente llegan los tres archivos por separado.

También aparte llegan las imágenes, sonidos, etc.

* HTML: Es un archivo en donde viene el contenido de la página web, cada HTML es
  una página web. Ahí adentro viene solamente el texto, con los títulos,
  secciones, párrafos, etc.

* Javascript: Todo el código Javascript viene en un archivo o varios por
  separado. Sirve para programar cosas que se van a ejecutar en el cliente, por
  ejemplo el juego. Te deja modificar el HTML y el CSS al apretar un botón por
  ejemplo.

* CSS: Es otro archivo aparte que tiene todos los estilos que se van a usar en
  el HTML. En el HTML viene solamente el texto dividido en títulos, párrafos,
  etc. En el CSS uno elige qué colores usar para los títulos, el tamaño de
  letra, el color de fondo, etc.

Lo que usamos para javascript
-----------------------------

Al final un juego terminado va a tener casi todo, PHP y las bases de datos son
opcionales, si no hay que guardar ningún progreso o puntaje en el servidor no
hacen falta.

El HTML y el CSS no son muy importantes, porque tienen todo lo que se ve en la
pagina que no sea el juego. Al final son dos archivos (.html y .css) simples con
pocas cosas.

El HTML es la base, ahí adentro dice donde están los CSS y donde están los
Javascript.

Todo el juego se hace en Javascript, se guarda en archivos .js. Las imágenes se
ponen en archivos aparte.

Si uno hace doble click en un HTML se va a abrir en el navegador, el CSS y el
Javascript van a funcionar. El problema es que por seguridad ante virus la
mayoría de navegadores, al abrir desde un archivo local de tu PC el Javascript
no tiene permitido abrir archivos, entonces no se pueden cargar las imágenes del
juego.

Entonces hay que instalar un servidor web simple, que no tiene ni PHP ni bases
de datos, lo único que hace es mandar los HTML, CSS y Javascript.

Para probar los juegos
----------------------

Ver el otro documento.
