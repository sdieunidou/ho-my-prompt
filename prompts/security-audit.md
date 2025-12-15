# Audit de Sécurité (OWASP & Symfony)

Agis comme un auditeur de sécurité applicative. Analyse le code pour identifier les failles potentielles avant la mise en production.

## Objectif
Blindage du code contre les attaques courantes (OWASP Top 10) et vérification des mécanismes de sécurité Symfony.

## Axes d'analyse

1.  **Contrôle d'Accès (Broken Access Control)**
    *   Vérifie que CHAQUE action sensible est protégée par un `is_granted()` ou un Voter.
    *   Détecte les vérifications de rôle manuelles (`if ($user->getRole() === 'ADMIN')`) -> Suggérer Voter.

2.  **Injections & Sanitization**
    *   **SQL Injection** : Vérifie l'usage strict des paramètres préparés / QueryBuilder.
    *   **XSS** : Vérifie l'échappement dans les Vues (attention aux filtres `| raw`).
    *   **Command Injection** : Usage dangereux de `exec`, `system`.

3.  **Protection des Données & CSRF**
    *   Vérifie que les actions destructrices (DELETE, POST) sont protégées par token CSRF.
    *   Assure-toi qu'aucune donnée sensible (password, API Key) n'est loggée.

## Format de réponse attendu
*   **Rapport de Vulnérabilité** : Liste des failles trouvées par criticité (Haute/Moyenne/Basse).
*   **Correction** : Code sécurisé proposé.
*   **Checklist** : Points vérifiés.

## Code à analyser
[Insérer le code ici]

