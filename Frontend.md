# Especificación de la aplicación

## Funcionalidades

### Aunteticación

La aplicación no necesita que el usuario esté autenticado desde un inicio, se puede acceder parcialmente al servicio brindado aunque ya para realizar operaciones avanzadas (comprar, postear) es necesario que el usuario este autenticado. 

En caso del usuario quiera realizar una operación la cual no puede hacer debido a que no se encuantra autenticado se mostrará un popup notificando al usuario que se autentique con un botón para ir a la página correspondiente.

Para proveer al usuario de feedback sobre si está autenticado o no se mantendrá en la barra superior de la aplicación un círculo conteniendo la foto del usuario en caso de estar autenticado o un placeholder en caso de no estarlo. Al tocar en este círculo se presentarán las opciones correspondientes:

- Se está auntenticado:
  - Se muestra la información del usuario
- No se está autenticado:
  - Se muestra una página para registrarse o para autenticarse

### Métodos de pago

Cada producto que se agregue deberá contener información sobre los métodos en los que es posible realizar el pago y el precio correspondiente para cada uno.

### Compra

Para poder realizar la compra de productos se necesita estar autenticado.
El flujo para comprar un producto puede variar de dos maneras. La primera es realizar la compra directa. La segunda es mediante un servicio de carrito de compras que permite manejar más cómodamente estas.

### Carrito de compra

El carrito de compras mantendrá una lista en la propia aplicación de los productos en los que se está interesado. Añadir un producto al carrito no tiene ningún efecto en el servidor, o sea no se reserva ni nada.

### Post

Para poder realizar un post de un producto se necesita estar autenticado.
Cuando se suba un producto al final de la construcción del post se preguntará si ya desea ponerlo en venta o si desea dejarlo no en venta.

### Producto

Un producto puede ser marcado como favorito.
Un producto puede estar en venta o no. Esta modalidad es para que los vendedores puedan subir y modificar el producto sin tener que ponerlo en venta instantáneamente.

### Notificaciones

Los usuarios recibirán notificaciones en caso de que ocurran diferentes eventos:
- Se compra un producto de los que está vendiendo
- Un producto como favorito que estaba out of stock volvió a estar disponible o fue le modificado el precio

### Manejador de errores

Encargado de manejar los errores, ya sea guardarlos para enviarlos al server o para hacer un auto-diagnóstico. Se puede usar para mostrar errores al usuario.

## Páginas

### Barra de navegación

Esta sección contiene el nombre de la página en que se está además de íconos en la parte derecha como los del carrito de compras y la foto del usuario 

### Feed de productos (Página principal)

Esta página consiste en un feed de productos en venta, mostrará en una lista de cards la información básica sobre los productos y al seleccionar uno de ellos se mostrará una página con mayor detalle sobre el producto en venta.  

### Carrito de compras

Esta página contendrá los productos que se quieren comprar. En los cards de los productos se podrá eliminar dicho producto del carrito y se mostrará información general sobre los productos en el carrito como precio total, cantidad, etc. 

### Página de Post

Esta página contendrá los productos que tiene en venta el usuario. Contiene una lista con cards mostrando los productos en venta. Al seleccionar estos productos se va a los detalles de este visualizando otros datos relacionados con las compras, por ejemplo, cantidad comprada, ganancias, etc.

### Detalles de productos en venta

Esta página muestra los detalles de un producto en venta, además de brindar los botones necesarios para la compra del mismo ya sea directamente o mediante añadirlo al carrito. También se podrá marcar como favorito o no tocando algún ícono que sugiera esto. Se tiene un feed de comentarios incorporados al final de los detalles.

En caso de haber comprado este producto se podrá realizar una calificación al producto y se podrá escribir un comentario sobre él

En caso de ser abierto desde el modo de vendedor se muestran los datos relacionados con las ventas de este.

### Autenticar Usuario

Esta página muestra dos entradas de texto encargados de proporcionar el nombre de usuario y la constraseña para la autenticación. Posee botones que guían al usuario a registrarse en el sistema y a relizar el cambio de contraseña en caso de haber olvidado.

### Perfil de Usuario

Esta página muestra los datos relacionados al usuario. Presenta botones que permiten ir a la página encargada de modificar dicha información.

### Modificar Usuario

Esta página es la encargada de modificar la información relacionada con el usuario. Además permite cambiar la contraseña.

### Registrar Usuario

Esta página se encarga de introducir toda la información del usuario necesaria para registrarlo en el sistema.
