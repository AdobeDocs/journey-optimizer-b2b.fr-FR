---
title: Créer et publier un Parcours
description: Créez des parcours de compte et de personne dans la zone de travail visuelle, ajoutez des nœuds d’action et d’événement, configurez la planification et publiez pour l’orchestration en direct dans Journey Optimizer B2B Edition.
feature: Account Journeys
role: User
exl-id: f536b1a1-8dfe-437f-a84d-b66879529621
autotag-review: 2026-03-30T23:14:46.843Z
TQID: 'https://experienceleague.adobe.com/-emMaxlrae40JXP0tThacD3xA27d5OzO8tX6o-mOnfg'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
subfeature_v2:
  - id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
    internal-label: Account Journeys
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
source-git-commit: 9d5641659907d61be992ed218088a023a5211c56
workflow-type: tm+mt
source-wordcount: '1101'
ht-degree: 5%
---
# Créer et publier un parcours

Pour commencer un nouveau parcours, créez le parcours, puis construisez les nœuds et le flux du parcours dans la carte du parcours.

![Vidéo](../../assets/do-not-localize/icon-video.svg){width="30"} [Regarder la vidéo de présentation](#overview-video)

## Créer un parcours

Sous **[!UICONTROL Gestion des Parcours]** dans le volet de navigation de gauche, sélectionnez le type de parcours à créer :

* **[!UICONTROL parcours de compte]**
* **[!UICONTROL parcours de personne]**

_Pour ajouter un nouveau parcours :_

+++Parcours de compte

1. Cliquez sur **[!UICONTROL Créer un Parcours de compte]** en haut à droite de la page.

1. Dans la boîte de dialogue, saisissez un **[!UICONTROL Nom]** unique (obligatoire) et une **[!UICONTROL Description]** (facultatif).

   ![Boîte de dialogue Créer un Parcours de compte](./assets/account-journey-create-dialog.png){width="400"}

1. Cliquez sur **[!UICONTROL Créer]**.

+++

+++Parcours d’une personne

1. Cliquez sur **[!UICONTROL Créer un Parcours]** en haut à droite de la page.

1. Dans la boîte de dialogue, saisissez un **[!UICONTROL Nom]** unique (obligatoire) et une **[!UICONTROL Description]** (facultatif).

   ![Boîte de dialogue Créer un Parcours](./assets/person-journey-create-dialog.png){width="400"}

1. Cliquez sur **[!UICONTROL Créer]**.

+++

## Composants pour la conception de parcours

La _carte de parcours_ est la zone centrale de l&#39;espace de travail de parcours. C’est dans cette zone que vous pouvez ajouter des nœuds de parcours et les configurer. Cliquez sur un nœud pour ouvrir son volet Propriétés à droite de la zone de travail et définissez-le en fonction de votre conception. Un parcours commence toujours par un nœud d’audience, où vous pouvez définir l’entrée de votre parcours :

* [Nœud d’audience de compte](./account-audience-nodes.md)
* [Nœud d’audience de personne](./person-audience-nodes.md)

Après avoir créé un parcours de compte et ajouté l’audience, concevez le parcours à l’aide de nœuds . La carte de parcours fournit une zone de travail, où vous pouvez créer vos cas d’utilisation marketing B2B à plusieurs étapes à l’aide des types de nœuds suivants pour créer un parcours de compte :

* [Entreprendre une action](./action-nodes.md)
* [Écouter un événement](./listen-for-event-nodes.md)
* [Chemins partagés](./split-merge-paths-nodes.md)
* [Variantes de chemins partagés](./variant-split-paths-nodes.md)
* [Deuxième meilleur chemin](./next-best-path-node.md)
* [Attendre](./wait-nodes.md)
* [Fusionner les chemins](./split-merge-paths-nodes.md)

## Garde-fous

Pour vous aider à créer un parcours sans rencontrer d’erreur, les mécanismes de sécurisation suivants sont en place :

* _Supprimer un nœud de chemin de partage_ : la suppression d’un nœud nécessite la suppression de tous les nœuds suivants dans chaque chemin.
* _Suppression d’un nœud de fusion_ : un nœud de fusion ne peut être supprimé que s’il existe un chemin d’accès qui lui est connecté. Pour supprimer un nœud de fusion, ne laissez qu’un seul chemin sélectionné.
* _Basculer entre les comptes et les personnes_ : si vous sélectionnez comptes en personnes, tous les nœuds suivants de chaque chemin sont supprimés.

## Ajouter un nœud

1. Accédez à la carte du parcours.

1. Cliquez sur l’icône plus ( **+** ) sur le chemin d’accès et choisissez le type de nœud.

   ![Cliquez sur + et choisissez le type pour ajouter le nœud de parcours au chemin d’accès](./assets/node-add-menu.png){width="400" zoomable="no"}

   Les types de nœud disponibles dépendent du type de parcours et du contexte du chemin d’accès. Voir [_nœuds de Parcours_](./journey-nodes.md) pour plus d’informations.

1. Définissez les propriétés du nœud sur la droite.

   Les propriétés dépendent du type de nœud.

## Étiqueter un nœud {#label-a-node}

Dans [!DNL Adobe Journey Optimizer B2B Edition], chaque nœud de la carte de parcours affiche son nom par défaut, tel que _Attente_ ou _Envoyer un e-mail_. Ajoutez des libellés d’affichage pour distinguer les nœuds du même type et identifier l’objectif de chaque étape. Par exemple, utilisez le _message de recharge de 48 heures_ ou l’_e-mail de bienvenue_.

Vous pouvez ajouter un libellé d’affichage à n’importe quel nœud d’un parcours de compte ou d’un parcours de personne.

1. Dans la carte de parcours, sélectionnez le nœud à étiqueter.

1. Dans les propriétés du nœud, saisissez le texte dans le champ **[!UICONTROL Libellé d&#39;affichage]**.

   Le libellé peut contenir 255 caractères maximum.

1. Cliquez en dehors du champ pour appliquer le libellé.

   ![Ajoutez un libellé d&#39;affichage pour distinguer le nœud dans le parcours](./assets/node-display-label.png){width="500" zoomable="no"}

   Le libellé remplace le nom par défaut du nœud dans la carte de parcours.

Pour restaurer le nom par défaut, effacez le champ **[!UICONTROL Afficher le libellé]** et cliquez en dehors du champ.

Lorsque vous publiez le parcours, le libellé affiché pour chaque nœud est enregistré avec le parcours publié.

>[!NOTE]
>
>Les libellés d’affichage ne sont pas disponibles pour les nœuds dans les parcours créés avant cette fonctionnalité.

Les libellés de nœud sont disponibles dans le schéma `AJOB2B - 1.5.4 - journey node` et le jeu de données `AJOB2B-1_5_4-journey_node`. Vous pouvez interroger les libellés dans [!DNL Adobe Experience Platform] et les utiliser pour les rapports dans [!DNL Adobe Customer Journey Analytics]. Pour plus d’informations sur l’interrogation des données exportées, consultez les [conditions préalables à l’interrogation d’un jeu de données](../data/aep-query-examples.md#prerequisites).

## Suppression d’un nœud

1. Accédez à la carte du parcours.

1. Dans les propriétés du nœud sur la droite, cliquez sur l’icône _Supprimer_ ( ![Icône Supprimer](../assets/do-not-localize/icon-delete.svg) ).

1. Dans la boîte de dialogue de confirmation, cliquez sur **[!UICONTROL Supprimer]**.

## Ajouter et supprimer un chemin d’accès

1. Dans la carte de parcours, cliquez sur l’icône plus ( **+** ) sur le chemin d’accès et ajoutez le nœud de chemin de division [&#128279;](./split-merge-paths-nodes.md#split-paths).

1. Dans les propriétés du nœud sur la droite, sélectionnez **[!UICONTROL Compte]**.

1. Pour ajouter d’autres chemins, cliquez sur **[!UICONTROL Ajouter un chemin]**.

   Pour chaque chemin d’accès créé dans le parcours, une nouvelle carte de chemin d’accès s’affiche dans les propriétés.

1. Accédez à l’un des chemins d’accès du parcours et ajoutez les nœuds [action](./action-nodes.md) ou [event](./listen-for-event-nodes.md) à ce chemin d’accès à l’aide de l’icône plus.

1. Sélectionnez le nœud [chemin de partage](./split-merge-paths-nodes.md) pour ouvrir les propriétés sur la droite.

   Les chemins comportant des nœuds ne peuvent pas être supprimés.

1. Pour supprimer un chemin d’accès, vous devez d’abord supprimer tous les nœuds qu’il contient.

## Planifier un parcours

Lorsque vous publiez un parcours, il peut commencer immédiatement ou à une date ultérieure planifiée. La date de fin peut être fixée à un maximum de trois ans à compter de la date de début. Une fois un parcours publié (statut _Actif_), vous pouvez mettre à jour la date de fin du parcours, mais pas sa date de début.

1. Accédez à la carte du parcours.

1. Planifiez votre parcours en cliquant sur **[!UICONTROL Paramètres du Parcours]** dans l’en-tête.

1. Dans la boîte de dialogue, définissez les options de planification :

   * Choisissez un type de planning.

     Pour activer le parcours au moment de la publication, choisissez **[!UICONTROL Immédiatement]**.

     Pour activer le parcours à une date ultérieure, choisissez **[!UICONTROL À une date spécifique]** et cliquez sur l&#39;icône _Calendrier_ pour sélectionner la date.

     ![Boîte de dialogue des paramètres de Parcours](./assets/account-journey-settings-dialog.png){width="400" zoomable="no"}

   * Spécifiez la **[!UICONTROL Date de fin]** pour le parcours. Il peut s’agir d’un maximum de trois ans à compter de la date de début (ce champ est obligatoire pour la publication).

1. Cliquez sur **[!UICONTROL Enregistrer]**

   Lorsque vous êtes prêt à publier votre parcours, vous pouvez consulter ces paramètres en cliquant sur _[!UICONTROL Publier]_.

## Publier un parcours

Vous pouvez publier un parcours en l’absence d’erreur de blocage. Une fois le parcours publié, son statut passe à _Actif_. Si le parcours comporte des erreurs, le bouton _[!UICONTROL Publier]_ est grisé avec les informations de contenu : `Resolve errors before publishing`.

>[!NOTE]
>
>Après la publication d’un parcours de compte, les comptes admissibles mettent jusqu’à 24 heures pour entrer dans le parcours.

1. En haut à droite de la carte des parcours, cliquez sur **[!UICONTROL Publier]**.

1. Dans la boîte de dialogue _[!UICONTROL Vérifier les paramètres de parcours]_, définissez les options de début de parcours.

   Si vous avez déjà défini les paramètres de parcours pour définir une planification, passez en revue les paramètres.

   Si vous devez définir l’activation du parcours, choisissez un type de planification :

   * Pour activer le parcours au moment de la publication, choisissez **[!UICONTROL Immédiatement]**.

   * Pour activer le parcours à une date ultérieure, choisissez **[!UICONTROL À une date spécifique]** et cliquez sur l&#39;icône _Calendrier_ pour sélectionner la date.

1. Si nécessaire, spécifiez la **[!UICONTROL date de fin]** pour le parcours.

   ![Boîte de dialogue des paramètres de Parcours](./assets/journey-publish-dialog.png){width="400" zoomable="no"}

   Il peut s’agir d’un maximum de trois ans à compter de la date de début (ce champ est obligatoire pour la publication).

1. Cliquez sur **[!UICONTROL Suivant]**.

1. Dans la boîte de dialogue de confirmation, cliquez sur **[!UICONTROL Publier]**.

## Vidéo de présentation

>[!VIDEO](https://video.tv.adobe.com/v/3443204/?learn=on)
