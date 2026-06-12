---
title: Verrouillage de contenu pour les modèles d’e-mail
description: Utilisez les paramètres de gouvernance dans le Prime B2B de Journey Optimizer pour verrouiller le contenu dans les modèles d’e-mail au niveau de la structure ou du composant, en contrôlant ce que les auteurs d’e-mail peuvent modifier.
badgeBeta: label="Beta" type="informative" tooltip="Cette fonctionnalité fait partie d’une version bêta limitée."
source-git-commit: 2f19137465c71f2292d37bea5786533b1df6e286
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---


# Verrouillage de contenu pour les modèles d’e-mail

Le verrouillage de contenu permet aux auteurs de modèles de définir des règles de gouvernance qui limitent les parties d&#39;un modèle d&#39;e-mail qui peuvent être modifiées lorsque le modèle est utilisé dans un parcours. Cela permet aux équipes de marque et de conformité de protéger les éléments de conception clés, tels que les en-têtes, les logos et le contenu légal, tout en permettant aux équipes marketing de personnaliser le message au sein de la structure approuvée.

>[!NOTE]
>
>Le verrouillage de contenu est une fonctionnalité de gouvernance au niveau de l’éditeur. Il contrôle ce que les auteurs et autrices peuvent modifier dans l’espace de conception d’e-mail, mais n’empêche pas les modifications apportées par l’API.

Seuls les utilisateurs disposant de l’autorisation **[!UICONTROL Gérer les modèles de contenu]** peuvent configurer les paramètres de gouvernance.

## Modes de gouvernance {#modes}

Lorsque vous activez la gouvernance sur un modèle, sélectionnez l’un des deux modes suivants :

| Mode | Description |
| ---- | ----------- |
| **[!UICONTROL Verrouillage de contenu]** | Verrouiller sélectivement des structures ou des composants spécifiques. Les zones déverrouillées restent modifiables par les auteurs. |
| **[!UICONTROL Lecture seule]** | Verrouillez le modèle entier. Les auteurs peuvent l’appliquer à un e-mail, mais ne peuvent pas modifier une partie de son contenu. |

## Activer la gouvernance {#enable}

1. Ouvrez le modèle dans l’espace de conception d’e-mail.
1. Dans le rail de droite, cliquez sur le composant **[!UICONTROL Corps]** pour le sélectionner.
1. Activez **[!UICONTROL Gouvernance]**.
1. Dans la liste déroulante Mode, sélectionnez **[!UICONTROL Verrouillage de contenu]** ou **[!UICONTROL Lecture seule]**.

Si vous avez sélectionné **[!UICONTROL Verrouillage de contenu]**, continuez en verrouillant des éléments individuels.

### Verrouiller une structure {#lock-structure}

1. Dans la zone de travail, sélectionnez la structure (mise en page des colonnes) à protéger.
1. Dans le rail de droite, activez le bouton (bascule) **[!UICONTROL Verrouiller la structure]**.

Tout le contenu imbriqué dans une structure verrouillée est automatiquement verrouillé. Pour permettre à un composant spécifique au sein d’une structure verrouillée de rester modifiable, sélectionnez le composant et activez **[!UICONTROL modifiable]** dans le rail de droite.

### Verrouiller un composant {#lock-component}

Dans une structure modifiable, vous pouvez verrouiller des composants de contenu individuels.

1. Sélectionnez le composant sur la zone de travail.
1. Dans le rail de droite, activez le bouton (bascule) **[!UICONTROL Verrouiller le contenu]**.

### Autoriser les ajouts de contenu {#allow-additions}

Lors de l’utilisation du mode **[!UICONTROL Verrouillage de contenu]**, vous pouvez permettre aux créateurs et créatrices d’ajouter du nouveau contenu au modèle tout en conservant les éléments verrouillés protégés :

1. Activez **[!UICONTROL Autoriser l’ajout de contenu]**.
1. Choisissez si les auteurs peuvent ajouter à la fois des structures et des composants de contenu, ou uniquement des composants de contenu.

## Identification des éléments verrouillés {#identify}

L’**[!UICONTROL arborescence de navigation]** dans le rail de gauche affiche des icônes de verrouillage et de crayon pour aider les auteurs à identifier rapidement ce qu’ils peuvent ou ne peuvent pas modifier :

* Une **icône de verrouillage** indique un élément verrouillé.
* Une **icône en forme de crayon** indique un élément modifiable.

Les éléments verrouillés sont indiqués visuellement dans la zone de travail lorsqu’un auteur ouvre le modèle.

## Considérations

Les paramètres de gouvernance sont enregistrés avec le modèle. Tout e-mail créé à partir d’un modèle régi hérite de sa configuration de verrouillage au moment de son application. La mise à jour des paramètres de gouvernance sur un modèle n’affecte pas les e-mails créés précédemment à partir de celui-ci.
