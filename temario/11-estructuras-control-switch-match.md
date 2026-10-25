# 11. Estructuras de Control: switch y match

## La sentencia `switch`

Compara una variable con múltiples casos mediante igualdad débil (`==`):

```php
<?php
$estadoHttp = 404;

switch ($estadoHttp) {
    case 200:
        echo "OK";
        break;
    case 301:
        echo "Moved Permanently";
        break;
    case 404:
        echo "Not Found";
        break;
    default:
        echo "Código de estado no contemplado";
        break;
}
?>
```

## La expresión `match` (PHP 8.0+)

`match` es la evolución moderna de `switch`:
1. Utiliza **comparación estricta (`===`)**.
2. **Retorna un valor**, por lo que puede asignarse a una variable.
3. No requiere `break` (no cae en cascada).
4. Si no coincide ninguna opción y falta `default`, lanza una excepción `UnhandledMatchError`.

```php
<?php
$estadoHttp = 404;

$mensaje = match ($estadoHttp) {
    200 => "OK",
    301, 302 => "Redirección detectada",
    404 => "Not Found",
    default => "Código desconocido",
};

echo $mensaje;
?>
```
