---
title: '[!DNL Adobe Target] des audiences externes'
description: Activer des audiences externes vers par le biais  [!DNL Adobe Target]  parcours de compte. Personnalisez les expériences web B2B et conservez la cohérence entre les plateformes.
feature: Integrations, Audiences, Account Journeys
role: User, Admin
source-git-commit: 598546c62cb2d567f19b26f7f760aa43e4dd0bc9
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 1%

---

# [!DNL Adobe Target] des audiences externes

Vous pouvez activer et personnaliser des expériences pour des audiences externes dans [!DNL Adobe Target] par le biais de parcours de compte. Utilisez cette intégration pour obtenir une personnalisation avancée et personnalisée qui accroît l’engagement et pour maintenir la cohérence entre les plateformes sur l’ensemble des [!DNL Target] et des [!DNL Journey Optimizer B2B Edition]. Cette cohérence permet aux équipes d’aligner et de personnaliser les canaux web pour les groupes d’achats sur l’ensemble du parcours des acheteurs B2B.

Il s’agit d’un workflow en deux étapes permettant d’activer une audience externe via Adobe Target :

1. [Ajouter à une audience client externe](#add-to-customer-external-audience-from-a-journey) à partir d’un parcours.
2. [Activez l’audience externe](#activate-the-external-audience-to-target-as-a-destination) pour la [!DNL Target] en tant que destination dans Experience Platform.

## Ajouter à l’audience externe du client à partir d’un parcours

Dans votre parcours, [ajoutez un nœud _Prendre une action_](../journeys/action-nodes.md) pour exécuter l’action _[!UICONTROL Ajouter à l’audience externe du client]_. Les actions sont généralement ce que vous souhaitez qu’il se produise à la suite d’un déclencheur, tel qu’un événement ou une action précédente. Le parcours exécute l’action lorsqu’un compte qualifié avec des profils de personne atteint le nœud .

>[!NOTE]
>
>Lorsqu’un compte qualifié avec des profils de personne atteint le nœud _Ajouter à l’audience externe du client_ dans un parcours publié, l’alimentation de ces profils dans l’audience externe peut prendre jusqu’à 48 heures.

1. Lorsque le nœud _Prendre une mesure_ est sélectionné dans la zone de travail du parcours, choisissez l’option _[!UICONTROL Action sur]_ **[!UICONTROL Personnes]**.

1. Pour _[!UICONTROL Action sur les personnes]_, choisissez **[!UICONTROL Ajouter à l’audience externe du client]**.

   ![nœud de Parcours - agir sur les personnes - ajouter à l’audience externe du client](./assets/node-add-external-audience.png){width="550" zoomable="yes"}

1. Dans les propriétés de nœud sur la droite, définissez l’audience externe.

   * Si une ou plusieurs audiences externes sont déjà créées, vous pouvez choisir **[!UICONTROL Sélectionner une audience existante]** et [sélectionner l’audience à utiliser](#choose-an-external-audience).

   * Si vous souhaitez [créer une audience](#create-an-external-audience) à utiliser pour le nœud, choisissez **[!UICONTROL Créer]**.

### Création d’une audience externe

1. Après avoir sélectionné l’option **[!UICONTROL Créer]** dans les propriétés du nœud, cliquez sur **[!UICONTROL Créer une audience client externe]**.

   ![Agir sur les personnes - Ajouter à l’audience externe du client - Créer une option](./assets/node-add-external-audience-create-new-option.png){width="400"}

1. Dans la boîte de dialogue, saisissez un **[!UICONTROL Nom]** (obligatoire) et un **[!UICONTROL Description]** (facultatif) pour la nouvelle audience.

   ![Boîte de dialogue Créer une audience client externe](./assets/create-external-customer-audience-dialog.png){width="400"}

1. Cliquez sur **[!UICONTROL Créer]**.

   Le système crée l’audience et affiche un message de confirmation. Vous pouvez ensuite l’utiliser comme audience existante pour l’action de nœud.

### Sélectionner une audience externe

1. Après avoir choisi l’option **[!UICONTROL Sélectionner un client existant]** dans les propriétés du nœud, cliquez sur **[!UICONTROL Sélectionner une audience client externe]**.

   ![Agir sur les personnes - Ajouter à l’audience externe du client - Sélectionner l’option existante](./assets/node-add-external-audience-select-existing-option.png){width="300"}

1. Dans la boîte de dialogue _[!UICONTROL Ajouter une audience]_, sélectionnez l’audience que vous souhaitez utiliser.

   Vous pouvez saisir du texte dans le champ _Rechercher_ pour filtrer les éléments affichés afin qu’ils correspondent au nom de l’audience.

   ![Agir sur les personnes - Ajouter à une audience client externe - Boîte de dialogue Ajouter une audience](./assets/add-audience-dialog.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Ajouter une audience]**.

## Activation de l’audience externe vers Target en tant que destination

L’activation de l’audience externe vers Adobe Target nécessite que vous ayez configuré [!DNL Adobe Target] comme destination dans [!DNL Real-time Customer Data Platform (RTCDP)]. Pour plus d&#39;informations sur cette configuration, consultez la documentation de RTCDP [&#128279;](https://experienceleague.adobe.com/fr/docs/platform-learn/tutorials/destinations/target/configure-the-target-destination){target="_blank"}.

>[!IMPORTANT]
>
>L’utilisation de l’activation par le biais d’un parcours nécessite que votre implémentation de RTCDP utilise l’adresse électronique comme identité.

Le processus d’activation nécessite l’ajout de [!DNL Adobe Target] en tant qu’audience externe ou destination externe. Commencez par créer une audience [!DNL Target] dans le créateur d’audiences. Vous pouvez également créer un espace réservé à l’audience et ajouter la fonctionnalité d’audience externe.

>[!BEGINSHADEBOX]

![Icône Autorisations AEP](../../assets/do-not-localize/icon_permissions-outline.svg) Ces étapes nécessitent les autorisations suivantes pour le rôle utilisateur qui vous a été attribué :

* **[!UICONTROL Experience Platform]** - Pour la ressource _[!UICONTROL Destinations]_ : `Activate Destinations`, `Manage and Activate Dataset Destination` et `View Destination`
* **[!DNL Target]** - `Approver`

>[!ENDSHADEBOX]

1. Dans Experience Platform, accédez à **[!UICONTROL Connexions]** > **[!UICONTROL Destinations]** dans le volet de navigation de gauche.

1. Sélectionnez l’onglet **[!UICONTROL Parcourir]**.

1. Recherchez la connexion de destination à utiliser pour activer des segments, cliquez sur l’icône _Plus de menu_ ( **...** ) à côté du nom, puis sélectionnez **[!UICONTROL Activer des audiences]**.

   Saisissez du texte dans le champ _[!UICONTROL Rechercher]_ pour filtrer les destinations affichées pour une correspondance par nom.

   ![Experience Platform - destinations - parcourir les destinations Target - menu plus &#x200B;](./assets/aep-destinations-activate-target-audience.png){width="800" zoomable="yes"}

1. Dans la liste _[!UICONTROL Audiences disponibles]_, sélectionnez votre audience externe et cliquez sur **[!UICONTROL Suivant]**.

   ![Experience Platform - destinations - parcourir les destinations Target - menu plus &#x200B;](./assets/aep-destinations-activate-target-audience-available-audiences.png){width="700" zoomable="yes"}

1. Effectuez un mappage de champs supplémentaire à la destination (facultatif) et cliquez sur **[!UICONTROL Suivant]**.

1. Vérifiez les nouveaux paramètres d’audience et cliquez sur **[!UICONTROL Terminer]**.

   ![Experience Platform - destinations - activer la destination - vérifier](./assets/aep-destinations-activate-target-audience-review.png){width="700" zoomable="yes"}

Lors de l’activation, vous pouvez voir l’audience dans [les audiences Adobe Target](https://experienceleague.adobe.com/fr/docs/target/using/audiences/create-audiences/audiences#use-list){target="_blank"} et les utiliser dans les activités Adobe Target.

