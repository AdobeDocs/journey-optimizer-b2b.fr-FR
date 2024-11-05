---
title: Noeuds de Parcours de compte
description: Découvrez les types de noeuds que vous pouvez utiliser pour créer vos parcours de compte dans Journey Optimizer B2B edition.
feature: Account Journeys
exl-id: 4edb87d9-cdf8-47a4-968b-6dc76d97b89c
source-git-commit: 30075a1804e520b9908ef6b2217a8a91e33e0a84
workflow-type: tm+mt
source-wordcount: '2142'
ht-degree: 10%

---

# Noeuds de Parcours de compte

Après avoir [créé un parcours de compte](journey-overview.md#create-an-account-journey) et [ajouté l’audience](journey-overview.md#add-the-account-audience-for-your-journey), construisez le parcours à l’aide de noeuds. La carte de parcours fournit un canevas, où vous pouvez créer vos cas d’utilisation marketing B2B à plusieurs étapes.

Créez votre parcours de compte en combinant les différents noeuds d’action, d’événement et d’orchestration sous la forme d’un scénario cross-canal à plusieurs étapes. Chaque noeud d’un parcours représente une étape le long d’un chemin logique. Utilisez les types de noeuds suivants pour créer un parcours de compte :

* [Audience (comptes)](#account-audience-node)
* [Agir](#take-an-action)
* [Écoute d’un événement](#listen-for-an-event)
* [Fractionner les chemins](#split-paths)
* [Attente](#wait)
* [Fusion des chemins](#merge-paths)

## Noeud Audience du compte

Le noeud [Audience du compte](journey-overview.md#add-the-account-audience-for-your-journey) définit l’audience du compte d’entrée (créée et gérée dans Adobe Experience Platform) pour le parcours. Ce noeud est toujours le premier noeud et est automatiquement créé par défaut.

## Agir

Exécutez une action comme envoyer un email, modifier un score, affecter à un groupe d’achats, etc.

**Action sur les comptes** : l’action est appliquée à toutes les personnes qui font partie de comptes sur ce chemin.

**Action sur les personnes** : l’action est appliquée à toutes les personnes sur ce chemin. Une action sur les personnes peut être utilisée dans le chemin partagé par les personnes ou le chemin partagé par les comptes.

### Actions et contraintes {#action-nodes}

| Contexte du noeud | Action | Contraintes |
| ------------ | ------ | ----------- |
| [Personnes](#add-a-people-action) | Ajouter à la liste | Sélectionnez Marketo Engage workspace<br/>Nom de liste |
| | Ajouter à la campagne de demande de Marketo Engage | Sélectionnez l’espace de travail Marketo Engage<br/>Sélectionner une campagne de requête |
| | Attribuer au groupe d’achat | Sélectionner un rôle dans l’intérêt de la solution<br/>Sélectionner un rôle |
| | Modification de la partition du peuple en Marketo Engage | Nouvelle répartition |
| | Modifier évaluation | Nom de la note<br/>Modifier |
| | Moment intéressant pour la personne | Type<br/>Description |
| | Supprimer du groupe d’achat | Sélectionner l’intérêt de la solution |
| | Supprimer de la liste | Sélectionnez Marketo Engage workspace<br/>Nom de liste |
| | Envoyer un e-mail | Créer un email<br/>Sélectionner un email à partir du Marketo Engage |
| | Envoyer un SMS | Créer un SMS |
| [Comptes](#add-an-account-action) | Valeur des données de changement de compte | Sélectionnez attribute<br/>Nouvelle valeur |
| | Moment intéressant du compte | Type (Email, Milestone ou Web)<br/>Description (facultatif) |
| | Ajouter un compte à (autre) Parcours | Sélectionner le Parcours de compte en direct |
| | Supprimer le compte du Parcours | Sélectionner le Parcours de compte en direct |
| | Envoyer une alerte de ventes | Sélectionner l’intérêt de la solution<br/>Envoyer un courrier électronique à |
| | Mise à jour de l’état du groupe d’achat | Sélectionner l’intérêt de la solution <br/>État (requis, 50 caractères max.) |

### Ajouter une action de compte

1. Accédez à l’éditeur de parcours.

1. Cliquez sur l’icône plus ( **+** ) sur un chemin et sélectionnez **[!UICONTROL Agir sur une action]**.

   ![ Ajouter un noeud de parcours - Chemins de division](./assets/add-node-action.png){width="400"}

1. Dans les propriétés du noeud à droite, sélectionnez **[!UICONTROL Comptes]** pour l’action.

1. Sélectionnez une action dans la liste et définissez les valeurs de l’action.

   ![Noeud de Parcours - effectuer une action sur un compte](./assets/node-take-action-account.png){width="700" zoomable="yes"}

### Ajout d’une action Personnes

1. Accédez à l’éditeur de parcours.

1. Cliquez sur l’icône plus ( **+** ) sur un chemin et sélectionnez **[!UICONTROL Agir sur une action]**.

1. Dans les propriétés du noeud à droite, sélectionnez **[!UICONTROL People]** pour l’action.

1. Sélectionnez une action dans la liste et définissez les valeurs de l’action.

![Noeud de Parcours - effectuer une action sur les personnes](./assets/node-take-action-people.png){width="700" zoomable="yes"}

## Écoute d’un événement

Déplacez votre audience vers l’étape suivante du parcours lorsqu’un événement se produit.

* Vous pouvez également définir la durée pendant laquelle le parcours attend cet événement. Le parcours se termine après un délai d’expiration.
* En outre, vous pouvez choisir d’ajouter d’autres noeuds sur votre chemin d’accès au délai d’expiration.

**Écouter les événements sur les comptes** : si au moins une personne d’un compte déclenche un événement, le compte passe à l’étape suivante du parcours.

**Écouter les événements sur les personnes** : les événements sur les personnes ne peuvent être appliqués que sur un chemin d’accès au compte ; il n’est pas disponible pour un noeud partagé par les personnes.

### Événements et contraintes {#event-nodes}

| Contexte du noeud | Événement | Contraintes |
| ------------ | ----- | ----------- |
| [Personnes](#add-a-people-event) | Affecté à un groupe d’achat | Centre d’intérêt de la solution<br/>Contraintes supplémentaires (facultatif) : <ul><li>Rôle</li><li>Date d’activité</li></ul><br/> Délai d’expiration (facultatif) |
| | Clique sur un lien dans un e-mail | Email<br/>Contraintes supplémentaires (facultatif) : <ul><li>Lien</li><li>ID lien</li><li>Est un appareil mobile</li><li>Appareil</li><li>Platform</li><li>Navigateur</li><li>Est du contenu prédictif</li><li>Est une activité du bot</li><li>Modèle d’activité du bot</li><li>Navigateur</li><li>Date d’activité</li><li>Min. nombre de fois</li></ul><br/> Délai d’expiration (facultatif) |
| | Clics lien dans SMS | Email<br/>Contraintes supplémentaires (facultatif) :<ul><li>Lien</li><li>Appareil</li><li>Platform</li><li>Date d’activité</li><li>Min. nombre de fois</li></ul><br/> Délai d’expiration (facultatif) |
| | Modifications valeur des données | Attribut Personne<br/>Contraintes supplémentaires (facultatif) :<ul><li>Nouvelle valeur</li><li>Valeur précédente</li><li>Motif</li><li>Source</li><li>Date d’activité</li><li>Min. nombre de fois</li></ul><br/> Délai d’expiration (facultatif) |
| | Ouvre l’e-mail | Email<br/>Contraintes supplémentaires (facultatif) : <ul><li>Lien</li><li>ID lien</li><li>Est un appareil mobile</li><li>Appareil</li><li>Platform</li><li>Navigateur</li><li>Est du contenu prédictif</li><li>Est une activité du bot</li><li>Modèle d’activité du bot</li><li>Navigateur</li><li>Date d’activité</li><li>Min. nombre de fois</li></ul><br/> Délai d’expiration (facultatif) |
| | Supprimé du groupe d’achat | Centre d’intérêt de la solution<br/>Date d’activité (facultatif)<br/>Délai d’expiration (facultatif) |
| | Modification du score | Nom de la note<br/>Contraintes supplémentaires (facultatif) :<ul><li>Changement</li><li>Nouveau score</li><li>Urgence</li><li>Priorité</li><li>Score relatif</li><li>Urgence relative</li><li>Date d’activité</li><li>Min. nombre de fois</li></ul><br/> Délai d’expiration (facultatif) |
| | SMS Bounces | Message SMS<br/>Contraintes supplémentaires (facultatif) :<ul><li>Date d’activité</li><li>Nombre minimum de fois</li></ul><br/> Délai d’expiration (facultatif) |
| [Comptes](#add-an-account-event) | Le compte a eu un moment intéressant | Type (Email, Milestone ou Web)<br/>Contraintes supplémentaires (facultatif) :<ul><li>Description</li><li>Source</li><li>Date d’activité</li></ul> <br/> Délai d’expiration (facultatif) |
| | Modification de la valeur des données du compte | Attribute<br/>Contraintes supplémentaires (facultatif) :<ul><li>Nouvelle valeur</li><li>Valeur précédente</li><li>Date d’activité</li></ul> <br/> Délai d’expiration (facultatif) |
| | Modification de l’état du groupe d’achat | Centre d’intérêt de la solution<br/>Contraintes supplémentaires (facultatif) :<ul><li>Nouveau statut</li><li>Statut précédent</li><li>Date d’activité</li></ul><br/> Délai d’expiration (facultatif) |
| | Modification du score d’exhaustivité | Centre d’intérêt de la solution<br/>Contraintes supplémentaires (facultatif) :<ul><li>Nouveau score</li><li>Score précédent</li><li>Date d’activité</li></ul><br/> Délai d’expiration (facultatif) |
| | Changement du score d’engagement | Centre d’intérêt de la solution<br/>Contraintes supplémentaires (facultatif) :<ul><li>Nouveau score</li><li>Score précédent</li><li>Date d’activité</li></ul><br/> Délai d’expiration (facultatif) |

### Ajout d’un événement de compte

1. Accédez à l’éditeur de parcours.

1. Cliquez sur l’icône plus ( **+** ) sur un chemin d’accès et sélectionnez **[!UICONTROL Listen for an event]**.

1. Dans les propriétés du noeud à droite, sélectionnez **[!UICONTROL Comptes]** pour le type d’événement.

   ![Noeud de Parcours - écoute des événements sur le compte](./assets/node-listen-events-account.png){width="700" zoomable="yes"}

1. Sélectionnez un événement dans la liste.

1. Cliquez sur **[!UICONTROL Modifier l’événement]** et définissez les détails de l’événement.

### Ajout d’un événement Personnes

1. Accédez à l’éditeur de parcours.

1. Cliquez sur l’icône plus ( **+** ) sur un chemin d’accès et sélectionnez **[!UICONTROL Listen for an event]**.

1. Dans les propriétés du noeud à droite, choisissez **[!UICONTROL People]** pour le type d’événement.

   ![Noeud de Parcours - écoute des événements sur les personnes](./assets/node-listen-events-people.png){width="700" zoomable="yes"}

1. Sélectionnez un événement dans la liste.

1. Cliquez sur **[!UICONTROL Modifier l’événement]** et définissez les détails de l’événement.

### Ajout d’un délai d’expiration à un noeud d’événement

Si nécessaire, définissez la durée pendant laquelle le parcours attend l’événement. Le parcours se termine après un délai d’expiration.

1. Activez le bouton d’activation/désactivation du délai d’expiration.

1. Sélectionnez la durée pendant laquelle le parcours attend qu’un événement se produise avant de expirer.

   Vous pouvez choisir de terminer le chemin ici ou d’effectuer une autre action en définissant un autre chemin.

1. Pour créer un chemin d’accès dans le parcours où vous pouvez ajouter des actions et des événements applicables aux comptes lorsque l’événement ne se produit pas, cochez la case **[!UICONTROL Définir le chemin d’accès au délai d’expiration]** .

   ![Noeud d’événement de Parcours - définir le chemin d’accès au délai d’expiration](./assets/node-event-timeout-set-path.png){width="700" zoomable="yes"}

## Diviser les chemins

Divisez votre audience en fonction des conditions de filtrage.

>[!NOTE]
>
>25 chemins au maximum sont pris en charge.

**Partage des chemins par comptes** : les chemins fractionnés par comptes peuvent inclure à la fois des actions et des événements de compte et de personne. Ces chemins peuvent être fractionnés plus loin.

_Comment fonctionne un chemin de partage par noeud de comptes ?_

* Lorsque vous ajoutez un noeud de chemin d’accès partagé et choisissez _Compte_, chaque chemin d’accès ajouté inclut un noeud de fin avec la possibilité d’ajouter des noeuds à chaque périphérie.
* Il est possible de fractionner le chemin en plusieurs fois par Comptes, par exemple de manière imbriquée. Un chemin partagé comprend une option permettant de ne pas ajouter le chemin par défaut.
* Si un compte/une personne ne remplit pas les conditions requises pour l’un des chemins de division, il ne passe pas en arrière dans le parcours.
* Ces chemins d’accès peuvent être combinés à l’aide d’un noeud de fusion.

![Noeud de Parcours - division des chemins par compte](./assets/node-split-paths-account.png){width="700" zoomable="yes"}

**Partage des chemins par personnes** : chemins fractionnés par personnes et ne peuvent inclure que des actions de personnes. Ces chemins ne peuvent pas être fractionnés à nouveau et rejoints automatiquement.

_Comment fonctionne un chemin de division par noeud de personnes ?_

* Les chemins d’accès fractionnés par les noeuds de personnes sont des noeuds regroupés. Ils fusionnent automatiquement afin que toutes les personnes de l’audience puissent passer à l’étape suivante sans perdre le contexte des comptes auxquels elles appartiennent.
* Le chemin de division des personnes ne peut pas être imbriqué : vous ne pouvez pas ajouter de chemin de division pour les personnes qui se trouvent dans ce noeud groupé.
* Le chemin de division comprend une option permettant de ne pas ajouter de chemin par défaut. Les comptes/personnes qui ne remplissent pas les critères ne sont pas redirigés dans le Parcours.

![Noeud de Parcours - division des chemins par personnes](./assets/node-split-paths-people.png){width="700" zoomable="yes"}

### Conditions de chemin {#path-conditions}

| Contexte du noeud | Conditions de chemin | Description |
| ------------ | --------------- | ----------- |
| [Personnes](#add-a-split-path-by-people-node) | [!UICONTROL Attributs de personne] | Attributs du profil de la personne, notamment : <ul><li>Ville</li><li>Pays</li><li>Date de naissance</li><li>Adresse e-mail</li><li>E-mail non valide</li><li>E-mail interrompu</li><li>Prénom</li><li>Région déduite</li><li>Intitulé du poste</li><li>Nom</li><li>Numéro téléphone mobile</li><li>Numéro de téléphone</li><li>Code postal</li><li>État</li><li>Désabonné</li><li>Raison désabonnement</li></ul> |
| | [!UICONTROL Historique des activités] > [!UICONTROL Email] | Activités de courrier électronique associées au parcours : <ul><li>[!UICONTROL Lien cliqué dans le courrier électronique]</li><li>E-mail ouvert</li><li>A reçu l’e-mail</li><li>A reçu un e-mail</li></ul> Ces conditions sont évaluées à l’aide d’un message électronique sélectionné plus tôt dans le parcours. |
| | [!UICONTROL Historique des activités] > [!UICONTROL Valeur de données modifiée] | Pour un attribut de personne sélectionné, un changement de valeur s’est produit. Ces types de modification incluent : <ul><li>Nouvelle valeur</li><li>Valeur précédente</li><li>Motif</li><li>Source</li><li>Date d’activité</li><li>Min. nombre de fois</li></ul> |
| | [!UICONTROL Historique Des Activités] > [!UICONTROL A Eu Un Moment Intéressant] | Activité de moment intéressant définie dans l’instance de Marketo Engage associée. Les contraintes incluent : ul><li>Étape</li><li>E-mail</li><li>Web</li></ul> |
| | [!UICONTROL Filtres spéciaux] > [!UICONTROL Membre du groupe d’achats] | La personne est ou n’est pas un membre du groupe d’achat évalué selon un ou plusieurs des critères suivants : <ul><li>Intérêt pour la solution</li><li>Statut du groupe d’achat</li><li>Score de complétude</li><li>Évaluation de l’engagement</li><li>Rôle</li></ul> |
| [Comptes](#add-a-split-path-by-account-node) | Attributs du compte | Attributs du profil du compte, notamment : <ul><li>Chiffre d’affaires annuel</li><li>Ville</li><li>Pays</li><li>Nombre d’employés</li><li>Secteur industriel</li><li>Nom</li><li>Code SIC</li><li>État</li></ul> |
| | [!UICONTROL Filtres spéciaux] > [!UICONTROL Avec groupe d’achat] | Les membres des groupes d’achats du compte sont évalués ou non selon un ou plusieurs des critères suivants : <ul><li>Intérêt pour la solution</li><li>Statut du groupe d’achat</li><li>Score de complétude</li><li>Évaluation de l’engagement</li></ul> |

### Ajout d’un chemin de division par noeud de compte

1. Accédez à l’éditeur de parcours.

1. Cliquez sur l’icône plus ( **+** ) sur un chemin et sélectionnez **[!UICONTROL Fractionner les chemins]**.

   ![ Ajouter un noeud de parcours - Chemins de division](./assets/add-node-split.png){width="300"}

1. Dans les propriétés du noeud à droite, sélectionnez **[!UICONTROL Comptes]** pour le partage.

1. Pour définir une condition applicable à _[!UICONTROL Path 1]_, cliquez sur **[!UICONTROL Apply condition]**.

   ![Noeud de chemin d’accès partagé - ajouter une condition](./assets/node-split-properties-apply-condition.png){width="500"}

1. Dans l’éditeur de conditions, ajoutez un ou plusieurs filtres pour définir le chemin de division.

   * Faites glisser et déposez les attributs de filtre depuis le volet de navigation de gauche et complétez la définition de correspondance.

   * Réglez vos conditions en appliquant la **[!UICONTROL logique de filtre]** en haut. Vous choisissez de correspondre à toutes les conditions d’attribut ou à n’importe quelle condition.

     ![Noeud de chemin de division - conditions logique de filtre](./assets/node-split-conditions.png){width="700" zoomable="yes"}

   * Cliquez sur **[!UICONTROL Terminé]**.

1. Pour ajouter d’autres chemins, cliquez sur **[!UICONTROL Ajouter un chemin]** et répétez les étapes précédentes pour ajouter des conditions applicables à ce chemin.

   Vous pouvez également libeller chaque chemin en fonction de ces conditions ou utiliser les libellés par défaut.

1. (Facultatif) Ajoutez un chemin par défaut pour les comptes non qualifiés pour les autres chemins. Dans le cas contraire, le parcours se termine pour ces comptes.

   ![ Diviser les propriétés du noeud de chemin d’accès - autres comptes](./assets/node-split-properties-other-accounts.png){width="700" zoomable="yes"}

### Ajouter un chemin de partage par noeud people

1. Accédez à l’éditeur de parcours.

1. Cliquez sur l’icône plus ( **+** ) sur un chemin et sélectionnez **[!UICONTROL Fractionner les chemins]**.

   ![ Ajouter un noeud de parcours - Chemins de division](./assets/add-node-split.png){width="300"}

1. Dans les propriétés du noeud à droite, sélectionnez **[!UICONTROL Personnes]** pour la division.

1. Pour définir une condition applicable à _[!UICONTROL Path 1]_, cliquez sur **[!UICONTROL Apply condition]**.

1. Dans l’éditeur de conditions, ajoutez un ou plusieurs filtres pour définir le chemin de division.

   * Faites glisser et déposez les attributs de filtre depuis le volet de navigation de gauche et complétez la définition de correspondance.

   * Réglez vos conditions en appliquant la **[!UICONTROL logique de filtre]** en haut. Vous choisissez de correspondre à toutes les conditions d’attribut ou à n’importe quelle condition.

   * Cliquez sur **[!UICONTROL Terminé]**.

1. Pour ajouter d’autres chemins, cliquez sur **[!UICONTROL Ajouter un chemin]** et répétez les étapes précédentes pour ajouter des conditions applicables à ce chemin.

   Vous pouvez également libeller chaque chemin en fonction de ces conditions ou utiliser les libellés par défaut.

1. Enfin, vous pouvez ajouter un chemin par défaut pour les personnes non qualifiées pour les chemins ci-dessus. Si ce n&#39;est pas le cas, le parcours se termine pour ces gens.

Lorsque des conditions sont définies pour chaque chemin de division de votre audience au niveau des personnes, vous pouvez ajouter des actions que vous souhaitez entreprendre sur les personnes.

>[!NOTE]
>
>Lorsque vous divisez l’audience par des personnes, vous ne pouvez ajouter que des actions de personnes.

## Attente

Patientez pendant une certaine durée avant de passer à l’étape suivante.

1. Accédez à l’éditeur de parcours.

1. Cliquez sur l’icône plus ( **+** ) sur un chemin et choisissez **[!UICONTROL Attente]**.

1. Dans les propriétés du noeud à droite, définissez la **[!UICONTROL durée]** d’attente avant que le parcours ne passe au noeud suivant du chemin d’accès.

![Noeud de Parcours - wait](./assets/node-wait.png){width="700" zoomable="yes"}

## Fusion des chemins

Différents chemins d’accès de votre parcours peuvent être fusionnés et non fusionnés à l’aide de ce noeud.

1. Accédez à l’éditeur de parcours.

1. Cliquez sur l’icône plus ( **+** ) sur un chemin et sélectionnez **[!UICONTROL Fractionner les chemins]**.

1. Cliquez sur le noeud partagé pour ouvrir ses propriétés à droite.

1. Cliquez sur [!UICONTROL Ajouter un chemin] pour créer trois chemins.

1. Ajoutez une combinaison d’actions et d’événements à chaque chemin.

1. Cliquez sur l’icône plus ( **+** ) pour l’un de ces chemins et sélectionnez **[!UICONTROL Fusionner]** parmi les options affichées.

   ![Noeud de Parcours - Chemins de fusion](./assets/node-plus-icon-merge-paths.png){width="400"}

1. Dans les propriétés du noeud de fusion, sélectionnez les chemins à fusionner.

   ![Noeud de Parcours - Chemins de fusion](./assets/node-merge-select-paths.png){width="600" zoomable="yes"}

   À ce stade, les chemins sont fusionnés afin que les comptes des chemins sélectionnés se combinent en un seul chemin qui peut continuer à progresser dans le parcours.

1. Si nécessaire, vous pouvez annuler la fusion des chemins en revenant aux propriétés du noeud de fusion et en désélectionnant la case correspondant aux chemins que vous souhaitez supprimer.
