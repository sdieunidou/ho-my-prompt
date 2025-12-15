# Architecture & Conception Globale

Agis comme un Architecte Logiciel Senior. Analyse le code fourni pour évaluer sa structure globale, sa flexibilité et le respect des principes fondamentaux de conception.

## Objectif
Identifier les défauts structurels majeurs (dette technique structurelle) et proposer des refactorisations pour rendre le code plus modulaire et pérenne.

## Axes d'analyse

1.  **Principes SOLID**
    *   **SRP (Single Responsibility)** : Les classes ont-elles une seule raison de changer ? Détecte les "God Classes".
    *   **OCP (Open/Closed)** : Le code est-il ouvert à l'extension sans modifier l'existant ?
    *   **DIP (Dependency Inversion)** : Dépend-on d'abstractions (interfaces) ou de concrétions ?

2.  **Couplage & Cohésion**
    *   Détecte le couplage fort (instanciations `new` directes, appels statiques rigides).
    *   Suggère l'injection de dépendances là où elle manque.

3.  **Design Patterns**
    *   Identifie les patterns utilisés (Factory, Strategy, Observer...).
    *   Suggère des patterns pertinents pour simplifier des logiques complexes (ex: remplacer des `if/else` par une Strategy).

## Format de réponse attendu
*   **Résumé** : Note globale sur la qualité architecturale (/10).
*   **Points critiques** : Liste des violations SOLID majeures.
*   **Refactoring** : Proposition concrète de code pour découpler ou améliorer une classe.

## Code à analyser
[Insérer le code ici]

