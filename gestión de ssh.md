# Gestión del servidor por SSH

## ¿Qué es SSH?

SSH (Secure Shell) es un protocolo de red que permite conectarse y administrar servidores y/o computadoras de manera remota  (siempre y cuando el server principal esté encendido) mediante un canal cifrado y seguro.

## Configuración SSH 

¡Importante! para esto tienes que tener instalado OpenSSH en tu servidor y tener tu segundo adaptador de red del servidor en modo solo anfitrión (Se crea la red solo anfitrión desde virtualbox usando Ctrl+H y creando una red "solo-anfitrión") 

1. Comprobaremos lo que tenemos con: ip a
2. Localizaremos el fichero de configuración con: ls etc/netplan/
3. Editaremos el fichero con: sudo nano /etc/netplan/50-cloud-init.yaml o con 00-cloud-init.yaml ( depende de cuál se tenga, lo sabremos usando el comando ls /etc/neptplan/ )


### ¡Detalle!
si no tienes OpenSSH instalado puedes usar el comando: **sudo apt install openssh-server -y** acompañado de **sudo systemctl enable --now ssh**
