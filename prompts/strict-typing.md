# Typage Strict (PHP 8+)

Analysez le code pour vérifier l'utilisation rigoureuse du système de typage de PHP 8+ et la déclaration stricte des types.

## Instructions
1. Vérifiez la présence de `declare(strict_types=1);` en haut de chaque fichier.
2. Assurez-vous que toutes les propriétés de classe, arguments de méthode et valeurs de retour sont typés.
3. Suggérez l'utilisation des types nullables (`?string`) et des unions de types (`int|float`) si nécessaire.
4. Repérez l'absence de type de retour `void` pour les méthodes qui ne retournent rien.

## Exemple de code à analyser
[Collez ici le code PHP/Symfony à analyser]

## Points à vérifier
- [ ] `declare(strict_types=1);` est-il présent ?
- [ ] Les types de retour sont-ils tous déclarés (y compris `void`) ?
- [ ] Les propriétés de classe sont-elles typées ?
- [ ] Utilise-t-on `mixed` uniquement en dernier recours ?
- [ ] Les DocBlocks `@param` sont-ils supprimés là où le typage natif suffit ?

