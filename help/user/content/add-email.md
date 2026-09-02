---
title: Ajouter un e-mail à votre Parcours
description: Pour un nœud d’action Envoyer un e-mail dans un parcours, créez des e-mails ou dupliquez des e-mails existants à utiliser pour les communications ciblées dans Journey Optimizer B2B edition.
feature: Email Authoring, Account Journeys
role: User
exl-id: 21a6ce0f-b59d-4be2-abc3-fda5c6a6334f
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: beb7a3c1-66ab-4786-b879-7621375b3c40
autotag-review: 2026-03-30T22:38:56.688Z
TQID: https://experienceleague.adobe.com/8poXn9D7fkr-5yQBUn3dAxV0izKGfW-U8Qf0gG4aRWw
source-git-commit: f67a6703d32e133be7c3422e1d5ceb6099da849e
workflow-type: tm+mt
source-wordcount: 1042
ht-degree: 0%

---

# Ajouter un e-mail à votre parcours

Utilisez Adobe Journey Optimizer B2B edition pour envoyer des e-mails à vos clients par le biais de parcours de compte. Vous pouvez choisir de créer, de personnaliser et de prévisualiser des messages dans l’espace de conception d’e-mail. Une fois que les e-mails sont en ligne dans parcours, surveillez l’envoi, la diffusion et l’engagement dans le rapport [&#x200B; Performances des e-mails &#x200B;](../dashboards/email-performance-dashboard.md).

>[!NOTE]
>
>Si vous envoyez un e-mail pour la première fois, assurez-vous que le canal e-mail est configuré. Pour en savoir plus, voir [Protocoles de tracking et de diffusion e-mail](../start/email-protocols.md).
>
>Pour plus d’informations sur l’évaluation des préférences de consentement des e-mails au moment de la diffusion, voir [&#x200B; Préférences de consentement &#x200B;](./channels-consent-preferences.md).

## Ajouter un nœud d’action d’envoi d’e-mail {#send-email-node}

Vous pouvez configurer des diffusions e-mail dans un parcours lorsque vous [ajoutez un nœud _[!UICONTROL Prendre une action]_ &#x200B;](../journeys/action-nodes.md) et que vous effectuez les opérations suivantes :

1. _(parcours de compte uniquement)_ Pour la cible _[!UICONTROL Action sur]_, choisissez **[!UICONTROL Personnes]**.

1. Pour l’action, choisissez **[!UICONTROL Envoyer un e-mail]**.

1. Cliquez sur **[!UICONTROL Créer un e-mail]**.

   ![Agir - Envoyer un e-mail](assets/journey-node-send-email.png){width="500"}

1. Dans la boîte de dialogue _Créer un e-mail_, choisissez de créer une ressource de contenu d’e-mail ou de dupliquer une ressource de contenu d’e-mail existante.

   * Choisissez l’option **[!UICONTROL Nouvel e-mail]** lorsque vous souhaitez créer un e-mail à l’aide d’une zone de travail vide ou d’un modèle d’e-mail.

     ![Boîte de dialogue Créer un e-mail - Nouvel e-mail](assets/create-new-email.png){width="400"}

     * Saisissez un **[!UICONTROL Nom]** unique pour l’e-mail et un **[!UICONTROL Objet]**.

     * Cliquez sur **[!UICONTROL Créer]**.

   * Choisissez l’option **[!UICONTROL Dupliquer l’e-mail existant]** lorsque vous souhaitez créer un e-mail à partir d’un e-mail existant du parcours actuel ou d’un autre parcours.

     Vous pouvez apporter des modifications à l’e-mail dupliqué en fonction de votre objectif pour le nœud de parcours.

     * Pour **[!UICONTROL E-mail existant à dupliquer]**, cliquez sur l’icône _Sélection_ ( ![Icône de sélection](../assets/do-not-localize/icon-email-select.svg) ) et sélectionnez l’e-mail à dupliquer et à utiliser pour le nœud de parcours.

       Vous pouvez filtrer la liste des e-mails en saisissant une chaîne de texte dans le champ de recherche pour correspondre au nom de l’e-mail. Cochez la case de l’e-mail à dupliquer et cliquez sur **[!UICONTROL Sélectionner]**.

       ![Sélectionner un e-mail](assets/create-new-email-duplicate-select-email.png){width="600" zoomable="yes"}

     * Saisissez un **[!UICONTROL Nom]** unique pour l’e-mail et un **[!UICONTROL Objet]**.

       ![Boîte de dialogue Créer un e-mail - Dupliquer l’e-mail existant](assets/create-new-email-duplicate.png){width="400"}

     * Cliquez sur **[!UICONTROL Créer]**.

1. Cliquez sur **[!UICONTROL Modifier l’e-mail]** pour définir l’e-mail [paramètres](#email-settings) et [contenu](./email-authoring.md).

   ![Nœud de parcours Envoyer un e-mail - Modifier l’e-mail](assets/journey-node-send-email-edit-email.png){width="500"}

## Définition des paramètres d’e-mail {#email-settings}

Une fois l’onglet **[!UICONTROL Détails]** sélectionné dans le panneau _Résumé_ à droite, faites défiler l’écran vers le bas pour afficher et définir les paramètres de l’e-mail.

![Paramètres de messagerie](./assets/email-summary-details-settings.png){width="700" zoomable="yes"}

| Option | Description |
| ------ | ----------- |
| [!UICONTROL À partir du nom] | Nom de l’expéditeur utilisé dans l’en-tête de l’e-mail. Saisissez le nom de l’expéditeur tel que vous souhaitez qu’il apparaisse au destinataire. Cliquez sur l’icône _Personnaliser_ ( ![Icône Personnaliser](../assets/do-not-localize/icon-personalize.svg) ) pour utiliser un jeton de personnalisation dans le champ. |
| [!UICONTROL E-mail de l’expéditeur] | Adresse expéditeur utilisée dans l’en-tête de l’e-mail. La valeur par défaut est renseignée à partir des [&#x200B; paramètres de diffusion du canal e-mail &#x200B;](../admin/configure-channels-emails.md#delivery-settings). Cliquez sur l’icône _Personnaliser_ ( ![Icône Personnaliser](../assets/do-not-localize/icon-personalize.svg) ) pour utiliser un jeton de personnalisation dans le champ. |
| [!UICONTROL &#x200B; Adresse de réponse &#x200B;] | Adresse expéditeur utilisée dans l’en-tête de l’e-mail. La valeur par défaut est renseignée à partir des [paramètres de diffusion du canal e-mail](../admin/configure-channels-emails.md#delivery-settings) ([!UICONTROL libellé de l’expéditeur]). Saisissez l’adresse e-mail à renseigner si le destinataire utilise la fonction de réponse (il peut s’agir d’une adresse différente ou identique à l’adresse expéditeur). Cliquez sur l’icône _Personnaliser_ ( ![Icône Personnaliser](../assets/do-not-localize/icon-personalize.svg) ) pour utiliser un jeton de personnalisation dans le champ. |
| [!UICONTROL Objet] | Texte affiché dans le champ Objet de l’e-mail. La valeur par défaut est renseignée à partir du texte que vous avez saisi dans la boîte de dialogue _[!UICONTROL Créer un e-mail]_. Vous pouvez modifier le texte si nécessaire. Cliquez sur l’icône _Personnaliser_ ( ![Icône Personnaliser](../assets/do-not-localize/icon-personalize.svg) ) pour utiliser un jeton de personnalisation dans le champ.<!-- Click the AI Assistant button ( ![AI Assistant icon](../../assets/do-not-localize/icon-gen-ai.svg){width="30" zoomable="no"} ) to generate the subject line based on the current email content.--> |
| [!UICONTROL Domaine de branding] | Si plusieurs domaines de branding [&#x200B; sont définis dans le système](../admin/configure-channels-emails.md#branding-domains) sélectionnez le domaine de branding à utiliser pour envoyer l’e-mail. Utilisez un domaine de marque spécifique pour envoyer des e-mails qui semblent provenir de votre marque plutôt que de la société dans son ensemble. Il établit la confiance avec la marque, personnalise l’expérience par e-mail et augmente les taux d’ouverture et de réponse. |
| [!UICONTROL &#x200B; E-mail opérationnel &#x200B;] | Cochez la case si vous souhaitez désigner l’e-mail comme opérationnel. Les e-mails opérationnels sont exclus des listes de désinscription et des limites de communication. Sélectionnez cette option uniquement lorsque le destinataire ne peut pas considérer l’e-mail comme un message commercial non sollicité (SPAM). |
| [!UICONTROL Inclure l’affichage en tant que page web] | Cochez la case pour inclure un lien vers une page web générée à partir du contenu de l’e-mail. Les e-mails disposent de fonctionnalités plus limitées que les pages web. Ils sont donc utiles pour JavaScript, les feuilles CSS étendues et les formulaires. Le texte utilisé pour générer le lien est configuré dans les [paramètres de diffusion du canal e-mail](../admin/configure-channels-emails.md#delivery-settings) ([!UICONTROL Afficher en tant qu&#39;HTML de page web] et [!UICONTROL Afficher en tant que texte de page web]). |
| [!UICONTROL Désactiver le suivi des ouvertures] | Cochez la case lorsque vous ne souhaitez pas suivre l’activité d’ouverture des e-mails. Lorsque la fonction est désactivée, le nombre d’activités d’ouverture d’e-mail est incrémenté uniquement lorsqu’une personne unique ouvre l’e-mail. Vous pouvez [gérer le suivi des liens de contenu d’e-mail](./email-authoring.md#edit-linked-url-tracking) lorsque vous concevez le contenu du corps de l’e-mail. |
| [!UICONTROL Preheader] | Cochez la case pour inclure un pré-titre. Un pré-titre est le texte de résumé court affiché après la ligne d&#39;objet dans certains clients de messagerie. Il fournit généralement un bref résumé de l’e-mail et se compose généralement d’une seule phrase. Saisissez le texte récapitulatif dans le champ<!-- , or click the AI Assistant button ( ![AI Assistant icon](../../assets/do-not-localize/icon-gen-ai.svg){width="30" zoomable="no"} ) to generate summary text based on the current email content -->. |

<!-- 
Removed, but may reappear elsewhere
| [!UICONTROL Dedicated IP] | If you have more than one dedicated IP addresses defined, select a dedicated IP address to use for sending the email. When you use a specific dedicated IP for your programs, you can track and monitor deliverability more closely and respond quickly to any changes in your delivery metrics. For more information about adding a dedicated IP for the connected Marketo Engage instance, refer to the [Marketo Engage documentation](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/deliverability/use-your-dedicated-ip-addresses-to-send-emails){target="_blank"}.|
| [!UICONTROL Fields used as CC addresses] | If available, select up to 25 Lead or Company fields that are set up in Marketo Engage using the `Email` type.  |
-->

## Vérifier les alertes {#check-alerts}

Lorsque vous définissez le contenu et les paramètres de votre e-mail, des alertes s’affichent dans l’interface (en haut à droite de la page) lorsque des paramètres clés sont manquants. Si ce bouton ne s’affiche pas, aucun problème n’est détecté.

![Alertes par e-mail](./assets/email-alerts.png){width="600" zoomable="yes"}

Il existe deux types d’alertes :

* **_avertissements_** qui se rapportent aux recommandations et aux bonnes pratiques telles que :

  * `The opt-out link is not present in the email body` : une bonne pratique consiste à ajouter un lien de désabonnement dans le corps de votre e-mail.

    >[!NOTE]
    >
    >Les e-mails de style marketing doivent inclure un lien d’opt-out, qui n’est pas obligatoire pour les messages transactionnels.

  * `Text version of HTML is empty` : définissez une version texte du corps de votre e-mail, qui est utilisée lorsque le contenu HTML ne peut pas être affiché.

  * `Empty link is present in email body` : vérifiez que tous les liens de votre e-mail sont corrects.

  * `Email size has exceeded the limit of 100KB` : pour une diffusion optimale, veillez à ce que la taille de votre e-mail ne dépasse pas 100KB.

* **_Erreurs_** qui vous empêchent de tester ou d’activer le parcours/la campagne tant qu’elles ne sont pas corrigées, telles que :

  * `From name is empty` : le champ e-mail _De_ (obligatoire) n’est pas défini.

  * `The subject line is missing` : l’objet de l’e-mail (obligatoire) n’est pas défini.

  * `The email version of the message is empty` : le contenu de l’e-mail n’est pas défini.
