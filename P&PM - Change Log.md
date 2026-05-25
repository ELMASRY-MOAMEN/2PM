# P&PM - Change Log

## Rôle de ce fichier

Ce fichier conserve l'historique synthétique des changements importants réalisés dans le vault P&PM.

Il sert à comprendre comment le réseau de connaissance évolue, quelles décisions structurantes ont été prises et quels impacts elles ont eu sur le projet.

Si l'agent a besoin de connaître les préférences utilisateur, les erreurs à ne pas répéter ou les règles apprises en cours de route, il doit ensuite lire [[P&PM - Mémoire vivante]].

## Règles de mise à jour

- Mettre à jour ce fichier lorsque l'utilisateur le demande.
- Mettre à jour ce fichier lorsqu'un jalon significatif est atteint.
- Ne pas noter chaque micro-action sans impact.
- Préférer les changements utiles pour comprendre l'évolution du vault.
- Mentionner les fichiers concernés lorsque c'est pertinent.

## Règles de chunking hebdomadaire

A la fin de chaque semaine, l'agent doit nettoyer la section de la semaine en cours :

1. Regrouper les changements similaires.
2. Supprimer les détails sans valeur durable.
3. Conserver les créations, modifications, suppressions, décisions et impacts importants.
4. Produire une synthèse hebdomadaire courte.
5. Déplacer la synthèse dans la section `Archives synthétiques par semaine`.

Le but est d'éviter que ce fichier devienne un dump illisible.

## Semaine en cours

### 2026-W22

| Date | Type | Changement | Impact | Fichiers concernés |
|---|---|---|---|---|
| 2026-05-25 | Initialisation | Création prévue des fichiers de pilotage racine du vault P&PM | Donne à l'agent un point d'entrée, un tableau de travaux, un historique et une mémoire vivante | [[P&PM - Index]], [[P&PM - Travaux]], [[P&PM - Change Log]], [[P&PM - Mémoire vivante]] |
| 2026-05-25 | Git | Initialisation locale du dépôt Git et configuration du remote `origin` vers `https://github.com/ELMASRY-MOAMEN/2PM.git` | Prépare les futurs commit + push vers le repo officiel du projet | [[P&PM - Index]], [[P&PM - Travaux]] |
| 2026-05-25 | Pilotage | Ajustement de la lecture des fichiers de pilotage en chaînage progressif | Evite que l'agent lise trop tôt des fichiers qui ne sont pas encore nécessaires à son contexte | [[P&PM - Index]], [[P&PM - Travaux]], [[P&PM - Change Log]] |
| 2026-05-25 | Architecture | Création de la première arborescence de connaissance sous `Product Management`, `Project Management` et `Transverses` | Donne une première séparation entre cycles produit, cycles projet et savoirs réutilisables | `Product Management`, `Project Management`, `Transverses`, [[P&PM - Travaux]] |
| 2026-05-25 | Ingestion | Création de [[P&PM - Skill ingestion documentaire]] et ajout des 126 fichiers sources de `Meta` au registre d'ingestion | Donne à l'agent une procédure et une checklist par fichier source avant toute ingestion | [[P&PM - Skill ingestion documentaire]], [[P&PM - Travaux]], [[P&PM - Index]] |

## Archives synthétiques par semaine

Les synthèses hebdomadaires seront ajoutées ici après chunking.

## Changements structurants

| Date | Changement | Raison | Impact |
|---|---|---|---|
| 2026-05-25 | Le vault est défini comme P&PM, une base de connaissance actionnable pour agents | Le contenu devra être transférable vers un autre vault opérationnel | Les notes doivent guider l'action, pas seulement expliquer les concepts |
| 2026-05-25 | Le repo GitHub officiel du projet est `ELMASRY-MOAMEN/2PM.git` | Les futurs commit + push doivent aller vers un dépôt unique et explicite | L'agent doit vérifier le remote avant de pousser |
| 2026-05-25 | L'architecture racine distingue `Product Management`, `Project Management` et `Transverses` | Les cycles produit et projet sont différents, mais plusieurs savoirs sont partagés | Les notes communes doivent aller dans `Transverses` pour limiter les doublons |

## Décisions importantes

| Date | Décision | Conséquence |
|---|---|---|
| 2026-05-25 | Les fichiers produits seront en Markdown | Les connaissances seront directement exploitables dans Obsidian |
| 2026-05-25 | Les notes existantes devront être améliorées plutôt que dupliquées | L'ingestion doit rester incrémentale et éviter la fragmentation inutile |
| 2026-05-25 | Le vault doit soutenir des actions one-shot et des parcours long-run | Une vue chronologique projet-produit devra être construite |
| 2026-05-25 | La lecture entre fichiers de pilotage doit être progressive | Les fichiers doivent guider vers le prochain fichier utile selon le besoin, pas exposer toute la structure trop tôt |
| 2026-05-25 | Les dossiers de connaissance peuvent être créés avant l'ingestion exhaustive | Une première hypothèse d'architecture aide à orienter les futures notes, mais reste ajustable après lecture des sources |
| 2026-05-25 | Chaque fichier source de `Meta` doit avoir une ligne de suivi dans [[P&PM - Travaux]] | L'ingestion doit être pilotée fichier par fichier avec cases de contrôle | L'agent ne peut pas marquer une source terminée sans passer par le skill et mettre à jour le registre |
