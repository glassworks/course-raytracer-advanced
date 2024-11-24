# Exercice 3 : Threading

Modifier la classe Camera du [raytracer ici](https://github.com/glassworks/course-optimisation-sample) afin d'ajouter le multithreading au processus de rendu.

Vous devrez procéder comme suit :

* Diviser votre image en X sections
* Créez un nouveau thread pour effectuer le rendu de chaque section. N'oubliez pas de transmettre toutes les informations nécessaires pour effectuer le rendu !
* Réassembler l'image finale
* Exécutez vos tests pour vous assurer que le résultat n'a pas changé.

Votre code doit inclure une [définition du compilateur](https://cmake.org/cmake/help/latest/command/add_compile_definitions.html#command:add_compile_definitions) afin d'activer ou de désactiver le multithreading en utilisant un **directive du compilateur**.

Mesurez votre scène de rendu avec :

* threading désactivé
* threading activé

Les performances se sont-elles améliorées ou avons-nous aggravé la situation ?

<table><thead><tr><th width="646">Aspect</th><th>Note</th></tr></thead><tbody><tr><td>Threading fonctionnel</td><td>3</td></tr><tr><td>Tests réussis, résultat du rendu inchangé</td><td>2</td></tr><tr><td>Résultats de l'optimisation (temps)</td><td>3</td></tr><tr><td>Directive du compilateur</td><td>2</td></tr></tbody></table>
