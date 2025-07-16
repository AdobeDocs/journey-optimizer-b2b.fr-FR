---
title: Tester le rendu des e-mails
description: Découvrez comment exploiter votre compte Litmus pour tester le rendu des e-mails dans Journey Optimizer B2B edition.
feature: Email Authoring, Integrations
level: Intermediate
role: User
exl-id: 26d87a56-6bd1-4d4a-8090-71f5b0a7e9f8
source-git-commit: dbb678f40b8d637f4eb534acb31328ebea0c182a
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 3%

---

# Tester le rendu des e-mails avec Litmus

Pour tester vos e-mails, vous pouvez utiliser un compte [Litmus](https://www.litmus.com/email-testing){target="_blank"} Enterprise de Journey Optimizer B2B edition. Grâce à cette intégration, vous pouvez prévisualiser votre rendu d’e-mail dans les clients de messagerie les plus courants. Cet outil vous permet de vous assurer que le contenu de votre e-mail s’affiche correctement et fonctionne comme prévu dans chaque boîte de réception.

>[!AVAILABILITY]
>
>Cette intégration est uniquement disponible pour les utilisateurs de Journey Optimizer B2B edition disposant de comptes Litmus Enterprise. Pour plus d&#39;informations, consultez la page [solution sur le site web de Litmus](https://www.litmus.com/solutions/esp/adobe-journey-optimizer){target="_blank"}.

1. Une fois votre conception d’e-mail terminée et prête à être testée, cliquez sur **[!UICONTROL Simuler du contenu]** dans l’espace de conception d’e-mail.

1. Cliquez sur **[!UICONTROL Rendu d’e-mail]** en haut à droite.

   ![Bouton Rendu d’e-mail](./assets/email-simulate-render-button.png){width="700" zoomable="yes"}

   Si vous ne vous êtes pas encore connecté à votre compte Litmus à partir de Journey Optimizer B2B edition, la page affichée propose une option pour démarrer un compte d’évaluation ou vous connecter à votre compte existant.

1. Cliquez sur **[!UICONTROL Connecter votre compte Litmus]** en haut à droite, ou utilisez le lien à l’intérieur de la page.

   ![Connecter votre compte Litmus](./assets/email-simulate-render-litmus-connect.png){width="700" zoomable="yes"}

1. Saisissez les identifiants de votre compte Litmus et cliquez sur **[!UICONTROL Se connecter]**.

1. Cliquez sur **[!UICONTROL Connexion]** pour confirmer la connexion entre Litmus et Journey Optimizer B2B edition et envoyer le contenu de l’e-mail pour le rendu.

   >[!IMPORTANT]
   >
   >Lorsque vous connectez votre compte Litmus à Journey Optimizer B2B edition, vous acceptez que les messages de test soient envoyés à Litmus. Ce contenu est ensuite géré dans Litmus et non dans Adobe. Par conséquent, la politique e-mail de rétention des données de Litmus s&#39;applique à ces e-mails, y compris les données de personnalisation qui peuvent être incluses dans les messages de test.

1. Cliquez sur **[!UICONTROL Exécuter le test]** en haut à droite pour générer des aperçus d’e-mail.

   ![Exécuter un test de rendu Litmus](./assets/email-simulate-render-litmus-run-test.png){width="700" zoomable="yes"}

1. Vérifiez le contenu de vos e-mails sur les clients courants de bureau, mobiles et Web.

   Cliquez sur la miniature affichée pour afficher les détails de l’un des tests clients rendus.

   ![Prévisualisations d’e-mails Litmus](./assets/email-simulate-render-litmus-previews.png){width="700" zoomable="yes"}

1. Lorsque vous avez terminé la révision, cliquez sur la flèche vers l’arrière ( ![icône Afficher ou masquer les filtres](../../assets/do-not-localize/icon_back-arrow.svg) ) en haut à gauche pour revenir à la page Simuler du contenu.

   Vous pouvez sélectionner un autre profil et effectuer un autre test de rendu, ou revenir à l’espace de conception des e-mails pour apporter les ajustements nécessaires en fonction de votre révision.
