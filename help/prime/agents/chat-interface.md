---
title: Interface de conversation
description: Utilisez le panneau de conversation de l’assistant AI dans Journey Optimizer B2B Prime pour créer des programmes, des parcours et des listes à l’aide du langage naturel ou du menu barre oblique (/).
badgeBeta: label="Beta" type="informative" tooltip="Cette fonctionnalité est actuellement en version bêta limitée"
autotag-review: '2026-06-12T22:46:23.441Z'
TQID: 'https://experienceleague.adobe.com/XyBLmqv63kNBcw-Jo4hKvUKIn2la7kac7-kTbNEU5aE'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
  - id: a30218bb-f80a-4410-8ac4-b039e99a15b4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 29d33656b0bd05e9fdf2cbdeb1f6e89d13c3d20e
workflow-type: tm+mt
source-wordcount: 869
ht-degree: 1%

---

# Interface de conversation

Le panneau de conversation est intégré à tout le [!DNL Adobe Journey Optimizer B2B Prime]. C’est là que vous interagissez avec les agents d’IA en utilisant un langage simple pour créer des programmes et des parcours, créer et comparer des listes de personnes, enquêter sur les prospects, configurer la notation, etc.

Sélectionnez l’icône _Assistant IA_ dans le volet de navigation de gauche pour ouvrir le panneau. L’en-tête du panneau comporte quatre commandes :

| Commande | Description |
|---------|-------------|
| **Nouvelle conversation** | Démarrer une nouvelle conversation (efface le thread actuel). |
| **Historique des conversations** | Ouvrez les conversations passées pour pouvoir en rouvrir une. |
| **Permuter les panneaux** | Déplacez le panneau de conversation de l’autre côté de l’espace de travail. |
| **Réduire** | Masquez le panneau pour donner plus d’espace à l’espace de travail. |

Au bas du panneau se trouve la boîte de message dans laquelle vous pouvez :

* Ajoutez un message et appuyez sur **Entrée** pour l’envoyer (**Maj+Entrée** insère une nouvelle ligne).
* Joignez un fichier à l’aide de l’icône _Joindre_ (formats pris en charge : `.txt`, `.md`, `.csv`, `.json`, `.xlsx`, `.docx`, `.pdf`). Utilisez les chargements de feuilles de calcul et de fichiers CSV pour démarrer une importation de prospect.

## Assistant Demander l’IA

Il existe deux manières tout aussi valables d’effectuer le travail : vous n’avez jamais besoin d’utiliser le menu barre oblique.

**Langage naturel** — Tapez votre demande de la même manière que vous le feriez à un collègue :

* _« Créez un parcours de bienvenue pour les nouvelles inscriptions à la version d’essai.«_
* _« Pourquoi john@acme.com n&#39;a-t-il pas rejoint ce parcours ?«_
* _« Comparez mes listes &#39;Participants au webinaire du 3e trimestre&#39; et &#39;Comptes d’entreprise&#39;.«_

L’agent adapte votre formulation à la compétence appropriée en arrière-plan et exécute le workflow approprié.

**Le menu barre oblique (/)** — Saisissez `/` pour ouvrir un menu de navigation de tout ce que l&#39;assistant peut faire. Cela s’avère utile lorsque vous souhaitez découvrir des fonctionnalités ou accéder directement à un workflow connu.

## Barre oblique (/)

Utilisez un `/` au début de la zone de message ou après un espace pour ouvrir le menu. Au fur et à mesure que vous continuez à taper, la liste filtre par nom, description ou ID — par exemple, `/journey` se réduit aux commandes liées au parcours.

Utilisez **/** pour parcourir les entrées, **Entrée** ou **Tabulation** pour les sélectionner, **Échap** pour les ignorer. Vous pouvez également cliquer directement sur une entrée.

Les entrées de menu sont regroupées en sections libellées :

| Section | Contient |
|---------|----------|
| **Enquête** | Diagnostics, recherches en lecture seule (par exemple, enquête de prospect, requêtes d’intention). |
| **Valider** | Workflows d’assurance qualité et d’audit. |
| **Créer** | Workflows de création (programmes, parcours, listes, notation). |
| **Importer** | Import de lead CSV. |
| **Other** (Autre) | Tout ce qui ne relève pas des catégories ci-dessus. |

Le menu répertorie également les **connecteurs** (par exemple, _Parcourir Marketo_ ouvre une boîte de dialogue de sélecteur) et **raccourcis de navigation** qui vous font accéder à un écran de l’espace de travail.

### Sélectionner un élément de menu

Lorsque vous sélectionnez une compétence ou un agent dans le menu, une invite de démarrage est insérée dans la zone de message pour que vous puissiez la modifier ; elle n’est **pas** envoyée automatiquement. Par exemple, si vous sélectionnez _Planifier des campagnes_ , le menu _« Planifier un nouveau programme Marketo pour [nom de la campagne] apparaît. Je vais charger le dossier.«_ Renseignez les espaces réservés entre crochets et appuyez sur **Entrée** pour envoyer.

Les connecteurs ouvrent une boîte de dialogue modale au lieu d’insérer du texte. Les raccourcis de navigation vous permettent d’accéder directement à cet écran dans l’espace de travail.

>[!NOTE]
>
>Certaines commandes apparaissent grisées et marquées _Bientôt disponible_. Ils sont enregistrés par des indicateurs de fonctionnalité et ne sont pas encore actifs pour votre compte ; en sélectionner un n’a aucun effet. L’ensemble disponible dépend des fonctionnalités qui sont activées pour vous.

## Compétences

Une compétence est un workflow empaqueté que l’agent sait exécuter : les éléments de base à la fois du menu `/` et des requêtes en langage naturel. Chaque compétence regroupe des instructions détaillées et les outils spécifiques nécessaires pour une tâche (par exemple, « publier un parcours », « comparer deux listes de personnes », « créer un modèle de notation »).

Éléments clés à connaître concernant les compétences :

* **Les compétences sont limitées au produit.** Dans AJO B2B Prime, vous verrez les compétences B2B d’AJO (parcours, listes de personnes, notation, canaux, optimisation de l’heure d’envoi, etc.). Quelques compétences sont limitées au Marketo et quelques-unes travaillent sur les deux produits (importation de lead, connaissance du produit). Vous ne voyez que les compétences pertinentes par rapport à l’endroit où vous êtes.
* **Vous n’avez pas besoin de mémoriser les noms des compétences.** Décrivez votre objectif et l’agent sélectionne la compétence correspondante. Le menu `/` est un raccourci plus rapide et détectable vers les mêmes workflows.
* **Certaines compétences ne font que lire, d’autres changent les choses.** Les compétences d’enquête et de rapport (par exemple, enquête de prospect, requête d’intention, rapport d’heure d’envoi) ne lisent que les données. Développez et configurez des compétences (par exemple, création de parcours, notation) pour créer ou modifier des données.

## Invites de relance

Une fois que l’assistant a répondu, une ligne d’invites de suivi cliquables adaptées à ce que vous venez de faire s’affiche souvent. Par exemple, après la création d’un parcours, il peut vous proposer l’_« Publier ce parcours »_ ou _« Ajouter une étape d’attente »_. Cliquez sur l’un d’eux pour continuer sans saisir de caractères. Il ne s’agit que de suggestions. Vous pouvez toujours saisir votre propre message suivant à la place.

## Conseils

* **Soyez spécifique avec les identifiants.** Lors de l’enquête ou de la modification, incluez l’adresse e-mail, le nom de personne, le nom de parcours ou le nom de liste afin que l’agent agisse sur la ressource appropriée.
* **Utiliser `/` pour explorer.** Si vous ne savez pas ce que l&#39;assistant peut faire, ouvrez le menu `/` et parcourez les catégories.
* **Modifiez l’invite de démarrage.** La sélection d’une compétence vous donne un modèle : remplacez les espaces réservés `[bracketed]` avant l’envoi.
* **Charger d’abord pour les importations.** Pour une importation de prospect, joignez d’abord le fichier CSV, puis décrivez ce que vous souhaitez en faire.
* **Démarrer une nouvelle conversation** lorsque vous passez à une tâche non liée, de sorte que le contexte précédent n’affecte pas la nouvelle demande.
