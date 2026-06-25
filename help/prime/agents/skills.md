---
title: Compétences de l’assistant IA
description: 'Examinez les compétences de l’assistant AI dans Journey Optimizer B2B Prime : workflows empaquetés pour les programmes, les parcours, les audiences, la notation, le contenu et l’optimisation de l’heure d’envoi.'
badgeBeta: label="Beta" type="informative" tooltip="Cette fonctionnalité est actuellement en version bêta limitée"
autotag-review: '2026-06-24T23:55:36.649Z'
TQID: 'https://experienceleague.adobe.com/iIi07OBWKxxa-oW-A6VrlkoTS02kmCx8kfMaCe-C-4o'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: bef5003b-cad2-4f40-bdb2-a80426d52ef5id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: ff10f619-348f-47e3-99bf-3ce4c817cf2cid: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 9433a1e86767e4504cb238ba8f3fae6e5c098a86
workflow-type: tm+mt
source-wordcount: 565
ht-degree: 8%

---

# Compétences de l’assistant IA

Une _compétence_ est un workflow empaqueté que l’agent sait exécuter, c’est-à-dire les éléments qui sous-tendent le menu `/` et les requêtes en langage naturel. Chaque compétence regroupe des instructions détaillées et les outils spécifiques nécessaires pour une tâche (par exemple, « publier un parcours », « comparer deux listes de personnes », « créer un modèle de notation »).

>[!NOTE]
>
>Chaque compétence est classée en fonction du fait qu’elle mute l’état [!DNL Journey Optimizer B2B Prime] ou [!DNL Marketo Engage] (**Écriture**), qu’elle ne génère/analyse que (**Lecture**) ou qu’elle possède des fonctions de requête et de mutation égales (**Lecture+Écriture**).

## Programmes et planification {#programs-planning}

| Compétence | Ce qu&#39;il fait | Accès | Surface de produit | Impact / flux de données |
|---|---|---|---|---|
| `falco-program-creation` | Création de programmes [!DNL Journey Optimizer B2B Prime] de bout en bout : programme, sous-dossiers, jetons, listes, parcours. | Écriture | [!DNL Journey Optimizer B2B Prime] | Lit + écrit [!DNL Journey Optimizer B2B Prime] |
| `adapt-program` | Générer des récits de migration à partir de programmes [!DNL Marketo Engage] pour l&#39;adaptation [!DNL Journey Optimizer B2B Prime]. | Lecture | [!DNL Journey Optimizer B2B Prime] | Lit [!DNL Marketo Engage], écrit [!DNL Journey Optimizer B2B Prime] |
| `folder-creation` | Créez des dossiers d’organisation dans l’arborescence de ressources. | Écriture | [!DNL Journey Optimizer B2B Prime] | Lit + écrit [!DNL Journey Optimizer B2B Prime] |
| `program-creation` *(Créer des programmes)* | Créez des programmes Marketo à partir d’un résumé de campagne. | Écriture | [!DNL Marketo Engage] | Lit + écrit [!DNL Marketo Engage] |
| `program-planning` *(Planifier Des Campagnes)* | Transformer des résumés en documents de configuration/d’implémentation. | Lecture | [!DNL Marketo Engage] | Lit [!DNL Marketo Engage] |
| `program-qa` *(Valider les programmes)* | Valider/auditer les programmes (règles uniquement, plan de test ou résumé). | Lecture | [!DNL Marketo Engage] | Lit [!DNL Marketo Engage] |

## Parcours {#journeys}

| Compétence | Ce qu&#39;il fait | Accès | Produit | Serveur principal (flux de données) |
|---|---|---|---|---|
| `journey-creation` | Créez et modifiez des parcours de personne en langage naturel. | Écriture | [!DNL Journey Optimizer B2B Prime] | Lit + écrit [!DNL Journey Optimizer B2B Prime] |
| `journey-edit-dates` | Modifier la date de début/fin d’un parcours sans le publier | Écriture | [!DNL Journey Optimizer B2B Prime] | Lit + écrit [!DNL Journey Optimizer B2B Prime] |
| `journey-publish` | Publier/lancer/planifier des parcours de personnes. | Écriture | [!DNL Journey Optimizer B2B Prime] | Lit + écrit [!DNL Journey Optimizer B2B Prime] |
| `journey-stop` | Interrompre, fermer, arrêter, arrêter ou tuer des parcours. | Écriture | [!DNL Journey Optimizer B2B Prime] | Lit + écrit [!DNL Journey Optimizer B2B Prime] |
| `journey-reentry` | Configurer la rentrée : autoriser/interdire, réinitialiser, max. les entrées. | Écriture | [!DNL Journey Optimizer B2B Prime] | Lit + écrit [!DNL Journey Optimizer B2B Prime] |
| `journey-trafficcontrol` | Exécutez une simulation du contrôle du trafic montrant le routage des profils. | Lecture | [!DNL Journey Optimizer B2B Prime] | Lit [!DNL Journey Optimizer B2B Prime] (simulation) |
| `journey-observability` | Déboguer/surveiller la progression : chemins, synchronisation, divisions, décrochages, séjour. | Lecture | [!DNL Journey Optimizer B2B Prime] | Lit [!DNL Journey Optimizer B2B Prime] + [!DNL Marketo Engage] (vérification de la liste statique). |

## Audiences et personnes {#audiences-people}

| Compétence | Ce qu&#39;il fait | Accès | Produit | Serveur principal (flux de données) |
|---|---|---|---|---|
| `audience-creation` | Adapter une liste dynamique de [!DNL Marketo Engage], créer une liste de personnes ou ajouter/mettre à jour des règles. | Écriture | [!DNL Journey Optimizer B2B Prime] | Lit [!DNL Marketo Engage] + lit/écrit [!DNL Journey Optimizer B2B Prime] |
| `people-list-comparison` | Comparer deux listes de personnes et afficher les membres qui se chevauchent | Lecture | [!DNL Journey Optimizer B2B Prime] | Lit [!DNL Journey Optimizer B2B Prime] |
| `import-leads` | Inspectez la qualité des données CSV et validez les importations dans [!DNL Marketo Engage]. | Lecture+Écriture | Les deux | Lit + écrit [!DNL Marketo Engage] |
| `lead-investigation` *(Enquêter sur les leads)* | Examiner l’activité, la notation, la qualification et le cycle de vie d’un prospect. | Lecture | [!DNL Marketo Engage] | Lit [!DNL Marketo Engage] |

## Contenu et canaux {#content-channels}

| Compétence | Ce qu&#39;il fait | Accès | Produit | Serveur principal (flux de données) |
|---|---|---|---|---|
| `content-personalization` | Parcourir/prévisualiser des modèles et modifier du contenu/générer des variantes. | Lecture+Écriture | [!DNL Journey Optimizer B2B Prime] | Lit + écrit [!DNL Journey Optimizer B2B Prime] |
| `asset-tokens` | CRUD de jeton complet sur les programmes/dossiers/parcours. | Lecture+Écriture | [!DNL Journey Optimizer B2B Prime] | Lit + écrit [!DNL Journey Optimizer B2B Prime] |
| `fcs-channels` | Recherches de canal et CRUD + publication/arrêt/suppression. | Lecture+Écriture | [!DNL Journey Optimizer B2B Prime] | Lit + écrit [!DNL Journey Optimizer B2B Prime] |

## Notation et signaux {#scoring-signals}

| Compétence | Ce qu&#39;il fait | Accès | Produit | Serveur principal (flux de données) |
|---|---|---|---|---|
| `scoring-studio` | Répertorier/obtenir des modèles de notation et les créer/publier. | Lecture+Écriture | [!DNL Journey Optimizer B2B Prime] | Lit + écrit des [!DNL Journey Optimizer B2B Prime] (service de notation) ; lit [!DNL Marketo Engage] champs de prospect/types d’activité |
| `engagementconfiguration` | Afficher la configuration de l&#39;engagement et modifier/mettre à jour les poids. | Lecture+Écriture | [!DNL Journey Optimizer B2B Prime] | Lit + écrit [!DNL Journey Optimizer B2B Prime] |
| `intentconfiguration` | Afficher la configuration d&#39;intention et définir/mettre à jour les poids. | Lecture+Écriture | [!DNL Journey Optimizer B2B Prime] | Lit + écrit [!DNL Journey Optimizer B2B Prime] |
| `intent-query` | Interroger et expliquer les scores d’intention par personne/segment/liste. | Lecture | [!DNL Journey Optimizer B2B Prime] | Lit [!DNL Journey Optimizer B2B Prime] |

## Optimisation de l’heure d’envoi {#sto}

| Compétence | Ce qu&#39;il fait | Accès | Produit | Serveur principal (flux de données) |
|---|---|---|---|---|
| `send-time-optimization` | Vérifiez le statut STO et activez/désactivez-le sur un nœud d’e-mail. | Lecture+Écriture | [!DNL Journey Optimizer B2B Prime] | Lit + écrit [!DNL Journey Optimizer B2B Prime] |
| `send-time-report` | Récupérez/affichez le rapport des performances de la STO. | Lecture | [!DNL Journey Optimizer B2B Prime] | Lit [!DNL Journey Optimizer B2B Prime] |

## Connaissances {#knowledge}

| Compétence | Ce qu&#39;il fait | Accès | Produit | Serveur principal (flux de données) |
|---|---|---|---|---|
| `product-knowledge` | Répondez aux questions pratiques/conceptuelles de la documentation [!DNL Journey Optimizer B2B Prime] sur Experience League. | Lecture | Les deux | Lit les documents externes — aucune donnée de produit |

## Cross-back-end {#cross-backend}

Ces compétences s’étendent sur plusieurs serveurs principaux :

- **`adapt-program`** — `gather_program_assets` lit [!DNL Marketo Engage] (`get_program`, `get_smart_campaign`, `list_emails`), puis écrit via `falcomcp_create_journey` — serveur principal classique.
- **`audience-creation`** — lit [!DNL Marketo Engage] listes dynamiques (`get_smart_list` / `get_smart_campaign`), puis écrit [!DNL Journey Optimizer B2B Prime] listes de personnes.
- **`journey-observability`** — [!DNL Journey Optimizer B2B Prime] lit plus un `check_lead_in_marketo_static_list` [!DNL Marketo Engage] lire.
- **`scoring-studio`** : lit [!DNL Marketo Engage] champs de prospect/types d&#39;activité ainsi que [!DNL Journey Optimizer B2B Prime] service de notation.

Tous les outils `falco-mcp_*` et parcours/jeton/notation/STO/FCS accèdent aux services [!DNL Journey Optimizer B2B Prime] ; les outils CSV/programme/prospect [!DNL Marketo Engage].
