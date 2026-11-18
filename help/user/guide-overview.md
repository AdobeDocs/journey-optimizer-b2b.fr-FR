---
title: Documentation d’Adobe Journey Optimizer B2B Edition
description: 'Documentation complète pour Journey Optimizer B2B Edition : explorez les ressources disponibles pour l’intégration, la création de groupes d’achat, la conception de parcours de compte et la gestion de contenu.'
exl-id: 3d7b6c82-95c3-4d89-b3dc-7fd5b0aef615
autotag-review: 2026-03-27T22:18:45.397Z
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: f467931a-9b22-4ca8-869f-adfbd64061ce
    internal-label: Onboarding
TQID: https://experienceleague.adobe.com/BK-uFYGIZyqRNy4Gx-vJB-oy3q8zpjERIoJwBvgofUY
source-git-commit: 262e06bce2cf9698731eda2cb0a3436c5080fddf
workflow-type: tm+mt
source-wordcount: '1103'
ht-degree: 23%
---
# Documentation d’Adobe Journey Optimizer B2B Edition

[!DNL Adobe Journey Optimizer B2B Edition] est une application unique en son genre qui permet aux équipes marketing et commerciales d’orchestrer des expériences basées sur un compte et de qualifier des groupes d’achat pour des produits spécifiques tout au long du cycle de vie du client. Il utilise l’IA pour impliquer et qualifier les groupes d’achats au sein des comptes cibles, ce qui permet à vos équipes de générer un pipeline de meilleure qualité et de concevoir de meilleures stratégies d’acquisition, d’expansion et de rétention. Il permet également aux équipes de vente et de marketing de partager des informations.

Cette documentation fournit des informations sur la maîtrise de l’application. Il est conçu pour les professionnels du marketing, les représentants du développement commercial, les analystes de données et les administrateurs opérationnels.

## Nouveautés

Consultez cet exemple des derniers ajouts et améliorations apportés à l’application [!DNL Journey Optimizer B2B Edition] et à la documentation.

>[!BEGINTABS]

>[!TAB Listes de personnes]

Créez des listes d’utilisateurs statiques et dynamiques réutilisables pour cibler les profils à l’aide d’attributs démographiques et d’un historique des événements d’expérience. Utilisez l’appartenance à une liste pour acheminer les personnes via des parcours de compte et de personne. Utilisez des actions de parcours pour ajouter des personnes à des listes statiques ou en supprimer.

[!BADGE En savoir plus]{type=Informative url="/help/user/audiences/people-lists.md" tooltip="En savoir plus sur les listes de personnes"}

>[!TAB Libellés de nœud de Parcours]

Ajoutez des libellés d’affichage aux nœuds dans les parcours de compte et de personne pour distinguer les étapes similaires et clarifier leur objectif sur la zone de travail du parcours.

[!BADGE En savoir plus]{type=Informative url="/help/user/journeys/create-publish-journey.md#label-a-node" tooltip="En savoir plus sur les libellés des nœuds de parcours"}

>[!TAB parcours de personne]

Orchestrez le marketing basé sur les leads avec des parcours de personne, qui utilisent les audiences et les données [!DNL Adobe Experience Platform] pour interagir avec des personnes individuelles. Les parcours de personne prennent désormais en charge les nœuds _Écouter un événement_, l’action externe, les chemins de partage externes, ainsi que la rentrée du parcours. Utilisez-les avec des parcours de compte et des groupes d&#39;achat pour orchestrer le parcours d&#39;achat complet.

[!BADGE En savoir plus]{type=Informative url="/help/user/journeys/journeys-overview.md" tooltip="En savoir plus sur les parcours de personne"}

>[!TAB Chemins de division des variantes]

Testez les variations au sein d’un parcours de compte ou de personne en attribuant des comptes ou des personnes à différents chemins de parcours en fonction des pourcentages que vous définissez. Dans les parcours de personne, l’affectation est déterministe, de sorte que chaque personne suit toujours le même chemin, qui prend en charge les expériences contrôlées.

[!BADGE En savoir plus]{type=Informative url="/help/user/journeys/variant-split-paths-nodes.md" tooltip="En savoir plus sur les chemins de partage des variantes"}

>[!TAB Optimisation de l’heure d’envoi]

Pour les nœuds d’action _Envoyer un e-mail_ dans les parcours de personne, vous pouvez désormais utiliser l’optimisation de l’heure d’envoi pour personnaliser le délai de diffusion des e-mails. Le système prédit le moment où chaque personne est le plus susceptible d’engager et planifie la diffusion en conséquence, plutôt que de l’envoyer à tous les destinataires en même temps.

[!BADGE En savoir plus]{type=Informative url="/help/user/content/email-send-time-optimization.md" tooltip="Découvrez l’optimisation de l’heure d’envoi"}

>[!TAB rentrée de Parcours]

Vous pouvez désormais envoyer plusieurs fois des comptes ou des personnes par le biais d’un parcours de compte ou de personne. La rentrée concerne plusieurs scénarios, tels que la réévaluation des critères de qualification et les workflows de maturation réutilisables. Utilisez les paramètres de rentrée pour définir des critères, des limites et des temps d’attente afin que les comptes ou les personnes se qualifient à nouveau pour le parcours de manière contrôlée.

[!BADGE En savoir plus]{type=Informative url="/help/user/journeys/journey-re-entry.md" tooltip="En savoir plus sur la rentrée dans le parcours"}

>[!ENDTABS]

## Commencer l’exploration {#section-explore}

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

Dernières notes de mise à jour

Restez informé des dernières notes de mise à jour, des nouvelles fonctionnalités et des améliorations de [!DNL Adobe Journey Optimizer B2B Edition].

[Afficher les notes de mise à jour](./release-notes/release-notes.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

Commencer

Consultez les conseils d’intégration [!DNL Journey Optimizer B2B Edition] pour les administrateurs et les spécialistes du marketing.

[Liste de contrôle pour les administrateurs](./setup-ultimate.md)

[Intégration des utilisateurs](./start/get-started.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

Gestion Des Données

Activez les schémas et champs XDM que vous souhaitez utiliser dans [!DNL Adobe Journey Optimizer B2B Edition] et découvrez le fonctionnement de ses données dans [!DNL Adobe Experience Platform].

[Afficher la gestion des champs XDM](./admin/xdm-field-management.md)
[Jeux de données exportés](./data/aep-exported-datasets.md)
[Requêtes de jeu de données](./data/aep-query-examples.md)
[Disponibilité des données et synchronisation](./data/data-availability-timing.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

Canaux de communication

Configurez et gérez les e-mails, SMS, WhatsApp et d’autres canaux pour les interactions personnalisées des clients.

[Configurer le canal e-mail](./admin/configure-channels-emails.md)
[Configurer le canal SMS](./admin/configure-channels-sms.md)
[Configurer le canal WhatsApp](./admin/configure-channels-whatsapp.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

Créer un parcours

Concevez, orchestrez, gérez et optimisez des parcours de compte et de personne personnalisés.

[Explorer les Parcours](./journeys/journeys-overview.md)
[Utiliser des listes de comptes dans parcours](./accounts/account-lists-journeys.md)
[Utiliser des listes de personnes dans les parcours](./audiences/people-lists-journeys.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/users.svg?lang=fr)

Comprendre les groupes d&#39;achat

Conseils détaillés sur la création, la gestion et l&#39;optimisation des groupes d&#39;achats pour un ciblage efficace.

[Comprendre les groupes d&#39;achats](./buying-groups/buying-groups-overview.md)
[Créer des groupes d&#39;achats](./buying-groups/buying-groups-create.md)
:::

::::

<!--
:::
![icon](https://cdn.experienceleague.adobe.com/icons/image.svg)

Design Content

Learn how to author and manage content for personalized customer experiences orchestrated through journeys.

[Explore Content Components](./content/content-components.md)
::: 
-->

## Démonstration de présentation

Découvrez les composants d’un groupe d’achat et les principes de base de la création d’un parcours de compte.

>[!VIDEO](https://video.tv.adobe.com/v/3432054?quality=12)

## Explorer la documentation

<table style="table-layout:auto">
  <tr style="border: 0;">
    <td>
      <img src="../assets/do-not-localize/icon-quick-start.svg" width="35px" alt="Commencer"><br/>
      <strong>Prise en main</strong><br/><a href="home-page.md">Page de connexion et d’accueil</a><br/><a href="./start/get-started.md">Conseils d’intégration</a> <br/><a href="./ai-coworker/ai-overview.md">Fonctionnalités d’IA</a>
    </td>
    <td>
      <img src="../assets/do-not-localize/icon_audience.svg" width="35px" alt="Groupes d’achat"><br/>
      <strong>Groupes d’achat</strong><br/><a href="./buying-groups/buying-groups-overview.md">Vue d’ensemble des groupes d’achat</a><br/><a href="./buying-groups/buying-groups-role-templates.md">Modèles de rôle</a><br/><a href="./buying-groups/solution-interests.md">Intérêts de la solution</a><br/><a href="./buying-groups/buying-groups-create.md">Créer des groupes d’achat</a>
    </td>
    <td>
      <img src="../assets/do-not-localize/icon-paths.svg" width="35px" alt="Parcours"><br/>
      <strong>Présentation des Parcours</strong><br/><a href="./journeys/journeys-overview.md">Parcours</a><br/><a href="./journeys/create-publish-journey.md#create-a-journey">Création d’un parcours de compte ou de personne</a><br/><a href="./journeys/journey-nodes.md">Nœuds de Parcours</a>
    </td>
  </tr>
  <tr style="border: 0;">
    <td>
      <img src="../assets/do-not-localize/icon-campaign.svg" width="35px" alt="Contenu de parcours"><br/>
      <strong>Contenu de Parcours</strong><br/><a href="./content/add-email.md">Canal e-mail</a><br/><a href="./content/generate-content-emails.md">Générer du contenu e-mail</a><br/><a href="./content/genstudio-email-workflow.md">Expériences e-mail GenStudio</a><br/><a href="./content/sms-authoring.md">Canal SMS</a>
    </td>
        <td>
      <img src="../assets/do-not-localize/icon_assets.svg" width="35px" alt="Gestion de contenu"><br/>
      <strong>Gestion de contenu</strong><br/><a href="./content/assets-overview.md">Présentation d’Assets</a><br/><a href="./content/email-templates.md">Modèles d’e-mail</a><br/><a href="./content/fragments.md">Fragments visuels</a><br/><a href="./content/conditional-content.md">Contenu conditionnel</a><br/><a href="./content/brand-themes.md">Thèmes de marque</a>
    </td>
    <td>
      <img src="../assets/do-not-localize/icon-offer.svg" width="35px" alt="Informations et tableaux de bord"><br/>
      <strong>Informations</strong><br/><a href="./dashboards/intelligent-dashboard.md">Tableau de bord intelligent</a><br/><a href="./dashboards/engagement-dashboard.md">Tableau de bord de l’engagement</a><br/><a href="./dashboards/buying-groups-dashboard.md">Tableau de bord des groupes d’achat</a><br/><a href="./dashboards/journeys-dashboard.md">Tableau de bord des Parcours</a><br/><a href="./buying-groups/incrm-insights.md">Informations dans le CRM</a>
    </td>
   </tr>
</table>

>[!BEGINSHADEBOX]

## [!DNL Marketo Qualifier]

[!DNL Adobe Marketo Qualifier] est une application gérée par l’IA que vous pouvez utiliser avec [!DNL Journey Optimizer B2B Edition]. Il met en œuvre la compétence Qualification du compte et est conçu pour rationaliser les workflows pour les représentants du développement commercial (BDR). [!DNL Marketo Qualifier] automatise les workflows de qualification des prospects, de sensibilisation et d’engagement des acheteurs sur l’ensemble des canaux. Il réduit la charge manuelle de BDR et accélère la vitesse du pipeline pour les entreprises B2B.

Pour plus d&#39;informations, consultez la [documentation de Marketo Qualifier](https://experienceleague.adobe.com/fr/docs/marketo-qualifier/using/home){target="_blank"}.

>[!ENDSHADEBOX]

## Ressources supplémentaires

<table style="table-layout:fixed">
<tr><td><strong>Adobe Journey Optimizer B2B Edition</strong><br/>
<a href="https://experienceleague.adobe.com/fr/docs/journey-optimizer-b2b-learn/tutorials/overview" target="_blank">Vidéos et tutoriels</a> - <a href="https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html" target="_blank">Description du produit</a> <!-- - <a href="https://www.adobe.com/content/dam/cc/en/security/pdfs/AJO_SecurityOverview.pdf" target="_blank">Security overview (PDF)</a> - <a href="https://developer.adobe.com/journey-optimizer-apis/" target="_blank">APIs reference</a> - <a href="https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html" target="_blank">Journey Optimizer Schema Dictionary</a> -->
</td>
<td><strong>Adobe Experience Platform</strong><br/>
<a href="https://experienceleague.adobe.com/fr/docs/experience-platform/landing/home" target="_blank">Documentation</a> - <a href="https://business.adobe.com/fr/products/experience-platform/documentation-and-developer-resources.html" target="_blank">Ressources pour les développeurs</a>
</td></tr>
<tr><td><strong>Adobe Real-Time Customer Data Platform</strong><br/>
<a href="https://experienceleague.adobe.com/fr/docs/experience-platform/rtcdp/home" target="_blank">Documentation</a> - <a href="https://experienceleague.adobe.com/fr/docs/platform-learn/getting-started-for-data-architects-and-data-engineers/overview" target="_blank">Tutoriels pour les développeurs</a>
</td><td><strong>Adobe Marketo Engage</strong><br/>
<a href="https://experienceleague.adobe.com/fr/docs/marketo/using/home" target="_blank">Documentation utilisateur</a> - <a href="https://experienceleague.adobe.com/fr/docs/marketo-developer/marketo/home" target="_blank">Documentation développeur</a>
</td>
</tr></table>
