# 🚰 Téléportation

{% hint style="info" %}
Si l'argument est encadré avec "\[]" il est facultatif. Avec "<>" il est obligatoire.
{% endhint %}

## TPA

<table><thead><tr><th width="233">Commande</th><th>Description</th></tr></thead><tbody><tr><td>/tpa &#x3C;joueur></td><td>Envoyer une demande de téléportation à un joueur.</td></tr><tr><td>/tpa</td><td>Ouvrir une interface GUI listant les joueurs en ligne pour envoyer une demande de téléportation.</td></tr><tr><td>/tpaccept</td><td>Accepter la dernière demande de téléportation reçue.</td></tr><tr><td>/tpdeny</td><td>Refuser la dernière demande de téléportation reçue.</td></tr></tbody></table>

### Explication des commandes

#### **/tpa**

* **Description** : Cette commande permet d'envoyer une demande de téléportation au joueur spécifié par `<pseudo>`.
* **Usage** : Tapez `/tpa <pseudo>` pour envoyer une demande de téléportation à `<pseudo>`.
* **Exemple** : `/tpa joueur123` enverra une demande de téléportation à `joueur123`.
* **Note** : Le joueur doit accepter la demande pour que la téléportation ait lieu.

#### **/tpa**

* **Description** : Si vous tapez simplement `/tpa`, une interface graphique (GUI) s'ouvrira listant tous les joueurs en ligne.
* **Usage** : Tapez `/tpa` pour ouvrir la GUI et choisir un joueur à qui envoyer une demande de téléportation.
* **Exemple** : Tapez `/tpa`, sélectionnez `joueur123` dans la liste pour envoyer une demande de téléportation.

#### **/tpaccept**

* **Description** : Cette commande accepte la dernière demande de téléportation que vous avez reçue.
* **Usage** : Tapez `/tpaccept` pour accepter la dernière demande de téléportation.
* **Exemple** : Si `joueur123` vous a envoyé une demande, tapez `/tpaccept` pour l'accepter.
* **Note** : Le joueur qui a envoyé la demande sera téléporté à votre position.

#### **/tpdeny**

* **Description** : Cette commande refuse la dernière demande de téléportation que vous avez reçue.
* **Usage** : Tapez `/tpdeny` pour refuser la dernière demande de téléportation.
* **Exemple** : Si `joueur123` vous a envoyé une demande, tapez `/tpdeny` pour la refuser.
* **Note** : Le joueur qui a envoyé la demande sera notifié du refus.

#### Gestion des demandes de téléportation

* **Envoyer une demande** :
  * Utilisez `/tpa <pseudo>` pour demander une téléportation à un joueur spécifique.
  * Utilisez `/tpa` pour ouvrir la GUI et choisir un joueur en ligne.
* **Accepter une demande** :
  * Utilisez `/tpaccept` pour accepter la dernière demande de téléportation reçue.
  * Cela téléportera le joueur qui a envoyé la demande à votre position.
* **Refuser une demande** :
  * Utilisez `/tpdeny` pour refuser la dernière demande de téléportation reçue.
  * Le joueur qui a envoyé la demande sera notifié du refus.
