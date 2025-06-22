---
icon: person-to-portal
---

# Téléportation

{% include "../.gitbook/includes/arguments.md" %}

## TPA

| Commande      | Description                                                                                             |
|---------------|---------------------------------------------------------------------------------------------------------|
| /tpa          | Ouvre une interface listant les joueurs en ligne à qui vous pouvez envoyer une demande de téléportation |
| /tpa <joueur> | Envoie une demande de téléportation au joueur indiqué                                                   |
| /tpaccept     | Accept la demande de téléportation                                                                      |
| /tpdeny       | Rejette une demande de téléportation                                                                    |
| /tpcancel     | Annule la demande de téléportation en cours                                                             |

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

#### **/tpcancel**

* **Description** : Cette commande annule la demande de téléportation en cours.
* **Usage** : Tapez `/tpcancel` pour annuler la demande de téléportation que vous avez envoyée.
* **Exemple** : Si vous avez envoyé une demande à `joueur123`, tapez `/tpcancel` pour annuler cette demande.
* **Note** : Cela ne concerne que les demandes que vous avez envoyées, pas celles que vous avez reçues.

#### Gestion des demandes de téléportation

* **Envoyer une demande** :
  * Utilisez `/tpa <pseudo>` pour demander une téléportation à un joueur spécifique.
  * Utilisez `/tpa` pour ouvrir le GUI et choisir un joueur en ligne.
* **Annuler une demande** :
  * Utilisez `/tpcancel` pour annuler la demande de téléportation que vous avez envoyée.
  * Cela annulera la demande avant qu'elle ne soit acceptée ou refusée.
* **Accepter une demande** :
  * Utilisez `/tpaccept` pour accepter la dernière demande de téléportation reçue.
  * Cela téléportera le joueur qui a envoyé la demande à votre position.
* **Refuser une demande** :
  * Utilisez `/tpdeny` pour refuser la dernière demande de téléportation reçue.
  * Le joueur qui a envoyé la demande sera notifié du refus.
