---
title: Courriel d’alerte de ventes
description: Découvrez comment inclure un email d’alerte de vente automatisé dans vos parcours de compte.
feature: Email Authoring, Content
exl-id: 01bffbce-6c73-483a-8731-de4e5569cf61
source-git-commit: 33bd8f68ae581d974fc52f94df6f2249d9493325
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 3%

---

# Email d’alerte commerciale

Un _e-mail d’alerte commerciale_ signale la remise des groupes d’achats aux ventes. L’email contient un résumé du groupe d’achat et des informations sur les membres du groupe d’achat et leurs activités.

En tant que marketeur, vous pouvez configurer un noeud d’email d’alerte commerciale dans vos parcours de compte afin d’alerter votre équipe commerciale de la fin du parcours pour des groupes d’achats spécifiques. Dans le noeud , vous pouvez spécifier les adresses électroniques de l’équipe commerciale ou un alias de distribution qui atteint un ensemble de comptes.

## Contenu des emails

+++Exemple d’email d’alerte de vente
![Exemple d&#39;un email d&#39;alerte commerciale utilisant le modèle par défaut](./assets/sales-alert-email-example.png){width="500" zoomable="yes"}

+++

| Section | Nom | Description |
| - | ---- | ----------- |
| Informations sur le groupe d’achat | Nom du groupe d’achat | Nom d’affichage du groupe d’achats. |
|   | Nom de compte | Nom du compte. |
|   | Évaluation de l’engagement | Score d’engagement du groupe d’achats, en fonction des activités d’engagement actives au cours des 30 derniers jours. |
|   | Score de complétude | Score de complétude du groupe d’achats. |
|   | Intérêt de la solution | Intérêt de la solution lié au groupe d’achat |
|   | Statut | État du groupe d’achats. |
| Faits saillants du groupe d’achat | Principaux membres engagés | Les membres les plus engagés du groupe d’achat en achetant le score et le rôle d’engagement des membres du groupe. |
|   | Sujet intéressant | Mots-clés les plus fréquents se produisant dans l’engagement du contenu, en fonction des emails, des téléchargements, de la conversation, de la révision du PDF, du résumé de l’activité et des questions du webinaire. |
|   | Rôles manquants | Rôles obligatoires dans le modèle, mais manquants dans le groupe d’achat. |
| Résumé pour le groupe d’achats | Résumé de l’activité (optimisé par l’IA générique) | Résumé généré par l’IA du groupe d’achat en fonction des activités des membres. Les activités des 30 derniers jours sont prises en compte. |
|   | Principaux moments intéressants | Derniers moments intéressants liés aux membres du groupe d&#39;achat. |
| Membres | Liste de quatre membres acheteurs | Détails des quatre premiers membres du groupe d’achat par score d’engagement et rôle. |
| Chaque membre du groupe d’achat | Nom du membre | Nom du membre du groupe d’achats. |
|   | Titre | Titre du membre du groupe d’achats. |
|   | Rôle | Le rôle de groupe d’achats du membre. |
|   | Évaluation de l’engagement | Score d’engagement des membres du groupe d’achat. Le score est basé sur les activités d’engagement actif au cours des 30 derniers jours. |
|   | Dernier moment intéressant | Le dernier moment le plus intéressant en rapport avec le membre. |
|   | Activités les plus récentes | Les deux dernières activités liées au membre du groupe d’achat. |
|   | ID d’e-mail | ID d’adresse électronique du membre du groupe d’achats. |
|   | Numéro de téléphone | Numéro de téléphone du membre du groupe d’achats. |

## Ajout d’une action email d’alerte commerciale dans un parcours de compte

Vous pouvez configurer des diffusions par email d’alerte commerciale dans un parcours de compte lorsque vous ajoutez un noeud _[!UICONTROL Take an action]_ et procédez comme suit :

1. Pour la cible _[!UICONTROL Action sur]_, choisissez **[!UICONTROL Compte]**.

1. Pour _[!UICONTROL Action sur les comptes]_, sélectionnez **[!UICONTROL Envoyer une alerte de vente]**.

1. Pour **[!UICONTROL Sélectionner l’intérêt de la solution]**, choisissez l’intérêt de la solution à utiliser pour le contenu d’email généré.

1. Pour **[!UICONTROL Envoyer un courrier électronique à]**, saisissez chaque adresse électronique ou alias à inclure pour la diffusion.

   ![Créer une boîte de dialogue de courrier électronique](assets/sales-alert-email-journey-node.png){width="600" zoomable="yes"}

   Une fois le parcours du compte publié, l’alerte de vente est diffusée en fonction de ces paramètres.
