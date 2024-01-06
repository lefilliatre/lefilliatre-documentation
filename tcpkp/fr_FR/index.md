---
layout: default
title: Plugin TcpKP
lang: fr_FR
pluginId: tcpKP
---

# Plugin Niren TcpKP

Ce plugin sert à communiquer avec les modules ethernet Niren TCP-KP-I8O8.
voir lien d'achat :[aliexpress][]

![TCP-kp I8O8](https://lefilliatre.github.io/lefilliatre-documentation/tcpkp/sources/niren.png)

Ce plugins creer :
- 8 commandes info pour connaitre l'état des 8 relais,
- 8 commandes info pour connaitre l'état des 8 entrées,
- 8 commandes action pour allumer les relais,
- 8 commandes action pour éteindre les relais

Il à la particularité d'être trés réactif les 32 infos/commandes sont raffraichies toutes les 320ms
Il posséde aussi une fonction "télérupteur" permettant (par le mappage) de reduire encore le temps de réation à la vitesse du réseau ethernet pour des fonctions de va&vient par exemple.

## Configuration plugins

Pour utilser le plugins, vous devez configurer les informations suivante:

![configuration](https://lefilliatre.github.io/lefilliatre-documentation/tcpkp/sources/configurationPlugins.png)

- adresse IP carte : Adresse IP du tcp-kp
- port communication carte : port de communication entre le demon et le tcpkp (mettre la même valeur que dans le module ex:12345)
- port communication Jeedom : port de communication entre le demon et jeedom (choisir un port de libre sur la box jeedom ex:54987)

### Mode télérupteur

Il est possible de piloter une sortie par une ou plusieurs entrées directement sans passer par jeedom afin d'avoir un system trés réactif.
![liste](https://lefilliatre.github.io/lefilliatre-documentation/tcpkp/sources/mapping.png)

Par exemple :
Si sur l'entrée 1 vous raccordé un interrupteur, sur l'entrée 2 un deuxieme interrupteur et que vous souhaitez faire une fonction va et vient pour piloter un éclairage raccordé sur la sortie 5,
Vous pouvez la programmé dans un scénario mais il y aurra un légé décallage entre l'appui sur l'interrupteur et l'allumage de la lampe du au temps de traitement de jeedom.
Pour s'affranchir du temps de traitement de jeedom, vous pouvez déclarer l'entrée 1 mappée sur la sortie 5, et l'entrée 2 mappé sur la sortie 5.
A chaque changement d'état des entrées 1 et 2,la sortie 5 changera d'état.
Cela n'empeche que les états des deux entrées et le pilotage de la sortie reste accessible et pilotable par jeedom.

Attention, il faut redémarrer le démon pour la prise en compte du mapping.

## Configuration du module
l'adresse Ip du module est par défaut: '192.168.1.199'
Il est en natif configuré en client.

Nous allons nous y connecter pour lui attribuer une IP fixe, renseigner le port de communication et le passer en serveur.

Pour cela il vous faudra lancer le logiciel de configuration disponible [ici][]

- changer l'adresse ip de votre Pc pour ce mettre sur la meme plage d'adresse que le module (192.168.1.XX)

- Lancer le logiciel configuration

- Dans le haut du logiciel, selectionner votre carte réseau à laquelle est connectée votre module

![Selection carte réseau](https://lefilliatre.github.io/lefilliatre-documentation/tcpkp/sources/selectCarte.png)

- Lancer ensuite la recherche du module

![Recherche du module](https://lefilliatre.github.io/lefilliatre-documentation/tcpkp/sources/recherche.png)

- Si tout est raccordé correctement, votre module doit apparaitre dans la fenetre

![liste](https://lefilliatre.github.io/lefilliatre-documentation/tcpkp/sources/liste.png)

- double cliquer dessus pour se connecter

(dans l'exemple ci dessous JEEDOM à pour adresse 192.168.1.100,le masque est 255.255.255.0, le module est en 192.168.1.101, le port de communication avec le démon est 12345
- Renseigner maintenant la configuration du module
	° L'adresse IP de votre jeedom (celle du rpi par exemple)
	° Le masque du réseau
	° L'adresse IP Fixe de votre module (celle mise dans la configuration du plugins)
	° Le port de communication du module (celle mise dans la configuration du plugins)
	° Le mode de fonctionnement (TCP_Server)
	
![liste](https://lefilliatre.github.io/lefilliatre-documentation/tcpkp/sources/param.png)

- Enregistrer les parametres

![liste](https://lefilliatre.github.io/lefilliatre-documentation/tcpkp/sources/enregistre.png)


- Re-cliquer sur votre module pour verifier que tout à été enregistré

![liste](https://lefilliatre.github.io/lefilliatre-documentation/tcpkp/sources/liste.png)

- Le module est prét à etre installé dans votre installation!

# FAQ
Vois sur le Forum jeedom

[aliexpress]: https://fr.aliexpress.com/item/33005606116.html?spm=a2g0o.seodetail.topbuy.1.2d4f5bf3IYMFA2 "aliexpress"
[ici]: https://lefilliatre.github.io/lefilliatre-documentation/tcpkp/sources/logiciel%20de%20configuration.zip "archive logiciel"
