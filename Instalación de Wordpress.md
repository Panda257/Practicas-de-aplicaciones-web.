# Instalación de WordPress
## Índice
1.  [¿Qué es WordPress?](#1.qué-es-wordpress)
2. [Instalación paso a paso de WordPress y prueba de uso (práctica WordPress)](#2-instalación-paso-a-paso-de-wordpress-y-prueba-de-uso-práctica-wordpress)

## 1. ¿Qué es WordPress?
### Un gestor de contenidos (CMS)

**WordPress** es un **CMS** (*Content Management System*, gestor de contenidos) una aplicación web hecha en **PHP** que permite crear y mantener una web desde un panel de administración, sin tener que programar cada página a mano.
Desde ese panel se pueden escribir entradas y páginas, subir imágenes, gestionar usuarios, cambiar el diseño con **temas** y añadir funciones con plugins
Es software **libre y gratuito**, y es el CMS más utilizado del mundo: lo usan desde blogs personales hasta webs de empresas, tiendas online y periódicos.

### ¿Dónde guarda WordPress cada cosa?
Esto es lo más importante: WordPress reparte la información entre **ficheros** y la **base de datos**.

| Qué | Dónde se guarda | Ejemplo |
|-----|-----------------|---------|
| El programa WordPress, los temas, los plugins y las imágenes subidas | **Ficheros**, en una carpeta de Apache | `/var/www/wordpress/wp-content` |
| Entradas, páginas, usuarios, comentarios y ajustes del sitio | **Base de datos** (MariaDB) | tabla `wp_posts` |
| Los datos para conectar con la base de datos | **Fichero de configuración** | `wp-config.php` |

### Cómo encaja en el LAMP
WordPress es la pieza final del servidor que he montado en las prácticas anteriores:

```
Navegador  -->  Apache  -->  PHP (WordPress)  -->  MariaDB
(visitante)    (sirve la web)  (genera la página)    (guarda los datos)
```

1. El **visitante** pide una página desde el navegador.
2. **Apache** recibe la petición y como es un fichero `.php`, se la pasa a **PHP**.
3. **WordPress** (escrito en PHP) pide a **MariaDB** los datos que necesita: el texto de la entrada, el título del sitio, los comentarios...
4. Con esos datos, WordPress genera la página HTML y Apache se la devuelve al navegador.

## 2. Instalación paso a paso de WordPress y prueba de uso (práctica WordPress)
### Apartado 1. Comprobar el punto de partida
Escribo lo siguiente en la consola:
```bash
systemctl is-active apache2 mariadb
php -v
ls /etc/apache2/sites-enabled/
grep Listen /etc/apache2/ports.conf
```
Me devolverá esto:
```
active
active
PHP 8.5.4 (cli) (built: Oct 19 2026 14:35:18) (NTS)
...
000-default.conf  sitio-9999.conf
Listen 80
```

![Punto de partida](punto%20partida.png)

### Apartado 2. Crear la base de datos y su usuario
Entramos a Mariadb:
```
sudo mariadb
```

Dentro de Mariadb:
```
CREATE DATABASE wordpress CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
CREATE USER 'wp_user'@'localhost' IDENTIFIED BY '********';
GRANT ALL PRIVILEGES ON wordpress.* TO 'wp_user'@'localhost';
FLUSH PRIVILEGES;
EXIT;
```

| Orden | Qué hace |
|-------|----------|
| `CREATE DATABASE` | Crea la base de datos `wordpress`. `utf8mb4` permite guardar tildes, ñ y emojis. |
| `CREATE USER` | Crea el usuario `wp_user`, que solo puede conectarse desde la propia máquina (`localhost`), con su contraseña. |
| `GRANT ALL PRIVILEGES ON wordpress.*` | Le da todos los permisos, pero **solo** sobre la base `wordpress`. |
| `FLUSH PRIVILEGES` | Aplica los cambios de permisos. |

Compruebo que el usuario funciona entrando con él:
```
mariadb -u wp_user -p wordpress
```

```
SHOW TABLES;
EXIT;
```

Se verá en consola:

```
Enter password:
...
MariaDB [wordpress]> SHOW TABLES;
Empty set (0.001 sec)
```

![Base de datos y usuario](bd%20usuario.png)

**Explicación:** WordPress necesita una base de datos propia y un usuario que solo tenga permisos sobre ella. Al entrar con `wp_user` la conexión funciona y `SHOW TABLES` responde `Empty set`: la base existe y el usuario puede usarla pero todavía está vacía porque las tablas las creará el asistente de WordPress (la contraseña no se ve al escribirla).


### Apartado 3. Descargar WordPress y colocarlo en su carpeta

```
cd /tmp
wget https://wordpress.org/latest.tar.gz
tar -xzf latest.tar.gz
ls wordpress
```

```
sudo mkdir -p /var/www/wordpress
sudo cp -a /tmp/wordpress/. /var/www/wordpress/
ls /var/www/wordpress
```

Se verá lo siguiente en la consola:

```
index.php        wp-activate.php     wp-comments-post.php  wp-content   wp-links-opml.php  wp-mail.php      wp-trackback.php
license.txt      wp-admin            wp-config-sample.php  wp-cron.php  wp-load.php        wp-settings.php  xmlrpc.php
readme.html      wp-blog-header.php  wp-includes           wp-login.php wp-signup.php
```
![Ficheros de WordPress](wordpress%20ficheros.png)

**Explicación:** trabajo en `/tmp`, una carpeta temporal. `wget` descarga la última versión de WordPress desde la web oficial y `tar -xzf` la descomprime (`x` extraer, `z` formato gzip, `f` fichero), después creo la carpeta definitiva con `mkdir -p` y copio el contenido con `cp -a` que conserva fechas y permisos. El `.` final de `/tmp/wordpress/.` hace que se copie el **contenido** de la carpeta incluidos los ficheros ocultos y no la carpeta en sí.

| Carpeta | Para qué sirve |
|---------|----------------|
| `wp-admin` | El panel de administración. |
| `wp-includes` | El núcleo de WordPress. No se toca. |
| `wp-content` | Temas, plugins e imágenes subidas. Es lo único que se personaliza. |

### Apartado 4. Propietario y permisos

```
sudo chown -R www-data:www-data /var/www/wordpress
sudo find /var/www/wordpress -type d -exec chmod 755 {} \;
sudo find /var/www/wordpress -type f -exec chmod 644 {} \;
ls -l /var/www/wordpress
```

Se verá algo así en la consola:

```
-rw-r--r--  1 www-data www-data   405 ... index.php
-rw-r--r--  1 www-data www-data 19903 ... license.txt
drwxr-xr-x  9 www-data www-data  4096 ... wp-admin
drwxr-xr-x  4 www-data www-data  4096 ... wp-content
drwxr-xr-x 30 www-data www-data 12288 ... wp-includes
...
```

![Permisos](permisos%20wordpress.png)
