# TypeScript

## Tipos de datos

* string
* number
* boolean

```ts
let myString: string = "mi primera variable tipo string";
```

* array

```ts
let obj: any {};
let arr: number [];
```

* Combinaciones de tipos

```ts
// Varios tipos
let obj: string | number []; // obj["hola",2];
let arr: string | number []; // arr["hola",2];
```

## Funciones

Se pueden tipar tanto sus parámetros como la salida del mismo.

```ts
function myFunction(data:string):number {}
```

### Recursividad en funciones

Se deben declarar los retornos incluso cuando le estamos pasando una llamada
a si misma.

```ts
function checkWeather(weather:string):string {
    if(weather != "raining"){
        return checkWeather(weather);
    } else {
        return "🌧☔Its raining!";
    }
}
```

## Constructor vs  Método - String() vs .toString()

* Constructor
  * El constructor al final lo que devuelve es el objeto que le estás pasando
  * No devuelve un error, sino devuelve que `null`.
  * Funciona con los primitivos y no con las clases modificadas.
  * Es el equivalente a usar `value + '';`
* Método
  * Nos devuelve un error de tipo.
  * permite modificar las clases, modificadas
  * ⚠ Prioridad de uso antes que el método

```ts
var value = null;
String(null); // "null"
value.toString(); // TypeError
```

## Promesas

Las promesas nos permiten hacer que el código espere a que estás se resuelvan hasta continuar
su camino y reciben un parámetro como función.

El callback de las promesas se le pasan dos parámetros , resolve y reject, los cuales sirven para salir de ellos de forma exitosa o errónea respectivamente.

```ts
new Promise ((resolve, reject) => {}).then((){});
```

### Bonus

Una función delay() como en c# [@LuisLLamas_es](https://github.com/luisllamasbinaburo)

```Ts
function delay(ms: number) {
  return new Promise((resolve) => setTimeout(resolve, ms));
}
```

## Módulos

Nos permite gestionar el proyecto en ficheros independientes (Módulos)

Formas:

1. CommonJS

    La forma que usa node-js

    ```js
    const state = require('./state.cjs');
    module.exports.state = state;
    ```

2. AMD

    la forma adaptada a partir de ECMAScript ES2015, común en
    JavaScript y TypeScript

    ```js
    import { magicNumber } from "./constants.js";
    export const magicNumber = 42;
    ```

---

## ✨ Agradecimientos

TDarom, [@PiterMcFlebor](https://github.com/pitermcflebor) y [@LuisLLamas_es](https://github.com/luisllamasbinaburo) por echarme una mano a entender todo esto.
