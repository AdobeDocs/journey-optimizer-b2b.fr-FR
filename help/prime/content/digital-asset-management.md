---
title: Ressources
description: Gérez les ressources d’images à partir de Journey Optimizer B2B edition pour les e-mails, les modèles et les fragments visuels.
feature: Assets, Content
role: User
badge: label="Beta" type="Informative"
autotag-review: '2026-06-18T20:11:57.611Z'
TQID: 'https://experienceleague.adobe.com/Xsl4zqpk4xqXuOS85Z5U08tnbv8GWm3FXdqsegPCBI4'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e666e996-b2cf-4c45-8fc2-1c625212ababid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: c8402946-ff35-44c5-ab98-74c1bba0975fid: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 0e90250101eef0572af0382cc7d24bca727d2b75
workflow-type: tm+mt
source-wordcount: 495
ht-degree: 3%

---

# Ressources

Dans [!DNL Adobe Journey Optimizer B2B Prime], les ressources sont généralement les images utilisées lors de la conception de contenu pour prendre en charge les parcours. Vous pouvez utiliser ces images dans vos e-mails, modèles d’e-mail et fragments visuels à partir du sélecteur de ressources ou une simple interface glisser-déposer dans l’espace de conception visuelle.

Formats de fichiers pris en charge : JPG, JPEG, GIF, PNG, EPS, SVG et RGB


>>
L’importation de ressources à partir de systèmes externes tels que la gestion des ressources numériques Marketo Engage et l’accès à une bibliothèque de ressources préremplie ne sont pas encore disponibles. Les prochaines versions devraient inclure l’importation de ressources à partir des systèmes existants, la prise en charge de dossiers et des fonctionnalités étendues de gestion des ressources.

<!-- You can [edit these assets using Adobe Express](./image-edit-adobe-express.md), and move them into folders to organize them for use across your emails, templates, and fragments. -->

La bibliothèque **** permet d’accéder au référentiel centralisé pour stocker et gérer les images et d’autres ressources de création. Il comprend des fonctionnalités optimisées par l’IA qui génèrent automatiquement des métadonnées et permettent la recherche en langage naturel.

Dans le volet de navigation de gauche, développez **[!UICONTROL Gestion de contenu]** et sélectionnez **[!UICONTROL Assets]**.

>[!NOTE]
>
>Dans cette version de Beta, vous pouvez choisir des images et des ressources à partir d’une copie unique de votre bibliothèque de ressources Marketo Engage directement dans la zone de travail d’e-mail. Vous pouvez également charger des ressources d’image supplémentaires à partir de la bibliothèque __ ou de l’espace de conception de contenu. Ces ressources chargées ne peuvent être utilisées que dans l’instance [!DNL Adobe Journey Optimizer B2B Prime].

![Bibliothèque ](./assets/dam-asset-library-list-view.png){width="800" zoomable="yes"}

>[!BEGINSHADEBOX]

La première fois que vous accédez à la bibliothèque __, consultez les _[!UICONTROL Conditions d’utilisation de Generative AI]_ et cliquez sur **[!UICONTROL Accepter et continuer]**.

![Bibliothèque ](./assets/dam-asset-library-gen-ai-agree.png){width="500"}

>[!ENDSHADEBOX]

La bibliothèque prend en charge deux options de disposition :

* **[!UICONTROL Liste]** — Cliquez sur l’icône _Vue Liste_ ( ![Icône de vue Liste](../../assets/do-not-localize/icon-falco-list-view.svg) ) pour afficher les ressources dans un tableau triable avec des colonnes de métadonnées.
* **[!UICONTROL Galerie]** — Cliquez sur l’icône _Galerie_ ( ![icône de la vue Galerie](../../assets/do-not-localize/icon-falco-gallery-view.svg) ) pour afficher les ressources sous forme de grille miniature visuelle.

## Recherche de ressources {#find-assets}

Utilisez le champ _[!UICONTROL Rechercher]_ pour rechercher des ressources en décrivant ce dont vous avez besoin en langage naturel. Les résultats de la recherche sont basés sur les métadonnées générées par l’IA. Vous n’êtes donc pas limité à la recherche par nom de fichier.

**Exemples :**

* `team members`
* `nature`
* `exercise`

![Image sélectionnée dans les résultats de recherche de la bibliothèque Assets](./assets/dam-asset-library-select-image.png){width="700" zoomable="yes"}

## Affichage des détails de la ressource {#view-details}

Sélectionnez une ressource pour ouvrir sa vue détaillée. La vue détaillée affiche une description générée par l’IA, des balises et des mots-clés, ainsi que des champs de métadonnées supplémentaires. Ces informations sont générées automatiquement lorsque la ressource est chargée.

Sélectionnez une ressource dans la vue Liste ou Galerie pour ouvrir sa vue détaillée à droite. Sélectionnez l’onglet Métadonnées d’IA pour afficher la description, les balises et les métadonnées générées par l’IA.

![Image sélectionnée dans les résultats de recherche de la bibliothèque Assets](./assets/dam-asset-library-select-image-metadata.png){width="700" zoomable="yes"}

## Chargement d’un élément {#upload}

1. Cliquez sur **[!UICONTROL Charger]** en haut à droite.

1. Dans la boîte de dialogue, effectuez un glisser-déposer d’un fichier de votre système local.

   ![Charger une ressource image](./assets/dam-upload-assets-dialog.png){width="450"}

   Vous pouvez également cliquer sur **[!UICONTROL Sélectionner un fichier sur votre ordinateur]** afin d’utiliser votre système de fichiers local pour localiser et sélectionner le fichier.

1. Cliquez sur **[!UICONTROL Télécharger le fichier]** pour confirmer et télécharger le fichier dans le référentiel.

Une fois le chargement terminé, le système génère automatiquement une description, attribue des balises et des mots-clés et extrait les attributs visuels tels que l’objet et le paramètre. Aucun balisage manuel n’est requis. La nouvelle image affiche un statut _[!UICONTROL TRAITEMENT]_ jusqu’à ce que ce processus soit terminé.

![Nouvelle ressource image au statut de traitement](./assets/dam-asset-library-upload-processing.png){width="700" zoomable="yes"}
<!-- -->
