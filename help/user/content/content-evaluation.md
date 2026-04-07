---
title: Score du contenu
description: Évaluez le contenu des e-mails avec le score d’alignement de la marque - validez les couleurs, les polices, les logos et le style d’écriture par rapport aux directives de la marque dans Journey Optimizer B2B edition.
badge: label="Beta" type="Informative"
feature: Content, Brand Identity
role: User
level: Beginner, Intermediate
exl-id: 686d5ce0-c597-48e1-a51f-e91e95a942d5
source-git-commit: 37e4a7976d716f24edf2c2e92cbfa4c149aa66ec
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 9%

---

# Notation du contenu {#content-scoring}

L’évaluation et la notation du contenu vous permettent de créer, de réviser et de gérer du contenu qui respecte les directives [définies dans la marque sélectionnée](./brands-manage-create.md#brand-definitions) et les normes de qualité générales. L’exécution d’une évaluation garantit la cohérence du ton, du message et de l’identité visuelle de vos campagnes par e-mail, tout en servant de contrôle qualité avant la mise en ligne de votre contenu.

>[!AVAILABILITY]
>
>Un [contrat d’utilisateur](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"} est requis avant de pouvoir utiliser les fonctionnalités optimisées par l’IA dans Adobe Journey Optimizer B2B edition. Pour en savoir plus, contactez votre représentant Adobe.
>
>Consultez [Autorisations liées aux marques](./brands-overview.md#brand-related-permissions) pour plus d’informations sur la manière dont les administrateurs et administratrices de produit peuvent activer ces fonctionnalités.

## Exécuter une évaluation

1. Après avoir créé le contenu de l’e-mail, cliquez sur l’icône _Alignement des marques_ ( ![Icône d’alignement des marques](../assets/do-not-localize/icon-brand-compliance.svg) ) à droite pour ouvrir le panneau de droite _Alignement des marques_ dans l’espace de conception d’e-mail.

   La [ marque par défaut ](./brands-manage-create.md#default-brand) est automatiquement sélectionnée.

   ![Accéder aux outils d’alignement des marques](./assets/brands-alignment-sidebar.png){width="600" zoomable="yes"}

   Vous pouvez cliquer sur l’icône _Plein écran_ ( ![Icône Plein écran](../assets/do-not-localize/icon-full-screen.svg) ) en haut du panneau pour afficher les outils d’alignement de la marque en mode plein écran.

1. Si nécessaire, cliquez sur la flèche du menu **[!UICONTROL Marque]** ( ![Flèche vers le bas](../assets/do-not-localize/icon-down-menu.svg) ) pour choisir une autre marque publiée.

1. Cliquez sur **[!UICONTROL Évaluer le score]** pour noter l’alignement du contenu avec la marque sélectionnée.

   Le système évalue le contenu en fonction des directives de la marque sélectionnée et affiche le score obtenu.

   ![Scores d’évaluation dans le panneau de droite](./assets/brands-alignment-evaluation.png){width="600" zoomable="yes"}

## Score d’alignement de la marque {#brand-score}

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_score_overview"
>title="Sélection de la marque"
>abstract="Sélectionnez votre marque pour vous assurer que votre contenu est conçu conformément à ses directives et standards spécifiques et à son identité propre, en préservant la cohérence et l’intégrité de la marque."

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_score"
>title="Score d’alignement de la marque"
>abstract="Le score d’alignement de votre marque mesure dans quelle mesure votre contenu respecte les directives de la marque afin d’assurer la cohérence des couleurs, des polices, du logo, des images et du style d’écriture."

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_colors_score"
>title="Score des couleurs"
>abstract="Score des couleurs"

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_fonts_score"
>title="Score des polices"
>abstract="Score des polices"

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_logos_score"
>title="Score des logos"
>abstract="Score des logos"

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement disponible en version bêta publique.

Une fois votre marque bien définie et publiée, évaluez son score d’alignement directement dans l’espace de conception d’e-mail pour vous assurer que le contenu correspond à vos directives de marque :

Le score est calculé en fonction des violations identifiées dans le contenu de l’e-mail évalué :

* 100 = Parfait - Aucune violation trouvée
* 80-99 = Bon - Violations mineures uniquement
* 60-79 = Juste - Quelques violations importantes
* En dessous de 60 = médiocre - Les violations majeures doivent être examinées

Vous pouvez consulter les résultats de l’évaluation plus en détail pour vous aider à identifier les violations et à améliorer les scores d’alignement des catégories (_Élevé_, _Medium_ et _Faible_), puis consulter les détails.

Dans le champ **[!UICONTROL Écriture de style]** ou **[!UICONTROL Contenu visuel]**, cliquez sur la flèche _Développer_ ( ![Flèche Développer](../assets/do-not-localize/icon-expand-right.svg) ) pour afficher les détails de l’évaluation.

![Détails de l’évaluation de l’alignement des marques](./assets/brands-alignment-evaluation-details.png){width="600" zoomable="yes"}

Cliquez sur l’icône _Plein écran_ ( ![Icône Plein écran pour obtenir des informations détaillées](../assets/do-not-localize/icon-full-screen.svg) ) pour obtenir une vue détaillée de chaque score insight.

Sélectionnez une directive marquée pour afficher les commentaires et suggestions spécifiques.

![Détails d’évaluation de l’alignement des marques en mode plein écran](./assets/brands-alignment-evaluation-details-full-screen.png){width="700" zoomable="yes"}

Vous pouvez apporter des modifications au contenu d’et cliquer sur **[!UICONTROL Réévaluer le score]** pour exécuter une autre évaluation et rechercher un résultat amélioré.

## Score de qualité du contenu {#quality-score}

>[!CONTEXTUALHELP]
>id="ajo-b2b_quality_score_overview"
>title="Qualité du contenu"
>abstract="Évaluez la qualité générale du contenu pour identifier les problèmes potentiels de lisibilité, de cohésion du contenu et d’efficacité. L’évaluation de la qualité est indépendante des directives de votre marque."

>[!NOTE]
>
>L’évaluation de la qualité du contenu est indépendante des directives de la marque. Même si une marque est sélectionnée, ses directives ne sont pas appliquées au contrôle qualité. La sélection de la marque n’est pertinente que pour la notation de l’alignement de la marque.

Outre l’alignement de la marque, vous pouvez évaluer la qualité générale du contenu afin d’identifier les problèmes potentiels de lisibilité, de cohésion du contenu et d’efficacité, indépendamment des directives de votre marque.

Faites défiler jusqu’à la section **[!UICONTROL Qualité du contenu]** pour consulter les informations sur la qualité et les recommandations.

![ Évaluation de la qualité du contenu ](./assets/content-scoring-quality-insights.png){width="600" zoomable="yes"}

Sélectionnez un élément avec indicateur pour afficher des commentaires spécifiques et des suggestions d’amélioration exploitables. Les scores sont basés sur les catégories suivantes :

* **[!UICONTROL Efficacité de CTA]** : évalue dans quelle mesure votre call-to-action motive les lecteurs à effectuer l’action souhaitée.
* **[!UICONTROL Objet]** : évalue la clarté, la pertinence et la qualité pour attirer l’attention afin d’encourager les ouvertures d’e-mails.
* **[!UICONTROL Lisibilité]** : mesure à quel point votre contenu est facile à comprendre et attrayant pour les lecteurs et lectrices.
* **[!UICONTROL Vérification anti-spam]** : identifie les déclencheurs de spam courants susceptibles d&#39;avoir un impact sur la délivrabilité.
* **[!UICONTROL Cohésion du contenu]** : garantit le bon déroulement de votre contenu et le respect des rubriques.
* **[!UICONTROL Relecture]** : vérifie les problèmes d’orthographe, de grammaire et de clarté.

Cliquez sur l’icône _Plein écran_ ( ![Icône Plein écran pour obtenir des informations détaillées](../assets/do-not-localize/icon-full-screen.svg) ) pour obtenir une vue détaillée de votre score de qualité.

![Affichage plein écran de l’évaluation de la qualité du contenu](./assets/content-scoring-quality-full-screen.png){width="700" zoomable="yes"}

En fonction des recommandations, vous pouvez modifier votre contenu pour améliorer la lisibilité, la cohésion du contenu et la qualité globale. Cliquez sur **[!UICONTROL Réévaluer le score]** après avoir apporté des modifications pour actualiser le score de qualité.
