Ce plugin eedomus permet de lire les valeurs (Temp�rature, Humidit�, Pression, Luminosit�, D�tection de mouvement, D�tection d'ouverture, Etat de communication du p�rip�rique, Etat batterie) des capteurs configur�s dans deCONZ.

## Pr�requis

* Un serveur deCONZ install� 


## Installation
Cliquez sur "Configuration" / "Ajouter ou supprimer un p�riph�rique" / "Store eedomus" / "Capteurs - deConz" / "Cr�er"

## Champs � configurer : 

![Configuration capteur deCONZ](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/deconzcap-config.png)

### IP + Port
* Adresse IP et port du serveur. Vous pouvez �galement cliquer sur "Recherche de serveur deCONZ" pour afficher une fen�tre avec la liste des serveurs deCONZ pr�sent sur votre r�seau.

![Recherche de serveur](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/serveur.png)

### Clef API
* Pour communiquer avec deCONZ, le syst�me a besoin d'un clef d'acc�s, si vous ne la connaissez pas, vous pouvez en cr�er une nouvelle avec le proc�dure suivante : Connectez-vous a **Phoscon-GW** puis allez dans **Settings/Gateway/Advanced**  puis, cliquez sur **Authenticate app**  (le param�tre IP + Port doit pr�alablement �tre renseign�)

![Activation authentification deCONZ](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/key-authenticate.png)

* Ensuite vous pouvez cliquer sur "Cliquez ici" : Si tout se passe bien une fen�tre affichera votre nouvelle Clef API, sinon un message d'erreur sera affich�.

**Clef OK :** 

![Clef OK](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/key-ok.png)

**Erreur :**

![Clef Erreur](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/key-erreur.png)

### Identifiants

* Dans La liste ci-dessous, vous pouvez choisir le ou les types de capteur que vous allez cr�er.pCet identifiant correspond au p�riph�rique que vous voulez g�rer, vous pouvez en obtenir la liste en cliquant sur le lien "Liste des actionneurs" (Les param�tres IP + Port et Clef API doivent pr�alablement �tre renseign�s)
![Liste des capteurs](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/liste-capteurs.png)

### Communication

* Information de l'�tat de la communication du capteur. [Identifiant Obligatoire]

### Batterie

* Pourcentage de la batterie

### Temp�rature

* Capteur de temp�rature.

### Humidit�

* Capteur du taux d'humidit�

### Pression

* Capteur de pression atmosph�rique.

### Luminosit�

* capteur de luminosit�

### D�tecteur de mouvement

* capteur de mouvement (0 - aucun mouvement, 100 - mouvement)

### D�tecteur d'ouverture

* capteur d'ouveture (0 - ferm�, 100 - ouvert)

### Fr�quence d'actualisation

* Permet de fixer le temps de rafraichement des valeurs du p�riph�rique (en minutes).

## P�riph�riques cr�es en fonction de votre s�lection : 

![capteurs](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/capteurs.png)

## P�riph�riques test�s 

* Ikea - Tradfri D�tecteur de mouvement 
* Xiaomi - Aqara Capteur de temp�rature, humidit�, pression
* Xiaomi - Aqara D�tecteur d'ouverture de porte/fen�tre (+ temp�rature)
* Xiaomi - Aqara D�tecteur de mouvement + luminosit� (+ temp�rature)

## Remarques 

* La mise en place d'un push vers l'eedomus via un autre syst�me (ex Domoticz, Node-RED...) connect� au webservice de deCONZ permet d'obtenir les changements d'�tat en temps r�el.

## Sources et historique des versions

* [Sources](https://github.com/2bprog/eedomus-deconzcap-plugin)
* [Historique des versions](https://github.com/2bprog/eedomus-deconzcap-plugin/blob/master/CHANGELOG.md)

## Liens 

* <https://phoscon.de/en/conbee2/install>
* <https://dresden-elektronik.github.io/deconz-rest-doc/>
* <https://github.com/Smanar/Domoticz-deCONZ>