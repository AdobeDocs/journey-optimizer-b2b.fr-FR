---
title: Utilisation de Experience Manager Assets
description: Découvrez comment utiliser des ressources d’image d’un référentiel AEM Assets connecté lors de la création de contenu dans Adobe Journey Optimizer B2B Edition.
feature: Assets, Content
source-git-commit: 0bdf0da4db0cbfc781d16f1c50716b1fc8ea4db9
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# Utilisation de ressources Experience Manager

Lorsqu’Adobe Experience Manager Assets as a Cloud Service est intégré à Adobe Journey Optimizer B2B Edition, vous pouvez facilement découvrir et accéder aux ressources numériques à utiliser dans votre contenu marketing. Lorsque vous créez votre contenu, les ressources sont accessibles à partir de l’élément _[!UICONTROL Assets]_ dans le volet de navigation de gauche, et lors de la création de contenu d’email pour un parcours de compte. Vous pouvez également charger des ressources vers le référentiel AEM Assets as a Cloud Service connecté directement à partir de Adobe Journey Optimizer B2B Edition.

>[!NOTE]
>
>Actuellement, seuls les fichiers image d’Adobe Experience Manager Assets sont pris en charge dans Adobe Journey Optimizer B2B Edition. Les modifications apportées aux ressources doivent être effectuées à partir du référentiel central d’Adobe Experience Manager Assets. [En savoir plus](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets)

Lorsque vous utilisez ces ressources numériques, les dernières modifications apportées à Assets as a Cloud Service se propagent automatiquement aux campagnes par e-mail en direct par le biais de références liées. Si des images sont supprimées as a Cloud Service Adobe Experience Manager Assets, les images apparaissent avec une référence rompue dans les emails. Lorsque des ressources actuellement utilisées dans les parcours de compte sont modifiées ou supprimées, les auteurs de parcours sont informés des modifications d’image et de la liste des parcours utilisant l’image. Toutes les modifications apportées aux ressources doivent être effectuées dans le référentiel central d’Adobe Experience Manager Assets.

## Utilisation d’AEM Assets comme source d’image

Si votre environnement dispose d’une ou de plusieurs [connexions de référentiels Assets](../admin/configure-aem-repositories.md), vous pouvez désigner AEM Assets comme source pour les ressources lorsque vous créez ou affichez des détails pour un email, un modèle de courrier électronique ou un fragment visuel.

* Lorsque vous créez un contenu, choisissez `AEM Assets` comme élément **[!UICONTROL Image Source]** dans la boîte de dialogue.

  ![Sélectionnez AEM Assets comme source d’image dans la boîte de dialogue de création](./assets/create-dialog-aem-assets.png){width="500"}

* Lorsque vous ouvrez une ressource de contenu existante, sélectionnez `AEM Assets` dans le panneau _[!UICONTROL Body]_ à droite.

  ![Sélectionnez AEM Assets comme source d’image dans les propriétés](./assets/content-source-aem-assets.png){width="700" zoomable="yes"}

## Accès aux ressources pour la création

>[!IMPORTANT]
>
>Un administrateur doit ajouter les utilisateurs qui doivent accéder à Assets aux profils de produit Utilisateurs consommateurs d’Assets ou/et Utilisateurs d’Assets . [En savoir plus](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/security/ims-support#managing-products-and-user-access-in-admin-console)

Dans l’éditeur de contenu visuel, cliquez sur l’icône _Sélecteur de ressources_ dans la barre latérale gauche. Le panneau Outils devient alors une liste des ressources disponibles dans le référentiel sélectionné.

![Cliquez sur l’icône du sélecteur Assets pour accéder aux ressources d’image](./assets/content-assets-selector-aem-assets.png){width="700" zoomable="yes"}

Si vous disposez de plusieurs référentiels AEM connectés, cliquez sur la flèche de menu de **[!UICONTROL Repository]** pour choisir le référentiel que vous souhaitez utiliser.

![Sélectionnez un référentiel AEM Assets pour accéder aux ressources d’image](./assets/content-assets-selector-aem-repo.png){width="700" zoomable="yes"}

Il existe plusieurs méthodes pour ajouter une ressource image à la zone de travail visuelle :

* Faites glisser une miniature d’image à partir du volet de navigation de gauche.

  ![Sélectionnez un référentiel AEM Assets pour accéder aux ressources d’image](./assets/content-drag-drop-image-aem-assets.png){width="700" zoomable="yes"}

* Ajoutez un composant image à la zone de travail et cliquez sur **[!UICONTROL Parcourir]** pour ouvrir la boîte de dialogue _[!UICONTROL Sélectionner Assets]_.

  Dans la boîte de dialogue, vous pouvez choisir une image dans le référentiel sélectionné.

  Plusieurs outils sont disponibles pour vous aider à localiser la ressource dont vous avez besoin.

  ![Utilisez l’outil dans la boîte de dialogue Sélectionner Assets pour rechercher et sélectionner une ressource image](./assets/content-select-assets-dialog-aem.png){width="700" zoomable="yes"}

   * Modifiez le **[!UICONTROL référentiel]** en haut à droite.

   * Cliquez sur **[!UICONTROL Gérer les ressources]** en haut à droite pour ouvrir le référentiel Assets dans un autre onglet du navigateur et utiliser les outils de gestion AEM Assets.

   * Cliquez sur le sélecteur _Type d’affichage_ en haut à droite pour modifier l’affichage en **[!UICONTROL Mode Liste]**, **[!UICONTROL Affichage de la grille]**, **[!UICONTROL Mode Galerie]** ou **[!UICONTROL Vue Cascade]**.

   * Cliquez sur l’icône _Ordre de tri_ pour changer l’ordre de tri entre croissant et décroissant.

   * Cliquez sur la flèche de menu **[!UICONTROL Trier par]** pour remplacer les critères de tri par **[!UICONTROL Nom]**, **[!UICONTROL Taille]** ou **[!UICONTROL Modifié]**.

   * Cliquez sur l’icône _Filtrer_ en haut à gauche pour filtrer les éléments affichés en fonction de vos critères.

   * Entrez du texte dans le champ Rechercher pour filtrer les éléments affichés pour qu’ils correspondent au nom de la ressource.

  ![Utilisez les filtres et le champ de recherche pour localiser la ressource](./assets/content-select-assets-dialog-aem-filter.png){width="700" zoomable="yes"}

<!-- 
## Upload assets

To import files to Assets as a Cloud Service, you first need to browse or create the folder to be used for storage. You can then import an asset and add it to your email content. After assets are uploaded, you can [use the image assets as you author content](./assets-overview.md#add-assets-to-your-content).

1. While authoring your content in the email designer, drag an image element into the canvas. 

   The properties on the right reflect the image element selection. 

1. Click **[!UICONTROL Import media]** to open the _[!UICONTROL Upload image]_ dialog.

1. If your file system is open to your image file, drag and drop the file on the box in the dialog.

   ![Upload image file to Assets repository](./assets/email-designer-image-upload.png){width="700" zoomable="yes"}

   You can also click the **[!UICONTROL Select a file from your computer]** link and use your file system to locate and select the image file. Click Open and the image file is displayed in the box.

1. Click **[!UICONTROL Import]**.

-->