# P&PM - Mémoire vivante

## Rôle de ce fichier

Ce fichier conserve les leçons apprises par l'agent au contact de l'utilisateur pendant le projet P&PM.

Il sert à éviter que l'utilisateur doive répéter deux fois les mêmes corrections, préférences ou règles de méthode.

## Règles d'utilisation

- Ajouter une leçon lorsqu'une correction utilisateur révèle une règle durable.
- Ajouter une préférence lorsqu'elle influence les futures actions dans le vault.
- Ajouter une erreur à ne pas répéter lorsqu'une action ou hypothèse de l'agent a été corrigée.
- Garder les formulations concrètes et applicables.
- Ne pas transformer ce fichier en journal complet de conversation.

## Préférences utilisateur

| Date | Préférence | Conséquence pour l'agent |
|---|---|---|
| 2026-05-25 | Nommer le vault P&PM pour Project and Product Management | Utiliser P&PM comme nom de référence du projet et du vault de connaissance |
| 2026-05-25 | Produire des fichiers Markdown dans Obsidian | Créer et modifier les connaissances au format `.md` avec liens internes |
| 2026-05-25 | Construire une base transposable vers un autre vault opérationnel | Rédiger des notes génériques, actionnables et non dépendantes uniquement du contexte de formation |
| 2026-05-25 | Synchroniser le projet avec le repo GitHub `ELMASRY-MOAMEN/2PM.git` | Utiliser ce dépôt comme destination officielle quand l'utilisateur demande un commit + push |

## Leçons apprises

| Date | Sujet | Leçon | Conséquence pour les prochaines actions |
|---|---|---|---|
| 2026-05-25 | Ingestion des sources | Ne pas créer systématiquement une nouvelle note par document source | Toujours chercher si une note existante peut être enrichie avant d'en créer une nouvelle |
| 2026-05-25 | Qualité des notes | Une note doit augmenter la capacité d'action d'un agent | Inclure les étapes, informations à demander, critères de qualité, pièges et liens utiles lorsque c'est pertinent |
| 2026-05-25 | Vision projet-produit | Le vault doit soutenir une lecture chronologique en entonnoir | Construire des parcours qui aident l'agent à savoir où il se situe et quelles prochaines actions mener |
| 2026-05-25 | Usage agentique | Les connaissances devront guider des actions réelles dans des outils comme Azure DevOps | Rédiger les compétences comme des procédures exploitables et pas seulement comme des définitions |
| 2026-05-25 | Lecture des fichiers de pilotage | Ne pas présenter trop tôt tous les fichiers de pilotage à l'agent | Organiser la lecture en chaînage progressif ou en poupée russe selon le contexte |
| 2026-05-25 | Architecture du vault | Séparer les dossiers racine en `Product Management`, `Project Management` et `Transverses` | Utiliser `Transverses` pour les savoirs communs afin d'éviter de dupliquer entre produit et projet |
| 2026-05-25 | Ingestion documentaire | Chaque fichier source de `Meta` doit être représenté dans [[P&PM - Travaux]] avec des cases de contrôle | L'agent doit suivre les étapes visibles dans le registre et ne pas déclarer une ingestion terminée sans preuve de complétude |
| 2026-05-25 | Validation avant création | Avant de créer les fichiers issus d'une ingestion, l'agent doit dire ce qu'il a fait, ce qu'il va créer et quels types d'informations seront ajoutés | Présenter l'intention de création et attendre validation humaine avant d'écrire les notes |

## Erreurs à ne pas répéter

| Date | Erreur | Correction attendue | Règle retenue |
|---|---|---|---|
| 2026-05-25 | Réduire le projet à la création de nouvelles notes | Intégrer aussi la modification, l'amélioration et la consolidation de notes existantes | L'ingestion est un processus évolutif qui crée, modifie et relie |
| 2026-05-25 | Penser uniquement en logique documentaire | Penser en compétences, savoirs actionnables et automatisation de parcours | Chaque note doit servir la décision ou l'action d'un agent |
| 2026-05-25 | Exposer tous les fichiers de pilotage dès l'Index | Guider l'agent vers le prochain fichier utile seulement au bon moment | La navigation de pilotage doit être progressive |
| 2026-05-25 | Créer des notes d'ingestion sans annoncer le contenu prévu | Annoncer d'abord les notes proposées, leur emplacement et leur type d'information | La validation humaine doit précéder la création des notes issues d'une ingestion |

## Standards de qualité du projet

- Les notes doivent être utiles pour agir.
- Les liens Obsidian doivent être intentionnels.
- Les doublons doivent être évités.
- Les sources doivent rester traçables.
- Les contenus doivent pouvoir être déplacés dans un autre vault.
- Les compétences doivent être décrites comme des étapes suivables.
- Les notions doivent être définies clairement et reliées aux notions voisines.
- Les livrables doivent préciser leur objectif, leur moment d'utilisation, leur structure et leurs critères de qualité.

## Décisions méthodologiques stables

| Date | Décision | Effet sur le projet |
|---|---|---|
| 2026-05-25 | Créer 4 fichiers racine de pilotage | Tout agent doit commencer par les lire avant d'agir |
| 2026-05-25 | Utiliser [[P&PM - Travaux]] comme cockpit opérationnel | Les actions en cours, terminées et à venir sont pilotées depuis ce fichier |
| 2026-05-25 | Utiliser [[P&PM - Change Log]] comme historique synthétique | Les changements importants sont conservés sans créer un dump |
| 2026-05-25 | Utiliser [[P&PM - Mémoire vivante]] comme mémoire de leçons | Les corrections de l'utilisateur deviennent des règles durables |
| 2026-05-25 | Utiliser `https://github.com/ELMASRY-MOAMEN/2PM.git` comme remote officiel | Les futurs commit + push doivent cibler ce repo |
| 2026-05-25 | Créer une première arborescence hypothétique avant ingestion | La structure initiale peut orienter le travail, mais doit rester ajustable selon les contenus réellement lus |
| 2026-05-25 | Créer [[P&PM - Skill ingestion documentaire]] à la racine | L'agent doit lire ce skill avant toute ingestion de source |
