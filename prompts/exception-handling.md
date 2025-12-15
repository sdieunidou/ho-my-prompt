# Gestion des Exceptions

Analysez le code pour vérifier que les exceptions sont utilisées correctement : typées, attrapées au bon niveau et jamais avalées silencieusement.

## Instructions
1. Repérez les blocs `try/catch` vides ou qui ne font que logger sans relancer/traiter l'erreur.
2. Identifiez l'usage d'exceptions génériques (`\Exception`) et suggérez des exceptions personnalisées ou spécifiques (`UserNotFoundException`).
3. Vérifiez que les exceptions ne sont pas utilisées pour le contrôle de flux normal (ex: `try { $user = find(); } catch...`).
4. Assurez-vous que les exceptions propagent suffisamment d'informations de contexte.

## Exemple de code à analyser
[Collez ici le code PHP/Symfony à analyser]

## Points à vérifier
- [ ] Y a-t-il des `catch (\Exception $e) {}` vides (Silent Failure) ?
- [ ] Les exceptions lancées sont-elles spécifiques au problème ?
- [ ] Le code appelant peut-il réagir différemment selon le type d'exception ?
- [ ] Les messages d'exception sont-ils clairs pour le développeur (et sécurisés pour l'utilisateur) ?

