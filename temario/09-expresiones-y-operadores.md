# 09. Expresiones y Operadores

## Operadores Aritméticos
`+` (suma), `-` (resta), `*` (multiplicación), `/` (división), `%` (módulo), `**` (potencia).

## Operadores de Comparación

- `==` : Igualdad de valor con conversión de tipos (`5 == "5"` es true).
- `===` : **Identidad estricta**: exige igualdad de valor y de tipo de dato (`5 === "5"` es false).
- `!=` o `<>` : Distinto valor.
- `!==` : No idéntico (distinto valor o distinto tipo).
- `<`, `>`, `<=`, `>=`.
- `<=>` : **Operador Nave Espacial (Spaceship):**
  - Devuelve `0` si ambos operandos son iguales.
  - Devuelve `-1` si el izquierdo es menor.
  - Devuelve `1` si el izquierdo es mayor.

```php
<?php
echo 1 <=> 2; // -1
echo 2 <=> 2; //  0
echo 3 <=> 2; //  1
?>
```

## Operador de Fusión de Null (`??`)

Devuelve el primer operando si existe y no es `null`; en caso contrario, devuelve el segundo:

```php
<?php
$usuario = $_GET['user'] ?? 'invitado';
?>
```

## Operadores Lógicos
`&&` (AND estricto), `||` (OR estricto), `!` (NOT). Existen también `and` y `or`, pero tienen una precedencia más baja que el operador de asignación `=`.
