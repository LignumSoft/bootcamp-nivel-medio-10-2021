# LIGNUM BOOTCAMP NIVEL MEDIO 10/2021 #

![LignumLogo](https://user-images.githubusercontent.com/15086662/89939428-5734d100-dbee-11ea-87ac-00d0910adaf5.png)

### Bienvenidos al bootcamp acelerado de octubre 2021.  ###

Este curso supone que ya adquirieron los conocimientos básicos de HTML-CSS-JS, validaciones, accesibilidad, media-queries, layouts, 
css-reset para mayor consistencia entre browsers como normalize.css, configuración de servidores locales, manejo de paquetes tanto locales como algún sistema de manejo de paquetes como npm,
entendimiento de CORS https://web.dev/cross-origin-resource-sharing/, Bootstrap,
el uso de herramientas de depuración como la consola de Chrome -> https://developer.chrome.com/docs/devtools/console/, livewire, vue, entre otros.

### Preparacion ###
1)Descargar e instalar un entorno de desarrollo, por ejemplo, apache -> https://www.apachefriends.org/es/index.html

2)Descargar e instalar laravel -> https://laravel.com/docs/8.x

3)Asegurarse de estar usando la última versión de su navegador, Firefox, Chrome, Edge, etc.

### Actividades ###

A pesar de que las palabras MVC ya no sirven para definir la estructura del proyecto, debido a la gran cantidad de capas extra que se agregaron en la complejidad de las aplicaciones, ya que Modelo es solo
una parte de la estructura de App, Controller es una parte de Http junto a Middleware, request, routes. Views es una parte de Resources...  Las siguientes actividades deben ser realizadas utilizando 
una estructura de Modelo-Vista-Controlador, un recurso didáctico un poco antiguo que podrían revisar si es que se les escapa algún concepto es este https://styde.net/laravel-5/

## Usted dispondrá de 48 horas para entregar o hacer lo mayor posible de las siguientes tareas. ##


#### Minimo (Ejemplo) ####
1)
Crear las migraciones de las siguientes tablas: -> https://laravel.com/docs/8.x/migrations

Aclaracion: Las siguientes tablas deberan llevar ademas de sus datos especificos "timestamps" y tener "softdeletes" habilitado. 

Si creen que algun campo deberia ser nullable o tener un valor default queda a su discrecion.

Evento:
Codigo
Nombre
Foto
Descripcion
FechaInicio
FechaFinalizacion
Lugar
Geolocalizacion
LocalidadID

Pais:
Descripcion
Codigo

Provincia con referencia a su pais y ademas:
Descripcion
Codigo

Localidad con referencia a su provincia y ademas:
Descripcion
Codigo
CodigoPostal
CodigoArea

2)
Crear las relaciones de pais-provincia provincia-localidad y evento-localdiad -> https://laravel.com/docs/8.x/eloquent-relationships

3)
Crear el CRUD de los mismos utilizando eloquent para el manejo de los datos y guardarlos en MySQL -> https://laravel.com/docs/8.x/controllers#resource-controllers

4)
Visualización de imagen del evento y el cargado de la misma desde el ABM (Desde local, no un link a una imagen).

5)
Crear un mapa en el frontend en donde se visualice la geolocalizacion del evento.
Extra nivel medio: Que el superusuario pueda geolocalizar el evento en un mapa (preferentemente google maps, cualquiera es admitido) y esa misma sea la que se visualice en el front.

### Tareas Por Nivel ###
#### Inicial: ####


I-1)Crear un listado CON LIVEWIRE donde se puedan ver los eventos -y elegir una de las siguientes opciones para desarrollar (A o B)-

I-1-a) Mostrar multiples eventos separados en carouseles segun tipo de evento (Festivos, corporativo, espectaculos, deportivos, etc)

o

I-1-b) Mostrar multiples eventos como lo verias por ejemplo en netflix pero con un maximo de 8 fotos por pantalla, utilizar lazy loading para hacer infinite scrolling. Debe ser responsive (minimamente para pantallas de 320, 375 y 425px)

I-2)Crear un apartado para ver eventos anteriores, al igual que con el apartado E-1 deberas mostrarlo en un carousel o infinite scrolling.

I-3)En las pantallas donde existan multiples selectores deberan ser dinamicos (ajax). Por ejemplo en evento seleccionariamos pais - provincia - localidad

#### Medio: ####

M-1)Selector con sugerencias - Debera recomendar al superusuario dinamicamente los paises-provincias-localidades que comiencen con lo que el haya escrito (Una vez que haya escrito al menos 3 letras)

M-2)Copy-paste para la carga de imagenes (sin necesidad de cargarla de un archivo de mi computadora)

#### Avanzado: ####

A-1)Crear un chat de contacto. Sera un FAB que le abra un modal con una leyenda animandolo a hacer sus preguntas (Crear las migraciones pertinentes para guardar estos chats, distinguiendo al usuario-cliente y al superusuario/usuario-soporte)

A-2)Crear un Buscador -del titulo del evento- con sugerencias:
A-2-a)Hacer un endpoint de API que devuelva un JSON y le muestre al usuario-cliente sugerencias de lo que escribió ejemplo: https://darkville.tv/ 

o

A-2-b)El listado de los eventos actualizados como si fuera Netflix (puntos extra por este último).

## Soy Nuevo en esto pero aun asi quiero intentarlo ¿Algun consejo? ##
### Criterios a tener en cuenta ###

*El proyecto deberia ser tan modular como sea posible.
Es decir, las funciones de un Evento deberian estar en EventoController y las de un usuario en UsuarioController, no mezcladas en el mismo archivo.

*El naming de las funciones deberia ser segun funcionalidad y luego el modelo, si el nombre es autodescriptivo todavia mejor.
Por ejemplo, si tengo una funcion para crear un evento y otra para crear una localidad deberian llamarse crearEvento() y crearLocalidad()

### Consejos ###
Las aplicaciones se pueden hacer en cualquier orden, pero talvez seguir estos pasos te ayuden.

*Crear las migraciones sus controladores, modelos y vistas.

*Crear la relación en los modelos.

*Crear las vistas que permitan al superusuario cargar los datos del evento.

*Crear la funcionalidad en el controlador para actualizar los datos.



*Crear una vista donde el usuario-cliente visualice los eventos y pueda buscarlos (Si realizo las actividades correspondientes, que se muestre el cambio con AJAX sin necesidad de recargar la pantalla)

*Crear una vista donde el usuario-cliente pueda ver un listado de eventos pasados.

*Crear lo necesario para que el superusuario pueda editar y borrar eventos.

### ¿Como comienzo? ###

Primero, piensa cual debería ser la estructura de tu aplicación (Primero estructura de datos de la base de datos, luego en que orden irían las pantallas).
No hace falta crear usuarios ni roles, pero sí que las pantallas se diferencien de cual sería para cada uno.

Luego piensa en las pantallas del CRUD de los eventos/datos geograficos.
El siguiente paso sería poder visualizar los eventos como el usuario que visita la página y permitir buscarlos.
Ahora crea la pantalla para ver el listado de los eventos pasados.

Por último, afina los detalles (drag & drop de imágenes, cargas dinamicas, estética, etc.).


### ¡Es poco probable que logre terminar esto! ###
No te preocupes por eso e intenta completar los puntos importantes.

Ten en cuenta que todo conocimiento sirve y que no hay un puntaje específico para cada actividad, no hay porque ponerse nervioso, es solo una pequeña muestra de lo que sabemos o aprendimos
en el bootcamp.

¡Manos a la obra!
