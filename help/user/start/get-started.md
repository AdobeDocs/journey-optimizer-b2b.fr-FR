---
title: Conseils d’intégration pour les administrateurs et les spécialistes marketing
description: En tant que nouvel utilisateur, nouvelle utilisatrice, nouvel administrateur ou nouvelle administratrice de l’édition B2B d’Adobe Journey Optimizer, découvrez les principaux domaines pour bien commencer.
role: Admin, User
level: Beginner
exl-id: 83f8e666-0b31-4323-9902-4fdf4446424c
source-git-commit: 1e430af82b972dc73178161e64da10d1cdaaefaf
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 83%

---

# Conseils d’intégration

Les fonctionnalités et outils que vous souhaitez aborder dans Adobe Journey Optimizer B2B edition dépendent de votre rôle au sein de votre équipe. Selon votre organisation, les administrateurs et administratrices peuvent définir plusieurs types d’utilisateurs et d’utilisatrices, puis leur accorder l’accès à certaines fonctionnalités selon leurs autorisations.

>[!TIP]
>
>Vérifiez vos droits de licence et la [description du produit](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} correspondante à propos des mécanismes de sécurisation des performances et des limitations statiques.

>[!BEGINTABS]

>[!TAB Administrateur]

Avant que votre équipe puisse commencer à utiliser les fonctionnalités d’Adobe Journey Optimizer B2B Edition, plusieurs étapes sont nécessaires pour préparer votre environnement. Suivez les étapes ci-après afin que les responsables de l’ingénierie des données et du marketing puissent commencer à travailler avec Adobe Journey Optimizer B2B Edition.

En tant qu’administrateur ou administratrice système, vous devez comprendre les profils de produit et attribuer des autorisations pour l’administration des sandbox et la configuration des canaux. Vous devez également configurer des sandbox et les gérer pour les profils de produit disponibles. Vous pouvez ensuite affecter des membres de l’équipe aux profils de produit. Les administrateurs et administratrices produit ayant accès au Adobe Admin Console peuvent gérer ces fonctionnalités. [En savoir plus sur Adobe Admin Console](https://helpx.adobe.com/fr/enterprise/using/admin-console.html).

Découvrez la gestion des accès dans les pages suivantes :

1. **Créer des sandbox** pour partitionner vos instances en environnements virtuels distincts et isolés. [En savoir plus](https://experienceleague.adobe.com/fr/docs/experience-platform/sandbox/home#understanding-sandboxes){target="_blank"}

1. **Collaborez avec votre ingénieur de données** pour planifier et mettre en œuvre l’activation de votre audience B2B et de votre profil. Passez en revue les plans directeurs publiés et suivez les instructions en fonction de vos besoins. [En savoir plus](https://experienceleague.adobe.com/en/docs/blueprints-learn/architecture/b2b-activation/overview){target="_blank"}

1. **Planifiez et implémentez l’intégration de Marketo Engage** pour incorporer un schéma personnalisé, l’ingestion des profils et des comptes et l’orchestration des parcours personnalisés pour les groupes d’achats. [En savoir plus](https://experienceleague.adobe.com/en/docs/blueprints-learn/architecture/b2b-activation/b2b-journeys-with-marketo){target="_blank"}

1. **Configurez le profil de produit**. Un profil de produit est un ensemble de droits unitaires dans Adobe Experience Platform qui permettent d’accéder à certaines fonctionnalités ou à certains objets dans l’interface. [En savoir plus](../admin/user-management.md#create-the-marketo-engage-product-profile)

1. **Définissez les autorisations d’utilisation** pour les profils de produit, y compris les sandbox, et donnez l’accès aux membres de votre équipe en les affectant à différents profils de produit. Cette étape est effectuée dans l’Admin Console. [En savoir plus](../admin/user-management.md#create-a-user-group)

1. **Configurez la diffusion e-mail** dans Marketo Engage, ce qui permet à votre équipe d’envoyer du contenu d’e-mail à partir de parcours de compte. [En savoir plus](https://experienceleague.adobe.com/fr/docs/marketo/using/getting-started/initial-setup/setup-steps#ensure-email-deliverability){target="_blank"}

1. **Configurez les services SMS**. Configurez l’un des fournisseurs de SMS tiers pris en charge qui offrent des services de messagerie SMS indépendamment et configurez les informations d’identification de compte dans Adobe Journey Optimizer B2B Edition. [En savoir plus](../admin/configure-channels-sms.md)

1. **Configurez et activez l’utilisation d’Adobe Experience Manager Assets** pour les équipes qui utilisent Assets as a Cloud Service pour la gestion centralisée des ressources numériques. [En savoir plus](../admin/configure-aem-repositories.md)

1. **Configurez des définitions d’événement d’expérience Adobe Experience Platform (AEP)** pour les équipes chargées de la création de parcours de compte qui écoutent les événements d’expérience AEP. [En savoir plus](../admin/configure-aep-events.md)

>[!TAB Professionnel du marketing]

En tant que spécialiste du marketing ou _spécialiste en parcours de compte_, vous êtes responsable de la conception des parcours et de l’élaboration du contenu. Vous pouvez commencer à utiliser Adobe Journey Optimizer B2B Edition une fois que l’administration système et l’ingénierie des données ont préparé votre environnement et vous ont accordé l’accès.

Reportez-vous aux sections suivantes pour configurer votre premier parcours, ajouter des ressources et envoyer du contenu :

1. **Ajoutez des audiences de compte**. Journey Optimizer B2B Edition vous permet de créer des audiences de compte via les définitions de segments directement à partir de l’application, puis de les exploiter dans vos parcours de compte. [En savoir plus](../audiences/account-audience-overview.md)

1. **Créez des groupes d’achat**. Définissez les composants clés permettant d’atteindre les buts et objectifs de votre entreprise, puis créez des groupes d’achat qui identifient les membres de vos listes de comptes cibles. [En savoir plus](../buying-groups/buying-groups-overview.md)

1. **Créez et gérez des ressources**. Adobe Experience Manager Assets fournit un référentiel de ressources unique et centralisé que vous pouvez utiliser pour renseigner vos messages. [En savoir plus](../content/assets-overview.md)

1. **Ajoutez des modèles d’e-mail personnalisés et dynamiques**. Profitez des fonctionnalités de personnalisation et du contenu dynamique de Journey Optimizer B2B Edition pour adapter votre message à votre audience. [En savoir plus](../content/email-templates.md)

1. **Concevez des parcours de compte pour offrir des expériences contextuelles personnalisées**. Journey Optimizer B2B Edition vous permet de créer des cas d’utilisation d’orchestration en temps réel avec des données contextuelles stockées dans des événements ou des sources de données. Concevez des scénarios avancés à plusieurs étapes avec les fonctionnalités suivantes :

   * Envoyez des diffusions unitaires en temps réel déclenchées lors de la réception d’un événement ou par lots à l’aide d’audiences Adobe Experience Platform.

   * Tirez parti des données contextuelles issues des événements, des informations d’Adobe Experience Platform ou des données provenant de services d’API tiers.

   * Utilisez les actions de canal intégrées (e-mail et SMS) pour envoyer des messages conçus dans Journey Optimizer B2B Edition.

   * Dans la carte de parcours, créez vos cas d’utilisation à plusieurs étapes, ajoutez des conditions et envoyez des messages personnalisés.

[En savoir plus](../journeys/journey-overview.md)

>[!ENDTABS]
