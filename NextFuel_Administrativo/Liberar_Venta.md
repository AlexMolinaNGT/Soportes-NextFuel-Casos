# Liberar venta (Ticket comprobado fiscalmente ante el SAT)

## Liberar Ticket

El facturista desea cancelar una factura en el portal de facturación, pero no tiene acceso, por lo que se debe importar la factura en el Administrativo 

### **Requisitos previos:**

Deben de incluir la factura donde se muestre que ya está cancelada por el SAT

**EJEMPLO:**

INSERTAR IMAGEN

Se debe tener el **UUID** (o folio fiscal) de la factura ya que se va a buscar por ese **UUID**, pero si nos envían la factura cancelada se puede obtener de ahí.

### Pasos para liberar venta

1. Ir al menú **Compras** / **Facturación**, filtrar por dia y por el folio fiscal de la factura para cancelarla

INSERTAR IMAGEN

2.  Ejecutar el Administrativo no compilado para ver la consola y ejecutar esto:
**portalFacturacion.consultarVentas([#])**
donde **#** debe se sustituirse por el ticket

revisar si tiene o no información en el campo factura

INSERTAR IMAGEN

o si puede tener 

INSERTAR IMAGEN

en ambos casos, si es null o no se continúa al paso 3

3.  ir al menú … (**tres puntos**) / **Soporte** / **Liberar Venta**, ingresar el número de ticket y dar click en el botón Liberar Venta

INSERTAR IMAGEN 1

INSERTAR IMAGEN 2

4. Ejecutar de nuevo **portalFacturacion.consultarVentas([#])**
y revisar que el estatusFacturacion sea **0**

INSERTAR IMAGEN 1

5. Confirmar que la factura se canceló en el menú Compras / Facturación Click en Botón “Facturas Canceladas”

INSERTAR IMAGEN 

**Respuesta de correo sugerida:**

    Buenas tardes

    Listo, ya se liberó el ticket

    Saludos.

---
#### [Indice](../Indice.md)
