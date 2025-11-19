---
title: Gestion des champs XDM
description: Utilisez la gestion des champs XDM pour contrôler les données disponibles dans Journey Optimizer B2B edition.
feature: Data Management, Integrations
role: User
badgeBeta: label="Beta" type="informative" tooltip="Cette fonctionnalité est actuellement en version bêta limitée"
source-git-commit: de7f5620556a48fe6f12ed1c70e925e11ec770f1
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 2%

---


# Gestion des champs XDM

Les champs de modèle de données d’expérience (XDM) sont des éléments de schéma qui fournissent des données à l’application [!DNL Journey Optimizer B2B Edition]. Vous utilisez les champs XDM comme filtres et contraintes dans les parcours, les groupes d’achats et les fonctionnalités telles que la personnalisation des e-mails et le contenu conditionnel.

Les schémas définissent des champs en fonction des classes XDM standard. Les classes XDM standard incluent le profil individuel, le compte professionnel et les événements d’expérience. Les schémas relationnels définissent également des champs qui vous permettent de modéliser des données structurées de la même manière que les bases de données relationnelles traditionnelles.

Les schémas de Adobe Experience Platform (AEP) contiennent généralement de nombreux champs dans des hiérarchies complexes. La traversée des arborescences de schéma XDM prend du temps. La gestion des champs XDM rationalise la sélection des champs en affichant uniquement les champs pertinents à chaque parcours. Les administrateurs contrôlent les champs qui s’affichent pour les créateurs et créatrices de parcours. Les administrateurs définissent également les champs en lecture seule ou modifiables. Ces actions améliorent l’efficacité lors de la conception du parcours.

Les administrateurs qui comprennent XDM et collaborent avec les ingénieurs de données ou les parties prenantes de la modélisation des données de la plateforme de données client (CDP) B2B suivent les procédures de ce guide.

>[!NOTE]
>Les [schémas relationnels](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/relational#) sont disponibles pour [!DNL Journey Optimizer B2B Edition] dans une version limitée. Les schémas Data Mirror et relationnels sont disponibles pour les détenteurs de licence des campagnes orchestrées Journey Optimizer. Les schémas relationnels sont également disponibles en tant que version limitée pour les utilisateurs de Customer Journey Analytics, selon votre licence et l’activation de la fonctionnalité. Contactez votre représentant Adobe pour obtenir l’accès.

## Accès aux classes XDM

Pour ouvrir la zone de gestion des champs XDM, accédez à **Configurations** > CONFIGURATION > **Classes XDM**.

* Vous ne pouvez ajouter de nouveaux champs qu’après l’utilisation active d’un schéma dans un parcours.
* La suppression, le changement de nom ou la modification de types de champ peut entraîner des problèmes de fonctionnalité de parcours. Soyez prudent lors de la manipulation des schémas.
* Ne renommez pas et ne supprimez pas les schémas, et ne modifiez pas les clés des schémas relationnels.

>[!IMPORTANT]
>Vous pouvez mettre à jour votre sélection de champs à tout moment en sélectionnant de nouveaux champs ou en désélectionnant les champs dont vous n’avez plus besoin. Une fois que vous avez publié un parcours à l’aide de ce schéma, vous verrouillez sa structure. La suppression ou le changement de nom du schéma, l’ajout de nouveaux champs ou la modification de types de champs n’est pas pris en charge et peut entraîner des échecs de parcours.

## Classes standard

Dans l’onglet Classes standard , vous pouvez modifier _Champs gérés_ et _Champs modifiables_.

* Les champs gérés apparaissent dans les parcours, les groupes d’achats et les fonctionnalités de personnalisation.
* Les champs pouvant être mis à jour servent de contraintes pour les nœuds de parcours _Mettre à jour le profil de compte_ et _Mettre à jour le profil de personne_.

![Onglet Classes standard affichant les champs gérés et modifiables pour la configuration de la classe XDM](assets/xdm-standard.png){width="600" zoomable="yes"}

Pour sélectionner des champs à partir du schéma d’union pour les classes XDM standard, procédez comme suit :

1. Accédez à **Administration** > **Configurations** > **Classes XDM**.
1. Ouvrez l’onglet **Standard**. Choisissez l’une des classes suivantes :

   * Profil individuel XDM
   * Compte professionnel XDM

Le tableau affiche des informations, notamment :

* Nombre de champs gérés
* Nombre de champs modifiables
* Heure de la dernière mise à jour

Cliquez sur le nom de la classe pour ouvrir la boîte de dialogue de sélection _Champs gérés_.

![Boîte de dialogue de sélection des champs gérés pour les classes XDM standard affichant les options de champs configurables](assets/xdm-standard-managed-fields.png){width="600" zoomable="yes"}

1. Cliquez sur le menu **...** pour basculer entre _[!UICONTROL Champs gérés]_ et _[!UICONTROL Champs modifiables]_. La boîte de dialogue répertorie tous les champs configurables.
1. Sélectionnez jusqu’à 100 champs pour chaque classe XDM.
1. Cliquez sur **[!UICONTROL Enregistrer]** pour confirmer vos sélections.

Utilisez le filtre [!UICONTROL Afficher uniquement les champs sélectionnés] pour afficher uniquement les champs actifs.

Pour les _champs pouvant être mis à jour_, accédez à une boîte de dialogue distincte qui vous permet de choisir des champs provenant d’autres sources de données :

1. Dans la liste déroulante Jeux de données , sélectionnez la source de données à configurer.
1. Modifiez les champs du jeu de données sélectionné.
1. Cliquez sur **[!UICONTROL Enregistrer]** pour appliquer vos modifications.

![ Boîte de dialogue permettant de sélectionner des champs pouvant être mis à jour à partir des jeux de données dans la configuration de schéma XDM](assets/xdm-select-updateable.png){width="600" zoomable="yes"}

Le champ doit d’abord être _Géré_ avant de pouvoir être _Modifiable_. Les _champs pouvant être mis à jour_ que vous sélectionnez doivent exister dans votre schéma fourni par l’utilisateur.

## Schémas relationnels

Les schémas relationnels vous permettent de créer des classes de données personnalisées. Grâce à l’accès à plusieurs jeux de données, vous pouvez créer des classes spécialement adaptées à vos besoins en matière de données.
Utilisez des schémas relationnels pour les entités commerciales telles que les achats, les licences et les enregistrements d’événements dans les décisions de parcours et la personnalisation des e-mails. Vous pouvez sélectionner jusqu’à 50 schémas et 100 champs par schéma.

![Onglet Schémas relationnels de l’éditeur de schémas affichant les champs d’entité commerciale pour Adobe Journey Optimizer](assets/xdm-relational.png)

>[!NOTE]
>Cette fonctionnalité prend actuellement en charge les cas d’utilisation d’objets personnalisés liés au compte , et prévoit de prendre en charge d’autres cas d’utilisation d’objets prêts à l’emploi à l’avenir.

Créez des schémas relationnels à l’aide de l’éditeur de schémas dans **Gestion des données** > **Schémas**.

Ces valeurs de configuration doivent être incluses lors de la création d’un schéma à utiliser avec [!DNL Journey Optimizer B2B Edition] :

* Comportement : enregistrement
* Segmentation : activée
* Type de relation : plusieurs à un
* Schéma de référence : compte B2B
* Champs obligatoires : clé de Principal, clé étrangère et descripteur de version
* Jeu de données associé : défini et mappé au schéma

### Création d’un schéma relationnel

Pour sélectionner les champs à utiliser dans [!DNL Journey Optimizer B2B Edition], procédez comme suit :

1. Accédez à **Administration** > **Configurations** > **Classes XDM**.
1. Ouvrez l’onglet **Relationnel** pour afficher vos schémas.
1. Cliquez sur **[!UICONTROL Sélectionner le schéma XDM relationnel]**.

   * Dans la version bêta, seuls les _objets personnalisés de compte multiples-à-un_ sont pris en charge.

1. Sélectionnez un schéma relationnel et cliquez sur **[!UICONTROL Suivant]**.

   * Dans la version bêta, vous ne pouvez pas supprimer un schéma de la liste une fois que vous l’avez sélectionné.

1. Saisissez un espace de noms ou utilisez l’espace de noms par défaut. Cliquez sur **[!UICONTROL Suivant]**.

   * Vous ne pouvez définir l’espace de noms qu’une seule fois et ne pouvez pas inverser cette action.

1. Examinez les champs de schéma relationnel . Cliquez sur l’icône ![Icône Info](../assets/do-not-localize/icon-info-light.svg) [!UICONTROL Info] pour afficher les métadonnées du champ.
1. Sélectionnez les champs à activer pour les parcours et la personnalisation. La plateforme sélectionne automatiquement les champs obligatoires suivants :

   * Clé étrangère
   * Clé primaire
   * Descripteur de version

1. Utilisez le curseur [!UICONTROL  Afficher uniquement les champs sélectionnés ] pour prévisualiser vos sélections.
1. Filtrez les champs par nom à l’aide de la barre de recherche.
1. Cliquez sur **[!UICONTROL Enregistrer]**

## Événements

Utilisez les événements d’expérience et leurs champs associés dans les décisions de parcours. Vous pouvez sélectionner jusqu’à 50 événements et 100 champs par événement.

![Onglet Événements présentant la sélection des Événements d’expérience et les champs de schéma pour les parcours et la personnalisation](assets/xdm-events.png){width="700" zoomable="yes"}

Cliquez sur le nom d’un événement pour en afficher les détails et modifier les champs configurés.

Pour sélectionner des champs de schéma et des événements d’expérience, procédez comme suit :

1. Accédez à **Administration** > **Configurations** > **Classes XDM**.
1. Ouvrez l’onglet **Événements**.
1. Pour sélectionner des champs pour un événement, cliquez sur **[!UICONTROL Sélectionner un événement d’expérience]**.
1. Sur la page Détails, cliquez sur **[!UICONTROL Sélectionner le type d’événement]**.
1. Dans la liste Événement , choisissez votre événement.
1. Cliquez sur **[!UICONTROL Sélectionner]** pour fermer la boîte de dialogue.

   * Dans la version bêta, vous ne pouvez pas supprimer les événements sélectionnés.

1. Cliquez sur **[!UICONTROL Sélectionner les champs]**.
1. Utilisez le curseur [!UICONTROL  Afficher uniquement les champs sélectionnés ] pour afficher vos sélections actuelles.
1. Sélectionnez les champs à utiliser dans les [!DNL Journey Optimizer B2B Edition]. Cliquez sur **[!UICONTROL Sélectionner]** pour fermer la boîte de dialogue.
1. Cliquez sur [!UICONTROL Enregistrer]
