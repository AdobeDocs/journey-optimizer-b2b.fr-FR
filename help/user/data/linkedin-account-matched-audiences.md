---
title: Audiences mises en correspondance de comptes linkedIn
description: Découvrez comment connecter un compte LinkedIn et activer un flux de données pour acheter des groupes.
source-git-commit: aa286aa7b0dbead59b3cec3b6c21ee3f332ad814
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 8%

---

# Audiences mises en correspondance de comptes linkedIn

L’édition B2B de Journey Optimizer permet de générer des audiences de publicité LinkedIn par le biais d’audiences mappées sur le compte. Elle est conçue pour vous aider à remplir des rôles vides dans vos groupes d’achats. En définissant un ensemble de filtres de groupe d’achats, vous pouvez gérer une audience mise en correspondance LinkedIn pour cibler les prospects qui correspondent aux paramètres de votre groupe d’achats. Cette fonctionnalité exploite les destinations Experience Platform pour gérer certains aspects de l’intégration. Il existe une limite de dix flux de données.

Avant de lancer un flux de données à partir de Journey Optimizer B2B Edition, vous devez avoir au moins une instance du [(Entreprises) connecteur de destination d’audience mappée LinkedIn](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/social/linkedin#connect) avec un compte LinkedIn Campaign Manager configuré dans votre application Experience Platform.

## Configurer une nouvelle connexion à un compte LinkedIn {#linkedin-destination-setup}

>[!CONTEXTUALHELP]
>id="ajo-b2b_linkedin_destination_setup"
>title="Une configuration de la destination LinkedIn est requise."
>abstract="Envoyez des comptes filtrés par groupes d’achat vers une destination LinkedIn pour interagir avec les membres potentiels du groupe d’achat. Vous pouvez créer jusqu’à 10 flux de données pour 10 groupes différents de comptes filtrés. Pour commencer à utiliser cette fonctionnalité, ajoutez d’abord une destination LinkedIn."

1. Dans Experience Platform, accédez à **[!UICONTROL Connexions]** > **[!UICONTROL Destinations]** dans le volet de navigation de gauche et sélectionnez l’onglet **[!UICONTROL Catalogue]** .

1. Dans le catalogue, recherchez le connecteur **[!UICONTROL (Entreprises) Audience mappée LinkedIn]** .

   >[!TIP]
   >
   >Vous pouvez rapidement trouver le connecteur en entrant `LinkedIn` dans la zone de recherche.

1. Dans la carte du connecteur, cliquez sur l&#39;icône _Plus_ (**...**) et sélectionnez **[!UICONTROL Configurer une nouvelle destination]**.

   ![Accès au connecteur d’audience mappée LinkedIn (entreprises)](./assets/aep-destinations-catalog-linkedin.png){width="800" zoomable="yes"}

1. Sélectionnez **[!UICONTROL Nouveau compte]** et cliquez sur **[!UICONTROL Se connecter à la destination]**.

   ![Connecter un nouveau compte LinkedIn](./assets/aep-destinations-catalog-linkedin-new-account.png){width="500"}

1. Indiquez vos informations d’identification LinkedIn et connectez-vous.

   Après l’authentification, le compte LinkedIn est connecté en tant que destination dans Experience Platform.

   ![ La confirmation de connexion au compte s&#39;affiche](./assets/aep-destinations-catalog-linkedin-connected.png){width="400"}

   >[!IMPORTANT]
   >
   >À ce stade, **ne saisissez pas** dans les _[!UICONTROL détails de la destination]_. Seule la connexion est nécessaire.

## Mise à jour des détails du compte

Le nom et la description du compte LinkedIn sont visibles pour les groupes d’achat dans Journey Optimizer B2B Edition. Il est recommandé de mettre à jour ces informations afin qu’elles soient facilement identifiables pour les marketeurs qui travaillent avec des groupes d’achats. Vous pouvez modifier les détails du compte dans l’interface utilisateur de l’Experience Platform ou de Journey Optimizer B2B Edition.

1. Accédez à **[!UICONTROL Connexions]** > **[!UICONTROL Destinations]** dans le volet de navigation de gauche et sélectionnez l’onglet **[!UICONTROL Comptes]** .

1. Pour le nouveau compte que vous avez créé, cliquez sur le menu _Plus_ (**...**) et sélectionnez **[!UICONTROL Modifier les détails]**.

   ![Modifier les détails du compte](./assets/aep-destinations-accounts-edit-details.png){width="800" zoomable="yes"}

1. Dans la boîte de dialogue, mettez à jour le nom et la description.

   ![Modifier le nom et la description](./assets/destinations-linkedin-account-edit-details-dialog.png){width="500"}

1. Cliquez sur **[!UICONTROL Enregistrer]**.

## Activation du compte pour les groupes d’achat

>[!NOTE]
>
>Si vous disposez déjà de dix flux de données, vous ne pouvez pas en créer un autre. Si vous ne pouvez pas le faire, supprimez-en un en Experience Platform avant d’en créer un dans Journey Optimizer B2B Edition.

1. Dans Journey Optimizer B2B Edition, accédez à **[!UICONTROL Comptes]** > **[!UICONTROL Groupes d’achats]** dans le volet de navigation de gauche.

1. Sélectionnez l&#39;onglet **[!UICONTROL Parcourir]** .

1. Cliquez sur **[!UICONTROL Activer la destination LinkedIn]** en haut à droite.

   ![Modifier les détails du compte](./assets/activate-linkedin-destination.png){width="800" zoomable="yes"}

1. Attribuez au flux de données un nom et une description descriptifs (facultatif).

   Après l’avoir enregistré, le nom que vous spécifiez pour le flux de données est précédé de _AJOB2B_ pour faciliter l’identification du flux de données dans Experience Platform.

1. Saisissez l’ [ ID de compte de votre compte LinkedIn Campaign Manager](https://www.linkedin.com/help/lms/answer/a424270).

   Vous pouvez trouver votre ID de compte en fonction du nom de votre compte dans l’interface utilisateur du gestionnaire de campagnes.

   ![Ajouter les détails du flux de données](./assets/destinations-linkedin-activate-details.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Sélectionner les filtres de groupe d&#39;achat]** et définissez les paramètres de l&#39;audience de votre compte.

   >[!IMPORTANT]
   >
   >Actuellement, les filtres ne peuvent pas être modifiés une fois le flux de données activé. Vérifiez deux fois votre travail avant d’activer le flux de données.

   ![Spécifiez le filtrage de l’audience du compte en fonction des groupes d’achat](./assets/destinations-linkedin-activate-buying-group-filters.png){width="400"}

   Pour le **[!UICONTROL score d&#39;engagement]**, l&#39;opérateur `Between` est inclusif, tout comme les plages de pourcentages. Par exemple, 5.1 et 5 sont tous deux _compris entre_ 5 et 6.

   Les conditions vides sont traitées comme `Is Any`.

   Cliquez sur **[!UICONTROL Enregistrer]** pour ajouter les filtres spécifiés.

1. Cliquez sur **[!UICONTROL Sélectionner la destination LinkedIn]** et sélectionnez la destination LinkedIn configurée que vous souhaitez utiliser.

   Lors de l’activation, ce paramètre crée le flux de données à l’aide de la configuration de destination et d’un segment virtuel correspondant.

1. Vérifiez deux fois vos paramètres et cliquez sur **[!UICONTROL Activer]** en haut à droite.

   Cliquez de nouveau sur **[!UICONTROL Activer]** dans la boîte de dialogue de confirmation.

   Une bannière s’affiche avec un lien vers le menu de flux de données dans Experience Platform afin que vous puissiez vérifier l’enregistrement du flux de données.
