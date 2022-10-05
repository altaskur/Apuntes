# Definición

Se considera un atajo del operador condicional [[If]].

Por lo tanto si la condición se resuelve con el [[boleano]] True, el resultado pasará a ser la primera expresión por lo contrario si es False pasará a ser la segunda expresión.

## [ Notas ]

Estas pueden estar anidadas, es decir puedes usar un ternario como expresión de otro.
No tienen porque estar dentro de una variable.

los ternarios tienen implícitos el return

## Sintaxis

condición ? primera expresión : segunda expresión ;

### Ejemplos:

``
let numero = 5;
let ternario = numero > 0 ? "es mayor que 0" : "es menor que 0";
console.log(ternario); // es mayor que 0

Anidación

let numero1 = 9;
ternario =  numero1 == 4 ? numero = 6 ? "Es 4 y 6 " : "Sólo es 4" : "No es 4";
console.log(ternario); // No es 4

Return implícito

    // Código del proyecto (https://github.com/altaskur/Buscaminas)[buscaminas]

    // if ( flags < 0 ) {
    //     flags = 0;
    //     return false;
    // }

    flags < 0 ? (flags = 0, false ) : null;

``

### Relacionados

* [[js-Funcion-flecha]]
* [[If]]
* [[js-Boleanos]]
