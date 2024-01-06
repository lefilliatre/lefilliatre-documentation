---
layout: default
title: plugin TcpKP
lang: fr_FR
pluginId: tcpkp
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
