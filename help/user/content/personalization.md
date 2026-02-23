---
title: Personnalisation du contenu
description: Personnalisez les e-mails B2B à l’aide des jetons de compte, de personne et système dans Journey Optimizer B2B edition. Découvrez comment utiliser l’éditeur de personnalisation et la syntaxe .
feature: Personalization, Content Design Tools, Email Authoring
topic: Personalization
role: User, Developer
level: Intermediate
keywords: expression, éditeur, commencer, personnalisation
exl-id: 60bf2e06-8d6e-4cc4-8aff-5c5ca11f05ab
source-git-commit: 10e02b821609c48b82ea0248501daa60de6daa12
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 1%

---

# Personnalisation du contenu {#add-personalization}

>[!CONTEXTUALHELP]
>id="aj-b2b_personalization"
>title="Personnaliser les expériences de contenu"
>abstract="Utilisez **Adobe Journey Optimizer B2B edition** pour adapter vos messages à chaque destinataire spécifique en exploitant les données et informations dont vous disposez à son sujet. Il peut s’agir de son prénom, de son secteur d’activité, de son titre, etc."

[!DNL Adobe Journey Optimizer B2B Edition] fonctionnalités de personnalisation vous permettent d’adapter vos e-mails à chaque destinataire spécifique en exploitant les données et informations dont vous disposez à son sujet. Il peut s’agir de son prénom, de son secteur d’activité, de son titre, etc.

À l’aide de l’_éditeur de personnalisation_, vous pouvez sélectionner, organiser, personnaliser et valider toutes les données afin de personnaliser votre contenu. Utilisez divers outils, tels que des fonctions d’assistance, pour adapter les messages. L’éditeur utilise une syntaxe de personnalisation intégrée basée sur _Handlebars_, où les expressions sont construites avec du contenu placé entre des accolades doubles `{{}}`.

Lors du traitement du message, Journey Optimizer B2B edition remplace l’expression par les données contenues dans le jeu de données Adobe Experience Platform et les valeurs du système local. Par exemple, `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` devient `Hello John Doe` de manière dynamique.

Cette syntaxe vous permet de personnaliser des messages dans plusieurs champs, notamment l’objet des e-mails, le corps des messages et les informations sur l’expéditeur.

## Jetons Personalization

Dans [!DNL Journey Optimizer B2B Edition], vous pouvez créer le contenu dynamique de votre e-mail à l’aide de jetons de personnalisation :

* **Jetons de compte** - Ces jetons sont basés sur les attributs du compte, tels que _nom du compte_, _secteur_ et _nombre d’employés_. Utilisez ces jetons pour renseigner les données d’attribut gérées par le schéma **_Détails du compte professionnel XDM_** défini dans Adobe Experience Platform.

* **Jetons de personne** - Ces jetons sont basés sur les attributs de l’entrepreneur, tels que _prénom_, _fonction_ et _nom de la société_. Utilisez ces jetons pour renseigner les données d’attribut gérées par le schéma **_Détails professionnels XDM_** défini dans Adobe Experience Platform.

* **Jetons système** - Ces jetons sont basés sur les valeurs des champs système, telles que _date_, _heure_ et _lien de désabonnement_.

* **Mes jetons** (lorsqu’ils sont définis pour le parcours) - [jetons personnalisés définis pour le parcours ](./personalization-my-tokens.md) où réside l’e-mail.

>[!NOTE]
>
>Pour en savoir plus sur les schémas XDM, consultez la documentation du modèle de données Adobe Experience Platform (XDM) [](https://experienceleague.adobe.com/fr/docs/experience-platform/xdm/home){target="_blank"}.

## Éditeur de personnalisation

L’éditeur de personnalisation est disponible dans tous les contextes où vous devez définir une personnalisation du contenu d’un e-mail. Dans l’éditeur, vous pouvez sélectionner, organiser, personnaliser et valider toutes les données afin de personnaliser le contenu.

Ajoutez une personnalisation à n’importe quel champ ou composant de contenu en cliquant sur l’icône _Ajouter une personnalisation_ ( ![icône Ajouter une personnalisation](../../assets/do-not-localize/icon-personalization-field.svg) ).

![Éditeur Personalization](./assets/personalization-editor.png){width="800" zoomable="yes"}

>[!NOTE]
>
>Les informations suivantes sur l’éditeur de personnalisation reflètent les modifications qui sont disponibles pour les environnements [!DNL Journey Optimizer B2B Edition] configurés sur l’[architecture simplifiée](../simplified-architecture.md).

### Jetons et fonctions d’assistance

Pour utiliser un jeton de personnalisation ou une fonction d’assistance, localisez-le dans le volet de navigation de gauche, puis cliquez sur **+** pour l’ajouter à l’expression.

Cliquez sur l’icône _Plus de menu_ ( **...** ) (en regard de l’icône _Ajouter_ ( **+** ) pour afficher plus de détails sur chaque attribut et ajouter les attributs les plus fréquemment utilisés aux _favoris_. Les attributs ajoutés aux favoris sont accessibles à partir du menu **[!UICONTROL Favoris]** dans le volet de navigation de gauche de l’éditeur.

![Éditeur Personalization - Jeton Menu Plus ](./assets/personalization-editor-token-more-menu.png){width="800" zoomable="yes"}

<!-- >>[!NOTE]
>
>By default, the attributes list shows only populated attributes. To display all attributes, click the _Settings_ icon above the search field and toggle off the **[!UICONTROL Show only populated attributes]** option.
-->
Vous pouvez également définir une chaîne de texte de remplacement par défaut qui s’affiche si un attribut de profil de type chaîne est vide. Cliquez sur l’icône _Plus_ ( **...** ) de l’attribut et sélectionnez **[!UICONTROL Insérer avec un texte de remplacement]**. Saisissez le texte à afficher lorsque la valeur de l’attribut est vide pour un profil, puis cliquez sur **[!UICONTROL Ajouter]**.

Il est recommandé de valider l’expression avant de l’insérer dans le contenu. Cliquez sur **[!UICONTROL Valider]** en bas de l’éditeur pour vérifier la syntaxe et vous assurer qu’il n’y a aucune erreur.

![Code validé par l’éditeur Personalization](./assets/personalization-editor-validated.png){width="500"}

Une fois l’expression terminée et sans erreur, cliquez sur **[!UICONTROL Enregistrer]**.

### Jeux de données personnalisés

[!BADGE Beta]{type=Informative tooltip="Fonctionnalité Beta"}

Vous pouvez utiliser des schémas relationnels pour la personnalisation des e-mails. Les objets personnalisés sont définis dans _schémas relationnels_ et un administrateur de produit peut [configurer des champs de schéma relationnel](../admin/xdm-field-management.md#relational-schemas) dans [!DNL Journey Optimizer B2B Edition]. Ces champs sont accessibles dans l’éditeur de personnalisation. Seuls les objets personnalisés ayant une relation un-à-plusieurs (1:M) avec des personnes ou un compte sont disponibles.

>[!IMPORTANT]
>
>Avant d’utiliser des objets personnalisés pour la personnalisation par script, veillez à consulter et à comprendre le [langage de modèle Handlebars](https://handlebarsjs.com/guide/), [syntaxe de personnalisation](./personalization-syntax.md) et les fonctions d’assistance [ intégrées](./personalization-helper-functions.md).

Lorsque vous définissez une personnalisation à l’aide d’objets personnalisés, vous pouvez accéder à toutes les variables des objets accessibles par script dans les **[!UICONTROL jetons Personalization]** (personne/prospect, compte, système et Mes jetons) et les **[!UICONTROL objets personnalisés]** (schémas relationnels). Lorsque des objets personnalisés sont sélectionnés, vous pouvez afficher les champs en cliquant sur le dossier d’objets personnalisés. Cliquez sur **+** pour chaque champ que vous souhaitez ajouter à l’expression.

![Éditeur Personalization - Classes basées sur des modèles - ajoutez des champs d’objet personnalisés](./assets/personalization-editor-custom-object-fields.png){width="700" zoomable="yes"}
