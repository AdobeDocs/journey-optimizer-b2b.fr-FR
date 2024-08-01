---
title: Groupes d’achat
description: Découvrez comment acheter des groupes et leurs composants.
feature: Buying Groups
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: 78d82aa8b3bb8b8d432eeb187d75e2354dbff3ee
workflow-type: tm+mt
source-wordcount: '1004'
ht-degree: 7%

---


# Groupes d’achat

Pour les activités de vente et de marketing B2B, les comptes sont essentiels à toute stratégie. Chaque compte est associé à un groupe de personnes, qui peuvent être des employés du compte ou des sous-traitants qui travaillent avec le compte. Les comptes sont hiérarchiques et différents produits peuvent être vendus à différents niveaux de la hiérarchie. Par exemple, Adobe Experience Platform peut être vendu au niveau de l’entreprise à un compte de niveau supérieur, tandis qu’Adobe Photoshop peut être vendu à un compte représentant une division ou un département au sein d’une organisation, par exemple un service de conception au sein d’une plus grande entreprise.

![ Diagramme de rôles de compte ](assets/account-roles-diagram.png){width="800"}

Dans le compte, il peut y avoir un sous-ensemble de personnes qui composent le _groupe d’achats_. Ces personnes sont celles qui prennent la décision d’achat. Elles ont donc besoin d’une attention particulière de la part du marketeur et peuvent avoir besoin d’informations différentes de celles des autres personnes associées au compte. Les groupes d’achats peuvent comprendre un groupe de personnes différent pour différentes lignes de produits ou offres. Par exemple, un produit de cybersécurité peut généralement nécessiter l’approbation d’un achat par un directeur de l’information ou un directeur de la sécurité, ainsi qu’un représentant du service juridique. Cependant, un produit de suivi des bogues peut généralement avoir un vice-président en ingénierie et un Director informatique en tant que membres du groupe d’achats.

## Composants clés

Vous pouvez accroître l’efficacité marketing en établissant des groupes d’achat dans l’édition B2B de Journey Optimizer qui identifient les membres manquants pour vos listes de comptes cibles en fonction des solutions que vos équipes de vente sont responsables de la vente. Avant de commencer à créer vos groupes d’achats avec votre équipe marketing, assurez-vous que les composants clés sont définis. Ces composants sont essentiels pour atteindre vos objectifs commerciaux.

| Composant | But |
| --------- | ------- |
| Intérêt de la solution | Ce composant fournit la réponse à : <ul><li>En tant qu&#39;organisation marketing, que vendez-vous ?</li><li>Quel produit ou collection de produits ciblez-vous vendre ?</li></ul>  **_Exemple :_** vente croisée du nouveau produit X aux clients existants |
| Audience (comptes) | Ce composant fournit la réponse à : <ul><li>À qui vendez-vous ?</li><li>Quelle est la liste des comptes ciblés ?</li></ul> **_Exemple :_** segment de compte défini par des comptes avec le produit Y dont les recettes dépassent 1M |
| Modèles de rôle de groupe d’achat | Ce composant fournit la réponse à : <ul><li>Quels rôles ciblez-vous ?</li><li>Quel ensemble de règles est utilisé pour déterminer qui est affecté à l’achat de rôles de groupe ?</li></ul>  **_Exemple :_** Affectez une personne avec un titre CMO au rôle du décideur |

## Workflow du groupe d’achats

1. Créez des groupes d’achat.

   Options :
   * Utilisation de [l’intérêt de la solution](./solution-interests.md) et [ modèle de rôle](./buying-groups-role-templates.md)
   * Utilisation de l’importation tierce
   * Génération à partir d’AI/ML

1. Identifier les personnes disparues.

   Analysez le groupe d’achat à l’aide de filtres.

   **_Exemple :_** Le rôle du décideur est manquant et le score d’exhaustivité est &lt; 50

1. Renseignez les définitions des groupes d’achat.
<!--
   * Acquire missing people
   * Send to LinkedIn Destination
   * Enrich with Zoominfo -->

1. Utilisation dans un parcours de compte par l’intermédiaire des centres d’intérêt de solution associés.

## Accès aux groupes d’achat et aux composants

Dans le volet de navigation de gauche, développez **[!UICONTROL Comptes]** et cliquez sur **[!UICONTROL Groupes d’achats]**.

La page _[!UICONTROL Groupes d&#39;achats]_ est organisée sous la forme d&#39;onglets :

| Tabulation | Description |
| --- | ----------- |
| [!UICONTROL Vue d’ensemble] | Cet onglet est la valeur par défaut et affiche le [tableau de bord des groupes d’achats](../dashboards/buying-groups-dashboard.md). |
| [!UICONTROL Parcourir] | Cet onglet prend en charge les activités suivantes : <ul><li>Affichez la liste des groupes d’achats existants. </li><li>Effectuez une recherche en achetant le nom du groupe. </li><li>Filtrez par intérêt de solution. </li><li>Découvrez comment acheter les détails du groupe. </li><li>Créez un groupe d’achats. Supprimez un groupe d’achats.</li></ul> |
| [!UICONTROL  Centres d’intérêt de solution] | Cet onglet prend en charge les activités suivantes : <ul><li>Affichez la liste des groupes d’achats existants. </li><li>Effectuez une recherche en achetant le nom du groupe. </li><li>Accédez aux propriétés d’intérêt de la solution et modifiez-les. </li><li>Créez un intérêt pour la solution. </li><li>Supprimez les centres d’intérêt d’une solution. </li><li>Affichez et supprimez les tâches de groupe d’achat. </li></ul> |
| [!UICONTROL Modèles de rôles] | Cet onglet prend en charge les activités suivantes : <ul><li>Affichez la liste des modèles de rôles existants. </li><li>Recherche par nom de modèle de rôles. </li><li>Accédez aux propriétés et aux conditions du modèle de rôles et modifiez-les. </li><li>Créez un modèle de rôles. </li><li>Supprimez un modèle de rôles. </li></ul> |

## Recherche et filtrage de groupes d’achat

Utilisez l’onglet _[!UICONTROL Parcourir]_ pour afficher la liste des groupes d’achats. Vous pouvez effectuer une recherche par nom et filtrer la liste par intérêt de solution.

![Page de navigation du groupe d’achats](assets/buying-groups-browse.png){width="800" zoomable="yes"}

## Détails du groupe d’achat

Pour accéder aux détails d’un groupe d’achats, cliquez sur le nom du groupe d’achats dans l’onglet _[!UICONTROL Parcourir]_ .

![Détails du groupe d’achat](assets/buying-group-details.png){width="600" zoomable="yes"}

### Score d’achèvement du groupe d’achat

Le score d’exhaustivité permet de déterminer si le groupe d’achats est terminé, ce qui signifie qu’il dispose des membres appropriés affectés aux rôles et qu’il est prêt à être utilisé dans un parcours de compte. Ce score est un pourcentage basé sur le nombre de rôles au sein du groupe d’achat et le nombre de rôles attribués avec au moins une piste.

Par exemple, s’il existe quatre rôles au sein d’un groupe d’achat et que trois des quatre rôles sont attribués à au moins un prospect, le groupe d’achat est complet à 75 %.

Le score d’exhaustivité du groupe d’achat est recalculé chaque fois qu’un groupe d’achat est créé ou mis à jour.

### Score d’engagement du groupe d’achat

Le score d’engagement est utilisé pour évaluer l’efficacité de vos programmes marketing en fonction des activités comportementales de groupe d’achat suivies sur plusieurs parcours. Ce score est dérivé de l’activité au cours des 30 derniers jours. Tout changement de rôle apporté à un modèle nécessite un recalcul du score d’engagement pour tous les groupes d’achats créés à l’aide de ce modèle. Seules les activités entrantes sont évaluées dans le calcul d’un score d’engagement.

Le score affiché est arrondi (par exemple, un score de 75.89999 est affiché comme 76), il n’existe aucune limite supérieure pour le score de disponibilité générale et un plafond de fréquence quotidienne de 20.

Les exemples suivants illustrent le calcul du score d’engagement :

**Groupe d’achat 1** - score d’engagement = 22,15

| Utilisateur | Rôle | Pondération de rôle | Action | Today | Hier | Poids de l’action | Score |
| ---- | ---- | ----------- | ------ | ----- | --------- | ------------- | ----- |
| Adam | Décisionnaire | 80 % | Site Web visité | 1000 | 2 | 1 | 22 |
| | | | E-mail cliqué | 1 | 0 | 1 | 1 |
| | | | Pub téléchargé | 1 | 3 | 1 | 4 |
| Bob | Personne influente | 15 % | Site Web visité | 1 | 2 | 1 | 3 |
| Calvin | Praticien | 5 % | Site Web visité | 1 | 1 | 1 | 2 |

**Groupe d’achats 2** - Score d’engagement = 8,55

| Utilisateur | Rôle | Pondération de rôle | Action | Today | Hier | Poids de l’action | Score |
| ---- | ---- | ----------- | ------ | ----- | --------- | ------------- | ----- |
| Alvin | Décisionnaire | 80 % | Site Web visité | 3 | 2 | 1 | 5 |
| | | | E-mail cliqué | 1 | 0 | 1 | 1 |
| | | | Pub téléchargé | 1 | 3 | 1 | 4 |
| Bret | Personne influente | 15 % | Site Web visité | 1 | 2 | 1 | 3 |
| Cam | Praticien | 5 % | Site Web visité | 1 | 1 | 1 | 2 |
