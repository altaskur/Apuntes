# Definición 
Este módulo proporciona métodos y propiedades con referencia al sistema operativo

```
const os = require('node:os');
```

# Propiedades

## platform()
Nos devuelve en forma de string la plataforma del sistema operativo.
Retorna los valores 'aix', 'darwin', 'freebsd','linux', 'openbsd', 'sunos', and 'win32'.

## homedir()
Devuelve en forma de string la ruta del directorio home del usuario.