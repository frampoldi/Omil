# Omil
OMIL est une application qui permet de gérer les ordres de mission  d'un laboratoire/organisme UCB/CNRS &amp; autres
Sad Mezzour 
Contact : sad.mezzour@lasim.univ-lyon1.fr
		  ixus.zone@gmail.com 	

Laboratoire : LASIM UMR5579

Contenu :

- OMIL : Qu'est ce que c'est ?
- Dépendances
- Installation et configuration


###########################################
--- OMIL Qu'est-ce que c'est ?
###########################################

OMIL une application WEB codé en PHP & MySQL, elle a été crée pour remplacer un formulaire papier
remplit par les usagers du laboratoire pour les demandes d'ordres de mission. OMIL est très pratique pour les
organismes situés dans des bâtiments différents, enfin il est accéssible via une interface web donc partout dans le monde.

OMIL est une application qui permet de gérer les ordres de mission 
d'un laboratoire/organisme UCB/CNRS & autres.

Les fonctionnalités principales de l'application s'articulent autour de trois
axes :

1) L'usager remplit le formulaire en 5 étapes avec possibilité d'envoyer
un récapitulatif de sa demande en copie par mail à ses collègues.

2) En fonction de la hiérarchie administrative, le directeur/Gestionnaire des crédits
reçoit une notification par mail lui indiquant de traiter la demande en fonction des
crédits propres au laboratoires. Il accède à son interface d'administration puis il 
traite la demande.

ATTENTION : tant que le directeur/ou gestionnaire n'a pas traiter la demande, les secrétaires ne recevront pas de 
notification par mail. VOUS DEVEZ IMPERATIVEMENT TRAITER LA DEMANDE EN TANT que "Type" directeur ou en superadmin

3) Après traitement du directeur/gestionnaire, la ou les secrétaires reçoivent un mail
leurs indiquant d'accéder à leurs espaces d'administration pour traiter la demande.
Après traitement sur Xlab ou Sifac, les utilisateurs recevront un mail les informant 
que leur demande a été traité. 
 
Enfin, cette application a pour but d'être dynamique et directement reliée
aux utilisateurs. Le formualaire se décline en Anglais & Français.


#############################################################
--- Dépendances (uniquement testé avec ces configurations)
#############################################################

1) Apache, PHP 5
2) MySQL 4.1.2 et supérieures
3) Javascript activé
4) Testé sous firefox, IE et Opera (Attention quelques pbs avec Chrome)
5) Développement de l'application sous environnement Linux (Debian) - Geany 

Librairies/classes :
LAMP (Apache/PHP/Mysql/PhpMyadmin)
Gimp
Jquery
calendar : www.dynarch.com
HtmltoPdf
Pjmail



##############################################################
--- INSTALLATION DE OMIL ET CONFIGURATION
##############################################################


--- Configuration nécessaire

Vous devez au minimum disposer d'un espace sur un serveur Web avec :
-  un accès au serveur pour l'installation des fichiers (FTP, SSH, etc);
-  le support de PHP4 ou supérieur compilé avec le support des sessions ;
-  un accès à une base de données MySQL.

Avant l'installation, vous devez avoir une base MySQL disponible. Si vous n'êtes pas l'administrateur du serveur, il faut demander l'activation d'une base MySQL à l'administrateur.

Vous devez connaître les paramêtres de votre connexion MySQL (fournies par l'administrateur) :
-  l'adresse du serveur MySQL ;
-  votre login MySQL ;
-  votre password MySQL ;
-  le nom de la base de données.


Décompactez l'archive sur votre ordinateur dans un répertoire de votre choix, puis transférez le contenu de ce répertoire sur le serveur Web.

Si vous êtes l'administrateur du serveur décompresser l'archive dans le répertoire racine d'Apache 
(/var/www  ou /var/www/html).

--- Installer les fichiers

Installez l'ensemble des fichiers OMIL dans l'espace Web, à l'endroit où vous voulez que OMIL soit accessible au public ci-possible en interne.

Maintenant, il est nécessaire d'accorder des permissions à certains répertoires, de manière à ce que PHP ait les droits en écriture sur : /backups
 
--- Début de l'installation

Avant tout, vous devez créer une base de données MySQL (ex: omil), puis importer le fichier omil.sql situé dans /bdd 
Ce fichier est composé de 4 tables.

Après importation, éditer le fichier connexion.php en insérant toutes les informations pour accéder à la base de données :

$host_db = "localhost";
$user_db = "";
$pass_db = "";
$bdd = "omil";

Par exemple : le serveur est localhost et le nom de la bdd est omil

Ensuite il vous suffit de faire pointer votre navigateur web sur le dossier racine de GLPI : http://votreserveur/omil/ pour accéder au formulaire
Si vous désirez accéder à l'espace super-administrateur : http://votreserveur/omil/adminixus.php

Login = admin
password = pass

N'oubliez pas de changer le mot de passe.

L'interface est intuitive, il suffit d'entrer les informations demandées.

--- Fin de l'installation




############################################
--- EVOLUTIONS
############################################


I) Evolution de l'application :

OMIL est une application dynamique, elle n'est pas parfaite et certainement évolutive. N'hésitez pas à l'à faire
évoluer (juste un petit mail pour m'informer sinon bonne continuation).
