---
title: Requêtes de jeu de données
description: Découvrez comment utiliser des exemples de requête SQL dans Query Service pour analyser les données de compte, de groupe d’achats, de personne et de parcours exportées par Adobe Journey Optimizer B2B Edition.
feature: Reporting, Data Management
role: Admin, Developer
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
    internal-label: Experience Platform
feature_v2:
  - id: f2da1b69-6919-4386-a5d2-9c7b5c9033db
    internal-label: Data management
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
source-git-commit: 6db81a0b993f450a3ff448dcb4c417e3e81ec70a
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 1%
---

# Requêtes de jeu de données

Recherchez des exemples de requête SQL prêts à l’emploi pour analyser les données de compte, de personne, de groupe d’achats et de parcours qui [!DNL Adobe Journey Optimizer B2B Edition] exportées vers [!DNL Adobe Experience Platform]. Pour générer des rapports sur les comptes, les groupes d&#39;achats, l&#39;engagement par e-mail et l&#39;activité de parcours, exécutez les requêtes dans [!DNL Query Service].

Pour les descriptions des jeux de données et des champs utilisés dans ces requêtes, voir [Jeux de données exportés](./aep-exported-datasets.md).

## Conditions préalables {#prerequisites}

Avant d’exécuter une requête sur cette page, vérifiez que vous disposez des éléments suivants :

* **Accès à [!DNL Query Service] :** vous devez avoir accès à [Query Service](https://experienceleague.adobe.com/fr/docs/experience-platform/query/home){target="_blank"} dans votre sandbox [!DNL Experience Platform].
* **Jeux de données disponibles :** les requêtes ciblent les jeux de données [!DNL Journey Optimizer B2B Edition] exportés. Dans votre sandbox, accédez à **[!UICONTROL Jeux de données]** et vérifiez que les jeux de données existent et contiennent des données.
* **Valeurs des champs de schéma :** assurez-vous que les champs de vos requêtes possèdent des valeurs dans le schéma correspondant. Les champs vides ne renvoient aucun résultat et ne produisent aucune erreur.

>[!NOTE]
>
>Les exemples utilisent des noms de table courts, tels que `account_table` et `person_activity_table`. Remplacez chaque nom de table par le nom du jeu de données correspondant dans votre sandbox. Si un nom de jeu de données contient des tirets, placez-le entre guillemets. Remplacez les valeurs d’espace réservé, telles que `Example Company` et `PASTE_COMPLETE_JOURNEY_ID_HERE`, par les valeurs de votre environnement.

## Exécuter une requête {#run}

Pour exécuter un exemple sur cette page, procédez comme suit :

1. Dans [!DNL Experience Platform], sélectionnez **[!UICONTROL Query Service]** > **[!UICONTROL Queries]**.
1. Collez l’exemple dans le requêteur, puis remplacez les noms du tableau et les valeurs des espaces réservés.
1. Sélectionnez **[!UICONTROL Exécuter]**.

Les exemples qui filtrent par date utilisent les 30 derniers jours. Pour modifier la période, modifiez la valeur de la `INTERVAL '30' DAY`.

## Choisir une requête

Utilisez le tableau suivant pour choisir une requête pour votre tâche de création de rapports.

| Je veux | Accéder à |
|---|---|
| Consulter les noms de compte, les secteurs d’activité et les emplacements | [Consulter les détails du compte](#account-details) |
| Comparer les groupes d&#39;achats par engagement | [Comparer l&#39;engagement du groupe d&#39;achat](#buying-group-engagement) |
| Rechercher les personnes associées à un compte | [Trouver des personnes dans un compte](#account-people) |
| Suivre les modifications apportées au statut du groupe d&#39;achat | [Vérifier les modifications du statut du groupe d&#39;achats](#buying-group-status-changes) |
| Rechercher les personnes ayant cliqué sur un e-mail | [Rechercher les personnes ayant cliqué sur un e-mail](#email-clicks) |
| Comparer les activités récentes par type | [Comparer l’activité récente d’une personne](#person-activity) |
| Comparer les parcours de compte par taille | [Comparer les comptes par parcours &#x200B;](#account-journey-counts) |
| Liste des comptes dans un parcours | [Liste des comptes dans un parcours &#x200B;](#journey-accounts) |
| Suivi de l’activité quotidienne du parcours de compte | [Suivi de l’activité quotidienne du compte](#account-daily-activity) |
| Recherche de l’historique d’un compte dans un parcours | [Vérifier la chronologie d’un parcours de compte](#account-timeline) |
| Comparer les parcours de personnes par taille et statut | [Comparer le nombre de personnes par parcours &#x200B;](#person-journey-counts) |
| Liste des personnes d&#39;un parcours | [Liste des personnes dans un parcours &#x200B;](#journey-people) |
| Voir où se trouvent les personnes dans un parcours | [Comparer le nombre de personnes par étape](#person-step-counts) |
| Suivi de l’activité récente d’un parcours de personne | [Suivre les activités récentes du parcours &#x200B;](#person-journey-activity) |
| Recherche de l’historique d’une personne dans un parcours | [Vérifier la chronologie du parcours d’une personne](#person-timeline) |

## Requêtes de compte et de groupe d&#39;achat

Utilisez ces requêtes pour consulter les comptes, les groupes d&#39;achats et les personnes disponibles pour la création de rapports.

### Consulter les détails du compte {#account-details}

Examinez les noms de compte, les secteurs d’activité, les emplacements et les tailles d’entreprise pour comprendre les comptes disponibles pour la création de rapports.

```sql
SELECT
a._id AS accountID,
a.accountName,
a.industry,
a.country,
a.numberOfEmployees
FROM account_table a
WHERE a.isDeleted = FALSE
ORDER BY a.accountName
LIMIT 100;
```

### Comparer l&#39;engagement du groupe d&#39;achat {#buying-group-engagement}

Comparez les groupes d’achats par score d’engagement enregistré, ainsi que par exhaustivité et intérêt pour la solution.

```sql
SELECT
bg._id AS buyingGroupID,
bg.buyingGroupName,
bg.engagementScore,
bg.completenessScore,
bg.solutionInterest,
bg.buyingGroupStatus
FROM buying_group_table bg
WHERE bg.isDeleted = FALSE
ORDER BY bg.engagementScore DESC NULLS LAST, bg.buyingGroupName
LIMIT 100;
```

### Trouver des personnes dans un compte {#account-people}

Recherchez les personnes et les titres de poste associés à un compte pour comprendre ses contacts. Remplacez `Example Company` par un nom de compte de votre sandbox.

```sql
SELECT DISTINCT
a._id AS accountID,
a.accountName,
p._id AS personID,
p.firstName,
p.lastName,
p.email,
p.jobTitle
FROM account_member_table m
JOIN account_table a ON m.accountID = a._id
JOIN person_table p ON m.personID = p._id
WHERE m.isDeleted = FALSE
AND a.isDeleted = FALSE
AND p.isDeleted = FALSE
AND a.accountName = 'Example Company'
ORDER BY p.lastName, p.firstName
LIMIT 100;
```

### Vérifier les modifications du statut du groupe d&#39;achats {#buying-group-status-changes}

Examinez les changements de statut des groupes d&#39;achats au cours des 30 derniers jours pour comprendre comment les groupes changent au fil du temps.

```sql
SELECT
bg._id AS buyingGroupID,
bg.buyingGroupName,
e.timestamp AS changedAt,
e.newStatus
FROM buying_group_event_table e
JOIN buying_group_table bg ON e.buyingGroupID = bg._id
WHERE bg.isDeleted = FALSE
AND e.eventType = 'buyingGroup.changeStatus'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY e.timestamp DESC
LIMIT 100;
```

## Requêtes d’engagement des personnes

Utilisez ces requêtes pour consulter l’engagement des e-mails et d’autres activités de personne enregistrées.

### Rechercher les personnes ayant cliqué sur un e-mail {#email-clicks}

Pour consulter l’engagement récent des e-mails, identifiez les personnes ayant enregistré des clics sur les e-mails au cours des 30 derniers jours.

```sql
SELECT DISTINCT
p._id AS personID,
p.firstName,
p.lastName,
p.email
FROM person_activity_table e
JOIN person_table p ON e.personID = p._id
WHERE e.isDeleted = FALSE
AND p.isDeleted = FALSE
AND e.eventType = 'directMarketing.emailClicked'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY p.lastName, p.firstName
LIMIT 100;
```

### Comparer l’activité récente d’une personne {#person-activity}

Comparez les types d’activités enregistrés et le nombre de personnes impliquées pour comprendre l’engagement récent.

```sql
SELECT
e.eventType,
COUNT(*) AS recordedRows,
COUNT(DISTINCT e.personID) AS distinctPeople
FROM person_activity_table e
WHERE e.isDeleted = FALSE
AND e.personID IS NOT NULL
AND e.personID <> ''
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
GROUP BY e.eventType
ORDER BY recordedRows DESC
LIMIT 100;
```

## Requêtes de parcours de compte

Utilisez ces requêtes pour analyser les parcours de compte. Remplacez `PASTE_COMPLETE_JOURNEY_ID_HERE` par la valeur `_id` du parcours de compte et `PASTE_COMPLETE_ACCOUNT_ID_HERE` par la valeur `_id` du compte.

### Comparer les comptes par parcours {#account-journey-counts}

Comparez les parcours de compte par statut et le nombre d’abonnements enregistrés pour identifier les parcours ayant les plus grandes populations de comptes.

```sql
SELECT
j._id AS journeyID,
j.accountJourneyName,
j.accountJourneyStatus,
COUNT(DISTINCT m.accountID) AS accountsWithRecordedMembership
FROM account_journey_table j
LEFT JOIN account_journey_member_table m
ON m.journeyID = j._id
AND m.isDeleted = FALSE
AND m.accountID <> ''
WHERE j.isDeleted = FALSE
GROUP BY j._id, j.accountJourneyName, j.accountJourneyStatus
ORDER BY accountsWithRecordedMembership DESC, j.accountJourneyName
LIMIT 100;
```

### Liste des comptes dans un parcours {#journey-accounts}

Examinez les comptes associés à un parcours particulier, y compris leurs secteurs d’activité et pays.

```sql
SELECT DISTINCT
a._id AS accountID,
a.accountName,
a.industry,
a.country
FROM account_journey_member_table m
JOIN account_table a ON m.accountID = a._id
WHERE m.isDeleted = FALSE
AND a.isDeleted = FALSE
AND m.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
ORDER BY a.accountName, accountID
LIMIT 100;
```

### Suivi de l’activité quotidienne du compte {#account-daily-activity}

Effectuez le suivi des ajouts, des suppressions et des modifications d’étape quotidiens de comptes pour comprendre l’activité dans un parcours au cours des 30 derniers jours.

```sql
SELECT
CAST(e.timestamp AS DATE) AS activityDate,
e.eventType,
COUNT(*) AS recordedRows,
COUNT(DISTINCT e.accountID) AS distinctAccounts
FROM account_activity_table e
WHERE e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.accountID IS NOT NULL
AND e.accountID <> ''
AND e.eventType IN (
'account.addAccountToJourney',
'account.removeAccountFromJourney',
'account.changeAccountJourneyNode'
)
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
GROUP BY CAST(e.timestamp AS DATE), e.eventType
ORDER BY activityDate DESC, e.eventType
LIMIT 100;
```

### Vérifier la chronologie d’un parcours de compte {#account-timeline}

Examinez l’historique des parcours récents d’un compte en examinant ses événements enregistrés et les étapes de parcours.

```sql
SELECT
e.timestamp AS activityAt,
e.eventType,
e.journeyNodeID,
n.nodeType,
e.previousJourneyNodeID,
e.buyingGroupID
FROM account_activity_table e
LEFT JOIN account_journey_node_table n
ON e.journeyNodeID = n._id
AND e.journeyID = n.accountJourneyID
AND n.isDeleted = FALSE
WHERE e.accountID = 'PASTE_COMPLETE_ACCOUNT_ID_HERE'
AND e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY e.timestamp DESC
LIMIT 100;
```

## Requêtes de parcours de personne.

Utilisez ces requêtes pour analyser les parcours de personne. Remplacez `PASTE_COMPLETE_JOURNEY_ID_HERE` par la valeur `_id` du parcours de la personne et `PASTE_COMPLETE_PERSON_ID_HERE` par la valeur `_id` de la personne.

### Comparer les nombres de personnes par parcours {#person-journey-counts}

Comparez les parcours des personnes par nombre d’adhésions enregistrées, statut et dates afin de connaître leur taille et leur cycle de vie.

```sql
SELECT
j._id AS journeyID,
j.personJourneyName,
j.personJourneyStatus,
j.startDate,
j.endDate,
COUNT(DISTINCT m.personID) AS peopleWithRecordedMembership
FROM person_journey_table j
LEFT JOIN person_journey_member_table m
ON m.journeyID = j._id
AND m.isDeleted = FALSE
AND m.personID <> ''
WHERE j.isDeleted = FALSE
GROUP BY
j._id,
j.personJourneyName,
j.personJourneyStatus,
j.startDate,
j.endDate
ORDER BY peopleWithRecordedMembership DESC, j.personJourneyName
LIMIT 100;
```

### Liste des personnes dans un parcours {#journey-people}

Vérifiez qui est associé à un parcours, quand il a été saisi pour la dernière fois et à quelle fréquence.

```sql
SELECT DISTINCT
m.personID,
p.firstName,
p.lastName,
p.email,
m.membershipDate,
m.lastEntryDate,
m.entryCount,
m.reentryOpensAt,
m.journeyNodeID
FROM person_journey_member_table m
LEFT JOIN person_table p
ON m.personID = p._id
AND p.isDeleted = FALSE
WHERE m.isDeleted = FALSE
AND m.personID IS NOT NULL
AND m.personID <> ''
AND m.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
ORDER BY m.lastEntryDate DESC NULLS LAST, m.personID
LIMIT 100;
```

### Comparer les nombres de personnes par étape {#person-step-counts}

Découvrez comment les personnes sont réparties entre les étapes enregistrées dans leurs abonnements au parcours.

```sql
SELECT
m.journeyNodeID,
n.nodeType,
COUNT(DISTINCT m.personID) AS peopleWithRecordedStep
FROM person_journey_member_table m
LEFT JOIN person_journey_node_table n
ON m.journeyNodeID = n._id
AND m.journeyID = n.personJourneyID
AND n.isDeleted = FALSE
WHERE m.isDeleted = FALSE
AND m.personID IS NOT NULL
AND m.personID <> ''
AND m.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
GROUP BY m.journeyNodeID, n.nodeType
ORDER BY peopleWithRecordedStep DESC, m.journeyNodeID
LIMIT 100;
```

### Suivi des activités de parcours récentes {#person-journey-activity}

Comparez les démarrages, les fins et les transitions de parcours enregistrés pour comprendre l’activité des personnes dans un parcours au cours des 30 derniers jours.

```sql
SELECT
e.eventType,
COUNT(*) AS recordedRows,
COUNT(DISTINCT e.personID) AS distinctPeople
FROM person_activity_table e
WHERE e.isDeleted = FALSE
AND e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.personID IS NOT NULL
AND e.personID <> ''
AND e.eventType IN (
'person.journeyAdd',
'person.journeyRemove',
'person.journeyStart',
'person.journeyEnd',
'person.journeyNodeTransition',
'person.journeySplitNode'
)
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
GROUP BY e.eventType
ORDER BY recordedRows DESC, e.eventType
LIMIT 100;
```

### Vérifier la chronologie du parcours d’une personne {#person-timeline}

Examinez l’historique des parcours récents d’une personne, y compris les transitions d’étape, les choix de division et les mises à jour de profil attribuées au parcours.

```sql
SELECT
e.timestamp AS activityAt,
e.eventType,
e.journeyNodeID,
e.previousJourneyNodeID,
e.newJourneyNodeID,
e.journeyChoiceNumber,
e.journeyEntryCount,
e.attributeName,
e.attributeOldValue,
e.attributeNewValue
FROM person_activity_table e
WHERE e.isDeleted = FALSE
AND e.personID = 'PASTE_COMPLETE_PERSON_ID_HERE'
AND e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY e.timestamp DESC
LIMIT 100;
```
