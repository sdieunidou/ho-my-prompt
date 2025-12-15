# Sanitization & Injections (XSS/SQLi)

Analysez le code pour détecter les vulnérabilités d'injection (SQL, XSS, Command) et vérifier l'échappement des données.

## Instructions
1. Recherchez toute concaténation de variables dans des chaînes SQL (`"SELECT * FROM users WHERE name = " . $name`).
2. Identifiez l'affichage de données brutes dans Twig (`raw` ou `| raw`) sans échappement préalable sûr.
3. Vérifiez l'utilisation de `exec()`, `system()`, `passthru()` avec des entrées utilisateur.
4. Assurez-vous que les données entrantes sont nettoyées si nécessaire.

## Exemple de code à analyser
[Collez ici le code PHP/Symfony à analyser]

## Points à vérifier
- [ ] Utilise-t-on les paramètres préparés (Prepared Statements) pour toutes les requêtes SQL ?
- [ ] Le filtre `raw` de Twig est-il utilisé de manière sécurisée (uniquement sur du contenu de confiance) ?
- [ ] Les commandes système échappent-elles les arguments (`escapeshellarg`) ?
- [ ] Les données HTML stockées en base sont-elles purifiées (ex: avec HTML Purifier) ?

