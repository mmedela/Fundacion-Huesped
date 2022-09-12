# Fundacion-Huesped

En la funcion send_file no incluyo mi propio mail por razones obvias de seguridad.


## Mejoras:

### El diseño:
    En este ejercicio decidi modelar el problema usando funciones por simplicidad, pero una solucion mejor y mas escalable hubiese sido modelarlo usando un objeto que se encargara de manejar el enviado de mails. Para esto usaria metodos estaticos siguiendo el patron de diseño singleton, evitando asi los problemas que suelen ocurrir cuando ddos proceso intentan escribir un archivo al mismo tiempo o cuando un proceso borra un archivo mientras otro esta intentando leerlo/escribirlo. Hacerlo de esta forma tambien permitiria chequear si ya estoy logeado para evitar hacerlo y configurar la sesion cada vez que quiero mandar un mail, ya que esta accion es bastante costosa.



### Parseo de los PDFs:
    En un caso mas realista los PDFs tendrian mas cosas que solo el nombre del cliente por lo que habria que modificar la funcion que los lee para que busque el nombre en estos, a diferencia de como esta ahora donde simplemente se queda con la primer linea que encuentra. Esto tambien es aplicable al mail de los clientes.


### Enviado de mails:
    Mi implementacion esta probada y funciona con direcciones de mail hosteadas por google pero en caso de que la empresa use otro proveedor de mail, esta puede ser invalida y necesitar modificaciones.