---
title: Journey Agent B2B
description: Découvrez comment utiliser le Journey Agent optimisé par l’IA et ses compétences pour créer, gérer et observer des parcours B2B robustes.
feature: Account Journeys, Person Journeys, Agentic AI
role: User
exl-id: 5d2945ab-4f6c-4d9c-b0a1-1a93dc1849f3
source-git-commit: 51bb47fe4f494095f1c598639f02f273b9a125ae
workflow-type: tm+mt
source-wordcount: '1170'
ht-degree: 0%

---

# Journey Agent B2B

Journey Agent B2B est un assistant optimisé par l’IA dans Adobe Journey Optimizer B2B edition qui vous aide à concevoir, exécuter, optimiser et surveiller les parcours B2B via le langage naturel. Il réduit le temps et la complexité nécessaires à la création et à la gestion des parcours clients en combinant l’automatisation, les recommandations basées sur les données et l’observabilité en temps réel.

![Invite B2B Journey Agent](./assets/journey-agent-prompt.png)

Le B2B de Journey Agent fournit un ensemble de compétences en IA, chacune axée sur un aspect différent du cycle de vie du parcours B2B. Les compétences actuellement disponibles sont les suivantes :

* **[Compétences de création de Parcours](#journey-build-skill)** - Créez, mettez à jour et optimisez des parcours à partir d’invites de langage naturel.
* **[Compétence Observabilité du Parcours](#journey-observability-skill)** - Posez des questions sur la manière dont les comptes et les personnes se déplacent dans les parcours actifs

## Parcours Développer les compétences

Les compétences Parcours Build traduisent vos objectifs marketing, votre stratégie d’engagement et vos KPI en parcours client B2B complets. Il relève trois défis majeurs auxquels sont confrontés les marketeurs B2B aujourd’hui :

* Gérer des parcours clients de plus en plus complexes (complexité en termes d’audience, de contenu et de messagerie, et omnicanal)
* Accroître l&#39;efficacité dans un contexte de resserrement budgétaire
* Déterminer la structure du parcours client optimal

En tant que spécialiste marketing, vous pouvez utiliser cette compétence pour :

* **Créer** - Transformez vos objectifs marketing, produits, stratégie d’engagement et KPI en un parcours client personnalisé avec automatisation et conditions
* **Recommander** - Tirez parti des engagements marketing passés et d’autres données historiques pour optimiser la création de parcours
* **Optimiser** - Analysez, ajustez et optimisez les parcours actifs en fonction des prévisions ou des performances réelles.
* **Gérer** - Hiérarchisez, gérez et orchestrez les parcours et la diffusion de messages qui se chevauchent

### Utilisation de base

Pour utiliser la compétence Journey Agent Build, saisissez dans la fenêtre d’invite ce que vous souhaitez créer, en utilisant le langage naturel :

« Créez un parcours B2B pour inviter les décideurs à une présentation dans les comptes engagés les plus susceptibles d’ouvrir un nouveau pipeline. »

![Invite B2B de l’agent de Parcours pour la compétence Créer](./assets/journey-agent-tasks.png)

Plus vous pouvez fournir de détails, mieux la réponse sera. Si des documents marketing existants décrivent l’événement, votre produit, etc., collez-les dans l’invite afin que l’agent ait une meilleure idée de l’objectif.

« Agissez en tant que stratégiste du parcours B2B pour créer un parcours de compte client à plusieurs étapes qui nourrit et implique les décideurs et les personnages marketing dans la phase d’exploration initiale de `<Solution Name>`. L’objectif est de convertir des visiteurs anonymes en contacts connus, d’approfondir l’engagement avec du contenu pertinent sur `<domain>`.com et de créer des prospects qualifiés pour la sensibilisation aux ventes `<Product Name>`. Utilisez des canaux tels que les e-mails et les médias achetés, en exploitant les segments d’audience et le contenu existants. Structurez le parcours entre les étapes de sensibilisation, de considération et d’évaluation sur 4 à 6 semaines, avec des déclencheurs, des actions et des objectifs clairs pour chaque étape. Incluez des KPI tels que les taux de conversion, les scores d’engagement et les demandes de démonstration, et renvoyez la sortie sous la forme d’un flux de parcours structuré. »

Cette invite détaillée fournit les éléments suivants :

* **Effacer l’intention** : que souhaitez-vous que l’IA fasse ? Soyez précis au sujet de la tâche ou du résultat.
* **Riche en contexte** : fournissez un arrière-plan ou des contraintes pertinents. Incluez des exemples ou des références si possible.
* **Format structuré** : utilisez des puces, des étapes numérotées ou des modèles.
* **Affectation de rôle** : spécifiez le rôle de l’IA - « Agir en tant qu’analyste de données... »

Utilisez l’agent pour itérer l’affinement : commencez simplement, puis affinez votre invite en fonction des résultats. Les boucles de rétroaction améliorent les résultats au fil du temps.

### Création de parcours B2B de bout en bout

La compétence Création de Parcours peut générer un flux de parcours de bout en bout (parcours de compte ou de personne) à partir d’invites textuelles et de métadonnées en langage naturel, par le biais d’une expérience de conversation plutôt que d’une interface utilisateur traditionnelle.

Exemples complets d’invites de Parcours :

* Créez un parcours cross-canal pour nourrir les comptes qui n’ont pas interagi avec mon contenu au cours des 30 derniers jours.
* Créez un parcours de vente croisée d’une solution à des comptes présentant une intention élevée sans pipeline ouvert en fournissant du contenu personnalisé pour les rôles de groupe d’achat les plus importants.
* Créez un parcours B2B pour inviter les décideurs à une présentation dans les comptes engagés les plus susceptibles d’ouvrir un nouveau pipeline.
* Création d’un parcours pour les comptes d’espaces blancs avec l’intention de ma solution, en mettant l’accent sur les personnes impliquées dans le contenu du site web.

### Parcours à plusieurs étapes

Vous pouvez agir en tant que concepteur de parcours B2B pour créer un parcours de compte client à plusieurs étapes qui informe les décideurs et les personnages marketing dès le début de la phase d’exploration.
L’objectif est de convertir des visiteurs anonymes en contacts connus, d’approfondir l’engagement avec du contenu pertinent et de créer des pistes qualifiées pour la sensibilisation des ventes.

* Utilisez des canaux tels que `Email`, `Paid media` et `Personalized web experiences` pour tirer parti des segments et du contenu d’audience existants.
* Structurez le parcours entre les étapes `awareness`, `consideration` et `evaluation` sur 4 à 6 semaines, avec des déclencheurs, des actions et des objectifs clairs pour chaque étape.
* Incluez des KPI, tels que `conversion rates`, `engagement scores` et `demo requests`, et renvoyez la sortie sous la forme d’un flux de parcours structuré.

## Compétence d’observabilité de parcours

Les compétences en observabilité des Parcours vous permettent de poser des questions en langage naturel sur la manière dont les comptes et les personnes se déplacent dans vos parcours B2B, sans devoir parcourir les cartes de parcours, les journaux ou les tableaux de bord. Il couvre deux domaines principaux : la progression des parcours et l’observabilité de la synchronisation des données.

Vous pouvez y accéder à deux endroits dans Journey Optimizer B2B edition :

* **Assistant Rail droit dans la carte des parcours** - Posez des questions spécifiques aux parcours directement à partir de la carte des parcours. Le nom du parcours est automatiquement injecté dans le contexte.

* **Page de l’assistant plein écran** - Une vue conversationnelle plus large adaptée aux questions complexes ou entre comptes et à l’exploration de plusieurs parcours.

### Insight de parcours au niveau du compte

Suivez le cheminement d’un compte spécifique dans un parcours en posant des questions telles que :

* « Donnez-moi des informations de base sur le compte ACME Industries. »
* « Dites-moi comment le compte Northstar Services a suivi la stratégie parcours de soutien des GAB. »
* « Quand le compte Contoso LLC a-t-il lancé ce parcours ? »

### Raisonnement et comptage du chemin du nœud partagé

Comprenez pourquoi une branche a été utilisée et combien de personnes ou de comptes ont suivi chaque chemin :

* « Pourquoi le compte QiDemoAccount24 a-t-il accédé au petit chemin technique US California au nœud partagé c764a9 ? »
* « Indiquez-moi le nombre de personnes pour chaque chemin d’accès dans le nœud partagé 459c7c. »
* « Montrez-moi des personnes sur le chemin San Jose pour le compte8. »

L’agent examine la logique de partage, les attributs de compte et les activités pour expliquer les décisions de routage et le nombre de retours par chemin ou les listes de personnes.

### Résultats du parcours au niveau des personnes

Analysez les résultats individuels au sein d’un compte ou sur l’ensemble d’un parcours, ce qui est particulièrement utile pour l’analyse de groupe d’achat et le suivi du comportement des décideurs par rapport à celui des influenceurs :

* « Donnez-moi le nombre de personnes dans chaque chemin pour ce nœud partagé pour le compte 123. »
* « Répertorier les personnes dans le chemin de saut masqué. »
* « Montrez-moi les personnes dont le chemin d’accès à l’emplacement est San Diego pour ce compte. »

### Cycle de vie et durée du parcours

Récupérez les dates et heures clés d’un parcours ou de comptes spécifiques :

* « Quand ce parcours a-t-il été mis en ligne ? »
* « Quand le premier compte a-t-il rejoint ce parcours ? »
* « Quand le compte QiDemoAccount50 a-t-il démarré ce parcours ? »

### Audience externe et visibilité de l’activation

Pour les parcours qui diffusent vers des canaux externes tels que LinkedIn, vous pouvez vérifier le statut d’activation :

* « bsmith@acme.com est-il présent dans l’audience externe ? »
* « Répertoriez toutes les personnes activées sur LinkedIn via ObservabilityExtAudience01. »

### Synchronisation des données et observabilité du pipeline

La compétence Observability peut également faire apparaître les informations d’intégrité de la synchronisation des données pour aider à résoudre les problèmes qui peuvent expliquer pourquoi un compte ou un prospect n’a pas été inclus dans un parcours :

* Mesures et statut de la tâche d’exportation d’audience externe
* Plannings de segmentation par lots et heures d’achèvement
* Planification de la maintenance du groupe d&#39;achats
* Statut du gestionnaire de tâches (terminé/échec)