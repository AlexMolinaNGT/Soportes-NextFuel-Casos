# Mermas 

**Solicitud:**

    Disculpe para solicitar de favor el apoyo con las ventas del dia 17 de julio
    El.sistema las envia como merma
    Le puedo pasar los cortes del tanque
    Del dia 17 ??

INSERTAR IMAGEN

**Revisión:**

Caso 1: Turno adicional

INSERTAR IMAGEN

INSERTAR IMAGEN

INSERTAR IMAGEN

INSERTAR IMAGEN

INSERTAR IMAGEN

INSERTAR IMAGEN

INSERTAR IMAGEN

Aqui fue un caso de revision:

    No hubo registro de cortes, lo cual no es raro pero si es un indicativo que no se capturo la información.
    En este caso me meti a la estacion y vi que el tanque estaba desconectado.
    Se reinicio el sistema.

Falta imagen de referencia

**Reinicio** = Cerrar y volver abrir el programa:

Asi deberia ser el estado del tanque:

INSERTAR IMAGEN

INSERTAR IMAGEN

Si no salen turnos para editar los cortes, eso significa que el turno 
esta en precierre:

INSERTAR IMAGEN

INSERTAR IMAGEN

INSERTAR IMAGEN

INSERTAR IMAGEN

---

Hay 2 maneras o opciones:

Opcion 1: Solicitar que abran el turno donde no tiene registro

Esto se puede se puede pedir e irnos al Modulo de control de mermas para poder ajustar de acuerdo a la tira.

En este caso se reviso en la base de datos, y no hay dato existen en el corte de la tira:

INSERTAR MUCHAS IMAGENES

En este caso me fui por la opcion rapida, aplicar el cambio en la BD debido al tiempo de urgencia del soporte y tiempos de espera

Recordar siempre, Actualizar para poder ver reflejado el cambio:

INSERTAR MUCHAS IMAGENES

**Caso extra:**

    Solicitando la cancelación de los ticket creados por cargas perdidas del turno 2025071702 del dia 17.07.2025:
    # 631680 $1450.28
    # 631683 $1589.02
    Se había levantado el soporte #9622671530 por supuestas cargar perdidas de acuerdo a las lecturas mecánicas que arrojo el sistema 
    pero checando a detalle las lecturas manuales de los turno 1 , 2 Y 3 realmente no fueron ventas perdidas lo reportado 
    a continuación :
    -- 2.- ( TICKET REPORTADO 631680 $1450.28 )isla 3 / bomba 6 / manguera 11 / supreme / diferencia litros: 239.070 / suma litros: 180.449faltante: 58.621 litros.

INSERTAR IMAGEN

    -- 3.- ( TICKET REPORTADO 631683 $1589.02 )isla 3 / bomba 6 / manguera 12 / extra / diferencia litros: 463.46 / suma litros: 396.946faltante: 66.514 litros.
    -- "Adjunto evidencia de las lecturas manuales de los 3 turnos

```SQL
Select * from ticket where id_ticket in (631680,631683);
```

En este caso, se realizaron la inserción de las ventas perdidas, pero de acuerdo a lo solicitado , las ventas estan demas, por lo que se tienen que omitir o dar de baja.

Como tal no podemos eliminar registros, por lo cual estas se reducen a 0 litros.

Actualmente este proceso solo se puede realizar en la BD:

INSERTAR IMAGEN X 4

ESTO REDUCIRA LA VENTA A $0 TANTO EN PESOS COMO LITRAJE
SE DEBE VERIFICAR ANTES QUE POR OMISION DE LA PERSONA NO ESTE FACTURADA
CON ESO ME REFIERO AL FOLIO
EN AMBOS CASOS SE REDUJO A CERO Y CONSULTANDO SE VE REFEJADO:

INSERTAR IMAGEN

EN TODAS LAS TABLAS COMO VERIFICACION RELACIONADAS  TICKETS DEBERIA BAJAR LOS LITROS Y PESOS

TICKET,TICKETPRODUCTOS Y TICKETPAGO

---

Configuracion Volumetricos:

[https://www.comercialrefinacion.pemex.com/portal/sccvi020/controlador](https://www.comercialrefinacion.pemex.com/portal/sccvi020/controlador)
[https://www.comercialrefinacion.pemex.com/portal/sccvi007/controlador?Destino=sccvi007_01.jsp](https://www.comercialrefinacion.pemex.com/portal/sccvi007/controlador?Destino=sccvi007_01.jsp)

INSERTAR IMAGEN

---
#### [Indice](../Indice.md)
