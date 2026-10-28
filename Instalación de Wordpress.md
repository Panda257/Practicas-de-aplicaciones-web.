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

![Punto de partida](punto%20partida.png)

