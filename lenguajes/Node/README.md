# Definición

Es un entrono de ejecución de JavaScript, construido con el motor V8, un proyecto OpenSource desarrollado por Google y escrito en C++ e implementa [ECMAScript]  y [WebAssembly].

## Módulos nativos

* [os](https://github.com/altaskur/Apuntes/blob/main/lenguajes/Node/os.md)
* [fs](https://github.com/altaskur/Apuntes/blob/main/lenguajes/Node/fs.md)
* [path](https://github.com/altaskur/Apuntes/blob/main/lenguajes/Node/path.md)

## Módulos personalizados

Nos permite gestionar el proyecto en ficheros independientes (Módulos)

Formas:

1. CommonJS

    La forma que usa node-js

    ```js
    const state = require('./state.cjs');
    module.exports.state = state;
    ```

2. AMD

    la forma adaptada a partir de ECMAScript ES2015, común en
    JavaScript y TypeScript

    ```js
    import { magicNumber } from "./constants.js";
    export const magicNumber = 42;
    ```

    * Problemas al pasar a la forma AMD

      1. "No existe __dirname"

         Para recuperar esta variable tenemos que recuperar desde `fileURLToPath`.

         ```js
         import path from "path";
         import { fileURLToPath } from "url";
         const __dirname = fileURLToPath(import.meta.url);
         ```

### Configuración

Cómo he indicado más adelante la forma predeterminada de node es la Common-js pero
podemos cambiarlo desde el package.json introduciendo la sentencia `"type": "module",` en alguna
parte alta del JSON.

```json
  "name": "Apuntes",
  "version": "0.1.0",
  "description": "example module",
  "main": "./src/main.js",

  "type": "module",
```
