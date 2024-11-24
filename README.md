---
cover: .gitbook/assets/sphere-galaxy-on-plane.png
coverY: 0
---

# Ingénierie avancée et optimisation

Vous avez probablement remarqué au cours du [développement de votre ray-tracer](https://docs.glassworks.tech/lanceur-de-rayon) que le processus d'ingénierie était plutôt difficile :

* Il y avait beaucoup d'incertitudes
* Vous vous êtes retrouvé à écrire du code désordonné
* Votre application n'était pas très performante et prenait beaucoup de temps pour rendre la moindre image.

Ce cours a pour but de fournir un débriefing et une discussion autour de votre expérience vécue au cours de ce projet, et nous examinerons les leçons que nous pouvons tirer de cette expérience :

* Gérer l'incertitude et le manque de connaissances dans un projet d'ingénierie
* Quelle conception serait appropriée pour ce type de projet ?
* Stratégies d'amélioration de la qualité de l'application, avec un accent particulier sur l'**optimisation**.

A l'issue de ce module, vous devriez avoir acquis les compétences suivantes :

* Être capable d'intégrer l'incertitude dans votre planification
* Evaluer la faisabilité d'un projet en présence d'incertitude
* Être à l'aise avec la notion de **conception basée sur les entités**, et les principes de conception de la programmation orientée objet, tels que **composition**, **héritage**, **polymorphisme** et **interfaces**.
* Être capable de lire et de concevoir un diagramme d'entité UML
* Avoir une approche rationnelle et stratégique de l'**optimisation**, notamment
  * quand optimiser
  * éviter les régressions (par des tests)
  * l'analyse de la complexité des algorithmes
  * les techniques d'optimisation.

## Evaluation

Ce cours sera évalué à travers un certain nombre de petits exercices que vous devrez réaliser individuellement ou en utilisant la programmation par paire (groupes de 2 personnes maximum).

La semaine consistera en un court cours où nous analyserons et discuterons d'un sujet particulier, suivi d'un exercice.

Lorsque vous serez prêts, vous devrez me présenter vos résultats au cours de la journée afin d'obtenir vos notes. J'aurai besoin de voir votre application exécuter et produire tout ou partie des résultats requis par chaque exercice.

## Etude de cas

Tout au long de ce cours, vous travaillerez avec mon implémentation de base d'un ray-tracer que vous pouvez télécharger ici :

[Kevin's Awesome Raytracer](https://github.com/glassworks/course-optimisation-sample)

Vous pouvez être tenté de commencer avec votre propre implémentation du ray-tracer, mais soyez averti que certains aspects requis pour les mesures et les tests peuvent ne pas être implémentés dans votre version.

Bonne chance !
