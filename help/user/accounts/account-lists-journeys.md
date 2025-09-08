---
title: Utiliser les listes de comptes dans Parcours et les programmes
description: Utilisez les listes de comptes dans parcours orchestration, ajoutez/supprimez des comptes dynamiquement et filtrez les listes dynamiques Marketo Engage dans Journey Optimizer B2B edition.
feature: Account Lists, Account Journeys
role: User
exl-id: 7cda080d-6263-4ccd-b144-432e4e78c298
source-git-commit: 937101d6570a8217ff11037822c414350c6026ae
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 0%

---

# Utiliser les listes de comptes dans les parcours et les programmes

Vous pouvez incorporer des listes de comptes dynamiques (publiés) de différentes manières dans les parcours de votre compte.

## Nœud d’audience de compte

Tous les parcours de compte commencent par un nœud [_Audience du compte_](../journeys/account-audience-nodes.md). Lorsque vous définissez ce nœud pour utiliser une liste de comptes, les comptes de membres se déplacent dans le parcours lors de sa mise en ligne (publication).

1. Sélectionnez l’option **[!UICONTROL Liste des comptes]** pour le nœud _Audience du compte_ de départ.

   ![Sélectionnez l’option de liste des comptes pour le nœud d’audience du compte](../journeys/assets/node-audience-account-list.png){width="500"}

1. Cliquez sur **[!UICONTROL Liste Ajouter des comptes]**.

1. Cochez la case de la liste des comptes et cliquez sur **[!UICONTROL Enregistrer]**.

   ![Sélectionnez l’option de liste des comptes pour le nœud d’audience du compte](../journeys/assets/node-audience-account-list-select-dialog.png){width="600" zoomable="yes"}

## Nœud Prendre une action - Ajouter à la liste

**_Listes de comptes statiques uniquement_**

Dans un parcours de compte, ajoutez des comptes à une liste de comptes statique à l’aide d’[un nœud _Prendre une action_](../journeys/action-nodes.md).

Par exemple, vous pouvez avoir un chemin de parcours où vous envoyez un e-mail et où certains comptes prennent différentes actions en tant qu’actions de réponse. Vous considérez cette activité comme un point de qualification dans le parcours. Avec la qualification, vous souhaitez les ajouter à une liste de comptes utilisée comme audience pour un autre parcours avec un flux différent pour les comptes qualifiés.

>[!NOTE]
>
>Si un compte figure déjà dans la liste lors de l’exécution du nœud, l’action est ignorée.

1. Sélectionnez l’option _[!UICONTROL Action sur]_ **[!UICONTROL Comptes]**.

1. Pour _[!UICONTROL Action sur les comptes]_, choisissez **[!UICONTROL Ajouter à la liste des comptes]**.

   ![Sélectionnez Ajouter à la liste des comptes](../journeys/assets/node-action-account-add-to-account-list.png){width="500"}

1. Pour **[!UICONTROL Sélectionner la liste des comptes statiques actifs]**, choisissez la liste des comptes dans laquelle vous souhaitez ajouter des comptes.

   ![Sélectionnez Ajouter à la liste des comptes](../journeys/assets/node-action-account-add-to-account-list-select.png){width="500"}

## Nœud Prendre une action - Supprimer du compte

**_Listes de comptes statiques uniquement_**

Dans un parcours de compte, supprimez des comptes d’une liste de comptes statique à l’aide d’[un nœud _Prendre une action_](../journeys/action-nodes.md).

Par exemple, vous pouvez avoir un chemin de parcours où vous envoyez un e-mail et où certains comptes prennent différentes actions en tant qu’actions de réponse. Vous considérez cette activité comme un point de qualification dans le parcours. Avec cette qualification, vous souhaitez les supprimer d’une liste de comptes utilisée comme audience pour un autre parcours qui envoie des e-mails supplémentaires afin de ne pas dupliquer vos communications de qualification.

>[!NOTE]
>
>Si un compte ne figure pas dans la liste où sa suppression est planifiée, l’action est ignorée.

1. Sélectionnez l’option _[!UICONTROL Action sur]_ **[!UICONTROL Comptes]**.

1. Pour _[!UICONTROL Action sur les comptes]_, choisissez **[!UICONTROL Supprimer de la liste des comptes]**.

   ![Sélectionnez Ajouter à la liste des comptes](../journeys/assets/node-action-account-remove-from-account-list.png){width="500"}

1. Pour **[!UICONTROL Sélectionner la liste des comptes statiques actifs]**, choisissez la liste des comptes dans laquelle vous souhaitez supprimer des comptes.

   ![Sélectionnez Ajouter à la liste des comptes](../journeys/assets/node-action-account-remove-from-account-list-select.png){width="500"}

## Programme Marketo Engage - Membre de la liste des comptes

En tant que spécialiste marketing, vous pouvez supprimer des programmes dans Marketo Engage pour les personnes qui font partie des listes de comptes dans Journey Optimizer B2B edition.

Dans l’instance Marketo Engage connectée à Journey Optimizer B2B edition, vous pouvez utiliser le filtre _[!UICONTROL Membre de la liste des comptes]_ de vos listes dynamiques pour identifier ces prospects en fonction de votre stratégie de campagne. Pour plus d’informations sur les listes dynamiques, consultez la documentation de [Marketo Engage](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/understanding-smart-lists){target="_blank"}.

### Ajouter le filtre à une liste dynamique

1. Dans Marketo Engage, sélectionnez une campagne et cliquez sur l’onglet **[!UICONTROL Liste dynamique]**.

1. Dans la liste Filtres affichée à droite, saisissez `Member` et recherchez le filtre **[!UICONTROL Liste des membres de compte]**.

1. Faites glisser le filtre sur la zone de travail de la liste dynamique.

1. Dans la zone de travail Liste dynamique , définissez la valeur de liste **[!UICONTROL Membre du compte]**.

   Cliquez sur la flèche vers le bas pour afficher toutes les listes de comptes ou saisissez une partie du nom de la liste de comptes pour vous aider à localiser la liste de comptes dont vous avez besoin.

   ![Filtre de liste dynamique Marketo Engage pour l&#39;appartenance à la liste des comptes](./assets/account-lists-marketo-engage-smart-list.png){width="800" zoomable="yes"}

1. Dans le flux de la campagne, ajoutez l’étape **[!UICONTROL Ajouter à la liste]** et choisissez la liste dans laquelle vous souhaitez renseigner les personnes de la liste des comptes Journey Optimizer B2B edition.

   Pour plus d’informations sur l’ajout d’étapes à un flux _[](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/add-a-flow-step-to-a-smart-campaign){target="_blank"} consultez la section_ Ajouter une étape de flux à une campagne dynamique dans la documentation de Marketo Engage.

### Vérifier les membres

Une fois le flux exécuté, vous pouvez afficher la liste des personnes renseignées dans la liste. Ouvrez la liste et sélectionnez l’onglet Personnes .

![liste de campagnes Marketo Engage renseignée à partir d&#39;une liste de comptes](./assets/account-lists-marketo-engage-smart-list-people.png){width="800" zoomable="yes"}
