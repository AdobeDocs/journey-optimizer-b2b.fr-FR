---
title: Parcours de la personne
description: Page d’espace réservé pour les parcours de personne.
source-git-commit: 2f19137465c71f2292d37bea5786533b1df6e286
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 22%

---

# Parcours de la personne

Dans Journey Optimizer B2B edition Prime, les parcours de personne sont des plans marketing automatisés, basés sur des prospects et à plusieurs étapes, qui utilisent des données Marketo Engage pour orchestrer des expériences personnalisées sur plusieurs canaux en réponse à l’engagement, aux événements métier ou aux campagnes planifiées.

Pour commencer à utiliser votre parcours de première personne :

1. Créez un parcours de personne.
1. Ajoutez les nœuds et définissez le flux du parcours dans la carte du parcours.
1. Publiez le parcours.

## Accès et navigation dans les parcours de personne

Dans le volet de navigation de gauche, développez **[!UICONTROL Marketing Management]** et sélectionnez **[!UICONTROL parcours de personne]**.

Vous pouvez saisir du texte dans l’outil _Rechercher_ en haut de la liste pour filtrer la liste affichée par nom.

### Colonnes de liste de parcours

La page de liste parcours comprend les colonnes suivantes :

Nom (cliquez sur le nom pour afficher la carte de parcours à modifier)
Statut
Date de création
Création par
Dernière mise à jour
Dernière mise à jour effectuée par
Publication le
Publication par
Date de début
Date de fin

Vous pouvez trier la liste par Statut, Date de création ou Dernière mise à jour en cliquant sur l’en-tête de colonne.

Pour personnaliser (afficher/masquer) les colonnes affichées dans le tableau, cliquez sur l’icône Personnaliser le tableau ( ) dans le coin supérieur droit. Cochez ou décochez les cases de la boîte de dialogue, puis cliquez sur Appliquer.

### Statut du parcours

Le statut d’un parcours peut changer en fonction des actions que vous appliquez. En fonction du statut d’un parcours, certaines actions peuvent être disponibles ou non dans l’en-tête.

| Statut | Description | Actions disponibles |
| ------ | ----------- | ----------------- |
| Brouillon | Parcours dépublié modifiable. | <li>Publier <li>Dupliquer <li>Supprimer |
| Actif | Le statut du parcours passe de Brouillon à Actif lorsqu’un parcours est publié. Dans ce statut, il n’est plus modifiable. | <li>Dupliquer |
| Terminé | Lorsque tous les membres de l’audience de compte ou de personne d’un parcours terminent le parcours, le statut passe de Actif ou Fermé à Nouvelles entrées et passe à Terminé. | <li>Dupliquer <li>Supprimer |

## Créer un parcours de personne

1. Cliquez sur **[!UICONTROL Créer un Parcours]** en haut à droite de la liste des parcours.

1. Dans la boîte de dialogue, saisissez un **[!UICONTROL Nom]** unique (obligatoire) et un **[!UICONTROL Description]** (facultatif).

<!-- 
   ![Create Journey dialog](./assets/person-journey-create-dialog.png){width="400"}
-->

1. Cliquez sur **[!UICONTROL Créer]**.

### Conception de parcours

La carte de parcours __ est la zone centrale de l&#39;espace de travail de parcours. C’est là que vous pouvez ajouter des nœuds de parcours et les configurer. Cliquez sur un nœud pour ouvrir ses propriétés dans le panneau situé à droite de la disposition et les définir en fonction de votre conception. Un parcours de personne commence toujours par un nœud _[!UICONTROL Audience de personne]_, où vous pouvez définir l’entrée du parcours.

<!--
   ![Journey map for newly created journey](./assets/person-journey-create-dialog.png){width="400"}
-->

Après avoir créé un parcours de personne et ajouté l’audience de personne, créez le parcours à l’aide de nœuds . La carte de parcours fournit une zone de travail, dans laquelle vous pouvez créer vos cas d’utilisation marketing B2B à plusieurs étapes à l’aide des types de nœuds suivants pour créer le parcours :

* [Entreprendre une action](./action-nodes.md)
* [Écouter un événement](./listen-for-event-nodes.md)
* [Attente](./wait-nodes.md)
* [Chemins partagés](./split-merge-paths-nodes.md)
* [Deuxième meilleur chemin](./next-best-path.md)
* [Fusionner les chemins](./split-merge-paths-nodes.md)


## Gestion des parcours



## Cartographie du parcours

Cliquez sur le nom (affiché sous forme de lien) dans la liste parcours pour passer en revue les détails, apporter des modifications et prendre des mesures.

L’en-tête de chaque mappage de parcours comprend :

Nom du parcours
Outil d’édition du nom du parcours (icône Modifier )
Etat du parcours
À partir du mappage de parcours, vous pouvez Ajouter les nœuds et définir le flux de parcours.

### Actions de parcours

La page de liste parcours comprend tous les parcours de compte ou de personne de votre instance Journey Optimizer B2B edition. La page de liste vous permet d’appliquer plusieurs actions à un parcours.



#### Dupliquer un parcours

Une action de duplication est similaire à une fonction de clonage, mais le parcours dupliqué n’inclut aucune ressource de contenu de parcours créée. Vous pouvez dupliquer les détails du parcours ou simplement un squelette de la structure du flux et du chemin.

REMARQUE

Cliquez sur l’icône Plus (...) à côté du nom du parcours et choisissez Dupliquer.

Selon le statut du parcours, vous pouvez également accéder à l’action en double à partir des détails du parcours ou de la carte des parcours :

Pour un brouillon de parcours, cliquez sur le menu Plus... en haut à droite et choisissez Dupliquer.
Pour tous les autres statuts de parcours, cliquez sur Dupliquer en haut à droite.
Dans la boîte de dialogue Dupliquer le Parcours , définissez le Nom et la Description du nouveau parcours.
Par défaut, la boîte de dialogue utilise le nom du parcours dupliqué suivi de _copy. Saisissez un autre nom unique pour le parcours, le cas échéant.

Choisissez le type de duplication :
Duplication partielle du contenu - Utilisez ce type pour copier tout le contenu du parcours, à l’exclusion des e-mails ou des SMS créés. Les nœuds qui font référence à un e-mail ou un SMS Marketo Engage sont entièrement intacts.
Dupliquer sans détails - Utiliser ce type pour copier uniquement la structure de nœud et les chemins d’accès. Tous les paramètres de nœud et conditions de chemin sont indéfinis (par défaut). Vous pouvez donc réutiliser le flux de base avec différents paramètres d’audience, d’actions et de segmentation de chemin. Tous les nœuds d’attente utilisent la valeur par défaut de cinq jours.
Cliquez sur Dupliquer.
Le parcours dupliqué s’ouvre dans la carte des parcours, où vous pouvez définir les détails et créer du contenu de parcours selon vos besoins.

Supprimer un parcours

Utilisez une action de suppression pour supprimer définitivement un parcours. Vous ne pouvez pas supprimer un parcours actif ou planifié.

Cliquez sur l’icône Plus (...) à côté du nom du parcours et choisissez Supprimer.
Selon le statut du parcours, vous pouvez également accéder à l’action de suppression à partir des détails du parcours ou de la carte des parcours :

Pour un brouillon de parcours, cliquez sur le menu Plus... en haut à droite et choisissez Supprimer.
Pour d’autres statuts de parcours, tels que Terminé ou Abandonné, cliquez sur Supprimer en haut à droite.
Dans la boîte de dialogue de confirmation, cliquez sur Supprimer.






