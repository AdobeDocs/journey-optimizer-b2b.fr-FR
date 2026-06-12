---
title: Ajouter des nœuds de Parcours
description: Page d’espace réservé pour les nœuds de parcours de personne.
autotag-review: '2026-06-12T23:02:52.147Z'
TQID: 'https://experienceleague.adobe.com/sTnrOvrGIrgboPqOMrrkUvNU1y6zZJX42zEJxuUInKQ'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: ba367494-9862-4596-bd6f-299c7e10a46b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: cb3217c9fd7beb712d0c61638d143b798010d2b7
workflow-type: tm+mt
source-wordcount: 1137
ht-degree: 2%

---

# Ajouter des nœuds de parcours

Après avoir créé un parcours de personne, ajoutez l’audience et créez le parcours à l’aide de nœuds . La carte de parcours fournit une zone de travail, où vous pouvez créer vos cas d’utilisation marketing B2B à plusieurs étapes.

Le nœud _[!UICONTROL Personne]_ est automatiquement le premier nœud du parcours. Après avoir sélectionné l’audience, créez votre parcours en combinant les différents nœuds d’action, d’événement et de décision en tant que scénario cross-canal à plusieurs étapes. Chaque nœud d’un parcours représente une étape le long d’un chemin logique.

## Nœud d’audience de personne

Le nœud d’audience de personne indique quels enregistrements de personne entrent dans le parcours. Lorsque vous créez un parcours de personne, le parcours commence toujours par un nœud d’audience de personne qui définit son entrée.

1. Cliquez sur le nœud pour le sélectionner.
1. Dans le panneau des propriétés de nœud à droite, utilisez l’une des options d’entrée suivantes pour le nœud de parcours d’audience de personne :

   * **[!UICONTROL Liste dynamique]** - Utilisez une liste de personnes dynamique, basée sur des règles. Les règles de liste sont évaluées au moment de l’exécution du parcours pour qualifier les membres du parcours. Les personnes qui seront ultérieurement disqualifiées pour la liste dynamique ne seront pas supprimées du parcours.

   * **[!UICONTROL Liste statique]** - Utilisez une liste statique de personnes comme membres de votre parcours. L’appartenance actuelle à la liste est évaluée au moment de l’exécution du parcours afin de qualifier les membres pour le parcours. Les personnes qui sont supprimées ultérieurement de la liste statique ne sont pas supprimées du parcours.

## Nœuds d’action des personnes

Dans un parcours de personne, utilisez une action sur les personnes lorsque vous souhaitez appliquer une modification à toutes les personnes sur le chemin de nœud. Pour un parcours de compte, ce type de nœud peut être utilisé dans le chemin de partage par personnes ou dans le chemin de partage par comptes.

### Actions et contraintes

| Action | Contraintes |
| ------ | ---------- |
| **[!UICONTROL Envoyer un e-mail]** | <li>Créer un e-mail <li>Optimisation de l’heure d’envoi (facultatif) |
| **[!UICONTROL Modifier la valeur des données]** | <li>Sélectionner l’attribut de personne <li>Définir une nouvelle valeur |

### Ajouter un nœud d’action

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

## Nœuds d’événement

Ajoutez le nœud _Écouter un événement_ pour faire passer votre audience à l’étape suivante du parcours lorsqu’un événement se produit.

### Filtres d’événement de personne

| Filtres | Description |
| ------- | ----------- |
| Historique des activités > E-mail | Activités d&#39;email basées sur des conditions évaluées à l&#39;aide d&#39;un ou plusieurs emails sélectionnés : <li>Lien ayant fait l’objet d’un clic dans l’e-mail <li>E-mail ouvert |
| Historique des activités > Valeur des données modifiée | Pour un attribut de personne sélectionné, une modification de valeur s’est produite. Ces types de modifications sont les suivants : <li>Nouvelle valeur <li>Valeur précédente <li>Motif <li>Source <li>Date de l’activité <li> Min. nombre de fois |

### Ajouter un nœud d’événement

1. Accédez à la carte du parcours.

1. Cliquez sur l’icône plus ( **+** ) d’un chemin et choisissez **[!UICONTROL Écouter un événement]**.

1. Dans les propriétés de nœud sur la droite, choisissez **[!UICONTROL Personnes]** pour le type d’événement.

   <!-- ![Journey node - listen to events on people](./assets/node-listen-events-people.png){width="700" zoomable="yes"} -->

1. Sélectionnez un événement dans la liste.

1. Cliquez sur **[!UICONTROL Modifier l’événement]** et définissez les détails de l’événement.

>[!NOTE]
>
>La fonctionnalité de temporisation d’Écouter pour un nœud d’événement ne fonctionne pas actuellement et sera activée dans une phase ultérieure.

## Nœuds de chemins de partage

Utilisez des nœuds fractionnés pour segmenter les personnes en fonction des conditions que vous définissez. Créez des chemins d’accès pour la liste d’audiences en fonction de conditions, définissez chaque chemin d’accès avec des nœuds d’action et d’événement pour le segment, puis combinez les chemins d’accès et poursuivez le parcours.

Un nœud Chemins partagés définit un ou plusieurs chemins segmentés en fonction des filtres de personnes.

<!-- A split based on a people filter is automatically closed with a merge paths node so that all people can move forward to the next step. Split by people paths can include only people actions. These paths cannot be split again and automatically join back. _not currently true_ -->


_**Fonctionnement d’un nœud de partage de chemin par personnes**_

* L’évaluation de chaque chemin s’effectue de haut en bas. Si une personne correspond pour le premier et le deuxième chemin, elle continue uniquement le premier chemin.
* Le nœud prend en charge la définition d’un chemin _Autres personnes_, où vous pouvez ajouter des actions ou des événements pour les personnes qui ne correspondent pas à l’un des segments/chemins définis.

### Filtres correspondants

Pour chaque chemin d’accès que vous définissez pour le nœud, utilisez les types de filtre suivants pour faire correspondre les personnes selon une ou plusieurs conditions :

* Historique des activités - Vous pouvez définir un chemin d’accès en fonction de l’activité de la personne liée aux éléments suivants :

   * Messages e-mail
   * Modification de la valeur des données

* Attributs de personne - Définissez une condition en fonction des attributs d’une personne, tels que le pays, la fonction ou l’appartenance à une liste.

### Ajouter un nœud de chemins de division

<!--
>[!NOTE]
>
>When you split paths by people, a _Close split paths_ node is automatically inserted to end the split. A split-by-people path allows only _Take an action_ on people nodes.
-->

1. Accédez à la carte du parcours.

1. Cliquez sur l’icône plus ( **+** ) d’un chemin d’accès et choisissez **[!UICONTROL Fractionner les chemins]**.

   <!-- ![Add journey node - split paths](./assets/add-node-split.png){width="300" zoomable="no"} -->

1. Pour définir une condition applicable à _[!UICONTROL Chemin 1]_, cliquez sur **[!UICONTROL Appliquer la condition]**.

1. Dans l’éditeur de conditions, ajoutez un ou plusieurs filtres pour définir le chemin de division.

   * Faites glisser et déposez l’un des filtres de personnes à partir du volet de navigation de gauche et terminez la définition de la correspondance.

   * Ajustez vos conditions en appliquant la logique **[!UICONTROL Filtre]** en haut. Vous pouvez choisir de correspondre à toutes les conditions ou à une seule condition.

     <!-- ![Split path node - conditions person filter logic](./assets/node-split-conditions-people.png){width="700" zoomable="yes"} -->

   * Cliquez sur **[!UICONTROL Terminé]**.

1. Pour ajouter d’autres chemins d’accès, cliquez sur **[!UICONTROL Ajouter un chemin d’accès]** et répétez les étapes précédentes pour ajouter des conditions applicables au chemin d’accès.

   Vous pouvez également libeller chaque chemin d’accès en fonction de ces conditions ou utiliser les libellés par défaut.

1. Si nécessaire, réorganisez les chemins en fonction de la priorité que vous souhaitez pour la division.

   Le filtrage des chemins d’accès est évalué dans l’ordre décroissant. Chaque personne suit le premier chemin correspondant.

   Cliquez sur les flèches vers le haut et vers le bas en haut à droite de chaque carte de chemin pour la déplacer vers le haut ou le bas dans la liste des chemins.

   <!-- ![Split path node - reorder paths](./assets/node-split-reorder-paths-people.png){width="500" zoomable="yes"} -->

1. Activez l’option **[!UICONTROL Autres personnes]** pour ajouter un chemin par défaut pour les personnes qui ne correspondent pas aux chemins définis.

   Lorsque cette option n’est pas activée, les personnes qui ne correspondent pas à un segment/chemin défini passent au-delà de la division et passent à l’étape suivante du parcours.

Lorsque des conditions sont définies pour chaque chemin, vous pouvez ajouter des nœuds d’action ou d’événement à appliquer aux personnes situées sur un chemin.

## Nœuds de chemins de fusion

1. Accédez à la carte du parcours et localisez le nœud de chemins de division avec plusieurs chemins d’accès.

   Chaque chemin doit comporter une combinaison d’actions et d’événements.

1. Cliquez sur l’icône plus ( **+** ) à la fin de l’un de ces chemins et choisissez **[!UICONTROL Fusionner les chemins]** dans les options affichées.

   <!-- ![Journey node - merge paths](./assets/node-plus-icon-merge-paths.png){width="400" zoomable="no"} -->

1. Dans les propriétés de nœud à droite, sélectionnez les chemins d’accès à fusionner.

   <!-- ![Journey node - merge paths](./assets/node-merge-select-paths.png){width="600" zoomable="yes"} -->

   À ce stade, les chemins d’accès sont fusionnés afin que les personnes des chemins d’accès sélectionnés se combinent pour former un chemin d’accès unique qui peut continuer à progresser dans le parcours.

1. Si nécessaire, vous pouvez annuler la fusion des chemins en revenant aux propriétés du nœud de chemins de fusion et en décochant la case correspondant aux chemins que vous souhaitez supprimer.
