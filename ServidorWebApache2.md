# Servidor Web Apache2

## ¿Qué es Apache2? 
Apache2 es un **servidor web**: un programa que está siempre escuchando en un **puerto** y cuando un navegador le pide una página mediante HTTP le devuelve el fichero correspondiente

## Proceso de instalación de Apache2
1. En la terminal escribiremos: **sudo apt install apache2 -y**
2. Comprobaremos que esté activo con: **systemctl status apache2**

### Lista de comandos para gestionar apache2:
1. sudo systemctl start apache2 : Inicia apache
2. sudo systemctl stop apache : Lo para
3. sudo systemctl restart apache2 : Lo reinicia y aplica cambios de configuración
4. sudo systemctl reload apache2 : Recarga la configuración sin cortar la conexión
5. sudo systemctl enable apache2 : Lo inicia junto con el sistema

## Ficheros y directorios más importantes

1. /etc/apache2/apache2.conf : Configuración general del servidor
2. /etc/apache2/ports.conf : Puertos en los que escucha ( listen )
3. /etc/apache2/sites-available/ : Ficheros de configuración de los sitios **disponibles** (no confundir con activos)
4. /etc/apache2/sites-enabled/ : Sitios **activos** con enlaces de **sites-available/**
5. /var/www/html/  : Carpeta de la web por defecto
6. /var/log/apache2/ : Registros: **access.log** (accesos) y **error.log** (errores)

### Relación entre sites available y enabled
1. Los sitios se escriben en sites-available/
2. Al habilitar un sitio (usando **a2ensite**), apache crea un enlace simbólico en **sites-enabled/**
3. Al deshabilitarlo (usando **a2dissite**), el enlace se borra pero el fichero original sigue en **sites-available/**
------------------------------------------------------------------------------------------------------------------------------
## Virtualhost: qué es, cómo se configura, cómo se habilita y deshabilita

### ¿Qué es virtualhost?
Virtualhost es un bloque de configuración que le dice a apache: "cuando te llegue una petición con ciertas características, enseña esta carpeta" por eso un único servidor con la instalación de Apache puede alojar varias webs a la vez.
Apache decide que Virtualhost usar según los siguientes criterios:
1. Por puerto : Cada web escucha un puerto distinto (:80 , :9999)
2. Por IP : Cada web responde a una IP distinta de la máquina virtual
3. Por nombre: Cada web responde a un nombre distinto
### ¿Cómo se configura por puerto y IP?

# Configuración por puerto:
1. Crear carpetas y páginas:

-------------------------------------------------------------------------------------------------

sudo mkdir -p /var/www/smr/web /var/www/smr/intranet
echo "<h1>Bienvenidos a SMR</h1>" | sudo tee /var/www/smr/web/index.html
echo "<h1>Intranet de SMR</h1>" | sudo tee /var/www/smr/intranet/intranet.html**

-------------------------------------------------------------------------------------------------

2. Decirle a Apache los puertos que va a escuchar:

Iremos a: **sudo nano /etc/apache2/ports.conf** y debajo de **Listen 80** pondremos otro puerto, en este caso pondremos el puerto 9999 quedando así:

Listen 80
Listen 9999

3.  Creación del fichero Virtualhost:

**sudo nano /etc/apache2/sites-available/smr.conf** (el fichero se crea vacío)
Se coloca el siguiente contenido (extender en modo edición para verse mejor):
---------------------------------------------------------------

![Fichero Virtualhost](Fichero%20Virtualhost.png)

<VirtualHost *:80>

    DocumentRoot /var/www/smr/web
</VirtualHost>


<VirtualHost *:9999>

    DocumentRoot /var/www/smr/intranet
    DirectoryIndex intranet.html
</VirtualHost>

---------------------------------------------------------------

4. Habilitar sitio y reiniciar apache

**sudo a2ensite smr.conf** : habilita nuestro sitio web

**sudo a2dissite 000-default.conf** : deshabilita el sitio de ejemplo de Apache

**sudo apachectl configtest** : comprueba la sintaxis. Debe responder **Syntax OK**

**sudo systemctl restart apache2** : aplica los cambios

### Para DESHABILITAR un sitio:

sudo a2dissite smr.conf

sudo systemctl reload apache2
-----------------------------------------------------------------------------
### Comprobación por IP y puerto (en el navegador anfitrión):

# Variante: Virtualhost por IP
Aquí el criterio es la IP a la que llega la petición  y para probarlo hace falta que la VM tenga dos IP (se puede añadir una segunda a la interfaz host-only en netplan)
