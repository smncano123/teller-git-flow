# Especificación de Requerimientos

## 1. Descripción del sistema
El sistema de gestión de tutorías académicas es una plataforma que permite organizar y administrar las tutorías ofrecidas por los profesores de la Universidad. El sistema permite a los profesores registrar tutorías indicando información como el tema, la fecha, la hora y la cantidad máxima de participantes. A su vez, los estudiantes pueden consultar las tutorías disponibles, inscribirse en ellas y cancelar su participación antes de que comiencen.

La plataforma busca centralizar la información de las tutorías, facilitar su consulta y controlar las inscripciones y los cupos disponibles.

## 2. Integrantes

- Nombre:Simon Cano
- Nombre:Sebastian Borrero
- Nombre:Takeshi Tatekawa
- Nombre:Maria jose Gomez


## 3. Requerimientos Funcionales

### RF-01 - registro-tutoria

#### Resumen 
el sistema debe poder registrar que una tutoria fue creada correctamente despues de que todos los parametros eesten completos 
#### Entrada
| Entrada | Tipo de dato | Descripción |
|---|---|---|
|ID profesor|String |identificador del profesor|
|tema tuto |String |tema a explicar|
|fecha|LocalDate|fecha de cuando se hara la tutoria |
|hora|LocalDate|hora en la cual se realizara la tutoria |
|cantidad de estudiantes|int |cantidad de estudintes que puedes estar en la tutoria |

#### Reglas o condiciones
No se permitirá programar una tutoría para una fecha anterior a la fecha actual y la cantidad máxima de participantes deberá estar entre 1 y 10 estudiantes
#### Salidas
| Salida | Tipo de dato | Descripción |
|---|---|---|
|mensaje|String|la tutoria fue creada correctamente|
#### Resultado esperado
Cuando el registro sea exitoso, el sistema asignará un identificador único a la tutoría e informará al profesor que esta fue creada correctamente

### RF-02 - consulta-tutorias

#### Resumen 
El estudiante podrá buscar y consultar las tutorías disponibles indicando obligatoriamente una fecha y, opcionalmente, una asignatura o tema. El sistema mostrará las tutorías que coincidan con los criterios de búsqueda y la información relevante de cada una.

#### Entradas

| Entrada | Tipo de dato | Descripción |
|Fecha|LocalDate|Fecha en la que el estudiante desea consultar las tutorías. Es obligatoria.|
|Asignatura/Tema|String|Asignatura o tema sobre el cual el estudiante desea buscar tutorías. Es opcional.|

#### Reglas o condiciones
- La fecha es obligatoria.
- La asignatura o tema es opcional.
- Solo se muestran tutorías disponibles que coincidan con la búsqueda.
- Si no hay coincidencias, se muestra un mensaje informándolo.

#### Salidas

| Salida | Tipo de dato | Descripción |
|Identificador|String|Identifica la tutoria|
|Tema|String|Tema de la tutoria|
|Profesor|String|Profesor Responsable|
|Fecha|LocalDate|Fecha de la tutoria|
|Hora|LocalDate|Hora de la tutoria|
|CuposDisponibles|Int|Cupos disponibles de la tutoria|
|Mensaje|String|Informa si no se encuentra tutorias|

#### Resultado esperado
El sistema devuelve al estudiante la lista de tutorías disponibles que coinciden con la fecha y, si fue indicada, con la asignatura o tema solicitado. Si no hay coincidencias, se muestra un mensaje informando que no existen tutorías disponibles para los criterios seleccionados.


### RF-03 - Inscripción tutoria

#### Resumen 
La plataforma tendra la opción de que el estudiante al una tutoría de su interés podrá solicitar su inscripción utilizando su código estudiantil y el identificador de la tutoría. Donde se verificara que el estudiante cumpla unas condiciones para que pueda inscribirse sin ninguna complicación o error en la plataforma.

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|
|codigoEstudiantil|String|Codigo que el estudiante tiene que lo relaciona con la institución educativa de la plataforma|
|identificador|String|Cadena de caracteres que identifica quien es la persona.

#### Reglas o condiciones
-El estudiante deberá encontrarse activo en la Universidad
-La tutoría deberá existir
-La tutoria deberá tener al menos un cupo disponible
-El estudiante no podrá encontrarse previamente inscrito en ella

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|
|mensajeConfirmacion|String|Mensaje que avisa al estudiante que se inscribio correctamente|
|mensajeError|String|Mensaje que avisa al estudiante que no se pudo inscribir y en que fallo el proceso|

#### Resultado esperado
-Cuando la inscripción sea exitosa, el sistema deberá registrarla, actualizar la cantidad de cupos disponibles y mostrar un mensaje de confirmación.
-Si alguna de las condiciones necesarias no se cumple, la inscripción no deberá realizarse y el sistema deberá informar la situación.

### RF-04 - cancelacion-inscripcion

#### Resumen
Permitir que un estudiante cancele su inscripción a una tutoría utilizando su código estudiantil y el identificador de la tutoría, siempre que exista una inscripción previa y la tutoría aún no haya comenzado

#### Entradas

| Entrada | Tipo de dato | Descripción |

| Entrada                     | Tipo de dato | Descripción                                                           |
| --------------------------- | ------------ | --------------------------------------------------------------------- |
| Código estudiantil          | String       | Identificador único del estudiante que desea cancelar su inscripción. |
| Identificador de la tutoría | String / int | Identificador de la tutoría en la que el estudiante está inscrito.    |

#### Reglas o condiciones

- El estudiante debe estar previamente inscrito en la tutoría.
- La tutoría no debe haber comenzado todavía.
- Si se cumplen ambas condiciones, se elimina la inscripción.
- Al eliminar la inscripción, se debe liberar nuevamente el cupo correspondiente.
- Si no existe una inscripción previa, no se puede realizar la cancelación.
- Si la tutoría ya comenzó, no se puede realizar la cancelación.
 - El sistema debe informar el motivo cuando la cancelación no sea posible.
#### Salidas

| Salida | Tipo de dato | Descripción |

| Salida                       | Tipo de dato | Descripción                                                                                      |
| ---------------------------- | ------------ | ------------------------------------------------------------------------------------------------ |
| Mensaje de operación exitosa | String       | Informa al estudiante que la inscripción fue cancelada correctamente y que el cupo fue liberado. |
| Mensaje de error             | String       | Indica el motivo por el cual no fue posible cancelar la inscripción.                             |


#### Resultado esperado
Si el estudiante está inscrito en la tutoría y esta aún no ha comenzado, el sistema elimina su inscripción, libera el cupo y muestra un mensaje confirmando que la cancelación fue exitosa. En caso contrario, la inscripción permanece sin cambios y se muestra un mensaje indicando el motivo por el cual no se pudo realizar la cancelación.

## 4. Gestión de Versiones

### Ramas utilizadas
-main
- develop
- feature/rf01-registro-tutoria
-feature/rf02-consulta-tutorias
-feature/rf03-inscripcion-tutoria
-feature/rf04-cancelacion-inscripcion
### Proceso de integración
main
   ↓
develop
   ↓
feature/*
   ↓
develop
   ↓
main
### Conflictos encontrados
NINGUNO
