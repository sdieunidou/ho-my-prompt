# Complexité Cognitive & "Early Return"

Analysez le code pour réduire sa complexité cognitive (indentation excessive, logique imbriquée) en utilisant notamment la technique du "Early Return".

## Instructions
1. Identifiez les structures `if/else` imbriquées profondément (Arrow Code).
2. Suggérez l'inversion des conditions pour traiter les cas d'erreur ou d'arrêt en premier (Early Return) et désindenter le code principal.
3. Repérez les méthodes trop longues qui font trop de choses et suggérez leur découpage.
4. Simplifiez les expressions booléennes complexes.

## Exemple de code à analyser
[Collez ici le code PHP/Symfony à analyser]

## Points à vérifier
- [ ] Le code est-il plat ou ressemble-t-il à une pyramide (Pyramid of Doom) ?
- [ ] Peut-on supprimer des `else` en retournant prématurément (`return`, `throw`) ?
- [ ] La méthode tient-elle dans un écran (taille raisonnable) ?
- [ ] Les conditions complexes sont-elles extraites dans des variables ou méthodes explicites (`isValidUser()`) ?

