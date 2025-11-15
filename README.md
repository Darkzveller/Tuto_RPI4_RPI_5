# Tuto_RPI4_RPI_5

Site officiel de la raspberry : *https://www.raspberrypi.com/*

- Commande de base : 

- Redémarré la raspberry pi

      sudo reboot 

- Eteindre la raspberry pi 

      sudo poweroff

- Espace de stockage disponible :

      df -h

- PROBLEME SSH DEPUIS WINDOWS SI REINSTALLATION OS (permet de supprimer l'ancienne clé dite offensive) 

      ssh-keygen -R 192.168.1.XX  ou ssh-keygen -R XX.local

## Initiation RPI

- Se connecter au RaspberryPi en SSH (Depuis un autre appareil) : https://www.youtube.com/watch?v=lZ3AMFr9oMQ

- Raspberry Pi : ce qu'il faut connaître pour bien commencer : https://www.youtube.com/watch?v=g9u6KleX7iU


## VNC VIEWER

- Raspberry Pi sans clavier ni écran ? Voici comment accéder à Linux à distance avec VNC. Tutoriel : https://www.youtube.com/watch?v=bfK_oP8fcEE&t=431s

- How to access Raspberry pi remotely with VNC direct connection and cloud connection : https://www.youtube.com/watch?v=pcn7WyxSHT0

- Commande a tapé, pour Installer vnc viewer  

      sudo apt-get install realvnc-vnc-server realvnc-vnc-viewer

## Installer vs code 

Doc vscode : https://code.visualstudio.com/docs/setup/raspberry-pi


## Installer git :

- Installe Git avec la commande suivante :

      sudo apt install git -y

- Vérifie l’installation

      git --version

- Configurer le profil

      git config --global user.name "Ton Nom"
      git config --global user.email "ton.email@example.com"

- Vérifier la configuration

      git config --global --list

- Voir également dépot suivant pour plus de détails : https://github.com/Darkzveller/config-memo_git/blob/main/README.md


## Installer Android TV (NE FONCTIONNE PAS BIEN VOIR PAS DU TOUT EN FONCTION DE L USAGE)

📺 CREEZ votre propre ANDROID TV BOX grâce à un Raspberry Pi (⚠️**DECONSEILLER DE FAIRE CELA POUR DES RASPBERRY PI INFERIEUR AU 5, CAR NE CONTIENT PAS LES CODECS D'ANDROID**) ! : https://www.youtube.com/watch?v=_gk0qncIvX8 

- Installer Android TV 11 Sur Raspberry Pi : https://www.youtube.com/watch?v=kuWCA1xqcN4

- konstakang rpi 4 : https://konstakang.com/devices/rpi4/

## Observer température cpu via le terminal

- Avoir la température a l'instant t

      vcgencmd measure_temp

- Avoir la température en temps réel toutes les secondes 

      watch -n 1 vcgencmd measure_temp

- Avoir la température en temps réel toutes les secondes en sautant de ligne permettant ainsi d'avoir l'historique de température 

      while true; do vcgencmd measure_temp ; sleep 1 ; done

- Ajouter le plugin, pour observer la température en temps réel en espagnol Como ver la temperatura del raspberry pi : https://www.youtube.com/watch?v=YE0B5rLgD1c

## Installer Neofetch pour avoir des détails sur sa distribution :

- Installer git au préalabre : 
            
      sudo apt install git -y

- cloner le dépot du projet : 

      git clone https://github.com/dylanaraps/neofetch.git

- Etre dans le répértoire créer : 

      cd neofetch

- Lance l'installation de neoftech

      sudo make install

- Revenir dans le dossier parent

      cd

- Supprime le dossier préalablement créer :

      rm -rf neofetch/

- Lance le logiciel :

      neofetch
  
- Tout faire en une seule ligne de commande

      git clone https://github.com/dylanaraps/neofetch.git && cd neofetch && sudo make install && cd && rm -rf neofetch/ && neofetch

- Supprimer neofetch

      git clone https://github.com/dylanaraps/neofetch.git && cd neofetch && sudo make uninstall

## Stress test  

- Commande pour l'installer 

      sudo apt install stress -y

- Exemple faire stresser les 4 thread/coeurs en meme temps pendant 60 secondes

      stress --cpu 4 --timeout 60 

## Changer langue du terminal 

### De manière permanent

     sudo nano /etc/locale.gen // Décommente ou ajoute la ligne : fr_FR.UTF-8 UTF-8

    sudo locale-gen

    sudo update-locale LANG=fr_FR.UTF-8 LANGUAGE=fr_FR:fr  

    source /etc/default/locale

    locale

### De manière provisoire

    export LANG=fr_FR.UTF-8

    export LANGUAGE=fr_FR:fr

    export LC_ALL=fr_FR.UTF-8
