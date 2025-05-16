---
title: Données d’intention
description: Découvrez comment assembler et envoyer des mots-clés pour générer des données d’intention pour Journey Optimizer B2B edition.
feature: Setup, Intent, Account Insights
roles: Admin
exl-id: c7f9f6fe-2275-42a4-af80-b5c3d1a82837
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# Données d’intention

Dans Journey Optimizer B2B edition, le modèle de détection des intentions prédit une solution/un produit ciblé avec un degré de confiance suffisamment élevé en fonction de l’activité du prospect. Il tire également parti des activités des autres membres du compte, ainsi que du contenu balisé. L’intention d’une personne peut être interprétée comme la probabilité d’avoir un intérêt dans un produit.

* Niveaux d’intention - Disponibles au niveau du prospect, du compte et du groupe d’achat connus.
* Types de signal d’intention : mots-clés, produit et solution

![Visualisation des données intentionnelles](../data/assets/intent-data-visualization.png){width="700" zoomable="yes"}

Pour activer cette fonctionnalité, vous pouvez envoyer une liste de mots-clés dans une feuille de calcul à votre gestionnaire de compte Adobe. Ces mots-clés sont utilisés pour le balisage de votre contenu.

Un ensemble de mots-clés (jusqu’à 20) peut être associé à un produit. Un ensemble de produits (jusqu’à 20) peut être associé à une catégorie. Vous pouvez avoir un maximum de 20 catégories. L’ensemble de ce modèle est réalisé à l’aide d’une simple feuille de calcul ingérée. La feuille de calcul peut contenir un seul onglet correspondant au nom du produit et une seule colonne correspondant à une liste de mots-clés.

![Mots-clés de données d’intention - onglet de produit unique](./assets/intent-data-keywords-single-product-tab.png){width="500" zoomable="yes"}

Vous pouvez ajouter plusieurs onglets, chacun portant un nom de produit, et l’ensemble de la feuille de calcul peut être corrélé à une catégorie.

![Mots-clés de données d’intention - plusieurs onglets de produits](./assets/intent-data-keywords-multiple-product-tabs.png){width="500" zoomable="yes"}
