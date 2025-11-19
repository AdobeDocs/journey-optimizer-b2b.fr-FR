---
title: Ressources
description: Gérez les ressources d’images de Journey Optimizer B2B edition et AEM Assets pour les e-mails, les modèles et les fragments.
feature: Assets, Content
role: User
exl-id: f3848e65-3196-4d1f-90cf-7aa6ceeafabb
source-git-commit: 1c5a08b293db9287d03b103d794cc17a1c186af0
workflow-type: tm+mt
source-wordcount: '852'
ht-degree: 60%

---

# Ressources

Dans [!DNL Adobe Journey Optimizer B2B Edition], les ressources sont généralement les images utilisées lors de la conception du contenu pour accompagner les parcours de compte. Vous pouvez utiliser ces images dans vos e-mails, modèles d’e-mail et fragments du sélecteur de ressources, ou une simple interface glisser-déposer dans l’espace de conception visuelle.

[!DNL Journey Optimizer B2B Edition] permet aux concepteurs et aux spécialistes du marketing d’accéder à deux types de bibliothèques de ressources : un référentiel de ressources [!DNL Journey Optimizer B2B Edition] interne et des [!DNL Adobe Experience Manager Assets as a Cloud Service]. Vous pouvez utiliser uniquement le référentiel intégré ou utiliser les deux types de bibliothèque en même temps (en fonction de la licence [!DNL Experience Manager Assets] dont vous disposez).

## Gestion des ressources

Si vous disposez d’[!DNL Adobe Experience Manager as a Cloud Services] et qu’il est configuré en tant que source de ressources dans [!DNL Journey Optimizer B2B Edition], vous avez accès aux deux types de référentiel lorsque votre compte utilisateur dispose des autorisations requises. Ces référentiels sont séparés et non synchronisés. Vous pouvez utiliser des images provenant de l’une ou l’autre source.

### Ressources internes

Le référentiel de ressources interne est fourni par défaut avec chaque abonnement [!DNL Journey Optimizer B2B Edition]. Cela signifie que vous avez accès à l’une des ressources d’image stockées dans le système de fichiers de ressources d’[!DNL Adobe Marketo Engage] connecté. Vous pouvez utiliser ce référentiel comme votre bibliothèque de ressources locale, y compris les fonctions de chargement et de téléchargement de ressources. Vous pouvez également utiliser ces ressources dans le contenu de votre parcours.

Vous pouvez [modifier ces ressources à l’aide d’Adobe Express](./image-edit-adobe-express.md) et les déplacer dans des dossiers pour les organiser afin de les utiliser dans vos e-mails, modèles et fragments.

Formats de fichiers pris en charge : JPG, JPEG, GIF, PNG, EPS, SVG et RGB

### Adobe Experience Manager Assets as a Cloud Service

Rassemblez les workflows marketing et créatifs à l’aide de [!DNL Adobe Experience Manager Assets]. Il est nativement intégré à [!DNL Journey Optimizer B2B Edition], ce qui vous permet d’accéder facilement à Assets as a Cloud Service pour découvrir et utiliser des ressources numériques. Vous avez ainsi accès à votre référentiel Assets de ressources que vous pouvez utiliser pour renseigner vos messages.

[!DNL Adobe Journey Optimizer B2B Edition] peut se connecter à [!DNL Adobe Experience Manager Assets as a Cloud Service] pour une gestion centralisée des ressources, étendant votre système de création et unifiant les ressources numériques pour la diffusion d’expériences. [!DNL Adobe Experience Manager Assets as a Cloud Service] offre une solution cloud facile à utiliser pour une gestion efficace des ressources numériques et des opérations Dynamic Media. Il intègre de manière transparente des fonctionnalités avancées, notamment l’intelligence artificielle et le machine learning.

Apprenez-en plus dans la [documentation d’Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/assets/overview){target="_blank"}.

{{aem-assets-licensing-note}}

Accédez à [!DNL Adobe Experience Manager Assets] directement dans [!DNL Journey Optimizer B2B Edition] à partir de l’élément **[!UICONTROL Experience Manager Assets]** dans le volet de navigation de gauche de conception de contenu. Vous pouvez également accéder aux ressources et aux dossiers lors de la conception de votre e-mail, de votre modèle d’e-mail et du contenu du fragment visuel.

Actuellement, vous ne pouvez utiliser que des images provenant d’Adobe Experience Manager Assets dans Adobe Journey Optimizer B2B Edition.

## Utiliser des ressources pour la création de contenu

Utilisez des ressources pour créer des e-mails, des modèles d’e-mail et des fragments visuels. L’éditeur de contenu visuel permet d’accéder aux images dans vos référentiels de ressources connectés. Si vous disposez également d’un abonnement à Experience Manager Assets as a Cloud Service, vous pouvez choisir des ressources d’image à partir de l’une ou l’autre des sources. Vous pouvez également charger une ressource image, qui la place dans le référentiel de ressources interne.

Vous pouvez choisir la source de l’image lorsque vous modifiez les paramètres d’un composant d’image ou directement sur la zone de travail :

* **_Paramètres des composants d’image_** - Lorsqu’un composant d’image est sélectionné dans la zone de travail, vous pouvez afficher et modifier les paramètres dans le panneau de droite. Pour ajouter ou modifier le fichier image affiché dans le composant, choisissez le type de source et sélectionnez un fichier image.

  ![Modifier les paramètres du composant d’image dans le panneau de droite](./assets/content-assets-image-settings.png){width="350"}

* **_Composant vide_** - Lorsque vous ajoutez un composant d’image à la zone de travail, il est vide et permet d’accéder facilement à une source et à sélectionner un fichier image.

  ![Choisir une source afin de sélectionner un fichier image pour le composant d’image vide](./assets/content-assets-image-component-empty.png){width="500"}

* **_Barre d’outils de composant d’image_** - Lorsqu’un composant d’image est sélectionné dans la zone de travail, la barre d’outils permet d’accéder facilement à une source et de sélectionner le fichier image.

  ![Utiliser la barre d’outils afin de choisir une source et sélectionner un fichier image pour le composant d’image](./assets/content-assets-image-toolbar-settings.png){width="500"}

Vous pouvez ajouter une ressource d’image au fur et à mesure que vous créez votre contenu, selon la source celle-ci. Vous pouvez également choisir une ressource d’image dans les paramètres d’arrière-plan d’un composant de structure.

>[!BEGINTABS]

>[!TAB Sélectionner une ressource]

Cliquez sur **[!UICONTROL Sélectionner une ressource]** pour ouvrir le sélecteur de ressources, où vous pouvez choisir une image dans le référentiel de ressources B2B edition Journey Optimizer.

![Sélectionner une ressource image](./assets/content-assets-internal-image-selected.png){width="700" zoomable="yes"}

Vous pouvez utiliser la recherche et les filtres pour localiser la ressource d’image souhaitée. Sélectionnez la ressource et cliquez sur **[!UICONTROL Sélectionner]** afin de l’utiliser pour le composant d’image.

Pour plus d’informations sur l’utilisation des ressources d’images internes, voir [ Utilisation des ressources dans votre contenu ](./internal-image-assets.md#use-assets-in-your-content).

>[!TAB Experience Manager Assets]

Cliquez sur **[!UICONTROL Experience Manager Assets]** pour ouvrir le sélecteur de ressources, dans lequel vous pouvez choisir une image dans le référentiel Experience Manager Assets.

![Sélectionner une ressource image dans le référentiel AEM Assets](./assets/content-assets-image-aem-selected.png){width="700" zoomable="yes"}

Vous pouvez utiliser la recherche et les filtres pour localiser la ressource d’image souhaitée. Sélectionnez la ressource et cliquez sur **[!UICONTROL Sélectionner]** afin de l’utiliser pour le composant d’image.

Pour plus d’informations sur l’utilisation des fichiers image d’[!DNL Experience Manager Assets], consultez [Accéder aux images AEM Assets](./aem-assets.md#access-aem-assets-images).

>[!TAB Importer un média]

Cliquez sur **[!UICONTROL Importer un média]** pour sélectionner un fichier image et l’importer en tant que ressource pouvant être utilisée pour le contenu Journey Optimizer B2B Edition.

![Sélectionner votre propre fichier image à importer en tant que ressource](./assets/content-assets-image-import-file-selected.png){width="450" zoomable="yes"}

Après avoir fait un glisser-déposer du fichier ou l’avoir sélectionné dans votre système de fichiers, cliquez sur **[!UICONTROL Importer]**. La ressource importée est stockée dans le référentiel de ressources [!DNL Journey Optimizer B2B Edition].

>[!ENDTABS]
