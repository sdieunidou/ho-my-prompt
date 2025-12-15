# Fuites de Mémoire & Processus Lourds

Analysez les scripts de commande (Console/Messenger) et les processus batch pour prévenir les fuites de mémoire et optimiser le traitement de gros volumes.

## Instructions
1. Vérifiez que l'EntityManager est nettoyé (`$em->clear()` ou `detach()`) périodiquement dans les boucles de traitement.
2. Identifiez les accumulations d'objets en mémoire (tableaux qui grossissent indéfiniment).
3. Suggérez l'utilisation de `iterate()` ou `toIterable()` pour traiter les résultats de requête ligne par ligne.
4. Assurez-vous que le Garbage Collector de PHP peut faire son travail.

## Exemple de code à analyser
[Collez ici le code PHP/Symfony à analyser]

## Points à vérifier
- [ ] Y a-t-il un `$em->clear()` ou `$em->detach($entity)` après le traitement d'un lot d'entités ?
- [ ] Les requêtes retournent-elles un itérateur (`toIterable`) au lieu de charger tous les résultats en mémoire ?
- [ ] Le script est-il conçu pour s'arrêter proprement (limite de temps/mémoire) pour être relancé par un superviseur (effet "PHP dies") ?
- [ ] L'option `--no-debug` est-elle utilisée en prod pour éviter le logging mémoire excessif ?

