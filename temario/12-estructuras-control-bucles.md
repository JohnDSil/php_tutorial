# 12. Estructuras de Control: Bucles

## 1. Bucle `while`
Ejecuta el bloque mientras la condición resulte verdadera. La condición se valida al inicio:

```php
<?php
$intentos = 0;
while ($intentos < 3) {
    echo "Intento de ping número: $intentos\n";
    $intentos++;
}
?>
```

## 2. Bucle `do-while`
Garantiza la ejecución del bloque al menos una vez, ya que la condición se valida al final:

```php
<?php
$contador = 0;
do {
    echo "Se ejecuta siempre al menos una vez.\n";
} while ($contador > 0);
?>
```

## 3. Bucle `for`
Estructurado en tres expresiones: `for (inicialización; condición; incremento)`:

```php
<?php
for ($puerto = 80; $puerto <= 83; $puerto++) {
    echo "Escaneando puerto TCP: $puerto\n";
}
?>
```

## Control de Bucles: `break` y `continue`

- `break`: Aborta y finaliza el bucle actual de forma inmediata.
- `continue`: Omite el resto de la iteración actual y salta a la siguiente comprobación de condición.
