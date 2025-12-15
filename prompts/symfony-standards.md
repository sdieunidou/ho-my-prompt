# Conformité aux Standards Symfony

Analysez le code pour vérifier qu'il respecte les conventions, l'arborescence et les bonnes pratiques standard du framework Symfony.

## Instructions
1. Vérifiez que les fichiers sont placés dans les bons répertoires (Controller, Service, Entity, Repository, etc.).
2. Contrôlez l'usage des fonctionnalités natives de Symfony au lieu de solutions "maison".
3. Assurez-vous que la configuration utilise les mécanismes modernes (services.yaml, variables d'env).
4. Vérifiez le respect des conventions de nommage Symfony.

## Exemple de code à analyser
[Collez ici le code PHP/Symfony à analyser]

## Points à vérifier
- [ ] L'arborescence des fichiers suit-elle la structure standard de Symfony ?
- [ ] Les contrôleurs étendent-ils `AbstractController` et retournent-ils des objets `Response` ?
- [ ] Les services sont-ils bien définis et autowirés ?
- [ ] Le ParamConverter (ou MapEntity) est-il utilisé pour simplifier les contrôleurs ?
- [ ] Les exceptions Symfony (HttpException, NotFoundHttpException) sont-elles utilisées ?

