# setInterval()

El método permite ejecutar una porción de código, cada x tiempo determinado.
Para que la función pueda ser detenida con el método clearTimeout(), tiene que estar declarada bajo una variable o constante.
El siguiente ejemplo está bajo una [[js-Funcion-flecha]], pero puede ejecutarse, llamando a otra variables, métodos y funciones.

## Ejemplo

``
Función flecha:
let contador =  window.setInterval( () => {
    // Porción de código
});

Función:
let contador = window.setInterval( function altasFuncion() );

Variable:
let contador = window.setInterval( altasVariable );
``

### Relacionados

* [[js-clearTimeout()]]
* [[js-Funcion-flecha]]
