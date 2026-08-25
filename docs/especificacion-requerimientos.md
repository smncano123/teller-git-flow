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


### RF-03 - [Nombre del requerimiento]

#### Resumen

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|

#### Reglas o condiciones

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|

#### Resultado esperado


### RF-04 - [Nombre del requerimiento]

#### Resumen

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|

#### Reglas o condiciones

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|

#### Resultado esperado


## 4. Gestión de Versiones

### Ramas utilizadas

### Proceso de integración

### Conflictos encontrados
