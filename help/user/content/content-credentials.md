---
title: Content Credentials
description: Découvrez comment Adobe Journey Optimizer B2B edition applique automatiquement Content Credentials aux images générées ou modifiées à l’aide d’outils d’IA génératifs et ce que cela signifie pour votre contenu.
feature: Assets, Content
role: User
autotag-review: '2026-07-31T22:15:54.535Z'
TQID: 'https://experienceleague.adobe.com/9XCqPWz62uDDLFAyxARfD2jErYx2aOiOB5fAOGLLTbo'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a65c8aea-b21a-41ce-9ed7-6b517a69fd0b
  - id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2:
  - id: c8402946-ff35-44c5-ab98-74c1bba0975f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: edb796d131c2b058215b73519b845125432d84f8
workflow-type: tm+mt
source-wordcount: 916
ht-degree: 0%

---

# Content Credentials

Les organisations marketing sont plus que jamais préoccupées par la transparence du contenu, la divulgation de l’IA et la prévention de l’altération des ressources. Le Content Authenticity Initiative (CAI) d’Adobe crée des outils conformes à la norme technique C2PA ([&#x200B; Coalition for Content Provenance and Authenticity](https://c2pa.org/specifications/specifications/1.1/specs/C2PA_Specification.html#_trust_model). __ est l’ensemble de métadonnées chiffrées et infalsifiables qui aide les visiteurs à comprendre la parenté du contenu et à assurer l’intégrité des ressources de la marque. Ces informations incluent :

* Émetteur ou signataire - Informations sur l’entité ou la société qui a émis la signature numérique pour certifier ou signer la ressource.
* Date de l’événement - Date à laquelle le Content Credential a été appliqué à la ressource.
* Crédit et utilisation - Informations sur le producteur de la ressource, y compris le nom, les identifiants de médias sociaux ou d’autres informations relatives à l’identité.
* Processus - Enregistrements de toutes les modifications apportées à la ressource.
* Détails de l’appareil : informations sur l’application ou l’appareil utilisé pour créer ou modifier la ressource.
* Outil d’IA utilisé - Si l’IA générative a été utilisée pour modifier ou créer la ressource, le nom du modèle utilisé peut être inclus.
* Autres informations pertinentes : des données supplémentaires peuvent également être incluses pour offrir plus de contexte sur l’historique d’une ressource.

Pour obtenir des informations complètes sur l’historique des ressources, vous pouvez utiliser l’outil [inspection](https://contentauthenticity.adobe.com/inspect) d’Adobe Content Authenticity.

Les Content Credentials sont conservées avec le fichier image. Lorsqu’une image qui a été générée ou modifiée avec l’IA générative est chargée vers ou exportée à partir de [!DNL Adobe Journey Optimizer B2B Edition], ses Content Credentials sont conservées.

>[!NOTE]
>
>Certaines méthodes d’importation d’images dans votre contenu, telles que l’extraction d’une image d’un PDF ou d’une source incorporée (base64), peuvent ne pas conserver le Content Credentials d’origine. Dans ce cas, Content Credentials ne peut pas être lu à partir de la source et aucun n’est créé pour le résultat.

>[!BEGINSHADEBOX]

## Persistance de Content Credentials par le biais des canaux {#channels}

Lorsque vous incluez des images dans vos e-mails ou messages WhatsApp, le Content Credentials des images diffusées est également conservé :

* **E-mail** - Lorsque vous utilisez une action de parcours _Envoyer un e-mail_, ajoutez l’image au contenu de votre e-mail à partir de la bibliothèque _Assets_. Lorsque l’e-mail est diffusé, le destinataire peut télécharger l’image à partir du message et le Content Credentials est intact.
* **WhatsApp** - Ajoutez l&#39;image à votre modèle de message WhatsApp dans votre compte professionnel Meta. Vous pouvez l&#39;ajouter directement à partir de votre propre système ou télécharger un fichier image à partir de la bibliothèque __. Utilisez le modèle pour une action de parcours _Send WhatsApp_. Lorsque le message WhatsApp est diffusé, le destinataire peut télécharger l&#39;image à partir du message et le Content Credentials est intact.

>[!ENDSHADEBOX]

## Actions affectant Content Credentials {#cc-workflows}

>[!INFO]
>
>De nouvelles lois émergent autour de la transparence générative de l’IA, et Adobe s’efforce de répondre aux exigences applicables dans toutes les juridictions. Content Credentials est l’outil de provenance utilisé par Adobe pour répondre aux exigences de ces lois.

Lorsque vous générez ou modifiez une image à l’aide d’outils d’IA générative dans [!DNL Journey Optimizer B2B Edition], Content Credentials est automatiquement associé à cette image et aucune action n’est requise de votre part.

### Générer une image {#generate}

**_Exemple:_** générez une image de bannière pour un e-mail à partir d’une invite de texte décrivant le visuel souhaité. Les Content Credentials sont jointes à l’image générée.

Lorsque vous créez une image à partir d’une invite de texte, d’une image de référence ou que vous générez une image similaire, les Content Credentials sont toujours jointes.

### Recadrer une image {#crop}

**_Examples:_**

* Recadrez une image de bannière générée pour l’adapter à une page web. Les Content Credentials sont préservées tout au long du recadrage.
* Utilisez une photo de catalogue chargée comme arrière-plan d’e-mail et recadrez-la pour l’adapter à l’écran. Si la photo de stock ne contient aucune information d’IA générative, les Content Credentials ne sont pas créées.

Lorsque vous apportez un ajustement à un fichier image, par exemple en le recadrant aux dimensions demandées, il ne conserve son Content Credentials que si l’image source en disposait déjà. Le recadrage recrée les pixels de l’image, ce qui supprime normalement ce Content Credential. Par conséquent, l’assistant AI la lit à partir de l’image source avant de la recadrer, puis la recrée et la joint à nouveau au résultat recadré. Le recadrage lui-même n&#39;ajoute pas une nouvelle action générative de l&#39;IA : il préserve celle qui existe.

### Ajouter une superposition de texte

**_Exemple:_** générez un titre promotionnel comme superposition de texte sur une image d’arrière-plan générée pour une page de destination. Le Content Credentials de l’image d’arrière-plan est conservé.

Lorsque vous effectuez le rendu du texte généré au-dessus d’une image d’arrière-plan, les Content Credentials ne sont jointes à l’image résultante que si l’image d’arrière-plan avait déjà Content Credentials. Le rendu du recouvrement génère une nouvelle image ; l’outil d’édition d’images lit donc le Content Credentials en arrière-plan et le relie au résultat. L’étape de recouvrement n’ajoute pas de nouvelle action d’IA générative.

### Recouvrir une image

**_Examples:_**

* Créez un en-tête d’e-mail en combinant une image de produit générée avec un arrière-plan généré. Le résultat transmet Content Credentials reflétant les deux sources d’IA génératives.
* Combinez deux photos de marque chargées dans une image de collage. Comme aucune image source ne transporte d’action d’IA générative, les Content Credentials ne sont pas créées.

Lorsque vous composez plusieurs images et que l’une des images sources possède Content Credentials, l’image combinée les conserve et les fusionne en un seul élément de métadonnées Content Credentials. La composition produit une nouvelle image à partir des sources, ce qui supprime normalement ces Content Credentials. Mais les outils d’édition d’images lisent chacun d’eux avant de les composer, puis créent un seul élément Content Credentials combiné qui répertorie chaque source ayant contribué à une action d’IA générative.

<!--

In [!DNL Adobe Journey Optimizer B2B Edition], you can see Content Credentials directly within the _Assets_ library. When you open the asset details, any image with Content Credentials (such as those created with GenAI services) shows the manifest details in a dedicated panel. If the asset is downloaded, published, or shared, the Content Credentials remain intact with the asset.

_To access Content Credentials:_

1. In the left navigation, expand **[!UICONTROL Content Management]** and select **[!UICONTROL Assets]**.

   This action opens a listing page with all the assets listed.

1. Navigate to a folder, and select the desired asset.

1. In the right panel, ??? where is it.

-->