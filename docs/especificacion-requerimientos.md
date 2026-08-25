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
