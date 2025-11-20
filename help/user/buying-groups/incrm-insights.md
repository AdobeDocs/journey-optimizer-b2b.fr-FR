---
title: Insights In-CRM
description: Accédez aux groupes d’achat Journey Optimizer B2B edition directement dans Salesforce. Les membres de l’équipe des ventes peuvent afficher les données d’engagement et identifier les opportunités de vente avec des informations In-CRM.
feature: Sales Insights, Buying Groups
role: User
source-git-commit: de7f5620556a48fe6f12ed1c70e925e11ec770f1
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---


# Insights In-CRM

La fonction Insights dans le CRM est une application web qui s’intègre à Salesforce, ce qui vous permet d’accéder à vos groupes d’achats Journey Optimizer B2B edition directement dans Salesforce. Il vous permet d’identifier les opportunités d’engagement et de potentiel de vente accru.

L’application Insights dans le CRM est disponible dans le package Insights de vente Marketo [&#128279;](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/marketo-sales-insight/msi-for-salesforce/installation/install-marketo-sales-insight-package-in-salesforce-appexchange).

## Autorisations

Pour accéder à l’application, les utilisateurs doivent être membres d’un rôle avec l’autorisation **Informations sur les ventes:View Informations sur les ventes** .

Si vous souhaitez restreindre un groupe d’utilisateurs à InCRM-Insights, suivez les instructions suivantes pour créer un rôle personnalisé spécifique à InCRM-Insights :

* Créez un rôle personnalisé avec uniquement le jeu d’autorisations **Informations sur les ventes:View Informations sur les ventes**.
* Créez un groupe d’utilisateurs, sans ajouter de profils de produit.
* Créez un autre groupe d’utilisateurs et ajoutez un profil de produit AEP, ou ajoutez un profil AEP existant au groupe d’utilisateurs que vous venez de créer.
* Affectez les nouveaux groupes d’utilisateurs au nouveau rôle et ajoutez de nouveaux utilisateurs aux nouveaux groupes d’utilisateurs.

## Utilisation des informations dans le CRM

L’application Insights dans le CRM est disponible dans Salesforce via le lanceur d’applications.

1. Cliquez sur le lanceur d’application dans Salesforce.
1. Sélectionnez ou recherchez des `Journey Optimizer B2B Edition`.
1. Dans l’onglet affiché, connectez-vous avec vos identifiants Adobe.
1. Choisissez un sandbox qui héberge vos Parcours de compte.

Vos groupes d&#39;achats sont chargés et disponibles. Les données sont en lecture seule via les informations In-CRM.

>[!NOTE]
>
>L’appartenance au rôle de produit [Utilisateur commercial B2B](../admin/user-management.md#b2b-built-in-roles) est requise pour accéder aux informations In-CRM.

Après avoir sélectionné un groupe d’achats, vous pouvez parcourir les [&#x200B; détails du groupe](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/accounts/sales-experience/buying-group-details#) comme dans Journey Optimizer B2B edition.
