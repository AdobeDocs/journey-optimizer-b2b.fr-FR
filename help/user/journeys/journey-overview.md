---
title: Parcours de compte
description: Découvrez les parcours de compte et comment les créer et les gérer.
feature: Account Journeys
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: 07198448d168e66023fada332f38099890ba4a1b
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 1%

---


# Parcours de compte

Définissez un engagement piloté par les ventes qui comprend des e-mails, des SMS, etc. à l’intérieur des parcours de compte afin de coordonner le marketing entrant avec les activités de vente sortantes pour chaque membre du groupe d’achats.

## Accès et navigation dans les parcours de compte

1. Sur la page d’accueil de Adobe Experience Platform, cliquez sur Adobe Journey Optimizer B2B Edition.

1. Dans le volet de navigation de gauche, cliquez sur **[!UICONTROL parcours de compte]**.

   ![Accès aux parcours de compte](./assets/account-journey-browse.png){width="800" zoomable="yes"}

   La page parcours affichée comprend les colonnes suivantes :

   * [!UICONTROL Nom] (cliquez sur le nom pour ouvrir le parcours de compte à modifier)
   * [!UICONTROL Status]
   * [!UICONTROL Description]
   * [!UICONTROL Créé par]
   * [!UICONTROL  Dernière mise à jour à ]
   * [!UICONTROL Dernière mise à jour par]
   * [!UICONTROL Publié le ]
   * [!UICONTROL Publié par]

Ce tableau permet de rechercher par nom et Créé par. Le tri n’est actuellement pas disponible.

Vous pouvez personnaliser le tableau affiché en cliquant sur l’icône _Colonnes_ dans le coin supérieur droit et en sélectionnant ou en désélectionnant les cases à cocher.

![Choisissez les colonnes à afficher dans la liste des parcours de compte](./assets/account-journeys-list-columns.png){width="800" zoomable="yes"}

## Anatomie d&#39;un parcours de compte

Cliquez sur le nom (affiché sous forme de lien) dans la liste _[!UICONTROL parcours de compte]_ pour passer en revue les détails, apporter des modifications et prendre des mesures.

![Espace de travail du parcours de compte](./assets/account-journey-workspace.png){width="800" zoomable="yes"}

L’en-tête de l’éditeur de chaque parcours de compte comprend :

* Nom du parcours
* Possibilité de modifier le nom (_Icône Edit_)
* État du parcours

Les actions suivantes sont disponibles dans l’en-tête :

* **Publish** - Vous pouvez publier un parcours en l’absence d’erreurs de blocage. Une fois publié, l’état du Parcours passe à _Live_. Si le parcours comporte des erreurs, le bouton est grisé avec les informations de contenu : `Resolve errors before publishing`.
* **Dupliquer** - Cette action est similaire à une fonction de clonage, mais le parcours dupliqué n’inclut aucune ressource.
* **Fermer aux nouvelles entrées** - Si vous fermez un parcours, les comptes actuellement en parcours continuent leur chemin dans le parcours et aucune autre entrée de parcours ne peut se produire. Un parcours fermé ne peut pas être redémarré. Vous pouvez dupliquer un parcours fermé.
* **Abandonner** - Si vous arrêtez un parcours, les comptes du parcours arrêtent immédiatement leur progression et aucune autre entrée de parcours ne peut se produire. Un parcours arrêté ne peut pas être redémarré. Si vous bloquez de nouvelles entrées sans arrêter le progrès des gens, envisagez plutôt de fermer le parcours.
* **Supprimer** - Cette action supprime définitivement le parcours.

L’état d’un Parcours change en fonction des actions que vous appliquez. En fonction de l’état d’un parcours, certaines actions ne sont pas disponibles dans l’en-tête.

| Statut | Description | Actions disponibles |
| ------ | ----------- | ----------------- |
| _**Version préliminaire**_ | Parcours non publié modifiable. | <ul><li>Publier</li><li>Dupliquer </li><li>Supprimer </li></ul> |
| _**Live**_ | L’état du parcours passe de Version préliminaire à En direct lorsqu’un parcours est publié. Dans cet état, il n’est plus modifiable. | <ul><li>Dupliquer </li><li>Fermer les nouvelles entrées </li><li>Abandonner </li></ul> |
| _**Fermé aux nouvelles entrées**_ | L’état du parcours passe de _Live_ à _Fermé aux nouvelles entrées_ lorsque vous cliquez sur [!UICONTROL Fermer aux nouvelles entrées] dans la barre de navigation supérieure. | <ul><li>Dupliquer </li><li>Abandonner </li></ul> |
| _**Aborted**_ | L’état du parcours passe de _Live_ ou _Fermé aux nouvelles entrées_ lorsque vous interrompez un parcours. Un parcours abandonné ne peut pas être redémarré. | <ul><li>Dupliquer </li><li>Supprimer </li></ul> |
| _**Terminé**_ | Lorsque tous les comptes d’un parcours terminent le parcours, l’état passe de En ligne ou Fermé aux nouvelles entrées à Terminé. | <ul><li>Dupliquer </li><li>Supprimer </li></ul> |

## Prise en main du parcours

Pour commencer à utiliser un parcours de compte, créez le parcours, puis construisez les noeuds et le flux de parcours dans l’éditeur de parcours.

### Création d’un parcours de compte

1. Dans le volet de navigation de gauche, cliquez sur **[!UICONTROL parcours de compte]**.

1. Cliquez sur **[!UICONTROL Créer un Parcours de compte]** en haut à droite de la page.

1. Dans la boîte de dialogue, saisissez un **[!UICONTROL Nom]** unique (obligatoire) et **[!UICONTROL Description]** (facultatif).

   ![Boîte de dialogue Créer un Parcours de compte](./assets/account-journey-create-dialog.png){width="400"}

1. Cliquez sur **[!UICONTROL Créer]**.

### Ajout de l’audience du compte pour votre parcours

Un parcours de compte commence toujours par Audience du compte où vous pouvez ajouter une entrée à votre parcours.

1. Cliquez sur le noeud **[!UICONTROL Audience du compte]** pour afficher les propriétés du noeud à droite.

   ![Noeud d’audience de compte](./assets/account-journey-account-audience-node.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Ajouter une audience de compte]**.

   Vous pouvez sélectionner un segment d’audience précédemment sélectionné en cliquant sur _[!UICONTROL Ajouter des audiences]_.

1. Pour créer un segment d’audience, sélectionnez **[!UICONTROL Audiences du compte]** dans le volet de navigation de gauche.

1. Cliquez sur **[!UICONTROL Créer une audience]** et suivez les étapes décrites dans le [guide Segmentation Service](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/account-audiences){target="_blank"}.

### Blocs de création d’un parcours

Le _canevas de parcours_ est la zone centrale du concepteur de parcours. C’est dans cette zone que vous pouvez ajouter des noeuds de parcours et les configurer. Cliquez sur un noeud pour ouvrir son volet de propriétés à droite du canevas et définissez-le en fonction de votre conception.

Vous pouvez créer votre parcours à l’aide de l’un des types de noeuds suivants :

* [Écoute d’un événement](journey-nodes.md#listen-for-an-event)
* [Agir](journey-nodes.md#take-an-action)
* [Fractionner les chemins](journey-nodes.md#split-paths)
* [Attente](journey-nodes.md#wait)
* [Fusion des chemins](journey-nodes.md#merge-paths)

### Garde les rails

Pour vous aider à créer un parcours sans rencontrer d’erreur, les rails de garde suivants sont en place :

* _Suppression d’un noeud de chemin de partage_ : vous ne pouvez pas supprimer un noeud sans supprimer tous les noeuds suivants dans chaque chemin d’accès.
* _Suppression d’un noeud de fusion_ : un noeud de fusion ne peut être supprimé que lorsqu’un chemin d’accès y est connecté. Pour supprimer un noeud de fusion, laissez un seul chemin d’accès sélectionné.
* _Basculement entre le compte et les personnes_ : vous ne pouvez pas modifier la sélection des comptes en personnes sans supprimer tous les noeuds suivants dans chaque chemin d’accès.

### Ajouter un noeud

1. Accédez à l’éditeur de parcours.

1. Cliquez sur l’icône plus ( **+** ) dans le chemin d’accès et sélectionnez le type de noeud.

1. Définissez les propriétés du noeud à droite.

### Supprimer un noeud

1. Accédez à l’éditeur de parcours.

1. Dans les propriétés du noeud à droite, cliquez sur l’icône _Supprimer_ (corbeille).

1. Dans la boîte de dialogue de configuration, cliquez sur **[!UICONTROL Supprimer]**.

### Ajout et suppression d’un chemin

1. Accédez à l’éditeur de parcours.

1. Cliquez sur l’icône plus ( **+** ) sur le chemin d’accès et ajoutez le noeud de chemin d’accès partagé.

1. Dans les propriétés du noeud à droite, sélectionnez **[!UICONTROL Compte]**.

1. Pour ajouter d’autres chemins, cliquez sur **[!UICONTROL Ajouter un chemin]**.

   Avec chaque chemin créé dans le parcours, une nouvelle carte apparaît dans les propriétés.

1. Accédez à l’un des chemins d’accès du parcours et ajoutez des noeuds d’action ou d’événement à ce chemin d’accès à l’aide de l’icône plus.

1. Sélectionnez le noeud de chemin de division pour ouvrir les propriétés à droite.

   Notez que les chemins contenant des noeuds ne peuvent pas être supprimés.

1. Pour supprimer ces chemins d’accès, vous devez d’abord supprimer tous les noeuds de ce chemin d’accès.

### Planification d’un parcours

Lorsque vous publiez un parcours, celui-ci peut commencer immédiatement ou à une date ultérieure planifiée. La date de fin peut être de trois ans au maximum à partir de la date de début. Une fois qu’un parcours est publié (_Live_ status), vous pouvez mettre à jour la date de fin du parcours, mais pas la date de début.

1. Accédez à l’éditeur de parcours.

1. Planifiez votre parcours en cliquant sur [!UICONTROL Paramètres du Parcours] dans l’en-tête.

1. Dans la boîte de dialogue, définissez les options de planification :

   * Choisissez un type de planification.

     Pour activer le parcours au moment de la publication, choisissez **[!UICONTROL Immédiatement]**.

     Pour activer le parcours à une date ultérieure, choisissez **[!UICONTROL À une date spécifique]** et cliquez sur l’icône _Calendrier_ pour sélectionner la date.

     ![Boîte de dialogue des paramètres de Parcours](./assets/account-journey-settings-dialog.png){width="400" zoomable="no"}

   * Spécifiez la **[!UICONTROL Date de fin]** pour le parcours. Il peut s’écouler trois ans au maximum à partir de la date de début (ce champ est obligatoire).

1. Cliquez sur **[!UICONTROL Enregistrer]**.

   Lorsque vous êtes prêt à publier votre parcours, vous pouvez consulter ces paramètres lorsque vous cliquez sur _[!UICONTROL Publish]_.
