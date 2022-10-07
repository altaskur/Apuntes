# clearTimeout()

Permite cancelar una acción relativa como la creada en [js-setInterval()](https://github.com/altaskur/Apuntes/blob/main/lenguajes/JavaScript/js-SetInterval().md).
Para ello debemos llamar a la identificación asociada a la función.

## Ejemplo

```JavaScript
setInterval(contador());

Caso práctico:

document.querySelector("input[type=button]").addEventListener('click', () =>{
    window.clearTimeout(contador);
});
```

### Relacionados

* [js-setInterval()](https://github.com/altaskur/Apuntes/blob/main/lenguajes/JavaScript/js-SetInterval().md)
