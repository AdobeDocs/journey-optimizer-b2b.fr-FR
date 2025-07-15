---
title: Notes de mise à jour de Journey Optimizer B2B Edition
description: Découvrez les dernières fonctionnalités et améliorations d’Adobe Journey Optimizer B2B Edition.
role: User, Admin
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: 7e9396a7ac029c173fe3d9b0b1bab6b7c4521ee0
workflow-type: tm+mt
source-wordcount: '2165'
ht-degree: 96%

---

# Notes de mise à jour de Journey Optimizer B2B Edition

Adobe Journey Optimizer B2B Edition offre en permanence des nouveautés, des améliorations aux fonctionnalités existantes en passant par les correctifs.

Journey Optimizer B2B Edition est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/release-notes/latest){target="_blank"}.

Consultez la [description du produit](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} pour plus d’informations sur les droits, les mécanismes de sécurisation des performances et les limitations.

## Notes de mise à jour 2025.5

**Date de déploiement** : 3 juin 2025

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Fonctionnalité | Test des e-mails avec Litmus | Avec un [compte Litmus](https://www.litmus.com/email-testing){target="_blank"}, vous pouvez désormais prévisualiser votre rendu d’e-mail dans les clients de messagerie populaires à partir de Journey Optimizer B2B edition. Cette intégration vous permet de vous assurer que le contenu de votre e-mail s’affiche correctement et fonctionne comme prévu dans chaque boîte de réception d’e-mail. [En savoir plus](../content/email-test-rendering.md) |
| Amélioration | Dupliquer l’e-mail | Lors de l’ajout d’un e-mail pour un nœud de parcours, vous pouvez désormais dupliquer un e-mail existant. Modifiez le paramètre ou le contenu de l’e-mail dupliqué ou laissez-le intact.  [En savoir plus](../content/add-email.md#add-an-email-to-your-journey) |
| Amélioration | Format du jeton Handlebars pour l’e-mail | Les jetons de personnalisation pour le contenu des e-mails utilisent désormais un format mis à jour entièrement compatible avec les scripts Handlebars. Ce format utilise la _Camel Case_ ou des traits de soulignement qui éliminent les espaces. [En savoir plus](../content/email-authoring.md#content-authoring---personalization) |
| Amélioration | Affichage du nombre total de listes | Les pages de liste _[!UICONTROL Intérêts de la solution]_ et _[!UICONTROL Parcours de compte]_ sont améliorées avec l’affichage du nombre total à côté de la barre de recherche. |

## Notes de mise à jour 2025.4

**Date de déploiement** : 29 avril 2025

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Fonctionnalité | Listes de comptes | Vous pouvez désormais créer une liste de comptes statiques ou dynamiques pour cibler les comptes nommés en fonction de vos critères définis, tels que le secteur d’activité, l’emplacement ou la taille de l’entreprise. <a href="../accounts/account-lists.md">En savoir plus</a> |
| Fonctionnalité | Orchestration du parcours de liste de comptes | Utilisez les nœuds d’action de parcours pour ajouter et supprimer des comptes pour les listes de comptes statiques. <a href="../accounts/account-lists-journeys.md#take-an-action-node---add-to-account">En savoir plus</a> |
| Amélioration | Filtrer l’adhésion à un parcours dans Marketo Engage | Utilisez les listes de comptes Adobe Journey Optimizer B2B Edition pour l’audience de parcours, puis utilisez le filtre _Membre d’une liste de comptes_ dans les listes intelligentes Marketo Engage. <a href="../accounts/account-lists-journeys.md#marketo-engage-program---member-of-account-list">En savoir plus</a> |
| Fonctionnalité | Filtres d’inactivité | Orchestrez des parcours en fonction de l’inactivité dans les campagnes et programmes Marketo Engage, y compris l’inactivité des e-mails, les moments intéressants, les modifications de valeur des données et les pages web visitées. <a href="../journeys/split-merge-paths-nodes.md#activity-filtering">En savoir plus</a> |
| Amélioration | Filtre des pages web visitées | Orchestrez des parcours en fonction de l’activité des pages web visitées associées aux campagnes et programmes Marketo Engage. <a href="../journeys/split-merge-paths-nodes.md#people-path-conditions">En savoir plus</a> |
| Amélioration | Liste des e-mails | Consultez une liste globale des e-mails actifs et des brouillons d’e-mail pour les rechercher, les examiner et les mettre à jour dans les parcours de compte associés. <a href="../content/emails-list.md">En savoir plus</a> |

## Notes de mise à jour 2025.3

**Date de publication** : 1er avril 2025

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Fonctionnalité | Dupliquer des parcours de compte | Une action de duplication est désormais disponible pour les parcours de compte. Vous pouvez dupliquer les détails du parcours de compte ou simplement un squelette de la structure des flux et des chemins d’accès. <a href="../journeys/journey-overview.md#duplicate-journey">En savoir plus</a> |
| Fonctionnalité | Mes jetons pour les parcours de compte | Vous pouvez maintenant définir un ensemble de jetons personnalisés avec des valeurs spécifiques au parcours de compte. Cet ensemble de jetons personnalisés est appelé _Mes jetons_ et l’un de ces jetons personnalisés est destiné à la personnalisation lors de la création d’e-mails de parcours. <a href="../content/personalization-my-tokens.md">En savoir plus</a> |
| Fonctionnalité | Supprimer les étapes du groupe d’achat | Vous pouvez supprimer le modèle d’étapes du groupe d’achat lorsqu’il est à l’état brouillon ou publié. S’il est publié (actif), vous pouvez le supprimer uniquement s’il n’est pas associé à un intérêt de solution. <a href="../buying-groups/buying-group-stages.md#delete-the-buying-group-stages-model">En savoir plus</a> |
| Amélioration | Nombre de nœuds de parcours | Amélioration de la visibilité sur le nombre d’adhésions au parcours publié au niveau du nœud. Dans le _mappage de parcours_, les nœuds affichent _[!UICONTROL Total des comptes saisis]_. Lorsque vous sélectionnez le nœud d’action, les détails sur la droite incluent également les _[!UICONTROL Comptes n’ayant pas encore fait l’objet d’une action]_. Les détails des nœuds _Écouter un événement_ incluent les _[!UICONTROL Comptes à cette étape]_. Utilisez ces informations pour valider la progression du compte dans vos parcours actifs, terminés et abandonnés. |

## Notes de mise à jour 2025.2

**Date de déploiement** : 11 mars 2025

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Fonctionnalité | Champs personnalisables - Fragments de contenu | Durant la conception du fragment visuel, vous pouvez désigner un paramètre pour un composant du fragment comme étant modifiable. Cette fonctionnalité permet à la personne créant l’e-mail ou le modèle de spécifier une valeur de champ personnalisé spécifique à ses besoins. Cette option de personnalisation est limitée aux composants visuels d’image, de texte et de bouton. <a href="../content/fragment-authoring.md#enable-fragment-customization">En savoir plus</a> |
| Fonctionnalité | Types de duplication de parcours | Lorsque vous dupliquez un parcours de compte, vous pouvez inclure les détails du nœud, à l’exclusion des e-mails et des SMS créés dans Journey Optimizer B2B Edition. Vous pouvez également créer une copie squelette de la structure et des flux de chemin d’accès, sans détails ni paramètres de nœud. <a href="../journeys/journey-overview.md#duplicate-journey">En savoir plus</a> |
| Amélioration | Quatre exemples supplémentaires de modèles d’e-mail | La bibliothèque d’exemples de modèles d’e-mail comprend désormais quatre modèles SecurFinancial qui servent d’exemples de contenu de réengagement, d’information, de stimulation et de commentaires. |

<!-- | Feature | B2B built-in roles and product permissions | Experience Platform now includes a set of built-in (default) roles that you can use to manage access to the B2B product capabilities. <a href="../admin/user-management.md#b2b-built-in-roles">Learn more</a> <br/>Administrators can now define custom roles in Adobe Experience Platform to include Journey Optimizer B2B Edition product permissions.  <a href="../admin/user-management.md#b2b-product-permissions">Learn more</a> | -->

## Notes de mise à jour 2025.1 {#Jan-2025}

**Date de déploiement** : 6 février 2025

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Fonctionnalité | Transfert des événements d’expérience | Les administrateurs et administratrices peuvent configurer des définitions d’événement basées sur Adobe Experience Platform (AEP). Ces configurations permettent aux spécialistes du marketing de créer des parcours de compte qui réagissent aux événements d’expérience AEP.  <a href="../admin/configure-aep-events.md">En savoir plus</a> |
| Fonctionnalité | Destinations de médias achetés | Qualifiez des personnes connues pour des campagnes de médias achetés à partir d’un parcours de compte afin de pouvoir les impliquer davantage sur les plateformes publicitaires telles que LinkedIn. Utilisez un nœud de fractionnement de chemin dans un parcours de compte pour segmenter les audiences de compte en fonction d’un comportement spécifique et identifier les comptes qui nécessitent un engagement supplémentaire. Ajoutez ensuite les personnes de ces comptes à une audience cliente externe via Real-Time CDP vers une destination de médias achetés prise en charge. <a href="../journeys/action-nodes.md#journey-optimizer-b2b-actions">En savoir plus</a> |
| Fonctionnalité | Tableau de bord intelligent | Affichez la progression des groupes d’achat à travers leurs parcours de compte, y compris les informations générées par l’IA pour une analyse plus intelligente et une hiérarchisation précise des comptes. <a href="../dashboards/intelligent-dashboard.md">En savoir plus</a> |
| Fonctionnalité | Détails du groupe d’achat et du compte | Affichez des informations au niveau du groupe d’achat et du compte pour disposer de plus de données contextuelles et historiques lorsque vous commencez à interagir avec un client ou une cliente.<p>Les détails du groupe d’achat incluent toute intention propriétaire détectée. <a href="../buying-groups/buying-group-details.md">En savoir plus</a><p>Les détails des comptes mettent en évidence l’augmentation subite de l’intention détectée au niveau de l’engagement. Vous pouvez ainsi alerter les ventes sur les comptes prêts pour un engagement personnalisé axé sur les ventes.  <a href="../accounts/account-details.md">En savoir plus</a> |
| Fonctionnalité | Vue d’ensemble des parcours | Lorsque vous accédez aux parcours de compte, l’onglet Vue d’ensemble fournit un instantané complet de vos parcours de compte actifs, détaillant la progression des comptes à l’aide de diagrammes circulaires et à barres qui catégorisent et quantifient les achèvements, ainsi que les activités d’engagement.  <a href="../dashboards/journeys-dashboard.md">En savoir plus</a> |
| Fonctionnalité | Modification d’images Adobe Express | Les actions rapides d’Adobe Express vous permettent d’apporter des modifications simples (recadrage et redimensionnement, par exemple) aux images pour améliorer l’aspect de votre contenu. <a href="../content/image-edit-adobe-express.md#quick-actions-in-adobe-express">En savoir plus</a>  <p>Pour obtenir un ensemble plus complet d’outils de conception, cette intégration permet d’obtenir une licence Adobe Express complète dans Journey Optimizer B2B Edition. Grâce à cette configuration, l’interface d’utilisation complète d’Adobe Express devient accessible dans l’espace de travail des ressources locales. <a href="../content/image-edit-adobe-express.md#adobe-express-enterprise-license">En savoir plus</a> |
| Fonctionnalité | Filtres d’intention pour les rôles de groupe d’achat | Lorsque vous envoyez vos mots-clés d’intention, le modèle de détection d’intention prédit une solution/un produit d’intérêt avec un degré de confiance suffisamment élevé en fonction de l’activité d’un lead. <a href="../admin/intent-data.md">En savoir plus</a> <p>Ces données d’intention sont disponibles pour définir les conditions de rôle du groupe d’achat <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">En savoir plus</a> |
| Amélioration | Prise en charge des événements Marketo Engage dans les parcours | Le nœud de parcours _Écouter un événement_ prend désormais en charge deux événements Marketo Engage au niveau des personnes : _Visite la page web_ et _Remplit le formulaire_. <a href="../journeys/listen-for-event-nodes.md#listen-for-marketo-engage-event">En savoir plus</a> |
| Amélioration | Filtres de groupe d’achat pour les listes intelligentes Marketo Engage | Affichez et créez des listes intelligentes avec des filtres de groupe d’achat dans Marketo Engage. Ces filtres ajoutés vous permettent de supprimer et d’inclure des membres de groupes d’achat dans les campagnes et programmes Marketo Engage à partir des parcours de compte dans Journey Optimizer B2B Edition. <a href="../buying-groups/marketo-engage-smart-list-buying-group-filters.md">En savoir plus</a> |
| Amélioration | Filtre d’appartenance à la liste Marketo Engage pour les parcours et les rôles | Dans Journey Optimizer B2B, vérifiez l’appartenance à la liste Marketo Engage comme condition d’un nœud _fractionner le chemin par personne_ afin d’éliminer les duplications dans les activités de parcours. <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">En savoir plus</a> <p> Pour les modèles de rôles de groupe d’achat, utilisez l’appartenance à une liste comme condition de rôle. <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">En savoir plus</a> |
| Amélioration | Tableau de bord de vue d’ensemble de l’engagement | Ce tableau de bord est mis à jour afin de fournir une vue complète de l’engagement. Il présente des mesures en temps réel des interactions des comptes et des individus par le biais de graphiques circulaires instantanés et de graphiques linéaires révélateurs de tendances au fil du temps. <a href="../dashboards/engagement-dashboard.md">En savoir plus</a> |

## Versions de 2024

Développez les listes suivantes pour connaître les fonctionnalités et améliorations de Journey Optimizer B2B Edition publiées en 2024.

+++Notes de mise à jour d’octobre 2024

**Date de déploiement** : 29 octobre 2024

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Fonctionnalité | Contenu conditionnel dans les modèles d’e-mail | Personnalisez le contenu de votre e-mail en fonction des caractéristiques comportementales et du profil des destinataires, au niveau du compte et du lead. <p>Lorsque vous créez un e-mail pour votre parcours de compte dans l’espace de conception visuelle d’e-mail, utilisez des règles conditionnelles pour définir plusieurs variantes pour tout composant de contenu. <a href="../content/conditional-content.md">En savoir plus</a> |
| Fonctionnalité | Actions de personne _Ajouter à la liste_ et _Supprimer de la liste_ dans les parcours | Personnalisez le contenu de votre e-mail en fonction des caractéristiques comportementales et du profil des destinataires, au niveau du compte et du lead. <a href="../journeys/action-nodes.md">En savoir plus</a> |
| Fonctionnalité | Gouvernance du contenu et verrouillage des composants | Pour garantir la conformité avec les conceptions de contenu approuvées, utilisez les fonctionnalités de gouvernance de contenu pour verrouiller les composants de contenu de modèle d’e-mail. Lorsque la gouvernance du contenu est activée dans le modèle d’e-mail, les spécialistes du marketing ne peuvent modifier que les éléments autorisés afin de rester en phrase avec la stratégie de contenu. <a href="../content/template-content-governance.md">En savoir plus</a> |
| Fonctionnalité | Étapes des groupes d’achat | Lorsque vous définissez et publiez un modèle personnalisé des étapes des groupes d’achat, vous pouvez suivre la progression des groupes d’achat tout au long des étapes du cycle de vie des groupes d’achat. Utilisez ces étapes pour identifier les meilleures actions à entreprendre pour les membres du groupe d’achat. Vous configurez les règles de transition et les nœuds de parcours qui déterminent la progression des étapes et déclenchent des actions en fonction des modifications. <a href="../buying-groups/buying-group-stages.md">En savoir plus</a> |
| Amélioration | Nouveaux modèles d’e-mail prêts à l’emploi | La bibliothèque d’exemples de modèles comprend désormais des modèles d’e-mail supplémentaires conçus pour les spécialistes du marketing B2B. Utilisez ces exemples de modèles comme point de départ et ajoutez votre propres branding et vos propres messages. <a href="../content/email-templates.md#select-a-design-template">En savoir plus</a> |
| Amélioration | Champs personnalisés comme attributs de personne | Si des champs de personne personnalisés sont définis dans le schéma d’audience du compte dans Experience Platform, ces champs peuvent également être utilisés en tant qu’attributs de personne dans les conditions. Utilisez ces attributs personnalisés dans : <li>Modèles de rôles <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">En savoir plus</a></li><li>Fractionner les chemins par nœuds de parcours de personnes <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">En savoir plus</a></li> |
| Amélioration | Paramètres de canal E-mail | Les paramètres d’e-mail sont désormais visibles dans l’interface Journey Optimizer B2B Edition. Vous pouvez passer rapidement en revue les configurations actuelles et les administrateurs et administratrices peuvent cliquer sur _[!UICONTROL Modifier les paramètres]_ pour accéder directement aux paramètres dans Marketo Engage et les mettre à jour en fonction des besoins de votre organisation. <a href="../admin/configure-channels-emails.md">En savoir plus</a> |

+++

+++Notes de mise à jour de septembre 2024

**Date de déploiement** : 7 octobre 2024

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Amélioration | Bibliothèque de ressources centrale | La _bibliothèque de ressources centrale_ améliorée, vous permet d’utiliser toutes les ressources d’image de votre instance Marketo Engage dans les espaces de travail Design Studio. Il existe des mécanismes de sécurisation intégrés qui empêchent les modifications apportées aux ressources Marketo Engage à partir de Journey Optimizer B2B Edition, ainsi que les opérations de suppression et de déplacement. Ces protections garantissent que les ressources sources (Marketo Engage Design Studio) sont conservées tout en facilitant la lecture et la réutilisation dans Journey Optimizer B2B Edition.<p>Pour les ressources destinées exclusivement à Journey Optimizer B2B Edition, un espace de travail spécifique fournit des fonctions complètes de gestion des ressources. <a href="../content/marketo-engage-design-studio.md">En savoir plus</a> |
| Fonctionnalité | Ressources récemment consultées | La page d’accueil de l’application Journey Optimizer B2B Edition comprend désormais la section _[!UICONTROL Récemment consultées]_, qui fournit une liste des dernières ressources consultées par les spécialistes du marketing ou l’équipe d’aministration. Vous pouvez utiliser cette liste pour accéder directement à la ressource sur laquelle vous avez récemment travaillé sans devoir parcourir une série de pages de ressources ni effectuer de recherche. <p>La liste fournit des informations supplémentaires concernant la modification afin que vous puissiez décider laquelle des ressources doit être modifiée par rapport à la dernière session. Pour les ressources d’e-mail, elle affiche le parcours de compte dans lequel la ressource d’e-mail est utilisée. <a href="../home-page.md">En savoir plus</a> |
| Amélioration | Nœud de fractionnement de parcours – Réorganiser les chemins | Dans les nœuds de fractionnement de chemin, le filtrage des chemins d’accès est évalué dans l’ordre décroissant. Chaque personne ou compte suit le premier chemin correspondant. Vous pouvez réorganiser les chemins définis en cliquant sur les flèches vers le haut et vers le bas en haut à droite de chaque carte de chemin pour la déplacer vers le haut ou le bas de la liste. <a href="../journeys/split-merge-paths-nodes.md#split-paths">En savoir plus</a> |
| Amélioration | Nœud de fractionnement de parcours – Attributs de condition supplémentaires de l’historique de l’activité | Lorsque vous utilisez des conditions pour définir le filtrage du chemin pour un nœud de fractionnement par personne, deux attributs supplémentaires sont disponibles : _E-mail ouvert_ et _E-mail diffusé_. Ces ajouts offrent une plus grande flexibilité pour filtrer les personnes dans le parcours en fonction de l’activité des e-mails. <a href="../journeys/journey-nodes.md#split-paths">En savoir plus</a> |

+++

+++Notes de mise à jour d’août 2024

**Date de déploiement** : 29 août 2024

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Fonctionnalité | Audiences correspondantes de compte LinkedIn | Générez des audiences d’annonces LinkedIn par le biais d’audiences correspondantes des comptes pour vous aider à remplir des rôles vides dans vos groupes d’achat. En définissant un ensemble de filtres de groupe d’achat, vous pouvez gérer une audience correspondante LinkedIn pour cibler les leads qui correspondent aux paramètres de votre groupe d’achat. <p>Cette fonctionnalité exploite les destinations Experience Platform pour gérer certains aspects de l’intégration. <a href="../data/linkedin-account-matched-audiences.md">En savoir plus</a> |
| Amélioration | Cycle de vie par statut des fragments de contenu visuel | Les fragments visuels sont désormais gérés à l’aide d’un cycle de vie par statut. Le statut du fragment détermine sa disponibilité pour une utilisation dans un e-mail ou un modèle d’e-mail, ainsi que les modifications que vous pouvez y apporter. <p>Ce workflow amélioré facilite la gestion du contenu réutilisé en fonction de du calendrier de vos promotions et communications. <a href="../content/fragments.md#fragment-status-and-lifecycle">En savoir plus</a> |

+++
