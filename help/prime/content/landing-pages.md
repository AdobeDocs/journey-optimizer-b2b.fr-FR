---
title: Pages de destination
description: 'Créez, concevez et publiez des pages de destination pour les parcours de personne : créez entièrement, importez des HTML, ajoutez des formulaires, personnalisez du contenu et des liens à partir d’e-mails dans Journey Optimizer B2B Prime.'
autotag-review: '2026-06-12T22:53:39.337Z'
TQID: 'https://experienceleague.adobe.com/BvtB0i5CzlVutPA6HAzZy-Gfymw7ppZwthyBauyciLc'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e666e996-b2cf-4c45-8fc2-1c625212ababid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: a96755d6-1f54-4f3f-a971-d31f83705ab7id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: cb3217c9fd7beb712d0c61638d143b798010d2b7
workflow-type: tm+mt
source-wordcount: 1461
ht-degree: 6%

---

# Pages de destination

Une page de destination est une page web autonome où vous pouvez diriger les contacts et les clients après qu&#39;ils ont cliqué sur un élément lié dans un e-mail, un SMS ou tout emplacement numérique. Vous pouvez incorporer ces pages dans les parcours de votre compte pour que vos prospects et clients voient vos messages sur le web et progressent dans les parcours de votre compte. Vous pouvez créer, personnaliser et prévisualiser des pages de destination dans l’espace de conception visuelle de la page de destination.

Cas d’utilisation courants des pages de destination :

* Fournir des communications marketing ou un service spécifique avec option d’opt-in ou d’opt-out Utiliser un lien dans un e-mail ou une autre communication vers une liste ciblée
* Collectez le consentement avant d’envoyer des communications et envoyez un e-mail de confirmation lors de l’opt-in ou de l’opt-out.
* Capturez ou mettez à jour les données de profil (profilage progressif, préférences, enregistrements et scénarios similaires) à l’aide de formulaires sur les pages de destination.
* Dirigez les personnes vers des informations spécifiques à une campagne conçues pour votre orchestration de parcours.
* Rediriger les personnes vers un formulaire web dédié sans créer de page externe en dehors de Journey Optimizer B2B Prime.

<!-- 
## Landing page workflow

To direct members of a journey audience to a defined web page when they click a specific link, create a landing page in Journey Optimizer B2B Edition: 


1. [Create the page](./landing-pages-create-publish.md) - Select a preset, set up the primary page, and add any required subpages.
1. [Design the landing page content](./landing-page-design.md) - Build the page content using drag-and-drop visual design components.
1. [Test and publish the landing page](./landing-pages-create-publish.md) - Preview the page, test form behavior, and then publish to make it live.
1. [Link to the page from your journey](#link-to-a-landing-page) - Add the landing page URL to an email, SMS, or journey action so that recipients can reach it.


For example, you can create and design landing pages to direct your users to online information. The page could include a form where they can opt in or opt out from receiving your communications. Or it could be an opportunity to subscribe to a recurring communications, such as a newsletter. 

You can create, personalize, and preview landing pages in the visual design space.
-->
## Accéder aux pages de destination et les gérer

Pour accéder aux pages de destination dans Journey Optimizer B2B Prime, accédez au volet de navigation de gauche et cliquez sur **[!UICONTROL Gestion de contenu]** > **[!UICONTROL Pages de destination]**. Cette action affiche la liste de toutes les pages de destination créées dans l’instance.

La liste est triée en fonction de la colonne _[!UICONTROL Modifié]_, les éléments les plus récemment mis à jour étant en haut. Cliquez sur le titre de la colonne pour passer d’un ordre croissant à un ordre décroissant.

### Filtrer la liste des landing pages

Pour rechercher une page de destination par nom, saisissez une chaîne de texte dans la barre de recherche pour rechercher une correspondance. Cliquez sur l’icône _Filtrer_ <!-- ( ![Show or hide filters icon](../assets/do-not-localize/icon-filter.svg) ) --> afficher les options de filtrage disponibles et modifier les paramètres pour filtrer les éléments affichés en fonction de vos critères spécifiés.

![Filtrer les pages de destination affichées](./assets/landing-pages-list-filtered.png){width="800" zoomable="yes"}

<!-- 
This is going away? ### Customize the column display

Customize the columns that you want to display in the table by clicking the _Customize table_ icon ( ![Customize table icon](../assets/do-not-localize/icon-column-settings.svg) ) at the top right. 

In the dialog, select the columns to display and click **[!UICONTROL Apply]**.

![Select the columns that you want to display](./assets/landing-pages-customize-table-dialog.png){width="300"} 
-->

### Statut et cycle de vie de la page de destination

Le statut de la page de destination détermine sa disponibilité pour la liaison dans le contenu de votre e-mail et de votre SMS, ainsi que les modifications que vous pouvez y apporter.

| Statut | Description |
| -------------------- | ----------- |
| Brouillon | Lorsque vous créez une page de destination, elle a le statut de brouillon. Il reste dans ce statut lorsque vous définissez ou modifiez le contenu visuel, et jusqu’à ce que vous le publiiez en tant que page hébergée. Actions disponibles :<br/><ul><li>Modifier le nom ou la description<li>Modifier l&#39;URL du lien<li>Modification dans l’espace de conception visuelle<li>Publier<li>Dupliquer<li>Supprimer |
| Publié | Lorsque vous publiez une page de destination, elle est hébergée sur l’instance Prime B2B de Journey Optimizer et peut être liée dans un contenu d’e-mail ou de SMS. Actions disponibles :<br/><ul><li>Modifier le nom ou la description<li>Modifier l&#39;URL du lien<li>Ajouter un lien dans le contenu d’un e-mail ou d’un SMS<li>Créer une version brouillon<li>Dupliquer<li>Supprimer |
| Publié avec le brouillon | Lorsque vous créez un brouillon à partir d’une page de destination publiée, la version publiée est conservée et le contenu du brouillon peut être modifié dans l’espace de conception visuelle. Si vous publiez le brouillon, il remplace la version publiée actuelle et le contenu est mis à jour dans la page hébergée. Actions disponibles :<br/><ul><li>Modifier le nom ou la description<li>Modifier l&#39;URL du lien<li>Ajouter un lien dans le contenu d’un e-mail ou d’un SMS<li>Modifier le brouillon dans l’espace de conception visuelle<li>Publier le brouillon<li>Dupliquer<li>Supprimer (supprime les deux versions)<li>Ignorer le brouillon (revient au statut publié) |

<!-- ![Landing page status lifecycle](./assets/status-lifecycle-diagram.png){zoomable="yes"} -->

## Créer une page de destination {#create-landing-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_create"
>title="Définissez et configurez votre page de destination."
>abstract="Pour créer une page de destination, vous devez sélectionner un préréglage, puis configurer la page principale et les sous-pages, et enfin tester la page avant de la publier."

À déterminer

## Configurer la page principale {#configure-primary-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_primary_page"
>title="Définissez les paramètres de votre page principale."
>abstract="Définissez la page principale, qui s’affiche immédiatement lorsqu’un destinataire clique sur le lien de la page de destination, par exemple à partir d’un e-mail ou d’un site web."

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_access_settings"
>title="Définissez lʼURL de votre page de destination."
>abstract="Dans cette section, définissez une URL de page de destination unique. La première partie de l’URL nécessite la configuration préalable d’un sous-domaine de page de destination dans le cadre du préréglage que vous avez sélectionné."

À déterminer

## Tester la page de destination {#test-landing-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_preview_lp_profiles"
>title="Prévisualiser et tester votre page de destination"
>abstract="Une fois que vous avez défini les paramètres et le contenu de votre page de destination, utilisez des profils de test pour prévisualiser la page."

À déterminer

## Modification d’une page de destination

Les modifications apportées à une landing page dépendent de son statut actuel :

* Lorsqu’une page de destination a le statut **_Brouillon_**, vous pouvez modifier n’importe quel de ses détails, l’URL et le contenu visuel.
* Lorsqu’une page de destination a le statut **_Publiée_**, vous pouvez modifier sa description, mais pas son nom. Pour modifier le contenu visuel, vous devez créer un brouillon de la page.
* Lorsqu’une page de destination affiche le statut **_Publiée avec le brouillon_**, la modification des détails se limite à la description. Vous pouvez également modifier le contenu visuel de la version brouillon.

>[!BEGINTABS]

>[!TAB Brouillon]

1. Dans la page de liste _[!UICONTROL Pages de destination]_, cliquez sur le nom de la page de destination pour l’ouvrir.

   Un aperçu du contenu visuel s’affiche, avec les détails de la page de destination sur la droite.

1. Modifiez l’un des détails, tels que le nom et la description.

   <!-- ![Details for landing page with Draft status](./assets/landing-page-draft-details.png){width="700" zoomable="yes"} -->

1. Pour apporter des modifications au contenu de l’espace de conception visuelle, cliquez sur **[!UICONTROL Modifier la page de destination]**.

   <!-- 
   Use the visual design tools as needed:

   * [Add structure and content](./landing-page-design.md#structure-content-landing-page)
   * [Add Assets](./landing-page-design.md#add-assets)
   * [Navigate the layers, settings, and styles](./landing-page-design.md#navigate-the-layers-settings-and-styles)
   * [Personalize content](./landing-page-design.md#personalize-content)
   * [Edit linked URL tracking](./landing-page-design.md#edit-linked-url-tracking)
   -->

1. Cliquez sur **[!UICONTROL Enregistrer]** ou **[!UICONTROL Enregistrer et fermer]** pour revenir aux détails de la page de destination.

1. Lorsque la page répond à vos critères et que vous souhaitez la rendre disponible pour affichage, cliquez sur **[!UICONTROL Publier]**.

>[!TAB Publié]

1. Dans la page de liste _[!UICONTROL Pages de destination]_, cliquez sur le nom de la page pour l’ouvrir.

   Un aperçu du contenu visuel s’affiche, avec les détails de la page de destination sur la droite.

1. Modifiez la description, si nécessaire.

   Pour une page de destination publiée, tous les autres détails ne peuvent pas être modifiés.

1. Si vous souhaitez mettre à jour le contenu, cliquez sur **[!UICONTROL Modifier la page de destination]** à droite.

   Cliquez sur **[!UICONTROL Créer un brouillon]** dans la boîte de dialogue pour ouvrir le brouillon dans l’espace de conception visuelle.

   <!-- 
   ![Create draft version dialog](./assets/landing-page-create-draft-version.png){width="300"} 

   Use the visual design tools as needed:

   * [Add structure and content](./landing-page-design.md#structure-content-landing-page)
   * [Add Assets](./landing-page-design.md#add-assets)
   * [Navigate the layers, settings, and styles](./landing-page-design.md#navigate-the-layers-settings-and-styles)
   * [Personalize content](./landing-page-design.md#personalize-content)
   * [Edit linked URL tracking](./landing-page-design.md#edit-linked-url-tracking)
   -->

1. Cliquez sur **[!UICONTROL Enregistrer]** ou **[!UICONTROL Enregistrer et fermer]** pour revenir aux détails de la page de destination.

1. Lorsque le brouillon de la page de destination répond à vos critères et que vous souhaitez que les modifications soient disponibles sur la page publiée, cliquez sur **[!UICONTROL Publier]**.

   Lorsque vous publiez le brouillon, il remplace la version publiée actuelle et le contenu est mis à jour pour l’URL de la page.

>[!TAB Publié avec le brouillon]

Lorsque vous ouvrez la page de destination, le brouillon s’affiche. Les onglets situés en haut de l’espace d’aperçu vous permettent de basculer l’affichage entre les versions publiées et les brouillons. Les actions de brouillon et les détails s’affichent à droite.

<!-- ![Preview and details for the landing page draft version](./assets/landing-page-published-draft-details.png){width="700" zoomable="yes"} -->

Pour mettre à jour le contenu :

1. Cliquez sur **[!UICONTROL Modifier la page de destination]** en haut à droite.

   <!--

   Use the visual design tools as needed:

   * [Add structure and content](./landing-page-design.md#structure-content-landing-page)
   * [Add Assets](./landing-page-design.md#add-assets)
   * [Navigate the layers, settings, and styles](./landing-page-design.md#navigate-the-layers-settings-and-styles)
   * [Personalize content](./landing-page-design.md#personalize-content)
   * [Edit linked URL tracking](./landing-page-design.md#edit-linked-url-tracking)

   -->

1. Cliquez sur **[!UICONTROL Enregistrer]** ou **[!UICONTROL Enregistrer et fermer]** pour revenir aux détails de la page de destination.

1. Lorsque le brouillon de page répond à vos critères et que vous souhaitez rendre les modifications disponibles, cliquez sur **[!UICONTROL Publier]**.

   Lorsque vous publiez le brouillon, il remplace la version publiée actuelle et le contenu est mis à jour dans la page hébergée.

>[!ENDTABS]

## Dupliquer une landing page

Vous pouvez dupliquer une page de destination à l’aide de l’une des méthodes suivantes :

* Sur la page de liste _[!UICONTROL Page de destination]_, cliquez sur l’icône _Plus_ (**...**) en regard du nom de la page de destination et choisissez **[!UICONTROL Dupliquer]**.
* En haut à droite de la page de détails de la page de destination, cliquez sur **[!UICONTROL ... En plus]** et choisissez **[!UICONTROL Dupliquer]**.

<!-- ![Duplicate the landing page](./assets/landing-page-details-duplicate-delete.png){width="600" zoomable="yes"} -->

Dans la boîte de dialogue, saisissez un nom utile (unique) et une description (facultatif). Cliquez sur **[!UICONTROL Dupliquer]** pour terminer l’action.

<!-- ![Enter a name and description for the duplicated landing page](./assets/landing-page-duplicate-dialog.png){width="350"} -->

La page dupliquée (nouvelle) apparaît alors dans la liste _Pages de destination_.

## Suppression d’une landing page

Vous pouvez supprimer une page de destination à l’aide de l’une des méthodes suivantes :

* Sur la page de liste _[!UICONTROL Page de destination]_, cliquez sur l’icône _Plus_ (**...**) en regard du nom de la page de destination et choisissez **[!UICONTROL Supprimer]**.
* En haut à droite de la page de détails de la page de destination, cliquez sur **[!UICONTROL ... Plus]** puis choisissez **[!UICONTROL Supprimer]**.

Cette action ouvre une boîte de dialogue de confirmation. Vous pouvez abandonner le processus en cliquant sur **[!UICONTROL Annuler]** ou sur **[!UICONTROL Supprimer]** pour confirmer la suppression.

<!-- ![Delete landing page dialog](./assets/landing-page-delete-dialog.png){width="400"} -->

## Lien vers une landing page

En tant que spécialiste marketing ou créatif qui produit du contenu d’e-mail, de fragment et de page, vous pouvez incorporer des liens vers les pages de destination publiées (en direct) qui sont créées dans votre instance Journey Optimizer B2B Prime.

1. Lorsque vous travaillez dans l’espace de conception visuelle d’un fragment, d’un e-mail, d’une page de destination ou d’un modèle, sélectionnez un extrait de texte, un composant de bouton ou un composant d’image pour le lien.

   Les options **[!UICONTROL Lien]** s’affichent dans le panneau de droite.

1. Pour l’option **[!UICONTROL Type]**, choisissez **[!UICONTROL Page de destination]**.

   <!-- ![Link options for a landing page](/help/assets/content-design-shared/content-design-link-settings.png){width="700" zoomable="yes"} -->

1. Pour l&#39;option **[!UICONTROL Landing page]**, cliquez sur l&#39;icône _Sélectionner une page_ <!-- ( ![Show links icon](/help/assets/do-not-localize/icon-landing-page-select.svg) ) -->.

1. Dans la boîte de dialogue Sélectionner une page de destination , définissez la **[!UICONTROL Source de la page de destination]** en tant que **[!UICONTROL B2B edition Journey Optimizer]**, cochez la case de la page de destination dans la liste des pages publiées, puis cliquez sur **[!UICONTROL Sélectionner]**.

   <!-- ![Link options for a landing page](/help/assets/content-design-shared/content-design-link-landing-page-select.png){width="600" zoomable="yes"} -->

1. Pour l’option **[!UICONTROL Cible]**, choisissez le comportement de la cible du lien :

   * **[!UICONTROL Aucune]** - Ouvre le lien à l’aide du comportement par défaut du navigateur.
   * **[!UICONTROL Vide]** - Ouvre le lien dans une nouvelle fenêtre ou un nouvel onglet.
   * **[!UICONTROL Self]** - Ouvre le lien dans le même cadre.
   * **[!UICONTROL Parent]** - Ouvre le lien dans le cadre parent.
   * **[!UICONTROL Haut]** - Ouvre le lien dans le corps complet de la fenêtre.

1. (Lien de texte uniquement) Pour souligner le texte lié, cochez la case **[!UICONTROL Souligner le lien]**.

   Vous pouvez définir un style supplémentaire pour le texte du lien, y compris la couleur du lien, en sélectionnant l’onglet **[!UICONTROL Styles]** dans le panneau de droite.
