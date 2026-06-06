---
title: Vue d’ensemble d’Adobe Journey Optimizer B2B Edition
description: 'Découvrez Adobe Journey Optimizer B2B Edition : orchestrez des parcours de compte avec des groupes d’achat, des informations basées sur l’IA et l’intégration d’Experience Platform pour le marketing B2B.'
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
autotag-review: 2026-04-29T23:21:13.339Z
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: f467931a-9b22-4ca8-869f-adfbd64061ce
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
TQID: https://experienceleague.adobe.com/L58cK4MP-S-8U9fFiXU2qZn4HCieNzjoOaSRCLkyanI
source-git-commit: ca0c6b10cf6a979249901d514116f373014544ad
workflow-type: tm+mt
source-wordcount: 803
ht-degree: 66%

---

# Vue d’ensemble d’Adobe Journey Optimizer B2B Edition

Avec Adobe Journey Optimizer B2B Edition, vous pouvez orchestrer des parcours de compte et de groupe d’achat à l’aide d’une IA générative intégrée et d’une automatisation de pointe afin d’optimiser la demande pour des offres spécifiques à l’aide de groupes d’achats qualifiés pour le marketing.

## Parcours de compte avec groupes d’achat

Lorsque vous comparez les parcours de compte aux fonctionnalités de parcours de Marketo Engage et Adobe Journey Optimizer standard, la distinction essentielle est que les parcours de compte déplacent les comptes à travers le parcours, et non les personnes. Une personne associée à un compte a généralement une progression non linéaire qui repose sur la progression du compte dans le parcours, et non sur ses actions individuelles. Par exemple, lorsqu’un compte en est à une phase précoce du parcours d’achat, les informations envoyées concernent généralement les fonctionnalités générales de la solution. Plus loin dans le processus d’achat, le contenu est davantage ciblé sur des offres particulières ou d’autres articles visant à conclure une vente. Une fois la solution achetée, les informations sont de nouveau modifiées afin de fournir des guides pratiques, des bonnes pratiques ou des informations sur les événements à venir, ou encore du contenu sur d’autres upsells. Même si une personne n’a pas interagi avec le contenu de la phase initiale, vous pouvez la faire passer à la phase actuelle en fonction des actions des autres personnes de leur compte ou de leur groupe d’achat.

## Architecture détaillée

Adobe Journey Optimizer B2B Edition utilise les _Audiences de comptes_ et les _Audiences de personnes_ d’Adobe Experience Platform pour alimenter un parcours de compte qui s’exécute dans Marketo Engage. Experience Platform est toujours la source principale de ces données, mais toute l’exécution et le traitement du parcours de compte se font dans l’infrastructure marketing B2B de Marketo Engage. L’orchestration renvoie les données à Experience Platform en temps quasi réel grâce au connecteur source Marketo Engage - Adobe Real-Time CDP B2B Edition, qui diffuse les modifications de données de Marketo Engage vers Experience Platform.

![Architecture de données détaillée](./assets/high-level-data-architecture.png){width="500" zoomable="yes"}

>[!NOTE]
>
>Vérifiez vos droits de licence et la [description du produit](https://helpx.adobe.com/fr/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} correspondante à propos des mécanismes de sécurisation des performances et des limitations statiques.

### Modèle d’abonnement

Une paire de sandbox Experience Platform (AEP) avec un abonnement Marketo Engage _Munchkin_ définit un abonnement à Journey Optimizer B2B edition. Un abonnement Marketo Engage unique ne peut pas être associé à plusieurs sandbox AEP. Si vous ne choisissez pas d’associer un abonnement Marketo Engage existant à Journey Optimizer B2B Edition, vous recevez un nouvel abonnement Marketo Engage vide à utiliser avec Journey Optimizer B2B Edition.

Experience Platform fournit une vue unifiée des données issues des instances Marketo Engage et des systèmes CRM associés afin d’agir sur ces données à l’aide d’un parcours de compte.

### Opérations de parcours de compte

Les parcours de compte sont créés dans Journey Optimizer B2B Edition et stockés dans l’instance Marketo Engage associée à l’abonnement. Bien qu’ils soient stockés dans le magasin de données Marketo Engage, ils ne sont pas visibles à partir de l’interface utilisateur de Marketo Engage et ne sont utilisables que dans Journey Optimizer B2B edition.

Un parcours de compte commence toujours par la sélection d’un segment de compte à utiliser comme audience de compte pour le parcours. La sélection de l’audience utilise le composant standard de sélecteur d’audience Experience Platform. Les spécialistes marketing peuvent ensuite implémenter le parcours de compte en divisant les chemins du parcours en fonction de leurs propres critères, qui peuvent inclure des critères de compte, de personne ou de groupe d’achat. Sur chaque branche, des actions peuvent être entreprises pour implémenter le parcours, telles que l’envoi d’un e-mail ou l’attente d’un événement.

Une fois le parcours de compte créé, il doit être publié. Lors de la publication, le parcours de compte est validé et converti en une série de campagnes Marketo Engage qui implémentent l’expérience du parcours. Les services d’intégration de données sont contactés pour démarrer le flux de données qui, à son tour, lance les opérations de parcours de compte. La première étape consiste à créer les segments pour les personnes du compte.

### Flux de données

Journey Optimizer B2B Edition utilise la segmentation de compte Real-Time CDP pour définir et exécuter les segments de compte et les segments de personne de compte associés requis par parcours. Lors de l’exécution d’un parcours publié, les données sur les personnes et les comptes peuvent changer et les données sont collectées sur les personnes qui interagissent avec le parcours. Journey Optimizer B2B edition s’appuie sur le connecteur source Marketo Engage pour Real-Time CDP B2B edition pour transmettre les modifications de données au sandbox Experience Platform, qui est la source de données principale.  Ces données sont transmises à AEP en temps quasi réel.

Seuls les types de données existants pris en charge par le connecteur source Marketo Engage (comptes, personnes et opportunités) sont renvoyés dans Real-Time CDP. Cela signifie que les données du groupe d’achat ne sont pas transmises à AEP et résident plutôt dans l’instance Marketo Engage utilisée par l’abonnement Journey Optimizer B2B Edition.
