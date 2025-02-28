---
title: Groupes d'achat
description: Découvrez comment les groupes d’achats dans Journey Optimizer B2B edition peuvent accroître l’efficacité du marketing en identifiant et en ciblant les membres de vos listes de comptes.
feature: Buying Groups
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: 8b2cfac4785e95e4fb994ac87068f59add40171d
workflow-type: tm+mt
source-wordcount: '1788'
ht-degree: 18%

---


# Groupes d’achat

Pour les activités de vente et de marketing B2B, les comptes sont la clé de toute stratégie. Chaque compte est associé à un groupe de personnes, qui peuvent être des employés du compte ou des sous-traitants qui travaillent avec le compte. Les comptes sont hiérarchiques et différents produits peuvent être vendus à différents niveaux de la hiérarchie. Par exemple, Adobe Experience Platform peut être vendu au niveau de l’entreprise à un compte de niveau supérieur, tandis qu’Adobe Photoshop peut être vendu à un compte qui représente une division ou un service au sein d’une organisation, tel qu’un service de conception au sein d’une grande entreprise.

![Diagramme Rôles de compte](assets/account-roles-diagram.png){width="800"}

Dans le compte, il peut y avoir un sous-ensemble de personnes qui composent le _groupe d’achat_. Ce sont ces personnes qui prennent la décision d’achat. Elles ont donc besoin d’une attention particulière de la part du spécialiste marketing et peuvent avoir besoin de différentes informations qui leur sont fournies par rapport aux autres personnes associées au compte. Les groupes d&#39;achat peuvent comprendre un groupe différent de personnes pour différentes gammes de produits ou offres. Par exemple, un produit de cybersécurité peut généralement nécessiter l’approbation d’un achat par un directeur des systèmes d’information ou un directeur de la sécurité, ainsi que par un représentant du service juridique, mais un produit de suivi des bogues peut généralement compter parmi ses membres un vice-président de l’ingénierie et un directeur informatique.

![Vidéo](../../assets/do-not-localize/icon-video.svg){width="30"} [Regardez la présentation vidéo](#overview-video)

## Composants clés

Vous pouvez accroître l&#39;efficacité du marketing en établissant des groupes d&#39;achat dans Journey Optimizer B2B edition qui identifient les membres manquants pour vos listes de comptes cibles en fonction des solutions que vos équipes commerciales sont chargées de vendre. Avant que vous et votre équipe marketing ne commenciez à créer vos groupes d’achats, assurez-vous que vous avez défini les composants clés. Ces composants sont essentiels pour atteindre les buts et objectifs de votre entreprise.

| Composant | But |
| --------- | ------- |
| Intérêt de la solution | Ce composant fournit la réponse aux questions suivantes : <ul><li>En tant qu&#39;organisation de marketing, que vendez-vous?</li><li>Quels produits ou collections de produits visez-vous à vendre ?</li></ul>  **_Exemple :_** vente croisée de nouveaux produits X à des clients existants |
| Audience (comptes) | Ce composant fournit la réponse aux questions suivantes : <ul><li>À qui vendez-vous ?</li><li>Quelle est la liste des comptes ciblés ?</li></ul> **_Exemple :_** segment de compte défini par des comptes avec le produit Y dont le chiffre d’affaires est supérieur à 1 million |
| Modèles de rôle de groupe d&#39;achat | Ce composant fournit la réponse aux questions suivantes : <ul><li>Quels rôles ciblez-vous ?</li><li>Quel jeu de règles est utilisé pour déterminer qui est affecté à des rôles de groupe d&#39;achat ?</li></ul>  **_Exemple :_** affecter une personne ayant le titre d’administrateur délégué au rôle de décideur |
| Étapes du groupe d’achat | (Facultatif) Ce composant fournit la réponse à la question suivante : comment le groupe d’achats suit-il la progression vers le succès ou l’échec ? |

## Workflow du groupe d’achat

1. Créer des groupes d&#39;achats.

   Options :
   * Utilisez [intérêt de la solution](./solution-interests.md) et [modèle de rôle](./buying-groups-role-templates.md)
   * Utiliser l’import tiers
   * Générer à partir de l’IA/ML

1. Identifier les personnes manquantes.

   Analysez le groupe d&#39;achat à l&#39;aide de filtres.

   **_Exemple :_** le rôle du décideur est manquant et le score d&#39;exhaustivité est &lt; 50

1. Renseignez les définitions des groupes d&#39;achats.
<!--
   * Acquire missing people
   * Send to LinkedIn Destination
   * Enrich with Zoominfo -->

1. Utiliser dans un parcours de compte par le biais de l’intérêt de solution associé.

## Afficher les groupes d&#39;achats et les composants

Dans le volet de navigation de gauche, développez **[!UICONTROL Comptes]** et cliquez sur **[!UICONTROL Groupes d’achat]**.

La page _[!UICONTROL Groupes d&#39;achats]_ est organisée sous forme d&#39;onglets :

| Tabulation | Description |
| --- | ----------- |
| [!UICONTROL Vue d’ensemble] | Cet onglet est le tableau de bord par défaut et affiche le tableau de bord [Groupes d&#39;achats](../dashboards/buying-groups-dashboard.md). |
| [!UICONTROL Parcourir] | Cet onglet prend en charge les activités suivantes : <ul><li>Afficher la liste des groupes d&#39;achats existants. </li><li>Effectuez une recherche par nom de groupe d&#39;achat. </li><li>Filtrez par intérêt de solution. </li><li>Accéder aux détails du groupe d&#39;achat. </li><li>Créez un groupe d&#39;achats. Supprimez un groupe d&#39;achats.</li></ul> |
| [!UICONTROL Centres d’intérêt des solutions] | Cet onglet prend en charge les activités suivantes : <ul><li>Afficher la liste des groupes d&#39;achats existants. </li><li>Effectuez une recherche par nom de groupe d&#39;achat. </li><li>Accédez aux propriétés d’intérêt de la solution et modifiez-les. </li><li>Créez un intérêt pour la solution. </li><li>Supprimez un intérêt de solution. </li><li>Afficher et supprimer des tâches de groupe d&#39;achat. </li></ul> |
| [!UICONTROL Modèles de rôles] | Cet onglet prend en charge les activités suivantes : <ul><li>Afficher la liste des modèles de rôles existants. </li><li>Effectuez une recherche par nom de modèle de rôles. </li><li>Accédez aux propriétés et conditions du modèle de rôles et modifiez-les. </li><li>Créez un modèle de rôles. </li><li>Supprimez un modèle de rôles. </li></ul> |
| [!UICONTROL Étapes] | Cet onglet prend en charge les activités suivantes : <ul><li>Affichez le modèle des étapes de groupes d&#39;achats existants. </li><li>Accédez au modèle de brouillon des étapes du groupe d&#39;achats et modifiez-le. </li><li>Créez le modèle d&#39;étapes du groupe d&#39;achats. </li></ul> |

## Recherche et filtrage des groupes d&#39;achat

Utilisez l&#39;onglet _[!UICONTROL Parcourir]_ pour afficher la liste des groupes d&#39;achats. Vous pouvez effectuer une recherche par nom et filtrer la liste par intérêt de solution.

![Page de navigation du groupe d’achats](assets/buying-groups-browse.png){width="800" zoomable="yes"}

## Détails du groupe d&#39;achat

Pour accéder aux détails d&#39;un groupe d&#39;achats, cliquez sur le nom du groupe d&#39;achats dans l&#39;onglet _[!UICONTROL Parcourir]_. [En savoir plus](./buying-group-details.md)

![Détails du groupe d&#39;achat](assets/buying-group-details.png){width="600" zoomable="yes"}

### Score d&#39;exhaustivité du groupe d&#39;achat

Le score d&#39;exhaustivité est utilisé pour déterminer si le groupe d&#39;achats est complet, ce qui signifie qu&#39;il dispose des membres appropriés affectés aux rôles et qu&#39;il est prêt à être utilisé dans un parcours de compte. Ce score est un pourcentage basé sur le nombre de rôles au sein du groupe d&#39;achat et le nombre de rôles affectés avec au moins un prospect.

Par exemple, s&#39;il existe quatre rôles au sein d&#39;un groupe d&#39;achat et que trois des quatre rôles sont affectés à au moins un prospect, le groupe d&#39;achat est terminé à 75 %.

Le score d&#39;exhaustivité du groupe d&#39;achats est recalculé chaque fois qu&#39;un groupe d&#39;achats est créé ou mis à jour.

### Score d’engagement du groupe d’achat

Le score d’engagement du groupe d’achat est un nombre permettant de déterminer l’engagement des membres d’un groupe d’achat, en fonction des activités qu’ils effectuent.

* Le calcul du score de l&#39;engagement démarre dès que le groupe d&#39;achat est généré.
* Toute activité entrante effectuée par les membres du groupe d&#39;achat au cours des 30 derniers jours est utilisée pour calculer la note.
* Avec une fenêtre de 30 jours et l’expiration des activités, le score pourrait baisser.
* Il existe une limite de fréquence quotidienne de 20 pour chaque activité. Si un membre d&#39;un groupe d&#39;achat effectue la même activité plus de 20 fois par jour, le nombre de l&#39;activité est plafonné à 20 et non à un nombre supérieur.
* Le score affiché est arrondi. Par exemple, un score de 75,89999 s’affiche comme 76.

+++Activités utilisées pour la notation

| Nom de l’activité | Description | Type d’engagement | Nb max de fréquences quotidiennes | Poids de l’activité |
| --- | --- | --- | --- | --- |
| S&#39;inscrire à l&#39;événement | S’enregistre pour un événement associé à une campagne | Événement | 20 | 60 |
| Participer à l&#39;événement | Participe à un événement de campagne | Événement | 20 | 90 |
| Ouvrir e-mail | Ouvre un email | E-mail | 20 | 30 |
| Cliquer sur e-mail | Clique sur un lien dans un e-mail | E-mail | 20 | 30 |
| Ouvrir l&#39;e-mail de vente | Ouvre un e-mail de vente | E-mail | 20 | 30 |
| Cliquer sur l&#39;e-mail de vente | Clique sur un lien dans un e-mail de vente | E-mail | 20 | 30 |
| Moment intéressant | A un moment intéressant | Organisé | 20 | 60 |
| Appuyer sur l’option d’activation des notifications Push | Reçoit une notification push | Mobile | 20 | 30 |
| Activité de l’application mobile | Effectue une activité sur une application mobile | Mobile | 20 | 30 |
| Session de l’application mobile | Est actif sur la session de l’application mobile | Mobile | 20 | 30 |
| Remplir le formulaire de publicités de leads Facebook | Remplit et envoie un formulaire de leads publicitaires sur une page Facebook | Social | 20 | 30 |
| Cliquer sur RTP Appel à l’action | Clics sur un appel à l’action personnalisé | Web | 20 | 60 |
| Afficher le message interne à l’application | Affiche un message in-app | Mobile | 20 | 30 |
| Appuyer sur le message interne à l’application | Appuie sur un message in-app | Mobile | 20 | 30 |
| Abonner aux SMS | S’abonne aux communications SMS | SMS | 20 | 90 |
| Répondre au courrier électronique de vente | Réponses à un email de vente | E-mail | 20 | 30 |
| A pris contact via une boîte de dialogue | S’engage dans une boîte de dialogue Dynamic Chat | Messagerie instantanée | 20 | 90 |
| A interagi avec un document dans la boîte de dialogue | Interagit avec un document dans une boîte de dialogue Dynamic Chat | Messagerie instantanée | 20 | 90 |
| A planifié une réunion dans la boîte de dialogue | Planifie un rendez-vous dans une boîte de dialogue Dynamic Chat | Messagerie instantanée | 20 | 90 |
| A atteint l&#39;objectif du dialogue | Atteint un objectif dans une boîte de dialogue Dynamic Chat |  | 20 | 90 |
| A répondu à un sondage dans le webinaire | Répond à un sondage dans un événement de webinaire | Messagerie instantanée | 20 | 90 |
| A cliqué sur l’appel à l’action dans le webinaire | Clique sur un lien d’appel à l’action dans un événement de webinaire | Appel | 20 | 30 |
| Télécharge la ressource dans le webinaire | Télécharge un fichier/une ressource dans un événement de webinaire | Événement | 20 | 60 |
| Pose des questions dans le webinaire | Pose des questions dans un événement de webinaire | Événement | 20 | 60 |
| A participé à un événement | A participé à un événement | Événement | 20 | 60 |
| A pris contact avec un agent dans la boîte de dialogue | Interagit avec un agent dans une boîte de dialogue Dynamic Chat | Messagerie instantanée | 20 | 90 |
| A cliqué sur le lien dans la conversation de la boîte de dialogue | Clique sur un lien dans une boîte de dialogue Dynamic Chat | Messagerie instantanée | 20 | 90 |
| A interagi avec un flux de conversation | S’engage dans un flux de conversation Dynamic Chat | Messagerie instantanée | 20 | 90 |
| Réunion planifiée dans le flux de conversation | Planifie un rendez-vous dans un flux de conversation Dynamic Chat | Messagerie instantanée | 20 | 90 |
| Objectif du flux de conversation atteint | Atteint un objectif dans un flux conversationnel Dynamic Chat | Messagerie instantanée | 20 | 90 |
| A interagi avec le document dans le flux de conversation | Interagit avec un document dans un flux de conversation Dynamic Chat | Messagerie instantanée | 20 | 90 |
| A pris contact avec un agent dans le flux de conversation | Interagit avec un agent dans un flux de conversation Dynamic Chat | Messagerie instantanée | 20 | 90 |
| A cliqué sur le lien dans le flux de conversation | Clique sur un lien dans un flux de conversation Dynamic Chat | Messagerie instantanée | 20 | 90 |
| Clic sur le lien dans SMS V2 | Clique sur un lien dans un SMS | SMS | 20 | 90 |

>[!NOTE]
>
>Les activités relatives au score de l’engagement sont enregistrées dans le journal d’activité de Marketo Engage [pour une personne](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/managing-people-in-smart-lists/locate-the-activity-log-for-a-person){target="_blank"}.

+++

#### Pondération

Les utilisateurs et utilisatrices peuvent attribuer une _pondération_ à chaque rôle dans le modèle de rôles afin d’attribuer différents poids pour un rôle dans le calcul du score d’engagement.

![Définir la pondération de chaque rôle dans le modèle de rôles](./assets/roles-templates-weighting.png){width="700" zoomable="yes"}

Chaque niveau de pondération se traduit par une valeur, qui est utilisée pour calculer le score d’engagement :

* [!UICONTROL Trivial] = 20
* [!UICONTROL Mineur] = 40
* [!UICONTROL Normal] = 60
* [!UICONTROL Important] = 80
* [!UICONTROL Vital] = 100

Un modèle de rôles avec trois rôles pondérés _[!UICONTROL Essentiel]_, _[!UICONTROL Important]_ et _[!UICONTROL Normal]_ convertit aux pourcentages pondérés suivants :

| Rôle | Pondération | Valeur système | Calcul de la valeur | Pourcentage |
|-------------- |--------- |------------- |------------------ |---------- |
|               |          |              |                   |           |
| Décisionnaire | Vital | 100 | 100/240 | 41,67 % |
| Personne influente | Important | 80 | 80/240 | 33,33 % |
| Praticien | Normal | 60 | 60/240 | 25 % |
|               | Total | 240 |                   |           |

#### Exemple de calcul

L’exemple suivant illustre le calcul du score de l’engagement à l’aide du pourcentage de poids du rôle indiqué, du nombre d’activités entrantes pour chaque membre du groupe d’achat et d’une limite quotidienne de 20 pour chaque événement (s’il s’est produit plusieurs fois).

| Rôle | Membre | Type d’activité | Nombre d’hier | Nombre d’aujourd’hui | Calcul | Score total |
|-------------- |--------- |-------------|-----------------|-------------|------|-----------|
|               |          |             |                 |             |      |           |
| Décisionnaire | Adam | Site web visité | 37 | 15 | 20 + 15 | 35 |
|               |          | E-mail cliqué | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Mark | Site web visité | 5 | 3 | 5 + 3 | 8 |
|               |          | E-mail cliqué | 1 | 1 | 1 + 1 | 2 |
|               |          | Pub téléchargé | 3 | 2 | 3 + 2 | 5 |
| **Score total des décideurs** |         |             |                 |             |      | 52 **** |
|               |          |             |                 |             |      |           |
| Personne influente | John | Site web visité | 19 | 9 | 19 + 9 | 28 |
| **score total des influenceurs** |         |             |                 |             |      | **28** |
|               |          |             |                 |             |      |           |
| Praticien | Bob | E-mail cliqué | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Paul | E-mail cliqué | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Calvin | E-mail cliqué | 1 | 1 | 1 + 1 | 2 |
|               |          | Site web visité | 1 | 7 | 1 + 7 | 8 |
|               |          | Pub téléchargé | 1 | 2 | 1 + 2 | 3 |
| **Score total des praticiens** |         |             |                 |             |      | **17** |

Le score d’engagement final est calculé en appliquant la pondération à chacun des scores de rôle :

| Rôle | Score total du rôle | % de poids du rôle | Score X poids % |
|-------------- |---------------- |------------- |---------------- |
| Décisionnaire | 52 | 41,67 % | 21,67 |
| Les plus influents | 28 | 33,33 % | 9,33 |
| Praticiens | 17 | 25 % | 4,25 |
| **Score d’engagement final** |                |             | 35,25 **** |

## Vidéo de présentation

>[!VIDEO](https://video.tv.adobe.com/v/3433078/?learn=on)
