---
title: Création d'un e-mail
description: Créez des e-mails avec des outils de conception visuelle, l’importation d’HTML ou des modèles. Utilisez la génération de contenu de l’assistant AI, le code CSS personnalisé et la personnalisation dans Journey Optimizer B2B edition.
feature: Email Authoring, Content Design Tools
role: User
exl-id: 0f4ae644-ade7-49a0-935c-7f4779c25ffb
source-git-commit: 9f8953423e3b6d578155431c7638e4fec9abf86a
workflow-type: tm+mt
source-wordcount: '1163'
ht-degree: 6%

---

# Création d’un e-mail

Après avoir [ajouté une ressource e-mail à un nœud d’action de parcours &#x200B;](./add-email.md), vous pouvez définir le contenu de l’e-mail.

Cliquez sur **[!UICONTROL Modifier le contenu de l’e-mail]** dans l’onglet _[!UICONTROL Détails]_ du panneau de droite.

![Cliquez sur Modifier le contenu de l’e-mail &#x200B;](./assets/add-email-content.png){width="700" zoomable="yes"}

Cette action lance les outils de conception d’e-mail, dans lesquels vous pouvez choisir la manière de concevoir votre e-mail à l’aide des options suivantes :

* [Concevez entièrement votre e-mail](#design-your-email-from-scratch) à l’aide de l’interface Email Designer.

* [Importez du contenu HTML existant](#import-existing-html-content) à partir d’un fichier ou d’un dossier .zip.

* [Sélectionnez un modèle existant](#select-a-template) dans une liste de modèles d’e-mail intégrés ou personnalisés.

Après avoir créé et personnalisé le contenu de l’e-mail, vous pouvez exporter le contenu pour le valider ou pour l’utiliser ultérieurement. Cliquez sur **[!UICONTROL Exporter HTML]** pour enregistrer le contenu sous la forme d’un fichier .zip contenant votre HTML et vos ressources.

>[!TIP]
>
>Utilisez l’assistant d’IA dans Adobe Journey Optimizer B2B edition, optimisé par l’IA générative pour élever votre contenu au niveau supérieur. L’assistant AI peut vous aider à optimiser l’impact de vos diffusions en générant des e-mails complets, du contenu textuel ciblé et en obtenant des recommandations de l’assistant AI pour les images qui résonnent avec votre audience. [En savoir plus](./ai-assistant-emails.md)

## Concevoir votre e-mail à partir de zéro {#design-from-scratch}

Utilisez l’espace de conception visuelle du contenu pour définir la structure et le contenu de l’e-mail. En ajoutant et en déplaçant des composants structurels à l’aide de simples actions de glisser-déposer, vous pouvez concevoir la forme du contenu d’e-mail réutilisable en quelques secondes.

1. Sur la page d’accueil _[!UICONTROL Concevez votre modèle]_, sélectionnez l’option **[!UICONTROL Créer en partant de zéro]**.

1. Dans la boîte de dialogue _[!UICONTROL Créer un e-mail]_, choisissez le type de contenu d’e-mail que vous souhaitez créer.

   * **[!UICONTROL Utiliser les thèmes]** - Sélectionnez cette option pour créer l’e-mail en _mode thème_. Dans ce mode, vous pouvez utiliser un thème de marque défini pour rationaliser le processus de création de contenu et vous assurer que la conception s’aligne sur les normes définies.

   * **[!UICONTROL Style manuel]** - Sélectionnez cette option pour créer l’e-mail en _mode manuel_. Dans ce mode, vous définissez manuellement la mise en forme de tous les composants de structure et de contenu que vous ajoutez à la zone de travail vierge.

1. [Ajoutez la structure et le contenu](./email-authoring.md#add-structure-and-content) au modèle.

1. [Vérifier et mettre à jour les liens](#preview-and-edit-linked-urls).

1. [Tester l’e-mail](#check-and-test-the-email).

<!-- If needed, you can further personalize your email by clicking **[!UICONTROL Switch to code editor]** from the advanced menu. The code editor allows you to edit the email source code, such as adding tracking or custom HTML tags.

>[!CAUTION]
>
>You cannot revert back to the visual design space for this email after switching to the code editor. -->

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
> Les modèles enregistrés peuvent avoir des paramètres de gouvernance (verrouillage de contenu) appliqués à un ou plusieurs composants. L’espace de conception visuelle fournit des instructions sur les composants verrouillés lorsque vous [créez un e-mail à partir d’un modèle régi](./email-authoring-governance.md).

## Ajouter la structure et le contenu {#structure-content}

{{$include /help/_includes/content-design-components.md}}

### Ajouter un CSS personnalisé

Vous pouvez ajouter votre propre CSS personnalisé directement dans l’espace de conception d’e-mail. Utilisez le CSS personnalisé pour appliquer un style avancé et spécifique, pour une plus grande flexibilité et un meilleur contrôle de l’aspect de votre contenu. Il est recommandé d’ajouter ce style de plus haut niveau avant d’inclure des composants de contenu, tels que des images, des boutons et du texte.

Avec au moins un composant de contenu dans la zone de travail, sélectionnez le composant **[!UICONTROL Corps]** dans l’arborescence de navigation de gauche pour accéder à l’éditeur CSS personnalisé.

>[!NOTE]
>
>Si votre e-mail est conçu à l’aide d’un [modèle avec du contenu verrouillé](./template-content-governance.md), vous ne pouvez pas ajouter de code CSS personnalisé à votre contenu. Le libellé du bouton se transforme en **[!UICONTROL Afficher le CSS personnalisé]** et tout CSS personnalisé déjà présent dans le contenu est en lecture seule.

![Accès aux styles de corps](./assets/email-body-styles.png){width="800" zoomable="yes"}

{{$include /help/_includes/content-design-custom-css.md}}

### Ajouter des fragments

>[!NOTE]
>
>Les fragments ne sont pas compatibles entre le _mode Thème_ et le _mode Manuel_ dans le contenu de l’e-mail. Pour utiliser un fragment dans le contenu d’e-mail auquel un thème est appliqué, le fragment doit également être créé en _mode Thème_.

{{$include /help/_includes/content-design-use-fragments.md}}

Une fois l’e-mail enregistré, il s’affiche dans la page des détails du fragment lorsque vous sélectionnez l’onglet _[!UICONTROL Utilisé par]_ dans le résumé.

### Ajout de ressources d’image

{{$include /help/_includes/content-design-assets.md}}

### Parcourir les calques, paramètres et styles

{{$include /help/_includes/content-design-navigation.md}}

### Personnaliser le contenu

{{$include /help/_includes/content-design-personalization-email.md}}

>[!NOTE]
>
>Si _[!UICONTROL Mes jetons]_ sont définis pour le parcours de compte, vous pouvez également utiliser ces jetons spécifiques au parcours pour le contenu de votre e-mail. Voir [Jetons personnalisés pour la personnalisation des e-mails](./personalization-my-tokens.md) pour plus d’informations.

### Modifier le tracking des URL liées

{{$include /help/_includes/content-design-links.md}}

### Appliquer le style du mode sombre

Utilisez le _mode sombre_ pour vérifier l’affichage de votre e-mail en fonction d’un thème sombre dans un client de messagerie. Un mode ou un thème sombre permet à un client de messagerie ou à une application de support d’afficher les e-mails avec des arrière-plans plus sombres et des couleurs plus claires pour le texte, les boutons et d’autres éléments visuels. Dans la partie supérieure droite de la zone de travail de conception, définissez le sélecteur sur _Mode sombre_ (![icône Mode sombre](../assets/do-not-localize/icon-content-dark-mode.svg) ). Ensuite, prévisualisez et définissez les paramètres personnalisés spécifiques utilisés pour l’affichage par les clients de messagerie de support lorsque leur thème sombre est activé.

![Zone de travail de conception des e-mails affichant le sélecteur en mode sombre et le contenu des e-mails affiché en mode sombre](./assets/email-color-mode-dark-selector.png){width="700" zoomable="yes"}

Pour plus d’informations sur le style du mode sombre et les bonnes pratiques, voir [Mode sombre pour le contenu des e-mails](./email-dark-mode.md).

### Afficher les options

Tirez parti des options d’affichage et de validation du contenu disponibles dans l’éditeur visuel d’e-mail.

* Effectuez un zoom avant/arrière sur le contenu dans les options de zoom prédéfinies.

* Basculez vers l’affichage du contenu sur les ordinateurs de bureau, les appareils mobiles ou en texte seul/texte brut.
   * Cliquez sur l’icône _Affichage_ pour afficher un aperçu du contenu sur tous les appareils.
   * Sélectionnez l’un des appareils prêts à l’emploi ou saisissez des dimensions personnalisées pour prévisualiser le contenu.

## Plus d’options

Dans le menu _[!UICONTROL Plus...]_ situé en haut de l’espace de conception visuelle, vous pouvez effectuer les actions suivantes :

![Cliquez sur Plus pour accéder aux actions du modèle](./assets/email-designer-more-menu.png){width="500"}

* **[!UICONTROL Réinitialiser l’e-mail]** - Cliquez sur cette option pour vider la zone de travail de conception d’e-mail et redémarrer la création de votre contenu.
* **[!UICONTROL Enregistrer en tant que fragment]** - Enregistrez l’intégralité ou une partie de l’e-mail en tant que fragment à réutiliser dans plusieurs e-mails ou modèles d’e-mail. Indiquez un nom et une description pour le fragment et enregistrez-le dans la liste des fragments disponibles.
* **[!UICONTROL Modifier votre conception]** - Revenez à la page _Concevoir votre e-mail_. De là, vous pouvez choisir un autre modèle pour redémarrer le processus de conception. Vous pouvez également choisir de concevoir le contenu à partir de zéro avec une zone de travail vierge (_mode classique_) ou à l’aide d’un [thème de marque](./brand-themes.md) (_mode thème_).
* **[!UICONTROL Enregistrer en tant que modèle de contenu]** - Enregistrez le corps de l’e-mail en tant que modèle d’e-mail à réutiliser dans plusieurs e-mails ou modèles d’e-mail. Indiquez un nom et une description pour le modèle, puis enregistrez-le dans la liste des modèles d’e-mail enregistrés.
* **[!UICONTROL Exporter HTML]** - Téléchargez le contenu de la zone de travail visuelle sur votre système local au format HTML présenté sous la forme d’un fichier zip.

## Vérifier et tester l’e-mail {#email-testing}

Lorsque le contenu de votre message est défini, vous pouvez utiliser des profils de test pour le prévisualiser, envoyer des BAT et vérifier son rendu dans les proportions pour ordinateurs de bureau et appareils mobiles. Si vous avez inséré du contenu personnalisé, vous pouvez prévisualiser l’affichage de celui-ci dans le message à l’aide des données de profil de test.

Pour [prévisualiser le contenu de l’e-mail](./email-simulate-content.md), cliquez sur **[!UICONTROL Simuler du contenu]** et sélectionnez un profil de test afin de vérifier votre message à l’aide des données de profil de personne.

![Simuler le contenu de l’e-mail pour vérifier votre conception](./assets/email-designer-simulate-content.png){width="700" zoomable="yes"}

Vous pouvez accéder à des outils supplémentaires pour valider et réviser le contenu de l’e-mail :

* [Envoyer un BAT](./email-simulate-content.md#send-proofs)
* [Test du rendu dans les clients de messagerie](./email-test-rendering.md)
<!-- * Generate a spam report -->
