# spa.js

Proporciona funciones de carga de contenido y control de navegación para implementar una *Single Page Application* (SPA).

* TOC
{:toc}

## spa.router

Configura el ruteo y carga de contenido de vistas (HTML, CSS, Javascript) ante el cambio en `window.location.hash`. 
Utiliza la libreria [SammyJS](http://sammyjs.org/) para manejar los cambios en la URL, y VueJS para el MVVM.

#### Propiedades

`previousUrl`
: Almacena la URL previa a la mostrada actualmente.

`onChange`
: *function(newUrl, prevUrl)* evaluada antes de procesar un ruteo.
  Si la función retorna `false` se cancela el cambio de ruta y 
  se restaura la URL/hash del navegador anterior.

## spa.views

Maneja la carga de contenido HTML+CSS de una vista, y el código JS que define el objeto Vue que controla esa vista.

#### Propiedades y métodos

`defaults`
: Controla los valores por defecto para la carga de vistas. Es un objeto con las siguientes propiedades:

> `container`
> : Selector CSS del elemento contenedor donde se carga el contenido de la vista. Por defecto es `"main"`.

`load(url,args,options)`
: Carga una vista con controlador Vue.

> `url`
>  : es la URL de la vista, que será resuelta por `requirejs`.

> `args`
>  : argumentos pasados al constructor del modelo Vue.

> `options`
>  : opciones de carga de la vista; es un objeto con las siguientes propiedades:

>> `container`
>> : selector CSS que determina el elemento donde se cargará el HTML de la vista. Valor por defecto: el de `spa.views.defaults.container`.

`disposeContainer(htmlElement)`
: libera los bindings (si existen) que mantiene un modelo Vue con el elemento HTML especificado.

