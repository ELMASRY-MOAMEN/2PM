# P&PM - Travaux

## Rôle de ce fichier

Ce fichier est le tableau de pilotage opérationnel du projet P&PM.

Tout agent qui intervient dans ce vault doit le lire après [[P&PM - Index]] afin de comprendre ce qui a déjà été fait, ce qui reste à faire, et quelle action doit être travaillée maintenant.

Si l'agent a besoin de comprendre les décisions et changements passés avant d'agir, il doit ensuite lire [[P&PM - Change Log]]. Sinon, il peut travailler directement sur l'action actuelle.

## Statuts utilisés

| Statut | Signification |
|---|---|
| A faire | Action identifiée mais non commencée |
| En cours | Action actuellement travaillée |
| Termine | Action réalisée et vérifiée |
| Bloque | Action impossible sans décision ou information supplémentaire |
| A revoir | Action réalisée mais nécessitant une amélioration |

## Action actuelle de l'agent

| Champ | Valeur |
|---|---|
| Priorité actuelle | Ingérer la prochaine source listée dans le registre `Meta` |
| Dossier ou fichier cible | `Meta/module 1/Deploiement informatique/TimeLine-Upgrade_GO LIVE projection go live_V4.xlsx` |
| Objectif immédiat | Lire [[P&PM - Skill ingestion documentaire]], analyser la prochaine source du registre et présenter les notes envisagées avant création |
| Critère de fin | La prochaine source est ingérée, les notes utiles sont créées ou modifiées après validation, et la ligne correspondante du registre est mise à jour |
| Prochaine étape après finition | Continuer avec la ligne suivante `A faire` dans le registre d'ingestion |

## Backlog des travaux

| ID | Statut | Priorité | Type | Objet | Description | Critère d'acceptation | Dépendance | Dernière mise à jour |
|---|---|---|---|---|---|---|---|---|
| PPM-001 | Termine | Haute | Initialisation | Fichiers de pilotage | Créer les 4 fichiers racine qui guident l'agent dans le projet P&PM | Les 4 fichiers existent à la racine du vault et se référencent entre eux | Aucune | 2026-05-25 |
| PPM-002 | Termine | Haute | Méthode | Protocole d'ingestion | Définir comment lire, analyser, découper, créer et améliorer les notes à partir des fichiers sources | [[P&PM - Skill ingestion documentaire]] existe à la racine et décrit le flow d'ingestion | PPM-001 | 2026-05-25 |
| PPM-003 | Termine | Haute | Inventaire | Cartographie du dossier Meta | Produire un inventaire exploitable des fichiers sources par module, thème, type et priorité d'ingestion | Les 126 fichiers sources de `Meta` sont listés dans le registre d'ingestion | PPM-002 | 2026-05-25 |
| PPM-004 | Termine | Haute | Architecture | Arborescence cible du vault | Définir les dossiers de connaissance actionnable, notamment parcours chronologique, compétences, notions, livrables, méthodes et sources | Une première arborescence est créée dans `Product Management`, `Project Management` et `Transverses` | PPM-002 | 2026-05-25 |
| PPM-005 | En cours | Haute | Ingestion | Premier fichier source | Lire entièrement le premier fichier du registre, puis créer ou améliorer les notes Markdown utiles | Le fichier source est traité, tracé et relié aux notes créées ou modifiées, après validation humaine de première ingestion | PPM-003, PPM-004 | 2026-05-25 |
| PPM-006 | A faire | Moyenne | Qualité | Règles anti-doublons | Mettre en place une règle opérationnelle pour éviter les notes redondantes pendant l'ingestion | Les agents savent rechercher, enrichir ou fusionner les notes avant d'en créer de nouvelles | PPM-002 | 2026-05-25 |
| PPM-007 | A faire | Moyenne | Pilotage | Vue chronologique projet-produit | Construire une première vue entonnoir du cycle de vie projet et produit | L'agent peut situer une demande dans une phase et identifier les prochaines actions possibles | PPM-004 | 2026-05-25 |
| PPM-008 | Termine | Haute | Git | Synchronisation GitHub | Initialiser Git localement et configurer le remote officiel du projet | Le remote `origin` pointe vers `https://github.com/ELMASRY-MOAMEN/2PM.git` et l'Index indique la règle commit + push | PPM-001 | 2026-05-25 |

## Registre d'ingestion des sources Meta

Ce registre liste tous les fichiers sources exploitables présents dans `Meta`. Chaque ligne doit être traitée avec [[P&PM - Skill ingestion documentaire]] avant d'être marquée `Termine`.

Règle de complétude : une source ne peut passer à `Termine` que si toutes les colonnes de contrôle nécessaires sont cochées ou explicitement justifiées.

| ID | Statut | Priorité | Source | Type | Domaine cible pressenti | Lecture complète | Extraction unités | Recherche anti-doublon | Création ou modification | Linkage Obsidian | Validation humaine | Pilotage mis à jour | Notes créées ou modifiées | Commentaire |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| SRC-001 | Termine | Moyenne | `Meta/module 1/Deploiement informatique/Formation AMOA - Déploiement Informatique - Agenda.pdf` | pdf | Project Management/06 - Deploiement et conduite du changement | [x] | [x] | [x] | [x] | [x] | Validée par l'utilisateur avant création | [x] | [[Déploiement informatique]], [[Réaliser une étude d'impact de déploiement]], [[Réaliser une analyse de risque de déploiement]], [[Définir une stratégie de déploiement]] | Première ingestion complète. Source conservée comme preuve et traçabilité après extraction des fiches actionnables. |
| SRC-002 | Termine | Moyenne | `Meta/module 1/Deploiement informatique/Formation AMOA_Déploiement informatique_v1.1 (3).pdf` | pdf | Project Management/06 - Deploiement et conduite du changement | [x] | [x] | [x] | [x] | [x] | Validée par l'utilisateur avant création/modification | [x] | [[Déploiement informatique]], [[Définir une stratégie de déploiement]], [[Migration des données dans un déploiement]], [[DevOps et déploiement informatique]] | Support complet utilisé pour enrichir les notes existantes et créer deux notes distinctes sur migration des données et DevOps. |
| SRC-003 | A faire | Moyenne | `Meta/module 1/Deploiement informatique/TimeLine-Upgrade_GO LIVE projection go live_V4.xlsx` | xlsx | Project Management | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-004 | A faire | Haute | `Meta/module 1/Recette métierr/AMOA_Les tests métier_V1.04 (3).pdf` | pdf | Project Management | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-005 | A faire | Haute | `Meta/module 1/Recette métierr/M2-Tests-EXO3-Defects-Énoncé-V1.3 (1).pdf` | pdf | Project Management | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-006 | A faire | Haute | `Meta/module 1/Recette métierr/M2-Tests-EXO3-Defects-V1.3 (2).xlsx` | xlsx | Project Management | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-007 | A faire | Haute | `Meta/module 1/Test/02-ISTQB_CTFL_Syllabus-v4.0_FR_1.0 (1).pdf` | pdf | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-008 | A faire | Haute | `Meta/module 1/Test/05 - Présentation de Squash_v2.0 (1).pdf` | pdf | Transverses/06 - Outils SI et collaboration | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-009 | A faire | Haute | `Meta/module 1/Test/EQL-M1-2025 -J5- Pilotage et bilan (2).pdf` | pdf | Transverses/07 - Data BI et bases de donnees | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-010 | A faire | Haute | `Meta/module 1/Test/EQL-M1-2025-01-Fondamentaux du Test (8).pdf` | pdf | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-011 | A faire | Haute | `Meta/module 1/Test/EQL-M1-2025-02-SquashTM, Exigence et cas de test (8).pdf` | pdf | Transverses/03 - Exigences et specifications | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-012 | A faire | Haute | `Meta/module 1/Test/EQL-M1-2025-03-Conception des cas de test (7).pdf` | pdf | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-013 | A faire | Haute | `Meta/module 1/Test/EQL-M1-2025-04-Exécution des tests (4).pdf` | pdf | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-014 | A faire | Haute | `Meta/module 1/Test/Exemple de rapport de synthèse de campagne-20260217.zip` | zip | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-015 | A faire | Haute | `Meta/module 1/Test/Exemple_bug_évitable_crash_pétrolier_Avril_2020 (1).pdf` | pdf | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-016 | A faire | Haute | `Meta/module 1/Test/Exercice Enregistrement passager - corrigéPAD (1).xlsx` | xlsx | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-017 | A faire | Haute | `Meta/module 1/Test/Exercice Enregistrement passager - ÉnoncéStagiaires (2).xlsx` | xlsx | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-018 | A faire | Haute | `Meta/module 1/Test/Générateur_JDD_Nom_Prénom_Téléphone_v1.0 (3).xlsx` | xlsx | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-019 | A faire | Haute | `Meta/module 1/Test/Glossaire-des-tests-logiciels-v3_2F-ISTQB-CFTL (1).pdf` | pdf | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-020 | A faire | Haute | `Meta/module 1/Test/Les 11 bugs les plus célèbres (1).pdf` | pdf | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-021 | A faire | Haute | `Meta/module 1/Test/Les normes ISO sur la Qualité Logicielle-20260217.zip` | zip | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-022 | A faire | Haute | `Meta/module 1/Test/Majeur_ou_pas (2).xlsx` | xlsx | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-023 | A faire | Haute | `Meta/module 1/Test/Matrice_d_opportunité_TNR (2).xlsx` | xlsx | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-024 | A faire | Haute | `Meta/module 1/Test/PICT_Manuel_FR (1).pdf` | pdf | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-025 | A faire | Haute | `Meta/module 1/Test/TEST DE TRANSITION D ÉTATS (1).pdf` | pdf | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-026 | A faire | Haute | `Meta/module 1/Test/TP REFONTE TOTO - RESSOURCES (Stagiaires)-20260217.zip` | zip | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-027 | A faire | Haute | `Meta/module 1/Test/TP_MODULE1 (3).pdf` | pdf | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-028 | A faire | Haute | `Meta/module 1/tester avec l'IA/04-08-2025 - IA Intro - J1 (1).pdf` | pdf | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-029 | A faire | Haute | `Meta/module 1/tester avec l'IA/04-08-2025-J2_ Pratiques_IA_en_entreprise (1).pdf` | pdf | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-030 | A faire | Haute | `Meta/module 1/tester avec l'IA/1900-2022_Evol_loi_de_Moore (1).pdf` | pdf | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-031 | A faire | Haute | `Meta/module 1/tester avec l'IA/Charte de test_exploratoire (2).json` | json | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-032 | A faire | Haute | `Meta/module 1/tester avec l'IA/ChatGPT_Exemple_Prompt Complétion (1).pdf` | pdf | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-033 | A faire | Haute | `Meta/module 1/tester avec l'IA/ECMA-404 (1).pdf` | pdf | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-034 | A faire | Haute | `Meta/module 1/tester avec l'IA/ERREUR DE LIA - Test des instructions.pdf` | pdf | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-035 | A faire | Haute | `Meta/module 1/tester avec l'IA/Evolution_Loi-de-Moore.pdf` | pdf | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-036 | A faire | Haute | `Meta/module 1/tester avec l'IA/Index des termes IA-2 (1).pdf` | pdf | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-037 | A faire | Haute | `Meta/module 1/tester avec l'IA/J1-Tester avec lIA_Histoire de l_IA (1).pdf` | pdf | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-038 | A faire | Haute | `Meta/module 1/tester avec l'IA/J2_ JSON un format adapté aux échanges IA (1).pdf` | pdf | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-039 | A faire | Haute | `Meta/module 1/tester avec l'IA/Note méthodologique (exemple).pdf` | pdf | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-040 | A faire | Haute | `Meta/module 1/tester avec l'IA/Prompt basique_J2 (1).pdf` | pdf | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-041 | A faire | Haute | `Meta/module 1/tester avec l'IA/PROMPT RÉINITIALISATION RÉVISÉ.pdf` | pdf | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-042 | A faire | Haute | `Meta/module 1/tester avec l'IA/prompt_créa_liste charte de test (1).txt` | txt | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-043 | A faire | Haute | `Meta/module 1/tester avec l'IA/Prompt_Tests_exploratoires.txt` | txt | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-044 | A faire | Haute | `Meta/module 1/tester avec l'IA/TALOS ET GOLEM (1).pdf` | pdf | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-045 | A faire | Haute | `Meta/module 1/tester avec l'IA/TOUT JSON EN 7 SCHÉMAS.pdf` | pdf | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-046 | A faire | Haute | `Meta/module 1/tester avec l'IA/UTLISER - et SIMULER - LES PARAMÈTRES IA (1).pdf` | pdf | Transverses/04 - Tests et qualite logicielle | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-047 | A faire | Moyenne | `Meta/Module 2/accompagner le changement informatique/Accompagner changement informatique_V1.1 (3).pdf` | pdf | Project Management/06 - Deploiement et conduite du changement | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-048 | A faire | Moyenne | `Meta/Module 2/accompagner le changement informatique/ChangeManagement-Fiches technicités-V0.7 (2).pdf` | pdf | Project Management/06 - Deploiement et conduite du changement | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-049 | A faire | Moyenne | `Meta/Module 2/accompagner le changement informatique/congés-analyse impact (2).xlsx` | xlsx | Project Management/06 - Deploiement et conduite du changement | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-050 | A faire | Moyenne | `Meta/Module 2/accompagner le changement informatique/M6-Change-Congés-EXO1-Brief AMO-V0.6 (1).pdf` | pdf | Project Management/06 - Deploiement et conduite du changement | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-051 | A faire | Moyenne | `Meta/Module 2/accompagner le changement informatique/M6-Change-Congés-EXO1-Brief Métier-V0.6.pdf` | pdf | Project Management/06 - Deploiement et conduite du changement | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-052 | A faire | Moyenne | `Meta/Module 2/analyse procesus métier/BPMN_et_Draw.io - Les bases.pptx` | pptx | Transverses/02 - Processus metier et BPMN | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-053 | A faire | Moyenne | `Meta/Module 2/analyse procesus métier/ExerciceDiagnosticCible2025.pdf` | pdf | Transverses/11 - IA et agents | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-054 | A faire | Moyenne | `Meta/Module 2/analyse procesus métier/M2_AMOA_AnalyseMétier_2025 (1).pdf` | pdf | Transverses/01 - AMOA et analyse metier | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-055 | A faire | Moyenne | `Meta/Module 2/analyse procesus métier/M2-Processus-DiagnosticCible-Template (2).xlsx` | xlsx | Transverses/02 - Processus metier et BPMN | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-056 | A faire | Moyenne | `Meta/Module 2/analyse procesus métier/M3-Analyse de processus-Check List-V1.0 (2).xlsx` | xlsx | Transverses/02 - Processus metier et BPMN | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-057 | A faire | Moyenne | `Meta/Module 2/analyse procesus métier/QL_M1_02_2024 - ExerciceModélisationProcessus de commande (2).pdf` | pdf | Transverses/02 - Processus metier et BPMN | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-058 | A faire | Moyenne | `Meta/Module 2/analyse procesus métier/Templates_Analyse exercices BPMN (4).xlsx` | xlsx | Transverses/02 - Processus metier et BPMN | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-059 | A faire | Moyenne | `Meta/Module 2/analyse procesus métier/Templates_Analyse exercices BPMN_Pizzaaaa.xlsx` | xlsx | Transverses/02 - Processus metier et BPMN | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-060 | A faire | Moyenne | `Meta/Module 2/API & webservices/API_KEY (5).txt` | txt | Transverses/08 - API webservices et integration | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-061 | A faire | Moyenne | `Meta/Module 2/API & webservices/Cours API v1.0 (4).pdf` | pdf | Transverses/08 - API webservices et integration | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-062 | A faire | Moyenne | `Meta/Module 2/API & webservices/TP_API_REST_TMDB_V1.2 (2).pdf` | pdf | Transverses/08 - API webservices et integration | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-063 | A faire | Haute | `Meta/Module 2/gestin des exigences/2024_AMOA_M2_Gestion des exigences_Intro_ANE (1).pdf` | pdf | Transverses/03 - Exigences et specifications | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-064 | A faire | Haute | `Meta/Module 2/gestin des exigences/M2_AMOA_Exigences_2025.pdf` | pdf | Transverses/03 - Exigences et specifications | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-065 | A faire | Haute | `Meta/Module 2/gestin des exigences/M2-Fiche récapitulative.pdf` | pdf | Transverses/08 - API webservices et integration | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-066 | A faire | Haute | `Meta/Module 2/gestin des exigences/M2-Requirement-EXO-GDR.pdf` | pdf | Transverses/03 - Exigences et specifications | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-067 | A faire | Haute | `Meta/Module 2/gestin des exigences/M4-Requirement-Check List-V1.0 (4).xlsx` | xlsx | Transverses/03 - Exigences et specifications | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-068 | A faire | Haute | `Meta/Module 2/gestin des exigences/Patrice-Gaudin_CDC_CoCoFunds-Enoncé-v04.pdf` | pdf | Transverses/03 - Exigences et specifications | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-069 | A faire | Haute | `Meta/Module 2/gestin des exigences/Patrice-Gaudin_CDC_CoCoFunds-Template-Liste-Exigences-v01 (1).xlsx` | xlsx | Transverses/03 - Exigences et specifications | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-070 | A faire | Haute | `Meta/Module 2/gestin des exigences/Requirement-EXO-Congés.pdf` | pdf | Transverses/03 - Exigences et specifications | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-071 | A faire | Haute | `Meta/Module 2/gestin des exigences/Requirement-EXO2-Congés-Template-V1.2.xlsx` | xlsx | Transverses/03 - Exigences et specifications | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-072 | A faire | Moyenne | `Meta/Module 2/La data  donnée, BDD, BI/DonneesExercicePowerBI (2).zip` | zip | Transverses/07 - Data BI et bases de donnees | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-073 | A faire | Moyenne | `Meta/Module 2/La data  donnée, BDD, BI/DumpDatabase (1).sql` | sql | Transverses/07 - Data BI et bases de donnees | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-074 | A faire | Moyenne | `Meta/Module 2/La data  donnée, BDD, BI/EQL-CoursModule2_Data_0.8 (4).pdf` | pdf | Transverses/07 - Data BI et bases de donnees | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-075 | A faire | Moyenne | `Meta/Module 2/La data  donnée, BDD, BI/Exercice Réservation de Vol.pdf` | pdf | Transverses/07 - Data BI et bases de donnees | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-076 | A faire | Moyenne | `Meta/Module 2/La data  donnée, BDD, BI/Lalgèbre de Boole (1).pdf` | pdf | Transverses/07 - Data BI et bases de donnees | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-077 | A faire | Haute | `Meta/Module 2/les specifications fonctionnelles/24.06.28_Hub Sante_Dossier des Specifications_compressed.pdf` | pdf | Transverses/03 - Exigences et specifications | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-078 | A faire | Haute | `Meta/Module 2/les specifications fonctionnelles/AMOA-Cours - Spécifications 2025.pdf` | pdf | Transverses/03 - Exigences et specifications | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-079 | A faire | Haute | `Meta/Module 2/les specifications fonctionnelles/BDD SP-MDSCN - Dossier de spécifications détaillées Parking Plus - Actions utilisateurs sur un scénario.pdf` | pdf | Transverses/07 - Data BI et bases de donnees | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-080 | A faire | Haute | `Meta/Module 2/les specifications fonctionnelles/Dossier de spécifications générales et détaillées du SI - Valdelia.pdf` | pdf | Transverses/03 - Exigences et specifications | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-081 | A faire | Haute | `Meta/Module 2/les specifications fonctionnelles/Exercice1SFG_PoésieMinute_CorrigéNonFonctionnel (1).pdf` | pdf | Transverses/03 - Exigences et specifications | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-082 | A faire | Haute | `Meta/Module 2/les specifications fonctionnelles/Exercice1SFG_PoésieMinute_CorrigéNonFonctionnel.pdf` | pdf | Transverses/03 - Exigences et specifications | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-083 | A faire | Haute | `Meta/Module 2/les specifications fonctionnelles/Exercice1SFG_PoésieMinute_NonFonctionnel (2).docx` | docx | Transverses/03 - Exigences et specifications | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-084 | A faire | Haute | `Meta/Module 2/les specifications fonctionnelles/Exercice2SFG_PoésieMinute_ClassementExigences.docx` | docx | Transverses/03 - Exigences et specifications | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-085 | A faire | Haute | `Meta/Module 2/les specifications fonctionnelles/Exercice3SFG_PoésieMinute_DiagrammeCasUtilisation.docx` | docx | Transverses/03 - Exigences et specifications | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-086 | A faire | Haute | `Meta/Module 2/les specifications fonctionnelles/Exercice4SFG_PoésieMinute_DiagrammeFlux.docx` | docx | Transverses/03 - Exigences et specifications | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-087 | A faire | Haute | `Meta/Module 2/les specifications fonctionnelles/Exercice5SFG_PoésieMinute_Rédaction.docx` | docx | Transverses/03 - Exigences et specifications | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-088 | A faire | Haute | `Meta/Module 2/les specifications fonctionnelles/Exercice6SpécificationsFonctionnelles_Reformulation.docx` | docx | Transverses/03 - Exigences et specifications | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-089 | A faire | Haute | `Meta/Module 2/les specifications fonctionnelles/ExerciceSFD_PoésieMinute.docx` | docx | Transverses/03 - Exigences et specifications | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-090 | A faire | Haute | `Meta/Module 2/les specifications fonctionnelles/gt_grand-public_specifications_externes_14022023.pdf` | pdf | Transverses/03 - Exigences et specifications | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-091 | A faire | Haute | `Meta/Module 2/les specifications fonctionnelles/SFD_IHMPortailUtilisateur_V1.0.docx` | docx | Transverses/03 - Exigences et specifications | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-092 | A faire | Haute | `Meta/Module 2/les specifications fonctionnelles/Spécifications fonctionnelles générales.docx` | docx | Transverses/03 - Exigences et specifications | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-093 | A faire | Haute | `Meta/Module 2/les specifications fonctionnelles/STRATIS_Limonest_specifications_fonctionnelles_1.1_20231006.pdf` | pdf | Transverses/03 - Exigences et specifications | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-094 | A faire | Moyenne | `Meta/Module 2/Numeriques responsable/ACME Inc. et ParkMe - Cas Pratique.pdf` | pdf | Transverses/10 - Numerique responsable | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-095 | A faire | Moyenne | `Meta/Module 2/Numeriques responsable/EQL - AMOA30 - Conception responsable de services numériques VDef (1).pdf` | pdf | Transverses/10 - Numerique responsable | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-096 | A faire | Moyenne | `Meta/Module 2/Numeriques responsable/infE2019-Kit Projet - Référentiel GR491 INR (3).xlsx` | xlsx | Transverses/10 - Numerique responsable | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-097 | A faire | Moyenne | `Meta/Module 2/UML/BD_Conception.pdf` | pdf | Transverses/09 - UML modelisation et architecture | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-098 | A faire | Moyenne | `Meta/Module 2/UML/elementsUMLV1 (6).pdf` | pdf | Transverses/09 - UML modelisation et architecture | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-099 | A faire | Moyenne | `Meta/Module 2/UML/IntroGL (1).pdf` | pdf | Transverses/09 - UML modelisation et architecture | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-100 | A faire | Moyenne | `Meta/Module 2/web et mobile/Tableau comparatif.pdf` | pdf | Transverses/07 - Data BI et bases de donnees | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-101 | A faire | Moyenne | `Meta/Module 2/web et mobile/Web et mobile_Glossaire (1).pdf` | pdf | Transverses/07 - Data BI et bases de donnees | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-102 | A faire | Moyenne | `Meta/Module 2/web et mobile/WebMobile.pdf` | pdf | Transverses/07 - Data BI et bases de donnees | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-103 | A faire | Haute | `Meta/Module 3/Approche Agile/2020-Scrum-Guide-French.pdf` | pdf | Transverses/05 - Agile Scrum et frameworks | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-104 | A faire | Haute | `Meta/Module 3/Approche Agile/2020-Scrum-Guide-US.pdf` | pdf | Transverses/05 - Agile Scrum et frameworks | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-105 | A faire | Haute | `Meta/Module 3/Approche Agile/Approche Agile - Frameworks - supplément (2).pptx` | pptx | Transverses/05 - Agile Scrum et frameworks | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-106 | A faire | Haute | `Meta/Module 3/Approche Agile/Approche Agile - Partie 1 - 2025.pdf` | pdf | Transverses/05 - Agile Scrum et frameworks | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-107 | A faire | Haute | `Meta/Module 3/Approche Agile/Approche Agile - Partie 2 - 2025.pdf` | pdf | Transverses/05 - Agile Scrum et frameworks | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-108 | A faire | Haute | `Meta/Module 3/Approche Agile/Approche Agile - Partie 3 - 2025.pdf` | pdf | Transverses/05 - Agile Scrum et frameworks | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-109 | A faire | Haute | `Meta/Module 3/Approche Agile/Approche Agile - Partie 4 - 2025.pdf` | pdf | Transverses/05 - Agile Scrum et frameworks | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-110 | A faire | Haute | `Meta/Module 3/Approche Agile/Approche Agile - Partie 5 - 2025.pdf` | pdf | Transverses/05 - Agile Scrum et frameworks | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-111 | A faire | Haute | `Meta/Module 3/Approche Agile/Approche Agile - Partie 6 - 2025.pdf` | pdf | Transverses/05 - Agile Scrum et frameworks | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-112 | A faire | Haute | `Meta/Module 3/Approche Agile/Approche Agile - Partie 7 - 2025.pdf` | pdf | Transverses/05 - Agile Scrum et frameworks | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-113 | A faire | Haute | `Meta/Module 3/Approche Agile/Approche Agile - Partie 8 - 2025.pdf` | pdf | Transverses/05 - Agile Scrum et frameworks | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-114 | A faire | Haute | `Meta/Module 3/Approche Agile/Guide_scrum_extension_pack_FR_FL.pdf` | pdf | Transverses/05 - Agile Scrum et frameworks | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-115 | A faire | Haute | `Meta/Module 3/Approche Agile/scrum-guide-expansion-pack.en-us.pdf` | pdf | Transverses/05 - Agile Scrum et frameworks | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-116 | A faire | Moyenne | `Meta/Module 3/conduite du changement métier/AMOA-Conduite de changement mé` | sans extension | Project Management/06 - Deploiement et conduite du changement | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-117 | A faire | Moyenne | `Meta/Module 3/conduite du changement métier/drivers-si on a du temps (1).xlsx` | xlsx | Project Management/06 - Deploiement et conduite du changement | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-118 | A faire | Moyenne | `Meta/Module 3/conduite du changement métier/OMOC.xlsx` | xlsx | Project Management/06 - Deploiement et conduite du changement | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-119 | A faire | Moyenne | `Meta/Module 3/conduite du changement métier/Synthèse OMOC.pptx` | pptx | Project Management/06 - Deploiement et conduite du changement | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-120 | A faire | Moyenne | `Meta/Module 3/Jira/Jira_AMOA_V2 (2).pdf` | pdf | Transverses/06 - Outils SI et collaboration | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-121 | A faire | Haute | `Meta/Module 3/product management/AMOA-Product Management-MB.pdf` | pdf | Product Management | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-122 | A faire | Haute | `Meta/Module 4/conduite de projet/AMOA-Conduite projet-Cadrage-MB - exo déco.pdf` | pdf | Project Management | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-123 | A faire | Haute | `Meta/Module 4/conduite de projet/AMOA-Conduite projet-Cadrage-MB_compressed.pdf` | pdf | Project Management | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-124 | A faire | Haute | `Meta/Module 4/conduite de projet/AMOA-Conduite projet-Pilotage-MB_compressed.pdf` | pdf | Project Management | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-125 | A faire | Moyenne | `Meta/Module 4/fondamentaux du management/Support Management AMOA30.pdf` | pdf | Project Management/08 - Management et posture | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |
| SRC-126 | A faire | Moyenne | `Meta/Module 4/Pilotage du run/Pilotage du Run V2.pdf` | pdf | Project Management | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |  |  |

## Journal court d'avancement

| Date | Avancement |
|---|---|
| 2026-05-25 | Démarrage du projet P&PM et définition des 4 fichiers de pilotage racine. |
| 2026-05-25 | Initialisation du dépôt Git local et configuration du remote GitHub officiel `ELMASRY-MOAMEN/2PM.git`. |
| 2026-05-25 | Création d'une première arborescence de dossiers dans `Product Management`, `Project Management` et `Transverses`, à partir d'une lecture globale du dossier `Meta`. |
| 2026-05-25 | Création de [[P&PM - Skill ingestion documentaire]] et ajout des 126 fichiers sources de `Meta` au registre d'ingestion. |
| 2026-05-25 | Ingestion de `SRC-001` et création de 4 notes sur le déploiement informatique. |
| 2026-05-25 | Ingestion de `SRC-002`, enrichissement des notes de déploiement et création de 2 notes sur migration des données et DevOps. |

## Décisions à prendre

| ID | Sujet | Décision attendue | Statut |
|---|---|---|---|
| DEC-001 | Arborescence cible | Ajuster la structure des dossiers après les premiers lots d'ingestion réelle | En cours |
| DEC-002 | Premier lot d'ingestion | Choisir le premier thème ou fichier source à traiter dans `Meta` | A prendre |
| DEC-003 | Niveau de granularité | Définir jusqu'où découper les contenus en notes séparées | A prendre |

## Règles de mise à jour

- Une seule action principale doit être marquée `En cours` à la fois, sauf exception justifiée.
- Lorsqu'une action est terminée, son statut doit passer à `Termine` et la prochaine action prioritaire doit être indiquée.
- Les actions bloquées doivent préciser la décision ou l'information manquante.
- Ce fichier doit rester court, lisible et directement utile pour reprendre le travail.
