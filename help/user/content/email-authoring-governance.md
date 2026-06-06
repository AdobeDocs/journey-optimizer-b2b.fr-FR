---
title: Créer à partir d’un modèle régi
description: Créer des e-mails à partir de modèles régis avec du contenu verrouillé - Identifiez les zones modifiables et respectez les contraintes de gouvernance dans Journey Optimizer B2B edition.
feature: Email Authoring, Content
role: User
exl-id: 1af996a6-a010-4899-96e9-bad76f93865c
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: f5c2a4bb-71ca-4d7e-8efd-442250e6ba48
autotag-review: 2026-03-30T22:35:16.900Z
TQID: https://experienceleague.adobe.com/iwVl-dwU9oGG0rHQ9-J3EO5r3B778jQCe6XK742ArEo
source-git-commit: 2c6aafd07cf033df8801621f7e5275dbeeb2768e
workflow-type: tm+mt
source-wordcount: 273
ht-degree: 1%

---

# Créer à partir d’un modèle régi

Les concepteurs de contenu peuvent activer la [gouvernance (_verrouillage de contenu_)](./template-content-governance.md) lors de la création de modèles d’e-mail. Les fonctionnalités de gouvernance leur permettent de désigner les parties de la conception qui ne peuvent pas être modifiées lorsqu’elles sont utilisées dans un parcours de compte. Lorsque vous [sélectionnez un modèle enregistré](./email-authoring.md#select-a-template) pour créer un email, l’espace de conception visuelle charge le modèle afin que vous puissiez l’utiliser comme base pour votre email.

Si la gouvernance est activée pour le modèle, une alerte s’affiche dans le panneau des propriétés à droite. Sélectionnez **[!UICONTROL Mettre en surbrillance les zones modifiables]** dans la partie supérieure de la zone de travail pour afficher les composants et les éléments de contenu modifiables à utiliser dans votre parcours.

![Affichage des zones modifiables dans un modèle régi](./assets/email-designer-governed-highlight.png){width="800" zoomable="yes"}

Vous pouvez également déterminer les éléments verrouillés ou modifiables à l’aide de l’_arborescence de navigation_. Cliquez sur l’icône _Arborescence de navigation_ ( ![Icône Lien](../assets/do-not-localize/icon-navigation-tree.svg) ) à gauche de la zone de travail pour afficher l’arborescence.

![Affichage des zones modifiables dans un modèle régi](./assets/email-designer-governed-tree.png){width="600" zoomable="yes"}

Les icônes indiquent les paramètres de verrouillage de contenu appliqués.

| Icône | Nom | Description |
|------|------|-------------|
| ![Icône Lecture seule](../assets/do-not-localize/icon-tree-lock.svg) | Lecture seule | Le composant est verrouillé et ne peut pas être modifié. Lorsqu’ils sont appliqués au niveau racine (_[!UICONTROL Body]_), tous les composants enfants sont verrouillés et ne peuvent pas être modifiés. |
| ![Icône de modification du contenu](../assets/do-not-localize/icon-tree-content-lock.svg) | Verrouillage de contenu | Le verrouillage de contenu est appliqué au niveau du composant. |
| ![&#x200B; Icône modifiable &#x200B;](../assets/do-not-localize/icon-edit.svg) | Modifiable | Le composant est entièrement modifiable. Cependant, il se peut que vous ne puissiez pas supprimer l’élément. |
| ![Icône de modification du contenu](../assets/do-not-localize/icon-tree-edit-text.svg) | Modifiable - Contenu uniquement | Le composant et le style sont statiques, mais vous pouvez modifier le contenu (texte ou image, par exemple). |
