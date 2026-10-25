# 01. Introducción a PHP

PHP (acrónimo recursivo de *PHP: Hypertext Preprocessor*) es un lenguaje de código abierto de propósito general especialmente adecuado para el desarrollo web y que puede ser incrustado en HTML.

## ¿Cómo funciona el ciclo Cliente-Servidor?

A diferencia de lenguajes del lado del cliente como JavaScript:
1. El usuario solicita una URL en su navegador (cliente).
2. El servidor web (Apache, Nginx) detecta la extensión `.php` y entrega el fichero al intérprete de PHP.
3. PHP ejecuta el script, realiza las consultas necesarias y genera código HTML plano.
4. El servidor web envía únicamente el HTML resultante al cliente. El código fuente PHP nunca es visible para el usuario final.

```
+------------+       Petición HTTP (index.php)       +---------------------+
|            | ------------------------------------> | Servidor Web        |
| Navegador  |                                       | (Apache / Nginx)    |
| (Cliente)  |                                       +----------+----------+
|            |                                                  | Invoca
|            |       Respuesta HTTP (HTML plano)                v
|            | <------------------------------------ +---------------------+
+------------+                                       | Intérprete PHP      |
                                                     +---------------------+
```

## Modos de Ejecución en Servidores

- **Módulo de Apache (`mod_php`):** PHP se ejecuta dentro del propio proceso del servidor Apache.
- **PHP-FPM (FastCGI Process Manager):** Demonio independiente recomendado en entornos de alto rendimiento con Nginx o Apache mediante sockets UNIX.
- **CLI (Command Line Interface):** Permite ejecutar scripts directamente desde la terminal del sistema (`php script.php`), ideal para automatización de tareas en Linux.
