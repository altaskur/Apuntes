# clearTimeout()

Permite cancelar una acción relativa como la creada en [[js-setInterval()]].
Para ello debemos llamar a la identificación asociada a la función.

## Ejemplo

``
setInterval(contador());

Caso práctico:

document.querySelector("input[type=button]").addEventListener('click', () =>{
    window.clearTimeout(contador);
});
``

### Relacionados

* [[js-setInterval()]]
