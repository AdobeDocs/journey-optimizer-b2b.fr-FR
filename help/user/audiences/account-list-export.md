---
title: Exporter des comptes
description: Exportez les listes de comptes filtrées au format CSV pour les plateformes tierces avec les groupes d’achat et les filtres de score d’engagement dans Journey Optimizer B2B Edition.
feature: Audiences
role: User
exl-id: 3ec8e8fd-1bc2-4efa-840f-f06520099060
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: e935834c-48b7-43d8-b754-a815196a1b05
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
autotag-review: '2026-03-30T19:51:33.392Z'
source-git-commit: ff337a5f215daee1ea6dbe8d6b643087ac3324e2
workflow-type: tm+mt
source-wordcount: 261
ht-degree: 100%

---

# Exporter des comptes

Utilisez la fonctionnalité _Exporter des comptes_ pour exporter tous les comptes ou un ensemble de comptes en fonction du filtrage que vous définissez. Le processus d’export génère un fichier CSV et envoie l’URL du fichier stocké dans une notification push. Vous pouvez utiliser cette fonctionnalité pour déplacer des comptes vers des plateformes tierces, si nécessaire.

1. Dans Journey Optimizer B2B Edition, accédez à **[!UICONTROL Comptes]** > **[!UICONTROL Groupes d’achat]** dans le volet de navigation de gauche.

1. Sélectionnez l’onglet **[!UICONTROL Parcourir]**.

1. Cliquez sur **[!UICONTROL Exporter des comptes]** en haut à droite.

   ![Modifier les détails du compte](./assets/export-accounts.png){width="800" zoomable="yes"}

1. Dans la boîte de dialogue, définissez les paramètres des audiences de comptes à exporter.

   ![Spécifier le filtrage de l’audience de comptes](./assets/export-accounts-dialog.png){width="400"}

   Pour le **[!UICONTROL score d’engagement]**, l’opérateur `Between` est inclusif, tout comme les plages de pourcentage. Par exemple, les paragraphes 5.1 et 5 sont tous deux compris _entre_ 5 et 6.

   Les paramètres de filtrage vides sont traités comme `Is Any`.

1. Cliquez sur **[!UICONTROL Exporter des comptes]** pour générer le fichier CSV à l’aide des filtres spécifiés.

1. Lorsque vous recevez la notification indiquant que l’export est terminé, cliquez sur le lien de notification pour accéder au fichier CSV.

   ![Cliquez sur la notification pour télécharger le fichier CSV de la liste des comptes exportés](./assets/export-accounts-notification.png){width="425"}

   >[!NOTE]
   >
   >Si vous avez configuré un abonnement aux notifications par e-mail dans les préférences de votre compte d’utilisateur ou d’utilisatrice Adobe, il peut s’agir d’une notification par e-mail.

   La page de l’application redirige vers l’onglet de navigation _Groupe d’achat_ et la boîte de dialogue d’enregistrement du fichier sur le système vous invite à enregistrer le fichier sur votre système. Si vous devez partager les données, vous pouvez utiliser le système de partage de fichiers de votre équipe.
