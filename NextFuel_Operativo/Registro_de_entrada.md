# Registro de entrada

**¿Qué reportan?:**

    En algunas ocasiones no se registra en el sistema la descarga de la pipa de combustible al 
    tanque, por lo que se tiene que registrar directamente en la base de datos en la tabla 
    “entradas”. Los datos se obtienen de la tira de descargas, por lo que hay que solicitar la tira de
    descarga

**Solución:** 

La tira de descarga se debe solicitar a la estación
En la base de datos de la estación crear un nuevo registro en la tabla entradas con los datos 
que vienen en la tira de descargas.  Incluyo imagen más abajo, pero antes, se debe revisar lo 
siguiente

Puntos a revisar antes de guardar los cambios:
  - El **id_compra** se establece en 0. 
  - El **id_tanque** se puede consultar desde la tabla de tanques con el nombre del producto correspondiente.
  - El campo **diferencia** y la **diferencia corregida** se puede verificar restando **volumen_final** menos **volumen inicial**
  - Revisar que la hora de inicio y fin  esté dentro del turno (Horario de 24 hrs). En la tabla **turnos** se pueden revisar cuando inicia y terminan los turnos.

En la siguiente imagen se muestra desde donde se toman los datos.

INSERTAR IMAGEN

---
#### [Indice](../Indice.md)
