---
title: Création de contenu - personnalisation
description: Section réutilisée sur l’utilisation de la personnalisation pour la création de contenu
source-git-commit: 3791beb98068a56882bb0a96fbc6b192e85130bb
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# Création de contenu - personnalisation

Journey Optimizer B2B edition utilise une syntaxe simple intégrée qui vous permet de créer des expressions avec du contenu personnalisé placé entre des accolades doubles `{}`. Vous pouvez ajouter plusieurs expressions dans le même contenu ou champ sans restriction.

Exemples :

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

Lors du traitement du contenu, Journey Optimizer B2B edition remplace l’expression par les données contenues dans la base de données Experience Platform. Donc, le premier exemple devient _Bonjour John Doe_.

L’exemple suivant décrit les étapes de personnalisation du contenu à l’aide d’attributs de lead/compte et de jetons système.

1. Sélectionnez le composant de texte et cliquez sur l’icône _Ajouter une personnalisation_ dans la barre d’outils.

   ![Cliquez sur l’icône Personnaliser](../assets/content-design-shared/visual-designer-personalize-icon.png){width="600"}

   Cette action ouvre la boîte de dialogue _Modifier le Personalization_.

1. Cliquez sur **+** ou **...** pour ajouter un jeton à l’espace vide.

   ![Créer du texte personnalisé à l’aide de jetons](../assets/content-design-shared/visual-designer-personalize-dialog.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Enregistrer]**.
