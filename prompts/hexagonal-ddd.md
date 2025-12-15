# Cohérence de l'Architecture Hexagonale / DDD

Analysez le code suivant pour vérifier si l'isolation entre la logique métier (Domain) et les détails techniques (Infrastructure/Framework) est respectée.

## Instructions
1. Identifiez les fuites de l'infrastructure vers le domaine (ex: annotations Doctrine ou classes Symfony dans les entités du Domaine).
2. Vérifiez que le Domaine ne dépend de rien d'autre que lui-même.
3. Contrôlez l'usage des Ports (Interfaces) et Adapters.
4. Assurez-vous que le langage ubiquitaire (Ubiquitous Language) est présent dans le code.

## Exemple de code à analyser
[Collez ici le code PHP/Symfony à analyser]

## Points à vérifier
- [ ] Le Domaine est-il pur et sans dépendance vers le framework ou l'ORM ?
- [ ] Les règles métier sont-elles encapsulées dans le Domaine (et non dans les Services Applicatifs) ?
- [ ] L'inversion de dépendance est-elle respectée via les Ports (Interfaces) ?
- [ ] Les Adapters (Infrastructure) implémentent-ils correctement les interfaces du Domaine ?
- [ ] Les agrégats et Value Objects sont-ils correctement identifiés et immuables si nécessaire ?

