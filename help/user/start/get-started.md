---
title: Prise en main de Journey Optimizer B2B edition
description: En tant que nouvel utilisateur ou nouvelle utilisatrice de l’édition B2B d’Adobe Journey Optimizer, découvrez les principaux domaines pour bien commencer.
exl-id: 83f8e666-0b31-4323-9902-4fdf4446424c
source-git-commit: c4df46db3c7123636311c47be36de171de24e1be
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 10%

---

# Prise en main de Journey Optimizer B2B edition

Les fonctionnalités et outils que vous souhaitez aborder dans Adobe Journey Optimizer B2B edition dépendent de votre rôle au sein de votre équipe.

En fonction de votre organisation, les administrateurs peuvent définir plusieurs types d’utilisateurs et leur accorder l’accès à certaines fonctionnalités en fonction de leurs autorisations.

>[!TIP]
>
>Vérifiez également vos droits de licence et la [description du produit](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} correspondante sur les barrières de performance et les limites statiques.

>[!BEGINTABS]

>[!TAB Démarrage rapide de l’administrateur]

Avant que votre équipe puisse commencer à utiliser les fonctionnalités de Adobe Journey Optimizer B2B edition, plusieurs étapes sont nécessaires pour préparer votre environnement. Procédez comme suit pour que l’ingénieur de données et le spécialiste du marketing puissent commencer à utiliser Adobe Journey Optimizer B2B edition.

En tant qu’administrateur système, vous devez comprendre les profils de produit et attribuer des autorisations pour l’administration des environnements de test et la configuration des canaux. Vous devez également configurer des environnements de test et les gérer pour les profils de produit disponibles. Vous pouvez ensuite affecter des membres de l’équipe aux profils de produit. Ces fonctionnalités peuvent être gérées par les administrateurs de produit qui ont accès à Adobe Admin Console. [En savoir plus sur Adobe Admin Console](https://helpx.adobe.com/fr/enterprise/using/admin-console.html).

Découvrez la gestion des accès dans les pages suivantes :

1. **Créer des sandbox** pour partitionner vos instances en environnements virtuels distincts et isolés. [En savoir plus](https://experienceleague.adobe.com/en/docs/experience-platform/sandbox/home#understanding-sandboxes)

1. **Configurez le profil de produit**. Un profil de produit est un ensemble de droits unitaires dans Adobe Experience Platform qui permet aux utilisateurs d’accéder à certaines fonctionnalités ou à certains objets dans l’interface. [En savoir plus](../admin/user-management.md#create-the-marketo-engage-product-profile)

1. **Configurez les autorisations d’utilisateur** pour les profils de produit, y compris les environnements de test, et donnez accès aux membres de votre équipe en les affectant à différents profils de produit. Cette tâche est effectuée dans l’Admin Console. [En savoir plus](../admin/user-management.md#create-a-user-group)

1. **Configurez la diffusion email** en Marketo Engage, ce qui permet à votre équipe d&#39;envoyer du contenu d&#39;email à partir des parcours du compte. [En savoir plus](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps#ensure-email-deliverability)

1. **Configurer les services SMS**. Configurez l’un des fournisseurs de SMS tiers pris en charge qui offre des services de messagerie texte indépendamment et configurez les informations d’identification du compte dans Adobe Journey Optimizer B2B edition. [En savoir plus](../admin/configure-channels-sms.md)

1. **Configurez et activez l’utilisation d’Adobe Experience Manager Assets** pour les équipes qui utilisent Assets as a Cloud Service pour la gestion centralisée des ressources numériques. [En savoir plus](../admin/configure-aem-repositories.md)

>[!TAB Démarrage rapide du marketeur]

En tant que spécialiste du marketing ou _praticien de Parcours de compte_, vous êtes responsable de la conception de parcours et de la conception de contenu. Vous pouvez commencer à utiliser Adobe Journey Optimizer B2B edition une fois que l’administrateur système et l’ingénieur des données ont préparé votre environnement et vous ont accordé l’accès.

Reportez-vous aux sections suivantes pour configurer votre premier parcours, ajouter des ressources et envoyer du contenu :

1. **Ajouter des audiences de compte**. Journey Optimizer B2B edition vous permet de créer des audiences de compte par le biais de définitions de segment directement à partir de l’application et de les exploiter dans vos parcours de compte. [En savoir plus](../audiences/account-audience-overview.md)

1. **Créez des groupes d’achat**. Définissez les composants clés permettant d’atteindre vos objectifs et objectifs professionnels, puis créez des groupes d’achat qui identifient les membres de vos listes de comptes cibles. [En savoir plus](../buying-groups/buying-groups-overview.md)

1. **Créer et gérer des ressources**. Adobe Experience Manager Assets fournit un référentiel unique et centralisé de ressources que vous pouvez utiliser pour remplir vos messages. [En savoir plus](../content/assets-overview.md)

1. **Ajoutez des modèles d&#39;email personnalisés et dynamiques**. Tirez parti des fonctionnalités de personnalisation et de contenu dynamique de Journey Optimizer B2B edition pour adapter votre message à votre audience. [En savoir plus](../content/email-templates.md)

1. **Concevez des parcours de compte pour offrir des expériences contextuelles personnalisées**. Journey Optimizer B2B edition vous permet de créer des cas d’utilisation d’orchestration en temps réel avec des données contextuelles stockées dans des événements ou des sources de données. Concevez des scénarios avancés à plusieurs étapes, optimisés par les fonctionnalités suivantes :

   * Envoyez une diffusion unitaire en temps réel déclenchée lors de la réception d’un événement ou par lots à l’aide des audiences Adobe Experience Platform.

   * Utilisez les données contextuelles issues d’événements, des informations provenant de Adobe Experience Platform ou des données issues de services d’API tiers.

   * Utilisez les actions de canal intégrées (email et SMS) pour envoyer des messages conçus dans Journey Optimizer B2B edition.

   * Dans le concepteur de parcours, créez vos cas d’utilisation à plusieurs étapes, ajoutez des conditions et envoyez des messages personnalisés.

[En savoir plus](../journeys/journey-overview.md)

>[!ENDTABS]
