---
title: Activation de Marketo Engage pour prendre en charge les actions de Parcours
description: Activez les connexions Marketo Engage pour prendre en charge les actions de parcours afin que les marketeurs puissent coordonner les campagnes entre Marketo Engage et Journey Optimizer B2B edition.
feature: Integrations, Audiences, Buying Groups
role: User, Admin
source-git-commit: 9b77570ddb9b416251f38db51a57507a935a526a
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 1%

---


# Activation des instances Marketo Engage pour la prise en charge des actions

Les actions Marketo Engage sont des actions _basées sur les personnes_ qui vous permettent de coordonner votre orchestration marketing _basée sur les comptes_ entre Journey Optimizer B2B edition et vos efforts marketing _basés sur les prospects_ dans Marketo Engage. Utilisez ces actions pour orchestrer l’appartenance à une liste statique et pour placer des personnes dans des campagnes.

Pour utiliser les actions de parcours Marketo Engage, un administrateur doit d’abord créer un [service personnalisé](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/custom-services){target="_blank"} dans Marketo Engage, qui fournit les informations d’identification nécessaires à l’authentification. Ensuite, un administrateur de produit pour Journey Optimizer B2B edition utilise les informations d’identification pour créer une connexion à Marketo Engage. Les utilisateurs de Journey Optimizer B2B edition peuvent ensuite référencer la connexion pour configurer des actions Marketo Engage dans des parcours de compte <!-- person and -->, tels que l’ajout ou la suppression de personnes des listes Marketo Engage ou leur ajout à des campagnes de demandes.

## Configurer une connexion Marketo Engage {#external-marketo-configure}

>[!CONTEXTUALHELP]
>id="ajo-b2b_marketo-configure-connections"
>title="Connexions Marketo Engage externes"
>abstract="Les administrateurs de produit peuvent configurer des connexions à des instances Marketo Engage externes, ce qui les rend disponibles pour des actions de parcours."

Effectuez les tâches suivantes pour configurer une instance Marketo Engage externe à utiliser avec des actions de parcours.

### Création du service personnalisé Marketo Engage

1. Connectez-vous à Marketo Engage en tant qu’administrateur et [créez un service personnalisé](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/create-a-custom-service-for-use-with-rest-api){target="_blank"}.
1. Copiez les valeurs suivantes à utiliser pour la connexion Journey Optimizer B2B edition :

   * ID Munchkin
   * Identifiant client
   * Secret client

La visibilité de l’espace de travail Marketo Engage pour les ressources, telles que les listes et les campagnes, est régie par les [autorisations de rôle attribuées dans le service personnalisé](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/custom-services#permission-list){target="_blank"}. Les marketeurs peuvent utiliser la même connexion plusieurs fois au sein d’un parcours et utiliser différentes connexions Marketo Engage dans le même parcours.

### Ajouter l’intégration

![Ajouter des détails d’intégration](assets/integration-connection-details.png){width="800" zoomable="yes"}

1. Dans Journey Optimizer B2B edition, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Configurations]**.
1. Sélectionnez dans l’onglet **[!UICONTROL Intégrations]**.
1. Cliquez sur **[!UICONTROL Créer une connexion]**.
1. Saisissez un **[!UICONTROL Nom]** (obligatoire) et un **[!UICONTROL Description]** (facultatif).
1. Sélectionnez la politique de mise à jour utilisée pour appliquer une action à un enregistrement de personne correspondant.

   Lorsqu’une action s’exécute pour l’instance Marketo Engage connectée, la _politique de mise à jour_ sélectionnée détermine les enregistrements de personne dans Marketo Engage pour déterminer s’il existe plusieurs identifiants dans le profil de personne unifié.

   * **[!UICONTROL Mettre à jour tous les enregistrements correspondants]**
   * **[!UICONTROL Mettre à jour uniquement le plus ancien enregistrement correspondant]**
   * **[!UICONTROL Mettre à jour uniquement le dernier enregistrement correspondant]**

   >[!NOTE]
   >
   >Les utilisateurs passent par le parcours indépendamment de la correspondance, sauf en cas d’erreur.

1. Saisissez l’ID Munchkin, l’ID client et le secret client pour le service créé dans l’instance Marketo Engage externe.
1. Cliquez sur **[!UICONTROL Connexion à Marketo]**.
1. Cliquez sur **[!UICONTROL Créer]**.

## Utiliser la connexion dans une action de parcours

Lorsqu’un spécialiste marketing utilise une action Marketo Engage dans un parcours, il peut configurer le nœud à l’aide du nom de la connexion.

Une fois l’intégration terminée, les actions Marketo Engage sont disponibles à partir de l’**Actions sur** dans les propriétés de nœud.

![Liste des actions Marketo](assets/marketo-actions-list.png){width="800" zoomable="yes"}