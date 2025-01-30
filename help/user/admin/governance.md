---
title: Fonctionnalités de gouvernance
description: Découvrez les fonctionnalités de gouvernance actuellement disponibles dans Journey Optimizer B2B edition.
exl-id: 2845272b-987c-4a37-adf4-6ee5bfd59fc0
source-git-commit: 3198ba223125c95263d8dcf5ee8cb285a888a26a
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 2%

---

# Fonctionnalités de gouvernance

Journey Optimizer B2B edition est une application Adobe Experience Platform intégrée. Il utilise plusieurs outils et services qui permettent de contrôler vos données d’expérience collectées conformément à vos pratiques commerciales, à vos obligations légales et à vos processus de développement. Les sections ci-dessous résument chacune de ces fonctionnalités de gouvernance.

## Confidentialité - RGPD

Journey Optimizer B2B edition utilise les fonctionnalités de gouvernance existantes pour le RGPD de Marketo Engage fournies par Privacy Service et le service Marketo Privacy Broker.

## Contrôle d’accès en fonction du rôle (RBAC)

Avec Journey Optimizer B2B edition et l’accès au Adobe Admin Console, les administrateurs peuvent accorder à un utilisateur des autorisations sur un type d’entité (affichage-segments, gestion-segments, gestion-parcours, etc.). Cette fonctionnalité fait partie de la structure des autorisations unifiées (UPF) qui permet à tous les clients Adobe Experience Platform de définir et de gérer des rôles et des autorisations pour leur organisation.

## Chiffrement des données

**_Chiffrement des données inactives_** - Toutes les données des profils de comptes et de personnes transférées de Adobe Experience Platform vers Journey Optimizer B2B edition sont chiffrées afin de garantir la conformité actuelle des Experience Platform. Toutes les entités provenant de Journey Optimizer B2B edition, telles que les parcours et les groupes d’achats, sont également chiffrées.

**_Chiffrement des données en transit_** (sur un réseau public) : toutes les API et entités Journey Optimizer B2B edition sont chiffrées en transit à l’aide de TLS 1.2.

## Souscription au consentement/désinscription

L’opt-in/opt-out du consentement est une forme de gouvernance où un profil peut se désinscrire d’un canal de communication, tel que les e-mails ou les SMS, et un profil est ensuite exclu du canal de communication.

Avec Journey Optimizer B2B edition, vous pouvez créer et gérer des cas d’utilisation d’abonnement/de désabonnement pour vos cas d’utilisation de diffusion par e-mail et SMS. Ces préférences de consentement sont stockées dans le groupe de champs de consentement du profil XDM. Elles sont synchronisées dans et hors de Journey Optimizer B2B edition dans le cadre du framework de synchronisation des données. Ces préférences sont utilisées au moment de la diffusion pour exclure les profils exclus des diffusions.

## Réinitialisation du sandbox

La réinitialisation du sandbox n’est **actuellement pas prise en charge** pour Adobe Journey Optimizer B2B edition. La réinitialisation ou la suppression d’un sandbox mappé à Journey Optimizer B2B edition peut entraîner une perte permanente de données dans Journey Optimizer B2B edition et peut nécessiter la mise en service d’une nouvelle instance Journey Optimizer B2B edition.

## Pas encore disponible

Les fonctionnalités de gouvernance suivantes ne sont pas encore disponibles :

* Application des libellés d’utilisation des données (DULE) / politiques d’utilisation
* Hygiène des données
* Politiques de consentement
* Contrôle d’accès au niveau du champ (FLAC)
* Contrôle d’accès au niveau de l’objet (OLAC)
* Chiffrement CMK des données inactives
* Service d’audits de plateforme
