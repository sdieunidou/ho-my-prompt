# Performance & Doctrine

Agis comme un expert en Performance Web et bases de données. Analyse le code pour détecter les goulots d'étranglement, les requêtes inefficaces et les problèmes de mémoire.

## Objectif
Optimiser les interactions avec la base de données et la consommation de ressources.

## Axes d'analyse

1.  **Le Problème N+1 (Doctrine)**
    *   Scanne les boucles (`foreach`) sur des entités.
    *   Détecte l'accès à des relations non initialisées (Lazy Loading) à l'intérieur de boucles.
    *   Solution : Suggère des jointures `join fetch` en DQL.

2.  **Optimisation SQL & DQL**
    *   Vérifie que l'on ne sélectionne pas trop de données (`select *` implicite).
    *   Suggère l'usage de **DTOs** (Data Transfer Objects) pour les lectures (listes, exports) afin d'éviter l'hydratation lourde.
    *   Analyse les index potentiellement manquants.

3.  **Gestion de la Mémoire**
    *   Pour les scripts Batch/Messenger : Vérifie la présence de `$em->clear()` ou `detach()`.
    *   Détecte les tableaux PHP qui grossissent indéfiniment.

## Format de réponse attendu
*   **Alertes Rouges** : Problèmes N+1 identifiés (ligne précise).
*   **Optimisation** : Réécriture de la requête DQL ou suggestion de DTO.
*   **Conseil Mémoire** : Bonnes pratiques pour le traitement par lots.

## Code à analyser
[Insérer le code ici]

