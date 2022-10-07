# Definición 
Provee utilidades para trabajar con archivos y rutas de directorios.

```
const path = require('node:path');
```


# Propiedades

## path.extname(path)
Devuelve la extensión que se localiza al final del último "." de la ruta.

Pero si el "." está situado al principio de la ruta este devuelve un string vacío y si después del "." no hay nada, este devolverá un ".".

### Ejemplo
```
path.extname('index.coffee.md');
// Returns: '.md'


path.extname('index.');
// Returns: '.'


path.extname('.index');
// Returns: ''


path.extname('index');
// Returns: ''
```


## path.isAbsolute(path) 
Devuelve si la ruta es absoluta

## path.join(paths)
Devuelve a partir de segmentos una ruta ya normalizada, es decir, adaptada a cada sistema operativo.

### Ejemplo
```
path.join('/foo', 'bar', 'baz/asdf', 'quux', '..');

// Returns: '/foo/bar/baz/asdf'
```

