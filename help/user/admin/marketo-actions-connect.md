---
title: Activation de Marketo Engage pour prendre en charge les actions de Parcours
description: Activez les connexions Marketo Engage pour prendre en charge les actions de parcours afin que les marketeurs puissent coordonner les campagnes entre Marketo Engage et Journey Optimizer B2B edition.
feature: Integrations, Audiences, Buying Groups
role: User, Admin
source-git-commit: de7f5620556a48fe6f12ed1c70e925e11ec770f1
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 2%

---


# Activation des instances Marketo Engage pour la prise en charge des actions

Les actions Marketo Engage sont des actions _basées sur les personnes_ qui vous permettent de coordonner votre orchestration marketing _basée sur les comptes_ entre Journey Optimizer B2B edition et vos efforts marketing _basés sur les prospects_ dans Marketo Engage. Utilisez ces actions pour orchestrer l’appartenance à une liste statique et pour placer des personnes dans des campagnes.

Pour utiliser les actions Marketo Engage, un administrateur doit d’abord créer un [service personnalisé](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/custom-services#) dans Marketo Engage, qui fournit les informations d’identification nécessaires à l’authentification.
Ensuite, un administrateur de produit pour Journey Optimizer B2B edition crée une connexion à Marketo Engage en saisissant les informations d’identification.
Les utilisateurs de Journey Optimizer B2B edition peuvent ensuite référencer la connexion pour configurer des actions Marketo Engage dans des parcours de compte <!-- Person and -->, tels que l’ajout ou la suppression de personnes des listes Marketo Engage ou leur ajout à des campagnes de demandes.

La visibilité de l’espace de travail Marketo Engage pour les ressources, telles que les listes et les campagnes, est régie par les autorisations de rôle attribuées dans le service personnalisé.

Une même connexion peut être utilisée plusieurs fois au sein d’un parcours et différentes connexions Marketo Engage peuvent coexister dans un seul parcours.

Lorsqu’une action s’exécute, elle utilise la stratégie de sélection pour déterminer quels enregistrements de personne dans Marketo Engage doivent être sélectionnés s’il existe plusieurs identifiants dans le profil de personne unifié. Les options incluent le choix des enregistrements Marketo Engage les plus anciens, les plus récents ou tous ceux correspondants. Les utilisateurs passent par le parcours indépendamment de la correspondance, sauf en cas d’erreur.

## Configurer une connexion Marketo Engage

Configurez une instance Marketo Engage distante à utiliser avec les actions de parcours Marketo Engage.

### Création du service personnalisé Marketo Engage

1. Connectez-vous à Marketo Engage en tant qu’administrateur et créez un service personnalisé.
1. Enregistrez les valeurs suivantes à utiliser pour la connexion :

   * ID Munchkin
   * Identifiant client
   * Secret client

### Ajouter l’intégration

![Ajouter des détails d’intégration](assets/integration-connection-details.png)

1. Dans Journey Optimizer B2B edition, accédez à **Administration** > **Configurations**.
1. Sélectionnez dans l’onglet **Intégrations**.
1. Cliquez sur **[!UICONTROL Créer une connexion]**.
1. Saisissez un nom (obligatoire) et une description (facultatif).
1. Sélectionnez une **Stratégie de sélection** pour les enregistrements de personne correspondants.
1. Saisissez votre identifiant Munchkin, votre identifiant client et votre secret client.
1. Cliquez sur **[!UICONTROL Connexion à Marketo]**.
1. Cliquez sur **[!UICONTROL Créer]**.

Lorsqu’un spécialiste marketing utilise une action Marketo Engage dans un parcours, il peut configurer le nœud à l’aide du nom de la connexion.

Une fois l’intégration terminée, les actions Marketo Engage sont disponibles à partir de l’**Actions sur** dans les propriétés de nœud.

![Liste des actions Marketo](assets/marketo-actions-list.png)