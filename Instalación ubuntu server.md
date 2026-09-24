# Instalación ubuntu server

## Creación máquina virtual
1. Abrir VirtualBox.
2. Hacer clic en "nuevo".
3. Ponerle nombre a tu máquina virtual y colocar la ISO (antes de continua, quita la instalación desatendida).
4. Luego hay que dejar la máquina virtual con 4Gb de RAM (4096 MB), 2-3 núcleos y 50-75Gb de almacenamiento.

## Configuración de los adaptadores de red
Con la máquina virtual apagada, entraremos a configuración y luego a red para configurar los adaptadores
**Es posible que aparezca este error, en caso de que lo tengas hay que desinstalar el VBox y hay que volverlo a instalar o solamente actualizarlo.**

![VirtualBox Error](Error%20VirtualBox.png) 

## Instalación con máquina encendida
5. Luego de iniciar la máquina elegimos el idioma del sistema y del teclado.
6. Elegimos el tipo de instalación "Ubuntu server" (El que pone "minimized" NO).
7. La proxy la dejamos en blanco.
8. En la parte de almacenamiento elegiremos usar el disco duro completo.
9. En el apartado de "perfil de usuario" introduciremos el nombre del servidor, el nombre del host (tú nombre) y una contraseña (importante que no te olvides lo que has puesto).
10. Para ir finalizando la instalación marcaremos la casilla "SSH Setup" (si nos olvidamos de marcar la casilla,luego también podremos instalarlo pero de manera manual con comandos).
11. Esperaremos mientras el sistema se instala y cuando acabe le daremos a "Reboot Now" (si nos pidiese retirar el medio de instalación, pulsa Enter).
