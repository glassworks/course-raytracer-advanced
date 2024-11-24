# Exercice 4 : Complexité 1

Le [raytracer fourni](https://github.com/glassworks/course-optimisation-sample) contient déjà une implémentation d'un AABB dans la bibliothèque `raymath`.

Votre tâche consiste à ajouter une instance `AABB` à chaque type de `SceneObject` (sphère, plan, triangle et mesh), en calculant ses valeurs `Min` et `Max`.

Insérer la ou les conditions correctes dans le code de rendu qui optimisera le processus de rendu en exploitant ces boîtes englobantes (en suivant le pseudo-code de la section précédente).

Testez votre optimisation sur :

* une scène avec seulement des sphères
* un mesh de sphère importé
* un maillage de singe importé
* une scène avec des sphères et le maillage du singe

N'oubliez pas d'effectuer vos tests pour vous assurer que le résultat du rendu n'a pas changé !

Exécutez vos tests **avec le threading désactivé** et comparez les résultats avant et après.

Ensuite, exécutez vos tests avec **AABBs désactivés**, mais **threading activé** et comparez les résultats avant et après.

Qu'est-ce qui s'avère être une meilleure optimisation, le threading ou les AABB ? Dressez un tableau de vos résultats.

<table><thead><tr><th width="612">Aspect</th><th>Note</th></tr></thead><tbody><tr><td>Optimisation correcte/éprouvée avec les AABB</td><td>5</td></tr><tr><td>Analyse complète avant/après</td><td>3</td></tr><tr><td>Conclusion</td><td>1</td></tr><tr><td>Tests fonctionnels</td><td>1</td></tr></tbody></table>
