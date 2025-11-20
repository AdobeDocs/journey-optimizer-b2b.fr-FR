---
title: Utiliser l’Assets d’image interne
description: 'Parcourez, gérez et utilisez des ressources Journey Optimizer B2B edition : organisez des dossiers, modifiez des images et créez du contenu pour les parcours de compte.'
feature: Assets, Content
role: User
exl-id: 430ae5b7-2691-454c-bbd2-5a0b7a8843fb
source-git-commit: 1c5a08b293db9287d03b103d794cc17a1c186af0
workflow-type: tm+mt
source-wordcount: '1758'
ht-degree: 1%

---

# Utilisation des ressources d’image internes

Le référentiel de ressources d’images interne est la source de ressources d’image par défaut. Vous pouvez facilement gérer et utiliser les ressources disponibles pour concevoir du contenu qui prend en charge les parcours de votre compte.

Vous disposez de l’ensemble des fonctions de gestion des ressources dans Journey Optimizer B2B edition. Ces fonctions incluent :

* [Remplacer](#replace-assets)
* [Supprimer](#delete-assets)
* [Déplacer](#create-a-folder)
* [Modifier avec Adobe Express](./image-edit-adobe-express.md)

## Parcourir et accéder aux ressources

Pour accéder aux ressources internes dans Journey Optimizer B2B edition, accédez au volet de navigation de gauche et cliquez sur **[!UICONTROL Gestion de contenu]** > **[!UICONTROL Assets]**. Cette action ouvre une page de liste contenant toutes les ressources répertoriées.

![Parcourir les ressources d’image](assets/assets-list-page.png){width="800" zoomable="yes"}

* Pour afficher les ressources par dossier, ouvrez la structure en cliquant sur l’icône _Afficher les dossiers_ en haut à gauche.

* Pour trier le tableau en fonction de l’une des colonnes, cliquez sur le titre de la colonne. La flèche située dans la ligne de titre indique la colonne de tri et l’ordre actuels.

* Pour rechercher une ressource image dans le dossier sélectionné, saisissez une chaîne de texte dans la barre de recherche.

* Pour personnaliser les colonnes affichées dans le tableau, cliquez sur l’icône _Personnaliser le tableau_ ( ![Personnaliser le tableau](../assets/do-not-localize/icon-column-settings.svg) ) en haut à droite.

  Sélectionnez les colonnes à afficher dans la liste et cliquez sur **[!UICONTROL Appliquer]**.

## Affichage des détails de la ressource

Cliquez sur le nom d’une ressource pour ouvrir la page des détails de la ressource.

![Accéder aux détails de la ressource](assets/assets-details.png){width="700" zoomable="yes"}

## Afficher les références de ressources utilisées par

Dans la page des détails de la ressource, cliquez sur l’onglet **[!UICONTROL Utilisé par]** pour afficher des détails sur l’emplacement où la ressource est actuellement utilisée dans Journey Optimizer B2B edition, dans les e-mails, les modèles d’e-mail et les fragments.

>[!IMPORTANT]
>
>Toute ressource actuellement _EN COURS D’UTILISATION_ dans l’un des e-mails, modèles d’e-mail ou fragments **ne peut pas** être supprimée.

Le panneau affiche les références par catégorie : _e-mail_, _modèle d’e-mail_ ou _fragment_. Les e-mails dans Journey Optimizer B2B edition sont incorporés et créés dans des parcours, de sorte que le parcours parent de l’e-mail qui utilise la ressource s’affiche dans les références.

Cliquer sur le lien vous redirige vers l’e-mail, le modèle d’e-mail ou le fragment correspondant où la ressource est utilisée.

![Afficher les éléments de contenu qui utilisent la ressource](assets/assets-used-by.png){width="700" zoomable="yes"}

## Ajout de ressources

Dans la page de liste _Assets_, vous pouvez ajouter des ressources d’image au référentiel de ressources de Journey Optimizer B2B edition.

1. Cliquez sur **[!UICONTROL Ajouter Assets]** en haut à droite.

1. Dans la boîte de dialogue _[!UICONTROL Ajouter des ressources]_, effectuez un glisser-déposer d’un ou de plusieurs fichiers de votre système dans la zone de fichier.

   ![Ajout de ressources à un dossier](./assets/assets-add-dialog.png){width="500"}

   Vous pouvez également cliquer sur le lien _[!UICONTROL Sélectionner un fichier sur votre ordinateur]_ pour utiliser votre système de fichiers local afin de rechercher et sélectionner des fichiers.

   Vous pouvez charger des ressources à partir de votre système local avec un maximum de 10 fichiers à la fois. La taille de fichier maximale est de 100 Mo.

   Les noms de fichier des images sélectionnées s’affichent dans la boîte de dialogue. Les noms de fichiers de ressources doivent être uniques (dans plusieurs dossiers) et, si un fichier portant ce nom existe déjà, un message s’affiche. Les noms peuvent contenir au maximum 100 caractères et ne peuvent pas contenir de caractères spéciaux (par exemple `;`, `:`, `\` et `|`).

1. Sélectionnez le dossier de destination dans lequel stocker les ressources.

1. Pour remplacer des fichiers lorsque vous chargez un ou plusieurs fichiers portant un nom de fichier existant, cochez la case **[!UICONTROL Remplacer les fichiers existants]**.

1. Cliquez sur **[!UICONTROL Ajouter]**.

## Suppression de ressources

Les ressources actuellement utilisées dans les e-mails, modèles d’e-mail ou fragments ne peuvent pas être supprimées. Vérifiez les références utilisées par avant de lancer la suppression d’une ressource. En outre, une action de suppression ne peut pas être annulée. Vérifiez-la avant de lancer une action de suppression.

Utilisez l’une des méthodes suivantes pour supprimer une ressource :

* Accédez aux détails de la ressource, cliquez sur **[!UICONTROL ... Plus]** en haut à droite, puis choisissez **[!UICONTROL Supprimer]** dans les options.

  ![Actions d’accès à la ressource](./assets/assets-details-more-menu.png){width="450" zoomable="yes"}

* Sur la page de liste _[!UICONTROL Assets]_, cliquez sur l’icône _Plus_ (**[!UICONTROL ...]**) à côté de l’élément de ressource et choisissez **[!UICONTROL Supprimer]** dans les options.

  ![Actions d’accès à la ressource](./assets/assets-list-file-more-menu.png){width="600" zoomable="yes"}

Cette action ouvre une boîte de dialogue de confirmation. Vous pouvez abandonner le processus en cliquant sur **[!UICONTROL Annuler]** ou sur **[!UICONTROL Supprimer]** pour confirmer la suppression.

Si la ressource est en cours d’utilisation, l’action ouvre une boîte de dialogue d’information qui vous avertit qu’elle ne peut pas être supprimée. Cliquez sur **[!UICONTROL OK]** pour annuler la suppression.

## Remplacement de ressources

Utilisez l’une des méthodes suivantes pour remplacer une ressource résidant dans le référentiel de ressources _[!UICONTROL Journey Optimizer B2B edition]_ :

* Accédez aux détails de la ressource, cliquez sur **[!UICONTROL ... Plus]** en haut à droite, puis choisissez **[!UICONTROL Remplacer]** dans les options.

* Sur la page de liste _[!UICONTROL Assets]_, cliquez sur l’icône _Plus_ (**[!UICONTROL ...]**) à côté de l’élément de ressource et sélectionnez **[!UICONTROL Remplacer]** dans les options.

Dans la boîte de dialogue _[!UICONTROL Remplacer la ressource]_, faites glisser le fichier de remplacement de votre système et déposez-le dans la zone de fichier. Vous pouvez également cliquer sur le lien _[!UICONTROL Sélectionner un fichier sur votre ordinateur]_ pour utiliser votre système de fichiers local afin de sélectionner un fichier. (Si vous sélectionnez plusieurs fichiers dans votre système local, le premier fichier sélectionné est utilisé pour le remplacement.)

![&#x200B; Boîte de dialogue Remplacer la ressource &#x200B;](./assets/assets-replace-dialog.png){width="500"}

Pour continuer, cliquez sur **[!UICONTROL Remplacer]**. Vous pouvez abandonner le processus en cliquant sur **[!UICONTROL Annuler]**.

Si le fichier à remplacer est en cours d’utilisation, une boîte de dialogue vous informe que le nouveau fichier image remplace l’image là où elle est utilisée (e-mails, modèles d’e-mail et fragments).

## Téléchargement de ressources

Vous pouvez télécharger une ressource à l’aide de l’une des méthodes suivantes :

* Accédez aux détails de la ressource et cliquez sur **[!UICONTROL Télécharger]** en haut à droite.

* Sur la page de liste _[!UICONTROL Assets]_, cliquez sur le _Points de suspension_ (**[!UICONTROL ...]**) à côté de l’élément de ressource et sélectionnez **[!UICONTROL Télécharger]** dans les options.

Dans la boîte de dialogue de confirmation, cliquez sur **[!UICONTROL Télécharger]** pour lancer le téléchargement de la ressource vers votre système local. Vous pouvez abandonner le processus en cliquant sur **[!UICONTROL Annuler]**.

## Application d’actions en bloc sur les ressources sélectionnées

Dans la page de liste (_[!UICONTROL Gestion de contenu]_ > _[!UICONTROL Assets]_), sélectionnez plusieurs ressources à la fois en cochant chaque case à gauche. Une bannière de message s’affiche en bas lorsque vous sélectionnez plusieurs ressources.

![&#x200B; Ressources sélectionnées &#x200B;](./assets/assets-list-selected.png){width="700" zoomable="yes"}

Vous pouvez effectuer les actions en bloc suivantes pour les ressources sélectionnées résidant dans le référentiel de ressources _[!UICONTROL Journey Optimizer B2B edition]_ :

+++Déplacer des ressources

1. Sur la bannière de sélection, cliquez sur **[!UICONTROL Déplacer]**.

   Cette action ouvre la boîte de dialogue _[!UICONTROL Déplacer Assets]_ qui répertorie les noms des ressources sélectionnées et vous permet de sélectionner le dossier _cible_ dans lequel vous souhaitez déplacer ces ressources.

1. Sélectionnez un dossier.

   Le chemin d’accès en regard de _[!UICONTROL Les ressources sélectionnées seront déplacées vers]_ reflète la modification.

1. Cliquez sur **[!UICONTROL Déplacer]**.

+++

+++Suppression de ressources

>[!NOTE]
>
>Vous pouvez appliquer une suppression en bloc pour un maximum de 20 ressources sélectionnées.

1. Sur la bannière de sélection, cliquez sur **[!UICONTROL Supprimer]**.

1. Dans la boîte de dialogue de confirmation, cliquez sur **[!UICONTROL Supprimer]**.

   Si l’une des ressources sélectionnées est en cours d’utilisation, la suppression de cette ressource est abandonnée et un message d’alerte s’affiche.

+++

## Création d’un dossier

1. Sur la page de liste _[!UICONTROL Assets]_, cliquez sur **[!UICONTROL Créer un dossier]** en haut à droite.

1. Dans la boîte de dialogue, saisissez le nom du dossier et sélectionnez le dossier de destination (parent) pour le nouveau dossier.

   Les noms de dossier doivent être uniques, comporter un maximum de 100 caractères et ne peuvent pas contenir de caractères spéciaux, tels que `;`, `:`, `\`, `|`.

   ![&#x200B; Boîte de dialogue Créer un dossier &#x200B;](./assets/assets-create-folder-dialog.png){width="500"}

1. Cliquez sur **[!UICONTROL Ajouter]**.

## Application d’actions au niveau du dossier

Vous pouvez appliquer des actions à un dossier ou à des ressources du dossier. Cliquez sur l’icône _Plus_ (**...**) en regard du dossier pour afficher les actions que vous pouvez lui appliquer.

![Appliquer des actions à un ou plusieurs dossiers dans le dossier](./assets/assets-folder-menu-options.png){width="700" zoomable="yes"}

Vous pouvez effectuer les actions suivantes au niveau du dossier :

+++Ajout de ressources

1. Sélectionnez **[!UICONTROL Ajouter des ressources]** pour charger des fichiers image dans le dossier.

1. Dans la boîte de dialogue _[!UICONTROL Ajouter des ressources]_, effectuez un glisser-déposer des fichiers de votre système. Vous pouvez également cliquer sur le lien pour utiliser votre système de fichiers et sélectionner les fichiers.

   Vous pouvez ajouter des ressources de votre système local contenant jusqu’à 10 fichiers à la fois. Vous avez la possibilité de remplacer des fichiers lorsque vous chargez un ou plusieurs fichiers portant un nom de fichier existant.

   Les noms de fichier des images sélectionnées s’affichent dans la boîte de dialogue. Les noms de fichiers de ressources doivent être uniques (dans plusieurs dossiers) et, si un fichier portant ce nom existe déjà, un message d’erreur s’affiche. Les noms peuvent contenir au maximum 100 caractères et ne peuvent pas contenir de caractères spéciaux (par exemple `;`, `:`, `\` et `|`).

1. Cliquez sur **[!UICONTROL Ajouter]**.

+++

+++Créer un sous-dossier

1. Choisissez **[!UICONTROL Créer un dossier]**.

1. Dans la boîte de dialogue, saisissez le nom du dossier.

   Les noms de dossier doivent être uniques, comporter un maximum de 100 caractères et ne peuvent pas contenir de caractères spéciaux, tels que `;`, `:`, `\`, `|`.

1. Cliquez sur **[!UICONTROL Ajouter]**.

+++

+++Renommer le dossier

1. Choisissez **[!UICONTROL Renommer]**.

1. Dans la boîte de dialogue, saisissez le nouveau nom de dossier.

   Les noms de dossier doivent être uniques, comporter un maximum de 100 caractères et ne peuvent pas contenir de caractères spéciaux, tels que `;`, `:`, `\`, `|`.

1. Cliquez sur **[!UICONTROL Enregistrer]**

+++

+++Déplacer le dossier

1. Pour déplacer le dossier vers un autre dossier parent, choisissez **[!UICONTROL Déplacer]**.

1. Dans la boîte de dialogue, sélectionnez le dossier cible comme nouveau parent pour le sous-dossier.

1. Cliquez sur **[!UICONTROL Déplacer]**.

   Si vous essayez de déplacer un dossier dans l’un de ses propres sous-dossiers (dans la structure du dossier sélectionné), un message d’erreur s’affiche et le déplacement est annulé.

+++

+++Supprimer le dossier

1. Choisissez **[!UICONTROL Supprimer]**.

1. Dans la boîte de dialogue de confirmation, cliquez sur **[!UICONTROL Supprimer]**.

Si l’une des ressources du dossier est en cours d’utilisation, l’action ouvre une boîte de dialogue d’alerte pour vous informer qu’elle ne peut pas être supprimée. Cliquez sur **[!UICONTROL OK]** pour annuler la suppression.

+++

+++Convertir en dossier d’archives

L’archivage d’un dossier rend les fichiers qu’il contient impossibles à rechercher. Utilisez la fonction d’archivage pour les fichiers de ressources que vous ne souhaitez pas que les membres de votre équipe utilisent à l’avenir, tels qu’un badge promotionnel d’événement obsolète ou du contenu saisonnier. Par la suite, vous pouvez désarchiver un dossier si vous souhaitez que le contenu soit à nouveau disponible.

* Choisissez **[!UICONTROL Convertir en dossier d’archive]**. Une bannière de confirmation s’affiche pour confirmer que le statut du dossier est passé à archivé.

* Choisissez **[!UICONTROL Désarchiver le dossier]**. Une bannière de confirmation s’affiche pour confirmer que le statut du dossier est passé à désarchivé.

+++

## Utilisation de ressources dans votre contenu

Assets peut être utilisé pour la création d’e-mails, de modèles d’e-mail ou de fragments visuels dans votre équipe à partir de l’éditeur de contenu visuel.

Dans l’espace de conception visuelle, sélectionnez l’icône _Assets_ ( ![icône Assets](../../assets/do-not-localize/icon-assets-me.svg) ) dans la barre latérale gauche.

Cette action modifie le panneau Outils qui affiche une liste des ressources disponibles. Il existe plusieurs méthodes pour ajouter une ressource d’image à la zone de travail visuelle :

* Glissez-déposez une miniature d’image à partir du volet de navigation de gauche.

* Ajoutez un composant d’image à la zone de travail et cliquez sur **[!UICONTROL Sélectionner une ressource]** dans le composant pour ouvrir la boîte de dialogue _[!UICONTROL Sélectionner une ressource]_.

  ![Utilisez les filtres et le champ de recherche pour trouver la ressource dont vous avez besoin](./assets/assets-select-dialog-marketo.png){width="700" zoomable="yes"}

  Dans la boîte de dialogue, vous pouvez choisir une image dans le référentiel sélectionné. Cliquez sur **[!UICONTROL Sélectionner]** pour ajouter la ressource.

  Plusieurs outils sont disponibles pour vous aider à localiser la ressource dont vous avez besoin :

   * Cliquez sur l’icône _Filtrer_ en haut à gauche pour filtrer les éléments affichés en fonction de vos critères.

   * Saisissez du texte dans le champ _Rechercher_ pour filtrer les éléments affichés afin qu’ils correspondent au nom de la ressource.

  ![Utilisez les filtres et le champ de recherche pour trouver la ressource dont vous avez besoin](./assets/assets-select-dialog-marketo-filtered.png){width="700" zoomable="yes"}
