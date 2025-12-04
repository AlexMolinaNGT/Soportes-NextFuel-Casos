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

# Documentacion obsoleta, esto esposible que se pueda borrar

```SQL
Select * from ticket where id_ticket in (65687376);
Select * from facturas where folio = '5c7a598d-3a6b-45fa-9d7a-ed88d899acd9';
```

INSERTAR IMAGEN 

Importar Facturas desde el portal de facturación

El cliente solicita cancelar factura en el portal de facturación pero el facturista no puede acceder al portal porque es privado para cada cliente. 
La siguiente imagen es un ejemplo de factura donde se resaltan los datos que se ocuparan

INSERTAR IMAGEN 

Revisar que no exista la factura en el Admin tanto activas como en el listado de canceladas.

INSERTAR IMAGEN 

INSERTAR IMAGEN 

Confirmamos que no existe en el listado de canceladas.
Se tiene que importar al Administrativo Compras / Facturación

Obtener el ticket de la venta en la misma factura en este ejemplo el ticket es 327377

INSERTAR IMAGEN 

y ejecutar esta función desde la inspección del Administrativo
portalFacturacion.consultarVentas([327377])

INSERTAR IMAGEN

INSERTAR IMAGEN

Con esto se revisa que el ticket corresponda a la factura y que la factura no está en el Administrativo

---
#### [Indice](../Indice.md)
