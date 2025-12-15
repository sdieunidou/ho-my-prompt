# Stratégie de Tests & Mocking

Agis comme un Expert QA/Test Automation. Analyse le code pour évaluer sa testabilité et suggérer une stratégie de test robuste.

## Objectif
S'assurer que le code est modulaire (testable) et identifier les cas limites à couvrir absolument.

## Axes d'analyse

1.  **Testabilité (Design for Testability)**
    *   Le code dépend-il d'interfaces (faciles à mocker) ou de classes concrètes ?
    *   Y a-t-il des appels statiques, des singletons, ou des fonctions globales (`time()`, `rand()`) qui bloquent les tests ?
    *   Suggère l'injection de dépendances là où elle manque.

2.  **Scénarios de Tests (Test Cases)**
    *   **Happy Path** : Le cas nominal.
    *   **Edge Cases** : Que se passe-t-il avec `null`, `[]`, `0`, ou des chaînes vides ?
    *   **Error Handling** : Les exceptions attendues sont-elles bien levées ?

## Format de réponse attendu
*   **Critique de Testabilité** : Points bloquants pour écrire des tests unitaires.
*   **Plan de Test** : Liste à puces des scénarios à implémenter (Nominal + Cas limites).

## Code à analyser
[Insérer le code ici]

