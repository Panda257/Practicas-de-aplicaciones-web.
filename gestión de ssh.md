# Gestión del servidor por SSH

## ¿Qué es SSH?

SSH (Secure Shell) es un protocolo de red que permite conectarse y administrar servidores y/o computadoras de manera remota  (siempre y cuando el server principal esté encendido) mediante un canal cifrado y seguro.

## Configuración SSH 

¡Importante! para esto tienes que tener instalado OpenSSH en tu servidor y tener tu segundo adaptador de red del servidor en modo solo anfitrión (Se crea la red solo anfitrión desde virtualbox usando Ctrl+H y creando una red "solo-anfitrión") 

### ¡Detalle!
si no tienes OpenSSH instalado puedes usar el comando: **sudo apt install openssh-server -y** acompañado de **sudo systemctl enable --now ssh**

1. Comprobaremos lo que tenemos con: ip a
2. Localizaremos el fichero de configuración con: ls etc/netplan/
3. Editaremos el fichero con: **sudo nano /etc/netplan/50-cloud-init.yaml** o con **00-cloud-init.yaml** ( depende de cuál se tenga, lo sabremos usando el comando ls /etc/neptplan/)
5. Nos encontraremos con algo como esto:

![NetPlan](Net%20Plan.png) 

6. Lo tendremos que dejar algo así (por ejemplo):

![NetPlanCompleto](Net%20PlanCompleto.png) 

7. Aplicaremos los cambios usando **sudo netplan apply** (en caso de haber hecho algo mal, este comando nos lo dirá ya que los cambios no se aplicarán y nos enseñará la línea con el error)
8. verificamos con **ip a**
9. Desde el ordenador anfitrión abrimos la terminal y escribimos: **ssh tu_usuario@192.168.56.10**

### La primera vez que accedamos nos preguntará si confiamos en el host, escribimos **yes** y ya estaremos conectados al servidor de forma remota
