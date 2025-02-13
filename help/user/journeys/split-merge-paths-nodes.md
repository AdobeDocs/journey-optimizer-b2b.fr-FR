---
title: Fractionner et fusionner les chemins
description: Découvrez les types de nœuds de chemins de division et de chemins de fusion que vous pouvez utiliser pour orchestrer vos parcours de compte dans Journey Optimizer B2B edition.
feature: Account Journeys
exl-id: 563d6a85-504d-4c70-b075-8a9a9e88bd6b
source-git-commit: d03e0e2d8070916d38bb956adff8dea3f3873aad
workflow-type: tm+mt
source-wordcount: '1519'
ht-degree: 5%

---

# Fractionner et fusionner les chemins

Utilisez les nœuds de chemin de partage et de fusion dans votre parcours de compte pour orchestrer vos parcours de compte. Vous pouvez segmenter l’audience en fonction des conditions que vous définissez et combiner les segments pour continuer.

![Vidéo](../../assets/do-not-localize/icon-video.svg){width="30"} [Regardez la vidéo de présentation](#overview-video)

## Partage de chemins

Ajoutez un nœud _Chemins partagés_ pour définir un ou plusieurs chemins segmentés en fonction des attributs de compte ou de personne.

>[!NOTE]
>
>25 chemins au maximum sont pris en charge.

**Fractionner les chemins d’accès par comptes** : les chemins d’accès fractionnés par comptes peuvent inclure des actions et des événements relatifs au compte et aux personnes. Ces chemins peuvent être divisés davantage.

_Comment fonctionne un nœud de partage de chemin d’accès par comptes ?_

* Lorsque vous ajoutez un nœud de chemin de division et choisissez _Compte_, chaque chemin ajouté comprend un nœud d’extrémité avec la possibilité d’ajouter des nœuds à chaque arête.
* Il est possible de fractionner le chemin d’accès par Comptes à plusieurs reprises, par exemple de manière imbriquée. Un chemin de division comprend une option permettant de ne pas ajouter le chemin par défaut.
* Si un compte ou une personne ne remplit pas les critères de l’un des chemins de partage, il ne progresse pas dans le parcours.
* Ces chemins peuvent être combinés à l’aide d’un nœud de fusion.

![Nœud de Parcours : fractionnez les chemins d’accès par compte](./assets/node-split-paths-account.png){width="700" zoomable="yes"}

**Fractionner les chemins par personnes** : les chemins fractionnés par personnes et ne peuvent inclure que des actions de personnes. Ces chemins ne peuvent pas être fractionnés à nouveau et rejoints automatiquement.

_Comment fonctionne un nœud de partage de chemin par personnes ?_

* _Fractionner le chemin par personnes_ les nœuds sont des nœuds groupés. Les chemins d’accès fusionnent automatiquement afin que toutes les personnes de l’audience puissent passer à l’étape suivante sans perdre le contexte de leur compte.
* _Les nœuds de chemin de partage par personnes_ ne peuvent pas être imbriqués ; vous ne pouvez pas ajouter de chemin de partage pour des personnes sur un chemin qui se trouve dans ce nœud groupé.
* Les nœuds de chemin de partage incluent une option permettant d’omettre un chemin par défaut, de sorte que les comptes/personnes sans chemin de correspondance ne puissent pas avancer dans le parcours.
* _Les nœuds de chemin de partage par personnes_ prennent en charge l’utilisation de _relations compte-personne_, qui vous permettent de filtrer les personnes en fonction de leur rôle (comme entrepreneur ou employé à temps plein), tel que défini dans les modèles de rôles.

![nœud de Parcours - fractionner les chemins par personnes](./assets/node-split-paths-people.png){width="700" zoomable="yes"}

### Conditions de chemin {#path-conditions}

| Contexte du nœud | Conditions de chemin | Description |
| ------------ | --------------- | ----------- |
| [Comptes](#add-a-split-path-by-account-node) | Attributs du compte | Attributs du profil de compte, notamment : <li>Chiffre d’affaires annuel</li><li>Ville</li><li>Pays</li><li>Nombre d’employés</li><li>Secteur industriel</li><li>Nom</li><li>Code SIC</li><li>État</li> |
| | [!UICONTROL Filtres spéciaux] > [!UICONTROL A un groupe d&#39;achat] | Le compte a ou n&#39;a pas de membres de groupes d&#39;achat évalués en fonction d&#39;un ou plusieurs des critères suivants : <li>Intérêt de la solution</li><li>Statut du groupe d&#39;achat</li><li>Score d&#39;exhaustivité</li><li>Évaluation de l’engagement</li> |
| [Personnes](#add-a-split-path-by-people-node) > [!UICONTROL Attributs des personnes uniquement] | [!UICONTROL Attributs de personne] | Attributs du profil de la personne, notamment : <li>Ville</li><li>Pays</li><li>Date de naissance</li><li>Adresse e-mail</li><li>E-mail non valide</li><li>E-mail interrompu</li><li>Prénom</li><li>Région déduite</li><li>Intitulé du poste</li><li>Nom</li><li>Numéro téléphone mobile</li><li>Numéro de téléphone</li><li>Code postal</li><li>État</li><li>Désabonné</li><li>Raison désabonnement</li> |
| | [!UICONTROL Historique des activités] > [!UICONTROL E-mail] | Activités e-mail associées au parcours : <li>[!UICONTROL Lien cliqué dans l’e-mail]</li><li>E-mail ouvert</li><li>A reçu l’e-mail</li><li>A reçu un e-mail</li> Ces conditions sont évaluées à l’aide d’un e-mail sélectionné plus tôt dans le parcours. |
| | [!UICONTROL Historique des activités] > [!UICONTROL Valeur des données modifiée] | Pour un attribut de personne sélectionné, une modification de valeur s’est produite. Ces types de modifications sont les suivants : <li>Nouvelle valeur</li><li>Valeur précédente</li><li>Motif</li><li>Source</li><li>Date d’activité</li><li>Min. nombre de fois</li> |
| | [!UICONTROL Historique des activités] > [!UICONTROL Moment intéressant] | Activité de moment intéressante définie dans l’instance Marketo Engage associée. Les contraintes sont les suivantes : <li>Étape</li><li>E-mail</li><li>Web</li> |
| | [!UICONTROL Filtres spéciaux] > [!UICONTROL Membre du groupe d&#39;achat] | La personne est ou n&#39;est pas un membre du groupe d&#39;achats évalué par rapport à un ou plusieurs des critères suivants : <li>Intérêt de la solution</li><li>Statut du groupe d&#39;achat</li><li>Score d&#39;exhaustivité</li><li>Évaluation de l’engagement</li><li>Rôle</li> |
| | [!UICONTROL Filtres spéciaux] > [!UICONTROL Membre de la liste] | La personne est membre ou non d’une ou de plusieurs listes Marketo Engage. |
| [Personnes](#add-a-split-path-by-people-node) > [!UICONTROL Attributs compte-personne uniquement] | Rôle dans les attributs de compte | Un rôle dans le compte est attribué ou non à la personne. Contraintes facultatives : <li>Saisir un nom de rôle</li> |

### Ajouter un chemin de division par nœud de compte

1. Accédez à l’éditeur de parcours.

1. Cliquez sur l’icône plus ( **+** ) d’un chemin d’accès et choisissez **[!UICONTROL Fractionner les chemins]**.

   ![Ajout d’un nœud de parcours - chemins de division](./assets/add-node-split.png){width="300"}

1. Dans les propriétés de nœud sur la droite, choisissez **[!UICONTROL Comptes]** pour la division.

1. Pour définir une condition applicable à _[!UICONTROL Chemin 1]_, cliquez sur **[!UICONTROL Appliquer la condition]**.

   ![Nœud de chemin de partage - Ajouter une condition](./assets/node-split-properties-apply-condition.png){width="500"}

1. Dans l’éditeur de conditions, ajoutez un ou plusieurs filtres pour définir le chemin de division.

   * Faites glisser et déposez les attributs de filtre à partir du volet de navigation de gauche et terminez la définition de correspondance.

   * Ajustez vos conditions en appliquant la logique **[!UICONTROL Filtre]** en haut. Vous choisissez de faire correspondre toutes les conditions d’attribut ou n’importe quelle condition.

     ![Nœud de chemin partagé - logique de filtre des comptes de conditions](./assets/node-split-conditions-accounts.png){width="700" zoomable="yes"}

   * Cliquez sur **[!UICONTROL Terminé]**.

1. Pour ajouter d’autres chemins d’accès, cliquez sur **[!UICONTROL Ajouter un chemin d’accès]** et répétez les étapes précédentes pour ajouter des conditions applicables à ce chemin d’accès.

   Vous pouvez également libeller chaque chemin d’accès en fonction de ces conditions ou utiliser les libellés par défaut.

1. Si nécessaire, réorganisez les chemins en fonction de la priorité que vous souhaitez pour la division.

   Le filtrage des chemins d’accès est évalué dans l’ordre décroissant. Chaque compte suit le premier chemin qui correspond.

   Cliquez sur les flèches vers le haut et vers le bas en haut à droite de chaque carte de chemin pour la déplacer vers le haut ou le bas dans la liste des chemins.

   ![Nœud de chemin partagé - réorganiser les chemins](./assets/node-split-reorder-paths-accounts.png){width="500" zoomable="yes"}

1. Activez l’option **[!UICONTROL Autres comptes]** pour ajouter un chemin d’accès par défaut pour les comptes qui ne correspondent pas aux chemins d’accès définis. Si ce n&#39;est pas le cas, le parcours se termine pour ces gens.

### Ajouter un nœud de partage de chemin par personnes

>[!NOTE]
>
>Lorsque vous fractionnez des chemins par personnes, un nœud _Fermer les chemins fractionnés_ est automatiquement inséré pour mettre fin à la division. Un chemin d’accès fractionné par personnes permet uniquement d’_effectuer une action_ sur les nœuds de personnes.

1. Accédez à l’éditeur de parcours.

1. Cliquez sur l’icône plus ( **+** ) d’un chemin d’accès et choisissez **[!UICONTROL Fractionner les chemins]**.

   ![Ajout d’un nœud de parcours - chemins de division](./assets/add-node-split.png){width="300"}

1. Dans les propriétés de nœud sur la droite, choisissez **[!UICONTROL Personnes]** pour la division.

1. Définissez les **[!UICONTROL Attributs utilisés pour les conditions]**.

   * Choisissez **[!UICONTROL Attributs de personne uniquement]** pour utiliser des conditions liées au profil de personne et aux événements.
   * Choisissez **[!UICONTROL Attributs de compte-personne uniquement]** pour utiliser des conditions liées à l’appartenance au rôle de la personne au sein d’un compte.

1. Pour définir une condition applicable à _[!UICONTROL Chemin 1]_, cliquez sur **[!UICONTROL Appliquer la condition]**.

1. Dans l’éditeur de conditions, ajoutez un ou plusieurs filtres pour définir le chemin de division.

   * Faites glisser et déposez l’un des attributs de personne à partir du volet de navigation de gauche et terminez la définition de la correspondance.

     >[!NOTE]
     >
     >Si des champs de personne personnalisés sont définis dans le schéma d’audience du compte dans Experience Platform, ces champs peuvent également être utilisés en tant qu’attributs de personne dans des conditions.

   * Ajustez vos conditions en appliquant la logique **[!UICONTROL Filtre]** en haut. Vous choisissez de faire correspondre toutes les conditions d’attribut ou n’importe quelle condition.

     ![Nœud de chemin partagé - conditionne la logique de filtre de personne](./assets/node-split-conditions-people.png){width="700" zoomable="yes"}

   * Cliquez sur **[!UICONTROL Terminé]**.

1. Pour ajouter d’autres chemins d’accès, cliquez sur **[!UICONTROL Ajouter un chemin d’accès]** et répétez les étapes précédentes pour ajouter des conditions applicables à ce chemin d’accès.

   Vous pouvez également libeller chaque chemin d’accès en fonction de ces conditions ou utiliser les libellés par défaut.

1. Si nécessaire, réorganisez les chemins en fonction de la priorité que vous souhaitez pour la division.

   Le filtrage des chemins d’accès est évalué dans l’ordre décroissant. Chaque personne suit le premier chemin correspondant.

   Cliquez sur les flèches vers le haut et vers le bas en haut à droite de chaque carte de chemin pour la déplacer vers le haut ou le bas dans la liste des chemins.

   ![Nœud de chemin partagé - réorganiser les chemins](./assets/node-split-reorder-paths-people.png){width="500" zoomable="yes"}

1. Activez l’option **[!UICONTROL Autres personnes]** pour ajouter un chemin par défaut pour les personnes qui ne correspondent pas aux chemins définis. Si ce n&#39;est pas le cas, le parcours se termine pour ces gens.

>[!BEGINSHADEBOX « Appartenance à une liste Marketo Engage »]

Dans Marketo Engage, les _campagnes intelligentes_ vérifient l’adhésion aux programmes pour vous assurer que les prospects ne reçoivent pas d’e-mails en double et ne sont pas membres de plusieurs flux d’e-mails en même temps. Dans Journey Optimizer B2B, vous pouvez vérifier l’appartenance à une liste Marketo Engage comme condition de votre chemin de partage par personnes afin d’éliminer la duplication dans les activités de parcours.

Pour ce faire, développez **[!UICONTROL Filtres spéciaux]** et faites glisser la condition **[!UICONTROL Membre de la liste]** dans l’espace de filtrage, puis renseignez la définition du filtre pour évaluer l’appartenance à une ou plusieurs listes Marketo Engage.

![Condition de partage du chemin par personnes pour l’appartenance à la liste Marketo Engage](./assets/node-split-paths-conditions-people-member-of-list.png){width="700" zoomable="yes"}

>[!ENDSHADEBOX]

Lorsque des conditions sont définies pour chaque chemin d’accès afin de fractionner votre audience au niveau des personnes, vous pouvez ajouter des actions que vous souhaitez entreprendre sur les personnes.

>[!NOTE]
>
>Lorsque vous fractionnez l’audience par personnes, vous ne pouvez ajouter que des actions de personnes jusqu’à ce que les chemins soient fermés ou fusionnés.

## Fusionner les chemins

Ajoutez un nœud _Fusionner les chemins_ pour combiner différents chemins fractionnés par compte dans votre parcours.

1. Accédez à l’éditeur de parcours.

1. Cliquez sur l’icône plus ( **+** ) d’un chemin d’accès et choisissez **[!UICONTROL Fractionner les chemins]**.

1. Cliquez sur le nœud de partage pour ouvrir ses propriétés sur la droite.

1. Cliquez sur [!UICONTROL Ajouter un chemin] pour créer trois chemins.

1. Ajoutez une combinaison d’actions et d’événements à chaque chemin.

1. Cliquez sur l’icône plus ( **+** ) pour l’un de ces chemins d’accès et choisissez **[!UICONTROL Fusionner]** dans les options affichées.

   ![nœud de Parcours - fusionner les chemins](./assets/node-plus-icon-merge-paths.png){width="400"}

1. Dans les propriétés du nœud de chemins de fusion, sélectionnez les chemins à fusionner.

   ![nœud de Parcours - fusionner les chemins](./assets/node-merge-select-paths.png){width="600" zoomable="yes"}

   À ce stade, les chemins d’accès sont fusionnés afin que les comptes des chemins d’accès sélectionnés se combinent pour former un chemin d’accès unique qui peut continuer à progresser dans le parcours.

1. Si nécessaire, vous pouvez annuler la fusion des chemins en revenant aux propriétés du nœud de chemins de fusion et en décochant la case correspondant aux chemins que vous souhaitez supprimer.

## Vidéo de présentation

>[!VIDEO](https://video.tv.adobe.com/v/3443231/?learn=on)
