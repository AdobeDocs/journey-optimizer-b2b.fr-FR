---
title: Listes de personnes
description: Découvrez les listes de personnes et comment les parcourir, les afficher, les modifier, les supprimer et les utiliser dans Journey Optimizer B2B Edition.
feature: Audiences
role: User
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
    internal-label: Audience segmentation
source-git-commit: d713d57bddf2ac6f8cf7e7a7d163281f607d729c
workflow-type: tm+mt
source-wordcount: '880'
ht-degree: 1%
---

# Listes de personnes

Dans [!DNL Journey Optimizer B2B Edition], une liste de personnes est une collection nommée de profils de personnes que vous pouvez réutiliser dans vos parcours. Au lieu de recréer le même ensemble de filtres dans chaque parcours, définissez une fois le groupe de personnes et référencez-le où vous en avez besoin. Par exemple, utilisez une liste de personnes pour exclure le personnel interne ou les clients existants d’un parcours d’éducation ou pour suivre les personnes qui ont terminé une étape dans un parcours afin qu’un autre parcours puisse agir sur elles.

Il existe deux types de listes de personnes :

* **[!UICONTROL Statique]** - L’appartenance ne change que lorsque vous ajoutez ou supprimez explicitement des personnes. Vous pouvez ajouter des personnes en appliquant un jeu de filtres afin de renseigner la liste en fonction des données de personne actuelles, ou ajouter et supprimer des personnes par le biais d’un compte ou d’un parcours de personne. Voir [Listes de personnes statiques](./people-lists-static.md).
* **[!UICONTROL Dynamique]** - Vous définissez un ensemble de règles (filtres) pour traiter automatiquement la liste. La liste s’actualise dynamiquement à mesure que les personnes deviennent qualifiées ou disqualifiées pour la définition de règles. Voir [Listes de personnes dynamiques](./people-lists-dynamic.md).

Vous pouvez [utiliser des listes de personnes dans des parcours de compte et des parcours de personne](./people-lists-journeys.md) pour fractionner les chemins en fonction de l’appartenance à une liste et pour ajouter des personnes aux listes statiques ou en supprimer.

>[!NOTE]
>
>Les listes de personnes incluent les profils de personnes qui sont déjà synchronisés et disponibles dans [!DNL Journey Optimizer B2B Edition]. Les profils ne sont pas lus directement à partir des audiences [!DNL Adobe Experience Platform] lors de l’évaluation de la liste.

## Accès et navigation dans les listes de personnes {#access-browse}

Accédez aux listes de personnes à partir du volet de navigation de gauche pour afficher, créer et gérer l’appartenance à une liste.

>[!AVAILABILITY]
>
>Les autorisations de produit suivantes contrôlent l’accès aux listes de personnes :
>
>* [!UICONTROL Gérer les listes de personnes B2B] - Afficher, créer, modifier et supprimer des listes de personnes.
>* [!UICONTROL Afficher les listes de personnes B2B] - Affichez les listes de personnes et leurs membres (lecture seule).
>
>Pour plus d&#39;informations sur l&#39;attribution d&#39;autorisations, voir [Accès et autorisations utilisateur](../admin/user-management.md#b2b-product-permissions).

* Dans le volet de navigation de gauche, développez **[!UICONTROL Comptes]** et sélectionnez **[!UICONTROL Listes de personnes]**.

* Sélectionnez **[!UICONTROL Listes dynamiques]** ou **[!UICONTROL Listes statiques]** pour basculer entre les deux types de liste.

* Saisissez du texte dans le champ _Rechercher_ en haut de la liste pour filtrer la liste affichée par nom.

  ![Accéder aux listes de personnes pour gérer vos audiences au niveau de la personne](./assets/people-lists-browse-search.png){width="800" zoomable="yes"}

* Cliquez sur l’icône _Paramètres de colonne_ ( ![Icône des paramètres de colonne](../assets/do-not-localize/icon-column-settings-new.svg) ) dans le coin supérieur droit pour sélectionner ou effacer les colonnes affichées.

* Pour modifier la largeur d’une colonne, faites glisser le séparateur entre les en-têtes de colonne.

Chaque onglet comprend les colonnes **[!UICONTROL Nom]**, **[!UICONTROL Dernière mise à jour]**, **[!UICONTROL Mis à jour par]**, **[!UICONTROL Créé le]** et **[!UICONTROL Créé par]**. Cliquez sur le nom de la liste des personnes pour en afficher les détails.

À partir de cette page, vous pouvez également effectuer les opérations suivantes :

* Créer des listes dynamiques et statiques.
* Ouvrez une liste et [vérifiez les membres actuels](#view-list-members).
* Cliquez sur l’icône _Autres actions_ ( **...** ) d’une liste et choisissez de la [modifier](#edit-list-properties) ou [supprimer](#delete-people-list).

## Créer une liste de personnes {#create-people-list}

1. Cliquez sur **[!UICONTROL Créer une liste]** en haut à droite de la page _[!UICONTROL Listes de personnes]_.

   ![Boîte de dialogue Créer une liste de personnes](./assets/people-list-create-dialog.png){width="450"}

1. Saisissez un **[!UICONTROL Nom]** (obligatoire) et une **[!UICONTROL Description]** (facultatif) pour la liste.

   Le nom peut contenir jusqu’à 180 caractères et doit être unique parmi les listes du même type. La description peut contenir jusqu’à 2 000 caractères.

1. Choisissez la liste **[!UICONTROL Type]** :

   * [**[!UICONTROL Statique]**](./people-lists-static.md) - Les filtres de qualification déterminent l’appartenance lorsque vous les appliquez à la liste. Les mises à jour d’appartenance uniquement lorsque vous ajoutez manuellement des personnes ou qu’un parcours les ajoute ou les supprime.
   * [**[!UICONTROL Dynamique]**](./people-lists-dynamic.md) - Les filtres de qualification déterminent dynamiquement l’appartenance. L’appartenance est automatiquement actualisée.

1. Cliquez sur **[!UICONTROL Créer]**.

   La nouvelle liste de personnes s’ouvre sur sa page de détails, et l’éditeur de filtres s’ouvre afin que vous puissiez définir les personnes de la liste. Pour ajouter des personnes à une liste statique, appliquez un ou plusieurs filtres. Pour une liste dynamique, définissez les règles d’appartenance à la liste.

## Afficher les membres de la liste {#view-list-members}

Sur la page de détails d’une liste de personnes, la liste **[!UICONTROL Membres]** affiche les personnes de la liste. Le nombre total de personnes dans la liste s’affiche en haut du tableau.

Le tableau des membres comprend les colonnes suivantes :

* **[!UICONTROL Nom]**
* **[!UICONTROL Adresse e-mail]**
* **[!UICONTROL Fonction]**
* **[!UICONTROL Société]**
* **[!UICONTROL Désabonné]**
* **[!UICONTROL Créé le]**
* **[!UICONTROL Dernière modification]**

Par défaut, le système trie les membres par **[!UICONTROL Dernière modification]**, en commençant par les personnes modifiées le plus récemment. Vous pouvez également trier par **[!UICONTROL Nom]**, **[!UICONTROL Adresse électronique]** ou **[!UICONTROL Créé le]**.

* Pour trouver un membre spécifique, utilisez le champ _Rechercher_. Vous pouvez effectuer une recherche par prénom, adresse e-mail ou société.
* Pour choisir les colonnes à afficher, cliquez sur l’icône _Paramètres des colonnes_ et cochez ou décochez les cases. La colonne _[!UICONTROL Name]_ est toujours affichée.
* Pour afficher le dernier abonnement, utilisez le menu _[!UICONTROL Plus]_ pour choisir **[!UICONTROL Actualiser les membres]**.
* Pour afficher des informations supplémentaires sur une personne, cliquez sur son nom pour ouvrir la page [détails de la personne](../accounts/person-details.md), où vous pouvez afficher son résumé et ses activités récentes.

## Modifier les propriétés de la liste de personnes {#edit-list-properties}

Vous pouvez modifier le nom et la description d’une liste de personnes statique ou dynamique.

1. Ouvrez la boîte de dialogue _[!UICONTROL Modifier la liste]_ à l’aide de l’une des méthodes suivantes :

   * Sur la page _[!UICONTROL Listes de personnes]_, cliquez sur l’icône _Plus d’actions_ ( **...** ) de la liste et sélectionnez **[!UICONTROL Modifier]**.
   * Sur la page de détails de la liste, cliquez sur **[!UICONTROL Modifier les propriétés de la liste]**.

1. Mettez à jour le **[!UICONTROL nom]** ou la **[!UICONTROL description]**.

1. Cliquez sur **[!UICONTROL Enregistrer]**

## Supprimer une liste de personnes {#delete-people-list}

>[!IMPORTANT]
>
>La suppression d’une liste de personnes est définitive et irréversible. Vous ne pouvez pas supprimer une liste de personnes utilisée par un parcours actif.

1. Supprimez la liste à l’aide de l’une des méthodes suivantes :

   * Sur la page _[!UICONTROL Listes des personnes]_, cliquez sur l’icône _Plus d’actions_ ( **...** ) à côté du nom de la liste et sélectionnez **[!UICONTROL Supprimer]**.
   * Sur la page de détails de la liste, cliquez sur **[!UICONTROL Supprimer la liste]**.

1. Dans la boîte de dialogue de confirmation, cliquez sur **[!UICONTROL Supprimer]**.
