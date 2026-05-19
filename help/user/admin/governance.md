---
title: Fonctionnalités de gouvernance
description: Découvrez les fonctionnalités de gouvernance actuellement disponibles dans Journey Optimizer B2B edition.
feature: Setup
role: Admin
exl-id: 2845272b-987c-4a37-adf4-6ee5bfd59fc0
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: d6e625c1-468f-4d73-9f32-fd1edb87f96bid: f2da1b69-6919-4386-a5d2-9c7b5c9033db
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
autotag-review: 2026-03-27T23:18:44.352Z
TQID: https://experienceleague.adobe.com/PwH34suDPc84nB9eiAWtrkVzsOw82RRGw4hrRogf9zE
source-git-commit: 94a8ed9584459cf85a72448cd698740ef450ddb2
workflow-type: tm+mt
source-wordcount: 418
ht-degree: 3%

---

# Fonctionnalités de gouvernance

Journey Optimizer B2B edition est une application Adobe Experience Platform intégrée. Il utilise plusieurs outils et services qui permettent de contrôler vos données d’expérience collectées conformément à vos pratiques commerciales, à vos obligations légales et à vos processus de développement. Les sections ci-dessous résument chacune de ces fonctionnalités de gouvernance.

## Confidentialité - RGPD

Journey Optimizer B2B edition utilise les fonctionnalités de gouvernance existantes du RGPD de Marketo Engage fournies par Privacy Service et le service Marketo Privacy Broker.

## Contrôle d’accès en fonction du rôle (RBAC)

Avec Journey Optimizer B2B edition et l’accès au Adobe Admin Console, les administrateurs peuvent accorder à un utilisateur des autorisations sur un type d’entité (affichage-segments, gestion-segments, gestion-parcours, etc.). Cette fonctionnalité fait partie de la structure des autorisations unifiées (UPF) qui permet à tous les clients Adobe Experience Platform de définir et de gérer des rôles et des autorisations pour leur organisation.

## Chiffrement des données

**_Chiffrement des données au repos_** - Toutes les données de profil de compte et de personne transférées de Adobe Experience Platform vers Journey Optimizer B2B edition sont chiffrées afin de garantir la conformité existante d’Experience Platform. Toutes les entités provenant de Journey Optimizer B2B edition, telles que les parcours et les groupes d’achats, sont également chiffrées.

**_Chiffrement des données en transit_** (sur un réseau public) : toutes les API et entités Journey Optimizer B2B edition sont chiffrées en transit à l’aide de TLS 1.2.

## Souscription au consentement/désinscription

Journey Optimizer B2B edition lit les préférences de consentement par personne stockées dans les profils XDM Adobe Experience Platform et les applique au moment de la diffusion des messages pour les canaux e-mail, SMS et WhatsApp. Les personnes qui se sont exclues d’un canal sont exclues de la diffusion avant l’envoi du contenu depuis le canal ou le fournisseur de messagerie en aval.

Le consentement est évalué au moment de la diffusion à l’aide des champs XDM du groupe de champs de consentement du profil. Le comportement de consentement par défaut diffère selon le canal : l’e-mail est activé par défaut lorsqu’aucune préférence n’est définie, tandis que les SMS et WhatsApp sont désactivés par défaut.

Pour plus d’informations sur les attributs XDM évalués pour chaque canal et leurs comportements par défaut, voir [Préférences de consentement](../content/channels-consent-preferences.md).

## Réinitialisation du sandbox

La réinitialisation du sandbox n’est **actuellement pas prise en charge** pour Adobe Journey Optimizer B2B edition. La réinitialisation ou la suppression d’un sandbox mappé à Journey Optimizer B2B edition peut entraîner une perte de données permanente et nécessiter la mise en service d’une nouvelle instance.

## Pas encore disponible

Les fonctionnalités de gouvernance suivantes ne sont pas encore disponibles :

* Application des libellés d’utilisation des données (DULE) / politiques d’utilisation
* Hygiène des données
* Politiques de consentement
* Contrôle d’accès au niveau du champ (FLAC)
* Contrôle d’accès au niveau de l’objet (OLAC)
* Chiffrement CMK des données inactives
* Service d’audits de plateforme
