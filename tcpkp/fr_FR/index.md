# Plugin Niren TcpKP

Ce plugin sert à communiquer avec les modules ethernet Niren TCP-KP-I8O8.
voir lien d'achat :[aliexpress][]

Ce plugins creer :
- 8 commandes info pour connaitre l'état des 8 relais,
- 8 commandes info pour connaitre l'état des 8 entrées,
- 8 commandes action pour allumer les relais,
- 8 commandes action pour éteindre les relais,

## Configuration plugins

Pour utilser le plugins, vous devez configurer les informations suivante:

- adresse IP du modules
- port de communication vers le module

## Configuration du module

l'adresse Ip du module est par défaut: '192.168.1.199'
Il est en natif configuré en client.

Nous allons nous y connecter pour lui attribuer une IP fixe, renseigner le port de communication et le passer en serveur.

Pour cela il vous faudra lancer le logiciel de configuration disponible [ici][]

- changer l'adresse ip de votre Pc pour ce mettre sur la meme plage d'adresse que le module (192.168.1.XX)

- Lancer le logiciel configuration

- Dans le haut du logiciel, selectionner votre carte réseau à laquelle est connectée votre module

![Selection carte réseau](https://lefilliatre.github.io/tcpkp/sources/selectCarte.png)

- Lancer ensuite la recherche du module
![Recherche du module](https://lefilliatre.github.io/tcpkp/sources/Recherche.png)

- Si tout est raccordé correctement, votre module doit apparaitre dans la fenetre
![liste](https://lefilliatre.github.io/tcpkp/sources/liste.png)

[aliexpress]: https://fr.aliexpress.com/item/33005606116.html?spm=a2g0o.seodetail.topbuy.1.2d4f5bf3IYMFA2 "aliexpress"
[ici]: https://lefilliatre.github.io/tcpkp/sources/logiciel%20de%20configuration.zip "archive logiciel"
