---
title: Création de contenu - personnalisation
description: Section réutilisée sur l’utilisation de la personnalisation pour la création de contenu
source-git-commit: d67f44419e09693ec93fd4db7982ec59c672b633
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 1%

---

# Création de contenu - personnalisation

Journey Optimizer B2B edition utilise une syntaxe simple intégrée qui vous permet de créer des expressions avec du contenu personnalisé placé entre des accolades `{}`. Vous pouvez ajouter plusieurs expressions dans le même contenu ou champ sans restriction.

Exemples :

* `Hello {{lead.firstName}} {{lead.lastName}}`
* `Hello {%= lead.mktoName ?: "Marketer" %}`

>[!NOTE]
>
>Journey Optimizer B2B edition suit désormais la syntaxe _casse mixte_ pour les jetons de personnalisation dans les e-mails, afin de correspondre aux autres applications Adobe Experience Platform pour une expérience cohérente. Ce format de jeton est entièrement compatible avec le [ langage de modèle Handlebars ](https://handlebarsjs.com/guide/#what-is-handlebars){target="_blank"}. Tous les jetons ajoutés avant cette modification sont automatiquement mis à jour.

Lors du traitement du contenu, Journey Optimizer B2B edition remplace l’expression par les données contenues dans la base de données Experience Platform. Donc, le premier exemple devient _Bonjour John Doe_.

L’exemple suivant décrit les étapes de personnalisation du contenu à l’aide d’attributs de lead/compte et de jetons système.

1. Sélectionnez le composant de texte et cliquez sur l’icône _Ajouter une personnalisation_ dans la barre d’outils.

   ![Cliquez sur l’icône Personnaliser](../assets/content-design-shared/visual-designer-personalize-icon.png){width="600"}

   Cette action ouvre la boîte de dialogue _Modifier le Personalization_.

1. Ajoutez un jeton en cliquant sur le symbole plus ( **+** ) situé en regard de celui-ci.

   Si vous souhaitez ajouter un jeton avec un texte de remplacement (texte par défaut qui s’affiche lorsque ce champ n’est pas disponible pour un prospect), cliquez sur l’icône _Plus_ ( **...** ) et choisissez **[!UICONTROL Insérer avec un texte de remplacement]**.

   ![Créer du texte personnalisé à l’aide de jetons](../assets/content-design-shared/visual-designer-personalize-dialog-handlebar.png){width="700" zoomable="yes"}

1. Ajoutez des jetons supplémentaires ou tout autre texte statique que vous souhaitez inclure.

1. Cliquez sur **[!UICONTROL Enregistrer]**.

   Le script de personnalisation s’affiche dans l’espace de conception visuelle. Vous pouvez la sélectionner pour apporter des modifications si nécessaire.

   ![Sélectionner le script de personnalisation](../assets/content-design-shared/visual-designer-select-personalization-script.png){width="600"}
