Ce plugin eedomus permet de lire les valeurs (Temp�rature, Humidit�, Pression, Luminosit�, D�tection de mouvement, D�tection d'ouverture, Button de T�l�commande, Etat de communication du p�rip�rique, Etat batterie) des capteurs configur�s dans deCONZ.

## Pr�requis
Un serveur deCONZ install�

## Installation
Cliquez sur "Configuration" / "Ajouter ou supprimer un p�riph�rique" / "Store eedomus" / "Capteurs - deConz" / "Cr�er"

## Champs a configurer : 
* IP + Port : Adresse ip et port (facultaf si votre serveur utiliser le port 80) de votre serveur
* Clef API : l'Identification l'acces a l'API deCONZ (pour cr�er une nouvelle clef d'acces : Connectez vous a **Phoscon-GW** puis allez dans **Settings/Gateway/Advanced**  puis, cliquez sur **Athenticate app** )
* Identifiant du capteur : TODO


## P�riph�riques test�s 

* Ikea - Tradfri D�tecteur de mouvement
* Ikea - Tradfri Commande On/Off
* Ikea - Tradfri Variateur
* Ikea - Tradfri T�l�commande
* Xiaomi - Aqara Capteur de temp�rature, humidit�, pression
* Xiaomi - Aqara D�tecteur d'ouverture de porte/fen�tre
* Xiaomi - Aqara D�tecteur de mouvement + luminosit�
* Xiaomi - Aqara Magic Cube

## Remarques 
La mise en place d'un push vers l'eedomus via un autre syst�me (ex Domoticz, Node-RED...) connect� au webservice de deCONZ permet d'obtenir les changements d'etat en temps r��l.
