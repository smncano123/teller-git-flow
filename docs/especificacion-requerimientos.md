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

### RF-02 - [Nombre del requerimiento]

#### Resumen

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|

#### Reglas o condiciones

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|

#### Resultado esperado


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
