---
title: Groupes d’achat
description: 'Optimisez l’Account-Based Marketing (ABM) avec des groupes d’achat : identifiez les décideurs/décideuses, suivez les scores d’engagement et automatisez le ciblage dans Journey Optimizer B2B Edition.'
feature: Buying Groups
role: User
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: b10d4af2ae69549ab9b7d571afa25548052c6816
workflow-type: ht
source-wordcount: '1193'
ht-degree: 100%

---


# Groupes d’achat

Pour les activités de vente et de marketing B2B, les comptes sont la clé de toute stratégie. Chaque compte est associé à un groupe de personnes, qui peuvent être des employés du compte ou des sous-traitants qui travaillent avec le compte. Les comptes sont hiérarchisés et différents produits peuvent être vendus à différents niveaux de la hiérarchie. Par exemple, Adobe Experience Platform peut être vendu au niveau de l’entreprise à un compte de niveau supérieur. Quant à Adobe Photoshop, il peut être vendu à un compte qui représente une division ou un service au sein d’une organisation, par exemple un service de conception au sein d’une grande entreprise.

![Diagramme des rôles de compte](assets/account-roles-diagram.png){width="800"}

Dans le compte, il peut y avoir un sous-ensemble de personnes qui composent le _groupe d’achat_. Ce sont ces personnes qui prennent la décision d’achat. Elles ont donc besoin d’une attention particulière de la part des spécialistes du marketing et peuvent avoir besoin d’informations différentes de celles fournies aux autres personnes associées au compte. Les groupes d’achat peuvent comprendre un groupe différent de personnes pour différentes gammes de produits ou offres. Par exemple, en ce qui concerne les produits de cybersécurité, il est généralement nécessaire qu’une personne responsable des systèmes d’information ou de la sécurité, ainsi qu’un représentant ou une représentante du service juridique approuvent l’achat. Pour un produit de suivi des bugs, une personne vice-présidente de l’ingénierie et un directeur ou une directrice informatique doivent généralement figurer au sein du groupe d’achat.

![Icône vidéo](../../assets/do-not-localize/icon-video.svg){width="30"} [Regarder la vidéo de présentation](#overview-video)

## Composants clés

Vous pouvez accroître l’efficacité marketing en établissant des groupes d’achat qui identifient les personnes membres de vos listes de comptes cibles en fonction des solutions que vos équipes commerciales sont chargées de vendre. Avant que vous et votre équipe marketing ne commenciez à créer vos groupes d’achat, assurez-vous que les composants clés sont définis. Ces composants sont essentiels pour atteindre les buts et objectifs de votre entreprise.

| Composant | But |
| --------- | ------- |
| Intérêt de la solution | Ce composant fournit la réponse aux questions suivantes : <ul><li>En tant qu’organisation de marketing, que vendez-vous ?</li><li>Quels produits ou gammes de produits souhaitez-vous vendre ?</li></ul>  **_Exemple:_** Vente croisée de nouveaux produits X à des clientes et clients existants |
| Audience de compte | Ce composant fournit la réponse aux questions suivantes : <ul><li>À qui vendez-vous ?</li><li>Quelle est la liste des comptes ciblés ?</li></ul> **_Exemple:_** Segment de compte défini par des comptes avec le produit Y dont le chiffre d’affaires est supérieur à 1 million |
| Modèles de rôles du groupe d’achat | Ce composant fournit la réponse aux questions suivantes : <ul><li>Quels rôles ciblez-vous ?</li><li>Quel ensemble de règles est utilisé pour déterminer qui est affecté à des rôles de groupe d’achat ?</li></ul>  **_Exemple:_** Attribuer le rôle de décisionnaire au directeur ou à la directrice marketing |
| Étapes des groupes d’achat | (Facultatif) Ce composant fournit la réponse à la question suivante : comment suivre les étapes de succès et d’échec des groupes d’achat ? |

## Affectation de membre

Les membres peuvent être affectés à un groupe d’achat ou supprimés de celui-ci de trois manières différentes. La liste suivante décrit ces méthodes d’ajout et de suppression dans l’ordre de priorité. La méthode indiquée en premier a la priorité la plus élevée et une méthode indiquée plus bas ne peut pas la remplacer.

1. **_Action manuelle_** : une action manuelle d’ajout ou de suppression de membre effectuée par un commercial ou une commerciale pour le groupe d’achat
2. **_Action de parcours_** : [nœuds d’action de parcours pour l’appartenance à un groupe d’achat](../journeys/action-nodes.md#add-a-people-based-action) (_Affecter au groupe d’achat_ ou _Supprimer du groupe d’achat_)
3. **_Traitements du système_** : traitements de [création](../buying-groups/buying-groups-create.md#buying-group-creation-jobs) et de maintenance de groupe d’achat.

Pour éviter tout remplacement incorrect de l’affectation d’une personne membre dans un groupe d’achat, cette liste suit l’ordre de priorité utilisé dans le système pour que l’affectation des personnes membres soit correcte. Par exemple, lorsqu’un commercial ou une commerciale ajoute manuellement un membre au groupe d’achat, un traitement de maintenance ne doit pas venir modifier cet ajout. Les scénarios suivants sont appliqués en suivant l’ordre de priorité :

* Si un utilisateur ou une utilisatrice affecte manuellement une personne membre à un groupe d’achat et que cette affectation est suivie d’un traitement de maintenance du groupe d’achat qui supprime cette personne membre du groupe d’achat, le traitement de maintenance **ne supprime pas** cette personne membre et ne peut pas remplacer l’affectation manuelle.
* Si un utilisateur ou une utilisatrice affecte manuellement une personne membre à un groupe d’achat et qu’ensuite un nœud de parcours déclenché supprime cette personne membre du groupe d’achat, l’action de nœud **ne supprime pas** cette personne membre et ne peut pas remplacer l’affectation manuelle.
* Si un nœud d’action de parcours déclenché ajoute une personne membre à un groupe d’achat et que cet ajout est suivi d’un traitement de maintenance du groupe d’achat qui supprime cette personne membre du groupe d’achat, le traitement de maintenance **ne supprime pas** cette personne membre et ne peut pas remplacer l’affectation d’action de parcours.

>[!NOTE]
>
>Les tâches de maintenance des groupes d’achats automatisés s’exécutent chaque jour, à partir de la version 2025.10.

## Workflow du groupe d’achat

1. Créez des groupes d’achats.

   * Définir l’[intérêt de la solution](./solution-interests.md) et le [modèle de rôle](./buying-groups-role-templates.md)
   * [Créez le groupe d’achat](./buying-groups-create.md#create-buying-groups), puis affectez les [étapes du groupe d’achat](./buying-group-stages.md).

1. Identifiez les personnes manquantes par exhaustivité.

   Analysez le groupe d’achat à l’aide de filtres.

   **_Exemple:_** Le rôle de décisionnaire est manquant et le score d’exhaustivité est &lt; 50.

1. Renseignez les définitions des groupes d’achat.
<!--
   * Acquire missing people
   * Send to LinkedIn Destination
   * Enrich with Zoominfo -->

1. Ajoutez des actions de groupe d’achat à vos parcours de compte.

## Afficher les groupes d’achat et les composants

Dans le volet de navigation de gauche, développez **[!UICONTROL Comptes]** et cliquez sur **[!UICONTROL Groupes d’achat]**.

La page _[!UICONTROL Groupes d’achat]_ est organisée sous forme d’onglets :

| Tabulation | Description |
| --- | ----------- |
| [!UICONTROL Vue d’ensemble] | Cet onglet est le tableau de bord par défaut et affiche le [tableau de bord des groupes d’achats](../dashboards/buying-groups-dashboard.md). |
| [!UICONTROL Parcourir] | Cet onglet prend en charge les activités suivantes : <ul><li>Afficher la liste des groupes d’achat existants. </li><li>Effectuez une recherche par nom de groupe d’achat. </li><li>Filtrer par intérêt de la solution. </li><li>Accéder aux détails du groupe d’achat. </li><li>Créez un groupe d’achat. </li></ul> |
| [!UICONTROL Intérêt de la solution] | Cet onglet prend en charge les activités suivantes : <ul><li>Afficher la liste des groupes d’achat existants. </li><li>Effectuez une recherche par nom de groupe d’achat. </li><li>Accéder aux propriétés d’intérêt de la solution et les modifier. </li><li>Créer un intérêt de la solution. </li><li>Supprimer un intérêt de la solution. </li><li>Afficher et supprimer des tâches de groupe d’achat. </li></ul> |
| [!UICONTROL Modèles de rôles] | Cet onglet prend en charge les activités suivantes : <ul><li>Afficher la liste des modèles de rôles existants. </li><li>Rechercher par nom de modèle de rôles. </li><li>Accéder aux propriétés et conditions du modèle de rôles et les modifier. </li><li>Créer un modèle de rôles. </li><li>Supprimer un modèle de rôles. </li></ul> |
| [!UICONTROL Étapes] | Cet onglet prend en charge les activités suivantes : <ul><li>Afficher le modèle des étapes de groupes d’achat existants. </li><li>Accéder au modèle de brouillon des étapes de groupe d’achat et le modifier. </li><li>Créer le modèle des étapes du groupe d’achat. </li></ul> |

## Rechercher et filtrer des groupes d’achat

Utilisez l’onglet _[!UICONTROL Parcourir]_ pour accéder à la liste des groupes d’achat. Vous pouvez effectuer une recherche par nom et filtrer la liste par intérêt de la solution.

![Page de navigation des groupes d’achat](assets/buying-groups-browse.png){width="800" zoomable="yes"}

## Détails du groupe d’achat

Pour accéder aux détails d’un groupe d’achats, cliquez sur le nom du groupe d’achat dans l’onglet _[!UICONTROL Parcourir]_. [En savoir plus](./buying-group-details.md)

![Détails du groupe d’achat](assets/buying-group-details.png){width="600" zoomable="yes"}

### Score d’exhaustivité du groupe d’achat

Le score d’exhaustivité est utilisé pour déterminer si le groupe d’achat dispose des bons rôles attribués au bon nombre de personnes membres et s’il peut être utilisé dans un parcours de compte. Ce score est un pourcentage basé sur le nombre de rôles au sein du groupe d’achat et sur l’exhaustivité de chacun des rôles définis.

Le calcul initial du score d’exhaustivité commence dès la création du groupe d’achat. Il est recalculé quotidiennement et à chaque fois qu’un groupe d’achat est créé ou mis à jour.

Voir la section [Scores d’exhaustivité](./completeness-scores.md) pour obtenir des informations détaillées sur les notations et les calculs d’exhaustivité.

### Score d’engagement du groupe d’achat {#engagement-score}

Le score d’engagement est basé sur les activités des personnes membres du groupe d’achat, les actions pondérées et les rôles pondérés. Le score obtenu est normalisé dans le client/l’instance afin de permettre une comparaison cohérente et de disposer d’informations exploitables.

Le calcul du score d’engagement initial commence dès que vous créez le groupe d’achat et est recalculé quotidiennement.

Consultez la section [Scores d’engagement](./engagement-scores.md) pour des informations détaillées sur les activités et les calculs de score d’engagement.

## Vidéo de présentation

>[!VIDEO](https://video.tv.adobe.com/v/3452929/?captions=fre_fr&learn=on)
