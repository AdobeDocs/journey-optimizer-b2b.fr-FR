---
title: Assistant d’IA dans Journey Optimizer B2B edition
description: 'Accélérez les workflows avec l’assistant IA : obtenez des connaissances sur les produits, une aide au dépannage et des informations opérationnelles pour Journey Optimizer B2B Edition.'
feature: AI Assistant
role: User, Admin
level: Beginner
exl-id: 52ff66d2-1969-4e2c-985a-c75e613368de
source-git-commit: 4fdd89bf32cb9d68b4cdc347f1fd09df8eabe24d
workflow-type: tm+mt
source-wordcount: '1258'
ht-degree: 6%

---

# Assistant d’IA dans Journey Optimizer B2B edition

L’assistant AI dans Journey Optimizer B2B edition est créé à partir de la même base technologique que l’[assistant AI dans Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/ai-assistant/home){target="_blank"}. Il s’agit d’une expérience de conversation que vous pouvez utiliser pour accélérer vos workflows dans Adobe Journey Optimizer B2B edition. Vous pouvez utiliser l’assistant d’IA pour mieux comprendre les fonctionnalités du produit, résoudre les problèmes ou parcourir les informations et trouver des informations opérationnelles pour Journey Optimizer B2B edition.

>[!IMPORTANT]
>
>Un accord sur les [instructions d’utilisation](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html) est requis avant de pouvoir utiliser l’assistant AI dans Journey Optimizer B2B edition. Cet accord contient également l’accord bêta public afin que vous puissiez utiliser des fonctionnalités supplémentaires de l’assistant AI lors de leur déploiement en version bêta.

+++Affichage de l’interface du contrat utilisateur

![Première page du contrat d’utilisation.](./assets/user-agreement-1.png)

![Dernière page du contrat d’utilisation.](./assets/user-agreement-2.png)

+++

## Fonctionnalités de l’assistant AI dans Journey Optimizer B2B edition

Pour formuler une réponse à vos questions envoyées, l’assistant AI interroge une base de données et traduit les données de la base de données en une réponse lisible par l’utilisateur. Cette réponse est une représentation interne des données sous-jacentes. Elle est également connue sous le nom de _**_graphique de connaissances_**_, un réseau complet de concepts, de données et de métadonnées pour une réponse donnée. Le graphique de connaissances se compose de sous-graphiques qui sont référencés chaque fois que des requêtes sont envoyées :

* Documentation Experience League.
* Artefacts opérationnels, tels que des schémas, des champs, des audiences et des parcours.

Déterminez le type de requête dont vous avez besoin avant d’envoyer une requête de l’assistant AI :

### Connaissances du produit

La connaissance des produits fait référence aux concepts et aux sujets abordés dans la documentation de Journey Optimizer B2B edition sur Adobe Experience League. Les questions relatives à la connaissance des produits peuvent être spécifiées de manière plus détaillée dans les sous-groupes suivants :

| Connaissances du produit | Exemples |
| --- | --- |
| Apprentissage par points | <li>Qu&#39;est-ce qu&#39;un groupe d&#39;achat ? <li> Me montrer un exemple de modèle de rôles de groupe d&#39;achat ? |
| Ouvrir la découverte | <li>Quelles sont les étapes pour créer des groupes d&#39;achat ? <li>Comment utiliser les champs personnalisés dans un modèle de rôles de groupe d&#39;achats ? |
| Dépannage | <li>Pourquoi les groupes d&#39;achat pour mon parcours n&#39;ont-ils pas été créés ? <li>Pourquoi ne puis-je pas trouver des événements d’expérience à écouter dans le parcours ? |

### Informations opérationnelles

_Informations opérationnelles_ reportez-vous aux réponses que l’assistant AI génère sur vos objets de métadonnées (attributs, audiences de compte, flux de données, jeux de données, destinations, parcours de compte, schémas, sources, modèles de groupe d’achat et centres d’intérêt des solutions). Ces informations incluent les nombres, les recherches et l’impact de la parenté. Elles n’examinent aucune donnée dans le sandbox.

* Quelle audience de compte a la plus grande taille d’audience et quelle est cette taille ?
* Combien d’audiences de compte n’ont jamais été utilisées dans aucun parcours ?
* Quels parcours actifs utilisent l’intérêt de la solution _x_ ?

Vous pouvez poser des questions à l’assistant d’IA sur vos informations opérationnelles dans les domaines suivants :

| Domaine | Métadonnées prises en charge | Métadonnées non prises en charge |
| --- | --- | --- |
| Attributs/champs | <li>Recherche de nom d’attribut <li>Attribut - relation de schéma <li>Attribut - relation du jeu de données <li>Attribut - Relation d’audience <li>Attribut - relation de destination | <li>Classe d’attribut <li>Audit <li>Statut d’obsolescence <li>Libellés <li>Valeur stockée dans les attributs |
| Audiences du compte <br><br>**_Remarque:_** l’assistant AI B2B d’AJO ne peut répondre aux questions d’audience que pour les audiences de compte, tandis que l’assistant AI d’Experience Platform ne peut répondre qu’aux questions des audiences de personne | <li>Nombre d’audiences <li>Type d’audience (diffusion en continu ou par lots) <li>Dates de création/modification <li>Statut d’activation <li>Nombre de membres <li>Dupliquer les audiences <li>Recherche par nom et ID | <li>Chevauchements des audiences <li>Activation de l’audience <li>Audit <li>Créer/modifier <li>Libellés <li>Tendances de qualification des membres |
| Flux de données | <li>Nombre de flux de données <li>Statut du flux de données <li>Flux de données - Relation du jeu de données <li>Flux de données - Relation source | <li>Création/modification <li>Relations flux de données-lot <li>Ingérer le nombre de profils |
| Jeux de données | <li>Nombre de jeux de données <li>Statut d’activation du profil <li>Date de création/modification <li>Jeu de données - Relation de schéma <li>Jeu de données - Relation d’audience <li>Relation jeu de données - attribut <li>Jeu de données - Relation de flux de données <li>Recherche de nom <li>Recherche par nom et ID | <li>Audit <li>Créé par <li>Jeu de données - Relation par lots <li>Création/modification de jeu de données <li>Taille du jeu de données <li>Nombre de profils <li>Nombre de lignes <li>Recherche de valeur |
| Destinations | <li>Nombre de destinations configurées <li>Relation destination-audience <li>Relation d’attributs de destination | <li>Configuration du compte <li>Informations d’identification du compte <li>Profils uniques activés |
| Parcours (Parcours de compte) | <li>Nombre <li>Recherche par nom et ID <li>Statut du parcours <li>Dates de création/modification | <li>Audit Attributs - Relations de parcours <li>Création/modification <li>Créé par |
| Schémas | <li>Nombre de schémas <li>Date de création/modification <li>Schéma - Relation des attributs <li>Schéma - Relation du jeu de données <li>Schéma - Relation d’audience <li>Statut d’activation du profil <li>Recherche de nom <li>Recherche par nom et ID | <li>Audit <li>Création/modification <li>Créé par <li>Groupes de champs <li>Identités <li>Espaces de noms d’identité <li>Libellés <li>Nombre de profils |
| Sources | <li>Comptes <li>Statut du compte <li>Flux de données actifs/inactifs pour chaque compte <li>Connecteur Source - Relation de flux de données <li>Compte Source - relation du flux de données | <li>Informations d’identification du compte <li>Configuration du compte Mesures d’ingestion de données <li>Nombre de relations profilsSource - lot |
| Modèle de groupe d&#39;achat | <li>Comptages <li>Statut <li>Rôles <li>Recherche par nom et ID | <li>Règles de rôle |
| Intérêt de la solution | <li>Comptages <li>Statut <li>Intérêt de la solution - Relation du modèle de groupe d’achat <li>Recherche par nom et ID | <li>Intérêt de la solution - Relation du groupe d’achat |

{style="table-layout:fixed"}

Pour les questions relatives aux informations opérationnelles, les réponses peuvent ne pas refléter l’état actuel de l’interface utilisateur. Les données sur lesquelles reposent ces questions sont mises à jour toutes les 24 heures. Par exemple, les modifications apportées par les utilisateurs et utilisatrices dans Real-Time CDP pendant la journée sont synchronisées avec les entrepôts de données la nuit, puis répondent aux questions des utilisateurs et utilisatrices le matin. Connectez-vous à un sandbox pour vous renseigner sur des données spécifiques liées aux objets .

### Périmètre de la fonctionnalité

Actuellement, la portée de l’assistant AI est la suivante :

* **Connaissance des produits** : l’assistant AI peut répondre aux questions sur la connaissance des produits pour Real-Time Customer Data Platform et Adobe Journey Optimizer B2B edition.

* **Informations opérationnelles** : vous pouvez poser des questions à l’assistant IA pour obtenir des informations opérationnelles sur les objets de données suivants : attributs, audiences de compte, flux de données, jeux de données, destinations, parcours de compte, schémas, sources, modèles de groupe d’achat et centres d’intérêt des solutions.

### Confidentialité, sécurité et gouvernance

L’assistant AI de Journey Optimizer B2B edition place la confidentialité, la sécurité et la gouvernance au premier plan. Consultez les informations suivantes pour en savoir plus sur les fonctionnalités axées sur la confiance du client que vous pouvez attendre de l’assistant AI :

* Aucune donnée personnelle n&#39;est actuellement utilisée par AI Assistant, même à des fins de formation.

* L’assistant AI ne connaît pas les données client, telles que les personnes, les comptes, les opportunités et les groupes d’achats.

* Vous devez disposer d’autorisations explicites pour interagir avec l’assistant AI.

   * Un administrateur peut définir des autorisations à l’aide de l’interface utilisateur [Autorisations](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions){target="_blank"} et de [Admin Console](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/browse){target="_blank"}.

   * Les autorisations sont granulaires et votre administrateur de sandbox peut configurer les utilisateurs autorisés à poser différentes catégories de questions (questions basées sur les connaissances du produit avec l’assistant AI ou questions sur les informations opérationnelles).

* Vous pouvez consulter un journal de vos interactions précédentes avec l’assistant AI avec une politique de conservation de 30 jours.

* L’assistant AI repose sur des données spécifiques aux sandbox et sur la documentation publique d’Adobe lorsqu’il répond aux invites des utilisateurs. Les données ne sont pas partagées entre les sandbox.

* Les invites que vous fournissez à l&#39;assistant AI ne sont pas partagées avec les autres clients.

### Questions fréquentes

Vous trouverez ci-dessous une liste de réponses aux questions fréquentes sur l’assistant AI dans Journey Optimizer B2B edition.

**Les informations de l’assistant AI sont-elles fournies en temps réel ?**

Les données présentées dans les réponses de l’assistant AI sont mises à jour quotidiennement. Ce cycle signifie que les données incluses dans les réponses peuvent être jusqu’à 24 heures plus anciennes que les données affichées dans l’interface utilisateur au moment de la réponse.

**Quelles sont les fonctionnalités de l’assistant AI ?**

L’assistant AI peut répondre aux requêtes sur les connaissances des produits Adobe et aux questions liées aux informations opérationnelles de vos artefacts opérationnels.

**L’assistant AI peut-il fournir des informations sur les données client ?**

Non. L’assistant AI n’a pas accès aux données client et par conséquent, elles ne sont pas consultées ni utilisées par l’assistant AI.

**Mes informations personnelles sont-elles utilisées dans les données de formation de l’assistant AI ?**

AI Assistant n’utilise pas d’informations personnelles à des fins de formation. Ne fournissez aucune information personnelle sur vous-même (y compris votre nom ou vos coordonnées) ou toute autre partie à AI Assistant.

## Étapes suivantes

Avec une compréhension générale de l’assistant AI, passez à l’activation et à l’utilisation de l’assistant AI au cours de vos workflows. Pour plus d’informations, reportez-vous à la documentation suivante :

* [Activer l’accès à l’assistant IA](./enable-ai-assistant-access.md)
* [Conseils sur les questions](./question-guidance.md)
* [Utiliser l’assistant IA](./use-ai-assistant.md)
