## Principio de Sustitucion de Liskov (LSP)

### Proposito del principio:
El principio de Sustitucion de Liskov indica que las clases hijas deben poder reemplazar a sus clases padre sin alterar el comportamiento esperado del programa. En otras palabras, si una clase hija hereda de una clase padre, podria usarse en lugar de padre sin causar errores ni comportamientos inesperados.

### Tipo del principio:
LPS es un principio de herencia segura, que busca garantizar que las extensiones del sistema mantengan la coherencia logica y funcional del codigo original.

### Motivacion
Cuando se utiliza herencia o interfaces en un sistema, es fundamental que las clases hijas respeten el contrato definido por su clase padre. Si una subclase cambia el comportamiento esperado, por ejemplo, lanza errores, ignora funcionalidades o actua de forma contradictoria, puede romper el funcionamiento del sistema y generar errores dificiles de rastrear.

El principio de Sustitucion de Liskov evita este problema al asegurar que cualquier clase derivada pueda sustituir a su clase base sin alterar el comportamiento logico del sistema. Esto permite que las funcionalidades se extiendan de forma segura sin temor a que nuevas implementaciones interfieran con lo ya construido.

Ejemplo: Imagina un sistema para gestionar dispositivos de impresion con una clase base DispositivoDeImpresion y subclases como Impresora y Fotocopiadora. Si la Fotocopiadora cambia el metodo imprimir() para realizar una funcion diferente como copiar en lugar de imprimir, se violaria el principio de Sustitucion de Liskov. Esto impediria que se sustituya un dispositivo por otro sin alterar el comportamiento esperado.

### Estructuras de Clases
