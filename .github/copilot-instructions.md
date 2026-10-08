---
source-git-commit: 1b4d8ad802265b537eb09439cfe34b97a3e61448
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%
---
# Instructions relatives au référentiel du pilote GitHub

Lorsque les directives générales des instructions Claude copiées entrent en conflit avec des conventions ou des instructions spécifiques à une tâche du référentiel, suivez les instructions spécifiques au référentiel ou à la tâche.

## But

Utilisez ces instructions de référentiel pour effectuer le travail de documentation dans ce référentiel. Veillez à ce que les modifications soient concises, techniquement exactes et conformes aux normes de documentation d’Adobe Experience League.

## Écrire dans le style de documentation du référentiel

- Privilégiez un langage clair, direct et axé sur l’utilisateur.
- Faites des phrases courtes et lisibles.
- Préférez un langage spécifique et exploitable au marketing ou au texte de remplissage.
- Évitez les sections standard telles que les « Rubriques connexes », les « FAQ » ou les blocs de résumé génériques, sauf si elles sont explicitement requises.
- Utilisez des liens croisés contextuels au lieu de blocs de navigation de fin de page.
- N’ajoutez pas de liste de références ni de section « Rubriques connexes » à la fin d’un article. Introduisez les liens connexes lorsqu’ils sont pertinents dans le contenu et expliquez comment chaque destination est liée à la rubrique actuelle.
- N’utilisez pas de langage spatial tel que « ci-dessous » ou « au-dessus » pour décrire l’ordre des documents ; utilisez plutôt « suivant », « précédent » ou « dans la section suivante ».

## Règles de dénomination pour la documentation externe

- N’utilisez pas d’acronymes de produit Adobe dans la documentation externe.
- La première mention des noms de produits Adobe doit utiliser le nom complet du produit, y compris « Adobe » le cas échéant.
- Utilisez des balises DNL pour les noms de produits dans le contenu, par exemple :
  - [!DNL Adobe Experience Platform]
  - [!DNL Adobe Journey Optimizer B2B Edition]
  - [!DNL Experience Platform]
  - [!DNL Journey Optimizer B2B Edition]
- Remplacez les références basées uniquement sur des acronymes telles que « AEP » et « AJO B2B » par leurs noms complets de produits dans la documentation destinée aux utilisateurs.
- Lorsqu’un produit est introduit pour la première fois, écrivez son nom complet. Les mentions ultérieures peuvent utiliser le nom de produit plus court sans l’acronyme et conserver la balise DNL lorsque le nom du produit apparaît dans le texte de l’interface utilisateur ou de la documentation.
- Appliquez ces termes de manière cohérente au titre de la page, au premier paragraphe, ainsi qu’aux libellés ou liens croisés visibles par les lecteurs et lectrices.

## Conventions de dénomination spécifiques au référentiel

- Utilisez « Adobe Journey Optimizer B2B Edition » pour le nom du produit dans la documentation destinée aux utilisateurs.
- Utilisez « Adobe Experience Platform » pour le nom de la plateforme dans la documentation destinée aux utilisateurs.
- Utilisez le nom du produit dans sa forme complète lors de la première mention, puis conservez des références courtes et cohérentes par la suite.
- Pour les références de jeux de données, conservez les noms et identifiants des jeux de données tels qu’ils apparaissent dans le contrat source, même s’ils incluent des préfixes hérités tels que `AJOB2B-`.

## Instructions de balisage et de formatage

- Écrivez un Markdown compatible avec GitHub valide.
- Gardez les en-têtes concis et descriptifs.
- Utilisez des tableaux uniquement lorsqu’ils aident les lecteurs à analyser les détails techniques.
- Utilisez des liens relatifs pour les références repo-locales.
- Gardez les blocs de code et les chemins de champ exacts et copiables.
- Évitez les références de produit redondantes dans les en-têtes si le titre de la page les indique déjà.

## Liste de contrôle de validation avant de terminer

- Assurez-vous qu’il n’existe aucun acronyme pour les produits Adobe dans le contenu destiné aux utilisateurs.
- Assurez-vous que les premières mentions utilisent le nom complet du produit.
- Assurez-vous que les noms de produit sont balisés avec [!DNL ...] si le style de référentiel l’exige.
- Veillez à ce que le document évite les problèmes de formulation standard et spatiale.
- Assurez-vous que le contenu technique reste précis et que les liens croisés contextuels sont conservés.
