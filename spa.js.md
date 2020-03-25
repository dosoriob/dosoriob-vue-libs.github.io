# spa.js
Funciones de utilidad general para el trabajo con APIs en una SPA.

* TOC
{:toc}

## spa.router

  Configura el ruteo a las vistas SPA (hash => vista). 
  Utiliza la libreria [SammyJS](http://sammyjs.org/) para el manejo de cambios en el hash.

  **Propiedades**

  | Nombre        | Descripción    |
  |--------------------------------|
  | spa.router.previousUrl | Almacena la URL previa a la mostrada actualmente. |
  | spa.router.onChange | *function(newUrl, prevUrl)* evaluada antes de procesar un ruteo. `this` accede al objeto `spa.router`. Si la función retorna `false` se cancela el cambio de ruta y se restaura la URL/hash del navegador anterior. |
  +--------------------------------|

### Propiedades

#### spa.router.previousUrl

  Almacena la URL previa a la mostrada actualmente.

#### spa.router.onChange

  *function(newUrl, prevUrl)* evaluada antes de procesar un ruteo. 
  `this` accede al objeto `spa.router`.

  *Retorno*
  - `true` para continuar con el cambio de ruta, o
  - `false` para cancelar el cambio de ruta y restaurar la URL/hash del navegador al que tenía previamente.

## spa.views

Permite cargar vistas VueJS en elementos contenedores de la página web.
