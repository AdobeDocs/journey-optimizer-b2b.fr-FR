---
title: Disponibilité des données et synchronisation temporelle
description: Découvrez la vitesse à laquelle les modifications de données apparaissent dans les parcours [!DNL Journey Optimizer B2B Edition] et les chronologies normales.
feature: Journeys, Data Management
role: User
autotag-review: '2026-10-08T18:36:33.252Z'
TQID: 'https://experienceleague.adobe.com/PA1IeRHnGWHmBtDpffzveoWIHOn99-Ctt4Y0OQb7CwE'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
    internal-label: Experience Platform
  - id: b27e5950-9033-45ac-9f86-eb22e567f615
    internal-label: Marketo Engage
feature_v2:
  - id: 095e8119-1425-57eb-9d8c-9e684f2c9771
    internal-label: Audiences
  - id: 33ca0c14-7e3b-55a1-8fd7-8a61b47da4e1
    internal-label: B2B
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
  - id: a50ad69b-1331-40e9-b634-531a085a6a54
    internal-label: Identities
  - id: afadf741-c5fe-42cd-8013-23bb6ff2d1bc
    internal-label: Buying Groups
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
  - id: eec185bd-7d60-4193-ba3f-da427569936a
    internal-label: Destinations
  - id: f2da1b69-6919-4386-a5d2-9c7b5c9033db
    internal-label: Data management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
source-git-commit: 827c313f032d482ac2b0a5fa8f41d6506e67b9cb
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%
---
# Disponibilité des données et synchronisation temporelle {#data-availability}

Utilisez cette rubrique pour connaître la vitesse à laquelle les modifications de données apparaissent dans vos parcours de [!DNL Adobe Journey Optimizer B2B Edition] et les chronologies normales. Connaître le timing prévu vous permet de concevoir des parcours en conséquence et de déterminer à quel moment un retard correspond à un comportement attendu.

## Temps d’attente attendus

| Type de données | Disponibilité standard |
| --- | --- |
| [Appartenance à une audience](#daily-refresh) | Jusqu’à 24 heures (cycle quotidien) |
| [Modifications de la relation compte/personne](#daily-refresh) | Jusqu’à 24 heures (cycle quotidien) |
| [Données de [!DNL Experience Platform] à [!DNL Journey Optimizer B2B Edition]](#platform-sync) | Jusqu’à 30 minutes (temps quasi réel) |
| [Données de [!DNL Journey Optimizer B2B Edition] à [!DNL Experience Platform]](#platform-sync) | Jusqu&#39;à quatre heures (micro-lots) |
| [Événements d’activité, tels que les clics et les ouvertures](#activity-and-actions) | Jusqu’à quatre heures |
| [[!DNL Marketo Engage] ajouter ou supprimer une liste](#activity-and-actions) | Dans les 30 minutes (temps quasi réel) |
| [Événements générés par Journey Optimizer B2B Edition](#activity-and-actions) | Utilisable dans les audiences par lots uniquement |
| [Population d’audiences LinkedIn](#linkedin-timing) | Même jour à 36-40 heures (au pire des cas) |

## Données d’audience et de relation {#daily-refresh}

[!DNL Journey Optimizer B2B Edition] évalue l’appartenance à l’audience du compte et de la personne une fois par jour, déclenchée par un planificateur de tâches par lots. Par conséquent :

* Les comptes ou les personnes nouvellement qualifiés pour une audience peuvent rejoindre un parcours dans les 24 heures suivant la qualification.
* Les modifications apportées aux critères d’audience prennent effet dans le prochain cycle d’évaluation quotidien.
* Si un compte s’est qualifié pour une audience aujourd’hui, mais n’a pas encore rejoint le parcours, attendez la fin du cycle quotidien suivant avant d’enquêter.
* Lorsque l’association de compte d’une personne change, par exemple lorsqu’un contact passe à un autre compte, la mise à jour de la relation se propage dans les 24 heures tout au long du cycle de synchronisation quotidien. Les parcours qui dépendent de l’appartenance au compte reflètent la relation mise à jour après le cycle quotidien suivant. Aucune action n’est nécessaire.

>[!TIP]
>
>Concevez des parcours en sachant que l’adhésion à l’audience est actualisée tous les jours, et non en temps réel. Si vous avez besoin de réponses en temps quasi réel, utilisez des [déclencheurs basés sur un événement](../journeys/listen-for-event-nodes.md) plutôt qu’une entrée basée sur une audience.

## Synchronisation des données avec [!DNL Experience Platform] {#platform-sync}

[!DNL Experience Platform] est le magasin de données principal pour les comptes, les personnes et les opportunités. [!DNL Journey Optimizer B2B Edition] possède des parcours, des groupes d’achat et des rôles de groupe d’achat. [En savoir plus sur l’architecture](../about-journey-optimizer-b2b-edition.md#high-level-architecture).

Les données se déplacent entre les deux systèmes dans chaque direction à un rythme différent :

* **[!DNL Experience Platform]à[!DNL Journey Optimizer B2B Edition]** - Les données se synchronisent en temps quasi réel et peuvent prendre jusqu’à 30 minutes.
* **[!DNL Journey Optimizer B2B Edition]à[!DNL Experience Platform]** - Les données se synchronisent par micro-lots et peuvent prendre jusqu’à 4 heures.

## Événements d’activité et actions de parcours {#activity-and-actions}

Le minutage des données d’activité et des actions de parcours dépend de la manière dont les données se déplacent entre les systèmes :

* **Données d’activité** - Les enregistrements d’activité d’une personne, tels que les ouvertures d’e-mail, les clics sur des liens et les remplissages de formulaire, peuvent prendre environ quatre heures pour apparaître dans les [!DNL Journey Optimizer B2B Edition]. Cette durée s’applique aux données d’activité par lots ; les déclencheurs d’événements d’expérience [!DNL Experience Platform] utilisent les données de diffusion en continu et peuvent réagir en temps quasi réel.
* **[!DNL Marketo Engage]des actions** - actions de Parcours qui appellent des [!DNL Marketo Engage] en temps quasi réel, car il s’agit d’appels API. Par exemple, lorsqu’une étape de parcours ajoute ou supprime une personne d’une liste [!DNL Marketo], l’action se termine généralement dans les 30 minutes. [En savoir plus sur les actions de parcours &#x200B;](../journeys/action-nodes.md).
* **Actions qui passent par[!DNL Experience Platform]** - Toute action qui revient en premier à [!DNL Experience Platform] est traitée par lots, de sorte qu’elle est soumise à une synchronisation par lots plutôt qu’à une synchronisation en temps quasi réel.
* **Événements générés par[!DNL Journey Optimizer B2B Edition]** - Les événements générés par [!DNL Journey Optimizer B2B Edition] dans [!DNL Experience Platform] ne peuvent être utilisés que dans les audiences par lots.

## [!DNL LinkedIn] des destinations d’audience {#linkedin-timing}

Si votre parcours comprend une action de destination [!DNL LinkedIn], attendez-vous à la chronologie suivante après la publication du parcours.

| Scénario | Attente attendue |
| --- | --- |
| Les comptes étaient déjà dans l’audience lors de la publication du parcours | Même jour, si le traitement est terminé avant minuit heure locale |
| Comptes arrivés après la publication du parcours | Jusqu’à 24 heures |
| Les comptes sont arrivés après la première fenêtre de synchronisation quotidienne | Jusqu’à 36-40 heures |

Les nombres de profils des audiences [!DNL LinkedIn] peuvent ne pas être mis à jour immédiatement. Ce délai est un délai attendu pendant que [!DNL Experience Platform] traite et diffuse le fichier d’audience à [!DNL LinkedIn]. Si le nombre de profils des audiences est toujours à 0 au bout de 48 heures, vérifiez. [En savoir plus sur les audiences appariées de comptes LinkedIn](./linkedin-account-matched-audiences.md).
