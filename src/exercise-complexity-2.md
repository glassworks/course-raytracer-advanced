# Exercice : BSP-Trees

Le [raytracer fourni](https://github.com/glassworks/course-optimisation-sample) contient déjà une implémentation d'un AABB dans la bibliothèque `raymath`.


Votre tâche est de créer un arbre BSP de votre scène, et de l'utiliser pendant votre phase de rendu pour réduire le temps de rendu (spécifiquement en essayant de trouver la collision rayon-objet la plus proche).

Testez votre optimisation sur :

- une scène avec seulement des sphères
- un mesh de sphère importé
- un maillage de singe importé
- une scène avec des sphères et le maillage du singe

N'oubliez pas d'effectuer vos tests pour vous assurer que le résultat du rendu n'a pas changé !

Exécutez vos tests **avec le threading désactivé** et comparez les résultats avant et après.

Ensuite, exécutez vos tests avec **BSP-Tree désactivé**, mais **threading activé** et comparez les résultats avant et après.

Qu'est-ce qui s'avère être une meilleure optimisation, le threading ou le BSP-Tree ? Dressez un tableau de vos résultats.

| Aspect    | Note              |
| ---------------------- | ----------------- |
| Optimisation correcte/éprouvée avec un BSP-Tree |         5          |
| Analyse complète avant/après |                 3   |
| Conclusion |   1 |
| Tests fonctionnels |         1 |