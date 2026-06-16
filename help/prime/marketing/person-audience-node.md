---
title: Nœud de Parcours d’audience de personne
description: Page d’espace réservé pour les parcours de personne.
autotag-review: '2026-06-16T21:21:01.614Z'
TQID: 'https://experienceleague.adobe.com/pk1NGg3M67oRieuCOZFdaguKl2bVkiZyEPVnJDTUBJs'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: beb5f4be-cec3-471a-9db6-831a77dd3ac9id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: ba367494-9862-4596-bd6f-299c7e10a46bid: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: b7cb8c2a43b8a562e55923d709f518b8f1d74b2a
workflow-type: tm+mt
source-wordcount: 212
ht-degree: 0%

---

# Nœud d’audience de personne

Le nœud _audience personne_ spécifie les profils de personnes qui rejoignent le parcours. Lorsque vous [créez un parcours de personne](./person-journeys.md), le parcours commence toujours par un nœud d’audience de personne qui définit son entrée. Le nœud d’audience de personne peut avoir l’un des deux types d’entrée d’audience suivants : une liste de personnes statique ou une liste de personnes dynamique.

Si la liste de personnes dont vous avez besoin pour le parcours de personnes n’existe pas déjà, [créez la liste de personnes](../audiences/audience-management.md#create-a-people-list) puis configurez le nœud Audience de la personne .

## Définissez l’audience pour le nœud audience de la personne .

1. Cliquez sur le nœud **[!UICONTROL Audience de la personne]**.

   Cette action affiche les propriétés du nœud sur la droite.

   <!-- ![Person audience journey node](./assets/person-journey-person-audience-node.png){width="700" zoomable="yes"} -->

1. Dans le panneau des propriétés de nœud à droite, utilisez l’une des options d’entrée suivantes pour le nœud de parcours d’audience de personne :

   * **[!UICONTROL Liste dynamique]** - Utilisez une liste de personnes dynamique, basée sur des règles. Les règles de liste sont évaluées au moment de l’exécution du parcours pour qualifier les membres du parcours. Les personnes qui seront ultérieurement disqualifiées pour la liste dynamique ne seront pas supprimées du parcours.

   * **[!UICONTROL Liste statique]** - Utilisez une liste statique de personnes comme membres de votre parcours. L’appartenance actuelle à la liste est évaluée au moment de l’exécution du parcours afin de qualifier les membres pour le parcours. Les personnes qui sont supprimées ultérieurement de la liste statique ne sont pas supprimées du parcours.

