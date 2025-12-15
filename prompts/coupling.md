# Détection du Couplage Fort

Analysez le code suivant pour détecter les dépendances rigides et le couplage fort entre les classes, et proposez des solutions pour le réduire.

## Instructions
1. Identifiez les dépendances directes vers des classes concrètes (instanciations avec `new`, types concrets dans les signatures).
2. Repérez les violations du principe d'inversion de dépendance (DIP).
3. Vérifiez l'utilisation excessive de méthodes statiques (couplage statique).
4. Suggérez l'introduction d'interfaces ou l'injection de dépendances pour assouplir le code.

## Exemple de code à analyser
[Collez ici le code PHP/Symfony à analyser]

## Points à vérifier
- [ ] Le code dépend-il d'abstractions (interfaces) ou de concrétions ?
- [ ] Y a-t-il des instanciations directes (`new`) au lieu de l'injection de dépendances ?
- [ ] Les dépendances externes (API, DB, Framework) sont-elles isolées ?
- [ ] L'utilisation de `static` rend-elle le code difficilement testable/mockable ?
- [ ] Le code respecte-t-il la Loi de Demeter (ne pas parler aux inconnus) ?

