---
title: Gestion des utilisateurs
description: Découvrez comment affecter des membres de l’équipe aux profils de produit de Journey Optimizer B2B Edition.
feature: Setup
roles: Admin
source-git-commit: dcd8ab2820d60654e8970944054142fc296ed54f
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 1%

---

# Gestion des utilisateurs

Une fois la mise en service terminée et les environnements de test liés, procédez comme suit pour fournir à votre équipe et à vos utilisateurs l’accès à Adobe Journey Optimizer B2B Edition.

1. [Créez un profil de produit Marketo Engage](#marketo-engage-profile) dans l’Admin Console (nouvelle instance de Marketo Engage uniquement).
1. [Créez un groupe d’utilisateurs](#create-user-group) dans l’Admin Console.
1. [Créez un rôle](#create-role) dans les autorisations AEP.
1. [Ajoutez des utilisateurs](#add-users) dans l’Admin Console.

En tant qu’administrateur, vous pouvez effectuer ces tâches dans Adobe Admin Console, qui constitue un emplacement central pour administrer et gérer vos licences de produit et utilisateurs Adobes. Dans l’Admin Console, vous pouvez créer et gérer des utilisateurs à un seul emplacement au lieu de dans vos différentes solutions individuelles. Pour en savoir plus sur ses fonctions et fonctionnalités, consultez la page [Aperçu de l’Admin Console](https://helpx.adobe.com/fr/enterprise/using/admin-console.html) .

## Accès à l’Admin Console

Avant de pouvoir utiliser l’Admin Console pour administrer les utilisateurs au sein de votre équipe, vous devez vous assurer que vous pouvez accéder à l’Admin Console et disposer des autorisations appropriées.

1. En tant qu’administrateur système, vous devriez recevoir plusieurs courriers électroniques d’Adobe dans le cadre du processus d’intégration.

   Recherchez l’e-mail de bienvenue qui fournit des informations sur le nom de l’organisation auquel vous avez accès.

1. Cliquez sur le lien **[!UICONTROL Commencer]** de votre e-mail de bienvenue pour accéder à l’Admin Console.

   Si vous ne trouvez pas l’email, ouvrez un navigateur directement sur l’Admin Console à l’adresse [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Connectez-vous à l’aide de votre Adobe ID.

   Une fois la connexion établie, la page Aperçu de Adobe Admin Console s’affiche.

1. Si vous avez accès à plusieurs organisations, vérifiez que vous vous êtes connecté à la bonne organisation.

   Pour modifier votre organisation, cliquez sur le nom de l’organisation dans le coin supérieur droit et sélectionnez l’organisation à laquelle vous avez besoin d’accéder.

1. Sélectionnez Administrateurs dans la carte Utilisateurs pour vérifier que vous êtes un administrateur système.

1. Effectuez une recherche en saisissant votre adresse électronique, votre nom d’utilisateur, votre prénom ou votre nom Adobe ID.

   * Si votre accès est correctement configuré, la recherche renvoie votre enregistrement.

   * Si la valeur de la colonne **[!UICONTROL ADMIN ROLE]** indique `System`, vous savez que vous (ou l’utilisateur affiché) êtes un administrateur système.

## Création du profil de produit du Marketo Engage {#marketo-engage-profile}

Lorsque vous accordez aux utilisateurs l’accès à une solution d’Adobe, vous ne souhaitez pas nécessairement leur accorder un accès complet. Les profils de produit permettent à chaque solution d’avoir son propre jeu d’autorisations utilisateur. Utilisez l’Admin Console pour attribuer des profils de produit.

>[!NOTE]
>
>Ces étapes ne peuvent être effectuées que par un administrateur système Admin Console ou un administrateur de produit Marketo Engage.

1. Connectez-vous à [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Choisissez Produits > Marketo Engage.

1. Cliquez sur Nouveau profil et saisissez un nom de profil de produit, par exemple _Utilisateur standard_.

1. Cliquez sur Suivant > Enregistrer

## Création d’un groupe d’utilisateurs {#create-user-group}

Un groupe d’utilisateurs est un ensemble d’utilisateurs auxquels sont attribués un ensemble partagé d’autorisations. Vous pouvez ajouter ou supprimer des utilisateurs dans votre groupe d’utilisateurs. Les autorisations de groupe restent les mêmes pendant que les utilisateurs du groupe changent.

>[!NOTE]
>
>Ces étapes ne peuvent être effectuées que par un administrateur système Admin Console.

1. Connectez-vous à [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Sélectionnez **[!UICONTROL Utilisateurs]** > **[!UICONTROL Groupes d’utilisateurs]** > **[!UICONTROL Nouveau groupe d’utilisateurs]**.

1. Saisissez un nom pour le groupe d’utilisateurs, par exemple _Utilisateurs standard_ et cliquez sur **[!UICONTROL Enregistrer]**.

1. Cliquez sur le groupe d’utilisateurs que vous venez de créer.

1. Cliquez sur **[!UICONTROL Attribuer des profils de produit]** > **[!UICONTROL Attribuer un profil]**.

1. Sélectionnez les produits suivants :
   * [!UICONTROL Marketo Engage - Utilisateur standard]
   * [!UICONTROL Adobe Experience Platform - AEP-Default-All-Users]
   * [!UICONTROL Collecte de données Adobe Experience Platform - Par défaut]
   * [!UICONTROL Accès à tous les accès à la collecte de données]

1. Cliquez sur **[!UICONTROL Enregistrer]**.

## Création d’un rôle dans les autorisations AEP {#create-role}

Les autorisations sont des droits unitaires qui vous permettent de définir les autorisations affectées à un profil de produit. Chaque autorisation est regroupée sous une fonctionnalité, telle que des parcours ou des groupes d’achat, qui représente les différentes fonctionnalités ou objets de Journey Optimizer B2B Edition.

_Autorisations_ est la zone de Adobe Experience Platform dans laquelle les administrateurs peuvent définir des rôles utilisateur et des stratégies d’accès pour gérer les autorisations d’accès aux fonctionnalités et aux objets dans une application de produit. Dans cette application, vous pouvez créer et gérer des rôles, ainsi qu’attribuer les autorisations de ressources souhaitées pour ces rôles. Les autorisations vous permettent également de gérer les libellés, les environnements de test et les utilisateurs associés à un rôle spécifique.

>[!NOTE]
>
>Pour accomplir les étapes suivantes, vous devez être un administrateur de produit pour Adobe Experience Platform.

1. Accédez à [experience.adobe.com](https://experience.adobe.com/).

1. Sélectionnez **[!UICONTROL Permissions]**.

   >[!NOTE]
   >
   >Si vous ne voyez pas les autorisations, vous devrez peut-être cliquer sur Afficher tout et le sélectionner dans les applications disponibles.

1. Sélectionnez **[!UICONTROL Rôles]** dans le volet de navigation de gauche, puis **[!UICONTROL Créer un rôle]**.

1. Dans la boîte de dialogue _[!UICONTROL Créer un nouveau rôle]_, saisissez un nom pour le rôle, par exemple _Utilisateur standard_, ainsi qu’une description (facultatif).

1. Cliquez sur **[!UICONTROL Confirmer]**.

1. Sélectionnez vos environnements de test.

1. Ajoutez les autorisations de profil :

   * Dans la liste _[!UICONTROL Resources]_ sur la gauche, recherchez l’élément **[!UICONTROL Gestion des profils]** et cliquez sur l’icône plus (**+**) pour ajouter l’attribut.

   * Pour l’attribut , ajoutez les autorisations suivantes :
      * [!UICONTROL Afficher les segments]
      * [!UICONTROL Gérer les segments]
      * [!UICONTROL Afficher les profils]
      * [!UICONTROL Gérer les profils]
      * [!UICONTROL Afficher le profil B2B]
      * [!UICONTROL Gérer le profil B2B]

1. Cliquez sur **[!UICONTROL Enregistrer]** en haut à droite.

1. Sélectionnez **[!UICONTROL Groupes d’utilisateurs]** > **[!UICONTROL Ajouter des groupes]**.

1. Cochez la case en regard du groupe d’utilisateurs que vous avez créé précédemment dans l’Admin Console.

1. Cliquez sur **[!UICONTROL Enregistrer]**.

## Ajout d’utilisateurs dans l’Admin Console

>[!NOTE]
>
>Ces étapes ne peuvent être effectuées que par un administrateur système Admin Console ou un administrateur de produit.

1. Accédez à [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Cliquez sur **[!UICONTROL Ajouter des utilisateurs]**.

1. Ajoutez chaque utilisateur :

   * Saisissez l’adresse électronique, le prénom et le nom de l’utilisateur.
   * Cliquez sur [!UICONTROL Groupes d’utilisateurs].
   * Sélectionnez le groupe d’utilisateurs que vous avez créé précédemment.

1. Cliquez sur **[!UICONTROL Apply]**.

1. Cliquez sur **[!UICONTROL Enregistrer]**.
