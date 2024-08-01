---
title: Audiences du compte
description: Découvrez les audiences de compte et comment elles activent les parcours basés sur un compte.
exl-id: f9ba690f-bab2-4c31-9000-f0be1342c8b3
source-git-commit: 78d82aa8b3bb8b8d432eeb187d75e2354dbff3ee
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 3%

---

# Audiences de compte

Une audience est un ensemble de personnes qui partagent des comportements et/ou des caractéristiques similaires. L’édition B2B de Journey Optimizer utilise les fonctionnalités de segmentation de compte disponibles dans les éditions B2B et B2P d’Adobe Real-Time Customer Data Platform. Grâce à la segmentation des comptes, les utilisateurs peuvent générer des audiences de compte en exploitant les données de l’une des entités B2B du système. Ces audiences de compte servent d’entrées aux parcours de compte de l’édition B2B de Journey Optimizer, ce qui facilite l’activation et la personnalisation en toute transparence.

Pour en savoir plus sur les audiences de compte et comment les définir, consultez la [documentation de Adobe Experience Platform Segmentation Service](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/account-audiences).

## Workflow d’audience de compte

Vous pouvez considérer Journey Optimizer B2B Edition comme une destination Experience Platform (AEP) qui n’apparaît pas dans le catalogue des destinations. Activez les audiences de compte vers Journey Optimizer B2B Edition en procédant comme suit :

1. Créez des schémas pour vos données dans AEP.
1. Ingérez vos données dans AEP.
1. Créez un segment de compte pour évaluer vos données.
1. Activez les données évaluées dans l’édition B2B de Journey Optimizer.

Dans Journey Optimizer B2B Edition, les audiences de compte sont utilisées comme entrée pour les parcours basés sur un compte, ce qui vous permet de cibler les personnes contenues dans ces comptes. Vous pouvez, par exemple, utiliser les audiences du compte pour récupérer les enregistrements de tous les comptes qui ne comportent aucune information de contact pour les personnes dont le titre est Chef des opérations (COO) ou Chef du marketing (CMO).

L’édition B2B de Journey Optimizer vous permet de créer des audiences de compte Adobe Experience Platform (AEP) directement à partir du volet de navigation de gauche, et de les intégrer à vos parcours de compte.

![Accès aux audiences de compte](./assets/account-audiences-browse.png){width="800" zoomable="yes"}

## Création d’une audience de compte

Définissez l’audience du compte en créant une segmentation de compte. Vous avez la possibilité de créer la segmentation de compte directement dans l’application Journey Optimizer B2B Edition ou vous pouvez utiliser l’[interface utilisateur du créateur de segments](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder). Vous trouverez ci-dessous la procédure à suivre pour créer une segmentation de compte dans Journey Optimizer B2B Edition.

1. Dans le volet de navigation de gauche, choisissez **[!UICONTROL Comptes]** > **[!UICONTROL Audiences]**.

1. Cliquez sur **[!UICONTROL Créer une audience]** en haut à droite.

1. Créez la définition de segment.

   Les attributs de compte et les audiences s’affichent dans la barre de navigation de gauche. Sous l’onglet _[!UICONTROL Attributs]_, vous pouvez ajouter des attributs personnalisés et créés par Platform. Faites glisser chaque attribut pour créer la logique pour le segment.

   >[!TIP]
   >
   >Lors de la création d&#39;une audience de compte, sachez que les événements sont répertoriés sous _[!UICONTROL People]_, car ces attributs sont associés à des personnes.<br/>
   >
   >Sous l’onglet _[!UICONTROL Audiences]_ , vous pouvez ajouter des audiences basées sur des personnes créées précédemment à partir desquelles créer une audience de compte lors de la création de votre propre audience.

   L’exemple suivant définit l’audience créée à l’aide de `Country Code`, `Revenue Amount` et `Market segment`. La requête en anglais serait : &quot;Je veux tous les comptes aux États-Unis qui se trouvent dans le segment des finances dont les recettes dépassent 1 million de dollars.&quot;

   ![Exemple de créateur de segments d’audience de compte](./assets/audience-segment-builder-US-finance-1M.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Enregistrer et fermer]** en haut à droite.

Pour activer l’audience de votre compte pour l’édition B2B de Journey Optimizer, vous devez [l’ajouter à un parcours de compte](../journeys/journey-overview.md#add-the-account-audience-for-your-journey) et [publier le parcours](../journeys/journey-overview.md).
