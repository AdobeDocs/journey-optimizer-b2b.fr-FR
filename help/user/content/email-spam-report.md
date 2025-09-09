---
title: Consulter le rapport sur les spams
description: Générez des rapports de spam avec le score SpamAssassin afin de vérifier si les emails déclenchent des filtres de spam et améliorent la délivrabilité dans Journey Optimizer B2B edition.
feature: Email Authoring
level: Beginner
role: User
exl-id: 0ab2a85c-fbab-4681-9964-74b7fd1d574f
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 2%

---

# Consulter le rapport de spam

De nombreux fournisseurs de boîte de réception et la plupart des systèmes d’entreprise utilisent un processus de filtrage du spam. L’envoi d’e-mails déclenchant ces filtres peut nuire gravement à la délivrabilité. Dans Journey Optimizer B2B edition, vous pouvez vérifier le score de spam du contenu des emails en générant un rapport sur les spams. Ce rapport utilise des [[!DNL SpamAssassin]](https://spamassassin.apache.org/) pour tester l&#39;e-mail et vous aide à déterminer si un message peut être considéré comme indésirable par les outils anti-spam. Vous pouvez utiliser les informations du rapport pour prendre des mesures qui améliorent le score et la délivrabilité du contenu des e-mails.

Lorsque vous passez en revue les paramètres de votre e-mail ou modifiez le contenu, ouvrez la page _[!UICONTROL Simuler]_ et générez un _Rapport sur les spams_ afin de passer en revue le score et les éléments marqués d&#39;un indicateur qui peuvent déclencher un filtrage anti-spam.

1. Sur la page _[!UICONTROL Simuler]_, cliquez sur **[!UICONTROL Rapport sur les spams]** en haut à droite.

   ![Bouton de rapport de spam](./assets/email-spam-report-button.png){width="700" zoomable="yes"}

   Le processus de création de rapports analyse le contenu de l’e-mail et génère un score avec une liste des règles de filtrage déclenchées utilisées pour générer le score. Les facteurs incluent la disposition du corps, la structure, la taille de l’image, les mots de déclenchement de spam et d’autres éléments. Pour obtenir la liste des tests d’évaluation des règles pour les éléments d’e-mail, reportez-vous à la [[!DNL SpamAssassin] liste des tests](https://spamassassin.apache.org/old/tests_3_0_x.html).

1. Vérifiez les scores et les descriptions de chaque élément.

   >[!NOTE]
   >
   >Le score de spam est calculé par l&#39;intermédiaire de SpamAssassin, et Adobe n&#39;est pas propriétaire des règles ou de la logique de score. Pour plus d’informations sur le projet open source [!DNL SpamAssassin], reportez-vous à la [[!DNL SpamAssassin] documentation](https://cwiki.apache.org/confluence/display/SPAMASSASSIN/).

   Plus le score est faible, moins l’e-mail risque d’être marqué comme indésirable.

   ![Score positif du rapport de spam](./assets/email-spam-report-positive.png){width="600" zoomable="yes"}

   Avec un score supérieur à 5, le rapport inclut un avertissement indiquant que certains messages peuvent être bloqués ou marqués comme spam à la réception. Il est recommandé de s’assurer que le score est inférieur à 2.

   ![Score négatif du rapport de spam](./assets/email-spam-report-negative.png){width="600" zoomable="yes"}

1. S’il existe des éléments pouvant être améliorés dans le contenu de l’e-mail, modifiez votre contenu pour appliquer les mises à jour nécessaires.

1. Une fois vos modifications effectuées, revenez à la page _[!UICONTROL Simuler]_ et cliquez de nouveau sur **[!UICONTROL Rapport sur les spams]** pour vérifier les améliorations du score qui en résultent.
