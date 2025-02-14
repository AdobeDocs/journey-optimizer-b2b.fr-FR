---
title: Gestion des utilisateurs
description: Découvrez comment affecter des membres de l’équipe aux profils de produits Journey Optimizer B2B edition.
feature: Setup
roles: Admin
exl-id: ddbdc6a5-49bc-46cd-8d9b-1d37223dffe2
source-git-commit: d5197e740a17de507bf72b4d7b64deb5af672346
workflow-type: tm+mt
source-wordcount: '1351'
ht-degree: 2%

---

# Gestion des utilisateurs

Une fois la mise en service terminée et les sandbox liés, procédez comme suit pour fournir un accès Adobe Journey Optimizer B2B edition à votre équipe et aux utilisateurs.

1. [Création d’un profil de produit Marketo Engage](#marketo-engage-profile) dans Admin Console (nouvelle instance Marketo Engage uniquement).
1. [Création d’un groupe d’utilisateurs](#create-user-group) dans Admin Console.
1. [Modifiez les rôles intégrés](#edit-roles) ou [créez un rôle personnalisé](#create-a-custom-role) avec les autorisations Journey Optimizer B2B edition.
1. [Ajoutez des utilisateurs](#add-users) des utilisatrices ou des [groupes](#add-user-groups-to-a-role) aux rôles.

En tant qu’administrateur, vous pouvez effectuer ces tâches dans le Adobe Admin Console, qui constitue un emplacement central pour administrer et gérer vos licences de produit et utilisateurs Adobe. Dans Admin Console, vous pouvez créer et gérer des utilisateurs à un seul emplacement plutôt qu’au sein de vos différentes solutions individuelles. Reportez-vous à la page [Présentation d’Admin Console](https://helpx.adobe.com/fr/enterprise/using/admin-console.html) pour en savoir plus sur ses fonctions et fonctionnalités.

## Accès à Admin Console

Avant de pouvoir utiliser Admin Console pour administrer les utilisateurs au sein de votre équipe, vous devez vous assurer que vous pouvez accéder à Admin Console et que vous disposez des autorisations appropriées.

1. En tant qu’administrateur système, vous devriez recevoir plusieurs e-mails d’Adobe dans le cadre du processus d’intégration.

   Recherchez l’e-mail de bienvenue qui fournit les informations sur le nom de l’organisation auquel vous avez accès.

1. Cliquez sur le lien **[!UICONTROL Commencer]** dans l’e-mail de bienvenue pour accéder à Admin Console.

   Si vous ne retrouvez pas l’e-mail en question, ouvrez un navigateur directement sur Admin Console à l’adresse [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Connectez-vous à l’aide de votre Adobe ID.

   Une fois la connexion établie, la page _Aperçu_ du Adobe Admin Console s’affiche.

1. Si vous avez accès à plusieurs organisations, vérifiez que vous vous êtes connecté à la bonne organisation.

   Pour modifier votre organisation, cliquez sur le nom de l’organisation dans le coin supérieur droit et sélectionnez l’organisation à laquelle vous avez besoin d’accéder.

1. Sélectionnez **[!UICONTROL Administrateurs]** dans la vignette _[!UICONTROL Utilisateurs]_ pour vérifier que vous êtes bien administrateur système.

   ![Présentation d’Admin Console - cliquez sur Administrateurs](./assets/admin-console-overview-administrators.png){width="700" zoomable="yes"}

1. Recherchez en saisissant votre adresse e-mail, votre nom d’utilisateur, votre prénom ou votre nom Adobe ID.

   * Si votre accès est correctement configuré, la recherche renvoie votre enregistrement.

   * Si la valeur de la colonne **[!UICONTROL RÔLE D’ADMINISTRATEUR]** s’affiche `System`, vous savez que vous (ou l’utilisateur affiché) êtes un administrateur ou une administratrice système.

## Création du profil de produit Marketo Engage {#marketo-engage-profile}

Lorsque vous accordez aux utilisateurs l’accès à une solution Adobe, vous ne souhaitez pas nécessairement leur accorder un accès complet. Les profils de produit permettent à chaque solution d’avoir son propre jeu d’autorisations utilisateur. Utilisez Admin Console pour attribuer des profils de produit.

Pour plus d’informations sur l’utilisation des profils de produit pour les droits des utilisateurs, voir [Gérer les profils de produit pour les utilisateurs d’entreprise](https://helpx.adobe.com/fr/enterprise/using/manage-product-profiles.html){target="_blank"} dans la documentation d’Admin Console.
<!--
>[!BEGINSHADEBOX]

When you add a user to the Marketo Engage product profile, they are subsequently added to the _Standard User_ role within the Default workspace of the Marketo Engage subscription. This role grants them all _Standard User_ permissions for Marketo Engage in that workspace. Currently, all Journey Optimizer B2B Edition users are required to be Marketo Engage users. A Marketo Engage administrator can restrict access by updating the permissions for the _Standard User_ role or by moving the user to a different Marketo Engage user role with more restrictive permissions.

For more information about managing these permissions within Marketo Engage, see [Managing User Roles and Permissions](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/users-and-roles/managing-user-roles-and-permissions){target="_blank"} in the Marketo Engage documentation.

>[!ENDSHADEBOX]-->

![Exigences relatives au rôle d’administrateur](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Un administrateur système ou un administrateur de produit Marketo Engage peut effectuer les étapes suivantes.

1. Connectez-vous à [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Sélectionnez l’onglet **[!UICONTROL Produits]**.

1. Ouvrez l’instance Marketo Engage à laquelle vous souhaitez ajouter le profil et cliquez sur **[!UICONTROL Nouveau profil]**.

   ![Admin Console - Instance Marketo Engage - Nouveau profil](./assets/admin-console-marketo-engage-instance-new-profile.png){width="700" zoomable="yes"}

1. Saisissez un nom de profil de produit, tel que _Utilisateur standard_.

1. Cliquez sur **Suivant** puis sur **Enregistrer**.

## Création d’un groupe d’utilisateurs {#create-user-group}

Un groupe d’utilisateurs est un ensemble d’utilisateurs auxquels est accordé un ensemble partagé d’autorisations. Vous pouvez ajouter ou supprimer des utilisateurs dans votre groupe d’utilisateurs. Les autorisations de groupe restent les mêmes tandis que les utilisateurs du groupe changent.

Pour plus d’informations sur l’utilisation des groupes d’utilisateurs pour gérer les autorisations, voir [Gérer les groupes d’utilisateurs](https://helpx.adobe.com/fr/enterprise/using/user-groups.html){target="_blank"} dans la documentation d’Admin Console.

![Exigences relatives au rôle d’administrateur](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Un administrateur système peut effectuer les étapes suivantes.

1. Connectez-vous à [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Sélectionnez l’onglet **[!UICONTROL Utilisateurs]**.

1. Sélectionnez **[!UICONTROL Groupes d’utilisateurs]** dans le volet de navigation de gauche.

1. Cliquez sur **[!UICONTROL Nouveau groupe d’utilisateurs]** en haut à droite.

1. Saisissez le nom du groupe d’utilisateurs, par exemple _Utilisateurs standard_ et cliquez sur **[!UICONTROL Enregistrer]**.

1. Cliquez sur le groupe d’utilisateurs que vous venez de créer.

1. Sélectionnez l’onglet **[!UICONTROL Profils de produit attribués]** et cliquez sur **[!UICONTROL Attribuer un profil]**.

1. Cliquez sur **+** et ajoutez chaque instance des produits suivants :

   * [!UICONTROL Marketo Engage]
   * [!UICONTROL Adobe Experience Platform - AEP-Default-All-Users]
   * [!UICONTROL Collecte de données dʼAdobe Experience Platform]
   * [!UICONTROL Accès complet à la collecte de données]

   ![Admin Console - groupe d’utilisateurs - ajout de produits](./assets/admin-console-user-group-add-products.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Enregistrer]**.

## Ajout d’utilisateurs à un groupe

Pour plus d’informations sur la gestion des utilisateurs, voir [Utilisateurs Admin Console](https://helpx.adobe.com/fr/enterprise/using/user-groups.html) dans la documentation d’Admin Console.

![Exigences relatives au rôle d’administrateur](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Un administrateur système ou un administrateur de produit peut effectuer les étapes suivantes. Un administrateur ou une administratrice de produit ne peut ajouter que des utilisateurs et utilisatrices qui existent déjà dans son organisation.

1. Accédez à [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Sous _[!UICONTROL Liens rapides]_, cliquez sur **[!UICONTROL Ajouter des utilisateurs]**.

1. Ajoutez chaque utilisateur :

   * Saisissez l’adresse e-mail, le prénom et le nom de l’utilisateur.

     ![Experience Platform - ajouter des profils pour le nouveau rôle](./assets/admin-console-add-users.png){width="600" zoomable="yes"}

   * Pour **[!UICONTROL Groupes d’utilisateurs]**, cliquez sur **+**.

   * Sélectionnez le groupe d’utilisateurs que vous avez créé précédemment.

   * Cliquez sur **[!UICONTROL Appliquer]**.

1. Cliquez sur **[!UICONTROL Enregistrer]**.

## Modifier les rôles pour les autorisations de produit {#edit-roles}

Les autorisations sont des droits unitaires qui vous permettent de définir les autorisations attribuées à un profil de produit. Chaque autorisation est regroupée sous une fonctionnalité, telle que parcours ou groupes d’achats, qui représente les différentes fonctionnalités ou objets dans Journey Optimizer B2B edition.

La zone _Autorisations_ de Adobe Experience Platform permet aux administrateurs de définir des rôles d’utilisateur et des politiques d’accès afin de gérer les autorisations d’accès aux fonctionnalités et objets d’une application de produit. Dans cette application, vous pouvez créer et gérer des rôles, ainsi qu’attribuer les autorisations de ressources souhaitées pour ces rôles. Les autorisations vous permettent également de gérer les sandbox et les utilisateurs associés à un rôle spécifique.

Pour plus d’informations sur les autorisations des rôles dans Experience Platform, voir [Gérer les autorisations pour un rôle](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions){target="_blank"} dans la documentation d’Experience Platform.
<!-- 
### B2B product permissions

The following permissions govern access to Journey Optimizer B2B Edition capabilities:

| Category | Description | Permissions |
| -------- | ----------- | ---------- |
| B2B Account Lists | Configure, manage, view, and publish permissions for B2B account lists. These permissions include actions such as add, remove, import, and delete accounts from account lists. | <li>Manage B2B Account Lists |
| B2B Admin Configurations | Configure, manage, and view permissions for B2B administrative configurations. These permissions include digital asset management connections, asset repositories, and events. | <li>Manage B2B Admin Configurations |
| B2B Assets | Configure, manage, and view permissions for B2B assets. These permissions include emails, SMS, landing pages, fragments, templates, and images. | <li>Manage B2B Assets <li>Manage B2B Templates <li>Manage B2B Fragments|
| B2B Buying Groups | Configure, manage, and view permissions for B2B buying groups. These permissions include solution interests, roles templates, and buying group status. | <li>Manage B2B Buying Groups |
| B2B Channel Configurations | Configure, manage, and view permissions for B2B channel configurations. These permissions include settings for communication limits, API credentials, and security settings. | <li>Manage B2B Channels Configurations |
| B2B Dashboards |Configure and view permissions for B2B dashboards. These permissions include account engagement, buying group stages, surging accounts, and contact coverage. | <li>Manage B2B Dashboards |
| B2B Journeys | Configure manage, view, and publish permissions for B2B journeys. These permissions include account and person actions, event listeners, and split paths | <li>Manage B2B Journeys |

### B2B built-in roles

When your organization has the Journey Optimizer B2B Edition product provisioned, Experience Platform includes a set of built-in (default) roles that you can use to manage access to the product capabilities:

| Role | Permissions |
| ---- | ----------- |
| B2B Journey Manager | <li>Manage B2B Journeys <li>Manage B2B Buying Groups <li>Manage B2B Account Lists <li>View B2B Intelligent Dashboard <li>View B2B Insights Dashboard |
| B2B Channel Manager | <li>Manage B2B Assets <li>Manage B2B Templates <li>Manage B2B Fragments |
| B2B System Administrator | <li>Manage B2B Channels Configurations <li>Manage B2B Admin Configurations |
| B2B Sales User | <li>View Intelligent Dashboard |

### Edit role permissions

For built-in or custom roles, you can decide at any time to add or delete permissions. If you modify a default or custom role, it impacts every user assigned to the role.

In the following example, you want to add permissions related to the B2B Journeys resource for users assigned to the B2B Channel Manager role. This change enables users for that role to manage account journeys also.

>[!NOTE]
>
>An Admin Console system administrator can perform these steps.

_To change the permissions for a role:_

1. Go to [experience.adobe.com](https://experience.adobe.com/).

1. In the _[!UICONTROL Quick access]_ panel, select **[!UICONTROL Permissions]**.

   >[!NOTE]
   >
   >If you don't see _[!UICONTROL Permissions]_, you may need to click **[!UICONTROL View all]** and select it from the available applications.

   ![Experience Platform - access Permissions](./assets/aep-permissions.png){width="700" zoomable="yes"}

1. Select **[!UICONTROL Roles]** in the left navigation.

1. Click the **_B2B Channel Manager_** role name.

1. In the details page, click **[!UICONTROL Edit]** at the top right.

   ![Experience Platform - edit the role](./assets/aep-permissions-role-edit.png){width="700" zoomable="yes"}

   In the role editor, the _[!UICONTROL Resources]_ menu displays the list of resources that apply to the Experience Cloud - Platform powered applications products.

   You can enter _B2B_ in the search tool to filter the list for the B2B product permissions. 
   
1. Click the _Add_ icon (**+**) for the B2B Journeys resource.

   ![Experience Platform - edit the role](./assets/aep-permissions-role-edit-b2b-journeys-add.png){width="700" zoomable="yes"}

1. In the _[!UICONTROL B2B Journeys]_ permissions card, select **[!UICONTROL Manage B2B Account Journeys]**.

1. Click **[!UICONTROL Save]**.

   ![Experience Platform - edit the role](./assets/aep-permissions-role-edit-b2b-journeys-done.png){width="700" zoomable="yes"}

1. Click **[!UICONTROL Close]** to return to the details page. -->

### Ajouter des utilisateurs à un rôle

![Exigences relatives au rôle d’administrateur](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Un administrateur système ou un administrateur de produit AEP peut effectuer les étapes suivantes.

1. Ouvrez les détails du rôle et sélectionnez l’onglet **[!UICONTROL Utilisateurs]**.

   Cet onglet affiche une liste de tous les utilisateurs affectés au rôle.

1. Cliquez sur **[!UICONTROL Ajouter des utilisateurs]**.

   ![Experience Platform - ajouter des utilisateurs au rôle](./assets/aep-permissions-role-add-users.png){width="700" zoomable="yes"}

1. Dans la boîte de dialogue _[!UICONTROL Ajouter des utilisateurs]_, recherchez et sélectionnez les utilisateurs que vous souhaitez ajouter au rôle.

   * Vous pouvez utiliser l’outil Rechercher pour filtrer la liste des utilisateurs.

   * Cochez la case de chaque utilisateur ou utilisatrice.

   ![Experience Platform - Boîte de dialogue Ajouter des utilisateurs](./assets/aep-permissions-role-add-users-dialog.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Enregistrer]** lorsque vous avez sélectionné tous les utilisateurs à ajouter.

### Ajouter des groupes d’utilisateurs à un rôle

Pour plus d’informations sur la gestion des utilisateurs, voir [Utilisateurs Admin Console](https://helpx.adobe.com/fr/enterprise/using/user-groups.html) dans la documentation d’Admin Console.

![Exigences relatives au rôle d’administrateur](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Un administrateur système ou un administrateur de produit AEP peut effectuer les étapes suivantes.

1. Ouvrez les détails du rôle et sélectionnez l’onglet **[!UICONTROL Groupes d’utilisateurs]**.

   Cet onglet affiche la liste de tous les groupes d’utilisateurs affectés au rôle.

1. Cliquez sur **[!UICONTROL Ajouter des groupes]**.

   ![Experience Platform - ajouter des utilisateurs au rôle](./assets/aep-permissions-role-add-groups.png){width="700" zoomable="yes"}

1. Dans la boîte de dialogue _[!UICONTROL Ajouter des groupes]_, recherchez et sélectionnez les groupes à ajouter au rôle.

   * Vous pouvez utiliser l’outil Rechercher pour filtrer la liste des groupes d’utilisateurs.

   * Cochez la case de chaque groupe d’utilisateurs.

   ![Experience Platform - Boîte de dialogue Ajouter des groupes](./assets/aep-permissions-role-add-groups-dialog.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Enregistrer]** lorsque vous avez sélectionné tous les utilisateurs à ajouter.

## Créer un rôle personnalisé

![Exigences relatives au rôle d’administrateur](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Un administrateur système ou un administrateur de produit AEP peut effectuer les étapes suivantes.

1. Sélectionnez **[!UICONTROL Rôles]** dans le volet de navigation de gauche, puis sélectionnez **[!UICONTROL Créer un rôle]**.

1. Dans la boîte de dialogue _[!UICONTROL Créer un nouveau rôle]_, saisissez un nom pour le rôle, tel que _Spécialistes du marketing B2B_, ainsi qu’une description (facultatif).

1. Cliquez sur **[!UICONTROL Confirmer]**.

1. Sélectionnez vos sandbox.

   ![Experience Platform - ajouter des sandbox pour le nouveau rôle](./assets/aep-permissions-role-sandboxes.png){width="700" zoomable="yes"}

1. Ajoutez les autorisations de profil :

   * Dans la liste _[!UICONTROL Ressources]_ sur la gauche, recherchez l’élément **[!UICONTROL Gestion des profils]** et cliquez sur l’icône _Ajouter_ (**+**) pour ajouter l’attribut.

   * Pour l’attribut , ajoutez les autorisations suivantes :
      * [!UICONTROL Affichage des segments]
      * [!UICONTROL Gérer les segments]
      * [!UICONTROL Affichage des profils]
      * [!UICONTROL Gérer les profils]
      * [!UICONTROL Afficher le profil B2B]
      * [!UICONTROL Gérer le profil B2B]

   ![Experience Platform - ajouter des profils pour le nouveau rôle](./assets/aep-permissions-role-profiles.png){width="700" zoomable="yes"}

1. Ajoutez les autorisations de produit B2B :

   Reportez-vous à la liste des autorisations de produit [B2B](#b2b-product-permissions) pour déterminer les fonctionnalités de produit souhaitées pour le rôle.

   Dans la liste _[!UICONTROL Ressources]_ sur la gauche, localisez les éléments **[!UICONTROL B2B]** et cliquez sur l’icône _Ajouter_ (**+**) pour ajouter chaque attribut que vous souhaitez activer pour le rôle.

   Vous pouvez saisir _B2B_ dans l’outil de recherche pour filtrer la liste des autorisations de produit B2B.

1. Cliquez sur **[!UICONTROL Enregistrer]** en haut à droite.

1. Accédez aux détails du rôle et sélectionnez l’onglet **[!UICONTROL Groupes d’utilisateurs]**.

1. Cliquez sur **[!UICONTROL Ajouter des groupes]**.

   ![Experience Platform - ajouter des profils pour le nouveau rôle](./assets/aep-permissions-role-add-groups.png){width="700" zoomable="yes"}

1. Cochez la case en regard du groupe d’utilisateurs que vous avez créé précédemment dans Admin Console.

1. Cliquez sur **[!UICONTROL Enregistrer]**.
