---
title: Nœuds d’audience de compte
description: Découvrez le type de nœud d’audience du compte que vous pouvez utiliser pour définir l’entrée de vos parcours de compte dans Journey Optimizer B2B edition.
feature: Account Journeys, Audiences, Account Lists
role: User
exl-id: 288ac5a8-79ed-4654-8ac1-83da2af04f2c
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 5%

---

# Nœuds de parcours d’audience de compte

Le nœud Audience du compte définit les comptes d’entrée du parcours. Lorsque vous [créez un parcours de compte](./journey-overview.md#create-an-account-journey), il commence toujours par un nœud _Audience du compte_ qui définit l’entrée du parcours.

Vous pouvez utiliser deux types d’entrées pour ce nœud :

* **[Audience du compte](../audiences/account-audience-overview.md)** - Il s’agit de l’audience de base synchronisée à partir du service de segmentation Experience Platform.
* **[Liste des comptes](../accounts/account-lists.md)** - Il s’agit d’une collection de comptes nommés que vous pouvez utiliser pour l’orchestration de parcours ciblés. Une liste de comptes cible les comptes nommés selon les critères définis, tels que le secteur d’activité, l’emplacement ou la taille de la société.

_Pour définir l’audience du nœud, procédez comme suit_

1. Cliquez sur le nœud **[!UICONTROL Audience du compte]** pour afficher les propriétés du nœud à droite.

   ![nœud Audience du compte](./assets/account-journey-account-audience-node.png){width="700" zoomable="yes"}

1. Choisissez le type de saisie des comptes à saisir dans le parcours :

   * **[!UICONTROL Audience du compte]**

     Choisissez ce type, puis cliquez sur **[!UICONTROL Ajouter une audience de compte]**.

     Dans la boîte de dialogue _[!UICONTROL Ajouter une audience]_, sélectionnez un segment d’audience précédemment créé et cliquez sur **[!UICONTROL Ajouter une audience]**.

     ![Sélectionnez un segment d’audience pour le nœud](./assets/node-audience-add-dialog.png){width="700" zoomable="yes"}

   * **[!UICONTROL Liste des comptes]**

     Choisissez ce type, puis cliquez sur **[!UICONTROL Ajouter une liste de comptes]**.

     Dans la boîte de dialogue _[!UICONTROL Sélectionner la liste des comptes actifs]_, sélectionnez une liste de comptes précédemment publiée et cliquez sur **[!UICONTROL Enregistrer]**.

     ![Sélectionnez une liste de comptes actifs pour le nœud](./assets/account-journey-account-audience-select-account-list.png){width="700" zoomable="yes"}

     Accédez à [Listes de comptes](../accounts/account-lists.md) pour obtenir des informations détaillées sur la création et la publication de listes de comptes.

_Pour créer un segment ciblé :_

1. Dans le volet de navigation de gauche, choisissez **[!UICONTROL Comptes]** > **[!UICONTROL Audiences]**.

1. Cliquez sur **[!UICONTROL Créer une audience]** en haut à droite.

   ![Créer un segment ciblé](./assets/audiences-list-create.png){width="800" zoomable="yes"}

1. Suivez les étapes décrites dans le [Guide de Segmentation Service](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/account-audiences){target="_blank"}.
