# La gestion dans l'incertitude

Vous avez probablement remarqué qu'il était assez difficile de planifier votre projet en raison de la grande part d'incertitude qu'il comporte.

Jusqu'à présent, vous avez probablement pris l'habitude de planifier efficacement vos projets, d'autant plus que le type de projet qui vous a été confié vous est très familier. Par exemple : 

- Développer une application Web avec :
  - une base de données
  - une API
  - Un front-end

La répartition des tâches est assez facile, car nous avons des sous-modules bien définis (front, back, devops, ...). De plus, vous avez déjà développé chacun de ces modules dans le cadre de votre cours, vous êtes familier avec les paramètres, vous avez peut-être déjà commencé à vous spécialiser dans un domaine particulier. La gestion du projet devient plus simple !

Mais avec le projet de raytracer, vous vous retrouvez soudain en terrain inconnu ! Il y a beaucoup d'incertitude :

- Travailler avec plusieurs coéquipiers que vous ne connaissez peut-être pas
- Vous n'êtes pas sûr du niveau d'expertise de chacun
- Peu ou pas de connaissance du domaine
- Peu ou pas de connaissance du langage de programmation
- ...

Comment répartir les tâches quand on ne sait même pas de quoi il s'agit ? A qui les assigner quand personne ne sait comment cela fonctionne ?

## Analyse

Un bon chef de projet ou responsable technique sait identifier les domaines dans lesquels il n'a que peu ou pas de connaissances et les inclut dans sa planification.

Mais comment identifier ces lacunes dans vos connaissances ? 

- Effectuez une **décomposition en profondeur des sous-tâches** nécessaires pour atteindre votre objectif. Ce n'est peut-être pas facile, mais essayez de décomposer autant d'étapes que vos connaissances actuelles vous le permettent. Et refaites votre analyse de manière récursive au fur et à mesure que vous acquérez de nouvelles connaissances.
- Effectuez une enquête au sein de votre équipe pour déterminer qui possède déjà certaines des compétences requises

Prenons l'exemple de notre raytracer. L'exigence était de *générer une image basée sur un algorithme de raytracing en utilisant C++*.

Il n'y a pas beaucoup d'informations sur lesquelles s'appuyer !

Mais nous pouvons déjà commencer à décomposer les sous-tâches :

- Nous devons connaître le C++
- Générer une image... comment faire ?
  - Nous devons générer un PNG... comment faire ?
- En savoir plus sur un algorithme de raytracing

Pour l'instant, l'algorithme de **raytracing** est encore une grande inconnue, mais les deux premiers points semblent gérables pour commencer.


## Prévoir l'incertitude

Indépendamment de la philosophie de développement et des outils que vous utilisez (Agile, Scrum, Kanban, ...), il serait bon d'inclure des **tâches exploratoires** dans votre planification, afin de vous permettre d'acquérir l'expertise nécessaire à l'exécution du projet.

Compte tenu des sous-tâches identifiées, nous pouvons déjà commencer à créer des tâches et à les distribuer à nos coéquipiers :

- Créer une application C++ « Hello World » : mettre en place la chaîne d'outils nécessaire à notre application.
- Recherche de bibliothèques pour l'exportation d'une image PNG : faire cela dans un projet parallèle juste pour acquérir les connaissances.
- Faire des recherches sur le raytracing

Nous avons suffisamment d'éléments pour qu'au moins 3 membres de notre équipe puissent commencer à travailler, et probablement obtenir des résultats en quelques heures !

Le membre responsable de l'élaboration de l'application C++ commencera à apprendre la structure du projet, l'orientation objet, le processus de construction, etc.

Le membre responsable de la recherche sur le raytracing commencera sans aucun doute à en apprendre plus sur les blocs de construction nécessaires : Vecteurs, rayons, etc. 

Le membre responsable de la recherche sur les images remarquera sans doute qu'il a besoin d'une représentation pour les couleurs.

Lors de notre prochaine réunion, chaque membre pourra présenter le résultat de son travail, et idéalement les autres membres pourront également acquérir les connaissances acquises. Par exemple, tout le monde saura maintenant comment démarrer une application C++ de base, et commencera probablement à s'approprier la notion de programmation orientée objet. 

Après avoir consulté le responsable technique, nous pouvons en toute confiance commencer à modéliser notre application. Nous avons déjà identifié certaines entités : Vecteur, Couleur, Image

Nous pouvons commencer à ajouter ces éléments à notre backlog :

- Créer une classe Vector3 avec l'ensemble des opérateurs de base (ajouter, soustraire, multiplier).
- Créer une classe Couleur
- Créer une classe Image dans laquelle nous pouvons écrire des couleurs et les sauvegarder sur le disque.

Il peut y avoir un chevauchement entre les 2 dernières tâches. Dans ce cas, la première itération de la personne qui crée la classe Image se contente d'écrire de fausses données sur le disque. Il s'agira d'une implémentation de type « preuve de concept » qui sera très probablement abandonnée. Mais une fois que la classe Color sera prête, nous pourrons perfectionner la classe Image afin de l'utiliser pour la représentation interne.



{% hint style="success" %}
Ce qu'il faut retenir, c'est que

**N'ayez pas peur d'ajouter des tâches exploratoires et de recherche à votre backlog**.
{% endhint %}

## Incertitude à l'égard de votre client

Même en tenant compte de l'incertitude, votre client voudra très probablement savoir exactement quand son produit sera prêt.
(Lorsque je parle d'un client, il peut s'agir de votre patron ou d'un client externe).
D'après mon expérience, il existe deux types de scénarios :

- **Les projets pour lesquels nous avons le pouvoir d'estimer le temps de développement et de déclarer la date de livraison**: C'est le meilleur scénario, mais attention, votre client ne va pas attendre indéfiniment ! Vous devez tout de même fournir une estimation de la durée du développement. 
- **Projets dont la date de livraison est fixe et inamovible**: Cette situation se produit lorsque votre projet correspond à un événement particulier et inamovible (comme la Saint-Sylvestre). C'est la situation la plus difficile à gérer, surtout lorsqu'il y a de l'incertitude. C'est difficile, mais il arrive que vous deviez refuser un projet parce que vous estimez qu'il est irréalisable !


### Estimation flexible

Comment calculer la date de livraison en présence d'une grande incertitude ?

D'après mon expérience, essayez de donner à votre équipe une grande marge de manœuvre pour cette incertitude !

La seule information dont vous disposez est celle que vous connaissez déjà. Vous ne savez pas encore ce que vous ne savez pas ! Utilisez ces informations pour décomposer les sous-tâches autant que possible. Partout où vous identifiez la plus grande lacune dans les connaissances, donnez-vous la plus grande marge de manœuvre pour faire des recherches et développer des preuves de concept.

Il est essentiel de maintenir des canaux de communication clairs avec votre client ! Il est fort possible que votre client connaisse votre domaine mieux que vous et qu'il :
- puisse vous donner une formation dans le domaine
- vous indiquer des ressources pertinentes
- vous présenter des personnes expérimentées que vous pouvez intégrer à votre équipe.

Au minimum, indiquez à votre client les lacunes de vos connaissances et incluez dans votre calendrier de livraison des étapes intermédiaires au cours desquelles vous livrerez les résultats de vos recherches. Il sera ainsi satisfait de l'avancement du projet. 

Si vous rencontrez un problème, cette approche vous permettra également de tenir le client informé et le rendra peut-être plus enclin à ajuster la date de livraison. 


### Dates d'échéance fixes

Il y a parfois des limites strictes à respecter - spectacles prévus, festivals, etc. Des dates de publication sur lesquelles même le client n'a aucun contrôle.

Dans ces situations, vous devez être en mesure d'estimer clairement si l'incertitude est trop grande pour garantir une livraison dans les délais. Si la date de livraison est suffisamment éloignée dans le temps, le projet peut encore être réalisable. Mais si la date est très proche, vous devrez peut-être faire des choix difficiles.

D'après mon expérience, il existe quelques solutions :

- **réduire la portée du projet**: expliquez à votre client où se situe exactement l'incertitude. Vous pouvez peut-être réduire la portée du projet afin d'éliminer autant d'incertitude que possible.
- **Refuser le projet**: expliquer clairement à votre client pourquoi l'incertitude vous empêche d'honorer la date de livraison.

Dans tous les cas, **la communication est essentielle**. Même si vous n'avez pas d'autre choix que d'accepter le projet, indiquez très clairement qu'il pourrait y avoir des risques graves quant à la faisabilité du projet. **Et assurez-vous d'avoir précisé ces risques par écrit !**

## Collecte itérative des connaissances

Comme indiqué ci-dessus, commencez par ce que vous savez et essayez d'améliorer vos connaissances au fur et à mesure que vous avancez dans le projet.

Vous devez continuellement **mettre à jour votre backlog**, **partager vos connaissances avec vos coéquipiers**, et **informer vos clients** des résultats de vos preuves de concept, de vos recherches.

{% hint style="success" %}

TLDR ;

Collecte récursive de connaissances et planification :

- analyser/planifier autant que vos connaissances le permettent
- ajouter des tâches exploratoires à votre carnet de commandes (recherche de preuves de concept)
- partagez des informations avec vos coéquipiers
- garder la communication ouverte avec vos clients

{% endhint %}