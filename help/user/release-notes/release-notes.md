---
title: Notes de mise à jour
description: Dernières notes de mise à jour pour l’édition B2B d’Adobe Journey Optimizer
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: 18a9f073f5c898d01c075611c6808d192d71dbc7
workflow-type: tm+mt
source-wordcount: '895'
ht-degree: 10%

---

# Notes de mise à jour de Journey Optimizer B2B edition

Adobe Journey Optimizer B2B edition offre en permanence de nouvelles fonctionnalités, des améliorations des fonctionnalités existantes et des correctifs.

Journey Optimizer B2B edition est basé en mode natif sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/release-notes/latest){target="_blank"}.

Passez en revue la [description du produit](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} pour plus d’informations sur les droits, les barrières de performance et les limitations.

## Notes de mise à jour d’octobre 2024 {#Oct-2024}

**Date de publication** : 29 octobre 2024

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Nouvelle fonctionnalité | Contenu conditionnel dans les modèles de courrier électronique | Personnalisez le contenu de vos emails en fonction du comportement des destinataires et des caractéristiques de profil, tant au niveau du compte qu’au niveau du prospect. <p>Lorsque vous créez un email pour votre parcours de compte dans le concepteur d’email, utilisez des règles conditionnelles pour définir plusieurs variantes pour n’importe quel composant de contenu. <a href="../content/conditional-content.md">En savoir plus</a> |
| Nouvelle fonctionnalité | _Ajouter à la liste_ et _Supprimer de la liste_ actions de personnes dans les parcours | Personnalisez le contenu de vos emails en fonction du comportement des destinataires et des caractéristiques de profil, tant au niveau du compte qu’au niveau du prospect. <a href="../journeys/journey-nodes.md#action-nodes">En savoir plus</a> |
| Nouvelle fonctionnalité | Gouvernance du contenu et verrouillage des composants | Pour garantir le respect des conceptions de contenu approuvées, utilisez les fonctionnalités de gouvernance de contenu pour verrouiller les composants de contenu de modèle d’email. La gouvernance du contenu étant activée dans le modèle d’email, les marketeurs ne peuvent modifier que les éléments autorisés pour rester en phase avec la stratégie de contenu. <a href="../content/template-content-governance.md">En savoir plus</a> |
| Nouvelle fonctionnalité | Étapes du groupe d’achat | Lorsque vous définissez et publiez un modèle d’évaluation de groupes d’achats personnalisé, vous pouvez suivre la progression d’un groupe d’achats tout au long des étapes du cycle de vie du groupe d’achats. Utilisez ces étapes pour identifier les meilleures actions à entreprendre pour acheter des membres de groupe. Configurez les règles de transition et les noeuds de parcours qui déterminent la progression de l’étape et déclenchent des actions en fonction des modifications. <a href="../buying-groups/buying-group-stages.md">En savoir plus</a> |
| Amélioration | Nouveaux modèles d’email d’usine | La bibliothèque d’exemples de modèles comprend désormais des modèles de courrier électronique supplémentaires conçus pour les spécialistes du marketing B2B. Utilisez ces exemples de modèles comme point de départ et ajoutez vos propres marques et messages. <a href="../content/email-templates.md#select-a-design-template">En savoir plus</a> |
| Amélioration | Champs personnalisés en tant qu’attributs de personne | Si des champs de personne personnalisés sont définis dans le schéma d’audience du compte en Experience Platform, ces champs peuvent également être utilisés comme attributs de personne dans des conditions. Utilisez ces attributs personnalisés dans : <li>Modèles de rôles <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">En savoir plus</a></li><li>Fractionner les chemins d’accès par personnes noeuds de parcours <a href="../journeys/journey-nodes.md#add-a-split-path-by-people-node">En savoir plus</a></li> |
| Amélioration | Paramètres du canal email | Les paramètres de courrier électronique sont désormais visibles dans l’interface B2B edition de Journey Optimizer. Vous pouvez passer rapidement en revue les configurations actuelles et les administrateurs peuvent cliquer sur _[!UICONTROL Modifier les paramètres]_ pour accéder directement aux paramètres de Marketo Engage et les mettre à jour en fonction des exigences de votre entreprise. <a href="../admin/configure-channels-emails.md">En savoir plus</a> |

## Notes de mise à jour de septembre 2024 {#Sept-2024}

**Date de publication** : 7 octobre 2024

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Amélioration | Bibliothèque de ressources Central | La _bibliothèque centrale de ressources_ améliorée vous permet d’utiliser toutes les ressources d’image dans votre instance de Marketo Engage, dans les espaces de travail de Design Studio. Il existe des barrières de sécurité intégrées qui empêchent les modifications des ressources du Marketo Engage à partir de Journey Optimizer B2B edition, ainsi que les opérations de suppression et de déplacement. Ces protections garantissent que les ressources source (Marketo Engage Design Studio) sont conservées tout en permettant une lecture et une réutilisation transparentes dans Journey Optimizer B2B edition.<p>Pour les ressources exclusivement destinées à Journey Optimizer B2B edition, un espace de travail spécifique fournit des fonctions de gestion des ressources complètes. <a href="../content/marketo-engage-design-studio.md">En savoir plus</a> |
| Nouvelle fonctionnalité | Ressources récemment consultées | La page d’accueil de l’application Journey Optimizer B2B edition comprend désormais la section _[!UICONTROL Récemment accédé]_, qui fournit une liste des ressources les plus récemment consultées pour le marketeur ou l’administrateur. Vous pouvez utiliser cette liste pour accéder directement à la ressource sur laquelle vous avez récemment travaillé sans parcourir une série de pages de ressources ni effectuer de recherche. <p>La liste fournit des informations supplémentaires sur la modification afin que vous puissiez décider quelles ressources doivent être modifiées à partir de la dernière session. Pour les ressources de courrier électronique, il affiche le parcours de compte dans lequel la ressource de courrier électronique est utilisée. <a href="../home-page.md">En savoir plus</a> |
| Amélioration | Noeud de partage de parcours - Réorganiser les chemins | Dans les noeuds de chemin de division, le filtrage de chemin est évalué dans l’ordre descendant. Chaque personne ou compte emprunte le premier chemin correspondant. Vous pouvez réorganiser les chemins définis en cliquant sur les flèches haut et bas en haut à droite de chaque carte de chemin pour les déplacer vers le haut ou le bas de la liste. <a href="../journeys/journey-nodes.md#split-paths">En savoir plus</a> |
| Amélioration | Noeud de partage de parcours - Attributs de condition de l’historique d’activité supplémentaires | Lors de l’utilisation de conditions pour définir le filtrage du chemin d’accès pour un noeud partagé par des personnes, il existe deux attributs supplémentaires : _Email ouvert_ et _Email distribué_. Ces ajouts offrent une plus grande flexibilité pour filtrer les personnes dans le parcours en fonction de l’activité de courrier électronique. <a href="../journeys/journey-nodes.md#split-paths">En savoir plus</a> |

## Notes de mise à jour d’août 2024 {#Aug-2024}

**Date de publication** : 29 août 2024

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Nouvelle fonctionnalité | Audiences mises en correspondance de comptes linkedIn | Générez des audiences LinkedIn Ad par le biais des audiences mises en correspondance de compte pour vous aider à remplir les rôles vides dans vos groupes d’achats. En définissant un ensemble de filtres de groupe d’achats, vous pouvez gérer une audience mise en correspondance LinkedIn pour cibler les prospects qui correspondent aux paramètres de votre groupe d’achats. <p>Cette fonctionnalité exploite les destinations Experience Platform pour gérer certains aspects de l’intégration. <a href="../data/linkedin-account-matched-audiences.md">En savoir plus</a> |
| Amélioration | Cycle de vie d’état des fragments de contenu visuel | Les fragments visuels sont désormais gérés à l’aide d’un cycle de vie d’état. L’état du fragment détermine sa disponibilité à utiliser dans un email ou un modèle de courrier électronique, ainsi que les modifications que vous pouvez y apporter. <p>Grâce à ce workflow amélioré, il est facile de gérer le contenu réutilisé en fonction de votre calendrier de promotion et de communication. <a href="../content/fragments.md#fragment-status-and-lifecycle">En savoir plus</a> |
