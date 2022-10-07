# Definición

Un evento establece información del evento generado (ratón, formulario, teclado etc.) al controlador autorizado que lo gestiona (función).

## Definiciones importantes

### Bubbling

Es el evento que surge cuando un evento se activa por otros eventos encontrados en el elemento padre que lo contiene.

## Funcionamiento básico

Todo evento tiene un objetivo `target`, registrado en el atributo `target` del evento, cuando el evento llega al objetivo todos las escuchas del evento `event listeners` registradas en `eventTarget` son activadas.

## Captura del evento

El proceso de captura se origina en la parte superior del DOM, y se va propagando hacia abajo de forma simétrica.

### Propagación de la captura

En el caso de que el evento se alterado durante la propagación, este continuará su camino respecto al estado inicial del árbol.

Si se quiere detener la propagación del mismo se puede utilizar el método `stopPropagation`, que detendrá el flujo de propagación, pero las que estén en el mismo nivel, estas seguirán recibiendo el evento.

## Métodos

### addEventListener

Este método registra el evento que ha de ser escuchado. si se declaran múltiples eventos con el mismo eventTarget las duplicidades se descartan.

#### Parámetros

> type Tipo de evento a escuchar
> listener El tipo de EventListener
> useCapture Si se establece en True, no activa los bubbles

### dispatchEvent

Lanza un evento directamente, es el último paso dentro del proceso de eventos.

#### Parámetros de dispatchEvent

> evt Especifica el tipo de evento

El valor de retorno es un booleano

### removeEventListener

Este método elimina las escuchas (eventListener) de cada eventTarget, una vez llamado, no se podrá volver a escuchar

#### Parámetros de removeEventListener

> type Tipo de evento a eliminar
> listener El tipo de EventListener a eliminar
> useCapture Si se establece en True, no activa los bubbles

## Tipos de eventos

### De ratón

* Click
  * Cuando el puntero del ratón es pulsado en el elemento.
* MouseDown
  * Cuando en el elemento un botón del puntero es presionado.
* MouseUp
  * Cuando en el elemento un botón del puntero se suelta.
* MouseOver
  * Cuando entra el puntero dentro del elemento.

#### Atributos

> screenX, screenY, clientX, clientY, altKey, ctrlKey, shiftKey, metaKey, button, detail.

* MouseMove
  * Cuando el puntero cambia de posición dentro del elemento
* MouseOut
  * Cuando el puntero sale del elemento.

### De teclado

### De HTML
