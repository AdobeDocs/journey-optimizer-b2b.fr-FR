---
title: Création de modèles de courrier électronique
description: Découvrez comment créer des modèles d’email de contenu qui peuvent être utilisés pour les emails de parcours de compte afin de réutiliser vos conceptions facilement et efficacement.
feature: Email Authoring, Content
source-git-commit: 8315c760e573aa36819652798a400206e6268ccc
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 11%

---

# Création de modèles d&#39;email

Après avoir [créé un modèle d’email](./email-templates.md#create-an-email-template), utilisez le concepteur visuel pour créer les composants structurels et de contenu dans votre modèle d’email.

## Ajouter la structure et le contenu {#structure-content}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_template"
>title="Ajout de composants de structure"
>abstract="Les composants de structure définissent la disposition du modèle. Faites glisser et déposez un composant de **structure** dans la zone de travail pour commencer à concevoir le contenu de votre modèle."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_template"
>title="À propos des composants de contenu"
>abstract="Les composants de contenu sont des espaces réservés de contenu vides que vous pouvez utiliser pour créer la disposition d’un modèle."

{{$include /help/_includes/content-design-components.md}}

### Ajouter des fragments

Dans l’éditeur visuel de contenu, l’icône _Fragments_ s’affiche sur la gauche. L’exemple suivant décrit les étapes à suivre pour ajouter des fragments au contenu du modèle.

1. Pour ouvrir la liste des fragments, sélectionnez l’icône _Fragments_ ( ![Icône Fragments](../assets/do-not-localize/icon-fragments.svg) ).

   Vous pouvez effectuer les actions suivantes :

   * Triez la liste.
   * Parcourir, rechercher ou filtrer la liste.
   * Basculez entre les modes Miniature et Liste.
   * Actualisez la liste pour refléter les fragments récemment créés.

   ![Sélectionner un fragment dans la liste](./assets/visual-designer-fragments.png){width="700" zoomable="yes"}

1. Faites glisser et déposez l’un des fragments dans l’espace réservé du composant structurel.

   L’éditeur effectue le rendu du fragment dans la section/l’élément de la structure de l’email.

Le contenu du fragment est mis à jour dynamiquement dans la structure afin d’afficher la manière dont le contenu apparaît dans l’email.

>[!TIP]
>
>Si vous souhaitez que le fragment occupe toute la mise en page horizontale dans l&#39;email, ajoutez une structure de colonne 1:1, puis faites glisser et déposez le fragment dans celle-ci.

Une fois l’email enregistré, il apparaît dans la page des détails du fragment lorsque vous sélectionnez l’onglet _[!UICONTROL Utilisé par]_ dans le résumé. Les fragments ajoutés à un modèle d’email ne sont pas modifiables dans le modèle : le fragment source définit le contenu.

### Ajout de ressources

{{$include /help/_includes/content-design-assets.md}}

### Navigation dans les calques, paramètres et styles

{{$include /help/_includes/content-design-navigation.md}}

### Personnaliser le contenu

{{$include /help/_includes/content-design-personalization.md}}

### Modification du suivi des URL liées

{{$include /help/_includes/content-design-links.md}}

## Options d’affichage

Tirez parti des options de vue et de validation du contenu disponibles dans le concepteur visuel.

* Zoom avant/arrière sur le contenu sur les options de zoom prédéfinies.

* Basculez l’affichage du contenu sur Bureau, Mobile ou Texte unique/Texte brut.
   * Cliquez sur l’icône _OEil_ pour afficher l’aperçu du contenu sur tous les appareils.
   * Sélectionnez l’un des appareils prêts à l’emploi ou saisissez des dimensions personnalisées pour prévisualiser le contenu.

### Plus d’options

Dans le menu _[!UICONTROL Plus...]_ situé en haut du Concepteur d&#39;email, vous pouvez effectuer les actions suivantes :

![Cliquez sur Plus pour accéder aux actions de modèle](./assets/visual-designer-more-menu.png){width="500"}

* **[!UICONTROL Réinitialiser le modèle]** - Cliquez sur cette option pour effacer le canevas du concepteur visuel sur une barre d’outils vide et redémarrer le contenu de création.
* **[!UICONTROL Enregistrer en tant que fragment]** - Enregistrez toutes ou parties du modèle en tant que fragment à réutiliser dans plusieurs emails ou modèles de courrier électronique. Vous fournissez un nom et une description pour le fragment et vous l’enregistrez dans la liste des fragments disponibles.
* **[!UICONTROL Modifiez votre conception]** - Revenez à la page _Concevez votre modèle_. À partir de là, vous pouvez choisir de entièrement concevoir votre modèle ou d’utiliser un modèle existant pour redémarrer le processus de conception.
* **[!UICONTROL Exporter l’HTML]** - Téléchargez le contenu dans la zone de travail visuelle vers votre système local au format d’HTML présenté sous la forme d’un fichier zip.
