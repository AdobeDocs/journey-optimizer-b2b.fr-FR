---
title: Création de SMS
description: Découvrez comment envoyer des SMS à vos clients sur leurs appareils mobiles, ainsi que comment personnaliser et prévisualiser des messages au format texte à partir de l’éditeur de SMS.
feature: SMS Authoring, Content
exl-id: bd648253-74de-4083-a37a-ab7ceaea2746
source-git-commit: e38ec0f128e811fd4ac21c624d9018854b91c78b
workflow-type: tm+mt
source-wordcount: '2041'
ht-degree: 4%

---

# Création de SMS

Utilisez Adobe Journey Optimizer B2B edition pour envoyer des SMS à vos clients sur leurs appareils mobiles. Vous pouvez créer, personnaliser et prévisualiser des messages au format texte à partir de l’éditeur de SMS.

## Paramétrages des SMS

Adobe Journey Optimizer B2B edition envoie des SMS par le biais des fournisseurs de services SMS (ou fournisseurs de passerelle SMS). Avant de créer votre SMS, configurez votre fournisseur de services à partir des paramètres _Administrator_.

### Fournisseurs de services de passerelle SMS

Adobe Journey Optimizer version B2B s’intègre actuellement aux fournisseurs tiers qui offrent des services de messagerie texte de manière indépendante. Les fournisseurs pris en charge pour la messagerie texte sont Sinch, Twilio et Infobip.

Avant de configurer un canal SMS dans Adobe Journey Optimizer B2B Edition, vous devez créer un compte auprès de l’un de ces fournisseurs pour obtenir votre jeton API et votre ID de service. Ces informations d’identification sont requises pour configurer la connexion entre Adobe Journey Optimizer B2B Edition et le fournisseur concerné.

>[!IMPORTANT]
>
>Votre utilisation des services de messages texte sera soumise aux conditions générales supplémentaires de la part du fournisseur concerné. En tant que solutions tierces, Sinch, Twilio et Infobip sont disponibles pour les utilisateurs de Adobe Journey Optimizer B2B edition par le biais d’une intégration. Adobe ne contrôle pas et n’est pas responsable des produits tiers. Pour tout problème ou toute demande d&#39;assistance relative aux services de messagerie texte (SMS), contactez votre fournisseur.

### Vérification d’une configuration d’API SMS existante

>[!NOTE]
>
>Les paramètres décrits sont accessibles uniquement aux utilisateurs disposant de droits d’administrateur SMS.

1. Dans le volet de navigation de gauche, développez la section **[!UICONTROL Administrator]** et cliquez sur **[!UICONTROL Channels]** (Canaux).

   ![Accéder à la configuration des informations d’identification de l’API SMS](./assets/config-sms-api.png){width="800" zoomable="yes"}

1. Dans le panneau de navigation, sélectionnez **[!UICONTROL Informations d’identification de l’API]**.

   La page répertorie les configurations d’API disponibles pour votre instance.

1. Si nécessaire, cliquez sur l&#39;icône _Filtrer_ ( ![Icône Afficher ou masquer les filtres](../assets/do-not-localize/icon-filter.svg) ) et sélectionnez des options pour afficher la liste des informations d&#39;identification d&#39;API configurées par le fournisseur de services SMS ou le créateur.

   ![Cliquez sur l’icône Filtrer pour affiner la liste des informations d’identification de l’API](./assets/config-sms-api-filter.png){width="600" zoomable="yes"}

### Création d’informations d’identification API pour un fournisseur de service SMS

>[!BEGINTABS]

>[!TAB Sinch]

_Pour configurer Sinch en tant que fournisseur de SMS avec Adobe Journey Optimizer B2B edition :_

1. Dans le volet de navigation de gauche, développez la section **[!UICONTROL Administrator]** et cliquez sur **[!UICONTROL Configuration]**.

1. Cliquez sur le bouton **[!UICONTROL Créer de nouvelles informations d’identification d’API]** en haut à droite de la liste _[!UICONTROL informations d’identification d’API]_.

1. Configurez vos informations dʼidentification pour lʼAPI SMS :

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

1. Configurez vos informations dʼidentification pour lʼAPI SMS :

   ![Configuration des informations d’identification de l’API SMS Twilio](./assets/config-sms-api-twilio.png){width="500"}

   * **[!UICONTROL Fournisseur de SMS]** - Sélectionnez `Twilio` comme fournisseur de SMS.

   * **[!UICONTROL Nom]** - Entrez un nom pour votre définition d’informations d’identification d’API.

   * **[!UICONTROL Compte SID]** et **[!UICONTROL Jeton d’authentification]** - Accédez au volet _Informations sur le compte_ de votre page de tableau de bord de la console Twilio pour trouver vos informations d’identification.

   Pour plus d’informations sur la recherche de ces informations pour votre compte Twilio, consultez le [Centre d’aide de Twilio](https://help.twilio.com/articles/14726256820123-What-is-a-Twilio-Account-SID-and-where-can-I-find-it-).

1. Cliquez sur **[!UICONTROL Submit]** en haut à droite de la page lorsque les détails de configuration de vos informations d’identification d’API sont terminés.

>[!TAB Infobip]

_Pour configurer Infobip en tant que fournisseur de SMS avec Adobe Journey Optimizer B2B edition :_

1. Dans le volet de navigation de gauche, développez la section **[!UICONTROL Administrator]** et cliquez sur **[!UICONTROL Configuration]**.

1. Cliquez sur le bouton **[!UICONTROL Créer de nouvelles informations d’identification d’API]** en haut à droite de la liste _[!UICONTROL informations d’identification d’API]_.

1. Configurez vos informations dʼidentification pour lʼAPI SMS :

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

1. Dans la boîte de dialogue, saisissez un **[!UICONTROL Nom]** unique pour le message SMS.

   ![Créer une boîte de dialogue SMS](assets/create-new-sms.png){width="400"}

1. Cliquez sur **[!UICONTROL Créer]**.

   Le _concepteur de contenu de Parcours_ s’ouvre et vous pouvez créer le message et définir les propriétés SMS pour envoyer le message.

### Créer le SMS

>[!IMPORTANT]
>
>**Gestion du consentement SMS**<br/>
>
>Conformément aux normes et réglementations du secteur, tous les messages de marketing SMS doivent contenir un moyen pour que les destinataires puissent se désabonner facilement. Pour ce faire, les destinataires de SMS peuvent répondre avec des mots-clés d’accord préalable et de droit d’opposition. Tous les mots-clés d’opt-in et d’opt-out standard sont pris en charge et respectés. En outre, tous les mots-clés personnalisés configurés pour votre compte de fournisseur de services SMS sont pris en charge et honorés.

Saisissez le texte que vous souhaitez envoyer dans le champ **[!UICONTROL Message]** .

Vous pouvez créer un message de 1 600 caractères maximum, pour chaque 160 caractères considérés comme un SMS unique.

![Cliquez sur l&#39;icône Personnaliser pour ajouter des jetons au message](./assets/sms-message-compose.png){width="800" zoomable="yes"}

#### Personnaliser le message texte

1. À tout moment lors de la création du message texte, cliquez sur l’icône _Personnaliser_ ( ![Icône Personnaliser](../assets/do-not-localize/icon-personalize.svg) ) à droite de la zone de message texte.

   La page affichée permet d’accéder à votre piste Adobe Marketo Engage et à vos jetons système. Les jetons standard et personnalisés sont inclus. Vous pouvez utiliser la barre _Recherche_ pour localiser le jeton dont vous avez besoin, ou parcourir l’arborescence de dossiers pour rechercher et sélectionner l’un des jetons de piste/système.

1. Placez le curseur à l’emplacement du message où vous souhaitez ajouter le jeton.

1. Ajoutez un jeton en cliquant sur le symbole plus ( **+** ) situé à côté.

   Si vous souhaitez ajouter le jeton avec une version de secours (valeur par défaut qui s’affiche si ce champ n’est pas disponible pour une piste), cliquez sur l’icône _Plus_ ( **...** ) et sélectionnez **[!UICONTROL Insérer avec le texte de remplacement]**.

   ![Cliquez sur les ellipses pour utiliser un secours pour le jeton](./assets/sms-message-personalize-ellipsis-fallback.png){width="700" zoomable="yes"}

1. Dans la boîte de dialogue _[!UICONTROL Entrer la valeur de secours]_, saisissez le texte qui s’affiche comme valeur de secours, puis cliquez sur **[!UICONTROL Ajouter]**.

   ![Entrez le texte de remplacement du jeton](./assets/sms-message-personalize-fallback-text.png){width="400"}

1. Lorsque vos jetons de personnalisation sont placés, cliquez sur **[!UICONTROL Enregistrer]** pour enregistrer les modifications et revenir à l’espace de travail principal de création de SMS.

   Vous pouvez continuer à éditer le message avec les jetons si nécessaire.

#### Ajouter des liens (URL) au message texte

1. Après avoir saisi le texte de votre message, cliquez sur l’icône _Lien_ ( ![Icône Lien](../assets/do-not-localize/icon-link.svg) ) à droite de la zone de message texte.

1. Dans la boîte de dialogue, choisissez le type d’URL à lier :

   * **[!UICONTROL Landing Page]** - Sélectionnez cette option pour sélectionner l’une des pages d’entrée Adobe Marketo Engage Design Studio approuvées dans votre instance de Marketo Engage. Sélectionnez l&#39;espace de travail, puis la landing page.

   * **[!UICONTROL URL externe]** - Ce type est une URL externe que vous saisissez dans la zone de texte.

1. Si vous choisissez d&#39;utiliser une landing page, définissez les options de tracking.

   * **[!UICONTROL Activer le suivi]** - Cochez cette case pour activer le suivi, qui nécessite _le raccourcissement_ de l’URL. Pour une page d’entrée, il utilise le sous-domaine du Marketo Engage pour l’URL abrégée. Un exemple de format d’URL raccourci s’affiche. L&#39;URL réelle est créée lorsque le SMS est envoyé au destinataire.

   * **[!UICONTROL Include mkt_tok]** - Cochez cette case pour effectuer le suivi de l’activité par rapport à un utilisateur.

     >[!NOTE]
     >
     >Lorsque vous autorisez le suivi, mais désactivez _[!UICONTROL Include mkt_tok]_, l’URL de destination n’inclut pas le paramètre de chaîne de requête `mkt_tok` après la redirection. Ce paramètre est utilisé par les landing pages Marketo Engage et Munchkin pour garantir le suivi des activités des personnes (par exemple lorsqu’une personne se désabonne d’un email). Ne désactivez pas cette option à moins que le paramètre ne provoque des problèmes sur votre site web.<br/>
     >Pour plus d&#39;informations sur l&#39;utilisation des codes de suivi Munchkin sur votre site web, consultez la [documentation du Marketo Engage](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/add-munchkin-tracking-code-to-your-website){target="_blank"}.

   ![Boîte de dialogue Ajouter un lien pour SMS](./assets/sms-add-link-dialog.png){width="470"}

1. Une fois les options de lien terminées, cliquez sur **[!UICONTROL Ajouter]** pour enregistrer les modifications et ajouter le lien URL au message SMS.

### Définir les propriétés du SMS

1. Dans la section _[!UICONTROL Propriétés SMS]_ , saisissez un **[!UICONTROL Nom]** (obligatoire, 100 caractères maximum) et une **[!UICONTROL Description]** (facultatif, 300 caractères maximum) pour votre message.

   Les caractères Alpha, numériques et spéciaux sont autorisés pour ces champs. Les caractères réservés suivants sont **non autorisés** : `\`, `/`, `:`, `*`, `?`, `"`, `<`, `>` et `|`.

1. Sélectionnez le **[!UICONTROL Type de SMS]** :

   * Utilisez `Marketing` pour les messages promotionnels, qui requièrent le consentement de l’utilisateur.
   * Utilisez `Transactional` pour les messages non commerciaux, tels que la confirmation de commande, les notifications de réinitialisation de mot de passe ou les informations de diffusion.

1. Pour la **[!UICONTROL configuration SMS]**, sélectionnez l’une des configurations d’API prédéfinies.

   Ce paramètre détermine le fournisseur de services de passerelle SMS et le compte utilisés pour diffuser le message.

1. Saisissez le **[!UICONTROL numéro d&#39;expéditeur]** &#x200B; que vous souhaitez utiliser pour vos communications.

   ![Agir - envoyer sms](./assets/sms-properties.png){width="700" zoomable="yes"}

   Le numéro de destinataire est toujours mappé au champ `Lead.mobilePhone` dans Marketo Engage.

### Simuler le contenu du message texte {#preview-test}

>[!CONTEXTUALHELP]
>id="ajo-b2b_sms_preview_simulate"
>title="Vérifier le rendu de votre contenu"
>abstract="Une fois votre contenu défini, vous pouvez le prévisualiser et vérifier le rendu du canal que vous utilisez."

Lorsque le contenu de votre message est défini, vous pouvez utiliser des profils de test pour simuler (prévisualiser) son contenu. Si vous avez inséré du contenu personnalisé, vous pouvez vérifier l’affichage de ce contenu dans le message à l’aide des données de profil de test.

>[!IMPORTANT]
>
>Veillez à enregistrer votre SMS avant de procéder à la simulation du message texte.

1. Cliquez sur **[!UICONTROL Simuler le contenu]** en haut de l’espace de travail de création de SMS.

1. Sur la page _[!UICONTROL Simuler le contenu]_, cliquez sur **[!UICONTROL Ajouter des personnes]**.

1. Utilisez la page _Simuler le contenu_ pour gérer les pistes utilisées pour votre profil de test.

   Dans la liste affichée, vous pouvez rechercher et ajouter n’importe laquelle des pistes (jusqu’à 10 pistes à la fois) provenant de la base de données de pistes du Marketo Engage.

   Pour effectuer une recherche, saisissez l’adresse électronique complète et appuyez sur _Entrée_. Le profil de prospect correspondant s’affiche pour sélection.

   L&#39;aperçu met à jour les champs de personnalisation du profil sélectionné.

   Toutes les pistes ajoutées s’affichent à gauche.

   Vous pouvez gérer cette liste en ajoutant d’autres personnes et en supprimant des pistes individuelles de la liste des profils (elle ne les supprime pas de la base de données).

1. Simuler le contenu d’une piste sélectionnée.

   Sélectionnez l’une des pistes répertoriées à gauche. L’aperçu SMS sur la page met à jour la piste sélectionnée.

   Vous pouvez également sélectionner une piste à partir du sélecteur situé au-dessus de l&#39;espace de prévisualisation pour mettre à jour l&#39;aperçu SMS sur la page pour la piste correspondante.

1. Pour quitter la page _[!UICONTROL Simuler le contenu]_ et revenir à l’espace de travail de création de SMS, cliquez sur **[!UICONTROL Fermer]** en haut à droite.

## Gestion du consentement SMS

La possibilité de se désabonner des destinataires de recevoir des communications d’une marque et de respecter ce choix est une obligation légale. Le non-respect de ces réglementations entraîne des risques juridiques pour votre marque. Cette fonction permet également d&#39;éviter d&#39;envoyer des communications non sollicitées à vos destinataires, ce qui pourrait les faire marquer vos messages comme spam et nuire à votre réputation.

Lorsque vous fournissez cette option, les destinataires SMS peuvent répondre avec des mots-clés d&#39;opt-in et d&#39;opt-out. Tous les mots-clés d&#39;opt-in et d&#39;opt-out standard sont pris en charge et respectés, ainsi que tous les mots-clés personnalisés configurés sur le fournisseur de services SMS. Lors du désabonnement, les profils sont automatiquement supprimés de l’audience des futurs messages marketing.

Journey Optimizer B2B edition permet de gérer l’exclusion dans les SMS à l’aide de la logique suivante :

* Par défaut, si un prospect a choisi de ne pas recevoir de communications de votre part, le profil correspondant est exclu des prochaines diffusions SMS.

* Ce consentement de piste provenant de différentes sources (telles qu’AEP ou le fournisseur de services SMS) est synchronisé avec Journey Optimizer B2B edition. Actuellement, il ne prend en charge qu’un seul état de consentement par prospect au niveau de l’instance (un &quot;John Doe&quot; de prospect est abonné ou désabonné à tous les SMS promotionnels de l’instance). Actuellement, il ne prend pas en charge le double opt-in au niveau de la marque ou de la liste d’abonnements individuelle.
