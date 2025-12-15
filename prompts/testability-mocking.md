# Facilité de Mocking

Analysez le code pour déterminer s'il est testable, c'est-à-dire si ses dépendances peuvent être facilement remplacées par des doublures (Mocks/Stubs) lors des tests unitaires.

## Instructions
1. Identifiez les dépendances "dures" (instanciations `new`, méthodes `static`, fonctions globales `time()`, `date()`) qui empêchent le mocking.
2. Suggérez l'injection de dépendances ou l'utilisation de wrappers (ex: `ClockInterface` au lieu de `new DateTime()`).
3. Vérifiez que les classes dépendent d'interfaces plutôt que de classes concrètes (pour faciliter le remplacement).
4. Détectez les méthodes trop longues ou complexes qui rendent les tests unitaires pénibles à écrire.

## Exemple de code à analyser
[Collez ici le code PHP/Symfony à analyser]

## Points à vérifier
- [ ] Les dépendances sont-elles injectées (constructeur) ou hard-codées ?
- [ ] Utilise-t-on des interfaces pour les services externes ?
- [ ] Le code utilise-t-il des singletons ou des façades statiques difficiles à mocker ?
- [ ] Peut-on tester cette classe sans démarrer tout le kernel Symfony ou la base de données ?

