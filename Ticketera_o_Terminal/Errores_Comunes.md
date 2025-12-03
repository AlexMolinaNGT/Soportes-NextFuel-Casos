# Ticketera y Terminal

## Ticketera saca papel en blanco (sin texto)
Acomodar bien el rollo de papel

--- 

## Ticketera no imprime
Direccion **IP** no conecta al servidor

**Solucion:** Obtener el **IP** de servidor mediante el comando **ipconfig** ya que se ocupará más adelante.
este sera ejecutado en **CMD** dentro del equipo **Servidor**

```bash
ipconfig
```

Ejemplo de resultado:

```bash
Configuración IP de Windows

Adaptador de LAN inalámbrica Wi-Fi:

Sufijo DNS específico para la conexión. . :
Dirección IPv6 . . . . . . . . . . : 2806:310:21c:b2b3:336b:b0c0:b9f9:eed6
Dirección IPv6 temporal. . . . . . : 2806:310:21c:b2b3:1d31:7e36:8cc3:d668
Vínculo: dirección IPv6 local. . . : fe80::33ae:e1b4:d48e:58b5%5
Dirección IPv4. . . . . . . . . . . . . . : 192.168.2.47
Máscara de subred . . . . . . . . . . . . : 255.255.255.0
Puerta de enlace predeterminada . . . . . : 192.168.2.1
```
El que nos importa es este

```bash
Dirección IPv4. . . . . . . . . . . . . . : 192.168.2.47
```

En la ticketera, **mantener presionado** el icono de **Terminal NF** para desplegar el cuadro de diálogo que dice **“Información de app”**

INSERTAR IMAGEN

Nos llevará a la siguiente pantalla en donde hay que dar click en **Espacio de almacenamiento**
Después en **“Eliminar Datos”**  y **Aceptar**

INSERTAR IMAGEN

Regresar y dar click en **Terminal NF**
Click en Imprimir Ticket

INSERTAR IMAGEN

y agregar el ip del servidor

INSERTAR IMAGEN

---

## Conectar Terminal a la Red
Para agregar la terminal a la red es igual que en un celular.

INSERTAR IMAGEN

---

## No se tiene acceso a la terminal
Problema del usuario: **“No se tiene acceso a la terminal”**

Solucion: Instalar el programa **TerminalNF**

### Se comparte el código QR al cual deberán ir actualizando las terminales

## Actualización TerminalNF 5.0 :

 Mejoras en cuestión de tickets más rápidos.
 
 Mejoras futuras con integración con EnergyPay

 ## Pasos de instalación para actualizar la nueva versión:
 1. 🖧 Contar con la información de la red y IP a la cual está conectado el servidor entrando al **“simbolo de sistema”** de windows y ejecutando el comando ipconfig y tomar el ip de la red local (por lo regular empiezan en 192.168.)

 2. 🗑️ En la terminal:  Eliminar la versión anterior arrastrándola al icono de basura. 

INSERTAR IMAGEN

Y revisar estas rutas con la app File Management
- download

- downloadapps

- installapps

El archivo TerminalOficial.apk **NO SE BORRAR** 

Terminal{##version}.apk.apk   este si se borra 

En caso de que continue con la desconexión se debe **Eliminar Datos** (borrar cache) 
esto se realiza manteniendo presionado el icono AppInstall por 3 seguandos hasta que se despliega
“información de app” y dar **click**
ahi, despues  Click en “Espacio de Almacenamiento“ y por ultimo click en Eliminar Datos

3. 💻 Realizar la conexión a la terminal en caso de que no esté conectada a la red.

INSERTAR IMAGEN

4. 📱 Click en AppInstall

INSERTAR IMAGEN

5. 🔍 Después click en  Scan Install, y escanear  el codigo QR.

INSERTAR IMAGEN

6. ⏳ Esperar el mensaje de confirmación de instalación (30 seg)

  - posible que no se muestre, si tarda más de 1 minuto revisar el escritorio de la terminal porque es posible que ya se encuentre el icono pero la terminal no informó.

INSERTAR IMAGEN

7. ✔️ Una vez instalada la aplicación, verificar la Versión actual, en este caso la Versión 5.0

8. 🌐 Ingresar a la aplicación e ingresar la IP que obtuvimos en el paso 1.

INSERTAR IMAGEN

INSERTAR IMAGEN QR

## Codigo Cerritos y Tello:

INSERTAR QR 1

---
#### [Indice](../Indice.md)
