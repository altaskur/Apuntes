# FS

## Definición

Este módulo nos permite interactuar con el sistema de archivos.

```JavaScript
import { fs } from 'node:fs';
```

## Métodos

### readdirSync()

Devuelve el contenido del archivo de manera asíncrona.

```JavaScript
readFileSync('directoryPath');
```

## lstatSync()

Devuelve información sobre el enlace simbólico de la ruta.

```JavaScript
 fs.lstatSync(filePath)
```

## isDirectory()

Devuelve un booleano, si la ruta es un directorio.

```JavaScrip
fs.lstatSync(filePath).isDirectory()
```

## existsSync()

Devuelve un booleano si el directorio o archivo de la ruta existe.

```JavaScript
existsSync('/etc/passwd')
```

## renameSync()

Renombra el archivo de la ruta seleccionada PERO, si el archivo existe lo reescribe.

```JavaScript
 fs.renameSync(oldpath, newpath);
```
