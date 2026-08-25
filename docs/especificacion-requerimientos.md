# Especificación de Requerimientos

## 1. Descripción del sistema

## 2. Integrantes

- Nombre:
- Nombre:
- Nombre:
- Nombre:
- Nombre:

## 3. Requerimientos Funcionales

### RF-01 - [Nombre del requerimiento]

#### Resumen

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|

#### Reglas o condiciones

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|

#### Resultado esperado


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

### Proceso de integración

### Conflictos encontrados
