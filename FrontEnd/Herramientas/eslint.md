# Eslint

Es una herramienta que te permite mantener tu código limpio y sin errores.

@Gitlazo: Normalmente el linter se pasa obligatoriamente en los procesos de CI/CD, para que no suba código "no linteado"

## estilos recomendados

* Backend
  * GOOGLE
  * https://www.npmjs.com/package/eslint-config-google

* Frontend
  * Airbnb (React)

## Instalación

```bash
npm install eslint --save-dev
```

## Incio del proyecto

```bash
npx eslint --init
```

## Configuración

Para trabajar con TypeScript tenemos que añadir una configuración extra.

```json
  "parserOptions": {
    "project": ["./tsconfig.json"] // Specify it only for TypeScript files
  },
  "parser": "@typescript-eslint/parser"
```

## Ejecución

`--ext .js` establece que se monitoren los archivos acabados en .js

```bash
npx eslint  . --ext .js
```

Aunque una buena práctica es introducir el comando en el apartado de
scripts de node.

```json
"scripts": {
  "lint": "eslint .  --ext .js"
},
```

Podemos hacer que automáticamente corrija los errores

```bash
npm run lint-fix
```

### Vscode

Podemos establecer a vscode que al guardar el archivo ejecute Eslint
tal y como lo hemos configurado, para ello añadimos esta opción al archivo de configuración de vscode.

```json
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  },
```
