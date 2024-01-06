---
layout: default
title: Plugin PoeleAgua
lang: fr_FR
pluginId: PoeleAgua
---

# Plugin PoeleAgua

Ce plugin sert à communiquer avec les poêles à bois et/ou granulé communiquant sur la base du system AGUA IOT.

Il se base sur le travail de fredericvl avec le script python [py-agua-iot][]
Ce plugin permet l’intégration des poêles connectés par la plateforme AGUA IOT de Micronova dans **Jeedom**

Attention ce plugin n’a pas été testé avec tous les poêles. , il n’y a donc aucune garantie que cela fonctionnera avec le vôtre.

Post forum listant des modéles testés [post forum Liste des matériels compatible][]

## Configuration

Pour utiliser le plugin, vous devez configurer les informations suivantes :

# Mode expert
Le mode expert permet d’ajouter des retour d’état et commandes spécifiques à chaque marque et modèle de poêle.

Attention : certaines commandes, si mal paramétrées, peuvent altérer le fonctionnement de votre poêle. Il est impératif de se référer à la documentation de votre équipement et de comprendre les différentes options et paramètres de votre poêle préalablement à toute intervention dans le plugin Poêle Agua IOT. 

## Bonnes pratiques :
Il est vivement conseillé de ne créer dans un premier temps que les retours d’états souhaités et d’en avoir l’historique (‘Historiser’ coché). Faire les tests de commande avec l’application Android ou Apple dédiée à côté de l’équipement et s’assurer que le changement d’état dans le plugin correspond bien à la commande désirée et modifie bien le comportement du poêle.
Créer ensuite les commandes dans le plugin. Faire les tests de commande avec le plugin à côté de l’équipement et s’assurer que le changement d’état dans l’application Android ou Apple dédiée correspond bien à la commande désirée et modifie bien le comportement du poêle.
Si un retour d’état ou une commande n’est pas disponible dans l’application Android ou Apple dédiée, elle ne le sera pas non plus dans le plugin !
