# Importar la factura
Para esto se debe habilitar la línea

```JS
//await this.generar_factura(facturadas);
```

del archivo **Nextfuel\controladores\ventas\ventas.js** 

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

Ahora se debe ejecutar la función

**portalFacturacion.consultarVentas([327377])**

Ahora ya se debería mostrar la factura en el listado de facturas del Administrativo

INSERTAR IMAGEN 

Ahora se le informa al facturista que ya puede cancelar la factura desde el Administrativo

**Correo sugerido:**

    Ya se encuentra disponible la factura para que usted proceda con la cancelación.

---
#### [Indice](../Indice.md)
