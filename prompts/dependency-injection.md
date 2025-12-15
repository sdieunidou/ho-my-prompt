# Audit de l'Injection de Dépendances

Analysez le code pour détecter les instanciations manuelles et vérifier que l'injection de dépendances (DI) est utilisée correctement via le constructeur.

## Instructions
1. Recherchez toute instanciation avec le mot-clé `new` pour des services ou classes qui devraient être gérés par le conteneur.
2. Vérifiez que l'injection se fait via le constructeur (Constructor Injection) et non via des setters ou l'accès direct au conteneur (`$container->get()`).
3. Assurez-vous que l'Autowiring est exploité.
4. Identifiez les dépendances inutilisées injectées dans le constructeur.

## Exemple de code à analyser
[Collez ici le code PHP/Symfony à analyser]

## Points à vérifier
- [ ] Y a-t-il des `new MyService()` au lieu de l'injection de dépendances ?
- [ ] Le code utilise-t-il `$container->get()` (Service Locator pattern, à éviter) ?
- [ ] L'injection est-elle faite via le constructeur (bonne pratique) ?
- [ ] Les interfaces sont-elles typées dans le constructeur pour permettre le remplacement (Liskov) ?
- [ ] Y a-t-il trop de dépendances dans une seule classe (signe de trop de responsabilités) ?

