# 02. Instalación y Configuración

## Instalación en Debian / Ubuntu Server

Para desplegar un entorno clásico LAMP:

```bash
# Actualizar lista de paquetes
sudo apt update

# Instalar Apache y PHP con soporte para MySQL
sudo apt install apache2 php libapache2-mod-php php-mysql -y

# Verificar versión del intérprete CLI
php -v
```

## Archivos de Configuración (`php.ini`)

El comportamiento del motor PHP se controla mediante el fichero `php.ini`. En distribuciones Debian/Ubuntu suele localizarse en:
- Apache: `/etc/php/8.x/apache2/php.ini`
- CLI: `/etc/php/8.x/cli/php.ini`
- FPM: `/etc/php/8.x/fpm/php.ini`

### Directivas críticas para administración de sistemas:

- `memory_limit = 128M` : Memoria máxima que puede consumir un script.
- `max_execution_time = 30` : Tiempo límite de ejecución en segundos antes de forzar la terminación.
- `display_errors = Off` : En producción debe estar en `Off` para no exponer datos del sistema a atacantes. En entornos de desarrollo/prácticas se cambia a `On`.
- `upload_max_filesize = 2M` : Tamaño máximo de archivos subidos.

Tras modificar `php.ini`, es imperativo reiniciar el servicio web:
```bash
sudo systemctl restart apache2
```
