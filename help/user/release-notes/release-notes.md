---
title: Notes de mise à jour de Journey Optimizer B2B Edition
description: Découvrez les fonctionnalités, améliorations et correctifs de bugs qui viennent de sortir dans Adobe Journey Optimizer B2B Edition. Informez-vous des nouvelles fonctionnalités et des améliorations apportées aux produits.
role: User, Admin
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: fd8b811eb7f4568a92213e7873dc626f572ae519
workflow-type: tm+mt
source-wordcount: '4434'
ht-degree: 80%

---

# Notes de mise à jour de Journey Optimizer B2B Edition

Adobe Journey Optimizer B2B Edition offre en permanence des nouveautés, des améliorations aux fonctionnalités existantes en passant par les correctifs.

Journey Optimizer B2B Edition est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/release-notes/latest){target="_blank"}.

Consultez la [description du produit](https://helpx.adobe.com/fr/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} pour plus d’informations sur les droits, les mécanismes de sécurisation des performances et les limitations.

## Notes de mise à jour 2026.2

**Date de déploiement** : samedi 20 février 2026

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Fonctionnalité | Champs XDM/schémas relationnels : prise en charge des objets personnalisés de personne | (Beta) Les administrateurs peuvent désormais sélectionner des objets personnalisés liés à une personne à l’aide d’une relation à un seul niveau avec un compte. Cette fonctionnalité permet à votre organisation marketing de représenter une vue plus riche de vos données commerciales réelles pour cibler, personnaliser et générer des rapports sur les entités au-delà du niveau de la personne ou du compte. [En savoir plus](../admin/xdm-field-management.md#relational-schemas) |
| Fonctionnalité | Conception d’e-mails - Prise en charge de Firefly et des modèles Generative AI personnalisés | Vous pouvez désormais activer l’intégration de modèles Firefly standard et personnalisés, ainsi que de modèles d’image tiers approuvés (tels que NanoBanana). Les spécialistes marketing peuvent sélectionner le meilleur modèle pour chaque cas d’utilisation : Firefly standard pour les besoins généraux, Firefly personnalisé pour la génération sur marque ou modèles tiers approuvés pour des scénarios spécialisés ou expérimentaux. |
| Amélioration | Conception d’e-mails - validation de la qualité du contenu | Outre l’alignement de la marque, vous pouvez évaluer la qualité globale du contenu pour identifier les problèmes potentiels de lisibilité, de cohésion et d’efficacité (indépendamment des directives de votre marque). Ces contrôles automatisés permettent d’identifier les messages peu clairs, le ton incohérent ou les lacunes structurelles. |
| Amélioration | rentrée de parcours | Vous pouvez désormais envoyer plusieurs fois des comptes/personnes par le biais d’un workflow de parcours. La rentrée prend en charge plusieurs scénarios, tels que la réévaluation des critères de qualification et les workflows de maturation réutilisables. |
| Amélioration | Activer vers les destinations : audiences réutilisables | Vous pouvez désormais réutiliser des audiences virtuelles dans les actions de parcours _Activer vers la destination_ au sein du même parcours et supprimer des comptes des audiences virtuelles. |
| Amélioration | Parcours de compte et de personne - prise en charge des objets personnalisés de personne | (Beta) Tirez parti des données relationnelles liées aux comptes pour filtrer les personnes au sein d’un parcours de compte ou de personne. [En savoir plus](../journeys/split-merge-paths-nodes.md#custom-data-filtering) |
| Amélioration | (Beta) Personnalisation du contenu : prise en charge des objets personnalisés d’une personne | Lorsque vous définissez la personnalisation du contenu à l’aide des objets personnalisés, vous pouvez accéder à des variables pour les objets personnalisés de classe basés sur un modèle (schémas relationnels). [En savoir plus](../content/personalization.md#custom-datasets) |

>[!NOTE]
>
>Ces modifications de version commencent le déploiement le 20 février 2026, avec un déploiement échelonné de chaque fonctionnalité et amélioration. Les dates de publication des fonctionnalités et des améliorations peuvent changer.

## Notes de mise à jour 2026.1

**Date de déploiement** : mercredi 3 février 2026

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Fonctionnalité | Kits de marque | (Beta) Définissez une marque dans Journey Optimizer B2B edition afin de fournir la source de vérité à votre équipe créative pour qu’elle l’utilise lorsqu’elle crée du contenu visuel ou écrit. Lorsque ces directives sont compilées et que les ressources de la marque sont partagées, n’importe quel membre de l’équipe ou collaborateur peut créer du contenu de marque pour votre produit. |
| Fonctionnalité | Marques pour la génération de contenu d’e-mail | Vous pouvez définir les directives de votre marque et utiliser ces informations pour générer du contenu d’e-mail. Grâce à cette fonctionnalité, le contenu des e-mails est conforme aux directives, aux styles et au ton de rédaction propres à votre marque. |
| Amélioration | Parcours _Nœud d’attente_ - Paramètres avancés | Pour un nœud _Wait_ dans un parcours, vous pouvez désormais spécifier des jours et des heures de sortie, puis sélectionner des fuseaux horaires. Cette amélioration vous permet de mieux contrôler l’orchestration des parcours et le timing des campagnes. |
| Amélioration | Membre du groupe d&#39;achat filtre spécial - Est supprimé contrainte | Le filtre spécial _[!UICONTROL Membre du groupe d&#39;achat]_ inclut désormais la contrainte _Est supprimé_. Lorsque vous ajoutez cette contrainte au filtre, vous pouvez inclure les membres supprimés du groupe d&#39;achats ou les exclure. Elle est également prise en charge dans les listes dynamiques Marketo Engage, où vous pouvez utiliser cette nouvelle contrainte dans le filtre _[!UICONTROL Membre du groupe d’achat]_. |
| Amélioration | Conception d’e-mail - puces à plusieurs niveaux | Les outils de l’espace de conception de contenu d’e-mail prennent désormais en charge les sous-puces (niveaux de puce). |

<!--
| Feature | Custom external actions for journeys | [!BADGE Simplfified architecture]{type=Informative tooltip="Available for simplified architecture"} (Beta) Developers can now use APIs to  build integrations with their first-party systems. | 
| -->

>[!NOTE]
>
>Le déploiement des modifications de la version commence le mercredi 3 février 2026, avec un déploiement échelonné de chaque fonctionnalité. Les dates de publication des fonctionnalités et des améliorations peuvent changer.

## Fonctionnalités d’IA agentique

Les fonctionnalités d’IA agentique suivantes sont désormais disponibles pour Journey Optimizer B2B Edition dans l’interface de l’assistant d’IA :

| Agent | Mise à jour | Description |
| ----- | ------ | ----------- |
| Agent de création de parcours | Nouveau et mis à jour | L’agent de création de parcours analyse, identifie et co-crée des parcours en temps réel, ce qui permet aux responsables marketing de se lancer plus rapidement, d’améliorer l’engagement et de générer des taux de conversion plus élevés. [En savoir plus](../agents/journey-agent.md) |
| Agent Audience | Nouveau | L’agent Audience identifie et crée automatiquement des groupes d’achats à l’aide de données structurées et non structurées. Ainsi, les responsables marketing ciblent les bonnes personnes plus rapidement et plus précisément. [En savoir plus](../agents/audience-agent-b2b.md) |
| Qualificateur de vente | Nouveau | Le qualificateur de vente est une application complémentaire pilotée par l’IA pour Adobe Journey Optimizer B2B edition qui contient le Account Qualification Agent et qui est conçue pour rationaliser les workflows pour les représentants au développement commercial (BDR). Il automatise les workflows de qualification des prospects, de sensibilisation et d’engagement des acheteurs sur tous les canaux [En savoir plus](../agents/sales-qualifier.md) |

## Notes de mise à jour 2025.10

**Date de déploiement** : 31 octobre 2025

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Fonctionnalité | Activer vers la destination pour les parcours | Utilisez l’action de compte d’entreprise _Activer vers la destination_ pour une activation directe vers les entreprises plutôt que vers les individus. (Limité aux sociétés LinkedIn pour cette version.) [En savoir plus](../journeys/action-nodes.md#activate-to-a-linkedin-destination) |
| Fonctionnalité | Thèmes de marque | Grâce aux thèmes, les utilisateurs et les utilisatrices non techniques ont la possibilité de créer du contenu réutilisable adapté à une marque et une langue de conception spécifiques en ajoutant un style personnalisé aux modèles standard. [En savoir plus](../content/brand-themes.md) |
| Fonctionnalité | Modèles d’e-mail - convertir l’image en HTML | Vous pouvez désormais utiliser vos fichiers de conception stockés en tant que fichiers image JPG ou PNG et générer automatiquement des modèles d’e-mail. [En savoir plus](../content/email-template-image-convert.md) |
| Fonctionnalité | Mappage de persona | Liez les membres de compte aux personas établies avec le mappage d’attributs. [En savoir plus](../admin/persona-mapping.md) |
| Fonctionnalité | Informations commerciales pour Salesforce et Dynamics | Les membres de l’équipe des ventes peuvent désormais afficher les groupes d’achats arrivant à maturité et les informations connexes dans une intégration Salesforce ou Dynamics pour identifier de nouvelles opportunités. Les détails du groupe d’achats tels que l’étape, le score et les membres associés sont inclus. [En savoir plus](../buying-groups/incrm-insights.md) |
| Fonctionnalité | Activer l’audience vers [!DNL Adobe Target] | Vous pouvez désormais activer une audience à partir d’un parcours de compte vers une audience client externe et la pousser vers [!DNL Adobe Target]. Grâce à cette intégration, vous pouvez diffuser une audience qualifiée par le biais d’une séquence de parcours pour une expérience web conçue dans [!DNL Target]. [En savoir plus](../audiences/target-external-audience.md) |
| Fonctionnalité | Tableau de bord d’engagement web | Nouveau tableau de bord qui fournit des informations sur la manière dont les visiteurs et visiteuses web interagissent avec le contenu clé. Il segmente les données entre les secteurs de compte et les régions afin de vous aider à comprendre les tendances d’engagement. [En savoir plus](../dashboards/web-engagement-dashboard.md) |
| Fonctionnalité | Tableau de bord Role Insights | Le nouveau tableau de bord _[!UICONTROL Informations sur les rôles]_ fournit des informations sur la manière dont vos campagnes et parcours influencent l’acquisition et l’engagement des rôles des groupes d’achats. [En savoir plus](../buying-groups/buying-group-role-insights.md) |
| Amélioration | Amélioration de la notation d’exhaustivité du groupe d’achat | Vous pouvez désormais vous assurer que les groupes d’achat présentent un réel processus de décision contenant des seuils de membre de rôle personnalisables pour la notation d’exhaustivité.  [En savoir plus](../buying-groups/completeness-scores.md) |
| Amélioration | Traitements de maintenance des groupes d’achat | La fréquence des traitements de maintenance des groupes d’achats passe de Hebdomadaire à Quotidienne. |
| Amélioration | Progression de parcours de compte | Pour un parcours publié dont le statut est défini sur _Actif_, _Fermé aux nouvelles entrées_, _Abandonné_ ou _Terminé_, vous pouvez ouvrir la cartographie du parcours afin de consulter une liste de comptes pour chaque nœud de parcours. |

>[!NOTE]
>
>Le déploiement des modifications de la version commence le 31 octobre 2025, avec un déploiement échelonné de chaque fonctionnalité. Les dates de publication des fonctionnalités et des améliorations peuvent changer.

### Architecture simplifiée

Adobe Journey Optimizer B2B Edition est désormais disponible avec une architecture simplifiée. Grâce à cette architecture mise à jour, Journey Optimizer B2B Edition et Marketo Engage ne sont plus sur le même système et le même magasin de données. Journey Optimizer B2B Edition reçoit des données uniquement d’Adobe Experience Platform. Cependant, il continue de dépendre des droits Marketo Engage et de certaines fonctionnalités de configuration pour approvisionner et configurer le système.

Cette architecture mise à jour offre de nombreux avantages :

* **Unifier et mettre à l’échelle facilement vos données** : la plateforme mise à jour prend en charge des modèles de données complexes, y compris les objets personnalisés, les groupes d’achats et les événements de compte.
* **Connecter plusieurs instances Adobe Marketo Engage** : gérez et unifiez les données de plusieurs environnements Adobe Marketo Engage en un seul endroit.
* **Protéger vos données** : les fonctionnalités avancées de confidentialité et de sécurité vous aident à protéger les informations de votre clientèle.
* **Conçue pour l’avenir** : cette mise à jour prépare votre organisation à des améliorations et innovations continues.

>[!NOTE]
>
>Si votre environnement est configuré sur cette architecture, consultez les [instructions de configuration](../simplified-architecture.md).

Grâce à l’architecture simplifiée, les nouvelles fonctionnalités et améliorations suivantes sont disponibles dans la version 2025.10 :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Fonctionnalité | Modèle de données relationnelles | Tirez parti des données relationnelles liées aux comptes B2B pour filtrer les comptes dans un parcours de compte ou personnaliser le contenu des e-mails. Ces données relationnelles peuvent représenter des entités commerciales réelles telles que des enregistrements d’achat, des enregistrements d’événement, des licences logicielles, des abonnements à des services ou des réservations. [En savoir plus](../admin/xdm-field-management.md#relational-schemas) |
| Fonctionnalité | Plusieurs activations de Marketo Engage | Configurez des connexions à des instances Marketo Engage distantes et utilisez ces connexions pour configurer des actions Marketo Engage pour parcours. Ces actions, telles que l’ajout ou la suppression de personnes dans des listes ou l’ajout de personnes à une campagne de demande, s’appliquent à l’instance Marketo Engage désignée. [En savoir plus](../admin/marketo-actions-connect.md) |
| Fonctionnalité | Déduplication des e-mails (procédure anti-fatigue) | Vous pouvez désormais activer la déduplication des e-mails pour vous assurer que le même e-mail n’est pas envoyé plusieurs fois à la même adresse dans un parcours. Les adresses en double sont bloquées jusqu’à ce que le premier enregistrement avec cette adresse e-mail termine le parcours.  [En savoir plus](../content/email-deduplication.md) |
| Amélioration | Pondération du score d’engagement - Événements AEP | La pondération du score de l’engagement peut désormais inclure n’importe quel événement Experience Platform standard ou personnalisé et être pondérée en fonction de vos besoins. [En savoir plus](../admin/engagement-score-weighting.md) |
| Amélioration | Limites de communication | Le système respecte désormais les limites de communication combinées de Marketo Engage et de Journey Optimizer B2B edition. [En savoir plus](../admin/configure-channels-emails.md#communication-limits) |

<!-- There are additional functional changes with the simplified architecture:

| Item | Description |
| ---- | ----------- |
| Asset management | The system supports an internal asset repository where you can organize folders, edit images, import images, and remove images. It does not support Marketo Engage Design Studio workspaces for asset management. |
| | | -->

<!-- hold for later release 

| Feature | Landing pages | You can now create and publish landing pages in Journey Optimizer B2B Edition to support your journeys and programs. _(Previously a Beta program feature.)_ [Learn more](../content/landing-pages.md) |
| Feature | Forms | You can now create and publish re-usable form components to enable data submission from landing pages that are created and published in Journey Optimizer B2B Edition. _(Previously a Beta program feature.)_ [Learn more](../content/forms.md) |

-->

## Notes de mise à jour 2025.9

**Date de déploiement** : 30 septembre 2025

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Fonctionnalité | Collaboration sur le contenu d’e-mail | Vous pouvez maintenant commenter la collaboration avec d’autres utilisateurs et utilisatrices de Journey Optimizer B2B Edition, dans le cadre d’une ressource d’e-mail. Vous pouvez mentionner les personnes membres de votre équipe afin qu’elles reçoivent une notification par e-mail contenant les détails du commentaire. La notification est également disponible sous la forme d’une notification Pulse. [En savoir plus](../content/email-collaboration-tools.md) |
| Fonctionnalité | Mode sombre pour la conception d’e-mail | L’espace de conception d’e-mail comprend désormais la possibilité de passer en _mode sombre_. En mode sombre, vous pouvez prévisualiser le contenu de l’e-mail et définir les paramètres personnalisés à afficher spécifiquement pour les personnes destinataires qui consultent leurs e-mails en mode sombre. [En savoir plus](../content/email-dark-mode.md) |
| Amélioration | Parcours - Partager le chemin par nombre de personnes dans le rôle | Utilisez un nœud de chemin de partage par compte pour cibler un compte avec le nombre de personnes dans un ou plusieurs rôles de groupe d’achat. Dans le chemin d’accès, vous pouvez évaluer la préparation du groupe d’achat aux alertes de ventes et à d’autres engagements en fonction de la profondeur de rôle. [En savoir plus](../journeys/split-merge-paths-nodes.md#buying-group-filtering-for-accounts) |
| Amélioration | Parcours - Filtres de personnes pour les événements | Utilisez les filtres de personnes pour écouter les événements de personnes. Ces filtres incluent la possibilité de cibler un rôle spécifique pour un groupe d’achat correspondant. [En savoir plus](../journeys/listen-for-event-nodes.md#add-filters-to-the-people-event) |

>[!NOTE]
>
>Le déploiement des modifications de la version commence le 30 septembre 2025, avec un déploiement échelonné de chaque fonctionnalité. Les dates de publication des fonctionnalités et des améliorations peuvent changer.

## Notes de mise à jour 2025.8

**Date de déploiement** : 26 août 2025

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Fonctionnalité | Filtres de score d’engagement de personne pour les modèles de rôles et les parcours | Vous pouvez désormais utiliser le _score d’engagement de personne_ comme filtre dans les modèles de rôles utilisés pour créer des groupes d’achat et dans les nœuds de parcours de chemin de partage. [En savoir plus](../buying-groups/buying-groups-role-templates.md#add-the-template-roles) |
| Fonctionnalité | Configuration des rôles personnalisés des groupes d’achat | Vous avez désormais la possibilité de configurer des rôles personnalisés pour les groupes d’achat, ce qui vous permet de définir les rôles spécifiques à vos cas d’utilisation. [En savoir plus](../buying-groups/default-custom-roles.md) |
| Fonctionnalité | Configuration de la pondération du score d’engagement | Vous pouvez désormais attribuer des pondérations aux activités qui influencent le score d’engagement du groupe d’achat. Cette fonctionnalité inclut la définition de vos propres modèles de score personnalisés et la modification du modèle actif qui influence les calculs de score d’engagement. [En savoir plus](../admin/engagement-score-weighting.md) |
| Amélioration | Contenu conditionnel pour les fragments | Vous pouvez désormais utiliser les outils de contenu conditionnel pour concevoir des fragments visuels. [En savoir plus](../content/conditional-content.md) |
| Amélioration | Mises à jour du score d’engagement | La logique de score d’engagement du groupe d’achat est mise à jour pour normaliser les scores. De plus, vous pouvez utiliser les scores d’engagement au niveau de la personne membre, ainsi que les scores d’engagement collectif pour l’ensemble du groupe d’achat. [En savoir plus](../buying-groups/engagement-scores.md) |
| Amélioration | Observabilité du parcours actif : comptes sur chaque nœud | Pour un parcours de compte actif, vous pouvez accéder à la liste des comptes qui ont atteint chaque nœud de compte dans le parcours. |

## Notes de mise à jour 2025.6

**Date de déploiement** : 15 juillet 2025

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Fonctionnalité | Intégration à GenStudio for Performance Marketing | (Disponibilité limitée) Vous pouvez désormais intégrer des expériences d’e-mail GenStudio for Performance Marketing à Journey Optimizer B2B Edition pour améliorer l’efficacité marketing et maintenir la cohérence de la marque. Grâce à cette intégration, vous pouvez combiner la création de contenu optimisée par l’IA dédiée à GenStudio avec les fonctionnalités avancées d’orchestration de Journey Optimizer B2B Edition. [En savoir plus](../content/genstudio-email-workflow.md) |
| Fonctionnalité | Rapports de détection de spams | Pour éviter les filtres anti-spam et vous assurer que les messages sont envoyés aux boîtes de réception de l’audience, vous pouvez générer un _rapport sur les spams_ directement dans l’espace de conception des e-mails. [En savoir plus](../content/email-spam-report.md) |
| Fonctionnalité | Page de détails de la personne | Vous pouvez désormais cliquer sur le nom d’une personne lorsqu’il est affiché (sous la forme d’un lien hypertexte) dans le tableau de bord intelligent, la page Détails du groupe d’achat et la page Détails du compte. Cette action ouvre la page des détails de la personne associée, avec les informations sur le contact, son activité et les groupes d’achat affichant le plus d’interactions. [En savoir plus](../accounts/person-details.md) |
| Fonctionnalité | Actions du compte et du groupe d’achat | Agissez directement à partir des pages Détails du compte et Détails du groupe d’achat pour un engagement opportun et intentionnel. <li>Utilisez l’action _Envoyer un e-mail_ pour envoyer un e-mail Marketo Engage approuvé aux contacts du compte ou aux membres du groupe d’achat sélectionnés. [En savoir plus](../accounts/account-details.md#send-emails) <li>Dans les détails du groupe d’achat, les actions incluent également _Attribuer un nouveau membre_, _Supprimer un membre_ et _Modifier un rôle_. [En savoir plus](../buying-groups/buying-group-details.md#members-tab) |
| Fonctionnalité | Accéder aux pages de détails dans CRM | Vous pouvez désormais configurer des liens directs vers les pages de détails de Journey Optimizer B2B Edition pour les comptes, contacts et leads dans votre outil de gestion de la relation clientèle (CRM), tel que Salesforce ou Microsoft Dynamics. [En savoir plus](../accounts/crm-linking.md) |
| Fonctionnalité | Prise en charge de CSS personnalisé pour la conception de contenu | Vous pouvez désormais ajouter votre propre CSS personnalisé lorsque vous créez du contenu d’e-mail et de page de destination dans l’espace de conception. [En savoir plus](../content/design-custom-css.md) |
| Fonctionnalité | Configuration du mappage de mots-clés d’intention | Pour activer et gérer le modèle Détection d’intention, vous pouvez désormais charger une feuille de calcul afin de définir une catégorie de mappage des données d’intention. [En savoir plus](../admin/intent-data.md) |
| Amélioration | Simuler le contenu à partir du résumé de l’e-mail | Vous pouvez désormais accéder aux outils _Simuler le contenu_ à partir du résumé de l’e-mail (détails et propriétés) lorsque vous ouvrez un e-mail à partir de la liste E-mails. Cet accès s’ajoute à l’espace de conception des e-mails. [En savoir plus](../content/email-simulate-content.md#display-the-email-preview) |
| Amélioration | Affichage du nombre total pour la liste des modèles de rôle | La page de liste _[!UICONTROL Modèles de rôle]_ est améliorée avec l’affichage du nombre total à côté de la barre de recherche. |

<!-- The following capabilities are currently available only for a set of program participants (Beta):

**Brand Kit with AI Assistant** - Maintain brand consistency across email assets by storing and managing brand assets. Add assets, such as colors, fonts, logos, themes, visual content, and compliance guidelines, and use them for your generative AI content creation. -->

## Notes de mise à jour 2025.5

**Date de déploiement** : 3 juin 2025

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Fonctionnalité | Test des e-mails avec Litmus | Avec un [compte Litmus Enterprise](https://www.litmus.com/email-testing){target="_blank"}, vous pouvez désormais prévisualiser le rendu de vos e-mails dans les principaux clients de messagerie à partir de Journey Optimizer B2B Edition. Cette intégration vous permet de vous assurer que le contenu de votre e-mail s’affiche correctement et fonctionne comme prévu dans chaque boîte de réception d’e-mail. [En savoir plus](../content/email-test-rendering.md) |
| Amélioration | Dupliquer l’e-mail | Vous pouvez désormais dupliquer un e-mail existant pour l’ajouter à un nœud de parcours. Modifiez le paramètre ou le contenu de l’e-mail dupliqué ou laissez-le intact.  [En savoir plus](../content/add-email.md#add-an-email-to-your-journey) |
| Amélioration | Format du jeton Handlebars pour l’e-mail | Les jetons de personnalisation pour le contenu des e-mails utilisent désormais un format mis à jour entièrement compatible avec les scripts Handlebars. Ce format utilise la _Camel Case_ ou des traits de soulignement qui éliminent les espaces. [En savoir plus](../content/email-authoring.md#content-authoring---personalization) |
| Amélioration | Affichage du nombre total de listes | Les pages de liste _[!UICONTROL Intérêts de la solution]_ et _[!UICONTROL Parcours de compte]_ sont améliorées avec l’affichage du nombre total à côté de la barre de recherche. |

## Notes de mise à jour 2025.4

**Date de déploiement** : 29 avril 2025

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Fonctionnalité | Listes de comptes | Vous pouvez désormais créer une liste de comptes statiques ou dynamiques pour cibler les comptes nommés en fonction de vos critères définis, tels que le secteur d’activité, l’emplacement ou la taille de l’entreprise. <a href="../accounts/account-lists.md">En savoir plus</a> |
| Fonctionnalité | Orchestration du parcours de liste de comptes | Utilisez les nœuds d’action de parcours pour ajouter et supprimer des comptes pour les listes de comptes statiques. <a href="../accounts/account-lists-journeys.md#take-an-action-node---add-to-account">En savoir plus</a> |
| Amélioration | Filtrer l’abonnement à un parcours dans Marketo Engage | Utilisez les listes de comptes Adobe Journey Optimizer B2B Edition pour l’audience de parcours, puis utilisez le filtre _Membre d’une liste de comptes_ dans les listes intelligentes Marketo Engage. <a href="../accounts/account-lists-journeys.md#marketo-engage-program---member-of-account-list">En savoir plus</a> |
| Fonctionnalité | Filtres d’inactivité | Orchestrez des parcours en fonction de l’inactivité dans les campagnes et programmes Marketo Engage, y compris l’inactivité des e-mails, les moments intéressants, les modifications de valeur des données et les pages web visitées. <a href="../journeys/split-merge-paths-nodes.md#activity-filtering">En savoir plus</a> |
| Amélioration | Filtre des pages web visitées | Orchestrez des parcours en fonction de l’activité des pages web visitées associées aux campagnes et programmes Marketo Engage. <a href="../journeys/split-merge-paths-nodes.md#people-path-filters">En savoir plus</a> |
| Amélioration | Liste des e-mails | Consultez une liste globale des e-mails actifs et des brouillons d’e-mail pour les rechercher, les examiner et les mettre à jour dans les parcours de compte associés. <a href="../content/emails-list.md">En savoir plus</a> |

## Notes de mise à jour 2025.3

**Date de publication** : 1er avril 2025

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Fonctionnalité | Dupliquer des parcours de compte | Une action de duplication est désormais disponible pour les parcours de compte. Vous pouvez dupliquer les détails du parcours de compte ou simplement un squelette de la structure des flux et des chemins d’accès. <a href="../journeys/journeys-overview.md#duplicate-journey">En savoir plus</a> |
| Fonctionnalité | Mes jetons pour les parcours de compte | Vous pouvez maintenant définir un ensemble de jetons personnalisés avec des valeurs spécifiques au parcours de compte. Cet ensemble de jetons personnalisés est appelé _Mes jetons_ et l’un de ces jetons personnalisés est destiné à la personnalisation lors de la création d’e-mails de parcours. <a href="../content/personalization-my-tokens.md">En savoir plus</a> |
| Fonctionnalité | Supprimer les étapes du groupe d’achat | Vous pouvez supprimer le modèle d’étapes du groupe d’achat lorsqu’il est à l’état brouillon ou publié. S’il est publié (actif), vous pouvez le supprimer uniquement s’il n’est pas associé à un intérêt de solution. <a href="../buying-groups/buying-group-stages.md#delete-the-buying-group-stages-model">En savoir plus</a> |
| Amélioration | Nombre de nœuds de parcours | Amélioration de la visibilité sur le nombre d’abonnements au parcours publié au niveau du nœud. Dans le _mappage de parcours_, les nœuds affichent _[!UICONTROL Total des comptes saisis]_. Lorsque vous sélectionnez le nœud d’action, les détails sur la droite incluent également les _[!UICONTROL Comptes n’ayant pas encore fait l’objet d’une action]_. Les détails des nœuds _Écouter un événement_ incluent les _[!UICONTROL Comptes à cette étape]_. Utilisez ces informations pour valider la progression du compte dans vos parcours actifs, terminés et abandonnés. |

## Notes de mise à jour 2025.2

**Date de déploiement** : 11 mars 2025

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Fonctionnalité | Champs personnalisables - Fragments de contenu | Durant la conception du fragment visuel, vous pouvez désigner un paramètre pour un composant du fragment comme étant modifiable. Cette fonctionnalité permet à la personne créant l’e-mail ou le modèle de spécifier une valeur de champ personnalisé spécifique à ses besoins. Cette option de personnalisation est limitée aux composants visuels d’image, de texte et de bouton. <a href="../content/fragment-authoring.md#enable-fragment-customization">En savoir plus</a> |
| Fonctionnalité | Types de duplication de parcours | Lorsque vous dupliquez un parcours de compte, vous pouvez inclure les détails du nœud, à l’exclusion des e-mails et des SMS créés dans Journey Optimizer B2B Edition. Vous pouvez également créer une copie squelette de la structure et des flux de chemin d’accès, sans détails ni paramètres de nœud. <a href="../journeys/journeys-overview.md#duplicate-journey">En savoir plus</a> |
| Amélioration | Quatre exemples supplémentaires de modèles d’e-mail | La bibliothèque d’exemples de modèles d’e-mail comprend désormais quatre modèles SecurFinancial qui servent d’exemples de contenu de réengagement, d’information, de stimulation et de commentaires. |

<!-- | Feature | B2B built-in roles and product permissions | Experience Platform now includes a set of built-in (default) roles that you can use to manage access to the B2B product capabilities. <a href="../admin/user-management.md#b2b-built-in-roles">Learn more</a> <br/>Administrators can now define custom roles in Adobe Experience Platform to include Journey Optimizer B2B Edition product permissions.  <a href="../admin/user-management.md#b2b-product-permissions">Learn more</a> | -->

## Notes de mise à jour 2025.1 {#Jan-2025}

**Date de déploiement** : 6 février 2025

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Fonctionnalité | Transfert des événements d’expérience | Les administrateurs et administratrices peuvent configurer des définitions d’événement basées sur Adobe Experience Platform (AEP). Ces configurations permettent aux spécialistes du marketing de créer des parcours de compte qui réagissent aux événements d’expérience AEP.  <a href="../admin/configure-aep-events.md">En savoir plus</a> |
| Fonctionnalité | Destinations de médias achetés | Qualifiez des personnes connues pour des campagnes de médias achetés à partir d’un parcours de compte afin de pouvoir les impliquer davantage sur les plateformes publicitaires telles que LinkedIn. Utilisez un nœud de partage de chemin pour segmenter les audiences de comptes en fonction d’un comportement spécifique et identifier les comptes qui nécessitent un engagement supplémentaire. Ajoutez ensuite les personnes de ces comptes à une audience cliente externe via Real-Time CDP vers une destination de médias achetés prise en charge. <a href="../journeys/action-nodes.md#journey-optimizer-b2b-actions">En savoir plus</a> |
| Fonctionnalité | Tableau de bord intelligent | Affichez la progression des groupes d’achat à travers leurs parcours de compte, y compris les informations générées par l’IA pour une analyse plus intelligente et une hiérarchisation précise des comptes. <a href="../dashboards/intelligent-dashboard.md">En savoir plus</a> |
| Fonctionnalité | Détails du groupe d’achat et du compte | Affichez des informations au niveau du groupe d’achat et du compte pour disposer de plus de données contextuelles et historiques lorsque vous commencez à interagir avec un client ou une cliente.<p>Les détails du groupe d’achat incluent toute intention propriétaire détectée. <a href="../buying-groups/buying-group-details.md">En savoir plus</a><p>Les détails des comptes mettent en évidence l’augmentation subite de l’intention détectée au niveau de l’engagement. Vous pouvez ainsi alerter les ventes sur les comptes prêts pour un engagement personnalisé axé sur les ventes.  <a href="../accounts/account-details.md">En savoir plus</a> |
| Fonctionnalité | Vue d’ensemble des parcours | Lorsque vous accédez aux parcours de compte, l’onglet Vue d’ensemble fournit un instantané complet de vos parcours de compte actifs, détaillant la progression des comptes à l’aide de diagrammes circulaires et de graphiques en barres qui catégorisent et quantifient les achèvements, ainsi que les activités d’engagement.  <a href="../dashboards/journeys-dashboard.md">En savoir plus</a> |
| Fonctionnalité | Modification d’images Adobe Express | Les actions rapides d’Adobe Express vous permettent d’apporter des modifications simples (recadrage et redimensionnement, par exemple) aux images pour améliorer l’aspect de votre contenu. <a href="../content/image-edit-adobe-express.md#quick-actions-in-adobe-express">En savoir plus</a>  <p>Pour obtenir un ensemble plus complet d’outils de conception, cette intégration permet d’obtenir une licence Adobe Express complète dans Journey Optimizer B2B Edition. Grâce à cette configuration, l’interface d’utilisation complète d’Adobe Express devient accessible dans l’espace de travail des ressources locales. <a href="../content/image-edit-adobe-express.md#adobe-express-enterprise-license">En savoir plus</a> |
| Fonctionnalité | Filtres d’intention pour les rôles de groupe d’achat | Lorsque vous envoyez vos mots-clés d’intention, le modèle de détection d’intention prédit une solution/un produit d’intérêt avec un degré de confiance suffisamment élevé en fonction de l’activité d’un lead. <a href="../admin/intent-data.md">En savoir plus</a> <p>Ces données d’intention sont disponibles pour définir les conditions de rôle du groupe d’achat <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">En savoir plus</a> |
| Amélioration | Prise en charge des événements Marketo Engage dans les parcours | Le nœud de parcours _Écouter un événement_ prend désormais en charge deux événements Marketo Engage au niveau des personnes : _Visite la page web_ et _Remplit le formulaire_. <a href="../journeys/listen-for-event-nodes.md#listen-for-marketo-engage-event">En savoir plus</a> |
| Amélioration | Filtres de groupe d’achat pour les listes intelligentes Marketo Engage | Affichez et créez des listes intelligentes avec des filtres de groupe d’achat dans Marketo Engage. Ces filtres ajoutés vous permettent de supprimer et d’inclure des membres de groupes d’achat dans les campagnes et programmes Marketo Engage à partir des parcours de compte dans Journey Optimizer B2B Edition. <a href="../buying-groups/marketo-engage-smart-list-buying-group-filters.md">En savoir plus</a> |
| Amélioration | Filtre d’abonnement à la liste Marketo Engage pour les parcours et les rôles | Dans Journey Optimizer B2B, vérifiez l’abonnement à la liste Marketo Engage comme condition d’un nœud _fractionner le chemin par personne_ afin d’éliminer les doublons dans les activités de parcours. <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">En savoir plus</a> <p> Pour les modèles de rôles de groupe d’achat, utilisez l’abonnement à une liste comme condition de rôle. <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">En savoir plus</a> |
| Amélioration | Tableau de bord de vue d’ensemble de l’engagement | Ce tableau de bord est mis à jour afin de fournir une vue complète de l’engagement. Il présente des mesures en temps réel des interactions des comptes et des individus par le biais de graphiques circulaires instantanés et de graphiques linéaires révélateurs de tendances au fil du temps. <a href="../dashboards/engagement-dashboard.md">En savoir plus</a> |

## Versions de 2024

Développez les listes suivantes pour connaître les fonctionnalités et améliorations de Journey Optimizer B2B Edition publiées en 2024.

+++Notes de mise à jour d’octobre 2024

**Date de déploiement** : 29 octobre 2024

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Fonctionnalité | Contenu conditionnel dans les e-mails | Personnalisez le contenu de votre e-mail en fonction du comportement et des caractéristiques du profil du destinataire au niveau du compte et du prospect. <p>Lorsque vous créez un e-mail pour votre parcours de compte dans l’espace de conception visuelle d’e-mail, utilisez des règles conditionnelles pour définir plusieurs variantes pour tout composant de contenu. <a href="../content/conditional-content.md">En savoir plus</a> |
| Fonctionnalité | Actions de personne _Ajouter à la liste_ et _Supprimer de la liste_ dans les parcours | Personnalisez le contenu de votre e-mail en fonction du comportement et des caractéristiques du profil du destinataire au niveau du compte et du prospect. <a href="../journeys/action-nodes.md">En savoir plus</a> |
| Fonctionnalité | Gouvernance du contenu et verrouillage des composants | Pour garantir la conformité avec les conceptions de contenu approuvées, utilisez les fonctionnalités de gouvernance de contenu pour verrouiller les composants de contenu de modèle d’e-mail. Lorsque la gouvernance du contenu est activée dans le modèle d’e-mail, les spécialistes du marketing ne peuvent modifier que les éléments autorisés afin de rester en phrase avec la stratégie de contenu. <a href="../content/template-content-governance.md">En savoir plus</a> |
| Fonctionnalité | Étapes des groupes d’achat | Lorsque vous définissez et publiez un modèle personnalisé des étapes des groupes d’achat, vous pouvez suivre la progression des groupes d’achat tout au long des étapes du cycle de vie des groupes d’achat. Utilisez ces étapes pour identifier les meilleures actions à entreprendre pour les membres du groupe d’achat. Vous configurez les règles de transition et les nœuds de parcours qui déterminent la progression des étapes et déclenchent des actions en fonction des modifications. <a href="../buying-groups/buying-group-stages.md">En savoir plus</a> |
| Amélioration | Nouveaux modèles d’e-mail prêts à l’emploi | La bibliothèque d’exemples de modèles comprend désormais des modèles d’e-mail supplémentaires conçus pour les spécialistes du marketing B2B. Utilisez ces exemples de modèles comme point de départ et ajoutez votre propres branding et vos propres messages. <a href="../content/email-templates.md#select-a-design-template">En savoir plus</a> |
| Amélioration | Champs personnalisés comme attributs de personne | Si des champs de personne personnalisés sont définis dans le schéma d’audience de comptes dans Experience Platform, ces champs peuvent également être utilisés en tant qu’attributs de personne dans les conditions. Utilisez ces attributs personnalisés dans : <li>Modèles de rôles <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">En savoir plus</a></li><li>Fractionner les chemins par nœuds de parcours de personnes <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">En savoir plus</a></li> |
| Amélioration | Paramètres de canal E-mail | Les paramètres d’e-mail sont désormais visibles dans l’interface Journey Optimizer B2B Edition. Vous pouvez passer rapidement en revue les configurations actuelles et les administrateurs et administratrices peuvent cliquer sur _[!UICONTROL Modifier les paramètres]_ pour accéder directement aux paramètres dans Marketo Engage et les mettre à jour en fonction des besoins de votre organisation. <a href="../admin/configure-channels-emails.md">En savoir plus</a> |

+++

+++Notes de mise à jour de septembre 2024

**Date de déploiement** : 7 octobre 2024

Cette version comprend les nouvelles fonctionnalités et améliorations suivantes :

| Type | Élément | Description |
| ---- | ---- | ----------- |
| Amélioration | Bibliothèque de ressources centrale | La _bibliothèque de ressources centrale_ améliorée, vous permet d’utiliser toutes les ressources d’image de votre instance Marketo Engage dans les espaces de travail Design Studio. Il existe des mécanismes de sécurisation intégrés qui empêchent les modifications apportées aux ressources Marketo Engage à partir de Journey Optimizer B2B Edition, ainsi que les opérations de suppression et de déplacement. Ces protections garantissent que les ressources sources (Marketo Engage Design Studio) sont conservées tout en facilitant la lecture et la réutilisation dans Journey Optimizer B2B Edition.<p>Pour les ressources destinées exclusivement à Journey Optimizer B2B Edition, un espace de travail spécifique fournit des fonctions complètes de gestion des ressources. <a href="../content/internal-image-assets.md">En savoir plus</a> |
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
