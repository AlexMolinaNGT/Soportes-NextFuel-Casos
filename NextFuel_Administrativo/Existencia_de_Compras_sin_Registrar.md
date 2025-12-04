# Existencia de Compras sin Registrar

## Existe una compra sin registrar

**Solución:** 

Unión de entradas

    Existe un caso donde llega un pipero el camion que descarga el combustible en la estación y 
    este lleva la cantidad de acuerdo a la factura.
    Actualización: Requieren unir dos (o más) entradas en una sola, ya que solo se tiene una 
    factura. El sistema dividió en tres la entrada y arroja estas 3 tiras.

INSERTAR IMAGEN

La factura es la siguiente:

INSERTAR IMAGEN

Se tienen tres entradas con los ids **1287** **1288** y **1289**:

INSERTAR IMAGEN

En caso que ya se haya **realizado el registro de la compra** (en este ejemplo el id 1008, 
imagen siguiente de la izquierda) se debe pedir (al que solicitó la unión) que se cancele la 
compra, para poder hacer la unión. El folio que se debe pasar al solicitante es el de 
**compra.folio_unico_relacion**.

INSERTAR IMAGEN

Después de la unión de las entradas **1287** **1288** y **1289**:

INSERTAR IMAGEN

las entradas **1288** y **1289** se eliminaron y solo quedo la **1287** con la suma de ambas

---
#### [Indice](../Indice.md)
