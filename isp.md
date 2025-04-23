## Principio de Segregacion de Interfaces (ISP)

### Proposito del principio:
El principio de Segregacion de Interfaces (ISP) establece que una clase no debe estar obligada a implementar interfaces que no utiliza. En otras palabras, las interfaces deben ser diseñadas de manera que cada clase implemente solo los metodos que necesita, sin verse forzada a implementar metodos innecesarios.

### Tipo del principio:
ISP es un principio de optimizacion de interfaces. Su objetivo es mantener las interfaces pequeñas y coherentes, evitando que las clases dependan de metodos que no van a usar.

### Como lo soluciona:
Fomenta la creacion de interfaces especificas y pequeñas, de forma que cada clase implemente no solo los metodos que necesita. Esto evita la sobrecarga innecesaria y mejora la cohesion.

### Motivacion
Si se creara una interfaz IUsuario que fuera implementada tanto por Paciente como Recepcionista, con metodos  como asignarTurno(), consultarHistorial() y resgistrarPaciente(), estariamos obligando a ciertas clases a implementar metodos que no le corresponden.

Con ISP, se puede dividir esa interfaz en IPaciente y IRecepcionista, para que cada clase implemente solo lo necesario. Asi se evita que una clase tenga que depender de metodos irrelevantes, y el diseño se vuelve mas limpio.

Ejemplo: Imaginá un sistema para gestionar diferentes tipos de vehículos: autos, camiones, bicicletas, etc. Si creamos una interfaz Vehiculo con métodos como encenderMotor(), transportarCarga() y acelerar(), la clase Bicicleta se vería obligada a implementar transportarCarga(), aunque no tiene esa funcionalidad.

Siguiendo el principio ISP, lo ideal sería dividir la interfaz Vehiculo en interfaces más pequeñas: VehiculoConMotor (con encenderMotor()) y VehiculoDeCarga (con transportarCarga()). De este modo, las clases como Bicicleta solo implementan los métodos relevantes para ellas.
### Estructuras de Clases

[Link de diagrama ISP](https://drive.google.com/file/d/1RzCRJSo705FdvnzmyG0QfCzZmAjXM-jQ/view?usp=sharing)

![Image](https://github.com/user-attachments/assets/82546aea-ca26-4eb4-bd86-4be9cd891706)
