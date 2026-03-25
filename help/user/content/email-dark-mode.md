---
title: Mode sombre pour le contenu des e-mails
description: Découvrez la conception d’e-mails en mode sombre dans Journey Optimizer B2B edition. Prévisualisez le rendu, personnalisez les paramètres, assurez l’accessibilité et effectuez des tests sur divers clients de messagerie.
feature: Email Authoring
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: mode sombre, e-mail, couleur, conception
exl-id: c9ffb883-d37f-48bc-b23d-6eccf7a04d9a
source-git-commit: b369ef39715f327fcff7237e827bebf4e82c27f6
workflow-type: tm+mt
source-wordcount: '1604'
ht-degree: 17%

---

# Mode sombre pour le contenu des e-mails {#dark-mode}

>[!CONTEXTUALHELP]
>id="ajo-b2b_dark_mode"
>title="Basculer vers le mode sombre"
>abstract="Passez en mode sombre où vous pouvez prévisualiser la manière dont il peut s’afficher et définir des paramètres personnalisés spécifiques. <br>Le rendu final dépend du client de messagerie du destinataire. Notez que tous les clients de messagerie ne prennent pas en charge le mode sombre personnalisé."

>[!CONTEXTUALHELP]
>id="ajo-b2b_dark_mode_preview"
>title="Basculer vers le mode sombre"
>abstract="Basculez vers le mode sombre pour prévisualiser la manière dont il peut s’afficher sur les clients de messagerie pris en charge. <br>Le rendu final dépend du client de messagerie du destinataire. Notez que tous les clients de messagerie ne prennent pas en charge le mode sombre."

Le _mode sombre_ permet à un client de messagerie ou à une application de support d&#39;afficher les e-mails avec des arrière-plans plus sombres et des couleurs plus claires pour le texte, les boutons et d&#39;autres éléments visuels. Ce type d&#39;écran peut réduire la fatigue visuelle, économiser l&#39;autonomie de la batterie et améliorer la lisibilité dans les environnements à faible luminosité pour une expérience de visionnage plus confortable. Tendance croissante au sein des principaux systèmes d’exploitation et applications, il est désormais important de prendre en compte dans la conception d’e-mails modernes afin de s’assurer que le contenu reste lisible et visuellement attrayant pour tous les utilisateurs et utilisatrices.

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

+++Clients appliquant leur propre mode sombre {#default-support}

Certains clients de messagerie appliquent systématiquement leur propre mode sombre par défaut à tous les e-mails reçus. Ils ajustent automatiquement les couleurs, les arrière-plans, les images et d’autres éléments en fonction de leurs paramètres de mode sombre. Les paramètres externes ne sont pas possibles. Ces clients sont les suivants :

* Gmail (messagerie électronique pour ordinateurs de bureau, iOS, Android™, messagerie électronique mobile)
* Outlook Windows
* Outlook Windows Mail

<!--It is important to note that less than 25% of email clients offer customization options for dark mode. Clients such as Gmail implement their own dark mode rendering, which is not subject to external modification.-->
In this case, the client dark mode settings override the custom dark mode settings that you define in [!DNL Journey Optimizer B2B Edition]

+++

+++Clients that support custom dark mode

Many of the most popular email clients offer the option to render custom dark mode with the `@media (prefers-color-scheme: dark)` query, which is the method used by the [!DNL Journey Optimizer B2B Edition] email styles. This list of clients includes:

* Apple Mail macOS
* Apple Mail iOS
* Outlook macOS
* Outlook.com
* Outlook iOS
* Outlook Android™

In this case, the specific settings you define in the [!DNL Journey Optimizer B2B Edition] are rendered. However, some restrictions could apply according to each email client. For example, some clients (such as Apple Mail 16 (macOS 13)) do not generate dark mode if images are present in the email content.

For optimal results, test your content with the email clients that you are targeting. To see a simulation that comes as close as possible to the final result for each client, use the [Litmus email test rendering](./email-test-rendering.md) integration in the email design space.

+++

## Design for dark mode

As you style your email content for dark mode in [!DNL Journey Optimizer B2B Edition], the visual design space provides two types of tools:

* Use the [preview function](#preview-default-dark-mode) to review the default dark mode rendering for most supporting email clients.

* If you want to override the default settings of supporting email clients, define and apply custom dark mode settings to your email content. [Learn more](#define-custom-dark-mode)

### Prévisualiser le mode sombre par défaut {#preview-dark-mode}

<!-- Should work with templates and themes, NOT for LP and fragments - but TBC with eng. 
>[!NOTE]
>
>Currently you may not be able to switch to dark mode if you select an [email template](use-email-templates.md) or if you apply a [theme](apply-email-themes.md).-->

1. Open the email content in the email design space.

   At the top right of the canvas, there is a light-dark selector that toggles the content display between light (default) and dark mode.

   ![Email design canvas showing the light mode selector in the top right corner](./assets/email-color-mode-light-selector.png){width="700" zoomable="yes"}

1. Change the selector to _Dark mode_ ( ![Dark mode icon](../assets/do-not-localize/icon-content-dark-mode.svg) ).

   The canvas displays the content using the default dark mode preview.x

   By default, the dark mode preview applies the `full color invert` color scheme to all elements except images and icons. This color scheme detects areas with light and dark elements and inverts them. Light backgrounds become dark and dark text becomes light, or dark backgrounds become light and light text becomes dark.

   ![Email design canvas showing the dark mode selector and email content displayed in dark mode](./assets/email-color-mode-dark-selector.png){width="700" zoomable="yes"}

>[!CAUTION]
>
>The final rendering could vary according to the recipient&#39;s email client. To see a simulation that comes as close as possible to the final result for each email client, use the [Litmus test email rendering](./email-test-rendering.md) integration.

### Define custom dark mode settings {#custom-dark-mode}

>[!CONTEXTUALHELP]
>id="ajo-b2b_dark_mode_image"
>title="Utiliser une image spécifique pour le mode sombre"
>abstract="You can select another image to display when dark mode is on. <br>Adding a specific image for dark mode does not guarantee that it renders correctly in all email clients. Notez que tous les clients de messagerie ne prennent pas en charge le mode sombre personnalisé."

After switching to dark mode, you can choose to edit specific styling elements of your content that are displayed only when dark mode is enabled in the recipient&#39;s email client (provided it supports that feature).

>[!NOTE]
>
>Le rendu final en mode sombre dépend de chaque client de messagerie. Le résultat peut donc varier d’un client à l’autre. Review the [email client considerations](#email-client-considerations) for more information.

The custom dark mode styling in the email design space uses the<!-- `@media (prefers-color-scheme: dark)` method--> `@media (prefers-color-scheme: dark)` CSS query, which detects if the email client is set to dark mode and applies the dark-themed design that is defined in your email.

_To define custom dark mode settings :_

1. If needed, move the selector to _Dark mode_ ( ![Dark mode icon](../assets/do-not-localize/icon-content-dark-mode.svg) ) at the top right of the design canvas.

1. Edit any styling color attributes, such as text, backgrounds, or buttons.

   ![Dark mode text styling settings panel showing color and font options](./assets/email-color-mode-dark-text-settings.png){width="700" zoomable="yes"}

1. For the images and icons, define specific assets for dark mode only.

   You cannot change the colors of images and icons, but you can define alternative assets to be used for dark mode. You can experiment with different color combinations for your icons or make adjustments for color and saturation for photographic images.

   ![Icons with different color combinations](../assets/do-not-localize/color-contrast-images-diagram.svg){width="80%"}

   Select any image and switch to **[!UICONTROL Dark mode]** using the dedicated toggle in the **[!UICONTROL Settings]** pane. Then, select a different image asset.

   ![Dark mode image settings showing option to select different image asset for dark mode](./assets/email-color-mode-dark-image-settings.png){width="700" zoomable="yes"}

   See [Add image assets](./email-authoring.md#add-image-assets) for more information about selecting an image asset.

1. At any point during your design changes, select **[!UICONTROL Switch to live view]** to check how your content might render on various device sizes.

   From this view, change the selector to _Dark mode_ ( ![Dark mode icon](../assets/do-not-localize/icon-content-dark-mode.svg) ) to preview the dark mode version of your content across the different devices.

   ![Panneau d’affichage en direct affichant le contenu des e-mails en mode sombre sur différentes tailles d’appareil](./assets/email-color-mode-dark-live-view.png){width="800" zoomable="yes"}

   >[!CAUTION]
   >
   >Le mode en direct est une prévisualisation générique conçue pour comparer l’aspect du rendu sur différentes tailles d’appareils. Le rendu final peut varier en fonction du client de messagerie du destinataire.

1. Une fois vos modifications du mode sombre effectuées, cliquez sur **[!UICONTROL Simuler du contenu]**.

   ![Zone de travail de conception d’e-mail avec le bouton Simuler le contenu mis en surbrillance pour tester le mode sombre](./assets/email-color-mode-dark-simulate-content.png){width="700" zoomable="yes"}

   Utilisez les outils de prévisualisation et de relecture pour tester votre conception d’e-mail. Voir [Prévisualiser et tester le contenu de votre e-mail](./email-simulate-content.md) pour plus d’informations.

1. Si vous disposez d’un compte d’entreprise Litmus, sélectionnez **[!UICONTROL Rendu de l’e-mail]** pour afficher le rendu final en mode sombre pour divers clients de messagerie dans Litmus .

   Voir [Test du rendu des e-mails avec Litmus](./email-test-rendering.md) pour plus d’informations.

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
| Tester vos e-mails dans un environnement en mode sombre | Liste de vérification :<ul><li>Utilisez l’[aperçu en mode sombre](#preview-dark-mode) dans l’espace de conception d’e-mail, qui utilise des modèles de couleurs inversés pour repérer les problèmes dès le début. <li>Utilisez un compte d’entreprise Litmus avec l’option [[!UICONTROL Rendu d’e-mail]](./email-test-rendering.md) pour simuler vos conceptions sur les principaux clients de messagerie (tels qu’Apple Mail, Gmail et Outlook) et voir comment les couleurs et les images se comportent en mode sombre. |

<!--KEEP dark mode accessibility best practices IN ONE SINGLE LOCATION - for now listed on this page.
If needed, it can be moved to the Design accessible content page:
The best practices for designing accesible content in dark mode are listed in [this section](accessible-content.md#dark-mode).-->

<!--**Inline critical styles**

Inline CSS helps maintain more control over styling, as some clients strip external styles in dark mode.-->
