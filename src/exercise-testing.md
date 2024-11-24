# Exercice 1 : Test

Vous avez reçu un raytracer de démonstration [ici](https://github.com/glassworks/course-optimisation-sample).

Votre premier exercice est le suivant :

Etendez ce projet avec un ou plusieurs tests end-to-end que nous pouvons utiliser pour nous assurer que notre optimisation ne casse rien !

Cet exercice comporte deux défis principaux :

1. Trouver, rechercher et implémenter un cadre de test pour C++. Puisque le projet principal utilise déjà CMake, vous pouvez, par exemple, utiliser [CTest](https://cmake.org/cmake/help/book/mastering-cmake/chapter/Testing%20With%20CMake%20and%20CTest.html).
2. Trouver comment créer un test de bout en bout qui puisse valider de manière fiable la sortie de notre raytracer - une image !

Il s'agit d'un exercice individuel ou en binôme (max. 2). Lorsque votre test fonctionne correctement, venez me le présenter pour recevoir vos points :


| Aspect    | Note              |
| ---------------------- | ----------------- |
| Cadre de test fonctionnel pouvant exécuter X tests  |         10          |
| Test pour un cas d'utilisation régulier |                 3   |
| Test pour un cas limite |   3 |
| Démonstration d'un scénario d'échec de test  |         4 |