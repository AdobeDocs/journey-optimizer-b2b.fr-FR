---
title: Insights In-CRM
description: Accédez aux groupes d’achat Journey Optimizer B2B edition directement dans les CRM. Les membres de l’équipe des ventes peuvent afficher les données d’engagement et identifier les opportunités de vente avec des informations In-CRM.
feature: Sales Insights, Buying Groups
role: User
source-git-commit: 2eb5b6226730a1948b480a9dee0c6f2786e01cc5
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 1%

---


# Insights In-CRM

[!DNL In-CRM Insights] est une application web qui s’intègre à Salesforce et Microsoft Dynamics 365, ce qui vous permet d’accéder à des groupes d’achat [!DNL Journey Optimizer B2B Edition] directement dans votre CRM. Il rassemble des sources de données de vente, ce qui facilite l’identification des opportunités d’engagement et de potentiel de vente accrus.

## Installation

Le processus d’installation comprend les étapes suivantes :

* Configuration des autorisations utilisateur et des groupes
* Installation du package logiciel
* Connexion via votre CRM

### Définition des autorisations

Les utilisateurs et utilisatrices installant le logiciel doivent disposer des autorisations nécessaires pour installer les packages Salesforce.

Pour accéder à l’application, les utilisateurs doivent être membres d’un rôle avec l’autorisation **Informations sur les ventes:View Informations sur les ventes**.

Si vous souhaitez limiter les utilisateurs et utilisatrices à l’[!DNL In-CRM Insights] :

1. Créez un [rôle personnalisé](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/accounts/buying-groups/default-custom-roles#create-a-custom-role) et attribuez-lui l’autorisation **Informations sur les ventes : Afficher les informations sur les ventes**.
1. Créez un [groupe d’utilisateurs](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management#create-user-group).
1. Ajoutez un profil de produit Experience Platform au groupe .

### Installation du package

Pour installer le package Insights dans le CRM, suivez les étapes pour Salesforce ou Microsoft Dynamics.

#### Salesforce

1. Téléchargez le [package du programme d’installation des insights dans CRM](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=salesforce).
1. Une fois connecté, vous êtes redirigé vers la page d’installation du package.
1. Sélectionnez l’option **[!UICONTROL Installer pour tous les utilisateurs]** et cliquez sur **[!UICONTROL Installer]**.

   ![Installation du package Insights In-CRM](assets/incrm-install-sf.png){width=500}

1. Approuvez l’accès tiers dans la boîte de dialogue, puis cliquez sur **[!UICONTROL Continuer]**.
1. Une fois l’installation terminée, cliquez sur **[!UICONTROL Terminé]**.

   Il est désormais répertorié sur la page **Packages installés** et **Journey Optimizer B2B edition** est répertorié dans le lanceur d’application.

   ![Informations dans le CRM configurées dans Salesforce](assets/in-crm-install-sf-done.png){width=800 zoomable="yes"}

#### MS Dynamics

1. Téléchargez le [package du programme d’installation des insights dans CRM](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=dynamics).
1. Accédez au portail [Power Apps](https://make.powerapps.com/){target=_blank}.
1. Une fois connecté, sélectionnez l’environnement du package, puis accédez à **[!UICONTROL Solutions]** dans le menu de gauche.
1. Cliquez sur **[!UICONTROL Importer la solution]**.
1. Recherchez et chargez le package du programme d’installation, puis cliquez sur **[!UICONTROL Suivant]**.
1. Vérifiez les détails du package et cliquez sur **[!UICONTROL Suivant]**.
1. Sous _Variables d’environnement_, vérifiez que la valeur est définie sur `prod` (ne modifiez pas la valeur), puis cliquez sur **[!UICONTROL Importer]**.
1. Une fois l’installation terminée, **[!UICONTROL Journey Optimizer B2B edition]** > **[!UICONTROL Groupes d’achats]** s’affiche sur la barre de navigation de gauche.

   ![Insights in-CRM disponibles dans Microsoft Dynamics](assets/incrm-ms-install-done.png){width=800 zoomable="yes"}

## Afficher vos groupes d&#39;achats

Suivez les invites pour vous connecter à votre compte Adobe. Vos groupes d&#39;achats sont chargés et peuvent être consultés.

Après avoir sélectionné un groupe d&#39;achats, vous pouvez parcourir les [détails du groupe](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/accounts/sales-experience/buying-group-details#). Il s’agit du même que les données et les informations affichées dans Journey Optimizer B2B edition, mais les données sont en lecture seule via [!DNL In-CRM Insights].
