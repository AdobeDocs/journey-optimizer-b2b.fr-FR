---
title: Gestion des parcours
description: 'Rationalisez la génération de la demande avec les parcours : créez, publiez, gérez l’engagement des groupes d’achats par e-mail, SMS et événements dans Journey Optimizer B2B edition.'
feature: Account Journeys
role: User
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: 6511f40329df34db665ed6f971fa20670be0ae32
workflow-type: tm+mt
source-wordcount: '1521'
ht-degree: 44%

---


# Gestion des parcours

Dans Journey Optimizer B2B edition, les parcours sont des plans marketing automatisés, à comptes à plusieurs étapes et basés sur des prospects qui orchestrent des expériences personnalisées sur plusieurs canaux en réponse à l’engagement, aux événements métier ou aux campagnes planifiées. Définissez un engagement axé sur les ventes qui inclut des e-mails, des SMS, etc. dans le but de coordonner le marketing entrant avec les activités de vente sortantes pour chaque membre du groupe d’achat.

Journey Optimizer B2B edition prend en charge deux types de parcours :

* **parcours de compte** - Rationalisez la génération de la demande et la qualification des groupes d’achat et stimulez la demande qualifiée pour vos programmes d’acquisition, de vente incitative/croisée et de rétention. Paramétrez des parcours personnalisés pour chaque groupe d’achat et membre du groupe d’achat à l’aide d’un engagement automatisé par e-mail, SMS, événement, etc.

  ![Vidéo](../../assets/do-not-localize/icon-video.svg){width="30"} [Regardez la vidéo de présentation du parcours de compte](#overview-video)

* **parcours de personne** - (Beta) Orchestrez le marketing basé sur les prospects à l’aide des audiences et des données Experience Platform. Avec les parcours de personne, vos opérations marketing ne dépendent pas de Marketo Engage ou de solutions de contournement pour les chaînes d’outils Adobe Campaign/B2C afin qu’elles puissent fonctionner avec les cas d’utilisation B2B.

  Utilisé de concert avec les parcours de compte et les groupes d’achat, un parcours de personne peut fournir aux marketeurs le pouvoir d’appliquer une orchestration complète au parcours d’achat.

  +++Limites actuelles des parcours de personne

  Certaines limitations peuvent bloquer certains cas d’utilisation ou entraîner des difficultés pour créer des parcours de personne. De nombreux problèmes résultent de la mise en œuvre initiale du programme bêta et devront être résolus ultérieurement.

   * Les événements ne peuvent pas être combinés avec des attributs de profil pour réduire les définitions d’audience.
   * Le contexte de l’événement qui qualifie un profil pour un parcours ne peut pas être utilisé pour la personnalisation ou l’orchestration.
   * Parcours ne peut actuellement pas avoir à la fois un événement et un critère d’entrée de segment de profil.
   * Les écouteurs d’événements ne peuvent pas écouter plusieurs événements.
   * Les nœuds d’attente ne disposent actuellement pas d’une suite complète d’options pour les critères de sortie de jour de la semaine ou d’heure de la journée.
   * L’éditeur d’e-mail fait référence de manière incorrecte à des fonctionnalités et attributs qui ne sont disponibles que pour les Parcours de compte
   * La prise en charge des jetons de parcours personnalisés (_Mes jetons_) n’est pas encore disponible.
   * Les nœuds de parcours Ajouter et Supprimer de la personne ne sont actuellement disponibles dans aucun des types de parcours.
   * L’historique des événements ne peut pas être utilisé pour l’orchestration ou la personnalisation.
   * Les objets associés (tels que le compte, le groupe d’achat, l’opportunité et les objets personnalisés) ne peuvent pas être utilisés pour l’orchestration ou la personnalisation.
   * Les canaux web, SMS et de plateforme publicitaire ne sont actuellement pas pris en charge.

  +++

## Commencer avec un parcours

Pour commencer à utiliser votre premier parcours :

1. [Créez un parcours](./create-publish-journey.md#create-a-journey).
1. [Ajoutez les nœuds](./create-publish-journey.md#add-a-node) et [définissez le flux de parcours](./create-publish-journey.md#add-and-delete-a-path) dans la cartographie du parcours.
1. [Publiez le parcours](./create-publish-journey.md#publish-a-journey).

## Accéder à vos parcours et les parcourir

>[!BEGINTABS]

>[!TAB parcours de compte]

Dans le volet de navigation de gauche, développez **[!UICONTROL Gestion des Parcours]** puis cliquez sur **[!UICONTROL parcours de compte]**.

Saisissez du texte dans l’outil _Rechercher_ en haut de la liste pour filtrer la liste affichée par nom.

![Filtrage de la liste des parcours de compte](./assets/account-journeys-list-search-filter.png){width="800" zoomable="yes"}

>[!TAB parcours de personne (Beta)]

[!BADGE Beta]{type=Informative tooltip="Disponible en version bêta sur l’architecture simplifiée"}

Dans le volet de navigation de gauche, développez **[!UICONTROL Gestion des Parcours]** puis cliquez sur **[!UICONTROL parcours de personne]**.

Saisissez du texte dans l’outil _Rechercher_ en haut de la liste pour filtrer la liste affichée par nom.

![Filtrer la liste des parcours de personne](./assets/person-journeys-list-search-filter.png){width="800" zoomable="yes"}

>[!ENDTABS]

### Colonnes de liste de parcours

La page de liste parcours comprend les colonnes suivantes :

* [!UICONTROL Nom] (cliquer sur le nom pour ouvrir le parcours et le modifier)
* [!UICONTROL Statut]
* [!UICONTROL Date de création]
* [!UICONTROL Créé par]
* [!UICONTROL Dernière mise à jour]
* [!UICONTROL Dernière mise à jour par]
* [!UICONTROL Publié sur]
* [!UICONTROL Publié par]
* [!UICONTROL &#x200B; Date de début &#x200B;]
* [!UICONTROL &#x200B; Date de fin &#x200B;]

Vous pouvez trier la liste par _[!UICONTROL Statut]_, _[!UICONTROL Date de création]_ ou _[!UICONTROL Dernière mise à jour]_ en cliquant sur l’en-tête de colonne.

Pour personnaliser (afficher/masquer) les colonnes affichées dans le tableau, cliquez sur l’icône _Personnaliser le tableau_ ( ![Personnaliser le tableau](../assets/do-not-localize/icon-column-settings.svg) ) dans le coin supérieur droit. Cochez ou décochez les cases de la boîte de dialogue, puis cliquez sur **[!UICONTROL Appliquer]**.

![Choisissez les colonnes à afficher dans la liste parcours &#x200B;](./assets/account-journeys-list-columns.png){width="800" zoomable="yes"}

### Statut du parcours

Le statut d’un parcours peut changer en fonction des actions que vous appliquez. En fonction du statut d’un parcours, certaines actions peuvent être disponibles ou non dans l’en-tête.

| Statut | Description | Actions disponibles |
| ------ | ----------- | ----------------- |
| _&#x200B;**Brouillon**&#x200B;_ | Parcours dépublié modifiable. | <li>[Publier](./create-publish-journey.md#publish-a-journey)<li>[Dupliquer](#duplicate-journey) <li>[Supprimer](#delete-journey) |
| _&#x200B;**Actif**&#x200B;_ | Le statut du parcours passe de _Brouillon_ à _Actif_ lorsqu’un parcours est publié. Dans ce statut, il n’est plus modifiable. | <li>[Dupliquer](#duplicate-journey)<li>[Fermer aux nouvelles entrées](#close-to-new-entries) <li>[Abandonner](#abort-journey) |
| _&#x200B;**Fermé aux nouvelles entrées**&#x200B;_ | Le statut du parcours passe de _Actif_ à _Fermé aux nouvelles entrées_ lorsque vous cliquez sur [!UICONTROL Fermer aux nouvelles entrées] dans le volet de navigation supérieur. | <li>[Dupliquer](#duplicate-journey) <li>[Abandonner](#abort-journey) |
| _&#x200B;**Abandonné**&#x200B;_ | Le statut du parcours passe de _Actif_ ou _Fermé aux nouvelles entrées_ lorsque vous abandonnez un parcours. Vous ne pouvez pas redémarrer un parcours abandonné. | <li>[Dupliquer](#duplicate-journey) <li>[Supprimer](#delete-journey) |
| _&#x200B;**Terminé**&#x200B;_ | Lorsque tous les membres de l’audience de compte ou de personne d’un parcours ont terminé le parcours, le statut passe de _Actif_ ou _Fermé aux nouvelles entrées_ à _Terminé_. | <li>[Dupliquer](#duplicate-journey) <li>[Supprimer](#delete-journey) |

## Mappages de parcours

Cliquez sur le nom (affiché sous forme de lien) dans la liste parcours pour passer en revue les détails, apporter des modifications et prendre des mesures.

![Espace de travail du parcours de compte](./assets/account-journey-workspace.png){width="800" zoomable="yes"}

L’en-tête de chaque mappage de parcours comprend :

* Nom du parcours
* Outil de modification du nom du parcours (![icône Modifier](../assets/do-not-localize/icon-edit.svg) _Icône Modifier_)
* [Statut](#journey-status) du parcours

À partir du mappage de parcours, vous pouvez [Ajouter les nœuds](./create-publish-journey.md#add-a-node) et [définir le flux de parcours &#x200B;](./create-publish-journey.md#add-and-delete-a-path).

## Actions de parcours

La page de liste parcours comprend tous les parcours de compte ou de personne de votre instance Journey Optimizer B2B edition. La page de liste vous permet d’appliquer plusieurs actions à un parcours.

### Abandonner le parcours

Si vous abandonnez (arrêtez) un parcours actif ou planifié, les comptes ou les personnes du parcours arrêtent immédiatement leur progression et aucune autre entrée de parcours ne peut se produire. Vous ne pouvez pas redémarrer un parcours abandonné.

>[!IMPORTANT]
>
>Lorsque le parcours est utilisé dans un autre parcours à partir d’un nœud _Prendre une action_ avec l’action _[!UICONTROL Ajouter un compte à un (autre) Parcours]_, l’abandon du parcours bloque cette action dans ce parcours.

1. Cliquez sur le nom du parcours pour l’ouvrir.

1. Cliquez sur le menu **[!UICONTROL Plus...]** en haut à droite et choisissez **[!UICONTROL Abandonner]**.

   ![Clic sur Plus en haut à droite](./assets/account-journey-live-more-menu.png){width="450"}

1. Dans la boîte de dialogue de confirmation, cliquez sur **[!UICONTROL Abandonner]**.

### Fermer aux nouvelles entrées

Si vous fermez un parcours actif, les comptes actuellement dans le parcours continuent leur chemin et aucune autre entrée dans le parcours ne peut se produire. Vous ne pouvez pas redémarrer un parcours fermé. Vous pouvez dupliquer un parcours fermé.

>[!IMPORTANT]
>
>Lorsque le parcours est utilisé dans un autre parcours à partir d’un nœud _Prendre une action_ avec l’action _[!UICONTROL Ajouter un compte à un (autre) Parcours]_, le fait de le fermer à de nouvelles entrées bloque cette action de ce parcours.

1. Cliquez sur le nom du parcours pour l’ouvrir.

1. Cliquez sur le menu **[!UICONTROL Plus...]** en haut à droite et choisissez **[!UICONTROL Fermer aux nouvelles entrées]**.

1. Dans la boîte de dialogue de confirmation, cliquez sur **[!UICONTROL Fermer aux nouvelles entrées]**.

### Dupliquer un parcours

Une action de duplication est similaire à une fonction de clonage, mais le parcours dupliqué n’inclut aucune ressource de contenu de parcours créée. Vous pouvez dupliquer les détails du parcours ou simplement un _squelette_ de la structure du flux et du chemin d’accès.

>[!NOTE]
>
>Cette action n’est actuellement pas disponible pour les parcours de personne.

1. Cliquez sur l’icône _Plus_ (**...**) en regard du nom du parcours et choisissez **[!UICONTROL Dupliquer]**.

   ![Clic sur l’icône ... et sélection de Dupliquer](./assets/account-journeys-list-more-menu.png){width="450"}

   Selon le statut du parcours, vous pouvez également accéder à l’action en double à partir des détails du parcours ou de la carte des parcours :

   * Pour un brouillon de parcours, cliquez sur le menu **[!UICONTROL Plus...]** en haut à droite et choisissez **[!UICONTROL Dupliquer]**.

   * Pour tous les autres statuts de parcours, cliquez sur **[!UICONTROL Dupliquer]** en haut à droite.

     ![Clic sur Dupliquer en haut à droite](./assets/account-journey-duplicate-button.png){width="450"}

1. Dans la boîte de dialogue _Dupliquer le parcours_, définissez les **[!UICONTROL Nom]** et **[!UICONTROL Description]** du nouveau parcours.

   Par défaut, la boîte de dialogue utilise le nom du parcours dupliqué suivi de __copy_. Saisissez un autre nom unique pour le parcours, le cas échéant.

   ![Boîte de dialogue Dupliquer le parcours](./assets/account-journey-duplicate-dialog.png){width="400"}

1. Choisissez le **[!UICONTROL type]** de duplication :

   * **[!UICONTROL Duplication partielle du contenu]** : utilisez ce type pour copier tout le contenu du parcours, à l’exclusion des e-mails ou des SMS créés. Les nœuds qui font référence à un e-mail ou un SMS Marketo Engage sont entièrement intacts.

   * **[!UICONTROL Dupliquer sans détails]** : utilisez ce type pour copier uniquement la structure de nœuds et les chemins d’accès. Les paramètres de nœud et conditions de chemin ne sont pas définis (par défaut). Vous pouvez donc réutiliser le flux de base avec différents paramètres d’audience, d’actions et de segmentation de chemin. Tous les nœuds d’_attente_ utilisent la valeur par défaut de cinq jours.

1. Cliquez sur **[!UICONTROL Dupliquer]**.

   Le parcours dupliqué s’ouvre dans la carte des parcours, où vous pouvez définir les détails et créer du contenu de parcours selon vos besoins.

### Supprimer un parcours

Utilisez une action de suppression pour supprimer définitivement un parcours. Vous ne pouvez pas supprimer un parcours actif ou planifié.

1. Cliquez sur l’icône _Plus_ (**...**) en regard du nom du parcours et choisissez **[!UICONTROL Supprimer]**.

   Selon le statut du parcours, vous pouvez également accéder à l’action de suppression à partir des détails du parcours ou de la carte des parcours :

   * Pour un brouillon de parcours, cliquez sur le menu **[!UICONTROL Plus...]** en haut à droite et choisissez **[!UICONTROL Supprimer]**.

   * Pour d’autres statuts de parcours, tels que _Terminé_ ou _Abandonné_, cliquez sur **[!UICONTROL Supprimer]** en haut à droite.

1. Dans la boîte de dialogue de confirmation, cliquez sur **[!UICONTROL Supprimer]**.

## Vérifier la progression du compte

Pour un parcours de compte publié dont le statut est défini sur _En ligne_, _Fermé aux nouvelles entrées_, _Abandonné_ ou _Terminé_, vous pouvez ouvrir le mappage de parcours pour consulter la progression du compte pour les nœuds de parcours. Chaque nœud de la carte affiche le nombre de comptes à atteindre ce nœud et, pour les parcours actifs, le nombre de comptes actuellement sur ce nœud.

![Informations sur la progression du compte pour les nœuds de parcours &#x200B;](./assets/node-account-progression-observability.png){width="400"}

Lorsque vous sélectionnez le nœud, cliquez sur le numéro pour afficher la liste des comptes qui y sont entrés ou qui se trouvent actuellement à cette étape du parcours.

![Informations sur la progression du compte pour les nœuds de parcours](./assets/node-accounts-entered-list.png){width="700" zoomable="yes"}

## Vidéo de présentation du parcours de compte {#overview-video}

>[!VIDEO](https://video.tv.adobe.com/v/3443202/?learn=on)
