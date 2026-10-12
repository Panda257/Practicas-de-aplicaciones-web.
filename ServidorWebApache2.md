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

##
