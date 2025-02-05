---
title: Parcours de compte
description: Découvrez les parcours de compte et comment les créer et les gérer.
feature: Account Journeys
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: 279bc07b90da96c3d497f67a14596a3bed308984
workflow-type: tm+mt
source-wordcount: '1141'
ht-degree: 2%

---


# Parcours de compte

Créez et exécutez des parcours personnalisés pour chaque groupe d’achats et membre du groupe d’achats à l’aide d’un engagement automatisé par e-mail, SMS, événement, etc. Grâce aux parcours de compte, vous pouvez rationaliser la génération de la demande et la qualification des groupes d&#39;achat et stimuler une demande plus qualifiée pour vos programmes d&#39;acquisition, de vente incitative/croisée et de rétention.

Définissez un engagement axé sur les ventes qui inclut des e-mails, des SMS et d’autres parcours de compte internes pour coordonner le marketing entrant avec les activités de vente sortantes pour chaque membre du groupe d’achats.

## Accéder aux parcours de compte et les parcourir

1. Sur la page d’accueil de Adobe Experience Platform, cliquez sur Adobe Journey Optimizer B2B edition.

1. Dans le volet de navigation de gauche, cliquez sur **[!UICONTROL parcours de compte]**.

   ![Accéder aux parcours de compte](./assets/account-journey-browse.png){width="800" zoomable="yes"}

   La page parcours affichée comprend les colonnes suivantes :

   * [!UICONTROL Nom] (cliquez sur le nom pour ouvrir le parcours de compte à modifier)
   * [!UICONTROL Statut]
   * [!UICONTROL Description]
   * [!UICONTROL Créé par]
   * [!UICONTROL Dernière mise à jour : ]
   * [!UICONTROL Dernière mise à jour par]
   * [!UICONTROL Publié le]
   * [!UICONTROL Publié par]

Ce tableau permet de rechercher des ressources par nom et par date de création. Le tri n’est actuellement pas disponible.

Vous pouvez personnaliser le tableau affiché en cliquant sur l’icône _Colonnes_ dans le coin supérieur droit, puis en cochant ou décochant les cases.

![Choisissez les colonnes à afficher dans la liste des parcours de compte](./assets/account-journeys-list-columns.png){width="800" zoomable="yes"}

## Anatomie d’un parcours de compte

Cliquez sur le nom (affiché sous forme de lien) dans la liste _[!UICONTROL parcours de compte]_ pour passer en revue les détails, apporter des modifications et prendre des mesures.

![Espace de travail du parcours de compte](./assets/account-journey-workspace.png){width="800" zoomable="yes"}

L’en-tête d’éditeur de chaque parcours de compte comprend :

* Nom du parcours
* Possibilité de modifier le nom (icône _Modifier_)
* Etat du parcours

Les actions suivantes sont disponibles dans l’en-tête :

* **Publish** - Vous pouvez publier un parcours s&#39;il n&#39;y a aucune erreur de blocage. Une fois publié, le statut du parcours passe à _Actif_. Si le parcours comporte des erreurs, le bouton est grisé avec les informations de contenu : `Resolve errors before publishing`.
* **Dupliquer** - Cette action est similaire à une fonction de clonage, mais le parcours dupliqué n’inclut aucune ressource.
* **Fermer aux nouvelles entrées** - Si vous fermez un parcours, les comptes actuellement dans le parcours continuent leur chemin dans le parcours et aucune autre entrée de parcours ne peut se produire. Impossible de redémarrer un parcours fermé. Vous pouvez dupliquer un parcours fermé.
* **Abandon** - Si vous arrêtez un parcours, les comptes du parcours arrêtent immédiatement leur progression et aucune nouvelle entrée de parcours ne peut se produire. Impossible de redémarrer un parcours arrêté. Si vous bloquez les nouvelles entrées sans arrêter la progression des gens, envisagez plutôt de fermer le parcours.
* **Supprimer** - Cette action supprime définitivement le parcours.

Le statut d’un Parcours change en fonction des actions que vous appliquez. En fonction du statut d’un parcours, certaines actions sont ou ne sont pas disponibles dans l’en-tête .

| Statut | Description | Actions disponibles |
| ------ | ----------- | ----------------- |
| _**Brouillon**_ | Parcours dépublié modifiable. | <ul><li>Publier</li><li>Dupliquer </li><li>Supprimer </li></ul> |
| _**En direct**_ | Le statut du parcours passe de Brouillon à Actif lorsqu’un parcours est publié. Dans ce statut, il n’est plus modifiable. | <ul><li>Dupliquer </li><li>Fermer aux nouvelles entrées </li><li>Abandonner </li></ul> |
| _**Fermé aux nouvelles entrées**_ | Le statut du parcours passe de _En ligne_ à _Fermé aux nouvelles entrées_ lorsque vous cliquez sur [!UICONTROL Fermer aux nouvelles entrées] dans le volet de navigation supérieur. | <ul><li>Dupliquer </li><li>Abandonner </li></ul> |
| _**Abandonné**_ | Le statut du parcours passe de _En ligne_ ou _Fermé aux nouvelles entrées_ lorsque vous abandonnez un parcours. Impossible de redémarrer un parcours abandonné. | <ul><li>Dupliquer </li><li>Supprimer </li></ul> |
| _**Terminé**_ | Lorsque tous les comptes d’un parcours ont terminé le parcours, le statut passe de Actif ou Fermé à Nouvelles entrées et passe à Terminé. | <ul><li>Dupliquer </li><li>Supprimer </li></ul> |

## Prise en main d’un parcours

Pour commencer à utiliser un parcours de compte, créez le parcours, puis construisez les nœuds et le flux de parcours dans l’éditeur de parcours.

### Création d’un parcours de compte

1. Dans le volet de navigation de gauche, cliquez sur **[!UICONTROL parcours de compte]**.

1. Cliquez sur **[!UICONTROL Créer un Parcours de compte]** en haut à droite de la page.

1. Dans la boîte de dialogue, saisissez un **[!UICONTROL Nom]** unique (obligatoire) et un **[!UICONTROL Description]** (facultatif).

   ![ Boîte de dialogue Créer un Parcours de compte ](./assets/account-journey-create-dialog.png){width="400"}

1. Cliquez sur **[!UICONTROL Créer]**.

### Blocs de construction d’un parcours

La carte de parcours __ est la zone centrale du concepteur de parcours. C’est dans cette zone que vous pouvez ajouter des nœuds de parcours et les configurer. Cliquez sur un nœud pour ouvrir son volet Propriétés à droite de la zone de travail et définissez-le en fonction de votre conception. Un parcours de compte commence toujours par un nœud [Audience du compte](./account-audience-nodes.md) où vous pouvez ajouter des données à votre parcours.

Après avoir créé un parcours de compte et ajouté l’audience, créez le parcours à l’aide de nœuds . La carte de parcours fournit une zone de travail, où vous pouvez créer vos cas d’utilisation marketing B2B à plusieurs étapes à l’aide des types de nœuds suivants pour créer un parcours de compte :

* [Effectuer une action](./action-nodes.md)
* [Écoute d’un événement](./listen-for-event-nodes.md)
* [Partage de chemins](./split-merge-paths-nodes.md)
* [Attente](./wait-nodes.md)
* [Fusionner les chemins](./split-merge-paths-nodes.md)

### Mécanismes de sécurisation

Pour vous aider à créer un parcours sans rencontrer d’erreur, les barrières de sécurité suivantes sont en place :

* _Suppression d’un nœud de chemin de division_ : vous ne pouvez pas supprimer un nœud sans supprimer tous les nœuds suivants dans chaque chemin.
* _Suppression d’un nœud de fusion_ : un nœud de fusion ne peut être supprimé que lorsqu’un chemin d’accès lui est connecté. Pour supprimer un nœud de fusion, ne laissez qu’un seul chemin sélectionné.
* _Basculer entre le compte et les personnes_ : vous ne pouvez pas modifier la sélection des comptes en personnes sans supprimer tous les nœuds suivants dans chaque chemin d’accès.

### Ajouter un nœud

1. Accédez à l’éditeur de parcours.

1. Cliquez sur l’icône plus ( **+** ) sur le chemin d’accès et sélectionnez le type de nœud.

1. Définissez les propriétés du nœud sur la droite.

### Suppression d’un nœud

1. Accédez à l’éditeur de parcours.

1. Dans les propriétés du nœud sur la droite, cliquez sur l’icône _Supprimer_ ( ![icône Supprimer](../assets/do-not-localize/icon-delete.svg) ).

1. Dans la boîte de dialogue de conformation, cliquez sur **[!UICONTROL Supprimer]**.

### Ajouter et supprimer un chemin d’accès

1. Accédez à l’éditeur de parcours.

1. Cliquez sur l’icône plus ( **+** ) sur le chemin d’accès et ajoutez le [nœud de chemin de fractionnement](./split-merge-paths-nodes.md#split-paths).

1. Dans les propriétés du nœud sur la droite, sélectionnez **[!UICONTROL Compte]**.

1. Pour ajouter d’autres chemins d’accès, cliquez sur **[!UICONTROL Ajouter un chemin]**.

   Pour chaque chemin d’accès créé dans le parcours, une nouvelle carte de chemin d’accès s’affiche dans les propriétés.

1. Accédez à l’un des chemins d’accès du parcours et ajoutez des nœuds [action](./action-nodes.md) ou [event](./listen-for-event-nodes.md) à ce chemin d’accès à l’aide de l’icône plus.

1. Sélectionnez le nœud [chemin de partage](./split-merge-paths-nodes.md) pour ouvrir les propriétés sur la droite.

   Les chemins comportant des nœuds ne peuvent pas être supprimés.

1. Pour supprimer ces chemins d’accès, vous devez d’abord supprimer tous les nœuds qu’ils contiennent.

### Planifier un parcours

Lorsque vous publiez un parcours, il peut commencer immédiatement ou à une date ultérieure planifiée. La date de fin peut être fixée à un maximum de trois ans à compter de la date de début. Une fois le parcours publié (statut _En ligne_), vous pouvez mettre à jour la date de fin du parcours, mais pas sa date de début.

1. Accédez à l’éditeur de parcours.

1. Planifiez votre parcours en cliquant sur [!UICONTROL Paramètres du Parcours ] dans l’en-tête.

1. Dans la boîte de dialogue, définissez les options de planification :

   * Choisissez un type de planning.

     Pour activer le parcours au moment de la publication, choisissez **[!UICONTROL Immédiatement]**.

     Pour activer le parcours à une date ultérieure, choisissez **[!UICONTROL À une date spécifique]** et cliquez sur l’icône _Calendrier_ pour sélectionner la date.

     Boîte de dialogue des paramètres du Parcours ![](./assets/account-journey-settings-dialog.png){width="400" zoomable="no"}

   * Spécifiez la **[!UICONTROL Date de fin]** pour le parcours. Il peut s’agir d’un maximum de trois ans à compter de la date de début (ce champ est obligatoire).

1. Cliquez sur **[!UICONTROL Enregistrer]**.

   Lorsque vous êtes prêt à publier votre parcours, vous pouvez vérifier ces paramètres en cliquant sur _[!UICONTROL Publish]_.

### Publish un parcours de compte


