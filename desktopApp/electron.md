# Electron

## Ventana

Para crear una nueva ventana llamaremos al objeto `BrowserWindow` dentro de este objeto
podemos encontrar las siguientes propiedades:

1. width
2. height
3. icon
4. webPreferences

### Tamaño

Estas propiedades se definen en px

### Icono

Establece el icono que se mostrará tanto en la barra de tareas como en la propia ventana,
admite la mayoría de formatos de imagen aunque es recomendable usar un .ico

### WebPreferences

Este apartado es un subObjeto con la configuración que va a tener internamente nuestra ventana
las opciones más comunes:

1. preload
2. nodeInegration
3. contexIsolation
4. setAppDetails

#### Preload

Es un script que se inicializa antes de crearse la página y se inyecta una vez esta, está finalmente creada, pudiendo asi acceder a las opciones de electron y del proceso principal de electron, aunque de forma limitada, para dotar a este sistema de más control tenemos que usar contexBridge.

```js
    webPreferences:{
        preload: path.join(__dirname, 'preload.js')
    }
```

esta práctica esta tremendamente recomendada, dotando asi de más seguridad y robustez a nuestra aplicación.

#### NodeIntegration

Mucha atención con esto, esta cualidad nos permite ejecutar código de node desde nuestra ventana y ¡Desde cualquier fuente no verificable! esta Fuertemente desaconsejado ya que es un riesgo de seguridad muy fuerte para nuestras apps.

Recuerda usar preload, para estos menesteres.

#### ContexIsolation

Con esta opción nos encargamos de separar el preload de nuestra página cargada, de esta manera no podemos acceder desde nuestra ventana a estos datos y opciones.

## Propiedades de la ventana

### OpenDevTools

Abrimos las herramientas de desarrollo de forma predeterminada
`win.webContents.openDevTools()`

### Menu

Eliminamos el menú nativo de electron
`win.removeMenu()`

### SetResizable

Eliminamos la posibilidad de modificar o rescalar la ventana
`win.setResizable(false)`

## Eventos de la ventana

```js
win.on('',()=>{

})
```

Con esto podemos detectar cuando se va a cerrar, maximizar minimizar o similares.

## Tray

Con esta función podemos crear un icono y un menu en la bandeja del sistema, perfectamente
compatible con Linux y Windows.

Con esto agregamos un icono y creamos la funcionalidad.

```js
    const tray = new Tray(path.join(__dirname, '/assets/img/logos/tanuki_logo.png'))
```

### setToolTip

De esta manera podemos modificar el texto que aparece en el icono.

```js
    tray.setToolTip('TanukiGochi center')
```

### setContextMenu

De esta manera podemos crear un menú para nuestro icono.

```js
    tray.setContextMenu(contextMenu)
```

### Menu.buildFromTemplate

```js
const contextMenu = Menu.buildFromTemplate([
    {
      label: 'Mostrar',
      click: function () {
        win.show()
      }
    },
    { type: 'separator' },
    {
      label: 'Salir',
      click: function () {
        app.quit()
      }
    }
  ])
```

### Eventos de Tray

los eventos probados son doble click y click y se construyan igual que la ventana

```js
tray.on("",()=>{

})
```

## Notificaciones

Con esta función podemos lanzar notificaciones en Windows o Linux
podemos cambiar el sonido, quitárselo añadir titulo, subtitulo e icono
asi como el tiempo de cada notificación.

```JavaScript
    const tanukiNotification = new Notification({ title, body })
    tanukiNotification.show()
```

### Eventos de notificaciones

Funciona igual que en las diferentes partes de electron, el que más uso
es poder llamar a la ventana minimizada al hacer click.

```JavaScript
    tanukiNotification.on('click', (event) => {
      win.show()
    })
```
