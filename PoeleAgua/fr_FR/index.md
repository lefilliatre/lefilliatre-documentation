# Plugin PoeleAgua

Ce plugin sert à communiquer avec les poêles à bois et ou granulé communiquant sur la base du system AGUA IOT.

Il se base sur le travail de fredericvl avec le script python [py-agua-iot][]
Ce plugins permet l'intégration des poêles connecté par la plateforme AGUA IOT de Micronova à **Jeedom**

Attention ce plugins n'a pas été testé avec tous les poêles. Aucune garantie que cela va fonctionner avec le votre.

## Configuration

Pour utilser le plugins, vous devez configurer les informations suivante:

### Api URL et Customer Code
Vous devez renseigner l'adresse de la plateforme Agua IOT de votre fabricant  et le code customer correspondant ex: https://jollymec.agua-iot.com 732584

```
| Fabricant                     | Customer Code | API URL                                | Separate login URL (only needed if specified)         |
| ----------------------------- | ------------- | -------------------------------------- | ----------------------------------------------------- |
| EvaCalòr - PuntoFuoco         | 635987        | https://evastampaggi.agua-iot.com      |                                                       |
| Elfire Wifi                   | 402762        | https://elfire.agua-iot.com            |                                                       |
| Karmek Wifi                   | 403873        | https://karmekone.agua-iot.com         |                                                       |
| Easy Connect                  | 354924        | https://remote.mcz.it                  |                                                       |
| Easy Connect Plus             | 746318        | https://remote.mcz.it                  |                                                       |
| Easy Connect Poêle            | 354925        | https://remote.mcz.it                  |                                                       |
| Lorflam Home                  | 121567        | https://lorflam.agua-iot.com           |                                                       |
| LMX Remote Control            | 352678        | https://laminox.agua-iot.com           |                                                       |
| Boreal Home                   | 173118        | https://boreal.agua-iot.com            |                                                       |
| Bronpi Home                   | 164873        | https://bronpi.agua-iot.com            |                                                       |
| EOSS WIFI                     | 326495        | https://solartecnik.agua-iot.com       |                                                       |
| LAMINOXREM REMOTE CONTROL 2.0 | 352678        | https://laminox.agua-iot.com           |                                                       |
| Jolly Mec Wi Fi               | 732584        | https://jollymec.agua-iot.com          |                                                       |
| Globe-fire                    | 634876        | https://globefire.agua-iot.com         |                                                       |
| TS Smart                      | 046629        | https://timsistem.agua-iot.com         |                                                       |
| Stufe a pellet Italia         | 015142        | https://stufepelletitalia.agua-iot.com |                                                       |
| My Corisit                    | 101427        | https://mycorisit.agua-iot.com         |                                                       |
| Fonte Flamme contrôle 1       | 848324        | https://fonteflame.agua-iot.com        |                                                       |
| Klover Home                   | 143789        | https://klover.agua-iot.com            |                                                       |
| Nordic Fire 2.0               | 132678        | https://nordicfire.agua-iot.com        |                                                       |
| GO HEAT                       | 859435        | https://amg.agua-iot.com               |                                                       |
| Wi-Phire                      | 521228        | https://lineavz.agua-iot.com           |                                                       |
| Thermoflux                    | 391278        | https://thermoflux.agua-iot.com        |                                                       |
| Darwin Evolution              | 475219        | https://cola.agua-iot.com              |                                                       |
| Moretti design                | 624813        | https://moretti.agua-iot.com           |                                                       |
| Fontana Forni                 | 505912        | https://fontanaforni.agua-iot.com      |                                                       |
| MyPiazzetta (MySuperior?)     | 458632        | https://piazzetta.agua-iot.com         | https://piazzetta.iot.web2app.it/api/bridge/endpoint/ |
| Alfaplam                      | 862148        | https://alfaplam.agua-iot.com          |                                                       |
| Nina                          | 999999        | https://micronova.agua-iot.com         |                                                       |
| Galletti                      | ?             | ?                                      |                                                       |
```
### UUID

UUID aléatoire (généré s'en un automatiquement : [https://www.uuidgenerator.net/version4)][]

### Marque

Généralement =1

### Login sur l'app
	
Login sur l'app (email)

### Login sur l'app
Mot de passe sur l'app

### Port de communication Jeedom
Renseigner un port de libre pour la communication avec jeedom 



[py-agua-iot]: https://github.com/fredericvl/py-agua-iot "Github"
[https://www.uuidgenerator.net/version4)]: https://www.uuidgenerator.net/version4 "Génération UUID"
