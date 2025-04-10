---
title: Notes de mise à jour
description: Dernières notes de mise à jour pour l’édition B2B d’Adobe Journey Optimizer
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: 775cecb2aa4e305ba9a80ba0655e5e854ddf69e2
workflow-type: tm+mt
source-wordcount: '1863'
ht-degree: 9%

---

# Notes de mise à jour de Journey Optimizer B2B edition

Adobe Journey Optimizer B2B edition offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs.

Journey Optimizer B2B edition est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/release-notes/latest){target="_blank"}.

Consultez la [description du produit](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} pour plus d’informations sur les droits, les mécanismes de sécurisation des performances et les limitations.

## notes de mise à jour 2025.3

**Date de publication** : mercredi 1 avril 2025

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Nouvelle fonctionnalité | Listes de comptes | Vous pouvez désormais créer une liste de comptes statique ou dynamique pour cibler les comptes nommés en fonction de vos critères définis, tels que le secteur d’activité, l’emplacement ou la taille de l’entreprise. <a href="../accounts/account-lists.md">En savoir plus</a> |
| Nouvelle fonctionnalité | Mes jetons pour les parcours de compte | Vous pouvez maintenant définir un ensemble de jetons personnalisés avec des valeurs spécifiques au parcours de compte. Cet ensemble de jetons personnalisés est appelé _Mes jetons_ et l’un de ces jetons personnalisés est destiné à la personnalisation lors de la création d’e-mails de parcours. <a href="../content/personalization-my-tokens.md">En savoir plus</a> |
| Nouvelle fonctionnalité | Supprimer les étapes du groupe d&#39;achat | Vous pouvez supprimer le modèle d&#39;étapes de groupe d&#39;achats lorsqu&#39;il est à l&#39;état de brouillon ou publié. S’il est publié (actif), vous pouvez le supprimer uniquement s’il n’est pas associé à un intérêt de solution. <a href="../buying-groups/buying-group-stages.md#delete-the-buying-group-stages-model">En savoir plus</a> |
| Amélioration | Nombre de nœuds de parcours | Amélioration de la visibilité sur le nombre d’adhésions au parcours publié au niveau du nœud. Dans le mappage de Parcours __, les nœuds affichent _[!UICONTROL Total des comptes saisis]_. Lorsque vous sélectionnez le nœud d’action, les détails sur la droite incluent également _[!UICONTROL Comptes n’ayant pas encore fait l’objet d’une action]_. Les détails des nœuds _Écouter un événement_ incluent les _[!UICONTROL Comptes à cette étape]_. Utilisez ces informations pour valider la progression du compte dans vos parcours actifs, terminés et abandonnés. |

## notes de mise à jour 2025.2

**Date de publication** : 11 mars 2025

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Nouvelle fonctionnalité | Champs personnalisables - fragments de contenu | En tant que concepteur de fragment de contenu, vous pouvez désigner un paramètre pour un composant du fragment comme étant modifiable. Cela permet à l’auteur de l’e-mail ou du modèle de spécifier une valeur de champ personnalisée spécifique à ses besoins. Cet indicateur de personnalisation est limité aux composants visuels d’image, de texte et de bouton. <a href="../content/fragment-authoring.md#enable-fragment-customization">En savoir plus</a> |
| Nouvelle fonctionnalité | Rôles intégrés B2B et autorisations de produit | Experience Platform comprend désormais un ensemble de rôles intégrés (par défaut) que vous pouvez utiliser pour gérer l’accès aux fonctionnalités du produit B2B. <a href="../admin/user-management.md#b2b-built-in-roles">En savoir plus</a> <br/>Les administrateurs peuvent désormais définir des rôles personnalisés dans Adobe Experience Platform pour inclure les autorisations de produit Journey Optimizer B2B edition.  <a href="../admin/user-management.md#b2b-product-permissions">En savoir plus</a> |
| Nouvelle fonctionnalité | Types de duplication de parcours | Lorsque vous dupliquez un parcours de compte, vous pouvez inclure les détails du nœud, à l’exclusion des e-mails et des SMS créés dans Journey Optimizer B2B edition. Vous pouvez également créer une copie squelette de la structure et des flux de chemin d’accès, sans détails ni paramètres de nœud. <a href="../journeys/journey-overview.md#duplicate-journey">En savoir plus</a> |
| Amélioration | Quatre exemples supplémentaires de modèles d’e-mail | La bibliothèque d’exemples de modèles d’e-mail comprend désormais quatre modèles SecurFinancial qui servent d’exemples de contenu pour le réengagement, l’information, le soutien et les commentaires |

## notes de mise à jour 2025.1 {#Jan-2025}

**Date de publication** : 6 février 2025

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Nouvelle fonctionnalité | Transfert d’événement d’expérience | Les administrateurs peuvent configurer des définitions d’événement basées sur Adobe Experience Platform (AEP). Ces configurations permettent aux spécialistes marketing de créer des parcours de compte qui réagissent aux événements d’expérience AEP.  <a href="../admin/configure-aep-events.md">En savoir plus</a> |
| Nouvelle fonctionnalité | Destinations de médias payants | Qualifiez des personnes connues pour des campagnes média payantes à partir d’un parcours de compte afin de pouvoir les impliquer davantage sur les plateformes publicitaires telles que LinkedIn. Utilisez un nœud de chemins de partage dans un parcours de compte pour segmenter les audiences de compte en fonction d’un comportement spécifique et identifier les comptes qui nécessitent un engagement supplémentaire. Ajoutez ensuite les utilisateurs de ces comptes à une audience client externe via Real-Time CDP vers une destination de médias achetés prise en charge. <a href="../journeys/action-nodes.md#journey-optimizer-b2b-actions">En savoir plus</a> |
| Nouvelle fonctionnalité | Tableau de bord intelligent | Affichez la progression des groupes d’achats à travers leurs parcours de compte, y compris les informations générées par l’IA pour une analyse plus intelligente et une hiérarchisation précise des comptes. <a href="../dashboards/intelligent-dashboard.md">En savoir plus</a> |
| Nouvelle fonctionnalité | Détails du groupe d&#39;achat et du compte | Affichez des informations au niveau du groupe d’achat et du compte pour disposer de plus de données contextuelles et historiques lorsque vous commencez à interagir avec un client.<p>Les détails du groupe d&#39;achats incluent toute intention propriétaire détectée. <a href="../buying-groups/buying-group-details.md">En savoir plus</a><p>Les comptes des détails du compte mettent en évidence l’augmentation subite de l’intention détectée au niveau de l’engagement. Vous pouvez ainsi alerter les ventes des comptes prêts pour un engagement personnalisé axé sur les ventes.  <a href="../accounts/account-details.md">En savoir plus</a> |
| Nouvelle fonctionnalité | Présentation de Parcours | Lorsque vous accédez aux parcours de compte, l’onglet Aperçu fournit un instantané complet de vos parcours de compte actifs, détaillant la progression du compte à l’aide de graphiques à barres et en cercles qui catégorisent et quantifient les éléments terminés, ainsi que les activités d’engagement.  <a href="../dashboards/journeys-dashboard.md">En savoir plus</a> |
| Nouvelle fonctionnalité | Modification d’images Adobe Express | Les actions rapides d’Adobe Express vous permettent d’apporter des modifications simples (recadrage et redimensionnement, par exemple) aux images pour améliorer l’aspect de votre contenu. <a href="../content/image-edit-adobe-express.md#quick-actions-in-adobe-express">En savoir plus</a>  <p>Pour obtenir un ensemble plus complet d’outils de conception, cette intégration permet d’obtenir une licence Adobe Express complète dans Journey Optimizer B2B edition. Grâce à cette configuration, l’interface utilisateur complète d’Adobe Express devient accessible dans l’espace de travail des ressources locales. <a href="../content/image-edit-adobe-express.md#adobe-express-enterprise-license">En savoir plus</a> |
| Nouvelle fonctionnalité | Filtres d’intention pour les rôles de groupe d’achat | Lorsque vous envoyez vos mots-clés d’intention, le modèle de détection d’intention prédit une solution/un produit d’intérêt avec un degré de confiance suffisamment élevé en fonction de l’activité d’un prospect. <a href="../admin/intent-data.md">En savoir plus</a> <p>Ces données d&#39;intention sont disponibles pour définir les conditions de rôle du groupe d&#39;achat <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">En savoir plus</a> |
| Amélioration | Prise en charge des événements Marketo Engage dans parcours | Le nœud de parcours _Écouter pour l’événement_ prend désormais en charge deux événements Marketo Engage au niveau des personnes : _Page web des visites_ et _Formulaire rempli_. <a href="../journeys/listen-for-event-nodes.md#listen-for-marketo-engage-event">En savoir plus</a> |
| Amélioration | Filtres de groupe d’achat pour les listes dynamiques Marketo Engage | Affichez et créez des listes dynamiques avec des filtres de groupe d’achat dans Marketo Engage. Ces filtres ajoutés vous permettent de supprimer et d’inclure des membres de groupes d’achat dans les campagnes et programmes Marketo Engage à partir des parcours de compte dans Journey Optimizer B2B edition. <a href="../buying-groups/marketo-engage-smart-list-buying-group-filters.md">En savoir plus</a> |
| Amélioration | Filtre d’appartenance à la liste Marketo Engage pour les parcours et les rôles | Dans Journey Optimizer B2B, vérifiez l’appartenance à la liste Marketo Engage comme condition d’un nœud _chemin de partage par personnes_ afin d’éliminer la duplication dans les activités de parcours. <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">En savoir plus</a> <p> Pour les modèles de rôles de groupe d’achat, utilisez l’appartenance à une liste comme condition de rôle. <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">En savoir plus</a> |
| Amélioration | Tableau de bord de présentation de l’engagement | Ce tableau de bord est mis à jour afin de fournir une vue complète de l’engagement. Il présente des mesures en temps réel des interactions de comptes et individuelles par le biais de graphiques en cercle à clichés et de graphiques en courbes révélateurs de tendances au fil du temps. <a href="../dashboards/engagement-dashboard.md">En savoir plus</a> |


## Notes de mise à jour d’octobre 2024 {#Oct-2024}

**Date de publication** : 29 octobre 2024

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Nouvelle fonctionnalité | Contenu conditionnel dans les modèles d’e-mail | Personnalisez le contenu de votre e-mail en fonction du comportement et des caractéristiques du profil du destinataire, au niveau du compte et du prospect. <p>Lorsque vous créez un e-mail pour votre parcours de compte dans l’espace de conception visuelle d’e-mail, utilisez des règles conditionnelles pour définir plusieurs variantes pour tout composant de contenu. <a href="../content/conditional-content.md">En savoir plus</a> |
| Nouvelle fonctionnalité | _Ajouter à la liste_ et _Supprimer de la liste_ les actions de personnes dans les parcours | Personnalisez le contenu de votre e-mail en fonction du comportement et des caractéristiques du profil du destinataire, au niveau du compte et du prospect. <a href="../journeys/action-nodes.md">En savoir plus</a> |
| Nouvelle fonctionnalité | Gouvernance du contenu et verrouillage des composants | Pour garantir la conformité aux conceptions de contenu approuvées, utilisez les fonctionnalités de gouvernance de contenu pour verrouiller les composants de contenu de modèle d’e-mail. Lorsque la gouvernance du contenu est activée dans le modèle d’e-mail, les marketeurs ne peuvent modifier que les éléments autorisés afin de rester alignés avec la stratégie de contenu. <a href="../content/template-content-governance.md">En savoir plus</a> |
| Nouvelle fonctionnalité | Étapes du groupe d’achat | Lorsque vous définissez et publiez un modèle d&#39;évaluation de groupes d&#39;achats personnalisé, vous pouvez suivre la progression des groupes d&#39;achats tout au long des étapes du cycle de vie des groupes d&#39;achats. Utilisez ces étapes pour identifier les meilleures actions suivantes pour les membres du groupe d&#39;achat. Vous configurez les règles de transition et les nœuds de parcours qui déterminent la progression de l’étape et déclenchent des actions en fonction des modifications. <a href="../buying-groups/buying-group-stages.md">En savoir plus</a> |
| Amélioration | Nouveaux modèles d’e-mail prêts à l’emploi | La bibliothèque d’exemples de modèles comprend désormais des modèles d’e-mail supplémentaires conçus pour les spécialistes du marketing B2B. Utilisez ces exemples de modèles comme point de départ et ajoutez vos propres marques et messages. <a href="../content/email-templates.md#select-a-design-template">En savoir plus</a> |
| Amélioration | Champs personnalisés comme attributs de personne | Si des champs de personne personnalisés sont définis dans le schéma d’audience du compte dans Experience Platform, ces champs peuvent également être utilisés en tant qu’attributs de personne dans des conditions. Utilisez ces attributs personnalisés dans : <li>Modèles de rôles <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">En savoir plus</a></li><li>Fractionner les chemins par nœuds de parcours de personnes <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">En savoir plus</a></li> |
| Amélioration | Paramètres du canal e-mail | Les paramètres d’e-mail sont désormais visibles dans l’interface Journey Optimizer B2B edition. Vous pouvez passer rapidement en revue les configurations actuelles et les administrateurs peuvent cliquer sur _[!UICONTROL Modifier les paramètres]_ pour accéder directement aux paramètres de Marketo Engage et les mettre à jour en fonction des besoins de votre organisation. <a href="../admin/configure-channels-emails.md">En savoir plus</a> |

## Notes de mise à jour de septembre 2024 {#Sept-2024}

**Date de publication** : 7 octobre 2024

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Amélioration | Bibliothèque de ressources centrale | La _bibliothèque de ressources centrale_ améliorée, vous permet d’utiliser toutes les ressources d’image de votre instance Marketo Engage dans les espaces de travail de Design Studio. Il existe des mécanismes de sécurisation intégrés qui empêchent la modification des ressources Marketo Engage à partir de Journey Optimizer B2B edition, ainsi que les opérations de suppression et de déplacement. Ces protections garantissent que les ressources sources (Marketo Engage Design Studio) sont conservées tout en permettant une lecture et une réutilisation transparentes dans Journey Optimizer B2B edition.<p>Pour les ressources destinées exclusivement à Journey Optimizer B2B edition, un espace de travail spécifique fournit des fonctions complètes de gestion des ressources. <a href="../content/marketo-engage-design-studio.md">En savoir plus</a> |
| Nouvelle fonctionnalité | Ressources récemment consultées | La page d’accueil de l’application Journey Optimizer B2B edition comprend désormais la section _[!UICONTROL Récemment consultés]_, qui fournit une liste des ressources consultées le plus récemment par le spécialiste marketing ou l’administrateur. Vous pouvez utiliser cette liste pour accéder directement à la ressource sur laquelle vous avez récemment travaillé sans devoir parcourir une série de pages de ressources ni effectuer de recherche. <p>La liste fournit des informations supplémentaires concernant la modification afin que vous puissiez décider laquelle des ressources doit être modifiée à partir de la dernière session. Pour les ressources d’e-mail, elle affiche le parcours de compte dans lequel la ressource d’e-mail est utilisée. <a href="../home-page.md">En savoir plus</a> |
| Amélioration | Nœud de partage de parcours - réorganiser les chemins | Dans les nœuds de chemin de division, le filtrage des chemins d’accès est évalué dans l’ordre décroissant. Chaque personne ou compte suit le premier chemin correspondant. Vous pouvez réorganiser les chemins définis en cliquant sur les flèches vers le haut et vers le bas en haut à droite de chaque carte de chemin pour la déplacer vers le haut ou le bas de la liste. <a href="../journeys/split-merge-paths-nodes.md#split-paths">En savoir plus</a> |
| Amélioration | Nœud de partage de parcours - Attributs de condition d’historique d’activité supplémentaires | Lorsque vous utilisez des conditions pour définir le filtrage du chemin d’accès pour un nœud partagé par personnes, deux attributs supplémentaires sont disponibles : _E-mail ouvert_ et _E-mail diffusé_. Ces ajouts offrent une plus grande flexibilité pour filtrer les personnes dans le parcours en fonction de l&#39;activité des e-mails. <a href="../journeys/journey-nodes.md#split-paths">En savoir plus</a> |

## Notes de mise à jour d’août 2024 {#Aug-2024}

**Date de publication** : 29 août 2024

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Nouvelle fonctionnalité | Audiences correspondantes du compte LinkedIn | Générez des audiences d&#39;annonces LinkedIn par le biais d&#39;audiences avec correspondance de compte pour vous aider à remplir des rôles vides dans vos groupes d&#39;achats. En définissant un ensemble de filtres de groupe d&#39;achat, vous pouvez gérer une Audience appariée LinkedIn pour cibler les prospects qui correspondent aux paramètres de votre groupe d&#39;achat. <p>Cette fonctionnalité exploite Experience Platform Destinations pour gérer certains aspects de l’intégration. <a href="../data/linkedin-account-matched-audiences.md">En savoir plus</a> |
| Amélioration | Cycle de vie du statut des fragments de contenu visuel | Les fragments visuels sont désormais gérés à l’aide d’un cycle de vie de statut. Le statut du fragment détermine sa disponibilité pour une utilisation dans un e-mail ou un modèle d’e-mail, ainsi que les modifications que vous pouvez y apporter. <p>Ce workflow amélioré facilite la gestion du contenu réutilisé en fonction de votre calendrier promotionnel et de communication. <a href="../content/fragments.md#fragment-status-and-lifecycle">En savoir plus</a> |
