# mi-primer-script-ip
Script básico para mostrar la IP privada del equipo

En primer lugar crearemos un fichero con el comando "touch script.sh"

Siempre recordar que al crear un script tenemos que darnos permisos de ejecucion con el comando "chmod +x script.sh"

Seguido a eso instalaremos el editor de texto neovim mediante el comando "sudo apt install neovim"

Al terminar la instalación, usaremos el comando "nvim script.sh" para poder entrar al editor de texto de ese archivo y pulsaremos la letra "i" para poder editar

Y insertamos esta linea de comandos:

#!/bin/bash

echo -e "\nEsta es tu dirección IP privada ->$(ifconfig | grep "inet" | sed -n '4p' | awk '{print $2}')\n"

