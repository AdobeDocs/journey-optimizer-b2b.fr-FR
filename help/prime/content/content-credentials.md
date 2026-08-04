---
title: Content Credentials
description: Découvrez comment Adobe Journey Optimizer B2B Prime applique automatiquement Content Credentials aux images générées avec l’IA générative et ce que cela signifie pour votre contenu.
feature: Assets, Content
role: User
badgeBeta: label="Beta" type="informative" tooltip="Cette fonctionnalité fait partie d’une version bêta limitée."
autotag-review: '2026-07-31T22:31:06.899Z'
TQID: 'https://experienceleague.adobe.com/fBPnAmupve3xMSw5fZPQBDTUfr-rwiH2-R3wbKvox-E'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a65c8aea-b21a-41ce-9ed7-6b517a69fd0bid: e666e996-b2cf-4c45-8fc2-1c625212ababid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: c8402946-ff35-44c5-ab98-74c1bba0975f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: edb796d131c2b058215b73519b845125432d84f8
workflow-type: tm+mt
source-wordcount: 562
ht-degree: 1%

---

# Content Credentials

Les organisations marketing sont plus que jamais préoccupées par la transparence du contenu, la divulgation de l’IA et la prévention de l’altération des ressources. Le Content Authenticity Initiative (CAI) d’Adobe crée des outils conformes à la norme technique C2PA ([ Coalition for Content Provenance and Authenticity](https://c2pa.org/specifications/specifications/1.1/specs/C2PA_Specification.html#_trust_model). __ est l’ensemble de métadonnées chiffrées et infalsifiables qui peuvent aider les visiteurs et les visiteuses à comprendre la traçabilité du contenu et à assurer l’intégrité des ressources de la marque. Ces informations incluent :

* Émetteur ou signataire : informations sur l’entité ou la société qui a émis la signature numérique pour certifier ou signer la ressource.
* Date d&#39;émission — Date à laquelle le Content Credential a été appliqué à la ressource.
* Crédit et utilisation — Informations sur le producteur de l&#39;actif, y compris le nom, les identifiants de médias sociaux ou d&#39;autres informations relatives à l&#39;identité.
* Processus — Enregistrements de toute modification apportée à l&#39;actif.
* Détails de l’appareil : informations sur l’application ou l’appareil utilisé pour créer ou modifier la ressource.
* Outil d’IA utilisé : si l’IA générative a été utilisée pour créer la ressource, le nom du modèle utilisé peut être inclus.
* Autres informations pertinentes : des données supplémentaires sont également incluses pour aider à fournir plus de contexte sur l’historique d’une ressource.

Pour obtenir des informations complètes sur l’historique des ressources, vous pouvez utiliser l’outil [inspection](https://contentauthenticity.adobe.com/inspect) d’Adobe Content Authenticity.

Les Content Credentials sont conservées avec le fichier image. Lorsqu’une image qui a été générée ou modifiée avec l’IA générative est chargée vers ou exportée à partir de [!DNL Adobe Journey Optimizer B2B Prime], ses Content Credentials sont conservées.

>[!NOTE]
>
>Certaines méthodes d’importation d’images dans votre contenu, telles que l’extraction d’une image d’un PDF ou d’une source incorporée (base64), peuvent ne pas conserver le Content Credentials d’origine. Dans ce cas, Content Credentials ne peut pas être lu à partir de la source et aucun n’est créé pour le résultat.

>[!BEGINSHADEBOX]

## Persistance de Content Credentials par le biais des canaux {#channels}

Lorsque vous incluez des images dans vos e-mails ou messages WhatsApp, le Content Credentials des images diffusées est également conservé :

* **E-mail** - Lorsque vous utilisez une action de parcours _Envoyer un e-mail_, ajoutez l’image au contenu de votre e-mail à partir de la bibliothèque _Assets_. Lorsque l’e-mail est diffusé, le destinataire peut télécharger l’image à partir du message et le Content Credentials est intact.
* **WhatsApp** - Ajoutez l&#39;image à votre modèle de message WhatsApp dans votre compte professionnel Meta. Vous pouvez l&#39;ajouter directement depuis votre système ou télécharger un fichier image à partir de la bibliothèque __. Utilisez le modèle pour une action de parcours _Send WhatsApp_. Lorsque le message WhatsApp est diffusé, le destinataire peut télécharger l&#39;image à partir du message et le Content Credentials est intact.

>[!ENDSHADEBOX]

## Génération d’images {#generate}

>[!INFO]
>
>De nouvelles lois émergent autour de la transparence générative de l’IA, et Adobe s’efforce de répondre aux exigences applicables dans toutes les juridictions. Content Credentials est l’outil de provenance utilisé par Adobe pour répondre aux exigences de ces lois.

Lorsque vous utilisez l’IA générative pour créer une image pour le contenu de votre e-mail dans [!DNL Journey Optimizer B2B Prime], les Content Credentials sont automatiquement jointes à l’image générée et aucune action n’est requise de votre part. Les outils d’IA générative produisent un élément Content Credentials combiné pour les variantes des images avec des informations d’identification existantes, y compris la source d’origine.

>[!NOTE]
>
>[!DNL Journey Optimizer B2B Prime] ne prend actuellement pas en charge les actions de modification manuelle d’images. Les workflows Content Credentials pour ces actions ne sont pas applicables à ce stade.
