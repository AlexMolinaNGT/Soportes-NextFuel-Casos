# Ruta Factura / Carpeta Compartida
Hay un mensaje que les sale en el módulo de Facturas de Nextfuel Administrativo

INSERTAR IMAGEN

Este mensaje nos dice que no se puede consultar la carpeta compartida que se encuentra en el servidor

Para ello debemos de consultar dependiendo en la estación la ruta donde las facturas.

Esto lo consultamos en la base de datos:

INSERTAR IMAGEN

Con esta ruta debemos hacer un arreglo ya que al momento de agregarla en el apartado de red no reconoce por ese tipo de slash

```CDM
\\DESKTOP-A9IA835/Users/HOME/Documents
```

Como se debe escribir es con los otros slash, Forma correcta:

```CDM
\\DESKTOP-A9IA835\Users\HOME\Documents
```

Una vez teniendo esta ruta se debe pegar en la computadora externa.

**CONSIDERAR QUE SI NO la ruta no abre es por que no se encuentra en la misma red aqui se le debe comentar a la persona que esto lo hace miramar inteligente**

**si abre la ruta se puede enlazar**
```CMD
'\\\\SERVIDOR-CERRIT\\Facturacion'
```

INSERTAR IMAGEN

si nos abre es que esta bien la ruta

INSERTAR IMAGEN

Hay 2 caminos o nos salta que la ruta esta protegida con credenciales y se debera poner

**usuario:** HOME 

**contraseña:** 123456

si la ruta la abre se debe de fijar

ahora para fijar la ruta en la red se debe dar click derecho

INSERTAR IMAGEN

aqui se le da click en conectar nueva unidad de red

INSERTAR IMAGEN

se le da en conectarse a nueva red

INSERTAR IMAGEN

al guardar se nos creara la nueva red con la ruta fija

INSERTAR IMAGEN

para comprobar que no sale el mensaje, entramos al apartado de facturas

checamos en el acceso de **facturas/nueva factura**

INSERTAR IMAGEN

si ya no salta es que esta creada y enlaza en la red del servidor

adicional se podria abrir una factura

INSERTAR IMAGEN

INSERTAR IMAGEN

| Estacion | Ruta Factura |
| -------- | ------------ |
| Ejercito(Canseco) | \\SERVIDOR-CANSECO |

---
#### [Indice](../Indice.md)
