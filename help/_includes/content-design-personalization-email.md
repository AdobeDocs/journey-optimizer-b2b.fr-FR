---
title: Création de contenu - personnalisation
description: Section réutilisée sur l’utilisation de la personnalisation pour la création de contenu
source-git-commit: fee5bddcce11b3035da6ab93b18bcc7006b4b554
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Création de contenu - personnalisation

Journey Optimizer B2B edition utilise une syntaxe simple intégrée qui vous permet de créer des expressions avec du contenu personnalisé placé entre des accolades `{{}}`. Vous pouvez ajouter plusieurs expressions dans le même contenu ou champ sans restriction.

Par exemple, vous pouvez ajouter une expression de personnalisation en tant que `Hello {{lead.firstName}} {{lead.lastName}}`. Lors du traitement du contenu, Journey Optimizer B2B edition remplace l’expression par les données contenues dans la base de données Experience Platform. Donc, le premier exemple devient _Bonjour John Doe_.

Consultez [Personnalisation de contenu](../user/content/personalization.md) pour obtenir des informations plus complètes sur l’utilisation des outils de personnalisation dans Journey Optimizer B2B edition.

>[!NOTE]
>
>Journey Optimizer B2B edition suit la syntaxe _casse mixte_ pour les jetons de personnalisation dans les e-mails afin de correspondre aux autres applications Adobe Experience Platform pour une expérience cohérente. Ce format de jeton est entièrement compatible avec le [&#x200B; langage de modèle Handlebars &#x200B;](https://handlebarsjs.com/guide/#what-is-handlebars){target="_blank"}. Tous les jetons ajoutés avant cette modification sont automatiquement mis à jour.

L’exemple suivant décrit les étapes de personnalisation du contenu à l’aide de jetons de personne et de système. Elle reflète les modifications disponibles pour les environnements Journey Optimizer B2B edition configurés sur l’[architecture simplifiée](../user/simplified-architecture.md).

1. Sélectionnez le composant de texte et cliquez sur l’icône _Ajouter une personnalisation_ ( ![Ajouter une icône de personnalisation](../assets/do-not-localize/icon-personalization-field.svg) ) dans la barre d’outils.

   ![Cliquez sur l’icône Personnaliser](../assets/content-design-shared/visual-designer-personalize-icon.png){width="600"}

   Cette action ouvre la boîte de dialogue _Modifier le Personalization_.

1. Ajoutez un jeton en cliquant sur le symbole plus ( **+** ) situé en regard de celui-ci.

   Si vous souhaitez ajouter un jeton avec un texte de remplacement (texte par défaut qui s’affiche lorsque ce champ n’est pas disponible pour un prospect), cliquez sur l’icône _Plus_ ( **...** ) et choisissez **[!UICONTROL Insérer avec un texte de remplacement]**.

   ![Créer du texte personnalisé à l’aide de jetons](../assets/content-design-shared/visual-designer-personalize-dialog-handlebar.png){width="700" zoomable="yes"}

1. Ajoutez des jetons supplémentaires ou tout autre texte statique que vous souhaitez inclure.

1. Cliquez sur **[!UICONTROL Enregistrer]**

   Le script de personnalisation s’affiche dans l’espace de conception visuelle. Vous pouvez la sélectionner pour apporter des modifications si nécessaire.

   ![Sélectionner le script de personnalisation](../assets/content-design-shared/visual-designer-select-personalization-script.png){width="600"}
