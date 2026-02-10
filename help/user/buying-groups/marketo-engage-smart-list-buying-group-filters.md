---
title: Filtres de groupe d'achat dans Marketo Engage
description: Filtrez les prospects en achetant l’appartenance à un groupe dans les listes dynamiques Marketo Engage avec des contraintes telles que le score d’exhaustivité pour optimiser les campagnes et le score des prospects.
feature: Buying Groups, Integrations
role: User
exl-id: b137e787-808e-4d36-8e8b-a1c7b999f8a2
source-git-commit: 764ea8631241b8da3cfae4ce59a29b1c82b53f0c
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 1%

---

# Filtres de groupe d’achat dans Marketo Engage

>[!IMPORTANT]
>
>**Obsolescence de fonctionnalités**</br></br>
>
>Avec l’[architecture simplifiée](../simplified-architecture.md) pour Journey Optimizer B2B edition, les filtres de groupe d’achats ne sont plus disponibles dans une instance Marketo Engage connectée.</br></br>
>
>Vous pouvez également créer une liste statique pour chaque solution qui vous intéresse, puis [utiliser l’action _Ajouter à la liste Marketo_](../journeys/action-nodes.md#marketo-engage-actions) à partir d’un nœud de parcours. Cette action ajoute les membres du groupe d&#39;achat à une liste statique particulière dans une instance Marketo Engage connectée. Ensuite, utilisez la liste statique axée sur les intérêts de la solution pour un filtre de liste dynamique.

En tant que spécialiste marketing, vous pouvez supprimer des campagnes dans Marketo Engage pour les personnes qui font partie de groupes d’achat dans Journey Optimizer B2B edition. Vous pouvez également informer les workflows de notation des leads dans Marketo Engage à l’aide d’informations sur les leads associés aux groupes d’achats. Par exemple :

* Ce prospect fait-il partie d&#39;un groupe d&#39;achat ?
* Le groupe d&#39;achat est-il complet et engagé ?

Si ces conditions sont vraies, vous pouvez choisir de noter le prospect le plus haut. Si ce n’est pas le cas, vous pouvez choisir de ne pas le marquer comme un prospect qualifié pour le marketing (MQL).

Dans votre instance Marketo Engage connectée à Journey Optimizer B2B edition, vous pouvez utiliser le filtre _[!UICONTROL Membre du groupe d’achat]_ dans vos listes dynamiques pour identifier ces prospects en fonction de votre stratégie de campagne.

1. Après avoir [créé une liste dynamique dans Marketo Engage](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/creating-a-smart-list/create-a-smart-list){target="_blank"}, sélectionnez l’onglet **[!UICONTROL Liste dynamique]** pour ouvrir l’éditeur de filtres.

1. Dans la liste de filtres située à droite, faites défiler la liste vers le bas et développez le dossier **[!UICONTROL Filtres spéciaux]**.

1. Cliquez sur le filtre **[!UICONTROL Membre du groupe d&#39;achat]** et faites-le glisser sur la zone de définition du filtre.

   ![Ajouter le filtre Membre du groupe d&#39;achat à la liste dynamique](./assets/me-member-of-buying-group-filter-add.png){width="700" zoomable="yes"}

1. Définissez l&#39;option _[!UICONTROL Membre du groupe d&#39;achat]_ sur **[!UICONTROL true]** ou **[!UICONTROL false]**.

   Cette contrainte est requise pour la définition.

1. (Facultatif) Ajoutez au filtre d’autres contraintes liées aux groupes d’achats en fonction de la manière dont vous souhaitez identifier les prospects pour la liste dynamique.

   * Cliquez sur **[!UICONTROL Ajouter une contrainte]** en haut à droite de la carte de filtre.

     ![Sélectionner une autre contrainte](./assets/me-member-of-buying-group-filter-add-constraint.png){width="700" zoomable="yes"}

   * Sélectionnez la contrainte à ajouter, par exemple _Score de complétion_ ou _Intérêt de la solution_.

   * Définissez l’évaluation que vous souhaitez utiliser pour une correspondance.

     Pour un score, vous pouvez utiliser une correspondance exacte ou une plage supérieure ou inférieure au nombre que vous avez entré.

     Pour exclure des membres qui ont été supprimés d&#39;un groupe d&#39;achats, utilisez la contrainte _[!UICONTROL Est supprimé]_ définie sur `false`. Vous pouvez également inclure explicitement des membres supprimés dans la liste dynamique en définissant cette contrainte sur `true`.

     Pour un élément discret, tel que les centres d’intérêt des solutions définis dans Journey Optimizer B2B edition, vous pouvez sélectionner un ou plusieurs éléments pour la liste.

     ![Sélectionnez une valeur pour la contrainte dans la liste](./assets/me-member-of-buying-group-filter-constraint-list.png){width="600" zoomable="yes"}

     Sélectionnez le premier et cliquez de nouveau sur le sélecteur pour ouvrir la boîte de dialogue _[!UICONTROL Sélecteur de valeurs multiples]_.

     ![Sélection de plusieurs valeurs pour la contrainte](./assets/me-member-of-buying-group-filter-constraint-multiple-value.png){width="500" zoomable="yes"}

     Déplacez l’un des éléments restants vers la droite et cliquez sur **[!UICONTROL OK]** lorsque vous disposez de la liste des éléments à utiliser pour la contrainte.

   * Répétez ces actions pour ajouter autant de contraintes que nécessaire.

   ![Filtre Membre du groupe d&#39;achat avec contraintes multiples](./assets/me-member-of-buying-group-filter-constraints-complete.png){width="600" zoomable="yes"}
