# Architecture Hexagonale & DDD

Agis comme un Expert en Domain-Driven Design (DDD) et Architecture Hexagonale. Analyse le code pour vérifier la pureté du Domaine et la bonne isolation des couches.

## Objectif
S'assurer que la logique métier est reine, indépendante de l'infrastructure, et qu'elle respecte le langage ubiquitaire.

## Axes d'analyse

1.  **Isolation du Domaine (The Core)**
    *   Le dossier `Domain` contient-il des dépendances vers le Framework, Doctrine ou des lib tiers ? (Interdit !)
    *   Les Entités sont-elles riches (comportement) ou anémiques (juste des getters/setters) ?

2.  **Ports & Adapters (Hexagonal)**
    *   **Ports (Interfaces)** : Sont-ils bien définis dans le Domaine pour les interactions externes (Repository, Mailer) ?
    *   **Adapters (Infrastructure)** : Les implémentations techniques sont-elles bien isolées dans l'Infrastructure ?

3.  **Règles Tactiques DDD**
    *   Les **Value Objects** sont-ils utilisés pour encapsuler des concepts (Email, Money) ?
    *   Les **Agrégats** garantissent-ils la cohérence transactionnelle ?
    *   Le **Langage Ubiquitaire** est-il respecté dans le nommage ?

## Format de réponse attendu
*   **Analyse de Pureté** : Liste des fuites d'infrastructure dans le domaine.
*   **Modélisation** : Suggestions pour enrichir les modèles anémiques ou créer des Value Objects.
*   **Structure** : Vérification de l'emplacement des fichiers.

## Code à analyser
[Insérer le code ici]

