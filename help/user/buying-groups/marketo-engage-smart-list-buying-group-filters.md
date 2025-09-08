---
title: Filtres de groupe d'achat dans l'engagement de marché
description: Filtrez les prospects en achetant l’appartenance à un groupe dans les listes dynamiques Marketo Engage afin d’optimiser les campagnes et la notation des prospects avec Journey Optimizer B2B edition.
feature: Buying Groups, Integrations
role: User
exl-id: b137e787-808e-4d36-8e8b-a1c7b999f8a2
source-git-commit: 6f141e08066097c3b5e991e27b6177148fad1fff
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 1%

---

# Filtres de groupe d’achat dans Market Engage

En tant que spécialiste marketing, vous pouvez supprimer des campagnes dans Marketo Engage pour les personnes qui font partie de groupes d’achat dans Journey Optimizer B2B edition. Vous pouvez également informer les workflows de notation des leads dans Marketo Engage à l’aide d’informations sur les leads associés aux groupes d’achats. Par exemple :

* Ce prospect fait-il partie d&#39;un groupe d&#39;achat ?
* Le groupe d&#39;achat est-il complet et engagé ?

Si ces conditions sont vraies, vous pouvez choisir de marquer le lead le plus élevé. Si ce n’est pas le cas, vous pouvez choisir de ne pas le marquer comme un prospect qualifié pour le marketing (MQL).

Dans votre instance Marketo Engage connectée à Journey Optimizer B2B edition, vous pouvez utiliser le filtre _[!UICONTROL Membre du groupe d’achat]_ dans vos listes dynamiques pour identifier ces prospects en fonction de votre stratégie de campagne.

1. Après avoir [créé une liste dynamique dans Marketo Engage](https://experienceleague.adobe.com/fr/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/creating-a-smart-list/create-a-smart-list){target="_blank"}, sélectionnez l’onglet **[!UICONTROL Liste dynamique]** pour ouvrir l’éditeur de filtres.

1. Dans la liste de filtres située à droite, faites défiler la liste vers le bas et développez le dossier **[!UICONTROL Filtres spéciaux]**.

1. Cliquez sur le filtre **[!UICONTROL Membre du groupe d&#39;achat]** et faites-le glisser sur la zone de définition du filtre.

   ![Ajouter le filtre Membre du groupe d&#39;achat à la liste dynamique](./assets/me-member-of-buying-group-filter-add.png){width="700" zoomable="yes"}

1. Définissez l&#39;option _[!UICONTROL Membre du groupe d&#39;achat]_ sur **[!UICONTROL true]** ou **[!UICONTROL false]**.

   Cette contrainte est requise pour la définition.

1. (Facultatif) Ajoutez au filtre d’autres contraintes liées aux groupes d’achats en fonction de la manière dont vous souhaitez identifier les prospects pour la liste dynamique.

   * Cliquez sur **[!UICONTROL Ajouter une contrainte]** en haut à droite de la carte de filtre.

     ![Sélectionner une autre contrainte](./assets/me-member-of-buying-group-filter-add-constraint.png){width="700" zoomable="yes"}

   * Sélectionnez la contrainte à ajouter, par exemple _Score de complétion_ ou _Intérêt de la solution_.

   * Définissez l’évaluation que vous souhaitez utiliser pour une correspondance. Pour un score, vous pouvez utiliser une correspondance exacte ou une plage supérieure ou inférieure au nombre que vous avez entré.

     Pour un élément discret, tel que les centres d’intérêt des solutions définis dans Journey Optimizer B2B edition, vous pouvez sélectionner un ou plusieurs éléments pour la liste.

     ![Sélectionnez une valeur pour la contrainte dans la liste](./assets/me-member-of-buying-group-filter-constraint-list.png){width="600" zoomable="yes"}

     Sélectionnez le premier et cliquez de nouveau sur le sélecteur pour ouvrir la boîte de dialogue _[!UICONTROL Sélecteur de valeurs multiples]_.

     ![Sélection de plusieurs valeurs pour la contrainte](./assets/me-member-of-buying-group-filter-constraint-multiple-value.png){width="500" zoomable="yes"}

     Déplacez l’un des éléments restants vers la droite et cliquez sur **[!UICONTROL OK]** lorsque vous disposez de la liste des éléments à utiliser pour la contrainte.

   * Répétez ces actions pour ajouter autant de contraintes que nécessaire.

   ![Filtre Membre du groupe d&#39;achat avec contraintes multiples](./assets/me-member-of-buying-group-filter-constraints-complete.png){width="600" zoomable="yes"}
