---
title: Paramétrages des SMS
description: Découvrez comment configurer des connexions à des fournisseurs SMS pris en charge pour une utilisation par la messagerie SMS Journey Optimizer B2B edition.
feature: Setup
source-git-commit: c3352db2235af08e31ba7e4d8690bc9e330dd41f
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 6%

---

# Paramétrages des SMS

Adobe Journey Optimizer B2B edition envoie des SMS par le biais des fournisseurs de services SMS (ou fournisseurs de passerelle SMS). Avant de créer votre SMS, configurez votre fournisseur de services à partir des paramètres _Administrator_.

## Fournisseurs de services de passerelle SMS

Adobe Journey Optimizer B2B edition s’intègre actuellement à des fournisseurs tiers qui offrent des services de messagerie texte indépendamment. Les fournisseurs pris en charge pour la messagerie texte sont Sinch, Twilio et Infobip.

Avant de configurer un canal SMS dans Adobe Journey Optimizer B2B edition, vous devez créer un compte auprès de l’un de ces fournisseurs pour obtenir votre jeton API et votre ID de service. Ces informations d’identification sont requises pour configurer la connexion entre Adobe Journey Optimizer B2B edition et le fournisseur concerné.

>[!IMPORTANT]
>
>Votre utilisation des services de messages texte sera soumise aux conditions générales supplémentaires de la part du fournisseur concerné. En tant que solutions tierces, Sinch, Twilio et Infobip sont disponibles pour les utilisateurs de Adobe Journey Optimizer B2B edition par le biais d’une intégration. Adobe ne contrôle pas et n’est pas responsable des produits tiers. Pour tout problème ou toute demande d&#39;assistance relative aux services de messagerie texte (SMS), contactez votre fournisseur.

## Vérification d’une configuration d’API SMS existante

>[!NOTE]
>
>Les paramètres décrits sont accessibles uniquement aux utilisateurs disposant de droits d’administrateur SMS.

1. Dans le volet de navigation de gauche, développez la section **[!UICONTROL Administrator]** et cliquez sur **[!UICONTROL Channels]** (Canaux).

   ![Accéder à la configuration des informations d’identification de l’API SMS](./assets/config-sms-api.png){width="800" zoomable="yes"}

1. Dans le panneau de navigation, sélectionnez **[!UICONTROL Informations d’identification de l’API]**.

   La page répertorie les configurations d’API disponibles pour votre instance.

1. Si nécessaire, cliquez sur l&#39;icône _Filtrer_ ( ![Icône Afficher ou masquer les filtres](../assets/do-not-localize/icon-filter.svg) ) et sélectionnez des options pour afficher la liste des informations d&#39;identification d&#39;API configurées par le fournisseur de services SMS ou le créateur.

   ![Cliquez sur l’icône Filtrer pour affiner la liste des informations d’identification de l’API](./assets/config-sms-api-filter.png){width="600" zoomable="yes"}

## Création d’informations d’identification API pour un fournisseur de service SMS

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

_Pour configurer Twilio en tant que fournisseur de SMS avec Adobe Journey Optimizer B2B edition :_

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
