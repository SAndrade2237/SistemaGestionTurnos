# INTRODUCCION

## DESCRIPCION DEL PARADIGMA ORIENTADO A OBJETOS
El paradigma orientado a objetos (POO) organiza el software mediante 'objetos', que combinan datos y métodos. Se fundamenta en principios como la encapsulación, la herencia y el polimorfismo, lo que permite una mayor reutilización del código, una mejor organización y la creación de programas más escalables y fáciles de mantener.

Es importante porque permite crear programas más grandes, complejos y fáciles de mantener. Facilita la reutilización de código, lo que ahorra tiempo y esfuerzo. Al estructurar el código en clases y objetos, se fomenta la organización, lo que hace el código más eficiente y comprensible.

## LOS CUATRO FUNDAMENTOS DE POO
**Abstracción:** Es el proceso de ocultar los detalles complejos y mostrar solo la información esencial. Se logra mediante clases abstractas que actúan como plantillas, permitiendo que las clases derivadas implementen los métodos específicos.

**Encapsulación:** Consiste en ocultar los detalles internos de un objeto y exponer solo los métodos necesarios para interactuar con él. Esto se logra mediante el uso de modificadores de acceso y métodos de control como getters y setters.

**Herencia:** Permite que una clase derive de otra, heredando sus atributos y métodos. Esto facilita la reutilización del código y la extensión de funcionalidades sin duplicación.

**Polimorfismo:** Es la capacidad de un objeto de adoptar diferentes formas. Permite que un mismo método se ejecute de manera diferente según el tipo de objeto que lo invoque, aumentando la flexibilidad y adaptabilidad del sistema.

## REQUISITOS INICIALES DEL SISTEMA
■ Llevar historial de turnos de pacientes.

■ Asignar turnos a los medicos para evitar solapamiento.

■ Notificar turnos aceptados, cancelados o modificados.

■ Restringir el acceso a la informacion de pacientes y profesionales.

■ Registrar en el sistema a pacientes y profecionales.


## CASOS DE USO
<ins>1- Admision paciente</ins>

**Actor(es) involucrado(s):** Recepcionista

**Descripcion breve:** Llega un nuevo paciente al centro de salud.

**Flujo principal de eventos:**

El recepcionista abre el sistema de gestion de pacientes.

Carga los datos del paciente.

Chequea si ya es paciente o es un ingresante.

Guarda la consulta.

**Precondiciones:**

El recepcionista debe tener acceso al sistema de gestion de pacientes.

El paciente debe brindarle sus datos al recepcionista.

**Postcondiciones:**

El paciente queda registrado en el sistema.


<ins>2-Gestion de turnos asignados</ins>

**Actor(es) involucrado(s):** Medico

**Descripcion breve:** El medico corrobora sus turnos asignados.

**Flujo principal de eventos:**

El medico ingresa al sistema 

Accede al calendario

Revisa sus turnos asignados

**Precondiciones:**
El medico debe terner acceso al sistema

Los turnos deben estar cargados en el sistema

**Postcondiciones:**

El medico puede planificar su jornada en base a los turnos asignados


<ins>3- Consulta historial de turnos paciente</ins>

**Actor(es) involucrado(s):** Medico

**Descripcion breve:** El medico consulta el historial de un paciente

**Flujo principal de eventos:**

El medico ingresa al sistema de gestion de pacientes

Solicita los datos al paciente

Revisa el historial de turnos del paciente

**Precondiciones:**

El paciente debe tener un historial registrado en el sistema

**Postcondiciones:**
El medico obtiene la informacion del historial del paciente


<ins>4- Cancelacion de turno</ins>

**Actor(es) involucrado(s):** Recepcionista y paciente

**Descripcion breve:** El paciente quiere cancelar un turno

**Flujo principal de eventos:**

El recepcionista ingresa al sistema de gestion de turnos

Solicita datos al paciente

Busca el turno a cancelar

El sistema actualiza el estado del turno a "cancelado"

**Precondiciones:**

El paciente debe tener un tunro asignado

La cancelacion del turno debe hacerse 72hs antes del mismo

**Postcondiciones:**
El paciente pudo cancelar el turno

Se envia notificacion de cancelacion al medico


<ins>5- Nuevo medico en el centro de salud</ins>

**Actor(es) involucrado(s):** Medico y recepcionista

**Descripcion breve:** Se incorpora un nuevo medico al centro de salud

**Flujo principal de eventos:** 

El recepcionista ingresa al sistema de gestion de personal

Solicita la informacion requerida al medico

Asigna al medico un ID único

El sistema guarda la informacion y el medico es oficialmente agregado al centro de salud

**Precondiciones:**

El medico debe haber completado los requisitos para ser contratado

El medico debe estar registrado en el sistema de salud como profesional habilitado

**Postcondiciones:**

El medico queda registrado en el sistema como personal del centro de salud

El sistema incluye al nuevo medico en el calendario de turnos y lo habilita para recibir pacientes
