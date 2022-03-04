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

#FAQ
## Certificats
Avec certainne plateforme, vous pouvez renconter des difficultées à vous connecter sur le serveur du fabricant (ex : mcz) à cause du certificat pour le https.
Pour corriger le pb sur remote-mcz par exemple:
*  récupérer le certificat (remote-mcz-it-chain.pem) du site (à partir de votre navigateur web)
Du genre:
```
-----BEGIN CERTIFICATE-----
MIIGujCCBaKgAwIBAgIQCu86AermVJHmCGKh0S0GrjANBgkqhkiG9w0BAQsFADBN
MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMScwJQYDVQQDEx5E
aWdpQ2VydCBTSEEyIFNlY3VyZSBTZXJ2ZXIgQ0EwHhcNMjAwNjAzMDAwMDAwWhcN
MjIwNjA4MTIwMDAwWjB4MQswCQYDVQQGEwJJVDEeMBwGA1UECBMVRnJpdWxpIFZl
bmV6aWEgR2l1bGlhMRYwFAYDVQQHEw1Gb250YW5hZnJlZGRhMRkwFwYDVQQKExBN
Q1ogR1JPVVAgUy5wLkEuMRYwFAYDVQQDEw1yZW1vdGUubWN6Lml0MIIBIjANBgkq
hkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEA7WKFHvKtmcCIT+DJXTdmYoLDP6glGqEh
dVU95C8XpjQJGd08b+J4p+s1ERLyyigF9RNgQjTJ/ehUyfSmLNOuszplcq7VTgsd
/i2+0AhtiyIgRdRjt7fODm/AC4pj74tPunBnt01JnQLRzelFleRQMu3iKnj4ctR7
KQO4nY2S0JHt6JpLvgALEN2zF2+pJiw+O6t8hANNJKI3KdVK5Cq2KDk7yMyEsvxR
4ns6lkwIR1moaAt6cUkULg+v5SgKhBFT4eQhqoY5HmnC4R0+RlLPNGhNXi6cUFM5
VxxD09gBMmTEkjSUz7b0h65LES3MW5U5GP4ihlaTBdRNGPcGpPYFewIDAQABo4ID
aTCCA2UwHwYDVR0jBBgwFoAUD4BhHIIxYdUvKOeNRji0LOHG2eIwHQYDVR0OBBYE
FJ+zPMkkxAeoVuCFOUCp3IAAX7s5MCsGA1UdEQQkMCKCDXJlbW90ZS5tY3ouaXSC
EXd3dy5yZW1vdGUubWN6Lml0MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggr
BgEFBQcDAQYIKwYBBQUHAwIwawYDVR0fBGQwYjAvoC2gK4YpaHR0cDovL2NybDMu
ZGlnaWNlcnQuY29tL3NzY2Etc2hhMi1nNi5jcmwwL6AtoCuGKWh0dHA6Ly9jcmw0
LmRpZ2ljZXJ0LmNvbS9zc2NhLXNoYTItZzYuY3JsMEwGA1UdIARFMEMwNwYJYIZI
AYb9bAEBMCowKAYIKwYBBQUHAgEWHGh0dHBzOi8vd3d3LmRpZ2ljZXJ0LmNvbS9D
UFMwCAYGZ4EMAQICMHwGCCsGAQUFBwEBBHAwbjAkBggrBgEFBQcwAYYYaHR0cDov
L29jc3AuZGlnaWNlcnQuY29tMEYGCCsGAQUFBzAChjpodHRwOi8vY2FjZXJ0cy5k
aWdpY2VydC5jb20vRGlnaUNlcnRTSEEyU2VjdXJlU2VydmVyQ0EuY3J0MAwGA1Ud
EwEB/wQCMAAwggF+BgorBgEEAdZ5AgQCBIIBbgSCAWoBaAB2ACl5vvCeOTkh8FZz
n2Old+W+V32cYAr4+U1dJlwlXceEAAABcnpRVP4AAAQDAEcwRQIgBzrv+Vk+eBMS
ji/TZdBL51eSwrPq67SOnUzya4Zl1aUCIQCDgBayJJxmKvFjhtQnGUe8/hoHC+rs
pRDADT6lU3j6nAB2ACJFRQdZVSRWlj+hL/H3bYbgIyZjrcBLf13Gg1xu4g8CAAAB
cnpRVS8AAAQDAEcwRQIgeCB/PwDSA68xE0MomkXyG7yBOJ9aXNr+bAbzEx6/WFsC
IQD3i5F/kW/RkkIxY69aElspCtPLLwlK280ONsVQrnK9aQB2AFGjsPX9AXmcVm24
N3iPDKR6zBsny/eeiEKaDf7UiwXlAAABcnpRVXkAAAQDAEcwRQIhAM/SHmuqvkA9
Fy0frQUn1vwn74MxMCqE23nUq6dlWm4DAiBzfERRSZi8nvHX52zyEmcR5uUD83rn
PvFttJdjhIISzjANBgkqhkiG9w0BAQsFAAOCAQEAAPMKwBwRGLA7x8b/NG2/C9Bj
JDTRXk+CAaOMh0+cjxvffEW4ehFFGasaUR4iHYTCU+KcA2Dr4c/uphHtnV8ajMBD
RL9xG5JHDlyUCX5mDw/tk9SueU8d1PmNzPfhdPRfhp2VRtUWRLG8U7GWPkQsi/NS
nHUoxi76FFtnlhDCghmYTvOMNNj3fEyWMYZdmR9JI1VTXuNe3R/WhasyYljKHmqc
AgydMsiJPv7QGlvIDxeD3iVZcZ6ARgoX+JTEhHPLPdDHmtPMnua5YToJdjH5GrLE
RI3kPIe0zku25r5RuUJUmbZ95X8H+geZGfxiDj//vASRcatN02p+eesdmvhvNg==
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
MIIElDCCA3ygAwIBAgIQAf2j627KdciIQ4tyS8+8kTANBgkqhkiG9w0BAQsFADBh
MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMRkwFwYDVQQLExB3
d3cuZGlnaWNlcnQuY29tMSAwHgYDVQQDExdEaWdpQ2VydCBHbG9iYWwgUm9vdCBD
QTAeFw0xMzAzMDgxMjAwMDBaFw0yMzAzMDgxMjAwMDBaME0xCzAJBgNVBAYTAlVT
MRUwEwYDVQQKEwxEaWdpQ2VydCBJbmMxJzAlBgNVBAMTHkRpZ2lDZXJ0IFNIQTIg
U2VjdXJlIFNlcnZlciBDQTCCASIwDQYJKoZIhvcNAQEBBQADggEPADCCAQoCggEB
ANyuWJBNwcQwFZA1W248ghX1LFy949v/cUP6ZCWA1O4Yok3wZtAKc24RmDYXZK83
nf36QYSvx6+M/hpzTc8zl5CilodTgyu5pnVILR1WN3vaMTIa16yrBvSqXUu3R0bd
KpPDkC55gIDvEwRqFDu1m5K+wgdlTvza/P96rtxcflUxDOg5B6TXvi/TC2rSsd9f
/ld0Uzs1gN2ujkSYs58O09rg1/RrKatEp0tYhG2SS4HD2nOLEpdIkARFdRrdNzGX
kujNVA075ME/OV4uuPNcfhCOhkEAjUVmR7ChZc6gqikJTvOX6+guqw9ypzAO+sf0
/RR3w6RbKFfCs/mC/bdFWJsCAwEAAaOCAVowggFWMBIGA1UdEwEB/wQIMAYBAf8C
AQAwDgYDVR0PAQH/BAQDAgGGMDQGCCsGAQUFBwEBBCgwJjAkBggrBgEFBQcwAYYY
aHR0cDovL29jc3AuZGlnaWNlcnQuY29tMHsGA1UdHwR0MHIwN6A1oDOGMWh0dHA6
Ly9jcmwzLmRpZ2ljZXJ0LmNvbS9EaWdpQ2VydEdsb2JhbFJvb3RDQS5jcmwwN6A1
oDOGMWh0dHA6Ly9jcmw0LmRpZ2ljZXJ0LmNvbS9EaWdpQ2VydEdsb2JhbFJvb3RD
QS5jcmwwPQYDVR0gBDYwNDAyBgRVHSAAMCowKAYIKwYBBQUHAgEWHGh0dHBzOi8v
d3d3LmRpZ2ljZXJ0LmNvbS9DUFMwHQYDVR0OBBYEFA+AYRyCMWHVLyjnjUY4tCzh
xtniMB8GA1UdIwQYMBaAFAPeUDVW0Uy7ZvCj4hsbw5eyPdFVMA0GCSqGSIb3DQEB
CwUAA4IBAQAjPt9L0jFCpbZ+QlwaRMxp0Wi0XUvgBCFsS+JtzLHgl4+mUwnNqipl
5TlPHoOlblyYoiQm5vuh7ZPHLgLGTUq/sELfeNqzqPlt/yGFUzZgTHbO7Djc1lGA
8MXW5dRNJ2Srm8c+cftIl7gzbckTB+6WohsYFfZcTEDts8Ls/3HB40f/1LkAtDdC
2iDJ6m6K7hQGrn2iWZiIqBtvLfTyyRRfJs8sjX7tN8Cp1Tm5gr8ZDOo0rwAhaPit
c+LJMto4JQtV05od8GiG7S5BNO98pVAdvzr508EIDObtHopYJeS4d60tbvVS3bR0
j6tJLp07kzQoH3jOlOrHvdPJbRzeXDLz
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
MIIDrzCCApegAwIBAgIQCDvgVpBCRrGhdWrJWZHHSjANBgkqhkiG9w0BAQUFADBh
MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMRkwFwYDVQQLExB3
d3cuZGlnaWNlcnQuY29tMSAwHgYDVQQDExdEaWdpQ2VydCBHbG9iYWwgUm9vdCBD
QTAeFw0wNjExMTAwMDAwMDBaFw0zMTExMTAwMDAwMDBaMGExCzAJBgNVBAYTAlVT
MRUwEwYDVQQKEwxEaWdpQ2VydCBJbmMxGTAXBgNVBAsTEHd3dy5kaWdpY2VydC5j
b20xIDAeBgNVBAMTF0RpZ2lDZXJ0IEdsb2JhbCBSb290IENBMIIBIjANBgkqhkiG
9w0BAQEFAAOCAQ8AMIIBCgKCAQEA4jvhEXLeqKTTo1eqUKKPC3eQyaKl7hLOllsB
CSDMAZOnTjC3U/dDxGkAV53ijSLdhwZAAIEJzs4bg7/fzTtxRuLWZscFs3YnFo97
nh6Vfe63SKMI2tavegw5BmV/Sl0fvBf4q77uKNd0f3p4mVmFaG5cIzJLv07A6Fpt
43C/dxC//AH2hdmoRBBYMql1GNXRor5H4idq9Joz+EkIYIvUX7Q6hL+hqkpMfT7P
T19sdl6gSzeRntwi5m3OFBqOasv+zbMUZBfHWymeMr/y7vrTC0LUq7dBMtoM1O/4
gdW7jVg/tRvoSSiicNoxBN33shbyTApOB6jtSj1etX+jkMOvJwIDAQABo2MwYTAO
BgNVHQ8BAf8EBAMCAYYwDwYDVR0TAQH/BAUwAwEB/zAdBgNVHQ4EFgQUA95QNVbR
TLtm8KPiGxvDl7I90VUwHwYDVR0jBBgwFoAUA95QNVbRTLtm8KPiGxvDl7I90VUw
DQYJKoZIhvcNAQEFBQADggEBAMucN6pIExIK+t1EnE9SsPTfrgT1eXkIoyQY/Esr
hMAtudXH/vTBH1jLuG2cenTnmCmrEbXjcKChzUyImZOMkXDiqw8cvpOp/2PV5Adg
06O/nVsJ8dWO41P0jmP6P6fbtGbfYmbW0W5BjfIttep3Sp+dWOIrWcBAI+0tKIJF
PnlUkiaY4IBIqDfv8NZ5YBberOgOzW6sRBc4L0na4UU+Krk2U886UAb3LujEV0ls
YSEY1QSteDwsOoBrp+uvFRTp2InBuThs4pFsiv9kuXclVzDAGySj4dzp30d8tbQk
CAUw7C29C79Fv1C5qfPrmAESrciIxpg0X40KPMbp1ZWVbd4=
-----END CERTIFICATE-----
```
* Renommer le certificat remote-mcz-it-chain.pem en remote-mcz-it-chain.crt
* Copier le dans le dossier /usr/share/ca-certificates
* Lancer la commande sudo dpkg-reconfigure ca-certificates
* Dans la fenetre, selectionner votre certificat


[py-agua-iot]: https://github.com/fredericvl/py-agua-iot "Github"
[https://www.uuidgenerator.net/version4)]: https://www.uuidgenerator.net/version4 "Génération UUID"
