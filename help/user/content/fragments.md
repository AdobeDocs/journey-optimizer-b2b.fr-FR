---
title: Fragments
description: Découvrez comment créer et utiliser des fragments de contenu visuels en tant que composants réutilisables pour les e-mails et les modèles de courrier électronique dans Adobe Journey Optimizer B2B edition.
feature: Content, Email Authoring
exl-id: 3c1d2ca0-d009-4a2a-9d81-1a838845b7fa
source-git-commit: bf57c152e758a757279f7666423f6a6ca61e1092
workflow-type: tm+mt
source-wordcount: '2624'
ht-degree: 3%

---

# Fragments

Un fragment est un composant réutilisable pouvant être référencé dans un ou plusieurs e-mails et modèles d’e-mail dans Adobe Journey Optimizer B2B edition. Il s’agit généralement d’un bloc de contenu (texte, image ou les deux) qui peut être précréé et rapidement inséré dans un e-mail ou un modèle d’e-mail. Grâce à cette fonctionnalité, vous pouvez précréer plusieurs blocs de contenu personnalisés à utiliser par les membres de votre équipe marketing pour assembler les contenus d’e-mail afin d’améliorer le processus de conception. Les cas d’utilisation courants incluent les blocs de contenu d’en-tête/de pied de page pour les e-mails, les bannières d’invitation et les salutations saisonnières.

>[!BEGINSHADEBOX]

**Fragments visuels**

Les fragments visuels sont des blocs visuels prédéfinis créés à l’aide du concepteur de contenu visuel que vous pouvez réutiliser dans plusieurs e-mails ou modèles d’e-mail. Le périmètre actuel de Journey Optimizer B2B edition et de cette documentation est celui des fragments visuels uniquement. Les fragments basés sur une expression ne sont pas encore pris en charge dans Journey Optimizer B2B edition.

>[!ENDSHADEBOX]

Pour tirer le meilleur parti des fragments dans vos workflows :

* _Créer vos propres fragments_ - Créez des fragments visuels, en partant de zéro ou en enregistrant du contenu en tant que fragment à partir de l’éditeur de contenu visuel.
* _Réutiliser des fragments_ - Utilisez-les autant de fois que nécessaire dans votre contenu.

## Accéder aux fragments et les gérer

Pour accéder aux fragments visuels dans Adobe Journey Optimizer B2B edition, accédez au volet de navigation de gauche et cliquez sur **[!UICONTROL Gestion de contenu]** > **[!UICONTROL Fragments]**. Cette action ouvre une page de liste répertoriant tous les fragments créés dans l’instance, répertoriés dans un tableau.

![Accéder à la bibliothèque de fragments](./assets/fragments-list.png){width="700" zoomable="yes"}

Le tableau est trié selon la colonne _[!UICONTROL Modifié]_, les fragments les plus récemment mis à jour étant en haut par défaut. Cliquez sur le titre de la colonne pour passer d’un ordre croissant à un ordre décroissant.

### Statut et cycle de vie du fragment

Le statut du fragment détermine sa disponibilité pour une utilisation dans un e-mail ou un modèle d’e-mail, ainsi que les modifications que vous pouvez y apporter.

| Statut | Description |
| -------------------- | ----------- |
| Brouillon | Lorsque vous créez un fragment, il est à l’état de brouillon. Il reste dans ce statut lorsque vous définissez ou modifiez le contenu visuel jusqu’à ce que vous le publiiez pour l’utiliser dans un e-mail ou un modèle d’e-mail. Actions disponibles :<br/><ul><li>Modifier tous les détails<li>Modifier dans le concepteur visuel<li>Publier<li>Dupliquer<li>Supprimer |
| Publié | Lorsque vous publiez un fragment, il peut être utilisé dans un e-mail ou un modèle d’e-mail. Le contenu du fragment publié ne peut pas être modifié dans le concepteur visuel. Actions disponibles :<br/><ul><li>Modifier la description<li>Ajouter à un e-mail ou un modèle<li>Créer une version brouillon<li>Dupliquer<li>Supprimer (si non utilisé) |
| Publié avec le brouillon | Lorsque vous créez un brouillon à partir d’un fragment publié, la version publiée reste disponible pour une utilisation dans un e-mail ou un modèle d’e-mail, et le contenu du brouillon peut être modifié dans le concepteur visuel. Si vous publiez le brouillon, il remplace la version publiée actuelle et le contenu est mis à jour dans les e-mails et les modèles d’e-mail où il est utilisé. Actions disponibles :<br/><ul><li>Modifier la description<li>Ajouter à un e-mail ou un modèle<li>Modifier le brouillon dans le concepteur visuel<li>Publier le brouillon<li>Dupliquer<li>Supprimer (si non utilisé) |

![ Cycle de vie du statut du fragment ](./assets/status-lifecycle-diagram.png){zoomable="yes"}

>[!IMPORTANT]
>
>Le statut du fragment a été introduit dans la version d’août de Journey Optimizer B2B edition. Tous les fragments créés avant cette version ont le statut _Brouillon_, même s’ils sont utilisés dans un e-mail ou un modèle. Si vous apportez des modifications à ces fragments, vous devez publier le fragment pour propager les modifications.

### Filtrer la liste des fragments

Pour rechercher un fragment par nom, saisissez une chaîne de texte dans la barre de recherche pour rechercher une correspondance. Cliquez sur l’icône _Filtrer_ ( ![Afficher ou masquer l’icône des filtres](../assets/do-not-localize/icon-filter.svg) ) pour afficher les options de filtre disponibles et modifier les paramètres afin de filtrer les éléments affichés en fonction de vos critères spécifiés.

![Filtrer les fragments affichés](./assets/fragments-list-filtered.png){width="700" zoomable="yes"}

### Personnalisation de l’affichage des colonnes

Personnalisez les colonnes à afficher dans le tableau en cliquant sur l’icône _Personnaliser le tableau_ ( ![Icône Personnaliser le tableau](../assets/do-not-localize/icon-column-settings.svg) ) en haut à droite.

Dans la boîte de dialogue, sélectionnez les colonnes à afficher et cliquez sur **[!UICONTROL Appliquer]**.

![Sélectionnez les colonnes à afficher](./assets/fragments-customize-table-dialog.png){width="300"}

## Créer des fragments

Vous pouvez créer des fragments visuels dans Journey Optimizer B2B edition en cliquant sur **[!UICONTROL Créer un fragment]** en haut à droite.

1. Dans la boîte de dialogue _[!UICONTROL Créer un fragment]_, saisissez un **[!UICONTROL Nom]** et un **[!UICONTROL Description]** utiles (facultatif).

   Exigences de fragment :

   * Nom : 100 caractères maximum, doit être unique et ne pas respecter la casse.

   * Description - 300 caractères maximum

   * Les caractères Alpha, numériques et spéciaux sont autorisés

   * Les caractères réservés ne sont **_pas autorisés_** : `\ / : * ? " < > |`

   ![ Boîte de dialogue Créer un fragment ](./assets/assets-fragments-create-dialog.png){width="400"}

1. Cliquez sur **[!UICONTROL Créer]**.

   Le concepteur visuel s’ouvre avec une zone de travail vide.

1. Utilisez les outils de conception de contenu pour créer le contenu du fragment visuel :

   * [Ajouter la structure et le contenu](./fragment-authoring.md#add-structure-and-content)
   * [Ajout d’Assets](./fragment-authoring.md#add-assets)
   * [Parcourir les calques, paramètres et styles](./fragment-authoring.md#navigate-the-layers-settings-and-styles)
   * [Personnaliser le contenu](./fragment-authoring.md#personalize-content)
   * [Activer les champs personnalisés](./fragment-authoring.md#enable-fragment-customization)
   * [Modifier le tracking des URL liées](./fragment-authoring.md#edit-linked-url-tracking)

1. Cliquez sur **[!UICONTROL Enregistrer]** à tout moment pour enregistrer le brouillon de fragment.

1. Lorsque vous êtes prêt à rendre le fragment disponible pour une utilisation dans un e-mail ou un modèle d’e-mail, cliquez sur **[!UICONTROL Publier]**.

## Affichage des détails du fragment

Cliquez sur le nom d’un fragment de la page de liste pour ouvrir la page des détails du fragment. Vous pouvez choisir de modifier le fragment, de le renommer ou de mettre à jour sa description. Effectuez des mises à jour et cliquez en dehors du champ de nom ou de description pour enregistrer automatiquement les modifications.

>[!NOTE]
>
>Si un fragment publié est utilisé par un e-mail ou un modèle d’e-mail, vous ne pouvez pas modifier le nom ni le contenu. Vous pouvez créer un brouillon si vous souhaitez apporter des modifications au fragment.

![Affichage des détails d’un fragment publié](./assets/fragment-details-published.png){width="600" zoomable="yes"}

Cliquez sur **[!UICONTROL Modifier le fragment]** pour ouvrir le fragment dans l’éditeur de contenu visuel.

Quittez la vue à tout moment en cliquant sur la flèche _Précédent_ en haut à gauche, qui vous renvoie à la page de liste _Fragments_.

## Afficher les références du fragment utilisé par

Dans la page des détails du fragment, cliquez sur l’onglet **[!UICONTROL Utilisé par]** pour afficher des détails sur l’emplacement où le fragment est actuellement utilisé dans Journey Optimizer B2B edition, dans les e-mails, les modèles d’e-mail et les fragments.

>[!IMPORTANT]
>
>Un fragment actuellement utilisé par un e-mail ou un modèle d’e-mail ne peut pas être supprimé.

Les références sont affichées selon la catégorie : _E-mail_ ou _Modèle d’e-mail_. Les e-mails dans Journey Optimizer B2B edition sont incorporés et créés dans des parcours de compte. De ce fait, le parcours parent de l’e-mail qui utilise le fragment est affiché dans les références.

![Utilisé par les références pour le fragment](./assets/fragment-used-by-published.png){width="600" zoomable="yes"}

Cliquez sur le lien pour ouvrir l’e-mail ou le modèle d’e-mail correspondant où le fragment est utilisé.

## Suppression de fragments

Un fragment actuellement utilisé par un e-mail ou un modèle d’e-mail ne peut pas être supprimé. Assurez-vous donc de vérifier les références _utilisé par_ avant de procéder à la suppression d’un fragment. En outre, une suppression ne peut pas être annulée. Vérifiez-la avant de lancer une action de suppression.

Vous pouvez supprimer un fragment à l’aide de l’une des méthodes suivantes :

* Dans les détails du fragment sur la droite, cliquez sur **[!UICONTROL Supprimer]**.
* Dans la page de liste _[!UICONTROL Fragments]_, cliquez sur les points de suspension en regard du fragment et choisissez **[!UICONTROL Supprimer]**.

Cette action ouvre une boîte de dialogue de confirmation. Vous pouvez abandonner le processus en cliquant sur **[!UICONTROL Annuler]** ou sur **[!UICONTROL Supprimer]** pour confirmer la suppression.

![Boîte de dialogue Supprimer le fragment](./assets/fragment-delete-dialog.png){width="400"}

Si le fragment est en cours d’utilisation, l’action ouvre une boîte de dialogue d’information qui vous avertit qu’il ne peut pas être supprimé. Cliquez sur **[!UICONTROL OK]** pour annuler la suppression.

![Boîte de dialogue Supprimer le fragment - impossible de supprimer le fragment en cours d’utilisation](./assets/fragment-delete-dialog-in-use.png){width="400"}

## Modifier des fragments

Les modifications apportées à un fragment dépendent de son statut actuel :

* Lorsqu’un fragment a le statut _Brouillon_, vous pouvez modifier n’importe lequel de ses détails et le contenu visuel.
* Lorsqu’un fragment a le statut _Publié_, vous pouvez modifier sa description, mais pas son nom. Vous ne pouvez pas modifier le contenu visuel.
* Lorsqu’un fragment possède le statut _Publié avec brouillon_, la modification des détails se limite à la description. Vous pouvez également modifier le contenu visuel de la version brouillon.

>[!BEGINTABS]

>[!TAB Brouillon]

1. Dans la page de liste _[!UICONTROL Fragments]_, cliquez sur le nom du fragment pour l’ouvrir.

   Un aperçu du contenu visuel s’affiche avec les détails du fragment sur la droite.

1. Modifiez l’un des détails, tels que le nom et la description.

   ![Détails du fragment avec le statut Brouillon ](./assets/fragment-draft-details.png){width="600" zoomable="yes"}

1. Pour modifier le contenu dans le concepteur visuel, cliquez sur **[!UICONTROL Modifier le fragment]**.

   Utilisez les outils du concepteur visuel selon vos besoins :

   * [Ajouter la structure et le contenu](./fragment-authoring.md#add-structure-and-content)
   * [Ajout d’Assets](./fragment-authoring.md#add-assets)
   * [Parcourir les calques, paramètres et styles](./fragment-authoring.md#navigate-the-layers-settings-and-styles)
   * [Personnaliser le contenu](./fragment-authoring.md#personalize-content)
   * [Activer les champs personnalisés](./fragment-authoring.md#enable-fragment-customization)
   * [Modifier le tracking des URL liées](./fragment-authoring.md#edit-linked-url-tracking)

   Cliquez sur **[!UICONTROL Enregistrer]** ou **[!UICONTROL Enregistrer et fermer]** pour revenir aux détails du fragment.

1. Lorsque le fragment répond à vos critères et que vous souhaitez le rendre disponible pour une utilisation dans un e-mail ou un modèle d’e-mail, cliquez sur **[!UICONTROL Publier]**.

>[!TAB Publié]

1. Dans la page de liste _[!UICONTROL Fragments]_, cliquez sur le nom du fragment pour l’ouvrir.

   Un aperçu du contenu visuel s’affiche avec les détails du fragment sur la droite.

1. Modifiez la description, si nécessaire.

   Pour un fragment publié, tous les autres détails ne peuvent pas être modifiés.

1. Si vous souhaitez mettre à jour le contenu, cliquez sur **[!UICONTROL Créer un brouillon]** en haut à droite.

   Cliquez sur **[!UICONTROL OK]** dans la boîte de dialogue pour ouvrir le brouillon dans le concepteur visuel.

   ![Boîte de dialogue Créer un brouillon](./assets/fragments-create-draft-version.png){width="300"}

   Utilisez les outils du concepteur visuel selon vos besoins :

   * [Ajouter la structure et le contenu](./fragment-authoring.md#add-structure-and-content)
   * [Ajout d’Assets](./fragment-authoring.md#add-assets)
   * [Parcourir les calques, paramètres et styles](./fragment-authoring.md#navigate-the-layers-settings-and-styles)
   * [Personnaliser le contenu](./fragment-authoring.md#personalize-content)
   * [Activer les champs personnalisés](./fragment-authoring.md#enable-fragment-customization)
   * [Modifier le tracking des URL liées](./fragment-authoring.md#edit-linked-url-tracking)

   Cliquez sur **[!UICONTROL Enregistrer]** ou **[!UICONTROL Enregistrer et fermer]** pour revenir aux détails du fragment.

1. Lorsque le brouillon répond à vos critères et que vous souhaitez rendre les modifications disponibles pour une utilisation dans un modèle d’e-mail ou de courrier électronique, cliquez sur **[!UICONTROL Publier]**.

   Lorsque vous publiez le brouillon, il remplace la version publiée actuelle et le contenu est mis à jour dans les e-mails et les modèles d’e-mail où il est déjà utilisé.

>[!TAB Publié avec le brouillon]

Vous pouvez ouvrir le brouillon pour le modifier de deux manières différentes à partir de la page de liste _[!UICONTROL Fragments]_ :

* Cliquez sur l’icône _Plus_ (**...**) en regard du nom du fragment et choisissez **[!UICONTROL Ouvrir le brouillon]**.

  ![Ouvrir le brouillon](./assets/fragments-create-draft-version.png){width="300"}

* Cliquez sur le nom du fragment pour l’ouvrir. Cliquez ensuite sur **[!UICONTROL Ouvrir le brouillon]** en haut à droite.

  Un aperçu du contenu visuel du brouillon s’affiche avec les détails du fragment à droite.

Pour mettre à jour le contenu :

1. Cliquez sur **[!UICONTROL Modifier le fragment]** en haut à droite. Utilisez les outils du concepteur visuel selon vos besoins :

   * [Ajouter la structure et le contenu](./fragment-authoring.md#add-structure-and-content)
   * [Ajout d’Assets](./fragment-authoring.md#add-assets)
   * [Parcourir les calques, paramètres et styles](./fragment-authoring.md#navigate-the-layers-settings-and-styles)
   * [Personnaliser le contenu](./fragment-authoring.md#personalize-content)
   * [Activer les champs personnalisés](./fragment-authoring.md#enable-fragment-customization)
   * [Modifier le tracking des URL liées](./fragment-authoring.md#edit-linked-url-tracking)

   Cliquez sur **[!UICONTROL Enregistrer]** ou **[!UICONTROL Enregistrer et fermer]** pour revenir aux détails du fragment.

1. Lorsque le brouillon répond à vos critères et que vous souhaitez rendre les modifications disponibles pour une utilisation dans un modèle d’e-mail ou de courrier électronique, cliquez sur **[!UICONTROL Publier]**.

   Lorsque vous publiez le brouillon, il remplace la version publiée actuelle et le contenu est mis à jour dans les e-mails et les modèles d’e-mail où il est déjà utilisé.

>[!ENDTABS]

## Fragments dupliqués

Vous pouvez dupliquer un fragment à l’aide de l’une des méthodes suivantes :

* Dans la page de liste _[!UICONTROL Fragments]_, cliquez sur l’icône _Plus_ (**...**) à côté du nom du fragment et sélectionnez **[!UICONTROL Dupliquer]**.
* En haut à droite de la page des détails du fragment, cliquez sur **[!UICONTROL ... En plus]** et choisissez **[!UICONTROL Dupliquer]**.

![Dupliquer le fragment](./assets/fragment-details-duplicate.png){width="600" zoomable="yes"}

Dans la boîte de dialogue, saisissez un nom utile (unique) et une description. Cliquez sur **[!UICONTROL Dupliquer]** pour terminer l’action.

![Saisissez un nom et une description pour le fragment dupliqué](./assets/fragment-duplicate-dialog.png){width="400"}

Le fragment (nouveau) dupliqué apparaît ensuite dans la liste _Fragments_.

## Enregistrer un nouveau fragment d’un e-mail ou du contenu de modèle

Lorsque vous créez/modifiez un e-mail ou un modèle d’e-mail dans l’éditeur visuel de contenu, vous pouvez choisir d’enregistrer tout ou partie du contenu en tant que fragment afin de le réutiliser.

1. Lorsque vous souhaitez enregistrer du contenu sous forme de fragment, cliquez sur **[!UICONTROL Plus]** et choisissez **[!UICONTROL Enregistrer sous forme de fragment]**.

1. Sélectionnez les différents éléments à inclure dans le fragment.

   Sélectionnez plusieurs structures en maintenant le bouton Maj ou Ctrl enfoncé.

   Vous pouvez uniquement sélectionner des structures adjacentes les unes aux autres et l&#39;interface ne vous permet pas de sélectionner des éléments non adjacents.

1. Une fois le contenu sélectionné, cliquez sur **[!UICONTROL Créer]** en haut à droite.

1. Dans la boîte de dialogue, saisissez un nom et une description utiles pour le fragment. Cliquez ensuite sur **[!UICONTROL Créer]**.

   Le nouveau fragment est ensuite affiché dans la page de liste _Fragments_ et peut également être utilisé dans les e-mails et les modèles d’e-mail.

## Ajouter des fragments visuels au contenu de votre e-mail ou modèle

Les fragments sont conçus pour être réutilisés et peuvent être insérés pour la création de modèles d’e-mail et d’e-mail. Vous pouvez ajouter jusqu’à 30 fragments dans un e-mail ou un modèle. Les fragments peuvent être imbriqués jusqu’à un seul niveau.

>[!BEGINTABS]

>[!TAB Ajouter des fragments à un email]

1. Accédez à **[!UICONTROL Parcours de compte]** et ouvrez un parcours parcours existant ou créez-en un.

1. Créez un nœud [_[!UICONTROL Envoyer un e-mail ]_](./add-email.md#add-an-email-action-node-in-a-journey).

1. Créez ou modifiez le [contenu d’e-mail pour le nœud](./email-authoring.md).

1. Faites glisser et déposez un élément du menu **[!UICONTROL Composants]** pour fournir une _structure_ pour le fragment.

1. Pour ouvrir la liste des fragments publiés, cliquez sur l’icône _Fragments_.

   Vous pouvez effectuer les actions suivantes :
   * Triez la liste.
   * Parcourez, recherchez et filtrez la liste.
   * Basculez entre les vues Carte (miniature) et Liste.
   * Actualisez la liste pour refléter l’un des fragments récemment créés.

   ![Rechercher un fragment dans le concepteur visuel](./assets/fragments-list-designer-search.png){width="600"}

1. Faites glisser et déposez l’un des fragments dans l’espace réservé du composant de structure.

   L’éditeur effectue le rendu du fragment dans la section/l’élément de la structure de l’e-mail.

Le contenu du fragment est mis à jour dynamiquement dans la structure pour rendre un visuel de la manière dont le contenu apparaît dans l’e-mail.

>[!TIP]
>
>Si vous souhaitez que le fragment occupe toute la disposition horizontale dans l’e-mail, ajoutez une structure de colonne [!UICONTROL 1:1] puis faites-y glisser le fragment et déposez-le.

Une fois l’e-mail enregistré, il apparaît dans la page des détails du fragment lorsque l’onglet _[!UICONTROL Utilisé par]_ est sélectionné. Les fragments ajoutés à un e-mail ne sont pas modifiables dans l’e-mail ou le modèle : le fragment source publié définit le contenu.

>[!TAB Ajouter des fragments à un modèle d’e-mail]

1. Dans le volet de navigation de gauche, cliquez sur **[!UICONTROL Gestion de contenu]** > **[!UICONTROL Modèles]**.

1. Créez un modèle ou ouvrez un modèle d’e-mail existant, puis cliquez sur **[!UICONTROL Modifier le modèle d’e-mail]**.

1. Faites glisser et déposez un élément du menu **[!UICONTROL Composants]** pour fournir une _structure_ pour le fragment.

1. Pour ouvrir la liste des fragments, cliquez sur l’icône _Fragments_.

   Vous pouvez effectuer les actions suivantes :
   * Triez la liste.
   * Parcourez, recherchez et filtrez la liste.
   * Basculez entre les vues Carte (miniature) et Liste.
   * Actualisez la liste pour refléter l’un des fragments récemment créés.

   ![Rechercher un fragment dans le concepteur visuel](./assets/fragments-list-designer-search.png){width="600"}

1. Faites glisser et déposez l’un des fragments dans l’espace réservé du composant de structure.

   L’éditeur effectue le rendu du fragment dans la section/l’élément de la structure du modèle d’e-mail.

1. Faites glisser et déposez l’un des fragments dans l’espace réservé du composant de structure.

   L’éditeur effectue le rendu du fragment dans la section/l’élément de la structure du modèle d’e-mail.

>[!TIP]
>
>Si vous souhaitez que le fragment occupe toute la disposition horizontale dans le modèle d’e-mail, ajoutez une structure de colonne _[!UICONTROL 1:1]_ puis faites-y glisser le fragment et déposez-le.

Une fois le modèle d’e-mail enregistré, il apparaît dans la page des détails du fragment lorsque l’onglet _[!UICONTROL Utilisé par]_ est sélectionné. Les fragments ajoutés à un modèle d’e-mail ne sont pas modifiables dans le modèle : le fragment source publié définit le contenu.

>[!ENDTABS]

## Actions sur les fragments lors de la création d’e-mails et de modèles

Lorsqu’un fragment est ajouté à un e-mail ou à un modèle d’e-mail, le contenu du fragment ne peut pas être modifié dans l’e-mail ou le modèle. Vous pouvez toutefois appliquer les actions suivantes :

* **[!UICONTROL Supprimer]** - Cette action supprime le fragment du contenu de l’e-mail ou du modèle d’e-mail actuel (la source du fragment n’est pas affectée).
* **[!UICONTROL Actualiser]** - Cette action actualise le contenu du fragment dans l’e-mail ou le modèle d’e-mail actuel. L’actualisation est utile lorsque vous souhaitez refléter des modifications récentes apportées au fragment après l’ajout à l’e-mail ou au modèle d’e-mail.
* **[!UICONTROL Dupliquer]** - Cette action duplique le fragment dans le même e-mail ou modèle d’e-mail dans l’éditeur, avec les mêmes dimensions et ajouté juste en dessous.
* **[!UICONTROL Ouvrir le fragment]** - Cette action ouvre un nouvel onglet du navigateur avec la page de l’éditeur de fragments et les détails.
* **[!UICONTROL Rompre l’héritage]** - Cette action rompt l’héritage du fragment (et de ses modifications) de la source. Utilisez cette action pour rendre le contenu du fragment disponible en tant que contenu indépendant et modifiable dans l’e-mail ou le modèle d’e-mail. Cette action supprime également l’e-mail ou le modèle d’e-mail de la référence _Utilisé par_ pour le fragment d’origine.

Lorsque vous sélectionnez le fragment sur la page de l’éditeur, ces actions sont disponibles dans la barre d’outils contextuelle et le panneau des propriétés à droite.

![Appliquer des actions au fragment sélectionné](./assets/fragment-actions-email-authoring.png){width="600" zoomable="yes"}
