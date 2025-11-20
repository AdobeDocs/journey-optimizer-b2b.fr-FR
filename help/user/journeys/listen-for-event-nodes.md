---
title: Écoute d’un événement
description: Configurez les nœuds d’événement pour les déclencheurs de compte et de personnes. Soyez à l’écoute des modifications des groupes d’achats, des clics sur les e-mails, des remplissages de formulaires et des événements Experience Platform dans Journey Optimizer B2B edition.
feature: Account Journeys
role: User
exl-id: d852660b-f1da-4da0-86f0-85271f55b79f
source-git-commit: 53875f5b1b61b5a4a87e3361eacae80a5c14d878
workflow-type: tm+mt
source-wordcount: '1810'
ht-degree: 12%

---

# Écouter un événement

Ajoutez le nœud _Écouter un événement_ pour faire passer votre audience à l’étape suivante du parcours de compte lorsqu’un événement se produit.

![Vidéo](../../assets/do-not-localize/icon-video.svg){width=« 30 », vertical-align=« middle »} [Regardez la vidéo de présentation](#overview-video)

>[!NOTE]
>
>Vous ne pouvez pas ajouter ce type de nœud sur le chemin de partage par personnes.

## Événements de compte

Ecoutez un événement en fonction du compte lorsque vous souhaitez déplacer le compte vers l’avant dans le parcours en fonction des événements déclenchés par l’activité du compte.

### Événements et contraintes

| Événement | Contraintes |
| ----- | ----------- |
| [!UICONTROL Le compte a eu un moment intéressant] | Type (e-mail, jalon ou web)<br/>Contraintes supplémentaires (facultatif) : <li>Description</li><li>Source</li><li>Date d’activité</li> <br/>Délai d’expiration (facultatif) |
| [!UICONTROL Modification de la valeur des données du compte] | Attribut<br/>Contraintes supplémentaires (facultatif) : <li>Nouvelle valeur</li><li>Valeur précédente</li><li>Date d’activité</li> <br/>Délai d’expiration (facultatif) |
| [!UICONTROL Changement dans l&#39;étape du groupe d&#39;achat] | Intérêt de la solution<br/>Contraintes supplémentaires (facultatif) : <li>Nouvelle étape</li><li>Étape précédente</li><li>Date d’activité</li>Délai d’expiration du <br/> (facultatif) |
| [!UICONTROL Changement de statut du groupe d&#39;achat] | Intérêt de la solution<br/>Contraintes supplémentaires (facultatif) : <li>Nouveau statut</li><li>Statut précédent</li><li>Date d’activité</li>Délai d’expiration du <br/> (facultatif) |
| [!UICONTROL Modification du score d’exhaustivité] | Intérêt de la solution<br/>Contraintes supplémentaires (facultatif) : <li>Nouveau score</li><li>Score précédent</li><li>Date d’activité</li>Délai d’expiration du <br/> (facultatif) |
| [!UICONTROL Modification du score d’engagement] | Intérêt de la solution<br/>Contraintes supplémentaires (facultatif) : <li>Nouveau score</li><li>Score précédent</li><li>Date d’activité</li>Délai d’expiration du <br/> (facultatif) |

### Ajouter un événement de compte

1. Accédez à la carte du parcours.

1. Cliquez sur l’icône plus ( **+** ) d’un chemin et choisissez **[!UICONTROL Écouter un événement]**.

1. Dans les propriétés de nœud sur la droite, choisissez **[!UICONTROL Comptes]** pour le type d’événement.

   ![nœud de Parcours - écouter les événements sur le compte](./assets/node-listen-events-account.png){width="700" zoomable="yes"}

1. Sélectionnez un événement dans la liste.

1. Cliquez sur **[!UICONTROL Modifier l’événement]** et définissez les détails de l’événement.

## Événements Personnes

Ecoutez un événement basé sur des personnes lorsque vous souhaitez déplacer le compte vers l’avant dans le parcours en fonction des événements déclenchés par l’activité des personnes. Vous pouvez également filtrer les événements en fonction des attributs des personnes,

### Événements et contraintes

| Type d’entrée | Événement | Contraintes |
| ---------- | ----- | ----------- |
| Journey Optimizer édition B2B | [!UICONTROL Affecté au groupe d&#39;achat] | Intérêt de la solution<br/><br/>Contraintes supplémentaires (facultatif) : <li>Rôle</li><li>Date d’activité</li><br/>Délai d’expiration (facultatif) |
| | [!UICONTROL Clics dans l’e-mail] | E-mail<br/><br/>Contraintes supplémentaires (facultatif) : <li>Lien</li><li>ID lien</li><li>Est un appareil mobile</li><li>Appareil</li><li>Platform</li><li>Navigateur</li><li>Est du contenu prédictif</li><li>Est une activité du bot</li><li>Modèle d’activité du bot</li><li>Navigateur</li><li>Date d’activité</li><li>Min. nombre de fois</li><br/>Délai d’expiration (facultatif) |
| | [!UICONTROL Clics sur le lien dans les SMS] | E-mail<br/><br/>Contraintes supplémentaires (facultatif) : <li>Lien</li><li>Appareil</li><li>Platform</li><li>Date d’activité</li><li>Min. nombre de fois</li><br/>Délai d’expiration (facultatif) |
| | [!UICONTROL Modifications de la valeur des données] | Attribut de personne<br/><br/>Contraintes supplémentaires (facultatif) : <li>Nouvelle valeur</li><li>Valeur précédente</li><li>Motif</li><li>Source</li><li>Date d’activité</li><li>Min. nombre de fois</li><br/>Délai d’expiration (facultatif) |
| | [!UICONTROL Ouvre l&#39;e-mail] | E-mail<br/><br/>Contraintes supplémentaires (facultatif) : <li>Lien</li><li>ID lien</li><li>Est un appareil mobile</li><li>Appareil</li><li>Platform</li><li>Navigateur</li><li>Est du contenu prédictif</li><li>Est une activité du bot</li><li>Modèle d’activité du bot</li><li>Navigateur</li><li>Date d’activité</li><li>Min. nombre de fois</li><br/>Délai d’expiration (facultatif) |
| | [!UICONTROL Supprimé du groupe d&#39;achat] | Intérêt de la solution<br/>Date de l’activité (facultatif)<br/>Délai d’expiration (facultatif) |
| | [!UICONTROL Le score est modifié] | Nom du score<br/><br/>Contraintes supplémentaires (facultatif) :<li>Changement</li><li>Nouveau score</li><li>Urgence</li><li>Priorité</li><li>Score relatif</li><li>Urgence relative</li><li>Date d’activité</li><li>Min. nombre de fois</li><br/>Délai d’expiration (facultatif) |
| | [!UICONTROL Rebonds SMS] | Message SMS<br/><br/>Contraintes additionnelles (optionnel) : <li>Date d’activité</li><li>Nombre minimum de fois</li><br/>Délai d’expiration (facultatif) |
| Marketo Engage | [!UICONTROL Page Web Visites] | <br/> de page web Sélectionnez une ou plusieurs pages Marketo Engage à faire correspondre. <br/><br/>Contraintes supplémentaires (facultatif) : <li>Chaîne de requête</li><li>Adresse IP du client</li><li>Référent</li><li>Agent utilisateur</li><li>Moteur de recherche</li><li>Requête</li><li>Jeton</li><li>Navigateur</li><li>Platform</li><li>Appareil</li><li>Date d’activité</li> |
| | [!UICONTROL Remplit le formulaire] | <br/> de formulaire Sélectionnez un ou plusieurs formulaires Marketo Engage à faire correspondre. <br/><br/>Contraintes supplémentaires (facultatif) : <li>Date d’activité</li><li>Chaîne de requête</li><li>Adresse IP du client</li><li>Référent</li><li>Agent utilisateur</li><li>Platform</li><li>Appareil</li><br/>Délai d’expiration (facultatif) |
| Adobe Experience Platform | [!UICONTROL Définition de l’événement] | Type d&#39;événement <br/><br/>Contraintes additionnelles (optionnelles) : <li>Champs</li> <br/>Contraintes additionnelles (non prises en charge) : <li>Date d’activité</li><li>Min. nombre de fois</li>Délai d’expiration du <br/> (facultatif) |

### Filtres d’événement de personne

| Filtres | Description |
| ------------ | ----------- |
| [!UICONTROL Historique des activités] > [!UICONTROL E-mail] | Les activités d’e-mail basées sur des conditions qui sont évaluées à l’aide d’un ou de plusieurs e-mails sélectionnés plus haut dans le parcours : <li>[!UICONTROL Lien cliqué dans l’e-mail] <li>E-mail ouvert <li>A été diffusé par e-mail <li>A reçu un e-mail <!-- <br>**[!UICONTROL Switch to inactivity filter]** - Use this option to filter based on lack of activity (a person did not have the email activity).--> |
| [!UICONTROL Historique des activités] > [!UICONTROL Message SMS] | Activités SMS basées sur des conditions qui sont évaluées à l’aide d’un ou de plusieurs messages SMS sélectionnés plus haut dans le parcours : <li>[!UICONTROL Lien cliqué dans le SMS] <li>[!UICONTROL SMS rebond] <!--  <br>**[!UICONTROL Switch to inactivity filter]** - Use this option to filter based on lack of activity (a person did not have the SMS activity). --> |
| [!UICONTROL Historique des activités] > [!UICONTROL Valeur des données modifiée] | Pour un attribut de personne sélectionné, une modification de valeur s’est produite. Ces types de modifications sont les suivants : <li>Nouvelle valeur<li>Valeur précédente<li>Motif<li>Source<li>Date d’activité<li>Min. nombre de fois <!--  <br>**[!UICONTROL Switch to inactivity filter]** - Use this option to filter based on lack of activity (a person did not have a data value change). --> |
| [!UICONTROL Historique des activités] > [!UICONTROL Moment intéressant] | Activité de moment intéressante définie dans l’instance Marketo Engage associée. Les contraintes sont les suivantes : <li>Étape<li>E-mail<li><!-- <br>**[!UICONTROL Switch to inactivity filter]** - Use this option to filter based on lack of activity (a person did not have an interesting moment).--> Web |
| [!UICONTROL Historique des activités] > [!UICONTROL Page web visitée] | Activité de page web qui, pour une ou plusieurs pages web, est gérée par l’instance Marketo Engage associée. Les contraintes sont les suivantes : <li>Page web (obligatoire)<li>Date d’activité<li>Adresse IP du client <li>Chaîne de requête <li>Référent <li>Agent utilisateur <li>Moteur de recherche <li>Requête <li>URL personnalisée <li>Jeton <li>Navigateur <li>Platform <li>Appareil <li>Min. nombre de fois <!-- <br>**[!UICONTROL Switch to inactivity filter]** - Use this option to filter based on lack of activity (a person did not visit the web page). --> |
| [!UICONTROL Attributs de personne] | Attributs du profil de la personne, notamment : <li>Ville <li>Pays <li>Date de naissance <li>Adresse e-mail <li>E-mail non valide <li>E-mail interrompu <li>Prénom <li>Région déduite<li>Titre du traitement <li>Nom <li>Numéro téléphone mobile <li>Score d’engagement de la personne <li>Numéro de téléphone <li>Code postal <li>État <li>Désabonné ou désabonnée <li>Raison désabonnement |
| [!UICONTROL Filtres spéciaux] > [!UICONTROL Membre du groupe d&#39;achat] | La personne est ou n&#39;est pas un membre du groupe d&#39;achats évalué par rapport à un ou plusieurs des critères suivants : <li>Intérêt de la solution</li><li>Statut du groupe d&#39;achat</li><li>Score d&#39;exhaustivité</li><li>Score d’engagement</li><li>Rôle</li> |
| [!UICONTROL Filtres spéciaux] > [!UICONTROL Membre de la liste] | La personne est membre ou non d’une ou de plusieurs listes Marketo Engage. |
| [!UICONTROL Filtres spéciaux] > [!UICONTROL Membre du programme] | La personne est membre ou non d’un ou de plusieurs programmes Marketo Engage. |

### Ajouter un événement de personne

1. Accédez à la carte du parcours.

1. Cliquez sur l’icône plus ( **+** ) d’un chemin et choisissez **[!UICONTROL Écouter un événement]**.

1. Dans les propriétés de nœud sur la droite, choisissez **[!UICONTROL Personnes]** pour le type d’événement.

   ![nœud de Parcours - écoutez les événements sur les personnes](./assets/node-listen-events-people.png){width="700" zoomable="yes"}

1. Sélectionnez un événement dans la liste.

1. Cliquez sur **[!UICONTROL Modifier l’événement]** et définissez les détails de l’événement.

### Écoute d’un événement Marketo Engage

Si vous disposez de pages web dans votre instance Marketo Engage connectée, vous pouvez déclencher un événement en fonction d’une visite ou d’une absence de visite de ces pages web, ainsi que des formulaires Marketo Engage qui ont été remplis ou non.

1. Sélectionnez un nœud **[!UICONTROL Écouter un événement]** dans le mappage de parcours.

1. Dans les propriétés de nœud sur la droite, choisissez **[!UICONTROL Personnes]** pour le type d’événement.

1. Cliquez sur la flèche du sélecteur **[!UICONTROL Sélectionner un événement de personne]** et faites défiler le menu vers la section **[!UICONTROL Marketo Engage]**.

1. Sélectionnez un type d’activité d’engagement de marché :

   * **[!UICONTROL Page Web Visites]**.
   * **[!UICONTROL Remplit Le Formulaire]**

   ![Écouter un événement d’expérience](./assets/node-listen-events-people-me-event.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Modifier l’événement]** et définissez une ou plusieurs pages web à faire correspondre et toute contrainte supplémentaire pour l’événement.

   * (Obligatoire) Dans la boîte de dialogue _[!UICONTROL Modifier l’événement]_, définissez la contrainte **[!UICONTROL Page web]** ou **[!UICONTROL Remplit le formulaire]**. Utilisez **[!UICONTROL is]** (par défaut) pour rechercher une correspondance sur une ou plusieurs pages ou formulaires sélectionnés. Utilisez **[!UICONTROL n’est pas]** pour correspondre à toutes les visites de page/formulaires avec l’exclusion d’une ou de plusieurs pages/formulaires sélectionnés. Vous pouvez également utiliser l’opérateur **[!UICONTROL is any]** pour établir une correspondance lors de toute visite de page web ou de tout formulaire rempli Marketo Engage.

   * (Facultatif) Cliquez sur **[!UICONTROL Ajouter une contrainte]** et sélectionnez le champ à utiliser pour la contrainte. Définissez l’opérateur et la valeur du champ .

     ![Écouter un événement d’expérience](./assets/node-listen-events-people-me-event-edit-dialog.png){width="700" zoomable="yes"}

     Vous pouvez répéter cette action pour inclure d’autres contraintes de champ, si nécessaire.

   * Si nécessaire, sélectionnez l’onglet **[!UICONTROL Filtres]** pour [ajouter des filtres pour l’événement](#add-a-filter-to-the-people-event).

   * Lorsque les contraintes et les filtres sont définis, cliquez sur **[!UICONTROL Terminé]**.

1. Si nécessaire, définissez l’option **[!UICONTROL Temporisation]** pour limiter la période d’écoute de l’événement (voir [Ajouter une temporisation à un nœud d’événement](#add-a-timeout-to-an-event-node)).

1. Dans la carte de parcours, ajoutez le nœud suivant à exécuter lorsque l’événement se produit.

### Écoute d’un événement d’expérience

Les administrateurs peuvent sélectionner [Événements d’expérience Adobe Experience Platform (AEP)](https://experienceleague.adobe.com/fr/docs/experience-platform/xdm/classes/experienceevent){target="_blank"}, ce qui permet aux spécialistes marketing de créer des parcours qui réagissent aux événements en temps quasi réel. L’utilisation d’événements d’expérience dans les parcours est un processus en deux étapes :

1. Un administrateur [sélectionne les types d’événements et les champs d’intérêt](../admin/configure-aep-events.md#select-an-event) pour les rendre disponibles dans les parcours.

2. Dans un parcours, ajoutez un nœud _Écouter un événement_ et sélectionnez un type d’événement Experience Platform pour un événement basé sur des personnes.

<!--
![Video](../../assets/do-not-localize/icon-video.svg){width="30", vertical-align="middle"} [Watch the video overview](../admin/configure-aep-events.md#overview-video) -->

_Pour inclure un événement d’expérience dans votre parcours :_

1. Sélectionnez un nœud **[!UICONTROL Écouter un événement]** dans le mappage de parcours.

1. Dans les propriétés de nœud sur la droite, choisissez **[!UICONTROL Personnes]** pour le type d’événement.

1. Cliquez sur la flèche du sélecteur **[!UICONTROL Sélectionner un événement de personne]** et faites défiler le menu vers la section **[!UICONTROL Adobe Experience Platform]**.

   ![Écouter un événement d’expérience](./assets/node-listen-events-people-aep-events.png){width="700" zoomable="yes"}

1. Sélectionnez l’événement.

   Le type d’événement s’affiche comme vide dans les détails du nœud.

   ![Modifier l’événement](./assets/node-listen-events-people-aep-events-edit.png){width="400" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Modifier l’événement]** et définissez une ou plusieurs contraintes pour l’événement.

   Les contraintes disponibles sont définies en tant que champs gérés pour la configuration de l&#39;événement.

   * Cliquez sur **[!UICONTROL Ajouter une contrainte]** et sélectionnez le champ à utiliser pour la contrainte.

   * Renseignez la condition de la contrainte.

     Vous pouvez utiliser l’opérateur **[!UICONTROL is]** par défaut pour faire correspondre une ou plusieurs valeurs de champ. Vous pouvez également utiliser l’opérateur **[!UICONTROL n’est pas]** pour faire correspondre sur toutes les valeurs avec l’exclusion d’une ou de plusieurs valeurs spécifiées.

     ![Écouter un événement d’expérience](./assets/node-listen-events-people-aep-events-edit-dialog.png){width="700" zoomable="yes"}

   * Si nécessaire, sélectionnez l’onglet **[!UICONTROL Filtres]** pour [ajouter des filtres pour l’événement](#add-a-filter-to-the-people-event).

   * (Facultatif) Cliquez sur **[!UICONTROL Ajouter une contrainte]** et répétez ces étapes pour inclure des contraintes de champ supplémentaires si nécessaire.

   * Lorsque les contraintes et les filtres sont définis, cliquez sur **[!UICONTROL Terminé]**.

1. Si nécessaire, définissez l’option **[!UICONTROL Temporisation]** pour limiter la période d’écoute de l’événement (voir [Ajouter une temporisation à un nœud d’événement](#add-a-timeout-to-an-event-node)).

1. Dans la carte de parcours, ajoutez le nœud suivant à exécuter lorsque l’événement se produit.

1. Renseignez les nœuds restants pour votre parcours et [publiez-le](./journey-overview.md).

   Lorsque le parcours est actif (publié) et atteint le nœud _Écouter pour un événement_, il commence à écouter les événements d’expérience AEP.

### Ajouter des filtres à l’événement personnes

1. Après avoir défini l’événement, sélectionnez l’onglet **[!UICONTROL Filtres]** dans la boîte de dialogue _[!UICONTROL Modifier l’événement]_.

   ![Écouter le nœud d’événement par les personnes - Sélectionnez l’onglet Filtres pour modifier l’événement](./assets/node-listen-event-people-edit-event-filters.png){width="700" zoomable="yes"}

1. Ajoutez un ou plusieurs filtres pour cibler les personnes de l&#39;événement.

   * Effectuez un glisser-déposer de l’un des [filtres de personnes](#people-event-filters) à partir du volet de navigation de gauche et renseignez la définition de correspondance.

     >[!NOTE]
     >
     >Si des champs de personne personnalisés sont définis dans le schéma d’audience du compte dans Experience Platform, ces champs sont également disponibles sous **[!UICONTROL Attributs]** pour être utilisés comme attributs de personne dans les filtres.

   * Ajustez votre filtrage en appliquant la **[!UICONTROL logique de filtre]** en haut. Vous choisissez de faire correspondre tous les filtres ou n’importe quel filtre.

     ![Filtres de personne utilisés dans une définition d’événement](./assets/node-split-conditions-people.png){width="700" zoomable="yes"}

   * Cliquez sur **[!UICONTROL Terminé]**.

## Ajouter une temporisation à un nœud d’événement

Si nécessaire, définissez le temps d’attente du parcours pour l’événement. Le parcours se termine après une temporisation, sauf si vous définissez un chemin de temporisation dans lequel vous pouvez ajouter d’autres nœuds.

1. Activez l’option **[!UICONTROL Délai d’expiration]**.

1. Sélectionnez la durée pendant laquelle le parcours attend qu’un événement se produise avant d’expirer.

   Vous pouvez choisir de terminer le chemin ici ou d’effectuer une autre action en définissant un autre chemin.

1. Pour créer un nouveau chemin dans le parcours où vous pouvez ajouter des actions et des événements applicables aux comptes lorsque l’événement ne se produit pas, cochez la case **[!UICONTROL Définir le chemin de temporisation]**.

   ![Nœud d’événement de Parcours : définissez le chemin de temporisation](./assets/node-event-timeout-set-path.png){width="700" zoomable="yes"}

<!-- ## Overview video

>[!VIDEO](https://video.tv.adobe.com/v/3443236/?captions=fre_fr&learn=on) -->
