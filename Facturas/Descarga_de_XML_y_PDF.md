# Descarga de XML y PDF 
El facturista no puede descargar del NextFuel Administrativo los XML y PDF de la factura por lo que solicita nuestro apoyo.

**Solución:**

    Generar el PDF y guardar el XML. Pero antes se debe revisar si 
    existe xml en el campo xml de la tabla facturas, para esto se realizan los 
    siguientes pasos

**Paso 1:**
- obtener el folio(UUID) a partir de la serie

```SQL
select folio, ticket.* from ticket where folio IN (select folio from facturas where serie IN ("BG-15671") );
```

**Paso 2:**
-revisar que exista el XML a partir de folio (se intentó en una sola consulta pero Error Code 2013 )

```SQL
Select xml, serie, folio, facturas.* from facturas where folio IN ('7ea598bb-79cb-49a8-81c1-4c9419d1e5f1');
```

## En caso que el campo XML sea NULL

**Se solicita a Pepe.**

En la siguiente imagen de muestra un ejemplo de cuando el campo xml  es null

INSERTAR IMAGEN

Una vez que Pepe nos pase los archivos se deben enviar al usuario que los solicitó y también se deben poner en la carpeta donde se guardan los XML  de la estación, en el caso de Autopista se guardan en esta carpeta:

INSERTAR IMAGEN

---

## En caso que el campo XML NO  sea NULL
Se debe ingresar el Administrativo no compilado y ejecutar esta función en la consola

```JS
fs.writeFile("aqui va el uuid"+".pdf", 'aqui pega el texto', {encoding: 'base64'}, function(e) {});
```

**'aqui pega el texto':** Hace referencia al campo **facturas.resp_facturacion**

---

## Ojo:
La información de este campo ya viene con comillas simples, por lo que no es necesario agregarle mas.

**Ejemplo:**

```JS
fs.writeFile("5e29efee-cacc-4f3b-8e18-71f0ba7af8b5.pdf", ‘ ’, {encoding: 'base64'}, function(e) {});
```

**Respuesta:**
Se espera que la respuesta sea **‘undefined’**, y el pdf se  guarda en la ruta de la carpeta donde se generó esta consulta.

**Consulta buscar factura por la serie:**

```SQL
select * from ticket where folio = (select folio from facturas where serie = "HM-9566");
```

---
#### [Indice](../Indice.md)
