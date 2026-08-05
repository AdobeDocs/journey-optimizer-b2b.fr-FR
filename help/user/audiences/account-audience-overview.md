---
title: Audiences de comptes
description: Créez des audiences de comptes à l’aide de la segmentation afin de cibler des comptes spécifiques et de permettre des parcours personnalisés basés sur les comptes dans Journey Optimizer B2B Edition.
feature: Audiences
role: User
exl-id: f9ba690f-bab2-4c31-9000-f0be1342c8b3
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
  - id: f2da1b69-6919-4386-a5d2-9c7b5c9033db
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
autotag-review: 2026-03-30T19:50:18.033Z
TQID: https://experienceleague.adobe.com/JvPzSX83WY7Edws8IMHseCSwqFR4Ro-jy-UO-WvRgDc
source-git-commit: 22de56a75a61ff2bf4345bcb09371b4c639206ba
workflow-type: tm+mt
source-wordcount: 600
ht-degree: 74%

---

# Audiences de comptes

Une audience est un ensemble de personnes qui partagent des comportements et/ou des caractéristiques similaires. Journey Optimizer B2B Edition utilise les fonctionnalités de segmentation de compte disponibles dans les éditions B2B et B2P d’Adobe Real-Time Customer Data Platform. Avec la segmentation de compte, les utilisateurs et utilisatrices peuvent générer des audiences de comptes en exploitant les données de l’une des entités B2B du système. Ces audiences de comptes servent d’entrées pour les parcours de compte Journey Optimizer B2B Edition, ce qui facilite l’activation et la personnalisation.

Découvrez les audiences de comptes et comment les définir dans la [documentation du service de segmentation d’Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/types/account-audiences){target="_blank"}.

## Workflow d’audience de comptes

Journey Optimizer B2B edition fonctionne comme une destination Experience Platform (AEP) qui n’apparaît pas dans le catalogue des destinations. Activez les audiences de comptes dans Journey Optimizer B2B Edition en procédant comme suit :

1. Créez des schémas pour vos données dans AEP.
1. Ingérez vos données dans AEP.
1. Créez un segment de compte pour évaluer vos données.
1. Activez vos données évaluées dans Adobe Journey Optimizer B2B Edition.

Dans Adobe Journey Optimizer B2B Edition, les audiences de comptes sont utilisées comme entrée pour les parcours basés sur les comptes, ce qui vous permet de cibler les personnes au sein de ces comptes. Par exemple, vous pouvez utiliser des audiences de comptes pour récupérer les enregistrements de tous les comptes qui ne disposent d’aucune information de contact pour une personne occupant le poste de Chief Operating Officer (COO) ou Chief Marketing Officer (CMO).

Adobe Journey Optimizer B2B Edition vous permet de créer des audiences de comptes Adobe Experience Platform (AEP) directement à partir du volet de navigation de gauche et de les intégrer à vos parcours de compte.

![Accéder aux audiences de comptes](./assets/account-audiences-browse.png){width="800" zoomable="yes"}

## Créer une audience de comptes

Définissez l’audience du compte en créant un segment de compte. Vous avez la possibilité de créer le segment de compte directement dans l’application Journey Optimizer B2B edition ou vous pouvez utiliser l’interface utilisateur du créateur de segments [IU](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/ui/segment-builder){target="_blank"}. Vous trouverez ci-dessous la procédure à suivre pour créer un segment de compte dans Journey Optimizer B2B edition.

1. Dans le volet de navigation de gauche, choisissez **[!UICONTROL Comptes]** > **[!UICONTROL Audiences]**.

1. Cliquez sur **[!UICONTROL Créer une audience]** en haut à droite.

1. Créez la définition de segment.

   Les attributs et audiences de compte s’affichent dans la barre de navigation de gauche. Dans l’onglet _[!UICONTROL Attributs]_, vous pouvez ajouter des attributs créés par Platform et des attributs personnalisés. Pour créer la logique du segment, faites glisser chaque attribut.

   >[!TIP]
   >
   >Lors de la création d’une audience de compte, gardez à l’esprit que les événements sont répertoriés sous _[!UICONTROL Personnes]_, car ces attributs sont associés à des personnes.<br/>
   >
   >Dans l’onglet _[!UICONTROL Audiences]_, vous pouvez ajouter des audiences basées sur les personnes, créées précédemment, sur lesquelles vous pouvez vous appuyer pour créer votre propre audience de compte.

   L’exemple suivant définit une audience créée à l’aide de `Country Code`, `Revenue Amount` et `Market segment`. La requête en anglais est la suivante : « Je souhaite que tous les comptes États-Unis du segment financier dont le chiffre d’affaires dépasse 1 million de dollars ».

   Exemple de créateur de segments d’audience ![account](./assets/audience-segment-builder-US-finance-1M.png){width="700" zoomable="yes"}
   <br/>

   >[!IMPORTANT]
   >
   >L’attribut `Account Name` pour les enregistrements de compte doit contenir une valeur à inclure dans les parcours de compte. Si cet attribut est vide (nul), l’enregistrement de compte est exclu.<br/>
   >Pour vous assurer que seuls les comptes dont le nom de compte n’est pas vide sont inclus, ajoutez l’attribut **[!UICONTROL Nom du compte]** et sélectionnez _[!UICONTROL existe]_ comme condition de correspondance.<br/>
   >![&#x200B; L’attribut Nom du compte existe](./assets/audience-segment-builder-account-name-exists.png){width="600"}
   ><br/>Si vous utilisez un attribut personnalisé pour le nom du compte, utilisez votre nom d’attribut personnalisé au lieu de _[!UICONTROL Nom du compte]_.

1. Cliquez sur **[!UICONTROL Enregistrer et fermer]** en haut à droite.

Pour activer votre audience de compte pour Journey Optimizer B2B Edition, vous devez [l’ajouter à un parcours de compte](../journeys/account-audience-nodes.md) et [publier le parcours &#x200B;](../journeys/journeys-overview.md).
