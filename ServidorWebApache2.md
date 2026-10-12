# Servidor Web Apache2

## ¿Qué es Apache2? 
Apache2 es un **servidor web**: un programa que está siempre escuchando en un **puerto** y cuando un navegador le pide una página mediante HTTP le devuelve el fichero correspondiente

## Proceso de instalación de Apache2
1. En la terminal escribiremos: **sudo apt install apache2 -y**
2. Comprobaremos que esté activo con: **systemctl status apache2**

### Lista de comandos para gestionar apache2:
1. sudo systemctl start apache2 : Inicia apache
2. sudo systemctl stop apache: Lo para
3. sudo systemctl restart apache2: Lo reinicia y aplica cambios de configuración
4. sudo systemctl reload apache2: Recarga la configuración sin cortar la conexión
5. sudo systemctl enable apache2: Lo inicia junto con el sistema

## Ficheros y directorios más importantes
