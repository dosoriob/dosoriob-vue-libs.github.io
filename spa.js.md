# spa.js
Funciones de utilidad general para el trabajo con APIs en una SPA.

{:toc}

## spa.router
Configura el ruteo a las vistas SPA (hash => vista). 
Utiliza la libreria [SammyJS](http://sammyjs.org/) para el manejo de cambios en el hash.

### spa.router.previousUrl
Almacena la URL previa a la mostrada actualmente.

### spa.router.onChange(newUrl, prevUrl)
Funcion evaluada antes de procesar un ruteo. Puede usar **this** dentro de la función para acceder al objeto **spa.router**.
**Retorno**
- `true` para continuar con el cambio de ruta, o
- `false` para cancelar el cambio de ruta y restaurar la URL/hash del navegador al que tenía previamente.

## spa.views
Permite cargar vistas VueJS en elementos contenedores de la página web.
