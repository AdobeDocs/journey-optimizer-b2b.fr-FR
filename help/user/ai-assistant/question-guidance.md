---
title: Conseils sur les questions pour l’assistant IA
description: Espace réservé
feature: AI Assistant
level: Beginner
source-git-commit: 5ca03b12fd459c64b245ad95e60a382c355922f9
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 1%

---

# Conseils sur les questions pour l’assistant AI dans Journey Optimizer B2B edition

Consultez les exemples de questions suivants pour interroger l’assistant AI dans Journey Optimizer B2B edition. Ces informations comprennent également des conseils sur la manière de formuler vos questions pour obtenir des réponses optimales de la part de l’assistant d’IA.

## Questions basées sur des objectifs

Les exemples de questions suivants sont regroupés en fonction des objectifs que vous pouvez atteindre lors de l’utilisation de l’assistant AI :

| Objectif | Description | Exemple |
| --- | --- | --- |
| Apprendre les concepts et poursuivre les workflows | En tant qu’utilisateur débutant, vous pouvez utiliser l’assistant AI pour apprendre les concepts de Real-Time CDP et de Adobe Journey Optimizer B2B edition, et vous intégrer à des produits et fonctionnalités que vous ne connaissez pas. <br>En tant qu’utilisateur expérimenté, vous pouvez utiliser l’assistant AI pour résoudre un cas de figure susceptible de bloquer votre workflow. | <li>Racontez-moi quelques cas d’utilisation pour Real-Time CDP. <li>Expliquez-moi le concept de groupe d&#39;achat. |
| Dépannage | Utilisez l’assistant AI pour savoir comment déboguer les erreurs de base que vous pouvez rencontrer dans votre workflow. | <li>A quoi correspond cette erreur &lt;MESSAGE_ERREUR> ? <li>Pourquoi ne puis-je pas supprimer l’audience nommée « ... » ? |
| Hygiène des sandbox | Utilisez l’assistant AI pour identifier les doublons ou les objets inutilisés afin de gérer efficacement votre sandbox. | <li>Pouvez-vous m’afficher des audiences de compte similaires ? <li>Existe-t-il des schémas auxquels aucun jeu de données n’est associé ? |
| Analyse des valeurs | Utilisez l’assistant AI pour identifier les objets de données les plus utilisés et évaluer les indicateurs de performance ou trouver les objets de données les plus précieux. | <li>Combien de comptes se trouvent dans notre définition de segment « ... » ? <li>Quand les audiences ont-elles été activées vers la destination Audiences Experience Cloud ? |
| Recherche | Utilisez l’assistant AI pour rechercher les objets B2B edition Experience Platform et Adobe Journey Optimizer pris en charge, tels que les audiences de compte, les jeux de données, les destinations, les schémas, les sources, les parcours de compte, les modèles de groupe d’achats et les centres d’intérêt des solutions | <li>Répertoriez les audiences dont le nom contient « Luma » et qui ont été utilisées dans les parcours de compte. <li>Quels sont les attributs du schéma XDM « Luma : actions personnalisées » ? |
| Analyse d&#39;impact | Utilisez l’assistant AI pour identifier les objets de données qui ont été utilisés dans certains workflows afin de pouvoir évaluer l’impact de toute modification. | <li>Quelles audiences de compte utilisent `workEmail.address` dans le schéma « Personne B2B » ? <li>Dans quels jeux de données les `jobTitle` ... sont-ils stockés ? |

## Formulation de vos questions

Vous devez formuler vos questions à l’assistant AI avec clarté et contexte pour obtenir une réponse aussi précise que possible. Consultez la liste suivante de conseils pour savoir comment poser une question claire avec du contexte :

* Exposez votre tâche et/ou question de façon concise.
* Évitez le langage ambigu ou une syntaxe trop complexe pour faciliter la compréhension.
* Fournissez un contexte pertinent concernant votre tâche et/ou question, car le contexte peut aider l’assistant d’IA à générer des réponses plus pertinentes.

Les tableaux suivants présentent quelques bonnes pratiques que vous pouvez suivre lors de l’utilisation de l’assistant AI :

| Faire | Exemple |
| --- | --- |
| <li>Soyez précis quant à l’objet ou aux informations que vous souhaitez récupérer ou analyser. <li>Essayez de placer les noms des objets de données entre guillemets. <li>Si vous ne connaissez qu’une partie du nom de l’objet, vous pouvez également la spécifier dans la question. | <li>Quels jeux de données utilisent le schéma « Compte B2B » ? <li>Montrez-moi les audiences activées dont le nom contient « Compte ». Classez-les par nombre de membres. |
| <li>Évitez toute ambiguïté et utilisez un langage clair. <li>Utilisez une terminologie précise pour garantir une meilleure clarté dans votre requête. <li>Lorsque vous posez des questions concernant Adobe Experience Platform et Adobe Journey Optimizer B2B edition, utilisez une terminologie spécifique à Experience Platform ou Adobe Journey Optimizer B2B edition pour améliorer la pertinence des réponses. | <li>Combien de membres ai-je dans « Mon audience de compte » ? <li>Combien de parcours de compte utilisent l’audience de compte « Mon audience de compte » ? |
| <li>Fournissez un contexte ou spécifiez un critère pour filtrer vos résultats. <li>Utilisez un critère de filtre dans les questions pour limiter le volume de données dans la réponse. | <li>Afficher les audiences de compte qui n’ont pas été activées et qui ont été créées il y a plus de 6 mois et qui n’ont jamais été modifiées. <li>Afficher les parcours de compte publiés au cours des 7 derniers jours et qui utilisent une audience de compte qui compte plus de 1 000 membres |

| Ne pas | Exemple |
| --- | --- |
| Utilisez un langage vague ou ambigu. | <li>Me donner des informations sur les jeux de données. <li>Que fait parcours x ? <li>Combien d’utilisateurs ai-je dans « Audience ACME » ? <li>Afficher les segments. <li>Attributs de liste. |
| Effectuer des demandes incomplètes | <li>« Luma - Jeu De Données De Fidélité » |
| Supposons des connaissances sans contextes. | <li>Audiences des 6 derniers mois. <li>Créez une requête pour moi. <li>Créer un parcours pour moi |
| Formulez des requêtes trop complexes. | <li>Fournissez une analyse complète de la parenté des données sur tous les objets et leurs dépendances. |
| Omettre les critères ou les paramètres. | <li>Afficher les jeux de données. |

## Exemples de questions non prises en charge

La liste suivante inclut des exemples de questions que l’assistant AI dans Journey Optimizer B2B edition ne prend actuellement pas en charge :

* Quelles audiences de compte utilisent le champ workEmail.address du groupe de champs ... dans sa condition ? 
* Montrez-moi le nombre de parcours actifs utilisant des audiences de compte d’une taille supérieure à 10 000, comprise entre 5 000 et 10 000, entre 1 000 et 5 000, et inférieure à 1 000, dans un visuel de répartition
* Qui a effectué la dernière mise à jour du parcours de compte x ?
* Combien de parcours actifs ajoutent des membres du groupe d&#39;achat pour l&#39;intérêt de la solution x ?
* Quels parcours actifs ajoutent des membres du groupe d&#39;achat pour l&#39;intérêt de la solution x ?
* Quel est le titre de décideur le plus courant des modèles de groupe d’achat ?
* Qui sont les décideurs pour l’achat du modèle de groupe x ?

## Étapes suivantes

Pour plus d’informations sur l’utilisation des fonctionnalités de l’assistant AI au cours de vos workflows, voir [Utiliser l’assistant AI dans Journey Optimizer B2B edition](./use-ai-assistant.md).
