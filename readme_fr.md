Ce plugin eedomus permet de lire les valeurs (Température, Humidité, Pression, Luminosité, Détection de mouvement, Détection d'ouverture, Etat de communication du péripérique, Etat batterie) des capteurs configurés dans deCONZ.

## Prérequis

* Un serveur deCONZ installé 


## Installation
Cliquez sur "Configuration" / "Ajouter ou supprimer un périphérique" / "Store eedomus" / "Capteurs - deConz" / "Créer"

## Champs à configurer : 

![Configuration capteur deCONZ](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/deconzcap-config.png)

### IP + Port
* Adresse IP et port du serveur. Vous pouvez également cliquer sur "Recherche de serveur deCONZ" pour afficher une fenêtre avec la liste des serveurs deCONZ présent sur votre réseau.

![Recherche de serveur](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/serveur.png)

### Clef API
* Pour communiquer avec deCONZ, le système a besoin d'un clef d'accès, si vous ne la connaissez pas, vous pouvez en créer une nouvelle avec le procédure suivante : Connectez-vous a **Phoscon-GW** puis allez dans **Settings/Gateway/Advanced**  puis, cliquez sur **Authenticate app**  (le paramètre IP + Port doit préalablement être renseigné)

![Activation authentification deCONZ](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/key-authenticate.png)

* Ensuite vous pouvez cliquer sur "Cliquez ici" : Si tout se passe bien une fenêtre affichera votre nouvelle Clef API, sinon un message d'erreur sera affiché.

**Clef OK :** 

![Clef OK](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/key-ok.png)

**Erreur :**

![Clef Erreur](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/key-erreur.png)

### Identifiants

* Dans La liste ci-dessous, vous pouvez choisir le ou les types de capteur que vous allez créer.pCet identifiant correspond au périphérique que vous voulez gérer, vous pouvez en obtenir la liste en cliquant sur le lien "Liste des actionneurs" (Les paramètres IP + Port et Clef API doivent préalablement être renseignés)
![Liste des capteurs](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/liste-capteurs.png)

### Communication

* Information de l'état de la communication du capteur. [Identifiant Obligatoire]

### Batterie

* Pourcentage de la batterie

### Température

* Capteur de température.

### Humidité

* Capteur du taux d'humidité

### Pression

* Capteur de pression atmosphérique.

### Luminosité

* capteur de luminosité

### Détecteur de mouvement

* capteur de mouvement (0 - aucun mouvement, 100 - mouvement)

### Détecteur d'ouverture

* capteur d'ouveture (0 - fermé, 100 - ouvert)

### Fréquence d'actualisation

* Permet de fixer le temps de rafraichement des valeurs du périphérique (en minutes).

## Périphériques crées en fonction de votre sélection : 

![capteurs](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/capteurs.png)

## Périphériques testés 

* Ikea - Tradfri Détecteur de mouvement 
* Xiaomi - Aqara Capteur de température, humidité, pression
* Xiaomi - Aqara Détecteur d'ouverture de porte/fenêtre (+ température)
* Xiaomi - Aqara Détecteur de mouvement + luminosité (+ température)

## Remarques 

* La mise en place d'un push vers l'eedomus via un autre système (ex Domoticz, Node-RED...) connecté au webservice de deCONZ permet d'obtenir les changements d'état en temps réel.

## Sources et historique des versions

* [Sources](https://github.com/2bprog/eedomus-deconzcap-plugin)
* [Historique des versions](https://github.com/2bprog/eedomus-deconzcap-plugin/blob/master/CHANGELOG.md)

## Liens 

* <https://phoscon.de/en/conbee2/install>
* <https://dresden-elektronik.github.io/deconz-rest-doc/>
* <https://github.com/Smanar/Domoticz-deCONZ>