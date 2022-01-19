# Resumen 2: Introducción JavaScript

Contiene temas como:

* Introdución a JavaScript
* Variables 
* Tipos de datos 
* Operadores
* Objetos globales
* Introducción a las funciones
* Control de flujo

El lenguaje de programación __JavaScript__ fue creado para en un principio para en _front-end_, es decir la parte estética de una página web, en la actualidad, por diversas  es el lenguaje de las páginas web. 

## Variables

Es un sistema de almacén donde puedo nombrar un _variable_ y asignarle valores excepto unas palabras universales que no se pueden asignar. Se estructura, tipo de variable `var`,  `cont`,  `let` + nombre = dato queremos asignarle, se escribe de la siguiente forma:

```js
var nombre_de_la_variable = 'tipo de dato';
```

### var

La variable `var`, es una variable que define de un nombre que puedes asignar a cualquier tipo de cosa, esta variable puede ser pisada si se asigna un nuevo dato. Por ejemplo tenemos:

```js
var deudas = 'problemas';
// deudas
// 'problemas'
```
### const

La variable `const`, es la variable que asigna de una nombre de una variable a constante, es decir es inamovible, por ejemplo tenemos:

```js
const áreaCir = "2rad";
// áreaCir
// "2rad"
```

### let

La variable `let`, es una variable este se usa en casos de que declare un dato en limitado alcance __scope__ al bloque. Es muy parecida a _var_, pero en su caso es un uso más global.

```js
let fav = 'Henry Curso', lov = 'Java Script';
```

## Tipo de datos

### Strings

Una __strings__ es valor en texto guardado, este es el tipo de dato está delimitado entre comillas `""` o como llamamos en la lengua castellana el apóstrofe `''`, como los ejemplos antes mostrados.

### Numbers

Este es el tipo de dato que se utiliza como número tanto negativo como positivo, este no tiene comillas porque pasa a ser una strings, se pasa a decimales con el punto `.`, la coma tiene otros usos.

```js
const PI = 3.1416;
PI
// 3.1416
```

### Boolean

Los __booleanos__ se utiliza con el fin de arrojar 2 tipos de resultados es el principio del lenguaje binario 0 y 1 o _verdadero o falso_, estos nos referimos a __true__ quiere decir de lo anterior es verdadero;  o __false__ quiere decir de lo anterior es falso. 

```js
var laAnteriorFraseEsFalsa = 'True';
// laAnteriorFraseEsFalsa
// True
```

### null

El término nulo es el resultado de nada, no representa un cero, ni una string vacía, no representa nada.

### undifine

El término indefinido es el resultado se arroja una variable que no tiene ningún tipo de dato, algo que puede definirse.

## Operadores

Los operadores se utilizan en java script básicamente como los símbolos matemáticos (`+`, `-`, `*`, `/`, `%`). Sin embargo, existen otros que no se asemejan a las matemáticas como las conocemos.

El operador módulo `%`, este operador matemático se usa divide los dos números y devolver el resto. 

El operador igual `=` se emplea para asignar una variable a un dato, el operador doble igual `==`, es completamente diferente a su antecesor este es un método de comparación que arroja un resultado booleano, y el operador triple igual `===`, no utiliza el método de comparación igual, este retorna _false_ si los datos son diferentes.

Los operadores `<`, `>`, `<=`, `=>`... Se asemejan a los booleanos, ya que utilizan el método de comparación determinando un estado de _true_ o _false_.

Estos se puede emplea en valores _numbers_ como en _strings_, como por ejemplo:

```js
const PI = 3.1416;
PI + 15;
// 18.1416

21 % 6;
// 3

'milhouse' = 1;
milhouse
// 1

'' == 0;
// True

'' === 0;
// False

1 > 1
// False

1 >= 1
// True
```

## Objetos globales

En java script existen una serie de objetos que existen en javascript y no se puede asignar un valor.

### console.log()

El `.log` es un objeto que sirve para grabar una secuencial de datos. Para grabar se usa `.log()` entre __paréntesis__ para delimitar los datos.

```js
console.log('Hola mundo');
// Hola mundo
```

### math.pow()

El `.pow` retorna la base elevada al exponente.

```js
Math.pow(3,3);
// 27
```

### math.round(), math.floor() y math.ceil()

El `Math` tiene métodos para redondear un número; `.round` redondea un número entero más cercano; `.floor` siempre redondeará un número al número entero más aproximado hacia abajo. `.ceil` tiene tendencia a redondear al número entero más cercano hacia arriba.

```js
Math.round(6.45);
// 6
Math.floor(6.999);
// 6
Math.ceil(6.0001);
// 7
```

### .length()

Este tiene relación al tipo de dato de _strings_, el `.length` retorna la cantidad de características de la cadena.

```js
var nombrePerro = 'Firulais';
console.log(nombrePerro.length); 
// 8
```

## Introducción a las funciones

### Funtion

Se utiliza para agrupar código, e imprimir en otras líneas la  función, nos permite de una forma rápida, copiar el código y reescribirlo en otra parte. La anatomía de una función:

```js
funtion nombreDeLaFunción (argumentos) {
    // código
}

let nombreFunción = funtion (argumentos) {
    // código
};

const nombFunción = (arguemntos) => {
    // código
};
```

Podemos invocar una función escribiendo el nombre de la función y poniendo los paréntesis, sin olvidar poner el punto y coma.

```js
funtion saludar(nombre) {
    console.log('Hola + nombre');
}

saludar();
// Hola

saludar(Tomas);
// Hola Tomas
```

### Argumento

Significa copiar un variable dentro de una función, que solo cuando utiliza la función tomara validez esa variable, de lo contrario no. Está delimitado después del nombre de la función entre `()` y cada argumento está separado con una coma `,`.

```js
function carateristicas(modelo, marca) {
    console.log("Los modelos que tenemos en stock " + modelo);
    console.log('de la marca ' + marca);
}
carateristicas('2021', 'Tesla');
// Los modelos que tenemos en stock 2021, de la marca Tesla
```

### Return

Al asignar la palabra clave __return__ traducción literal del español de retornar la función, lo que hacer `return` es devuelve un valor, que será el resultado de una función que se ejecute, en el caso de que el resultado sea verdadero retorna y corta la función aunque siga el código, si es falso puede seguir los siguientes parámetros.

```js
function areaCir (r) {
    return 3.1416 * (r*r);
}
var resultado = areaCir(4)
// El área del círculo es: 50.2656
```

## Control de flujo

Lo que nos permite control de flujo es poder hacer preguntas de comparación binaria, es decir true o false, y ejecutar dividir y clasificar nuestro código según ciertas condiciones.

Se estructura de la siguiente forma:

```js
if (condición) {
    // Ejecuta el código si cumple con la codición
} else if (condición) {
    // si no, sí cumple la condición ejecuta este otro código
} else {
    // si no ejecuta este código
}
```

### if, else if, if

Torna como un condicional, como él en lenguaje usamos la palabra _Si_, lo que nos permite es comparar una condición, es decir, si la respuesta en código binario, en el `if` si la respuesta es _true_ se ejecuta el código; `else if` si no es la respuesta if, entonces ejecuta este otro código, `else` si la respuesta no es ninguna de las anteriores, entonces ejecuta este código.

```js
function excesoDeVelocidad (kilómetros) {
    if (kilómetros > 60) {
        conlose.log('Tienes infracción');
    } else if (kilómetros < 60) {
        console.log('Infracción no cometida');
    } else {
        console.log('Error de detección');
    }
}
excesoDeVelocidad(88);
// Tienes infracción
excesoDeVelocidad(49);
// Infracción no cometida
excesoDeVelocidad();
// Error de detección
```

## Scope

El _alcance_ es el término que se emplea al alcance determinado de accesibilidad del __lexical statenmet__, es decir, si llama a una variable o función dentro de su lexical statenmet y no la encuentra definida, busca en el __lexical statement madre__, repite este proceso hasta buscar toparse con el __global context__, dicho proceso es llamado __scope__. En el caso de no ser encontrado determina undefine, si es una variable no retorna el valor que tiene dicha variable, en cambio, si es una función la invoca.