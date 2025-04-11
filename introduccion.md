# Introduccion


## Descripcion del paradigma oriendado a objetos
El paradigma orientado a objetos (POO) organiza el software mediante 'objetos', que combinan datos y métodos. Se fundamenta en principios como la encapsulación, la herencia y el polimorfismo, lo que permite una mayor reutilización del código, una mejor organización y la creación de programas más escalables y fáciles de mantener.

Es importante porque permite crear programas más grandes, complejos y fáciles de mantener. Facilita la reutilización de código, lo que ahorra tiempo y esfuerzo. Al estructurar el código en clases y objetos, se fomenta la organización, lo que hace el código más eficiente y comprensible.


## Los cuatros fundamentos de POO
<ins>***Abstracción:***</ins> Es el proceso de ocultar los detalles complejos y mostrar solo la información esencial. Se logra mediante clases abstractas que actúan como plantillas, permitiendo que las clases derivadas implementen los métodos específicos.

**Ejemplo:** Cajero automatico: Solo presionas botones para retirar dinero, transferir o consultar tu saldo.

 El sistema esta ocultando los detalles tecnicos y muestra solo lo que es necesario para el usuario: seleccionar una opcion. No importa como se gestionan internamente las transacciones ni como se validan los datos. El cajero te da una interfaz simple y clara para interactuar con el sistema bancario sin preocuparte por los procesos complicados detras de la pantalla.

| Cajero automatico| 
| ----------- | 
| Opcion 1: Consultar saldo | 
| Opcion 2: Retiro de efectivo |
| Opcion 3: Transferencias | 

<ins>***Encapsulación:***</ins> Consiste en ocultar los detalles internos de un objeto y exponer solo los métodos necesarios para interactuar con él. Esto se logra mediante el uso de modificadores de acceso y métodos de control como getters y setters.

**Ejemplo:** Licuadora: Solo usas el boton de encendido y controlas la velocidad.

La licuadora oculta su funcionamiento interno (como el motor y las cuchillas) y solo te da los controles que necesitas (encender, apagar, ajustar velocidad). De esta manera, la complejidad del sistema está "encapsulada" y no necesitas saber cómo funciona internamente para poder usarla.

| Licuadora | 
| ----------- | 
| Boton de encendido/apagado | 
| Ajuste de velocidad |



<ins>***Herencia:***</ins> Permite que una clase derive de otra, heredando sus atributos y métodos. Esto facilita la reutilización del código y la extensión de funcionalidades sin duplicación.

**Ejemplo:** Los vehiculos son una categoria general que incluye coches, camiones y motocicletas. Todos estos vehiculos tienen cosas en comun, como tener ruedas y un motor, pero cada uno tiene diferencias que los hacen unicos.

El vehiculo es una clase base que tiene atributos comunes como ruedas, motor y capacidad para moverse. Luego Choche, Camion y Motocicleta heredan esas caracteristicas, pero cada uno añade nuevas caracteristicas especificas: el coche tiene puertas y aire acondicionado, el camion tiene capacidad para carga y remolque, y la motocicleta tiene un manubrio y un numero distintos de ruedas

| Vehiculo | 
| ----------- | 
| Ruedas | 
| Motor |
| Capacidad de moverse |

            
| Coche | 
| ----------- | 
| Numero de puertas | 
| Aire acondicionado |

            
| Camion | 
| ----------- | 
| Capacidad de carga | 
| Remolque |

            
| Motocicleta | 
| ----------- | 
| Numero de ruedas | 
| Manubrio|

**Polimorfismo:** Es la capacidad de un objeto de adoptar diferentes formas. Permite que un mismo método se ejecute de manera diferente según el tipo de objeto que lo invoque, aumentando la flexibilidad y adaptabilidad del sistema.


## Requisitos iniciales del sistema
■ Llevar historial de turnos de pacientes.

■ Asignar turnos a los medicos para evitar solapamiento.

■ Notificar turnos aceptados, cancelados o modificados.

■ Restringir el acceso a la informacion de pacientes y profesionales.

■ Registrar en el sistema a pacientes y profecionales.



## Casos de Uso

### Caso de uso 1: **Admisión de paciente**

**Actor(es) involucrado(s):** Recepcionista

**Descripción breve:** El recepcionista registra a un nuevo paciente.

**Flujo principal de eventos:**
1. El recepcionista abre el sistema de gestión de pacientes.
2. El sistema solicita las credenciales de acceso al recepcionista.
3. El recepcionista ingresa sus credenciales de usuario y contraseña.
4. El sistema valida las credenciales y permite el acceso al sistema.
5. El recepcionista selecciona la opcion "Registrar nuevo paciente".
6. El recepcionista solicita los datos del paciente.
7. El sistema verifica si el paciente ya esta registrado en la base de datos.
8. Si no esta registrado, el recepcionista completa el formulario con los datos requeridos.
9. El sistema genera un ID unico para el paciente y guarda los datos en la base.
10. El sistema confirma la admision y muestra un resumen del perfil del paciente.

**Precondiciones:**
- El recepcionista debe tener acceso al sistema.
- El paciente debe brindar sus datos correctamente.

**Postcondiciones:**
- El paciente queda registrado en el sistema con un ID único.
- El proceso de admisión ha sido completado exitosamente.

---

### Caso de uso 2: **Gestión de turnos asignados**

**Actor(es) involucrado(s):** Médico

**Descripción breve:** El médico revisa los turnos asignados.

**Flujo principal de eventos:**
1. El médico ingresa al sistema de gestión de turnos.
2. El sistema solicita las credenciales del medico.
3. El medico ingresa su ID y contraseña.
4. El sistema valida las credenciales y permite el acceso.
5. El medico accede a la seccion "Mis turnos".
6. El sistema muestra los turnos asignados por dia y semana.
7. El medico selecciona  un turno para ver los detalles del paciente.
8. El medico puede modificar horarios si hay conflictos o notificar indisponibilidad.
9. El sistema registra cualquier modificacion o actualizacion en tiempo real.
10. El sistema muestra un resumen actualizado del calendario del medico.

**Precondiciones:**
- El médico debe tener acceso al sistema.
- Los turnos deben estar previamente cargados en el sistema.

**Postcondiciones:**
- El médico puede planificar su jornada según los turnos asignados.

---

### Caso de uso 3: **Consulta historial de turnos paciente**

**Actor(es) involucrado(s):** Médico

**Descripción breve:** El médico consulta el historial de turnos de un paciente.

**Flujo principal de eventos:**
1. El médico ingresa al sistema de gestión de pacientes.
2. El sistema solicita las credenciales del médico.
3. El medico ingresa su ID y contraseña.
4. El sistema valida las credenciales y permite el acceso.
5. El medico selecciona la opcion "Historial del paciente".
6. El medico solicita al paciente su nombre completo o ID.
7. El sistema busca el historial correspondiente en la base de datos.
8. el sistema muestra la lista de turnos con fecha, medico asignado y diagnostico.
9. El medico puede ver el detalle de cada turno individualmente.
10. El sistema permite descargar o imprimir el historial si es necesario.

**Precondiciones:**
- El paciente debe tener un historial registrado en el sistema.
- El médico debe tener acceso autorizado al historial del paciente.

**Postcondiciones:**
- El médico obtiene la información completa del historial de turnos del paciente.

---

### Caso de uso 4: **Cancelación de turno**

**Actor(es) involucrado(s):** Recepcionista y paciente

**Descripción breve:** El paciente cancela un turno previamente asignado.

**Flujo principal de eventos:**
1. El paciente solicita la cancelación de su turno al recepcionista.
2. El recepcionista accede al sistema de gestion de turnos.
3. el sistema solicita sus credenciales de acceso.
4. El recepcionista ingresa su usuario y contraseña.
5. El sistema valida el acceso y permite continuar.
6. El recepcionista solicita al paciente su nombre y numero de turno.
7. El sistema verifica si el turno existe y si esta dentro del plazo de cancelacion (72 horas).
8. Si cumple con los requisitos, el recepcionista confirma la cancelacion.
9. El sistema cambia el estado del turno a "cancelado".
10. El sistema notifica al medico y al paciente sobre la cancelacion.

**Precondiciones:**
- El paciente debe tener un turno asignado.
- La cancelación debe realizarse con 72 horas de anticipación.

**Postcondiciones:**
- El paciente ha cancelado el turno con éxito.
- El médico recibe una notificación de la cancelación del turno.

---

### Caso de uso 5: **Nuevo médico en el centro de salud**

**Actor(es) involucrado(s):** Médico y recepcionista

**Descripción breve:** Se incorpora un nuevo médico al centro de salud.

**Flujo principal de eventos:**
1. El recepcionista accede al sistema de gestión de personal.
2. El sistema solicita las credenciales de acceso del recepcionista.
3. El recepcionista ingresa su ID y contraseña para acceder al sistema.
4. El sistema valida las credenciales y permite continuar.
5. El recepcionista selecciona la opcion "Agregar nuevo medico".
6. El recepcionista solicita al nuevo medico su documentacion.
7. El sistema valida los documentos y verifica que el medico no este registrado previamente.
8. EL sistema genera un ID unico y crea el perfil del medico.
9. El sistema asigna al medico un calendario inicial con turnos disponibles.
10. El nuevo medico recibe sus credenciales de acceso al sistema.

**Precondiciones:**
- El médico debe haber completado todos los requisitos para ser contratado.
- El médico debe estar registrado como profesional habilitado.

**Postcondiciones:**
- El médico queda registrado en el sistema como personal del centro de salud.
- El sistema incluye al nuevo médico en el calendario de turnos y lo habilita para recibir pacientes.

## Boceto

[Link boceto](https://drive.google.com/file/d/1S0EYYTKtPr1tepANDVSbaqEgU2LtwZYW/view?usp=sharing)

![Image](https://github.com/user-attachments/assets/5e96f6d3-0ecc-49e1-b2f5-37c93bc97855)

