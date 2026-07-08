---
title: Fonctionnalités de gouvernance et de confidentialité
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
source-git-commit: 61481d57fb8eca805d9a9bc545124aed568b5416
workflow-type: tm+mt
source-wordcount: 697
ht-degree: 2%

---

# Fonctionnalités de gouvernance et de confidentialité

[!DNL Journey Optimizer B2B Edition] est une application Adobe Experience Platform intégrée. Il utilise plusieurs outils et services qui permettent de contrôler vos données d’expérience collectées conformément à vos pratiques commerciales, à vos obligations légales et à vos processus de développement. Les sections ci-dessous résument chacune de ces fonctionnalités de gouvernance.

## Confidentialité

Plusieurs réglementations s’appliquent aux clients [!DNL Journey Optimizer B2B Edition] qui détiennent des données pour les titulaires de données résidant dans les régions ou pays respectifs mentionnés ci-dessus (UE, Californie, Thaïlande, Brésil, Nouvelle-Zélande). Ces informations sur cette page ne sont pas des conseils juridiques et ne garantissent pas votre conformité avec la loi applicable.

### RGPD

Le Règlement général sur la protection des données (RGPD) est la loi de l’Union européenne (UE) sur la protection de la vie privée qui harmonise et modernise les [ exigences en matière de protection des données ](https://commission.europa.eu/law/law-topic/data-protection/data-protection-explained_en){target="_blank"} pour les pays de l’UE.

[!DNL Journey Optimizer B2B Edition] utilise les fonctionnalités de gouvernance existantes du RGPD de Marketo Engage fournies par Privacy Service et le service Marketo Privacy Broker.

### CNIL

Le 14 avril 2026, la Commission nationale de l&#39;informatique et des libertés (CNIL) [a publié une recommandation](https://cnil.fr/sites/default/files/2026-05/recommandation_tracking_pixels_emails.pdf) sur l&#39;utilisation des pixels de tracking dans les emails. Ces conseils clarifient le moment où le consentement est requis et soulignent l’importance de bonnes pratiques de consentement pour le suivi des pixels d’e-mail. Cette politique affecte toute entité qui envoie des e-mails à des abonnés basés en France.

La CNIL a prévu un délai de trois mois à compter de la date de la recommandation pour que les entreprises informent leurs destinataires d&#39;emails de la présence des pixels de tracking, de leur finalité et du droit de désinscription des destinataires. Pendant cette période de transition, les utilisateurs de Marketo Engage doivent informer leurs destinataires du suivi des pixels et fournir un droit d’opposition si nécessaire. La CNIL devrait commencer ses activités d&#39;application après le 14 juillet 2026.

Alors que la CNIL et d’autres organismes de réglementation clarifient les conseils sur le tracking des pixels et les problèmes associés, Adobe continuera à surveiller les mises à jour et à vous informer de l’évolution des fonctionnalités techniques.

[!DNL Journey Optimizer B2B Edition] offre des commandes qui vous aident à gérer le suivi des ouvertures au niveau des e-mails. Les utilisateurs sont responsables de déterminer leurs propres obligations de conformité en vertu des directives de la CNIL applicables et d&#39;autres lois. Pour plus d’informations sur l’utilisation de ces fonctionnalités pour gérer le suivi des ouvertures d’e-mail, voir [_Gérer le suivi des e-mails_](../content/email-tracking-manage.md).

## Contrôle d’accès en fonction du rôle (RBAC)

Avec Journey Optimizer B2B edition et l’accès au Adobe Admin Console, les administrateurs peuvent accorder à un utilisateur des autorisations sur un type d’entité (affichage-segments, gestion-segments, gestion-parcours, etc.). Cette fonctionnalité fait partie de la structure des autorisations unifiées (UPF) qui permet à tous les clients Adobe Experience Platform de définir et de gérer des rôles et des autorisations pour leur organisation.

## Chiffrement des données

**_Chiffrement des données au repos_** - Toutes les données de profil de compte et de personne transférées de Adobe Experience Platform vers Journey Optimizer B2B edition sont chiffrées afin de garantir la conformité existante d’Experience Platform. Toutes les entités provenant de Journey Optimizer B2B edition, telles que les parcours et les groupes d’achats, sont également chiffrées.

**_Chiffrement des données en transit_** (sur un réseau public) : toutes les API et entités Journey Optimizer B2B edition sont chiffrées en transit à l’aide de TLS 1.2.

## Souscription au consentement/désinscription

Journey Optimizer B2B edition lit les préférences de consentement par personne stockées dans les profils XDM Adobe Experience Platform et les applique au moment de la diffusion des messages pour les canaux e-mail, SMS et WhatsApp. Une personne qui s’est désabonnée d’un canal est exclue de la diffusion avant que le contenu ne soit envoyé à partir du canal ou du fournisseur de messagerie en aval.

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
