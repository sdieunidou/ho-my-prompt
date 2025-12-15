# Fuite de Données Sensibles

Analysez le code pour détecter l'exposition accidentelle de données sensibles (mots de passe, clés API, PII) dans les logs, les exceptions ou le code source.

## Instructions
1. Recherchez des clés d'API, mots de passe ou tokens "hard-codés" dans le code.
2. Vérifiez que les exceptions ne sont pas loggées avec les données sensibles de la requête (mots de passe en clair).
3. Assurez-vous que les données personnelles (GDPR) ne sont pas exposées inutilement dans les logs applicatifs.
4. Vérifiez la configuration de `monolog` pour exclure certains champs sensibles.

## Exemple de code à analyser
[Collez ici le code PHP/Symfony à analyser]

## Points à vérifier
- [ ] Y a-t-il des secrets (clés, mots de passe) committés dans le code ? (Utiliser `.env` / Secrets Vault)
- [ ] Les mots de passe utilisateurs apparaissent-ils dans les logs lors d'erreurs de formulaire ?
- [ ] Les entités User sont-elles sérialisées entièrement (JSON) exposant le hash du mot de passe ou le salt ?
- [ ] Le mode DEBUG est-il bien désactivé en production pour éviter la stacktrace publique ?

