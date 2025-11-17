---
title: Configuration des SMS
description: Connectez les fournisseurs SMS tels que Sinch, Twilio et Infobip aux informations d’identification d’API pour activer la messagerie texte dans les parcours B2B edition Journey Optimizer.
feature: Setup, Channels
role: Admin
exl-id: bd41a5ec-929f-489f-a757-0720c1b44ed2
source-git-commit: 325ae8e8c1f3bbf25e0d96907ede6cb9f2e76e3d
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 6%

---

# Configuration des SMS

Adobe Journey Optimizer B2B edition envoie des SMS par l’intermédiaire de fournisseurs de services SMS (ou de fournisseurs de passerelles SMS). Avant de créer votre SMS, configurez votre fournisseur de services à partir des paramètres _Administrateur_.

## Fournisseurs de services de passerelle SMS

Adobe Journey Optimizer B2B edition s’intègre actuellement à des fournisseurs tiers qui offrent des services de messagerie texte de manière indépendante. Les fournisseurs pris en charge pour la messagerie texte sont Sinch, Twilio et Infobip.

Avant de configurer un canal SMS dans Adobe Journey Optimizer B2B edition, vous devez créer un compte auprès de l’un de ces fournisseurs afin d’obtenir votre jeton API et votre identifiant de service. Ces informations d’identification sont requises pour configurer la connexion entre Adobe Journey Optimizer B2B edition et le fournisseur approprié.

>[!IMPORTANT]
>
>Votre utilisation des services de messages texte sera soumise aux conditions générales supplémentaires de la part du fournisseur concerné. En tant que solutions tierces, Sinch, Twilio et Infobip sont disponibles pour les utilisateurs de Adobe Journey Optimizer B2B edition par le biais d’une intégration. Adobe ne contrôle pas et n’est pas responsable des produits tiers. Pour tout problème ou toute demande d’assistance liés aux services de messagerie texte (SMS), contactez votre fournisseur.

## Vérifier une configuration d’API SMS existante

>[!NOTE]
>
>Les paramètres décrits ne sont accessibles que par les utilisateurs disposant de privilèges d’administrateur SMS.

1. Dans le volet de navigation de gauche, développez la section **[!UICONTROL Administrateur]** et cliquez sur **[!UICONTROL Canaux]**.

   ![Accéder à la configuration des informations d’identification d’API SMS](./assets/config-sms-api.png){width="800" zoomable="yes"}

1. Dans le panneau de navigation, sélectionnez **[!UICONTROL Informations d’identification de l’API]**.

   La page répertorie les configurations d’API disponibles pour votre instance.

1. Si nécessaire, cliquez sur l’icône _Filtrer_ ( ![Afficher ou masquer l’icône des filtres](../assets/do-not-localize/icon-filter.svg) ) et sélectionnez des options pour afficher la liste des informations d’identification d’API configurées par le fournisseur ou le créateur de services SMS.

   ![Cliquez sur l’icône Filtrer pour affiner la liste des informations d’identification d’API](./assets/config-sms-api-filter.png){width="600" zoomable="yes"}

## Créer de nouvelles informations d’identification d’API pour un fournisseur de services SMS

>[!BEGINTABS]

>[!TAB  Sinch ]

_Pour configurer Sinch en tant que fournisseur SMS avec Adobe Journey Optimizer B2B edition :_

1. Dans le volet de navigation de gauche, développez la section **[!UICONTROL Administrateur]**, puis cliquez sur **[!UICONTROL Configuration]**.

1. Cliquez sur le **[!UICONTROL Créer des informations d’identification d’API]** en haut à droite de la liste _[!UICONTROL Informations d’identification d’API]_.

1. Configurez vos informations dʼidentification pour lʼAPI SMS :

   ![Configurer les informations d’identification de l’API SMS Sinch](./assets/config-sms-api-sinch.png){width="500"}

   * **[!UICONTROL Fournisseur SMS]** - Choisissez `Sinch` comme fournisseur SMS.

   * **[!UICONTROL Nom]** - Saisissez un nom pour vos informations d’identification API.

   * **[!UICONTROL ID de service]** et **[!UICONTROL Jeton API]** - Accédez à la page des API à partir de votre compte Sinch (vos informations d’identification se trouvent sous l’onglet SMS).

   Pour plus d’informations sur la recherche de ces informations pour votre compte Sinch, consultez la [documentation Sinch destinée aux développeurs](https://developers.sinch.com/docs/sms/getting-started)

1. Cliquez sur **[!UICONTROL Envoyer]** lorsque les détails de configuration de vos informations d’identification API sont terminés.

>[!TAB  Twilio ]

_Pour configurer Twilio en tant que fournisseur SMS avec Adobe Journey Optimizer B2B edition :_

1. Dans le volet de navigation de gauche, développez la section **[!UICONTROL Administrateur]**, puis cliquez sur **[!UICONTROL Configuration]**.

1. Cliquez sur le **[!UICONTROL Créer des informations d’identification d’API]** en haut à droite de la liste _[!UICONTROL Informations d’identification d’API]_.

1. Configurez vos informations dʼidentification pour lʼAPI SMS :

   ![Configurer les informations d’identification de l’API SMS Twilio](./assets/config-sms-api-twilio.png){width="500"}

   * **[!UICONTROL Fournisseur SMS]** - Choisissez `Twilio` comme fournisseur SMS.

   * **[!UICONTROL Nom]** - Saisissez un nom pour votre définition d’informations d’identification API.

   * **[!UICONTROL SID du compte]** et **[!UICONTROL Jeton d’authentification]** - Accédez au volet _Informations du compte_ de la page Tableau de bord de la console Twilio pour trouver vos informations d’identification.

   Pour plus d’informations sur la recherche de ces informations pour votre compte Twilio, consultez le [Centre d’aide Twilio](https://help.twilio.com/articles/14726256820123-What-is-a-Twilio-Account-SID-and-where-can-I-find-it-).

1. Cliquez sur **[!UICONTROL Envoyer]** en haut à droite de la page lorsque les détails de configuration de vos informations d’identification API sont terminés.

>[!TAB  Infobip ]

_Pour configurer Infobip en tant que fournisseur SMS avec Adobe Journey Optimizer B2B edition :_

1. Dans le volet de navigation de gauche, développez la section **[!UICONTROL Administrateur]**, puis cliquez sur **[!UICONTROL Configuration]**.

1. Cliquez sur le **[!UICONTROL Créer des informations d’identification d’API]** en haut à droite de la liste _[!UICONTROL Informations d’identification d’API]_.

1. Configurez vos informations dʼidentification pour lʼAPI SMS :

   ![Configurer les informations d’identification de l’API SMS Infobip](./assets/config-sms-api-infobip.png){width="500"}

   * **[!UICONTROL Fournisseur SMS]** - Choisissez `Infobip` comme fournisseur SMS.

   * **[!UICONTROL Nom]** - Saisissez un nom pour votre définition d’informations d’identification API.

   * **[!UICONTROL URL de base de l’API]** et **[!UICONTROL clé API]** - Accédez à la page d’accueil de votre interface web ou à la page de gestion des clés API pour que votre compte Infobip puisse trouver vos informations d’identification.

   Pour plus d’informations sur la recherche de ces informations pour votre compte Infobip, consultez la [documentation Infobip](https://www.infobip.com/docs/api/_blank).

1. Cliquez sur **[!UICONTROL Envoyer]** en haut à droite de la page lorsque les détails de configuration de vos informations d’identification API sont terminés.

>[!ENDTABS]

Lorsque vous cliquez sur _[!UICONTROL Envoyer]_, les informations d’identification sont immédiatement validées et enregistrées, vous redirigeant vers la page de liste _[!UICONTROL Informations d’identification de l’API]_. Si les informations d’identification envoyées ne sont pas valides, le système affiche un message d’erreur sur la page de liste. Dans ce cas, vous pouvez choisir d’annuler la configuration ou de la mettre à jour et de l’envoyer à nouveau.
