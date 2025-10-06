---
title: Mode sombre pour le contenu des e-mails
description: Découvrez la conception d’e-mails en mode sombre dans Journey Optimizer B2B edition. Prévisualisez le rendu, personnalisez les paramètres, assurez l’accessibilité et effectuez des tests sur les clients de messagerie.
feature: Email Authoring
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: mode sombre, e-mail, couleur, conception
source-git-commit: 1b59c4260ee49c21d9205ffa740bf3b0ae345287
workflow-type: tm+mt
source-wordcount: '1600'
ht-degree: 19%

---

# Mode sombre pour le contenu des e-mails {#dark-mode}

>[!CONTEXTUALHELP]
>id="ajo-b2b_dark_mode"
>title="Basculer vers le mode sombre"
>abstract="Basculez vers le mode sombre pour prévisualiser le rendu et définir des paramètres personnalisés spécifiques. <br>Le rendu final dépend du client de messagerie de la personne destinataire. Notez que tous les clients de messagerie ne prennent pas en charge le mode sombre personnalisé."

>[!CONTEXTUALHELP]
>id="ajo-b2b_dark_mode_preview"
>title="Basculer vers le mode sombre"
>abstract="Basculez vers le mode sombre pour prévisualiser le rendu sur les clients de messagerie pris en charge. <br>Le rendu final dépend du client de messagerie de la personne destinataire. Notez que tous les clients de messagerie ne prennent pas en charge le mode sombre."

Le _mode sombre_ permet à un client de messagerie ou à une application de support d’afficher les e-mails avec des arrière-plans plus sombres et des couleurs plus claires pour le texte, les boutons et d’autres éléments visuels. Ce type d&#39;écran peut réduire la fatigue visuelle, économiser l&#39;autonomie de la batterie et améliorer la lisibilité dans les environnements à faible luminosité pour une expérience de visionnage plus confortable. Tendance croissante au sein des principaux systèmes d’exploitation et applications, il est désormais important de prendre en compte dans la conception d’e-mails modernes afin de s’assurer que le contenu reste lisible et visuellement attrayant pour tous les utilisateurs et utilisatrices.

![Diagramme de concept des modes clair et sombre présentant le rendu du contenu dans les thèmes clair et sombre](../assets/do-not-localize/light-dark-mode.svg){width="50%"}

Lorsque vous [créez le contenu de votre e-mail](./email-authoring.md) dans l’espace de conception visuelle [!DNL Journey Optimizer B2B Edition], vous pouvez passer à la vue _**[!UICONTROL Mode sombre]**_. Dans cette vue, vous pouvez également définir des paramètres personnalisés spécifiques pour la prise en charge des clients de messagerie lorsque leur mode sombre est activé.

## Remarques concernant le client de messagerie

Il existe des différences significatives dans la manière dont les différents clients de messagerie et applications appliquent le mode sombre. Pour cette raison, prenez en compte les attentes en matière de rendu en mode sombre avec précaution. Avant d’utiliser le mode sombre dans l’espace de conception d’e-mail, tenez compte des cas d’utilisation de client de messagerie suivants :
<!--
* Check out the list of [email clients supporting dark mode](https://www.caniemail.com/search/?s=dark){target="_blank"}

* Learn more on Dark mode in this [Litmus blog post](https://www.litmus.com/blog/the-ultimate-guide-to-dark-mode-for-email-marketers){target="_blank"}
-->

+++Clients qui ne prennent pas en charge le mode sombre

Certains clients de messagerie ne prennent pas du tout en charge cette fonctionnalité, tels que :

* [!DNL Yahoo! Mail]
* [!DNL AOL]

Si vous définissez des paramètres personnalisés en mode sombre dans la conception d’e-mail, ces clients de messagerie ne peuvent pas afficher de rendu en mode sombre. <!--Regardless of whether the interface is in light or dark mode, your email will render the same.-->

+++

+++Clients appliquant leurs propres {#default-support} en mode sombre

Certains clients de messagerie appliquent systématiquement leur propre mode sombre par défaut à tous les e-mails reçus. Ils ajustent automatiquement les couleurs, les arrière-plans, les images et d’autres éléments en fonction de leurs paramètres de mode sombre. Les paramètres externes ne sont pas possibles. Ces clients sont les suivants :

* Gmail (messagerie électronique pour ordinateurs de bureau, iOS, Android™, messagerie électronique mobile)
* Outlook Windows
* Outlook Windows Mail

<!--It is important to note that less than 25% of email clients offer customization options for dark mode. Clients such as Gmail implement their own dark mode rendering, which is not subject to external modification.-->
Dans ce cas, les paramètres du mode sombre du client remplacent ceux que vous définissez dans [!DNL Journey Optimizer B2B Edition]

+++

+++Clients qui prennent en charge le mode sombre personnalisé

La plupart des clients de messagerie les plus populaires offrent la possibilité de rendre le mode sombre personnalisé avec la requête `@media (prefers-color-scheme: dark)`, qui est la méthode utilisée par les styles d’e-mail [!DNL Journey Optimizer B2B Edition]. Cette liste de clients comprend :

* Apple Mail macOS
* Apple Mail iOS
* MacOS Outlook
* Outlook.com
* Outlook iOS
* Outlook Android™

Dans ce cas, les paramètres spécifiques que vous définissez dans le [!DNL Journey Optimizer B2B Edition] sont rendus. Cependant, certaines restrictions peuvent s’appliquer en fonction de chaque client de messagerie. Par exemple, certains clients (tels qu’Apple Mail 16 (macOS 13)) ne génèrent pas de mode sombre si des images sont présentes dans le contenu de l’e-mail.

Pour des résultats optimaux, testez votre contenu avec les clients de messagerie que vous ciblez. Pour voir une simulation qui se rapproche le plus possible du résultat final pour chaque client, utilisez l’intégration [Rendu des tests d’e-mail Litmus](./email-test-rendering.md) dans l’espace de conception d’e-mail.

+++

## Conception pour le mode sombre

Lorsque vous mettez en forme le contenu de votre e-mail pour le mode sombre en [!DNL Journey Optimizer B2B Edition], l’espace de conception visuelle fournit deux types d’outils :

* Utilisez la fonction [preview](#preview-default-dark-mode) pour passer en revue le rendu du mode sombre par défaut pour la plupart des clients de messagerie de support.

* Si vous souhaitez remplacer les paramètres par défaut des clients de messagerie de prise en charge, définissez et appliquez des paramètres de mode sombre personnalisés à votre contenu d’e-mail. [En savoir plus](#define-custom-dark-mode)

### Prévisualiser le mode sombre par défaut {#preview-dark-mode}

<!-- Should work with templates and themes, NOT for LP and fragments - but TBC with eng. 
>[!NOTE]
>
>Currently you may not be able to switch to dark mode if you select an [email template](use-email-templates.md) or if you apply a [theme](apply-email-themes.md).-->

1. Ouvrez le contenu de l’e-mail dans l’espace de conception d’e-mail.

   En haut à droite de la zone de travail se trouve un sélecteur clair-sombre qui permet de basculer l’affichage du contenu entre le mode clair (par défaut) et le mode sombre.

   ![Zone de travail de conception des e-mails affichant le sélecteur de mode clair dans le coin supérieur droit](./assets/email-color-mode-light-selector.png){width="700" zoomable="yes"}

1. Remplacez le sélecteur par _Mode sombre_ (![icône Mode sombre](../assets/do-not-localize/icon-content-dark-mode.svg) ).

   La zone de travail affiche le contenu à l’aide du mode sombre par défaut preview.x

   Par défaut, l’aperçu en mode sombre applique le modèle de couleurs `full color invert` à tous les éléments, à l’exception des images et des icônes. Ce jeu de couleurs détecte les zones comportant des éléments clairs et sombres et les inverse. Les arrière-plans clairs deviennent sombres et le texte sombre devient clair, ou les arrière-plans sombres deviennent clairs et le texte clair devient sombre.

   ![Zone de travail de conception des e-mails affichant le sélecteur en mode sombre et le contenu des e-mails affiché en mode sombre](./assets/email-color-mode-dark-selector.png){width="700" zoomable="yes"}

>[!CAUTION]
>
>Le rendu final peut varier en fonction du client de messagerie du destinataire. Pour voir une simulation qui se rapproche le plus possible du résultat final pour chaque client de messagerie, utilisez l’intégration [Rendu des e-mails de test Litmus](./email-test-rendering.md).

### Définition des paramètres personnalisés du mode sombre {#custom-dark-mode}

>[!CONTEXTUALHELP]
>id="ajo-b2b_dark_mode_image"
>title="Utiliser une image spécifique pour le mode sombre"
>abstract="Vous pouvez sélectionner une autre image à afficher lorsque le mode sombre est activé. <br>L’ajout d’une image spécifique pour le mode sombre ne garantit pas qu’elle s’affiche correctement dans tous les clients de messagerie. Notez que tous les clients de messagerie ne prennent pas en charge le mode sombre personnalisé."

Après le passage en mode sombre, vous pouvez choisir de modifier des éléments de style spécifiques de votre contenu qui s’affichent uniquement lorsque le mode sombre est activé dans le client de messagerie du destinataire (à condition qu’il prenne en charge cette fonctionnalité).

>[!NOTE]
>
>Le rendu final en mode sombre dépend de chaque client de messagerie. Le résultat peut donc varier d’un client à l’autre. Pour plus d’informations, consultez les [considérations relatives au client de messagerie](#email-client-considerations) .

Le style personnalisé en mode sombre de l’espace de conception d’e-mail utilise <!-- `@media (prefers-color-scheme: dark)` method--> `@media (prefers-color-scheme: dark)` requête CSS, qui détecte si le client de messagerie est en mode sombre et applique la conception avec thème sombre définie dans votre e-mail.

_Pour définir les paramètres personnalisés du mode sombre :_

1. Si nécessaire, déplacez le sélecteur vers _Mode sombre_ ( ![icône Mode sombre](../assets/do-not-localize/icon-content-dark-mode.svg) ) en haut à droite de la zone de travail de conception.

1. Modifiez des attributs de couleur de style, tels que du texte, des arrière-plans ou des boutons.

   ![Panneau des paramètres de style de texte en mode sombre avec options de couleur et de police](./assets/email-color-mode-dark-text-settings.png){width="700" zoomable="yes"}

1. Pour les images et les icônes, définissez des ressources spécifiques pour le mode sombre uniquement.

   Vous ne pouvez pas modifier les couleurs des images et des icônes, mais vous pouvez définir d’autres ressources à utiliser en mode sombre. Vous pouvez tester différentes combinaisons de couleurs pour vos icônes ou ajuster la couleur et la saturation des images photographiques.

   ![Icônes avec différentes combinaisons de couleurs](../assets/do-not-localize/color-contrast-images-diagram.svg){width="80%"}

   Sélectionnez une image et passez en **[!UICONTROL mode sombre]** à l’aide du bouton dédié dans le volet **[!UICONTROL Paramètres]**. Sélectionnez ensuite une autre ressource image.

   ![Paramètres d’image du mode sombre affichant l’option permettant de sélectionner une ressource d’image différente pour le mode sombre](./assets/email-color-mode-dark-image-settings.png){width="700" zoomable="yes"}

   Consultez [Ajout de ressources d’image](./email-authoring.md#add-image-assets) pour plus d’informations sur la sélection d’une ressource d’image.

1. À tout moment pendant vos modifications de conception, sélectionnez **[!UICONTROL Basculer vers la vue en direct]** pour vérifier comment votre contenu peut s’afficher sur différentes tailles d’appareil.

   Dans cet affichage, remplacez le sélecteur par _Mode sombre_ ( ![icône Mode sombre](../assets/do-not-localize/icon-content-dark-mode.svg) ) pour prévisualiser la version en mode sombre de votre contenu sur les différents appareils.

   ![Panneau d’affichage dynamique affichant le contenu des e-mails en mode sombre sur différentes tailles d’appareil](./assets/email-color-mode-dark-live-view.png){width="800" zoomable="yes"}

   >[!CAUTION]
   >
   >Le mode en direct est une prévisualisation générique conçue pour comparer l’aspect du rendu sur différentes tailles d’appareils. Le rendu final peut varier en fonction du client de messagerie du destinataire.

1. Une fois les modifications du mode sombre effectuées, cliquez sur **[!UICONTROL Simuler du contenu]**.

   ![Zone de travail de conception d’e-mail avec le bouton Simuler du contenu mis en surbrillance pour tester le mode sombre](./assets/email-color-mode-dark-simulate-content.png){width="700" zoomable="yes"}

   Utilisez les outils de prévisualisation et de relecture pour tester votre conception d’e-mail. Voir [Prévisualiser et tester le contenu de votre e-mail](./email-simulate-content.md) pour plus d’informations.

1. Si vous disposez d’un compte d’entreprise Litmus, sélectionnez **[!UICONTROL Rendu d’e-mail]** pour afficher le rendu final en mode sombre pour divers clients de messagerie dans Litmus .

   Pour plus d’informations, consultez [Test du rendu des e-mails avec Litmus](./email-test-rendering.md) .

   >[!CAUTION]
   >
   >Bien que la simulation se rapproche de la façon dont les e-mails apparaissent en mode sombre, le rendu réel peut différer en raison de variations au niveau des fournisseurs de services de messagerie ou des paramètres au niveau de l’appareil.

## Bonnes pratiques {#best-practices}

À mesure que l’adoption du mode sombre augmente dans les principaux clients de messagerie, il est essentiel d’examiner le rendu de vos e-mails à la fois dans les environnements clairs et sombres, que vous utilisiez le [mode sombre personnalisé](#define-custom-dark-mode) ou non.

Le mode sombre peut modifier les couleurs, les arrière-plans et les images, parfois en remplaçant les choix définis lors de la conception. Pour garantir la cohérence visuelle, l’accessibilité et l’intégrité de la marque, appliquez les bonnes pratiques suivantes :

| Pratique |            |
| -------- | ---------- |
| Optimisation des images et des logos | Liste de vérification :<ul><li>Enregistrez les logos et les icônes en tant que fichiers PNG avec des arrière-plans transparents pour éviter les zones blanches visibles en mode sombre. <li>Évitez les images avec des arrière-plans blancs ou clairs codés en dur. <li>Si vous ne pouvez pas utiliser la transparence, placez les images sur un arrière-plan uni dans votre conception pour éviter des inversions de couleurs inappropriées. |
| Surveiller vos antécédents | Liste de vérification :<ul><li>Vérifiez que le contraste entre le texte et les couleurs d’arrière-plan est suffisant pour garantir une bonne lisibilité en mode clair et en mode sombre. <li>Évitez de vous fier uniquement aux couleurs d’arrière-plan pour du contenu important. Certains clients remplacent les couleurs de fond en mode sombre, afin de s’assurer que les informations clés sont toujours visibles. |
| Conception de contenu accessible en mode sombre | Liste de vérification :<ul><li>Utilisez des combinaisons de couleurs faciles à distinguer pour les personnes atteintes de daltonisme. <li>Utilisez une palette de tons moyens pour garantir un contraste adéquat par rapport à des arrière-plans clairs et sombres. <li>Utilisez des combinaisons de couleurs accessibles avec un contraste élevé pour améliorer la lisibilité et respecter les normes [!DNL Web Content Accessibility Guidelines (WCAG)]. Utilisez des outils tels que [!DNL WebAIM Contrast Checker] pour vérifier le contraste des couleurs. <li>Évitez les polices de caractères fines, car elles peuvent affecter la lisibilité. Si votre marque nécessite l’utilisation d’une police fine, mettez-la en gras en mode sombre. <li>Ignorez le blanc pur sur le noir pur, ce qui peut entraîner une fatigue oculaire et pourrait être inversé automatiquement dans certains clients de messagerie. <li>Fournissez un style de secours accessible si le mode sombre n’est pas pris en charge. |
| Tester vos e-mails dans un environnement en mode sombre | Liste de vérification :<ul><li>Utilisez l’aperçu [ mode sombre ](#preview-dark-mode) dans l’espace de conception d’e-mail, qui utilise des modèles de couleurs inversés pour repérer les problèmes dès le début. <li>Utilisez un compte d’entreprise Litmus avec l’option [[!UICONTROL Rendu d’e-mail]](./email-test-rendering.md) pour simuler vos conceptions sur les principaux clients de messagerie (tels qu’Apple Mail, Gmail et Outlook) et voir comment les couleurs et les images se comportent en mode sombre. |

<!--KEEP dark mode accessibility best practices IN ONE SINGLE LOCATION - for now listed on this page.
If needed, it can be moved to the Design accessible content page:
The best practices for designing accesible content in dark mode are listed in [this section](accessible-content.md#dark-mode).-->

<!--**Inline critical styles**

Inline CSS helps maintain more control over styling, as some clients strip external styles in dark mode.-->
