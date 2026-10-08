---
title: Jeux de données Experience Platform exportés
description: Référence pour les noms de jeux de données Adobe Experience Platform et les chemins d’accès aux champs clés exportés par Adobe Journey Optimizer B2B Edition.
feature: Setup, Data Management
role: Admin
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
    internal-label: Experience Platform
feature_v2:
  - id: f2da1b69-6919-4386-a5d2-9c7b5c9033db
    internal-label: Data management
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
    internal-label: Integrations
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
autotag-review: '2026-09-29T00:00:00.000Z'
source-git-commit: 801025ee02617d56fc8ab933b59385bca38f5097
workflow-type: tm+mt
source-wordcount: '4845'
ht-degree: 7%
---

# Jeux de données [!DNL Experience Platform] exportés

[!DNL Adobe Journey Optimizer B2B Edition] rend les informations sur le compte, la personne, le groupe d&#39;achat et le parcours disponibles dans [!DNL Adobe Experience Platform]. Un jeu de données est un ensemble d’enregistrements associés. Par exemple, un jeu de données personne décrit des personnes, un jeu de données abonnement connecte des personnes à des comptes ou à des parcours et un jeu de données événement enregistre des actions telles que l’ouverture d’un e-mail.

Utilisez ce guide pour comprendre ce que contient chaque jeu de données, ce que signifient ses champs et comment les enregistrements associés se connectent. Les noms des jeux de données suivent ce modèle :

**`AJOB2B-<datasetVersion>-<entity>`**

Ici, `<entity>` décrit les informations, telles que `person`, `account_relational` ou `person_event`. `<datasetVersion>` identifie la version des définitions de champ du jeu de données. Les en-têtes de section affichent les noms documentés ; votre environnement [!DNL Experience Platform] peut également contenir des versions plus anciennes.

Pour connaître la configuration des espaces de noms et des schémas qui prend en charge ces exportations, consultez [Espaces de noms et schémas B2B](./namespaces-schemas.md).

>[!NOTE]
>
>Adobe conserve les anciennes versions des jeux de données afin d’éviter de perturber l’utilisation existante. Par conséquent, il se peut que vous trouviez plusieurs versions du même jeu de données dans votre sandbox. Si vous n’utilisez plus un ancien jeu de données, vous pouvez demander à Adobe de le supprimer. Avant de demander la suppression, vérifiez que le jeu de données n’est plus utilisé.

## Lecture de ce guide

- **Nom du champ :** le nom exact que vous voyez dans [!DNL Experience Platform]. Des points séparent les niveaux dans un champ, par exemple `consents.marketing.email.val`.
- **ID d’enregistrement :** identifie l’enregistrement dans ce jeu de données.
- **Relation :** nomme le jeu de données et le champ auxquels l’identifiant correspond. Par exemple, `Matches AJOB2B-1_5_4-buying_group (_id)` signifie que le champ fait référence à la `_id` d’un groupe d’achats. Faire correspondre l&#39;identifiant complet; ne pas le raccourcir ou essayer de le recréer.
- **Format Adobe standard :** utilise les définitions de champ partagé Adobe.
- **Format d’enregistrement associé :** organise les informations sous forme d’enregistrements que vous pouvez connecter à l’aide d’identifiants correspondants.

Par exemple, `buying_group_member.buyingGroupID` correspond à `buying_group._id`, et son `personID` correspond à `person_relational._id` ou au `personKey.sourceKey` du jeu de données Personne. Ces liens vous aident à comprendre qui appartient à un groupe d&#39;achat. [!DNL Experience Platform] ne crée pas automatiquement de rapports ou d’audiences à partir des seuls liens.

Certains identifiants font référence à des informations qui ne contiennent pas de jeu de données distinct dans ce guide, telles qu’un programme marketing. La colonne Relation le remarque au lieu de nommer un jeu de données qui n’existe pas ici.

`isDeleted` est `true` lorsque l&#39;enregistrement est marqué comme supprimé et `false` lorsqu&#39;il ne l&#39;est pas. Ne le traitez pas comme un membre actif général ou un indicateur de consentement. `lastUpdatedDate` décrit la dernière mise à jour des données de l’enregistrement ; pour les événements, utilisez `timestamp` pour comprendre quand l’activité s’est produite. Un champ vide signifie que les informations ne sont pas disponibles ou ne s&#39;appliquent pas à cet enregistrement.

Les jeux de données d’enregistrements associés utilisent la version `1_5_4`. Lorsqu’un champ n’est pas actuellement renseigné ou nécessite une gestion spéciale, la section pertinente explique la limitation de la visibilité des clients.

Une audience est un groupe de personnes qui répondent à des critères sélectionnés. La disponibilité de la création d’audiences dépend de votre configuration [!DNL Experience Platform] pour la combinaison d’informations dans des profils de personnes. La présence d’un jeu de données dans [!DNL Experience Platform] ne signifie pas en soi qu’il est disponible pour la segmentation.

## Choisir un jeu de données

| Ce que vous voulez comprendre | Jeux de données à rechercher |
|---|---|
| Personnes et leurs préférences de messagerie | `person` |
| Détails du compte et coordonnées de la personne | `account_relational`, `person_relational` |
| Les personnes associées à un compte | `account_member`, `account_person` |
| Groupes d&#39;achat, leurs membres et changements de statut | `buying_group`, `buying_group_member`, `buying_group_event` |
| Parcours de compte et comptes participants | `account_journey`, `account_journey_member`, `account_event` |
| Parcours de personnes et participants | `person_journey`, `person_journey_member` |
| Étapes d’un parcours | `account_journey_node`, `person_journey_node`, `journey_node` |
| E-mail, web et autres activités de personne prises en charge | `person_event`, `person_event_relational` |

Les sections suivantes fournissent les noms complets des jeux de données et les détails des champs. Un parcours décrit l’expérience globale ; une adhésion connecte une personne ou un compte à ce parcours ; un événement décrit ce qui s’est passé.

+++Diagramme de relation d&#39;entité

![Diagramme de relation d’entité pour les jeux de données exportés vers [!DNL Adobe Experience Platform]](./assets/ajo-b2b-data-model.svg)

+++

## `AJOB2B-1_5_1-person`

Chaque enregistrement décrit une personne, ses identifiants et ses préférences de marketing par e-mail. Utilisez-le pour la création de rapports au niveau de la personne et, lorsque Profile est configuré, pour créer des audiences.

**Format:** Format Adobe standard

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `personID` | ID d’enregistrement | Identifiant de la personne. Utilisez la valeur complète pour faire correspondre les enregistrements associés. |
| `personKey.sourceID` |  | Identifiant de la personne dans le système connecté. |
| `personKey.sourceInstanceID` |  | Identifiant de l’environnement [!DNL Experience Platform] ou du compte connecté. |
| `personKey.sourceType` |  | Nom du produit connecté. |
| `personKey.sourceKey` |  | Identifiant complet de la personne utilisé pour faire correspondre les enregistrements associés. |
| `identityMap` |  | D’autres identifiants qui [!DNL Experience Platform] aident à reconnaître la même personne sur l’ensemble de vos données connectées. |
| `consents.marketing.email.val` |  | Préférence de marketing par e-mail : `n` indique un processus d’opt-out ; `y` indique qu’aucun processus d’opt-out n’est enregistré dans ce champ. Ce champ seul n’établit pas l’autorisation d’envoyer des e-mails marketing. |
| `consents.marketing.email.time` |  | Date et heure de la dernière mise à jour de la préférence e-mail. |
| `consents.marketing.email.reason` |  | Motif de désinscription, le cas échéant (défini uniquement en cas de désabonnement). |
| `isDeleted` |  | Indique si cet enregistrement de personne est marqué comme supprimé. |

>[!NOTE]
>
>Votre organisation peut avoir d’autres champs de personne en plus de ceux répertoriés ici.

Lorsque votre organisation utilise ses propres jeux de données de compte ou de personne configurés, ces enregistrements peuvent également inclure des `isDeleted`. Voir [Jeux de données détenus par le client](#customer-owned-datasets).

## `AJOB2B-1_5_4-account_member`

Chaque enregistrement lie un compte à une personne. Utilisez ce jeu de données pour signaler les personnes associées à chaque compte ; il décrit la relation plutôt que l’un ou l’autre profil.

**Format:** Format d’enregistrement associé

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | ID d’enregistrement de la relation. |
| `accountID` | Correspond à `AJOB2B-1_5_4-account_relational` (`_id`) | Identifiant du compte. |
| `personID` | Correspond à `AJOB2B-1_5_4-person_relational` (`_id`) | Identifiant de la personne. |
| `isDeleted` |  | Indique si cet enregistrement est marqué comme supprimé. |
| `lastUpdatedDate` |  | Heure de la dernière modification. |

## `AJOB2B-1_5_4-buying_group`

Chaque enregistrement décrit un groupe d&#39;achats associé à un compte, y compris son nom, son statut, le centre d&#39;intérêt de la solution, ainsi que ses scores d&#39;engagement et d&#39;exhaustivité. L&#39;étape du groupe d&#39;achat n&#39;est pas renseignée actuellement.

**Format:** Format d’enregistrement associé

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | ID enregistrement du groupe d&#39;achat (utilisez la valeur complète). |
| `buyingGroupName` |  | Nom du groupe d&#39;achat. |
| `engagementScore` |  | Score d’engagement. |
| `completenessScore` |  | Score d&#39;exhaustivité. |
| `accountID` | Correspond à `AJOB2B-1_5_4-account_relational` (`_id`) | Identifiant du compte associé. |
| `solutionInterest` |  | Libellé d’intérêt de la solution. |
| `buyingGroupStatus` |  | Statut. |
| `buyingGroupStage` |  | Nom de l&#39;étape du groupe d&#39;achat. |
| `isDeleted` |  | Indique si cet enregistrement est marqué comme supprimé. |
| `lastUpdatedDate` |  | Heure de la dernière modification. |

>[!NOTE]
>
>**Note de disponibilité :** `buyingGroupStage` est actuellement vide. Ne l&#39;utilisez pas pour filtrer ou regrouper des groupes d&#39;achats par étape.

## `AJOB2B-1_5_4-buying_group_member`

Chaque enregistrement associe une personne à un groupe d&#39;achats et enregistre le rôle de cette personne. Utilisez-le pour signaler la composition du groupe d&#39;achat et la couverture des rôles.

`isDeleted` n&#39;indique pas toujours si une personne a été retirée d&#39;un groupe d&#39;achats. N’utilisez pas ce champ seul pour déterminer l’appartenance actuelle. Le nom du rôle peut être vide lorsqu’aucune information n’est disponible.

**Format:** Format d’enregistrement associé

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | ID d’enregistrement de l’abonnement. |
| `buyingGroupID` | Correspond à `AJOB2B-1_5_4-buying_group` (`_id`) | Identifiant du groupe d&#39;achat. |
| `personID` | Correspond à `AJOB2B-1_5_4-person_relational` (`_id`) | Identifiant de la personne. |
| `buyingGroupMemberRole` |  | Nom du rôle, le cas échéant. |
| `isDeleted` |  | Indique si cet enregistrement est marqué comme supprimé. |
| `lastUpdatedDate` |  | Heure de la dernière modification. |

## `AJOB2B-1_5_4-account_journey`

Chaque enregistrement décrit un parcours de compte, avec son nom, son statut, ses dates de début et de fin. Utilisez-le pour indiquer le cycle de vie et le statut du parcours pour les comptes.

**Format:** Format d’enregistrement associé

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | ID enregistrement du parcours (utilisez la valeur complète). |
| `accountJourneyName` |  | Nom du parcours. |
| `accountJourneyStatus` |  | Statut (par exemple brouillon, actif, terminé). |
| `startDate` |  | Date et heure de début. |
| `endDate` |  | Date et heure de fin. |
| `isDeleted` |  | Indique si cet enregistrement est marqué comme supprimé. |
| `lastUpdatedDate` |  | Heure de la dernière modification. |

## `AJOB2B-1_5_4-account_journey_member`

Chaque enregistrement connecte un compte à un parcours de compte. Utilisez-le pour identifier et signaler les comptes qui participent à chaque parcours.

**Format:** Format d’enregistrement associé

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | ID d’enregistrement de l’abonnement. |
| `accountID` | Correspond à `AJOB2B-1_5_4-account_relational` (`_id`) | Identifiant du compte. |
| `journeyID` | Correspond à `AJOB2B-1_5_4-account_journey` (`_id`) | Identifiant du parcours de compte. |
| `isDeleted` |  | Indique si cet enregistrement est marqué comme supprimé. |
| `lastUpdatedDate` |  | Heure de la dernière modification. |

## `AJOB2B-1_5_4-person_journey`

Chaque enregistrement décrit un parcours de personne, avec son nom, son statut, ses dates de début et de fin. Utilisez-le pour générer des rapports sur le cycle de vie et l’état des parcours pour les parcours axés sur les personnes.

**Format:** Format d’enregistrement associé

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | ID enregistrement du parcours (utilisez la valeur complète). |
| `personJourneyName` |  | Nom du parcours. |
| `personJourneyStatus` |  | Statut (par exemple brouillon, actif, terminé). |
| `startDate` |  | Date et heure de début. |
| `endDate` |  | Date et heure de fin. |
| `isDeleted` |  | Indique si cet enregistrement est marqué comme supprimé. |
| `lastUpdatedDate` |  | Heure de la dernière modification. |

## `AJOB2B-1_5_4-person_journey_member`

Chaque enregistrement décrit l’appartenance d’une personne à un parcours, y compris le nœud de parcours actuel, les dates d’appartenance et d’entrée, ainsi que le nombre d’entrées. Utilisez-le pour signaler l’inscription, la rentrée et la progression du parcours.

**Format:** Format d’enregistrement associé

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | ID d’enregistrement de l’abonnement. |
| `marketingProgramID` |  | Identifiant du programme marketing auquel appartient le parcours. |
| `personID` | Correspond à `AJOB2B-1_5_4-person_relational` (`_id`) | Identifiant de la personne. |
| `journeyID` | Correspond à `AJOB2B-1_5_4-person_journey` (`_id`) | Identifiant du parcours. |
| `journeyNodeID` | Correspond à `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identifiant du nœud de parcours où se trouve actuellement la personne. |
| `membershipDate` |  | Lorsque la personne est devenue membre du programme marketing. |
| `lastEntryDate` |  | Date à laquelle la personne a rejoint le parcours pour la dernière fois. |
| `reentryOpensAt` |  | Lorsque la personne peut entrer à nouveau dans le parcours. |
| `entryCount` |  | Nombre de fois où la personne a accédé au parcours. |
| `createdDate` |  | Date de création de l’enregistrement. |
| `updatedDate` |  | Date de la dernière modification de l’enregistrement. |
| `isDeleted` |  | Indique si cet enregistrement est marqué comme supprimé. |
| `lastUpdatedDate` |  | Heure de la dernière modification. |

## `AJOB2B-1_5_4-account_journey_node`

Chaque enregistrement décrit une étape d’un parcours, y compris le type d’étape et le parcours auquel il appartient. Un nœud de parcours est une étape telle qu’un démarrage, une attente ou une décision. Les mêmes étapes peuvent apparaître dans `person_journey_node` ; faites correspondre les `accountJourneyID` à un parcours de compte avant de traiter une étape comme étant spécifique au compte.

**Format:** Format d’enregistrement associé

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | ID d’enregistrement du nœud (utilisez la valeur complète). |
| `accountJourneyID` | Correspond à `AJOB2B-1_5_4-account_journey` (`_id`) | Identifiant du parcours parent. |
| `uuid` |  | Identifiant supplémentaire de l’étape de parcours. |
| `journeyNodeTypeID` |  | Numéro identifiant le type d’étape de parcours. |
| `nodeType` |  | Libellé identifiant le type d’étape de parcours. |
| `isDeleted` |  | Indique si cet enregistrement est marqué comme supprimé. |
| `createdDate` |  | Date de création de l’enregistrement. |
| `lastUpdatedDate` |  | Heure de la dernière modification. |

## `AJOB2B-1_5_4-person_journey_node`

Chaque enregistrement décrit une étape d’un parcours, y compris le type d’étape et le parcours auquel il appartient. Les mêmes étapes peuvent apparaître dans `account_journey_node` ; faites correspondre `personJourneyID` à un parcours de personne avant de traiter une étape comme spécifique à une personne.

**Format:** Format d’enregistrement associé

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | ID d’enregistrement du nœud (utilisez la valeur complète). |
| `personJourneyID` | Correspond à `AJOB2B-1_5_4-person_journey` (`_id`) | Identifiant du parcours parent. |
| `uuid` |  | Identifiant supplémentaire de l’étape de parcours. |
| `journeyNodeTypeID` |  | Numéro identifiant le type d’étape de parcours. |
| `nodeType` |  | Libellé identifiant le type d’étape de parcours. |
| `isDeleted` |  | Indique si cet enregistrement est marqué comme supprimé. |
| `createdDate` |  | Date de création de l’enregistrement. |
| `lastUpdatedDate` |  | Heure de la dernière modification. |

## `AJOB2B-1_5_4-account_event`

Chaque enregistrement capture un événement de parcours de compte : un compte ajouté ou supprimé d’un parcours, ou déplacé entre les nœuds de parcours. Utilisez `eventType` et `timestamp` pour créer un journal d’activité de compte ; `buyingGroupID` est disponible lorsque l’événement est attribué à un groupe d’achat.

**Format:** Format d’enregistrement associé

`eventType` fournit des informations sur ce qui s’est passé. Les tableaux suivants décrivent les champs de chaque type d’activité.

`lastUpdatedDate` n’est actuellement pas renseigné pour ces événements. Utilisez `timestamp` pour la date de l’activité.

### Compte ajouté à un parcours (`account.addAccountToJourney`)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | Identifiant de l’activité. |
| `eventType` |  | `account.addAccountToJourney`. |
| `timestamp` |  | Moment où l’activité s’est produite. |
| `accountID` | Correspond à `AJOB2B-1_5_4-account_relational` (`_id`) | Identifiant du compte. |
| `journeyID` | Correspond à `AJOB2B-1_5_4-account_journey` (`_id`) | Identifiant du parcours. |
| `journeyNodeID` | Correspond à `AJOB2B-1_5_4-account_journey_node` (`_id`) | Identifiant du nœud du parcours. |
| `buyingGroupID` | Correspond à `AJOB2B-1_5_4-buying_group` (`_id`) | Identifiant du groupe d&#39;achat, lorsque l&#39;ajout de parcours est attribué au groupe d&#39;achat. |
| `lastUpdatedDate` |  | Enregistrer l’heure de mise à jour. Actuellement vide. Utilisez l’horodatage pour la date de l’activité. |

### Compte supprimé d’un parcours (`account.removeAccountFromJourney`)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | Identifiant de l’activité. |
| `eventType` |  | `account.removeAccountFromJourney`. |
| `timestamp` |  | Moment où l’activité s’est produite. |
| `accountID` | Correspond à `AJOB2B-1_5_4-account_relational` (`_id`) | Identifiant du compte. |
| `journeyID` | Correspond à `AJOB2B-1_5_4-account_journey` (`_id`) | Identifiant du parcours. |
| `journeyNodeID` | Correspond à `AJOB2B-1_5_4-account_journey_node` (`_id`) | Identifiant du nœud du parcours. |
| `buyingGroupID` | Correspond à `AJOB2B-1_5_4-buying_group` (`_id`) | Identifiant du groupe d&#39;achat, lorsque la suppression du parcours est attribuée au groupe d&#39;achat. |
| `lastUpdatedDate` |  | Enregistrer l’heure de mise à jour. Actuellement vide. Utilisez l’horodatage pour la date de l’activité. |

### Compte déplacé entre les étapes de parcours (`account.changeAccountJourneyNode`)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | Identifiant de l’activité. |
| `eventType` |  | `account.changeAccountJourneyNode`. |
| `timestamp` |  | Moment où l’activité s’est produite. |
| `accountID` | Correspond à `AJOB2B-1_5_4-account_relational` (`_id`) | Identifiant du compte. |
| `journeyID` | Correspond à `AJOB2B-1_5_4-account_journey` (`_id`) | Identifiant du parcours. |
| `journeyNodeID` | Correspond à `AJOB2B-1_5_4-account_journey_node` (`_id`) | Identifiant du nœud du parcours. |
| `previousJourneyNodeID` | Fait référence à `AJOB2B-1_5_4-account_journey_node` (`_id`) ; les valeurs peuvent ne pas correspondre. | Identifiant de l’étape de parcours précédente. Cette valeur peut ne pas correspondre à l’enregistrement d’étape correspondant. Ne vous fiez pas uniquement à elle pour connecter les enregistrements. |
| `buyingGroupID` | Correspond à `AJOB2B-1_5_4-buying_group` (`_id`) | Identifiant du groupe d’achat, lorsque le changement de nœud est attribué au groupe d’achat. |
| `lastUpdatedDate` |  | Enregistrer l’heure de mise à jour. Actuellement vide. Utilisez l’horodatage pour la date de l’activité. |

## `AJOB2B-1_5_4-buying_group_event`

Chaque enregistrement capture une modification du statut d&#39;un groupe d&#39;achats, y compris le nouveau statut et le moment où il a été modifié. Le champ nouvelle étape n’est actuellement pas renseigné.

**Format:** Format d’enregistrement associé

### Statut du groupe d&#39;achat modifié (`buyingGroup.changeStatus`)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | Identifiant de l’activité. |
| `eventType` |  | `buyingGroup.changeStatus`. |
| `timestamp` |  | Moment où l’activité s’est produite. |
| `buyingGroupID` | Correspond à `AJOB2B-1_5_4-buying_group` (`_id`) | Identifiant du groupe d&#39;achat. |
| `newStatus` |  | Nouvelle valeur de statut. |
| `newStage` |  | Nouvelle étape du groupe d&#39;achat. Actuellement vide. |
| `lastUpdatedDate` |  | Enregistrer l’heure de mise à jour. |

>[!NOTE]
>
>**Note de disponibilité :** utilisez `newStatus` pour signaler les changements de statut. N’utilisez pas `newStage` pour signaler les modifications de l’étape, car elle est actuellement vide.

## `AJOB2B-1_5-person_event`

Chaque enregistrement décrit un événement web, e-mail au niveau de la personne ou tout autre événement d’activité pris en charge. Utilisez `eventType` et `timestamp` pour analyser le comportement au fil du temps, les détails spécifiques à l’événement étant renseignés uniquement pour le type d’événement correspondant.

**Format:** Format Adobe standard

`eventType` vous dit ce qui s&#39;est passé. Les tableaux suivants décrivent les champs de chaque type d’activité. Les détails qui ne s’appliquent pas à un événement sont vides.

### E-mail envoyé (`directMarketing.emailSent`)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | Identifiant de l’activité. |
| `eventType` |  | `directMarketing.emailSent`. |
| `timestamp` |  | Moment où l’activité s’est produite. |
| `personID` | Correspond à `AJOB2B-1_5_1-person` (`personID`) | Identifiant de la personne. |
| `personKey.sourceID` |  | Identifiant de la personne dans le système connecté. |
| `personKey.sourceType` |  | Nom du produit connecté. |
| `personKey.sourceInstanceID` |  | Identifiant de l’environnement [!DNL Experience Platform] ou du compte connecté. |
| `personKey.sourceKey` |  | Identifiant complet de la personne utilisé pour faire correspondre les enregistrements associés. |
| `directMarketing.emailSent.mailingKey.sourceID` |  | ID de ressource de publipostage. |
| `directMarketing.emailSent.mailingKey.sourceType` |  | Nom du produit connecté. |
| `directMarketing.emailSent.mailingKey.sourceInstanceID` |  | Identifiant de l’instance. |
| `directMarketing.emailSent.mailingKey.sourceKey` |  | Identifiant complet du contenu de l’e-mail. |
| `directMarketing.emailSent.mailingName` |  | Nom du publipostage. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Correspond à `AJOB2B-1_5_4-person_journey` (`_id`) | Identifiant du parcours (si attribué). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Correspond à `AJOB2B-1_5_4-person_journey_node` (`_id`) | ID de nœud de parcours (si attribué). |

### E-mail diffusé (`directMarketing.emailDelivered`)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | Identifiant de l’activité. |
| `eventType` |  | `directMarketing.emailDelivered`. |
| `timestamp` |  | Moment où l’activité s’est produite. |
| `personID` | Correspond à `AJOB2B-1_5_1-person` (`personID`) | Identifiant de la personne. |
| `personKey.sourceID` |  | Identifiant de la personne dans le système connecté. |
| `personKey.sourceType` |  | Nom du produit connecté. |
| `personKey.sourceInstanceID` |  | Identifiant de l’environnement [!DNL Experience Platform] ou du compte connecté. |
| `personKey.sourceKey` |  | Identifiant complet de la personne utilisé pour faire correspondre les enregistrements associés. |
| `directMarketing.mailingKey.sourceID` |  | ID de ressource de publipostage. |
| `directMarketing.mailingKey.sourceType` |  | Nom du produit connecté. |
| `directMarketing.mailingKey.sourceInstanceID` |  | Identifiant de l’instance. |
| `directMarketing.mailingKey.sourceKey` |  | Identifiant complet du contenu de l’e-mail. |
| `directMarketing.mailingName` |  | Nom du publipostage. |
| `directMarketing.email` |  | Adresse électronique. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Correspond à `AJOB2B-1_5_4-person_journey` (`_id`) | Identifiant du parcours (si attribué). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Correspond à `AJOB2B-1_5_4-person_journey_node` (`_id`) | ID de nœud de parcours (si attribué). |

### Désabonnement des e-mails (`directMarketing.emailUnsubscribed`)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | Identifiant de l’activité. |
| `eventType` |  | `directMarketing.emailUnsubscribed`. |
| `timestamp` |  | Moment où l’activité s’est produite. |
| `personID` | Correspond à `AJOB2B-1_5_1-person` (`personID`) | Identifiant de la personne. |
| `personKey.sourceID` |  | Identifiant de la personne dans le système connecté. |
| `personKey.sourceType` |  | Nom du produit connecté. |
| `personKey.sourceInstanceID` |  | Identifiant de l’environnement [!DNL Experience Platform] ou du compte connecté. |
| `personKey.sourceKey` |  | Identifiant complet de la personne utilisé pour faire correspondre les enregistrements associés. |
| `directMarketing.mailingKey.sourceID` |  | ID de ressource de publipostage. |
| `directMarketing.mailingKey.sourceType` |  | Nom du produit connecté. |
| `directMarketing.mailingKey.sourceInstanceID` |  | Identifiant de l’instance. |
| `directMarketing.mailingKey.sourceKey` |  | Identifiant complet du contenu de l’e-mail. |
| `directMarketing.mailingName` |  | Nom du publipostage. |
| `directMarketing.email` |  | Adresse électronique. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Correspond à `AJOB2B-1_5_4-person_journey` (`_id`) | Identifiant du parcours (si attribué). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Correspond à `AJOB2B-1_5_4-person_journey_node` (`_id`) | ID de nœud de parcours (si attribué). |

### E-mail ouvert (`directMarketing.emailOpened`)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | Identifiant de l’activité. |
| `eventType` |  | `directMarketing.emailOpened`. |
| `timestamp` |  | Moment où l’activité s’est produite. |
| `personID` | Correspond à `AJOB2B-1_5_1-person` (`personID`) | Identifiant de la personne. |
| `personKey.sourceID` |  | Identifiant de la personne dans le système connecté. |
| `personKey.sourceType` |  | Nom du produit connecté. |
| `personKey.sourceInstanceID` |  | Identifiant de l’environnement [!DNL Experience Platform] ou du compte connecté. |
| `personKey.sourceKey` |  | Identifiant complet de la personne utilisé pour faire correspondre les enregistrements associés. |
| `directMarketing.mailingKey.sourceID` |  | ID de ressource de publipostage. |
| `directMarketing.mailingKey.sourceType` |  | Nom du produit connecté. |
| `directMarketing.mailingKey.sourceInstanceID` |  | Identifiant de l’instance. |
| `directMarketing.mailingKey.sourceKey` |  | Identifiant complet du contenu de l’e-mail. |
| `directMarketing.mailingName` |  | Nom du publipostage. |
| `directMarketing.email` |  | Adresse électronique. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Correspond à `AJOB2B-1_5_4-person_journey` (`_id`) | Identifiant du parcours (si attribué). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Correspond à `AJOB2B-1_5_4-person_journey_node` (`_id`) | ID de nœud de parcours (si attribué). |
| `device.isMobileDevice` |  | Indique si un appareil mobile a été enregistré pour l’activité. |
| `device.model` |  | Informations sur l’appareil ou le client de messagerie. |
| `environment.browserDetails.userAgent` |  | Informations sur le navigateur ou le client de messagerie. |
| `environment.operatingSystem` |  | Système d’exploitation. |

### Lien de l’e-mail sur lequel l’utilisateur a cliqué (`directMarketing.emailClicked`)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | Identifiant de l’activité. |
| `eventType` |  | `directMarketing.emailClicked`. |
| `timestamp` |  | Moment où l’activité s’est produite. |
| `personID` | Correspond à `AJOB2B-1_5_1-person` (`personID`) | Identifiant de la personne. |
| `personKey.sourceID` |  | Identifiant de la personne dans le système connecté. |
| `personKey.sourceType` |  | Nom du produit connecté. |
| `personKey.sourceInstanceID` |  | Identifiant de l’environnement [!DNL Experience Platform] ou du compte connecté. |
| `personKey.sourceKey` |  | Identifiant complet de la personne utilisé pour faire correspondre les enregistrements associés. |
| `directMarketing.mailingKey.sourceID` |  | ID de ressource de publipostage. |
| `directMarketing.mailingKey.sourceType` |  | Nom du produit connecté. |
| `directMarketing.mailingKey.sourceInstanceID` |  | Identifiant de l’instance. |
| `directMarketing.mailingKey.sourceKey` |  | Identifiant complet du contenu de l’e-mail. |
| `directMarketing.mailingName` |  | Nom du publipostage. |
| `directMarketing.email` |  | Adresse électronique. |
| `directMarketing.linkURL` |  | URL du lien cliqué. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Correspond à `AJOB2B-1_5_4-person_journey` (`_id`) | Identifiant du parcours (si attribué). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Correspond à `AJOB2B-1_5_4-person_journey_node` (`_id`) | ID de nœud de parcours (si attribué). |
| `device.isMobileDevice` |  | Indique si un appareil mobile a été enregistré pour l’activité. |
| `device.model` |  | Informations sur l’appareil ou le client de messagerie. |
| `environment.browserDetails.userAgent` |  | Informations sur le navigateur ou le client de messagerie. |
| `environment.operatingSystem` |  | Système d’exploitation. |

### E-mail non remis (`directMarketing.emailBounced`)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | Identifiant de l’activité. |
| `eventType` |  | `directMarketing.emailBounced`. |
| `timestamp` |  | Moment où l’activité s’est produite. |
| `personID` | Correspond à `AJOB2B-1_5_1-person` (`personID`) | Identifiant de la personne. |
| `personKey.sourceID` |  | Identifiant de la personne dans le système connecté. |
| `personKey.sourceType` |  | Nom du produit connecté. |
| `personKey.sourceInstanceID` |  | Identifiant de l’environnement [!DNL Experience Platform] ou du compte connecté. |
| `personKey.sourceKey` |  | Identifiant complet de la personne utilisé pour faire correspondre les enregistrements associés. |
| `directMarketing.mailingKey.sourceID` |  | ID de ressource de publipostage. |
| `directMarketing.mailingKey.sourceType` |  | Nom du produit connecté. |
| `directMarketing.mailingKey.sourceInstanceID` |  | Identifiant de l’instance. |
| `directMarketing.mailingKey.sourceKey` |  | Identifiant complet du contenu de l’e-mail. |
| `directMarketing.mailingName` |  | Nom du publipostage. |
| `directMarketing.email` |  | Adresse électronique. |
| `directMarketing.emailBouncedCode` |  | Catégorie/code de rebond. |
| `directMarketing.emailBouncedDetails` |  | Texte du détail. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Correspond à `AJOB2B-1_5_4-person_journey` (`_id`) | Identifiant du parcours (si attribué). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Correspond à `AJOB2B-1_5_4-person_journey_node` (`_id`) | ID de nœud de parcours (si attribué). |

### E-mail soft bounce (`directMarketing.emailBouncedSoft`)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | Identifiant de l’activité. |
| `eventType` |  | `directMarketing.emailBouncedSoft`. |
| `timestamp` |  | Moment où l’activité s’est produite. |
| `personID` | Correspond à `AJOB2B-1_5_1-person` (`personID`) | Identifiant de la personne. |
| `personKey.sourceID` |  | Identifiant de la personne dans le système connecté. |
| `personKey.sourceType` |  | Nom du produit connecté. |
| `personKey.sourceInstanceID` |  | Identifiant de l’environnement [!DNL Experience Platform] ou du compte connecté. |
| `personKey.sourceKey` |  | Identifiant complet de la personne utilisé pour faire correspondre les enregistrements associés. |
| `directMarketing.mailingKey.sourceID` |  | ID de ressource de publipostage. |
| `directMarketing.mailingKey.sourceType` |  | Nom du produit connecté. |
| `directMarketing.mailingKey.sourceInstanceID` |  | Identifiant de l’instance. |
| `directMarketing.mailingKey.sourceKey` |  | Identifiant complet du contenu de l’e-mail. |
| `directMarketing.mailingName` |  | Nom du publipostage. |
| `directMarketing.email` |  | Adresse électronique. |
| `directMarketing.emailBouncedCode` |  | Catégorie/code de rebond. |
| `directMarketing.emailBouncedDetails` |  | Texte du détail. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Correspond à `AJOB2B-1_5_4-person_journey` (`_id`) | Identifiant du parcours (si attribué). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Correspond à `AJOB2B-1_5_4-person_journey_node` (`_id`) | ID de nœud de parcours (si attribué). |

### Page web consultée (`web.webpagedetails.pageViews`)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | Identifiant de l’activité. |
| `eventType` |  | `web.webpagedetails.pageViews`. |
| `timestamp` |  | Moment où l’activité s’est produite. |
| `personID` | Correspond à `AJOB2B-1_5_1-person` (`personID`) | Identifiant de la personne. |
| `personKey.sourceID` |  | Identifiant de la personne dans le système connecté. |
| `personKey.sourceType` |  | Nom du produit connecté. |
| `personKey.sourceInstanceID` |  | Identifiant de l’environnement [!DNL Experience Platform] ou du compte connecté. |
| `personKey.sourceKey` |  | Identifiant complet de la personne utilisé pour faire correspondre les enregistrements associés. |
| `web.webPageDetails.webPageKey.sourceID` |  | ID de ressource de page. |
| `web.webPageDetails.webPageKey.sourceType` |  | Nom du produit connecté. |
| `web.webPageDetails.webPageKey.sourceInstanceID` |  | Identifiant de l’instance. |
| `web.webPageDetails.webPageKey.sourceKey` |  | Identifiant de page complet. |
| `web.webPageDetails.name` |  | Nom de la page. |
| `web.webPageDetails.URL` |  | URL de la page. |
| `web.webPageDetails.queryParameters` |  | Informations supplémentaires incluses dans une adresse web. |
| `web.webPageDetails.webPageID` |  | ID de page. |
| `environment.browserDetails.userAgent` |  | Informations sur le navigateur ou le client de messagerie. |
| `web.webReferrer.URL` |  | URL du référent. |

### Lien web sur lequel l’utilisateur a cliqué (`web.webinteraction.linkClicks`)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | Identifiant de l’activité. |
| `eventType` |  | `web.webinteraction.linkClicks`. |
| `timestamp` |  | Moment où l’activité s’est produite. |
| `personID` | Correspond à `AJOB2B-1_5_1-person` (`personID`) | Identifiant de la personne. |
| `personKey.sourceID` |  | Identifiant de la personne dans le système connecté. |
| `personKey.sourceType` |  | Nom du produit connecté. |
| `personKey.sourceInstanceID` |  | Identifiant de l’environnement [!DNL Experience Platform] ou du compte connecté. |
| `personKey.sourceKey` |  | Identifiant complet de la personne utilisé pour faire correspondre les enregistrements associés. |
| `web.webInteraction.webInteractionKey.sourceID` |  | Identifiant de la ressource Interaction. |
| `web.webInteraction.webInteractionKey.sourceType` |  | Nom du produit connecté. |
| `web.webInteraction.webInteractionKey.sourceInstanceID` |  | Identifiant de l’instance. |
| `web.webInteraction.webInteractionKey.sourceKey` |  | Identifiant complet de l’interaction. |
| `web.webInteraction.linkID` |  | Identifiant du lien. |
| `web.webInteraction.linkURL` |  | URL de destination. |
| `web.webPageDetails.queryParameters` |  | Informations supplémentaires incluses dans une adresse web. |
| `web.webPageDetails.webPageID` |  | ID de page. |
| `environment.browserDetails.userAgent` |  | Informations sur le navigateur ou le client de messagerie. |
| `web.webReferrer.URL` |  | URL du référent. |

### Formulaire envoyé (`web.formFilledOut`)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | Identifiant de l’activité. |
| `eventType` |  | `web.formFilledOut`. |
| `timestamp` |  | Moment où l’activité s’est produite. |
| `personID` | Correspond à `AJOB2B-1_5_1-person` (`personID`) | Identifiant de la personne. |
| `personKey.sourceID` |  | Identifiant de la personne dans le système connecté. |
| `personKey.sourceType` |  | Nom du produit connecté. |
| `personKey.sourceInstanceID` |  | Identifiant de l’environnement [!DNL Experience Platform] ou du compte connecté. |
| `personKey.sourceKey` |  | Identifiant complet de la personne utilisé pour faire correspondre les enregistrements associés. |
| `web.fillOutForm.webFormKey.sourceID` |  | ID de ressource de formulaire. |
| `web.fillOutForm.webFormKey.sourceType` |  | Nom du produit connecté. |
| `web.fillOutForm.webFormKey.sourceInstanceID` |  | Identifiant de l’instance. |
| `web.fillOutForm.webFormKey.sourceKey` |  | Identifiant de formulaire complet. |
| `web.fillOutForm.webFormID` |  | ID du formulaire. |
| `web.fillOutForm.webFormName` |  | Nom du formulaire. |
| `web.webPageDetails.queryParameters` |  | Informations supplémentaires incluses dans une adresse web. |
| `web.webPageDetails.webPageID` |  | ID de page. |
| `environment.browserDetails.userAgent` |  | Informations sur le navigateur ou le client de messagerie. |
| `web.webReferrer.URL` |  | URL du référent. |

### Moment intéressant enregistré (`leadOperation.interestingMoment`)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | Identifiant de l’activité. |
| `eventType` |  | `leadOperation.interestingMoment`. |
| `timestamp` |  | Moment où l’activité s’est produite. |
| `personID` | Correspond à `AJOB2B-1_5_1-person` (`personID`) | Identifiant de la personne. |
| `personKey.sourceID` |  | Identifiant de la personne dans le système connecté. |
| `personKey.sourceType` |  | Nom du produit connecté. |
| `personKey.sourceInstanceID` |  | Identifiant de l’environnement [!DNL Experience Platform] ou du compte connecté. |
| `personKey.sourceKey` |  | Identifiant complet de la personne utilisé pour faire correspondre les enregistrements associés. |
| `leadOperation.interestingMoment.date` |  | Date/heure du moment. |
| `leadOperation.interestingMoment.description` |  | Description |
| `leadOperation.interestingMoment.source` |  | Nom du produit ou de la campagne associé. |
| `leadOperation.interestingMoment.type` |  | Tapez le libellé. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Correspond à `AJOB2B-1_5_4-person_journey` (`_id`) | Identifiant du parcours (si attribué). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Correspond à `AJOB2B-1_5_4-person_journey_node` (`_id`) | ID de nœud de parcours (si attribué). |

## `AJOB2B-1_5_4-journey_node`

Chaque enregistrement décrit une étape de parcours, le parcours auquel il appartient et le type d’étape. Les mêmes étapes peuvent apparaître dans les jeux de données d’étapes de parcours compte et personne. Faire correspondre les `journeyID` au parcours approprié ; ne pas compter une étape plus d’une fois car elle apparaît dans plusieurs jeux de données.

**Format:** Format d’enregistrement associé

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | ID d’enregistrement du nœud (utilisez la valeur complète). |
| `journeyID` | Correspond à `AJOB2B-1_5_4-account_journey` ou `AJOB2B-1_5_4-person_journey` (`_id`) | Identifiant du parcours parent. |
| `nodeType` |  | Type d’étape de parcours, comme un début, une fin, une attente ou une décision. |
| `isDeleted` |  | Indique si cet enregistrement est marqué comme supprimé. |
| `lastUpdatedDate` |  | Heure de la dernière modification. |

## `AJOB2B-1_5_4-account_relational`

Chaque enregistrement décrit un compte, y compris les détails de son organisation, son emplacement, sa taille, son chiffre d’affaires et ses champs personnalisés. Utilisez ces informations pour ajouter un contexte de compte aux rapports de groupe d&#39;achats et de parcours.

**Format:** Format d’enregistrement associé

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | ID enregistrement du compte (utilisez la valeur complète). |
| `accountName` |  | Nom du compte. |
| `industry` |  | Classification des secteurs d&#39;activité. |
| `country` |  | Pays. |
| `sicCode` |  | Code de classification industrielle standard. |
| `domainName` |  | Principal du domaine web. |
| `primaryEmailDomain` |  | Principal du domaine d&#39;e-mail. |
| `street` |  | Rue. |
| `city` |  | Ville. |
| `state` |  | État ou région. |
| `postalCode` |  | Code postal. |
| `region` |  | Région géographique. |
| `phoneNumber` |  | Numéro de téléphone. |
| `logoUrl` |  | URL du logo du compte. |
| `annualRevenue` |  | Chiffre d’affaires annuel. |
| `numberOfEmployees` |  | Nombre d&#39;employés. |
| `createdDate` |  | Date de création de l’enregistrement. |
| `sourceType` |  | Nom du système connecté identifiant le compte. |
| `sourceInstanceID` |  | Identifiant de votre organisation ou compte dans ce système connecté. |
| `sourceID` |  | Identifiant du compte sur ce système connecté. |
| `customAttributes` |  | Noms et valeurs de champs personnalisés stockés ensemble sous forme de texte. |
| `isDeleted` |  | Indique si cet enregistrement est marqué comme supprimé. |
| `lastUpdatedDate` |  | Heure de la dernière modification. |

## `AJOB2B-1_5_4-person_relational`

Chaque enregistrement décrit une personne, y compris ses coordonnées, les détails de sa tâche, ses identifiants et ses champs personnalisés. Utilisez-le pour ajouter des informations sur les personnes aux rapports d’abonnement, de parcours et d’activité.

**Format:** Format d’enregistrement associé

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | Identifiant complet de la personne utilisé pour faire correspondre les enregistrements associés. |
| `email` |  | Adresse électronique. |
| `firstName` |  | Prénom. |
| `middleName` |  | Deuxième prénom. |
| `lastName` |  | Nom. |
| `jobTitle` |  | Intitulé du poste. |
| `personType` |  | Type de personne : contact, prospect ou prospect en attente. |
| `isLead` |  | Si la personne est un prospect. |
| `isAnonymous` |  | Si la personne est anonyme. |
| `salutation` |  | Salutation ou honneur. |
| `phone` |  | Numéro de téléphone Principal. |
| `mobile` |  | Numéro de téléphone portable. |
| `sourceType` |  | Nom du système connecté qui identifie la personne, tel que [!DNL Marketo Engage]. |
| `sourceInstanceID` |  | Identifiant de votre organisation ou compte dans ce système connecté. |
| `sourceID` |  | Identifiant de la personne dans ce système connecté. |
| `identityNamespace` |  | Libellé identifiant le type d’identifiant de personne supplémentaire. |
| `identityValue` |  | Valeur de l’identité secondaire. |
| `customAttributes` |  | Noms et valeurs de champs personnalisés stockés ensemble sous forme de texte. |
| `isDeleted` |  | Indique si cet enregistrement est marqué comme supprimé. |
| `lastUpdatedDate` |  | Heure de la dernière modification. |

## `AJOB2B-1_5_4-account_person`

Chaque enregistrement associe un profil de compte à un profil de personne. Utilisez-le pour créer des rapports sur les relations entre les jeux de données de compte et de profil de personne.

**Format:** Format d’enregistrement associé

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | ID d’enregistrement de la relation compte-personne (utilisez la valeur complète). |
| `accountID` | Correspond à `AJOB2B-1_5_4-account_relational` (`_id`) | Identifiant complet du compte (références `account_relational._id`). |
| `personID` | Correspond à `AJOB2B-1_5_4-person_relational` (`_id`) | Identifiant complet de la personne (références `person_relational._id`). |
| `createdDate` |  | Lors de la création de la relation compte-personne. |
| `isDeleted` |  | Indique si cet enregistrement est marqué comme supprimé. |
| `lastUpdatedDate` |  | Heure de la dernière modification. |

## `AJOB2B-1_5_4-person_event_relational`

Chaque enregistrement décrit une activité de personne prise en charge, telle que l’affichage d’une page web, l’interaction avec un e-mail ou le déplacement dans un parcours. Utilisez `eventType` et `activityTypeID` pour comprendre ce qui s’est passé. Seuls les détails relatifs à ce type d’activité sont renseignés.

**Format:** Format d’enregistrement associé

La liste de champs suivante couvre tous les types d’activités pris en charge. Un enregistrement individuel contient uniquement les détails qui s’appliquent à son activité.

>[!NOTE]
>
>**Disponibilité :** certaines activités peuvent avoir un `_id` vide. Ne supposez pas que chaque activité possède un identifiant d’enregistrement utilisable. Le jeu de données ne garantit pas un historique d’activités complet.

Les détails du parcours (`journeyID`, `journeyNodeID`, `journeyStepID` et champs similaires) sont fournis pour les activités de parcours (`person.journeyAdd`, `person.journeyRemove`, `person.journeyStart`, `person.journeyEnd`, `person.journeyNodeTransition`, `person.journeySplitNode`) et pour `person.attributeChanged` activités associées à une étape de parcours « Mettre à jour le profil de la personne ».

Les champs de changement d’attribut (`attributeName`, `attributeID`, `attributeNewValue`, `attributeOldValue`, `attributeChangeReason`) sont renseignés pour `person.attributeChanged` uniquement.

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id` | ID d’enregistrement | Identifiant de l’activité, le cas échéant. |
| `timestamp` |  | Moment où l’activité s’est produite. |
| `eventType` |  | Libellé de l’activité. Valeurs : `web.webpagedetails.pageViews`, `web.formFilledOut`, `web.webinteraction.linkClicks`, `directMarketing.emailSent`, `directMarketing.emailDelivered`, `directMarketing.emailBounced`, `directMarketing.emailBouncedSoft`, `directMarketing.emailUnsubscribed`, `directMarketing.emailOpened`, `directMarketing.emailClicked`, `leadOperation.interestingMoment`, `person.attributeChanged`, `person.journeyAdd`, `person.journeyRemove`, `person.journeyStart`, `person.journeyEnd`, `person.journeyNodeTransition`, `person.journeySplitNode`,,. |
| `activityTypeID` |  | Code de l’activité. Utilisez-le avec des `eventType` pour distinguer les activités qui partagent le même libellé d’événement. |
| `personID` | Correspond à `AJOB2B-1_5_4-person_relational` (`_id`) | Identifiant de personne complet utilisé pour faire correspondre l’activité à un enregistrement de personne. |
| `journeyID` | Correspond à `AJOB2B-1_5_4-person_journey` (`_id`) | Identifiant complet du parcours. Vide pour les activités non associées à un parcours. |
| `journeyNodeID` | Correspond à `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identifiant complet de la parcours-étape. Vide pour les activités non associées à un parcours. |
| `previousJourneyNodeID` | Correspond à `AJOB2B-1_5_4-person_journey_node` (`_id`) | Nœud de parcours précédent (renseigné pour `person.journeyNodeTransition` et `person.journeySplitNode`). |
| `newJourneyNodeID` | Correspond à `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identifiant du nœud du parcours de destination (`person.journeyNodeTransition` et `person.journeySplitNode`). Est généralement égal à `journeyNodeID`. |
| `journeyStepID` |  | Identifiant de l’étape de parcours associée à l’activité. |
| `journeyChoiceNumber` |  | Numéro à choix partagé pour `person.journeySplitNode`. Enregistré en nombre entier. |
| `journeyEntryCount` |  | Nombre de fois où cette personne a accédé au parcours (renseigné sur les événements d’ajout/de démarrage de parcours). Enregistré en nombre entier. |
| `journeyProgramID` | Aucun jeu de données de programme marketing distinct dans ce guide | Identifiant du programme marketing associé à l’activité de parcours. |
| `activitySource` |  | Nom du produit ou de l’action associée à l’activité. |
| `campaignID` |  | [!DNL Marketo Engage] l’identifiant de campagne lorsque l’activité est attribuée à la campagne. |
| `attributeName` |  | Nom du champ modifié (`person.attributeChanged` uniquement). |
| `attributeID` |  | Identifiant du champ qui a été modifié (`person.attributeChanged` uniquement). |
| `attributeNewValue` |  | Nouvelle valeur de champ, enregistrée en tant que texte (`person.attributeChanged` uniquement). |
| `attributeOldValue` |  | Valeur du champ précédent, enregistrée en tant que texte (`person.attributeChanged` uniquement). |
| `attributeChangeReason` |  | Libellé du motif de la modification (`person.attributeChanged` uniquement). |
| `assetID` |  | Identifiant du contenu, de la page ou du formulaire associé à l’e-mail. |
| `assetName` |  | Nom du contenu associé. |
| `recipientEmail` |  | Adresse email du destinataire, le cas échéant. Uniquement renseigné pour les codes d’activité **27** (soft bounce) et **48** (soft bounce d’e-mail de vente) ; vide pour les autres activités d’e-mail. Pour ces activités, recherchez l’enregistrement de personne à l’aide de `personID`. `assetName` identifie le contenu de l’e-mail, et non l’adresse du destinataire. |
| `bouncedCode` |  | Code de catégorie de rebond (emailBouncé / emailBouncéSoft uniquement). |
| `bouncedDetails` |  | Raison détaillée du bounce (emailBouncé / emailBouncéSoft uniquement). |
| `isMobileDevice` |  | Si un appareil mobile a été enregistré pour une ouverture d’e-mail ou un clic. |
| `deviceModel` |  | Modèle d’appareil (emailOpened / emailClicked uniquement). |
| `operatingSystem` |  | Système d&#39;exploitation (emailOpened / emailClicked uniquement). |
| `userAgent` |  | Informations sur le navigateur ou le client de messagerie, pour les ouvertures d’e-mail, les clics sur e-mail et les activités web. |
| `clickedLinkUrl` |  | URL du lien d’e-mail cliqué (emailClicked uniquement). |
| `webPageUrl` |  | URL de la page web (`web.webpagedetails.pageViews` uniquement). |
| `queryParameters` |  | Informations supplémentaires dans une adresse web pour les pages vues, les envois de formulaire ou les clics sur des liens web. |
| `webPageID` |  | ID de la page web [!DNL Marketo Engage] (pageViews, formFilledOut, linkClicks). |
| `referrerUrl` |  | URL du référent (pageViews, formFilledOut, linkClicks). |
| `formID` |  | ID de formulaire [!DNL Marketo Engage] (`web.formFilledOut` uniquement). |
| `linkID` |  | ID de lien [!DNL Marketo Engage] (`web.webinteraction.linkClicks` uniquement). |
| `interestingMomentDate` |  | Date du moment (`leadOperation.interestingMoment` uniquement). |
| `interestingMomentDescription` |  | Description en texte libre (interestMoment uniquement). |
| `interestingMomentSource` |  | Produit ou campagne associé (moment intéressant uniquement). |
| `interestingMomentType` |  | Catégorie / type (moment intéressant uniquement). |
| `isDeleted` |  | Indique si cet enregistrement est marqué comme supprimé. |
| `lastUpdatedDate` |  | Heure de la dernière modification. |

### Référence du champ par type d’activité

Les tableaux suivants indiquent les détails qui s’appliquent à chaque activité. Les autres détails sont vides. Certaines activités partagent le même libellé `eventType` : les codes 8 et 48 utilisent tous les deux `directMarketing.emailBounced`. Utilisez des `activityTypeID` pour les distinguer.

#### Page web consultée (`web.webpagedetails.pageViews`) (Type d’activité 1)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID d’enregistrement : `_id` ; `personID` correspond à `AJOB2B-1_5_4-person_relational` (`_id`) | Champs communs. |
| `assetID` |  | ID de page. |
| `assetName` |  | Nom de la page. |
| `webPageUrl` |  | URL de la page. |
| `queryParameters` |  | Informations supplémentaires incluses dans une adresse web. |
| `webPageID` |  | ID de la page web [!DNL Marketo Engage]. |
| `referrerUrl` |  | URL du référent. |
| `userAgent` |  | Informations sur le navigateur ou le client de messagerie. |
| `isDeleted`, `lastUpdatedDate` |  | Champs communs. |

#### Formulaire soumis (`web.formFilledOut`) (Type d&#39;activité 2)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID d’enregistrement : `_id` ; `personID` correspond à `AJOB2B-1_5_4-person_relational` (`_id`) | Champs communs. |
| `assetID` |  | ID du formulaire. |
| `assetName` |  | Nom du formulaire. |
| `formID` |  | ID de formulaire [!DNL Marketo Engage]. |
| `queryParameters` |  | Informations supplémentaires incluses dans une adresse web. |
| `webPageID` |  | ID de la page web [!DNL Marketo Engage]. |
| `referrerUrl` |  | URL du référent. |
| `userAgent` |  | Informations sur le navigateur ou le client de messagerie. |
| `isDeleted`, `lastUpdatedDate` |  | Champs communs. |

#### Lien web sur lequel l’utilisateur a cliqué (`web.webinteraction.linkClicks`) (Type d’activité 3)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID d’enregistrement : `_id` ; `personID` correspond à `AJOB2B-1_5_4-person_relational` (`_id`) | Champs communs. |
| `assetID` |  | Identifiant de l’interaction/du lien. |
| `assetName` |  | URL de destination. |
| `linkID` |  | ID du lien [!DNL Marketo Engage]. |
| `queryParameters` |  | Informations supplémentaires incluses dans une adresse web. |
| `webPageID` |  | ID de la page web [!DNL Marketo Engage]. |
| `referrerUrl` |  | URL du référent. |
| `userAgent` |  | Informations sur le navigateur ou le client de messagerie. |
| `isDeleted`, `lastUpdatedDate` |  | Champs communs. |

#### E-mail envoyé (`directMarketing.emailSent`) (types d’activités 6, 39)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID d’enregistrement : `_id` ; `personID` correspond à `AJOB2B-1_5_4-person_relational` (`_id`) | Champs communs. |
| `assetID` |  | ID de publipostage. |
| `assetName` |  | Nom du publipostage. |
| `campaignID` |  | [!DNL Marketo Engage] l’identifiant de campagne, lorsqu’il est attribué par la campagne. |
| `isDeleted`, `lastUpdatedDate` |  | Champs communs. |

#### Email diffusé (`directMarketing.emailDelivered`) (Types d’activités 7, 45)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID d’enregistrement : `_id` ; `personID` correspond à `AJOB2B-1_5_4-person_relational` (`_id`) | Champs communs. |
| `assetID` |  | ID de publipostage. |
| `assetName` |  | Nom du publipostage. |
| `campaignID` |  | [!DNL Marketo Engage] l’identifiant de campagne, lorsqu’il est attribué par la campagne. |
| `isDeleted`, `lastUpdatedDate` |  | Champs communs. |

#### Désabonnement des e-mails (`directMarketing.emailUnsubscribed`) (Type d&#39;activité 9)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID d’enregistrement : `_id` ; `personID` correspond à `AJOB2B-1_5_4-person_relational` (`_id`) | Champs communs. |
| `assetID` |  | ID de publipostage. |
| `assetName` |  | Nom du publipostage. |
| `campaignID` |  | [!DNL Marketo Engage] l’identifiant de campagne, lorsqu’il est attribué par la campagne. |
| `isDeleted`, `lastUpdatedDate` |  | Champs communs. |

#### E-mail ouvert (`directMarketing.emailOpened`) (Types d’activités 10, 40)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID d’enregistrement : `_id` ; `personID` correspond à `AJOB2B-1_5_4-person_relational` (`_id`) | Champs communs. |
| `assetID` |  | ID de publipostage. |
| `assetName` |  | Nom du publipostage. |
| `isMobileDevice` |  | Indique si un appareil mobile a été enregistré pour l’activité. |
| `deviceModel` |  | Modèle d’appareil. |
| `operatingSystem` |  | Système d’exploitation. |
| `userAgent` |  | Informations sur le navigateur ou le client de messagerie. |
| `campaignID` |  | [!DNL Marketo Engage] l’identifiant de campagne, lorsqu’il est attribué par la campagne. |
| `isDeleted`, `lastUpdatedDate` |  | Champs communs. |

#### Lien d’e-mail sur lequel l’utilisateur a cliqué (`directMarketing.emailClicked`) (Types d’activités 11, 41)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID d’enregistrement : `_id` ; `personID` correspond à `AJOB2B-1_5_4-person_relational` (`_id`) | Champs communs. |
| `assetID` |  | ID de publipostage. |
| `assetName` |  | Nom du publipostage. |
| `clickedLinkUrl` |  | URL du lien cliqué. |
| `isMobileDevice` |  | Indique si un appareil mobile a été enregistré pour l’activité. |
| `deviceModel` |  | Modèle d’appareil. |
| `operatingSystem` |  | Système d’exploitation. |
| `userAgent` |  | Informations sur le navigateur ou le client de messagerie. |
| `campaignID` |  | [!DNL Marketo Engage] l’identifiant de campagne, lorsqu’il est attribué par la campagne. |
| `isDeleted`, `lastUpdatedDate` |  | Champs communs. |

#### Email rebond (`directMarketing.emailBounced`) : hard bounce (Type d&#39;activité 8)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID d’enregistrement : `_id` ; `personID` correspond à `AJOB2B-1_5_4-person_relational` (`_id`) | Champs communs. |
| `assetID` |  | ID de publipostage. |
| `assetName` |  | Nom du publipostage. |
| `bouncedCode` |  | Code catégorie de rebond. |
| `bouncedDetails` |  | Raison détaillée du bounce. |
| `campaignID` |  | [!DNL Marketo Engage] l’identifiant de campagne, lorsqu’il est attribué par la campagne. |
| `isDeleted`, `lastUpdatedDate` |  | Champs communs. |

Cette activité partage le libellé `directMarketing.emailBounced` avec le code d&#39;activité 48, mais `recipientEmail` est vide pour le code 8. Utilisez `activityTypeID` pour distinguer les deux.

#### Email bounce (`directMarketing.emailBounced`) : soft bounce d&#39;email de vente (type d&#39;activité 48)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID d’enregistrement : `_id` ; `personID` correspond à `AJOB2B-1_5_4-person_relational` (`_id`) | Champs communs. |
| `assetID` |  | ID de publipostage. |
| `assetName` |  | Nom du publipostage. |
| `recipientEmail` |  | Adresse e-mail du destinataire. |
| `bouncedCode` |  | Code catégorie de rebond. |
| `bouncedDetails` |  | Raison détaillée du bounce. |
| `campaignID` |  | [!DNL Marketo Engage] l’identifiant de campagne, lorsqu’il est attribué par la campagne. |
| `isDeleted`, `lastUpdatedDate` |  | Champs communs. |

#### Email soft bounce (`directMarketing.emailBouncedSoft`) (Type d&#39;activité 27)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID d’enregistrement : `_id` ; `personID` correspond à `AJOB2B-1_5_4-person_relational` (`_id`) | Champs communs. |
| `assetID` |  | ID de publipostage. |
| `assetName` |  | Nom du publipostage. |
| `recipientEmail` |  | Adresse e-mail du destinataire. |
| `bouncedCode` |  | Code catégorie de rebond. |
| `bouncedDetails` |  | Raison détaillée du bounce. |
| `campaignID` |  | [!DNL Marketo Engage] l’identifiant de campagne, lorsqu’il est attribué par la campagne. |
| `isDeleted`, `lastUpdatedDate` |  | Champs communs. |

#### Moment intéressant enregistré (`leadOperation.interestingMoment`) (Type d&#39;activité 46)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID d’enregistrement : `_id` ; `personID` correspond à `AJOB2B-1_5_4-person_relational` (`_id`) | Champs communs. |
| `interestingMomentDate` |  | Date/heure du moment. |
| `interestingMomentDescription` |  | Description en texte libre. |
| `interestingMomentSource` |  | Nom du produit ou de la campagne associé. |
| `interestingMomentType` |  | Tapez le libellé. |
| `isDeleted`, `lastUpdatedDate` |  | Champs communs. |

`assetID` et `assetName` ne sont pas renseignés pour ce type d’activité.

#### Champ de personne modifié (`person.attributeChanged`) (Type d’activité 13)

Inclus uniquement lorsque la modification est associée à un parcours, comme une étape « Mettre à jour le profil de la personne ». Les modifications en dehors d’un parcours ne sont pas incluses.

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID d’enregistrement : `_id` ; `personID` correspond à `AJOB2B-1_5_4-person_relational` (`_id`) | Champs communs. |
| `attributeName` |  | Nom du champ modifié. |
| `attributeID` |  | Identifiant du champ modifié. |
| `attributeNewValue` |  | Nouvelle valeur de champ, enregistrée en tant que texte. |
| `attributeOldValue` |  | Valeur du champ précédent, enregistrée en tant que texte. |
| `attributeChangeReason` |  | Libellé du motif de la modification. |
| `journeyID` | Correspond à `AJOB2B-1_5_4-person_journey` (`_id`) | Identifiant du parcours. |
| `journeyNodeID` | Correspond à `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identifiant du nœud du parcours. |
| `journeyStepID` |  | Identifiant de l’étape de parcours. |
| `journeyProgramID` | Aucun jeu de données de programme marketing distinct dans ce guide | ID du programme de parcours. |
| `activitySource` |  | Produit ou action associé à l’activité. |
| `isDeleted`, `lastUpdatedDate` |  | Champs communs. |

#### Personne ajoutée à ou ayant démarré un parcours (`person.journeyAdd`, `person.journeyStart`) (Types d’activités 182, 184)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID d’enregistrement : `_id` ; `personID` correspond à `AJOB2B-1_5_4-person_relational` (`_id`) | Champs communs. |
| `journeyID` | Correspond à `AJOB2B-1_5_4-person_journey` (`_id`) | Identifiant du parcours. |
| `journeyNodeID` | Correspond à `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identifiant du nœud du parcours. |
| `journeyStepID` |  | Identifiant de l’étape de parcours. |
| `journeyEntryCount` |  | Nombre de fois où cette personne est entrée dans le parcours. |
| `journeyProgramID` | Aucun jeu de données de programme marketing distinct dans ce guide | ID du programme de parcours. |
| `activitySource` |  | Produit ou action associé à l’activité. |
| `isDeleted`, `lastUpdatedDate` |  | Champs communs. |

#### Personne supprimée d’un parcours ou à laquelle il a été mis fin (`person.journeyRemove`, `person.journeyEnd`) (Types d’activités 183, 185)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID d’enregistrement : `_id` ; `personID` correspond à `AJOB2B-1_5_4-person_relational` (`_id`) | Champs communs. |
| `journeyID` | Correspond à `AJOB2B-1_5_4-person_journey` (`_id`) | Identifiant du parcours. |
| `journeyNodeID` | Correspond à `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identifiant du nœud du parcours. |
| `journeyStepID` |  | Identifiant de l’étape de parcours. |
| `journeyProgramID` | Aucun jeu de données de programme marketing distinct dans ce guide | ID du programme de parcours. |
| `activitySource` |  | Produit ou action associé à l’activité. |
| `isDeleted`, `lastUpdatedDate` |  | Champs communs. |

#### Personne a suivi une branche de parcours (`person.journeySplitNode`) (Type d’activité 186)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID d’enregistrement : `_id` ; `personID` correspond à `AJOB2B-1_5_4-person_relational` (`_id`) | Champs communs. |
| `journeyID` | Correspond à `AJOB2B-1_5_4-person_journey` (`_id`) | Identifiant du parcours. |
| `journeyNodeID` | Correspond à `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identifiant du nœud de parcours (nœud de partage). |
| `previousJourneyNodeID` | Correspond à `AJOB2B-1_5_4-person_journey_node` (`_id`) | Nœud dans lequel se trouvait la personne avant la division. |
| `newJourneyNodeID` | Correspond à `AJOB2B-1_5_4-person_journey_node` (`_id`) | Nœud vers lequel la personne a été déplacée (généralement `journeyNodeID`). |
| `journeyStepID` |  | Identifiant de l’étape de parcours. |
| `journeyChoiceNumber` |  | Quelle branche de la division a été prise. |
| `journeyProgramID` | Aucun jeu de données de programme marketing distinct dans ce guide | ID du programme de parcours. |
| `activitySource` |  | Produit ou action associé à l’activité. |
| `isDeleted`, `lastUpdatedDate` |  | Champs communs. |

#### Personne déplacée entre les étapes de parcours (`person.journeyNodeTransition`) (Type d’activité 600)

| Nom du champ | Relations | Ce que ça vous dit |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | ID d’enregistrement : `_id` ; `personID` correspond à `AJOB2B-1_5_4-person_relational` (`_id`) | Champs communs. |
| `journeyID` | Correspond à `AJOB2B-1_5_4-person_journey` (`_id`) | Identifiant du parcours. |
| `journeyNodeID` | Correspond à `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identifiant du nœud de parcours courant. |
| `previousJourneyNodeID` | Correspond à `AJOB2B-1_5_4-person_journey_node` (`_id`) | Nœud depuis lequel la personne a effectué la transition. |
| `newJourneyNodeID` | Correspond à `AJOB2B-1_5_4-person_journey_node` (`_id`) | Nœud vers lequel la personne a effectué la transition (est généralement égal à `journeyNodeID`). |
| `journeyStepID` |  | Identifiant de l’étape de parcours. |
| `journeyProgramID` | Aucun jeu de données de programme marketing distinct dans ce guide | ID du programme de parcours. |
| `activitySource` |  | Produit ou action associé à l’activité. |
| `isDeleted`, `lastUpdatedDate` |  | Champs communs. |

## Jeux de données détenus par le client {#customer-owned-datasets}

Votre entreprise peut utiliser ses propres jeux de données [!DNL Experience Platform] pour les comptes ou les personnes. Une fois configurés, [!DNL Adobe Journey Optimizer B2B Edition] pouvez ajouter des informations à ces jeux de données au lieu de créer un autre jeu de données de compte ou de personne.

Leurs noms et champs disponibles dépendent de la configuration de votre entreprise. Utilisez l’identifiant de compte ou de personne configuré pour reconnaître les enregistrements correspondants. Disposer d’enregistrements dans ces jeux de données ne les rend pas automatiquement disponibles pour les audiences. La disponibilité dépend de votre configuration de [!DNL Experience Platform].
