---
title: rentrée de parcours
description: Contrôlez quand et à quelle fréquence les comptes peuvent entrer à nouveau dans le même parcours de compte.
feature: Account Journeys
role: User
level: Intermediate
exl-id: e5153125-6d5b-4835-bd19-c9b7ce67e46a
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
subfeature_v2: id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: d00e9f03-e50b-4162-b143-0c0817c937c2
autotag-review: '2026-04-29T23:21:59.633Z'
source-git-commit: 7cd6c4ecfbbd3a86b4f30d1b4fe6f06655a9c4f5
workflow-type: tm+mt
source-wordcount: 419
ht-degree: 9%

---

# rentrée de parcours

parcours de compte uniquement **__**

Lorsque vous activez la rentrée pour un parcours de compte, vous pouvez contrôler quand et à quelle fréquence un compte peut entrer à nouveau dans le même parcours. Utilisez les paramètres de rentrée pour définir des critères, des limites et des temps d’attente afin que les comptes soient à nouveau qualifiés pour le parcours de manière contrôlée.

Un compte peut être requalifié pour un parcours lorsque les éléments suivants sont vrais :

* Le compte ne dépasse pas le nombre de nouvelles saisies autorisées pour le parcours.
* Le compte a atteint le seuil de temps d’attente (temps d’attente minimum avant de pouvoir être requalifié).
* Le compte n’est pas actuellement dans le parcours.

## Activer la rentrée pour un parcours de compte

Vous pouvez activer la rentrée et modifier les paramètres de rentrée lorsque le parcours a le statut _Brouillon_.

1. Ouvrez le brouillon de parcours de compte.

1. Cliquez sur le menu **[!UICONTROL Plus...]** en haut à droite et choisissez **[!UICONTROL Rentrée]**.

   ![Clic sur Plus en haut à droite](./assets/account-journey-draft-more-menu.png){width="450"}

1. Dans la boîte de dialogue _[!UICONTROL Rentrée de Parcours]_, activez l’option **[!UICONTROL Activer la reprise]**.

   Lorsque la fonction est activée, les options de minutage, de délai et de limites s’affichent.

   Boîte de dialogue de rentrée de Parcours ![avec fonctionnalité activée](./assets/journey-re-entry-dialog-enabled.png){width="450"}

1. Pour **[!UICONTROL Délai de rentrée]**, choisissez le mode de calcul de l’attente :

   * **[!UICONTROL Attente de la fin du parcours]** - La période d’attente commence lorsque le compte se ferme ou termine le parcours. Par exemple, « 30 jours après que le compte a terminé le parcours, il peut saisir à nouveau ».

   * **[!UICONTROL Attente depuis le début du parcours]** - La période d’attente est basée sur la date à laquelle le compte a rejoint le parcours pour la première fois. Par exemple, « 30 jours à partir du moment où le compte a commencé le parcours, il peut saisir à nouveau ».

1. Définissez le **[!UICONTROL délai de reprise]**, qui correspond à la durée d’attente en heures ou en jours.

   Ce paramètre détermine la durée pendant laquelle un compte doit attendre après avoir quitté ou démarré le parcours avant de pouvoir entrer à nouveau.

1. Définissez la **[!UICONTROL limite d’entrée]** pour définir le nombre maximal de fois qu’un compte est autorisé à entrer dans le parcours.

   Lorsqu’un compte atteint la limite, il n’est plus éligible tant que la limite n’a pas été réinitialisée ou que le parcours n’a pas été republié avec une nouvelle limite.

   Cette limite s’applique par compte pour ce parcours.

1. Cliquez sur **[!UICONTROL Enregistrer]**

## Progression et activité du compte

Pour un parcours de compte publié, la carte de parcours affiche [progression du compte](./journeys-overview.md#review-account-progression) pour les nœuds de parcours. Chaque nœud de la carte affiche le nombre de comptes à atteindre ce nœud et, pour les parcours actifs, le nombre de comptes actuellement sur ce nœud. Chaque fois qu’un compte entre à nouveau dans un parcours, il est comptabilisé comme une entrée distincte.

<!-- 
You can see how many times accounts have entered the journey. ?? 

When you drill in to [account details](../accounts/account-details.md), the account activity shows each time the account entered the journey. It includes explicit activity and a recurrence count so that you can see re-entries clearly.
-->
