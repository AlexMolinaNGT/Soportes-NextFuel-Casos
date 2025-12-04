# Cancelación de factura que está en el Portal 
Se solicita la cancelación de una factura que está en el portal de facturación

[https://palmas.nextgt.com.mx/nexum/login](https://palmas.nextgt.com.mx/nexum/login)

INSERTAR IMAGEN

Actualización Oct 09

Ir al menú Lista de ventas

ingresar la fecha de la factura y dar click en buscar ventas

INSERTAR IMAGEN

Dar click en **Sincronizar Información**

INSERTAR IMAGEN

**Solución:** Importar la factura cancelada al Administrativo

Se debe ingresar al Administrativo (no compilado) y descomentar esta linea de codigo (del archivo Nextfuel\controladores\ventas\ventas.js) para generar y consultar la venta:

**DESCOMENTAR ESTA LINEA:**

```JS
//await this.generar_factura(facturadas);
```

**ANTES:**

```JS
async consultarVentas(ventas = []){
            try{
                var [{id_estacion : clave}] = await estacion.registro();
                const datos = {
    				"estacion" : clave,
    				"ventas" : ventas
    			}
				let r = await this.enviar('ventas/estatus',datos); 
				let facturadas = r.filter(index => index.estatusFacturacion);
				//await this.generar_factura(facturadas);
				return facturadas;
            }
			catch(e){
                alertify.log("!Ups¡ Ha ocurrido un error al consultar las ventas en el portal de facturación");
				console.log(e);
				return [];
            }
		},
```

**DESPUES:**

```JS
async consultarVentas(ventas = []){
            try{
                var [{id_estacion : clave}] = await estacion.registro();
                const datos = {
    				"estacion" : clave,
    				"ventas" : ventas
    			}
				let r = await this.enviar('ventas/estatus',datos); 
				let facturadas = r.filter(index => index.estatusFacturacion);
				await this.generar_factura(facturadas);
				return facturadas;
            }
			catch(e){
                alertify.log("!Ups¡ Ha ocurrido un error al consultar las ventas en el portal de facturación");
				console.log(e);
				return [];
            }
		},
```

Ahora se ejecuta la función **portalFacturacion.consultarVentas([ # ])** en donde # se sustituye por el número del ticket

INSERTAR IMAGEN

y ya podemos revisar que se encuentra el listado de facturas en el Administrativo.

INSERTAR IMAGEN

---
#### [Indice](../Indice.md)
