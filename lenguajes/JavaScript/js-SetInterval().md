# setInterval()

El método permite ejecutar una porción de código, cada x tiempo determinado.
Para que la función pueda ser detenida con el método clearTimeout(), tiene que estar declarada bajo una variable o constante.
El siguiente ejemplo está bajo una [js-Funcion-flecha](https://github.com/altaskur/Apuntes/blob/main/lenguajes/JavaScript/js-Funcion-flecha().md), pero puede ejecutarse, llamando a otra variables, métodos y funciones.

## Ejemplo

```Javascript
Función flecha:
let contador =  window.setInterval( () => {
    // Porción de código
});

Función:
let contador = window.setInterval( function altasFuncion() );

Variable:
let contador = window.setInterval( altasVariable );
```

### Relacionados

* [js-clearTimeout()](https://github.com/altaskur/Apuntes/blob/main/lenguajes/JavaScript/js-ClearTimeout().md)
* [js-Funcion-flecha](https://github.com/altaskur/Apuntes/blob/main/lenguajes/JavaScript/js-Funcion-flecha().md)
