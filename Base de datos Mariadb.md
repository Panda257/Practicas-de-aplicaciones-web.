# Base de datos Mariadb
## Índice
1. ¿Por qué un SGBD como MariaDB? ¿Qué es?
2. Instalación de MariaDB

## 1. ¿Por qué un SGBD como MariaDB? ¿Qué es?

### ¿Qué es una base de datos?

Una base de datos en un conjunto de información guardada de forma ordenada para poder buscarla y usarla rápidamente, se organizan en tablas que tienen lo siguiente:

- columnas: el tipo de dato que se guarda (por ejemplo "título", "autor")
- Filas: cada elemento guardado (por ejemplo, cada entrada del blog)

| id | título | autor | fecha |
|---|---------|-------|-------|
| 1 | Hola mundo | admin | 2026-10-26 |
| 2 | Horario de matrícula | admin | 2026-10-27 |

### ¿Qué es un SGBD?

Un **SGBD** (Sistema Gestor de Bases de Datos) es el **programa que se encarga de manejar la base de datos**, los programas como WordPress no leen ni escriben los datos directamente en el disco sino que se lo piden al SGBD y este se encarga de:

- **Guardar** los datos de forma ordenada y segura.
- **Buscarlos rápido** cuando alguien los pide usando el lenguaje **SQL**.
- **Controlar quién accede** con usuarios, contraseñas y permisos.
- **Evitar errores** cuando muchas personas usan los datos a la vez (por ejemplo dos visitantes comentando al mismo tiempo).
- **Mantener la información coherente** aunque falle algo a mitad de una operación.

### ¿Por qué usar un SGBD y no guardar los datos en ficheros?

| Guardar datos en ficheros sueltos | Usar un SGBD |
|-----------------------------------|---|
| Buscar algo obliga a leer todo el fichero | Busca muy rápido aunque haya miles de datos |
| Si dos usuarios escriben a la vez, se pueden corromper los datos | Gestiona el acceso simultáneo sin errores |
| Seguridad limitada a los permisos del fichero | Usuarios y permisos propios para cada base de datos |
| Cada programa organiza los datos a su manera | Lenguaje estándar (SQL) que entienden muchos programas |

Por eso cualquier web dinámica (tiendas online, foros, wordpress...) necesita un SGBD.

### ¿Qué es MariaDB?

**MariaDB** es un **SGBD relacional, libre y gratuito**, naciendo en 2009 como una copia mejorada de **MySQL** creada por el propio creador de MySQL cuando esta pasó a manos de Oracle. Por eso es **compatible con MySQL**: usa los mismos comandos y los programas que funcionan con MySQL funcionan también con MariaDB

Se usa porque:
 
- Es **software libre** y gratuito.
- Viene en los **repositorios oficiales de Ubuntu** así que se instala con un solo comando.
- Es totalmente **compatible con WordPress**.
- Es rápido, estable y muy utilizado en servidores reales.

### ¿Para qué la necesita WordPress?
 
WordPress guarda en la base de datos todo lo que no son ficheros: **entradas, páginas, comentarios, usuarios y la configuración del sitio**. Cada vez que alguien visita la web, WordPress le pide a MariaDB los datos para montar la página

### Cómo encaja todo (LAMP)
 
```
Navegador  -->  Apache  -->  PHP  -->  MariaDB
(visitante)    (sirve la web) (ejecuta WordPress) (guarda los datos)
```

| Letra | Pieza | Estado antes de esta práctica |
|-------|-------|-------------------------------|
| **L** | Linux (Ubuntu 24.04) | Instalado (práctica anterior) |
| **A** | Apache | Instalado (práctica anterior) |
| **M** | MariaDB | Instalado (en esta práctica) |
| **P** | PHP | Instalado (en esta práctica) |

## 2. Instalación de MariaDB (práctica MariaDB)
### Apartado 1. Preparación del sistema

```
sudo apt update
systemctl is-active apache2
```
En la consola se mostrará:
```
active
```

### Apartado 2. Instalación de MariaDB

```
sudo apt install mariadb-server -y
mariadb --version
```
En la consola se verá algo así:
```
mariadb  Ver 15.1 Distrib 10.11.14-MariaDB, for debian-linux-gnu (x86_64)
```

Explicación: `apt install mariadb-server` instala el servidor de bases de datos. La opción `-y` responde "sí" automáticamente a la confirmación. Con `mariadb --version` compruebo que se ha instalado la versión **10.11**, que es una versión LTS (soporte largo) compatible con WordPress.

### Apartado 3. Comprobación del funcionamiento
#### 3.1. Estado del servicio
```
sudo systemctl status mariadb
systemctl is-enabled mariadb
```
En la consola se verá algo como esto:

```
● mariadb.service - MariaDB 10.11.14 database server
     Loaded: loaded (/usr/lib/systemd/system/mariadb.service; enabled; preset: enabled)
     Active: active (running)
```
 
Explicación: `systemctl status` muestra el estado detallado del servicio. Aparece `active (running)`, es decir, está funcionando ahora mismo. `is-enabled` responde `enabled`, así que arrancará solo cada vez que se encienda el equipo, Ubuntu lo configura así automáticamente al instalar. 
