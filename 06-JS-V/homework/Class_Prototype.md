Lección 5: Clases y Prototipos

- Clases e instancias
- key `new`
- Prototype
- Herencia

## Class

Una **class** es una plantilla para la creación de objetos de datos según un modelo predefinido. En un lenguaje orientado a objetos como (Java o C#), aunque en JavaScript no posee un "verdadero" sistema de clases.

### Función Constructora

Esta función permite fabricar objetos, se pueden identificar porque el en nombre de la función comienza con la letra mayúscula. Es decir, cuando se crea una función constructora, se crea una plantilla, eso se llama una **class**, con esa nueva clase, clasificando en **keys** tienes una instancia de **object**, con esto ya tienes una fábrica de instancia de objetos.

```JS
function Car (marca, cv, color) {
    this.marca: marca,
    this.cv: cv,
    this.color: color
}
const audi = new Car('audi', 2200, 'negro');
audi;
// Car { marca: 'audi', cv: 2200, color: 'negro' }
```

## new

De instancia de manera pseudo-clásica, usando la palabra clave **new**, puede tomar como argumento, añadimos nombre a con la primera letra en mayúscula. El método new, por dentro ópera de la siguiente forma: origina un objeto, cambia los valores de this por objetos y finalmente retorna el objeto.

```JS
const object = {};

function Car (marca, cv, color) {
    object.marca: marca,
    object.cv: cv,
    object.color: color
}
Car('audi', 2200, 'negro').bind(object); // el this de la funtion 'Car' = 'object'

return object;
```

## Prototype

Ah nivel de consumo de memoria, la creación de funciones y sus respectivos métodos, puede dejar miles de objetos, por tal motivo, las clases tienen maneras de establecer métodos **prototype**, en sí lo que hace es una declaración de un objeto para implementar una herencia basada en prototipos. El polimorfismo es la capacidad de unos objetos distintos puedan referirse al mismo llamado de acuerdo con su herencia.

```JS
Car.prototype.query = function () {
    return 'stock ' + this.marca + 'de color ' + this.color; // object heredados de la funcion constructora
}
```

## Herencia

Ya sabemos que JavasScript el **prototype** puede heredar de su constructor métodos y objetos, además podemos heredar otros constructores la cual pueden ser variantes de constructor padre.

```JS
function Bike (marca, cv, color) { // metodo heredado de la funcion padre
    object.marca: marca,
    object.cv: cv,
    object.color: color
}
const audi = new bike('audi', 2200, 'negro'); // object heredados de la funcion constructora
```
