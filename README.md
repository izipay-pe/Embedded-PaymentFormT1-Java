# Embedded-PaymentFormT1-Java

Ejemplo de formulario en JAVA.

## Requisitos Previos

* Extraer claves de autentificación. [Guía Aquí](https://github.com/izipay-pe/obtener-credenciales-de-conexion)
* Servidor Web
* Java 7 o superior

## 1) Descargar proyecto

Descargar el proyecto .zip haciendo click [Aquí](https://github.com/izipay-pe/Embedded-PaymentFormT1-Java/archive/refs/heads/main.zip) o clonarlo desde Git.
```sh
git clone https://github.com/izipay-pe/Embedded-PaymentFormT1-Java.git
``` 
## 2) Subir a un servidor web

Crearse una cuenta gratuita en 000webhost y subir el proyecto a la carpeta raiz del hosting public_html/ (Ya sea por el administrador de archivos o filezilla)

Crearse un nuevo sitio.
Seleccionar Administrar sitio web.
Selccionar File Manager y luego Upload Files

## 3) Configurar claves

La información la puede obtener desde su Back Office Vendedor (Configuración --> Tienda --> Claves)

Editar el archivo `config.properties`

```sh
// Identificador de su tienda
site_id=12345678

// Clave de Test
key_test=XXXXXXXXXXXXXXXXXXX

// Clave de Producción
key_prod=XXXXXXXXXXXXXXXXXXX

// Método

return_mode=POST

// URL del servidor de Izipay
gateway_url=https://api.micuentaweb.pe
``` 

## 4) Transacción de prueba

El formulario de pago está listo, puede intentar realizar una transacción utilizando una tarjeta de prueba con la barra de herramientas de depuración (en la parte inferior de la página).

Si intenta pagar, tendrá el siguiente error: **CLIENT_998: Demo form, see the documentation**.
Es porque el **formToken** que ha definido usando **KR.setFormConfig** está configurado en **DEMO-TOKEN-TO-BE-REPLACED**.

you have to create a **formToken** before displaying the payment form using Charge/CreatePayment web-service.
For more information, please take a look to:

- [Formulario incrustado: prueba rápida](https://secure.micuentaweb.pe/doc/es-PE/rest/V4.0/javascript/quick_start_js.html)
- [Primeros pasos: pago simple](https://secure.micuentaweb.pe/doc/es-PE/rest/V4.0/javascript/guide/start.html)
- [Servicios web - referencia de la API REST](https://secure.micuentaweb.pe/doc/es-PE/rest/V4.0/api/reference.html)

## 5) Implementar IPN

* Ver manual de implementacion de la IPN [Aquí](https://secure.micuentaweb.pe/doc/es-PE/rest/V4.0/kb/payment_done.html)

* Ver el ejemplo de la respuesta IPN con PHP [Aquí](https://github.com/izipay-pe/Redirect-PaymentForm-IpnT1-PHP)

* Ver el ejemplo de la respuesta IPN con NODE.JS [Aquí](https://github.com/izipay-pe/Response-PaymentFormT1-Ipn)

## 6) Ejemplo de formulario

Ver el ejemplo [Aquí](https://prueba55.herokuapp.com/)
