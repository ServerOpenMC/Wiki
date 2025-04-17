---
icon: clipboard
---

# Prérequis

## Le serveur Minecraft

OpenMC est un plugin [**Paper**](https://papermc.io/downloads/paper) mais vous pouvez aussi utiliser [**Purpur**](https://purpurmc.org/download/purpur) et d'autres forks.
Veuillez vous munir de la version la plus récente.

## Les dépendances de **OpenMC**

Le plugin **OpenMC** n'a pas de dépendances "durs". Autrement dit, vous pouvez l'utiliser tout seul sans autre plugin.
Cependant, beaucoup de fonctionnalités nécessitent d'autre plugins pour fonctionner. Ainsi, pour avoir toute les fonctionnalités
du plugin sur votre serveur il vous faudra quatre plugins supplémentaires (à la version la plus récente si possible):
- **LuckPerms** pour les grades et permissions
- **ItemsAdder** pour les items, blocks et menus custom (n'oubliez pas d'utiliser la [configuration ItemsAdder de **OpenMC**](https://github.com/ServerOpenMC/ItemsAdder) pour que tout fonctionne)
- **PlaceholderAPI** et **ProtocolLib** pour certaines utilités

## La base de données

Afin de stocker ses données, le plugin **OpenMC** nécessite une base de donnée compatible **MySQL**.
Il faudra vous munir des identifiants et de l'addresse de la base de données et les rensigner dans `plugins/OpenMC/config.yml` sur votre serveur.
