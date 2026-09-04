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
source-git-commit: 8d2fc3ebc7df1674ac9af441679228a9e19d8d5a
workflow-type: tm+mt
source-wordcount: 739
ht-degree: 15%

---

# Vue d’ensemble d’Adobe Journey Optimizer B2B Edition

Avec Adobe Journey Optimizer B2B edition, vous pouvez orchestrer des parcours de personnes et de comptes à l’aide de l’IA générative intégrée et de l’automatisation de pointe, afin de maximiser la demande pour des offres spécifiques à l’aide de groupes d’achats qualifiés pour le marketing.

## Parcours de compte avec groupes d’achat

Lorsque vous comparez les parcours de compte aux fonctionnalités de parcours de Marketo Engage et Adobe Journey Optimizer standard, la distinction essentielle est que les parcours de compte déplacent les comptes à travers le parcours, et non les personnes. Une personne associée à un compte a généralement une progression non linéaire qui repose sur la progression du compte dans le parcours, et non sur ses actions individuelles. Par exemple, lorsqu’un compte en est à une phase précoce du parcours d’achat, les informations envoyées concernent généralement les fonctionnalités générales de la solution. Plus loin dans le processus d’achat, le contenu est davantage ciblé sur des offres particulières ou d’autres articles visant à conclure une vente. Une fois la solution achetée, les informations sont de nouveau modifiées afin de fournir des guides pratiques, des bonnes pratiques, des informations sur les événements à venir ou du contenu sur d’autres ventes incitatives. Même si une personne n’a pas interagi avec le contenu de la phase initiale, vous pouvez la faire passer à la phase actuelle en fonction des actions des autres personnes de leur compte ou de leur groupe d’achat.

## Architecture détaillée

Adobe Journey Optimizer B2B edition repose sur Adobe Experience Platform, y compris Real-Time CDP B2B. Journey Optimizer B2B edition et Marketo Engage s’exécutent sur des systèmes distincts, chacun disposant de sa propre banque de données. Experience Platform est le magasin de données principal et la source faisant autorité pour les comptes, les personnes et les opportunités. Journey Optimizer B2B edition est propriétaire de vos parcours de compte, de vos groupes d’achat et de vos rôles de groupe d’achat.

Une instance Marketo Engage dédiée prend en charge chaque abonnement Journey Optimizer B2B edition. Cette instance ne stocke pas vos parcours de compte, audiences ou groupes d&#39;achats. Au lieu de cela, il fournit des droits et des services principaux, tels que la diffusion d’e-mail, la configuration de l’expéditeur et les domaines de marque.

Pour prendre en charge les actions de parcours, vous pouvez également connecter une ou plusieurs de vos instances Marketo Engage existantes, y compris votre instance de production. Les actions de parcours permettent aux spécialistes marketing de coordonner des parcours basés sur un compte dans Journey Optimizer B2B edition avec des campagnes basées sur des prospects dans Marketo Engage, comme l’ajout de personnes à une liste ou une campagne de demande. [En savoir plus sur la connexion des instances Marketo Engage](./admin/marketo-actions-connect.md).

![Architecture de données de haut niveau présentant Journey Optimizer B2B edition connecté à Adobe Experience Platform comme source de vérité pour les audiences de compte et de personnes, une instance Marketo Engage dédiée qui fournit des droits et des services principaux, ainsi qu’une instance Marketo Engage de production facultative utilisée pour exécuter des actions de parcours.](./assets/high-level-data-architecture.png){zoomable="yes"}

>[!NOTE]
>
>Vérifiez vos droits de licence et la [description du produit](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} correspondant pour connaître les mécanismes de sécurisation des performances et les limitations statiques.

### Modèle d’abonnement

Un sandbox Experience Platform associé à une instance Marketo Engage dédiée définit un abonnement Journey Optimizer B2B edition. Cette instance dédiée est distincte de votre instance Marketo Engage de production et existe pour prendre en charge les droits et les services principaux plutôt que pour stocker les données de parcours de compte. [En savoir plus sur la configuration](./setup-ultimate.md).

Experience Platform fournit une vue unifiée des données de vos instances Marketo Engage et systèmes CRM connectés. Utilisez ces données unifiées pour créer et exécuter vos parcours.

### opérations de parcours

Journey Optimizer B2B edition crée, stocke et exécute les parcours de votre compte. Les parcours de compte n’apparaissent pas dans Marketo Engage et ne sont utilisables que dans Journey Optimizer B2B edition.

Un parcours commence toujours par une audience qui qualifie des prospects ou des comptes et leurs personnes pour le parcours. Sélectionnez cette audience à l’aide du sélecteur d’audience Experience Platform standard. Les marketeurs implémentent le parcours en fractionnant les chemins à l’aide de critères de compte, de personnes ou de groupes d’achats. Sur chaque chemin, les actions envoient des communications ou attendent qu’un événement se produise.

Après avoir créé un parcours de compte, publiez-le pour activer le parcours. Les comptes admissibles intègrent un parcours publié dans les 24 heures.

### Flux de données

Journey Optimizer B2B edition fonctionne comme une destination Adobe Real-Time CDP B2B edition. Utilisez la segmentation de compte Real-Time CDP pour créer et évaluer les audiences de compte et les audiences de personnes qui qualifient des comptes et des personnes pour un parcours. Lorsque vous publiez un parcours, Journey Optimizer B2B edition active les audiences admissibles à partir d’Experience Platform.

Les groupes d’achats, les rôles des groupes d’achats et les scores des groupes d’achats sont créés et stockés dans Journey Optimizer B2B edition. [En savoir plus sur les groupes d&#39;achat](./buying-groups/buying-groups-overview.md).
