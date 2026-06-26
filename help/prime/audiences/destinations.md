---
title: Destinations
description: Découvrez comment connecter des destinations et activer des listes statiques de personnes dans Journey Optimizer B2B Prime pour exporter des données d’audience vers des plateformes publicitaires, de messagerie électronique et d’autres plateformes marketing.
autotag-review: '2026-06-17T18:30:02.442Z'
TQID: 'https://experienceleague.adobe.com/xO1p-VvIfv1KB77g0l2-fFRHQ0w2hy97vnG1QHpMw8c'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: af10a912422f1736fdc86e0609aee76f5d4daa46
workflow-type: tm+mt
source-wordcount: 289
ht-degree: 2%

---

# Destinations

Les destinations sont des intégrations préconfigurées qui vous permettent d’exporter des données de listes de personnes de [!DNL Adobe Journey Optimizer B2B Prime] vers des plateformes marketing externes telles que des réseaux publicitaires, des fournisseurs de services de messagerie électronique et des systèmes CRM. Dans [!DNL Journey Optimizer B2B Prime], vous activez les [listes de personnes statiques](./people-lists.md#static-list) (composées d’enregistrements de personne Marketo Engage) vers les destinations afin que ces audiences soient disponibles pour le ciblage et l’engagement dans les canaux en aval.

<!-- 
Does not align w/AEP info for Beta

Activating a static list to a destination follows a three-step process:

1. **Connect** — Authenticate and configure a connection to a destination platform.
1. **Map** — Select the static list and map its people attributes to the fields required by the destination.
1. **Schedule** — Define when and how often the list data is exported to the destination.

Destination activations reflect the membership state of the static list at the time of each synch.

## Destination types {#destination-types}

[!DNL Journey Optimizer B2B Prime] supports the following destination types for activating static people lists:

| Type | Description |
|--- |--- |
| Streaming | Real-time API-based connections that push audience membership updates to the destination as they occur. |
| File-based (batch) | Scheduled exports that deliver audience data as structured files to cloud storage or SFTP locations, which the destination platform then ingests. |

-->

## Connecter une destination {#connect-destination}

1. Dans le volet de navigation de gauche, développez **[!UICONTROL Connexions]** et sélectionnez **[!UICONTROL Destinations]**.

1. Dans l’onglet _[!UICONTROL Catalogue]_, recherchez le connecteur de type destination externe.

   >[!TIP]
   >
   >Vous pouvez rapidement trouver le connecteur en saisissant le nom, par exemple `LinkedIn`, dans la zone de recherche.

   ![Accéder aux types de connecteur disponibles](./assets/destinations-catalog.png){width="800" zoomable="yes"}

1. Dans la carte de connecteur, cliquez sur **[!UICONTROL Configurer une nouvelle destination]**.

1. Sélectionnez **[!UICONTROL Nouveau compte]** et saisissez les informations d’identification de votre compte.

   ![Connecter un nouveau compte de destination](./assets/destinations-configure-new.png){width="500"}

1. Cliquez sur **[!UICONTROL Se connecter à la destination]**.

   >[!IMPORTANT]
   >
   >À ce stade, **ne saisissez pas** les _[!UICONTROL détails de la destination]_. Seule la connexion est nécessaire.

1. Vérifiez les paramètres des actions marketing et de gouvernance des données, puis cliquez sur **[!UICONTROL Enregistrer]**.

La destination connectée apparaît dans la liste de l’onglet _[!UICONTROL Parcourir]_ et est disponible pour l’activation de la liste statique.

## Activation d’une liste statique vers une destination {#activate}

>[!NOTE]
>
>Seules les [listes de personnes statiques](./people-lists.md#static-list) peuvent être activées vers des destinations dans [!DNL Journey Optimizer B2B Prime]. Les [listes dynamiques](./people-lists.md#dynamic-lists) ne sont pas éligibles à l’activation de destination.

1. Dans le volet de navigation de gauche, développez **[!UICONTROL Gestion marketing]**.

1. À droite dans la liste de ressources **[!UICONTROL Marketing]**, sélectionnez **[!UICONTROL Listes des personnes]**.

   ![Accéder aux listes de personnes pour gérer vos audiences](./assets/people-lists.png){width="800" zoomable="yes"}

1. Sélectionnez l’onglet **[!UICONTROL Listes statiques]**.

1. Recherchez la liste statique que vous souhaitez activer vers une destination.

1. Cliquez sur l’icône _Activer_ ( ![Icône Activer](../../assets/do-not-localize/icon-falco-activate-dest.svg) ) en regard du nom de la liste statique.

1. Cochez la case correspondant à la connexion de destination configurée.

   ![Destinations configurées disponibles pour activation](./assets/static-list-activate-destination-select.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Enregistrer]**

<!--

This method not working for Beta

1. On the _[!UICONTROL Browse]_ tab, locate the destination you want to use for the activation and click the name to open it.

1. Select the **[!UICONTROL Activation data]** tab.

1. Click **[!UICONTROL Activate people lists]**.

1. Select the static people list you want to export and click **[!UICONTROL Next]**.

1. Map the people list attributes to the required fields of the destination schema and click **[!UICONTROL Next]**.

1. Set the export schedule:

   * **[!UICONTROL Frequency]** — Choose how often the list is exported (for example, daily or weekly).
   * **[!UICONTROL Start date]** — Set when the first export should run.

1. Review the activation summary and click **[!UICONTROL Finish]**.

The activation is created and the static list data is exported to the destination according to the defined schedule.

-->
