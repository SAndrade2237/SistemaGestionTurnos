## Principio de Abierto/Cerrado (OCP)

### Proposito del principio:
El principio Abierto/Cerrado plantea que las clases deben estar abiertas para la extension pero cerradas para la modificacion. Es decirm el comportamiento de un modulo debe poder extenderse sin necesidad de cambiar su codigo original. Esto ayuda a evitar errores al modificar codigo que ya funciona, y promueve un diseño mas flexible.

### Tipo del principio:
OCP es un principio de extensibilidad. Esta orientado a permitir que nuevas funcionalidades se agreguen al sistema sin alterar el codigo existente, lo que reduce el riesgo de introducir fallos.

### Como lo soluciona:
Permite extender el comportamiento de una clase sin modificar su codigo original, utilizando herencia, interfaces o composicion. Asi, el sistema crece sin comprometer su estabilidad.

### Motivacion
La clase SistemaNotificaciones maneaja el envio y generacion de mensajes. Si en un futuro se quiere implementar notificaciones por otros medios (WhatsApp, notificacion in-app, etc.), habria que modificar directamente esta clase.

Aplicando OCP, se puede definir una interfaz INotificador y luego implementar clases como NotificadorEmail, NotificadorSMS, etc. Asi SistemaNotificaciones puede extenderse con nuevas funcionalidades sin modificar su estructura, manteniendola cerrada al cambio pero abierta a extensiones.

Ejemplo: imagina una maquina expendedora que solo acepta monedas. Si en el futuro se requiere agregar la opcion de pagar con tarjeta, no seria logico abrir la maquina y modificar todo el sistema original de monedas. Lo ideal seria extender la funcionalidad agregando un nuevo modulo para tarjetas que se conecte al sistema sin alterar el mecanismo ya existente.

### Estructuras de Clases

[Link boceto OCP](https://drive.google.com/file/d/1901lqPkDTTshthEH_N938RqbPf3m8ZDY/view?usp=sharing)

![Image](https://github.com/user-attachments/assets/b7c32ad6-3fbf-4665-83ca-0fa17ae0f81b)
