# La base de donnés

## Table des matières
- [L'ORM](#lorm)
- [Integrer un manager avec **ORMLite**](#integrer-un-manager-avec-ormlite)
  - [Créer un objet a stocké](#créer-un-objet-a-stocké)
  - [Intiliaser la table et le `DAO`](#initialiser-la-table-et-le-dao)
  - [Utiliser le `DAO`](#utiliser-le-dao)
- [Bonnes pratiques](#bonnes-pratiques)

## L'ORM

Le plugin **OpenMC** utilise l'ORM [**ORMLite**](https://ormlite.com/) pour communiquer
plus facilement avec la base de donnés (dans notre cas **MySQL**). Un ORM c'est
un **Object Relational Mapping**, soit un système qui permet de relier les tables
et colonnes d'un schéma de DB traditionnel avec des objets **Java**. Ce guide vous
expliqueras les bases d'**ORMLite** et son intégration dans le plugin. Si vous
voulez plus d'informations ou juste des docs plus détaillés du système rendez-vous
sur l'excellente documentation officielle de
[**ORMLite**](https://ormlite.com/javadoc/ormlite-core/doc-files/ormlite.html).

## Integrer un manager avec **ORMLite**

Nous prendrons l'exemple des maires pour ce guide (soit les classes `Mayor`
et `MayorManager`).

### Créer un objet a stocké

Avec **ORMLite** chaque table de la base de donnés est représenté par un objet
**Java**.

Dans un premier temps, pour qu'un objet puisse être utiliser par **ORMLite**
il lui faut un constructeur sans arguments avec une visibilté au niveau du package.

```java
class Mayor {
    Mayor() {
        // required for ORMLite
    }
}
```

Ensuite, il faut que la class et ses membres soient annotés par les interface
`@DatabaseTable` et `@DatabaseField`.

L'interface `@DatabaseTable` permet de configurer l'aspect général de la table.
Il doit être placé sur la déclaration de la classe. Vous pouvez utiliser le
paramètres `tableName` pour changer le nom de la table. Par défaut c'est le nom
de la classe.

```java
@DatabaseTable(tableName = "mayors")
class Mayor {
    Mayor() {
        // required for ORMLite
    }
}
```

L'interface `@DatabaseField` permet de configurer les colonnes de la table. Pour
qu'ils soient détectés, les membres doivent être annotés par cette interface. Si
un membre n'est pas annotté, il ne seras pas sauvegarder dans la DB.
Quelque paramètres utiles:

- `columnName`: Le nom de la colonne. Le nom du membre par défaut.
- `id`: Si ce membre est l'ID de la table. Peut être utiliser qu'une seule fois par table.
- `generatedId`: Si l'ID doit être généré automatiquement.
- `unique`: Si ce membre doit être unique.
- `canBeNull`: Si ce membre peut être null. Utile pour le stockage d'`UUID`.
- `defaultValue`: La valeur par défaut de la colonne. Doit être un `String` même si la variable a un type différent (exemple: `defaultValue = "0"`)

```java
@DatabaseTable(tableName = "mayors")
public class Mayor {
    @DatabaseField(id = true)
    private String city;
    @DatabaseField
    private UUID uuid;
    @DatabaseField(canBeNull = false)
    private String name;
    @DatabaseField
    private String mayorColor;
    @DatabaseField(canBeNull = false)
    private int idPerk1;
    @DatabaseField(canBeNull = false)
    private int idPerk2;
    @DatabaseField(canBeNull = false)
    private int idPerk3;
    @DatabaseField(canBeNull = false, columnName = "election_type")
    private String electionType;

    Mayor() {
        // required for ORMLite
    }
}
```

### Initialiser la table et le `DAO`

Par convention dans la codebase **OpenMC**, le base de donnés est initialisée
par le `DatabaseManager` a travers une fonction `init_db`. Cette fonction
doit créer la/les table(s) si elle(s) n'existe(nt) pas et initialiser le
`DAO`. Le `Data Access Object` est l'objet qui permet d'intéragir avec la table
associée de la DB.

Le `Dao` doit être initialiser avec le type a stocké dans la DB et le type
du membre annoter avec `id = true`. Si le type n'a pas d'ID, un type quelquonque
peut être utiliser.

{% hint style="warning" %}
Attention, si vous utilisés le `Dao` dans la fonction `init_db` cela risque de
bloquer les unit tests (je pense que c'est un problème avec les driver `h2` mais
        je ne suis pas sûre).
{% endhint %}

```java
private static Dao<Mayor, String> mayorsDao;

public static void init_db(ConnectionSource connectionSource) throws SQLException {
    TableUtils.createTableIfNotExists(connectionSource, Mayor.class);
    mayorsDao = DaoManager.createDao(connectionSource, Mayor.class);
}
```

### Utiliser le `DAO`

Maitenant que vous avez votre table et votre `DAO`, vous pouvez commencé à
manipuler la base de donnés. Voici quelque fonctions utiles:

- `queryForAll`: Retourne une liste du type stocké. Ex: `List<Mayor>`
- `queryForId`: Retourne l'élément avec l'ID donnée.
- `create`: Sauvegarde l'objet ou la liste d'objets donnés.
- `update`: Met à jour l'objet donné (fonctionne uniquement si le type a un `id = true`).
- `createOrUpdate`: Créé l'objet si il n'existe pas et le met à jour s'il existe (fonctionne uniquement si le type a un `id = true`).
- `delete`: Supprime l'objet donné.

Vous pouvez aussi créé des requêtes plus complexes à l'aide du `QueryBuilder`
et du `DeleteBuilder`.

```java
DeleteBuilder<Mayor, String> mayorsDelete = mayorsDao.deleteBuilder();
mayorsDelete.where().eq("city", city.getUUID());
mayorsDao.delete(mayorsDelete.prepare());
```

Pour plus d'informations rendez-vous sur la
[documentation officielle](https://ormlite.com/javadoc/ormlite-core/doc-files/ormlite.html#Statement-Builder)

## Bonnes pratiques

1. Garder le `Dao` en `private` sans `@Getter` afin de garder localiser les interactions avec la DB.
2. Mettre les operations de sauvegarde dans des fonction asynchrones pour de meilleurs performances.

Rédigé par [PiquelChips](https://github.com/PiquelChips)
