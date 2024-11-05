---
title: Gouvernance du contenu du modèle
description: Découvrez comment verrouiller des éléments de contenu dans vos modèles de courrier électronique afin que vous puissiez déterminer comment les modifier pour les utiliser dans les parcours de compte.
feature: Email Authoring, Content
source-git-commit: 44413c763ca57d04b83ba78df0ae846142180ec3
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 0%

---

# Gouvernance du contenu du modèle

Dans de nombreuses organisations marketing, il existe des professionnels du contenu qui conçoivent des campagnes par e-mail. Une conception donnée peut servir de base pour les parcours de compte personnalisés dans l’ensemble de l’entreprise. Pour garantir le respect des conceptions de contenu approuvées, vous pouvez utiliser les fonctionnalités de gouvernance de contenu pour verrouiller les composants de modèle. Le verrouillage du contenu étant activé dans le modèle d&#39;email, les marketeurs ne peuvent modifier que les éléments autorisés pour s&#39;aligner sur la stratégie de contenu.

Par exemple, vous pouvez verrouiller l’en-tête et le pied de page conçus pour assurer la continuité des communications de marque. Vous pouvez également verrouiller la colonne contenant la section de corps principale, mais permettre aux auteurs de modifier le texte afin qu’il réponde à leur objectif dans la conception de parcours de compte.

## Activer la gouvernance du contenu pour le modèle

Après avoir utilisé le concepteur visuel pour [créer les composants structurels et de contenu](./email-template-authoring.md) pour votre modèle de courrier électronique, activez la gouvernance et appliquez un verrouillage de contenu spécifique si nécessaire.

1. Dans le concepteur visuel, accédez aux calques/conteneurs et aux éléments à l’aide de l’ _arborescence de navigation_.

   Cliquez sur l’icône _Arborescence de navigation_ ( ![Icône Lien](../assets/do-not-localize/icon-navigation-tree.svg) ) à gauche de la zone de travail pour afficher l’arborescence.

1. Dans l’arborescence, sélectionnez le composant racine **[!UICONTROL Body]**.

   Le panneau des propriétés situé à droite du canevas affiche l’onglet _[!UICONTROL Paramètres]_ par défaut.

1. Activez l’option **[!UICONTROL Gouvernance]** .

   ![Activer la gouvernance pour un modèle de courrier électronique](./assets/governance-template-enable.png){width="800" zoomable="yes"}

   Avec cette option activée, le _[!UICONTROL Mode]_ par défaut est **[!UICONTROL Lecture seule]**. Lorsque ce mode est défini au niveau racine, tous les éléments du modèle sont verrouillés. L’arborescence de gauche affiche l’icône _Lecture seule_ ( ![Icône Lecture seule](../assets/do-not-localize/icon-tree-lock.svg) ) en regard de la racine et de tous les éléments enfants.

1. Pour activer le verrouillage de contenu spécifique dans le modèle, remplacez le **[!UICONTROL mode]** par **[!UICONTROL verrouillage de contenu]**.

   Lorsque ce mode est défini au niveau racine, tous les éléments du modèle sont déverrouillés. L’arborescence de gauche affiche l’icône _de verrouillage du contenu_ ( ![Icône de verrouillage du contenu](../assets/do-not-localize/icon-tree-content-lock.svg) ) en regard de l’élément racine. Appliquez le verrouillage du contenu à des composants de contenu (structurels) et individuels, si nécessaire.

   Pour permettre aux auteurs d’emails de parcours d’ajouter des éléments structurels ou de contenu, activez l’option **[!UICONTROL Activer l’ajout de contenu]**. Choisissez le type d’ajouts que vous souhaitez autoriser :

   * **[!UICONTROL Autoriser la structure et l’ajout de contenu]** - Sélectionnez cette option si vous souhaitez permettre aux auteurs d’ajouter à la fois des éléments structurels et de contenu.

   * **[!UICONTROL Autoriser l’ajout de contenu uniquement]** - Sélectionnez cette option si vous souhaitez permettre aux auteurs d’ajouter uniquement des éléments de contenu.

   ![Activer les ajouts de contenu](./assets/governance-template-content-additions.png){width="600" zoomable="yes"}

   Lorsque ce mode est défini au niveau racine, tous les éléments du modèle sont verrouillés. L’arborescence de gauche affiche l’icône _Lecture seule_ ( ![Icône Lecture seule](../assets/do-not-localize/icon-tree-lock.svg) ) en regard de la racine et de tous les éléments enfants.
<!-- 

   
- ![Link icon](../assets/do-not-localize/icon-navigation-tree.svg)
- ![Read only icon](../assets/do-not-localize/icon-tree-lock.svg)
- ![Content edit icon](../assets/do-not-localize/icon-tree-content-lock.svg)
- ![Content edit icon](../assets/do-not-localize/icon-tree-edit-text.svg)
- ![Edit element](../assets/do-not-localize/icon-edit.svg) -->

## Appliquer un verrouillage à une structure

A l’aide du modèle d’héritage structurel, planifiez la disposition et la structure de votre modèle d’email en fonction de la gouvernance que vous souhaitez appliquer. Utilisez les composants structurels comme conteneurs pour regrouper les éléments de manière à les désigner facilement comme verrouillés ou modifiables. Une fois la conception du modèle d&#39;email en place, vérifiez la structure et appliquez des fonctions de verrouillage en fonction de votre plan.

L’application d’un type de verrouillage au niveau de la structure fournit un paramètre par défaut pour ses composants enfants. Vous pouvez ensuite appliquer un paramètre de verrouillage spécifique au niveau de la colonne ou de l’élément de contenu, si nécessaire.

1. Cliquez sur l’icône _Arborescence de navigation_ ( ![Icône Lien](../assets/do-not-localize/icon-navigation-tree.svg) ) à gauche de la zone de travail pour afficher l’arborescence.

1. Sélectionnez la structure dans l&#39;arborescence.

   Le panneau des propriétés situé à droite du canevas affiche l’onglet _[!UICONTROL Paramètres]_ par défaut.

1. Définissez le **[!UICONTROL type de verrouillage]** :

   * **[!UICONTROL Verrouillé]** - Avec ce paramètre, tous les composants enfants sont verrouillés par défaut. L’arborescence de gauche affiche l’icône _Lecture seule_ ( ![Icône Lecture seule](../assets/do-not-localize/icon-tree-lock.svg) ) en regard de tous les composants enfants.

   * **[!UICONTROL Modifiable]** - Avec ce paramètre, tous les composants enfants sont modifiables par défaut. L’arborescence de gauche n’affiche pas d’icônes en regard des composants enfants.

   ![Appliquer le verrouillage de contenu à un composant structurel](./assets/governance-template-structure-locking.png){width="800" zoomable="yes"}

## Définition du verrouillage d’un composant enfant

1. Sélectionnez le composant dans l’arborescence.

   Le panneau des propriétés situé à droite du canevas affiche l’onglet _[!UICONTROL Paramètres]_ par défaut.

1. Activez l’option **[!UICONTROL Utiliser un verrouillage spécifique]** .

1. Choisissez le type de gouvernance à appliquer :

   * **[!UICONTROL Modifiable]** - Permet un contrôle éditorial complet du composant pendant la création d&#39;emails.
   * **[!UICONTROL Contenu modifiable uniquement]** - Permet aux auteurs de courrier électronique de modifier le contenu, mais pas le composant lui-même.
   * **[!UICONTROL Verrouillé]** - Empêche toute modification du composant pendant la création d’emails.

     Pour un composant verrouillé, vous pouvez autoriser la suppression du composant pendant la création d’un email en activant l’option **[!UICONTROL Autoriser la suppression]**.

   ![Appliquer le verrouillage de contenu à un composant enfant](./assets/governance-template-component-locking.png){width="800" zoomable="yes"}

