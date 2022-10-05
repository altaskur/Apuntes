# Definición

Una de las entradas más extensas de la wiki, iré completándola según se trabaje en los proyectos.

El objeto Date(), devuelve una fecha, de un momento determinado, desde 1 de Enero de 1970 UTC, hasta ~ 20 de Abril de 271821 a. e. c.
Por lo tanto tiene una limitación de ±8,640,000,000,000,000 milisegundos.
Trabaja en milisegundos.

## Métodos

### new Date()

Nos devuelve la fecha, en forma de objeto en formato de hora local, es decir la hora del cliente incluida su zona horaria.

``
let today = new Date(  );
``

3## .getDate()
Nos devuelve el día del mes del objeto Date() en formato 1 - 31.

``
let day = today.getDate();

console.log(day); //  3
``

### .getMonth()

Nos devuelve el mes del objeto Date() en formato 0-11.

``
let month = today.getMonth();

console.log(month); // 8
``

### .getFullYear()

Nos devuelve el año del objeto Date() en formato 1000 y 9999.

``
let year = today.getFullYear();

console.log(day); // 2022
``

### .[[js-toLocaleDateString()]]

Nos devuelve un [[String]] al idioma y la forma especificada, ver [[toLocaleDateString()]

## Relacionados

* [[js-toLocaleDateString()]]
* [[js-String]]
