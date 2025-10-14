---
title: Score d’alignement des marques
description: Évaluez le contenu des e-mails avec le score d’alignement de la marque - validez les couleurs, les polices, les logos et le style d’écriture par rapport aux directives de la marque dans Journey Optimizer B2B edition.
badge: label="Beta" type="Informative"
feature: Content, Brand Identity
hide: true
hidefromtoc: true
role: User
level: Beginner, Intermediate
exl-id: 686d5ce0-c597-48e1-a51f-e91e95a942d5
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 23%

---

# Score d’alignement de la marque {#brand-score}

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_score_overview"
>title="Sélection de la marque"
>abstract="Sélectionnez votre marque pour vous assurer que votre contenu est conçu conformément à ses directives et standards spécifiques et à son identité propre, en préservant la cohérence et l’intégrité de la marque."

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_score"
>title="Score d’alignement de la marque"
>abstract="Le score d’alignement de votre marque mesure la concordance de votre contenu avec vos directives de marque, en assurant la cohérence des couleurs, des polices, du logo, des images et du style d’écriture."

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_colors"
>title="Score des couleurs"
>abstract="Score des couleurs"

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_fonts"
>title="Score des polices"
>abstract="Score des polices"

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_logos"
>title="Score des logos"
>abstract="Score des logos"

L’évaluation et les scores d’alignement de la marque vous permettent de créer, de réviser et de gérer du contenu qui respecte les directives [définies dans la marque sélectionnée](./brands-manage-create.md#brand-definitions). Elle garantit la cohérence du ton, des messages et de l’identité visuelle dans vos campagnes par e-mail, tout en servant de contrôle qualité avant la mise en ligne de votre contenu.

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement disponible en version bêta privée et une disponibilité progressive est prévue pour tous les clients dans les prochaines versions.
>
>Un [contrat d’utilisateur](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"} est requis avant de pouvoir utiliser les fonctionnalités optimisées par l’IA dans Adobe Journey Optimizer B2B edition. Pour plus d’informations, contactez votre représentant ou représentante Adobe.
>
>Consultez [Autorisations liées aux marques](./brands-overview.md#brand-related-permissions) pour plus d’informations sur la manière dont les administrateurs et administratrices de produit peuvent activer ces fonctionnalités.

## Valider l’alignement de votre marque

Une fois votre marque bien définie et publiée, évaluez son score d’alignement directement dans l’espace de conception d’e-mail pour vous assurer que le contenu correspond à vos directives de marque :

1. Après avoir créé le contenu de l’e-mail, cliquez sur l’icône _Alignement des marques_ ( ![Icône d’alignement des marques](../assets/do-not-localize/icon-brand-compliance.svg) ) à droite pour ouvrir le panneau de droite _Alignement des marques_ dans l’espace de conception d’e-mail.

   La [&#x200B; marque par défaut &#x200B;](./brands-manage-create.md#default-brand) est automatiquement sélectionnée.

   ![Accéder aux outils d’alignement des marques](./assets/brands-alignment-sidebar.png){width="600" zoomable="yes"}

   Vous pouvez cliquer sur l’icône _Plein écran_ ( ![Icône Plein écran](../assets/do-not-localize/icon-full-screen.svg) ) en haut du panneau pour afficher les outils d’alignement de la marque en mode plein écran.

1. Si nécessaire, cliquez sur la flèche du menu **[!UICONTROL Marque]** ( ![Flèche vers le bas](../assets/do-not-localize/icon-down-menu.svg) ) pour choisir une autre marque publiée.

1. Cliquez sur **[!UICONTROL Évaluer le score]** pour noter l’alignement du contenu avec la marque sélectionnée.

   Le système évalue le contenu en fonction des directives de la marque sélectionnée et affiche le score obtenu.

   ![Score d’évaluation de l’alignement des marques](./assets/brands-alignment-evaluation.png){width="600" zoomable="yes"}

## Vérifier l’évaluation

Le score est calculé en fonction des violations identifiées dans le contenu de l’e-mail évalué :

* 100 = Parfait - Aucune violation trouvée
* 80-99 = Bon - Violations mineures uniquement
* 60-79 = Juste - Quelques violations importantes
* En dessous de 60 = médiocre - Les violations majeures doivent être examinées

Vous pouvez consulter les résultats de l’évaluation plus en détail pour vous aider à identifier les violations et à améliorer les scores d’alignement des catégories (_Élevé_, _Medium_ et _Faible_), puis consulter les détails. Dans le champ **[!UICONTROL Écriture de style]** ou **[!UICONTROL Contenu visuel]**, cliquez sur la flèche _Développer_ ( ![Flèche Développer](../assets/do-not-localize/icon-expand-right.svg) ) pour afficher les détails de l’évaluation.

![Détails de l’évaluation de l’alignement des marques](./assets/brands-alignment-evaluation-details.png){width="600" zoomable="yes"}

Sélectionnez une directive marquée pour afficher les commentaires et suggestions spécifiques.

Vous pouvez apporter des modifications au contenu d’et cliquer sur **[!UICONTROL Réévaluer le score]** pour exécuter une autre évaluation et rechercher un résultat amélioré.
