---
title: Gestion des utilisateurs
description: Découvrez comment affecter des membres de l’équipe à des profils de produit Journey Optimizer B2B edition.
feature: Setup
roles: Admin
exl-id: ddbdc6a5-49bc-46cd-8d9b-1d37223dffe2
source-git-commit: 97a9932a8a2a1c7a37dcc110b59cee70a61b5763
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 4%

---

# Gestion des utilisateurs

Une fois la mise en service terminée et les environnements de test liés, procédez comme suit pour accorder l’accès à Adobe Journey Optimizer B2B edition à votre équipe et à vos utilisateurs.

1. [Créez un profil de produit Marketo Engage](#marketo-engage-profile) dans l’Admin Console (nouvelle instance de Marketo Engage uniquement).
1. [Créez un groupe d’utilisateurs](#create-user-group) dans l’Admin Console.
1. [Créez un rôle](#create-role) dans les autorisations AEP.
1. [Ajoutez des utilisateurs](#add-users) dans l’Admin Console.

En tant qu’administrateur, vous pouvez effectuer ces tâches dans Adobe Admin Console, qui constitue un emplacement central pour administrer et gérer vos licences de produit et utilisateurs Adobes. Dans l’Admin Console, vous pouvez créer et gérer des utilisateurs à un seul emplacement au lieu de dans vos différentes solutions individuelles. Pour en savoir plus sur ses fonctions et fonctionnalités, consultez la page [Aperçu de l’Admin Console](https://helpx.adobe.com/fr/enterprise/using/admin-console.html) .

## Accès à Admin Console

Avant de pouvoir utiliser l’Admin Console pour administrer les utilisateurs au sein de votre équipe, vous devez vous assurer que vous pouvez accéder à l’Admin Console et disposer des autorisations appropriées.

1. En tant qu’administrateur système, vous devriez recevoir plusieurs courriers électroniques d’Adobe dans le cadre du processus d’intégration.

   Recherchez l’e-mail de bienvenue qui fournit des informations sur le nom de l’organisation auquel vous avez accès.

1. Cliquez sur le lien **[!UICONTROL Commencer]** de votre e-mail de bienvenue pour accéder à l’Admin Console.

   Si vous ne trouvez pas l’email, ouvrez un navigateur directement sur l’Admin Console à l’adresse [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Connectez-vous à l’aide de votre Adobe ID.

   Une fois la connexion établie, la page _Aperçu_ de Adobe Admin Console s’affiche.

1. Si vous avez accès à plusieurs organisations, vérifiez que vous vous êtes connecté à la bonne organisation.

   Pour modifier votre organisation, cliquez sur le nom de l’organisation dans le coin supérieur droit et sélectionnez l’organisation à laquelle vous avez besoin d’accéder.

1. Sélectionnez **[!UICONTROL Administrateurs]** dans la carte _[!UICONTROL Utilisateurs]_ pour vérifier que vous êtes un administrateur système.

   ![Aperçu de l’Admin Console - cliquez sur Administrateurs](./assets/admin-console-overview-administrators.png){width="700" zoomable="yes"}

1. Effectuez une recherche en saisissant votre adresse électronique, votre nom d’utilisateur, votre prénom ou votre nom Adobe ID.

   * Si votre accès est correctement configuré, la recherche renvoie votre enregistrement.

   * Si la valeur de la colonne **[!UICONTROL ADMIN ROLE]** indique `System`, vous savez que vous (ou l’utilisateur affiché) êtes un administrateur système.

## Création du profil de produit du Marketo Engage {#marketo-engage-profile}

Lorsque vous accordez aux utilisateurs l’accès à une solution d’Adobe, vous ne souhaitez pas nécessairement leur accorder un accès complet. Les profils de produit permettent à chaque solution d’avoir son propre jeu d’autorisations utilisateur. Utilisez l’Admin Console pour attribuer des profils de produit.

Pour plus d’informations sur l’utilisation des profils de produit pour les droits des utilisateurs, voir [Gestion des profils de produit pour les utilisateurs d’entreprise](https://helpx.adobe.com/fr/enterprise/using/manage-product-profiles.html){target="_blank"} dans la documentation Admin Console.
<!--
>[!BEGINSHADEBOX]

When you add a user to the Marketo Engage product profile, they are subsequently added to the _Standard User_ role within the Default workspace of the Marketo Engage subscription. This role grants them all _Standard User_ permissions for Marketo Engage in that workspace. Currently, all Journey Optimizer B2B Edition users are required to be Marketo Engage users. A Marketo Engage administrator can restrict access by updating the permissions for the _Standard User_ role or by moving the user to a different Marketo Engage user role with more restrictive permissions.

For more information about managing these permissions within Marketo Engage, see [Managing User Roles and Permissions](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/users-and-roles/managing-user-roles-and-permissions){target="_blank"} in the Marketo Engage documentation.

>[!ENDSHADEBOX]-->

>[!NOTE]
>
>Un administrateur système Admin Console ou un administrateur de produit Marketo Engage peut effectuer ces étapes.

1. Connectez-vous à [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Sélectionnez l’onglet **[!UICONTROL Produits]** .

1. Ouvrez l’instance Market Engage dans laquelle vous souhaitez ajouter le profil, puis cliquez sur Nouveau profil.

   ![Admin Console - instance de Marketo Engage - nouveau profil](./assets/admin-console-marketo-engage-instance-new-profile.png){width="700" zoomable="yes"}

1. Saisissez un nom de profil de produit, tel que _Utilisateur standard_.

1. Cliquez sur **Suivant**, puis sur **Enregistrer**.

## Création d’un groupe d’utilisateurs {#create-user-group}

Un groupe d’utilisateurs est un ensemble d’utilisateurs auxquels sont attribués un ensemble partagé d’autorisations. Vous pouvez ajouter ou supprimer des utilisateurs dans votre groupe d’utilisateurs. Les autorisations de groupe restent les mêmes pendant que les utilisateurs du groupe changent.

Pour plus d’informations sur l’utilisation des groupes d’utilisateurs pour gérer les autorisations, voir [Gestion des groupes d’utilisateurs](https://helpx.adobe.com/fr/enterprise/using/user-groups.html){target="_blank"} dans la documentation de l’Admin Console.

>[!NOTE]
>
>Un administrateur système Admin Console peut effectuer ces étapes.

1. Connectez-vous à [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Sélectionnez l’onglet **[!UICONTROL Utilisateurs]** .

1. Sélectionnez **[!UICONTROL Groupes d’utilisateurs]** dans le volet de navigation de gauche.

1. Cliquez sur **[!UICONTROL Nouveau groupe d’utilisateurs]** en haut à droite.

1. Saisissez un nom pour le groupe d’utilisateurs, par exemple _Utilisateurs standard_ et cliquez sur **[!UICONTROL Enregistrer]**.

1. Cliquez sur le groupe d’utilisateurs que vous venez de créer.

1. Sélectionnez l’onglet **[!UICONTROL Profils de produit attribués]** et cliquez sur **[!UICONTROL Attribuer le profil]**.

1. Cliquez sur **+** et ajoutez chaque instance des produits suivants :

   * [!UICONTROL Marketo Engage]
   * [!UICONTROL Adobe Experience Platform - AEP-Default-All-Users]
   * [!UICONTROL Collecte de données dʼAdobe Experience Platform]
   * [!UICONTROL Accès à tous les accès à la collecte de données]

   ![Admin Console - user-group - add products](./assets/admin-console-user-group-add-products.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Enregistrer]**.

## Création d’un rôle dans les autorisations AEP {#create-role}

Les autorisations sont des droits unitaires qui vous permettent de définir les autorisations affectées à un profil de produit. Chaque autorisation est regroupée sous une fonctionnalité, telle que des parcours ou des groupes d’achat, qui représente les différentes fonctionnalités ou objets dans Journey Optimizer B2B edition.

La zone _Autorisations_ de Adobe Experience Platform permet aux administrateurs de définir des rôles utilisateur et des stratégies d’accès afin de gérer les autorisations d’accès pour les fonctionnalités et les objets au sein d’une application de produit. Dans cette application, vous pouvez créer et gérer des rôles, ainsi qu’attribuer les autorisations de ressources souhaitées pour ces rôles. Les autorisations vous permettent également de gérer les libellés, les sandbox et les utilisateurs associés à un rôle spécifique.

Pour plus d’informations, voir [Gestion des autorisations pour un rôle](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions){target="_blank"} dans la documentation de l’Experience Platform.

>[!NOTE]
>
>Pour accomplir les étapes suivantes, vous devez être un administrateur de produit pour Adobe Experience Platform.

1. Accédez à [experience.adobe.com](https://experience.adobe.com/).

1. Dans le panneau _[!UICONTROL Accès rapide]_, sélectionnez **[!UICONTROL Autorisations]**.

   >[!NOTE]
   >
   >Si vous ne voyez pas _[!UICONTROL Autorisations]_, vous devrez peut-être cliquer sur **[!UICONTROL Afficher tout]** et le sélectionner dans les applications disponibles.

   ![Experience Platform - Autorisations d’accès](./assets/aep-permissions.png){width="700" zoomable="yes"}

1. Sélectionnez **[!UICONTROL Rôles]** dans le volet de navigation de gauche, puis **[!UICONTROL Créer un rôle]**.

1. Dans la boîte de dialogue _[!UICONTROL Créer un nouveau rôle]_, saisissez un nom pour le rôle, par exemple _AJO B2B_, ainsi qu’une description (facultative).

1. Cliquez sur **[!UICONTROL Confirmer]**.

1. Sélectionnez vos environnements de test.

   ![Experience Platform - ajouter des environnements de test pour le nouveau rôle](./assets/aep-permissions-role-sandboxes.png){width="700" zoomable="yes"}

1. Ajoutez les autorisations de profil :

   * Dans la liste _[!UICONTROL Resources]_ sur la gauche, recherchez l’élément **[!UICONTROL Gestion des profils]** et cliquez sur l’icône plus (**+**) pour ajouter l’attribut.

   * Pour l’attribut , ajoutez les autorisations suivantes :
      * [!UICONTROL Afficher les segments]
      * [!UICONTROL Gérer les segments]
      * [!UICONTROL Afficher les profils]
      * [!UICONTROL Gérer les profils]
      * [!UICONTROL Afficher le profil B2B]
      * [!UICONTROL Gérer le profil B2B]

   ![Experience Platform - ajouter des profils pour le nouveau rôle](./assets/aep-permissions-role-profiles.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Enregistrer]** en haut à droite.

1. Accédez aux détails du rôle et sélectionnez l’onglet **[!UICONTROL Groupes d’utilisateurs]** .

1. Cliquez sur **[!UICONTROL Ajouter des groupes]**.

   ![Experience Platform - ajouter des profils pour le nouveau rôle](./assets/aep-permissions-role-add-groups.png){width="700" zoomable="yes"}

1. Cochez la case en regard du groupe d’utilisateurs que vous avez créé précédemment dans l’Admin Console.

1. Cliquez sur **[!UICONTROL Enregistrer]**.

## Ajout d’utilisateurs au groupe dans l’Admin Console

>[!NOTE]
>
>Un administrateur système Admin Console ou un administrateur de produit peut effectuer ces étapes.

Pour plus d’informations sur la gestion des utilisateurs, voir [Utilisateurs Admin Console](https://helpx.adobe.com/fr/enterprise/using/user-groups.html) dans la documentation Admin Console.

1. Accédez à [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Sous _[!UICONTROL Liens rapides]_, cliquez sur **[!UICONTROL Ajouter des utilisateurs]**.

1. Ajoutez chaque utilisateur :

   * Saisissez l’adresse électronique, le prénom et le nom de l’utilisateur.

     ![Experience Platform - ajouter des profils pour le nouveau rôle](./assets/admin-console-add-users.png){width="600" zoomable="yes"}

   * Pour **[!UICONTROL Groupes d’utilisateurs]**, cliquez sur **+**.

   * Sélectionnez le groupe d’utilisateurs que vous avez créé précédemment.

   * Cliquez sur **[!UICONTROL Appliquer]**.

1. Cliquez sur **[!UICONTROL Enregistrer]**.
