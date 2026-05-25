# P&PM - Skill ingestion documentaire

## Rôle de ce skill

Ce skill décrit la procédure obligatoire pour ingérer un document source du dossier `Meta` dans le réseau de connaissance P&PM.

L'objectif n'est pas de produire un résumé. L'objectif est de transformer un document source en connaissances Markdown actionnables, reliées et réutilisables par un agent en gestion de produit, gestion de projet et AMOA.

## Quand utiliser ce skill

L'agent doit utiliser ce skill avant d'ingérer chaque fichier listé dans [[P&PM - Travaux]].

L'agent doit aussi l'utiliser lorsqu'il améliore une note existante à partir d'une nouvelle source.

## Entrées attendues

- Un fichier source du dossier `Meta`.
- La ligne correspondante dans le registre d'ingestion de [[P&PM - Travaux]].
- Les notes Markdown déjà présentes dans `Product Management`, `Project Management` et `Transverses`.

## Sorties attendues

- Une ou plusieurs notes Markdown créées, modifiées ou reliées.
- Des liens Obsidian utiles entre les notes.
- Une trace de la source utilisée.
- Une ligne mise à jour dans [[P&PM - Travaux]].
- Une demande de validation humaine lorsque le seuil de validation est atteint.

## Règles fondamentales

- Lire le document entièrement avant de décider quoi créer ou modifier.
- Ne jamais créer une note sans chercher si une note équivalente existe déjà.
- Améliorer une note existante plutôt que créer un doublon.
- Penser en capacités pour agent : comprendre, décider, demander, produire, vérifier, agir.
- Placer les connaissances produit dans `Product Management`.
- Placer les connaissances projet dans `Project Management`.
- Placer les connaissances communes dans `Transverses`.
- Garder les sources traçables.
- Mettre à jour [[P&PM - Travaux]] après chaque ingestion.

## Étape 1 - Préparer l'ingestion

Avant de lire le fichier source, l'agent doit :

1. Lire [[P&PM - Index]].
2. Lire [[P&PM - Travaux]].
3. Identifier la prochaine ligne `A faire` ou `En cours` dans le registre d'ingestion.
4. Lire ce skill.
5. Vérifier si une validation humaine est requise avant de continuer.

## Étape 2 - Identifier le document source

Pour le fichier cible, l'agent doit identifier :

- chemin du fichier ;
- type de fichier ;
- module source ;
- thème apparent ;
- domaine cible probable ;
- niveau de difficulté d'ingestion ;
- éventuel blocage technique.

Si le fichier est illisible ou incomplet, l'agent ne doit pas inventer son contenu. Il marque la ligne comme `Bloque` dans [[P&PM - Travaux]] et indique la raison.

## Étape 3 - Lire entièrement le document

L'agent doit lire le document en entier, en distinguant :

- concepts ;
- méthodes ;
- étapes de processus ;
- livrables ;
- exemples ;
- exercices ;
- templates ;
- règles de qualité ;
- pièges ou erreurs à éviter ;
- informations purement contextuelles peu réutilisables.

## Étape 4 - Extraire les unités de connaissance

Après lecture, l'agent doit lister les unités de connaissance candidates :

- compétences actionnables ;
- notions ;
- méthodes ;
- processus ;
- outils ;
- livrables ;
- modèles ;
- checklists ;
- décisions ou arbitrages ;
- liens avec d'autres connaissances.

Chaque unité doit être évaluée selon sa valeur pour un agent : peut-elle aider à agir, conseiller, produire ou vérifier ?

## Étape 5 - Décider quoi créer, modifier ou relier

Pour chaque unité de connaissance :

1. Chercher une note existante proche.
2. Si une note existe, l'enrichir.
3. Si aucune note n'existe, créer une nouvelle note.
4. Si l'information est seulement un exemple, l'ajouter à la note pertinente.
5. Si l'information contredit ou nuance une note existante, ajouter la nuance avec prudence.
6. Relier la note aux notions, compétences, livrables ou phases concernées.

## Étape 6 - Rédiger les notes Markdown

Une note doit être claire, courte quand c'est possible, et orientée action.

Une compétence doit contenir :

- objectif ;
- quand l'utiliser ;
- informations nécessaires ;
- étapes à suivre ;
- livrables produits ;
- critères de qualité ;
- pièges à éviter ;
- liens utiles.

Une notion doit contenir :

- définition ;
- rôle dans P&PM ;
- exemples ;
- notions proches ;
- liens utiles.

Un livrable doit contenir :

- objectif ;
- moment d'utilisation ;
- structure recommandée ;
- données nécessaires ;
- critères de qualité ;
- liens avec les compétences qui le produisent.

Un processus doit contenir :

- déclencheur ;
- étapes ;
- acteurs ;
- entrées ;
- sorties ;
- points de décision ;
- critères de passage à l'étape suivante.

## Étape 7 - Relier les notes

L'agent doit ajouter des liens Obsidian intentionnels.

Les liens doivent aider un futur agent à naviguer entre :

- une phase et ses compétences ;
- une compétence et ses notions ;
- une compétence et ses livrables ;
- une méthode et ses cas d'usage ;
- un outil et les actions qu'il permet ;
- une source et les notes qu'elle a alimentées.

## Étape 8 - Validation humaine

L'agent doit demander une validation humaine dans les cas suivants :

- première ingestion complète d'un nouveau grand domaine ;
- avant de créer les notes issues d'une ingestion, en présentant les notes envisagées, leur emplacement, leur type et les informations qui seront ajoutées ;
- création ou modification d'une structure de dossiers ;
- fusion de notes existantes ;
- suppression d'une note ;
- arbitrage entre `Product Management`, `Project Management` et `Transverses` ;
- ingestion d'un document très volumineux qui crée beaucoup de notes ;
- incertitude sur la granularité des notes à produire.

Sans validation humaine, l'agent peut continuer les ingestions simples qui respectent une structure déjà validée.

## Étape 9 - Mettre à jour le pilotage

Après l'ingestion, l'agent doit mettre à jour [[P&PM - Travaux]] :

- statut du fichier ;
- cases d'étapes cochées ;
- notes créées ;
- notes modifiées ;
- validation humaine si demandée ou obtenue ;
- blocages ou points à revoir.

L'agent met à jour [[P&PM - Change Log]] uniquement pour les changements significatifs.

L'agent met à jour [[P&PM - Mémoire vivante]] lorsqu'une leçon durable est apprise de l'utilisateur.

## Checklist de fin d'ingestion

- [ ] Le fichier source a été lu entièrement.
- [ ] Les unités de connaissance ont été extraites.
- [ ] Les notes existantes ont été recherchées.
- [ ] Les notes nécessaires ont été créées ou modifiées.
- [ ] Les liens Obsidian utiles ont été ajoutés.
- [ ] La source est traçable.
- [ ] Le registre dans [[P&PM - Travaux]] est mis à jour.
- [ ] La validation humaine a été demandée si nécessaire.

## Erreurs à éviter

- Résumer sans transformer en connaissance actionnable.
- Créer une note par document sans réflexion.
- Dupliquer une note existante.
- Oublier les liens Obsidian.
- Mélanger produit et projet alors qu'un contenu doit aller dans `Transverses`.
- Marquer une ingestion terminée sans avoir mis à jour [[P&PM - Travaux]].
