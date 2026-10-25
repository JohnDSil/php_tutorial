# 05. Tipos de Datos

PHP es un lenguaje de tipado dinámico débil: no es obligatorio definir el tipo de una variable al declararla.

## Clasificación según php.net

### 1. Tipos escalares (un solo valor)
- **bool (Booleano):** Expresa un valor de verdad. Puede ser `true` o `false` (insensible a mayúsculas).
- **int (Entero):** Números sin decimales. Admite bases decimal (`1234`), binaria (`0b1010`), octal (`0123`) y hexadecimal (`0x1A`).
- **float (Punto flotante):** Números reales (`1.234`, `1.2e3`).
- **string (Cadena):** Secuencia binaria de caracteres. Admite comillas dobles (interpreta variables y caracteres de escape como `\n`) y simples (literal estricto).

```php
<?php
$activo = true;
$puerto = 8080;
$temperatura = 24.6;
$nombre = "Servidor";

echo "El $nombre está activo\n"; // Expande la variable
echo 'El $nombre no se expande';  // Muestra textualmente "$nombre"
?>
```

### 2. Tipos compuestos
- **array:** Mapas ordenados de pares clave-valor.
- **object:** Instancias de clases definidas.
- **callable:** Métodos o funciones que pueden ser llamados dinámicamente.
- **iterable:** Cualquier estructura que puede recorrerse con `foreach`.

### 3. Tipos especiales
- **null:** Variable que no tiene ningún valor asignado (o ha sido borrada con `unset()`).
- **resource:** Puntero a un recurso abierto fuera del entorno de PHP (ficheros con `fopen()`, sockets, conexiones de red).

## Inspección de variables

```php
<?php
$memoria = 512;
var_dump($memoria); // Muestra tipo y valor exacto: int(512)
?>
```
