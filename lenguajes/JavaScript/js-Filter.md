# Definición

array.filter() nos devuelve un nuevo array, (no modifica el original)
creando una copia con las mismas referencias del objeto principal, denominada [shallow copy]

## Sintaxis

```JavaScript
// Funciones flecha
playersNickname = GAME_SETTINGS.players.filter((player) => player.nickname);
```

```JavaScript
// Funciones Callback
function isPrime(number){
   for (let i = 2; num > i; i++) {
    if (num % i === 0) {
      return false;
    }
  }
  return num > 1;
}
const array = [-3, -2, -1, 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13];
array.filter(isPrime)
```

### Relacionados

* [js-array-map](https://github.com/altaskur/Apuntes/blob/main/lenguajes/JavaScript/js-array-map.md)
* [js-some]
* [js-Arrays](https://github.com/altaskur/Apuntes/blob/main/lenguajes/JavaScript/js-Arrays.md)
