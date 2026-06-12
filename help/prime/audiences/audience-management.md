---
title: Gestion de l’audience
description: Page d’espace réservé pour les audiences.
autotag-review: '2026-06-12T22:47:10.727Z'
TQID: 'https://experienceleague.adobe.com/KWT9-Lr6358MQ0sLQyKAlb4SLERnBl-QQL7Cj1iXCZM'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: cb3217c9fd7beb712d0c61638d143b798010d2b7
workflow-type: tm+mt
source-wordcount: 442
ht-degree: 4%

---

# Gestion des audiences

Comment les audiences sont-elles lues dans AJO B2B Prime ?

Dans le hub de gestion marketing, cliquez sur **[!UICONTROL Listes de personnes]** dans le volet de navigation de droite.

![Accéder aux listes de personnes pour gérer vos audiences](./assets/people-lists.png){width="800" zoomable="yes"}

La page comporte deux onglets pour l’affichage et la gestion des **[!UICONTROL listes dynamiques]** et **[!UICONTROL listes statiques]**. Cliquez sur l’onglet pour basculer dans la vue Liste entre chaque type.

Cette page vous permet d’effectuer les opérations suivantes :

* Création de listes dynamiques et statiques
* Rechercher des listes existantes
* Afficher les informations sur les ressources
* Accéder aux listes pour vérifier leur appartenance

<!--
## Audience Hub

The AI Audience Hub is a centralized, AI-driven starting point for all audience-related capabilities across AJO B2B. It is designed to accelerate first-time user success while progressively unlocking advanced intelligence, insights, and control for returning and power users.

The Hub acts as:

* A guided starting point for discovering, creating, and refining person lists, account lists, and buying groups

* A visibility layer for audience health, coverage, overlap, engagement patterns, and AI-driven insights

* A control center for audience governance, optimization, reuse, and readiness for activation across journeys and sales workflows

### High level structure

Prompt-based starting point - Quick Start prompts and freeform input to help users discover, create, or optimize audiences.

1. AI insights feed - Surfaces key audience signals such as overlap, gaps, saturation risk, and optimization opportunities.

1. Adaptive audience library - A personalized view of people lists, account lists, and buying groups that adapts based on usage, relevance, and activation.

1. Optimization and arbitration nudges - Guides users to refine, split, or reuse audiences before activation.

1. Audience visibility and reporting - High-level insight into audience health, engagement patterns, and usage across active journeys.


### Empty and Error States (High-Level)

No audiences / no data - Show Quick Start prompts to help first-time users create or import person lists

Low data or incomplete audience - Explain what's missing (e.g., insufficient contacts, missing persona coverage, or low engagement data) and suggest next steps.

AI insights unavailable - Provide a graceful fallback with a clear explanation, so users understand why insights aren't shown and what actions they can take manually.
-->

## Créer une liste de personnes


Pour créer une liste dynamique ou statique, procédez comme suit :

1. Cliquez sur **Créer une liste** en haut à droite de la page _[!UICONTROL Listes de personnes]_.
1. Sélectionnez un programme comme **[!UICONTROL Parent]** pour la liste.
1. Saisissez une **[!UICONTROL Nom]** et une **[!UICONTROL Description]** dans la liste (facultatif).
1. Choisissez puis listez **[!UICONTROL Type]** :

   * **[!UICONTROL Statique]** - L’appartenance est déterminée par les filtres de qualification évalués lors de la création de la liste. L’appartenance à la liste ne se met pas à jour, sauf si vous qualifiez ou disqualifiez manuellement des enregistrements.
***[!UICONTROL Dynamique]** - L’appartenance est déterminée dynamiquement par des filtres admissibles. L’appartenance à la liste s’actualise automatiquement.

1. Cliquez sur **[!UICONTROL Créer]**.

>[!NOTE]
>
>La suppression et la duplication ne sont actuellement pas prises en charge pour les listes de personnes dans cette version de Beta.

## Listes statiques

L’appartenance à une liste statique est définie par des filtres simples qui référencent les attributs et les activités des personnes. L&#39;adhésion ne change que si vous remplissez ou disremplissez manuellement les conditions d&#39;adhésion.

### Ajouter des membres

1. Ouvrez la liste statique et cliquez sur **[!UICONTROL Ajouter des personnes]** en haut à droite.

1. Dans la boîte de dialogue, définissez les règles de qualification de vos prospects en glissant-déposant des filtres depuis la gauche.

   Vous pouvez filtrer les personnes à l’aide de n’importe quelle combinaison des éléments suivants :

   * Historique des activités
   * Attributs de la société
   * Attributs de la personne
   * Filtres spéciaux tels que l’appartenance à un Parcours

1. Pour enregistrer vos modifications, cliquez sur **[!UICONTROL Terminé]**.

1. Sélectionnez l’onglet **[!UICONTROL Membres]**.

   Après un bref instant, les membres admissibles apparaissent dans la liste.

### Supprimer des membres

1. Ouvrez la liste statique et cliquez sur **[!UICONTROL Supprimer des personnes]** en haut à droite.

1. Dans la boîte de dialogue, ajoutez les filtres pour faire correspondre les membres que vous souhaitez disqualifier.

1. Pour enregistrer vos modifications, cliquez sur **[!UICONTROL Terminé]**.

1. Sélectionnez l’onglet **[!UICONTROL Membres]**.

   Après un court laps de temps, les membres disqualifiés quittent la liste.

## Listes dynamiques

L’appartenance à une liste dynamique est définie à l’aide de filtres simples qui référencent les attributs et les activités des personnes. L’appartenance est automatiquement maintenue en qualifiant et en disqualifiant les prospects selon la logique du filtre.

### Définir la logique d’appartenance

1. Ouvrez la liste statique et sélectionnez l’onglet Règles .

1. Cliquez sur Modifier les règles.

1. Dans la boîte de dialogue, définissez les règles de qualification de vos prospects en glissant-déposant des filtres depuis la gauche.

   Vous pouvez qualifier des prospects pour la liste à l’aide de n’importe quelle combinaison des éléments suivants :

   * Historique des activités
   * Attributs de la société
   * Attributs de la personne
   * Filtres spéciaux tels que l’appartenance à un Parcours

1. Pour enregistrer vos modifications, cliquez sur **[!UICONTROL Terminé]**.

1. Sélectionnez l’onglet **[!UICONTROL Membres]**.

   Après un bref instant, les membres admissibles apparaissent dans la liste.

Pour ouvrir la page des détails du profil de prospect dans laquelle vous pouvez afficher le résumé et les activités récentes, cliquez sur le nom d’une personne dans la liste.