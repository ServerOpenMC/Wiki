# Utiliser le plugin sois-même

{% include "../.gitbook/includes/docs-unfinished.md" %}

{% hint style="warning" %}
En lisant ce guide, nous présupposons que vous savez créé un serveur Minecraft avec des plugins.
{% endhint %}

## Etape 1 : Récupérer un `.jar` du plugin

Nous n'avons pour l'instant pas de distribution de fichiers du plugin. Il vous faudra donc [compiler vous-même le plugin](contribute/contribute/build.md).

## Etape 2 : Le serveur **Minecraft**

OpenMC est un plugin [**Paper**](https://papermc.io/downloads/paper) mais vous pouvez aussi utiliser [**Purpur**](https://purpurmc.org/download/purpur) et d'autres forks.
Veuillez vous munir de la version la plus récente.

## Etape 3 : Les dépendances de **OpenMC**

Le plugin **OpenMC** n'a pas de dépendances "durs". Autrement dit, vous pouvez l'utiliser tout seul sans autre plugin.
Cependant, beaucoup de fonctionnalités nécessitent d'autre plugins pour fonctionner. Ainsi, pour avoir toute les fonctionnalités
du plugin sur votre serveur il vous faudra quatre plugins supplémentaires (à la version la plus récente si possible):
- **LuckPerms** pour les grades et permissions
- **ItemsAdder** pour les items, blocks et menus custom (n'oubliez pas d'utiliser la [configuration ItemsAdder de **OpenMC**](https://github.com/ServerOpenMC/ItemsAdder) pour que tout fonctionne)
- **PlaceholderAPI** et **ProtocolLib** pour certaines utilités

## Etape 4 : La base de données

Afin de stocker ses données, le plugin **OpenMC** nécessite une base de donnée compatible **MySQL**.
Il faudra vous munir des identifiants et de l'addresse de la base de données et les rensigner dans `plugins/OpenMC/config.yml`

## Etape 5 : Jouez !

Vous avez maintenant un serveur avec le plugin **OpenMC**. Amusez-vous bien!
