---
title: Consentement de la messagerie de canal
description: Découvrez comment Journey Optimizer B2B edition lit les préférences de consentement du profil XDM AEP et applique les processus d’opt-in et d’opt-out au moment de la diffusion des messages pour les canaux e-mail, SMS et WhatsApp.
feature: Setup, Channels
role: Admin, User
autotag-review: '2026-05-19T16:18:37.228Z'
TQID: 'https://experienceleague.adobe.com/-c0dJnpfiIcj0B5gViyEQ7E1Ws0BwP864OLF003rOjw'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
subfeature_v2:
  - id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
  - id: a22f05f6-0fcf-40c0-a70e-e13a3db185f7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: cba977f62f3d2a83bcf2487a8ec612b76a655954
workflow-type: tm+mt
source-wordcount: 412
ht-degree: 2%

---

# Consentement des messages de canal

Adobe Journey Optimizer B2B edition lit les préférences de consentement par personne stockées dans les profils XDM Adobe Experience Platform et les applique au moment de la diffusion des messages, dans le cadre des [contrôles de gouvernance](../admin/governance.md) de l’application. Les personnes qui se sont exclues d’un canal sont exclues de la diffusion avant l’envoi du contenu depuis le canal ou le fournisseur de messagerie en aval.

Les sections suivantes décrivent comment Journey Optimizer B2B edition évalue le consentement au moment de l’envoi du message pour chaque canal pris en charge.

## Adresse e-mail {#email}

Journey Optimizer B2B edition évalue l’attribut XDM suivant pour le consentement par e-mail lors de l’envoi de messages sur le [canal e-mail](../admin/configure-channels-emails.md) :

| Attribut XDM | `y` | `n` | Aucune valeur |
| --- | --- | --- | --- |
| `consents.marketing.email.val` | Opt-in | Opt-out | Opt-in |

Tenez compte des points suivants pour le consentement par e-mail :

* Les personnes qui se sont désinscrites des e-mails peuvent recevoir des e-mails marqués comme opérationnels.
* Les préférences au niveau de l’abonnement ne sont pas prises en charge.

## SMS {#sms}

Journey Optimizer B2B edition évalue les attributs XDM suivants pour le consentement par SMS lors de l’envoi de messages par le biais du [&#x200B; canal SMS &#x200B;](../admin/configure-channels-sms.md) :

| Attribut XDM | `y` | `n` | Aucune valeur |
| --- | --- | --- | --- |
| `consents.marketing.sms.val` | Opt-in | Opt-out | Opt-out |
| `consents.marketing.subscriptions.<senderID>` | Opt-in | Opt-out | Opt-out |
| `consents.marketing.sms.subscriptions.<senderId>.subscribers.<phoneNumber>` | Opt-in | Opt-out | Opt-out |

Tenez compte des points suivants pour le consentement par SMS :

* Lorsqu’un enregistrement de prospect (personne) est exclu des SMS, l’enregistrement est entièrement exclu et n’est pas transmis aux fournisseurs SMS en aval.
* Lorsqu’il est disponible, le consentement au niveau de l’abonnement est évalué. Le processus d’opt-out global est utilisé comme solution de secours lorsque le consentement au niveau de l’abonnement n’est pas disponible.
* Les personnes désinscrites des SMS peuvent toujours recevoir des messages marqués comme opérationnels.
* Si plusieurs enregistrements de prospect partagent le même numéro de téléphone, ils partagent le même statut d’opt-in ou d’opt-out.

## WhatsApp {#whatsapp}

Journey Optimizer B2B edition évalue les attributs XDM suivants pour le consentement WhatsApp lors de l’envoi de messages par le biais d’un canal [WhatsApp](../admin/configure-channels-whatsapp.md) configuré :

| Attribut XDM | `y` | `n` | Aucune valeur |
| --- | --- | --- | --- |
| `consents.marketing.whatsApp.val` | Opt-in | Opt-out | Opt-out |
| `consents.idSpecific.Phone.<number>.marketing.whatsApp.val` | Opt-in | Opt-out | Opt-out |

Gardez à l’esprit les points suivants pour le consentement WhatsApp :

* Si la valeur d’attribut WhatsApp globale (`consents.marketing.whatsApp.val`) est présente, elle est utilisée pour l’évaluation du consentement.
* Si la valeur d’attribut globale n’est pas présente, mais qu’une entrée spécifique à l’expéditeur est présente, l’entrée spécifique à l’expéditeur est utilisée pour l’évaluation du consentement.
* Si aucune valeur n’est présente pour l’un des attributs, la personne est traitée comme ayant exercé son droit d’opposition.

## Non pris en charge {#not-supported}

Les fonctionnalités suivantes liées au consentement ne sont actuellement pas prises en charge dans Journey Optimizer B2B edition :

* Politiques de consentement d’AEP
* Attributs de préférences marketing (`consents.marketing.preferred`)
