---
title: Qualificateur de vente
description: Découvrez comment utiliser l’application Qualificateur des ventes pour accélérer et gérer vos parcours.
feature: Account Journeys, AI Assistant
role: User
source-git-commit: 8fb86fe3434a5acdec6fd638fad571a0bc901884
workflow-type: tm+mt
source-wordcount: '1316'
ht-degree: 1%

---


# Qualificateur de vente

>[!NOTE]
>Cette fonctionnalité est actuellement en disponibilité limitée et n’est pas disponible pour tous les utilisateurs et utilisatrices.
>

Le qualificateur de vente est une application complémentaire pilotée par l’IA pour Adobe Journey Optimizer B2B edition qui contient le Account Qualification Agent et qui est conçue pour rationaliser les workflows pour les représentants au développement commercial (BDR). Le qualificateur de vente automatise les workflows de qualification des prospects, de sensibilisation et d’engagement des acheteurs sur l’ensemble des canaux, réduisant la charge manuelle de BDR et accélérant la vitesse du pipeline pour les entreprises B2B.
Utilisez le navigateur et les modules externes d’e-mail pour accéder à Business Intelligence directement dans les CRM ou Outlook.

Le qualificateur de vente est inclus dans AJO B2B, mais il s’agit d’une application distincte dans AEP Experience Cloud.

![Page d’accueil du qualificateur de vente](assets/home-screen.png)

## Agent Account Qualification

Le Account Qualification Agent (AQA) est au cœur du qualificateur de vente. L’AQA utilise l’IA pour lire vos comptes et déterminer lesquels sont prêts pour l’étape suivante.  Il aide à la recherche, à la rédaction de courriers électroniques et aux mises à jour CRM.

![Account Qualification Agent](assets/acc-qualification-agent.png)

* **Recherche de prospects**

  Effectuez des recherches de prospects en utilisant la récupération et l&#39;affichage automatiques des informations clés sur les prospects (telles que la fonction, les engagements récents, l&#39;appartenance à un groupe d&#39;achat) pour fournir une image complète en quelques secondes.

* **Étude de compte**

  Effectuez des recherches sur les comptes à l’aide de la récupération et de l’affichage automatiques d’informations détaillées sur l’organisation d’un prospect. Ces informations comprennent les informations vitales de l’entreprise, les actualités récentes, les priorités stratégiques et les membres les plus engagés.

* **Brouillons d’e-mails**

  Générez des brouillons d’e-mails en synthétisant les recherches des prospects et des informations de compte afin de produire du contenu d’e-mail unique pertinent et personnalisé en fonction de l’objectif du rapport BDR.

* **E-mails relatifs au plan d’engagement**

  Créez des brouillons d’e-mails de plan d’engagement personnalisés pour chaque étape d’une cadence de sensibilisation définie par BDR, en veillant à ce que la séquence entière soit personnalisée

### Utilisation de base

Les agents de l’IA d’Adobe utilisent _requêtes en langage naturel_, ce qui signifie qu’ils utilisent la même langue dans l’invite de texte que vous le feriez en parlant à une personne. Plus vous êtes détaillé, meilleurs sont les résultats.

En utilisant le langage naturel, vous pouvez demander à l’agent de :

* Afficher mes prospects affectés sans encore engagement
* Me montrer toutes mes pistes qui ne font pas partie d’un engagement autonome
* Donnez-moi un résumé détaillé des `<company>`, y compris leur groupe d&#39;achat, les signaux d&#39;intention récents et nos engagements passés.

Vous pouvez immédiatement comprendre quels comptes et prospects sont les plus actifs et afficher la plus haute intention, de sorte que vous pouvez concentrer votre énergie là où elle a le plus d&#39;impact.

Effectuez une itération sur votre parcours en affinant vos invites pour obtenir les résultats dont vous avez besoin. Par exemple :

* Rédigez un e-mail de relance à partir du contexte, comme des appels de rémunération ou des rapports. Jusqu’à 120 mots. Objet : Captivant, intégrant un thème clé. Introduction : crochet avec citation directe de sources de contexte. Corps : permet de se connecter aux points faibles et aux propositions de valeur. CTA : proposez un bref appel pour en savoir plus.

* L’objectif de cet e-mail est de commencer une conversation et de renforcer votre crédibilité. Rédigez un e-mail de 120 mots, au ton consultatif et empathique. Veillez à éviter une approche trop familière ou commerciale et à ne pas utiliser les expressions « j&#39;espère que vous allez bien », « je vous demande simplement de vous enregistrer » ou « s&#39;il vous plaît ».

## Prospects

Cette fenêtre répertorie tous les prospects auxquels vous avez accès. Il est rapide de vérifier des éléments tels que le statut du lead et la dernière activité.

![Voir tous vos prospects dans le tableau Prospects](assets/prospects.png)

Cliquez sur l’icône Filtrer ![icône Filtrer](../assets/icon-filter.png) pour filtrer par statut de prospect.

## Plans d’engagement

Cette fenêtre fournit des détails sur les plans d&#39;engagement définis.

![Plans d’engagement](assets/engagement-plans.png)

Pour créer un plan d’engagement, cliquez sur **[!UICONTROL Créer un plan d’engagement]**.

1. À l’étape Détails , indiquez un nom et une description facultative. Cliquez sur **[!UICONTROL Enregistrer et continuer]**.
1. À l’étape Sélectionner les prospects, sélectionnez les prospects qui doivent appartenir à ce plan.
1. À l’étape Définir le rythme, définissez les paramètres du plan.
1. À l’étape Aperçu , assurez-vous que tout fonctionne comme prévu.

## Boîte d’envoi d’e-mail

Le panneau Boîte d’envoi d’e-mail répertorie tous les e-mails automatisés que vous avez envoyés.

## Réservation de réunion

Ce panneau affiche toutes les réunions configurées par automatisation.

## Boîte de réception de conversation

Ce panneau affiche tous vos threads de conversation.

![Boîte de réception de conversation](assets/chat-inbox.png)

Non seulement vous pouvez interagir avec des clients, mais vous pouvez également voir un résumé du contact et un résumé du thread, de sorte que vous pouvez rapidement savoir où vous vous trouvez dans le thread.

## Intégrations

Avec les intégrations , le qualificateur de vente peut exploiter les CRM et d’autres sources de données pour enrichir les profils client et exploiter les activités de vente :

* Effectuez une intégration à votre boîte de réception e-mail pour suivre les e-mails entrants pertinents et générer des réponses.
* Lire et mettre à jour des données CRM, telles que Salesforce ou Microsoft® Dynamics, ZoomInfo ou Buildwidth.

![Intégration Outlook du qualificateur de vente](assets/outlook.png)

### Configurer une nouvelle intégration

Pour démarrer une nouvelle intégration, cliquez sur **[!UICONTROL Créer une intégration]** en haut à droite.

![Détails de l’intégration](assets/integration-details.png)

Nous définissons ici l’URL de l’intégration et établissons la payload à envoyer.

1. Attribuez un nom unique et une description (facultatif) à l’intégration.
1. Définissez le champ URL sur le point d’entrée d’authentification d’intégration de votre site d’intégration.
1. Dans Paramètres de chemin d’accès, définissez la méthode HTTP .
1. Dans Paramètres d’en-tête , définissez les en-têtes HTTP à envoyer. En règle générale, il s’agit d’un objet JSON envoyé qui nécessite un en-tête de type contenu.
1. Dans Paramètres de requête, définissez les paramètres requis.
1. Sous Authentification, configurez les informations de connexion pour le site d’intégration.

   * Aucune
   * OAuth 2.0
   * Clé API
   * Authentification de base

1. Définissez les valeurs de limitation et de cache dans la section Configuration de la payload .
1. Sous Configuration de la payload, cliquez sur l’icône en forme de crayon. Dans la boîte de dialogue Coller la payload , collez ou saisissez votre objet de payload JSON.
   * Payload de requête : objet JSON contenant des données pour envoyer le site d’intégration.
   * Payload de réponse : structure des données que vous prévoyez d’obtenir en retour.
1. Cliquez sur [!UICONTROL Tester la connexion] pour vous assurer que vos paramètres sont corrects.

Lorsque les paramètres de connexion sont valides, cliquez sur **[!UICONTROL Enregistrer comme brouillon]**.

Lorsque vous êtes de retour sur le tableau Intégrations principal, sélectionnez l’intégration et cliquez sur **[!UICONTROL Activer]** pour activer l’intégration, ou **[!UICONTROL Enregistrer en tant que brouillon]**.



#### Gérer l’accès

Vous pouvez gérer l’accès aux utilisateurs et le type de données partagées avec différents groupes d’utilisateurs.

Cliquez sur **[!UICONTROL Gérer l’accès]** pour ouvrir la boîte de dialogue Gérer l’accès .

Cette boîte de dialogue répertorie tous les libellés qui ont été établis par votre organisation. Sélectionnez les libellés que vous souhaitez appliquer à cette intégration.

Si vous avez besoin d’une nouvelle étiquette, cliquez sur **[!UICONTROL Créer une étiquette]** et renseignez les champs suivants :

* Nom
* Nom convivial
* Description

## Paramètres représentatifs

C&#39;est là que vous entrez les informations vous concernant : les détails personnels, les paramètres d&#39;e-mail et de calendrier, et la disponibilité du chat.

### Détails

L’onglet Détails vous permet de saisir des informations vous concernant :

![Paramètres Détails du qualificateur de vente](assets/details.png)

### Paramètres d’e-mail

Dans l’onglet Paramètres de messagerie , configurez vos connexions par e-mail.

![Paramètres de messagerie](assets/email-settings.png)

#### Connexions aux e-mails

Cliquez sur **[!UICONTROL Connexion]** et suivez la procédure de connexion Microsoft.

#### Signature de l’e-mail

Configurez votre signature d’e-mail utilisée dans les e-mails générés automatiquement.

### Paramètres du calendrier

Dans l&#39;onglet Paramètres du calendrier , définissez votre fuseau horaire et votre disponibilité.

![Paramètres du calendrier](assets/calendar-settings.png)

#### Connexion au calendrier

Cliquez sur **[!UICONTROL Connexion]** et suivez la procédure de connexion Microsoft pour intégrer votre calendrier.

#### E-mail de confirmation de la réunion

Lorsqu’un client confirme une réunion avec vous, il reçoit l’e-mail de confirmation en tant que réponse.
Utilisez ces paramètres pour définir l’objet et le corps de l’e-mail.

#### Préférences

Définissez la durée de votre réunion par défaut et le temps que vous souhaitez entre deux réunions consécutives.

### Paramètres de conversation

Dans cet onglet, définissez la disponibilité de votre fuseau horaire Live Chat.

![Paramètres de conversation](assets/chat-settings.png)

## Gestion représentative

Dans ce panneau, un tableau de tous les représentants définis et de leur statut de calendrier s&#39;affiche.

## Performances de la réunion

Ce panneau présente des analyses autour des réunions terminées.

## Configuration du plug-in Chrome

Le plug-in Chrome de l’assistant AI est disponible sur le [Google Store](https://chromewebstore.google.com/detail/ai-assistant/hancbabllcmckehonngbdkhilocpdfji?authuser=0&hl=en).

Lorsque le plug-in est installé dans Chrome, le logo Adobe s’affiche au milieu à droite lorsque vous vous trouvez sur un site intégré :

* Applications web Adobe
* Salesforce
* Outlook
* Microsoft Dynamics et applications web
* Applications Google

## Modifier la barre de navigation de gauche

En bas à gauche de l’application, cliquez sur **[!UICONTROL Modifier]** pour contrôler laquelle des icônes est visible dans la navigation. Vous pouvez également les faire glisser et les déposer pour les réorganiser selon vos besoins.

## Vidéo de démonstration

La vidéo suivante présente brièvement le qualificateur de vente et le Account Qualification Agent.

>[!VIDEO](https://video.tv.adobe.com/v/3476563?captions=fre_fr)
