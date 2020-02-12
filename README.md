Ce plugin eedomus permet de lire les valeurs des capteurs configurés dans deCONZ (Application de dresden elektronik qui gère les clefs zigbee ConBee, ConBee II et RaspBee). Si vous utiliser Domoticz, vous pouvez utiliser le plugin [Domoticz - Events](https://forum.eedomus.com/viewtopic.php?f=50&t=9274) pour envoyer les changements de valeur dans l'Eedomus. Il prends en charge les élements suivants : 

* Température
* Humidité
* Pression
* Luminosité
* Détection de mouvement
* Détection d'ouverture
* Etat de communication du périphérique
* Etat batterie
* Télécommande
* Tête Thermostatique
* Elément personnalisé

## Prérequis

* Un serveur deCONZ installé 

## Installation
Cliquez sur "Configuration" / "Ajouter ou supprimer un périphérique" / "Store eedomus" / "Capteurs - deConz" / "Créer"

![Configuration capteur deCONZ](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/deconzcap-config1-0.0.4.png)

## Champs à configurer : 

![Configuration capteur deCONZ](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/deconzcap-config2-0.0.4.png)

### IP + Port
* Adresse IP et port du serveur. Vous pouvez également cliquer sur "Recherche de serveur deCONZ" pour afficher une fenêtre avec la liste des serveurs deCONZ présent sur votre réseau.
* Vous pouvez également enregistrer l'ip et le port puis les charger lors d'une utilisation ultérieure.

![Recherche de serveur](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/serveur.png)

### Clef API
* Pour communiquer avec deCONZ, le système a besoin d'un clef d'accès, si vous ne la connaissez pas, vous pouvez en créer une nouvelle avec le procédure suivante : Connectez-vous a **Phoscon-GW** puis allez dans **Settings/Gateway/Advanced**  puis, cliquez sur **Authenticate app**  (le paramètre IP + Port doit préalablement être renseigné)
* Vous pouvez également enregistrer la clef API puis la charger lors d'une utilisation ultérieure.

![Activation authentification deCONZ](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/key-authenticate.png)

* Ensuite vous pouvez cliquer sur "Cliquez ici" : Si tout se passe bien une fenêtre affichera votre nouvelle Clef API, sinon un message d'erreur sera affiché.

**Clef OK :** 

![Clef OK](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/key-ok.png)

**Erreur :**

![Clef Erreur](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/key-erreur.png)

### Identifiants

![Configuration capteur deCONZ](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/deconzcap-config3-0.0.4.png)

* Dans les différentes zones de saisie, vous pouvez saisir des identifiants différents en fonction du type de capteur (0 => pas de création du capteur). Ils seront au final associés au capteur de communication. Vous pouvez également obtenir la liste des capteurs en cliquant sur "Liste des capteurs". Le champ "type" affiche les capteurs disponibles associé au périphérique. (Les paramètres IP + Port et Clef API doivent préalablement être renseignés)

![Liste des capteurs](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/liste-capteurs.png)

* **Communication** : Information de l'état de la communication du capteur. [Identifiant Obligatoire]
* **Batterie** : Pourcentage de la batterie.
* **Température** :  Capteur de température.
* **Humidité** :  Capteur du taux d'humidité.
* **Pression** :  Capteur de pression atmosphérique.
* **Luminosité** :  Capteur de luminosité.
* **Détecteur de mouvement** :  Capteur de mouvement (0 - aucun mouvement, 100 - mouvement).
* **Détecteur d'ouverture** :  Capteur d'ouverture (0 - fermé, 100 - ouvert).
* **Télélecommande (1)** : Boutons de télécommande (fonctionne seulement avec le plugin )
* **Tête Thermostatique** : Consigne de température, Ouverture de la vanne, mode du thermostat
* **Personnalisé** : en utilisant un xpath (exemple pour un detecteur de mouvement Ikea : //dark)

* **Fréquence d'actualisation** :  Permet de fixer le temps de rafraichement des valeurs du périphérique (en minutes).

## Périphériques crées en fonction de votre sélection : 

![capteurs](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/capteurs-0.0.4.png)

## Périphériques testés 

* Ematronic Spirit - Tête Thermostatique
* Ikea - Tradfri Commande On/Off
* Ikea - Tradfri Détecteur de mouvement 
* Ikea - Tradfri Télécommande
* Ikea - Tradfri Variateur
* Xiaomi - Aqara Capteur de température, humidité, pression
* Xiaomi - Aqara Détecteur d'ouverture de porte/fenêtre (+ température)
* Xiaomi - Aqara Détecteur de mouvement + luminosité (+ température)
* Xiaomi - Interrupteur 2 boutons WXKG02LM Rev.2
* Xiaomi - Mi Magic Cube
* Xiaomi - Smart Switch WXKG11LM Rev.2

## Remarques 

* La mise en place d'un push vers l'eedomus via un autre système (ex Domoticz, Node-RED...) connecté au webservice de deCONZ permet d'obtenir les changements d'état en temps réel.
* (1)
* Si vous utiliser Domoticz, vous pouvez utiliser le plugin [Domoticz - Events](https://forum.eedomus.com/viewtopic.php?f=50&t=9274) pour envoyer les changements de valeur dans l'Eedomus.


## Sources et historique des versions

* [Sources](https://github.com/2bprog/eedomus-deconzcap-plugin)
* [Historique des versions](https://github.com/2bprog/eedomus-deconzcap-plugin/blob/master/CHANGELOG.md)

## Liens 

* [Plugin deCONZ- Capteurs](https://forum.eedomus.com/viewtopic.php?f=50&t=9238)
* [Plugin deCONZ- Actionneurs](https://forum.eedomus.com/viewtopic.php?f=50&t=9236)
* [Plugin Domoticz - Events](https://forum.eedomus.com/viewtopic.php?f=50&t=9274)
* <https://phoscon.de/en/conbee2/install>
* <https://dresden-elektronik.github.io/deconz-rest-doc/>
* <https://github.com/Smanar/Domoticz-deCONZ>