---
title: Gérer le suivi des ouvertures d’e-mail
description: Désactivez le suivi des ouvertures d’e-mail pour un e-mail individuel ou capturez les préférences de suivi d’une personne et utilisez un chemin de partage pour envoyer des variantes d’e-mail de suivi et de non-suivi.
feature: Account Journeys, Channels
topic: Content Management
role: User
level: Beginner, Intermediate
autotag-review: '2026-07-08T00:02:50.497Z'
TQID: 'https://experienceleague.adobe.com/LIutoajlpVQTeJP2y4i0Wv7H-WqGj-c-LVsOGfin384'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: d6e625c1-468f-4d73-9f32-fd1edb87f96bid: e666e996-b2cf-4c45-8fc2-1c625212ababid: f01b5556-e951-40ba-8625-2e3001864f2b
subfeature_v2: id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 61481d57fb8eca805d9a9bc545124aed568b5416
workflow-type: tm+mt
source-wordcount: 860
ht-degree: 0%

---

# Gérer le suivi des ouvertures d’e-mail

Vous pouvez désactiver le suivi des ouvertures pour un e-mail individuel ou capturer les préférences de suivi de chaque personne dans Adobe Experience Platform et utiliser un chemin de partage pour acheminer les personnes vers des variantes d’e-mail de suivi et de non-suivi.

>[!BEGINSHADEBOX « Conseils de la CNIL sur les pixels de tracking email »]

Le 14 avril 2026, la *Commission nationale de l&#39;informatique et des libertés* (CNIL) a publié une [recommandation sur l&#39;utilisation des pixels de tracking dans les emails](https://www.cnil.fr/sites/default/files/2026-04/recommandation-pixels_de_suivi.pdf). Ces conseils clarifient le moment où le consentement est requis et soulignent l’importance de bonnes pratiques de consentement pour le suivi des pixels d’e-mail. Cette politique peut avoir un impact sur les pratiques d’envoi pour toute entité diffusant des e-mails aux abonnés basés en France.

Un pixel de tracking d’e-mail est une image transparente 1x1 incorporée dans l’HTML d’un e-mail. Lorsque le client de messagerie du destinataire charge cette image, le pixel envoie un ping à un serveur qui enregistre des données telles qu’une date et une heure, un type d’appareil, un client de messagerie et parfois une adresse IP pour un emplacement approximatif. Ce journal est ensuite lié à l’enregistrement d’un destinataire, ce qui permet aux spécialistes marketing de savoir si un e-mail est ouvert.

Les fonctionnalités du produit [!UICONTROL Journey Optimizer B2B edition] décrites ici sont des blocs de construction qui, configurés et utilisés de manière appropriée, peuvent prendre en charge une implémentation conforme. Chaque client est responsable de déterminer et de respecter ses obligations en vertu de la loi applicable.

>[!ENDSHADEBOX]

## Désactiver le tracking d’un seul email {#disable-tracking-single-email}

Utilisez cette option pour qu’un e-mail spécifique ne signale jamais l’activité d’ouverture, quelle que soit la personne qui le reçoit.

1. Dans les propriétés du nœud de parcours à droite, ouvrez l’e-mail.

1. Dans les propriétés de l’e-mail, cochez la case **[!UICONTROL Désactiver le suivi des ouvertures]**.

   ![Désactiver le suivi des ouvertures d’e-mail](./assets/email-tracking-disable-all.png){width="500" zoomable="yes"}

   Pour obtenir la liste complète des propriétés d’e-mail](./add-email.md#define-the-email-settings) voir [ Définir les paramètres d’e-mail .

## Segmenter les personnes en fonction des préférences de tracking {#segment-people-tracking-preference}

Si vous souhaitez laisser chaque personne choisir si ses ouvertures d’e-mail sont suivies, capturez cette préférence en tant qu’attribut de personne dans Adobe Experience Platform (AEP). Vous pouvez utiliser ce champ dans un [formulaire de page de destination](./forms.md) afin que vos contacts aient la possibilité de se désinscrire du suivi des ouvertures d’e-mails. Vous pouvez ensuite utiliser un nœud _Chemins partagés_ dans vos parcours pour acheminer les personnes assurant et ne assurant pas le suivi vers différentes variantes d’e-mail. Vous pouvez ainsi honorer un opt-out individuel sans désactiver le suivi des ouvertures pour tout le monde.

Le workflow comporte trois parties :

1. [Ajoutez un champ personnalisé pour les préférences de tracking](#add-custom-field-tracking-preference) dans AEP et envoyez une communication d’opt-out avec un lien de formulaire.
1. [Ajoutez un chemin de partage pour le suivi des désinscriptions](#add-split-path-tracking) dans le parcours.
1. [Configurez les variantes d’e-mail de suivi et de non-suivi](#configure-tracking-and-non-tracking-email-variants) pour chaque chemin.

### Ajout d’un champ personnalisé pour les préférences de tracking {#add-custom-field-tracking-preference}

>[!NOTE]
>
>L’ajout et le mappage de champs XDM personnalisés sont une tâche d’administration de Adobe Experience Platform. Contactez votre administrateur AEP ou votre équipe d’ingénierie des données pour effectuer cette étape.

1. Dans AEP, ouvrez le schéma utilisé pour votre profil de personne B2B (par exemple, _Personne B2B_).

1. Sous l’identifiant client, recherchez ou créez un groupe de champs pour les champs de gestion du consentement de votre organisation (par exemple, `consents`).

1. Ajoutez un champ au groupe de champs, tel qu’un champ booléen nommé `emailTracking`, pour indiquer si la personne a consenti au suivi des ouvertures.

1. Saisissez le nom et le nom d’affichage du champ, définissez le type, affectez-le au groupe de champs, puis cliquez sur **[!UICONTROL Appliquer]**.

1. Cliquez sur **[!UICONTROL Enregistrer]** pour enregistrer les modifications apportées au schéma.

   ![Ajouter le champ emailTracking au groupe de champs de consentement du schéma AEP](./assets/email-tracking-xdm-field-aep-schema.png){width="800" zoomable="yes"}

1. Rendez le champ disponible dans [!DNL Journey Optimizer B2B Edition] en le sélectionnant en tant que _Champ géré_ pour la classe [!UICONTROL Profil individuel XDM] dans la [Gestion des champs XDM](../admin/xdm-field-management.md#managed-fields).

   ![Sélectionnez emailTracking comme champ géré dans la gestion des champs XDM](./assets/email-tracking-xdm-field-select.png){width="450"}

   Le champ est ainsi disponible en tant que condition dans les nœuds de chemin de division.

### Ajouter un chemin de partage pour le suivi des désinscriptions {#add-split-path-tracking}

Ajoutez à votre parcours un nœud [_Partage des chemins par personnes_ ](../journeys/split-merge-paths-nodes.md#split-paths-by-people) et définissez un chemin pour chaque valeur de préférence de suivi.

1. Ajoutez un nœud **[!UICONTROL Chemins partagés]** et choisissez **[!UICONTROL Personnes]** pour le partage.

1. Pour le premier chemin, appliquez une condition à l’aide de votre champ de préférence de suivi personnalisé (par exemple, `emailTracking` est `true`) pour identifier les personnes qui autorisent le suivi des ouvertures.

   ![Condition de chemin de partage : ajoutez le champ de tracking e-mail true](./assets/email-tracking-condition-true.png){width="700" zoomable="yes"}

1. Ajoutez un deuxième chemin et appliquez la condition inverse (`emailTracking` est `false`) pour identifier les personnes qui se sont désinscrites du suivi.

   Pour obtenir des instructions générales sur l’ajout de chemins, l’application de conditions et la réorganisation des chemins, consultez [Ajouter un chemin de partage par nœud de personnes](../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node).

   ![Partage du chemin par personnes - conditions d’activation et de désactivation du suivi des e-mails](./assets/email-tracking-split-paths.png){width="500" zoomable="yes"}

### Configuration des variantes d’e-mail de tracking et de non-tracking {#configure-tracking-and-non-tracking-email-variants}

Ajoutez un nœud d’action [_[!UICONTROL Envoyer un e-mail ]_](./add-email.md) à chaque chemin d’accès afin que chaque personne reçoive la variante d’e-mail correspondant à sa préférence de suivi.

1. Sur le chemin activé pour le suivi, ajoutez une action **[!UICONTROL Envoyer un e-mail]** et sélectionnez ou créez l’e-mail comme d’habitude, en laissant **[!UICONTROL Désactiver le suivi des ouvertures]** effacé dans les propriétés d’e-mail.

1. Sur le chemin d’accès d’exclusion, ajoutez une action **[!UICONTROL Envoyer un e-mail]** à l’aide du même e-mail ou d’un e-mail dupliqué, puis cochez la case **[!UICONTROL Désactiver le suivi des ouvertures]** dans les propriétés d’e-mail à droite.

   ![E-mail pour le suivi du chemin - Désactivez le suivi des ouvertures](./assets/email-tracking-disable.png){width="600" zoomable="yes"}

1. [Publiez le parcours](../journeys/create-publish-journey.md#publish-a-journey).

   Les personnes sont automatiquement acheminées vers la variante d’e-mail qui correspond à la valeur de leur champ de préférence de suivi, et toutes les mises à jour qu’elles apportent à leur préférence sont reflétées la prochaine fois qu’elles entrent dans le parcours.
