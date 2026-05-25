# P&PM - Index

## Mission du vault

Ce vault Obsidian, nommé **P&PM** pour **Project and Product Management**, a pour mission de transformer les supports présents dans le dossier `Meta` en un réseau de connaissance actionnable pour un agent spécialisé en AMOA, gestion de projet et gestion de produit.

Le vault ne doit pas devenir une simple bibliothèque de résumés. Il doit devenir une mémoire métier structurée, reliée et exploitable, capable d'aider un agent à comprendre une situation, identifier la phase d'un projet ou d'un produit, demander les informations manquantes, choisir les prochaines actions et produire des livrables de qualité.

## Objectif final

L'objectif final est de créer une base Markdown transférable vers un autre vault opérationnel, où un agent pourra utiliser ces connaissances pour agir dans des outils réels, comme Azure DevOps, et accompagner des activités telles que la rédaction de user stories, la gestion des exigences, la recette métier, le pilotage projet, la conduite du changement ou le product management.

Le contenu doit donc être écrit pour augmenter les capacités d'action d'un agent quelconque, pas seulement pour documenter les cours sources.

## Démarrage agentique

Ce fichier est le point d'entrée du vault. L'agent doit d'abord comprendre la mission, les objectifs et les règles générales ci-dessous.

Une fois cette lecture terminée, l'agent doit poursuivre vers [[P&PM - Travaux]] pour identifier l'action actuelle, les travaux en cours et les prochaines priorités.

L'agent ne doit pas commencer une action de création, modification, déplacement ou suppression sans avoir compris l'action actuelle indiquée dans [[P&PM - Travaux]].

Si l'action actuelle concerne l'ingestion d'un fichier source, l'agent doit ensuite lire [[P&PM - Skill ingestion documentaire]] avant d'ouvrir ou traiter le document source.

## Ce que l'agent doit construire

L'agent doit progressivement construire :

- des notes de compétences actionnables ;
- des notes de notions métier ;
- des notes de méthodes et frameworks ;
- des notes de livrables ;
- des notes de processus chronologiques ;
- des notes d'outils ;
- des liens Obsidian utiles entre ces éléments ;
- une traçabilité entre les connaissances créées et les fichiers sources du dossier `Meta`.

## Principes de travail

- Lire les fichiers sources entièrement avant d'en extraire la connaissance.
- Raisonner en termes de capacité ajoutée au cerveau de l'agent.
- Transformer le contenu source en notes Markdown utilisables dans l'action.
- Préférer l'amélioration d'une note existante à la création d'un doublon.
- Créer une nouvelle note seulement si elle représente une compétence, une notion, un livrable, une méthode ou une étape réellement distincte.
- Relier les notes avec des liens Obsidian explicites.
- Maintenir une vision chronologique du cycle de vie projet et produit.
- Garder les fichiers de pilotage à jour lorsque l'utilisateur le demande ou lorsqu'un jalon significatif est atteint.

## Synchronisation GitHub

Le vault P&PM doit être synchronisé avec le dépôt GitHub suivant :

`https://github.com/ELMASRY-MOAMEN/2PM.git`

Quand l'utilisateur demande à l'agent de `commit + push`, `commit et push`, `committer et pusher`, ou toute formulation équivalente, l'agent doit utiliser ce dépôt comme remote GitHub officiel du projet.

Avant de committer, l'agent doit vérifier les changements en cours pour ne pas inclure accidentellement des modifications qui ne relèvent pas de sa mission.

Avant de pousser, l'agent doit vérifier que le remote pointe bien vers `ELMASRY-MOAMEN/2PM.git`.

Si le dépôt local n'est pas encore initialisé, l'agent doit initialiser Git dans la racine du vault, puis configurer le remote `origin` vers `https://github.com/ELMASRY-MOAMEN/2PM.git`.

## Règles d'ingestion des sources

Pour chaque fichier source dans `Meta`, l'agent doit :

1. Identifier le fichier et sa thématique.
2. Lire le contenu exploitable.
3. Déterminer les compétences, savoirs, méthodes, livrables et notions qu'il contient.
4. Vérifier si des notes existantes couvrent déjà ces éléments.
5. Créer les nouvelles notes nécessaires.
6. Modifier ou enrichir les notes existantes lorsque c'est plus pertinent.
7. Ajouter les liens Obsidian nécessaires.
8. Documenter l'avancement dans [[P&PM - Travaux]].

## Règles anti-doublons

Avant de créer une note, l'agent doit chercher si une note proche existe déjà.

Si une note existe déjà mais qu'elle est trop succincte, l'agent doit l'améliorer au lieu de créer un doublon.

Si deux concepts semblent proches mais ne sont pas identiques, l'agent doit clarifier leur différence dans les notes concernées et créer des liens entre elles.

## Règles de contenu actionnable

Une note est actionnable si elle aide un agent à répondre à au moins une des questions suivantes :

- Quand utiliser cette connaissance ?
- Dans quelle phase du projet ou du produit se situe-t-elle ?
- Quelles informations faut-il demander avant d'agir ?
- Quelles étapes suivre ?
- Quel livrable produire ?
- Quels critères de qualité vérifier ?
- Quels risques ou pièges éviter ?
- Quelles notions liées faut-il connaître ?

## Règles de traçabilité

Chaque note issue d'un fichier source doit conserver une trace de son origine lorsque c'est utile.

La trace peut prendre la forme d'une section `Sources`, d'un lien vers une note source, ou d'une mention du fichier d'origine.

Le registre principal d'avancement est indiqué dans le prochain fichier de lecture : [[P&PM - Travaux]].
