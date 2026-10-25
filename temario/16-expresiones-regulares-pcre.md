# 16. Expresiones Regulares (PCRE)

PHP implementa expresiones regulares compatibles con Perl mediante la biblioteca PCRE. Los patrones van delimitados entre barras: `/patron/modificadores`.

## Sintaxis común de patrones

- `^` : Inicio de cadena.
- `$` : Fin de cadena.
- `\d` : Dígito numérico (equivalente a `[0-9]`).
- `\w` : Carácter alfanumérico o guion bajo (`[a-zA-Z0-9_]`).
- `+` : Una o más repeticiones.
- `*` : Cero o más repeticiones.
- `{n,m}` : Entre $n$ y $m$ repeticiones.
- `i` : Modificador que ignora mayúsculas/minúsculas.

## Funciones Principales

### `preg_match()`
Valida si el patrón se cumple (devuelve 1 si coincide, 0 si no):

```php
<?php
// Validar formato simple de dirección IPv4 (cuatro grupos numéricos)
$ip = "192.168.1.100";
$patron = '/^(\d{1,3}\.){3}\d{1,3}$/';

if (preg_match($patron,$ip)) {
    echo "Formato de dirección IP válido";
} else {
    echo "Formato de dirección IP no válido";
}
?>
```

### `preg_replace()`
Busca un patrón y lo sustituye por una nueva cadena:

```php
<?php
$cadena = "El puerto de escucha es 8080 en el servidor";
$resultado = preg_replace('/\d+/', '443',$cadena);
echo $resultado; // Salida: El puerto de escucha es 443 en el servidor
?>
```
