---
title: Ressources
description: Découvrez la gestion des ressources dans Journey Optimizer B2B Edition.
feature: Assets, Content
exl-id: f3848e65-3196-4d1f-90cf-7aa6ceeafabb
source-git-commit: dcd8ab2820d60654e8970944054142fc296ed54f
workflow-type: tm+mt
source-wordcount: '963'
ht-degree: 0%

---

# Ressources

Assets sont généralement les images utilisées pour créer le contenu de votre parcours dans Adobe Journey Optimizer B2B Edition. Vous pouvez utiliser ces images dans les emails, les modèles d’email et les fragments créés dans Journey Optimizer B2B Edition par le biais d’un sélecteur de ressources ou d’une simple interface glisser-déposer dans l’éditeur de contenu visuel.

Adobe Journey Optimizer B2B Edition offre aux marketeurs l’accès à deux types de bibliothèques de ressources : Adobe Marketo Engage Design Studio et Adobe Experience Manager Assets as a Cloud Service. Vous pouvez utiliser uniquement Adobe Marketo Engage Design Studio ou les deux bibliothèques configurées en même temps (en fonction de la licence AEM Assets que vous possédez).

## Gestion des ressources

Si vous disposez d’un compte de Marketo Engage et de Adobe Experience Manager en tant que Cloud Service, vous avez accès aux référentiels pour la gestion des actifs numériques des Marketo Engage et Adobe Experience Manager Assets as a Cloud Service lorsque votre compte d’utilisateur dispose des autorisations requises. Ces référentiels sont séparés et non synchronisés. Vous pouvez utiliser des images provenant d’une source ou d’une autre, mais une seule peut être activée à la fois dans l’éditeur de contenu. Un administrateur peut rendre le passage de la gestion des actifs numériques du Marketo Engage à Adobe Experience Manager Assets as a Cloud Service. L’élément _[!UICONTROL Assets]_ dans le volet de navigation de gauche affiche le référentiel actuellement défini.

### Adobe Marketo Engage Design Studio

Le référentiel de ressources de Adobe Marketo Engage Design Studio est fourni par défaut avec chaque abonnement à Journey Optimizer B2B Edition. Cela signifie que vous avez accès à l’une des ressources d’image stockées dans Adobe Marketo Engage > Design Studio > Images et fichiers. Vous pouvez utiliser ce référentiel comme bibliothèque de ressources locales, notamment pour charger, supprimer et télécharger des fonctions de ressources. Vous pouvez également utiliser ces ressources dans le contenu de votre parcours.

Formats de fichiers pris en charge : JPEG, GIF, PNG, EPS, SVG, RGB

### as a Cloud Service Adobe Experience Manager Assets

Rassemblez les workflows marketing et créatifs à l’aide d’Adobe Experience Manager Assets. Il est nativement intégré à Adobe Journey Optimizer B2B Edition, ce qui vous permet d’accéder facilement à Assets as a Cloud Service pour découvrir et utiliser des ressources numériques. Il permet d’accéder au référentiel Assets pour les ressources que vous pouvez utiliser pour remplir vos messages.

Adobe Experience Manager Assets peut se connecter à Adobe Experience Manager Assets as a Cloud Service pour des espaces de travail de ressources centralisés qui étendent votre système de création et unifient les ressources numériques en vue de la diffusion de l’expérience. Adobe Experience Manager Assets as a Cloud Service offre une solution cloud conviviale pour une gestion efficace des actifs numériques et des opérations Dynamic Media. Elle intègre de manière transparente des fonctionnalités avancées, notamment l’intelligence artificielle et l’apprentissage automatique.

Pour en savoir plus, consultez la [documentation Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/assets/overview).

Adobe Experience Manager Assets est accessible directement dans Adobe Journey Optimizer B2B Edition à partir de l’élément **[!UICONTROL Assets]** dans le volet de navigation de gauche. Vous pouvez également accéder aux ressources et aux dossiers lors de la conception d’un contenu d’email.

>[!NOTE]
>
>AEM Assets en tant que Cloud Service et les licences Dynamic Media sont des conditions préalables à cette intégration.<br/>
>En fonction de votre contrat et de votre configuration, Adobe Experience Manager Assets as a Cloud Service est accessible directement depuis Adobe Journey Optimizer B2B Edition via la section Assets du menu de gauche. Vous pouvez également accéder aux ressources et aux dossiers lors de la conception d’un contenu d’email.

Actuellement, vous ne pouvez utiliser que des images d’Adobe Experience Manager Assets dans Adobe Journey Optimizer Édition B2B.

## Utilisation de ressources pour la création de contenu

Utilisez des ressources lorsque vous créez vos emails, modèles de courrier électronique et fragments visuels. L’interface utilisateur de l’éditeur de contenu visuel permet d’accéder aux images de vos référentiels de ressources connectés.

### Choix d’une source de ressources

Si vous disposez d’un abonnement Experience Manager Assets as a Cloud Service ainsi que de Adobe Marketo Engage Design Studio par défaut, vous pouvez choisir des ressources d’image à partir de l’une des sources. Pour ce faire, vous devez sélectionner la source de l’image au moment de la création pour un nouvel email, un modèle d’email ou un fragment visuel. Vous pouvez également sélectionner la source de l’image lorsque vous modifiez le contenu. La sélection s’applique uniquement à l’expérience de modification. Vous pouvez modifier la source de l’image pour accéder aux ressources d’une autre bibliothèque, le cas échéant.

Créer un email

Modification d’un email : pour choisir une source de ressources d’image dans l’éditeur visuel, utilisez le sélecteur **[!UICONTROL Sélectionner la source d’image]** situé en haut de la zone de travail.

### Ajout de ressources à votre contenu

Vous pouvez ajouter une ressource image lorsque vous créez votre contenu, en fonction de la source de la ressource d’image sélectionnée.

>[!BEGINTABS]

>[!TAB  Ajout de ressources d’image Marketo Engage Design Studio ]

Vous pouvez ajouter des ressources Marketo Engage Design Studio à l’aide de l’une des méthodes suivantes :

* Ajoutez un élément structurel, puis faites glisser des ressources depuis le volet de navigation de gauche vers le canevas visuel.
* Ajoutez un élément structurel, puis faites glisser et déposez le type de contenu _image_ dans la structure. Dans les paramètres des propriétés à droite, il existe deux manières de spécifier l’image :
   * Cliquez sur **[!UICONTROL Parcourir]** pour ouvrir le sélecteur de ressources, où vous pouvez choisir une image dans la bibliothèque de ressources de Adobe Marketo Engage Design Studio.
   * Cliquez sur **[!UICONTROL Importer un média]** pour importer une ressource à partir de votre système local. La ressource importée est stockée dans le dossier racine Assets de votre bibliothèque Adobe Marketo Engage Design Studio.

Pour modifier l’image, vous pouvez mettre à jour l’URL source de l’image dans les propriétés à droite.

>[!TAB Ajouter des images Experience Manager Assets]

1. Lors de la création du contenu de votre email dans le concepteur d&#39;email, faites glisser un élément image sur la zone de travail.

   Les propriétés sur la droite reflètent la sélection de l’élément d’image.

1. Cliquez sur **[!UICONTROL Sélectionner une ressource]** pour ouvrir le sélecteur de ressources Experience Manager.

   Vous pouvez y rechercher, filtrer et accéder à la ressource de contenu souhaitée à ajouter à votre ressource marketing. Pour plus d’informations sur l’utilisation du sélecteur, reportez-vous à cette page .

   >[!NOTE]
   >
   >Si plusieurs référentiels sont configurés, vous pouvez utiliser le sélecteur de référentiel sur le sélecteur de ressources.

1. Sélectionnez la ressource à insérer dans le courrier électronique.

>[!ENDTABS]