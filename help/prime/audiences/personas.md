---
title: Personnages dérivés
description: Utilisez les rôles dérivés dans Journey Optimizer B2B Prime pour cibler les listes de personnes et les chemins d’accès aux parcours. Découvrez les mappages de persona par défaut et le filtre de persona dérivé.
badgeBeta: label="Beta" type="informative" tooltip="Cette fonctionnalité est actuellement en version bêta limitée"
autotag-review: '2026-06-23T22:01:21.605Z'
TQID: 'https://experienceleague.adobe.com/OZ4GDkaqg9a5Aikic-m-f0MtHSpc3BO0h41fTAL1Rww'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: beb5f4be-cec3-471a-9db6-831a77dd3ac9id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: c3d6e661-d372-4e98-9fd9-eac771e7e4ee
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 47afe74615b02c805ef0a931e54899cbc2f30a05
workflow-type: tm+mt
source-wordcount: 636
ht-degree: 2%

---

# Personnages dérivés

La classification des personas transforme les données client brutes en une compréhension sémantique des acheteurs que l’IA peut utiliser pour générer du contexte et orienter des décisions personnalisées sur chaque canal et parcours. Ce profil unifié permet d’effectuer les opérations suivantes :

* _Embranchement de Parcours_ - Partagez les chemins d’accès des prospects par rôle, personne et profondeur d’engagement
* _Arbitrage de Parcours_ - Détermine à quelle culture un prospect appartient en ce moment, évitant les collisions de messages entre les programmes simultanés
* _Personnalisation du contenu_ - Contenu comprenant des récits spécifiques au rôle (« pour un cadre » ou « pour un professionnel ou une professionnelle »)
* _Contexte du qualificateur de vente_ - Les BDR reçoivent un résumé sur un seul écran qui indique « qui est cette personne, ce qui leur importe, où elle se trouve sur le parcours des acheteurs »

## Personnages par défaut {#default-ersonas}

Pour la version Beta de Journey Optimizer B2B Prime, les rôles par défaut suivants sont définis en fonction de l’attribut de titre du poste :

| Persona | Titres de poste |
| ------- | ---------- |
| [!UICONTROL PDG/PDV] | PDG, DPI, directeur des technologies de l’information, directeur financier, vice-président exécutif de la stratégie |
| [!UICONTROL SVP/VP] | Vice-président principal du marketing, vice-président directeur des ventes, vice-président directeur des opérations, vice-président directeur des produits, vice-président directeur informatique |
| [!UICONTROL Cadre supérieur / Responsable] | Responsable marketing principal, responsable informatique, responsable des opérations, responsable des ventes, responsable des ressources humaines |
| [!UICONTROL Contributeur individuel] | Responsable de compte, Ingénieur logiciel, Spécialiste marketing, Représentant du succès client |
| [!UICONTROL Analyste] | Analyste commercial, Analyste des données, Analyste des études de marché, Analyste financier, Analyste des opérations |
| [!UICONTROL Développeur ou développeuse] | Développeur front-end, Développeur back-end, Développeur full-stack, Développeur d’applications mobiles, Ingénieur DevOps |
| [!UICONTROL Professionnels] | Spécialiste RH, Conseiller juridique, Responsable de la conformité, Chef de projet, Spécialiste des achats |
| [!UICONTROL Consultant] | Consultant en gestion, conseiller en TI, consultant en processus d&#39;affaires, consultant en marketing |
| [!UICONTROL Other] (Autre) | Spécialiste de l&#39;industrie, conseiller indépendant, consultant indépendant, expert en la matière |

>[!NOTE]
>
>Dans la mise à jour de disponibilité générale, vous pourrez modifier l’une de ces personnalités par défaut en fonction des besoins de votre entreprise. Il prend également en charge les définitions de persona personnalisées et le mappage.

## Filtrer par persona dérivé {#derived-persona-filter}

Le Prime B2B de Journey Optimizer dérive un persona pour chaque enregistrement de personne en évaluant les attributs de l’enregistrement par rapport aux personas définis. _Vous pouvez utiliser le résultat déduit (« Persona dérivé_) comme filtre lors de la définition de l’audience pour une liste de personnes ou un parcours de personnes.

Le filtre _[!UICONTROL Persona dérivé]_ s’affiche dans le panneau de filtrage sous la catégorie **[!UICONTROL Attributs de personne]**.

![Accéder aux rôles configurés](../../user/admin/assets/configuration-persona-mapping.png){width="800" zoomable="yes"}

### Listes de personnes {#people-lists}

Lorsque vous ajoutez ou supprimez des membres d’une [liste de personnes statique](./people-lists.md#static-list), ou lorsque vous définissez les règles d’appartenance à une [liste de personnes dynamique](./people-lists.md#dynamic-lists), vous pouvez filtrer par persona dérivé pour cibler toutes les personnes dont les attributs correspondent à une personne configurée spécifique.

**Liste statique — Ajouter des membres**

1. Ouvrez la liste statique et cliquez sur **[!UICONTROL Ajouter des personnes]** en haut à droite.

1. Dans la boîte de dialogue de filtre, développez **[!UICONTROL Attributs de personne]** et faites glisser **[!UICONTROL Persona dérivé]** sur la zone de travail.

1. Dans la condition de filtre, choisissez **[!UICONTROL is]** et sélectionnez une ou plusieurs personnes dans la liste.

1. Cliquez sur **[!UICONTROL Terminé]** pour appliquer le filtre et qualifier les personnes correspondantes dans la liste.

**Liste dynamique — Définit les règles d&#39;appartenance**

1. Ouvrez la liste dynamique et sélectionnez l’onglet **[!UICONTROL Règles]**.

1. Cliquez sur **[!UICONTROL Modifier les règles]**.

1. Dans la boîte de dialogue de filtre, développez **[!UICONTROL Attributs de personne]** et faites glisser **[!UICONTROL Persona dérivé]** sur la zone de travail.

1. Dans la condition de filtre, choisissez **[!UICONTROL is]** et sélectionnez une ou plusieurs personnes dans la liste.

1. Cliquez sur **[!UICONTROL Terminé]** pour enregistrer la règle.

   L’appartenance est automatiquement mise à jour lorsque les enregistrements de la personne sont évalués par rapport à la règle.

### Parcours de personne {#person-journeys}

Lorsque vous configurez la segmentation d’un parcours de personne dans un nœud [_Partage de chemins_ ](../marketing/split-merge-paths-nodes.md), vous pouvez utiliser un persona dérivé comme filtre de profil de personne pour contrôler quelles personnes entrent dans le chemin du parcours.

1. Cliquez sur le nœud **[!UICONTROL Chemins fractionnés]** dans la zone de travail du parcours.

1. Dans le panneau des propriétés de nœud à droite, cliquez sur **[!UICONTROL Appliquer la condition]** ou **[!UICONTROL Modifier la condition]** pour un chemin d’accès.

1. Dans la boîte de dialogue de filtre, développez **[!UICONTROL Attributs de personne]** et faites glisser **[!UICONTROL Persona dérivé]** sur la zone de travail.

1. Dans la condition de filtre, choisissez **[!UICONTROL is]** et sélectionnez une ou plusieurs personnes dans la liste.

1. Cliquez sur **[!UICONTROL Terminé]** pour enregistrer le filtre du chemin d’accès.
