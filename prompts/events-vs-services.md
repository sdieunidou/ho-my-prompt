# Utilisation des Events vs Services

Analysez le code pour déterminer si l'usage de l'EventDispatcher serait plus approprié que des appels directs de services, ou inversement.

## Instructions
1. Repérez les séquences d'appels de services qui s'enchaînent de manière rigide (ex: après une commande, envoyer un mail, puis logger, puis notifier).
2. Suggérez l'utilisation d'événements Symfony pour découpler ces actions secondaires de l'action principale.
3. À l'inverse, vérifiez qu'on n'utilise pas des événements pour une logique séquentielle critique qui nécessite un retour immédiat.
4. Vérifiez la création et la structure des classes d'événements.

## Exemple de code à analyser
[Collez ici le code PHP/Symfony à analyser]

## Points à vérifier
- [ ] La logique métier principale est-elle polluée par des appels à des services secondaires (Email, Log, Notification) ?
- [ ] L'EventDispatcher pourrait-il découpler le code et améliorer l'extensibilité ?
- [ ] Les événements créés sont-ils pertinents et bien nommés (ex: `OrderPlacedEvent`) ?
- [ ] Les écouteurs (Listeners/Subscribers) sont-ils bien isolés ?
- [ ] Le code abuse-t-il des événements, rendant le flux d'exécution difficile à suivre ?

