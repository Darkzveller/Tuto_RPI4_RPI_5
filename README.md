# Tuto_RPI4_RPI_5

Commande de base : 

Redémarré la raspberry pi : sudo reboot 

-- Initiation RPI

Se connecter au RaspberryPi en SSH (Depuis un autre appareil)

https://www.youtube.com/watch?v=lZ3AMFr9oMQ

Raspberry Pi : ce qu'il faut connaître pour bien commencer

https://www.youtube.com/watch?v=g9u6KleX7iU

-- VNC VIEWER

Raspberry Pi sans clavier ni écran ? Voici comment accéder à Linux à distance avec VNC. Tutoriel

https://www.youtube.com/watch?v=bfK_oP8fcEE&t=431s

How to access Raspberry pi remotely with VNC direct connection and cloud connection

https://www.youtube.com/watch?v=pcn7WyxSHT0

Commande a tapé : 

Installer vnc viewer : sudo apt-get install realvnc-vnc-server realvnc-vnc-viewer

-- Installer vs code 

https://code.visualstudio.com/docs/setup/raspberry-pi


-- Installer git :


On vérifie les mise a jour : 

sudo apt update

Installe Git avec la commande suivante :

sudo apt install git

Vérifie l’installation : 

git --version

Configurer le profil :

git config --global user.name "Ton Nom"
git config --global user.email "ton.email@example.com"

Vérifier la configuration : 

git config --global --list


-- Installer Android TV :

📺 CREEZ votre propre ANDROID TV BOX grâce à un Raspberry Pi !

https://www.youtube.com/watch?v=_gk0qncIvX8 

Installer Android TV 11 Sur Raspberry Pi:

https://www.youtube.com/watch?v=kuWCA1xqcN4

konstakang rpi 4 : 

https://konstakang.com/devices/rpi4/

-- Observer température cpu via le terminal

Avoir la température a l'instant t : vcgencmd measure_temp

Avoir la température en temps réel toutes les secondes : watch -n 1 vcgencmd measure_temp
