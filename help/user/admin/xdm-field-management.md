---
title: Gestion des champs XDM
description: Utilisez la gestion des champs XDM pour contrôler les données disponibles dans Journey Optimizer B2B edition.
feature: Data Management, Integrations
role: User
badgeBeta: label="Beta" type="informative" tooltip="Cette fonctionnalité fait actuellement partie d’une version bêta limitée de l’architecture simplifiée"
exl-id: 4f0f2c79-3831-47ab-b5ed-d5534be000d5
source-git-commit: 863265860a59abac4a73971bf923fa4cc1456e8d
workflow-type: tm+mt
source-wordcount: '1158'
ht-degree: 1%

---

# Gestion des champs XDM

Les champs de modèle de données d’expérience (XDM) sont des éléments de schéma qui fournissent des données à l’application [!DNL Journey Optimizer B2B Edition]. Utilisez les champs XDM comme filtres et contraintes dans les nœuds de parcours, les groupes d’achat et pour les fonctionnalités de contenu, telles que la personnalisation des e-mails et le contenu conditionnel.

Les schémas définissent des champs en fonction des classes XDM standard. Les classes XDM standard incluent le profil individuel, le compte professionnel et les événements d’expérience. Les schémas relationnels définissent également des champs qui vous permettent de modéliser des données structurées de la même manière que les bases de données relationnelles traditionnelles.

Les schémas de Adobe Experience Platform (AEP) contiennent généralement de nombreux champs dans des hiérarchies complexes. La traversée des arborescences de schéma XDM prend du temps. La gestion des champs XDM rationalise la sélection des champs en affichant uniquement les champs pertinents à chaque parcours. Les administrateurs contrôlent les champs qui s’affichent pour les créateurs et créatrices de parcours. Les administrateurs définissent également les champs en lecture seule ou modifiables. Ces actions améliorent l’efficacité lors de la conception du parcours.

Les administrateurs qui comprennent XDM et collaborent avec les ingénieurs de données ou les parties prenantes de la modélisation des données de la plateforme de données client (CDP) B2B doivent suivre les étapes suivantes pour configurer les classes XDM pour [!DNL Journey Optimizer B2B Edition].

>[!NOTE]
>
>La gestion des champs XDM est disponible pour les environnements Journey Optimizer B2B edition configurés sur l’[architecture simplifiée](../simplified-architecture.md).

## Accès aux classes XDM

1. Dans le volet de navigation de gauche, choisissez **[!UICONTROL Administration]** > **[!UICONTROL Configuration]**.

1. Cliquez sur **[!UICONTROL Classes XDM]** dans le panneau intermédiaire.

   * Utilisez les onglets **[!UICONTROL Standard]** et **[!UICONTROL Relationnel]** pour ajouter de nouveaux champs et les rendre disponibles dans Journey Optimizer B2B edition.

   * Utilisez l’onglet **Événements** pour [sélectionner des événements d’expérience AEP spécifiques et leurs champs associés](./configure-aep-events.md) à utiliser pour les nœuds d’événement de parcours.

## Sélections de champs

>[!IMPORTANT]
>
>Vous pouvez mettre à jour votre sélection de champs à tout moment en sélectionnant de nouveaux champs ou en désélectionnant les champs dont vous n’avez plus besoin. Lorsque vous publiez un parcours à l’aide de ce schéma, vous verrouillez la structure du schéma. La suppression ou le changement de nom du schéma, l’ajout de nouveaux champs ou la modification de types de champs n’est pas pris en charge et peut entraîner des échecs de parcours.

Appliquez les instructions suivantes pour effectuer des sélections de champs :

* Vous ne pouvez ajouter de nouveaux champs qu’après l’utilisation active d’un schéma dans un parcours.
* La suppression, le changement de nom ou la modification de types de champ peut entraîner des problèmes de fonctionnalité de parcours. Soyez prudent lors de la manipulation des schémas.
* Ne renommez pas et ne supprimez pas les schémas, et ne modifiez pas les clés des schémas relationnels.

### Classes standard

Dans l’onglet _[!UICONTROL Standard]_, vous pouvez modifier _Champs gérés_ et _Champs modifiables_ pour les classes standard :

* Les champs gérés apparaissent dans les parcours, les groupes d’achats et les fonctionnalités de personnalisation.
* Les champs pouvant être mis à jour servent de contraintes pour les nœuds de parcours _Mettre à jour le profil de compte_ et _Mettre à jour le profil de personne_.

![Onglet Classes standard affichant la configuration de la classe XDM](assets/xdm-standard.png){width="600" zoomable="yes"}

La liste comprend deux classes :

* **[!UICONTROL XDM Individual Profile]**
* **[!UICONTROL Compte professionnel XDM]**

Les informations de classe affichées incluent :

* Nombre de champs gérés
* Nombre de champs modifiables
* Heure de la dernière mise à jour

Pour sélectionner des champs dans le schéma d’union pour les classes XDM standard, cliquez sur le nom de la classe pour ouvrir la boîte de dialogue de sélection _Champs gérés_ ou cliquez sur l’icône _Plus_ ( **...** ) pour choisir entre _[!UICONTROL Champs gérés]_ et _[!UICONTROL Champs pouvant être mis à jour]_.

![Cliquez sur l’icône du menu Plus pour choisir entre les champs gérés et les champs modifiables](./assets/xdm-classes-standard-more-menu.png){width="550" zoomable="yes"}

>[!NOTE]
>
>Un champ doit d’abord être _Géré_ avant de pouvoir être _Mis à jour_. Les _champs pouvant être mis à jour_ que vous sélectionnez doivent exister dans votre schéma fourni par l’utilisateur. Votre schéma peut ne pas inclure les champs obligatoires, à l’exception des champs définis par le système.

#### Champs gérés

Lorsque vous choisissez **[!UICONTROL Champs gérés]**, la boîte de dialogue _Sélectionner les champs_ répertorie tous les champs configurables.

1. Sélectionnez jusqu’à 100 champs pour chaque classe XDM.

   Utilisez le champ _[!UICONTROL Rechercher]_ pour filtrer la liste affichée par nom. Utilisez le curseur **[!UICONTROL Afficher uniquement les champs sélectionnés]** pour passer en revue les sélections actuelles.

   ![Boîte de dialogue de sélection des champs gérés pour les classes XDM standard affichant les options de champs configurables](assets/xdm-standard-managed-fields.png){width="450" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Enregistrer]** pour confirmer vos sélections.

#### Champs modifiables

Avant de configurer des champs pouvant être mis à jour, ils doivent résider dans un jeu de données personnalisé. Pour une présentation du workflow du jeu de données personnalisé, voir [Création de jeux de données et ingestion de données](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data#){target="_blank"} et utiliser l’option **[!UICONTROL Création d’un jeu de données à partir d’un schéma]**. Ce jeu de données est utilisé pour isoler les champs modifiables. Tous les champs pouvant être mis à jour doivent se trouver dans ce jeu de données.

>[!IMPORTANT]
>
>Mécanismes de sécurisation pour les champs modifiables :
>
>* Schémas - Dans la classe XDM Individual Profile, tous les champs obligatoires du schéma doivent être définis par le système, par exemple `identityMap` ou `personID`.
>* Jeux de données - N’utilisez pas un jeu de données déjà utilisé à d’autres fins. Il est recommandé de créer des jeux de données dédiés spécifiquement pour stocker les champs pouvant être mis à jour. Utilisez un jeu de données distinct pour chaque classe XDM.

Créez un jeu de données pour Profil individuel et un autre pour Compte professionnel. Sélectionnez chaque nouveau jeu de données pendant le processus de configuration :

1. Pour **[!UICONTROL Jeux de données]**, sélectionnez la nouvelle source de données que vous avez créée.

1. Choisissez les champs du jeu de données sélectionné.

   ![ Boîte de dialogue permettant de sélectionner des champs pouvant être mis à jour à partir des jeux de données dans la configuration de schéma XDM](./assets/xdm-select-updateable.png){width="450" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Enregistrer]** pour appliquer vos modifications.

### Schémas relationnels

Les schémas relationnels vous permettent de créer des classes de données personnalisées. Grâce à l’accès à plusieurs jeux de données, vous pouvez créer des classes spécialement adaptées à vos besoins en matière de données. Utilisez des schémas relationnels pour les entités commerciales telles que les achats, les licences et les enregistrements d’événements dans les décisions de parcours et la personnalisation des e-mails. Vous pouvez sélectionner jusqu’à 50 schémas et 100 champs par schéma.

Pour plus d’informations sur l’utilisation des champs sélectionnés pour la personnalisation avancée des e-mails, voir [Personnalisation de contenu](../content/personalization.md#custom-datasets). Pour plus d’informations sur l’utilisation des champs sélectionnés pour la prise de décision par parcours (chemins partagés par compte ou personnes), voir [Filtrage des données personnalisées](../journeys/split-merge-paths-nodes.md#custom-data-filtering).

>[!AVAILABILITY]
>
>Les [Schémas relationnels](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/relational#) sont disponibles à l’[!DNL Journey Optimizer B2B Edition] dans une version à disponibilité limitée. Les schémas Data Mirror et relationnels sont disponibles pour les détenteurs de licence [!DNL Journey Optimizer Orchestrated Campaigns]. Les schémas relationnels sont également disponibles en tant que version limitée pour les utilisateurs [!DNL Customer Journey Analytics], selon votre licence et l’activation de la fonctionnalité. Contactez votre représentant Adobe pour obtenir l’accès.

>[!NOTE]
>
>Cette fonctionnalité prend actuellement en charge les cas d’utilisation d’objets personnalisés liés au compte et aux personnes, et prévoit de prendre en charge d’autres cas d’utilisation d’objets prêts à l’emploi à l’avenir.

Vous pouvez créer des schémas relationnels à l’aide de l’éditeur de schémas (accédez à **[!UICONTROL Gestion des données]** > **[!UICONTROL Schémas]** dans le volet de navigation de gauche).

Lors de la création d’un schéma à utiliser avec [!DNL Journey Optimizer B2B Edition], les valeurs de configuration suivantes sont requises :

* Comportement : enregistrement
* Segmentation : activée
* Type de relation : plusieurs à un
* Schéma de référence : compte B2B
* Champs obligatoires : clé de Principal, clé étrangère et descripteur de version
* Jeu de données associé : défini et mappé au schéma

Pour sélectionner des champs de schéma relationnel à utiliser dans [!DNL Journey Optimizer B2B Edition] :

1. Sélectionnez l’onglet **[!UICONTROL Relationnel]** pour afficher vos schémas.

   ![Onglet Schémas relationnels dans l’éditeur de schémas affichant les champs d’entité commerciale pour Adobe Journey Optimizer B2B edition](assets/xdm-relational.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Sélectionner le schéma XDM relationnel]**.

   >[!NOTE]
   >
   >Dans cette version bêta, seuls les _objets personnalisés de compte et de personne à un_ sont pris en charge.

1. Sélectionnez un schéma relationnel et cliquez sur **[!UICONTROL Suivant]**.

   ![Sélectionnez un schéma relationnel dans la boîte de dialogue](./assets/xdm-classes-relational-select-schema-dialog.png){width="500" zoomable="yes"}

1. Saisissez un espace de noms ou utilisez l’espace de noms par défaut. Cliquez sur **[!UICONTROL Suivant]**.

   Vous ne pouvez définir l’espace de noms qu’une seule fois et ne pouvez pas inverser cette action.

   ![Espace de noms par défaut dans la boîte de dialogue Créer un espace de noms ](./assets/xdm-classes-relational-create-namespace.png){width="400" zoomable="yes"}

1. Examinez les champs de schéma relationnel .

   Cliquez sur l’icône _Info_ ![Icône Info](../assets/do-not-localize/icon-info-light.svg) pour afficher les métadonnées du champ.

1. Sélectionnez les champs à activer pour les parcours et la personnalisation.

   La plateforme sélectionne automatiquement les champs obligatoires suivants :

   * Clé étrangère
   * Clé primaire
   * Descripteur de version

   Utilisez le champ _[!UICONTROL Rechercher]_ pour filtrer la liste affichée par nom. Utilisez le curseur **[!UICONTROL Afficher uniquement les champs sélectionnés]** pour passer en revue les sélections actuelles.

   ![Sélectionnez les champs du schéma relationnel dans la boîte de dialogue](./assets/xdm-classes-relational-select-schema-fields.png){width="500" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Enregistrer]**
