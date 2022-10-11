# Embedded-PaymentFormT1-Java

Ejemplo de formulario en JAVA.

## Requisitos Previos

- Servidor Web
- Java 7 o superior
- Claves de Integración, Ver ejemplo.

## 1) Descargar proyecto

Descargar el proyecto .zip haciendo click Aquí o clonarlo desde Git.

git clone https://github.com/izipay-pe/Embedded-PaymentFormT1-Java.git

## 2) Subir a un servidor web

Crearse una cuenta gratuita en 000webhost y subir el proyecto a la carpeta raiz del hosting public_html/ (Ya sea por el administrador de archivos o filezilla)

Crearse un nuevo sitio.
Seleccionar Administrar sitio web.
Selccionar File Manager y luego Upload Files

## 3) Configurar claves

Editar el archivo keys.example.php

// Identificador de su tienda
IzipayController::setDefaultUsername("12345678");

// Clave de Test o Producción
IzipayController::setDefaultPassword("testpassword_111111111111111111111111111111111111");

// Clave Pública de Test o Producción
IzipayController::setDefaultPublicKey("2222222222222222222222222222222222222222222222222");

// Clave HMAC-SHA-256 de Test o Producción
IzipayController::setDefaultHmacSha256("33333333333333333333333333333333333333333333333");

// URL del servidor de Izipay
IzipayController::setDefaultEndpointApiRest("https://api.micuentaweb.pe");

## 4) Implementar IPN

Ver el ejemplo Aquí
