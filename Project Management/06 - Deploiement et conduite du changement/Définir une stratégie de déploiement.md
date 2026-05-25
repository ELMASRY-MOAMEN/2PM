# Définir une stratégie de déploiement

## Objectif

Définir comment déployer un élément software, hardware ou mixte dans un environnement réel, en maîtrisant les impacts, les risques, les acteurs et la traçabilité.

## Quand l'utiliser

Utiliser cette compétence après :

- [[Réaliser une étude d'impact de déploiement]]
- [[Réaliser une analyse de risque de déploiement]]

Elle sert à choisir le mode de déploiement, les étapes, les responsabilités, les outils et les dispositifs d'accompagnement.

Elle doit aussi sécuriser le moment où la solution commence à être utilisée opérationnellement par le métier, souvent appelé `cut over`.

## Entrées nécessaires

- étude d'impact du déploiement ;
- analyse de risque du déploiement ;
- contraintes de planning ;
- contraintes métier ;
- volumes à déployer ;
- contraintes techniques ;
- acteurs et responsabilités ;
- capacités de support, formation et communication.
- contexte projet : contrainte réglementaire, contrainte technique, objectif métier, problème de production ;
- contexte métier : contraintes horaires, dispersion des utilisateurs, opportunité de gains rapides ;
- caractéristiques applicatives : application monobloc ou modulaire, architecture homogène ou complexe, criticité.

## Étapes à suivre

1. Vérifier que l'étude d'impact et l'analyse de risque sont disponibles.
2. Décider si un déploiement pilote est nécessaire.
3. Si un pilote est retenu, définir un échantillon représentatif : environnements de travail, types d'assets, configurations, marques, logiciels installés, sites ou populations.
4. Définir le mode de déploiement industriel : big bang ou séquentiel.
5. Définir l'ordre de déploiement : sites, services, utilisateurs, modules ou périmètres.
6. Construire une matrice RACI validée par les acteurs.
7. Définir le plan de déploiement.
8. Interfacer le déploiement avec les processus d'entreprise : achats, approvisionnement, assistance, maintenance, sécurité, formation.
9. Définir la traçabilité du déploiement : données, outils, indicateurs, statuts réalisés, en cours et à faire.
10. Définir les outils de déploiement : outil industriel ou outil bureautique selon le contexte.
11. Prévoir la récupération et l'exploitation des retours utilisateurs.
12. Coordonner la communication et la formation avec la conduite du changement.
13. Définir le mode produit après le projet : mise au catalogue, déploiement unitaire, assistance et maintenance.

## Démarche transverse projet-produit

Le déploiement se prépare dès les phases amont du projet.

Une démarche complète couvre :

1. Études : faire une étude d'impact, définir la stratégie, créer une checklist macro, gérer les risques.
2. Préparation : détailler la checklist, préparer le déploiement, communiquer, former et documenter.
3. Réalisation : faire des tirs à blanc, conduire le cut over, accompagner les utilisateurs, gérer les risques.
4. Exploitation : déployer régulièrement, passer vers le support, maintenir l'accompagnement et améliorer le processus.

Le lien avec la conduite du changement est fort : un déploiement réussi facilite l'appropriation métier.

## Options de stratégie

### Déploiement pilote

Un pilote déploie la solution sur un échantillon représentatif pour roder les processus, vérifier l'opérationnalité des postes ou environnements, et collecter du feedback utilisateur.

### Déploiement big bang

Le big bang déploie tout en une fois. C'est la stratégie la plus risquée. Elle peut être nécessaire lorsque l'ancien système doit s'arrêter ou qu'une marche en double est impossible.

Pour une stratégie big bang, l'agent doit prévoir une checklist macro, des tirs à blanc, un chronogramme détaillé, un dispositif de support renforcé et une décision claire sur le point de non-retour.

### Déploiement séquentiel

Le déploiement séquentiel avance par site, service, module ou population. Il permet de roder le processus et le support avant de traiter les périmètres les plus sensibles.

### Marche en double

La marche en double consiste à faire fonctionner l'ancien et le nouveau dispositif pendant une période donnée. Elle réduit le risque de bascule, mais demande souvent des interfaces avec le SI de production, une organisation métier plus lourde et une période longue entre mise en production et mise en service.

### Site pilote

Le site pilote combine une logique de pilote et une logique de déploiement localisé. Il permet de tester en conditions réelles sur un périmètre limité avant d'élargir.

### Rollback

Le rollback consiste à prévoir le retour arrière si le déploiement échoue ou si les impacts deviennent inacceptables.

L'agent doit identifier les mécanismes macro de rollback, les outils éventuels, le point de non-retour, puis construire et tester les outils de retour arrière.

## Livrable produit

Le livrable attendu est une stratégie de déploiement.

Elle doit préciser :

- le mode de déploiement ;
- les étapes ;
- les responsabilités ;
- les outils ;
- la traçabilité ;
- le support ;
- la communication ;
- la formation ;
- les modalités de retour utilisateur ;
- le passage éventuel en mode produit.
- les modalités de cut over ;
- les mécanismes de rollback ;
- la checklist et le chronogramme.

## Critères de qualité

- La stratégie est validée par les parties prenantes concernées.
- Elle utilise les procédures standards existantes lorsque c'est pertinent.
- Elle est reliée à l'analyse d'impact et à l'analyse de risque.
- Elle contient des actions concrètes, pas seulement des intentions.
- Elle précise comment suivre ce qui est fait, en cours et restant.
- Elle prépare le support durable après le déploiement.
- Elle précise le point de non-retour si la stratégie contient une bascule sensible.
- Elle explicite la logique de mise en production et de mise en service lorsque les deux moments sont distincts.

## Pièges à éviter

- Choisir le big bang sans justification solide.
- Oublier le support utilisateur au lancement.
- Négliger les retours utilisateurs.
- Définir une stratégie sans RACI clair.
- Oublier la transition vers l'assistance et la maintenance.
- Confondre mise en production technique et utilisation opérationnelle par le métier.
- Sous-estimer les efforts de marche en double.
- Prévoir un rollback sans le tester.

## Liens utiles

- [[Déploiement informatique]]
- [[Réaliser une étude d'impact de déploiement]]
- [[Réaliser une analyse de risque de déploiement]]
- [[Migration des données dans un déploiement]]
- [[DevOps et déploiement informatique]]

## Sources

- `Meta/module 1/Deploiement informatique/Formation AMOA - Déploiement Informatique - Agenda.pdf`
- `Meta/module 1/Deploiement informatique/Formation AMOA_Déploiement informatique_v1.1 (3).pdf`

