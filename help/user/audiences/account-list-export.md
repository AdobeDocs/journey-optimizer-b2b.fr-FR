---
title: Exporter la liste des comptes
description: Découvrez comment exporter la liste des comptes en fonction du filtre des groupes d’achat.
feature: Account Lists
role: User
exl-id: 3ec8e8fd-1bc2-4efa-840f-f06520099060
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: ht
source-wordcount: '253'
ht-degree: 100%

---

# Exporter la liste des comptes

Utilisez la fonctionnalité _Exporter la liste des comptes_ pour exporter tous les comptes ou un ensemble de comptes en fonction du filtrage que vous définissez. Le processus d’export génère un fichier CSV et envoie l’URL du fichier stocké dans une notification push. Vous pouvez utiliser cette fonctionnalité pour déplacer des comptes vers des plateformes tierces, si nécessaire.

1. Dans Journey Optimizer B2B Edition, accédez à **[!UICONTROL Comptes]** > **[!UICONTROL Groupes d’achat]** dans le volet de navigation de gauche.

1. Sélectionnez l’onglet **[!UICONTROL Parcourir]**.

1. Cliquez sur **[!UICONTROL Exporter des comptes]** en haut à droite.

   ![Modifier les détails du compte](./assets/export-accounts.png){width="800" zoomable="yes"}

1. Dans la boîte de dialogue, définissez les paramètres des audiences de compte à exporter.

   ![Spécifier le filtrage de l’audience du compte](./assets/export-accounts-dialog.png){width="400"}

   Pour le **[!UICONTROL score d’engagement]**, l’opérateur `Between` est inclusif, tout comme les plages de pourcentage. Par exemple, les paragraphes 5.1 et 5 sont tous deux compris _entre_ 5 et 6.

   Les paramètres de filtrage vides sont traités comme `Is Any`.

1. Cliquez sur **[!UICONTROL Exporter des comptes]** pour générer le fichier CSV à l’aide des filtres spécifiés.

1. Lorsque vous recevez la notification indiquant que l’export est terminé, cliquez sur le lien de notification pour accéder au fichier CSV.

   ![Cliquez sur la notification pour télécharger le fichier CSV de la liste des comptes exportés](./assets/export-accounts-notification.png){width="425"}

   >[!NOTE]
   >
   >Si vous avez configuré un abonnement aux notifications par e-mail dans les préférences de votre compte d’utilisateur ou d’utilisatrice Adobe, il peut s’agir d’une notification par e-mail.

   La page de l’application redirige vers l’onglet de navigation _Groupe d’achat_ et la boîte de dialogue d’enregistrement du fichier sur le système vous invite à enregistrer le fichier sur votre système. Si vous devez partager les données, vous pouvez utiliser le système de partage de fichiers de votre équipe.
