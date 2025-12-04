# División de aumento en descarga

**¿Qué pasa?:**

    Se realizó una sola descarga del producto pero se generaron dos facturas de la descarga por
    lo que se requiere dividir la entrada para que corresponda con lo facturación. Esta división se
    hace por la mitad.

**Solución:** 

Se debe contar con la tira de la entrada (o descarga o aumento de inventario), por lo que si no 
la proporcionaron se debe pedir. Se incluye imagen de referencia.

INSERTAR IMAGEN

En la base de datos de la estación
- Modificar la entrada actual para que solo registre la primera mitad del volumen.
- Crear una nueva entrada con la segunda mitad.

Procedimiento:
1. Identificar la entrada original mediante los siguientes criterios:
    - id_turno
    - id_producto
    - id_tanque (si aplica)
  
2. Calcular la diferencia de volumen (**volumen_final** - **volumen_inicial**) y compararla con el aumento bruto de la tira.
3. Dividir la diferencia a la mitad.
4. Actualizar la entrada original:
    - Ajustar el **volumen_final** sumando solo la primera mitad.
    - Modificar la **temperatura_final** y **fecha_final** según corresponda (valor intermedio entre inicial y final).
    - Recalcular **diferencia** y **diferencia_corregida**.
  
5. Crear una nueva entrada en la que se registrara la segunda mitad:
    - En el campo **id_compra** es 0
    - Asignar mismo **id_turno**, **id_producto**, **id_tanque**
    - Asignar como **volumen_inicial** el nuevo volumen final de la entrada anterior (la primera mitad).
    - Ajustar el **volumen_final** con la segunda mitad.
    - Ajustar la **temperatura_inicial**, **fecha_inicial**, **temperatura_final** y **fecha_final** proporcionales al intervalo (iniciando con los valores finales de la entrada anterior).
  
6. Verificar que ambas entradas permanezcan dentro del rango horario del turno correspondiente.

**Ejemplo:**

| Campo     | Entrada original (antes) | Entrada 1 (ajustada) | Entrada 2 (nueva) |
| --------- | ------------------------ | -------------------- | ----------------- |
| id_entrada | 100 | 100 | 101 |
| id_compra | 0 | 0 | 0 |
| id_tanque | 1 | 1 | 1 |
| id_producto | 2 | 2 | 2 |
| id_turno | 2025080203 | 2025080203 | 2025080203 |
| volumen_inicial | 3067.89 | 3067.89 | 3567.89(nuevo val calculado) |
| volumen_final | 4067.89 | 3567.89 (nuevo val calculado) | 4067.89 (val entrada original) |
| temperatura_inicial | 31.50 | 31.50 | 32.00 |
| temperatura_final | 32.60 | 32.00 | 32.60 |
| fecha_inicial | 2025-08-02 20:17:00 | 2025-08-02 20:17:00 | 2025-08-02 20:31:00 |
| fecha_final | 2025-08-02 20:46:00 | 2025-08-02 20:31:00 | 2025-08-02 20:46:00 | 
| diferencia | 1000 | 500 | 500 |
| diferencia_corregida | 1000 | 500 | 500 |

---
#### [Indice](../Indice.md)
