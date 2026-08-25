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
