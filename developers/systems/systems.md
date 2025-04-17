---
description: Les systèmes et les APIs du plugin, commment les modifier et les utiliser
---

# Systems

## [Le système de quêtes](quests.md)

## Le système d'intérèt

Dans le plugin **OpenMC** il y a un système de banques. Il y a des banques personnels (pour chaque joueur) et des banques de ville (pour chaque ville).
Les deux sortes de banques peuvent percevoir des intérèts deux fois par semaine. Le Lundi et le Jeudi à 2h du matin (heure Française).

Si une feature que vous développez à besoin de modifier le taux d'intérêt des joueurs et/ou des villes il suffit de modifier les fonctions suivants:
- Pour les joueurs, la fonction `calculatePlayerInterest` dans la classe  `BankManager`
- Pour les villes, la fonction `calculateCityInterest` dans la classe `City`
La valeur retournée est le taux d'intérêt en proportion et non en pourcentage.
