Ce plugin eedomus permet de lire les valeurs (Température, Humidité, Pression, Luminosité, Détection de mouvement, Détection d'ouverture, Button de Télécommande, Etat de communication du péripérique, Etat batterie) des capteurs configurés dans deCONZ.

## Prérequis
Un serveur deCONZ installé

## Installation
Cliquez sur "Configuration" / "Ajouter ou supprimer un périphérique" / "Store eedomus" / "Capteurs - deConz" / "Créer"

## Champs a configurer : 
* IP + Port : Adresse ip et port (facultaf si votre serveur utiliser le port 80) de votre serveur
* Clef API : l'Identification l'acces a l'API deCONZ (pour créer une nouvelle clef d'acces : Connectez vous a **Phoscon-GW** puis allez dans **Settings/Gateway/Advanced**  puis, cliquez sur **Athenticate app** )
* Identifiant du capteur : TODO


## Périphériques testés 

* Ikea - Tradfri Détecteur de mouvement
* Ikea - Tradfri Commande On/Off
* Ikea - Tradfri Variateur
* Ikea - Tradfri Télécommande
* Xiaomi - Aqara Capteur de température, humidité, pression
* Xiaomi - Aqara Détecteur d'ouverture de porte/fenêtre
* Xiaomi - Aqara Détecteur de mouvement + luminosité
* Xiaomi - Aqara Magic Cube

## Remarques 
La mise en place d'un push vers l'eedomus via un autre système (ex Domoticz, Node-RED...) connecté au webservice de deCONZ permet d'obtenir les changements d'etat en temps réèl.
