# Arrays

## Definición

Es un objeto que contiene una lista de objetos.
Lo que nos permite acceder a los objetos de la lista y recorrerlos.

## Sintaxis

```JavaScript
    let lista = [elemento0, elemento1,elemento2];

```

## Ejemplos

```JavaScript
    let lista = ['huevos','pan','leche'];
    console.log(lista[0]); // huevos
    console.log(lista[2]); // leche
    console.log(lista); // huevos, pan, leche
```

## Métodos

### pop()

Altera el array, eliminando y devolviendo el último elemento.

#### Ejemplo

```JavaScript
let lista = ['huevos', 'pan', 'leche'];

let ultimoElemento = lista.pop();

console.log(ultimoElemento) // leche
console.log(lista) // huevos, pan

```

### push()

#### Relacionados

* [Objetos]
* [If]
* [Boleanos]
