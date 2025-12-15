# Validation & Formulaires

Analysez le code pour vérifier que la validation des données passe par le composant Validator et les Formulaires Symfony, et non par des vérifications manuelles.

## Instructions
1. Repérez les blocs `if` qui valident manuellement des données d'entrée (`if (empty($data['email']))`).
2. Suggérez l'utilisation des Contraintes de Validation (Constraints) sur les entités ou les DTOs.
3. Vérifiez l'utilisation correcte des FormTypes pour la gestion des formulaires.
4. Assurez-vous que la méthode `isValid()` est bien appelée après `handleRequest()` ou `submit()`.

## Exemple de code à analyser
[Collez ici le code PHP/Symfony à analyser]

## Points à vérifier
- [ ] La validation est-elle centralisée via les attributs de validation (`#[Assert\NotBlank]`) ?
- [ ] Des validations manuelles dans le contrôleur pourraient-elles être remplacées par des Constraints ?
- [ ] Les formulaires sont-ils définis dans des classes `Type` dédiées et non dans le contrôleur ?
- [ ] La protection CSRF est-elle active (par défaut dans les Forms) ?
- [ ] Les messages d'erreur de validation sont-ils gérés correctement ?

