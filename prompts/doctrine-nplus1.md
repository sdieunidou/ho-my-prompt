# Chasse aux problèmes N+1

Analysez le code pour détecter les boucles sur des entités Doctrine qui génèrent le problème "N+1 queries" (une requête pour la liste, N requêtes pour les relations).

## Instructions
1. Repérez les boucles `foreach` sur une collection d'entités où l'on accède à une relation non initialisée.
2. Identifiez les relations `ManyToOne` ou `OneToMany` chargées en `LAZY` (par défaut) et accédées dans une boucle.
3. Suggérez l'utilisation de `join fetch` (DQL) ou de chargement EAGER pour récupérer les données en une seule requête.
4. Vérifiez si les templates Twig déclenchent aussi ces requêtes cachées.

## Exemple de code à analyser
[Collez ici le code PHP/Symfony (Controller ou Twig) à analyser]

## Points à vérifier
- [ ] Une boucle itère-t-elle sur des entités en accédant à leurs relations (`$article->getAuthor()->getName()`) ?
- [ ] Le Repository utilise-t-il des jointures (`addSelect`) pour pré-charger les données nécessaires ?
- [ ] Le nombre de requêtes SQL augmente-t-il linéairement avec le nombre d'éléments affichés ?
- [ ] Y a-t-il des appels à la base de données à l'intérieur d'une boucle ?

