---
title: Gouvernance du contenu des modèles
description: Découvrez comment verrouiller les éléments de contenu dans vos modèles d’e-mail afin de pouvoir régir la manière dont ils peuvent être modifiés pour une utilisation dans les parcours de compte.
feature: Templates, Email Authoring, Content
role: User
exl-id: 0cf852cd-491c-4478-8d5e-51fd2cc2625a
source-git-commit: 4905346d8160147f7d71b7b1131ea33f26d3bba0
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 0%

---

# Gouvernance du contenu des modèles

Dans de nombreuses organisations marketing, des professionnels du contenu conçoivent des campagnes par e-mail. Une conception donnée peut être utilisée comme base pour les parcours de compte personnalisés à l’échelle de l’organisation. Pour garantir la conformité aux conceptions de contenu approuvées, vous pouvez utiliser les fonctionnalités de gouvernance de contenu pour verrouiller les composants de modèle. Lorsque le verrouillage de contenu est activé dans le modèle d’e-mail, les personnes spécialisées dans le marketing ne peuvent modifier que les éléments autorisés pour rester alignées sur la stratégie de contenu.

Par exemple, vous pouvez verrouiller l’en-tête et le pied de page conçus pour assurer la continuité des communications de la marque. Vous pouvez également verrouiller la colonne qui contient la section du corps principale, mais autoriser les auteurs à modifier le texte afin qu’il réponde à leur objectif dans la conception du parcours de compte.

## Activer la gouvernance de contenu pour le modèle

Après avoir utilisé le concepteur visuel pour [créer les composants de structure et de contenu](./email-template-authoring.md) pour votre modèle d’e-mail, activez la gouvernance et appliquez un verrouillage de contenu spécifique si nécessaire.

1. Dans le concepteur visuel, accédez aux calques/conteneurs et aux éléments à l’aide de l’_arborescence de navigation_.

   Cliquez sur l’icône _Arborescence de navigation_ ( ![Icône Lien](../assets/do-not-localize/icon-navigation-tree.svg) ) à gauche de la zone de travail pour afficher l’arborescence.

1. Dans l’arborescence, sélectionnez le composant racine **[!UICONTROL Corps]**.

   Le panneau des propriétés situé à droite de la zone de travail affiche par défaut l’onglet _[!UICONTROL Paramètres]_.

1. Activez l’option **[!UICONTROL Gouvernance]**.

   ![Activer la gouvernance pour un modèle d’e-mail](./assets/governance-template-enable.png){width="800" zoomable="yes"}

   Lorsque cette option est activée, le _[!UICONTROL Mode]_ par défaut est **[!UICONTROL Lecture seule]**. Lorsque ce mode est défini au niveau racine, tous les éléments du modèle sont verrouillés. L’arborescence à gauche affiche l’icône _Lecture seule_ ( ![Icône Lecture seule](../assets/do-not-localize/icon-tree-lock.svg) ) à côté des éléments racine et tous les éléments enfants.

1. Pour activer le verrouillage de contenu spécifique dans le modèle, remplacez le **[!UICONTROL Mode]** par **[!UICONTROL Verrouillage de contenu]**.

   Lorsque ce mode est défini au niveau racine, tous les éléments du modèle sont déverrouillés. L’arborescence à gauche affiche l’icône _Verrouillage du contenu_ ( ![Icône de verrouillage du contenu](../assets/do-not-localize/icon-tree-content-lock.svg) ) en regard de l’élément racine. Appliquez un verrouillage de contenu pour contenir (structurel) et les composants de contenu individuels selon les besoins.

   Pour permettre aux auteurs d’e-mails de parcours d’ajouter des éléments de structure ou de contenu, activez **[!UICONTROL Activer l’ajout de contenu]**. Choisissez le type d’ajouts que vous souhaitez autoriser :

   * **[!UICONTROL Autoriser l’ajout de structure et de contenu]** - Sélectionnez cette option si vous souhaitez autoriser les auteurs à ajouter des éléments de structure et de contenu.

   * **[!UICONTROL Autoriser l’ajout de contenu uniquement]** - Sélectionnez cette option si vous souhaitez autoriser les auteurs à ajouter uniquement des éléments de contenu.

   ![Activer les ajouts de contenu](./assets/governance-template-content-additions.png){width="600" zoomable="yes"}

   Lorsque ce mode est défini au niveau racine, tous les éléments du modèle sont verrouillés. L’arborescence à gauche affiche l’icône _Lecture seule_ ( ![Icône Lecture seule](../assets/do-not-localize/icon-tree-lock.svg) ) à côté des éléments racine et tous les éléments enfants.
<!-- 

   
- ![Link icon](../assets/do-not-localize/icon-navigation-tree.svg)
- ![Read only icon](../assets/do-not-localize/icon-tree-lock.svg)
- ![Content edit icon](../assets/do-not-localize/icon-tree-content-lock.svg)
- ![Content edit icon](../assets/do-not-localize/icon-tree-edit-text.svg)
- ![Edit element](../assets/do-not-localize/icon-edit.svg) -->

## Appliquer un verrouillage à une structure

À l’aide du modèle d’héritage structurel, planifiez la disposition et la structure de votre modèle d’e-mail en fonction de la gouvernance que vous souhaitez appliquer. Utilisez les composants structurels en tant que conteneurs pour regrouper les éléments de manière à faciliter leur désignation comme verrouillés ou modifiables. Lorsque la conception du modèle d’e-mail est en place, passez en revue la structure et appliquez les fonctions de verrouillage en fonction de votre plan.

L’application d’un type de verrouillage au niveau de la structure fournit un paramètre par défaut pour ses composants enfants. Vous pouvez ensuite appliquer un paramètre de verrouillage spécifique au niveau de la colonne ou de l’élément de contenu, selon vos besoins.

1. Cliquez sur l’icône _Arborescence de navigation_ ( ![Icône Lien](../assets/do-not-localize/icon-navigation-tree.svg) ) à gauche de la zone de travail pour afficher l’arborescence.

1. Sélectionnez la structure dans l&#39;arborescence.

   Le panneau des propriétés situé à droite de la zone de travail affiche par défaut l’onglet _[!UICONTROL Paramètres]_.

1. Définissez le **[!UICONTROL type de verrouillage]** :

   * **[!UICONTROL Verrouillé]** - Avec ce paramètre, tous les composants enfants sont verrouillés par défaut. L’arborescence à gauche affiche l’icône _Lecture seule_ ( ![Icône Lecture seule](../assets/do-not-localize/icon-tree-lock.svg) ) en regard de tous les composants enfants.

   * **[!UICONTROL Modifiable]** - Avec ce paramètre, tous les composants enfants sont modifiables par défaut. L’arborescence à gauche n’affiche pas d’icônes en regard des composants enfants.

   ![Appliquer un verrouillage de contenu à un composant structurel](./assets/governance-template-structure-locking.png){width="800" zoomable="yes"}

## Définir le verrouillage d’un composant enfant

1. Sélectionnez le composant dans l’arborescence.

   Le panneau des propriétés situé à droite de la zone de travail affiche par défaut l’onglet _[!UICONTROL Paramètres]_.

1. Activez l’option **[!UICONTROL Utiliser un verrouillage spécifique]**.

1. Choisissez le type de gouvernance à appliquer :

   * **[!UICONTROL Modifiable]** : permet un contrôle éditorial complet du composant lors de la création d’un e-mail.
   * **[!UICONTROL Contenu modifiable uniquement]** - Permet aux auteurs d’e-mail de modifier le contenu, mais pas le composant lui-même.
   * **[!UICONTROL Verrouillé]** - Empêche toute modification du composant lors de la création d’un e-mail.

     Dans le cas d’un composant verrouillé, vous pouvez autoriser la suppression du composant lors de la création d’un e-mail en activant l’option **[!UICONTROL Autoriser la suppression]**.

   ![Appliquer un verrouillage de contenu à un composant enfant](./assets/governance-template-component-locking.png){width="800" zoomable="yes"}
