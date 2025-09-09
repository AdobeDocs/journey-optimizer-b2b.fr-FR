---
title: Groupes d’achat
description: Optimisez le marketing basé sur les comptes avec des groupes d’achats - identifiez les décideurs, suivez les scores d’engagement et automatisez le ciblage dans Journey Optimizer B2B edition.
feature: Buying Groups
role: User
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: 0eaf713deee1ae8bd04c82b6aaab0443bd60e5e7
workflow-type: tm+mt
source-wordcount: '1187'
ht-degree: 73%

---


# Groupes d’achat

Pour les activités de vente et de marketing B2B, les comptes sont la clé de toute stratégie. Chaque compte est associé à un groupe de personnes, qui peuvent être des employés du compte ou des sous-traitants qui travaillent avec le compte. Les comptes sont hiérarchisés et différents produits peuvent être vendus à différents niveaux de la hiérarchie. Par exemple, Adobe Experience Platform peut être vendu au niveau de l’entreprise à un compte de niveau supérieur. Quant à Adobe Photoshop, il peut être vendu à un compte qui représente une division ou un service au sein d’une organisation, par exemple un service de conception au sein d’une grande entreprise.

![Diagramme des rôles de compte](assets/account-roles-diagram.png){width="800"}

Dans le compte, il peut y avoir un sous-ensemble de personnes qui composent le _groupe d’achat_. Ce sont ces personnes qui prennent la décision d’achat. Elles ont donc besoin d’une attention particulière de la part des spécialistes du marketing et peuvent avoir besoin d’informations différentes de celles fournies aux autres personnes associées au compte. Les groupes d’achat peuvent comprendre un groupe différent de personnes pour différentes gammes de produits ou offres. Par exemple, en ce qui concerne les produits de cybersécurité, il est généralement nécessaire qu’une personne responsable des systèmes d’information ou de la sécurité, ainsi qu’un représentant ou une représentante du service juridique approuvent l’achat. Pour un produit de suivi des bugs, une personne vice-présidente de l’ingénierie et un directeur ou une directrice informatique doivent généralement figurer au sein du groupe d’achat.

![Icône Vidéo](../../assets/do-not-localize/icon-video.svg){width="30"} [Regardez la présentation vidéo](#overview-video)

## Composants clés

Vous pouvez accroître l&#39;efficacité du marketing en établissant des groupes d&#39;achat qui identifient les membres de vos listes de comptes cibles pour les solutions que vos équipes commerciales sont chargées de vendre. Avant que vous et votre équipe marketing ne commenciez à créer vos groupes d’achat, assurez-vous que les composants clés sont définis. Ces composants sont essentiels pour atteindre les buts et objectifs de votre entreprise.

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

Pour éviter de remplacer incorrectement une affectation de membre dans un groupe d&#39;achats, cette liste est établie dans l&#39;ordre de priorité suivi dans le système pour garantir une affectation précise des membres. Par exemple, lorsqu’un commercial ou une commerciale ajoute manuellement un membre au groupe d’achat, un traitement de maintenance ne doit pas venir modifier cet ajout. Les scénarios suivants sont appliqués en suivant l’ordre de priorité :

* Si l&#39;utilisateur affecte manuellement un membre à un groupe d&#39;achats et qu&#39;il est suivi d&#39;une tâche de maintenance du groupe d&#39;achats qui supprime le même membre du groupe d&#39;achats, la tâche de maintenance **ne supprime pas** ce membre et ne peut pas remplacer l&#39;affectation manuelle.
* Si un utilisateur affecte manuellement un membre à un groupe d&#39;achats et qu&#39;il est suivi d&#39;un nœud de parcours déclenché qui supprime le même membre du groupe d&#39;achats, l&#39;action de nœud **ne supprime pas** ce membre et ne peut pas remplacer l&#39;affectation manuelle.
* Si un nœud d&#39;action de parcours déclenché ajoute un membre à un groupe d&#39;achats et qu&#39;il est suivi d&#39;une tâche de maintenance du groupe d&#39;achats qui supprime le même membre du groupe d&#39;achats, la tâche de maintenance **ne supprime pas** ce membre et ne peut pas remplacer l&#39;affectation d&#39;action de parcours.

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

Le score d&#39;exhaustivité permet de déterminer si le groupe d&#39;achat dispose des membres appropriés affectés aux rôles et s&#39;il est prêt à être utilisé dans un parcours de compte. Ce score est un pourcentage basé sur le nombre de rôles au sein du groupe d’achat et le nombre de rôles affectés avec au moins un lead.

Par exemple, s’il existe quatre rôles au sein d’un groupe d’achat et que trois des quatre rôles sont affectés à au moins un lead, le groupe d’achat est complet à 75 %.

Le score d’exhaustivité de groupe d’achat est recalculé chaque fois qu’un groupe d’achat est créé ou mis à jour.

### Score d’engagement du groupe d’achat {#engagement-score}

Le score de l’engagement est basé sur les activités des membres du groupe d’achat, les actions pondérées et les rôles pondérés. Le score obtenu est normalisé dans le client/l’instance afin de permettre une comparaison cohérente et de disposer d’informations exploitables.

Le calcul du score de l&#39;engagement initial commence dès que vous créez le groupe d&#39;achats et est recalculé quotidiennement.

Consultez [Scores d’engagement](./engagement-scores.md) pour plus d’informations sur les activités et les calculs de score d’engagement.

## Vidéo de vue d’ensemble

>[!VIDEO](https://video.tv.adobe.com/v/3452929/?learn=on&captions=fre_fr)
