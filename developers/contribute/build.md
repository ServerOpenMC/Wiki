---
icon: brick-wall
---

# Build le plugin

## Dans **IntelliJ**

* A droite, dans **Gradle** (l'éléphant) :
  * Ouvrez `Tasks`, puis le sous-dossier `shadow`
  * Double-cliquez sur `shadowJar`
* La console s'ouvrira en bas, si il y a une erreur, elle sera affiché ici, voici à quoi ressemble un build réussi
* Une fois build sans erreur, le plugin sera dans `builds` **avec un S**

## En ligne de commande

* Sur **Windows**
  * `.\gradlew.bat shadowJar`
* Sur **Unix-like** (Linux/MacOS/...)
  * `./gradlew shadowJar`
* Une fois build sans erreur, le plugin sera dans `builds` **avec un S**
