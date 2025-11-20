---
title: Sélectionner des champs et des événements d’expérience
description: Sélectionnez des événements et des champs Experience Platform pour déclencher une prise de décision en temps réel dans les parcours en fonction du comportement du client.
feature: Setup, Integrations
role: Admin
badgeBeta: label="Beta" type="informative" tooltip="Cette fonctionnalité est actuellement en version bêta"
solution: Journey Optimizer B2B Edition, Experience Platform
exl-id: a7696d03-f4c4-4f64-8ef2-b15e59b59770
source-git-commit: 046d3648c5e482a69719d0095c297a766dd852ea
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%

---

# Sélectionner des événements d’expérience et des champs

Les administrateurs peuvent sélectionner des [événements d’expérience AEP spécifiques](https://experienceleague.adobe.com/fr/docs/experience-platform/xdm/classes/experienceevent){target="_blank"} et leurs champs associés dans le schéma d’union des événements d’expérience. Une fois la sélection effectuée, les utilisateurs peuvent configurer des règles de prise de décision pour écouter ces événements d’expérience afin d’activer les actions de campagne dynamiques et ciblées basées sur les données d’événement en temps quasi réel.

<!-- ![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Watch the video overview](#overview-video) -->
L’utilisation des événements d’expérience AEP dans parcours est un processus en deux étapes :

1. Un administrateur [ajoute des événements et des champs d’expérience AEP](#add-an-event) dans les configurations Journey Optimizer B2B edition.

2. Dans un parcours, un spécialiste marketing ajoute un nœud _Écouter pour un événement_ et [&#x200B; sélectionne un événement d’expérience](../journeys/listen-for-event-nodes.md#listen-for-an-experience-event).

   * Sélectionne l’événement à utiliser dans le nœud .
   * Sélectionne les champs à utiliser comme contraintes.

>[!BEGINSHADEBOX]

## Instructions et restrictions

Lorsque vous sélectionnez des événements pour atteindre les objectifs de votre organisation, tenez compte des points suivants :

* Vous pouvez sélectionner jusqu’à 50 événements et 100 champs par événement.

* Parcours peut écouter les événements d’expérience ingérés à l’aide des fonctionnalités de diffusion en continu d’Experience Platform, telles que l’API Web SDK ou HTTP.

* Vous pouvez utiliser les événements d’expérience à des fins de prise de décision dans un parcours, mais ils ne sont pas conservés. Par conséquent, vous ne pouvez pas utiliser un enregistrement historique des événements d’expérience dans Journey Optimizer B2B edition.

* Lorsque vous utilisez un événement d’expérience et publiez le parcours, vous pouvez ajouter d’autres champs, mais vous ne pouvez pas supprimer les champs précédemment sélectionnés.

* Vous pouvez référencer un événement d’expérience dans plusieurs parcours ou en utiliser un plusieurs fois dans le même parcours.

>[!ENDSHADEBOX]

## Gestion des événements d’expérience

1. Dans le volet de navigation de gauche, choisissez **[!UICONTROL Administration]** > **[!UICONTROL Configurations]**.

1. Cliquez sur **[!UICONTROL Classes XDM]** dans le panneau intermédiaire, puis sur l’onglet **[!UICONTROL Événements]** pour afficher la liste des événements disponibles.

   ![Accéder aux événements d’expérience sélectionnés](./assets/configurations-xdm-classes-events.png){width="800" zoomable="yes"}

   Le tableau est trié selon la colonne _[!UICONTROL Dernière mise à jour]_, les événements les plus récemment mis à jour étant en haut par défaut.

   Sur cette page, vous pouvez [sélectionner](#add-an-event) et [modifier](#edit-an-event) les événements à utiliser dans les parcours.

   Pour accéder aux détails d’un événement sélectionné, cliquez sur son nom.

### Filtrer la liste des événements

Saisissez du texte dans le champ _[!UICONTROL Rechercher]_ pour filtrer les événements affichés afin qu’ils correspondent au nom de l’événement.

![Filtrer la liste des événements sélectionnés par nom](./assets/configurations-xdm-classes-events-search.png){width="600" zoomable="yes"}

### Ajouter un événement

Pour rendre un événement d’expérience disponible pour un nœud _Écouter un événement_ dans un parcours, sélectionnez l’événement et les champs pris en charge.

>[!NOTE]
>
>Dans la version bêta, vous ne pouvez pas supprimer des événements de la liste. Assurez-vous que chaque événement ajouté est destiné à être utilisé par votre organisation.

1. Cliquez sur **[!UICONTROL Sélectionner un événement d’expérience]** en haut à droite.

   La page de détails de l’événement s’affiche. Sur cette page, vous pouvez choisir le type d’événement et les champs.

   ![Détails de l’événement pour un nouvel événement](./assets/configurations-xdm-classes-events-select-new.png){width="700" zoomable="yes"}

1. Choisissez le type d’événement.

   * Cliquez sur **[!UICONTROL Sélectionner le type d’événement]**.

   * Dans la boîte de dialogue, choisissez le type d’événement.

     Utilisez le champ _[!UICONTROL Rechercher]_ pour filtrer la liste affichée par nom. Utilisez le curseur **[!UICONTROL Afficher uniquement les champs sélectionnés]** pour passer en revue les sélections actuelles.

     ![Boîte de dialogue Sélectionner le type d’événement](./assets/configurations-xdm-classes-select-event-type-dialog.png){width="450" zoomable="yes"}

   * Cliquez sur **[!UICONTROL Sélectionner]**.

1. Choisissez un ou plusieurs champs pour le type d&#39;événement.

   * Cliquez sur **[!UICONTROL Sélectionner les champs]**.

   * Dans la boîte de dialogue, sélectionnez les champs à utiliser comme contraintes pour les événements correspondants.

     Utilisez le champ _[!UICONTROL Rechercher]_ pour filtrer la liste affichée par nom. Utilisez le curseur **[!UICONTROL Afficher uniquement les champs sélectionnés]** pour passer en revue les sélections actuelles.

     ![Boîte de dialogue Sélectionner les champs](./assets/configurations-xdm-classes-select-fields-dialog.png){width="450" zoomable="yes"}

   * Cliquez sur **[!UICONTROL Sélectionner]**.

1. Dans la page des détails de l&#39;événement, cliquez sur **[!UICONTROL Enregistrer]**.

L&#39;événement enregistré est affiché dans la liste de l&#39;onglet _[!UICONTROL Événements]_.

### Modification d’un événement

Modifiez les détails de l’événement pour modifier les champs.

1. Cliquez sur le nom de l’événement ou cliquez sur l’icône _Plus_ ( **...** ) et choisissez **[!UICONTROL Modifier]**.

   ![Cliquez sur l’icône du menu Plus &#x200B;](./assets/configurations-xdm-classes-events-more-menu.png){width="500" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Modifier les champs]** pour ajouter d’autres champs ou supprimer des sélections existantes dans la boîte de dialogue _[!UICONTROL Sélectionner les champs]_.

1. Cliquez sur **[!UICONTROL Sélectionner]** pour enregistrer vos sélections.

### Supprimer un événement

>[!NOTE]
>
>Pour la version Beta de cette fonctionnalité, vous ne pouvez pas supprimer un événement de la liste des événements sélectionnés. La suppression d’événements est prévue pour la version mise à disposition générale.

<!-- ## Overview video

>[!VIDEO](https://video.tv.adobe.com/v/3448637/?learn=on) -->