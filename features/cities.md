---
description: Le meilleur moyen de s'organiser entre joueurs
icon: handshake
---

# Les Villes

{% include "../.gitbook/includes/docs-unfinished.md" %}

{% include "../.gitbook/includes/arguments.md" %}

## Sommaire

- [La commande `/city`](#la-commande-city)
- [Rejoindre une ville](#rejoindre-une-ville)
- [Quitter une ville](#quitter-une-ville)
- [Gérer les membres](#gérer-les-membres)
  - [Permissions disponibles](#permissions-disponibles)
- [Types de villes](#types-de-villes)
- [Mascotte de la ville](#mascotte-de-la-ville)
- [Banque de la ville](#banque-de-la-ville)
- [Coffre de la ville](#coffre-de-la-ville)
- [Claim et Unclaim](#claim-et-unclaim)
- [Warp de la ville](#warp-de-la-ville)
- [Liste des villes](#liste-des-villes)

## La commande `/city`

Cette commande est la principale commande utilisée pour les villes. Elle permet de rejoindre, quitté, gérer les membres
et la mascotte... tout ce qu'il y a en lien avec les villes. Vous pouvez utiliser soit le menu (`/city`), soit les
commandes (`/city [sous-commande]`).

| Commande                 | Description                                                                   |
|--------------------------|-------------------------------------------------------------------------------|
| /city                    | Ouvre le menu des villes.                                                     |
| /city create \<nom>      | Crée une ville avec le nom spécifié.                                          |
| /city invite \<joueur>   | Invite un joueur à rejoindre votre ville.                                     |
| /city accept \<nom>      | Rejoint la ville qui vous a invité.                                           |
| /city deny \<nom>        | Refuse l'invitation à rejoindre une ville.                                    |
| /city leave              | Quitte la ville dans laquelle vous êtes.                                      |
| /city kick \<joueur>     | Exclut un joueur de la ville.                                                 |
| /city map                | Ouvre le menu carte.                                                          |
| /city mayor              | Ouvre le menu du maire.                                                       |
| /city rename \<nom>      | Renomme la ville.                                                             |
| /city ranks              | Ouvre le menu des grades.                                                     |
| /city info               | Affiche les informations de la ville.                                         |
| /city bank               | Ouvre la banque de la ville.                                                  |
| /city chest              | Ouvre le coffre de la ville.                                                  |
| city upgradechest        | Améliore le coffre de la ville.                                               |
| /city claim              | Claim le chunk ou vous vous trouvez pour la ville, s'il n'est pas déjà claim. |
| /city unclaim            | Unclaim le chunk ou vous vous trouvez pour la ville, s'il est déjà claim.     |
| /city list               | Affiche la liste des villes existantes.                                       |
| /city setwarp            | Définit le warp de la ville à votre position actuelle.                        |
| /city warp               | Vous téléporte au warp de la ville, s'il a été défini.                        |
| /city type               | Ouvre le menu de type de ville.                                               |
| /city transfer \<joueur> | Transfère la propriété de la ville à un autre joueur.                         |
| /city chat               | Active ou désactive le chat de la ville.                                      |
| /city perms              | Ouvre le menu des permissions de la ville.                                    |

## Créer une ville

Pour créer une ville, utilisez la commande `/city create <nom>`. Lorsque vous créez une ville, celle-ci sera automatiquement
en type PAIX, ce qui signifie qu'elle ne peut pas être attaquée et ne peut pas attaquer d'autres villes. Vous disposerez
de 300 secondes pour poser la mascotte à l'aide du bâton de mascotte, sinon la ville sera supprimée.

Vous pouvez ensuite inviter d'autres joueurs à rejoindre votre ville en utilisant la commande `/city invite <joueur>`.

{% hint style="info" %} Lorsque la ville est créée, vous serez en automatiquement défini propriétaire. Pour transférer la propriété de la ville
à un autre joueur, utilisez la commande `/city transfer <joueur>`. Le joueur doit être membre de la ville pour pouvoir
recevoir la propriété. Une fois que vous avez transféré la propriété, vous ne pourrez plus gérer la ville à moins
d'être réinvité par le nouveau propriétaire. {% endhint %}

## Rejoindre une ville

Pour rejoindre une ville, vous devez d'abord être invité par un joueur qui en est le maire ou un membre.
Une fois que vous avez reçu l'invitation, vous pouvez accepter en utilisant la commande `/city accept <nom>` ou en
cliquant sur l'invitation dans le chat.

## Quitter une ville

Pour quitter une ville, utilisez la commande `/city leave`. Vous serez alors retiré de la ville et ne pourrez plus
interagir avec ses fonctionnalités. Si vous êtes le propriétaire, vous devrez transférer la propriété de la ville à un
autre joueur avant de pouvoir quitter.

## Gérer les membres

Pour gérer les membres de votre ville, vous pouvez utiliser la commande `/city ranks` ou `/city perms` pour définir des
rôles et des permissions.

### Permissions disponibles

| Permission                     | Description                                                                   |
|--------------------------------|-------------------------------------------------------------------------------|
| Inviter                        | Permet d'inviter des joueurs à rejoindre la ville.                            |
| Expulser                       | Permet d'exclure des joueurs de la ville.                                     |
| Placer des blocks              | Permet de placer des blocs dans la ville.                                     |
| Casser des blocks              | Permet de casser des blocs dans la ville.                                     |
| Ouvrir les coffres             | Permet d'ouvrir les coffres dans la ville (Shulkers Boxes et EC non compris). |
| Interagir                      | Permet d'interagir avec les blocs dans la ville (hors coffres et barils).     |
| Claim                          | Permet de claim/unclaim des chunks pour la ville.                             |
| Voir les claims                | Permet de voir les chunks claims par la ville.                                |
| Renommer                       | Permet de renommer la ville.                                                  |
| Déposer de l'argent            | Permet de déposer de l'argent dans la banque de la ville.                     |
| Voir l'argent                  | Permet de voir le montant d'argent dans la banque de la ville.                |
| Retirer de l'argent            | Permet de retirer de l'argent de la banque de la ville.                       |
| Permissions                    | Permet de gérer les permissions/grades des membres de la ville.               |
| Coffre de ville                | Permet d'ouvrir le coffre de la ville.                                        |
| Améliorer le coffre            | Permet d'améliorer le coffre de la ville.                                     |
| Changer le type de ville       | Permet de changer le type de la ville.                                        |
| Déplacer la mascotte           | Permet de déplacer la mascotte de la ville.                                   |
| Changer le skin de la mascotte | Permet de changer le skin de la mascotte.                                     |
| Améliorer la mascotte          | Permet d'améliorer la mascotte de la ville.                                   |
| Soigner la mascotte            | Permet de soigner la mascotte de la ville.                                    |
| Lancer des guerres             | Permet de lancer des guerres contre d'autres villes.                          |

## Types de villes

Il existe plusieurs types de villes, PAIX et GUERRE. Une ville de type PAIX ne peut pas être attaquée et ne peut pas
attaquer d'autres villes, tandis qu'une ville de type GUERRE peut être attaquée et attaquer d'autres villes. Vous pouvez
changer le type de votre ville en utilisant la commande `/city type`.

## Mascotte de la ville

La mascotte est posée lors de la création de la ville et en est le cœur. Elle peut être déplacée et améliorée afin d'avoir
plus de PV. Si vous êtes en type GUERRE, la mascotte peut être attaquée et détruite par les autres villes. Je vous conseille
de bien la protéger et de la soigner si sa vie n'est pas au maximum.

## Banque de la ville

La banque de la ville est un coffre qui permet de stocker de l'argent pour la ville. Vous pouvez y déposer de l'argent
pour éviter de le perdre en cas de mort (voir [ici]()). Vous pouvez y accéder en utilisant la commande `/city bank`.

## Coffre de la ville

Le coffre de la ville permet de stocker des items pour la ville. Le coffre est accessible par tous les membres de la ville
et peut être amélioré pour augmenter sa capacité de stockage. Vous pouvez y accéder en utilisant la commande `/city chest`.

{% hint style="info" %} Vous ne pouvez aps accéder au coffre de ville si quelqu'un d'autre y est. {% endhint %}

## Claim et Unclaim

Pour claim un chunk pour votre ville, vous devez vous trouver dans le chunk que vous souhaitez claim — pourvu qu'il ne
soit pas déjà claim — et utiliser la commande `/city claim`. Cela protégera le chunk contre les autres joueurs et
permettra à votre ville d'y construire en toute sécurité.

Pour unclaim un chunk, vous devez vous trouver dans le chunk que vous souhaitez unclaim et utiliser la commande
`/city unclaim`. Cela retirera la protection du chunk et permettra à d'autres joueurs de l'utiliser.

{% hint style="info" %} Vous pouvez aussi passer par le menu map (`/city map`) pour claim ou unclaim des chunks. Il vous suffit de
cliquer sur le chunk que vous souhaitez claim ou unclaim. {% endhint %}

## Warp de la ville

Pour définir un warp pour votre ville, vous devez être le propriétaire de la ville et vous trouver à l'endroit où vous
souhaitez que le warp soit défini. Utilisez la commande `/city setwarp` pour définir le warp. Les joueurs de la ville 
pourront ensuite se téléporter au warp de la ville avec la commande `/city warp`.

## Liste des villes

Pour afficher la liste des villes existantes, utilisez la commande `/city list`. Cela vous montrera les villes disponibles
et vous permettra de voir dans quelle ville se trouvent vos amis. Vous pouvez cliquer sur la ville pour en savoir plus.

Si vous préférez le chat, vous pouvez voir les informations de chaque ville en utilisant la commande `/city info <nom>`.