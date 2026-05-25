# Migration des données dans un déploiement

## Objectif

Préparer, exécuter et vérifier la migration des données lorsqu'un [[Déploiement informatique]] implique une refonte, une nouvelle application, une montée de version ou un changement de modèle de données.

## Quand l'utiliser

Utiliser cette compétence dès qu'un déploiement doit reprendre des données existantes, transformer des données, initialiser de nouvelles données ou garantir une continuité métier entre ancien et nouveau système.

Dans certains contextes, la migration des données devient un sous-projet à part entière.

## Pourquoi c'est important

Une migration mal préparée peut bloquer la mise en service, dégrader la confiance métier, créer des erreurs opérationnelles et rendre le retour arrière plus complexe.

La migration des données est un enjeu métier : le métier doit être intégré au chantier et peut en être le pilote.

## Entrées nécessaires

- périmètre des données à migrer ;
- ancien modèle de données ;
- nouveau modèle de données ;
- règles métier de transformation ;
- tables de correspondance ;
- contraintes de qualité des données ;
- stratégie de déploiement ;
- calendrier de cut over ;
- acteurs métier, IT et data.

## Étapes à suivre

1. Identifier les données à reprendre, transformer ou abandonner.
2. Définir les tables de correspondance entre ancienne et nouvelle application.
3. Identifier les règles de transformation métier.
4. Décider si la migration doit être manuelle, semi-automatisée ou automatisée.
5. Créer les scripts ou outils nécessaires lorsque l'automatisation est retenue.
6. Planifier plusieurs tirs à blanc.
7. Tester les résultats de migration.
8. Vérifier les écarts avec le métier.
9. Prévoir l'initialisation éventuelle de nouvelles données.
10. Intégrer la migration dans le chronogramme de déploiement.
11. Prévoir les critères de go/no-go liés aux données.
12. Documenter les contrôles et les responsabilités.

## Livrables produits

- stratégie de migration des données ;
- mapping ou tables de correspondance ;
- scripts ou procédures de migration ;
- plan de tirs à blanc ;
- PV ou rapport de contrôle de migration ;
- critères de go/no-go liés aux données.

## Critères de qualité

- Le métier valide les règles de transformation.
- Les tirs à blanc sont réalisés suffisamment tôt.
- Les contrôles portent sur la complétude, la cohérence et l'utilisabilité métier.
- Les anomalies de données sont suivies et corrigées.
- La migration est intégrée au plan de déploiement.
- Les responsabilités sont claires pendant le cut over.

## Pièges à éviter

- Traiter la migration comme un détail technique.
- Oublier les données à initialiser dans la nouvelle solution.
- Faire un seul tir à blanc trop tard.
- Ne pas impliquer le métier dans la validation.
- Ne pas prévoir de décision go/no-go spécifique aux données.

## Liens utiles

- [[Déploiement informatique]]
- [[Définir une stratégie de déploiement]]
- [[Réaliser une analyse de risque de déploiement]]

## Sources

- `Meta/module 1/Deploiement informatique/Formation AMOA_Déploiement informatique_v1.1 (3).pdf`

