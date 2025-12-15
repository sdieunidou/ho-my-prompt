# Audit des Voters & Permissions

Analysez le code pour vérifier que l'accès aux ressources est sécurisé via le système de Voters de Symfony et non par une logique ad-hoc.

## Instructions
1. Vérifiez que chaque action de contrôleur ou accès aux données est protégé par un `is_granted()`.
2. Identifiez les logiques de permission complexes "hard-codées" dans les contrôleurs (`if ($user->getRole() === 'ADMIN' && $post->getAuthor() === $user)`) et suggérez leur déplacement dans un Voter.
3. Assurez-vous que les Voters soutiennent le principe de moindre privilège.
4. Vérifiez la cohérence des attributs de sécurité utilisés.

## Exemple de code à analyser
[Collez ici le code PHP/Symfony à analyser]

## Points à vérifier
- [ ] L'accès aux méthodes du contrôleur est-il restreint (`IsGranted`, `denyAccessUnlessGranted`) ?
- [ ] La logique de permission métier est-elle encapsulée dans des classes `Voter` ?
- [ ] Évite-t-on de vérifier les rôles (`ROLE_ADMIN`) directement dans le code métier (préférez les capacités/attributs) ?
- [ ] Le Voter gère-t-il correctement le cas où l'utilisateur n'est pas connecté ?

