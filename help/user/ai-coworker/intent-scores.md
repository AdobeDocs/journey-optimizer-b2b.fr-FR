---
title: Scores d’intention
description: Découvrez comment Journey Optimizer B2B edition calcule les scores d’intention à partir de l’engagement de la personne et de la pertinence du contenu, et comment les scores s’agrègent aux comptes.
feature: Dashboards, Intent, Intelligent Insights
role: User
autotag-review: '2026-09-11T14:56:32.307Z'
TQID: 'https://experienceleague.adobe.com/ajtUdNKafSoE1BC08imOpyflpDeAsXaQ3tdlbeYT6NU'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: f979fe0e-02fe-4599-b492-7b3df1d4e7dc
subfeature_v2:
  - id: e388c29d-df1e-4b47-ad27-1b14ae45776e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: 2da5c7bbbadde4bbb5df82a81398ecb970165da2
workflow-type: tm+mt
source-wordcount: 1445
ht-degree: 0%

---


# Scores d’intention {#intent-scores}

Une note d’intention mesure l’intérêt d’une personne ou d’un compte pour un mot-clé, un produit ou une catégorie de produits. Adobe Journey Optimizer B2B edition calcule le score à l’aide du machine learning qui mesure la similarité de signification, plutôt que des règles manuelles ou un système de points fixes. Chaque score est normalisé de 0 à 1, avec des nombres plus élevés indiquant une intention plus forte.

La pertinence du contenu s’actualise environ toutes les 12 heures et les scores d’intention sont recalculés quotidiennement. Les scores s’agrégent du mot-clé au produit et de la personne au compte. Les scores d’intention apparaissent dans le [tableau de bord intelligent](../dashboards/intelligent-dashboard.md) et dans les pages [détails du compte](../accounts/account-details.md), [_détails du groupe d’achat_ page](../buying-groups/buying-group-details.md) et [détails de la personne](../accounts/person-details.md).

![Visualisation des données intentionnelles](../data/assets/intent-data-visualization.png){width="700" zoomable="yes"}

Les sections suivantes expliquent les concepts de base de la notation d’intention, le processus continu qui maintient les notes à jour, la logique de calcul derrière chaque note et les paramètres que vous pouvez configurer.

## Concepts principaux {#core-concepts}

La détection d’intention mesure à quel point ce avec quoi une personne interagit correspond à vos produits et mots-clés, puis pondère cette similarité par le degré d’interaction de la personne. Trois entités composent ce modèle.

| Entité | Description |
|--------|--------------|
| Personne | Personne qui interagit avec votre contenu en ouvrant des e-mails, en visitant des pages web et en interagissant au fil du temps. |
| Contenu | E-mails et pages web avec lesquels une personne interagit. D’autres formats, tels que les webinaires et les campagnes, sont ajoutés au fil du temps. |
| Taxonomie | Votre structure de mots-clés, de produits et de catégories de produits qui représente les intérêts que vous souhaitez mesurer. |

### Taxonomie et mises à jour par défaut {#taxonomy}

Votre taxonomie, les mots-clés, produits et catégories en fonction desquels l’intention est mesurée, peut être utilisée sans configuration requise.

Vous pouvez vérifier et mettre à jour les mappages de taxonomie à tout moment sur la page _[!UICONTROL Mappage d’intention]_. Voir [Données d’intention](../admin/intent-data.md) pour le processus de configuration de la taxonomie.

### Pertinence du contenu {#content-relevance}

Journey Optimizer B2B edition traduit le contenu et la taxonomie en une représentation mathématique de leur signification, puis utilise un modèle de similarité pour mesurer à quel point ils s’alignent. Le contenu qui correspond étroitement à un mot-clé ou à un produit reçoit un score de pertinence élevé. Le contenu sans rapport reçoit un score faible.

Le modèle de similarité est pré-entraîné sur la langue générale, de sorte qu’aucune formation spécifique au client n’est nécessaire pour commencer.

## Processus de notation {#scoring-process}

Un processus continu transforme l’engagement brut en un score d’intention terminé. Chaque étape s’appuie sur ce que l’étape précédente a produit.

![Diagramme de flux de cinq étapes de notation : capture d’engagement, extraction de contenu, notation de pertinence, calcul d’intention quotidien et diffusion de la notation.](./assets/intent-scores-pipeline.svg){width="700"}

### Capture de l’engagement {#engagement-capture}

Chaque point de contact significatif d’une personne est capturé au fur et à mesure et lié au contenu impliqué.

* Les visites de page, les ouvertures d’e-mail et les clics, les envois de formulaire et les activités similaires sont enregistrées en tant qu’événements d’engagement.
* Chaque élément de contenu unique est également noté afin qu’il puisse être analysé à l’étape suivante.
* **Cadence d’actualisation** - Continue, au fur et à mesure que l’engagement se produit.

### Extraction de contenu {#content-extraction}

Avant que le contenu puisse être noté pour la pertinence, Journey Optimizer B2B edition extrait et lit son texte.

* Pour chaque nouvel élément de contenu, le système extrait le texte sous-jacent, qu’il réside sur une page web ou dans un e-mail.
* Certains types d’activité, tels que les remplissages de formulaire, comportent déjà leur propre contenu descriptif et ignorent cette étape.
* Le contenu qui ne peut pas être récupéré, tel qu’un lien rompu ou supprimé, est consigné et exclu à l’avenir.
* **Cadence d’actualisation** - À mesure que du nouveau contenu est découvert.

### Score de pertinence {#relevance-scoring}

Chaque ressource est mesurée par rapport à votre taxonomie, indépendamment de la personne qui l’a utilisée.

* Chaque e-mail et page web est analysé et comparé à vos mots-clés, produits et catégories à l’aide du modèle de similarité.
* Le résultat est un score de pertinence compris entre 0 et 1 pour cette ressource par rapport à chaque mot-clé ou produit associé.
* **Fréquence d’actualisation** - Toutes les 12 heures.

### Calcul de l’intention quotidienne {#daily-intent-calculation}

L’engagement et la pertinence du contenu se combinent en un score d’intention quotidien par personne, par mot-clé ou produit.

* Chaque type d’activité est associé à un poids configurable. Par exemple, un envoi de formulaire peut compter beaucoup plus qu’une page vue.
* L’activité récente importe plus que l’activité plus ancienne, les scores favorisent donc ce que quelqu’un a fait cette semaine par rapport à il y a un mois.
* Une mesure de confiance reflète la cohérence de l’engagement d’une personne, et pas seulement son volume.
* **Fréquence d’actualisation** - Tous les jours.

### Diffusion du score {#score-delivery}

Les scores quotidiens s’agrègent, reçoivent un niveau d’intention et sont diffusés à votre tableau de bord.

* Chaque score est balisé avec un niveau d’intention Élevé, Medium ou Faible.
* Les notes sont liées au compte correct afin que les équipes commerciales et marketing puissent voir le but au niveau de la personne et du compte.
* Seules les personnes dont le niveau d’intention a changé sont mises à jour, de sorte que le tableau de bord reflète la dernière modification significative.
* **Fréquence d’actualisation** - Tous les jours.

## Logique de calcul des scores {#score-calculation-logic}

Le calcul se compose de cinq couches, chacune ajoutant plus de contexte aux données brutes de pertinence et d’engagement.

### Pertinence du contenu par rapport à une rubrique {#relevance-to-topic}

Chaque élément de contenu et chaque sujet, c’est-à-dire un mot-clé, un produit ou une catégorie, est traduit en une représentation mathématique de sa signification. Un contenu ayant une signification similaire à un sujet se trouve plus près dans cette représentation. La pertinence est une mesure de proximité dans le sens, et non une correspondance exacte des mots.

### Pondération quotidienne de l’engagement {#engagement-weighting}

Un jour donné, le score d&#39;une personne est une moyenne pondérée de la pertinence de tout ce avec quoi elle s&#39;est engagée. Les activités à forte valeur ajoutée comptent davantage.

>[!BEGINSHADEBOX « Exemple »]

Une personne interagit avec trois éléments de contenu en une journée. Les pages vues ont un poids égal à un et les envois de formulaires un poids égal à cinq.

Comme leur envoi de formulaire compte cinq fois plus qu’une page vue, cela influence considérablement leur score quotidien, même s’ils ont interagi avec trois éléments au total.

Leur score quotidien pour ce sujet est d’environ 0,70 sur une échelle de 0 à 1.

>[!ENDSHADEBOX]

### Atténuation de la récence {#recency-decay}

Le score d’une personne reflète un mélange des derniers jours, l’activité récente étant beaucoup plus pondérée que l’activité plus ancienne. Après environ une semaine, une activité plus ancienne a un impact minimal, de sorte que le score reflète toujours l’intérêt actuel. En pratique, une visite aujourd’hui l’emporte sur une visite d’hier, qui l’emporte sur une visite d’il y a 10 jours.

### Normalisation des scores et niveaux d’intention {#normalization-intent-levels}

Chaque score ajusté est placé sur une échelle cohérente de 0 à 1 par rapport aux autres personnes de votre instance, puis regroupé dans un niveau d’intention.

| Score final | Niveau d’intention |
|-------------|--------------|
| Au-Dessus De 0,6 | Élevé |
| 0,2 à 0,6 | Support |
| Inférieur À 0,2 | Faible |

### Agrégation des scores {#score-aggregation}

Les scores individuels s’agrègent afin que vous puissiez examiner l’intention au niveau qui importe pour une décision, et pas seulement au niveau le plus granulaire.

* **Mot-clé en produit** - Scores calculés au niveau de l’agrégat mot-clé pour montrer l’intérêt pour un produit, et pas seulement pour un terme de recherche.
* **Personne à compte** - Un score de compte agrège tous les scores de ses clients, de sorte que vous puissiez voir quand l’ensemble d’un groupe d’achats affiche son intention.

![Diagramme affichant les scores des mots-clés agrégés aux scores de produit et les scores des personnes agrégés aux scores du compte.](./assets/intent-scores-aggregation.svg){width="500"}

Utilisez la vue au niveau du produit pour identifier les produits qui suscitent un intérêt croissant, plutôt que les mots-clés individuels qui génèrent les tendances. Utilisez la vue au niveau du compte pour voir quand un groupe d’achats entier montre un intérêt accru ensemble, plutôt que de réagir à une seule personne engagée.

## Paramètres configurables {#configurable-settings}

La plupart de la logique de notation est corrigée afin de conserver des résultats fiables et comparables au fil du temps. Un administrateur de produit peut personnaliser deux paramètres pour répondre à vos besoins :

* **Poids des activités** - Pour appliquer un impact plus important aux scores d’intention, augmentez le poids des activités à forte valeur, telles qu’une demande de démonstration ou une visite de page de tarification. Pour exclure entièrement une activité, définissez son poids sur zéro, ce qui est utile pour des actions telles que les désabonnements qui ne contribuent pas à l’intention. Les poids d’activité pour le calcul de l’intention utilisent le même modèle de pondération qui oriente également les [scores d’engagement](../buying-groups/engagement-scores.md). Voir [_Configurer la pondération du score d’engagement_](../admin/engagement-score-weighting.md) pour modifier les poids des activités.

* **Mappages de taxonomie** - Les mots-clés, produits et catégories sur lesquels la notation est basée peuvent être utilisés. Passez-les en revue et mettez-les à jour à tout moment sur la page _[!UICONTROL Mappage d’intention]_. Voir [_Données d’intention_](../admin/intent-data.md) pour le processus de configuration.

Tous les autres éléments, notamment la pertinence du contenu, la baisse d’activité et les seuils _Élevé_, _Medium_ et _Faible_, sont corrigés afin que les scores restent cohérents et comparables au fil du temps.

## Principes de notation {#scoring-principles}

Gardez les principes suivants à l’esprit lorsque vous examinez des scores d’intention et que vous agissez en conséquence.

### Score piloté par le modèle {#model-driven}

Il n’existe aucune affectation de point ni règle de mot-clé à gérer. Le modèle apprend la pertinence directement à partir de votre contenu et de votre taxonomie, ce qui maintient la cohérence de la notation à mesure que votre bibliothèque de contenu se développe et change, sans configuration continue.

### Score relatif {#relative-scoring}

Un score reflète le rang d’une personne ou d’un compte parmi vos autres contacts aujourd’hui et le système le recalcule quotidiennement en fonction de la population actuelle. Utilisez des scores pour comparer des personnes et des comptes au sein de votre propre instance, plutôt que comme un nombre fixe et universel. Les notes ne sont pas directement comparables d&#39;une entreprise à l&#39;autre.

### Actualisation des données {#data-freshness}

La pertinence du contenu s’actualise environ toutes les 12 heures au fur et à mesure que du nouveau contenu apparaît. Les scores d’intention sont recalculés une fois par jour, de sorte que le tableau de bord reflète l’activité de la journée précédente chaque matin.
