---
title: Canal e-mail
description: 'Ajouter des nœuds d’action e-mail aux parcours de compte : créez des e-mails ou utilisez les e-mails Marketo Engage existants pour les communications ciblées dans Journey Optimizer B2B edition.'
feature: Email Authoring, Account Journeys
role: User
autotag-review: '2026-06-18T20:30:25.418Z'
TQID: 'https://experienceleague.adobe.com/K3OZnLvtSdwSq6AT4JlRQ62t32d6smIJ4K9EEnK-QUc'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 0a877cc1fc0dfd9c3d8271c8f7be6a5e34a69a9a
workflow-type: tm+mt
source-wordcount: 881
ht-degree: 4%

---

# Canal e-mail

[!DNL Adobe Journey Optimizer B2B Prime] offre aux spécialistes du marketing B2B une expérience moderne de création et de diffusion d’e-mails de niveau entreprise. Cette version introduit des outils de conception d’e-mail repensés et un ensemble complet de contrôles de délivrabilité des e-mails.

>[!NOTE]
>
>Si vous envoyez un e-mail pour la première fois, assurez-vous que le [canal e-mail et délivrabilité](../admin/configuration-email-deliverability.md) est configuré.

## Présentation du canal e-mail {#overview}

* **Configurations du canal e-mail** - Gérez l’identité de l’expéditeur, le comportement de réponse, les types de messages marketing par rapport aux messages transactionnels et le suivi.
* **Contrôles de délivrabilité des e-mails** - Configurez votre canal de délivrabilité des e-mails, y compris la délégation de sous-domaines (méthodes Fully Delegated et CNAME), DMARC, la configuration automatique SPF/DKIM et la prise en charge du pool d’adresses IP partagées.
* **Action Envoyer un e-mail** - À partir d’un parcours, ajoutez un nœud d’action _Envoyer un e-mail_, y compris la personnalisation à l’aide d’attributs de profil (syntaxe Handlebars).
* **Outils visuels de conception d’e-mail par glisser-déposer** - Concevez le contenu de votre e-mail avec des structures, des composants de contenu, des thèmes, une prise en charge du mode sombre et des fragments visuels réutilisables.
* **Ressources Marketo Design Studio** — Sélectionnez des images et des ressources à partir d’une copie ponctuelle de votre bibliothèque de ressources Marketo Engage directement dans la zone de travail d’e-mail.
* **Modèles et fragments réutilisables** — Enregistrez les en-têtes, pieds de page, CTA et dispositions complètes d&#39;e-mail courants et réutilisez-les dans les parcours.
* **Contrôle d’accès en fonction du rôle (RBAC)** — Appliquez des autorisations granulaires pour créer, modifier, approuver et envoyer des e-mails.

## Principaux concepts {#key-concepts}

Avant de créer des e-mails pour les parcours de personne et de créer du contenu d’e-mail, passez en revue les concepts suivants :

| Concept | Dans [!DNL Journey Optimizer B2B Prime] Prime |
| ------- | ---------------------- |
| **_Espace de conception des emails_** | Canevas visuel et outils de conception utilisés pour composer du contenu d’e-mail. Il comprend des composants de disposition à glisser-déposer, des modèles, des fragments, des thèmes et un éditeur de personnalisation. |
| **_Modèle_** | Disposition d’e-mail réutilisable disponible pour la création d’un e-mail. Il peut s’agir d’un modèle type intégré fourni par Adobe ou d’un modèle personnalisé créé par votre équipe. |
| **_Fragment visuel_** | Bloc de contenu réutilisable (par exemple, en-tête, pied de page, CTA, clause de non-responsabilité) pouvant être inséré dans plusieurs e-mails. La mise à jour d’un fragment propage la modification à chaque e-mail qui l’utilise. |
| **_Thème_** | Paramètre prédéfini de style réutilisable (couleurs, typographie, espacement, styles de bouton) appliqué à un e-mail. |
| **_Jeton_** | Une expression Handlebars, par exemple `{{profile.firstName}}`, résolue au moment de l’envoi à l’aide des données de profil de chaque destinataire. |
| **_Action Envoyer un e-mail_** | Nœud d’action de parcours qui utilise une configuration de canal et du contenu d’e-mail pour diffuser un e-mail. |

## Ajout d’un e-mail à partir d’un parcours

Pour envoyer un e-mail à partir d’un parcours, ajoutez un nœud _Prendre une action_ et configurez-le pour envoyer un e-mail.

1. Dans la zone de travail de parcours, cliquez sur l’icône **+** et sélectionnez **[!UICONTROL Effectuer une action]**.

1. Dans les propriétés de nœud sur la droite, définissez l’action sur **[!UICONTROL Envoyer un e-mail]**.

   ![Agir - Envoyer un e-mail](./assets/person-action-node-send-email.png){width="450"}

1. Choisissez la source de l’e-mail :

   * **Créer/modifier un e-mail** - Sélectionnez cette option pour définir le contenu de l’e-mail, y compris l’objet, les informations de l’expéditeur et le corps de l’e-mail dans l’espace de conception d’e-mail.

   * **[!UICONTROL Utiliser un e-mail personnalisé par l’IA]** - Sélectionnez cette option pour affiner un e-mail généré par l’IA dans l’espace de conception d’e-mail. Ces e-mails sont optimisés de sorte que les clients de boîte de réception assistés par l’IA fondent leurs résumés et leurs réponses dans vos offres et appels à l’action.

1. Cliquez sur **[!UICONTROL Créer un e-mail]**.

1. Dans la boîte de dialogue _[!UICONTROL Créer un e-mail]_, saisissez un **[!UICONTROL Nom]** unique (obligatoire) et un **[!UICONTROL Description]** (facultatif).

1. Cliquez sur **[!UICONTROL Créer]**.

## Définir les propriétés et les actions de l’e-mail

1. Une fois le nœud _[!UICONTROL Envoyer un e-mail]_ sélectionné dans la zone de travail du parcours, cliquez sur **[!UICONTROL Modifier l’e-mail]** dans les propriétés du nœud à droite.

<!-- Staging environment broken -->

pour l’e-mail et une **[!UICONTROL ligne d’objet]**.

L’onglet **[!UICONTROL Actions]** s’ouvre, dans lequel vous pouvez sélectionner ou créer la configuration d’e-mail à utiliser.

1. (Facultatif) Sélectionnez un ensemble de règles dans Règles de gestion pour appliquer des règles de limitation à votre action e-mail.

Vous pouvez utiliser l’option [Optimisation de l’heure d’envoi](./email-send-time-optimization.md) pour prévoir la meilleure heure d’envoi du message afin d’optimiser l’engagement en fonction des taux historiques d’ouverture et de clic. Voici comment procéder

Sélectionnez le bouton Modifier le contenu et créez votre contenu selon vos besoins à l’aide du Designer d’e-mail.

Revenez à la zone de travail parcours. Si nécessaire, complétez votre flux de parcours en faisant glisser et en déposant des actions ou des événements supplémentaires.

Pour plus d’informations sur la création, la configuration et la publication d’un parcours, consultez cette page.


### Définir les paramètres d’e-mail {#email-settings}

Configurez les paramètres dans l’onglet **[!UICONTROL Détails]** du panneau de résumé du nœud.

| Paramètre | Description |
| ------- | ----------- |
| **[!UICONTROL À partir du nom]** | Nom de l’expéditeur affiché dans l’en-tête de l’email. Prend en charge les jetons de personnalisation. |
| **[!UICONTROL E-mail de l’expéditeur]** | Adresse e-mail de l’expéditeur. La valeur par défaut est issue de la configuration du canal. Prend en charge la personnalisation. |
| **[!UICONTROL Adresse de réponse]** | Adresse qui reçoit les réponses des destinataires. Prend en charge la personnalisation. |
| **[!UICONTROL Objet]** | Objet de l’e-mail. Modifiable à partir de la valeur saisie lors de la création. |
| **[!UICONTROL Domaine de branding]** | Domaine utilisé pour l’envoi spécifique à la marque. |
| **[!UICONTROL Adresse IP dédiée]** | Adresse IP spécifique pour le tracking de la délivrabilité. |
| **[!UICONTROL E-mail opérationnel]** | Lorsqu’elle est activée, contourne la suppression du processus d’opt-out et du désabonnement. À utiliser uniquement pour les messages opérationnels légitimes. |
| **[!UICONTROL Inclure l’affichage en tant que page web]** | Génère un lien vers une page web pour le contenu de l’e-mail. |
| **[!UICONTROL Désactiver le suivi des ouvertures]** | Empêche le suivi de l’activité d’ouverture des e-mails. |
| **[!UICONTROL Preheader]** | Texte de résumé court affiché après la ligne d’objet dans les aperçus de boîte de réception. |
| **[!UICONTROL Adresses CC]** | Ajoutez jusqu’à 25 champs d’e-mail de prospect ou d’entreprise pour recevoir une copie. |

### Vérifier les alertes {#alerts}

[!DNL Journey Optimizer B2B Prime] fait apparaître les problèmes dans le coin supérieur droit de l’éditeur d’e-mail. Résolvez toutes les erreurs avant d’activer le parcours ; les avertissements ne sont que des recommandations.

**Erreurs** (empêcher l’activation du parcours) :

* Le nom de l’expéditeur est vide
* Objet manquant
* Le contenu de l’e-mail est vide

**Avertissements** (recommandations) :

* Le lien d’exclusion n’est pas présent dans le corps de l’e-mail.
* La version texte d’HTML est vide.
* Liens vides détectés
* E-mail dépasse 100 000
