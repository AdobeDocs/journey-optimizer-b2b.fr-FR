---
title: Fragments
description: Découvrez comment créer et utiliser des fragments de contenu visuel comme composants réutilisables pour les emails et les modèles d’email dans Adobe Journey Optimizer B2B Edition.
feature: Content, Email Authoring
source-git-commit: dcd8ab2820d60654e8970944054142fc296ed54f
workflow-type: tm+mt
source-wordcount: '1701'
ht-degree: 0%

---

# Fragments

Un fragment est un composant réutilisable pouvant être référencé dans un ou plusieurs emails et modèles d’email dans Adobe Journey Optimizer B2B Edition. Il s’agit généralement d’un bloc de contenu (texte, image ou les deux) qui peut être précréé et inséré rapidement dans un email ou un modèle d’email. Grâce à cette fonctionnalité, vous pouvez précréer plusieurs blocs de contenu personnalisés qui peuvent être utilisés par les membres de votre équipe marketing pour assembler les contenus d’email afin d’améliorer le processus de conception. Les cas d’utilisation courants incluent les blocs de contenu d’en-tête/de pied de page pour le courrier électronique, les bannières d’invitation à un événement et les salutations saisonnières.

Pour optimiser l’utilisation des fragments dans vos workflows :

* _Créez vos propres fragments_ - Créez des fragments visuels, à partir de zéro ou en enregistrant du contenu en tant que fragment à tout moment à partir de l’éditeur de contenu visuel.
* _Réutiliser vos fragments_s : utilisez-les autant de fois que nécessaire dans votre contenu.

## Fragments visuels

Les fragments visuels sont des blocs visuels prédéfinis créés à l’aide de l’éditeur de contenu visuel que vous pouvez réutiliser dans plusieurs emails ou modèles d’email. La portée actuelle de l’édition B2B de Journey Optimizer et de cette documentation sont celles des fragments visuels uniquement. Les fragments basés sur des expressions ne sont pas encore pris en charge dans Journey Optimizer B2B Edition.

## Accès et gestion des fragments

Pour accéder aux fragments visuels dans l’édition B2B de Adobe Journey Optimizer, accédez au volet de navigation de gauche et cliquez sur **[!UICONTROL Gestion de contenu]** > **[!UICONTROL Fragments]**. Cette action ouvre une page de liste avec tous les fragments créés dans l’instance répertoriés dans un tableau.

![Accès à la bibliothèque de fragments](./assets/fragments-list.png){width="700" zoomable="yes"}

Le tableau est trié par colonne _[!UICONTROL Modifié]_, les fragments mis à jour le plus récemment se trouvant en haut de la liste par défaut. Cliquez sur le titre de la colonne pour passer d’un titre croissant à un titre décroissant.

Recherchez un fragment en saisissant une chaîne de texte dans la barre de recherche pour rechercher une correspondance par nom de fragment. Cliquez sur l’icône _Filtrer_ pour filtrer les éléments affichés en fonction des critères que vous avez spécifiés.

![Filtrer les fragments affichés](./assets/fragments-list-filtered.png){width="700" zoomable="yes"}

Personnalisez les colonnes que vous souhaitez afficher dans le tableau en cliquant sur l’icône _Personnaliser le tableau_ en haut à droite. Sélectionnez les colonnes à afficher et cliquez sur **[!UICONTROL Appliquer]**.

## Créer des fragments

Vous pouvez créer des fragments visuels dans Journey Optimizer B2B Edition en cliquant sur **[!UICONTROL Créer un fragment]** en haut à droite.

1. Dans la boîte de dialogue _[!UICONTROL Créer un fragment]_, saisissez un **[!UICONTROL nom]** et une **[!UICONTROL description]** (facultatif).

   Exigences en matière de fragment :

   * Nom : 100 caractères maximum doivent être uniques et ne pas respecter la casse.

   * Description : 300 caractères maximum

   * Les caractères Alpha, numériques et spéciaux sont autorisés

   * Les caractères réservés ne sont pas autorisés : `\ / : * ? " < > |`

   ![Boîte de dialogue Créer un fragment](./assets/assets-fragments-create-dialog.png){width="500"}

1. Cliquez sur **[!UICONTROL Créer]**.

   L’éditeur de contenu visuel s’ouvre avec une zone de travail vide. Pour créer un fragment à l’aide de l’éditeur de contenu visuel, reportez-vous aux rubriques de création de contenu :

<!-- To be linked to the corresponding sections on this page: Adobe Journey Optimizer B2B Edition - Email Templates

Adding structure & content
Adding assets
Navigating the layers
Previewing & editing URLs
View options
More options -->

## Affichage des détails d’un fragment

Cliquez sur le nom d’un fragment dans la page de liste pour ouvrir la page de détails du fragment.

À partir de là, vous pouvez modifier le fragment, le renommer ou mettre à jour la description du fragment (effectuez des mises à jour et cliquez en dehors de la zone nom/description pour enregistrer automatiquement les modifications).

Cliquez sur **[!UICONTROL Modifier]** pour ouvrir le fragment dans l’éditeur de contenu visuel.

Quittez la vue à tout moment en cliquant sur la flèche _Précédent_ en haut à gauche, ce qui vous renvoie à la page de liste _Fragments_.

## Affichage des références utilisées par le fragment

Dans la page des détails du fragment, cliquez sur l’onglet **[!UICONTROL Utilisé par]** pour afficher les détails de l’emplacement actuel du fragment dans Journey Optimizer B2B Edition, dans les emails, les modèles d’email et les fragments.

>[!IMPORTANT]
>
>Un fragment qui est actuellement utilisé par un email ou un modèle de courrier électronique ne peut pas être supprimé.

Les références s’affichent en fonction de la catégorie : _Email_ ou _Modèle de courrier électronique_. Les emails de Journey Optimizer B2B Edition sont incorporés et créés dans des parcours de compte. Par conséquent, le parcours parent de l’email qui utilise le fragment s’affiche dans les références.

Cliquez sur le lien pour ouvrir l’email ou le modèle d’email correspondant dans lequel le fragment est utilisé.

## Suppression de fragments

Un fragment qui est actuellement utilisé par un courrier électronique ou un modèle de courrier électronique ne peut pas être supprimé. Vérifiez donc les références _used-by_ avant de lancer la suppression d’un fragment. En outre, une suppression ne peut pas être annulée. Vérifiez donc avant de lancer une action de suppression.

Vous pouvez supprimer un fragment en utilisant l’une des méthodes suivantes :

* Dans les détails du fragment sur la droite, cliquez sur **[!UICONTROL Supprimer]**.
* Sur la page de liste _[!UICONTROL Fragments]_, cliquez sur les points de suspension en regard du fragment et choisissez **[!UICONTROL Supprimer]**.

Cette action ouvre une boîte de dialogue de confirmation. Vous pouvez interrompre le processus en cliquant sur **[!UICONTROL Annuler]** ou sur **[!UICONTROL Supprimer]** pour confirmer la suppression.

Si le fragment est en cours d’utilisation, l’action ouvre une boîte de dialogue d’information vous avertissant qu’il ne peut pas être supprimé. Cliquez sur **[!UICONTROL OK]** pour abandonner la suppression.

## Modifier des fragments

Vous pouvez modifier un fragment à l’aide de l’une des méthodes suivantes :

* Dans les détails du fragment sur la droite, cliquez sur **[!UICONTROL Modifier]**.
* Sur la page de liste _[!UICONTROL Fragments]_, cliquez sur les points de suspension en regard du fragment et choisissez **[!UICONTROL Modifier]**.

Cette action ouvre le fragment dans un éditeur de contenu visuel, où vous pouvez modifier le fragment à l’aide de l’une des fonctionnalités de [création d’un fragment](#create-fragments).

## Dupliquer des fragments

Vous pouvez dupliquer un fragment à l’aide de l’une des méthodes suivantes :

* Dans les détails du fragment sur la droite, cliquez sur **[!UICONTROL Dupliquer]**.
* Sur la page de liste _[!UICONTROL Fragments]_, cliquez sur les points de suspension en regard du fragment et sélectionnez **[!UICONTROL Dupliquer]**.

Dans la boîte de dialogue, saisissez un nom (unique) et une description utiles. Cliquez sur **[!UICONTROL Dupliquer]** pour terminer l’action.

Le fragment dupliqué (nouveau) apparaît ensuite dans la liste _Fragments_.

## Enregistrer un fragment dans l’éditeur de courrier électronique ou de modèle

Chaque fois que vous vous trouvez dans l’éditeur visuel de contenu pour créer/modifier un email ou un modèle d’email, vous pouvez choisir d’enregistrer tout ou partie du contenu en tant que fragment afin qu’il soit disponible pour réutilisation.

1. Lorsque vous souhaitez enregistrer du contenu en tant que fragment, cliquez sur **[!UICONTROL Plus]** et choisissez **[!UICONTROL Enregistrer en tant que fragment]**.

1. Sélectionnez les différents éléments à inclure dans le fragment.

   Sélectionner plusieurs structures en maintenant le bouton Ctrl enfoncé

   Vous ne pouvez sélectionner que les structures adjacentes ; l’interface ne permet pas de sélectionner des éléments non adjacents.

1. Une fois le contenu sélectionné, cliquez sur **[!UICONTROL Créer]** en haut à droite.

1. Dans la boîte de dialogue, saisissez un nom et une description utiles pour le fragment. Cliquez ensuite sur **[!UICONTROL Créer]**.

   Le nouveau fragment est ensuite affiché dans la page de liste _Fragments_ et peut également être utilisé dans les emails et les modèles de courrier électronique.

## Ajout de fragments visuels à un email ou à un modèle

Les fragments sont conçus pour être réutilisés et peuvent être insérés pour la création de modèles d’email et d’email. Vous pouvez ajouter jusqu’à 30 fragments dans un email ou un modèle donné. Les fragments ne peuvent être imbriqués qu’à un seul niveau.

>[!BEGINTABS]

>[!TAB Ajouter des fragments à un email]

1. Accédez à Parcours de compte et ouvrez un parcours existant ou créez un parcours.

1. Créez un noeud &quot;Agir sur une action > Action Personnes > Envoyer un courrier électronique&quot;.

1. Créez ou modifiez le contenu d’un email pour le noeud.

1. Faites glisser et déposez un élément du menu Composants pour fournir une _structure_ pour le fragment.

1. Pour ouvrir la liste des fragments, cliquez sur l’icône _Fragments_ .

   Vous pouvez :
   * Triez la liste.
   * Parcourir, rechercher, filtrer la liste.
   * Basculez entre les modes Miniature et Liste.
   * Actualisez la liste pour refléter les fragments récemment créés.

1. Faites glisser l’un des fragments dans l’espace réservé du composant de structure.

   L’éditeur effectue le rendu du fragment dans la section/l’élément de la structure de l’email.

Le contenu du fragment est mis à jour de manière dynamique dans la structure afin d’afficher un visuel sur l’affichage du contenu dans l’email.

Si vous souhaitez ajouter le fragment afin qu&#39;il occupe l&#39;intégralité de la disposition horizontale dans l&#39;email, ajoutez une structure de colonnes 1:1, puis faites glisser et déposez le fragment dans celui-ci.

Une fois l’email enregistré, il apparaît dans la section Détails du fragment > Utilisé par . Les fragments ajoutés à un email ne sont pas modifiables dans l’email : le contenu est défini par le fragment source.

>[!TAB Ajouter des fragments à un modèle d’email]

1. Dans le volet de navigation de gauche, cliquez sur **[!UICONTROL Gestion de contenu]** > **[!UICONTROL Modèles]**.

1. Créez un modèle ou ouvrez un modèle de courrier électronique existant et cliquez sur **[!UICONTROL Modifier le modèle de courrier électronique]**.

1. Faites glisser et déposez un élément du menu Composants pour fournir une _structure_ pour le fragment.

1. Pour ouvrir la liste des fragments, cliquez sur l’icône _Fragments_ .

   Vous pouvez :
   * Triez la liste.
   * Parcourir, rechercher, filtrer la liste.
   * Basculez entre les modes Miniature et Liste.
   * Actualisez la liste pour refléter les fragments récemment créés.

1. Faites glisser l’un des fragments dans l’espace réservé du composant de structure.

   L&#39;éditeur effectue le rendu du fragment dans la section/l&#39;élément de la structure du modèle d&#39;email.

1. Faites glisser l’un des fragments dans l’espace réservé du composant de structure.

   L&#39;éditeur effectue le rendu du fragment dans la section/l&#39;élément de la structure du modèle d&#39;email.

Si vous souhaitez ajouter le fragment afin qu&#39;il occupe l&#39;intégralité de la disposition horizontale dans le modèle d&#39;email, ajoutez une structure de colonnes 1:1, puis faites glisser et déposez le fragment dans celui-ci.

Une fois le modèle d’email enregistré, il apparaît dans la section Détails du fragment > _[!UICONTROL Utilisé par]_ . Les fragments ajoutés à un modèle d’email ne sont pas modifiables dans le modèle : le contenu est défini par le fragment source.

>[!ENDTABS]

## Actions de fragment lors de la création

Une fois qu’un fragment est ajouté à un email ou à un modèle d’email, le contenu du fragment ne peut pas être modifié dans l’email ou le modèle. Vous pouvez toutefois appliquer les actions suivantes :

* **[!UICONTROL Supprimer]** - Cette action supprime le fragment du contenu actuel de l’email ou du modèle d’email (la source du fragment n’est pas affectée).
* **[!UICONTROL Actualiser]** : cette action actualise le contenu du fragment dans l’email ou le modèle d’email actuel. Cela s’avère utile lorsque vous souhaitez refléter les modifications récentes apportées au fragment après son ajout au courrier électronique ou au modèle de courrier électronique.
* **[!UICONTROL Dupliquer]** - Cette action duplique le fragment dans le même email ou modèle d&#39;email dans l&#39;éditeur, avec les mêmes dimensions et l&#39;ajoute juste en dessous.
* **[!UICONTROL Ouvrir le fragment]** - Cette action ouvre un nouvel onglet du navigateur avec la page et les détails de l’éditeur de fragments.
* **[!UICONTROL Rompre l’héritage]** : cette action rompt l’héritage du fragment (et de ses modifications) à partir de la source. Utilisez cette action pour rendre le contenu du fragment disponible en tant que contenu modifiable et indépendant dans l’email ou le modèle d’email. Cette action supprime également l’email ou le modèle d’email de la référence _Utilisé par_ pour le fragment d’origine.

Lorsque vous sélectionnez le fragment sur la page de l’éditeur, ces actions sont disponibles dans la barre d’outils contextuelle et dans le panneau des propriétés à droite.
