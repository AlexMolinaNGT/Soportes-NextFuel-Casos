# Diferencias entre vental total y monto de la estación:
En este caso en particular nos reportan una diferencia a favor en el total del monto de la estación con las ventas totales

INSERTAR IMAGEN

**CASO COMÚN:**

    HIPÓTESIS: Debido a una dispersión realizada por el sistema y 
    una perdida de conexión es que se ingresaron de mas 2 entradas

Nos dirigiremos a la BD de la estación y ejecutaremos esta consulta que nos dirá la diferencia entre la suma y los ticket totales:
```SQL
SELECT t1.id_ticket, total_ticket, sum(monto) suma
FROM nextfuel_cert.ticket t1
join ticketpago t2 on t1.id_ticket = t2.id_ticket
group by t1.id_ticket  having suma != total_ticket;
```

INSERTAR IMAGEN 1

INSERTAR IMAGEN 2

Si nos arroja un resultado tendríamos que hacer un delete de la entrada extra , en el caso aplicado , fueron 2 más de $1582, dando la diferencia de $1582 en la primera captura.

**CASO ESPECIAL:** 

    Si el método de pago es 101 irse a la tabla ventasnexum y buscar el
    ticket con el campo id_venta, eliminar el duplicado que también aparece

INSERTAR IMAGEN

## **ELIMINANDO ENTRADAS:**

**Ticketpago:**

INSERTAR IMAGEN

```SQL
DELETE FROM `nextfuel_cert`.`ticketpago` WHERE (`id_ticket_pago` = '28451') and (`id_ticket` = '25683') and (`id_metodo_pago` = '101') and (`id_producto` = '2') and (`id_reembolso` = '0');
```

**Ventasnexum:**

INSERTAR IMAGEN

```SQL
DELETE FROM `nextfuel_cert`.`ventasnexum` WHERE (`id` = '366');
```

Una vez terminado el proceso hacemos la comprobación con la consulta de suma y nos debe de aparecer vacía la diferencia así habremos acabado el proceso.

INSERTAR IMAGEN

---
#### [Indice](../Indice.md)
