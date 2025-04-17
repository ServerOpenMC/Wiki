---
description: Contribuer au plugin opensource OpenMC
---

# Contribuer au plugin

{% include "../../.gitbook/includes/docs-unfinished.md" %}

## [Prérequis](prerequisits.md)

## Impératif

Avant faire une contribution, vous êtes OBLIGÉ de lire&#x20;

{% embed url="https://github.com/ServerOpenMC/PluginV2/blob/master/CONTRIBUTING.md" fullWidth="false" %}

{% embed url="https://github.com/ServerOpenMC/PluginV2/blob/master/CODE_OF_CONDUCT.md" %}

Sinon votre pull request sera refusée

## 🧱 Comment build son plugin

### Dans `IntelliJ`

* A droite, dans Gradle (l'éléphant) :
  * Ouvrez `Tasks`, puis le sous-dossier `shadow`
  * Double-cliquez sur `shadowJar`
* La console s'ouvrira en bas, si il y a une erreur, elle sera affiché ici, voici à quoi ressemble un build réussi
* Une fois build sans erreur, le plugin sera dans `builds` **avec un S**

### En ligne de commande

* Sur Windows
  * `.\gradlew.bat shadowJar`
* Sur Unix-like (Linux/MacOS/...)
  * `./gradlew shadowJar`
* Une fois build sans erreur, le plugin sera dans `builds` **avec un S**

## 📤 Avant une pull request

* Le plugin se compile sur votre machine
* Le plugin se lance et fonctionne sans erreur sur votre machine
* Il n'y ai aucun conflits
