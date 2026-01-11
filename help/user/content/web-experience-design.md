---
title: Conception d’expérience web
description: Concevez des expériences web avec des éditeurs visuels et non visuels. Ajoutez des modifications, gérez les mises à jour de contenu, activez le suivi des clics et personnalisez le contenu dans Journey Optimizer B2B edition.
feature: Content Design Tools, Channels
role: User
badgeBeta: label="Beta" type="informative" tooltip="Cette fonctionnalité est actuellement en version bêta limitée"
source-git-commit: d01f4c14f72ebf78b10e4fc6691df42707bedb47
workflow-type: tm+mt
source-wordcount: '2333'
ht-degree: 4%

---

# Conception d’expériences web

Après avoir [créé une expérience web](./web-experiences.md#create-a-web-experience), utilisez l’espace de conception de contenu pour définir les modifications à appliquer à vos pages web.

>[!BEGINSHADEBOX]

**Conditions préalables**

Avant de pouvoir concevoir des expériences web, assurez-vous que les exigences suivantes sont remplies :

* Un administrateur de produit a configuré un ou plusieurs canaux web pour définir les URL (pages) à inclure pour une expérience web. Pour plus d’informations, voir [Configurations du canal web](../admin/configure-channels-web.md).

* [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/js-overview) (`alloy.js`) est implémenté pour l&#39;identification des visiteurs et la diffusion de contenu sur votre site Web. Adobe Experience Platform Web SDK version 2.16 ou ultérieure est requis.

* Vous disposez des [autorisations](../admin/user-management.md#b2b-product-permissions) nécessaires pour créer et gérer des expériences web dans un parcours :
   * _[!UICONTROL Campagnes]_ > _[!UICONTROL Gérer les campagnes]_ - Obligatoire pour ajouter ou mettre à jour un nœud d’action de personnalisation web.
   * _[!UICONTROL Campagnes]_ > _[!UICONTROL Afficher les campagnes]_ - Obligatoire pour afficher les détails des nœuds d’une action de personnalisation web.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>Avant de concevoir une expérience web, assurez-vous que l’extension de navigateur Visual Editing Helper de Adobe Experience Cloud est installée pour votre navigateur web. Cette extension est nécessaire pour ouvrir, créer et prévisualiser vos pages web de manière fiable dans l’espace de conception d’expérience web de Journey Optimizer B2B edition.<br/>
>
>Google Chrome et Microsoft Edge sont actuellement les seuls navigateurs qui prennent en charge l’extension et la création d’expériences web dans Journey Optimizer B2B edition. Pour plus d’informations, voir [Installation de l’extension Visual Editing Helper](./web-experiences.md#install-the-visual-editing-helper-extension).

## Éditeurs d’expérience web

Journey Optimizer B2B edition fournit deux types d’éditeurs pour la conception de modifications web :

| Éditeur | Description | Idéal pour |
| ------ | ----------- | -------- |
| [éditeur visuel](#visual-editor) | Un éditeur WYSIWYG (_What You See Is What You Get_) qui affiche votre site web et vous permet de sélectionner et de modifier directement des éléments. Elle nécessite l’extension [ Visual Editing Helper ](./web-experiences.md#install-the-visual-editing-helper-extension) dans le navigateur web Google Chrome ou Microsoft Edge. | Apporter des modifications visuelles aux éléments de page visibles, tels que le texte, les images, les boutons et les bannières. |
| [ Éditeur non visuel ](#non-visual-editor) | Éditeur basé sur le code pour appliquer des modifications qui ne peuvent pas être apportées via l’éditeur visuel. | Ciblage des éléments difficiles à sélectionner visuellement, application de modifications CSS avancées ou modification d’éléments masqués. |

Dans les propriétés de l’expérience web, utilisez l’option **[!UICONTROL Éditeur visuel]** pour déterminer le type d’éditeur. Activez l’option pour utiliser l’éditeur visuel ou désactivez-la pour utiliser l’éditeur non visuel.

![Option éditeur visuel activée](./assets/web-experience-design-visual-editor-option.png){width="400"}

## Éditeur visuel {#visual-editor}

>[!CONTEXTUALHELP]
>id="ajo-b2b_web_experience_browse"
>title="Utiliser le mode de navigation"
>abstract="Dans ce mode, vous pouvez accéder à la page exacte que vous souhaitez personnaliser pour la configuration de canal web sélectionnée."

L’éditeur visuel charge les pages web dans un iframe, où vous pouvez sélectionner des éléments et appliquer des modifications directement dans l’aperçu de la page. Pour utiliser l’éditeur visuel afin de concevoir votre expérience web, procédez comme suit :

1. Une fois l’onglet _[!UICONTROL Contenu]_ affiché dans la page de détails de l’expérience web, cliquez sur **[!UICONTROL Modifier l’expérience web]** dans le panneau de droite.

   L’éditeur visuel charge votre site web en fonction de la configuration du canal web.

   ![Éditeur visuel de l’expérience web](./assets/web-experience-design-visual-editor.png){width="800" zoomable="yes"}

1. Si nécessaire, cliquez sur **[!UICONTROL Parcourir]** en haut à droite et utilisez la barre de navigation du site pour charger la page que vous souhaitez modifier.

   Vous pouvez également saisir l’URL de la page dans le champ en haut.

   >[!NOTE]
   >
   >Assurez-vous que la page chargée correspond aux modèles d’URL définis dans votre configuration de canal web. Cliquez sur **[!UICONTROL Afficher les détails de la configuration]** en haut à droite pour afficher les règles de correspondance d’URL ou de page pour la configuration de canal web sélectionnée.

   ![Mode de navigation dans l’éditeur visuel](./assets/web-experience-design-visual-editor-browse.png){width="700" zoomable="yes"}

   <!-- If the web channel configuration is defined using page matching rules, use the left and right arrows to sequence through the matched pages -- right now these buttons don't do anything -->

   Cliquez sur **[!UICONTROL Conception]** en haut à droite pour charger la page dans l’espace de conception.

1. Pour définir la manière dont vous souhaitez que la page affichée soit modifiée pour l’expérience web, vous pouvez :

   * [Insérez de nouveaux composants](#insert-new-components) (séparateur, HTML, image, en-tête, paragraphe ou lien) dans la page pour l’expérience web.

   * Sélectionnez un élément existant de la page, tel qu’une image, un bouton, un paragraphe, un texte, un conteneur, un en-tête ou un lien, et modifiez-le [ l’expérience web](#modify-elements).

   * [Ajouter le suivi des clics](#click-tracking-for-web-experiences) pour les éléments permettant de mesurer l’engagement et de recueillir des informations.

1. Répétez l’étape 2 pour charger d’autres pages que vous souhaitez inclure dans l’expérience web et répétez l’étape 3 pour définir les modifications de page.

1. [Passez en revue vos modifications](#manage-modifications) et effectuez les ajustements nécessaires.

1. Une fois vos modifications terminées, cliquez sur la flèche de gauche au-dessus de l’éditeur pour revenir aux propriétés de l’expérience web.

### Modification des éléments

Cliquez sur un élément de la page affichée pour le sélectionner. Une bordure bleue indique l’élément sélectionné et une barre d’outils contextuelle s’affiche avec les options de modification.

![Sélectionner un élément à modifier](./assets/web-experience-design-select-element.png){width="700" zoomable="yes"}

Les options de la barre d’outils dépendent du type de composant sélectionné :

| Action | Description |
| ------ | ----------- |
| **[!UICONTROL Options de texte]** | Modifiez la classe de l’élément de texte ou le style du texte de l’élément sélectionné. |
| **[!UICONTROL Choisir une image]** | Remplacez la source de l’image ou ajoutez une image à l’élément. |
| **[!UICONTROL Modifier le lien / Ajouter un lien]** | Modifier ou ajouter une URL de lien. |
| **[!UICONTROL Organiser]** | Déplace l’élément sélectionné vers l’arrière ou vers l’avant dans l’affichage. |
| **[!UICONTROL Ajouter une personnalisation]** | Insérez une personnalisation. |
| **[!UICONTROL Élément de suivi des clics]** | Ajoutez le suivi des clics pour l’élément. |
| **[!UICONTROL Supprimer]** | Supprimer l’élément sélectionné de la page. |

Pour un élément sélectionné, les propriétés du panneau de droite changent pour refléter les styles et actions disponibles. Cliquez sur une icône d’action en haut du panneau pour dupliquer, suivre un clic, supprimer ou masquer l’élément sélectionné.

![cliquez sur une icône d’action pour l’élément sélectionné](./assets/web-experience-design-visual-editor-element-properties-icons.png){width="300"}

+++Éléments de texte

1. Sélectionnez un élément de texte sur la page.

1. Saisissez le nouveau contenu textuel ou sélectionnez une chaîne de texte et saisissez le texte de remplacement.

1. (Facultatif) Utilisez les [options de mise en forme de texte](./content-components.md#text) telles que le gras, l’italique et l’alignement.

1. Cliquez en dehors de l’élément de texte pour appliquer la modification.

Pour plus d’informations sur les options de style de texte des composants de texte, voir [Composants de contenu](./content-components.md#text).

+++

+++Éléments d’image

1. Sélectionnez un élément image sur la page.

1. Cliquez sur l’icône _[!UICONTROL Choisir une image]_ dans la barre d’outils contextuelle ou dans le panneau de droite.

1. Recherchez et sélectionnez une image dans votre bibliothèque de ressources.

1. Utilisez les [options de style d’image](./content-components.md#image) dans le panneau de droite selon vos besoins.

+++

+++Éléments de bouton

1. Sélectionnez un élément de bouton sur la page.

1. (Facultatif) Saisissez le nouveau texte du bouton ou sélectionnez la chaîne de texte et saisissez le texte de remplacement.

   Vous pouvez utiliser la personnalisation pour modifier le texte du bouton à l’aide des données provenant des profils de compte ou de personne.

1. Utilisez les [options de style de bouton](./content-components.md#button) dans le panneau de droite selon vos besoins.

+++

+++ Éléments de conteneur

1. Sélectionnez un élément de conteneur sur la page.

1. Utilisez les [options de style de conteneur](./content-components.md#container) dans le panneau de droite selon vos besoins.

+++

### Insérer de nouveaux composants

Lorsque vous sélectionnez l’icône **+** dans le volet de navigation de gauche Conception de l’éditeur visuel, vous pouvez ajouter les types de composants suivants à la page en tant que modification de l’expérience web :

* **[!UICONTROL Diviseur]** - Utilisez ce composant pour insérer une ligne de séparation afin d’organiser la disposition et le contenu de votre e-mail. Vous pouvez ajuster les attributs de style, tels que la couleur, le style et la hauteur des lignes à partir des propriétés du panneau de droite. Voir [Diviseur](./content-components.md#divider) dans _Composants de contenu_ pour plus d’informations.
* **[!UICONTROL HTML]** - Utilisez ce composant pour copier-coller le code HTML dans la structure existante. Il permet de créer des composants modulaires HTML gratuits pour réutiliser du contenu externe. Voir [HTML](./content-components.md#html) dans _Composants de contenu_ pour plus d’informations.
* **[!UICONTROL Image]** - Utilisez ce composant pour insérer un fichier image dans la page. Vous pouvez ajuster les attributs de style, tels que la largeur et la hauteur, à partir des propriétés du panneau de droite. Voir [Image](./content-components.md#image) dans _Composants de contenu_ pour plus d’informations.
* **[!UICONTROL En-tête]** - Utilisez ce composant pour insérer du texte de classe d’en-tête. Vous pouvez ajuster les attributs de style, tels que la couleur, le style, la police et la taille du texte, à partir des propriétés du panneau de droite. Voir [Texte](./content-components.md#text) dans _Composants de contenu_ pour plus d’informations.
* **[!UICONTROL Paragraphe]** - Utilisez ce composant pour insérer un élément de texte standard. Vous pouvez ajuster les attributs de style, tels que la couleur, le style, la police et la taille du texte, à partir des propriétés du panneau de droite. Voir [Texte](./content-components.md#text) dans _Composants de contenu_ pour plus d’informations.
* **[!UICONTROL Lien]** - Utilisez ce composant pour insérer un lien textuel autonome vers une URL spécifiée. Vous pouvez ajuster les attributs de style, tels que la couleur, le style, l’alignement et la taille du texte, à partir des propriétés du panneau de droite.

Sélectionnez un type de composant à gauche, puis passez la souris sur un élément adjacent à l’endroit où vous souhaitez l’ajouter.

![Interface de l’éditeur visuel - nouveau composant](./assets/web-experience-design-visual-editor-insert-component.png){width="800" zoomable="yes"}

Cliquez sur l’un des boutons affichés pour placer le composant :

* ***[!UICONTROL Insérer avant]** - Insérez le composant avant l’élément sélectionné.
* ***[!UICONTROL Insérer après]** - Insérez le composant après l’élément sélectionné.

Pour désélectionner un type de composant à insérer, cliquez sur **[!UICONTROL Échap]** dans la bannière contextuelle bleue affichée en haut de la page.

## Éditeur non visuel {#non-visual-editor}

Utilisez l’éditeur non visuel lorsque vous devez apporter des modifications qui ne peuvent pas être facilement effectuées dans l’éditeur visuel. Cette approche basée sur le code vous permet de contrôler précisément le ciblage et la modification des éléments. Pour utiliser l’éditeur non visuel afin de concevoir votre expérience web, procédez comme suit :

1. Une fois l’onglet _[!UICONTROL Contenu]_ affiché dans la page Détails de l’expérience web, cliquez sur **[!UICONTROL Ajouter une modification]** dans le panneau de droite.

   L’éditeur non visuel charge une page en fonction de la configuration du canal web.

   ![Interface de l’éditeur non visuel](./assets/web-experience-design-non-visual-editor.png){width="800" zoomable="yes"}

1. Définissez la première modification que vous souhaitez apporter.

   Le panneau de gauche affiche une liste des modifications existantes (le cas échéant). Cliquez sur **[!UICONTROL Ajouter]** pour définir une nouvelle modification. Si aucune modification n’est définie, le panneau affiche par défaut les options _[!UICONTROL Ajouter une modification]_.

   * Choisissez le **[!UICONTROL Type de modification]** :

     | Type | Description |
     | ---- | ----------- |
     | [**[!UICONTROL  Sélecteur CSS ]**](#css-selector-modifications) | Ciblez des éléments à l’aide d’une chaîne de sélecteur CSS. |
     | [**[!UICONTROL  Page ]**](#page-modifications) | Insérez des HTML, CSS ou JavaScript personnalisés dans des éléments de niveau page, tels que `<head>` ou `<body>`. |

   * Configurez les paramètres de modification en fonction du type :

      * **[!UICONTROL Sélecteur CSS]** - Saisissez un sélecteur CSS valide pour cibler des éléments spécifiques.
      * **[!UICONTROL Type d’action]** - Sélectionnez l’action à effectuer (modifier, masquer, supprimer, insérer, remplacer).
      * **[!UICONTROL Contenu]** - Fournissez le contenu ou le style à appliquer.

1. Cliquez sur **[!UICONTROL Enregistrer]** pour appliquer la modification.

### Modifications du sélecteur CSS

Les modifications du sélecteur CSS vous permettent de cibler des éléments précisément en utilisant la syntaxe standard du sélecteur CSS.

1. Choisissez **[!UICONTROL Sélecteur CSS]** comme type de modification.

1. Saisissez le sélecteur dans le champ **[!UICONTROL Sélecteur d’éléments CSS]**.

<!-- This field helps you find and select the HTML elements (or nodes in the DOM tree). -->

    **Exemples de sélecteurs :**
    
    | Sélecteur | Cibles |
    | -------- | ------- |
    | `#hero-banner` | Élément avec ID « hero-banner » |
    | `.cta-button` | Tous les éléments de la classe « cta-button » |
    | `en-tête et a` | Liens dans la navigation, dans l’en-tête |
    | `[data-offer=« premium »]` | Éléments avec un attribut de données spécifique |

1. Choisissez un **[!UICONTROL Type d’action]** et spécifiez les informations/contenus requis.

   * **[!UICONTROL Définir le contenu]** - Saisissez le texte dans le champ **[!UICONTROL Contenu]** de l’élément identifié par la valeur _[!UICONTROL Sélecteur d’éléments CSS]_.

   * **[!UICONTROL Définir l’attribut]** - Spécifiez un attribut à associer au sélecteur CSS actuel afin que l’élément puisse être identifié par cet attribut. Saisissez un nom dans le champ **[!UICONTROL Nom de l’attribut]** et une valeur dans le champ **[!UICONTROL Contenu]**. Si l’attribut existe déjà, la valeur est mise à jour ; dans le cas contraire, un nouvel attribut est ajouté avec le nom et la valeur spécifiés.

   ![Modification du sélecteur CSS de l’éditeur non visuel](./assets/web-experience-design-non-visual-editor-modification-css-selector.png){width="800" zoomable="yes"}

1. (Facultatif) Cliquez sur **[!UICONTROL Ajouter une personnalisation]** et utilisez le [éditeur de personnalisation](./personalization.md#personalization-editor) pour créer une personnalisation personnalisée du contenu.

### Modifications de page

Vous pouvez ajouter du code personnalisé à l’aide du type de modification Page `<head>` . L’élément `<head>` est un conteneur pour les métadonnées et est placé entre la balise `<html>` et la balise `<body>`. Dans ce cas, le code n’attend pas les événements de chargement de page ou de corps, il est exécuté au début du chargement de la page.

L’élément `<head>` est généralement utilisé pour ajouter du code JavaScript ou CSS en haut de la page. Les sélecteurs pour les actions visuelles suivantes dépendent des éléments HTML ajoutés dans cet onglet.

>[!NOTE]
>
>Le code personnalisé s’exécute dans le navigateur du visiteur. Assurez-vous que votre code est sécurisé, testé et n’a pas d’impact négatif sur les performances des pages ou sur l’expérience utilisateur.

1. Choisissez **[!UICONTROL Page`<head>`]** comme type de modification.

1. Ajoutez votre code personnalisé dans la zone **[!UICONTROL Contenu]**.

   >[!CAUTION]
   >
   >Vous pouvez uniquement ajouter les éléments `<script>` et `<style>` à la section `<head>`. L’ajout de balises `<div>` et d’autres éléments peut entraîner le remplissage des éléments `<head>` restants dans le `<body>`.

   ![Modification de l’en-tête de page de l’éditeur non visuel](./assets/web-experience-design-non-visual-editor-modification-page-head.png){width="800" zoomable="yes"}

1. (Facultatif) Cliquez sur **[!UICONTROL Ajouter une personnalisation]** et utilisez le [éditeur de personnalisation](./personalization.md#personalization-editor) pour créer une personnalisation personnalisée du contenu.

## Gérer les modifications {#manage-modifications}

>[!CONTEXTUALHELP]
>id="ajo-b2b_web_experience_modifications"
>title="Gérer facilement toutes les modifications"
>abstract="Ce volet vous permet de parcourir et de gérer tous les réglages et ajouts définis pour la page web."

Toutes les modifications que vous créez sont suivies et peuvent être gérées à partir du panneau **[!UICONTROL Modifications]** de l’éditeur visuel et de l’éditeur non visuel. Cliquez sur l’icône _[!UICONTROL Modifications]_ <!-- ( ![Modifications icon](../assets/do-not-localize/icon-web-exp-modifications.svg) ) --> dans la barre d’outils de gauche pour afficher toutes les modifications.

Chaque enregistrement de modification comprend :

* L’élément cible ou le sélecteur
* Type de modification (modification, masquage ou insertion, par exemple)
* Un aperçu de la modification

![Panneau Modifications](./assets/web-experience-design-modifications-list.png){width="500" zoomable="yes"}

### Modification d’une modification

1. Dans la liste _[!UICONTROL Modifications]_, recherchez la modification que vous souhaitez modifier.

1. Cliquez sur l’icône _Plus de menu_ ( **...** ) et choisissez **[!UICONTROL Modifier]**.

1. Mettez à jour les propriétés de modification si nécessaire.

1. Cliquez sur **[!UICONTROL Enregistrer]** pour enregistrer vos modifications.

### Suppression d’une modification

1. Dans la liste _[!UICONTROL Modifications]_, recherchez la modification à supprimer.

1. Cliquez sur l’icône _Plus de menu_ ( **...** ) et choisissez **[!UICONTROL Supprimer la modification]**.

1. Confirmez la suppression lorsque vous y êtes invité.

<!-- ### Reorder modifications

Modifications are applied in the order that they appear in the list. If you have multiple modifications that affect the same element, the order may impact the final result.

Drag and drop modifications in the list to change the order. The preview updates to reflect the new modification order. -->

## Prévisualiser vos modifications

Avant de publier, prévisualisez la manière dont vos modifications sont présentées aux visiteurs et visiteuses.

Utilisez les options de prévisualisation de l’appareil dans la partie supérieure de l’éditeur visuel pour afficher vos modifications sur :

* Bureau
* Tablette
* Mobile

![Modifier la taille de l’appareil pour l’aperçu](./assets/web-experience-design-device-view.png){width="550" zoomable="yes"}

L’aperçu se met à jour pour afficher le rendu des modifications sur chaque taille d’appareil.

Utilisez la barre d’URL pour accéder à différentes pages dans la configuration de votre canal web. Vérifiez ensuite que les modifications s’appliquent correctement aux pages ciblées en fonction de vos règles de correspondance d’URL.

## Suivi des clics pour les expériences web {#web-click-tracking}

Suivez les interactions des utilisateurs avec les éléments pour mesurer l’engagement et recueillir des informations. Les données de suivi des clics sont disponibles dans vos rapports d’engagement et peuvent être utilisées pour mesurer l’efficacité de vos modifications de l’expérience web.

Lorsque votre expérience web est activée (en direct), vous pouvez également créer des rapports à l’aide d’Adobe Customer Journey Analytics (qui nécessite un abonnement au produit). Pour améliorer le suivi de l’expérience web, vous pouvez également suivre les clics sur n’importe quel élément spécifique de votre site web. Le tracking permet d’afficher le nombre de clics effectués sur cet élément dans les rapports web.

Pour plus d’informations sur Customer Journey Analytics et la création de rapports web, consultez la documentation de Customer Journey Analytics [](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-landing).

1. Sélectionnez un élément dans l’éditeur d’expérience web, tel qu’une image ou un lien.

1. Dans les propriétés de l’élément ou dans la barre d’outils contextuelle, cliquez sur l’icône _[!UICONTROL Clic sur l’élément de suivi]_.

   ![Activer le suivi des clics pour les éléments d’expérience web](./assets/web-experience-design-visual-editor-click-tracking-icons.png){width="600" zoomable="yes"}

1. Ouvrez la liste Suivi des clics dans le panneau de gauche et modifiez la valeur **[!UICONTROL Actions suivies]** pour identifier cette interaction dans vos rapports.

   ![Définir l’identification du suivi des clics pour l’expérience web](./assets/web-experience-design-visual-editor-click-tracking-identifier.png){width="600" zoomable="yes"}
