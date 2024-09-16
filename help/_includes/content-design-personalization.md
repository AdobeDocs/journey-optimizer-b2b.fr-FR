---
title: Création de contenu - personnalisation
description: Section réutilisée sur l’utilisation de la personnalisation pour la création de contenu
source-git-commit: 0a9c05ac2ddd95e1fa5321f44f5cbe8cfa595007
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 2%

---

# Création de contenu - personnalisation

Journey Optimizer B2B Edition utilise une syntaxe simple intégrée qui vous permet de créer des expressions avec du contenu personnalisé encadré de doubles accolades `{}`. Vous pouvez ajouter plusieurs expressions dans le même contenu ou champ sans restriction.

Exemples :

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

Lors du traitement du message (email et SMS), Journey Optimizer B2B Edition remplace l&#39;expression par les données contenues dans la base de données Experience Platform. Ainsi, le premier exemple devient _Hello John Doe_.

L’exemple suivant décrit les étapes de personnalisation du contenu à l’aide des attributs de prospect/compte et des jetons système.

1. Sélectionnez le composant de texte et cliquez sur l’icône _Ajouter la personnalisation_ de la barre d’outils.

   ![Cliquez sur l’icône Personnaliser](../assets/content-design-shared/visual-designer-personalize-icon.png){width="600"}

   Cette action ouvre la boîte de dialogue _Modifier Personalization_.

1. Cliquez sur **+** ou **...** pour ajouter un jeton à l’espace vide.

   ![Créer du texte personnalisé à l’aide de jetons](../assets/content-design-shared/visual-designer-personalize-dialog.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Enregistrer]**.
