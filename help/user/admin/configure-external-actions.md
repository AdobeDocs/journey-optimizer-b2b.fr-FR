---
title: Configuration des actions externes
description: Découvrez comment les développeurs, les administrateurs et les spécialistes du marketing travaillent ensemble pour implémenter, configurer et utiliser des actions externes qui connectent Journey Optimizer B2B edition à des services externes dans les parcours de compte.
feature: Setup, Integrations
role: Admin, Developer
source-git-commit: 6d3967babc1bc868fde0c76ac9068e63156070cd
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 1%

---

# Configuration des actions externes

Les actions externes permettent aux parcours de compte dans Journey Optimizer B2B edition de se connecter à des systèmes externes directement à partir de la zone de travail de parcours. Lorsqu’une audience de compte atteint un nœud d’action externe, le système effectue un appel sortant asynchrone vers un service externe configuré, en transmettant les données d’attribut d’audience pour les comptes, les personnes ou les deux. Le service externe traite les données et répond à l’aide d’un rappel , renvoyant les données et métadonnées de l’audience qui peuvent être utilisées pour guider l’exécution du parcours.

Cette fonctionnalité prend en charge deux types de nœuds de parcours :

* **Action externe** - Appelle un service externe et continue le long d’un seul chemin sortant. Idéal pour les intégrations _à déclenchement et à oubli_ telles que la mise à jour d’un enregistrement CRM ou le déclenchement d’une notification en aval.
* **Chemins de partage externes** - Appelle un service externe et évalue la réponse pour acheminer les comptes le long de l’un des chemins définis.

>[!NOTE]
>
>Les services d’action externe sont pris en charge uniquement pour les parcours de compte. Ces types de nœuds ne sont pas disponibles pour les parcours de personnes.

## Présentation de l’implémentation

La configuration des actions externes nécessite une coordination entre trois rôles successifs :

| | Rôle | Tâche |
| ---- | ---- | ---- |
| 1 | Développeur | [Implémenter et publier le service externe](#implement-service) |
| 2 | Administrateur | [Configurer l’action dans Journey Optimizer B2B edition](#configure-action) |
| 3 | Spécialiste marketing | [Ajouter un nœud externe à un parcours de compte](#add-journey-node) |

## Implémenter le service externe {#implement-service}

Le développeur doit créer et publier un service web public conforme à l&#39;interface du fournisseur de services d&#39;actions externes de Adobe Journey Optimizer B2B edition [&#128279;](https://developer.adobe.com/journey-optimizer-b2b-apis/).

>[!NOTE]
>
>La fonction de rappel nécessite un jeton porteur. Récupérez-le en configurant les informations d’identification de serveur à serveur [OAuth) dans Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation) pour votre organisation IMS.

Une fois le service actif, fournissez l’URL de la spécification OpenAPI et les informations d’authentification à l’administrateur de produit chargé de configurer l’action.

## Configurer l’action {#configure-action}

Une action doit être configurée et activée avant que les marketeurs puissent l&#39;utiliser dans un parcours. Les actions sont créées à l’état _Brouillon_ et vos modifications sont enregistrées automatiquement. Il reste en tant que brouillon jusqu’à ce que vous l’activiez.

>[!PREREQUISITES]
>
>Obtenez l’URL vers la spécification OpenAPI et les informations d’authentification du développeur avant d’ajouter la configuration.
>
>Pour définir et activer une action externe, vous devez disposer de l’autorisation _[!UICONTROL Gérer les configurations d’administration B2B]_ [produit](./user-management.md#b2b-product-permissions).

1. Accédez à **[!UICONTROL Administration]** > **[!UICONTROL Configurations]**.

1. Cliquez sur **[!UICONTROL Actions externes]** dans le panneau intermédiaire.

   ![Accéder à l&#39;espace de configuration des Actions externes](./assets/configuration-external-actions-list.png){width="800" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Créer une action]** en haut à droite.

1. Saisissez l’URL de la spécification OpenAPI pour votre service externe et cliquez sur **[!UICONTROL Créer]**.

   ![Saisir l’URL du service](./assets/configuration-external-actions-create-url.png){width="500"}

   >[!NOTE]
   >
   >Votre service externe doit être actif et accessible pour que cette étape réussisse.

1. Une fois l’URL résolue, passez en revue les **[!UICONTROL Détails du service]**.

   Les détails du service sont lus directement à partir de la spécification OpenAPI lors de la création de l’action. Vous ne pouvez pas modifier ces propriétés dans la configuration après leur création.

   | Propriété | Description | Propriété de spécification OpenAPI |
   | -------- | ----------- | --------------------- |
   | [!UICONTROL Nom] | Nom de l’action | `info.title` |
   | [!UICONTROL Description] | Description de l’action | `info.description` |
   | [!UICONTROL URL] | URL vers la spécification OpenAPI qui définit le service externe | `servers.url` |

1. Saisissez les informations d’identification **[!UICONTROL Authentification]** pour le service externe (`components.securitySchemes`).

   >[!NOTE]
   >
   >Les champs d’identification affichés dépendent du mécanisme d’authentification défini dans le service externe. Les types pris en charge sont les suivants : clé API, OAuth2 et authentification de base HTTP.

   ![Ajoutez les informations d’authentification](./assets/configuration-external-actions-auth-credentials.png){width="600" zoomable="yes"}

   Vous pouvez modifier les informations d’identification selon vos besoins lorsque l’action configurée a le statut _Brouillon_ ou _Actif_.

1. Cliquez sur **[!UICONTROL Suivant]**.

1. Définissez les propriétés **[!UICONTROL Configurations]** pour définir la manière dont l’action échange des données avec le service externe.

   >[!NOTE]
   >
   >Les propriétés marquées comme _Statiques_ ne peuvent pas être mises à jour au moment de la configuration et sont basées sur la définition de service.

   * **[!UICONTROL Type d’action]** (_statique_) - Le type de nœud de parcours pris en charge :

      * [!UICONTROL Action externe] (`enableSplitPath` = false)
      * [!UICONTROL Chemin de partage de l’action externe] (`enableSplitPath` = true)

     Vous ne pouvez pas modifier le type d’action après avoir créé la configuration d’action.

   * **[!UICONTROL Accessoires]** (_Statique_) - (Chemin de division d’action externe uniquement) Les variables renvoyées par le service externe pour être disponibles en tant que conditions de chemin dans un nœud de chemin de division externe. (`invocationPayloadDef.accessorsMetadata`)

   * **[!UICONTROL Contexte du Parcours]** (_Statique_) - Portée des données d’audience envoyées dans la requête (`supportedEntityType`) :

      * [!UICONTROL Compte] - Envoie uniquement les comptes

      * [!UICONTROL Personnes] - Envoie uniquement des personnes

      * [!UICONTROL Personnes sur le compte] - Envoie les comptes et les personnes associées au compte

   * **[!UICONTROL Champs sortants]** - Mappez chaque champ de la table à un [champ XDM](../admin/xdm-field-management.md). Ces champs sont envoyés au service externe dans le corps de la requête. Propriétés de définition de service : `invocationPayloadDef.accountFields`, `invocationPayloadDef.fields`.

   ![Mapper les champs sortants d’action externe](./assets/configuration-external-actions-fields.png){width="600" zoomable="yes"}

   * **[!UICONTROL Champs entrants]** - Mappez chaque champ de la table à un [champ XDM modifiable](../admin/xdm-field-management.md#updatable-fields). Ces champs sont renseignés à partir de la réponse du service externe. Propriétés de définition de service : `callbackPayloadDef.accountFields`, `callbackPayloadDef.fields`. Modifiable après la création.

   * **[!UICONTROL Paramètres d’en-tête]** - Saisissez une valeur pour chaque ligne à transmettre en tant qu’en-tête HTTP dans la requête. Propriété de définition du service : `invocationPayloadDef.headers`.

   * **[!UICONTROL Délai d’expiration]** - Saisissez le nombre de minutes à attendre pour que le service externe appelle le rappel avant que la demande ne soit considérée comme ayant échoué. Propriété de définition du service : `timeout`.

   * **[!UICONTROL Attributs globaux]** - Saisissez une valeur pour chaque ligne à inclure en tant que champ statique dans le corps de la requête. Propriété de définition du service : `invocationPayloadDef.globalAttributes`.

   ![Paramètres d’en-tête d’action externe, délai d’expiration et attributs globaux](./assets/configuration-external-actions-header-timeout-global.png){width="600" zoomable="yes"}

1. Cliquez sur la _flèche Précédent_ pour revenir à la liste et conserver l’action à l’état _Brouillon_.

   Ou cliquez sur **[!UICONTROL Activer]** pour définir la configuration de l’action sur l’état _Actif_. L’action externe configurée doit être active pour pouvoir être utilisée dans les parcours de compte.

## Ajouter un nœud externe à un parcours {#add-journey-node}

Une fois qu’une action est activée, les spécialistes marketing peuvent ajouter un nœud _[!UICONTROL Action externe]_ ou _[!UICONTROL Chemin de partage externe]_ à n’importe quel parcours de compte. Pour plus d’informations sur l’ajout et l’utilisation de ces nœuds dans la zone de travail du parcours de compte, voir [Nœuds externes](../journeys/external-nodes.md).
