## Principio de Segregacion de Interfaces (ISP)

### Proposito del principio:
El principio de Segregacion de Interfaces (ISP) establece que una clase no debe estar obligada a implementar interfaces que no utiliza. En otras palabras, las interfaces deben ser diseñadas de manera que cada clase implemente solo los metodos que necesita, sin verse forzada a implementar metodos innecesarios.

### Tipo del principio:
ISP es un principio de optimizacion de interfaces. Su objetivo es mantener las interfaces pequeñas y coherentes, evitando que las clases dependan de metodos que no van a usar.

### Motivacion
Cuando se utiliza herencia o interfaces en un sistema, es fundamental que las clases hijas respeten el contrato definido por su clase padre. Si una subclase cambia el comportamiento esperado, por ejemplo, lanza errores, ignora funcionalidades o actua de forma contradictoria, puede romper el funcionamiento del sistema y generar errores dificiles de rastrear.

El principio de Sustitucion de Liskov evita este problema al asegurar que cualquier clase derivada pueda sustituir a su clase base sin alterar el comportamiento logico del sistema. Esto permite que las funcionalidades se extiendan de forma segura sin temor a que nuevas implementaciones interfieran con lo ya construido.

Ejemplo: Imagina un sistema para gestionar dispositivos de impresion con una clase base DispositivoDeImpresion y subclases como Impresora y Fotocopiadora. Si la Fotocopiadora cambia el metodo imprimir() para realizar una funcion diferente como copiar en lugar de imprimir, se violaria el principio de Sustitucion de Liskov. Esto impediria que se sustituya un dispositivo por otro sin alterar el comportamiento esperado.

### Estructuras de Clases
