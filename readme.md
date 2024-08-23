# Sincronia y Asincronia JS

## Sincronia en Javascript

Por naturaleza, JS es un lenguaje sincrónico y de un solo hilo. Esto significa que las operaciones son ejecutadas de forma secuencial de manera que cuando una operación se está ejecutando las otras operaciones no se ejecutan y estarán en espera hasta que esta haya sido finalizada.

## Protocolo HTTP

HTTP o `Protocolo de Transferencia de Hipertexto`, es un protocolo de solicitud-respuesta en el que un cliente envía una solicitud a un servidor y el servidor responde con los datos solicitados o un mensaje de error.

### Verbos HTTP (Ejemplos)

También conocidos como métodos, son las acciones que se desean realizar con un recurso.

Los más comunes son:

#### POST (Crear Data / Mandar Información)

Envía datos al servidor para crear un nuevo recurso.

#### GET (Obtener Información)

Solicita un recurso específico.

#### PUT (Actualizar Información)

Envía datos al servidor para actualizar un recurso existente.

#### DELETE (Eliminar)

Solicita la eliminación de un recurso existente en el servidor.

### Body

En una petición HTTP, el body contiene los datos que se envían en la petición.

Se usa principalmente en métodos como POST y PUT donde se envian datos (Ej: Datos de un formulario).

El body contiene datos en varios formatos como `JSON, XML, y texto plano`.

### Headers

Proporcionan información adicional sobre la solicitud o respuesta.

Pueden incluir detalles sobre el tipo de contenido, su longitud, codificación, token, etc.

### Code response

Los codigos de respuesta indican el resultado de una solicitud HTTP y su estado.
Están enumerados de la siguiente manera:

> 100 - 10X  
> 200 - 20X  
> 300 - 30X  
> 400 - 40X  
> 500 - 50X

Algunos ejemplos:

- 200 (OK)
- 201 (Created)
- 400 (Bad Request)
- 404 (Not Found)
- 500 (Internal Server Error)

### Request y Response

El `Request` es el mensaje enviado por el cliente al servidor.
Contiene una línea de solicitud (método, URL y versión HTTP), encabezados y un cuerpo.

El `Response` es el mensaje enviado por el servidor al cliente en respuesta a una solicitud.
Contiene una línea de estado (código de estado y mensaje), encabezados y un cuerpo con los datos solicitados o un mensaje de error.

## Asincronia en Javascript

Se pueden realizar peticiones asíncronas las cuales permiten solicitar datos a un servidor sin bloquear la ejecución del resto del código.

Esto es crucial para una mejor UX ya que permite a la UI responder mientras se realizan operaciones como la obtención de datos o la carga de archivos.

### Peticiones Asincronas

Para realizar peticiones asíncronas se usa `XML HttpRequest`, `Fetch` y `Axios`.
Estas solicitudes se ejecutan en segundo plano, y JS utiliza mecanismos como `promises` para manejar la respuesta una vez que los datos estén listos.

### Manejar la data luego de la peticion asincrona

Después de realizar una petición asíncrona, se utilizan técnicas como `callbacks, Promesas o async/await` para manejar los datos obtenidos.

#### Callbacks

Funciones que se pasan como argumento a otras funciones y se ejecutan después de que una operación asíncrona se completa.

#### Promises

Objetos que representan un valor que puede estar disponible ahora, en el futuro, o nunca. Usan métodos como .then() y .catch() para manejar resultados y errores.

#### Async / Await

Sintaxis moderna para trabajar con Promesas que hace que el código sea más fácil de leer y escribir. await se utiliza para esperar a que una Promesa se resuelva.
