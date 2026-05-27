---
title: Rapport des performances des e-mails
description: Utilisez le rapport Performance des e-mails dans Journey Optimizer B2B edition pour surveiller les mesures d’envoi, de diffusion, d’engagement et de désinscription des e-mails sur tous les parcours dans une vue unifiée.
feature: Dashboards, Reporting
role: User
autotag-review: '2026-05-21T15:04:51.176Z'
TQID: 'https://experienceleague.adobe.com/hA63o9-2-atw0kRNFeEu6H449WmZ59CjL3uiVS7nEcA'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
subfeature_v2:
  - id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 8226114f1a34adf85437579ef17a50b80ccfa596
workflow-type: tm+mt
source-wordcount: 833
ht-degree: 5%

---

# Rapport Performances des emails

Le rapport **Performances des e-mails** offre aux marketeurs une vue unifiée de l&#39;activité des e-mails sur tous les parcours dans Adobe Journey Optimizer B2B edition. Il agrège les mesures d’envoi, de diffusion, d’engagement et de désinscription. En faisant apparaître le nombre brut et les taux calculés, vous pouvez surveiller l’intégrité de la campagne, comparer les performances des e-mails et identifier en un coup d’œil les problèmes de délivrabilité ou d’engagement. Pour les mesures au niveau du parcours sur les canaux e-mail et SMS, reportez-vous au tableau de bord [Parcours de compte](./journeys-dashboard.md).

## Accès au rapport

1. Dans le volet de navigation de gauche, sélectionnez **[!UICONTROL Tableau de bord]**.
1. Sélectionnez l’onglet **[!UICONTROL Performances des e-mails]** en haut du tableau de bord de création de rapports.

![&#x200B; Rapport sur les performances des e-mails &#x200B;](./assets/email-performance-dashboard.png){width="800" zoomable="yes"}

## Filtrer les données

Cliquez sur l’icône _Filtre_ ( ![Icône Filtrer](../assets/do-not-localize/icon-filter.svg) ) en haut à gauche pour filtrer l’affichage des données à l’aide des deux types de filtres pris en charge. Ces filtres s’appliquent simultanément à tous les panneaux :

* **[!UICONTROL Parcours]** - Filtre le rapport afin d’afficher les données d’un ou de plusieurs parcours sélectionnés. Utilisez ce filtre pour isoler les performances des parcours qui sont importants pour votre campagne ou votre programme.

* **Période** - Limite toutes les mesures aux e-mails envoyés dans la période spécifiée. Prend en charge des périodes prédéfinies et un sélecteur de date personnalisé. Le sélecteur de période se trouve dans le coin supérieur droit du tableau de bord.

![Filtres de Parcours et de période dans la boîte de dialogue Filtres](./assets/email-performance-filters.png){width="500"}

Lorsque vous modifiez les filtres dans la boîte de dialogue Filtres, cliquez sur **[!UICONTROL Appliquer]**.

## Comptage et taux des graphiques de mesures

La section supérieure du rapport Performances des emails contient deux graphiques à barres côte à côte qui fournissent un résumé visuel de l&#39;intégrité globale des programmes d&#39;email au cours de la période et du parcours sélectionnés.

**Compter les mesures** — Affiche le volume absolu de l&#39;activité e-mail. Chaque barre représente le nombre total d’événements d’e-mail clés dans tous les e-mails de la portée filtrée : envoyés, diffusés, ouverts, ayant fait l’objet d’un clic, rejetés et désabonnements.

**Mesures des taux** — Affiche des taux calculés en pourcentage, ce qui vous permet d&#39;évaluer l&#39;engagement et la qualité de la délivrabilité indépendamment du volume : taux de diffusion, taux d&#39;ouverture, taux de clics, taux de rebonds, taux de clics pour ouverture et taux de désabonnements.

Pointez sur le graphique pour afficher des données numériques.

![Pointez sur le graphique à barres - nombre affiché](./assets/email-performance-counts-hover.png){width="500"}

| Mesure | Type | Description |
|--------|------|-------------|
| Envoyé | Nombre | Nombre total de messages e-mail envoyés pour diffusion. |
| Diffusé | Nombre | E-mails acceptés par le serveur de messagerie du destinataire. |
| Ouvert | Nombre | Nombre d’e-mails diffusés ouverts au moins une fois. |
| Cliqué | Nombre | Nombre d’e-mails ayant reçu au moins un clic sur un lien. |
| Renvoi | Nombre | Emails n’ayant pas pu être délivrés (hard ou soft bounce). |
| Désabonnements | Nombre | Les destinataires qui se sont désabonnés via un lien de désabonnement dans l&#39;email. |
| Taux de diffusion | Taux | Livré ÷ envoyé. Indique le pourcentage d’e-mails ayant atteint les boîtes de réception. |
| Taux dʼouverture | Taux | Ouvert ÷ diffusé. Mesure l’engagement des destinataires avec les objets. |
| Taux de clic | Taux | A Cliqué ÷ Diffusé. Mesure l’engagement global des clics par e-mail diffusé. |
| Taux de rebond | Taux | Rebond ÷ envoyé. Met en évidence la délivrabilité et répertorie les problèmes d’intégrité. |
| Taux de clic-ouverture (CTOR) | Taux | Clic ÷ Ouverture. Mesure l’efficacité du contenu et de CTA parmi les lecteurs et lectrices engagés. |
| Taux de désinscription | Taux | Les Désabonnements ÷ Diffusés. Signale la pertinence et l’adéquation de l’audience. |

## Tableau des performances des e-mails

Au bas de la page, un tableau détaillé affiche les mesures par e-mail pour chaque ressource d’e-mail dans la portée filtrée. Par défaut, le tableau affiche 10 lignes par page.

La colonne **Désabonnement %** est une mesure prioritaire pour surveiller l&#39;activité de désinscription directement dans la vue du tableau.

| Colonne | Description |
|--------|-------------|
| Nom d&#39;e-mail | Nom de la [ressource e-mail](../content/add-email.md) tel que configuré dans le parcours. |
| Envoyé | Nombre total d’envois pour cet e-mail au cours de la période sélectionnée. |
| Diffusé | Nombre d’e-mails envoyés avec succès aux serveurs de messagerie des destinataires. |
| % de diffusion | Diffusés ÷ envoyés, exprimés en pourcentage. |
| Ouvertures | Nombre total d’événements ouverts enregistrés pour cet e-mail. |
| % d’ouverture | Ouvertures ÷ diffusions, exprimées en pourcentage. |
| Clics | Nombre total d’événements de clic sur les liens pour cet e-mail. |
| Cliquez sur % | Clics ÷ diffusés, exprimés en pourcentage. |
| CTOR % | Taux de clic-ouverture : clics ÷ ouvertures, exprimé en pourcentage. |
| Rebonds | Nombre d&#39;emails en échec (hard + soft bounces). |
| % de rebond | Rebonds ÷ envoyés, exprimés en pourcentage. |
| % des désinscriptions | Les Désabonnements ÷ Diffusés. Mesure prioritaire pour la surveillance de l’intégrité du processus d’opt-out. |
| Première activité | Date et heure du premier événement enregistré (envoi, ouverture ou clic) pour cet e-mail au cours de la période sélectionnée. |
| Dernière activité | Horodatage de l’événement le plus récent enregistré pour cet e-mail au cours de la période sélectionnée. |

## Exporter les données du rapport

Le rapport Performances des e-mails prend en charge l’exportation des données pour une analyse plus approfondie dans des outils externes ou pour partager les résultats avec les parties prenantes. Vous pouvez exporter les données du tableau au format CSV, compatible avec n’importe quel outil d’analyse de données ou de BI.

>[!CAUTION]
>
>Les exportations reflètent les filtres actuellement actifs. Assurez-vous que vos filtres de période et de parcours sont correctement définis avant l’exportation afin d’éviter les données incomplètes dans le fichier de sortie.

**_Pour exporter des données de rapport:_**

1. Définissez votre période en haut à droite et appliquez un filtrage de **[!UICONTROL Parcours]** si nécessaire.
1. Cliquez sur l’icône du menu **...** dans le coin supérieur droit du panneau Performances des e-mails et choisissez **[!UICONTROL Afficher plus]**.
1. Cliquez sur **[!UICONTROL Télécharger CSV]** dans le menu.

   ![Affichage des données détaillées et téléchargement du fichier CSV](./assets/email-performance-data-export.png){width="700" zoomable="yes"}

   Le fichier est téléchargé automatiquement à l’emplacement de téléchargement par défaut de votre navigateur.

1. Cliquez sur **[!UICONTROL Fermer]** pour revenir au rapport Performances des emails.
