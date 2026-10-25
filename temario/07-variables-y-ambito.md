# 07. Variables y Ámbito (Scope)

Las variables se identifican mediante el símbolo dólar (`$`) seguido de una letra o un guion bajo, continuando con cualquier número de letras, números o guiones bajos.

## Sensibilidad a mayúsculas

Los nombres de variables son sensibles a mayúsculas y minúsculas:
```php
<?php
$servidor = "web01";
$Servidor = "db01"; // Variable totalmente distinta a la anterior
?>
```

## Ámbitos de resolución

### 1. Ámbito Local y Global

Una variable definida en el script principal no está disponible dentro de una función por defecto:

```php
<?php
$ip = "192.168.1.10"; // Ámbito global

function mostrarIp() {
    // Generaría un aviso de variable indefinida a menos que se use 'global'
    global $ip;
    echo $ip;
}

mostrarIp();
?>
```

### 2. Variables Estáticas (`static`)

Conservan su valor entre sucesivas ejecuciones de una función:

```php
<?php
function contadorConexiones() {
    static $contador = 0;
    $contador++;
    echo $contador . "\n";
}

contadorConexiones(); // Imprime: 1
contadorConexiones(); // Imprime: 2
contadorConexiones(); // Imprime: 3
?>
```
