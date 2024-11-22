---
title: Création à partir d’un modèle régi
description: Découvrez comment utiliser la création d’emails avec un modèle gouverné qui contient des composants de contenu verrouillé.
feature: Email Authoring, Content
source-git-commit: d7e2b7673b0a6709d2841893d87617e580b62298
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 1%

---

# Création à partir d’un modèle géré

Les concepteurs de contenu peuvent activer la [gouvernance (_verrouillage du contenu_)](./template-content-governance.md) lors de la création de modèles d’email. Les fonctions de gouvernance leur permettent de désigner les parties de la conception qui ne peuvent pas être modifiées lorsqu’elles sont utilisées dans un parcours de compte. Lorsque vous [sélectionnez un modèle enregistré](./email-authoring.md#select-a-template) pour créer un email, le concepteur visuel charge le modèle afin que vous puissiez l’utiliser comme base de votre email.

Si la gouvernance est activée pour le modèle, une alerte s’affiche dans le panneau des propriétés à droite. Vous pouvez activer les **[!UICONTROL zones modifiables de mise en surbrillance]** en haut de la zone de travail pour voir les composants et les éléments de contenu modifiables à utiliser dans votre parcours.

![ Afficher les zones modifiables dans un modèle régi](./assets/email-designer-governed-highlight.png){width="800" zoomable="yes"}

Vous pouvez également déterminer les éléments verrouillés ou modifiables à l’aide de l’_arborescence de navigation_. Cliquez sur l’icône _Arborescence de navigation_ ( ![Icône Lien](../assets/do-not-localize/icon-navigation-tree.svg) ) à gauche de la zone de travail pour afficher l’arborescence.

![ Afficher les zones modifiables dans un modèle régi](./assets/email-designer-governed-tree.png){width="600" zoomable="yes"}

Les icônes indiquent les paramètres de verrouillage du contenu appliqués.

| Icône | Nom | Description |
|------|------|-------------|
| ![Icône Lecture seule](../assets/do-not-localize/icon-tree-lock.svg) | Lecture seule | Le composant est verrouillé et ne peut pas être modifié. Lorsqu’ils sont appliqués au niveau racine (_[!UICONTROL Body]_), tous les composants enfants sont verrouillés et ne peuvent pas être modifiés. |
| ![Icône de modification du contenu](../assets/do-not-localize/icon-tree-content-lock.svg) | Verrouillage de contenu | Le verrouillage du contenu est appliqué au niveau du composant. |
| ![Icône modifiable](../assets/do-not-localize/icon-edit.svg) | Modifiable | Le composant est entièrement modifiable. Cependant, il se peut que vous ne puissiez pas supprimer l’élément. |
| ![Icône de modification du contenu](../assets/do-not-localize/icon-tree-edit-text.svg) | Modifiable - contenu uniquement | Le composant et le style sont statiques, mais vous pouvez modifier le contenu (texte ou image, par exemple). |