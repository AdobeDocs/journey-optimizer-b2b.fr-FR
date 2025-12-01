---
title: Sélectionner des champs et des événements d’expérience
description: Sélectionnez des événements et des champs Experience Platform pour déclencher une prise de décision en temps réel dans les parcours en fonction du comportement du client.
feature: Setup, Integrations
role: Admin
badgeBeta: label="Beta" type="informative" tooltip="Cette fonctionnalité est actuellement en version bêta"
solution: Journey Optimizer B2B Edition, Experience Platform
exl-id: a7696d03-f4c4-4f64-8ef2-b15e59b59770
source-git-commit: 5f3d7bb8eb72c48409273de43b03114d273cb80c
workflow-type: tm+mt
source-wordcount: '1463'
ht-degree: 10%

---

# Sélectionner des événements d’expérience et des champs

Les administrateurs peuvent sélectionner des [événements d’expérience AEP spécifiques](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/experienceevent){target="_blank"} et leurs champs associés dans le schéma d’union des événements d’expérience. Une fois la sélection effectuée, les utilisateurs peuvent configurer des règles de prise de décision pour écouter ces événements d’expérience afin d’activer les actions de campagne dynamiques et ciblées basées sur les données d’événement en temps quasi réel.

<!-- ![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Watch the video overview](#overview-video) -->
L’utilisation des événements d’expérience AEP dans parcours est un processus en deux étapes :

1. Un administrateur [ajoute des événements et des champs d’expérience AEP](#add-an-event) dans les configurations Journey Optimizer B2B edition.

2. Dans un parcours, un spécialiste marketing ajoute un nœud _Écouter pour un événement_ et [ sélectionne un événement d’expérience](../journeys/listen-for-event-nodes.md#listen-for-an-experience-event).

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
>Dans la version bêta, vous ne pouvez pas supprimer des événements de la liste. Assurez-vous que chaque événement que vous ajoutez est un événement que votre organisation a l’intention d’utiliser.

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

   ![Cliquez sur l’icône du menu Plus ](./assets/configurations-xdm-classes-events-more-menu.png){width="500" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Modifier les champs]** pour ajouter d’autres champs ou supprimer des sélections existantes dans la boîte de dialogue _[!UICONTROL Sélectionner les champs]_.

1. Cliquez sur **[!UICONTROL Sélectionner]** pour enregistrer vos sélections.

### Supprimer un événement

>[!NOTE]
>
>Pour la version Beta de cette fonctionnalité, vous ne pouvez pas supprimer un événement de la liste des événements sélectionnés. La suppression d’événements est prévue pour la version mise à disposition générale.

## Événements et champs

Par [!DNL Journey Optimizer B2B Edition], certaines activités au niveau des personnes sont capturées en tant qu’événements d’expérience [!DNL Experience Platform]. Ces événements sont stockés dans un jeu de données système qui utilise le schéma d’événement d’expérience XDM et inclut des groupes de champs spécifiques au parcours. Vous pouvez utiliser ces événements dans [!UICONTROL Journey Optimizer B2B edition] comme tout autre événement d’expérience.

Chaque événement expose un ensemble défini de champs qui peuvent être utilisés dans le parcours _Écouter un événement_ nœuds (prise de décision basée sur des événements). Passez en revue les types d’événement disponibles et leurs champs pour déterminer l’événement et les champs à utiliser dans ces nœuds de parcours :

### E-mail envoyé

Cet événement effectue le suivi lorsqu’un e-mail marketing a été envoyé à une personne.

Type d’événement : `directMarketing.emailSent`

+++Champs

| Champ | Type de champ |
| ----- | ---------- |
| Identifiant | `_id` |
| Type d’événement | `eventType` |
| Date et heure | `timestamp` |
| ID de personne | `personID` |
| ID de source de la personne | `personKey.sourceID` |
| Type de source de la personne | `personKey.sourceType` |
| ID d’instance source de la personne | `personKey.sourceInstanceID` |
| Clé source de la personne | `personKey.sourceKey` |
| ID de la source de l’e-mail | `directMarketing.emailSent.mailingKey.sourceID` |
| Type de source de l’e-mail | `directMarketing.emailSent.mailingKey.sourceType` |
| Identifiant de l’instance source de l’e-mail | `directMarketing.emailSent.mailingKey.sourceInstanceID ` |
| Clé source de l’e-mail | `directMailing.emailSent.mailingKey.sourceKey` |
| Nom du publipostage | `directMarketing.emailSent.mailingName` |
| ID PARCOURS | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID de nœud | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-mail remis au destinataire

Cet événement effectue le suivi lorsqu’un e-mail a été correctement envoyé au service de messagerie d’une personne.

Type d’événement : `directMarketing.emailDelivered `

+++Champs

| Champ | Type de champ |
| ----- | ---------- |
| Identifiant | `_id` |
| Type d’événement | `eventType` |
| Date et heure | `timestamp` |
| ID de personne | `personID` |
| ID de source de la personne | `personKey.sourceID` |
| Type de source de la personne | `personKey.sourceType` |
| ID d’instance source de la personne | `personKey.sourceInstanceID` |
| Clé source de la personne | `personKey.sourceKey` |
| Identifiant de la source du publipostage | `directMarketing.mailingKey.sourceID` |
| Type de source de mailing | `directMarketing.mailingKey.sourceType` |
| Identifiant de l’instance source du mailing | `directMarketing.mailingKey.sourceInstanceID` |
| Clé source du mailing | `directMarketing.mailingKey.sourceKey` |
| Nom du publipostage | `directMarketing.mailingName` |
| ID PARCOURS | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID de nœud | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-mail ouvert

Cet événement effectue le suivi lorsqu’une personne a ouvert un e-mail marketing.

Type d’événement : `directMarketing.emailOpened`

+++Champs

| Champ | Type de champ |
| ----- | ---------- |
| Identifiant | `_id` |
| Type d’événement | `eventType` |
| Date et heure | `timestamp` |
| ID de personne | `personID` |
| ID de source de la personne | `personKey.sourceID` |
| Type de source de la personne | `personKey.sourceType` |
| ID d’instance source de la personne | `personKey.sourceInstanceID` |
| Clé source de la personne | `personKey.sourceKey` |
| Identifiant de la source du publipostage | `directMarketing.mailingKey.sourceID` |
| Type de source de mailing | `directMarketing.mailingKey.sourceType` |
| Identifiant de l’instance source du mailing | `directMarketing.mailingKey.sourceInstanceID` |
| Clé source du mailing | `directMarketing.mailingKey.sourceKey` |
| Nom du publipostage | `directMarketing.mailingName` |
| Est un appareil mobile | `device.isMobileDevice` |
| Modèle d’appareil | `device.model` |
| Agent utilisateur | `environment.browserDetails.userAgent` |
| Operating system (Système d’exploitation) | `environment.operatingSystem` |
| ID PARCOURS | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID de nœud | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-mail sur lequel l’utilisateur a cliqué

Cet événement effectue le suivi lorsqu’une personne clique sur un lien dans un e-mail marketing.

Type d’événement : `directMarketing.emailClicked`

+++Champs

| Champ | Type de champ |
| ----- | ---------- |
| Identifiant | `_id` |
| Type d’événement | `eventType` |
| Date et heure | `timestamp` |
| ID de personne | `personID` |
| ID de source de la personne | `personKey.sourceID` |
| Type de source de la personne | `personKey.sourceType` |
| ID d’instance source de la personne | `personKey.sourceInstanceID` |
| Clé source de la personne | `personKey.sourceKey` |
| Identifiant de la source du publipostage | `directMarketing.mailingKey.sourceID` |
| Type de source de mailing | `directMarketing.mailingKey.sourceType` |
| Identifiant de l’instance source du mailing | `directMarketing.mailingKey.sourceInstanceID` |
| Clé source du mailing | `directMarketing.mailingKey.sourceKey` |
| Nom du publipostage | `directMarketing.mailingName` |
| URL du lien | `directMarketing.linkURL` |
| Est un appareil mobile | `device.isMobileDevice` |
| Modèle | `device.model` |
| Agent utilisateur | `environment.browserDetails.userAgent` |
| Operating system (Système d’exploitation) | `environment.operatingSystem` |
| ID PARCOURS | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID de nœud | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-mail renvoyé

Cet événement effectue le suivi du rebond d’un e-mail envoyé à une personne.

Type d’événement : `directMarketing.emailBounced`

+++Champs

| Champ | Type de champ |
| ----- | ---------- |
| Identifiant | `_id` |
| Type d’événement | `eventType` |
| Date et heure | `timestamp` |
| ID de personne | `personID` |
| ID de source de la personne | `personKey.sourceID` |
| Type de source de la personne | `personKey.sourceType` |
| ID d’instance source de la personne | `personKey.sourceInstanceID` |
| Clé source de la personne | `personKey.sourceKey` |
| Identifiant de la source du publipostage | `directMarketing.mailingKey.sourceID` |
| Type de source de mailing | `directMarketing.mailingKey.sourceType` |
| Identifiant de l’instance source du mailing | `directMarketing.mailingKey.sourceInstanceID` |
| Clé source du mailing | `directMarketing.mailingKey.sourceKey` |
| Nom du publipostage | `directMarketing.mailingName` |
| E-mail | `directMarketing.email` |
| Code de rebond de l’e-mail | `directMarketing.emailBouncedCode` |
| Détails de l’e-mail rebond | `directMarketing.emailBouncedDetails` |
| ID PARCOURS | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID de nœud | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-mail renvoyé provisoirement

Cet événement effectue le suivi des soft bounces d&#39;un e-mail envoyé à une personne.

Type d’événement : `directMarketing.emailBouncedSoft`

+++Champs

| Champ | Type de champ |
| ----- | ---------- |
| Identifiant | `_id` |
| Type d’événement | `eventType` |
| Date et heure | `timestamp` |
| ID de personne | `personID` |
| ID de source de la personne | `personKey.sourceID` |
| Type de source de la personne | `personKey.sourceType` |
| ID d’instance source de la personne | `personKey.sourceInstanceID` |
| Clé source de la personne | `personKey.sourceKey` |
| Identifiant de la source du publipostage | `directMarketing.mailingKey.sourceID` |
| Type de source de mailing | `directMarketing.mailingKey.sourceType` |
| Identifiant de l’instance source du mailing | `directMarketing.mailingKey.sourceInstanceID` |
| Clé source du mailing | `directMarketing.mailingKey.sourceKey` |
| Nom du publipostage | `directMarketing.mailingName` |
| E-mail | `directMarketing.email` |
| Code de rebond de l’e-mail | `directMarketing.emailBouncedCode` |
| Détails de l’e-mail rebond | `directMarketing.emailBouncedDetails` |
| ID PARCOURS | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID de nœud | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-mail désinscrit

Cet événement effectue le suivi lorsqu’une personne s’est désabonnée d’un e-mail marketing.

Type d’événement : `directMarketing.emailUnsubscribed `

+++Champs

| Champ | Type de champ |
| ----- | ---------- |
| Identifiant | `_id` |
| Type d’événement | `eventType` |
| Date et heure | `timestamp` |
| ID de personne | `personID` |
| ID de source de la personne | `personKey.sourceID` |
| Type de source de la personne | `personKey.sourceType` |
| ID d’instance source de la personne | `personKey.sourceInstanceID` |
| Clé source de la personne | `personKey.sourceKey` |
| Identifiant de la source du publipostage | `directMarketing.mailingKey.sourceID` |
| Type de source de mailing | `directMarketing.mailingKey.sourceType` |
| Identifiant de l’instance source du mailing | `directMarketing.mailingKey.sourceInstanceID` |
| Clé source du mailing | `directMarketing.mailingKey.sourceKey` |
| Nom du publipostage | `directMarketing.mailingName` |
| ID PARCOURS | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID de nœud | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### Visite de page web

Ce type d’événement est la méthode standard pour marquer l’accès comme une page vue.

Type d’événement : `web.webpagedetails.pageViews`

+++Champs

| Champ | Type de champ |
| ----- | ---------- |
| Identifiant | `_id` |
| Type d’événement | `eventType` |
| Date et heure | `timestamp` |
| ID de personne | `personID` |
| ID de source de la personne | `personKey.sourceID` |
| Type de source de la personne | `personKey.sourceType` |
| ID d’instance source de la personne | `personKey.sourceInstanceID` |
| Clé source de la personne | `personKey.sourceKey` |
| Identifiant de la source de la page web | `web.webPageDetails.webPageKey.sourceID` |
| Type de source de la page web | `web.webPageDetails.webPageKey.sourceType` |
| Identifiant de l’instance source de la page web | `web.webPageDetails.webPageKey.sourceInstanceID` |
| Clé source de la page web | `web.webPageDetails.webPageKey.sourceKey` |
| Nom de la page web | `web.webPageDetails.name` |
| URL de la page web | `web.webPageDetails.URL` |
| Paramètres de requête des pages web | `web.webPageDetails.queryParameters` |
| Identifiant de la page web | `web.webPageDetails.webPageID` |
| Agent utilisateur | `environment.browserDetails.userAgent` |
| URL du référent | `web.webReferrer.URL` |

+++

### Formulaire rempli

Cet événement effectue le suivi lorsqu’une personne a rempli un formulaire sur une page web.

Type d’événement : `web.formFilledOut`

+++Champs

| Champ | Type de champ |
| ----- | ---------- |
| Identifiant | `_id` |
| Type d’événement | `eventType` |
| Date et heure | `timestamp` |
| ID de personne | `personID` |
| ID de source de la personne | `personKey.sourceID` |
| Type de source de la personne | `personKey.sourceType` |
| ID d’instance source de la personne | `personKey.sourceInstanceID` |
| Clé source de la personne | `personKey.sourceKey` |
| Identifiant de la source du formulaire web | `web.fillOutForm.webFormKey.sourceID` |
| Type de source du formulaire web | `web.fillOutForm.webFormKey.sourceType` |
| Identifiant de l’instance source du formulaire web | `web.fillOutForm.webFormKey.sourceInstanceID` |
| Clé source du formulaire web | `web.fillOutForm.webFormKey.sourceKey` |
| ID du formulaire web | `web.fillOutForm.webFormID` |
| Nom du formulaire web | `web.fillOutForm.webFormName` |
| Paramètres de requête des pages web | `web.webPageDetails.queryParameters` |
| Identifiant de la page web | `web.webPageDetails.webPageID` |
| Agent utilisateur | `environment.browserDetails.userAgent` |
| URL du référent | `web.webReferrer.URL` |

+++

### Lien web sur lequel l’utilisateur a cliqué

L’événement signale que le SDK Web a automatiquement enregistré un clic sur le lien.

Type d’événement : `web.webinteraction.linkClicks`

+++Champs

| Champ | Type de champ |
| ----- | ---------- |
| Identifiant | `_id` |
| Type d’événement | `eventType` |
| Date et heure | `timestamp` |
| ID de personne | `personID` |
| ID de source de la personne | `personKey.sourceID` |
| Type de source de la personne | `personKey.sourceType` |
| ID d’instance source de la personne | `personKey.sourceInstanceID` |
| Clé source de la personne | `personKey.sourceKey` |
| Identifiant de la source de l&#39;interaction web | `web.webInteraction.webInteractionKey.sourceID` |
| Type de source de l&#39;interaction web | `web.webInteraction.webInteractionKey.sourceType` |
| Identifiant de l&#39;instance source de l&#39;interaction web | `web.webInteraction.webInteractionKey.sourceInstanceID` |
| Clé source de l’interaction web | `web.webInteraction.webInteractionKey.sourceKey` |
| Identifiant du lien de l&#39;interaction web | `web.webInteraction.linkID` |
| URL du lien d&#39;interaction web | `web.webInteraction.linkURL` |
| Paramètres de requête des pages web | `web.webPageDetails.queryParameters` |
| Identifiant de la page web | `web.webPageDetails.webPageID` |
| Agent utilisateur | `environment.browserDetails.userAgent` |
| URL du référent | `web.webReferrer.URL` |

+++

### Moment significatif

Cet événement permet de déterminer à quel moment un moment intéressant a été enregistré pour une personne.

Type d’événement : `leadOperation.interestingMoment `

+++Champs

| Champ | Type de champ |
| ----- | ---------- |
| Identifiant | `_id` |
| Type d’événement | `eventType` |
| Date et heure | `timestamp` |
| ID de personne | `personID` |
| ID de source de la personne | `personKey.sourceID` |
| Type de source de la personne | `personKey.sourceType` |
| ID d’instance source de la personne | `personKey.sourceInstanceID` |
| Clé source de la personne | `personKey.sourceKey` |
| Date du moment | `leadOperation.interestingMoment.date` |
| Description du moment | `leadOperation.interestingMoment.description` |
| Source du moment | `leadOperation.interestingMoment.source` |
| Type de moment | `leadOperation.interestingMoment.type` |
| ID PARCOURS | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID de nœud | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

<!-- ## Overview video

>[!VIDEO](https://video.tv.adobe.com/v/3448637/?learn=on) -->