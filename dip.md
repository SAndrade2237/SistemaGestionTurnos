## Principio de Inversion de Dependencias (DIP)

### Proposito del principio:
El principio de Inversion de Dependencias establece que los modulos de alto nivel no deben depender de modulos de bajo nivel, ambos deben depender de abstracciones. Ademas, las abstracciones no deben depender de los detalles, los detalles deben depender de las abstracciones.

En otras palabras, se busca que las clases no esten acopladas directamente entre si, sino que se comuniquen a traves de interfaces o abstracciones, para lograr un diseño mas flexible y desacoplado.

### Tipo del principio:
DIP es un principio de desacoplamiento, que permite reducir la dependencia directa entre componentes y facilita la escalabilidad, el testing y el mantenimiento del sistema.

### Como lo soluciona:
Reduce el acoplamiento al hacer que los modulos dependan de abstracciones en lugar de implementaciones concretas. Esto se logra usanto interfaces e inyeccion de dependencias, lo que mejora la flexibilidad y la testabilidad del sistema.

### Motivacion
Cuando un modulo de alto nivel (por ejemplo, una clase que maneja la logica principal del sistema) depende directamente de clases de bajo nivel (como una clase que envia correos), cualquier cambio en esas clases concretas obliga a modificar el codigo del modulo principal. Esto rompe la estabilidad del sistema, genera un fuerte acoplamiento y dificulta el mantenimiento

El principio de Inversion de Dependencias permite que ambos niveles trabajen a traves de abstracciones, como interfaces. Esto hace que el sistema sea mas flexible, facil de probar y extender, ya que las implementaciones concretas pueden cambiar sin alterar la logica principal.

Ejemplo: Imagina una cafetera que viene con una marca especifica de filtro incorporado. Si quisieras cambiar el tipo de filtro, tendrias que modificar la estructura interna de la cafetera. En cambio, si la cafetera acepta cualquier tipo de filtro que cumpla con una forma o estandar, podes usar cualquier marca sin modificar nada mas. La cafetera depende de una abstraccion (el estandar del filtro), no de una implementacoin concreta.

### Estructuras de Clases

