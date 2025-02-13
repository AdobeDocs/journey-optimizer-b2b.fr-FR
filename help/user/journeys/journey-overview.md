---
title: Parcours de compte
description: Découvrez les parcours de compte et comment les créer et les gérer.
feature: Account Journeys
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: d03e0e2d8070916d38bb956adff8dea3f3873aad
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 4%

---


# Parcours de compte

Créez et exécutez des parcours personnalisés pour chaque groupe d’achats et membre du groupe d’achats à l’aide d’un engagement automatisé par e-mail, SMS, événement, etc. Grâce aux parcours de compte, vous pouvez rationaliser la génération de la demande et la qualification des groupes d&#39;achat et stimuler une demande plus qualifiée pour vos programmes d&#39;acquisition, de vente incitative/croisée et de rétention.

Définissez un engagement axé sur les ventes qui inclut des e-mails, des SMS et d’autres parcours de compte internes pour coordonner le marketing entrant avec les activités de vente sortantes pour chaque membre du groupe d’achats.

![Vidéo](../../assets/do-not-localize/icon-video.svg){width="30"} [Regardez la vidéo de présentation](#overview-video)

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

* **Publier** - Vous pouvez publier un parcours en l’absence d’erreur de blocage. Une fois publié, le statut du parcours passe à _Actif_. Si le parcours comporte des erreurs, le bouton est grisé avec les informations de contenu : `Resolve errors before publishing`.
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

Pour commencer à utiliser les parcours de compte :

1. [Créez un parcours](./create-publish-journey.md#create-an-account-journey).
1. [Ajoutez les nœuds](./create-publish-journey.md#add-a-node) et [définissez le flux de parcours ](./create-publish-journey.md#add-and-delete-a-path) dans la carte de parcours.
1. [Publier le parcours ](./create-publish-journey.md#publish-an-account-journey).

## Vidéo de présentation

>[!VIDEO](https://video.tv.adobe.com/v/3443202/?learn=on)
