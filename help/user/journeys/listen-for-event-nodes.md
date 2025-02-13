---
title: Écoute d’un événement
description: Découvrez le type de nœud d’événement Écouter pour que vous puissiez utiliser pour orchestrer vos parcours de compte dans Journey Optimizer B2B edition.
feature: Account Journeys
exl-id: d852660b-f1da-4da0-86f0-85271f55b79f
source-git-commit: d03e0e2d8070916d38bb956adff8dea3f3873aad
workflow-type: tm+mt
source-wordcount: '1368'
ht-degree: 13%

---

# Écoute d’un événement

Ajoutez le nœud _Écouter un événement_ pour faire passer votre audience à l’étape suivante du parcours de compte lorsqu’un événement se produit.

![Vidéo](../../assets/do-not-localize/icon-video.svg){width="30"} [Regardez la vidéo de présentation](#overview-video)

>[!NOTE]
>
>Vous ne pouvez pas ajouter ce type de nœud sur le chemin de partage par personnes.

## Événements de compte

Ecoutez un événement en fonction du compte lorsque vous souhaitez déplacer le compte vers l’avant dans le parcours en fonction des événements déclenchés par l’activité du compte.

### Événements et contraintes

| Événement | Contraintes |
| ----- | ----------- |
| Le compte a eu un moment intéressant | Type (e-mail, jalon ou web)<br/>Contraintes supplémentaires (facultatif) : <li>Description</li><li>Source</li><li>Date d’activité</li> <br/>Délai d’expiration (facultatif) |
| Modification de la valeur des données du compte | Attribut<br/>Contraintes supplémentaires (facultatif) : <li>Nouvelle valeur</li><li>Valeur précédente</li><li>Date d’activité</li> <br/>Délai d’expiration (facultatif) |
| Changement dans l&#39;étape du groupe d&#39;achat | Intérêt de la solution<br/>Contraintes supplémentaires (facultatif) : <li>Nouvelle étape</li><li>Étape précédente</li><li>Date d’activité</li>Délai d’expiration du <br/> (facultatif) |
| Changement de statut du groupe d&#39;achat | Intérêt de la solution<br/>Contraintes supplémentaires (facultatif) : <li>Nouveau statut</li><li>Statut précédent</li><li>Date d’activité</li>Délai d’expiration du <br/> (facultatif) |
| Modification du score d&#39;exhaustivité | Intérêt de la solution<br/>Contraintes supplémentaires (facultatif) : <li>Nouveau score</li><li>Score précédent</li><li>Date d’activité</li>Délai d’expiration du <br/> (facultatif) |
| Modification du score d’engagement | Intérêt de la solution<br/>Contraintes supplémentaires (facultatif) : <li>Nouveau score</li><li>Score précédent</li><li>Date d’activité</li>Délai d’expiration du <br/> (facultatif) |

### Ajouter un événement de compte

1. Accédez à l’éditeur de parcours.

1. Cliquez sur l’icône plus ( **+** ) d’un chemin et choisissez **[!UICONTROL Écouter un événement]**.

1. Dans les propriétés de nœud sur la droite, choisissez **[!UICONTROL Comptes]** pour le type d’événement.

   ![nœud de Parcours - écouter les événements sur le compte](./assets/node-listen-events-account.png){width="700" zoomable="yes"}

1. Sélectionnez un événement dans la liste.

1. Cliquez sur **[!UICONTROL Modifier l’événement]** et définissez les détails de l’événement.

## Événements Personnes

Ecoutez un événement basé sur des personnes lorsque vous souhaitez déplacer le compte vers l’avant dans le parcours en fonction des événements déclenchés par l’activité des personnes.

### Événements et contraintes

| Type d’entrée | Événement | Contraintes |
| ---------- | ----- | ----------- |
| Journey Optimizer édition B2B | Affecté au groupe d&#39;achat | Intérêt de la solution<br/><br/>Contraintes supplémentaires (facultatif) : <li>Rôle</li><li>Date d’activité</li><br/>Délai d’expiration (facultatif) |
| | Clique sur un lien dans un e-mail | E-mail<br/><br/>Contraintes supplémentaires (facultatif) : <li>Lien</li><li>ID lien</li><li>Est un appareil mobile</li><li>Appareil</li><li>Platform</li><li>Navigateur</li><li>Est du contenu prédictif</li><li>Est une activité du bot</li><li>Modèle d’activité du bot</li><li>Navigateur</li><li>Date d’activité</li><li>Min. nombre de fois</li><br/>Délai d’expiration (facultatif) |
| | Clics lien dans SMS | E-mail<br/><br/>Contraintes supplémentaires (facultatif) : <li>Lien</li><li>Appareil</li><li>Platform</li><li>Date d’activité</li><li>Min. nombre de fois</li><br/>Délai d’expiration (facultatif) |
| | Modifications valeur des données | Attribut de personne<br/><br/>Contraintes supplémentaires (facultatif) : <li>Nouvelle valeur</li><li>Valeur précédente</li><li>Motif</li><li>Source</li><li>Date d’activité</li><li>Min. nombre de fois</li><br/>Délai d’expiration (facultatif) |
| | Ouvre l’e-mail | E-mail<br/><br/>Contraintes supplémentaires (facultatif) : <li>Lien</li><li>ID lien</li><li>Est un appareil mobile</li><li>Appareil</li><li>Platform</li><li>Navigateur</li><li>Est du contenu prédictif</li><li>Est une activité du bot</li><li>Modèle d’activité du bot</li><li>Navigateur</li><li>Date d’activité</li><li>Min. nombre de fois</li><br/>Délai d’expiration (facultatif) |
| | Retiré du groupe d&#39;achat | Intérêt de la solution<br/>Date de l’activité (facultatif)<br/>Délai d’expiration (facultatif) |
| | Modification du score | Nom du score<br/><br/>Contraintes supplémentaires (facultatif) :<li>Changement</li><li>Nouveau score</li><li>Urgence</li><li>Priorité</li><li>Score relatif</li><li>Urgence relative</li><li>Date d’activité</li><li>Min. nombre de fois</li><br/>Délai d’expiration (facultatif) |
| | Rebonds SMS | Message SMS<br/><br/>Contraintes additionnelles (optionnel) : <li>Date d’activité</li><li>Nombre minimum de fois</li><br/>Délai d’expiration (facultatif) |
| Marketo Engage | Visites sur la page Internet | <br/> de page web Sélectionnez une ou plusieurs pages Marketo Engage à faire correspondre. <br/><br/>Contraintes supplémentaires (facultatif) : <li>Chaîne de requête</li><li>Adresse IP du client</li><li>Référent</li><li>Agent utilisateur</li><li>Moteur de recherche</li><li>Requête</li><li>Jeton</li><li>Navigateur</li><li>Platform</li><li>Appareil</li><li>Date d’activité</li> |
| | Remplit le formulaire | <br/> de formulaire Sélectionnez un ou plusieurs formulaires Marketo Engage à faire correspondre.  <br/><br/>Contraintes supplémentaires (facultatif) : <li>Date d’activité</li><li>Chaîne de requête</li><li>Adresse IP du client</li><li>Référent</li><li>Agent utilisateur</li><li>Platform</li><li>Appareil</li><br/>Délai d’expiration (facultatif) |
| Adobe Experience Platform | Définition de l’événement | Type d&#39;événement <br/><br/>Contraintes additionnelles (optionnelles) : <li>Champs</li> <br/>Contraintes additionnelles (non prises en charge) : <li>Date d’activité</li><li>Min. nombre de fois</li>Délai d’expiration du <br/> (facultatif) |

### Ajouter un événement de personne

1. Accédez à l’éditeur de parcours.

1. Cliquez sur l’icône plus ( **+** ) d’un chemin et choisissez **[!UICONTROL Écouter un événement]**.

1. Dans les propriétés de nœud sur la droite, choisissez **[!UICONTROL Personnes]** pour le type d’événement.

   ![nœud de Parcours - écoutez les événements sur les personnes](./assets/node-listen-events-people.png){width="700" zoomable="yes"}

1. Sélectionnez un événement dans la liste.

1. Cliquez sur **[!UICONTROL Modifier l’événement]** et définissez les détails de l’événement.

### Écoute de l’événement Marketo Engage

Si des pages web sont créées dans votre instance Marketo Engage connectée, vous pouvez déclencher un événement en fonction d’une visite ou d’une absence de visite des pages web Marketo Engage, ainsi que des formulaires Marketo Engage qui ont été remplis ou non.

1. Sélectionnez un nœud **[!UICONTROL Écouter un événement]** dans l’éditeur de parcours.

1. Dans les propriétés de nœud sur la droite, choisissez **[!UICONTROL Personnes]** pour le type d’événement.

1. Cliquez sur la flèche du sélecteur **[!UICONTROL Sélectionner un événement de personne]** et faites défiler le menu vers la section **[!UICONTROL Marketo Engage]**.

1. Sélectionnez un type d’activité d’engagement de marché :

   * **[!UICONTROL Page Web Visites]**.
   * **[!UICONTROL Remplit Le Formulaire]**

   ![Écouter un événement d’expérience](./assets/node-listen-events-people-me-event.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Modifier l’événement]** et définissez une ou plusieurs pages web à faire correspondre et toute contrainte supplémentaire pour l’événement.

   * (Obligatoire) Dans la boîte de dialogue _[!UICONTROL Modifier l’événement]_, définissez la contrainte **[!UICONTROL Page web]** ou Remplit le formulaire. Utilisez **[!UICONTROL is]** (par défaut) pour rechercher une correspondance sur une ou plusieurs pages ou formulaires sélectionnés. Utilisez **[!UICONTROL n’est pas]** pour correspondre à toutes les visites de page/formulaires avec l’exclusion d’une ou de plusieurs pages/formulaires sélectionnés. Vous pouvez également utiliser **[!UICONTROL est n’importe lequel]** pour faire correspondre sur n’importe quelle page web Marketo Engage visitée ou formulaire rempli.

   * (Facultatif) Cliquez sur **[!UICONTROL Ajouter une contrainte]** et sélectionnez le champ à utiliser pour la contrainte. Définissez l’opérateur et la valeur du champ .

     ![Écouter un événement d’expérience](./assets/node-listen-events-people-me-event-edit-dialog.png){width="700" zoomable="yes"}

     Vous pouvez répéter cette action pour inclure d’autres contraintes de champ, si nécessaire.

   * Lorsque les contraintes sont définies, cliquez sur **[!UICONTROL Terminé]**.

1. Si nécessaire, définissez l’option **[!UICONTROL Temporisation]** pour limiter la période d’écoute de l’événement (voir [Ajouter une temporisation à un nœud d’événement](#add-a-timeout-to-an-event-node)).

1. Dans l’éditeur de parcours, ajoutez le nœud suivant à exécuter lorsque l’événement se produit.

### Écoute d’un événement d’expérience

Les administrateurs peuvent configurer des définitions d’événement basées sur Adobe Experience Platform (AEP), ce qui permet aux spécialistes marketing de créer des parcours de compte qui réagissent aux [événements d’expérience AEP](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/experienceevent). L’utilisation d’événements d’expérience AEP dans les parcours de compte est un processus en deux étapes :

1. [Créer et publier une définition d’événement AEP](../admin/configure-aep-events.md).

2. Dans un parcours de compte, ajoutez un nœud _Écouter un événement_ et sélectionnez une définition d’événement Experience Platform pour un événement basé sur des personnes.

_Pour inclure un événement d’expérience dans votre parcours, procédez comme suit_

1. Sélectionnez un nœud **[!UICONTROL Écouter un événement]** dans l’éditeur de parcours.

1. Dans les propriétés de nœud sur la droite, choisissez **[!UICONTROL Personnes]** pour le type d’événement.

1. Cliquez sur la flèche du sélecteur **[!UICONTROL Sélectionner un événement de personne]** et faites défiler le menu vers la section **[!UICONTROL Adobe Experience Platform]**.

   ![Écouter un événement d’expérience](./assets/node-listen-events-people-aep-events.png){width="700" zoomable="yes"}

1. Sélectionnez l’événement.

   Le type d’événement s’affiche comme vide dans les détails du nœud.

   ![Modifier l’événement](./assets/node-listen-events-people-aep-events-edit.png){width="400" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Modifier l’événement]** et définissez les types d’événement et les contraintes supplémentaires pour l’événement.

   * (Obligatoire) Dans la boîte de dialogue _[!UICONTROL Modifier l’événement]_, définissez le type d’événement. Vous pouvez utiliser l’opérateur **[!UICONTROL is]** par défaut pour établir une correspondance avec un ou plusieurs types d’événements sélectionnés. Vous pouvez également utiliser l’opérateur **[!UICONTROL n’est pas]** pour faire correspondre sur tous les types d’événement à l’exclusion d’un ou de plusieurs types d’événement sélectionnés.

   * (Facultatif) Cliquez sur **[!UICONTROL Ajouter une contrainte]** et sélectionnez le champ à utiliser pour la contrainte. Définissez l’opérateur et la valeur du champ .

     ![Écouter un événement d’expérience](./assets/node-listen-events-people-aep-events-edit-dialog.png){width="700" zoomable="yes"}

     >[!NOTE]
     >
     >Les contraintes de _date d&#39;activité_ et _nombre minimum de fois_ ne sont pas prises en charge.

     Vous pouvez répéter cette action pour inclure d’autres contraintes de champ, si nécessaire.

   * Lorsque les contraintes sont définies, cliquez sur **[!UICONTROL Terminé]**.

1. Si nécessaire, définissez l’option **[!UICONTROL Temporisation]** pour limiter la période d’écoute de l’événement (voir [Ajouter une temporisation à un nœud d’événement](#add-a-timeout-to-an-event-node)).

1. Dans l’éditeur de parcours, ajoutez le nœud suivant à exécuter lorsque l’événement se produit.

1. Renseignez les nœuds restants pour votre parcours et [publiez-le](./journey-overview.md).

   Lorsque le parcours est actif (publié) et atteint le nœud _Écouter pour un événement_, il commence à écouter les événements d’expérience AEP.

## Ajouter une temporisation à un nœud d’événement

Si nécessaire, définissez le temps d’attente du parcours pour l’événement. Le parcours se termine après une temporisation, sauf si vous définissez un chemin de temporisation dans lequel vous pouvez ajouter d’autres nœuds.

1. Activez l’option **[!UICONTROL Délai d’expiration]**.

1. Sélectionnez la durée pendant laquelle le parcours attend qu’un événement se produise avant d’expirer.

   Vous pouvez choisir de terminer le chemin ici ou d’effectuer une autre action en définissant un autre chemin.

1. Pour créer un nouveau chemin dans le parcours où vous pouvez ajouter des actions et des événements applicables aux comptes lorsque l’événement ne se produit pas, cochez la case **[!UICONTROL Définir le chemin de temporisation]**.

   ![Nœud d’événement de Parcours : définissez le chemin de temporisation](./assets/node-event-timeout-set-path.png){width="700" zoomable="yes"}

## Vidéo de présentation

>[!VIDEO](https://video.tv.adobe.com/v/3443219/?learn=on)
