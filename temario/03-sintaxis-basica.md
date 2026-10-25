# 03. Sintaxis Básica

## Etiquetas de apertura y cierre

El código PHP se delimita mediante las etiquetas canónicas:

```php
<?php
echo "Código PHP válido";
?>
```

> **Regla de estilo oficial (PSR-12 / php.net):** Si un fichero contiene únicamente código PHP, se **debe omitir** la etiqueta de cierre `?>`. Esto previene el envío accidental de saltos de línea o espacios en blanco antes del envío de cabeceras HTTP.

## Escape desde HTML

PHP permite alternar bloques de marcado y de ejecución:

```php
<p>Este texto es procesado directamente como HTML.</p>
<?php echo "<p>Este texto lo genera dinámicamente PHP.</p>"; ?>
<p>De vuelta al intérprete HTML.</p>
```

## Terminación de Instrucciones

Cada instrucción simple se cierra de forma obligatoria con un punto y coma (`;`). La etiqueta de cierre `?>` implica el final de la instrucción, pero omitir el `;` antes de una nueva línea provoca un error de análisis (`Parse error`).
