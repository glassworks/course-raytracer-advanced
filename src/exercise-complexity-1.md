# Exercise : Compléxité 1 - AABBS

Le [raytracer fourni](https://github.com/glassworks/course-optimisation-sample) contient déjà une implémentation d'un AABB dans la bibliothèque `raymath`.

Votre tâche consiste à ajouter une instance `AABB` à chaque type de `SceneObject` (sphère, plan, triangle et mesh), en calculant ses valeurs `Min` et `Max`.

Insérer la ou les conditions correctes dans le code de rendu qui optimisera le processus de rendu en exploitant ces boîtes englobantes (en suivant le pseudo-code de la section précédente).

Testez votre optimisation sur :

- une scène avec seulement des sphères
- un mesh de sphère importé
- un maillage de singe importé
- une scène avec des sphères et le maillage du singe

N'oubliez pas d'effectuer vos tests pour vous assurer que le résultat du rendu n'a pas changé !

Exécutez vos tests **avec le threading désactivé** et comparez les résultats avant et après.

Ensuite, exécutez vos tests avec **AABBs désactivés**, mais **threading activé** et comparez les résultats avant et après.

Qu'est-ce qui s'avère être une meilleure optimisation, le threading ou les AABB ? Dressez un tableau de vos résultats.


| Aspect    | Note              |
| ---------------------- | ----------------- |
| Optimisation correcte/éprouvée avec les AABB |         5          |
| Analyse complète avant/après |                 3   |
| Conclusion |   1 |
| Tests fonctionnels |         1 |