# 15. Variables Superglobales

Son arrays asociativos internos siempre disponibles en todos los ámbitos del script sin necesidad de invocar `global`.

## 1. `$_SERVER`
Contiene información relativa al entorno del servidor web, rutas y cabeceras de peticiones:

- `$_SERVER['REMOTE_ADDR']`: Dirección IP del cliente que realiza la petición.
- `$_SERVER['REQUEST_METHOD']`: Método HTTP utilizado (`GET`, `POST`, `HEAD`, `PUT`).
- `$_SERVER['SERVER_NAME']`: Nombre del host del servidor.
- `$_SERVER['SCRIPT_FILENAME']`: Ruta absoluta del script en ejecución.

## 2. `$_GET`
Recupera variables transmitidas en la URL a través de la cadena de consulta (*query string*):

```php
<?php
// Si la petición es: ver_log.php?servicio=apache&lineas=50
$servicio = $_GET['servicio'] ?? 'desconocido';
$lineas   = (int)($_GET['lineas'] ?? 10);
?>
```

## 3. `$_POST`
Recupera variables enviadas en el cuerpo de una petición HTTP POST (habitual en formularios HTML):

```php
<?php
$usuario = $_POST['txt_usuario'] ?? '';
$clave   = $_POST['txt_password'] ?? '';
?>
```

## 4. `$GLOBALS`
Array que almacena referencias a todas las variables que se encuentran en el ámbito global del script.
