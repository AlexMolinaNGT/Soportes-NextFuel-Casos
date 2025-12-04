# Correccion de mermas

**Únicamente se corrigen mermas  en Yugar (la de pueblo viejo)**

En otro caso se puede responder algo como esto:

    En cuanto a las mermas, nosotros no realizamos el ajuste, este tema lo pueden 
    revisar con el encargado que realiza la revisión de las mermas. 

```SQL
SELECT * FROM nextfuel_cert.cortetanques where id_turno like '20250720%'
```

INSERTAR IMAGEN

Se debe ingresar el nivel de tanque en el campo **corte_inicio**, pero como no lo vemos lo buscamos en el turno anterior.

INSERTAR IMAGEN 1

INSERTAR IMAGEN 2

Revisar en el sistema administrativo se revisa si hubo ventas en el menu …/Turnos filtrando por el dia

INSERTAR IMAGEN 1

INSERTAR IMAGEN 2

Vemos que en el turno 1 esta en ceros, porque no hubo venta, por lo que en la tabla **cortetanques** en el campo **corte_fin** queda con lo mismo que en **corte_inicio**, en este caso 

INSERTAR IMAGEN 1

INSERTAR IMAGEN 2

---
#### [Indice](../Indice.md)
