## Principio de Segregacion de Interfaces (ISP)

### Proposito del principio:
El principio de Segregacion de Interfaces (ISP) establece que una clase no debe estar obligada a implementar interfaces que no utiliza. En otras palabras, las interfaces deben ser diseñadas de manera que cada clase implemente solo los metodos que necesita, sin verse forzada a implementar metodos innecesarios.

### Tipo del principio:
ISP es un principio de optimizacion de interfaces. Su objetivo es mantener las interfaces pequeñas y coherentes, evitando que las clases dependan de metodos que no van a usar.

### Motivacion
Cuando una clase implementa una interfaz grande y generica, que contiene muchos metodos que no son relevantes para esa clase, puede surgir un problema: la clase se ve obligada a implementar metodos que no necesita, lo que aumenta la complejidad y reduce la cohesion del sistema. Esto tambien puede resultar en errores o comportamientos indeseados, ya que el codigo tiene que lidiar con metodos innecesarios.

El principio de Segregacion de Interfaces (ISP) resuelve este problema al promover la creacion de interfaces mas pequeñas y especificas, permitiendo que las clases implementen solo lo que realmente necesitan. De esta maneram se mejora la cohesion y flexibilidad del sistema y facilita su mantenimiento.

Ejemplo: Imaginá un sistema para gestionar diferentes tipos de vehículos: autos, camiones, bicicletas, etc. Si creamos una interfaz Vehiculo con métodos como encenderMotor(), transportarCarga() y acelerar(), la clase Bicicleta se vería obligada a implementar transportarCarga(), aunque no tiene esa funcionalidad.

Siguiendo el principio ISP, lo ideal sería dividir la interfaz Vehiculo en interfaces más pequeñas: VehiculoConMotor (con encenderMotor()) y VehiculoDeCarga (con transportarCarga()). De este modo, las clases como Bicicleta solo implementan los métodos relevantes para ellas.
### Estructuras de Clases
