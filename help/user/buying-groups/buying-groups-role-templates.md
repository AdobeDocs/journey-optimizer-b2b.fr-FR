---
title: Modèles de rôle de groupe d’achat
description: Découvrez comment définir un modèle de rôle à utiliser comme composant de groupe d’achats.
feature: Buying Groups
exl-id: 9206356e-e9cf-486c-8982-c7d893222413
source-git-commit: 19633e2676c3e9d747a1e65bfc48a3ba421674b9
workflow-type: tm+mt
source-wordcount: '857'
ht-degree: 1%

---

# Modèles de rôle de groupe d’achat

Dans un marché B2B, les décisions d’achat sont généralement prises par plusieurs individus. Ces personnes participent au processus décisionnel en fonction de leur rôle au sein de l’organisation. Créez des modèles de rôle Groupe d’achat qui contiennent ces définitions de rôle en fonction de chaque cas d’utilisation de type d’offre de produit ou de compte.

## Accès et navigation dans les modèles de rôle

1. Sur la page d’accueil de Adobe Experience Platform, cliquez sur Adobe Journey Optimizer B2B Edition.

1. Dans le volet de navigation de gauche, cliquez sur **[!UICONTROL Groupes d’achats]**.

1. Sur la page _[!UICONTROL Groupes d&#39;achats]_, sélectionnez l&#39;onglet **[!UICONTROL Modèles de rôles]** .

   ![Onglet Modèles de rôles](assets/roles-templates-tab.png){width="700" zoomable="yes"}

   Cet onglet contient un inventaire de tous les modèles de rôles existants, avec les colonnes suivantes :

   * [!UICONTROL Nom]
   * [!UICONTROL Statut]
   * [!UICONTROL Date de création]
   * [!UICONTROL Créé par]
   * [!UICONTROL Dernière mise à jour]
   * [!UICONTROL Dernière mise à jour par]
   * [!UICONTROL Publié le ]
   * [!UICONTROL Publié par]

   La liste est triée par défaut par la colonne _[!UICONTROL Dernière mise à jour]_ .

   Le nombre de modèles de rôles _live_ (publié) s’affiche en haut à droite de la page. Tous les modèles de rôles ont un état `Draft` ou `Live`.

1. Pour filtrer la liste par nom, utilisez le champ de recherche situé en haut de la liste.

   Saisissez les premiers caractères du nom pour réduire la liste affichée aux éléments correspondants.

   ![Filtrage des modèles de rôles par chaîne de recherche](assets/roles-templates-search.png){width="700" zoomable="yes"}

## Création d’un modèle de rôles

1. Dans l’onglet _[!UICONTROL Modèles de rôles]_, cliquez sur **[!UICONTROL Créer un modèle]** dans le coin supérieur droit.

1. Dans la boîte de dialogue, saisissez un **[!UICONTROL Nom]** unique (obligatoire) et une **[!UICONTROL Description]** (facultatif) pour le modèle.

   ![Boîte de dialogue Créer un modèle de rôles](assets/roles-template-create-dialog.png){width="400"}

1. Ajoutez une règle pour chaque rôle que vous souhaitez définir pour le modèle.

   * Sélectionnez le **[!UICONTROL rôle de groupe d’achat]** dans la liste.

     Pour la version actuelle, il existe six rôles : `Decision Maker`, `Influencer`, `Practitioner`, `Executive Steering Committee`, `Champion` et `Other`.

     ![Liste des rôles de groupe d’achat](./assets/roles-template-create-roles-list.png){width="700" zoomable="yes"}

   * Définissez la **[!UICONTROL pondération]** pour le rôle, qui est utilisé pour calculer le score d’engagement.

     La valeur de chaque option est traduite en pourcentage pour le calcul du score : [!UICONTROL Trivial] = 20, [!UICONTROL Mineur] = 40, [!UICONTROL Normal] = 60, [!UICONTROL Important] = 80, et [!UICONTROL Vital] = 100.

     Par exemple, un modèle de rôle avec des rôles utilisant des rôles Vital, Important et Normal, est ensuite converti en 100/240, 80/240, 60/240.

   * **[!UICONTROL Ajouter des conditions pour l’affectation automatique]** - Cochez cette case pour ajouter des conditions pour l’affectation automatique de membres au groupe d’achats qui correspondent à la condition. Si la case à cocher n’est pas cochée, l’ajout de conditions n’est PAS obligatoire.

   * **[!UICONTROL Obligatoire pour le score d’exhaustivité]** - Cochez cette case pour le rôle si vous souhaitez qu’il soit nécessaire pour calculer un score d’exhaustivité. —>

   * Cliquez sur **[!UICONTROL Ajouter une condition]**.

      * Dans la boîte de dialogue de condition, développez la liste des **[!UICONTROL attributs de personne]** et recherchez un attribut que vous souhaitez utiliser pour correspondre au rôle. Faites-la glisser à droite et déposez-la dans l’espace de filtrage.

        ![ Le modèle de rôles ajoute l’attribut de glisser-déposer de condition ](assets/roles-template-role-attribute.png){width="700" zoomable="yes"}

      * Utilisez l’attribut pour créer un filtre correspondant utilisant une ou plusieurs valeurs.

        Dans l’exemple suivant, l’attribut Job title est utilisé pour identifier une correspondance pour Decision Maker. Toute valeur pour le titre commençant par `Director` ou `Sr Director` est évaluée comme true pour la condition.

        ![Exemple de condition de modèle de rôles utilisant le titre de la tâche](assets/roles-template-condition-example-job-title.png){width="700" zoomable="yes"}

      * Si nécessaire, ajoutez un autre attribut et une condition qui affine davantage les critères pour qu’une correspondance soit établie avec le rôle.

      * Cliquez sur **[!UICONTROL Terminé]**.

   Pour chaque rôle supplémentaire que vous souhaitez inclure pour le modèle, cliquez sur **[!UICONTROL Ajouter un autre rôle]** et définissez une ou plusieurs conditions correspondant au rôle.

   ![ Modèle de rôles avec plusieurs rôles définis](assets/roles-template-multiple-roles.png){width="700" zoomable="yes"}

1. Si le modèle est prêt à l’emploi, cliquez sur **[!UICONTROL Publish]** en haut à droite.

   La publication du modèle le définit sur un état _Live_ et le rend disponible pour être associé à un intérêt de solution. Il doit y avoir au moins un rôle défini pour publier le modèle de rôles.

   Vos modifications sont automatiquement enregistrées à l’état _Brouillon_ . Si vous n’êtes pas prêt à publier le modèle de rôles, cliquez sur la flèche vers la gauche (arrière) en haut de la page et revenez à la liste Modèles de rôles .

## Modification d’un modèle de rôles de brouillon

Lorsqu’un modèle de rôles se trouve dans un état _Draft_, vous pouvez continuer à modifier les rôles définis. Toutes les modifications que vous apportez sont automatiquement enregistrées.

Modifiez les paramètres de l’en-tête de la carte des rôles, y compris le rôle du groupe d’achat, la pondération, l’affectation automatique et l’exigence de notation de l’exhaustivité.

![Modification des propriétés de rôle de groupe d’achat](./assets/roles-template-role-properties.png){width="600"}

### Modification des filtres pour un rôle

Pour modifier la logique de filtrage de l’un des rôles, cliquez sur l’icône _Modifier_ (crayon) en haut à droite de la carte de rôle. Cette action ouvre l’espace de travail _[!UICONTROL Conditions]_ où vous pouvez modifier un filtre existant, ajouter un autre filtre, supprimer un filtre ou modifier la logique du filtre.

### Suppression d’une carte de rôle

Si vous souhaitez supprimer un rôle du modèle, cliquez sur l’icône _Supprimer_ (corbeille) dans la carte de rôle.

### Définition de la priorité des rôles

Vous pouvez réorganiser les rôles dans le modèle, ce qui détermine la priorité d’attribution des prospects à un rôle. Un contrôleur **[!UICONTROL Priority]** s’affiche à droite de chaque carte de rôle. Cliquez sur la flèche _Haut_ ou _Bas_ à droite pour déplacer la carte de rôle vers le haut ou vers le bas en priorité.

![Modification de la priorité du rôle](./assets/roles-template-role-priority.png){width="700"}

## Suppression d’un modèle de rôles

Vous pouvez supprimer un modèle de rôles s’il se trouve dans l’état _Brouillon_ .

1. Sélectionnez le modèle de rôles dans la liste pour l’ouvrir.

1. Cliquez sur **[!UICONTROL Supprimer]** en haut à droite.

   ![Modification de la priorité du rôle](./assets/roles-template-delete.png){width="700"}

1. Dans la boîte de dialogue, cliquez sur **[!UICONTROL Supprimer]** pour confirmer.
