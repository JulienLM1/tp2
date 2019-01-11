TP 2 - Exploration du réseau d'un point de vue client
I. Exploration locale en solo
1. Affichage d'informations sur la pile TCP/IP locale
En ligne de commandes

Ecrire 'ipconfig /all' dans l'invite de commandes ou 'ifconfig' sur Linux ou Mac

Interface WiFi :
Nom : Carte réseau sans fil Wi-Fi
Adresse MAC : 98.28.a6.17.7e.98
Adresse IPv4 : 169.254.6.228/16
Adresse de réseau : 10.33.0.0
Adresse de broadcast : 10.33.3.255
Passerelle par défaut : 10.33.3.253

Interface Ethernet :
Nom : Carte Ethernet Ethernet
Adresse MAC : 98.28.a6.17.7e.98
Adresse IP : Inexistante car non connecté
Adresse de réseau : Inexistante car non connecté
Adresse de broadcast : Inexistante car non connecté

La gateway d'Ingésup est une IP réelle qui est un équipement présent sur le réseau Ingésup. Elle permet de sortir du réseau et de se connecter sur Internet.

En graphique

Panneau de configuration > Réseau & Internet > Aficher vos propriétés réseau

2. Modifications des informations
A. Modification d'adresse IP - pt. 1
1ère adresse du réseau disponible : 10.33.0.1
Dernière adresse du réseau disponible : 10.33.3.254
10.33.3.253 = gateway
Pour changer son adresse IP de la carte WiFi (sous Windows) :

Panneau de configuration > Réseau et Internet > Wi-Fi > Centre Réseau & partage.
Choisir votre connexion via WiFi@YNOV, puis sur Propriétés > Protocole Internet version 4 (TCP/IPv4) > Propriétés
Prendre l'adresse IP suivante et rentrez une adresse IP entre la 1ère et la dernière adresse IP disponible (calculez plus tôt)
Masque de sous-réseau : 255.255.252.0
Passerelle par défaut : 10.33.3.253
Serveurs DNS  : 89.2.0.1

B. nmap
Installez Nmap, puis ouvrir une invite de commandes. Rendez-vous dans le dossier dans lequel Nmpa est installé et tapez 'nmap -sn -PE 10.33.0.0/22' L'outil va scanner le réseau est afficher toutes les adresses IP utilisées dans l'ordre croissant.

C. Modification d'adresse IP - pt. 2
Choississez une adresse IP libre grâce à Nmap et modifiez votre adresse IP actuelle (voir I.2.A.) Dans notre cas on choisira 10.33.3.235 En changeant notre adresse de gateway en 10.33.3.251, il nous est impossible d'accèder à Internet.

II. Exploration locale en duo
1. Prérequis
deux PCs avec ports RJ45
un câble RJ45
firewalls désactivés sur les deux PCs
Pour désactiver le firewall (le pare-feu), se rendre dans : Paramètres > Mise à jour & Sécurité Dans l'onglet Sécurité de Windows > Pare-feu et protection réseau Puis désactivez chacun des réseaux (avec domaine, privé, public).

2. Câblage

3. Modification d'adresse IP
Pour modifier l'IP des deux machines pour qu'elles soient dans le même réseau, suivez les mêmes étapes que dans la partie locale en solo (à l'étape 2 cliquez sur Ethernet)
Vérifiez à l'aide de commandes que vos changements ont pris effet (voir ipconfig partie I. 1.)
Utilisez ping pour tester la connectivité entre les deux machines.

J'ai essaié de faire la partie deux et trois avec des personnes de la classe et seul d'ou mon retard pour l'envoie.
