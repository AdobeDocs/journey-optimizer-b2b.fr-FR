---
title: Créateur de scripts
description: Utilisez Script Builder, un assistant optimisé par l’IA dans l’espace de conception d’e-mail, pour générer des scripts de personnalisation Handlebars et convertir des scripts Marketo Engage Velocity dans Journey Optimizer B2B edition.
feature: AI Assistant, Generative AI, Personalization, Email Authoring
role: User, Developer
badgeBeta: label="Beta" type="informative" tooltip="Cette fonctionnalité est actuellement en version bêta limitée"
autotag-review: '2026-07-27T16:18:02.498Z'
TQID: 'https://experienceleague.adobe.com/JWnXAAbCuZVLv4ZhWubpNsZ61xbYU7xtdOXkG9uoWis'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2: id: bd3c685c-6c92-4a4a-becb-535cc25215de
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 0004f8fba0c3d4ae89063418e4d3ef8fea22b0c3
workflow-type: tm+mt
source-wordcount: 1074
ht-degree: 2%

---

# Créateur de scripts

_Script Builder_ est un assistant optimisé par l’IA disponible dans l’espace de conception d’e-mail [!DNL Adobe Journey Optimizer B2B Edition]. Il permet aux marketeurs et aux développeurs d’e-mails de créer plus rapidement des scripts de personnalisation et de migrer depuis [!DNL Marketo Engage] en convertissant la logique de personnalisation existante en [!DNL Journey Optimizer B2B Edition] sans réécrire le code manuellement.

>[!AVAILABILITY]
>
>Script Builder est actuellement disponible pour certains clients sous la forme d’une version bêta limitée pour les e-mails dans les parcours de **_compte uniquement_**. La prise en charge des parcours de personne est prévue pour une version ultérieure. Pour obtenir l’accès, contactez votre représentant Adobe.

La création d’une personnalisation d’e-mail conditionnelle, comme le changement de blocs de langue par paramètre régional, la permutation de contenu par zone géographique ou persona, ou l’insertion de valeurs de profil dynamique ou d’objets personnalisés, nécessite la création d’expressions _Handlebars_. Si vous migrez depuis [!DNL Marketo Engage], vous avez le défi supplémentaire de réécrire les scripts _Velocity_ ligne par ligne. Script Builder résout les deux obstacles à partir d’une seule interface de conversation :

* Générez un nouveau script de personnalisation Handlebars à partir d’une description en langage clair.
* Collez un script [!DNL Marketo Engage] Velocity et convertissez-le en script Handlebars équivalent avec mappage automatique des jetons.
* Prévisualisez, modifiez, validez et enregistrez la sortie directement dans l’e-mail, sans copier et coller entre les outils.

## Instructions et restrictions

>[!IMPORTANT]
>
>L’accès des utilisateurs et utilisatrices au Script Builder est contrôlé par les mêmes autorisations que celles utilisées pour les autres fonctionnalités d’IA générative dans [!DNL Journey Optimizer B2B Edition]. Pour plus d’informations sur l’octroi des autorisations de fonctionnalités, voir [Activer l’accès de l’assistant AI](../ai-assistant/enable-ai-assistant-access.md).

Avant d’utiliser Script Builder, passez en revue les [instructions et restrictions](../ai-assistant/generative-ai-content.md#general-guidelines-and-limitations) qui s’appliquent aux fonctionnalités d’IA générative dans [!DNL Journey Optimizer B2B Edition]. [Accord utilisateur](https://www.adobe.com/fr/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"} l’acceptation est également requise avant de pouvoir utiliser les fonctionnalités d’IA.

Familiarisez-vous avec le [langage de modèle Handlebars](https://handlebarsjs.com/guide/){target="_blank"}, la [syntaxe de personnalisation](./personalization-syntax.md) et les [fonctions d’assistance](./personalization-helper-functions.md) prises en charge dans [!DNL Journey Optimizer B2B Edition]. Script Builder génère des barres de contrôle valides, mais comprendre la syntaxe vous permet de vérifier et de modifier la sortie en toute confiance.

## Ouvrir le générateur de scripts {#open-script-builder}

Script Builder est disponible à partir de l’[éditeur de personnalisation](./personalization.md) lorsque vous [créez du contenu d’e-mail](./email-authoring.md) pour un parcours de compte.

1. Dans l’espace de conception d’e-mail, sélectionnez le composant dans lequel vous souhaitez ajouter ou remplacer un script de personnalisation.

1. Pour ouvrir l’éditeur de personnalisation, cliquez sur l’icône _Ajouter une personnalisation_ ( ![icône Ajouter une personnalisation](../../assets/do-not-localize/icon-personalization-field.svg) ).

1. Dans l’éditeur, sélectionnez **[!UICONTROL Créateur de scripts]**.

   ![Éditeur Personalization - sélectionnez le créateur de scripts](./assets/personalization-script-builder-select.png){width="700" zoomable="yes"}

   >[!BEGINSHADEBOX]

   La première fois que vous accédez à Script Builder, consultez les [_[!UICONTROL Conditions d’utilisation de Generative AI ]_](https://www.adobe.com/fr/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"} et confirmez votre accord.

   ![Boîte de dialogue d’accord sur les conditions d’utilisation de Generative AI dans Script Builder](./assets/personalization-script-builder-gen-ai-terms.png){width="400"}

   >[!ENDSHADEBOX]

   Le panneau Script Builder s’ouvre avec une interface de conversation.

   ![Éditeur Personalization - Panneau Créateur de scripts](./assets/personalization-script-builder-welcome.png){width="700" zoomable="yes"}

1. Démarrez la conversation en fonction de ce que vous souhaitez faire :

   * [Générer un nouveau script](#generate-personalization-script)
   * [Convertir un script Velocity existant](#convert-marketo-velocity-script)

## Générer un script de personnalisation {#generate-personalization-script}

Utilisez le générateur de scripts pour créer un script de personnalisation Handlebars à partir d’une description en langage clair, sans écrire l’expression vous-même.

Script Builder comprend une bibliothèque de mappages qui résout [!DNL Marketo Engage] champs de prospect et de compte en leurs attributs de profil XDM [!DNL Journey Optimizer B2B Edition] équivalents, en fonction du mappage [champ XDM](../admin/xdm-field-management.md) défini pour votre organisation.

1. Dans l’interface de conversation du générateur de scripts, décrivez la logique de personnalisation de votre choix.

   Par exemple, décrivez l’attribut, l’objet personnalisé ou la condition qui détermine la variante de contenu à afficher.

1. Consultez le script Handlebars généré dans le volet d’aperçu.

1. Modifiez le script directement dans le volet d’aperçu si vous souhaitez affiner la logique ou le libellé.

1. Cliquez sur **[!UICONTROL Valider]** pour comparer le script au schéma [!DNL Journey Optimizer B2B Edition].

   La validation intercepte les erreurs de syntaxe et les références de jeton non résolues avant d’enregistrer le script, de sorte que la personnalisation rompue ne soit jamais publiée dans un e-mail en direct.

1. Cliquez sur **[!UICONTROL Enregistrer]** pour insérer le script directement à l’emplacement sélectionné dans l’e-mail.

## Conversion d’un script Marketo Engage Velocity {#convert-marketo-velocity-script}

Utilisez Script Builder pour migrer un script [!DNL Marketo Engage] Velocity existant vers un script Handlebars équivalent à des fins d’[!DNL Journey Optimizer B2B Edition].

1. Dans la conversation Script Builder, saisissez `Convert this` et collez le script Velocity à convertir.

   Script Builder analyse les éléments Velocity, fait correspondre les références de jeton aux attributs de profil XDM et génère le script Handlebars équivalent.

1. Consultez le [rapport de conversion](#review-conversion-report) et [résolvez les jetons qui nécessitent un mappage manuel](#resolve-tokens-without-mapping).

1. [Prévisualiser et valider](#preview-validate-script) le script généré, puis l’enregistrer directement dans l’e-mail.

### Éléments pris en charge par Velocity {#supported-velocity-constructs}

Script Builder convertit les éléments de flux de contrôle [!DNL Marketo Engage] Velocity suivants en barres de contrôle ou expressions de contenu conditionnel équivalentes :

| Construction de la vitesse | Handlebars ou équivalent de contenu conditionnel |
| ------------------- | --------------------------------------------- |
| `#if` / `#elseif` / `#else` | Handlebars `{{#if}}`, `{{else if}}` et `{{else}}` des assistants de bloc ou une règle [!DNL Journey Optimizer B2B Edition] [contenu conditionnel](./conditional-content.md) |
| `#set` | Une affectation de variable Handlebars dans le script généré |

Il traduit la logique conditionnelle basée sur les segments en règles [contenu conditionnel](./conditional-content.md) qui répliquent le comportement d’embranchement, y compris les e-mails avec de nombreux blocs de variantes de langue.

Si un concept Velocity n’a pas de barres de contrôle directes ou d’équivalent de contenu conditionnel, le créateur de scripts le signale dans le [rapport de conversion](#review-conversion-report) au lieu de générer une expression incomplète ou incorrecte.

### Consulter le rapport de conversion {#review-conversion-report}

Après chaque conversion, Script Builder fait apparaître un rapport structuré qui répertorie les éléments suivants :

* Jetons mappés avec succès.
* Jetons nécessitant une résolution manuelle.
* Velocity construit sans équivalent direct Handlebars.

Utilisez le rapport pour confirmer que la conversion est terminée avant de résoudre les jetons restants et d’enregistrer le script.

### Résoudre les jetons sans mappage {#resolve-tokens-without-mapping}

Pour les jetons qui ne se trouvent pas dans la bibliothèque de mappages, tels que les attributs de prospect personnalisés ou les objets de [!DNL Marketo Engage] personnalisés, Script Builder tente de résoudre un mappage dans l’ordre suivant :

1. Elle suggère un mappage probable en fonction des champs XDM disponibles et, pour les objets personnalisés, des [classes basées sur des modèles](./personalization.md#custom-datasets) configurées pour votre organisation, lorsqu’une correspondance fiable existe.

1. S’il ne peut pas suggérer de correspondance fiable, il vous demande le mappage correct dans le chat.

Lorsque vous confirmez un mappage pour un jeton qui ne se trouvait pas dans la bibliothèque, Script Builder vous demande si vous souhaitez vous souvenir de la décision. Si vous êtes d’accord, le mappage est mémorisé pour l’instance de [!DNL Marketo Engage] source, identifiée par son identifiant Munchkin, de sorte que le même jeton soit résolu automatiquement la prochaine fois que vous convertissez un script à partir de cette instance.

### Prévisualiser et valider le script {#preview-validate-script}

Avant de valider une conversion, Script Builder affiche un aperçu côte à côte du script Velocity d’origine et de la sortie Handlebars générée, avec prise en charge de la modification en ligne. Utilisez l’aperçu pour comparer les deux versions et effectuer les réglages directement dans le script généré.

Cliquez sur **[!UICONTROL Valider]** pour comparer les barres de contrôle générées au schéma [!DNL Journey Optimizer B2B Edition]. La validation s’exécute à nouveau lorsque vous enregistrez, de sorte que la personnalisation rompue ne soit jamais publiée dans un e-mail en direct.

Lorsque le résultat vous convient, cliquez sur **[!UICONTROL Enregistrer]** pour insérer le script directement à l’emplacement choisi dans l’e-mail.

<!--
### Save reusable conversion profiles {#save-reusable-conversion-profiles}

Save your field mappings and segment mappings as a reusable conversion profile so that your token schema does not need to be re-entered for each script or migration batch. Select a saved profile at the start of a conversion to apply its mappings automatically.

### Audit logs {#conversion-audit-logs}

Script Builder records an audit log for every conversion event, including which scripts were processed, which tokens were remapped, which tokens required manual intervention, and who approved the final output. Use the audit log to review migration activity across your organization.

-->
