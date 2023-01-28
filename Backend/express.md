# Express-JS

Express es un framework de node-js que nos permite levantar un servidor web.

## Uso de Middleware

Los middleware se ejecutan antes de que llegue la petición HTTP al manejador de rutas
o antes de que un cliente reciba la respuesta.

### Middleware que más uso

> 1. Morgan
> 2. Body-parser
> 3. Session
> 4. CookieParser

#### Morgan

Nos permite ver los logs de nuestro servidor, tanto de peticiones como de otros datos importantes.

#### BodyParser

Nos permite interpretar el req.body

#### Session

Nos permite almacenar sesiones en el lado del servidor.

#### CookieParser

nos permite crear y usar cookies

## Rutas

Para poder detectar las rutas de express usaremos el método app.get()

```JavaScript

// ruta raíz
app.get('/', (req, res)=>{

});

// ruta adicional
app.get('/quack/test', (req, res)=>{

});
```

### Parámetros

Tenemos dos tipos de datos las opciones (query's) y los parámetros.

Query's

```javaScript

// de esta manera las query's las pasamos con este formato
// http://localhost/quack?mode=dark&user=altaskur

app.get('/quack', (req, res) => {
  const { quack } = req.body;
    const { mode } = req.query;
    const { user } = req.query;
  res.send({
    user,
    mode
  });
});

// Las acciones las obtendríamos de esta manera:
// Este ejemplo es una combinación de ambas tanto de acción como de parámetro
// http://localhost/quack/altaskur?mode=dark

app.get('/quack/:user', (req, res) => {
  const userId = req.params.user;
  const { mode } = req.query;

  res.send({
    userId,
    mode,
  });
});
```

## Plantillas

Express funciona co una gran amplitud de motores de plantillas [Motores soportados](https://expressjs.com/en/resources/template-engines.html)

Las plantillas se utilizan para generar contenido dinámico en una página web

## Consultas

### POST

```js
//Ejemplo: POST http://localhost:8080/item
app.post('/item', function(req, res) {
   var data = req.body.data;
   res.send('Add ' + data);
   console.log('Add ' + data);
});
```

### UPDATE

```Js
//Update
//Ejemplo: PATCH http://localhost:8080/item/10
app.patch('/item/:id', function(req, res) {
   var itemId = req.params.id;
   var data = req.body.data;
   res.send('Update ' + itemId + ' with ' + data);
   console.log('Update ' + itemId + ' with ' + data);
});
```

### DELETE

```js
//Delete
//Ejemplo: DEL http://localhost:8080/item
app.delete('/item/:id', function(req, res) {
   var itemId = req.params.id;
   res.send('Delete ' + itemId);
   console.log('Delete ' + itemId);
});
```

#### Agradecimientos

* [luisllamas.es](https://www.luisllamas.es/montar-un-api-rest-con-nodejs-y-express/)

* Seguidres: Gringobsts
