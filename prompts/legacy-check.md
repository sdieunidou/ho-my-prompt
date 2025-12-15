# Bye-bye le "Legacy"

Analysez le code pour détecter l'utilisation de méthodes dépréciées, d'anciennes versions de PHP ou de pratiques Symfony obsolètes.

## Instructions
1. Identifiez l'usage des Annotations (/** @Route */) et suggérez le passage aux Attributs PHP 8 (`#[Route]`).
2. Repérez les fonctions ou classes marquées comme `@deprecated` dans les versions récentes de Symfony.
3. Vérifiez l'utilisation des nouvelles fonctionnalités de PHP 8+ (match, nullsafe operator, constructor property promotion).
4. Suggérez la modernisation du code pour assurer sa pérennité.

## Exemple de code à analyser
[Collez ici le code PHP/Symfony à analyser]

## Points à vérifier
- [ ] Le code utilise-t-il des Attributs PHP 8 au lieu des Annotations PHPDoc ?
- [ ] Les "Constructor Property Promotion" sont-elles utilisées pour alléger les entités/services ?
- [ ] Y a-t-il des appels à des méthodes dépréciées de Symfony (ex: Repository comme service sans interface) ?
- [ ] Le code tire-t-il parti des types d'union et de retour de PHP 8 ?
- [ ] La syntaxe des arrays (`[]`) est-elle utilisée partout au lieu de `array()` ?

