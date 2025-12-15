# Hydratation & DTO

Analysez le code pour identifier les cas où l'hydratation d'entités complètes est inutile et suggérez l'utilisation de DTOs (Data Transfer Objects) pour la lecture seule.

## Instructions
1. Repérez les actions de lecture (listes, rapports, exports) qui n'ont pas besoin de modifier les données.
2. Identifiez l'hydratation d'entités lourdes qui consomment beaucoup de mémoire inutilement.
3. Suggérez la projection directe des résultats de requête dans des DTOs (classes PHP simples ou records).
4. Vérifiez si le mode d'hydratation `ARRAY` pourrait suffire.

## Exemple de code à analyser
[Collez ici le code PHP/Symfony à analyser]

## Points à vérifier
- [ ] Hydrate-t-on des entités managées pour un simple affichage en lecture seule ?
- [ ] Pourrait-on utiliser `SELECT NEW MyDto(...)` en DQL pour mapper directement le résultat ?
- [ ] L'usage mémoire est-il optimisé en évitant l'overhead de l'UnitOfWork de Doctrine ?
- [ ] Les DTOs sont-ils bien définis (immuables, typés) ?

