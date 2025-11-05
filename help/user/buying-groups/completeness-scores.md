---
title: Scores d'exhaustivité pour les groupes d'achat
description: Calculez les scores de complétion du groupe d’achats à l’aide de seuils basés sur les rôles, d’exigences personnalisables des membres et de paramètres de complétion dans Journey Optimizer B2B edition.
feature: Buying Groups
role: User
source-git-commit: 1ebc27a709e1b82029c22950897505f3945a507f
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 4%

---


# Scores d&#39;exhaustivité {#completeness-scores}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_completeness_score"
>title="Score d’exhaustivité"
>abstract="Les scores d&#39;exhaustivité reflètent la mesure dans laquelle l&#39;appartenance à un groupe d&#39;achat est alignée pour un groupe d&#39;achat prêt pour les ventes."

Un score d&#39;exhaustivité est un pourcentage qui indique dans quelle mesure un groupe d&#39;achats est renseigné avec les membres requis dans ses rôles définis. Ces scores sont basés sur les seuils des membres du rôle que vous configurez dans le modèle de rôles et sur le nombre réel de membres affectés à chaque rôle dans le groupe d&#39;achat. Les scores obtenus aident les professionnels du marketing à évaluer leur niveau de préparation aux ventes et à identifier les écarts dans la composition du groupe d’achats. Le calcul du score se produit automatiquement lorsque l&#39;appartenance à un groupe d&#39;achat change.

![Scores d&#39;exhaustivité du groupe d&#39;achat](./assets/buying-group-details-page-completeness-scores.png){width="800" zoomable="yes"}

Il existe deux types de scores d&#39;exhaustivité :

* **Score d&#39;exhaustivité du groupe d&#39;achat** - Le score d&#39;exhaustivité du groupe d&#39;achat est un pourcentage compris entre 0 % et 100 % et représente l&#39;exhaustivité globale du groupe d&#39;achat en fonction des calculs d&#39;exhaustivité au niveau du rôle.

  Le score d&#39;exhaustivité du groupe d&#39;achats est affiché sur la page [Détails du groupe d&#39;achats](./buying-group-details.md). Ce score permet de voir en un coup d’œil si le groupe d’achat dispose des parties prenantes requises pour l’engagement commercial.

* **Score d&#39;exhaustivité du rôle** - Le score d&#39;exhaustivité du rôle est un pourcentage pour chaque rôle individuel au sein d&#39;un groupe d&#39;achats, en fonction du nombre de membres affectés à ce rôle.

  Le score d&#39;exhaustivité des rôles pour chaque rôle est affiché dans la page des détails du groupe d&#39;achats lorsque vous modifiez des rôles et ajustez les paramètres d&#39;exhaustivité. Ces scores vous aident à identifier les rôles spécifiques nécessitant des membres supplémentaires pour atteindre le seuil de préparation aux ventes.

  La page de détails affiche les deux premiers scores d&#39;exhaustivité des rôles avec un lien n_+ pour tous les rôles supplémentaires. Cliquez sur le lien pour afficher les scores de complétion de rôle supplémentaires.

Les scores d&#39;exhaustivité reflètent l&#39;état actuel de l&#39;appartenance au groupe d&#39;achat et sont automatiquement mis à jour à mesure que des membres sont ajoutés ou supprimés. Les scores affichés s’affichent sous la forme de pourcentages entiers (par exemple, un score de 66,67 % s’affiche sous la forme de 67 %).

## Évaluation du niveau de préparation des ventes

Adobe Journey Optimizer B2B edition dote les marketeurs d’outils qui garantissent que les groupes d’achats s’alignent sur les processus de prise de décision réels. Vous pouvez définir des groupes d&#39;achats complets à l&#39;aide de seuils de membre de rôle personnalisables qui reflètent la méthodologie des ventes de votre organisation. En établissant des exigences minimales et maximales pour chaque rôle, vous établissez des critères clairs pour ce qui constitue un groupe d&#39;achat prêt à vendre.

Le score d&#39;exhaustivité du groupe d&#39;achats fournit une mesure précise du niveau de préparation des ventes pour le groupe. Par exemple, pour saisir une opportunité pour une solution spécifique, vous pouvez avoir besoin d’au moins deux décideurs, d’un influenceur et d’au moins un praticien. Le calcul de la note d&#39;exhaustivité tient compte de chacun de ces besoins spécifiques au rôle, ce qui donne une vue de la préparation globale du groupe d&#39;achat.

## Mesurer l’efficacité du parcours

La complétude du groupe d&#39;achat agit comme un indicateur de performance clé (IPC) pour l&#39;efficacité du parcours. L’objectif d’un parcours spécifique peut être d’augmenter le degré de complétude du groupe d’achats d’un certain pourcentage ou d’atteindre un seuil minimum avant de déclencher des alertes prêtes pour les ventes.

Dans une grande entreprise, vous pouvez identifier une personne par rôle. Cependant, il se peut que cette personne ne soit pas le bon contact pour la vente ou que vous ayez besoin de plusieurs contacts occupant des rôles critiques. Par exemple, une grande organisation peut avoir plusieurs décideurs en technologie de l&#39;information (TI) répartis entre les ministères ou les unités opérationnelles. Identifier un seul décideur peut ne pas suffire pour une vente d&#39;entreprise complexe.

Après avoir analysé l&#39;exhaustivité actuelle du groupe d&#39;achats, vous pouvez ajuster le nombre requis de contacts pour chaque rôle dans le modèle de rôles. Ces ajustements vous permettent d&#39;ajuster votre stratégie d&#39;achat en fonction des tendances réelles et des résultats de vente.

<!-- ## Analyze audiences for journey optimization

Marketers can view the starting buying group completeness score of target account audiences to find the best performance indicators for a solution. This visibility enables marketers to:

* Determine if they need to adjust the completeness score requirements for each role to make journeys more effective.
* Identify which buying groups are closest to sales-ready status and prioritize them for acceleration campaigns.
* Segment buying groups by completeness score ranges and create tailored nurture strategies for different maturity levels.

>[!BEGINSHADEBOX]

The buying group completeness score is available to use for filtering in [journey split-path-by-account nodes](../journeys/split-merge-paths-nodes.md#account-path-filters) and for audience segmentation. Role completeness can be used to create personalized content that addresses specific gaps in buying group composition.

>[!ENDSHADEBOX] -->

## Calcul de l&#39;exhaustivité des rôles {#role-completeness-calculation}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_role_completeness_calculation"
>title="Calcul de l&#39;exhaustivité des rôles"
>abstract="Les scores de complétion des rôles sont calculés sous la forme d&#39;un pourcentage en fonction du nombre de membres affectés à un rôle."

Journey Optimizer B2B edition calcule le score d&#39;exhaustivité pour chaque rôle de groupe d&#39;achats individuel sous la forme d&#39;un pourcentage. Basez ce score sur le nombre de membres affectés au rôle, par rapport au nombre [requis dans le modèle de rôles](./buying-groups-role-templates.md#change-the-completeness-score-settings) pour l&#39;achèvement.

Le calcul de l&#39;exhaustivité des rôles est un pourcentage linéaire compris entre zéro et le seuil spécifié (membres requis) :

* Si le nombre de membres affectés est **zéro**, l&#39;exhaustivité du rôle est de **0 %**.
* Si le nombre de membres affectés est **égal ou supérieur au seuil**, l&#39;exhaustivité du rôle est de **100 %**.
* Si le nombre de membres affectés est **compris entre un et le seuil**, la complétion est calculée proportionnellement.

### Formule de complétion du rôle

Le pourcentage d&#39;exhaustivité du rôle est calculé à l&#39;aide de la formule suivante :

```text
Role Completeness % = ((Assigned Members - Threshold) / (Threshold)) × 100
```

Où ce qui suit est vrai :

* `Assigned Members` = nombre actuel de membres dans le rôle
* `Threshold` = valeur requise pour les membres définie dans le modèle de rôles

### Exemples d&#39;exhaustivité des rôles

Les exemples suivants illustrent les calculs d&#39;exhaustivité des rôles avec différentes configurations de seuil :

| Rôle | Membres requis | Membres affectés | Calcul | Exhaustivité du rôle |
|------|------------------|------------------|-------------|-------------------|
| Décisionnaire | 3 | 0 | Aucune | 0 % |
|  |  | 1 | 1/3 × 100 | 33 % |
|  |  | 2 | 2/3 × 100 | 66 % |
|  |  | 3 | Au seuil | 100 % |
|  |  | 4 | Au-dessus du seuil | 100 % |
| Personne influente | 5 | 0 | Aucune | 0 % |
|  |   | 1 | 1/5 × 100 | 20 % |
|  |   | 2 | 2/5 × 100 | 40 % |
|  |   | 3 | 3/5 × 100 | 60 % |
|  |   | 4 | 4/5 × 100 | 80 % |
|  |   | 5 | Au seuil | 100 % |
|  |   | 6 | Au-dessus du seuil | 100 % |

## Calcul de l&#39;exhaustivité du groupe d&#39;achat {#buying-group-completeness-calculation}

Le score de complétion du groupe d&#39;achats agrège les scores de complétion des rôles individuels. Ce calcul fournit une vue holistique du niveau de préparation du groupe d&#39;achat pour tous les rôles définis.

### Formule de complétion d&#39;un groupe d&#39;achat

Le pourcentage d&#39;exhaustivité du groupe d&#39;achats est calculé à l&#39;aide de la formule suivante :

```text
Buying Group Completeness % = Σ(Role Completeness %) / Number of defined roles
```

Où ce qui suit est vrai :

* `Role Completeness %` = pourcentage d’exhaustivité des rôles individuels (0-100 %)
* `Σ` = Somme de tous les rôles du groupe d&#39;achat

<!--

## Use completeness scores in journeys

Use buying group completeness scores and role-level completeness scores to optimize your account journeys and personalize engagement strategies.

### Split paths by completeness

Use completeness thresholds in [journey split-path-by-account nodes](../journeys/split-merge-paths-nodes.md#account-path-filters) to route buying groups through different journey paths based on their readiness. For example:

* **High completeness path** (≥70%) - Buying groups that are nearly sales-ready can be routed to sales teams or receive call-to-action campaigns
* **Medium completeness path** (40-69%) - Buying groups in active development receive nurture campaigns focused on filling specific role gaps
* **Low completeness path** (<40%) - Newly formed buying groups receive awareness and education content to build initial engagement

### Trigger actions based on completeness milestones

Set up journey events that trigger specific actions when buying groups reach completeness milestones. FOr example:

* Alert sales teams when a buying group reaches 70% completeness.
* Send a _stakeholder alignment_ campaign when completeness increases by 20% or more within a defined timeframe.
* Trigger an automated assessment when a buying group stalls at the same completeness level for an extended period.

By leveraging completeness scores throughout the journey, you create more targeted, efficient campaigns that align with the actual composition and maturity of your buying groups.

-->