---
title: Création d’emails
description: Découvrez comment créer du contenu d’email personnalisé utilisé dans les Parcours de compte.
feature: Email Authoring, Content
exl-id: 0f4ae644-ade7-49a0-935c-7f4779c25ffb
source-git-commit: ce38e378ad316fb379cb649a4592ed831250296d
workflow-type: tm+mt
source-wordcount: '1294'
ht-degree: 11%

---

# Création d’emails

Utilisez Adobe Journey Optimizer B2B Edition pour envoyer des messages électroniques à vos clients. Vous pouvez créer, personnaliser et prévisualiser des messages dans le concepteur d’e-mail.

## Ajout d’une action de courrier électronique dans un parcours de compte

Vous pouvez configurer des diffusions email dans un Parcours de compte lorsque vous ajoutez un noeud _[!UICONTROL Take an action]_ et procédez comme suit :

1. Pour la cible _[!UICONTROL Action sur]_, choisissez **[!UICONTROL Personnes]**.
1. Pour l’ _[!UICONTROL action sur les personnes]_, choisissez **[!UICONTROL Envoyer un email]**.
1. Pour la _[!UICONTROL source d&#39;email]_, choisissez **[!UICONTROL Créer un email]**.

   Vous pouvez également sélectionner l’option _[!UICONTROL Sélectionner un email dans Adobe Marketo Engage]_ pour utiliser l’un des emails précréés dans Marketo Engage et l’envoyer dans le cadre du Parcours de compte.

   >[!NOTE]
   >
   >Si vous créez un email pour la première fois, assurez-vous que le canal email est configuré dans Adobe Marketo Engage. Pour en savoir plus, consultez la section [Assurer la délivrabilité des emails](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps#ensure-email-deliverability) dans la documentation du Marketo Engage.

   ![Agir - envoyer un email](assets/journey-node-send-email.png){width="700" zoomable="yes"}

1. Au bas du panneau _[!UICONTROL Agir sur une action]_, cliquez sur **[!UICONTROL Créer un email]**.

1. Dans la boîte de dialogue, saisissez un **[!UICONTROL nom]** unique pour l’email et une **[!UICONTROL ligne Objet]**.

   ![Créer une boîte de dialogue de courrier électronique](assets/create-new-email.png){width="400"}

1. Cliquez sur **[!UICONTROL Créer]**.

   Dans la section _[!UICONTROL Propriétés de l&#39;email]_ de la page de contenu de l&#39;email, les champs _[!UICONTROL De l&#39;email]_ et _[!UICONTROL Répondre à l&#39;adresse]_ sont déjà configurés. Vous pouvez saisir des valeurs pour les champs _[!UICONTROL From name]_ et _[!UICONTROL Description]_ (facultatif).

## Créer le contenu d’un e-mail

Cliquez sur **[!UICONTROL Ajouter du contenu d&#39;email]** en haut du panneau d&#39;aperçu _[!UICONTROL Email]_.

![Cliquez sur Ajouter un contenu d’email ](./assets/add-email-content.png){width="700" zoomable="yes"}

Cette action lance le Designer d&#39;email, dans lequel vous pouvez choisir la manière dont vous souhaitez concevoir votre email à partir des options suivantes :

* [Concevez entièrement votre email](#design-your-email-from-scratch) à l’aide de l’interface Designer des emails.

* [Importez du contenu HTML existant](#import-existing-html-content) à partir d’un fichier ou d’un dossier .zip.

* [Sélectionnez un modèle existant](#select-a-template) dans une liste de modèles d’email intégrés ou personnalisés.

Pour configurer et personnaliser la ligne d’objet à l’aide de l’éditeur d’expression, cliquez sur l’icône _Personalization_ et ajoutez les jetons du Marketo Engage.

Après avoir créé et personnalisé le contenu de l’email, vous pouvez l’exporter pour validation ou pour une utilisation ultérieure. Cliquez sur **[!UICONTROL Exporter l’HTML]** pour enregistrer le contenu sous la forme d’un fichier .zip contenant votre HTML et vos ressources.

>[!TIP]
>
>Utilisez l’assistant d’IA dans l’édition B2B de Adobe Journey Optimizer, optimisé par l’IA générative, pour élever le contenu au niveau suivant. L’assistant d’IA peut vous aider à optimiser l’impact de vos diffusions en générant des emails complets, du contenu texte ciblé et en obtenant des recommandations d’assistant d’IA pour les images qui résonnent avec votre audience. [En savoir plus](./ai-assistant-emails.md)

### Concevoir entièrement votre email

1. Sur la page d’accueil du Concepteur, cliquez sur l’option **[!UICONTROL Créer en partant de zéro]**.

1. Pour commencer la conception de contenu, faites glisser un élément de l’élément **[!UICONTROL Structures]** et déposez-le sur la zone de travail.

   Répétez cette étape pour chaque composant de structure afin de construire la mise en page de votre email.

1. Ajoutez autant d&#39;éléments de _Structures_ que nécessaire et modifiez les paramètres de chacun dans le volet de droite.

   Sélectionnez le composant n:n colonne pour définir le nombre de colonnes de votre choix (entre trois et dix). Vous pouvez également définir la largeur de chaque colonne en déplaçant les flèches sous la colonne.

   La taille de chaque colonne ne peut pas être inférieure à 10 % de la largeur totale du composant de structure. Seules les colonnes vides peuvent être supprimées.

1. Développez la section **[!UICONTROL Contenu]** et ajoutez autant d’éléments que nécessaire dans un ou plusieurs composants de structure.

1. Si nécessaire, vous pouvez effectuer des personnalisations supplémentaires pour chaque composant dans les onglets _[!UICONTROL Paramètres]_ ou _[!UICONTROL Style]_ .

   Par exemple, vous pouvez modifier le style de texte, la marge ou la marge intérieure de chaque composant.

1. Dans le sélecteur de ressources, vous pouvez sélectionner directement des ressources stockées dans la bibliothèque Assets.

   Double-cliquez sur le dossier contenant vos ressources. Faites glisser les éléments dans un composant de structure.

1. Insérez des champs de personnalisation pour personnaliser votre contenu à partir des attributs de profil, des appartenances à l’audience, des attributs contextuels, etc.

<!-- 1. Click **[!UICONTROL Enable condition content]** to add dynamic content and adapt the content to the targeted profiles based on conditional rules.
-->
1. Sélectionnez l’onglet **[!UICONTROL Liens]** dans le volet de gauche pour afficher toutes les URL de votre contenu qui font l’objet d’un suivi.

   Vous pouvez modifier le _Type de suivi_ ou le _Libellé_ et ajouter des balises si nécessaire.

Au besoin, vous pouvez personnaliser davantage votre e-mail en cliquant sur **[!UICONTROL Basculer vers l’éditeur de code]** dans le menu avancé. L’éditeur de code vous permet de modifier le code source de l’email, tel que l’ajout de balises de suivi ou d’HTML personnalisées.

>[!CAUTION]
>
>Vous ne pouvez pas revenir au concepteur visuel de cet email après avoir basculé vers l’éditeur de code.

Une fois le contenu terminé, cliquez sur **[!UICONTROL Simuler le contenu]** dans la partie supérieure pour vérifier le rendu. Vous pouvez choisir la vue bureau ou la vue mobile.

Une fois prêt, cliquez sur Enregistrer.

### Importer du contenu d’HTML existant

Le contenu importé peut être :

* Un fichier d’HTML avec une feuille de style intégrée
* Dossier .zip contenant un fichier d’HTML, la feuille de style (.css) et les fichiers image.

>[!NOTE]
>
>Il n’existe aucune contrainte sur la structure des fichiers .zip. Cependant, les références doivent être relatives et s’ajuster à l’arborescence du dossier .zip.

_Pour importer un fichier contenant du contenu HTML :_

1. Dans la page d’accueil du concepteur d’e-mail, sélectionnez **[!UICONTROL Importer du contenu HTML]**.

1. Faites glisser et déposez le fichier HTML ou .zip contenant le contenu HTML, puis cliquez sur [!UICONTROL Importer].

   Une fois le chargement du contenu de l’HTML terminé, votre contenu est en _mode de compatibilité_. Dans ce mode, vous pouvez uniquement personnaliser votre texte, ajouter des liens ou inclure des ressources à votre contenu.

### Sélectionner un modèle

Vous pouvez choisir parmi les options suivantes :

* Exemples de modèles. L’interface de Journey Optimizer propose 20 modèles d’email d’usine que vous pouvez choisir.

* Modèles enregistrés.

* Un modèle personnalisé que vous avez créé entièrement à l’aide du menu _Modèles_ ou enregistré à partir d’un email dans un parcours à l’aide de l’option _[!UICONTROL Enregistrer en tant que modèle de contenu]_ .

_Pour commencer à créer votre contenu avec l’un des exemples ou modèles enregistrés :_

1. Accédez au _Designer d&#39;email_ à partir de l&#39;espace de travail d&#39;édition du contenu d&#39;email.

   Sur la page _[!UICONTROL Créer votre email]_, l&#39;onglet **[!UICONTROL Modèles d&#39;exemple]** est sélectionné par défaut.

1. Pour utiliser un modèle personnalisé, sélectionnez l’onglet **[!UICONTROL Modèles enregistrés]** .

   La liste de tous les modèles de contenu créés sur l’environnement de test actuel s’affiche. Vous pouvez les trier par nom, Dernière modification ou Dernière création.

1. Sélectionnez le modèle de votre choix dans la liste.

1. Après avoir sélectionné une catégorie, vous pouvez naviguer entre tous les modèles de cette catégorie (exemple ou enregistré selon votre sélection) en utilisant les flèches droite et gauche.

1. Cliquez sur **[!UICONTROL Utiliser ce modèle]** en haut à droite de la page.

1. Modifiez le contenu selon les besoins dans le _Designer email_.

## Vérifier les alertes

Lorsque vous concevez le contenu de vos emails, des alertes s’affichent dans l’interface (en haut à droite de la page) lorsque des paramètres clés sont manquants.

Si ce bouton ne s’affiche pas, aucun problème n’est détecté.

Deux types d’alertes peuvent être détectés :

* **_Avertissements_** qui font référence à des recommandations et à des bonnes pratiques, telles que :

   * `The opt-out link is not present in the email body` : l&#39;ajout d&#39;un lien de désinscription dans le corps de votre email est une bonne pratique.

     >[!NOTE]
     >
     >Les messages électroniques de style marketing doivent inclure un lien d’exclusion, qui n’est pas obligatoire pour les messages transactionnels.

   * `Text version of HTML is empty` : n’oubliez pas de définir une version texte du corps de votre email, qui est utilisée lorsque le contenu de l’HTML ne peut pas être affiché.

   * `Empty link is present in email body` : vérifiez que tous les liens de votre email sont corrects.

   * `Email size has exceeded the limit of 100KB` : pour une diffusion optimale, vérifiez que la taille de votre email ne dépasse pas 100 Ko.

* **_Erreurs_** qui vous empêchent de tester ou d’activer le parcours/la campagne tant qu’elles ne sont pas résolues, par exemple :

   * `The subject line is missing` : l’objet de l’email est obligatoire.

   * `The email version of the message is empty` : cette erreur s&#39;affiche lorsque le contenu de l&#39;email n&#39;a pas été configuré.

## Vérifier et tester l&#39;email

Lorsque le contenu de votre message est défini, vous pouvez utiliser des profils de test pour le prévisualiser, envoyer des bons à tirer et contrôler son rendu sur les clients courants de bureau, de mobile et web. Si vous avez inséré du contenu personnalisé, vous pouvez prévisualiser l&#39;affichage de ce contenu dans le message à l&#39;aide des données de profil de test.

Pour prévisualiser le contenu de l&#39;email, cliquez sur **[!UICONTROL Simuler le contenu]**, puis ajoutez un profil de test pour vérifier votre message à l&#39;aide des données de profil de test.

![Simuler le contenu de l&#39;email pour vérifier votre conception](./assets/email-designer-simulate-content.png){width="700" zoomable="yes"}
