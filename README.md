# Airzone CE6 dans Home Assistant avec un Elfin EW11A

Guide communautaire pour raccorder une centrale Airzone CE6 a Home Assistant par Modbus TCP, au moyen d'une passerelle Elfin EW11A.

## Guide complet

[Telecharger le guide PDF](docs/guide-airzone-ce6-ew11a-home-assistant.pdf)

Le guide couvre :

- le raccordement RS-485 entre CE6 et EW11A ;
- les reglages serie et TCP de l'EW11A ;
- la configuration de l'integration AirZone dans Home Assistant ;
- le correctif local requis pour les commandes marche / arret ;
- les fonctions validees et les limites de la liaison.

## Raccordement

La reference est toujours le nom de la borne, et non la couleur du fil :

| EW11A | CE6 |
| --- | --- |
| `T` | `A` |
| `R` | `B` |
| `-` | `-` |
| `+` | `+` |

Sur le connecteur vertical du bus domotique no 4 de la CE6, la position jaune superieure reste libre. Couper l'alimentation de la climatisation avant toute intervention et ne raccorder l'EW11A qu'au bus domotique.

## A propos des couleurs de fils

Les couleurs visibles dans le guide correspondent au cable utilise pour l'installation de reference : vert pour `T -> A`, blanc pour `R -> B`, noir pour `- -> -` et rouge pour `+ -> +`. Elles ne constituent pas une norme : sur une autre installation, il faut suivre les reperes des bornes et etiqueter les fils.

## Confidentialite

Le PDF ne contient aucune adresse IP, SSID, adresse MAC, identifiant, nom de zone ni photographie non anonymisee.

## Sources

- [Integration HACS AirZone](https://github.com/gpulido/homeassistant-airzone)
- [Documentation Modbus Airzone](https://doc.airzonecloud.com/Documentation/AZ6/X6/MI_AZX6_MODBUS_MUL.pdf)
- [Support Airzone CE6](https://www.airzonecontrol.com/nf/fr/support/details-techniques/platine-centrale-airzone-du-systeme-innobus-pro6-ce6/)
