---
title: Prise en main de Journey Optimizer B2B edition
description: En tant que nouvel utilisateur ou nouvelle utilisatrice de l’édition B2B d’Adobe Journey Optimizer, découvrez les principaux domaines pour bien commencer.
exl-id: 83f8e666-0b31-4323-9902-4fdf4446424c
source-git-commit: b403ff764c002796953956379e33fec6eb8c0611
workflow-type: tm+mt
source-wordcount: '664'
ht-degree: 10%

---

# Prise en main de Journey Optimizer B2B edition

Les fonctionnalités et outils que vous souhaitez aborder dans Adobe Journey Optimizer B2B edition dépendent de votre rôle au sein de votre équipe.

Selon votre organisation, les administrateurs peuvent définir plusieurs types d’utilisateurs et leur accorder l’accès à certaines fonctionnalités en fonction de leurs autorisations.

>[!TIP]
>
>Vérifiez également vos droits de licence et la [description du produit](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} correspondante à propos des mécanismes de sécurisation des performances et des limitations statiques.

>[!BEGINTABS]

>[!TAB Démarrage rapide administrateur]

Avant que votre équipe puisse commencer à utiliser les fonctionnalités de Adobe Journey Optimizer B2B edition, plusieurs étapes sont nécessaires pour préparer votre environnement. Effectuez les étapes suivantes afin que l’ingénieur de données et le marketeur puissent commencer à travailler avec Adobe Journey Optimizer B2B edition.

En tant qu’administrateur système, vous devez comprendre les profils de produit et attribuer des autorisations pour l’administration des sandbox et la configuration des canaux. Vous devez également configurer des sandbox et les gérer pour les profils de produit disponibles. Vous pouvez ensuite affecter des membres de l’équipe aux profils de produit. Ces fonctionnalités peuvent être gérées par les administrateurs de produit qui ont accès au Adobe Admin Console. [En savoir plus sur Adobe Admin Console](https://helpx.adobe.com/fr/enterprise/using/admin-console.html).

Découvrez la gestion des accès dans les pages suivantes :

1. **Créer des sandbox** pour partitionner vos instances en environnements virtuels distincts et isolés. [En savoir plus](https://experienceleague.adobe.com/en/docs/experience-platform/sandbox/home#understanding-sandboxes)

1. **Configurer le profil de produit**. Un profil de produit est un ensemble de droits unitaires dans Adobe Experience Platform qui permettent aux utilisateurs d&#39;accéder à certaines fonctionnalités ou à certains objets de l&#39;interface. [En savoir plus](../admin/user-management.md#create-the-marketo-engage-product-profile)

1. **Configurez des autorisations utilisateur** pour les profils de produit, y compris les sandbox, et donnez l’accès aux membres de votre équipe en les affectant à différents profils de produit. Cette tâche est effectuée dans l&#39;Admin Console. [En savoir plus](../admin/user-management.md#create-a-user-group)

1. **Configurez la diffusion e-mail** dans Marketo Engage, ce qui permet à votre équipe d’envoyer du contenu d’e-mail à partir de parcours de compte. [En savoir plus](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps#ensure-email-deliverability)

1. **Configurer les services SMS**. Configurez l’un des fournisseurs de SMS tiers pris en charge qui offrent des services de messagerie texte indépendamment et configurez les informations d’identification de compte dans Adobe Journey Optimizer B2B edition. [En savoir plus](../admin/configure-channels-sms.md)

1. **Configurez et activez l’utilisation d’Adobe Experience Manager Assets** pour les équipes qui utilisent Assets as a Cloud Service pour la gestion centralisée des ressources numériques. [En savoir plus](../admin/configure-aem-repositories.md)

1. **Configurer des définitions d’événement d’expérience Adobe Experience Platform (AEP)** pour les équipes chargées de la création de parcours de compte qui écoutent les événements d’expérience AEP. [En savoir plus](../admin/configure-aep-events.md)

>[!TAB Démarrage rapide pour les professionnels du marketing]

En tant que spécialiste du marketing ou _praticien en Parcours de compte_, vous êtes responsable de la conception des parcours et de l’élaboration du contenu. Vous pouvez commencer à utiliser Adobe Journey Optimizer B2B edition une fois que l’administrateur système et l’ingénieur de données ont préparé votre environnement et vous ont accordé l’accès.

Reportez-vous aux sections suivantes pour configurer votre premier parcours, ajouter des ressources et envoyer du contenu :

1. **Ajouter des audiences de compte**. Journey Optimizer B2B edition vous permet de créer des audiences de compte par le biais de définitions de segment directement à partir de l’application et de les exploiter dans vos parcours de compte. [En savoir plus](../audiences/account-audience-overview.md)

1. **Créer des groupes d&#39;achats**. Définissez les composants clés permettant d’atteindre les buts et objectifs de votre entreprise, et créez des groupes d’achats qui identifient les membres de vos listes de comptes cibles. [En savoir plus](../buying-groups/buying-groups-overview.md)

1. **Créer et gérer des ressources**. Adobe Experience Manager Assets fournit un référentiel de ressources unique et centralisé que vous pouvez utiliser pour renseigner vos messages. [En savoir plus](../content/assets-overview.md)

1. **Ajouter des modèles d’e-mail personnalisés et dynamiques**. Tirez parti de la personnalisation et des fonctionnalités de contenu dynamique de Journey Optimizer B2B edition pour adapter votre message à votre audience. [En savoir plus](../content/email-templates.md)

1. **Concevoir des parcours de compte pour offrir des expériences contextuelles personnalisées**. Journey Optimizer B2B edition vous permet de créer des cas d’utilisation d’orchestration en temps réel avec des données contextuelles stockées dans des événements ou des sources de données. Concevez des scénarios avancés à plusieurs étapes, optimisés par les fonctionnalités suivantes :

   * Envoyez des diffusions unitaires en temps réel déclenchées lorsqu’un événement est reçu ou par lots à l’aide d’audiences Adobe Experience Platform.

   * Utilisez des données contextuelles issues d’événements, des informations de Adobe Experience Platform ou des données provenant de services d’API tiers.

   * Utilisez les actions de canal intégrées (e-mail et SMS) pour envoyer des messages conçus dans Journey Optimizer B2B edition.

   * Dans le concepteur de parcours, créez vos cas d’utilisation à plusieurs étapes, ajoutez des conditions et envoyez des messages personnalisés.

[En savoir plus](../journeys/journey-overview.md)

>[!ENDTABS]
