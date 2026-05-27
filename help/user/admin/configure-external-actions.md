---
title: Configuration des actions externes
description: Découvrez comment les développeurs, les administrateurs et les spécialistes du marketing travaillent ensemble pour implémenter, configurer et utiliser des actions externes qui connectent Journey Optimizer B2B edition à des services externes dans les parcours de compte.
feature: Setup, Integrations
role: Admin, Developer
exl-id: 226fbf23-7df2-4fd7-b5a4-2057a417a261
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
autotag-review: '2026-04-29T23:21:59.633Z'
source-git-commit: effa8e2a45ecc5afbaa5a3f75437735bef89a400
workflow-type: tm+mt
source-wordcount: 1306
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

   Le service externe doit être actif et accessible pour que cette étape réussisse. En cas d’erreur de validation, la boîte de dialogue affiche un message pour décrire l’erreur et une suggestion pour la résoudre. Pour plus d’informations, voir [_Dépannage_](#troubleshooting).

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

### Dépannage {#troubleshooting}

Lorsque vous saisissez l’URL de la spécification OpenAPI pour votre service externe et cliquez sur **[!UICONTROL Créer]**, le système effectue la validation du service. Lorsqu’elle rencontre une erreur, la boîte de dialogue affiche un message pour décrire l’erreur.

![&#x200B; Message d’erreur de validation du service d’URL d’action externe &#x200B;](./assets/configuration-external-actions-create-url-error.png){width="600" zoomable="yes"}

>[!NOTE]
>
>La plupart des erreurs suivantes nécessitent que vous collaboriez avec le développeur ou la développeuse qui a créé et publié le service web public pour les résoudre.

#### Détails de l’erreur de validation

| Erreur affichée | Pourquoi cela s’est produit | Que faire |
|---|---|---|
| `This URL is already used by another external action` | Cette URL de spécification est déjà enregistrée dans une autre action de votre organisation. | Utilisez une autre URL de spécification ou supprimez l’action existante qui l’utilise déjà. |
| `An action with this name already exists` | La `info.title` de votre spécification correspond à une action qui existe déjà | Remplacez le titre du champ `info.title` de votre spécification par quelque chose d’unique. |
| `Duplicate operation ID found in the specification` | Plusieurs opérations de votre spécification partagent la même `operationId`. | Attribuez un `operationId` unique à chaque opération. |
| `Field in the specification exceeds the maximum allowed length` | Un champ de texte de votre spécification (tel qu’un titre ou une description) est trop long. | Raccourcissez le champ marqué. |
| `The entity type value is invalid` | Une extension `x-` spécifique à Adobe pour le type d’entité a une valeur non reconnue | Corrigez le type d’entité sur une valeur prise en charge. Consultez la [documentation pour les développeurs](https://developer.adobe.com/journey-optimizer-b2b-apis/) pour connaître les options valides. |
| `The provided document is not a valid OpenAPI specification` | La spécification ne peut pas être analysée structurellement. | Validez votre spécification par rapport au schéma OpenAPI 3.0 et corrigez les problèmes. |
| `Required OpenAPI field is missing` | Il n’y a pas de champ obligatoire OpenAPI standard (`info` ou `paths`, par exemple). | Ajoutez le champ manquant. |
| `Required endpoint is missing from the specification` | Un point d’entrée requis par Adobe Journey Optimizer B2B edition n’est pas défini dans votre spécification. | Ajoutez le point d’entrée requis. Pour connaître les points d’entrée nécessaires[&#128279;](https://developer.adobe.com/journey-optimizer-b2b-apis/) consultez la  documentation pour les développeurs et développeuses . |
| `Required extension field is missing` | Un champ d’extension Adobe `x-` obligatoire est absent de votre spécification. | Ajoutez le champ d’extension manquant comme décrit dans la documentation. |
| `Security schemes are missing from the specification` | Aucune spécification n’a `securitySchemes` définie sous `components`. | Définissez au moins un schéma de sécurité. |
| `Multiple authentication types are not supported` | Votre spécification définit plusieurs schémas d’authentification. | Mettez à jour votre spécification pour utiliser un seul type d’authentification. |
| `The authentication type is not supported` | Le type de schéma de sécurité que vous avez utilisé (`oauth2` ou `openIdConnect`, par exemple) n’est pas pris en charge. | Basculez vers un type d’authentification pris en charge. Consultez la documentation destinée aux développeurs pour connaître les options prises en charge. |
| `The OpenAPI version is not supported` | Incompatibilité de version au niveau de la spécification | Mettez à jour votre spécification pour utiliser OpenAPI 3.0.x. |
| `An unexpected error occurred` | Un problème non classé a été détecté dans votre spécification. | Vérifiez votre spécification pour tout élément inhabituel et réessayez. Si l’erreur persiste, contactez l’assistance. |

<!--
## Errors you'll see if something goes wrong with the request itself

This error appears below the URL field (not in the alert banner) and means there was a network problem or an unexpected server response — not a problem with your URL or spec.

| What you'll see | Why it happened | What to do |
|---|---|---|
| `Failed to create external action. Please try again.` | A network error occurred or the server returned an unexpected response | Check your connection and try again. If it keeps happening, contact support |
-->

## Ajouter un nœud externe à un parcours {#add-journey-node}

Une fois qu’une action est activée, les spécialistes marketing peuvent ajouter un nœud _[!UICONTROL Action externe]_ ou _[!UICONTROL Chemin de partage externe]_ à n’importe quel parcours de compte. Pour plus d’informations sur l’ajout et l’utilisation de ces nœuds dans la zone de travail du parcours de compte, voir [Nœuds externes](../journeys/external-nodes.md).
