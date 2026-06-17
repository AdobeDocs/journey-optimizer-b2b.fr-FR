---
title: Écoute d’un nœud d’événement
description: Configurez Écouter pour les nœuds d’événement dans Journey Optimizer B2B edition Prime - définissez des déclencheurs d’événement, appliquez des filtres facultatifs et faites avancer les personnes lorsque des activités ou des modifications de données se produisent.
autotag-review: '2026-06-12T23:00:36.531Z'
TQID: 'https://experienceleague.adobe.com/SBEfrrIKSCnO5x1tGXQTz1EZryH0IKhQx4tuqVn78FI'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d0031543-532c-4a26-8f90-01af2b91e6d0id: ba367494-9862-4596-bd6f-299c7e10a46bid: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 3368f815edc0ce817cb7ed371157b63fa548d848
workflow-type: tm+mt
source-wordcount: 233
ht-degree: 8%

---

# Écoute d’un nœud d’événement

Ajoutez le nœud _Écouter un événement_ pour faire passer votre audience à l’étape suivante du parcours lorsqu’un événement se produit.

## Déclencheurs d’événement {#event-triggers}

Obtenir la liste à partir du PM

## Filtres d’événement {#event-filters}

Obtenir la liste mise à jour à partir du PM

| Filtres | Description |
| ------- | ----------- |
| Historique des activités > E-mail | Activités d&#39;email basées sur des conditions évaluées à l&#39;aide d&#39;un ou plusieurs emails sélectionnés : <li>Lien ayant fait l’objet d’un clic dans l’e-mail <li>E-mail ouvert |
| Historique des activités > Valeur des données modifiée | Pour un attribut de personne sélectionné, une modification de valeur s’est produite. Ces types de modifications sont les suivants : <li>Nouvelle valeur <li>Valeur précédente <li>Motif <li>Source <li>Date de l’activité <li> Min. nombre de fois |

## Ajouter un nœud d’événement {#add-event-node}

1. Accédez à la zone de travail de parcours.

1. Cliquez sur l’icône plus ( **+** ) d’un chemin et choisissez **[!UICONTROL Écouter un événement]**.

   ![Cliquez sur Ajouter une icône sur le chemin du parcours ](./assets/person-journey-canvas-add-node.png){width="200"}

1. Dans les propriétés de nœud sur la droite, cliquez sur **[!UICONTROL Ajouter des critères d’événement]**.

1. Dans la boîte de dialogue _[!UICONTROL Modifier l’événement]_, ajoutez les événements à déclencher.

   ![Modifier l’événement - Déclencheurs d’événement](./assets/edit-event-triggers.png){width="600" zoomable="yes"}

1. (Facultatif) Sélectionnez l’onglet **[!UICONTROL Filtres]** dans la boîte de dialogue et ajoutez des critères de filtrage pour les déclencheurs.

1. Cliquez sur **[!UICONTROL Modifier l’événement]** et définissez les détails de l’événement.

   ![Modifier l&#39;événement - Filtrage des événements](./assets/edit-event-filters.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Enregistrer]**

<!--
1. If needed, set the **[!UICONTROL Timeout]** option to limit the time period to listen for the event.

   >[!NOTE]
   >
   >The journey ends after a timeout unless you define a timeout path, where you can add other nodes.

   Enable the **[!UICONTROL Timeout]** option and select the duration for which the journey waits for an event to occur before it times out.

   You can choose to end the path here or take a different course of action by setting another path. To create a new path in the journey where you can add actions and events applicable to accounts when the event does not occur, select the **[!UICONTROL Set timeout path]** check box.

   ![Journey event node - set timeout path](../../user/journeys/assets/node-event-timeout-set-path.png){width="700" zoomable="yes"}
-->

>[!NOTE]
>
>La fonctionnalité de temporisation d’Écouter pour un nœud d’événement ne fonctionne pas actuellement. Il est prévu de le publier ultérieurement.
