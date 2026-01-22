---
title: Expériences Web
description: Créez, concevez et publiez des expériences web personnalisées pour les parcours de compte. Apportez des modifications de contenu ciblées aux visiteurs et visiteuses du site web dans Journey Optimizer B2B edition.
feature: Content, Channels
role: User
badgeBeta: label="Beta" type="informative" tooltip="Cette fonctionnalité est actuellement en version bêta limitée"
source-git-commit: e3c00ab4657c7bf05573e049bbcb4bb3628e751e
workflow-type: tm+mt
source-wordcount: '1497'
ht-degree: 4%

---

# Expériences web

Le canal web dans Adobe Journey Optimizer B2B edition vous permet de créer des expériences personnalisées directement sur votre site web, ce qui vous permet d’entrer en contact avec les clients de manière significative. Cette fonctionnalité propose une boîte à outils flexible que vous pouvez utiliser pour améliorer l’engagement avec du contenu personnalisé et l’intégrer facilement à d’autres canaux, tels que les e-mails et les SMS.

Les expériences web vous permettent :

* Apporter des modifications de contenu personnalisées aux visiteurs et visiteuses ciblés du site web
* Personnalisez les éléments du site web tels que les bannières, le texte, les images et les boutons en fonction des attributs de compte.
* Cibler des pages spécifiques ou appliquer des modifications sur plusieurs pages à l’aide de règles de correspondance d’URL
* Suivre l’engagement et surveiller l’impact de vos efforts de personnalisation web

>[!BEGINSHADEBOX]

## Conditions préalables

Avant de pouvoir créer des expériences web, assurez-vous que les exigences suivantes sont remplies :

* Un administrateur de produit a configuré un ou plusieurs canaux web pour définir les URL (pages) à inclure pour une expérience web. Pour plus d’informations, voir [Configurations du canal web](../admin/configure-channels-web.md).

* [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/js-overview) (`alloy.js`) est implémenté pour l&#39;identification des visiteurs et la diffusion de contenu sur votre site Web. Assurez-vous que la version de Adobe Experience Platform Web SDK est la version 2.16 ou ultérieure.

* Vous disposez des [autorisations](../admin/user-management.md#b2b-product-permissions) nécessaires pour créer et gérer des expériences web dans un parcours :
   * _[!UICONTROL Campagnes]_ > _[!UICONTROL Gérer les campagnes]_ - Obligatoire pour ajouter ou mettre à jour un nœud d’action de personnalisation web.
   * _[!UICONTROL Campagnes]_ > _[!UICONTROL Afficher les campagnes]_ - Obligatoire pour afficher les détails des nœuds d’une action de personnalisation web.
   * _[!UICONTROL Campagnes]_ > _[!UICONTROL Approuver et publier des campagnes]_ - Obligatoire pour publier un parcours qui comporte un ou plusieurs nœuds d’action de personnalisation web.

* Adobe Experience Cloud [Extension de navigateur Visual Editing Helper](#install-the-visual-editing-helper-extension) est installé pour votre navigateur web. Cette extension est nécessaire pour ouvrir, créer et prévisualiser vos pages web de manière fiable dans l’espace de conception de contenu Journey Optimizer B2B edition.

  >[!NOTE]
  >
  >Google Chrome et Microsoft Edge sont actuellement les seuls navigateurs qui prennent en charge la création de pages web dans Journey Optimizer B2B edition.

>[!ENDSHADEBOX]

## Installer l’extension Visual Editing Helper

1. Ouvrez un nouvel onglet dans votre navigateur ([!DNL Google Chrome] ou [!DNL Microsoft Edge]).

1. Accédez au [Chrome Web Store de Google](https://chromewebstore.google.com/category/extensions).

   Si vous utilisez [!DNL Microsoft Edge], sélectionnez _Autoriser les extensions_ dans d’autres magasins sur la bannière supérieure. L’activation de cette option vous permet d’ajouter des extensions du [!DNL Chrome Web Store] à [!DNL Microsoft Edge].

1. Recherchez l’extension de navigateur _[!DNL Adobe Experience Cloud Visual Editing Helper]_et accédez-y.

   ![Extension Visual Editing Helper de Adobe Experience Cloud pour Google Chrome](./assets/web-experience-google-chrome-adobe-visual-editing-extension.png){width="800" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Ajouter à Chrome]**, puis sur **[!UICONTROL Ajouter une extension]** dans la boîte de dialogue de confirmation.

   Si vous utilisez [!DNL Microsoft Edge], cette action ajoute l’extension à [!DNL Edge].

1. Assurez-vous que l’extension de navigateur [!DNL Visual Editing Helper] est correctement activée dans la barre d’outils du navigateur.

   Icône de l’extension Visual Editing Helper de Adobe Experience Cloud ![dans la barre d’outils de Google Chrome](./assets/web-experience-google-chrome-adobe-visual-editing-extension-icon.png){width="450"}

Le [!DNL Adobe Experience Cloud Visual Editing Helper] est désormais automatiquement activé lorsqu’un site web est ouvert dans l’éditeur visuel de Journey Optimizer B2B edition pour les expériences web. L’extension ne dispose d’aucun paramètre conditionnel et gère automatiquement tous les paramètres, y compris les paramètres des cookies SameSite.

>[!NOTE]
>
>Certains sites web peuvent ne pas s’ouvrir de manière fiable dans l’éditeur web de Journey Optimizer B2B edition, et ce, pour l’une des raisons suivantes :
>
>* Le site web a des politiques de sécurité strictes.
>* Le site web est dans un iframe.
>* Le site d’assurance qualité ou d’évaluation du client n’est pas disponible en externe (site interne).

## Créer une expérience web

Vous pouvez configurer des expériences web dans un parcours lorsque vous [ajoutez un nœud _[!UICONTROL Prendre une action]_](../journeys/action-nodes.md) et procédez comme suit :

1. Pour la cible _[!UICONTROL Action sur]_, choisissez **[!UICONTROL Personnes]**.

1. Pour l’_[!UICONTROL Action sur les personnes]_, choisissez **[!UICONTROL Personnaliser l’expérience web]**.

   ![Agir - personnaliser l’expérience web](./assets/web-experience-add-journey-node.png){width="500"}

1. Cliquez sur **[!UICONTROL Créer une expérience web]**.

1. Dans la boîte de dialogue _[!UICONTROL Créer une expérience web]_, saisissez un **[!UICONTROL Nom]** et un **[!UICONTROL Description]** utiles (facultatif).

   * Nom : 100 caractères maximum, doit être unique et ne pas respecter la casse.

   * Description - 300 caractères maximum

   >[!NOTE]
   >
   >Les champs Nom et Description prennent en charge les caractères alpha, numériques et spéciaux. Les caractères réservés (`\ / : * ? " < > |`) ne sont **_autorisés_**.

   ![ Boîte de dialogue Créer une expérience web ](./assets/web-experience-create-dialog.png){width="400"}

<!-- What is this for? 1. Properties? -->

1. Dans l’onglet **[!UICONTROL Propriétés]** , saisissez la description de l’expérience web.

1. Cliquez sur l’onglet **[!UICONTROL Actions]** et sélectionnez le **[!UICONTROL canal web]** à utiliser pour l’expérience web.

   La configuration du canal web détermine où les modifications de contenu sont appliquées en fonction des règles de correspondance de page configurées. Voir [Configurations de canal web](../admin/configure-channels-web.md) pour plus d’informations.

   ![Configuration de canal web sélectionnée](./assets/web-experience-journey-node-actions-tab.png){width="700" zoomable="yes"}

1. Pour définir les modifications web, cliquez sur **[!UICONTROL Modifier le contenu]**.

   L’éditeur s’ouvre dans l’onglet _[!UICONTROL Contenu]_ où vous pouvez définir les modifications pour votre expérience web. Consultez [Conception d’expérience web](./web-experience-design.md) pour plus d’informations sur l’utilisation des outils de conception afin d’ajouter les modifications de contenu de l’expérience web.

1. Dans le panneau de droite, définissez les propriétés de l’expérience web en fonction de la manière dont vous souhaitez les définir et les gérer.

   * **[!UICONTROL Éditeur visuel]** - Basculez entre l’[éditeur visuel et non visuel](./web-experience-design.md#web-design-tools) pour la conception de modification de l’expérience web.
   * **[!UICONTROL Redirection des visiteurs]** - Activez cette option pour [rediriger les visiteurs vers une autre URL existante](#redirect-to-url) plutôt que de créer une nouvelle variation dans l’onglet de contenu.

   ![Activer/désactiver les propriétés de l’éditeur visuel et de l’URL de redirection](./assets/web-experience-journey-node-content-properties.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Modifier la page web]** pour [concevoir vos modifications web](./web-experience-design.md).

1. Une fois les modifications effectuées, cliquez sur la flèche de gauche au-dessus de l’éditeur pour revenir à l’onglet contenu et aux propriétés de nœud d’expérience web personnalisées.

   Vous pouvez cliquer sur la flèche gauche tout en haut pour revenir à la zone de travail du parcours.

## Modification d’une expérience web

1. Ouvrez le parcours et sélectionnez le nœud d’action **[!UICONTROL Personnaliser l’expérience web]**.

1. Pour apporter des modifications à la configuration ou au contenu du canal web, cliquez sur **[!UICONTROL Modifier l’expérience web]**.

1. Sélectionnez l’onglet **[!UICONTROL Actions]** et modifiez la configuration web si nécessaire.

1. Sélectionnez l’onglet **[!UICONTROL Contenu]** et utilisez les outils de conception visuelle selon vos besoins.

   * _Éditeur visuel_ - Cliquez sur **[!UICONTROL Modifier le contenu]**.
   * _Éditeur non visuel_ - Cliquez sur **[!UICONTROL Ajouter une modification]**.

   Voir [Conception d’expérience web](./web-experience-design.md) pour plus d’informations.

1. Une fois les définitions de modification terminées, cliquez sur la flèche de gauche au-dessus de l’éditeur pour revenir à l’onglet contenu et aux propriétés de l’expérience web.

   Vous pouvez cliquer sur la flèche gauche tout en haut pour revenir à la zone de travail du parcours.

## Rediriger vers l’URL

Lors de la création d’une expérience web, vous pouvez rediriger les visiteurs vers une autre URL existante plutôt que de créer une nouvelle variation dans l’éditeur de contenu. Cette option est utile lorsque vous souhaitez exécuter une expérience de contenu comparant deux expériences différentes au lieu de simplement modifier quelques éléments dans une page.

Par exemple, créez une campagne web avec deux traitements :

Dans le traitement A, créez une expérience web à l’aide de l’éditeur de contenu pour la moitié de votre population ciblée.

Dans le traitement B, sélectionnez l’option _[!UICONTROL Rediriger vers l’URL]_ pour l’autre moitié de la population ciblée. Saisissez l’URL d’une page avec une conception alternative que vous avez créée en dehors de Journey Optimizer B2B edition.

![Définissez la redirection du visiteur pour rediriger les visiteurs vers une URL spécifique](./assets/web-experience-journey-node-content-visitor-redirection.png){width="500" zoomable="yes"}

>[!NOTE]
>
>Lorsque cette option est sélectionnée, l’aperçu du site web n’est pas affiché et le bouton (bascule) _[!UICONTROL Éditeur visuel]_ est désactivé.

Lorsque votre campagne web est active, vous pouvez suivre les performances de l’expérience web que vous avez définie dans Journey Optimizer B2B edition par rapport aux expériences web qui ont utilisé une redirection vers la page alternative.

## Test de l’expérience web

Une fois la conception du contenu terminée pour l’expérience web, vous pouvez utiliser la fonctionnalité _Simuler du contenu_ pour prévisualiser les modifications de votre page web. Si vous avez inséré du contenu personnalisé, vous pouvez utiliser les données du profil de test pour vérifier le rendu du contenu. Les outils de simulation sont disponibles à partir de l’onglet _[!UICONTROL Contenu]_ pour l’expérience web ou dans l’éditeur de conception visuelle du contenu.

1. Cliquez sur **[!UICONTROL Simuler du contenu]** en haut à droite.

1. Sélectionnez un profil de test.

1. Ajoutez un profil de test pour vérifier votre page web à l’aide des données de profil de test.

<!-- This works differently than emails (rely on Marketo data), currently. Will expand when we figure it out -->

## Activer votre expérience web

Votre expérience web est activée et rendue visible par l’audience lorsque vous [publiez le parcours ](../journeys/create-publish-journey.md#publish-a-journey). Avant d’activer une expérience web par le biais d’un parcours, tenez compte des points suivants :

* Si vous publiez un parcours avec une expérience web ayant un impact sur les mêmes pages qu’un autre parcours déjà actif, toutes les modifications sont appliquées aux pages web.

* Si plusieurs parcours mettent à jour les mêmes éléments de votre site web, la dernière modification appliquée est prioritaire.

### Exigences de diffusion

Pour activer la diffusion de l’expérience web, les paramètres suivants doivent être définis :

* Dans la collecte de données Adobe Experience Platform, assurez-vous qu’un train de données est défini avec l’option Adobe Journey Optimizer B2B edition activée sous le service Adobe Experience Platform.

  Cette configuration permet de s’assurer que Adobe Experience Platform Edge peut gérer correctement les événements entrants. [En savoir plus](https://experienceleague.adobe.com/fr/docs/experience-platform/datastreams/configure)

* Dans Adobe Experience Platform, assurez-vous d’avoir une politique de fusion avec l’option _[!UICONTROL Politique de fusion Active-On-Edge]_ activée.

  Sélectionnez une politique sous le menu Experience Platform Client > Profils > Politiques de fusion . [En savoir plus](https://experienceleague.adobe.com/en/docs/experience-platform/profile/merge-policies/ui-guide#configure)

  Cette politique de fusion est utilisée par les canaux entrants Journey Optimizer B2B edition pour activer et publier correctement les expériences web entrantes sur Edge. [En savoir plus](https://experienceleague.adobe.com/en/docs/experience-platform/profile/merge-policies/ui-guide)

### Dépannage

Vous pouvez utiliser la vue Edge Delivery dans Adobe Experience Platform Assurance pour résoudre les problèmes de diffusion des expériences web Journey Optimizer B2B edition. Ce plug-in vous permet d’examiner en détail les appels de requête, de vérifier les appels Edge attendus et d’examiner les données de profil. Ces données de profil comprennent les mappages d’identité, les appartenances aux segments et les paramètres de consentement. Vous pouvez également consulter les activités qualifiées et non qualifiées pour la requête.

Pour plus d’informations sur la vue Edge Delivery dans Assurance, consultez la [documentation Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/assurance/view/edge-delivery).
