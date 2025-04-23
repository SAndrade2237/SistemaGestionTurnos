## Principio de Responsabilidad Unica (SRP)

### Proposito del principio:
El principio de Responsabilidad Unica resuelve el problema de clases que realizan multiples tareas, lo que dificulta su mantenimiento y extension. Cuando una clase tiene mas de una razon para cambiar, se complica su modificacion, ya que un cambio en una parte del sistema podria afectar otras funciones que no estan relacionadas, creando errores inesperados.

### Tipo del principio:
SRP es un principio de cohesion. Busca que cada clase se encargue de una unica responsabilidad, lo que hace que el codigo sea mas limpio, entendible y facil de modificar.

### Como lo soluciona:
Divide las clases para que cada una tenga una unica razon para cambiar, enfoncandose en una funcionalidad. Esto facilita el mantenimiento, ya que los cambios en una parte del sistema no afectan funcionalidades no relacionadas.

### Motivacion
En el diagrama, se observa que la clase Recepcionista tiene metodos para registrar pacientes, cancelar turnos y asignarlos. Estas son dos responsabilidades distintas: gestion de usuarios y gestion de turnos. Si cambia la forma de registrar un paciente (por ejemplo, añadiendo verificacion por email), la clase Recepcionista se veria afectada, aunque no tenga los relacion con los turnos.

Separando las responsabilidades en clases diferentes, por ejemplo GestorPaciente y GestorTurnos, se cumple SRP, y cada clase se puede mantener y actualizar de forma mas clara y sin afectar otras funcionalidades.

Ejemplo: en una oficina de correos, si una sola persona se encarga de recibir paquetes, clasificarlos, antender clientes y entregar correspondencia, cualquier cambio o error puede afectar todo el proceso. En cambio, si cada empleado tiene una tarea especifica, el sistema funciona mejor y es mas facil de ajustar o mejorar.

### Estructuras de Clase

[Link diagrama SRP](https://drive.google.com/file/d/1a1VsXyi3AmNyzNlwK12anT0YsTsb2Wzj/view?usp=sharing)

![Image](https://github.com/user-attachments/assets/bf61acac-0325-4f88-8216-430ed3e78e8e)
