# Airzone CE6 dans Home Assistant avec un Elfin EW11

Guide communautaire pour raccorder une centrale Airzone CE6 à Home Assistant par Modbus TCP, au moyen d'une passerelle Elfin EW11 / EW11A et de son adaptateur RJ45 vers bornier à vis.

## Guide complet

[Télécharger le guide PDF](guide-airzone-ce6-ew11a-home-assistant.pdf)

Le guide couvre :

- le raccordement RS-485 entre CE6 et EW11A ;
- les réglages série et TCP de l'EW11A ;
- la configuration de l'intégration AirZone dans Home Assistant ;
- le correctif local requis pour les commandes marche / arrêt ;
- les fonctions validées et les limites de la liaison.

## Matériel nécessaire

- une passerelle **Elfin EW11 / EW11A** ;
- un **adaptateur RJ45 mâle vers bornier à vis 4 pôles** ;
- quatre fils pour le raccordement entre l'adaptateur et la centrale CE6.

L'adaptateur se branche au port RJ45 RS-485 de l'Elfin. Malgré sa forme, il ne constitue pas une liaison Ethernet vers le routeur : ce connecteur transporte le RS-485 et l'alimentation de l'Elfin.

## Raccordement

La référence est toujours le nom de la borne, et non la couleur du fil :

| EW11 | CE6 |
| --- | --- |
| `T` | `A` |
| `R` | `B` |
| `-` | `-` |
| `+` | `+` |

Sur le connecteur vertical du bus domotique n° 4 de la CE6, la position jaune supérieure reste libre. Couper l'alimentation de la climatisation avant toute intervention et ne raccorder l'EW11A qu'au bus domotique.

## À propos des couleurs de fils

Les couleurs visibles dans le guide correspondent au câble utilisé pour l'installation de référence : vert pour `T -> A`, blanc pour `R -> B`, noir pour `- -> -` et rouge pour `+ -> +`. Elles ne constituent pas une norme : sur une autre installation, il faut suivre les repères des bornes et étiqueter les fils.

## Confidentialite

Le PDF ne contient aucune adresse IP, SSID, adresse MAC, identifiant, nom de zone ni photographie non anonymisée.

## Sources

- [Intégration HACS AirZone](https://github.com/gpulido/homeassistant-airzone)
- [Documentation Modbus Airzone](https://doc.airzonecloud.com/Documentation/AZ6/X6/MI_AZX6_MODBUS_MUL.pdf)
- [Support Airzone CE6](https://www.airzonecontrol.com/nf/fr/support/details-techniques/platine-centrale-airzone-du-systeme-innobus-pro6-ce6/)
