---
title: Nœud de Parcours d’audience de personne
description: Configurez le nœud audience de personne dans Journey Optimizer B2B pour spécifier les profils qui rejoignent un parcours à l’aide de listes de personnes dynamiques ou d’audiences basées sur un événement.
badgeBeta: label="Beta" type="informative" tooltip="Cette fonctionnalité est actuellement en version bêta limitée"
autotag-review: '2026-06-16T21:21:01.614Z'
TQID: 'https://experienceleague.adobe.com/pk1NGg3M67oRieuCOZFdaguKl2bVkiZyEPVnJDTUBJs'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: ba367494-9862-4596-bd6f-299c7e10a46b
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a48a12635d2ba4f14dda49e25e79a5496ebbdecf
workflow-type: tm+mt
source-wordcount: 226
ht-degree: 4%

---

# Nœud d’audience de personne

Le nœud _audience personne_ spécifie les profils de personnes qui rejoignent le parcours. Lorsque vous [créez un parcours de personne](./person-journeys.md), le parcours commence toujours par un nœud d’audience de personne qui définit son entrée. Le nœud d’audience de personne peut avoir l’un des deux types d’entrée d’audience suivants : une liste de personnes statique ou une liste de personnes dynamique.

Si la liste de personnes dynamique dont vous avez besoin pour le parcours de personnes n’existe pas déjà, [créez la liste de personnes](../audiences/people-lists.md#create-a-people-list) puis configurez le nœud Audience de la personne .

_Pour configurer l&#39;audience de parcours :_

1. Cliquez sur le nœud **[!UICONTROL Audience de la personne]**.

   Cette action affiche les propriétés du nœud sur la droite.

   ![Nœud de parcours d’audience de personne](./assets/person-audience-node-properties.png){width="500" zoomable="yes"}

1. Utilisez l’une des options de configuration d’audience suivantes pour l’audience de personne :

   * **[!UICONTROL Liste dynamique]** - Utilisez une liste de personnes dynamique, basée sur des règles. Les règles de liste sont évaluées au moment de l’exécution du parcours pour qualifier les membres du parcours. Les personnes qui seront ultérieurement disqualifiées pour la liste dynamique ne seront pas supprimées du parcours. Voir _[Listes dynamiques](../audiences/people-lists.md#dynamic-lists)_.

   * **[!UICONTROL Audience de l’événement]** - Utilisez une audience d’événement pour définir l’audience du parcours en fonction des événements admissibles. Définissez des membres d’audience à l’aide du filtrage de profil de personne et déclenchez une entrée de parcours selon des critères d’événement. Voir _[Audiences basées sur un événement](../audiences/event-based-audiences.md)_.
