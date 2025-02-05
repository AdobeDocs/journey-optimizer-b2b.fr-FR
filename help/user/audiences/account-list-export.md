---
title: Exporter la liste des comptes
description: Découvrez comment exporter la liste des comptes en fonction du filtre des groupes d’achats.
source-git-commit: c51ee8c8b58e8154c81f6a2ffada3f58a08eb6b4
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---

# Exporter la liste des comptes

Utilisez la fonction _Exporter la liste des comptes_ pour exporter tous les comptes ou un ensemble de comptes en fonction du filtrage que vous définissez. Le processus d’exportation génère un fichier CSV et envoie l’URL du fichier stocké dans une notification Push. Vous pouvez utiliser cette fonctionnalité pour déplacer des comptes vers des plateformes tierces, si nécessaire.

1. Dans Journey Optimizer B2B edition, accédez à **[!UICONTROL Comptes]** > **[!UICONTROL Groupes d’achat]** dans le volet de navigation de gauche.

1. Sélectionnez l’onglet **[!UICONTROL Parcourir]**.

1. Cliquez sur **[!UICONTROL Exporter des comptes]** en haut à droite.

   ![Modifier les détails du compte](./assets/export-accounts.png){width="800" zoomable="yes"}

1. Dans la boîte de dialogue, définissez les paramètres des audiences de compte à exporter.

   ![Spécifiez le filtrage de l’audience du compte](./assets/export-accounts-dialog.png){width="400"}

   Pour le **[!UICONTROL score de l’engagement]**, le `Between` de l’opérateur est inclusif, tout comme les plages de pourcentage. Par exemple, les paragraphes 5.1 et 5 sont tous deux _compris entre_ 5 et 6.

   Les paramètres de filtrage vides sont traités comme des `Is Any`.

1. Cliquez sur **[!UICONTROL Exporter des comptes]** pour générer le fichier CSV à l’aide des filtres spécifiés.

1. Lorsque vous recevez la notification indiquant que l’exportation est terminée, cliquez sur le lien de notification pour accéder au fichier CSV.

   ![Cliquez sur la notification pour télécharger le fichier CSV de la liste des comptes exportés](./assets/export-accounts-notification.png){width="425"}

   >[!NOTE]
   >
   >Si vous disposez d’un abonnement aux notifications par e-mail configuré dans les préférences de votre compte utilisateur d’Adobe, il peut s’agir d’une notification par e-mail.

   La page de l&#39;application redirige vers l&#39;onglet de navigation _Groupe d&#39;achat_ et la boîte de dialogue d&#39;enregistrement du fichier système vous invite à enregistrer le fichier sur votre système. Si vous devez partager les données, vous pouvez utiliser le système de partage de fichiers de votre équipe.
