---
title: Détails du parcours
description: Surveillez les performances des parcours de compte et de personne dans Adobe Journey Optimizer B2B Edition. Examinez les mesures d’achèvement, d’engagement et de canal pour chaque parcours.
feature: Dashboards, Account Journeys, Person Journeys
role: User
exl-id: 09a0e06a-1fd3-44da-9774-23f125f2823d
autotag-review: 2026-03-30T23:21:08.953Z
TQID: 'https://experienceleague.adobe.com/a5tIOW39sq3Lq30pQ3yr7-IvLGaAXC6LKqY8-mpxCDY'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
  - id: f979fe0e-02fe-4599-b492-7b3df1d4e7dc
    internal-label: Intelligent Insights
  - id: 7da10825-0f0b-5df3-8450-465ae8d76951
    internal-label: Dashboards
subfeature_v2:
  - id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
    internal-label: Account Journeys
  - id: ba367494-9862-4596-bd6f-299c7e10a46b
    internal-label: Person Journeys
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 5c053f91ea231cd8517e2329b7170aa08c33dc24
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 1%
---
# Détails du parcours

Dans [!DNL Adobe Journey Optimizer B2B Edition], ouvrez un parcours de compte ou de personne publié et sélectionnez l’onglet **[!UICONTROL Aperçu]**. Examinez la progression, l’engagement et les performances des canaux pour le parcours sélectionné.

Les parcours de compte signalent la progression des comptes. Les parcours de personne signalent la progression pour les personnes. Les widgets et les libellés de mesure disponibles varient selon le type de parcours. Sélectionnez l’onglet correspondant pour afficher les détails du tableau de bord.

Pour les mesures d’e-mail agrégées entre les parcours, utilisez le [rapport sur les performances des e-mails](../dashboards/email-performance-dashboard.md).

>[!BEGINTABS]

>[!TAB parcours de compte]

Le tableau de bord du parcours de compte affiche la progression du compte, l’engagement, les performances du canal et des résumés IA génératifs. Il faut environ quatre heures pour que les données commencent à remplir les graphiques et les tableaux.

![Onglet Aperçu du parcours de compte affichant la progression, l’engagement et les performances du canal.](./assets/journey-detail-overview-account.png){width="700" zoomable="yes"}

## achèvement du parcours

Cette section présente deux mesures d’achèvement :

* **[!UICONTROL Statut des comptes dans le parcours]** : affiche le nombre total de comptes et une répartition par statut de parcours, y compris _Terminé_, _En cours_ et _Abandonné_. Chaque segment affiche un statut, un pourcentage et un nombre de comptes.
* **[!UICONTROL Comptes terminés au fil du temps]** : affiche le nombre de comptes ayant terminé le parcours au fil du temps. L’axe horizontal affiche les dates, et l’axe vertical les nombres de comptes.

>[!NOTE]
>
>Dans les parcours de comptes, le **[!UICONTROL Statut des comptes dans le graphique de parcours]** inclut les comptes qui ont passé le parcours, même s’ils ont été supprimés par la suite. **[!UICONTROL L&#39;exploration en amont]** exclut les comptes supprimés, de sorte qu&#39;elle peut afficher moins d&#39;enregistrements que le graphique. Cette différence est attendue. La suppression de comptes ne modifie pas les historiques de statut du parcours.

## Engagement du parcours

Cette section présente deux mesures d’engagement :

* **[!UICONTROL Engagement par comptes]** - Ce graphique en cercle segmente les comptes d’un parcours en _engagements_ et _non engagés_. La figure centrale affiche le nombre total. Cette visualisation permet de comprendre rapidement l’engagement global du compte.
* **[!UICONTROL Engagement par les personnes]** : affiche le nombre de personnes ayant des activités d’engagement dans le parcours. Cette valeur compte pour les personnes, pas pour les activités d’engagement.

## performance du parcours

Cette section présente deux mesures essentielles :

* **[!UICONTROL Taux d&#39;achèvement du Parcours]** - Pourcentage de comptes ayant terminé leur parcours avec succès.
* **[!UICONTROL Délai moyen d’achèvement du parcours]** : temps moyen nécessaire aux comptes pour terminer le parcours, exprimé en jours.

## Performances du canal {#email-and-sms-performance}

Le tableau de bord comprend **[!UICONTROL Performances des e-mails]**, **[!UICONTROL Performances des SMS]** et **[!UICONTROL Performances de WhatsApp]** pour le parcours de compte sélectionné. Utilisez les mesures de diffusion et d’engagement disponibles pour évaluer chaque point de contact de communication.

**[!UICONTROL Performances des e-mails]** colonnes du tableau :

* _[!UICONTROL Nom de la ressource]_ - Nom de la ressource
* _[!UICONTROL Envoyé]_ - Nombre d’e-mails envoyés
* _[!UICONTROL Taux de diffusion]_ - Nombre d&#39;e-mails diffusés divisé par le nombre envoyé
* _[!UICONTROL Taux d&#39;ouvertures]_ - Nombre de messages ouverts divisé par le nombre de messages diffusés
* _[!UICONTROL Taux de clics publicitaires]_ - Nombre d’e-mails cliqués divisé par le nombre de messages diffusés

**[!UICONTROL Performances des SMS]** colonnes du tableau :

* _[!UICONTROL Nom de la ressource]_ - Nom de la ressource
* _[!UICONTROL Envoyés]_ - Nombre de SMS envoyés
* _[!UICONTROL Taux de diffusion]_ - Nombre de SMS diffusés divisé par le nombre envoyé
* _[!UICONTROL Taux de clic publicitaire]_ - Nombre de SMS ayant fait l’objet d’un clic divisé par le nombre de messages diffusés
<!--
To generate a shareable PDF of your current view, click **[!UICONTROL Export]** at the top right of the page. 
-->

## Actions supplémentaires

Utilisez le menu **...** pour qu’un graphique ou un tableau accède à ses actions disponibles.

### Analyser en amont

Pour le **[!UICONTROL Statut des comptes dans le graphique parcours]**, choisissez **[!UICONTROL Analyser en amont]** pour une analyse approfondie des statuts des comptes individuels.

![L&#39;exploration en amont des données du graphique](./assets/journey-status-drill-through.png){width="600" zoomable="yes"}
<!--
The applied global filters are carried over to the view and displayed at the top. Click the _Filter_ icon at the top left to filter the data display by journey.
-->

### Afficher plus

Choisissez **[!UICONTROL Afficher plus]** pour accéder aux données étendues. Le pop-up affiché fournit une répartition des données.

![Afficher les données étendues](./assets/journey-completion-over-time-view-more.png){width="600" zoomable="yes"}

Pour télécharger les données, sélectionnez **[!UICONTROL Télécharger CSV]**. Pour revenir au tableau de bord de _[!UICONTROL Présentation]_, sélectionnez **[!UICONTROL Fermer]**.

>[!TAB parcours de personne]

Le tableau de bord du parcours de personnes affiche les performances d’achèvement, d’engagement et d’e-mail pour les personnes du parcours sélectionné.

![Onglet Aperçu du parcours de la personne affichant la progression, l’engagement et les performances des e-mails.](./assets/journey-detail-overview-person.png){width="700" zoomable="yes"}

## achèvement du parcours {#person-journey-completion}

Utilisez les graphiques suivants pour consulter le statut des personnes dans les tendances de parcours et d’achèvement :

* **[!UICONTROL Statut des personnes dans le parcours]** : affiche le nombre total de personnes et une répartition par statut de parcours. Chaque segment affiche un statut, un pourcentage et un nombre de personnes.
* **[!UICONTROL Nombre de personnes ayant terminé le parcours au fil du temps]** : affiche le nombre de personnes ayant terminé le test au fil du temps. La série **[!UICONTROL incrémentielle terminée]** affiche les terminaisons pour chaque intervalle de temps. La série **[!UICONTROL Cumulé terminé]** affiche le total cumulé des terminaisons.

>[!NOTE]
>
>Dans les parcours en personne, le **[!UICONTROL Statut des personnes dans le graphique de parcours]** inclut les personnes qui ont passé le parcours, même si elles ont été supprimées par la suite. **[!UICONTROL L&#39;exploration en amont]** exclut les personnes supprimées, de sorte qu&#39;elle peut afficher moins d&#39;enregistrements que le graphique. Cette différence est attendue. La suppression de personnes ne modifie pas l’historique des statuts de parcours.

Pour le statut _[!UICONTROL des personnes dans le graphique de parcours], cliquez sur l’icône_ Plus_ ( **...** ) et sélectionnez **[!UICONTROL Analyser]** pour consulter les statuts de chaque personne.

## Engagement du parcours {#person-journey-engagement}

Le widget **[!UICONTROL Engagement par les personnes]** affiche le nombre de personnes ayant des activités d’engagement dans le parcours. Cette valeur compte pour les personnes, pas pour les activités d’engagement.

## performance du parcours {#person-journey-performance}

Utilisez les mesures suivantes pour évaluer les performances d’achèvement :

* **[!UICONTROL Taux d&#39;achèvement du Parcours]** : pourcentage de personnes ayant terminé le parcours.
* **[!UICONTROL Délai moyen d’exécution du parcours]** : temps moyen nécessaire aux personnes pour effectuer le parcours, exprimé en jours.

## Performances des e-mails {#person-journey-email-performance}

Le tableau **[!UICONTROL Performances des e-mails]** affiche le nombre de chaque ressource d’e-mail dans le parcours de personne sélectionné, plutôt que les taux :

* **[!UICONTROL Nom de la ressource]** : nom de la ressource e-mail
* **[!UICONTROL Envoyé]** : nombre d&#39;e-mails envoyés
* **[!UICONTROL Diffusés]** : nombre d&#39;e-mails diffusés
* **[!UICONTROL Ouvert]** : nombre d&#39;e-mails ouverts
* **[!UICONTROL Clic]** : nombre d’e-mails sur lesquels l’utilisateur a cliqué

>[!ENDTABS]
