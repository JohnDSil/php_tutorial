# 08. Constantes y Constantes Mágicas

Una constante es un identificador para un valor simple que no puede variar durante la ejecución.

## Definición de Constantes

```php
<?php
// Método tradicional (en tiempo de ejecución)
define("MAX_INTENTOS", 3);

// Método mediante palabra reservada (en tiempo de compilación)
const PUERTO_SSH = 22;

echo MAX_INTENTOS;
echo PUERTO_SSH;
?>
```

*Nota: Las constantes no llevan el prefijo `$` y tienen ámbito global automático.*

## Constantes Mágicas

Cambian su valor en función del contexto exacto del código donde se leen:

| Constante | Descripción |
| :--- | :--- |
| `__LINE__` | Número de la línea actual en el script. |
| `__FILE__` | Ruta completa y nombre del archivo actual. |
| `__DIR__` | Directorio en el que reside el archivo actual. |
| `__FUNCTION__` | Nombre de la función en ejecución. |
| `__CLASS__` | Nombre de la clase actual. |
| `__METHOD__` | Nombre del método de clase en ejecución. |

```php
<?php
echo "Ejecutando script desde: " . __DIR__ . " en la línea " . __LINE__;
?>
```
