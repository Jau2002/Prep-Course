# Lección 4: Objetos

- Fundamentos de objetos
- Propiedades
- Metodos

## Objetos

Los objetos dictan de ser muy parecidos a las array o matrices, para saber que es un objeto tememos que saber que se diferencia. El array es una agrupación de múltiples, en cambio los objetos sintetizan más la información de un solo elemento del array, así podemos almacenar más información sobre algo en específico. Los elementos usan llaves como forma de invocación `{}`, se separa con `:` la propiedad del valor y con una coma `,` se separa una propiedad entre otra. Podemos detallar que JavaScript casi todo son objetos, que son representados de diferentes formas.

```js
const nameObject = {
	key1: value1,
	key2: value2
};
```

### keys

Las `llaves` son lo que podemos identificar el elemento en el que está ubicado en el array, esta contiene un valor único y está identificado numéricamente (recordar que empieza desde cero: [0] [1] [2]...), y se escribe de la siguiente forma: NombreArray[Numero de elemento].

### Values

Los valores va muy arriegado con las keys, el `value` es el que queremos guardar en una clave dentro de un array, varias claves pueden tener el mismo valor, estas pueden agregar cualquier tipo de valor, streas, números, booleanos, matriz...

```js
const object = {
	key1: value1,
	keyN: valueN
};
// objeto ['key1']
// value1
```

## Propiedades

### Dot notation

Después de ya tener claves con su respectivo valor, se puede acceder llamando el nombre del objeto poner un punto y el nombre de la clave.

```js
object.key1;
// value1
```

### Bracket Notation

Este usualmente es utilizado al tener que recorrer un loop de una propiedad asignada, se puede utilizar los corchetes `[]` como elemento de una matriz, escribir la clave entre comillas:

```js
object['key1'];
// value1
```

### Eliminar propiedades

La palabra `delete` nos permite eliminar una propiedad del objeto que tengamos un valor:

```js

object.push = {
    keyDelete: valorBorrable;
}

object
{   key1: 'value1',
    keyN: 'valueN',
    llaveDelete: 'valorBorrable' }

delete objeto.propiedadDelete;
// propiedad eliminada

object
{   key1: 'value1',
    keyN: 'valueN' }
```

## Metodos

### For..in

El método `for in` normalmente utilizado para recorrer las keys de un objeto, es un método muy útil si no precisamos específicamente del **index** en el recorrido for tradicional. Este método NO es apto para usarlo en arrays.

```JS
for (const key in object) {
    console.log(key);
    console.log(object[key]);
}
// key1
// key2

// value1
// valueN
```

### This

la palabra clave `This` es para referenciar un objeto dentro de un objeto o propiedad, se puede ejecutar código modificado fuera del objeto englobando todo el objeto, es decir, this apropia de una propiedad, haciendo que el valor de dicha propiedad sea completamente global. Por ejemplo tenemos.

```js
objeto
{   key1: 'value1',
    keyN: 'valueN' }

object.push = keyCambiable: funtion () {
    console.log('estado actual key cambiable' + this.key1)
}

object.keycambiable = 'key Alterada';
// La key fue cambiada

objeto.keycambiable ();
//estado actual de key cambiale propiedad Alterada
```
