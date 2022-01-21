# Lección 3: flujos de control, operadores de comparación y Bucles

* Conceptos Expressions y statements
* Veracidad
* Flujos de control
* Operadores lógicos
* Bucles `for`

## Expressions

es un __expreseión__ que puede ser evaluado de un valor, es decir, es forzado arrojar un valor, las expresiones primarias se calsifican.

### Expresiones ariméticas

son expresiones que devuelven valor numerico.

```js
10 + 4;
// 14
```

### Expresiones de strings

Son expresiones que retornaa un valor en __string__.

```js
'Hola ' + 'bro';
// hola bro
```

### Expresiones lógicas

Son expresiones que resuelven a un valor __boleano__.

```js
1 > 1;
// false
```

### Expresiones de asignación

Esta se utiliza el operado `=` esta retorna valor asignado.

```js
a = 'Luis';
a + 'Perez';
// Luis Perez
```

### Expresiones side effects

Como ultimo tenemos expresiones con efectos secudarios, al ser evaluadas retorna el valor añadido.

```js
var contador = 1
contador++;
// 2
++contador;
// 0
```

## Statements

Los __statements__ o traducido en el español como sentencias son instrucciónes que JS puede ejecutar, crea una variable que el código puede ejecutar N catidad de veces. Se puede clasificar en:

### Declaration statemets

Este tipo de senntencia indica que declara con el una nueva variable

```js
var inocente;
// declaro la varaible inocente

function pruebas(evidencia1, evidencia2){
    // declaro la funcion de pruebas
}
```

### Function expersions

Este tiene similitudes con las de declaración, dependiendo del contexto y la interpretación.

```js
var homicidio = function(culpable, inocente) {
    // declara la varaible homicido y ejecuta una función por lo que lo combierte en statement
    // asigna en vez de una expresión, una función asi que pasamos function expressions
}

(function (){
    console.log('Life is live');
    // inediatamente invoca una expresion como función
})();
```

> Las funciones anonimas son las que no tienen nombre antes de los argumentos.

### conditional Statements

Estos __statements__ sirven para controlar el flujo del código sí cumple una las condiciones

```js
if (condición) {
  // ejecuta este bloque si condicion es true
} else if (condición2) {
  // ejecuta este bloque de código si condicion no es true y condicion2 es true
} else {
  // ejecuta este bloque de código si condición y condición2 no son true.
}
```

### Loops y Jumps

Los statements de bucles y saltos funcionan igual que los condiciones, pero para utilidades diferentes.

```js
// loops
while(condicion) { 
  // ejecuta este código mientras condicion sea true
}

for (let i = N; i < N; i++) {
  // ejecuta este bloque de código N cantidad de veces
}

// jumps

function () {
  return;  // se ejecuta la función y retorna un valor
}

for (let i = N; i < N; i++) {
  continue; // salta a la siguiente iteración del bucle;
  // desde acá no se ejecuta;
}
```

## Veracidad

Los valores __booleanos__, es decir, si es `true` o `false`. En JS la "coerción de tipo" es la forma de covertir cualquier dato y pasarlo a binario, que se lee en booleano, cada tipo de dato tiene una veracidad:

### Truthy

Se llaman a los datos que son forzados a `true`.

```js
true; // true
-1; // true
{}; // true
[]; // true
' '; // true
!!true; // true
function () {} // true
```

###Falsey

Se llaman a todos los datos que son forzados a `false`.

```js
''; // false
0; // false
undefined; // false
null; // false
!true; // false
```

## Operadores lógicos

## &&

AND se utiliza para comparar dos operadores que necesitan verificar si son verdaderos, _este ínicamente muestra verdadero si los 2 operadores son `true`, de lo contrario es muestra `false`_.

## ||

OR se utiliza de igual manera para comparar dos operadores que necesitan verificar si son falsos, _este únicamente arroja `false` si los dos opreadores son falsos, de lo contrario muestra `true`_.

## !

NOT es utilizado para negar el operador seleccionado, es decir, niega toda comparacioón en el que el operador sea verdadero.

## Don´t Repeate Yourself (DRY CODE)

###for

El bucle `for`, imprime un bloque de código N cantidad de veces, este posee una estructura:

```js
for (let x = N; x <= N; x++){
    // bloque de código
}
```

Esto quiere decir que `for` imprima bloque de código `(`nombre de la variable, que `x` empiece en `N` numero; que `x` pare cuando sea ` menor o igual` a `N` números; y `x` sume uno al anterior`)`.