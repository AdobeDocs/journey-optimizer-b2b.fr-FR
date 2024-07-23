---
title: Création de SMS
description: Découvrez comment envoyer des SMS à vos clients sur leurs appareils mobiles, ainsi que comment personnaliser et prévisualiser des messages au format texte à partir de l’éditeur de SMS.
feature: SMS Authoring, Content
exl-id: bd648253-74de-4083-a37a-ab7ceaea2746
source-git-commit: e0d9359560f31b3e66f593426c66e64d31044d54
workflow-type: tm+mt
source-wordcount: '1244'
ht-degree: 0%

---

# Création de SMS

Utilisez Adobe Journey Optimizer B2B Edition pour envoyer des SMS à vos clients sur leurs appareils mobiles. Vous pouvez créer, personnaliser et prévisualiser des messages au format texte à partir de l&#39;éditeur de SMS.

## Paramétrages des SMS

L’édition B2B de Adobe Journey Optimizer envoie des messages texte par le biais de fournisseurs de services SMS (ou fournisseurs de passerelle SMS). Avant de créer votre SMS, configurez votre fournisseur de services à partir des paramètres Administrateur.

### Fournisseurs de services de passerelle SMS

Adobe Journey Optimizer version B2B s’intègre actuellement aux fournisseurs tiers qui offrent des services de messagerie texte de manière indépendante. Les fournisseurs pris en charge pour la messagerie texte sont Sinch, Twilio et Infobip.

Avant de configurer un canal SMS dans Adobe Journey Optimizer B2B Edition, vous devez créer un compte auprès de l’un de ces fournisseurs pour obtenir votre jeton API et votre ID de service. Ces informations d’identification sont requises pour configurer la connexion entre Adobe Journey Optimizer B2B Edition et le fournisseur concerné.

>[!IMPORTANT]
>
>Votre utilisation des services de messagerie texte est soumise à des conditions supplémentaires de la part du fournisseur concerné. En tant que solutions tierces, Sinch, Twilio et Infobip sont disponibles pour les utilisateurs de Adobe Journey Optimizer B2B Edition via une intégration. Adobe ne contrôle pas et n’est pas responsable des produits tiers. Pour tout problème ou toute demande d&#39;assistance relative aux services de messagerie texte (SMS), contactez votre fournisseur.

### Vérification d’une configuration d’API SMS existante

>[!NOTE]
>
>Les paramètres décrits sont accessibles uniquement aux utilisateurs disposant de droits d’administrateur SMS.

Dans le volet de navigation de gauche, développez la section **[!UICONTROL Administrator]** et cliquez sur **[!UICONTROL Configuration]**.

![Accès à la configuration des informations d’identification de l’API AMA](./assets/config-sms-api.png){width="800" zoomable="yes"}

La page répertorie les configurations d’API disponibles pour votre instance. Vous pouvez filtrer les informations d’identification de l’API affichées par le fournisseur ou le créateur de services SMS.

![Cliquez sur l’icône de filtre pour filtrer la liste des informations d’identification de l’API](./assets/config-sms-api-filter.png){width="500"}

### Création d’informations d’identification API pour un fournisseur de service SMS

>[!BEGINTABS]

>[!TAB Sinch]

_Pour configurer Sinch en tant que fournisseur de SMS avec Adobe Journey Optimizer B2B Edition :_

1. Dans le volet de navigation de gauche, développez la section **[!UICONTROL Administrator]** et cliquez sur **[!UICONTROL Configuration]**.

1. Cliquez sur le bouton **[!UICONTROL Créer de nouvelles informations d’identification d’API]** en haut à droite de la liste _[!UICONTROL informations d’identification d’API]_.

1. Configurez vos informations d’identification d’API SMS :

   ![Configuration des informations d’identification de l’API SMS Sinch](./assets/config-sms-api-sinch.png){width="500"}

   * **[!UICONTROL Fournisseur de SMS]** - Sélectionnez `Sinch` comme fournisseur de SMS.

   * **[!UICONTROL Nom]** - Entrez un nom pour vos informations d’identification API.

   * **[!UICONTROL ID de service]** et **[!UICONTROL Jeton API]** - Accédez à la page API à partir de votre compte Sinch (vous trouverez vos informations d’identification sous l’onglet SMS).

   Pour plus d’informations sur la recherche de ces informations pour votre compte Sinch, consultez la [documentation pour les développeurs Sinch](https://developers.sinch.com/docs/sms/getting-started/#2-get-credentials)

1. Cliquez sur **[!UICONTROL Envoyer]** lorsque les détails de configuration de vos informations d’identification d’API sont terminés.

>[!TAB Twilio]

_Pour configurer Twilio en tant que fournisseur de SMS avec Adobe Journey Optimizer B2B Edition :_

1. Dans le volet de navigation de gauche, développez la section **[!UICONTROL Administrator]** et cliquez sur **[!UICONTROL Configuration]**.

1. Cliquez sur le bouton **[!UICONTROL Créer de nouvelles informations d’identification d’API]** en haut à droite de la liste _[!UICONTROL informations d’identification d’API]_.

1. Configurez vos informations d’identification d’API SMS :

   ![Configuration des informations d’identification de l’API SMS Twilio](./assets/config-sms-api-twilio.png){width="500"}

   * **[!UICONTROL Fournisseur de SMS]** - Sélectionnez `Twilio` comme fournisseur de SMS.

   * **[!UICONTROL Nom]** - Entrez un nom pour votre définition d’informations d’identification d’API.

   * **[!UICONTROL Compte SID]** et **[!UICONTROL Jeton d’authentification]** - Accédez au volet _Informations sur le compte_ de votre page de tableau de bord de la console Twilio pour trouver vos informations d’identification.

   Pour plus d’informations sur la recherche de ces informations pour votre compte Twilio, consultez le [Centre d’aide de Twilio](https://help.twilio.com/articles/14726256820123-What-is-a-Twilio-Account-SID-and-where-can-I-find-it-).

1. Cliquez sur **[!UICONTROL Submit]** en haut à droite de la page lorsque les détails de configuration de vos informations d’identification d’API sont terminés.

>[!TAB Infobip]

_Pour configurer Infobip en tant que fournisseur de SMS avec Adobe Journey Optimizer B2B Edition :_

1. Dans le volet de navigation de gauche, développez la section **[!UICONTROL Administrator]** et cliquez sur **[!UICONTROL Configuration]**.

1. Cliquez sur le bouton **[!UICONTROL Créer de nouvelles informations d’identification d’API]** en haut à droite de la liste _[!UICONTROL informations d’identification d’API]_.

1. Configurez vos informations d’identification d’API SMS :

   ![Configuration des informations d’identification de l’API SMS Infobip](./assets/config-sms-api-infobip.png){width="500"}

   * **[!UICONTROL Fournisseur de SMS]** - Sélectionnez `Infobip` comme fournisseur de SMS.

   * **[!UICONTROL Nom]** - Entrez un nom pour votre définition d’informations d’identification d’API.

   * **[!UICONTROL URL de base de l’API]** et **[!UICONTROL clé de l’API]** - Accédez à la page d’accueil de votre interface web ou à la page de gestion des clés d’API de votre compte Infobip pour trouver vos informations d’identification.

   Pour plus d’informations sur la recherche de ces informations pour votre compte Infobip, consultez la [documentation Infobip](https://www.infobip.com/docs/api/_blank).

1. Cliquez sur **[!UICONTROL Submit]** en haut à droite de la page lorsque les détails de configuration de vos informations d’identification d’API sont terminés.

>[!ENDTABS]

Lorsque vous cliquez sur _[!UICONTROL Submit]_, les informations d’identification sont immédiatement validées et enregistrées, vous redirigeant vers la page de liste __ des informations d’identification de l’API. Si les informations d’identification envoyées ne sont pas valides, le système affiche un message d’erreur sur la page de liste. Dans ce cas, vous pouvez choisir d’annuler la configuration ou de la mettre à jour et de l’envoyer à nouveau.

## Ajout d’une action SMS dans un parcours de compte

Vous pouvez configurer des diffusions de messages texte dans un Parcours de compte lorsque vous ajoutez un noeud _[!UICONTROL Take an action]_ et procédez comme suit :

1. Pour la cible _[!UICONTROL Action sur]_, choisissez **[!UICONTROL Personnes]**.

1. Pour l’ _[!UICONTROL action sur les personnes]_, choisissez **[!UICONTROL Envoyer un SMS]**.

   ![Agir - envoyer sms](assets/journey-node-send-sms.png){width="800" zoomable="yes"}

1. Au bas du panneau _[!UICONTROL Agir sur une action]_, cliquez sur **[!UICONTROL Créer un SMS]**.

1. Dans la boîte de dialogue, saisissez un **[!UICONTROL nom]** unique pour l’email et une **[!UICONTROL ligne Objet]**.

   ![Créer une boîte de dialogue SMS](assets/create-new-sms.png){width="500"}

## Créer le SMS

>[!IMPORTANT]
>
>**Gestion du consentement SMS**<br/>
><br/>
>Conformément aux normes et réglementations du secteur, tous les messages de marketing SMS doivent contenir un moyen pour que les destinataires puissent se désabonner facilement. Pour ce faire, les destinataires SMS peuvent répondre avec des mots-clés d&#39;opt-in et d&#39;opt-out. Tous les mots-clés d’opt-in et d’opt-out standard sont pris en charge et respectés. En outre, tous les mots-clés personnalisés configurés pour votre compte de fournisseur de services SMS sont pris en charge et honorés.

1. Saisissez le texte que vous souhaitez envoyer dans le champ **[!UICONTROL Message]** .

   Vous pouvez créer un message de 1 600 caractères maximum, pour chaque 160 caractères considérés comme un SMS unique.

1. **Personnalisez le message texte**.

   À tout moment lors de la création du message texte, cliquez sur l’icône _Personnaliser_ située à droite de la zone de message texte.

   ![Cliquez sur l&#39;icône Personnaliser pour ajouter des jetons au message](./assets/sms-message-personalize-icon.png){width="800" zoomable="yes"}

   La page affichée permet d’accéder à votre piste Adobe Marketo Engage et à vos jetons système. Les jetons standard et personnalisés sont inclus. Vous pouvez utiliser la barre de recherche pour localiser le jeton dont vous avez besoin ou parcourir l’arborescence de dossiers pour rechercher et sélectionner l’un des jetons de piste/système.

   Placez le curseur à l’emplacement du message où vous souhaitez ajouter le jeton. Ajoutez un jeton en cliquant sur le symbole plus ( **+** ) situé à côté. Si vous souhaitez ajouter le jeton avec une version de secours (valeur par défaut qui s’affiche si ce champ n’est pas disponible pour une piste), cliquez sur les points de suspension ( **...** ) et choisissez **[!UICONTROL Insérer avec le texte de remplacement]**.

   ![Cliquez sur les ellipses pour utiliser un secours pour le jeton](./assets/sms-message-personalize-ellipsis-fallback.png){width="700" zoomable="yes"}

   Dans la boîte de dialogue _[!UICONTROL Entrer la valeur de secours]_, saisissez le texte qui s’affiche comme valeur de secours, puis cliquez sur **[!UICONTROL Ajouter]**.

   ![Entrez le texte de remplacement du jeton](./assets/sms-message-personalize-fallback-text.png){width="400"}

   Lorsque vos jetons de personnalisation sont placés, cliquez sur **[!UICONTROL Enregistrer]** pour enregistrer les modifications et revenir à l’espace de travail principal de création de SMS. Vous pouvez continuer à éditer le message avec les jetons si nécessaire.

<!-- 1. **Add URLs to text message**.

   After defining your content, you can add URLs to your message by clicking the _Link_ icon.
   
   You can add two types of URLs: 

   External URLs - This is ANY external URL that can be directly typed into/ pasted into the input text box
   Adobe Marketo Engage Design Studio Landing Pages - Selecting this option, you will see a 'Landing Page picker' from which you can select any of the listed approved Landing Pages from Marketo Engage

   You can choose to 'shorten' either of these URLs by selecting the checkbox
   Note that the URL shortening function, uses the Marketo subdomain for shortening
   The shortened URL appears as a read-only field within the modal
   You can optionally track clicks on the URL
   You can also choose to include 'mkt_tok' for tracking activity against a user
   Click on Add to save changes & add the chosen URL to the SMS message
-->

## Définir les propriétés du SMS

1. Dans la section _[!UICONTROL Propriétés SMS]_ , saisissez un **[!UICONTROL Nom]** (obligatoire, 100 caractères maximum) et une **[!UICONTROL Description]** (facultatif, 300 caractères maximum) pour votre message.

   Les caractères Alpha, numériques et spéciaux sont autorisés pour ces champs. Les caractères réservés suivants sont **non autorisés** : `\`, `/`, `:`, `*`, `?`, `"`, `<`, `>` et `|`.

1. Sélectionnez le **[!UICONTROL Type de SMS]** :

   * Utilisez `Marketing` pour les messages promotionnels, qui requièrent le consentement de l’utilisateur.
   * Utilisez `Transactional` pour les messages non commerciaux, tels que la confirmation de commande, les notifications de réinitialisation de mot de passe ou les informations de diffusion.

1. Pour la **[!UICONTROL configuration SMS]**, sélectionnez l’une des configurations d’API prédéfinies.

   Ce paramètre détermine le fournisseur de services de passerelle SMS et le compte utilisés pour diffuser le message.

1. Saisissez le **[!UICONTROL numéro d&#39;expéditeur]** &#x200B; que vous souhaitez utiliser pour vos communications.

   ![Agir - envoyer sms](./assets/sms-properties.png){width="700" zoomable="yes"}

   Le numéro de destinataire est toujours mappé au champ `Lead.MainPhone` dans Marketo Engage.

<!-- ## Preview the text message content

When your message content is defined, you can use test profiles to preview its content. If you inserted personalized content, you can check how this content is displayed in the message, using test profile data.

1. Click **[!UICONTROL Simulate Content]** at the top of the SMS authoring workspace.

1. From the _[!UICONTROL Simulate Content]_ page, click **[!UICONTROL Add People]**.

1. Use the # page to manage the leads used for your test profile.

   In the displayed list, you can search for and add any of the leads (up to 10 leads at a time) from the Marketo Engage lead database.

   To search, enter the whole email address and click enter. The corresponding lead profile shows up for selection.

   The preview updated to the personalization fields for the selected profile.

   All the added leads appear on the left rail of the 'Simulate Content' page

   You can manage this list by adding more people and deleting individual leads from the profile listing (it does not remove them from the database).

1. Simulate content for a lead.

   Select any of the leads listed on the left rail of the Simulate Content page and the SMS preview on the page updates for the corresponding lead.

   You can also select a lead from the 'drop-down' box above the preview space and the SMS preview on the page updates for the corresponding lead

1. To exit the _[!UICONTROL Simulate Content]_ page and return back to the SMS authoring workspace, click Close. -->
