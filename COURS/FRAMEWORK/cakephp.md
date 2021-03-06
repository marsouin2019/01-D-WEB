# Cakephp qu'est-ce que c'est ?

-- source : https://book.cakephp.org/1.3/fr/The-Manual/Beginning-With-CakePHP/What-is-CakePHP-Why-Use-it.html  --

CakePHP est un framework de développement rapide pour PHP, gratuit et open-source.
C’est un ensemble de briques élémentaires pour les programmeurs qui créent des applications web.
Notre objectif principal est de vous permettre de travailler de manière rapide et structurée, sans toutefois perdre en flexibilité.

# Comprendre le modèle MVC

-- source : https://book.cakephp.org/1.3/fr/The-Manual/Beginning-With-CakePHP/Understanding-Model-View-Controller.html --


Tous ce qui va suivre se fait exclusivement en ligne de commande dans le terminal de votre système.

# pré-requis pour installer cakephp

Penser à votre environnement de travail avant de vous lancer dans une installation de cakephp.
Il fonctionne avec le serveur web Apache, nginx, LightHTTPD ou Microsoft IIS.


    Un serveur HTTP. Par exemple: Apache. mod_rewrite est préférable, mais en aucun cas nécessaire.
    PHP 5.6 ou plus (y compris PHP 7.3)
    L’extension PHP mbstring
    L’extension PHP intl
    L’extension PHP simplexml

## Configuration serveur apache2

Pour installer les packages cités :
- sudo apt-get install php7.2-mbstring
- sudo apt-get install php7.2-intl
- sudo apt-get install php7.2-simplexml

Relancer ensuite le serveur Apache2
- sudo service apache2 restart

**OU**

- sudo /etc/init.d/apache2 restart


# Installer Composer local

Installer si ce n'est pas encore fait 'Curl' correspondant à votre version de PHP. Vérifier votre version de PHP :
- php -v
ici notre version est php7.2 
Ce n'est pas génant si votre version est différente, il faut chercher les installations correspondante exclusivement à votre version.

Puis :
- sudo apt-get install php7.2-curl

**ATTENTION** : regarder les informations sur votre écran
**SI** vous avez un message comme par exemple : 

----
php7.2-curl is already the newest version (7.2.13-1+0~20191218.50+debian9~1.gbp23c2da).
The following package was automatically installed and is no longer required:
  libtidy5
Use 'apt autoremove' to remove it.

----

Ici le message vous indique que vous devez utiliser la commande **'sudo apt-get autoremove'** pour supprimer les packages php obsoletes.

## Télécharger Composer. 

Composer un est fichier script 'composer.phar' qui comprend un ensemble d'instruction qui seront utiles pour installer tous programmes (application web) pour Linux ou Windows.

la commande est : 
- sudo curl -sS https://getcomposer.org/installer | php

Cela va prendre un peu de temps, tout dépendra de votre connexion internet.

Une fois téléchargé, vous aurez un message de confirmation tel que :

---
Composer (version 1.9.2) successfully installed to: /root/composer.phar
Use it: php composer.phar

---
Ce message vous indique que l'installation c'est bien passée. Pour utiliser 'composer' utiliser la commande 'php composer.phar'


# Installer cakephp

Se positionner sur votre espace web (var/www/html) et créer le dossier correpondant à votre nom de domaine :
- cd /var/www/html
- sudo mkdir madapitt.com

**LA CREATION DU DOSSIER N'EST PAS UNE OBLIGATION DANS CE CAS UNIQUEMENT.**

Télécharger les fichiers du framework 'cakephp' :

- sudo php composer.phar create-project --prefer-dist cakephp/app:^3.8 madapitt.com/

La commande **'composer'** avec l'instruction **'create-project'** permet de créer notre dossier nom de domaine, **'--prefer-dist cakephp/app:^3.8'** indique le nom de la distribution que nous souhaitons installer et sa version.

Cela va prendre un peu de temps, tout dépendra de votre connexion internet.

## Question lors de l'installation

Created '/var/www/html/madapitt.com/tmp/cache/views/' directory
Set Folder Permission ? Y

Les droits d'écriture seront poser sur tout les dossiers de tmp/*


## Lancer le serveur

Après votre installation cakephp, mets à votre disposition une commande pour lancer directement le site via une commande serveur.
- sudo cake/bin server


## Les erreurs lors de l'installation

### Fichier 'composer.json' manquant

Ce fichier est comme une base de données il historise toutes les actions de composer sur notre serveur.
Le plus simple pour régler ce problème est de télécharger directement sur github cakephp v3.8.8 (janvier 2020).


**Comment faire**
- Se rendre sur votre dossier projet de votre serveur (cd /var/www/html/madapitt.com)
- Télécharger cakephp : sudo wget https://github.com/cakephp/cakephp/releases/download/3.8.8/cakephp-3-8-8.zip
- Dézipper le fichier 3.8.8.zip : sudo unzip -d cakephp-3.8.8.zip


**ATTENTION**
----------------
A la décompresion du fichier cakephp-3.8.8.zip, il est possible que vous ayez un répertoire portant le même nom. Dans ce cas, et uniquement si cela c'est produit, se déplacer dans ce dossier et copier l'ensemble des fichiers et dossier et les coller dans votre dossier web de travail.

- cd cakephp-3.8.8
- sudo cp -r * ../madapitt.com/

POUR INFO : Commande linux pour copier (-R,-r, --recursive 	Pour copier récursivement les répertoires)

### Probleme de droit

Sur les erreurs de droits sur des dossiers nommer changer les droits en :
- sudo chmod -R 777 logs/


