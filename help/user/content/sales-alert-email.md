---
title: E-mail d’alerte de ventes
description: Configurez les e-mails d’alerte commerciale dans les parcours de compte pour informer les équipes commerciales. Cela inclut des résumés des groupes d’achats, des informations sur l’IA et des détails des membres dans Journey Optimizer B2B edition.
feature: Email Authoring, Account Journeys
role: User
exl-id: 01bffbce-6c73-483a-8731-de4e5569cf61
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 6%

---

# E-mail d’alerte de vente

Un _e-mail d’alerte de vente_ signale la remise des groupes d’achats au service des ventes. L&#39;e-mail contient un résumé du groupe d&#39;achat et des informations sur les membres du groupe d&#39;achat et leurs activités.

En tant que spécialiste marketing, vous pouvez configurer un nœud d’e-mail d’alerte de vente dans les parcours de votre compte pour avertir votre équipe des ventes de l’achèvement du parcours pour des groupes d’achats spécifiques. Dans le nœud , vous pouvez spécifier les adresses e-mail de l’équipe commerciale ou un alias de distribution qui atteint un ensemble de comptes.

>[!IMPORTANT]
>
>Assurez-vous que la place sur la liste autorisée de votre organisation est mise à jour afin qu’un e-mail d’alerte commerciale puisse être diffusé. Pour plus d’informations, voir [Protocoles de tracking et de diffusion e-mail](../start/email-protocols.md).

## Contenu de l’e-mail

+++Exemple d’e-mail d’alerte de vente
![Exemple d’e-mail d’alerte vente utilisant le modèle par défaut](./assets/sales-alert-email-example.png){width="500" zoomable="yes"}

+++

| Section | Nom | Description |
| - | ---- | ----------- |
| Informations sur le groupe d&#39;achat | Nom du groupe d&#39;achat | Nom d&#39;affichage du groupe d&#39;achat. |
|   | Nom de compte | Nom du compte. |
|   | Score d’engagement | Score d’engagement du groupe d’achat, basé sur les activités d’engagement actives au cours des 30 derniers jours. |
|   | Score d’exhaustivité | Score d&#39;exhaustivité du groupe d&#39;achat. |
|   | Intérêt de la solution | Intérêt de la solution lié au groupe d’achat » |
|   | Statut | Statut du groupe d&#39;achat. |
| Points forts du groupe d’achat | Membres les plus engagés | Membres les plus engagés du groupe d&#39;achat par score et rôle d&#39;engagement des membres du groupe d&#39;achat. |
|   | Sujet d&#39;intérêt | Mots-clés les plus courants intervenant dans l’engagement du contenu, basés sur les e-mails, les téléchargements, le chat, la révision PDF, le résumé de l’activité et les questions du webinaire. |
|   | Rôles manquants | Rôles obligatoires dans le modèle mais manquants dans le groupe d&#39;achat. |
| Résumé du groupe d&#39;achat | Résumé des activités (optimisé par l’IA générative) | Résumé généré par IA du groupe d&#39;achat basé sur les activités des membres. Les activités des 30 derniers jours sont prises en compte. |
|   | Principaux moments intéressants | Récents moments intéressants liés aux membres du groupe d&#39;achat. |
| Membres | Liste de quatre membres acheteurs | Détails des quatre principaux membres du groupe d’achat par score d’engagement et rôle. |
| Chaque membre du groupe d&#39;achat | Nom du membre | Nom du membre du groupe d&#39;achat. |
|   | Titre | Titre du membre du groupe d&#39;achat. |
|   | Rôle | Rôle de groupe d&#39;achat du membre. |
|   | Score d’engagement | Score d’engagement des membres du groupe d’achat. Le score est basé sur les activités d’engagement actives au cours des 30 derniers jours. |
|   | Dernier moment significatif | Le dernier moment le plus intéressant a été celui du député. |
|   | Activités les plus récentes | Les deux dernières activités liées au membre du groupe d&#39;achat. |
|   | ID d’e-mail | ID d&#39;e-mail du membre du groupe d&#39;achat. |
|   | Numéro de téléphone | Numéro de téléphone du membre du groupe d&#39;achat. |

## Ajout d’une action d’e-mail d’alerte de ventes dans un parcours de compte

Vous pouvez configurer des diffusions par e-mail d’alerte de vente dans un parcours de compte lorsque vous ajoutez un nœud _[!UICONTROL Agir]_ et que vous effectuez les opérations suivantes :

1. Pour la cible _[!UICONTROL Action sur]_, choisissez **[!UICONTROL Compte]**.

1. Pour _[!UICONTROL Action sur les comptes]_, choisissez **[!UICONTROL Envoyer une alerte de vente]**.

1. Pour **[!UICONTROL Sélectionner l’intérêt de la solution]**, choisissez l’intérêt de la solution à utiliser pour le contenu d’e-mail généré.

1. Dans le champ **[!UICONTROL Envoyer un e-mail à]**, saisissez chaque adresse e-mail ou alias que vous souhaitez inclure pour la diffusion.

   ![Boîte de dialogue Créer un e-mail](assets/sales-alert-email-journey-node.png){width="600" zoomable="yes"}

   Lorsque le parcours de compte est actif, l’alerte de vente est diffusée en fonction de ces paramètres.
