# DAW JOB 4: Configurar respuesta a errores en apache

## Directiva `ErrorDocument`

Para definir una respuesta personalizada en apache a ciertos códigos `HTTP` se debe modificar el fichero de configuración `httpd.conf`. En este fichero se emplea la directiva `ErrorDocument` seguida del código que se quiere manejar y el contenido con el que se va a responder (texto plano, redirección local o redirección externa).

![](/assets/images/error-document.png)

## Ejemplo de 404

Se puede provocar fácilmente un `404` intentando acceder a un recurso que no existe. Por ejemplo, en mi servidor la ruta `/www/example/patata.php` no se corresponde con ningún recurso, en consecuencia el servidor responde con la redirección local que se ha definido.

![](/assets/images/not-found-example.png)

## Ejemplo de 500

El fichero `.htaccess` es un fichero de configuración que modifica el comportamiento de apache. Una forma de obtener un `500` es crear uno de estos ficheros con contenido arbitrario, la ruta donde se ubique no será correctamente manejada por nuestro servidor.

![](/assets/images/htaccess-content.png)
![](/assets/images/internal-error-example.png)
