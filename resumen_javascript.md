Acá hago un resumen de lo más importante de Javascript

Básico
======

Comentarios
-----------

Se pueden hacer de dos formas

~~~~~~~~~~~~{.javascript}
// Comentario de una linea

x = 3; // Comentario de una linea al lado de código

/* Comentario multilinea
El comentario sigue hasta ser cerrado con */

/*
 * Comentario multilinea pero mas lindo
 *
 * Es mas prolijo, los asteriscos extra están de adorno
 */

/**
 * Comentario multilinea que se usa para explicar que hace una función o clase
 *
 * Empieza con dos asteriscos, lo que tiene de especial es que en algunos
 * editores esto se muestra cuando uno quiere saber como se usa una funcion o
 * clase
 */
~~~~~~~~~~~~~~~~~~~~~~~~~

Console.log
-----------

Imprime en la consola del navegador lo que uno le da. Es una función.

~~~~~~~~~~~~{.javascript}
console.log('Hola');
~~~~~~~~~~~~~~~~~~~~~~~~~

Convenciones
------------

Los espacios y saltos de línea que se usan no influyen en nada pero sirven para
ordenar todo. Hay convenciones a seguir pero la mayoría de espacios y saltos de
línea no son necesarios para que el programa funcione.

Siempre que se abren llaves se empieza a usar Tab hasta cerrar.

Los Tabs pueden ser cualquier cosa pero la convención es usar 4 espacios en vez
de Tab, sino hay que configurar el editor.

Normalmente no se escribe nada que tenga más de 80 caracteres de ancho, para que
uno pueda ver simultaneamente dos códigos uno al lado de otro en una notebook, o
3 al mismo tiempo en una PC.

Usar o no puntos y comas es lo mismo. No se que conviene, si usar o no.

Normalmente lasVariablesSeLlamanAsi (los objetos también), y las clases
EmpiezanConMayuscula.

~~~~~~~~~~~~{.javascript}
function hola(nombre) {
    if (nombre == 'martin') {
        console.log(nombre);
    }
    else {
        console.log('...');
    }
    
    nombre = 'juan';
    return nombre;
}
~~~~~~~~~~~~~~~~~~~~~~~~~


Variables
---------

Para definir variables, hay que definirlas (crearlas) con ```let``` antes de
usarlas

~~~~~~~~~~~~{.javascript}
// Variables numericas

let edad = 3;
edad += 1; // Sumarle 1
edad++; // Es una abreviacion de lo mismo
edad = 50;

// Variables de string

let nombre; // Definir sin darle valor
nombre = 'martin'
nombre = "juan" // Es lo mismo ' que "

// Variables booleanas

let encendido = True;
encendido = False;

// Arrays (listas)

let nombres = ['martin', 'juan', 'gian'];
nombres[1] = 'eze'; // Reemplaza juan por eze, fijense que el primer elemento
                    // es el 0
nombres.length; // Te dice el largo del array (3)
~~~~~~~~~~~~~~~~~~~~~~~~~

Los objetos o funciones también se guardan en variables

Estructuras
===========

if
--

Para comparar usar ```==```, ```<=```, ```<```, ```!=```, etc.

Para usar **or** uno usa ```||```, el **and** es ```&&```, el **not** es ```!```

~~~~~~~~~~~~{.javascript}
if (edad >= 10 && edad < 60) {
    viejo = False;
}
else if (edad < 10) {
    viejo = False;
}
else {
    viejo = True;
}

if (viejo) { // No hace falta usar 'viejo == True'
    console.log('Estas viejo');
}
if (!viejo) {
    console.log('Estas joven');
}
~~~~~~~~~~~~~~~~~~~~~~~~~

for
---

Primero va el valor inicial (se debe usar ```let``` si es una variable nueva),
después la condición y al final lo que cambia en cada vuelta.

~~~~~~~~~~~~{.javascript}
for (let i = 0; i < 20; i++) {
    console.log(i);
}
~~~~~~~~~~~~~~~~~~~~~~~~~

while
-----

~~~~~~~~~~~~{.javascript}
while (cantPelotas > 0) {
    cantPelotas -= 1;
}
~~~~~~~~~~~~~~~~~~~~~~~~~

Funciones
=========

Reciben todos los argumentos que quieras y devuelve un valor.

Puede no recibir nada o no devolver nada.

~~~~~~~~~~~~{.javascript}
/**
 * Lo unico que hace es mostrar 'Hola'. No recibe ni devuelve nada
 */
function decirHola() {
    console.log('Hola');
}

/**
 * Calcula el promedio de dos números, recibe como argumento a dos números
 * y devuelve el resultado
 */
function calcularPromedio(n, m) {
    let promedio = (n + m) / 2;

    return promedio; // Devuelve una variable
}

let a = promedio(1, 4); // Llama a una función, le da los argumentos y guarda
                        // el resultado en 'a'
let b = promedio(6, 7);

console.log(a + b);
~~~~~~~~~~~~~~~~~~~~~~~~~

Objetos
=======

Primero se define una clase, que es un tipo de objeto. Después uno puede crear
todos los objetos que uno quiera.

La clase es en donde uno define cómo funciona el objeto. El objeto es una
instancia de una clase, que se guarda en una variable y se usa para lo que uno
quiere.

Los objetos adentro pueden tener variables y funciones. Si las variables y
funciones pertenecen a un objeto, se nombran en realidad atributos y métodos.

Cuando se usan atributos o metodos propios hay que usar ```this```. Cuando se
usa ```this``` no hace falta usar ```let```

~~~~~~~~~~~~{.javascript}
class Auto {

    /**
     * Esta función se ejecuta cuando se crea un nuevo auto
     */
    constructor(color, velocidad, marca) {
        this.ancho = 2;
        this.largo = 4;
        this.velocidad = 0;
        
        /*
         * No es lo mismo 'color' que 'this.color'
         * 'color' es una variable local a esta función, la variable del objeto
         * es 'this.color'
         */
        this.color = color;

        if (velocidadMaxima > 200) {
            velocidadMaxima = 200; // Limitar velocidad máxima
        }
        this.maxVel = velocidadMaxima;

        this.marca = marca;
    }
    
    /**
     * Esta funcion acelera al auto cambaindo una variable
     */
    acelerar() {
        this.velocidad += 10;
        if (this.velocidad > this.maxVel) {
            this.velocidad = this.maxVel; // Limitar velocidad máxima
        }
    }

    frenar() {
        this.velocidad += 10;
        if (this.velocidad < 0) {
            this.velocidad = 0; // Limitar velocidad minima
        }
    }
}

autoDelMartin = new Auto('rojo', 180, 'chevrolet'); // Crear un auto
autoDelNano = new Auto('gris', 80, 'ford'); // Crear otro auto

autoDelMartin.acelerar(); // Ejecutar funciones del auto

autoDelMartin.color = 'azul'; // Usar variables del auto
~~~~~~~~~~~~~~~~~~~~~~~~~
