---
title: Ajouter un e-mail à votre Parcours
description: Découvrez comment ajouter, définir et optimiser des actions d’e-mail dans Adobe Journey Optimizer B2B. Améliorez les parcours de votre compte avec des communications par e-mail ciblées.
feature: Email Authoring, Account Journeys
role: User
exl-id: 21a6ce0f-b59d-4be2-abc3-fda5c6a6334f
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '963'
ht-degree: 0%

---

# Ajouter un e-mail à votre parcours

Utilisez Adobe Journey Optimizer B2B edition pour envoyer des e-mails à vos clients par le biais de parcours de compte. Vous pouvez choisir de créer, de personnaliser et de prévisualiser des messages dans l’espace de conception d’e-mail. Vous pouvez également choisir d’envoyer un e-mail déjà défini dans l’instance Marketo Engage connectée.

>[!NOTE]
>
>Si vous envoyez un e-mail pour la première fois, assurez-vous que le canal e-mail est configuré depuis Adobe Marketo Engage. Pour en savoir plus, voir [Protocoles de tracking et de diffusion e-mail](../start/email-protocols.md).

## Ajout d’un nœud d’action d’e-mail dans un parcours

Vous pouvez configurer des diffusions e-mail dans un parcours lorsque vous [ajoutez un nœud _[!UICONTROL Prendre une action]_ ](../journeys/action-nodes.md) et que vous effectuez les opérations suivantes :

1. Pour la cible _[!UICONTROL Action sur]_, choisissez **[!UICONTROL Personnes]**.

1. Pour l’_[!UICONTROL Action sur les personnes]_, choisissez **[!UICONTROL Envoyer un e-mail]**.

1. Pour l’option _[!UICONTROL Source de l’e-mail]_, choisissez la manière dont vous souhaitez générer l’e-mail à envoyer.

   ![Agir - Envoyer un e-mail](assets/journey-node-send-email.png){width="700" zoomable="yes"}

   * Choisissez **[!UICONTROL Créer un e-mail]** pour créer l’e-mail en mode natif dans Journey Optimizer B2B edition.

     Cette option permet de gérer le contenu de l’e-mail de manière native dans Journey Optimizer B2B edition. Cliquez sur **[!UICONTROL Créer un e-mail]** pour ouvrir la boîte de dialogue _Créer un e-mail_. Vous pouvez créer une ressource de contenu d’e-mail<!-- or duplicate an existing email content asset-->.

     Dans la boîte de dialogue, saisissez un **[!UICONTROL Nom]** unique pour l’e-mail et un **[!UICONTROL Objet]**, puis cliquez sur **[!UICONTROL Créer]**.

     ![Boîte de dialogue Créer un e-mail - Nouvel e-mail](assets/create-new-email-no-duplicate.png){width="400"}

     Dans la section _[!UICONTROL Propriétés de l’e-mail]_ de la page de contenu de l’e-mail, les champs _[!UICONTROL De l’e-mail]_ et _[!UICONTROL Répondre à l’adresse]_ sont déjà configurés. Vous pouvez saisir des valeurs pour les champs _[!UICONTROL Nom de l’expéditeur]_ et _[!UICONTROL Description]_ (facultatif).

     Définissez l’e-mail [paramètres](#define-the-email-settings) et cliquez sur **[!UICONTROL Modifier le contenu de l’e-mail]** pour [concevoir le contenu](./email-authoring.md).

     <!-- +++New email {#new-email}
     When you want to create an email using an empty canvas or an email template, use the _[!UICONTROL New email]_ option. 

     1. In the dialog, choose **[!UICONTROL New email]**.

     1. Enter a unique **[!UICONTROL Name]** for the email and a **[!UICONTROL Subject line]**.

        ![Create new email dialog - new email](assets/create-new-email.png){width="400"}

     1. Click **[!UICONTROL Create]**.

       In the _[!UICONTROL Email properties]_ section of the email content page, the _[!UICONTROL From email]_ and _[!UICONTROL Reply to address]_ fields are already configured. You can enter values for the _[!UICONTROL From name]_ and _[!UICONTROL Description]_ (optional) fields.

     1. Click **[!UICONTROL Edit email]** to define the email [settings](#define-the-email-settings) and design the [content](./email-authoring.md).

     +++

     +++Duplicate existing email {#duplicate-email}
     When you want to create an email using an existing email from the current journey or from another journey, use the Duplicate existing journey option. You can make changes to the duplicated email according to your objective for the journey node.

     1. In the dialog, choose **[!UICONTROL Duplicate existing email]**.

     1. For **[!UICONTROL Existing email to duplicate]**, click the _Select email_ icon and select the email you want to duplicate and use for the journey node.

      You can filter the list of emails by entering a text string in the search field to match the email name.

      ![Select email](assets/create-new-email-duplicate-select-email.png){width="600" zoomable="yes"}

      Select the checkbox for the email that you want to duplicate and click **[!UICONTROL Select]**. 

     1. Enter a unique **[!UICONTROL Name]** for the email and a **[!UICONTROL Subject line]**.

        ![Create new email dialog - duplciate existing email](assets/create-new-email.png){width="400"}

     1. Click **[!UICONTROL Create]**.

        In the _[!UICONTROL Email properties]_ section of the email content page, the _[!UICONTROL From email]_ and _[!UICONTROL Reply to address]_ fields are already configured. You can enter values for the _[!UICONTROL From name]_ and _[!UICONTROL Description]_ (optional) fields.

     1. If needed, click **[!UICONTROL Edit email]** to modify the email [settings](#define-the-email-settings) and [content](./email-authoring.md).

     +++
   —>
   * Choisissez **[!UICONTROL Sélectionner un e-mail dans Adobe Marketo Engage]** pour utiliser l’un des e-mails précréés dans Marketo Engage et l’envoyer dans le cadre du parcours.

     ![Sélectionner l’e-mail Marketo Engage](./assets/email-select-marketo.png){width="500" zoomable="yes"}

     Avec cette option, le nœud est défini et le contenu de l’e-mail n’a pas besoin d’être défini davantage dans le parcours.

## Définition des paramètres d’e-mail

Une fois l’onglet **[!UICONTROL Détails]** sélectionné dans le panneau _Résumé_ à droite, faites défiler l’écran vers le bas pour afficher et définir les options d’e-mail.

![Paramètres de messagerie](./assets/email-summary-details-settings.png){width="600" zoomable="yes"}

| Option | Description |
| ------ | ----------- |
| [!UICONTROL À partir du nom] | Nom de l’expéditeur utilisé dans l’en-tête de l’e-mail. Saisissez le nom de l’expéditeur tel que vous souhaitez qu’il apparaisse au destinataire. Cliquez sur l’icône _Personnaliser_ ( ![Icône Personnaliser](../assets/do-not-localize/icon-personalize.svg) ) pour utiliser un jeton de personnalisation dans le champ. |
| [!UICONTROL E-mail de l’expéditeur] | Adresse expéditeur utilisée dans l’en-tête de l’e-mail. La valeur par défaut est renseignée à partir des [ paramètres de diffusion du canal e-mail ](../admin/configure-channels-emails.md#delivery-settings). Cliquez sur l’icône _Personnaliser_ ( ![Icône Personnaliser](../assets/do-not-localize/icon-personalize.svg) ) pour utiliser un jeton de personnalisation dans le champ. |
| [!UICONTROL  Adresse de réponse ] | Adresse expéditeur utilisée dans l’en-tête de l’e-mail. La valeur par défaut est renseignée à partir des [paramètres de diffusion du canal e-mail](../admin/configure-channels-emails.md#delivery-settings) ([!UICONTROL libellé de l’expéditeur]). Saisissez l’adresse e-mail à renseigner si le destinataire utilise la fonction de réponse (il peut s’agir d’une adresse différente ou identique à l’adresse expéditeur). Cliquez sur l’icône _Personnaliser_ ( ![Icône Personnaliser](../assets/do-not-localize/icon-personalize.svg) ) pour utiliser un jeton de personnalisation dans le champ. |
| [!UICONTROL Objet] | Texte affiché dans le champ Objet de l’e-mail. La valeur par défaut est renseignée à partir du texte que vous avez saisi dans la boîte de dialogue _[!UICONTROL Créer un e-mail]_. Vous pouvez modifier le texte si nécessaire. Cliquez sur l’icône _Personnaliser_ ( ![Icône Personnaliser](../assets/do-not-localize/icon-personalize.svg) ) pour utiliser un jeton de personnalisation dans le champ.<!-- Click the AI Assistant button ( ![AI Assistant icon](../../assets/do-not-localize/icon-gen-ai.svg){width="30" zoomable="no"} ) to generate the subject line based on the current email content.--> |
| [!UICONTROL &#x200B; E-mail opérationnel &#x200B;] | Cochez la case si vous souhaitez désigner l’e-mail comme opérationnel. Les e-mails opérationnels sont exclus des listes de désinscription et des limites de communication. Sélectionnez cette option uniquement lorsque le destinataire ne peut pas considérer l’e-mail comme un message commercial non sollicité (SPAM). |
| [!UICONTROL Inclure l’affichage en tant que page web] | Cochez la case pour inclure un lien vers une page web générée à partir du contenu de l’e-mail. Les e-mails disposent de fonctionnalités plus limitées que les pages web. Ils sont donc utiles pour JavaScript, les feuilles CSS étendues et les formulaires. Le texte utilisé pour générer le lien est configuré dans les [paramètres de diffusion du canal e-mail](../admin/configure-channels-emails.md#delivery-settings) ([!UICONTROL Afficher en tant qu&#39;HTML de page web] et [!UICONTROL Afficher en tant que texte de page web]). |
| [!UICONTROL Désactiver le suivi des ouvertures] | Cochez la case lorsque vous ne souhaitez pas suivre l’activité d’ouverture des e-mails. Lorsque la fonction est désactivée, le nombre d’activités d’ouverture d’e-mail est incrémenté uniquement lorsqu’une personne unique ouvre l’e-mail. Vous pouvez [gérer le suivi des liens de contenu d’e-mail](./email-authoring.md#content-authoring---link-tracking) lorsque vous concevez le contenu du corps de l’e-mail. |
| [!UICONTROL Preheader] | Cochez la case pour inclure un pré-titre. Un pré-titre est le texte de résumé court affiché après la ligne d&#39;objet dans certains clients de messagerie. Il fournit généralement un bref résumé de l’e-mail et se compose généralement d’une seule phrase. Saisissez le texte récapitulatif dans le champ<!-- , or click the AI Assistant button ( ![AI Assistant icon](../../assets/do-not-localize/icon-gen-ai.svg){width="30" zoomable="no"} ) to generate summary text based on the current email content -->. |
| [!UICONTROL Champs utilisés comme adresses CC] | Le cas échéant, sélectionnez jusqu’à 25 champs Lead ou Société configurés dans Marketo Engage à l’aide du type de `Email`. |

## Vérifier les alertes

Lorsque vous concevez le contenu de votre e-mail, des alertes s’affichent dans l’interface (en haut à droite de la page) lorsque des paramètres clés sont manquants. Si ce bouton ne s’affiche pas, aucun problème n’est détecté.

![Alertes par e-mail](./assets/email-alerts.png){width="600" zoomable="yes"}

Deux types d’alertes peuvent être détectés :

* **_avertissements_** qui se rapportent aux recommandations et aux bonnes pratiques telles que :

   * `The opt-out link is not present in the email body` : une bonne pratique consiste à ajouter un lien de désinscription dans le corps de votre e-mail.

     >[!NOTE]
     >
     >Les e-mails de style marketing doivent inclure un lien d’opt-out, qui n’est pas obligatoire pour les messages transactionnels.

   * `Text version of HTML is empty` : n’oubliez pas de définir une version texte du corps de votre email, qui est utilisée lorsque le contenu HTML ne peut pas être affiché.

   * `Empty link is present in email body` : vérifiez que tous les liens de votre e-mail sont corrects.

   * `Email size has exceeded the limit of 100KB` : pour une diffusion optimale, veillez à ce que la taille de votre e-mail ne dépasse pas 100KB.

* **_Erreurs_** qui vous empêchent de tester ou d’activer le parcours/la campagne tant qu’elles ne sont pas corrigées, telles que :

   * `The subject line is missing` : l’objet de l’e-mail est obligatoire.

   * `The email version of the message is empty` : cette erreur s’affiche lorsque le contenu de l’e-mail n’a pas été configuré.
