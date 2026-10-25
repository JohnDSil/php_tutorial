# 06. Malabarismo de Tipos (Type Juggling) y Casting

## Coerción Automática (*Type Juggling*)

PHP convierte automáticamente el tipo de una variable según el contexto donde se emplee:

```php
<?php
$foo = "0";      // $foo es string ("0")
$foo += 2;        // $foo ahora es integer (2)
$foo = $foo + 1.3; // $foo ahora es float (3.3)
?>
```

## Conversión Forzada (*Type Casting*)

Para obligar a una variable a comportarse como un tipo explícito, se coloca el nombre del tipo entre paréntesis delante de la expresión:

```php
<?php
$cadena = "45 usuarios";
$entero = (int)$cadena; // Transforma a: 45

$decimal = 9.99;
$enteroTruncado = (int)$decimal; // Transforma a: 9 (descarta decimales)

$booleano = (bool)0; // Transforma a: false (0, "", "0", null y [] evalúan como false)
?>
```

### Moldes permitidos:
- `(int)`, `(integer)`
- `(bool)`, `(boolean)`
- `(float)`, `(double)`, `(real)`
- `(string)`
- `(array)`
- `(object)`
- `(unset)` *(obsoleto/eliminado en versiones recientes)*
