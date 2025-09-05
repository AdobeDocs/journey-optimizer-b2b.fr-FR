---
title: Configurer la pondération du score d’engagement
description: Découvrez comment configurer la pondération de score d’engagement personnalisée pour refléter la logique de notation qui s’aligne sur vos stratégies d’entreprise.
feature: Setup, Engagement, Buying Groups
role: Admin
exl-id: 50d79d31-5ad8-41ed-a62b-4aa2ed9e837f
source-git-commit: 855e06e07fff9223c607bce9adde5ef4f4f6b97b
workflow-type: tm+mt
source-wordcount: '890'
ht-degree: 0%

---

# Configurer la pondération du score d’engagement personnalisé

Un score d&#39;engagement du groupe d&#39;achat reflète le niveau d&#39;engagement en évaluant diverses activités enregistrées pour les membres du groupe d&#39;achat. Grâce à la pondération de score personnalisée, les équipes opérationnelles marketing ont la possibilité de définir leurs propres modèles de pondération des activités les plus pertinentes pour l’engagement. Un modèle de notation personnalisé donne une image plus précise de votre pipeline en priorisant les comportements qui signalent le plus précisément l’intention d’achat dans votre processus de vente.

En tant qu’administrateur ou administratrice, vous pouvez définir plusieurs modèles de score d’engagement pour votre organisation, mais un seul modèle peut être actif à la fois. Vous définissez un modèle de score en fonction du poids appliqué à chaque activité de score d’engagement.

## Accéder aux modèles de pondération de score de l’engagement

1. Dans le volet de navigation de gauche, choisissez **[!UICONTROL Administration]** > **[!UICONTROL Configurations]**.

1. Cliquez sur **[!UICONTROL Pondération de score de l’engagement]** dans le panneau intermédiaire pour afficher la liste des modèles de score.

   À partir de cette page, vous pouvez [créer (dupliquer)](#create-an-engagement-score-model), [activer](#activate-a-score-model) et [modifier](#change-the-engagement-weighting-settings) des modèles de score d’engagement.

   ![Accéder aux définitions d’événement configurées](./assets/configuration-engagement-scoring-list.png){width="800" zoomable="yes"}

   Le tableau présente les modèles les plus récemment mis à jour (triés par _[!UICONTROL Dernière mise à jour]_) et offre la possibilité de rechercher par _[!UICONTROL Nom]_.

   Vous pouvez personnaliser le tableau affiché en cliquant sur l’icône _Paramètres des colonnes_ ( ![Paramètres des colonnes](../assets/do-not-localize/icon-column-settings.svg) ) dans le coin supérieur droit, puis en cochant ou décochant les cases des colonnes.

   ![Colonnes à afficher dans la liste de pondération du score d’engagement](./assets/configuration-engagement-scoring-list-columns.png){width="300"}

1. Pour accéder aux détails d’un modèle de score d’engagement, cliquez sur le nom.

### Modèle de score par défaut

Le système crée un modèle de score d’engagement initial nommé _Modèle de pondération des activités 1_, qui est le modèle actif jusqu’à ce que vous créiez votre propre modèle personnalisé et que vous l’activiez. Lorsque vous activez votre modèle personnalisé, le modèle par défaut passe à un statut _Archivé_. Vous pouvez le dupliquer si vous décidez de revenir au modèle de score d’engagement par défaut ou de l’utiliser comme point de départ pour un autre modèle personnalisé.

![Modèle de pondération du score d’engagement par défaut](./assets/configuration-engagement-scoring-model-default.png){width="600" zoomable="yes"}

### Supprimer un modèle de brouillon

Vous pouvez supprimer un modèle de score d’engagement provisoire si vous décidez de ne plus l’activer par la suite. Cliquez sur l’icône _Plus de menu_ (***...***) en regard du nom du modèle de score du brouillon dans la liste, puis choisissez **[!UICONTROL Supprimer]**.

![Supprimer le modèle de score du brouillon](./assets/configuration-engagement-scoring-model-more-delete.png){width="350"}

Dans la boîte de dialogue de confirmation, cliquez sur **[!UICONTROL Supprimer]**.

## Créer un modèle de notation d’engagement personnalisé

Pour créer un modèle de score d’engagement personnalisé, dupliquez le modèle par défaut ou un autre modèle personnalisé déjà créé. Vous pouvez dupliquer le modèle _actif_ actuel, un modèle _Brouillon_ ou un modèle _archivé_. Modifiez ensuite le modèle en double en fonction de vos besoins.

1. Cliquez sur le nom du modèle pour ouvrir la page des détails du modèle, puis cliquez sur **[!UICONTROL Dupliquer]** en haut à droite.

   ![ Dupliquer le modèle actif ](./assets/configuration-engagement-scoring-model-duplicate.png){width="600" zoomable="yes"}

   Vous pouvez également cliquer sur l’icône _Plus_ (***...***) en regard du nom du modèle de score dans la liste et choisir **[!UICONTROL Dupliquer]**.

   ![Utilisez le menu Plus pour dupliquer le modèle actif](./assets/configuration-engagement-scoring-model-more-duplicate.png){width="325"}

1. Dans la boîte de dialogue _Dupliquer_, saisissez un nom unique pour le modèle dupliqué et cliquez sur **[!UICONTROL Dupliquer]**.

   ![Confirmer pour dupliquer le modèle de score](./assets/configuration-engagement-scoring-model-duplicate-dialog.png){width="500"}

   Le modèle dupliqué s’affiche dans la liste avec un statut _Brouillon_. Cliquez sur le nom pour ouvrir les détails du modèle de score et apporter vos modifications.

### Modifier les paramètres de pondération de l’engagement

Les paramètres de poids définissent les bandes que vous pouvez affecter à chaque activité du modèle. Vous pouvez modifier les bandes pour refléter les stratégies de votre organisation pour évaluer l’engagement. Par exemple, vous pouvez ajuster la plage de pondération _Normale_ à une valeur de 65 si vous souhaitez attribuer une valeur plus élevée aux activités normales. Vous pouvez également ajouter une bande de pondération conçue pour capturer les activités comprises entre _Normale_ et _Importante_. Dans ce cas, vous pouvez ajouter une bande et l’étiqueter comme _Significatif_ et attribuer une valeur de bande de poids de 75.

1. Dans la page des détails du modèle de score, cliquez sur **[!UICONTROL Paramètres de poids de l’engagement]** dans la partie supérieure.

   ![Accéder aux paramètres de poids d’engagement](./assets/configuration-engagement-scoring-model-weight-settings-button.png){width="600" zoomable="yes"}

1. Pour chaque plage de poids, ajustez le nom ou les valeurs en fonction de vos besoins :

   * Modifiez le nom dans le champ _[!UICONTROL Bande de pondération]_.
   * Saisissez une nouvelle valeur. Vous pouvez également cliquer sur **&amp;plus;** ou **−** pour augmenter ou diminuer la valeur.

   ![Paramètres de poids de l’engagement](./assets/configuration-engagement-scoring-model-weight-settings.png){width="500"}

1. Si nécessaire, ajouter une autre plage de pondération :

   Cliquez sur **[!UICONTROL + Ajouter une bande de pondération]** au bas de la liste. Cette action insère une bande de pondération vide en bas de la liste.

   Saisissez le nom et définissez la valeur de la bande. Veillez à utiliser un nom et une valeur uniques.

1. Si nécessaire, supprimez une bande de pondération, puis cliquez sur l’icône _Supprimer_ ( ![Icône Supprimer](../assets/do-not-localize/icon-delete-outline.svg) ) pour la ligne de bande de pondération.

1. Une fois vos modifications effectuées, cliquez sur **[!UICONTROL Enregistrer]**.

### Modifier la pondération de l&#39;activité

Chaque modèle de score comprend la liste complète des activités de score d’engagement prises en charge :

{{engagement-activities}}

Pour chaque activité de la liste, définissez la valeur à affecter à chaque occurrence de l’activité. Cliquez sur la flèche vers le bas dans le champ **[!UICONTROL Pondération]** et choisissez la bande de pondération telle que définie dans les paramètres de pondération d&#39;engagement.

![Définir la pondération d’activité](./assets/configuration-engagement-scoring-model-set-activity-weighting.png){width="500"}

Si vous ne souhaitez pas que le calcul du score de l&#39;engagement utilise une activité, définissez la pondération sur une valeur nulle (0).

Vos modifications sont enregistrées automatiquement.

## Activer un modèle de score

Lorsque vous activez un modèle de score de brouillon, il remplace le modèle actif. Le modèle actuellement actif est automatiquement archivé.

1. Ouvrez un modèle de score de brouillon pour afficher la page de détails.

1. Cliquez sur **[!UICONTROL Activer]**.

1. Dans la boîte de dialogue de confirmation, cliquez sur **[!UICONTROL Activer]**.

   ![Accéder aux définitions d’événement configurées](./assets/configuration-engagement-scoring-activate-dialog.png){width="400"}
