---
title: Création de contenu - Ajout de formulaires
description: Section réutilisée sur l’ajout de formulaires dans les landing pages et les modèles
source-git-commit: 97d8e5b366e8786e517c18828236f95304f3f3be
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 0%

---

# Création de contenu - Ajout de formulaires

Un formulaire est un composant réutilisable pouvant être référencé par plusieurs pages de destination et modèles de page de destination dans Adobe Journey Optimizer B2B edition. Il s’agit d’un bloc de champs et d’un bouton d’envoi qui peuvent être précréés et rapidement insérés pour accélérer la conception des pages et la rendre plus cohérente.

L’exemple suivant décrit les étapes à suivre pour ajouter un formulaire lors de la conception de votre page.

1. Sous la section **[!UICONTROL Contenu]**, faites glisser l’élément **[!UICONTROL Formulaire]** et déposez-le dans un composant structurel de l’espace de conception de page.

   ![Faites glisser un composant Formulaire dans l’espace de conception visuelle](../assets/content-design-shared/content-design-add-form.png){width="600"}

   >[!TIP]
   >
   >Pour ajouter le formulaire de sorte qu’il occupe toute la disposition horizontale dans l’e-mail, ajoutez une structure de colonnes 1:1, puis faites-y glisser le formulaire et déposez-le.

1. Cliquez sur l’icône _Formulaire_ dans la barre d’outils du composant ou utilisez les propriétés **[!UICONTROL Incorporer le formulaire]** à droite pour sélectionner le formulaire publié.

   ![Sélectionnez le formulaire publié](../assets/content-design-shared/content-design-add-form-properties.png){width="600"}

1. Si vous souhaitez remplacer le **[!UICONTROL type de suivi]** par défaut pour le formulaire, modifiez le paramètre en fonction des exigences de la page ou du modèle.

   Il s’agit également de la page _Merci_ pour le formulaire. Ce paramètre détermine ce qui se passe lorsqu’un visiteur envoie le formulaire :

   * **[!UICONTROL Rester sur la page]** - Sélectionnez cette option pour que le visiteur reste sur la même page lors de l’envoi du formulaire.

   * **[!UICONTROL Page de destination]** - Sélectionnez cette option pour sélectionner n’importe quelle page de destination Journey Optimizer B2B edition ou Marketo Engage comme suite.

   * **[!UICONTROL URL externe]** - Sélectionnez cette option pour spécifier n’importe quelle URL comme page de suivi. Une fois que le visiteur a envoyé le formulaire, le navigateur charge l’URL désignée.

     >[!TIP]
     >
     >Si vous souhaitez utiliser le formulaire pour télécharger un fichier, vous pouvez spécifier une URL pour le fichier hébergé. Avec cette configuration, le bouton d’envoi fonctionne comme un bouton de téléchargement.

   ![Modifier le paramètre de relance](../assets/content-design-shared/content-design-add-form-follow-up.png){width="280"}

1. Si vous souhaitez limiter l’affichage du formulaire par type d’appareil, modifiez le paramètre **[!UICONTROL Options d’affichage]** :

   * **[!UICONTROL Afficher uniquement sur les ordinateurs de bureau]**
   * **[!UICONTROL Afficher uniquement sur les appareils mobiles]**
   * **[!UICONTROL Afficher sur tous les appareils]** (par défaut)

1. Si nécessaire, sélectionnez l’onglet **[!UICONTROL Styles]** dans le panneau de droite pour définir les marges du formulaire dans la page.
