---
title: Créer des modèles de notation personnalisés
description: Créez, prévisualisez et publiez des modèles de notation de prospect personnalisés dans le Prime B2B de Journey Optimizer à l’aide des compétences Scoring Studio dans l’interface de conversation de l’assistant AI.
badgeBeta: label="Beta" type="informative" tooltip="Cette fonctionnalité est actuellement en version bêta limitée"
autotag-review: '2026-06-25T21:20:26.754Z'
TQID: 'https://experienceleague.adobe.com/-D5EaJ-3GQ5iwaE6hChscZGEdflKmZ3tdp6VUNuPjWk'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: bef5003b-cad2-4f40-bdb2-a80426d52ef5id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: ff10f619-348f-47e3-99bf-3ce4c817cf2cid: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 95f506e5ec59996bf4af53151cd0553d23b19082
workflow-type: tm+mt
source-wordcount: 489
ht-degree: 8%

---

# Créer des modèles de notation personnalisés

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_scoring_studio"
>title="Studio de notation"
>abstract="Utilisez les compétences du studio de notation pour créer, configurer et publier des modèles de notation de lead personnalisés via l’interface de chat de l’assistant IA."

La compétence [_Studio de notation_ ](./skills.md#scoring-signals) de [!DNL Adobe Journey Optimizer B2B Prime] fournit une solution de notation de prospect native à l’IA qui vous permet de créer, de configurer et de publier des modèles de notation de prospect. Studio associe un workflow piloté par les agents à une interface utilisateur visuelle. Vous pouvez créer des modèles de notation à l’aide d’invites en langage naturel dans l’interface de chat de l’assistant [AI](./chat-interface.md) ou en interagissant directement avec les commandes de l’interface utilisateur.

* **Compétences** - `scoring-studio`
* **Invocation** - Utilisez une barre oblique pour ouvrir Scoring Studio. Par exemple : _« open Scoring Studio.«_
* **Lit à partir de / écrit sur** - [!DNL Journey Optimizer B2B Prime] service de notation ; lit [!DNL Marketo Engage] champs de prospect et les types d’activité.

Au lancement, l’assistant d’IA récupère automatiquement le contexte approprié (y compris les types d’activité, les champs de prospect, les listes de personnes et les listes de scores existantes) pour ancrer ses suggestions dans vos données.

![Scoring Studio lancé dans l’interface de chat de l’assistant AI](./assets/scoring-studio.png){width="700" zoomable="yes"}

## Création d’un modèle de notation {#create-model}

Lorsque vous ouvrez Scoring Studio, l’assistant AI propose un exemple de modèle de notation pertinent pré-renseigné avec une liste statique et un ensemble d’activités notées. Vous pouvez accepter ce point de départ suggéré ou fournir votre propre invite pour définir un modèle personnalisé.

### Prévisualiser le modèle {#preview-model}

Après avoir fourni une invite, l’assistant AI génère un aperçu du modèle avant d’apporter des modifications. Les surfaces d’aperçu :

* Dimensions de notation utilisées
* Attributs et activités en cours de notation
* Listes statiques ou listes dynamiques appliquées en tant que segments
* Résumé de l’objectif du modèle, du segment cible et des signaux principaux

Vous pouvez vérifier l’aperçu et choisir de créer le modèle en fonction de celui-ci, ou continuer à l’affiner via la conversation avant de finaliser.

### Structure du modèle {#model-structure}

Le modèle créé est organisé en _dimensions_ et _signaux_. Vous pouvez configurer chaque signal à l’aide du panneau des propriétés de l’interface utilisateur :

* **Type de signal** — Basé sur l&#39;activité ou basé sur les attributs
* **Activité ou attribut** — Élément spécifique à noter
* **Paramètres du signal** — Paramètres réglables pour le signal

Vous pouvez créer et configurer des modèles entièrement via l’assistant AI en utilisant le langage naturel ou interagir directement avec les commandes de l’interface utilisateur.

## Publication d’un modèle de notation {#publish-model}

Une fois votre modèle finalisé, demandez à l’assistant AI de le publier. Le processus de publication gère automatiquement les éléments suivants :

| Étape | Ce qui se passe |
|---|---|
| **Compilation des règles** | Toutes les règles de notation sont compilées et validées |
| **Création de la tâche de score** | Une tâche de score planifiée est créée et configurée pour s’exécuter quotidiennement |

Après la publication, vous avez également la possibilité de déclencher une exécution manuelle pour traiter les scores immédiatement.

## Affichage des résultats de la notation {#view-results}

Une fois l’exécution de notation terminée, les notes sont réécrites dans [!DNL Marketo Engage] via le processus d’importation de prospect. Une fois l’importation terminée, les scores mis à jour peuvent être vérifiés directement dans [!DNL Marketo Engage].

Après chaque exécution, vous pouvez afficher un résumé des résultats qui indique :

* Nombre de personnes notées
* Le score individuel change par personne

Un journal d’audit est disponible pour consulter des détails d’exécution supplémentaires.
