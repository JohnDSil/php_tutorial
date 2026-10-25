# 14. Funciones Definidas por el Usuario

Una función es un bloque de instrucciones reutilizable.

## Definición estándar con Tipado Fuerte

PHP permite definir el tipo de los argumentos y del valor devuelto:

```php
<?php
function calcularPorcentajeUso(int $usado, int$total): float {
    if ($total <= 0) {
        return 0.0;
    }
    return ($usado / $total) * 100;
}

echo calcularPorcentajeUso(40, 200) . "%"; // Salida: 20%
?>
```

## Argumentos por Defecto

```php
<?php
function configurarInterfaz(string $nombre, int$mtu = 1500): string {
    return "Interfaz $nombre asignada con MTU$mtu";
}

echo configurarInterfaz("eth0");      // MTU toma 1500 por defecto
echo configurarInterfaz("eth1", 9000); // Sobrescribe a 9000
?>
```

## Paso por Referencia (`&`)

Por defecto, las variables se pasan por valor (copia). El operador `&` permite modificar la variable original:

```php
<?php
function reiniciarContador(int &$valor) {$valor = 0;
}

$intentos = 15;
reiniciarContador($intentos);
echo $intentos; // Muestra 0
?>
```
