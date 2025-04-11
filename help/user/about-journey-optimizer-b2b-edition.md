---
title: Présentation de Adobe Journey Optimizer B2B edition
description: Découvrez les fonctionnalités clés, les cas d’utilisation et les architectures de l’édition B2B d’Adobe Journey Optimizer.
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
source-git-commit: 5ca03b12fd459c64b245ad95e60a382c355922f9
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 5%

---

# Présentation de Adobe Journey Optimizer B2B edition

Avec Adobe Journey Optimizer, édition B2B, vous pouvez orchestrer des parcours de compte et de groupe d’achat à l’aide d’une IA générative intégrée et d’une automatisation de pointe afin d’optimiser la demande pour des offres spécifiques à l’aide de groupes d’achats qualifiés pour le marketing.

## Parcours de compte avec groupes d&#39;achat

En comparant Adobe Journey Optimizer B2B edition à Marketo Engage et Adobe Journey Optimizer standard, la distinction essentielle est que les parcours de compte déplacent les comptes à travers le Parcours, et non les personnes. Une personne associée à un compte a généralement une progression non linéaire qui repose sur la progression du compte par rapport au parcours, et non sur ses actions individuelles. Par exemple, lorsqu’un compte est dans une phase précoce du parcours d’achat, les informations envoyées peuvent concerner les fonctionnalités générales de la solution. Plus tard dans le processus d’achat, le contenu peut cibler davantage des offres particulières ou d’autres articles visant à conclure une vente. Une fois la solution achetée, les informations peuvent être modifiées à nouveau afin de fournir des guides pratiques, des bonnes pratiques ou des informations sur les événements à venir, ou encore du contenu sur d’autres upsells. Même si une personne n’a pas interagi avec le contenu de la phase initiale, vous souhaitez toujours la faire passer à la phase actuelle en fonction non pas de ses propres actions, mais des actions des autres personnes au sein de son compte ou de son groupe d’achat.

## Architecture de haut niveau

Adobe Journey Optimizer B2B edition utilise _Audiences de compte_ et _Audiences de personnes_ de Adobe Experience Platform pour alimenter un parcours de compte qui s’exécute dans Marketo Engage. Experience Platform est toujours la source de vérité pour ces données, mais toute l’exécution et le traitement du parcours de compte se font au sein de l’infrastructure marketing B2B de Marketo Engage. L’orchestration renvoie les données à Experience Platform en temps quasi réel grâce au connecteur source Marketo Engage - Adobe Real-Time CDP B2B edition, qui diffuse les modifications de données de Marketo Engage vers Experience Platform.

![Architecture de données de haut niveau](./assets/high-level-data-architecture.png){width=« 500 » zoomable=« yes »}

>[!NOTE]
>
>Vérifiez vos droits de licence et la [description du produit](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target=« _blank »} correspondante à propos des mécanismes de sécurisation des performances et des limitations statiques.

### Modèle d’abonnement

Un abonnement Journey Optimizer B2B edition est défini par une paire de sandbox Experience Platform (AEP) avec un abonnement Marketo Engage _Munchkin_. Un abonnement Marketo Engage unique ne peut pas être associé à plusieurs sandbox AEP. Si vous ne choisissez pas d’associer un abonnement Marketo Engage existant à Journey Optimizer B2B edition, vous recevez un nouvel abonnement Marketo Engage vide à utiliser avec Journey Optimizer B2B edition.

L’objectif d’Experience Platform dans cette configuration est de fournir une vue d’ensemble des données issues des instances Marketo Engage (et des systèmes CRM associés), puis de pouvoir agir sur ces données à l’aide d’un parcours de compte.

### Opérations de parcours de compte

Les parcours de compte sont créés dans Journey Optimizer B2B edition et stockés dans l’instance Marketo Engage associée à l’abonnement. Bien qu’il soit stocké dans le magasin de données Marketo Engage, il n’est pas visible à partir de l’interface utilisateur de Marketo Engage et il n’est jamais utilisable qu’à partir de Journey Optimizer B2B edition.

Un parcours de compte commence toujours par la sélection d’un segment de compte à utiliser comme audience de compte pour le parcours. La sélection de l’audience utilise le composant standard Sélecteur d’audience Experience Platform. Les marketeurs peuvent ensuite implémenter le parcours de compte en divisant les chemins d’accès du parcours en fonction de leurs propres critères, qui peuvent inclure des critères de compte, des critères de personne ou des critères de groupe d’achats. Sur chaque branche, des actions peuvent être entreprises pour implémenter le parcours, telles que l’envoi d’un e-mail ou l’attente d’un événement.

Une fois le parcours de compte créé, il doit être publié. Lors de la publication, le parcours de compte est validé et converti en une série de campagnes Marketo Engage qui mettent en œuvre l’expérience du parcours. Les services d’intégration de données sont contactés pour démarrer le flux de données qui, à son tour, lance les opérations de parcours de compte. La première étape consiste à créer les segments pour les Personnes du compte.

### Flux de données

Journey Optimizer B2B edition utilise la segmentation de compte Real-Time CDP pour définir et exécuter les segments de compte et les segments de personne-compte associés requis par parcours. Lors de l’exécution d’un parcours publié, les données sur les personnes et les comptes peuvent changer et les données sont collectées sur les personnes qui interagissent avec le parcours. Journey Optimizer B2B edition s’appuie sur le connecteur source Marketo Engage pour Real-Time CDP B2B edition pour transmettre les modifications de données au sandbox Experience Platform, qui est la source de vérité.  Ces données sont diffusées à AEP en temps quasi réel.

Seuls les types de données existants pris en charge par le connecteur source Marketo Engage (comptes, personnes et opportunités) reviennent dans Real-Time CDP. Cela signifie que les données du groupe d’achats ne sont pas transmises à AEP et résident plutôt dans l’instance Marketo Engage utilisée par l’abonnement Journey Optimizer B2B edition.
