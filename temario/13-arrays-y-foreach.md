# 13. Arrays y el Constructor foreach

En PHP, un `array` es un mapa ordenado que asocia valores con claves.

## Tipos de Arrays

### 1. Indexados (claves numéricas automáticas):
```php
<?php
$dns = ["8.8.8.8", "1.1.1.1", "9.9.9.9"];
echo $dns[1]; // Salida: 1.1.1.1
?>
```

### 2. Asociativos (claves de texto explícitas):
```php
<?php
$servidor = [
    "hostname" => "srv-backup",
    "ip"       => "192.168.10.5",
    "rol"      => "Almacenamiento"
];

echo $servidor["ip"]; // Salida: 192.168.10.5
?>
```

## Recorrido con `foreach`

Es la estructura estándar para procesar arrays:

```php
<?php
// Recorrido de clave y valor en array asociativo:
foreach ($servidor as $propiedad => $valor) {
    echo "$propiedad: $valor\n";
}
?>
```

## Funciones esenciales para Arrays

- `count($arr)` : Devuelve el número de elementos.
- `in_array($aguja,$pajar)` : Comprueba si un valor existe dentro del array.
- `array_key_exists($clave,$arr)` : Verifica si una clave existe en el array.
- `array_push($arr,$valor)` : Agrega elementos al final.
