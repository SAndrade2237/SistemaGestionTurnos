## Principio de Inversion de Dependencias (DIP)

### Proposito del principio:
El principio de Inversion de Dependencias establece que los modulos de alto nivel no deben depender de modulos de bajo nivel, ambos deben depender de abstracciones. Ademas, las abstracciones no deben depender de los detalles, los detalles deben depender de las abstracciones.

En otras palabras, se busca que las clases no esten acopladas directamente entre si, sino que se comuniquen a traves de interfaces o abstracciones, para lograr un diseño mas flexible y desacoplado.

### Tipo del principio:
DIP es un principio de desacoplamiento, que permite reducir la dependencia directa entre componentes y facilita la escalabilidad, el testing y el mantenimiento del sistema.

### Como lo soluciona:
Reduce el acoplamiento al hacer que los modulos dependan de abstracciones en lugar de implementaciones concretas. Esto se logra usanto interfaces e inyeccion de dependencias, lo que mejora la flexibilidad y la testabilidad del sistema.

### Motivacion
Actualmente, las clases interactuan directamente con SistemaNotificaciones. Esto genera una dependencia directa: si cambia esa clase, hay que modificar las clases que la usan (por ejemplo, Turno en su metodo notificarCambio().

Al aplicar DIP, en lugar de que Turno dependa de SistemaNotificaciones, dependeria de una interfaz como Inotificador. Luego, se puede inyectar una clase concreta (NotificadorEmail, NotificadorSMS, etc.) Esto permite desacoplar la logica del negocio de los detalles tecnicos.

Ejemplo: Imagina una cafetera que viene con una marca especifica de filtro incorporado. Si quisieras cambiar el tipo de filtro, tendrias que modificar la estructura interna de la cafetera. En cambio, si la cafetera acepta cualquier tipo de filtro que cumpla con una forma o estandar, podes usar cualquier marca sin modificar nada mas. La cafetera depende de una abstraccion (el estandar del filtro), no de una implementacoin concreta.

### Estructuras de Clases
[Link diagrama DIP](https://drive.google.com/file/d/13sQLg-sKKEo4lQ82iRvH7Omw5H6OXiBz/view?usp=sharing)

![Image](https://github.com/user-attachments/assets/1c2ee0d3-3fc0-439a-818a-22792650fa25)
