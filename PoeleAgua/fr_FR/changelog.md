---
layout: default
title: Changelog PoeleAgua
lang: fr_FR
pluginId: PoeleAgua
---

# Changelog plugin PoeleAgua

>**IMPORTANT**
>
>Pour rappel s'il n'y a pas d'information sur la mise à jour, c'est que celle-ci concerne uniquement de la mise à jour de documentation, de traduction ou de texte.

# 26/02/2023
- RELEASE : Retour sur la release du 31-01-20223
- BETA : Suite mise a jour

# 25/02/2023
- Tentative correction suite maj du 23/02/2023

# 23/02/2023
- Mise à jour suite à mise a jour serveur JollyMec (UUID à modifier avec valeur de la doc et la version a changer)

# 31/01/2023
- Passage de la beta du 27/01/2023 en release.

# BETA 27/01/2023
- Suite correction meilleur gestion des problemes de communication entre le serveur et le poele

# BETA 15/01/2023
- Correction pour meilleur gestion des problemes de communication entre le serveur et le poele
- Correction formatage du host en version 1.6.0

# 12/01/2023
- Passage de la beta du 11/01/2023 en release.

# BETA 11/01/2023
- Mise à jour des statusTexte et AlarmeTexte

# BETA 10/01/2023
- Mise en forme des logs pour meilleur interprétation

# 03/01/2023
- Mise à jour de la documentation

# BETA 03/01/2023
- Correction Commande action qui ne fonctionne pas sur version >1.8.1 micronova (Merci à @Scorpix)

# BETA 28/12/2022
- Modification pour support version 1.9.0 de micronova.
- Test sur myPiazzeta (Merci à @Damien77)
- Attention il faut maintenant préciser la version exact (voir la documentation)

# BETA 24/12/2022
- Modification pour support version 1.8.1 de micronova.
- Test sur mysuperior

# 10/12/2022
- Passage de la beta du 22/11/2022 en release.
- Ajout de status et texte d'alarme

# BETA 22/11/2022
- Correction erreur dans le demon qui avait pour effet de lancer deux connexions sur la plateforme agua-iot au lieu d'une. Peut-etre une piste pour les personnes qui ont des défauts de "fetching device..."

# 20/11/2022
- Passage de la beta du 15/11/2022 en release. Pour info les commandes action "start" et "stop" peuvent etre utiliser à la place de la liste déroulante "startstop".

# BETA 15/11/2022
- Traduction de certain status de poele (Moretti) (Merci à dan_73)
- Correction retour état start/stop sur commande action start/stop pouvant empecher le pilotage sur version web

# 11/11/2022
- Correction récupération description du poêle aprés modification dans l'app
- Correction documentation
- Correction champs enlevés à la conversion V4.2

# 04/11/2022
- Modification pour core jeedom V4.2
 
# 01/10/2022
- Passage de la beta du 26/09/2022 en release. Attention nécessite la suppression de la commande : status géré qui sera recréer

# BETA 28/09/2022
- Ajout detail dans les logs avec connexion par url de login

# BETA 26/09/2022
- Ajout mode "expert" pour l'ajout de commandes spécifique. (voir doc du plugins)

# BETA 22/09/2022
- Preparation pour ajout des commandes spécifique à une marque ou modele. Attention nécessite la suppression de la commande : status géré qui sera recréer automatiquement.

# BETA 06/06/2022
- Ajout url de login dans la configuration du plugins pour poele MyPiazzetta

# 02/04/2022
- correction intall dépendance six (merci micke74)
 
# 01/04/2022
- Forcage décodage json en UTF8

# 18/03/2022
- Mise a jour des états texte pour les modèles moretti (merci SosoSoja)

# 14/03/2022
- Modification remontée de la température fumée et commandes spéciales pour les poêles moretti design
- suppression du login et mot de passe des logs pour pouvoir les poster sans risque

# 08/03/2022
- Augmentation timeout http + ajout log

# 03/03/2022
- Ajout jwt et serial en dependance

# 25/02/2022
- Correction bug caractere spéciaux dans mot de passe (merci numerobis08)

# 24/02/2022
- passage de py-agua-iot de dépendance à package
- Ajout de la dé-installation de py-agua-iot avant la mise a jour

# 23/02/2022
- Amélioration des logs en debug
- Ajout requests en dépendance

# 14/02/2022
- Correction probleme six sur installation dépendances

# 12/02/2022
- Ajout de l'alrme au format texte

# 29/01/2022
- Ajout py-agua-iot en dépendance

# 27/01/2022
- suppression dependance inutile

# 20/01/2022
- Mise sur le market

# 19/01/2022
- Mise a jour de la documentation

# 18/01/2022
- Création du plugins
