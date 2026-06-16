---
title: Prendre un nœud d’action
description: Espace réservé
autotag-review: '2026-06-12T22:58:21.806Z'
TQID: 'https://experienceleague.adobe.com/uR-WvNz3gA6V7yyN3RRXH-MggrmGb1qvu1CBhMZRuAc'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: af7eab5e-3580-4254-9f56-3c20b4f6ef42id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: bf2854a777f62ba2f74f79942ee3336b6e8ab9dd
workflow-type: tm+mt
source-wordcount: 197
ht-degree: 2%

---

# Nœud Prendre une action

Dans un parcours de personne, utilisez une action sur les personnes lorsque vous souhaitez appliquer une modification à toutes les personnes sur le chemin de nœud. Pour un parcours de compte, ce type de nœud peut être utilisé dans le chemin de partage par personnes ou dans le chemin de partage par comptes.

## Actions et contraintes

| Action | Contraintes |
| ------ | ---------- |
| **[!UICONTROL Envoyer un e-mail]** | <li>Créer un e-mail <li>Optimisation de l’heure d’envoi (facultatif) |
| **[!UICONTROL Modifier la valeur des données]** | <li>Sélectionner l’attribut de personne <li>Définir une nouvelle valeur |

## Ajouter un nœud d’action {#add-an-action-node}

1. Accédez à la carte du parcours.

1. Cliquez sur l’icône plus ( **+** ) d’un chemin d’accès et choisissez **[!UICONTROL Effectuer une action]**.

1. Dans les propriétés de nœud sur la droite, sélectionnez une action dans la liste et définissez ses valeurs.

<!-- ![Person journey node - take an action](./assets/node-take-action-people.png){width="700" zoomable="yes"} -->

+++[!UICONTROL Envoyer un e-mail]

Utilisez cette action pour envoyer un e-mail. Après avoir créé l’e-mail pour le nœud , vous pouvez concevoir, personnaliser et prévisualiser des e-mails dans l’espace de conception des e-mails (voir [Création d’e-mails](../content/email-authoring.md)).

<!-- ![Take an action - Send email](./assets/node-action-send-email-from-marketo.png){width="300"} -->

Vous pouvez utiliser l’[optimisation de l’heure d’envoi](../marketing/email-send-time-optimization.md) pour personnaliser le délai de diffusion des e-mails en prédisant le moment où chaque profil est le plus susceptible d’interagir.

<!--
>[!NOTE]
>
>You can use email deduplication in account journeys to ensure that the same email is not sent multiple times to the same email address within a journey. For more information, see [Email deduplication](../content/email-deduplication.md).
-->

+++

+++[!UICONTROL Modifier la valeur des données]

Utilisez cette action pour modifier la valeur d&#39;un attribut de profil de personnes dans la base de données. Sélectionnez l’attribut, puis définissez la nouvelle valeur.

<!-- ![Take an action - Update person profile](./assets/node-action-update-person-profile.png){width="300"} -->

+++
