---
title: Fonctionnalités de gouvernance
description: Découvrez les fonctionnalités de gouvernance actuellement disponibles dans Journey Optimizer B2B Edition.
source-git-commit: 1353defe804947617a4d7489592d380bf372c7df
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 1%

---

# Fonctionnalités de gouvernance

En tant qu’application Adobe Experience Platform intégrée, Journey Optimizer B2B Edition utilise plusieurs services et outils qui vous permettent de contrôler en toute confiance vos données d’expérience collectées afin de respecter vos pratiques commerciales, obligations légales et processus de développement. Les sections ci-dessous fournissent un résumé de chacune de ces fonctions de gouvernance.

## Confidentialité - RGPD

Journey Optimizer Édition B2B utilise les fonctionnalités de gouvernance du RGPD de Marketo Engage existantes fournies par Privacy Service et Marketo Privacy Broker Service.

## Contrôle d’accès en fonction du rôle (RBAC)

Avec Journey Optimizer Édition B2B et l’accès à Adobe Admin Console, les administrateurs peuvent accorder à un utilisateur des autorisations sur un type d’entité (segments d’affichage, segments de gestion, parcours de gestion, etc.). Cette fonctionnalité fait partie de l’Unified Permissions Framework (UPF) qui permet à tous les clients Adobe Experience Platform de définir et de gérer des rôles et des autorisations pour leur organisation.

## Cryptage des données

**_Chiffrement des données au repos_** - Toutes les données de comptes et de profils de personnes transférées de Adobe Experience Platform vers Journey Optimizer B2B Edition sont chiffrées afin de maintenir la conformité existante de l’Experience Platform. Toutes les entités provenant de Journey Optimizer B2B Edition, telles que les parcours et les groupes d’achat, sont également chiffrées.

**_Chiffrement des données en transit_** (sur un réseau public) - Toutes les API et entités de l’édition B2B de Journey Optimizer sont chiffrées en transit à l’aide de TLS 1.2.

## Accord préalable/accord préalable

L’opt-in/opt-out du consentement est une forme de gouvernance dans laquelle un profil peut se désinscrire d’un canal de communication, comme un email ou un SMS, et un profil doit ensuite être exclu de ce canal de communication.

Avec Journey Optimizer B2B Edition, vous pouvez créer et gérer des cas d’utilisation d’abonnement/désabonnement pour vos cas d’utilisation de diffusion email et SMS. Ces préférences de consentement sont stockées dans le groupe de champs de consentement XDM Profile et sont synchronisées dans et hors de Journey Optimizer B2B Edition dans le cadre de la structure de synchronisation des données. Ces préférences sont utilisées au moment de la diffusion pour exclure les profils désinscrits des diffusions.

## Pas encore disponible

Les fonctionnalités de gouvernance suivantes ne sont pas encore disponibles, mais sont incluses dans la feuille de route du produit :

* Application des étiquettes d’utilisation des données (DULE) / stratégies d’utilisation
* Assurance des données
* Réinitialisation du sandbox
* Règles de consentement
* Contrôle d’accès au niveau du champ (FLAC)
* Contrôle d’accès de niveau objet (OLAC)
* Cryptage CMK des données au repos
* Service d’audits de plateformes
