---
title: Création de fragments
description: 'Créez des fragments de contenu réutilisables avec des outils de conception visuelle : ajoutez la structure, les ressources, la personnalisation, le contenu conditionnel et le suivi des URL liées pour les e-mails et les modèles dans le Prime B2B de Journey Optimizer.'
badgeBeta: label="Beta" type="informative" tooltip="Cette fonctionnalité fait partie d’une version bêta limitée."
autotag-review: '2026-07-13T16:38:09.506Z'
TQID: 'https://experienceleague.adobe.com/Zn5L6Bc3x8SuGyjOPDdTWI-oxrrhk06a2f8ZvX2SN4s'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: aed878b8-11d0-487c-828b-d23b2051ec37id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2: id: e1663313-7961-4100-bea9-fa9f4edf8493id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 5206ed7bc0ce24e65700da28b023d76c68cb6419
workflow-type: tm+mt
source-wordcount: 215
ht-degree: 4%

---

# Création de fragments

Après avoir [créé un fragment](./fragments.md#create-fragments), utilisez l’espace de conception visuelle pour créer les composants de structure et de contenu dans votre fragment.

## Ajouter la structure et le contenu {#design-fragment}

{{$include /help/_includes/content-design-components-prime.md}}

## Ajout de ressources {#add-assets}

Dans l’espace de conception visuelle, sélectionnez l’icône __ ( ![icône Assets](../../assets/do-not-localize/icon-assets-me.svg) ) dans la barre de navigation de gauche pour parcourir et sélectionner des ressources d’image dans la bibliothèque de ressources d’[!DNL Journey Optimizer B2B Prime].

Pour connaître les étapes de sélection, de remplacement ou de chargement de ressources d’image, consultez [Utilisation de ressources pour la création de contenu](./digital-asset-management.md#assets-authoring).

## Parcourir les calques, paramètres et styles {#navigate-layers-settings-styles}

{{$include /help/_includes/content-design-navigation.md}}

## Personnaliser le contenu {#personalize-content}

[!DNL Journey Optimizer B2B Prime] utilise la syntaxe Handlebars pour la personnalisation. Les jetons sont remplacés au moment de l’envoi par des valeurs provenant des données de profil de chaque destinataire.

_Pour ajouter de la personnalisation :_

1. Sélectionnez le composant de texte et cliquez sur l’icône _Ajouter une personnalisation_ ( ![Icône Personnaliser](../../user/assets/do-not-localize/icon-personalize.svg) ) dans la barre d’outils.
1. Dans la boîte de dialogue de personnalisation, parcourez l’arborescence du schéma à gauche et sélectionnez un attribut de profil. L’éditeur insère l’expression Handlebars correspondante, par exemple, `{{profile.firstName}}`.
1. Ajoutez une valeur de secours pour gérer les données manquantes, si nécessaire, par exemple, `{{profile.firstName | default: "there"}}`.
1. Cliquez sur **[!UICONTROL Confirmer]** ou **[!UICONTROL Insérer]**. L’expression apparaît en ligne dans le champ.

Pour plus d’informations sur les outils et la syntaxe de l’éditeur d’expression, voir [Éditeur ](./personalization-expressions.md).

## Modifier le tracking des URL liées {#edit-linked-url-tracking}

{{$include /help/_includes/content-design-links.md}}
