---
title: Création d'un e-mail
description: Découvrez comment créer du contenu d’e-mail dans Adobe Journey Optimizer B2B. Utilisez des modèles, des importations HTML et des outils optimisés par l’IA pour personnaliser et optimiser vos communications par e-mail.
feature: Email Authoring, Content Design Tools
role: User
exl-id: 0f4ae644-ade7-49a0-935c-7f4779c25ffb
source-git-commit: 633f23525a6fd2b03460ecbef17379077d6b51d2
workflow-type: tm+mt
source-wordcount: '928'
ht-degree: 20%

---

# Création d’un e-mail

Après avoir [ajouté une nouvelle ressource e-mail<!-- or duplicated --> à un nœud d’action de parcours ](./add-email.md), vous pouvez définir le contenu de l’e-mail.

Cliquez sur **[!UICONTROL Modifier le contenu de l’e-mail]** dans l’onglet _[!UICONTROL Détails]_ du panneau de droite.

![Cliquez sur Modifier le contenu de l’e-mail ](./assets/add-email-content.png){width="700" zoomable="yes"}

Cette action lance les outils de conception d’e-mail, dans lesquels vous pouvez choisir la manière de concevoir votre e-mail à l’aide des options suivantes :

* [Concevez entièrement votre e-mail](#design-your-email-from-scratch) à l’aide de l’interface Email Designer.

* [Importez du contenu HTML existant](#import-existing-html-content) à partir d’un fichier ou d’un dossier .zip.

* [Sélectionnez un modèle existant](#select-a-template) dans une liste de modèles d’e-mail intégrés ou personnalisés.

Après avoir créé et personnalisé le contenu de l’e-mail, vous pouvez exporter le contenu pour le valider ou pour l’utiliser ultérieurement. Cliquez sur **[!UICONTROL Exporter HTML]** pour enregistrer le contenu sous la forme d’un fichier .zip contenant votre HTML et vos ressources.

>[!TIP]
>
>Utilisez l’assistant d’IA dans Adobe Journey Optimizer B2B edition, optimisé par l’IA générative pour élever votre contenu au niveau supérieur. L’assistant AI peut vous aider à optimiser l’impact de vos diffusions en générant des e-mails complets, du contenu textuel ciblé et en obtenant des recommandations de l’assistant AI pour les images qui résonnent avec votre audience. [En savoir plus](./ai-assistant-emails.md)

## Concevoir votre e-mail à partir de zéro {#design-from-scratch}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_landing_page"
>title="Ajout de composants de structure"
>abstract="Les composants de structure définissent la disposition de la page de destination. Faites glisser et déposez un composant de **structure** dans la zone de travail pour commencer à concevoir le contenu de votre page de destination."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_landing_page"
>title="À propos des composants de contenu"
>abstract="Les composants de contenu sont des espaces réservés de contenu vides que vous pouvez utiliser pour créer la disposition d’une page de destination."

Utilisez l’espace de conception visuelle du contenu pour définir la structure et le contenu de l’e-mail. En ajoutant et en déplaçant des composants structurels à l’aide de simples actions de glisser-déposer, vous pouvez concevoir la forme du contenu d’e-mail réutilisable en quelques secondes.

1. Sur la page d’accueil _[!UICONTROL Concevez votre modèle]_, sélectionnez l’option **[!UICONTROL Créer en partant de zéro]**.
1. [Ajoutez la structure et le contenu](#add-structure-and-content) à l’e-mail.
1. [Ajoutez des ressources d’image](#add-assets) à l’e-mail.
1. [Personnaliser le contenu de l’e-mail](#personalize-content).
1. [Vérifier et mettre à jour les liens](#preview-and-edit-linked-urls).

<!-- If needed, you can further personalize your email by clicking **[!UICONTROL Switch to code editor]** from the advanced menu. The code editor allows you to edit the email source code, such as adding tracking or custom HTML tags.

>[!CAUTION]
>
>You cannot revert back to the visual designer for this email after switching to the code editor. -->

Une fois votre contenu terminé, cliquez sur **[!UICONTROL Simuler du contenu]** en haut pour vérifier le rendu. Vous pouvez choisir la vue bureau ou la vue mobile.

Lorsque le contenu vous convient, cliquez sur **[!UICONTROL Enregistrer]**.

## Importer du contenu HTML existant

{{$include /help/_includes/content-design-import.md}}

![importer du contenu html dans un fichier zip](./assets/email-import-zip-file.png){width="500"}

>[!NOTE]
>
>L’utilisation d’une balise `<table>` comme première couche d’un fichier HTML peut entraîner une perte de style, y compris les paramètres d’arrière-plan et de largeur dans la balise de couche supérieure.

Vous pouvez personnaliser le contenu importé selon vos besoins à l’aide des outils de l’éditeur visuel d’e-mail.

## Sélectionner un modèle

{{$include /help/_includes/content-design-select-template.md}}

>[!NOTE]
>
> Les modèles enregistrés peuvent avoir des paramètres de gouvernance (verrouillage de contenu) appliqués à un ou plusieurs composants. Le concepteur visuel fournit des instructions sur les composants verrouillés lorsque vous [créez un email à partir d’un modèle régi](./email-authoring-governance.md).

## Ajouter la structure et le contenu {#structure-content}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_email"
>title="Ajout de composants de structure"
>abstract="Les composants de structure définissent la disposition de votre e-mail. Faites glisser et déposez un composant de **structure** dans la zone de travail pour commencer à concevoir le contenu de votre e-mail."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_email"
>title="À propos des composants de contenu"
>abstract="Les composants de contenu sont des espaces réservés de contenu vides que vous pouvez utiliser pour créer la disposition d’un e-mail."

{{$include /help/_includes/content-design-components.md}}

### Ajouter des fragments

{{$include /help/_includes/content-design-use-fragments.md}}

Une fois l’e-mail enregistré, il s’affiche dans la page des détails du fragment lorsque vous sélectionnez l’onglet _[!UICONTROL Utilisé par]_ dans le résumé.

### Ajout de ressources

{{$include /help/_includes/content-design-assets.md}}

### Parcourir les calques, paramètres et styles

{{$include /help/_includes/content-design-navigation.md}}

### Personnaliser le contenu

{{$include /help/_includes/content-design-personalization.md}}

>[!NOTE]
>
>Si _[!UICONTROL Mes jetons]_ sont définis pour le parcours de compte, vous pouvez également utiliser ces jetons spécifiques au parcours pour le contenu de votre e-mail. Voir [Jetons personnalisés pour la personnalisation des e-mails](./personalization-my-tokens.md) pour plus d’informations.

### Modifier le tracking des URL liées

{{$include /help/_includes/content-design-links.md}}

### Afficher les options

Tirez parti des options d’affichage et de validation du contenu disponibles dans l’éditeur visuel d’e-mail.

* Effectuez un zoom avant/arrière sur le contenu dans les options de zoom prédéfinies.

* Basculez vers l’affichage du contenu sur les ordinateurs de bureau, les appareils mobiles ou en texte seul/texte brut.
   * Cliquez sur l’icône _Affichage_ pour afficher un aperçu du contenu sur tous les appareils.
   * Sélectionnez l’un des appareils prêts à l’emploi ou saisissez des dimensions personnalisées pour prévisualiser le contenu.

### Plus d’options

Dans le menu _[!UICONTROL Plus...]_ situé en haut de l’espace de conception des e-mails, vous pouvez effectuer les actions suivantes :

![Cliquez sur Plus pour accéder aux actions du modèle](./assets/email-designer-more-menu.png){width="500"}

* **[!UICONTROL Réinitialiser l’e-mail]** - Cliquez sur cette option pour vider la zone de travail du Concepteur d’e-mail visuel et redémarrer la création de votre contenu.
* **[!UICONTROL Enregistrer en tant que fragment]** - Enregistrez l’intégralité ou une partie de l’e-mail en tant que fragment à réutiliser dans plusieurs e-mails ou modèles d’e-mail. Indiquez un nom et une description pour le fragment et enregistrez-le dans la liste des fragments disponibles.
* **[!UICONTROL Modifier votre conception]** - Revenez à la page _Concevoir votre e-mail_. De là, vous pouvez choisir un autre modèle pour redémarrer le processus de conception ou choisir de concevoir le contenu à partir de zéro dans une zone de travail noire.
* **[!UICONTROL Enregistrer en tant que modèle de contenu]** - Enregistrez le corps de l’e-mail en tant que modèle d’e-mail à réutiliser dans plusieurs e-mails ou modèles d’e-mail. Indiquez un nom et une description pour le modèle, puis enregistrez-le dans la liste des modèles d’e-mail enregistrés.
* **[!UICONTROL Exporter HTML]** - Téléchargez le contenu de la zone de travail visuelle sur votre système local au format HTML présenté sous la forme d’un fichier zip.

## Vérifier et tester l’e-mail {#preview-test}

>[!CONTEXTUALHELP]
>id="ajo-b2b_email_preview_simulate"
>title="Vérifier le rendu de votre contenu"
>abstract="Une fois votre contenu défini, vous pouvez le prévisualiser et vérifier si le rendu est correct en fonction du canal que vous utilisez."

Lorsque le contenu de votre message est défini, vous pouvez utiliser des profils de test pour le prévisualiser, envoyer des BAT et contrôler son rendu sur les clients de bureau, mobiles et web les plus courants. Si vous avez inséré du contenu personnalisé, vous pouvez prévisualiser l’affichage de celui-ci dans le message à l’aide des données de profil de test.

Pour prévisualiser le contenu de l’e-mail, cliquez sur **[!UICONTROL Simuler du contenu]** puis ajoutez un profil de test pour vérifier votre message à l’aide des données de profil de test.

![Simuler le contenu de l’e-mail pour vérifier votre conception](./assets/email-designer-simulate-content.png){width="700" zoomable="yes"}
