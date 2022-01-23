# Lección 4: Bubles for y Arrays

- Introducción arrays
- Areglos con .legth(), .push(), pop(), .Unshift() y shift()
- For de Arrays

## Arrays

Se usan para armar base de datos, podemos agrupar tanto spressions como statemets. Los arreglos se nombre con el símbolo de corchetes `[]`, así mismo se invocan con el dato 0, 1, 2... definido en el array. Por ejemplo tenemos:

```js
var array ['hola', 24, function () { console.log('chao') }, null, ['leo', '1', 62]]

array [0]
// "hola"

array [2]
// "chao"

array [1]
// 24

array [24]
// undifined
```

Además en las streans podemos contar el número de letras dentro de las `" "` de un array. En cambio los números no tiene la propiedad `.length`. Se puede explicar:

```js
letras []
// ["hola", 24,]

letras [0][1]
// 'h'

letras [0][2]
// 'o'

letras [0][2]
// 'l'

letras [0][2]
// 'a'

letras [1]
// undefined
```

Se puede definir de diferentes formas:

```js
var array ['hola', 24, function () { console.log('chao') }, null, ['leo', '1', 62]];
// Definicion literal

var lista [];
// Creamos un array llamado lista
lista [0] = 'producto1';
// En posicion 0 del arra agregue 'producto1'
lista [9] = 'producto2';
// En posicion 9 del arra agregue 'producto2'

lista [];
// ['Producto1', <8 items undefine>, 'producto2']
// el la lista aparece lo que se definio y lo que falta ya que no es defnido el arreglo 1, 2, 3, 4, 5, 6, 7, 8

lista [0] = 'arreglo pisado';
lista [];
// ['arreglo pisado', undefine, 'producto2']
```

## .length()

Este puede también ser usado para calcular el número de elementos del arreglo, con la propiedad `length`. Es decir:

```js
array []
// ["hola", 24, function () { console.log('chao') }, null, ['leo', '1', 62]]

array.length
// 4

array[4].length
// 3
```

### .push()

Lo que hace el `.push()` es por medio de un argumento, agregar una nueva expresión al último eslabón de la matriz.

```js
letras []
// ["hola", 24]

letras.push(undefine);
//undefine

letras []
// ["hola", 24, undefine]
```

### .pop()

el `.pop()` a lo contrario del anterior, se utiliza para sacar el último elemento de la matriz.

```js
letras []
// ["hola", 24, undefine]

letras.pop();
// ["hola", 24]
```

### .unshift()

Opera de la misma manera que push, su diferencia es al colocar un elemento, el .push() agregar una expresión al final, `.unshift()` agregar una expresión al principio de la matriz. Por ejemplo:

```js
array []
// ["hola", 24, function () { console.log('chao') }, null, ['leo', '1', 62]]

array [0]
// "hola"


array.unshift(undefine);
// [undefine, "hola", 24, function () { console.log('chao') }, null, ['leo', '1', 62]]

array [0]
// undefine
```

### .shift()

Opera de la misma manera de pop, radica en que `.shift()` elimina el primer elemento de la matriz, de lo contrario que pasa con .pop. Tenemos como ejemplo:

```js

array []
// [undefine, "hola", 24, function () { console.log('chao') }, null, ['leo', '1', 62]]

array.shift();
// undefine

array []
// ["hola", 24, function () { console.log('chao') }, null, ['leo', '1', 62]]
```

## loops de arrays

Los bucles puede ser un complemento para agregar arreglos en tu código, cuando es necesario utilizar repetitiva modificación de un array, es útil usarlos

```js
var list = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9];
// definimos arreglo list

for (i = 0; i < list.length; i++) {
	console.log(list[i]);
}
// 0, 1, 2, 3, 4, 5, 6, 7, 8, 9

while (list.length < 3) {
	console.log(list.pop());
}
// Eliminara todos los de la lista hasta llegar a tener 3 ítems
// 0, 1, 2 solo para la ejecución al ser menor de 3
```
