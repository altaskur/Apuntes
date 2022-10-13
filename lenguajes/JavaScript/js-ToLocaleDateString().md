# Definición

El método toLocaleDateString() nos devuelve un string del objeto [js-Date()](https://github.com/altaskur/Apuntes/blob/main/lenguajes/JavaScript/js-Date().md), formateado al idioma y forma especificada.

[Más detalles](https://tc39.es/ecma262/multipage/numbers-and-dates.html#sec-date.prototype.tolocaledatestring) * Enlace externo a Ecma International

## Sintaxis

date().toLocaleDateString(`idioma`, {opciones});

## Idiomas

Usa las etiquetas de lenguaje de  [[BCP-47]].

Exceptuando:

* "numberingSystem" Sistema numérico.

 > “arab", "arabext", "bali", "beng", "deva", "fullwide", "gujr", "guru", "hanidec", "khmr", "knda", "laoo", "latn", "limb", "mlym", "mong", "mymr", "orya", "tamldec", "telu", "thai", "tibt".

* "calendar" Formato de calendario.

> “buddhist", "chinese", "coptic", "ethiopia", "ethiopic", "gregory", "hebrew", "indian", "islamic", "iso8601", "japanese", "persian", "roc".

## Estilos

El estilo de los días `"dateStyle"` y las horas  `"timeStyle"` se clasifican en:

* "full"
* "long"
* "medium"
* "short"
* "weekday"

## Opciones

* era

> "long" // Anno domini
> "short" // AD
> "narrow" // A

* year

> "numeric" // 2020
> "2-digit" // 20

* month

> "numeric" // 1
> "2-digit" // 01
> "long" // Enero
> "short" // Ene
> "narrow" // E

* weekday

> "long" // Lunes
> "short" // Lun
> "narrow" L

* day

> "numeric" // 1
> "2-digit" // 01

* hour

> "numeric" // 1
> "2-digit" // 01

* minute

> "numeric" // 1
> "2-digit" // 01

* second

> "numeric" // 1
> "2-digit" // 01

* timeZone

 > Usa el formato de tiempo de [IANA](https://www.iana.org/time-zones)

* timeZoneName

  >  “long" // (e.g., Pacific Standard Time)
  >  “short" // (e.g., PST)

* localeMatcher
* hour12
* hourCycle
* formatMatcher

## Ejemplos

```JavaScript
let date = new date();
let options =
{
    weekday: 'long',
    year: 'numeric',
    month: 'long',
    day: 'numeric',
    hour: '2-digit',
    minute: '2-digit',
    timeZone: 'UTC',
    timeZoneName: 'long'
};

console.log(date.toLocaleDateString('de-DE', options));

// Sonntag, 5. Juni 2022 um 17:13 Koordinierte Weltzeit

console.log(date.toLocaleDateString('es-ES', options));

//  domingo, 5 de junio de 2022, 17:12 tiempo universal coordinado
```
