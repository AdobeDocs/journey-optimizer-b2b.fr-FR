---
title: Création de fragments
description: 'Créez des fragments de contenu réutilisables avec des outils de conception visuelle : ajoutez des composants, de la personnalisation, du contenu conditionnel et des champs personnalisables pour les e-mails et les modèles dans Journey Optimizer B2B edition.'
feature: Fragments, Content Design Tools
role: User
exl-id: d29754cf-6721-489c-bff8-cde034456db2
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e666e996-b2cf-4c45-8fc2-1c625212abab
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: f5c2a4bb-71ca-4d7e-8efd-442250e6ba48id: a09a5a04-e30b-4d55-b031-38e6f5ec86db
autotag-review: 2026-03-30T22:26:28.969Z
TQID: https://experienceleague.adobe.com/mCpO2VPJbZtkGFlIljSZ4Zsx-3cKW38YfX-KmZC4RZ0
source-git-commit: 9baf03a1ddc1733385b0398ffadde8f548c431cc
workflow-type: tm+mt
source-wordcount: 391
ht-degree: 6%

---

# Création de fragments

Après avoir [créé un fragment](./fragments.md#create-fragments), utilisez l’espace de conception visuelle pour créer les composants de structure et de contenu dans votre fragment.

## Ajouter la structure et le contenu {#design-fragment}

{{$include /help/_includes/content-design-components.md}}

## Ajout de ressources

{{$include /help/_includes/content-design-assets.md}}

## Parcourir les calques, paramètres et styles

{{$include /help/_includes/content-design-navigation.md}}

## Personnaliser le contenu

{{$include /help/_includes/content-design-personalization.md}}

## Contenu conditionnel

Pour ajouter du contenu conditionnel qui adapte le contenu aux profils ciblés en fonction de règles, sélectionnez un composant de contenu et cliquez sur le bouton **[!UICONTROL Activer le contenu conditionnel]** dans la barre d’outils du composant. Lorsque le fragment publié est inclus dans un e-mail, les règles conditionnelles déterminent la variante d’un composant conditionnel rendu dans l’e-mail.

Pour plus d’informations, voir [_Contenu conditionnel_](./conditional-content.md).

## Activer la personnalisation des fragments

Lorsqu’un auteur ajoute un fragment à un [e-mail](./email-authoring.md#content-authoring---use-visual-fragments) ou [modèle d’e-mail](./email-template-authoring.md#content-authoring---use-visual-fragments), le contenu du fragment est verrouillé par défaut. Toutes les modifications apportées au fragment publié sont automatiquement propagées à toutes les ressources de contenu dans lesquelles le fragment est utilisé. Lorsque vous désignez un paramètre pour un composant du fragment comme modifiable, l’auteur de l’e-mail ou du modèle peut spécifier une valeur de champ personnalisé spécifique à ses besoins. Cette option de personnalisation est limitée aux composants visuels d’image, de texte et de bouton.

Par exemple, si vous concevez une bannière réutilisable qui comprend un bouton cliquable, vous pouvez désigner le paramètre d’URL du bouton comme étant modifiable. Les auteurs d’e-mails peuvent ensuite utiliser une URL plus spécifique à leur campagne par e-mail. Grâce à ces champs personnalisables, les marketeurs peuvent gérer et personnaliser du contenu réutilisable sans avoir à créer des blocs de contenu entièrement nouveaux ou à interrompre les mises à jour héritées du fragment d’origine.

1. Dans l’éditeur de contenu visuel, sélectionnez l’image, le texte ou l’élément de bouton sur lequel vous souhaitez activer la personnalisation.

1. Dans les détails du composant sur la droite, sélectionnez l’onglet **[!UICONTROL Champs modifiables]**.

1. Cliquez sur le bouton (bascule) de l’option **[!UICONTROL Activer l’édition]** et définissez les champs modifiables.

   ![Activer les champs modifiables pour un composant d’image de fragment](./assets/fragment-editable-fields-image.png){width="700" zoomable="yes"}

   Vous pouvez activer la personnalisation des champs affichés, selon le type de composant et les paramètres définis dans le fragment.

   Définissez le bouton (bascule) sur Activé pour chaque champ où vous souhaitez autoriser la personnalisation.

1. Cliquez sur **[!UICONTROL Aperçu]** pour consulter tous les champs modifiables et leurs valeurs par défaut.

   ![Examinez les champs modifiables et leurs valeurs par défaut](./assets/fragment-editable-fields-image-overview.png){width="700" zoomable="yes"}

1. Enregistrez vos modifications.

## Modifier le tracking des URL liées

{{$include /help/_includes/content-design-links.md}}
