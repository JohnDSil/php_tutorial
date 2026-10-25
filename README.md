# PHP - Nivel 1: Fundamentos y Sintaxis del Lenguaje
> Documentación basada en el manual oficial de [php.net/manual/es/](https://www.php.net/manual/es/)

Guía técnica paso a paso orientada a administración de sistemas (ASIR) y fundamentos de programación web.

---

## 📑 Índice Oficial del Repositorio

| Bloque Oficial | Archivo en `/temario` | Conceptos Clave |
| :--- | :--- | :--- |
| **I. Conceptos Básicos** | [`01-introduccion.md`](temario/01-introduccion.md) | ¿Qué es PHP?, CGI vs Módulo, ciclo cliente-servidor |
| | [`02-instalacion-config.md`](temario/02-instalacion-config.md) | `apt install`, directivas de `php.ini`, FastCGI/FPM |
| **II. Referencia del Lenguaje** | [`03-sintaxis-basica.md`](temario/03-sintaxis-basica.md) | Etiquetas de PHP (`<?php ?>`), escape a HTML, separación de instrucciones (`;`) |
| | [`04-comentarios.md`](temario/04-comentarios.md) | Sintaxis de una línea (`//`, `#`) y multilínea (`/* */`) |
| | [`05-tipos-de-datos.md`](temario/05-tipos-de-datos.md) | Tipos escalares (bool, int, float, string), compuestos y especiales (null) |
| | [`06-casting-y-malabarismo.md`](temario/06-casting-y-malabarismo.md) | Conversión de tipos explícita (`(int)`) y coerción automática de PHP |
| | [`07-variables-y-ambito.md`](temario/07-variables-y-ambito.md) | `$identificador`, ámbito local, `global` y variables estáticas (`static`) |
| | [`08-constantes-y-magicas.md`](temario/08-constantes-y-magicas.md) | `define()`, `const` y constantes mágicas (`__DIR__`, `__FILE__`, `__LINE__`) |
| | [`09-expresiones-y-operadores.md`](temario/09-expresiones-y-operadores.md) | Aritméticos, asignación, comparación estricta (`===`), lógicos y operador nave espacial (`<=>`) |
| | [`10-estructuras-control-if.md`](temario/10-estructuras-control-if.md) | `if`, `else`, `elseif` y sintaxis alternativa para plantillas |
| | [`11-estructuras-control-switch-match.md`](temario/11-estructuras-control-switch-match.md) | `switch` tradicional vs expresión `match` estricta de PHP 8 |
| | [`12-estructuras-control-bucles.md`](temario/12-estructuras-control-bucles.md) | `while`, `do-while`, `for`, `break` y `continue` |
| | [`13-arrays-y-foreach.md`](temario/13-arrays-y-foreach.md) | Arrays indexados, asociativos y recorrido con `foreach ($k => $v)` |
| | [`14-funciones.md`](temario/14-funciones.md) | Parámetros tipados, argumentos por referencia (`&`), valores por defecto y retornos |
| **III. Variables Predefinidas** | [`15-superglobales.md`](temario/15-superglobales.md) | `$_SERVER`, `$_GET`, `$_POST`, `$GLOBALS` |
| **IV. Procesamiento de Texto** | [`16-expresiones-regulares-pcre.md`](temario/16-expresiones-regulares-pcre.md) | Sintaxis PCRE, `preg_match`, `preg_match_all`, `preg_replace` |

---

## 🛠️ Requisitos de Laboratorio
- **Servidor Web:** Apache 2.4 o Nginx
- **Motor PHP:** PHP 8.2 o superior
- **Comprobación:** `php -v`
