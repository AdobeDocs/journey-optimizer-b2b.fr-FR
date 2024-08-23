---
title: Groupes d’achat
description: Découvrez comment acheter des groupes et leurs composants.
feature: Buying Groups
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: 5e500f616dcbbebcdfacfead9ae386b523a4d1a4
workflow-type: tm+mt
source-wordcount: '1186'
ht-degree: 6%

---


# Groupes d’achat

Pour les activités de vente et de marketing B2B, les comptes sont essentiels à toute stratégie. Chaque compte est associé à un groupe de personnes, qui peuvent être des employés du compte ou des sous-traitants qui travaillent avec le compte. Les comptes sont hiérarchiques et différents produits peuvent être vendus à différents niveaux de la hiérarchie. Par exemple, Adobe Experience Platform peut être vendu au niveau de l’entreprise à un compte de niveau supérieur, tandis qu’Adobe Photoshop peut être vendu à un compte représentant une division ou un département au sein d’une organisation, par exemple un service de conception au sein d’une plus grande entreprise.

![ Diagramme de rôles de compte ](assets/account-roles-diagram.png){width="800"}

Dans le compte, il peut y avoir un sous-ensemble de personnes qui composent le _groupe d’achats_. Il s’agit des personnes qui prennent la décision d’achat. Elles ont donc besoin d’une attention particulière de la part du marketeur et peuvent avoir besoin d’informations différentes de celles des autres personnes associées au compte. Les groupes d’achats peuvent comprendre un groupe de personnes différent pour différentes lignes de produits ou offres. Par exemple, un produit de cybersécurité peut généralement nécessiter l’approbation d’un achat par un directeur de l’information ou un directeur de la sécurité, ainsi qu’un représentant du service juridique. Cependant, un produit de suivi des bogues peut généralement avoir un vice-président en ingénierie et un Director informatique en tant que membres du groupe d’achats.

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

## Affichage des groupes d’achat et des composants

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

Le score d’engagement d’un groupe d’achat est un nombre permettant de déterminer l’engagement des membres d’un groupe d’achat en fonction des activités qu’ils effectuent. Toute activité entrante effectuée par les membres du groupe d&#39;achat au cours des 30 derniers jours est utilisée pour calculer le score.

Chaque activité est limitée à 20 fréquences par jour. Si un membre d’un groupe d’achat exécute la même activité plus de 20 fois par jour, le nombre de l’activité est plafonné à 20 et n’est pas supérieur au nombre.

Le score affiché est arrondi. Par exemple, un score de 75,89999 s’affiche comme 76.

#### Pondération

Les utilisateurs peuvent affecter une _pondération_ à chaque rôle dans le modèle de rôles afin d’allouer différents poids pour un rôle afin de calculer le score d’engagement.

![Définir la pondération pour chaque rôle dans le modèle de rôles](./assets/roles-templates-weighting.png){width="700" zoomable="yes"}

Chaque niveau de pondération correspond à une valeur utilisée pour calculer le score d’engagement :

* [!UICONTROL Trivial] = 20
* [!UICONTROL Mineur] = 40
* [!UICONTROL Normal] = 60
* [!UICONTROL Important] = 80
* [!UICONTROL Vital] = 100

Un modèle de rôles avec trois rôles pondérés sous la forme _[!UICONTROL Vital]_, _[!UICONTROL Important]_ et _[!UICONTROL Normal]_ sont convertis en pourcentages pondérés suivants :

| Rôle | Pondération | Valeur système | Calcul de la valeur | Pourcentage |
|-------------- |--------- |------------- |------------------ |---------- |
|               |          |              |                   |           |
| Décisionnaire | Vital | 100 | 100/240 | 41,67 % |
| Personne influente | Important | 80 | 80/240 | 33,33 % |
| Praticien | Normal | 60 | 60/240 | 25 % |
|               | Total | 240 |                   |           |

#### Exemple de calcul

L’exemple suivant illustre le calcul du score d’engagement à l’aide du pourcentage de poids du rôle indiqué, du nombre d’activités entrantes pour chaque membre du groupe d’achats et d’une limite quotidienne de 20 pour chaque événement (s’il s’est produit à plusieurs reprises).

| Rôle | Membre | Type d’activité | Décompte d&#39;hier | Le comptage d&#39;aujourd&#39;hui | Calcul | Score total |
|-------------- |--------- |-------------|-----------------|-------------|------|-----------|
|               |          |             |                 |             |      |           |
| Décisionnaire | Adam | Site Web visité | 37 | 15 | 20 + 15 | 35 |
|               |          | Courriel cliqué | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Marquer | Site Web visité | 5 | 3 | 5 + 3 | 8 |
|               |          | Courriel cliqué | 1 | 1 | 1 + 1 | 2 |
|               |          | Pub téléchargé | 3 | 2 | 3 + 2 | 5 |
| **Score total des décideurs** |         |             |                 |             |      | **52** |
|               |          |             |                 |             |      |           |
| Personne influente | John | Site Web visité | 19 | 9 | 19 + 9 | 28 |
| **Score total des influenceurs** |         |             |                 |             |      | **28** |
|               |          |             |                 |             |      |           |
| Praticien | Bob | Courriel cliqué | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Paul | Courriel cliqué | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Calvin | Courriel cliqué | 1 | 1 | 1 + 1 | 2 |
|               |          | Site Web visité | 1 | 7 | 1 + 7 | 8 |
|               |          | Pub téléchargé | 1 | 2 | 1 + 2 | 3 |
| **Score total des praticiens** |         |             |                 |             |      | **17** |

Le score final de l’engagement est calculé en appliquant la pondération pour chacun des scores de rôle :

| Rôle | Score total du rôle | Poids du rôle % | Score X weight % |
|-------------- |---------------- |------------- |---------------- |
| Décisionnaire | 52 | 41,67 % | 21,67 |
| Les plus influents | 28 | 33,33 % | 9,33 |
| Praticiens | 17 | 25 % | 4,25 |
| **Score final d’engagement** |                |             | **35.25** |
