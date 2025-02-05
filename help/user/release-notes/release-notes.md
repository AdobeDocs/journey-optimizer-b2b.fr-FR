---
title: Notes de mise à jour
description: Dernières notes de mise à jour pour l’édition B2B d’Adobe Journey Optimizer
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: 9438b1472df38eddc3e1fa6cd5bc3992af0c9eec
workflow-type: tm+mt
source-wordcount: '895'
ht-degree: 10%

---

# Notes de mise à jour de Journey Optimizer B2B edition

Adobe Journey Optimizer B2B edition offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs.

Journey Optimizer B2B edition est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/release-notes/latest){target="_blank"}.

Consultez la [description du produit](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} pour plus d’informations sur les droits, les mécanismes de sécurisation des performances et les limitations.

## Notes de mise à jour d’octobre 2024 {#Oct-2024}

**Date de publication** : 29 octobre 2024

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Nouvelle fonctionnalité | Contenu conditionnel dans les modèles d’e-mail | Personnalisez le contenu de votre e-mail en fonction du comportement et des caractéristiques du profil du destinataire, au niveau du compte et du prospect. <p>Lorsque vous créez un e-mail pour votre parcours de compte dans le Concepteur d’e-mail, utilisez des règles conditionnelles pour définir plusieurs variantes pour tout composant de contenu. <a href="../content/conditional-content.md">En savoir plus</a> |
| Nouvelle fonctionnalité | _Ajouter à la liste_ et _Supprimer de la liste_ les actions de personnes dans les parcours | Personnalisez le contenu de votre e-mail en fonction du comportement et des caractéristiques du profil du destinataire, au niveau du compte et du prospect. <a href="../journeys/action-nodes.md">En savoir plus</a> |
| Nouvelle fonctionnalité | Gouvernance du contenu et verrouillage des composants | Pour garantir la conformité aux conceptions de contenu approuvées, utilisez les fonctionnalités de gouvernance de contenu pour verrouiller les composants de contenu de modèle d’e-mail. Lorsque la gouvernance du contenu est activée dans le modèle d’e-mail, les marketeurs ne peuvent modifier que les éléments autorisés afin de rester alignés avec la stratégie de contenu. <a href="../content/template-content-governance.md">En savoir plus</a> |
| Nouvelle fonctionnalité | Étapes du groupe d’achat | Lorsque vous définissez et publiez un modèle d&#39;évaluation de groupes d&#39;achats personnalisé, vous pouvez suivre la progression des groupes d&#39;achats tout au long des étapes du cycle de vie des groupes d&#39;achats. Utilisez ces étapes pour identifier les meilleures actions suivantes pour les membres du groupe d&#39;achat. Vous configurez les règles de transition et les nœuds de parcours qui déterminent la progression de l’étape et déclenchent des actions en fonction des modifications. <a href="../buying-groups/buying-group-stages.md">En savoir plus</a> |
| Amélioration | Nouveaux modèles d’e-mail prêts à l’emploi | La bibliothèque d’exemples de modèles comprend désormais des modèles d’e-mail supplémentaires conçus pour les spécialistes du marketing B2B. Utilisez ces exemples de modèles comme point de départ et ajoutez vos propres marques et messages. <a href="../content/email-templates.md#select-a-design-template">En savoir plus</a> |
| Amélioration | Champs personnalisés comme attributs de personne | Si des champs de personne personnalisés sont définis dans le schéma d’audience du compte dans Experience Platform, ces champs peuvent également être utilisés en tant qu’attributs de personne dans des conditions. Utilisez ces attributs personnalisés dans : <li>Modèles de rôles <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">En savoir plus</a></li><li>Fractionner les chemins par nœuds de parcours de personnes <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">En savoir plus</a></li> |
| Amélioration | Paramètres du canal e-mail | Les paramètres d’e-mail sont désormais visibles dans l’interface Journey Optimizer B2B edition. Vous pouvez passer rapidement en revue les configurations actuelles et les administrateurs peuvent cliquer sur _[!UICONTROL Modifier les paramètres]_ pour accéder directement aux paramètres dans le Marketo Engage et les mettre à jour en fonction des besoins de votre entreprise. <a href="../admin/configure-channels-emails.md">En savoir plus</a> |

## Notes de mise à jour de septembre 2024 {#Sept-2024}

**Date de publication** : 7 octobre 2024

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Amélioration | Bibliothèque de ressources centrale | La _bibliothèque de ressources centrale_ améliorée, vous permet d’utiliser toutes les ressources d’image dans votre instance de Marketo Engage, sur l’ensemble des espaces de travail de Design Studio. Il existe des mécanismes de sécurisation intégrés qui empêchent la modification des ressources du Marketo Engage à partir de Journey Optimizer B2B edition, ainsi que les opérations de suppression et de déplacement. Ces protections garantissent que les ressources sources (Marketo Engage Design Studio) sont conservées tout en permettant une lecture et une réutilisation transparentes dans Journey Optimizer B2B edition.<p>Pour les ressources destinées exclusivement à Journey Optimizer B2B edition, un espace de travail spécifique fournit des fonctions complètes de gestion des ressources. <a href="../content/marketo-engage-design-studio.md">En savoir plus</a> |
| Nouvelle fonctionnalité | Ressources récemment consultées | La page d’accueil de l’application Journey Optimizer B2B edition comprend désormais la section _[!UICONTROL Récemment consultés]_, qui fournit une liste des ressources consultées le plus récemment par le spécialiste marketing ou l’administrateur. Vous pouvez utiliser cette liste pour accéder directement à la ressource sur laquelle vous avez récemment travaillé sans devoir parcourir une série de pages de ressources ni effectuer de recherche. <p>La liste fournit des informations supplémentaires concernant la modification afin que vous puissiez décider laquelle des ressources doit être modifiée à partir de la dernière session. Pour les ressources d’e-mail, elle affiche le parcours de compte dans lequel la ressource d’e-mail est utilisée. <a href="../home-page.md">En savoir plus</a> |
| Amélioration | Nœud de partage de parcours - réorganiser les chemins | Dans les nœuds de chemin de division, le filtrage des chemins d’accès est évalué dans l’ordre décroissant. Chaque personne ou compte suit le premier chemin correspondant. Vous pouvez réorganiser les chemins définis en cliquant sur les flèches vers le haut et vers le bas en haut à droite de chaque carte de chemin pour la déplacer vers le haut ou le bas de la liste. <a href="../journeys/split-merge-paths-nodes.md#split-paths">En savoir plus</a> |
| Amélioration | Nœud de partage de parcours - Attributs de condition d’historique d’activité supplémentaires | Lorsque vous utilisez des conditions pour définir le filtrage du chemin d’accès pour un nœud partagé par personnes, deux attributs supplémentaires sont disponibles : _E-mail ouvert_ et _E-mail diffusé_. Ces ajouts offrent une plus grande flexibilité pour filtrer les personnes dans le parcours en fonction de l&#39;activité des e-mails. <a href="../journeys/journey-nodes.md#split-paths">En savoir plus</a> |

## Notes de mise à jour d’août 2024 {#Aug-2024}

**Date de publication** : 29 août 2024

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Nouvelle fonctionnalité | Audiences correspondantes du compte linkedIn | Générez des audiences d’annonces LinkedIn par le biais d’audiences avec correspondance de compte pour vous aider à remplir des rôles vides dans vos groupes d’achats. En définissant un ensemble de filtres de groupe d’achats, vous pouvez gérer une Audience appariée LinkedIn pour cibler les prospects qui correspondent aux paramètres de votre groupe d’achats. <p>Cette fonctionnalité exploite les destinations Experience Platform pour gérer certains aspects de l’intégration. <a href="../data/linkedin-account-matched-audiences.md">En savoir plus</a> |
| Amélioration | Cycle de vie du statut des fragments de contenu visuel | Les fragments visuels sont désormais gérés à l’aide d’un cycle de vie de statut. Le statut du fragment détermine sa disponibilité pour une utilisation dans un e-mail ou un modèle d’e-mail, ainsi que les modifications que vous pouvez y apporter. <p>Ce workflow amélioré facilite la gestion du contenu réutilisé en fonction de votre calendrier promotionnel et de communication. <a href="../content/fragments.md#fragment-status-and-lifecycle">En savoir plus</a> |
