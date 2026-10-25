# 10. Estructuras de Control: Condicionales (if, else, elseif)

Permiten ejecutar fragmentos de código en función de una expresión lógica.

```php
<?php
$carga_cpu = 85.5;

if ($carga_cpu >= 90.0) { echo "ESTADO CRÍTICO: Carga de CPU superior al 90\%"; } elseif ($carga_cpu >= 75.0) {
    echo "ALERTA: Carga de CPU elevada";
} else {
    echo "ESTADO NOMINAL: Carga dentro de límites aceptables";
}
?>
```

## Sintaxis Alternativa para Plantillas HTML

En entornos mixtos PHP/HTML, se recomienda evitar las llaves para mejorar la legibilidad:

```php
<?php if ($carga_cpu > 80): ?>
    <div class="alerta-roja">Peligro en el servidor</div>
<?php else: ?>
    <div class="alerta-verde">Servidor estable</div>
<?php endif; ?>
```
