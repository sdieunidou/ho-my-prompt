# CSRF & Protection des Routes

Analysez le code pour vérifier que les actions modifiant l'état (POST, PUT, DELETE, PATCH) sont protégées contre les attaques CSRF et respectent la sémantique HTTP.

## Instructions
1. Vérifiez que les actions de modification ne sont pas accessibles via GET.
2. Assurez-vous que les formulaires et les actions AJAX incluent et vérifient le token CSRF.
3. Repérez les méthodes de contrôleur qui effectuent des actions destructrices sans validation de token.
4. Contrôlez la configuration globale de sécurité CSRF.

## Exemple de code à analyser
[Collez ici le code PHP/Symfony à analyser]

## Points à vérifier
- [ ] Les actions de suppression/modification exigent-elles la méthode POST/DELETE (et non GET) ?
- [ ] Le token CSRF est-il vérifié pour chaque soumission de formulaire (`$form->handleRequest()` le fait par défaut) ?
- [ ] Les appels AJAX modifiants envoient-ils le header X-CSRF-TOKEN ?
- [ ] Les liens de déconnexion (`/logout`) sont-ils configurés correctement pour éviter le CSRF ?

