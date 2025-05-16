---
title: Audiences correspondantes de compte LinkedIn
description: Découvrez comment connecter un compte LinkedIn et activer un flux de données pour les groupes d’achats.
feature: Integrations, Audiences, Buying Groups
role: User, Admin
exl-id: d2303529-16c4-4b0b-b8c8-404dff8ec63d
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 16%

---

# Audiences correspondantes de compte LinkedIn

Journey Optimizer B2B edition offre la possibilité de générer des audiences d’annonces LinkedIn par le biais d’audiences avec correspondance de compte. Il est conçu pour vous aider à remplir des rôles vides dans vos groupes d’achats. En définissant un ensemble de filtres de groupe d&#39;achat, vous pouvez gérer une Audience appariée LinkedIn pour cibler les prospects qui correspondent aux paramètres de votre groupe d&#39;achat. Cette fonctionnalité exploite les destinations Experience Platform pour gérer certains aspects de l’intégration. Il existe une limite de dix flux de données.

Avant de lancer un flux de données à partir de Journey Optimizer B2B edition, vous devez disposer d’au moins une instance du connecteur de destination [(Entreprises) LinkedIn Matched Audience](https://experienceleague.adobe.com/fr/docs/experience-platform/destinations/catalog/social/linkedin#connect){target="_blank"} avec un compte LinkedIn Campaign Manager configuré dans votre application Experience Platform.

## Configurer une nouvelle connexion à un compte LinkedIn {#linkedin-destination-setup}

>[!CONTEXTUALHELP]
>id="ajo-b2b_linkedin_destination_setup"
>title="Une configuration de la destination LinkedIn est requise."
>abstract="Envoyez des comptes filtrés par groupes d’achat vers une destination LinkedIn pour interagir avec les membres potentiels du groupe d’achat. Vous pouvez créer jusqu’à 10 flux de données pour 10 groupes différents de comptes filtrés. Pour commencer à utiliser cette fonctionnalité, ajoutez d’abord une destination LinkedIn."

1. Dans Experience Platform, accédez à **[!UICONTROL Connexions]** > **[!UICONTROL Destinations]** dans le volet de navigation de gauche, puis sélectionnez l’onglet **[!UICONTROL Catalogue]**.

1. Dans le catalogue, recherchez le connecteur **[!UICONTROL (Entreprises) LinkedIn Matched Audience]**.

   >[!TIP]
   >
   >Vous pouvez rapidement trouver le connecteur en saisissant `LinkedIn` dans la zone de recherche.

1. Dans la carte de connecteur, cliquez sur l’icône _Plus_ (**...**) et choisissez **[!UICONTROL Configurer une nouvelle destination]**.

   ![Accéder au connecteur d’audience correspondante LinkedIn (entreprises)](./assets/aep-destinations-catalog-linkedin.png){width="800" zoomable="yes"}

1. Sélectionnez **[!UICONTROL Nouveau compte]** puis cliquez sur **[!UICONTROL Se connecter à la destination]**.

   ![Connecter un nouveau compte LinkedIn](./assets/aep-destinations-catalog-linkedin-new-account.png){width="500"}

1. Fournissez vos identifiants LinkedIn et connectez-vous.

   Après l’authentification, le compte LinkedIn est connecté en tant que destination dans Experience Platform.

   ![La confirmation de connexion au compte s’affiche](./assets/aep-destinations-catalog-linkedin-connected.png){width="400"}

   >[!IMPORTANT]
   >
   >À ce stade, **ne saisissez pas** les _[!UICONTROL détails de la destination]_. Seule la connexion est nécessaire.

## Mettre à jour les détails du compte

Le nom et la description du compte LinkedIn sont visibles pour les groupes d’achats dans Journey Optimizer B2B edition. Il est recommandé de mettre à jour ces informations afin qu’elles soient facilement identifiables pour vos spécialistes marketing travaillant avec des groupes d’achats. Vous pouvez modifier les détails du compte dans l’interface utilisateur d’Experience Platform ou de Journey Optimizer B2B edition.

1. Accédez à **[!UICONTROL Connexions]** > **[!UICONTROL Destinations]** dans le volet de navigation de gauche, puis sélectionnez l’onglet **[!UICONTROL Comptes]**.

1. Pour le nouveau compte que vous avez créé, cliquez sur le menu _Plus_ (**...**) et choisissez **[!UICONTROL Modifier les détails]**.

   ![Modifier les détails du compte](./assets/aep-destinations-accounts-edit-details.png){width="800" zoomable="yes"}

1. Dans la boîte de dialogue, mettez à jour le nom et la description.

   ![Modifier le nom et la description](./assets/destinations-linkedin-account-edit-details-dialog.png){width="500"}

1. Cliquez sur **[!UICONTROL Enregistrer]**.

## Activer le compte pour les groupes d&#39;achats

>[!NOTE]
>
>Si vous disposez déjà de dix flux de données, vous ne pouvez pas en créer d’autres. Si vous avez atteint le maximum, supprimez-en un dans Experience Platform avant d’en créer un nouveau dans Journey Optimizer B2B edition.

1. Dans Journey Optimizer B2B Edition, accédez à **[!UICONTROL Comptes]** > **[!UICONTROL Groupes d’achat]** dans le volet de navigation de gauche.

1. Sélectionnez l’onglet **[!UICONTROL Parcourir]**.

1. Cliquez sur **[!UICONTROL Activer vers la destination LinkedIn]** en haut à droite.

   ![Modifier les détails du compte](./assets/activate-linkedin-destination.png){width="800" zoomable="yes"}

1. Attribuez un nom et une description descriptifs au flux de données (facultatif).

   Après l’avoir enregistré, le nom que vous spécifiez pour le flux de données est précédé de _AJOB2B_ pour faciliter l’identification du flux de données dans Experience Platform.

1. Saisissez l’[Identifiant de compte de votre compte LinkedIn Campaign Manager](https://www.linkedin.com/help/lms/answer/a424270).

   Votre identifiant de compte est disponible en fonction de votre nom de compte dans l’interface utilisateur de Campaign Manager.

   ![Ajouter les détails du flux de données](./assets/destinations-linkedin-activate-details.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Sélectionner des filtres de groupe d’achats]** et définissez les paramètres de l’audience de votre compte.

   >[!IMPORTANT]
   >
   >Actuellement, les filtres ne peuvent pas être modifiés une fois le flux de données activé. Vérifiez à nouveau votre travail avant d’activer le flux de données.

   ![Spécifiez le filtrage des audiences de compte en fonction des groupes d’achats](./assets/destinations-linkedin-activate-buying-group-filters.png){width="400"}

   Pour le **[!UICONTROL score d’engagement]**, l’opérateur `Between` est inclusif, tout comme les plages de pourcentage. Par exemple, les paragraphes 5.1 et 5 sont tous deux compris _entre_ 5 et 6.

   Les conditions vides sont traitées comme des `Is Any`.

   Cliquez sur **[!UICONTROL Enregistrer]** pour ajouter les filtres spécifiés.

1. Cliquez sur **[!UICONTROL Sélectionner la destination LinkedIn]** et choisissez la destination LinkedIn configurée que vous souhaitez utiliser.

   Lors de l’activation, ce paramètre crée le flux de données à l’aide de la configuration de destination et d’un segment virtuel correspondant.

1. Vérifiez deux fois vos paramètres et cliquez sur **[!UICONTROL Activer]** en haut à droite.

   Cliquez à nouveau sur **[!UICONTROL Activer]** dans la boîte de dialogue de confirmation.

   Une bannière contenant un lien vers le menu de vos flux de données dans Experience Platform s’affiche afin que vous puissiez vérifier l’enregistrement du flux de données.

## Orchestrer l’engagement des médias achetés

Vous pouvez interagir avec les membres du compte par le biais d’un canal de média payant, tel que les audiences d’annonces LinkedIn, afin de les acquérir, de les entretenir et de les qualifier pour les ventes. Utilisez un nœud _Agir_ dans un parcours de compte pour automatiser l’engagement avec les membres importants d’un compte par le biais d’un canal externe adapté aux différents membres du compte.

>[!VIDEO](https://video.tv.adobe.com/v/3448649/?learn=on)