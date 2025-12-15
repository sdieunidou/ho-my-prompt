# Audit SOLID & Responsabilité Unique

Analysez le code suivant pour vérifier le respect des 5 principes SOLID, avec une attention particulière portée au principe de responsabilité unique (Single Responsibility Principle - SRP).

## Instructions
1. Analysez chaque classe pour identifier si elle a plus d'une raison de changer.
2. Vérifiez si une classe mélange logique métier, logique de présentation et accès aux données.
3. Identifiez les violations des autres principes SOLID (Open/Closed, Liskov, Interface Segregation, Dependency Inversion) si elles sont flagrantes.
4. Proposez une refactorisation concrète pour séparer les responsabilités (ex: extraire un Service, un Repository ou un DTO).

## Exemple de code à analyser
[Collez ici le code PHP/Symfony à analyser]

## Points à vérifier
- [ ] La classe a-t-elle une responsabilité unique et clairement définie ?
- [ ] Les contrôleurs contiennent-ils de la logique métier (Fat Controller) ?
- [ ] Les entités contiennent-elles de la logique complexe (hors état) ?
- [ ] Les services sont-ils focalisés sur une tâche ou sont-ils des "God Objects" ?
- [ ] Le code est-il ouvert à l'extension mais fermé à la modification (Open/Closed) ?

