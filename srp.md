## Principio de Responsabilidad Unica (SRP)

### Proposito del principio:
El principio de Responsabilidad Unica resuelve el problema de clases que realizan multiples tareas, lo que dificulta su mantenimiento y extension. Cuando una clase tiene mas de una razon para cambiar, se complica su modificacion, ya que un cambio en una parte del sistema podria afectar otras funciones que no estan relacionadas, creando errores inesperados.

### Tipo del principio:
SRP es un principio de cohesion. Busca que cada clase se encargue de una unica responsabilidad, lo que hace que el codigo sea mas limpio, entendible y facil de modificar.

### Motivacion
En sistemas complejos como este (Sistema de gestion de turnos medicos), un problema comun es la mezcla de responsabilidades dentro de las clases. Por ejemplo, una clase que gestiona tanto la representacion de un turno como la logica para asignarlo o notificar a los usuarios puede volverse dificil de mantener. Cualquier cambio en la asignacion de turnos o en la forma de representar los datos podria tener efectos nod eseados en otras partes del sistema, lo que incrementa el riesgo de errores.

El principio de Responsabilidad Unica (SRP) resuelve este problema al garantizar que cada clase tenga una unica razon para cambiar. Esto implica que una clase debe ocuparse de una sola tarea, lo que facilita el mantenimiento y la extension del sistema sin afectar otras funcionalidades.

Ejemplo: en una oficina de correos, si una sola persona se encarga de recibir paquetes, clasificarlos, antender clientes y entregar correspondencia, cualquier cambio o error puede afectar todo el proceso. En cambio, si cada empleado tiene una tarea especifica, el sistema funciona mejor y es mas facil de ajustar o mejorar.

### Estructuras de Clases
