## Principio de Abierto/Cerrado (OCP)

### Proposito del principio:
El principio Abierto/Cerrado plantea que las clases deben estar abiertas para la extension pero cerradas para la modificacion. Es decirm el comportamiento de un modulo debe poder extenderse sin necesidad de cambiar su codigo original. Esto ayuda a evitar errores al modificar codigo que ya funciona, y promueve un diseño mas flexible.

### Tipo del principio:
OCP es un principio de extensibilidad. Esta orientado a permitir que nuevas funcionalidades se agreguen al sistema sin alterar el codigo existente, lo que reduce el riesgo de introducir fallos.

### Motivacion
A medida que un sistema crece, es comun que surjan nuevos requerimentos, como agregar funcionalidades o modificar comportamientos. Si cada vez que necesitamos extender el sistema debemos modificar el codigo existente, corremos el riesgo de romper funcionalidades que ya estaban funcionando correctamente.

El principio Abierto/Cerrado(OCP) ayuda a resolver este problema al fomentar un diseño en el que se pueda agregar un nuevo comportamiento sin tener que modificar las clases ya desarrolladas. Esto permite que el sistema evolucione de forma segura, estable y mas predecible.

Ejemplo: imagina una maquina expendedora que solo acepta monedas. Si en el futuro se requiere agregar la opcion de pagar con tarjeta, no seria logico abrir la maquina y modificar todo el sistema original de monedas. Lo ideal seria extender la funcionalidad agregando un nuevo modulo para tarjetas que se conecte al sistema sin alterar el mecanismo ya existente.

### Estructuras de Clases
