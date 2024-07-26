---
title: Présentation de Adobe Journey Optimizer B2B Edition
description: Découvrez les fonctionnalités clés, les cas d’utilisation et les architectures de l’édition B2B de Adobe Journey Optimizer.
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
source-git-commit: 164a038ecce64cbf113c50b9328f84a95aa7b201
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 0%

---

# Présentation de Adobe Journey Optimizer B2B Edition

Avec Adobe Journey Optimizer B2B Edition, vous pouvez orchestrer des parcours de compte et de groupe d’achat à l’aide d’une IA générée intégrée et d’une automatisation de pointe du secteur afin d’optimiser la demande pour des offres spécifiques à l’aide de groupes d’achats qualifiés pour le marketing.

## Parcours de compte avec des groupes d’achat

En comparant Adobe Journey Optimizer B2B Edition à Marketo Engage et Adobe Journey Optimizer standard, la principale différence réside dans le fait que les parcours de compte déplacent les comptes à travers le Parcours, et non les personnes. Une personne associée à un compte a très probablement une progression non linéaire, basée sur la progression du compte par le parcours, et non sur ses actions individuelles. Par exemple, lorsqu’un compte est dans une phase précoce du parcours d’achat, les informations envoyées peuvent concerner les fonctionnalités ou fonctionnalités générales de la solution. Plus loin dans le processus d’achat, le contenu peut devenir plus ciblé sur des offres particulières ou d’autres articles destinés à fermer une vente. Une fois la solution achetée, les informations peuvent à nouveau changer afin de fournir des guides pratiques, des bonnes pratiques ou des informations sur les événements à venir, ou du contenu sur des ventes supplémentaires. Même si une personne n’a pas interagi avec le contenu de la phase initiale, vous souhaitez tout de même passer à la phase actuelle, en vous basant non pas sur ses propres actions, mais sur les actions des autres personnes de son compte ou de son groupe d’achat.

## Architecture de haut niveau

L’édition B2B de Adobe Journey Optimizer utilise les _audiences du compte_ et les _audiences du compte_ de Adobe Experience Platform pour alimenter un parcours de compte, qui est exécuté dans Marketo Engage. L’Experience Platform est toujours la source de vérité pour ces données, mais l’exécution et le traitement du parcours de compte se produisent dans l’infrastructure marketing B2B du Marketo Engage. L’orchestration récupère les données en temps quasi réel dans l’Experience Platform par le connecteur source Marketo Engage existant - Adobe Real-Time CDP B2B Edition , qui diffuse les modifications des données de Marketo Engage vers Experience Platform.

![Architecture de données de haut niveau](./assets/high-level-data-architecture.png){width="500" zoomable="yes"}

### Modèle d’abonnement

Un abonnement à Journey Optimizer B2B Edition est défini par une paire d’environnements de test Experience Platform (AEP) avec un abonnement Marketo Engage _munchkin_. Il n’est pas possible qu’un seul abonnement de Marketo Engage soit associé à plusieurs environnements de test AEP. Si vous ne choisissez pas d’utiliser un abonnement de Marketo Engage existant avec Journey Optimizer Édition B2B ou si vous n’utilisez pas actuellement Marketo Engage, vous disposez d’un nouvel abonnement de Marketo Engage vide à utiliser avec Journey Optimizer Édition B2B.

Dans cette configuration, l’objectif de l’Experience Platform est de fournir une vue unifiée des données des instances de Marketo Engage (et des systèmes CRM associés), puis de pouvoir agir sur les données unifiées à l’aide d’un parcours de compte.

### Opérations de parcours de compte

Les parcours de compte sont créés dans Journey Optimizer B2B Edition et stockés dans l’instance de Marketo Engage associée à l’abonnement. Bien qu’il soit stocké dans l’entrepôt de données du Marketo Engage, il n’est pas visible à partir de l’interface utilisateur du Marketo Engage et il n’est utilisable que depuis l’édition B2B de Journey Optimizer.

Un parcours de compte commence toujours par la sélection d’un segment de compte à utiliser comme audience de compte pour le parcours. La sélection de l’audience utilise le composant de sélecteur d’audience Experience Platform standard. Les marketeurs peuvent ensuite implémenter le parcours de compte en fractionnant les chemins du parcours selon leurs propres critères, qui peuvent inclure des critères de compte, des critères de personnes ou des critères de groupe d’achat. Sur chaque branche, des actions peuvent être entreprises pour mettre en oeuvre le parcours, comme l’envoi d’un email ou l’attente d’un événement.

Une fois le parcours du compte créé, il doit être publié. Au moment de la publication, le parcours de compte est validé et converti en une série de campagnes de Marketo Engage qui mettent en oeuvre l’expérience de parcours. De plus, les services d’intégration de données sont contactés pour démarrer le flux de données qui, à son tour, lance les opérations de parcours de compte. La première étape consiste à créer les segments pour les personnes du compte.

### Flux de données

L’édition B2B de Journey Optimizer utilise la segmentation des comptes Real-Time CDP pour définir et exécuter des segments de compte et des segments de personnes de compte associés requis par parcours. Lorsqu’un parcours publié s’exécute, les données sur les personnes et les comptes peuvent changer, et les données sont collectées sur les personnes qui interagissent avec le parcours. Journey Optimizer B2B Edition s’appuie sur le connecteur source du Marketo Engage pour Real-Time CDP B2B Edition pour que les modifications de données reviennent à l’environnement de test de l’Experience Platform, qui est la source de vérité.  Ces données sont diffusées à AEP en temps quasi réel.

Seuls les types de données existants pris en charge par le connecteur source du Marketo Engage (comptes, personnes et opportunités) reviennent dans Real-Time CDP. Cela signifie que l’achat de données de groupe n’est pas transmis à AEP et réside à la place dans l’instance de Marketo Engage utilisée par l’abonnement Journey Optimizer B2B Edition.
