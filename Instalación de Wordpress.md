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
