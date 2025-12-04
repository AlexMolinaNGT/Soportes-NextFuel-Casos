# Inventario

Detalle del incidente:

INSERTAR IMAGEN

Se reportó que en el sistema VPI General, los productos **"Fluido Dirección Hidráulica"** y **"Mobil Coolant Convent 33 948 ml"** 
presentan cantidades existentes con decimales 40.88 y 130.88 en lugar de valores enteros 41 y 131.

**Acción correctiva:**

Se solicita redondear las piezas existentes al valor entero más cercano.

**Procedimiento para corrección de cantidades con decimales en inventario (VPI):**

1. Acceso y verificación en el sistema
- Ingresar al módulo de Reportes.
     
INSERTAR IMAGEN

- Localizar el reporte llamado "VPI".

INSERTAR IMAGEN

- Filtrar el reporte por la fecha indicada por el usuario, estableciendo la misma fecha tanto en el campo de inicio como en el de fin.

- Buscar en el listado los productos reportados.

INSERTAR IMAGEN

- Confirmar que las cantidades existentes coincidan con los valores especificados por el usuario (en este caso, con decimales).

2. Identificación de productos en la base de datos

- Acceder a la base de datos y localizar los productos en la tabla productos para obtener su id_producto.

INSERTAR IMAGEN

3. Revisión y ajuste en inventarios

INSERTAR IMAGEN

- Ejecutar la consulta para la tabla inventarios:

```SQL
SELECT * FROM nextfuel_cert.inventarios WHERE id_producto IN (21, 53);
```

- Identificar las cantidades con valores decimales.

INSERTAR IMAGEN

- Redondear los valores al número entero más cercano según la unidad de medida.

- Aplicar la actualización de los registro.

4. Validación en el sistema

- Regenerar el reporte VPI en el sistema para verificar que los cambios se reflejen correctamente.

INSERTAR IMAGENES

5. Evidencia y cierre

- Tomar captura de pantalla del reporte corregido o generar el PDF del mismo.

- Adjuntar la evidencia en la notificación de respuesta al usuario, indicando que el problema ha sido corregido.

INSERTAR IMAGENES

---
#### [Indice](../Indice.md)
