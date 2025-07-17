---
title: Création de modèles d’e-mail
description: Découvrez comment créer des modèles d’e-mail de contenu qui peuvent être utilisés pour les e-mails de parcours de compte afin de réutiliser vos conceptions facilement et efficacement.
feature: Templates, Email Authoring, Content
role: User
exl-id: 2d532f93-c452-400a-8a82-e1f0eb89b199
source-git-commit: 9b053f81e3074f03740fe1f3b69f632219ad269a
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 14%

---

# Création de modèle d’e-mail

Après avoir [créé un modèle d’e-mail](./email-templates.md#create-an-email-template), utilisez l’espace de conception visuelle pour créer les composants de structure et de contenu dans votre modèle d’e-mail.

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

### Ajouter un CSS personnalisé

Vous pouvez ajouter votre propre CSS personnalisé directement dans l’espace de conception de modèle d’e-mail. Utilisez le CSS personnalisé pour appliquer un style avancé et spécifique, pour une plus grande flexibilité et un meilleur contrôle de l’aspect de votre contenu. Il est recommandé d’ajouter ce style de niveau supérieur avant d’inclure des composants tels que des images, des boutons et du texte.

Avec au moins un composant de contenu dans la zone de travail, sélectionnez le composant **[!UICONTROL Corps]** dans l’arborescence de navigation de gauche pour accéder à l’éditeur CSS personnalisé.

![Accès aux styles de corps](./assets/email-template-body-styles.png){width="800" zoomable="yes"}

{{$include /help/_includes/content-design-custom-css.md}}

### Ajouter des fragments

{{$include /help/_includes/content-design-use-fragments.md}}

Une fois le modèle enregistré, il s’affiche dans la page des détails du fragment lorsque vous sélectionnez l’onglet _[!UICONTROL Utilisé par]_ dans le résumé.

### Ajout de ressources

{{$include /help/_includes/content-design-assets.md}}

### Parcourir les calques, paramètres et styles

{{$include /help/_includes/content-design-navigation.md}}

### Personnaliser le contenu

{{$include /help/_includes/content-design-personalization-email.md}}

### Modifier le tracking des URL liées

{{$include /help/_includes/content-design-links.md}}

## Afficher les options

Tirez parti des options d’affichage et de validation du contenu disponibles dans l’espace de conception visuelle.

* Effectuez un zoom avant/arrière sur le contenu dans les options de zoom prédéfinies.

* Basculez vers l’affichage du contenu sur les ordinateurs de bureau, les appareils mobiles ou en texte seul/texte brut.
   * Cliquez sur l’icône _Œil_ pour afficher un aperçu du contenu sur tous les appareils.
   * Sélectionnez l’un des appareils prêts à l’emploi ou saisissez des dimensions personnalisées pour prévisualiser le contenu.

### Plus d’options

Dans le menu _[!UICONTROL Plus...]_ situé en haut de l’espace de conception des e-mails, vous pouvez effectuer les actions suivantes :

![Cliquez sur Plus pour accéder aux actions du modèle](./assets/visual-designer-more-menu.png){width="500"}

* **[!UICONTROL Réinitialiser le modèle]** - Cliquez sur cette option pour vider la zone de travail de conception et redémarrer la création de contenu.
* **[!UICONTROL Enregistrer en tant que fragment]** - Enregistrez la totalité ou une partie du modèle en tant que fragment à réutiliser dans plusieurs e-mails ou modèles d’e-mail. Indiquez un nom et une description pour le fragment et enregistrez-le dans la liste des fragments disponibles.
* **[!UICONTROL Modifier votre conception]** - Revenez à la page _Concevoir votre modèle_. À partir de là, vous pouvez choisir de concevoir votre modèle à partir de zéro ou utiliser un modèle existant pour redémarrer le processus de conception.
* **[!UICONTROL Exporter HTML]** - Téléchargez le contenu de la zone de travail visuelle sur votre système local au format HTML présenté sous la forme d’un fichier zip.
