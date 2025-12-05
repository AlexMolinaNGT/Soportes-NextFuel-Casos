# Recepciones
**El soporte llega de esta forma:**

    17/08/2025 Ejército
    En el JSON en Extra el volumen de existencias anterior aparece como 31101 pero 
    según las tiras de veeder y el VPI la cantidad correcta es 31203, se debe corregir la cantidad en el JSON.

**Se ejecutan las siguientes consultas para ubicar el detalle:**

```SQL
SELECT * FROM nextfuel_cert.productos;
SELECT * FROM nextfuel_cert.tanques;
SELECT * FROM nextfuel_cert.cortetanques where id_turno like "20250816%" and id_producto = 2 and id_tanque = 2;
SELECT * FROM nextfuel_cert.cortetanques where id_turno like "20250817%" and id_producto = 2 and id_tanque = 2;
SELECT p.nombre, c.id_turno as turno, c.corte_inicio as inicio_nivel, c.corte_fin as fin_nivel, c.fecha FROM nextfuel_cert.cortetanques c left join productos p on p.id_producto = c.id_producto where id_turno like "20250817%" and c.id_producto = 1 and c.id_tanque = 1;

```

INSERTAR IMAGEN

Este fue un caso especial en el que se encontraron registros duplicados y la información no cuadraba por el turno.

*Normalmente ellos pueden abrir el turno y modificar la diferencia.

---
#### [Indice](../Indice.md)
