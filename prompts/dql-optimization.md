# Optimisation des Requêtes DQL/QueryBuilder

Analysez les requêtes Doctrine (DQL ou QueryBuilder) pour optimiser leur performance, leur lisibilité et l'usage des index.

## Instructions
1. Vérifiez que seules les données nécessaires sont sélectionnées (`select('p.id, p.name')` vs `select('p')`).
2. Assurez-vous que les jointures sont pertinentes et utilisent `leftJoin` ou `innerJoin` selon le besoin.
3. Vérifiez l'utilisation des index de base de données dans les clauses `WHERE` et `ORDER BY`.
4. Suggérez l'usage de méthodes de Repository dédiées plutôt que de construire des requêtes complexes dans les contrôleurs.

## Exemple de code à analyser
[Collez ici le code PHP/Symfony à analyser]

## Points à vérifier
- [ ] La requête récupère-t-elle tout l'objet alors que seuls quelques champs sont utilisés (Partial Objects) ?
- [ ] Les jointures sont-elles accompagnées de `addSelect` pour éviter le Lazy Loading ultérieur ?
- [ ] La requête est-elle suffisamment complexe pour justifier du SQL natif ou une Vue SQL ?
- [ ] La pagination est-elle gérée efficacement (au niveau SQL, pas en mémoire PHP) ?

