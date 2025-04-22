## Principio de Sustitucion de Liskov (LSP)

### Proposito del principio:
El principio de Sustitucion de Liskov indica que las clases hijas deben poder reemplazar a sus clases padre sin alterar el comportamiento esperado del programa. En otras palabras, si una clase hija hereda de una clase padre, podria usarse en lugar de padre sin causar errores ni comportamientos inesperados.

### Tipo del principio:
LPS es un principio de herencia segura, que busca garantizar que las extensiones del sistema mantengan la coherencia logica y funcional del codigo original.

### Como lo soluciona:
Asegura que las subclases puedan reemplazar a sus clases base sin alterar el comportamiento esperado. Esto se logra respetando la logica de la superclase y evitando cambios inesperados al extender funcionalidades.

### Motivacion
Si el sistema introduce una subclase de Turno como TurnoMedico, esta deberia comportarse como un turno normal. Por ejemplo, metodos como confirmarTurno() o cancelarTurno() deberian funcionar igual, sin romper el flujo del programa.

Si TurnoMedicina cambia el comportamiento esperado, como no permitir la cancelacion despues de confirmarse, se rompe LPS. Por eso, cualquier subclase debe respetar las reglas del padre (Turno), permitiendo que pueda ser reemplazada sin errores.

Ejemplo: Imagina un sistema para gestionar dispositivos de impresion con una clase base DispositivoDeImpresion y subclases como Impresora y Fotocopiadora. Si la Fotocopiadora cambia el metodo imprimir() para realizar una funcion diferente como copiar en lugar de imprimir, se violaria el principio de Sustitucion de Liskov. Esto impediria que se sustituya un dispositivo por otro sin alterar el comportamiento esperado.

### Estructuras de Clases
