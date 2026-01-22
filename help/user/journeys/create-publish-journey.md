---
title: Créer et publier un Parcours
description: Créez des parcours de compte et de personne dans la zone de travail visuelle, ajoutez des nœuds d’action et d’événement, configurez la planification et publiez pour l’orchestration en direct dans Journey Optimizer B2B edition.
feature: Account Journeys
role: User
exl-id: f536b1a1-8dfe-437f-a84d-b66879529621
source-git-commit: 433b08efbb24453f318bbce989ce18c9d96dea05
workflow-type: tm+mt
source-wordcount: '857'
ht-degree: 4%

---

# Créer et publier un parcours

Pour commencer à utiliser un parcours, créez le parcours, puis construisez les nœuds et le flux du parcours dans la carte du parcours.

![Vidéo](../../assets/do-not-localize/icon-video.svg){width="30"} [Regarder la vidéo de présentation](#overview-video)

## Créer un parcours

Sous **[!UICONTROL Gestion des Parcours]** dans le volet de navigation de gauche, sélectionnez le type de parcours à créer :

* **[!UICONTROL parcours de compte]**
* **[!UICONTROL parcours de personne]** (Beta)

_Pour ajouter un nouveau parcours :_

+++Parcours de compte

1. Cliquez sur **[!UICONTROL Créer un Parcours de compte]** en haut à droite de la page.

1. Dans la boîte de dialogue, saisissez un **[!UICONTROL Nom]** unique (obligatoire) et un **[!UICONTROL Description]** (facultatif).

   ![ Boîte de dialogue Créer un Parcours de compte ](./assets/account-journey-create-dialog.png){width="400"}

1. Cliquez sur **[!UICONTROL Créer]**.

+++

+++Parcours Personne (Beta)

1. Cliquez sur **[!UICONTROL Créer un Parcours]** en haut à droite de la page.

1. Dans la boîte de dialogue, saisissez un **[!UICONTROL Nom]** unique (obligatoire) et un **[!UICONTROL Description]** (facultatif).

   ![ Boîte de dialogue Créer un Parcours ](./assets/person-journey-create-dialog.png){width="400"}

1. Cliquez sur **[!UICONTROL Créer]**.

+++

## Blocs de création pour la conception de parcours

La carte de parcours __ est la zone centrale de l&#39;espace de travail de parcours. C’est dans cette zone que vous pouvez ajouter des nœuds de parcours et les configurer. Cliquez sur un nœud pour ouvrir son volet Propriétés à droite de la zone de travail et définissez-le en fonction de votre conception. Un parcours commence toujours par un nœud d’audience, où vous pouvez définir l’entrée de votre parcours :

* [Nœud d’audience de compte](./account-audience-nodes.md)
* [Nœud d’audience de personne](./person-audience-nodes.md)

Après avoir créé un parcours de compte et ajouté l’audience, créez le parcours à l’aide de nœuds . La carte de parcours fournit une zone de travail, où vous pouvez créer vos cas d’utilisation marketing B2B à plusieurs étapes à l’aide des types de nœuds suivants pour créer un parcours de compte :

* [Entreprendre une action](./action-nodes.md)
* [Écouter un événement](./listen-for-event-nodes.md)
* [Chemins partagés](./split-merge-paths-nodes.md)
* [Attendre](./wait-nodes.md)
* [Fusionner les chemins](./split-merge-paths-nodes.md)

## Mécanismes de sécurisation

Pour vous aider à créer un parcours sans rencontrer d’erreur, les barrières de sécurité suivantes sont en place :

* _Suppression d’un nœud de chemin de division_ : la suppression d’un nœud nécessite la suppression de tous les nœuds suivants dans chaque chemin.
* _Suppression d’un nœud de fusion_ : un nœud de fusion ne peut être supprimé que lorsqu’un chemin d’accès lui est connecté. Pour supprimer un nœud de fusion, ne laissez qu’un seul chemin sélectionné.
* _Basculer entre le compte et les personnes_ : si vous choisissez comptes dans personnes, tous les nœuds suivants sont supprimés dans chaque chemin.

## Ajouter un nœud

1. Accédez à la carte du parcours.

1. Cliquez sur l’icône plus ( **+** ) sur le chemin d’accès et sélectionnez le type de nœud.

1. Définissez les propriétés du nœud sur la droite.

## Suppression d’un nœud

1. Accédez à la carte du parcours.

1. Dans les propriétés du nœud sur la droite, cliquez sur l’icône _Supprimer_ ( ![icône Supprimer](../assets/do-not-localize/icon-delete.svg) ).

1. Dans la boîte de dialogue de conformation, cliquez sur **[!UICONTROL Supprimer]**.

## Ajouter et supprimer un chemin d’accès

1. Accédez à la carte du parcours.

1. Cliquez sur l’icône plus ( **+** ) sur le chemin d’accès et ajoutez le [nœud de chemin de fractionnement](./split-merge-paths-nodes.md#split-paths).

1. Dans les propriétés du nœud sur la droite, sélectionnez **[!UICONTROL Compte]**.

1. Pour ajouter d’autres chemins d’accès, cliquez sur **[!UICONTROL Ajouter un chemin]**.

   Pour chaque chemin d’accès créé dans le parcours, une nouvelle carte de chemin d’accès s’affiche dans les propriétés.

1. Accédez à l’un des chemins d’accès du parcours et ajoutez des nœuds [action](./action-nodes.md) ou [event](./listen-for-event-nodes.md) à ce chemin d’accès à l’aide de l’icône plus.

1. Sélectionnez le nœud [chemin de partage](./split-merge-paths-nodes.md) pour ouvrir les propriétés sur la droite.

   Les chemins comportant des nœuds ne peuvent pas être supprimés.

1. Pour supprimer ces chemins d’accès, vous devez d’abord supprimer tous les nœuds qu’ils contiennent.

## Planifier un parcours

Lorsque vous publiez un parcours, il peut commencer immédiatement ou à une date ultérieure planifiée. La date de fin peut être fixée à un maximum de trois ans à compter de la date de début. Une fois le parcours publié (statut _En ligne_), vous pouvez mettre à jour la date de fin du parcours, mais pas sa date de début.

1. Accédez à la carte du parcours.

1. Planifiez votre parcours en cliquant sur **[!UICONTROL Paramètres du Parcours]** dans l’en-tête.

1. Dans la boîte de dialogue, définissez les options de planification :

   * Choisissez un type de planning.

     Pour activer le parcours au moment de la publication, choisissez **[!UICONTROL Immédiatement]**.

     Pour activer le parcours à une date ultérieure, choisissez **[!UICONTROL À une date spécifique]** et cliquez sur l’icône _Calendrier_ pour sélectionner la date.

     Boîte de dialogue des paramètres du Parcours ![](./assets/account-journey-settings-dialog.png){width="400" zoomable="no"}

   * Spécifiez la **[!UICONTROL Date de fin]** pour le parcours. Il peut s’agir d’un maximum de trois ans à compter de la date de début (ce champ est obligatoire pour la publication).

1. Cliquez sur **[!UICONTROL Enregistrer]**

   Lorsque vous êtes prêt à publier votre parcours, vous pouvez consulter ces paramètres en cliquant sur _[!UICONTROL Publier]_.

## Publier un parcours

Vous pouvez publier un parcours en l’absence d’erreur de blocage. Une fois le parcours publié, son statut passe à _Actif_. Si le parcours comporte des erreurs, le bouton _[!UICONTROL Publier]_ est grisé avec les informations de contenu : `Resolve errors before publishing`.

>[!NOTE]
>
>Après la publication d’un parcours de compte, les comptes admissibles mettent jusqu’à 24 heures pour entrer dans le parcours.

1. Dans la partie supérieure droite de la carte des parcours, cliquez sur **[!UICONTROL Publier]**.

1. Dans la boîte de dialogue _[!UICONTROL Vérifier les paramètres du parcours]_, définissez les options de début du parcours.

   Si vous avez déjà défini les paramètres de parcours pour définir une planification, passez en revue les paramètres.

   Si vous devez définir l’activation du parcours, choisissez un type de planification :

   * Pour activer le parcours au moment de la publication, choisissez **[!UICONTROL Immédiatement]**.

   * Pour activer le parcours à une date ultérieure, choisissez **[!UICONTROL À une date spécifique]** et cliquez sur l’icône _Calendrier_ pour sélectionner la date.

1. Si nécessaire, spécifiez la **[!UICONTROL date de fin]** pour le parcours.

   Boîte de dialogue des paramètres du Parcours ![](./assets/journey-publish-dialog.png){width="400" zoomable="no"}

   Il peut s’agir d’un maximum de trois ans à compter de la date de début (ce champ est obligatoire pour la publication).

1. Cliquez sur **[!UICONTROL Suivant]**.

1. Dans la boîte de dialogue de confirmation, cliquez sur **[!UICONTROL Publier]**.

## Vidéo de présentation

>[!VIDEO](https://video.tv.adobe.com/v/3443204/?learn=on)
