---
title: Audience Agent B2B
description: Audience Agent B2B dans l’édition B2B de Parcours Optimizer utilise l’analyse d’intention et le mappage de persona pour créer des groupes d’achat et accélérer les workflows marketing B2B.
feature: Audiences, AI Assistant
role: User
hidefromtoc: true
source-git-commit: 9cb77da73778c313392af1c42632d6b9e7e92f3b
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Audience Agent B2B

Optimisé par [Adobe Experience Platform Agent Orchestrator](https://experienceleague.adobe.com/fr/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator), Audience Agent B2B est disponible dans Journey Optimizer B2B edition. L’utilisation de cet agent améliore l’efficacité de l’exploration et de la mise à l’échelle des audiences, accélérant la création de groupes d’achats et les workflows transparents pour l’activation du parcours :

* **_Hiérarchiser les audiences cibles par intention_** - Déduisez des rôles en fonction de l’intention du produit pour diverses audiences et rationalisez la planification des campagnes, en réduisant le temps consacré à la validation des audiences.

* **_Tirez parti de l’IA pour détecter les groupes d’achat_** - Utilisez l’IA, des données structurées et non structurées et des données propriétaires unifiées pour rationaliser la découverte et la création de groupes d’achat.

![Audience Agent B2B en mode Pleine page](./assets/audience-agent-full.png){width="700" zoomable="yes"}

## Fonctionnalités d’Audience Agent

| Zone | Ce qu&#39;il fait | Valeur commerciale |
| ---- | ------------ | -------------- |
| Analyse de l’intention | <li> Mesurez l’intensité de l’intention du compte (faible, moyenne et élevée, par exemple) pour des produits spécifiques. <li>Comparez les tendances d’intérêt des produits au fil du temps (par exemple, les meilleurs produits au cours des _n_ derniers jours). <li>Identifier les comptes présentant un intérêt actif pour des produits spécifiques. <li>Affichez les modèles d’engagement qui combinent l’activité du compte à la couverture personnelle. | <li>Permet aux équipes de se concentrer sur les bons comptes au bon moment. <li>Améliore la qualité du pipeline en donnant la priorité aux comptes avec des signaux d’achat authentiques. <li>Permet un engagement proactif avant que les concurrents n’agissent. |
| Mappage de persona | <li>Détecter et classer les meilleures personnes par intention de produit. <li>Identifiez les personnes impliquées dans l’achat d’un ou de plusieurs produits. <li>Mappez les rôles aux rôles fonctionnels (champion, décideur, influenceur, etc.) avec une justification. <li>Validez pourquoi une personne donnée est considérée comme un champion. | <li>Garantit que les ventes mobilisent les véritables décideurs et influenceurs. <li>Réduit les efforts perdus sur les contacts à faible impact. <li>Augmente les taux de gain en alignant la sensibilisation avec la dynamique du pouvoir d&#39;achat. |
| Évaluation d&#39;un groupe d&#39;achat | <li>Évaluez la taille du groupe d&#39;achat (p. ex., les groupes comptant plus de n membres). <li>Mesurez la couverture personnelle entre les comptes (par exemple, sous x %). <li>Suivez la répartition des rôles et les écarts de couverture au sein des groupes d&#39;achats. <li>Mettez en évidence les comptes avec les champions identifiés dans les accords récents. | <li>Révèle des lacunes de couverture qui pourraient bloquer les transactions. <li>Renforce les stratégies multi-threads en assurant une représentation complète des rôles. <li>Améliore le suivi de l’intégrité des contrats grâce à des informations d’engagement au niveau du groupe. |

## Exemples d&#39;invites

Ces exemples d’invite illustrent plusieurs façons d’utiliser l’agent :

* Afficher la fenêtre de tendance : première et dernière mise à jour pour l’intention de produit du compte par produit.
* Par `<product>`, répertoriez les groupes d’achats avec l’intention du produit et les scores.
* Par `<product>`, répertoriez les rôles et les rôles avec leurs mesures d’opportunité (taux de succès, taux d’abonnement, nombres).
* Pour les comptes en `<industry>`, quelle est la couverture moyenne du profil de compte pour `<product>` ?
* Quels comptes ont une faible intention pour un produit, mais ont toujours des opportunités ouvertes (qui valent la peine d’être encouragées) ?
* Quels comptes ont ajouté de nouveaux signaux d’intention pour `<account_name>` cette semaine ?
