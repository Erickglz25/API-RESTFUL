### API RESTful
___

#### ¿Qué es una API?

Una API es un conjunto de funciones y procedimientos que cumplen una o muchas funciones con el fin de ser utilizadas por otro software. Las siglas API vienen del inglés Application Programming Interface.
Una API nos permite implementar las funciones y procedimientos que engloba en nuestro proyecto sin la necesidad de programarlas de nuevo.


#### ¿Qué es una API REST?

Una API REST es una una biblioteca apoyada totalmente en el estándar HTTP. Visto de una forma más sencilla, una API REST es un servicio que nos provee de funciones que nos dan la capacidad de hacer uso de un servicio web que no es nuestro, dentro de una aplicación propia, de manera segura.

El no tener estado es una desventaja clara: tener que pasar el estado en cada llamada es, como mínimo, tedioso, pero la contrapartida es clara: escalabilidad. Para mantener un estado se requiere algún sitio (generalmente memoria) donde guardar todos los estados de todos los clientes. A más clientes, más memoria, hasta que al final podemos llegar a no poder admitir más clientes, no por falta de CPU, sino de memoria.

Al usar una API todo el desarrollo que se quiera realizar estará limitado por los métodos o funciones que esta incluya, es decir, no pueden ser añadidas nuevas funcionalidades.

#### Arquitectura REST "Representational State Transfer"

Un servicio REST no tiene estado (es stateless), lo que quiere decir que, entre dos llamadas cualesquiera, el servicio pierde todos sus datos..

Por lo tanto REST es el tipo de arquitectura más natural y estándar para crear APIs para servicios orientados a Internet.

> El protocolo de comunicación utilizado en los servicios REST es el protocolo HTTP

![Api restful](https://ayudawp.com/wp-content/uploads/2016/01/WordPress-json-rest-api.png "titulo")

Para considerarse REST además de utilizar este protocolo deberían hacer un uso correcto de los métodos y los códigos de estado o error.

#### Identificación de recursos mediante URIs

los diferentes elementos de información lse denominan “recursos”. Un recurso puede ser información sobre libros, clientes, coches, etc. pero un recurso nunca será una acción como por ejemplo “comprar_libro” o “crear_coche”.
Un recurso debe estar identificado de forma única por una URI. Una URI no es más que una cadena de texto con una estructura determinada que nos permite identificar un elemento.

> Si tenemos una api situada en http://miapideejemplo.com, y un recurso llamado “productos”, la URI de acceso al producto cuyo identificador es 57 sería http://miapideejemplo.com/productos/57.

#### Hipermedia 

La descripción de la arquitectura REST no incluye la definición de un formato concreto de respuesta. Normalmente los formatos elegidos son XML o JSON, ya que son dos lenguajes que permiten describir fácilmente estructuras y jerarquías, a la vez que son ampliamente utilizados y conocidos en la actualidad. El servicio no debe estar supeditado al formato de las respuestas que va a devolver, de hecho, es muy común que un mismo servicio REST sea capaz de devolver las respuestas en diferentes formatos. Incluso en servicios capaces de devolver respuestas en diferentes formatos, las URIs deben ser totalmente independientes de dicho formato. Si por ejemplo nuestro servicio es capaz de devolver un listado de productos en formato XML y en formato JSON, el acceso al recurso no debe indicar el formato de acceso.

La definición de la arquitectura REST si que indica el uso de hipermedios para la información de la aplicación y para las transiciones de estado de la aplicación. Un hipermedio no es más que un vínculo que permite enlazar un recurso con otro. Estos enlaces permiten navegar desde un recurso REST a otros recursos relacionados con él

**CONSTRUCCIÓN ADECUADA DE UNA API RESTful**
Si queremos construir una interfaz de comunicaciones cuya arquitectura sea REST debemos tener en cuenta los aspectos anteriormente comentados, que a modo de resumen son:

1. Usar Http como protocolo cliente/servidor sin estados, utilizando correctamente sus métodos y códigos de error.
2. Identificación única de los recursos mediante URIs independientes del formato de las respuestas
3. Permitir que las respuestas sean cacheables mediante un sistema de caché
4. El servidor debe ser un sistema capaz de ser escalado y dividido en capas
5. Uso de hypermedia


### REFERENCIAS Y RECURSOS
* http://www.i2factory.com/es/integracion/qu%C3%A9-es-un-servicio-restful
* http://www.desarrolloweb.com/articulos/crear-api-rest-json-server.html 
* http://asiermarques.com/2013/conceptos-sobre-apis-rest









