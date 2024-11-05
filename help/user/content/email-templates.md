---
title: Modèles d'e-mail
description: Découvrez comment gérer et créer des modèles d’email qui peuvent être utilisés pour créer facilement et efficacement des emails de parcours de compte.
feature: Email Authoring, Content
exl-id: 4e146802-e3ef-4528-b581-191e28afe86f
source-git-commit: 10f8f254f49bb5dfb498758a4f39b23112c123a0
workflow-type: tm+mt
source-wordcount: '1396'
ht-degree: 4%

---

# Modèles d’e-mail

Pour accélérer et améliorer le processus de conception, vous pouvez créer des modèles d’email autonomes pour réutiliser du contenu personnalisé dans les parcours de compte B2B edition Adobe Journey Optimizer. Grâce aux modèles, les membres de votre équipe orientés contenu peuvent travailler sur le contenu d’un email en dehors des parcours. Les stratèges marketing peuvent ensuite réutiliser et adapter ces modèles autonomes dans leurs parcours de compte. Par exemple, un membre de l’équipe est responsable du contenu uniquement, sans accès aux parcours du compte. Cependant, ils peuvent créer un modèle de courrier électronique que les marketeurs peuvent sélectionner comme point de départ pour les communications par courrier électronique et le personnaliser en fonction des exigences du parcours.

## Accès et gestion des modèles d’email

Pour accéder aux modèles d’email dans Adobe Journey Optimizer B2B edition, accédez au volet de navigation de gauche et cliquez sur **[!UICONTROL Gestion de contenu]** > **[!UICONTROL Modèles]**. Cette action ouvre une page de liste avec tous les modèles d&#39;email créés dans l&#39;instance répertoriés dans un tableau.

Le tableau est trié par colonne _[!UICONTROL Modifié]_, les modèles mis à jour le plus récemment se trouvant en haut de la liste par défaut. Cliquez sur le titre de la colonne pour passer d’un titre croissant à un titre décroissant.

Pour rechercher un modèle par nom, saisissez une chaîne de texte dans la barre de recherche. Cliquez sur l’icône _Filtrer_ en haut à gauche pour filtrer la liste en fonction des dates de création ou de modification et des modèles que vous avez créés ou modifiés.

![Accédez à la bibliothèque de modèles d&#39;email et filtrez par nom et dates](./assets/templates-list-search-filter.png){width="700" zoomable="yes"}

Personnalisez les colonnes que vous souhaitez afficher dans le tableau en cliquant sur l’icône _Personnaliser le tableau_ en haut à droite. Sélectionnez les colonnes à afficher et cliquez sur **[!UICONTROL Appliquer]**.

Sur la page de liste, vous pouvez effectuer les actions décrites dans les sections suivantes.

## Création d’un modèle de courrier électronique

Vous pouvez créer un modèle d’email à partir de la page de liste des modèles d’email en cliquant sur **[!UICONTROL Créer un modèle]** en haut à droite.

1. Dans la boîte de dialogue, saisissez un **[!UICONTROL Nom]** et une **[!UICONTROL Description]** (facultatif).

   ![ Entrez les propriétés initiales du nouveau modèle d&#39;email ](./assets/templates-create-dialog.png){width="400"}

1. Définissez la **[!UICONTROL source d&#39;image]** initiale.

   Si vous disposez d’un abonnement pour Experience Manager Assets as a Cloud Service ainsi que de Adobe Marketo Engage Design Studio par défaut, vous pouvez sélectionner des ressources d’image à partir de l’une des sources. Pour cela, vous devez sélectionner la source de l&#39;image au moment de la création pour un modèle d&#39;email ou un fragment visuel. Cependant, vous pouvez également sélectionner la source de l’image lorsque vous modifiez le contenu.

   Pour plus d’informations sur les sources d’images, voir [Assets](./assets-overview.md).

1. Cliquez sur **[!UICONTROL Créer]**.

La page _[!UICONTROL Concevez votre modèle]_ s’ouvre et fournit plusieurs options pour créer le modèle : _[!UICONTROL Concevoir à partir de zéro]_, _[!UICONTROL Importer un HTML]_ ou _[!UICONTROL Sélectionner un modèle de conception]_.

![Choisissez comment commencer avec votre conception de modèle d&#39;email](./assets/templates-create-design.png){width="800" zoomable="yes"}

Après avoir sélectionné la méthode que vous souhaitez utiliser pour démarrer votre conception de modèle d&#39;email, utilisez le concepteur visuel pour [créer le contenu de votre modèle d&#39;email](./email-template-authoring.md).

### Créer en partant de zéro

Utilisez l&#39;éditeur visuel de contenu pour définir la structure du contenu de l&#39;email. En ajoutant et en déplaçant des composants structurels à l’aide de simples actions de glisser-déposer, vous pouvez concevoir la forme du contenu d’email réutilisable en quelques secondes.

>[!NOTE]
>
>Les outils de conception disponibles sont équivalents aux outils utilisés pour la [création d’email](./email-authoring.md). La différence est que ce contenu est ensuite enregistré comme un modèle qui peut être réutilisé sur plusieurs noeuds _envoyer un email_ dans les parcours de compte.

1. Sur la page d&#39;accueil _[!UICONTROL Concevez votre modèle]_ , sélectionnez l&#39;option **[!UICONTROL Concevoir à partir de zéro]** .

1. [Ajoutez la structure et le contenu](./email-authoring.md#add-structure-and-content) au modèle.

### Importer du contenu HTML

Adobe Journey Optimizer B2B edition vous permet d’importer du contenu d’HTML existant pour concevoir vos modèles de courrier électronique.

{{$include /help/_includes/content-design-import.md}}

![importer du contenu html dans un fichier zip](./assets/templates-import-zip-file.png){width="500"}

>[!NOTE]
>
>L’utilisation d’une balise `<table>` comme première couche d’un fichier HTML peut entraîner une perte de style, y compris les paramètres d’arrière-plan et de largeur dans la balise de couche supérieure.

Vous pouvez personnaliser le contenu importé selon vos besoins à l’aide du concepteur visuel.

### Sélection d’un modèle de conception

{{$include /help/_includes/content-design-select-template.md}}

## Afficher les détails d’un modèle de courrier électronique

Sur la page de liste Modèles , cliquez sur le nom d’un modèle de courrier électronique pour ouvrir la page de détails du modèle de courrier électronique. À partir de là, vous pouvez afficher les propriétés de base du modèle d’email et accéder à l’éditeur visuel de contenu pour apporter des modifications au contenu du modèle.

![Accédez à la bibliothèque de modèles d&#39;email et filtrez par nom et dates](./assets/template-details.png){width="700" zoomable="yes"}

* Affichez les détails du modèle de courrier électronique, tels que le nom et la description. Ces paramètres peuvent être modifiés. Cliquez en dehors de la zone de description pour enregistrer automatiquement les modifications.

* Affichez les propriétés du modèle d’email telles que les propriétés créées par, créées le, mises à jour le plus récent et modifiées par .

* Cliquez sur **[!UICONTROL Plus]** en haut à droite pour exécuter des actions rapides sur le modèle de courrier électronique, telles que _Dupliquer_ et _Supprimer_.

* S’il existe des alertes actives (erreurs et avertissement pour le modèle d’email), cliquez sur **[!UICONTROL Alertes]** en haut à droite pour afficher les informations.

  Bien que ces alertes n’interdisent pas l’utilisation du modèle d’email pour la création d’email, ces informations permettent aux marketeurs de se familiariser avec ce qui pourrait ne pas fonctionner et les mises à jour requises avant qu’il ne puisse être utilisé pour la diffusion.

## Affichage des références utilisées par le modèle de courrier électronique

Dans la page des détails des modèles d’email, cliquez sur l’onglet **[!UICONTROL Utilisé par]** pour afficher les détails de l’utilisation de ce modèle d’email dans les emails sur les parcours de compte.

![ Cliquez sur l’onglet Utilisé par pour vérifier l’utilisation des modèles](./assets/template-details-used-by.png){width="400"}

Les emails dans Journey Optimizer B2B edition sont incorporés et créés dans parcours. Par conséquent, le parcours parent de l’email qui utilise le modèle s’affiche dans les références.

* Cliquez sur le lien pour accéder à l&#39;email de parcours correspondant dans lequel le modèle d&#39;email est utilisé.

* Quittez la vue à tout moment en cliquant sur la flèche Précédent, ce qui vous ramène à la page de liste.

## Modifier des modèles de courrier électronique

Cette action peut être réalisée à partir des éléments suivants :

* La page de détails - Cliquez sur **[!UICONTROL Modifier le modèle d&#39;email]**.
* La page de liste : cliquez sur les points de suspension (**...**) en regard d’un modèle de courrier électronique et choisissez **[!UICONTROL Modifier]**.

Cette action vous conduit à la page _Concevoir votre modèle_ ou à la page de l’éditeur de contenu visuel en fonction du dernier état enregistré du modèle d’email. À partir de là, vous pouvez modifier le contenu de votre modèle d’email selon vos besoins. Pour plus d’informations sur les options de modification, voir [Création de modèles d’email](#create-email-templates) .

## Dupliquer des modèles d&#39;email

Vous pouvez dupliquer un modèle d&#39;email en utilisant l&#39;une des méthodes suivantes :

* Dans les détails du modèle d&#39;email sur la droite, développez **[!UICONTROL Plus]** et cliquez sur **[!UICONTROL Dupliquer]**.

  ![Cliquez sur Plus pour accéder aux actions Supprimer et dupliquer](./assets/template-details-more-menu.png){width="400"}

* Sur la page de liste _Modèles d&#39;email_, cliquez sur les points de suspension (...) en regard du modèle et sélectionnez **[!UICONTROL Dupliquer]**.

Dans la boîte de dialogue, saisissez un nom (unique) et une description utiles. Cliquez sur **[!UICONTROL Dupliquer]** pour terminer l’action.

Le modèle de courrier électronique dupliqué (nouveau) s’affiche alors dans la liste _Modèles de courrier électronique_.

## Supprimer des modèles de courrier électronique

La suppression d’un modèle de courrier électronique est irréversible. Vérifiez donc avant de lancer une action de suppression. Vous pouvez supprimer un modèle d&#39;email à l&#39;aide de l&#39;une des méthodes suivantes :

* Dans les détails du modèle à droite, développez **[!UICONTROL Plus]** et cliquez sur **[!UICONTROL Supprimer]**.
* Sur la page de liste _Modèles d&#39;email_, cliquez sur les points de suspension (...) en regard du modèle et choisissez **[!UICONTROL Supprimer]**.

  ![Cliquez sur ... pour accéder aux actions Dupliquer et Supprimer](./assets/templates-list-more-menu.png){width="500"}

Cette action ouvre une boîte de dialogue de confirmation. Vous pouvez interrompre le processus en cliquant sur **[!UICONTROL Annuler]** ou sur **[!UICONTROL Supprimer]** pour confirmer la suppression.

## Actions en masse

Dans la page de liste des modèles d’email, sélectionnez plusieurs modèles à la fois en cochant les cases à gauche. Une bannière s’affiche en bas lorsque vous sélectionnez plusieurs modèles.

![Une bannière affiche le nombre de modèles sélectionnés et l’icône Supprimer](./assets/templates-multi-select-banner.png){width="600"}

**[!UICONTROL Supprimer]** : vous pouvez supprimer jusqu’à 20 modèles à la fois. Une boîte de dialogue de confirmation vous permet d’abandonner l’action ou de confirmer la suppression des modèles.

## Création d’un email à partir d’un modèle enregistré

Depuis l’écran _Créer votre e-mail_, utilisez la section _Sélectionner un modèle de conception_ pour commencer à créer votre contenu à partir d’un modèle.

Pour commencer à créer votre contenu avec l’un des modèles d’email créés, procédez comme suit :

1. Accédez au Designer d&#39;email à partir de la page _Modifier le contenu_ .

   Sur la page _Créer votre email_, l&#39;onglet _Modèles d&#39;exemple_ est sélectionné par défaut.

1. Pour utiliser un modèle de courrier électronique personnalisé, sélectionnez l’onglet **[!UICONTROL Modèles enregistrés]** .

   Cet onglet affiche la liste de tous les modèles de courrier électronique créés dans l’environnement de test. Vous pouvez les trier _Par nom_, _Dernière modification_ et _Dernière création_.

1. Sélectionnez le modèle de votre choix dans la liste.

   Une fois la sélection effectuée, un aperçu du modèle s’affiche. En mode Aperçu, vous pouvez naviguer entre tous les modèles d’une catégorie (échantillon ou enregistré, selon votre sélection) à l’aide des flèches droite et gauche.

1. Cliquez sur **[!UICONTROL Utiliser ce modèle]** en haut à droite.

1. Dans le concepteur de contenu visuel, modifiez votre contenu selon vos besoins.
