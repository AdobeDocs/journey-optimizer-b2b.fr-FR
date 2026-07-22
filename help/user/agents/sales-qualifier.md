---
title: Qualificateur de vente
description: Automatisez la qualification et la sensibilisation des prospects B2B avec le qualificateur de vente. Il fournit des recherches optimisées par l’IA, la rédaction d’emails, l’intégration de CRM et des workflows sortants d’IA pour les fichiers BDR.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
exl-id: cc590444-41df-44fe-830b-92241718ee81
autotag-review: '2026-06-05T16:42:16.451Z'
TQID: 'https://experienceleague.adobe.com/VNgs0cTpjCTG7JpFjFErnVMmRtR-gmw-iRRHZanZDUs'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
  - id: fc1ff3b2-6614-41ad-a113-de48597598fd
  - id: f979fe0e-02fe-4599-b492-7b3df1d4e7dc
subfeature_v2:
  - id: fe583b80-65a2-48c2-b4e1-9ea8fbac0a8a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: a5145b53d6b5c9462392f7c540a81b7d85abdd7b
workflow-type: tm+mt
source-wordcount: 6084
ht-degree: 1%

---

# Qualificateur de vente

Sales Qualifier est une application gérée par l’IA que vous pouvez utiliser avec Adobe Journey Optimizer B2B edition. Il met en œuvre Account Qualification Agent et est conçu pour rationaliser les workflows pour les représentants du développement commercial (BDR). Le qualificateur de vente automatise les workflows de qualification des prospects, de sensibilisation et d’engagement des acheteurs sur l’ensemble des canaux. Il réduit la charge manuelle de BDR et accélère la vitesse du pipeline pour les entreprises B2B.

Les BDR peuvent utiliser les plug-ins de navigateur et d’e-mail pour accéder à la Business Intelligence directement dans les CRM ou Outlook. La vidéo suivante présente brièvement le qualificateur de vente et le Account Qualification Agent.

>[!VIDEO](https://video.tv.adobe.com/v/3476550)

## Page de départ Application

Le qualificateur de vente est inclus dans [!UICONTROL Journey Optimizer B2B edition], mais il s’agit d’une application distincte dans Adobe Experience Platform.

![Écran d’accueil du qualificateur de vente](./assets/home-screen.png){width="800" zoomable="yes"}

### Agent Account Qualification

Le Account Qualification Agent (AQA) est au cœur du qualificateur de vente. L’AQA utilise l’IA pour lire vos comptes et déterminer lesquels sont prêts pour l’étape suivante. Il facilite la recherche, la rédaction d’e-mails et le contexte orienté CRM lorsque votre organisation a connecté le CRM.

<!--
## Edit the left navigation bar

At the bottom left of the application, click the _Edit_ ( ![Edit icon](../assets/do-not-localize/icon-edit.svg) ) icon to control which elements are visible in the left navigation. You can also drag and drop them to reorder as you want.
-->

### Utilisation de base de l’agent

Les agents Adobe AI utilisent _requêtes en langage naturel_, ce qui signifie qu’ils utilisent la même langue dans l’invite de texte que vous lorsque vous parlez à une personne. Plus vous êtes détaillé, meilleurs sont les résultats.

En utilisant le langage naturel, vous pouvez demander à l’agent de :

* `Tell me the latest financial results of Bodea`
* `Tell me more about hiring at TechNova`
* `Tell me about the new AI features in Bodea LumaSecure4`

Itérez vos workflows sortants en affinant vos invites pour obtenir les résultats dont vous avez besoin. Par exemple :

* _Rédiger un e-mail de relance à partir du contexte, comme des appels de rémunération ou des rapports._ Jusqu’à 120 mots. Objet : Captivant, intégrant un thème clé. Introduction : commencez par une citation directe de sources de contexte. Corps : permet de se connecter aux points faibles et aux propositions de valeur. CTA : proposez un bref appel pour en savoir plus._

* _L’objectif de cet e-mail est de commencer une conversation et de créer de la crédibilité._ Rédigez un e-mail de 120 mots, au ton consultatif et empathique. Évitez d&#39;adopter une approche trop familière ou commerciale et n&#39;utilisez pas les expressions « j&#39;espère que vous allez bien », « je vous demande simplement de vous enregistrer » ou « s&#39;il vous plaît ».

### Accès aux produits et groupes d’utilisateurs

L’accès aux fonctionnalités du qualificateur de vente est géré par l’intermédiaire de deux groupes d’utilisateurs dans Adobe Admin Console. Les administrateurs de produit doivent configurer les groupes lors de l’intégration avant que les utilisateurs puissent accéder à l’application.

#### Utilisateurs du qualificateur de vente

Les utilisateurs doivent être membres du groupe d&#39;utilisateurs `Sales Qualifier` pour accéder à l&#39;application Qualificateur de vente.

1. Dans Adobe Admin Console, créez un groupe d’utilisateurs nommé `Sales Qualifier`.
1. Attribuez le profil AEP **Tous les accès de production par défaut** au groupe .
1. Ajoutez les utilisateurs qui doivent accéder au qualificateur de vente.

#### Administrateurs du qualificateur de vente

Les administrateurs qui configurent les paramètres [Connexions CRM](#integrations-and-crm), [Centre de connaissances](#knowledge-center) et de désinscription globale aux e-mails doivent également être membres du groupe d’utilisateurs `Sales Qualifier Admins`.

1. Dans Adobe Admin Console, créez un groupe d’utilisateurs nommé `Sales Qualifier Admins`.
1. Ajoutez les administrateurs aux groupes `Sales Qualifier` et `Sales Qualifier Admins`.

L’appartenance aux deux groupes rend **[!UICONTROL Paramètres d’administration]** visible sous **[!UICONTROL Administration]** dans le volet de navigation de gauche. Les utilisateurs standard peuvent utiliser les champs, filtres et playbook configurés. Le pied de page d’opt-out configuré est appliqué à leurs e-mails sortants. Ils ne peuvent pas modifier ces paramètres.

>[!NOTE]
>
>Les noms des groupes d’utilisateurs doivent correspondre exactement comme indiqué dans les étapes précédentes.

## Prospects

Sélectionnez **[!UICONTROL Prospects]** dans le volet de navigation de gauche pour afficher une liste des prospects auxquels vous pouvez accéder. La liste fournit un aperçu rapide des informations, telles que le statut du prospect et la dernière activité.

![Tableau des prospects affichant le statut du prospect et la dernière activité pour la gestion des prospects](./assets/prospects.png){width="800" zoomable="yes"}

### Création de votre liste de prospects

La liste des prospects regroupe des personnes provenant de plusieurs sources :

* **Prospects provenant d’un CRM** - Lorsque vous connectez un CRM, celui-ci importe automatiquement les prospects appartenant à l’utilisateur connecté. Voir [&#x200B; Intégrations et CRM &#x200B;](#integrations-and-crm).
* **Prospects importés** - Importez une liste de prospects à partir d’un fichier CSV.
* **Prospects ajoutés manuellement** - Ajoutez une personne directement dans l’application.

Pour ajouter des prospects qui ne proviennent pas de votre CRM :

1. Sur la page **[!UICONTROL Prospects]**, sélectionnez **[!UICONTROL Ajouter des prospects]**.
1. Choisissez **[!UICONTROL Importer CSV]** ou **[!UICONTROL Ajouter manuellement]**.

   * Pour un import au format CSV, chargez le fichier et mappez ses colonnes aux champs du prospect.
   * Pour ajouter une personne manuellement, saisissez ses détails dans le formulaire.

1. Sélectionnez **[!UICONTROL Enregistrer]**.

### Filtrer et rechercher des prospects

Sélectionnez l’icône _Filtrer_ ![Icône Filtrer](../../assets/do-not-localize/icon_filter-outline.svg) pour affiner la liste. Vous pouvez filtrer par :

* Statut du lead
* Score d’engagement
* Moments significatifs marqués par le marketing
* Score d&#39;étoile et score de flamme
* Offres associées

Les administrateurs peuvent également rendre les champs CRM mappés disponibles en tant que filtres. Dans **[!UICONTROL Paramètres d’administration]**, ils activent **[!UICONTROL Filtrable]** pour les champs que les représentants utilisent pour rechercher des prospects. Voir [&#x200B; Mappage des champs CRM &#x200B;](#map-crm-fields-inbound-mapping).

### Consulter les détails du prospect

Sélectionnez un prospect pour ouvrir son profil. Examinez les signaux qui comptent avant de vous adresser à :

* **Liste des activités** - Une liste chronologique des activités du prospect, avec un **résumé des activités d’IA** en haut qui met en évidence le comportement récent le plus pertinent.
* **Vue Chronologie** - Chronologie visuelle de l’engagement sur l’ensemble des canaux.
* **Contenu consulté** - Ouvrez le contenu réel qu’un prospect a consulté, tel qu’une page web ou une ressource, directement à partir d’une activité.

## Comptes

Sélectionnez **[!UICONTROL Comptes]** dans le volet de navigation de gauche pour utiliser les comptes dans lesquels vous effectuez des ventes. Le qualificateur de vente rassemble les détails démographiques, le pipeline et l’engagement afin que vous puissiez prioriser la sensibilisation au niveau du compte.

La présentation du compte résume des éléments essentiels tels que le chiffre d’affaires, le secteur, la taille de l’entreprise et le siège social. Outre ces détails, chaque compte fait apparaître :

* **Opportunités ouvertes** - Les opportunités ouvertes associées au compte, provenant de votre CRM connecté, afin que vous puissiez aligner la portée sur le pipeline actif.
* **Membres les plus engagés** - Les contacts du compte avec l’engagement le plus récent, de sorte que vous sachiez qui prioriser au sein du groupe d’achat.
* **Entrées CRM** - Champs de compte, opportunités et informations sur le ou la propriétaire sont apparus à partir de votre CRM connecté. Consultez [&#x200B; Intégrations et CRM &#x200B;](#integrations-and-crm) pour savoir comment ces données sont mappées.

### Séance d’immersion dans le compte

Pour démarrer un examen approfondi, ouvrez un compte . Le Account Qualification Agent (AQA) donne la priorité aux signaux qui sont les plus pertinents pour la stratégie de vente de votre organisation, afin que vous puissiez rapidement comprendre la position du compte et décider de la suite à donner.

## Workflows sortants

>[!NOTE]
>
>Les workflows sortants créés par les administrateurs de produit sont partagés avec tous les utilisateurs de votre organisation.

Un _workflow sortant_ est la structure utilisée par le qualificateur de vente pour exécuter une cadence pilotée par les objectifs. Vous définissez un objectif de sensibilisation et des critères de ciblage, et l’IA propose une cadence multi-touch et écrit du contenu d’e-mail personnalisé pour chaque prospect. Vous passez en revue et approuvez chaque e-mail avant que l’inscription n’active le rythme, de sorte que les messages soient envoyés uniquement pendant la fenêtre configurée.

Un workflow sortant connecte quatre éléments :

* **Objectif** - Résultat que vous souhaitez obtenir de la sensibilisation (par exemple, la réservation d’un appel de découverte ou l’enregistrement d’un événement de conduite).
* **Filtres de ciblage** - Conditions qui déterminent les prospects éligibles.
* **Cadence des points de contact** - Séquence ordonnée d’étapes, chacune à un jour planifié. Les points de contact peuvent être **e-mails**, **appels téléphoniques** ou **LinkedInMails**.
* **Contenu d’e-mail personnalisé** - Pour chaque point de contact d’e-mail, l’IA rédige le contenu en utilisant le profil du prospect, le contexte du compte, l’historique d’engagement et les actualités récentes.

L’objectif mène tout en aval : l’IA l’utilise pour suggérer des filtres de ciblage, concevoir la cadence, les invites de point de contact de brouillon et personnaliser la forme de chaque e-mail généré.

![Onglet Aperçu du workflow sortant](./assets/outbound-workflow-overview.png){width="800" zoomable="yes"}

### Principaux concepts

| Concept | Description |
| --- | --- |
| **Workflow** | Activité sortante réutilisable définie par un objectif, des filtres de ciblage, une cadence et des paramètres. |
| **Objectif** | Ce que la sensibilisation devrait accomplir. |
| **Point de contact** | Une étape de la cadence (e-mail, appel téléphonique ou LinkedInMail), planifiée par rapport à l’inscription. |
| **invite de point de contact** | Instructions que l’IA suit lors de la génération du corps et de l’objet de l’e-mail pour un prospect (ton, longueur, focus et call to action). |
| **Cadence** | La séquence complète des points de contact : combien, dans quel ordre et à quels jours. |
| **Filtre de ciblage** | Une condition qui limite le workflow à un sous-ensemble de prospects. |
| **Brouillon** | Un e-mail généré qui est prêt pour la révision mais pas encore approuvé. |
| **Raisonnement** | L’explication de l’IA sur la manière dont elle a écrit un e-mail donné (quels signaux et sources de données elle a utilisés). |
| **Inscription** | La validation des brouillons d’un prospect, qui active le rythme et met en file d’attente les e-mails à envoyer pendant la fenêtre d’envoi du workflow. |

Les sections suivantes décrivent l’ensemble du cycle de vie : création d’un workflow dans l’assistant, révision des e-mails générés, approbation des prospects et gestion des workflows au fil du temps.

### Création d’un workflow sortant

La création de workflow est un assistant en cinq étapes : **Objectif**, **Ciblage**, **Générer des points de contact**, **Paramètres** et **Ajouter des prospects**. Chaque étape s’appuie sur la dernière ; votre objectif initial façonne chaque décision ultérieure.

1. Dans le volet de navigation de gauche, sélectionnez **[!UICONTROL Workflow sortant]**.

1. Dans l’onglet **[!UICONTROL Parcourir]**, cliquez sur **[!UICONTROL + Créer un workflow]** dans le coin supérieur droit.

#### Étape 1 : définir votre objectif

L’objectif est l’entrée la plus importante : elle indique à l’IA à quoi ressemble la réussite et ancre le ciblage, la cadence et la génération d’e-mails.

1. Choisissez **[!UICONTROL Démarrer à partir de zéro]** pour écrire votre propre objectif, ou **[!UICONTROL Démarrer à partir d’un modèle]** pour utiliser un modèle enregistré.

   ![Créer entièrement un workflow sortant](./assets/outbound-workflow-create-start-from-scratch.png){width="700" zoomable="yes"}

1. Sélectionnez l’un des **[!UICONTROL Objectifs recommandés]** comme point de départ ou saisissez votre propre objectif.

1. Cliquez sur **[!UICONTROL Suivant : Ciblage]**.

Les objectifs fonctionnent mieux lorsqu’ils énoncent un **résultat concret**, et pas seulement un sujet. Pour donner à l’IA plus d’outils pour travailler, utilisez un objectif comme `Book a 15-minute discovery call with marketing leaders evaluating campaign automation` au lieu de `Promote campaign automation`.

#### Étape 2 : Configuration des filtres de ciblage

Les filtres de ciblage définissent les prospects éligibles. Lorsque vous ajoutez des prospects ultérieurement, seuls ceux qui correspondent à ces filtres apparaissent dans la liste de sélection.

1. Cliquez sur la flèche vers le bas pour afficher la liste **[!UICONTROL Ajouter un filtre]** et sélectionnez un filtre à appliquer.

   ![Création de filtres de ciblage de workflow sortant](./assets/outbound-workflow-create-targeting-filter-list.png){width="700" zoomable="yes"}

1. Définissez des valeurs pour le filtre.

1. Ajoutez d’autres filtres si vous devez limiter l’audience.

   ![Créer un workflow sortant Ciblage des filtres ajoutés avec des valeurs](./assets/outbound-workflow-create-targeting-filters-values.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Suivant : générer des points de contact]**.

#### Étape 3 : génération et révision des points de contact

Une fois le ciblage défini, l’IA crée la **_cadence_** : elle analyse votre objectif et votre ciblage, définit la séquence de points de contact et écrit une **_invite de point de contact_** pour chaque étape. Une cadence à plusieurs étapes s’affiche avec chaque point de contact un jour spécifique. Le rythme peut combiner des étapes d’e-mail, d’appel téléphonique et d’InMail LinkedIn.

![Cadence et invites de point de contact générées par le workflow sortant](./assets/outbound-workflow-create-touchpoints.png){width="700" zoomable="yes"}

Pour lire son invite, développez un point de contact d’e-mail. Ces instructions guident l’IA lors de l’écriture de l’e-mail de chaque prospect, y compris le ton, la longueur, le focus et __.

**Régénérer le rythme**

Si la cadence ne vous convient pas, cliquez sur **[!UICONTROL Régénérer]** et saisissez une instruction d’affinement. Par exemple :

* `Make it 3 touchpoints across 2 weeks`
* `Lead with an executive briefing offer in the first email`
* `Add a nurture touch focused on a relevant case study`

L’IA réécrit la cadence complète en fonction de vos instructions.

Pour ajuster un seul point de contact d’e-mail sans régénérer l’ensemble de la cadence, modifiez le texte de l’invite directement dans sa zone de texte.

**Utiliser un playbook dans vos invites**

Si votre entreprise a créé un playbook dans le [Centre de connaissances](#knowledge-center), vous pouvez demander à l’IA de s’en inspirer lors de la rédaction d’e-mails. Dans l’invite, nommez le document et le contexte que l’IA doit utiliser, par exemple, `Use the ABC positioning guide from the Knowledge Center and focus on the security value proposition`. Les e-mails générés reflètent ensuite les messages de ce playbook.

Lorsque le rythme et les invites sont corrects, cliquez sur **[!UICONTROL Suivant : Paramètres]**.

Raffiner les invites de point de contact avant que la génération par prospect ne soit importante : ces invites sont les instructions principales que l&#39;IA utilise pour chaque prospect ultérieurement. Le temps passé ici est mis à l’échelle sur tous les e-mails générés.

#### Étape 4 : configurer les paramètres de workflow

L’étape **Paramètres** contrôle le fonctionnement du workflow.

![Paramètres du workflow sortant](./assets/outbound-workflow-create-settings.png){width="700" zoomable="yes"}

1. Vérifiez le **[!UICONTROL nom du workflow]** et modifiez-le si vous souhaitez un libellé plus clair.
1. Dans **[!UICONTROL Nombre maximal de prospects par workflow]**, confirmez la limite supérieure du nombre de prospects que le workflow peut gérer à la fois.
1. Définissez la **[!UICONTROL fenêtre d’envoi]** pour les heures pendant lesquelles les e-mails sortants sont autorisés à être envoyés.
1. Activez l’option **[!UICONTROL Ignorer les week-ends]** pour déplacer tout point de contact qui se trouve un week-end vers le jour ouvrable suivant.
1. Pour arrêter automatiquement les points de contact de suivi une fois qu’un prospect a réservé une réunion, activez **[!UICONTROL Pause de la réservation de réunion]**.
1. Vérifiez que le **[!UICONTROL fuseau horaire]** correspond à votre audience.
1. Cliquez sur **[!UICONTROL Enregistrer et ajouter des prospects]**.

Le pied de page d’opt-out est configuré globalement par un administrateur et s’applique aux e-mails sortants indépendamment des paramètres du workflow. Voir [Synchronisation globale des désinscriptions](#global-opt-out-sync).

#### Étape 5 : ajouter des prospects et commencer la génération d’e-mails

L’enregistrement ouvre la vue de sélection des prospects, déjà filtrée par votre ciblage de l’étape 2.

![Ajout de prospects aux workflows sortants](./assets/outbound-workflow-create-add-prospects.png){width="700" zoomable="yes"}

1. Passez en revue la liste.

   Les lignes comprennent généralement le nom, le compte, l’adresse e-mail, la fonction, le statut d’engagement et le statut du prospect.

1. Ajustez les filtres ici si vous devez développer ou réduire la liste.
1. Sélectionnez des prospects à l’aide des cases à cocher.
1. Cliquez sur **[!UICONTROL Suivant : consulter les points de contact]** pour commencer la génération d’e-mails **par prospect**.

L’IA génère des e-mails personnalisés pour chaque prospect sélectionné **chaque point de contact d’e-mail** à la cadence. Les points de contact Téléphone et LinkedInMail restent dans le rythme des étapes planifiées. La génération peut s’exécuter en arrière-plan. Utilisez **[!UICONTROL Notifier lorsque vous êtes prêt]** si vous souhaitez continuer une autre tâche pendant qu’elle se termine.

Pour chaque prospect, l’IA combine chaque invite de point de contact avec des données spécifiques au prospect (personne, compte, historique d’engagement, actualités récentes) afin de produire l’objet et le corps.

### Consulter et affiner les e-mails générés

Une fois la génération terminée, la vue détaillée du workflow affiche une bannière pour réviser les brouillons. Une révision est requise et rien n’est envoyé tant que vous n’avez pas approuvé.

![E-mails générés lors de la révision du workflow sortant](./assets/outbound-workflow-create-review-generated-emails.png){width="700" zoomable="yes"}

1. Dans la vue détaillée du workflow, cliquez sur **[!UICONTROL Vérifier les brouillons]** dans la bannière.
1. L’étape **[!UICONTROL Vérifier les points de contact]** comporte deux onglets :
   * **[!UICONTROL Prêt pour la révision]** - E-mails dont la génération est terminée.
   * **[!UICONTROL Génération en cours]** - Les e-mails sont toujours en cours d’écriture.
1. Dans la liste des prospects de gauche, cliquez sur un nom pour charger les points de contact de ce prospect à droite.
1. Utilisez le chevron (**>**) sur un point de contact pour développer et lire l’objet et le corps complets.

#### Lire le raisonnement de l’IA

Pour chaque e-mail généré, la section **[!UICONTROL REASONING]** explique comment l’IA a conçu ce message, y compris les signaux, les attributs et les sources qui ont façonné le contenu et le call to action. Passez en revue ces informations et validez la personnalisation avant d’approuver.

![Raisonnement de l’IA dédiée aux e-mails générés par le workflow sortant](./assets/outbound-workflow-create-review-generated-email-reasoning.png){width="600" zoomable="yes"}

#### Modifier directement les e-mails

Pour les petites modifications (libellé, ton, une seule phrase) :

1. Sur le point de contact développé, cliquez sur l’icône _Modifier_ pour ouvrir l’éditeur.
1. Modifiez l’objet ou le corps.
1. Cliquez sur **[!UICONTROL Enregistrer]**

#### Affiner les e-mails avec l’IA

Pour des modifications plus importantes (restructuration, changement de focus ou recadrage du message), utilisez **[!UICONTROL Générer avec l’IA]**. L’agent AI réécrit l’e-mail tout en conservant le contexte de personnalisation.

1. Dans l’éditeur d’e-mail, cliquez sur **[!UICONTROL Générer avec IA]**.

   ![Amélioration des e-mails générés par le workflow sortant avec l’IA](./assets/outbound-workflow-create-review-generated-email-edit-regenerate.png){width="600" zoomable="yes"}

1. Saisissez une instruction claire, par exemple :
   * `Make it shorter and more direct. Keep it under 100 words.`
   * `Focus more on the prospect's role and how the solution helps them specifically.`
   * `Change the call-to-action to suggest a 15-minute introductory call instead.`
1. Passez en revue la révision et apportez les modifications manuellement, si nécessaire.
1. Cliquez sur **[!UICONTROL Enregistrer]**

>[!TIP]
>
>Les modifications directes suivent le libellé et le ton. Utilisez _[!UICONTROL Générer avec l’IA]_ pour réécrire l’e-mail en partant de zéro.

### Approuver et inscrire des prospects

La validation active le rythme d’un prospect. Tant qu’un prospect n’est pas approuvé et inscrit, le système ne lui envoie pas d’e-mails.

1. Dans la liste de gauche des prospects, sélectionnez les prospects dont vous avez vérifié les e-mails et qui sont prêts à envoyer.
1. Cliquez sur **[!UICONTROL Approuver et inscrire les prospects]** (en bas à droite).

![Workflow sortant : sélectionner et approuver les prospects](./assets/outbound-workflow-create-approve-enroll-prospects.png){width="700" zoomable="yes"}

Les e-mails approuvés sont envoyés pendant le workflow **fenêtre d’envoi** dans le **fuseau horaire** configuré, le jour prévu de chaque point de contact par rapport à l’inscription. Les prospects que vous n’approuvez pas restent dans l’état **[!UICONTROL Prêt pour la révision]** jusqu’à ce que vous agissiez. Après approbation, le workflow s’exécute selon la cadence que vous avez définie.

### Gestion des workflows existants

Sur la page _[!UICONTROL Workflow sortant]_, l’onglet **[!UICONTROL Parcourir]** répertorie chaque workflow. Chaque carte affiche l’objectif, les points de contact configurés et les mesures de performances. Utilisez cette vue pour surveiller les workflows actifs, revenir aux brouillons qui doivent encore être examinés ou ouvrir un workflow pour ajouter d’autres prospects.

### Bonnes pratiques relatives au workflow sortant

* **Investissez dans l’objectif.** Le ciblage en aval, la cadence et les e-mails remontent tous jusqu’à l’objectif. Les objectifs spécifiques axés sur les résultats surpassent les objectifs vagues.
* **Finalisez les invites de point de contact avant la génération par prospect.** Après la génération en bloc, les modifications sont généralement apportées un prospect à la fois.
* **Utiliser le raisonnement comme contrôle de qualité.** Si le mauvais signal est souligné (ou si un signal évident est manquant), modifiez l’e-mail ou revenez à l’invite du point de contact et régénérez la cadence.
* **Faire correspondre l’outil d’édition à la modification.** Modifications directes du libellé et du ton ; **[!UICONTROL Générer avec l’IA]** pour restructurer ou recadrer.
* **Approuver uniquement ce que vous avez révisé.** Développez les points de contact, lisez le contenu et affinez-les si nécessaire avant l’inscription.

### Synchronisation globale du processus d’opt-out

Les administrateurs peuvent ajouter un pied de page de désabonnement léger qui utilise un verbiage [!DNL Marketo] préapprouvé à chaque e-mail sortant. Lorsqu’un prospect sélectionne le lien d’exclusion, le qualificateur de vente le supprime définitivement des autres e-mails et synchronise le statut d’exclusion avec le CRM connecté. Voir [&#x200B; Configuration du processus d’opt-out global des e-mails](#configure-global-email-opt-out).

## Boîte d’envoi d’e-mail

Le panneau Boîte d’envoi d’e-mail répertorie tous les e-mails automatisés que vous avez envoyés.

<!--
## Meeting bookings

This panel displays all meetings set up through automation.

## Chat inbox

This panel displays all your chat threads.

![Panel showing chat threads with contact and thread summaries for sales automation](assets/chat-inbox.png)

You can interact with clients, and see summaries for the contact and the thread so that you can quickly know where you are in the thread.

-->

## Tâches

La zone _Tâches_ dans le qualificateur de vente offre aux représentants du développement commercial (BDR) un espace dédié pour gérer et traiter leurs actions de workflow sortant. Le moteur de workflow sortant génère automatiquement des tâches qui représentent les actions spécifiques qu’un BDR doit effectuer avec chaque prospect (appels téléphoniques, LinkedInMails et révisions des e-mails).

L’expérience de gestion des tâches est une **file d’attente de traitement**, pas une liste de tâches. Vous pouvez ouvrir une tâche, effectuer une action, la marquer comme terminée et passer à la suivante, le tout sans quitter la page.

Sélectionnez **[!UICONTROL Tâches]** dans la barre de navigation de gauche pour ouvrir la page complète des tâches. Cette page est l’espace de travail principal pour le traitement des tâches une par une.

![Page Tâches affichant la file d’attente de tâches et le panneau des détails](./assets/tasks.png){width="800" zoomable="yes"}

<!--
**Homepage feed** - The homepage displays a running feed of your most urgent tasks, with overdue items at the top followed by today's tasks. Each item in the feed has an "Open" button that takes you directly to that task in the Tasks page with the detail panel already loaded.
-->

### Types de tâches

Toutes les tâches sont liées aux étapes de workflow sortant. Il en existe trois types :

**Appel téléphonique** — Créé lorsqu’une cadence atteint une étape d’appel téléphonique. Le panneau des tâches affiche des points de présentation générés par l’agent et un champ de notes intégrées pour capturer les notes d’appel.

**LinkedInMail** — Créé lorsqu’une cadence atteint une étape LinkedInMail. Le panneau des tâches affiche une ligne d’objet et un corps de message générés par l’IA que vous pouvez copier et envoyer en dehors du produit.

**Révision d&#39;email** — Créé une fois que le système a fini de générer des emails personnalisés pour un prospect inscrit dans un workflow. Vous examinez et approuvez les e-mails avant le début de l’envoi pour ce prospect. Chaque prospect reçoit une tâche de révision d’e-mail distincte. Si vous inscrivez 10 prospects à un workflow, vous voyez jusqu’à 10 tâches de révision d’e-mail à mesure que la génération est terminée.

### Gestion des tâches

La page Tâches est divisée en deux panneaux :

* **Gauche — Liste des tâches :** votre file d’attente de tâches, classées et filtrées en fonction de l’affichage et des paramètres de tri sélectionnés.
* **Droite — Panneau de travail de la tâche :** détails de la tâche sélectionnée, y compris les informations sur le prospect, le contexte du workflow, le contenu spécifique à la tâche et les commandes d’action.

La sélection d’une tâche dans le panneau de gauche charge ses détails dans le panneau de droite sans quitter la page.

#### Contrôles de file d&#39;attente

Le panneau de travail comprend des commandes **Suivant** et **Précédent** pour vous déplacer dans la file d’attente des tâches dans l’ordre. La file d’attente respecte les paramètres de tri et de filtrage que vous appliquez à la liste. Ainsi, si vous travaillez sur des tâches d’appel téléphonique en retard triées par date d’échéance, _Suivant_ et _Précédent_ passez exactement par cet ensemble.

Lorsque vous marquez une tâche comme terminée, le panneau passe automatiquement à la tâche suivante dans la file d’attente.

#### Notes

Pour les tâches Appel téléphonique et LinkedInMail , un champ de notes intégrées est disponible dans le panneau de travail. Les notes sont enregistrées automatiquement lorsque vous cliquez ailleurs afin de ne pas les perdre lorsque vous accédez à une autre tâche avant de marquer la tâche en cours comme terminée.

#### Actions liées à la tâche

Utilisez les actions suivantes pour gérer vos tâches :

* **[!UICONTROL Marquer comme terminé]** - Action principale. Utilisez cette action une fois la tâche exécutée : avez passé l’appel, envoyé l’InMail ou révisé et approuvé les e-mails. Une fois la tâche terminée, elle est enregistrée comme **Terminée** et la file d’attente avance automatiquement.

* **[!UICONTROL Ignorer le point de contact]** - Disponible dans le menu de débordement du panneau de travail. Utilisez cette option lorsque vous ne pouvez pas terminer cette étape, mais que le prospect reste une cible valide dans le workflow.
  * Le prospect passe à l’étape suivante de la cadence. Les futures tâches sont toujours générées dans les délais.
  * Sélectionnez une raison : *Informations de contact incorrectes*, *Mauvais timing*, *Contenu non pertinent* ou *Autre* (avec un champ de texte libre).
  * Le statut de la tâche est défini sur **Ignorée** et consignée avec la raison et l’horodatage.
  * S’il s’agissait de la dernière étape du workflow, l’exécution du workflow du prospect se termine. La tâche est toujours consignée comme Ignorée (non supprimée).

* **[!UICONTROL Supprimer du workflow]** - Disponible à partir du menu de débordement dans le panneau de travail. Utilisez cette option lorsque le prospect n’appartient plus à ce workflow.

  Lorsque vous supprimez un prospect d&#39;un workflow :
  * Toutes les tâches en attente et futures pour ce prospect dans ce workflow sont annulées.
  * Le statut d&#39;inscription du prospect passe à **Supprimé par BDR**.
  * Sélectionnez un motif : *Société de gauche*, *Dupliquer*, *Mauvaise coupe*, *Déjà converti* ou *Autre* (avec un champ de texte).
  * Une boîte de dialogue de confirmation s’affiche : *« Cette action annule tous les points de contact restants pour [Prospect] dans [Nom du workflow]. Continuer ?«*
  * Le statut de la tâche est défini sur **Supprimé**. Toutes les tâches frères annulées sont également marquées **Supprimées**.

>[!NOTE]
>
>Les données de motif Ignorer et Supprimer informent les analyses, y compris les taux d’omission de canal, les taux de suppression de workflow et les principales raisons. Cela permet d’améliorer la qualité des workflows et d’éclairer l’analyse des performances au fil du temps.

**Saut automatique**

Les tâches Stagnant de LinkedInMail et d&#39;appel téléphonique sont automatiquement ignorées si elles restent incomplètes pendant deux jours. L’omission automatique permet à un prospect de se déplacer rapidement sans bloquer l’exécution, et n’affecte pas la chronologie de l’e-mail. Les points de contact d’e-mail planifiés continuent à envoyer comme prévu.

### Statut de la tâche

Chaque tâche passe par les états suivants :

| Statut | Description |
|---|---|
| **En attente** | Créée mais l’étape de workflow précédente n’est pas encore terminée. Non visible dans votre liste de tâches. |
| **À venir** | L’étape précédente est terminée, mais la date d’échéance se situe dans le futur. Visible et exploitable : vous pouvez le terminer plus tôt si le moment est venu. |
| **Ouvrir** | Échéance aujourd&#39;hui. Visible et exploitable. |
| **En retard** | Date d&#39;échéance passée, pas encore terminée. Visible, exploitable et marqué visuellement. |
| **Terminé** | Vous avez exécuté et marqué la tâche comme terminée. |
| **Ignoré** | Vous avez ignoré ce point de contact. Le prospect progresse dans le workflow. |
| **Supprimé** | Vous avez supprimé le prospect du workflow. Toutes les tâches frères sont annulées. |
| **Annulé** | Annulation du système en raison d&#39;une modification du workflow ou de la suppression d&#39;un prospect. |

### Vues Liste

Utilisez les onglets situés en haut de la liste des tâches pour basculer entre les vues :

* **Aujourd&#39;hui** *(par défaut)* — Tâches dues aujourd&#39;hui qui ne sont pas terminées.

* **En retard** — Tâches dont l&#39;échéance est dépassée et qui sont toujours en cours. Commencez par vous occuper de ces tâches.

* **À venir** — Tâches à échéance future où l&#39;étape précédente du workflow est déjà terminée. Ces tâches sont visibles de manière anticipée, ce qui vous permet de planifier ou d&#39;agir plus tôt si le moment est propice (par exemple, si vous êtes déjà contacté par un prospect). La date d’échéance prévue s’affiche afin que vous connaissiez la planification.

* **Terminé** — Enregistrement des tâches que vous avez terminées, ignorées ou supprimées. Utile à des fins de révision et d’audit.

### Filtrage et recherche

Il existe plusieurs façons de filtrer la liste des tâches :

* Filtrez par type de tâche à l’aide d’une liste à sélection multiple. La sélection de plusieurs types affiche les tâches correspondant *à l’un* types sélectionnés (Appel téléphonique **ou Révision** e-mail, par exemple).

* Filtrez par statut de tâche. La sélection de plusieurs statuts affiche les tâches correspondant à l’un des statuts sélectionnés.

* Filtrez les groupes à l’aide de la logique **AND**. Par exemple, `Type = Phone Call and Status = Overdue` affiche uniquement les tâches d’appel en retard.

Utilisez la barre de recherche pour rechercher des tâches par nom de prospect, nom de société ou nom d’engagement. La recherche s’applique à tous les filtres actifs. Correspondance de texte uniquement : correspondances partielles exactes, pas de recherche floue.

### Tri

Utilisez le contrôle **Trier par** pour choisir le classement de la liste des tâches. Le tri détermine également l’ordre dans lequel Suivant et Précédent traversent la file d’attente.

| Option de tri | Comportement |
|---|---|
| **Date d’échéance (croissant)** *(par défaut)* | Date d&#39;échéance la plus ancienne en premier. Les tâches échues apparaissent avant les tâches d&#39;aujourd&#39;hui. |
| **Échéance (Descendante)** | Dernière date d&#39;échéance en premier. |
| **Date de création (la plus récente)** | Tâches créées en premier. |
| **Date De Création (La Plus Ancienne)** | Tâches créées les plus anciennes en premier. |
| **Type de tâche** | Regroupés par type dans l&#39;ordre : Appel téléphonique → LinkedInMail → Email Review. Dans chaque groupe, trié par date d’échéance en ordre croissant. |

### Tâches en retard

Une tâche devient en retard le jour suivant sa date d&#39;échéance si elle n&#39;est pas terminée. Tâches en retard :

* S’affichent dans la vue **En retard** et en haut du flux de la page d’accueil.
* Sont marqués visuellement avec un badge « En retard » dans la liste des tâches.
* Restez entièrement exploitable : vous pouvez les terminer, les ignorer ou les supprimer.

### Tâches à venir

Les tâches à venir sont créées au moment où un prospect termine une étape de workflow, même si la date d’échéance de l’étape suivante se situe toujours dans le futur. Cette visibilité vous permet d’intégrer rapidement insight à votre pipeline afin de planifier ou d’agir rapidement lorsque l’opportunité se présente.

Les tâches à venir affichent leur date d&#39;échéance prévue, de sorte que vous sachiez toujours quand elles sont censées être traitées. Le moteur de workflow enregistre la date d&#39;achèvement effective et avance normalement le prospect afin de permettre l&#39;exécution anticipée d&#39;une tâche à venir.

### Achèvement de tâche

L’achèvement d’une tâche ne se limite pas à la page Tâches .

**Affichage du prospect engagé :** les aperçus de point de contact sur la page d’un prospect engagé incluent une action _Marquer comme terminé_ ainsi qu’un aperçu du contenu et un champ de notes facultatives. Lorsque vous terminez une tâche, son statut est immédiatement mis à jour dans la page Tâches. Cette vue ne déclenche pas de comportement d’avance automatique ; il s’agit d’une surface d’affichage et d’action, et non d’une surface de traitement de file d’attente.

**Salesforce (module externe CRM) :** le module externe Qualificateur de vente de Salesforce affiche le statut de la tâche (à venir, en attente, terminée, en retard, ignorée) dans la carte de workflow sortant. Dans la version actuelle, la carte CRM est **en lecture seule** — vous pouvez voir le statut des tâches, mais vous devez effectuer les tâches à partir du qualificateur de vente.

### États vides

* **Aujourd’hui sans tâche :** un message _Vous êtes tous pris pour aujourd’hui_ s’affiche. Si des tâches à venir existent, une invite s’affiche comme _Vous avez [N] tâches à venir — Afficher les tâches à venir_.
* **Présence de tâches en retard :** une invite vous incite à traiter d’abord les tâches en retard.

## Réservation de réunion

Le qualificateur de vente transforme les conversations engagées en réunions réservées sans quitter le flux sortant. Lorsque vous connectez votre calendrier, le qualificateur de vente génère un lien de réservation personnel que les prospects utilisent pour planifier des heures avec vous.

* **Liens de réservation** - Configurez la connexion et la disponibilité de votre calendrier dans [Paramètres du profil](#profile-settings). Votre lien de réservation peut être ajouté à votre signature d&#39;email afin qu&#39;il apparaisse dans les emails sortants.
* **Insertion automatique dans une cadence** - Le qualificateur de vente insère votre lien de réservation à des points appropriés dans une cadence, de sorte que l&#39;invitation à une réunion apparaît quand elle est la plus pertinente. Vous pouvez remplacer l’emplacement manuellement.
* **Pause de la réservation** - Lorsqu’un prospect réserve une réunion, **[!UICONTROL Pause de la réservation de la réunion]** arrête automatiquement les autres suivis. Voir [Configurer les paramètres de workflow](#step-4-configure-workflow-settings).

Suivez les résultats de la réservation dans la section [Performances](#performance).

## Centre de connaissances

Le _[!UICONTROL Centre de connaissances]_ permet au Account Qualification Agent (AQA) d’accéder à vos propres supports commerciaux, de sorte que le qualificateur des ventes puisse générer des recherches, des informations sur les qualifications et des activités de sensibilisation qui reflètent les ventes de votre entreprise. La création et la gestion du playbook sont une tâche d’administration.

![&#x200B; Centre de connaissances &#x200B;](./assets/integrations-knowledge-center.png){width="700" zoomable="yes"}

### Chargement du dérivé de vente

1. Dans le volet de navigation de gauche, développez **[!UICONTROL Administration]** et sélectionnez **[!UICONTROL Paramètres d’administration]**.
1. Sélectionnez **[!UICONTROL Centre de connaissances]** sous **[!UICONTROL Intégrations]**.
1. Définissez les **[!UICONTROL Nom de la société]** et **[!UICONTROL URL de la société]** que le qualificateur de vente utilise pour rechercher votre société et rédiger des e-mails.
1. Chargez des pièces de théâtre commerciales, des profils client idéaux, des guides de positionnement et d’autres documents promotionnels au format PDF, PPTX ou DOCX.

Chaque document chargé affiche son statut de traitement, tel que **[!UICONTROL Prêt]**, et la date de sa dernière mise à jour.

### Créer un playbook

Une fois vos documents chargés, sélectionnez **[!UICONTROL Créer un playbook]** pour les transformer en playbook.

>[!NOTE]
>
>Un playbook prend environ 24 heures à traiter avant d’être prêt à l’emploi.

Lorsque le manuel est prêt, il fournit à la fois des informations et de l’aide :

* **Invites d’e-mails sortants** - Référencez le playbook lors de la génération des e-mails en nommant le document et le contexte dans votre invite. Voir [&#x200B; Générer et réviser des points de contact](#step-3-generate-and-review-touchpoints).
* **Assistant de vente conversationnel** - Pour extraire du manuel, pointez l’assistant vers le centre de connaissances. Voir [Assistant commercial de conversation](#conversational-sales-assistant).

## Assistant commercial de conversation

L’assistant de vente conversationnel est une expérience de conversation où vous posez des questions en langage naturel et obtenez des réponses ancrées dans votre contexte de vente. L&#39;assistant s&#39;appuie sur :

* Votre base de connaissances interne, y compris tout playbook [&#x200B; Centre de connaissances &#x200B;](#knowledge-center)
* Signaux CRM de votre CRM connecté
* [!DNL Marketo] des données d’activité et d’engagement
* Recherche sur le Web

Utilisez l’assistant pour vous préparer avant la réunion, par exemple pour définir le positionnement du compte avant une réunion. Pour extraire une partie d’un manuel, indiquez l’assistant au Centre de connaissances dans votre question. Par exemple : `From the Knowledge Center, help me position our security solution for ABC Corp ahead of tomorrow's call.`

## Performance

La section **[!UICONTROL Performances]** indique l’état de votre trafic sortant, de sorte que vous puissiez voir ce qui fonctionne et où effectuer des ajustements.

### Performances des e-mails

Vérifiez le volume et l’efficacité de votre e-mail sortant :

* E-mails envoyés
* Taux dʼouverture
* Taux de clic
* Taux de réponse

Le qualificateur de vente identifie les réponses d&#39;absence du bureau et les bounces avec leurs statuts correspondants, de sorte que vous puissiez les distinguer des engagements de prospect.

### Performances de réservation de réunion

Les cartes de statut de réservation de réunion résument la situation de vos réunions réservées. Filtrez les cartes pour vous concentrer sur les réunions et les statuts que vous souhaitez examiner.

## Intégrations et CRM

Grâce aux intégrations, le qualificateur de vente se connecte à votre CRM de sorte que le Account Qualification Agent (AQA) et les workflows sortants partagent une vue cohérente des prospects, comptes, contacts, activités et propriétaires dans Salesforce ou Microsoft Dynamics 365. Le qualificateur de vente lit les données et les activités de vente CRM pour enrichir les informations. Il peut également réécrire les activités de sensibilisation consignées et le statut d’opt-out. Il ne modifie pas par ailleurs vos enregistrements CRM via cette connexion.

Les connexions CRM, le mappage des champs entrants et la synchronisation des activités sont configurés par un administrateur sous **[!UICONTROL Administration]** > **[!UICONTROL Paramètres d’administration]** > **[!UICONTROL Connexions CRM]**. Les utilisateurs standard utilisent les données et les filtres CRM configurés, mais ne peuvent pas modifier ces paramètres.

### CRM MCP et le plug-in intégré

Le qualificateur de vente fonctionne avec votre CRM de plusieurs façons :

* **Requête sur les données du CRM via le MCP CRM** - Le Account Qualification Agent interroge les données du CRM en direct via le MCP CRM, de sorte que les réponses et les informations reflètent l’état actuel de vos enregistrements.
* **Plug-in intégré** - Le plug-in CRM intégré récupère les informations principales de [!DNL Marketo Sales Insights] (MSI) avec les nouvelles données agentiques, directement dans votre CRM. Depuis le plug-in, ajoutez un prospect au qualificateur de vente en un seul clic.
* **Synchronisation des activités** - Lorsqu’un administrateur active la **[!UICONTROL synchronisation des activités]**, les activités de proximité se synchronisent à nouveau dans le CRM, de sorte que les représentants voient l’activité du qualificateur de vente dans les outils qu’ils utilisent déjà.

>[!IMPORTANT]
>
>Pour accéder à **[!UICONTROL Paramètres d’administration]**, vous devez être membre des groupes d’utilisateurs `Sales Qualifier` et `Sales Qualifier Admins`.

### Étendue de l’accès CRM

Le qualificateur de vente lit les entités CRM dont il a besoin et ne peut écrire qu’un ensemble défini de données. Les entités typiques lues incluent les utilisateurs, les contacts, les mappages de propriétaires, les prospects, les comptes, les opportunités et les activités. L’écriture différée est limitée aux activités de sensibilisation enregistrées et au statut d’opt-out. Votre administrateur CRM prépare l’accès à l’API dans Salesforce ou Dynamics. Vous connectez ensuite le qualificateur de vente, mappez les champs entrants et choisissez de synchroniser ou non les activités dans l’application.

>[!NOTE]
>
>Les étapes d’identification qui suivent décrivent l’accès en lecture aux objets CRM. Si vous activez la synchronisation des activités ou l’écriture différée d’opt-out, contactez votre administrateur CRM pour obtenir l’accès en écriture correspondant à celui requis par votre configuration CRM.

### Préparation des informations d’identification dans votre CRM

Contactez votre administrateur CRM avant de connecter le qualificateur de vente. Vous trouverez ci-dessous un résumé des éléments généralement créés dans chaque système.

#### Microsoft Dynamics 365 (Dataverse/Power Platform)

1. Dans Azure Active Directory, enregistrez une application (**[!UICONTROL Enregistrements des applications]**).

   Notez les **ID client** et **ID client**, puis créez un **Secret client**.

1. Dans le **[!UICONTROL Centre d’administration Power Platform]**, ouvrez votre environnement et accédez à **[!UICONTROL Paramètres]** > **[!UICONTROL Utilisateurs + autorisations]** > **[!UICONTROL Utilisateurs de l’application]**.

1. Créez un utilisateur de l’application lié à cette application Azure AD.

1. Attribuez un rôle de sécurité qui accorde un accès **lecture** aux entités dont le qualificateur des ventes a besoin, telles que les prospects, les contacts, les comptes, les opportunités et les activités.

   L’application nécessite un rôle de sécurité avec un accès en lecture aux données de lecture.

**Informations à fournir lors de la connexion de Dynamics :**

* Identifiant client
* Secret client
* Identifiant du tenant
* URL de l&#39;instance Dynamics (URL de l&#39;organisation)

#### Salesforce

Dans Salesforce, [créez une application client externe](https://help.salesforce.com/s/articleView?id=xcloud.create_a_local_external_client_app.htm&type=5) (ou une _application connectée_) avec OAuth activé et des portées qui permettent à l’API d’accéder à l’identité et aux données, en respectant les normes de sécurité de votre organisation. L’utilisateur intégrateur doit disposer d’un accès en lecture à des objets tels que des prospects, des comptes, des contacts, des tâches, des événements et des opportunités. Les tâches administratives nécessitent souvent qu’un utilisateur disposant de l’autorisation **[!UICONTROL Gérer les applications connectées]** (entre autres autorisations) affiche une clé de client et un secret après sa création.

>[!PREREQUISITES]
>
>Pour créer une application client externe, un administrateur de produit doit vérifier que les éléments suivants sont activés (à partir du profil ou du jeu d’autorisations) :
>
>* Personnaliser l’application
>* Afficher l’installation et la configuration
>* Modifier toutes les données
>* Gérer les applications connectées (important)
>
>   Si l’option _Gérer les applications connectées_ n’est pas activée, vous ne pouvez pas afficher l’identifiant client et le secret client après avoir créé l’application client externe.

Lorsque vous créez l’application cliente externe, activez OAuth et accordez des autorisations. Activez également les informations d’identification client suivantes :

* Accéder au service d’URL d’identité (identifiant, profil, e-mail, adresse, téléphone)
* Gestion des données utilisateur via des API (api)
* Accéder aux identifiants d’utilisateur uniques (openid)

Après avoir créé l’application, activez à nouveau le flux d’informations d’identification du client et utilisez l’adresse électronique du contact comme nom d’utilisateur.  Lorsque les informations d’identification du client sont activées, configurez un utilisateur sur _Exécuter en tant que_.

Assurez-vous que l’utilisateur configuré dispose d’un accès en lecture aux objets suivants :

* Prospects
* Comptes
* Contacts
* Tâches
* Événements
* Opportunité
* OpportunityContactRoles
* OpportunityLineItems

**Informations à fournir lors de la connexion de Salesforce dans le qualificateur de vente :**

* Identifiant client (clé du client)
* Secret client (Consumer Secret)
* URL de rappel (telle que configurée sur l’application connectée)
* URL de l’instance Salesforce

>[!IMPORTANT]
>
>N’envoyez pas de secrets clients par e-mail. Utilisez le canal sécurisé approuvé de votre organisation pour partager les informations d’identification avec la personne qui les saisit dans le qualificateur de vente.

### Connexion à votre CRM

1. Connectez-vous au qualificateur de vente et vérifiez que le sandbox ou l’environnement approprié est sélectionné.

1. Dans le volet de navigation de gauche, développez **[!UICONTROL Administration]** et sélectionnez **[!UICONTROL Paramètres d’administration]**.

1. Sélectionnez **[!UICONTROL Connexions CRM]** sous **[!UICONTROL Intégrations]**.

   La page affiche des cartes pour Salesforce et Microsoft Dynamics. Une connexion inactive affiche **[!UICONTROL Connexion]**. Une connexion configurée affiche **[!UICONTROL Connecté]** et une action **[!UICONTROL Gérer]**.

   ![Paramètres d’administration Connexions CRM à Salesforce et cartes de connexion Dynamics](./assets/integrations-crm-connections.png){width="800" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Connexion]** pour le CRM que vous utilisez.

1. Saisissez l’ID client, les secrets, les valeurs de client ou de rappel et l’**URL de l’instance** à partir de votre administrateur CRM.

1. Une fois la connexion établie, vérifiez que la carte indique **[!UICONTROL Connecté]**.

### Instructions relatives aux URL d’instance

L’**URL de l’instance** doit être l’URL de base de l’environnement utilisée par votre CRM pour la configuration de l’API et de l’intégration, et non un nom d’hôte réservé à l’interface utilisateur.

**Salesforce**

1. Connectez-vous et notez votre organisation _Mon domaine_ sous-domaine dans la barre d’adresse du navigateur (valeur `{{mydomain}}`).

1. Pour le qualificateur de vente, utilisez le formulaire canonique : `https://{{mydomain}}.my.salesforce.com` .

   N’utilisez **&#x200B;**&#x200B;une URL `lightning.force.com` comme URL d’instance.

**Microsoft Dynamics 365**

1. Ouvrez votre CRM dans le navigateur et copiez l’URL de base depuis la barre d’adresse.

   Il se présente généralement sous la forme `https://{{org}}.crm.dynamics.com`.

### Mappage des champs CRM (mapping entrant)

Une fois le CRM connecté, sélectionnez **[!UICONTROL Gérer]** pour la connexion et ouvrez **[!UICONTROL Mapping entrant]**. Le mappage entrant contrôle les champs CRM que le qualificateur de vente extrait dans l’application.

1. Sélectionnez un groupe d’objets : **[!UICONTROL Contact]**, **[!UICONTROL Prospect]** ou **[!UICONTROL Compte]**.
1. Sélectionnez **[!UICONTROL Ajouter une section]** et saisissez un nom de section et une description facultative.
1. Ajoutez les champs CRM à la section .

   Chaque ligne de champ affiche ses **[!UICONTROL Nom d’affichage]**, **[!UICONTROL Nom du champ]** et **[!UICONTROL Type de données]**.

1. Activez **[!UICONTROL Filtrable]** pour chaque champ qui doit être disponible en tant que filtre sur la liste **[!UICONTROL Prospects]**.
1. Prévisualisez le mappage et enregistrez-le.

Les champs mappés apparaissent dans les zones correspondantes du qualificateur de vente :

* Les champs Prospect et Contact s’affichent dans l’onglet **[!UICONTROL Personne]** pour les prospects.
* Les champs Compte s’affichent dans la vue Compte.
* Les champs liés à l’opportunité apparaissent dans les zones d’opportunité de l’expérience de compte.

### Configuration de la synchronisation des activités (mapping sortant)

1. Dans **[!UICONTROL Connexions CRM]**, sélectionnez **[!UICONTROL Gérer]** pour le CRM connecté.
1. Ouvrez **[!UICONTROL Mapping sortant]**.
1. Activez **[!UICONTROL Synchronisation des activités]** pour synchroniser les activités de sensibilisation du qualificateur de vente avec le CRM.

Lorsque la synchronisation des activités est désactivée, le qualificateur de vente peut continuer à utiliser les données CRM entrantes, mais il n’écrit pas les activités de sensibilisation dans le CRM.

### Configuration du processus d’opt-out global des e-mails

1. Dans le volet de navigation de gauche, développez **[!UICONTROL Administration]** et sélectionnez **[!UICONTROL Paramètres d’administration]**.
1. Sélectionnez **[!UICONTROL Paramètres de messagerie]** sous **[!UICONTROL Conformité]**.
1. Activez **[!UICONTROL Inclure un lien d’opt-out dans chaque e-mail]** pour ajouter un pied de page de désabonnement aux e-mails sortants.
1. Dans **[!UICONTROL Modèle de message d’opt-out]**, saisissez le texte du pied de page. Incluez le jeton `{{opt_out_link}}` où le lien de désabonnement cliquable doit apparaître.
1. Enregistrez les paramètres.

Lorsqu’un prospect sélectionne le lien, le qualificateur de vente le supprime définitivement des autres e-mails. Le statut d’opt-out est également synchronisé à nouveau avec le CRM connecté.

### Référence : exemples de paramètres d’API

Votre équipe CRM peut utiliser ces exemples pour confirmer que l’accès en lecture renvoie les champs de prospect attendus.

**Dynamics (extrait de style OData)**

```text
$select=fullname,_ownerid_value,leadid,emailaddress1,jobtitle,statuscode,createdon,modifiedon,statecode
$filter=_ownerid_value eq '<crmUserId>' [AND additional filters]
$expand=Lead_ActivityPointers(...),parentaccountid(...)
$orderby=modifiedon desc
```

**Salesforce (extrait SOQL)**

```sql
SELECT Id, Salutation, FirstName, LastName, Name, Title, Company, Email,
  LeadSource, Status, OwnerId, LastModifiedDate, LastActivityDate, CreatedDate,
  (SELECT Id, Subject, ActivityDate, Status FROM Tasks ORDER BY ActivityDate DESC LIMIT 1),
  (SELECT Id, Subject, ActivityDateTime FROM Events ORDER BY ActivityDateTime DESC LIMIT 1)
FROM Lead
WHERE OwnerId = '<crmUserId>' AND IsDeleted = false
ORDER BY LastModifiedDate DESC
```

## Paramètres de profil

Les paramètres de profil spécifient des informations sur vous-même, notamment des détails personnels, l’adresse e-mail, le calendrier et la disponibilité du chat.

### Paramètres d’e-mail

Dans l’onglet **[!UICONTROL Paramètres de messagerie]**, configurez vos connexions par e-mail.

![Onglet Paramètres de messagerie affichant les options de connexion aux e-mails et la configuration des signatures e-mail](assets/email-settings.png)

* **[!UICONTROL Connexions e-mail]** - Cliquez sur **[!UICONTROL Connexion]** et suivez la procédure de connexion Microsoft.

* **[!UICONTROL Signature d’e-mail]** - Configurez la signature d’e-mail utilisée dans les e-mails générés automatiquement. Ajoutez votre lien [réservation de réunion](#meeting-booking) à la signature afin que les prospects puissent planifier du temps avec vous.

### Configuration du calendrier

Définissez votre fuseau horaire et votre disponibilité dans l’onglet **[!UICONTROL Configuration du calendrier]**.

<!-- 
![Calendar settings tab showing time zone and availability options](assets/calendar-settings.png)
-->

* **[!UICONTROL Connexion au calendrier]** - Cliquez sur **[!UICONTROL Connexion]** et suivez la procédure de connexion Microsoft pour intégrer votre calendrier.

* **[!UICONTROL E-mail de confirmation de réunion]** - Lorsqu’un client confirme une réunion avec vous, il reçoit l’e-mail de confirmation en tant que réponse. Utilisez ces paramètres pour définir l’objet et le corps de l’e-mail.

* **[!UICONTROL Préférences]** - Définissez la durée par défaut de votre réunion et la durée entre deux réunions consécutives.

Si vous déconnectez votre calendrier :

* Les liens de réservation actifs sont désactivés.
* La page de réservation affiche un état convivial, temporairement indisponible.
* La reconnexion conserve les paramètres.

### Disponibilité du calendrier

La disponibilité du calendrier dans le qualificateur de vente repose sur deux entrées :

* Votre calendrier professionnel connecté (Outlook ou Gmail)
* Votre disponibilité configurée + règles d’intervalle dans _Paramètres du calendrier_.

Le qualificateur de vente lit le statut de disponibilité à partir du calendrier connecté, et non le contenu complet de l&#39;événement, et l&#39;utilise avec les règles configurées pour décider quels emplacements de réservation un prospect peut voir.

Vous pouvez configurer les éléments suivants :

* Heures de travail par jour de la semaine
* Plusieurs blocs par jour (par exemple : 9 h-12 h et 1 h-5 h)
* Votre fuseau horaire
* Durée de la réunion
* Tampon avant/après les réunions
* Avis minimal
* Fenêtre de réservation

<!-- 
### Chat settings

In the **[!UICONTROL Chat settings]** tab, set your Timezone Live chat availability.

![Chat settings tab for configuring timezone and live chat availability](assets/chat-settings.png)

## Representative management

The _[!UICONTROL Representative management]_ panel displays the defined representatives and their calendar status.

## Meeting performance

This panel presents analytics around your completed meetings.
-->

<!--
 SHPHR-24341 remove section
## Set up the Chrome plugin

The AI Assistant Chrome plugin is available on the [Google Store](https://chromewebstore.google.com/detail/ai-assistant/hancbabllcmckehonngbdkhilocpdfji?authuser=0&hl=en).

When the plugin is installed in Chrome, the Adobe logo appears on the middle right when you are on an integrated site:

* Adobe web applications
* Salesforce
* Outlook
* Microsoft Dynamics and web applications
* Google applications 
-->
