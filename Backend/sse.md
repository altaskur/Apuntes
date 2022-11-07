# SSE

## Definición

Server Send Server, es un protocolo de comunicación de servidor - cliente, unidireccional funciona mediante HTTP y
no requiere de confirmación, ni reenvia los paquetes perdidos, es decir mantiene un canal abierto de notificaciones en tiempo real del servidor al cliente.

Para ampliar conocimientos puedes ver [RFC8895](https://www.rfc-editor.org/rfc/rfc8895#name-server-push-server-sent-eve).

## Servidor

Estableceremos los siguientes parámetros del lado del servidor:

1. Headers

    * "Content-Type" -> definimos el contenido del mensaje como "event-stream".
    * "Connection" -> mantenemos la conexión abierta.
    * "Cache-Control"
      * "no-cache" -> Evitamos que se active la cache y nos repita la información.
      * "no-transform" -> Evitamos la compresión gzip de la transmisión (no todos los navegadores la soportan).

    ```Js
    const headers = {
        "Content-Type": "text/event-stream",
        "Connection": "keep-alive",
        "Cache-Control": "no-cache",
    };
    ```

2. Mensaje
El mensaje de un envento tiene que tener el siguiente formato `"data: 'pon aquí tu mensaje' \n\n"` y sólo se puede mandar en formato string.

    ```Js
    data = JSON.stringify(data);
    let header = "data: ";
    let footer = "\n\n";

    let message = header + data + footer;
    ```

3. Otros
Servidores como NGINX y Apache interpretan `"Connection":"keep-alive"` de forma distinta, pudiendo cerrar el canal por inactividad.
por loque podemos implementar un `retry` para volver a conectar o un mensaje `"event: ping\n"`

## Cliente

### Ejemplo de conexión

```js
const SSE = new EventSource('http://localhost:5173/stream');
```

### Eventos

* onmessage
* onopen
* onerrror

    ```js
        SSE.onmessage = (event) => {
            console.log("Evento: ",event);
        }
    ```
