# Embedded-PaymentFormT1-Java

Ejemplo de formulario en JAVA.

## Requisitos Previos

- Servidor Web
- Java 7 o superior
- Claves de Integración, [Ver ejemplo.](https://github.com/JunioratWork/Obtener_Credenciales#readme)

## 1) Descargar proyecto

Descargar el proyecto .zip haciendo click [Aquí](https://github.com/izipay-pe/Embedded-PaymentFormT1-Java) o clonarlo desde Git.
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

## 4) Implementar IPN

Ver el ejemplo [Aquí](https://github.com/izipay-pe/Redirect-PaymentForm-IpnT1-PHP)

## 5) Ejemplo de formulario

Ver el ejemplo [Aquí](https://prueba55.herokuapp.com/)
