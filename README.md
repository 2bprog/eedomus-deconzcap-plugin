Ce plugin eedomus permet de lire les valeurs des capteurs configur�s dans deCONZ (Application de dresden elektronik qui g�re les clefs zigbee ConBee, ConBee II et RaspBee). Si vous utiliser Domoticz, vous pouvez utiliser le plugin [Domoticz - Events](https://forum.eedomus.com/viewtopic.php?f=50&t=9274) pour envoyer les changements de valeur dans l'Eedomus. Il prends en charge les �lements suivants : 

* Temp�rature
* Humidit�
* Pression
* Luminosit�
* D�tection de mouvement
* D�tection d'ouverture
* Etat de communication du p�riph�rique
* Etat batterie
* T�l�commande
* T�te Thermostatique
* El�ment personnalis�

## Pr�requis

* Un serveur deCONZ install� 

## Installation
Cliquez sur "Configuration" / "Ajouter ou supprimer un p�riph�rique" / "Store eedomus" / "Capteurs - deConz" / "Cr�er"

![Configuration capteur deCONZ](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/deconzcap-config1-0.0.3.png)

## Champs � configurer : 

![Configuration capteur deCONZ](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/deconzcap-config2-0.0.3.png)

### IP + Port
* Adresse IP et port du serveur. Vous pouvez �galement enregistrer l'ip et le port puis les charger lors d'une utilisation ult�rieure.
* Vous pouvez cliquer sur "Recherche de serveur deCONZ" pour afficher une fen�tre avec la liste des serveurs deCONZ pr�sent sur votre r�seau.

![Recherche de serveur](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/serveur.png)

### Clef API
* Pour communiquer avec deCONZ, le syst�me a besoin d'un clef d'acc�s, si vous ne la connaissez pas, vous pouvez en cr�er une nouvelle avec le proc�dure suivante : Connectez-vous a **Phoscon-GW** puis allez dans **Settings/Gateway/Advanced**  puis, cliquez sur **Authenticate app**  (le param�tre IP + Port doit pr�alablement �tre renseign�)
* Vous pouvez �galement enregistrer la clef API puis la charger lors d'une utilisation ult�rieure.

![Activation authentification deCONZ](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/key-authenticate.png)

* Ensuite vous pouvez cliquer sur "Cliquez ici" : Si tout se passe bien une fen�tre affichera votre nouvelle Clef API, sinon un message d'erreur sera affich�.

**Clef OK :** 

![Clef OK](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/key-ok.png)

**Erreur :**

![Clef Erreur](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/key-erreur.png)

### Identifiants

![Configuration capteur deCONZ](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/deconzcap-config3-0.0.3.png)

* Dans les diff�rentes zones de saisie, vous pouvez saisir des identifiants diff�rents en fonction du type de capteur (0 => pas de cr�ation du capteur). Ils seront au final associ�s au capteur de communication. Vous pouvez �galement obtenir la liste des capteurs en cliquant sur "Liste des capteurs". Le champ "type" affiche les capteurs disponibles associ� au p�riph�rique. (Les param�tres IP + Port et Clef API doivent pr�alablement �tre renseign�s)

![Liste des capteurs](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/liste-capteurs-0.0.3.png)

* **Communication** : Information de l'�tat de la communication du capteur. [Identifiant Obligatoire]
* **Batterie** : Pourcentage de la batterie.
* **Temp�rature** :  Capteur de temp�rature.
* **Humidit�** :  Capteur du taux d'humidit�.
* **Pression** :  Capteur de pression atmosph�rique.
* **Luminosit�** :  Capteur de luminosit�.
* **D�tecteur de mouvement** :  Capteur de mouvement (0 - aucun mouvement, 100 - mouvement).
* **D�tecteur d'ouverture** :  Capteur d'ouverture (0 - ferm�, 100 - ouvert).
* **T�l�lecommande (1)** : Boutons de t�l�commande (fonctionne seulement avec le plugin [Domoticz - Events](https://forum.eedomus.com/viewtopic.php?f=50&t=9274))
* **T�te Thermostatique** : Consigne de temp�rature, Ouverture de la vanne, mode du thermostat
* **Personnalis�** : en utilisant un xpath (exemple pour un detecteur de mouvement Ikea : //dark)
* **Fr�quence d'actualisation** :  Permet de fixer le temps de rafraichement des valeurs du p�riph�rique (en minutes).

## P�riph�riques cr�es en fonction de votre s�lection : 

![capteurs](https://raw.githubusercontent.com/2bprog/eedomus-deconzcap-plugin/master/doc/capteurs-0.0.3.png)

## P�riph�riques test�s 

* Ematronic Spirit - T�te Thermostatique
* Ikea - Tradfri Commande On/Off
* Ikea - Tradfri D�tecteur de mouvement 
* Ikea - Tradfri T�l�commande
* Ikea - Tradfri Variateur
* Xiaomi - Aqara Capteur de temp�rature, humidit�, pression
* Xiaomi - Aqara D�tecteur d'ouverture de porte/fen�tre (+ temp�rature)
* Xiaomi - Aqara D�tecteur de mouvement + luminosit� (+ temp�rature)
* Xiaomi - Interrupteur 2 boutons WXKG02LM Rev.2
* Xiaomi - Mi Magic Cube
* Xiaomi - Smart Switch WXKG11LM Rev.2

## Remarques 

* La mise en place d'un push vers l'eedomus via un autre syst�me (ex Domoticz, Node-RED...) connect� au webservice de deCONZ permet d'obtenir les changements d'�tat en temps r�el.
* Si vous utiliser Domoticz, vous pouvez utiliser le plugin [Domoticz - Events](https://forum.eedomus.com/viewtopic.php?f=50&t=9274) pour envoyer les changements de valeur dans l'Eedomus.


## Sources et historique des versions

* [Sources](https://github.com/2bprog/eedomus-deconzcap-plugin)
* [Historique des versions](https://github.com/2bprog/eedomus-deconzcap-plugin/blob/master/CHANGELOG.md)

## Liens 

* [Forum deCONZ- Capteurs](https://forum.eedomus.com/viewtopic.php?f=50&t=9238)
* [Forum deCONZ- Actionneurs](https://forum.eedomus.com/viewtopic.php?f=50&t=9236)
* [Forum Domoticz - Events](https://forum.eedomus.com/viewtopic.php?f=50&t=9274)
* <https://phoscon.de/en/conbee2/install>
* <https://dresden-elektronik.github.io/deconz-rest-doc/>
* <https://github.com/Smanar/Domoticz-deCONZ>