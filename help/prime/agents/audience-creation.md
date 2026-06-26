---
title: Création d’audiences pour des programmes
description: Utilisez les compétences de création d’audience dans Journey Optimizer B2B Prime pour créer des listes de personnes, adapter les listes dynamiques Marketo et modifier les règles de liste dans le chat.
badgeBeta: label="Beta" type="informative" tooltip="Cette fonctionnalité est actuellement en version bêta limitée"
autotag-review: '2026-06-25T19:19:21.361Z'
TQID: 'https://experienceleague.adobe.com/l3xd0u8LR0UDLfeGMXPEEJ9qwXPJX5DxkaH41W4Q7PE'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
  - id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
  - id: ff10f619-348f-47e3-99bf-3ce4c817cf2c
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 0f014bd931324eb41e841a788ee4cf2058522455
workflow-type: tm+mt
source-wordcount: 1496
ht-degree: 2%

---

# Créer des audiences pour les programmes

Dans [!DNL Adobe Journey Optimizer B2B Prime], les [_listes de personnes_](../audiences/people-lists.md) définissent l’audience des parcours de personnes, sous la forme de listes dynamiques basées sur des filtres qui se mettent à jour automatiquement ou de listes statiques à appartenance fixe. À partir de l’[interface de conversation](./chat-interface.md), la compétence _Création d’audience_ permet d’établir, d’adapter et de modifier des listes de personnes par le biais d’une conversation guidée.

* **Compétences** - `audience-creation` et `people-list-comparison`
* **Appel** - Décrivez directement les critères d’audience, chargez une liste dynamique [!DNL Marketo Engage] ou nommez une liste existante à modifier
* **Lit à partir de / écrit sur** - [!DNL Journey Optimizer B2B Prime] ; lit le [!DNL Marketo Engage] lors de l’adaptation des listes intelligentes

## Workflows pris en charge {#workflows}

L’assistant prend en charge trois workflows et détermine celui qui s’applique à partir de votre requête. Si votre intention est ambiguë, il vous demande avant de continuer.

| Workflow | Quand l’utiliser | Exemple d’invite |
|---|---|---|
| **Créer en partant de zéro** | Vous souhaitez une nouvelle liste de personnes définie par critères ou appartenance. | _« Créez une liste dynamique de vice-présidents marketing dans les entreprises SaaS en Amérique du Nord. »_ |
| **Adapter une [!DNL Marketo Engage] liste dynamique** | Vous disposez déjà d’une liste dynamique de [!DNL Marketo Engage] ou d’une campagne dynamique et souhaitez une liste de personnes équivalente. | _« Adaptez cette liste dynamique Marketo en liste de personnes.«_ (joindre la ressource) |
| **Modifier une liste existante** | Vous souhaitez ajouter ou remplacer des règles dans une liste que vous avez déjà. | _« Ajoutez une règle à ma liste &#39;Essais sur les entreprises&#39; pour un score de prospect supérieur à 50.«_ |

## Créer entièrement une liste de personnes {#create-from-scratch}

Avant de générer quoi que ce soit, l’assistant confirme les quatre éléments suivants. Il demande toutes les données manquantes dans un seul message.

1. **Règles/critères** — Description en langage clair de la personne qui fait partie de la liste.
1. **Nom** — Comment appeler la liste.
1. **Emplacement** — Dans quel programme la liste doit se trouver. Indiquez un nom de programme que l’assistant trouvera ; s’il existe plusieurs correspondances, il vous demandera de sélectionner.
1. **Type** : dynamique (basée sur des filtres, mise à jour automatique) ou statique (appartenance fixe). Ceci est obligatoire — l&#39;assistant ne devinera pas ; si vous ne spécifiez pas, il demande.

### Listes dynamiques

Pour les listes dynamiques, l’assistant suggère de manière proactive d’inclure des attributs de personnalisation pour enrichir le ciblage. Ces attributs sont **_inclus par défaut — vous vous désinscrivez, pas dans_** :

| Attribut | Pourquoi cela est utile |
|---|---|
| **Persona dérivé** | persona acheteur déduit par l’IA pour le ciblage du contenu basé sur les personas. |
| **Intention dérivée** | Les intentions d’achat présumées signalent que les comptes sur le marché apparaissent. |
| **Niveau d’engagement** | Niveau d’engagement calculé qui donne la priorité aux contacts engagés. |

Prévenez l&#39;assistant si vous souhaitez supprimer l&#39;un de ces éléments avant de continuer.

### Listes statiques

* **Statique, aucun critère** — La liste est créée vide, prête pour que vous ajoutiez manuellement des membres.
* **Statique à partir de critères (instantané)** — L’assistant AI crée l’ensemble correspondant et copie ces personnes dans. La population est asynchrone : l’assistant confirme que la liste a été créée, mais note que l’affichage des personnes peut prendre quelques minutes. Il ne prétendra pas que la liste est prête immédiatement.

## Vérifier la carte {#review-card}

Rien n’est créé tant que vous ne l’avez pas approuvé. Une fois vos critères décrits, l’assistant présente une vignette interactive _Révision de la création de la liste de personnes_ (pour les adaptations à partir de [!DNL Marketo Engage] listes, la vignette est intitulée _Révision de la conversion de la liste de personnes_).

Chaque ligne de la carte représente une condition :

| Colonne | Signification |
|---|---|
| **Conditions requises** (ou le nom de la liste [!DNL Marketo Engage] pour les adaptations) | Votre demande d’origine ou le filtre Marketo source. |
| **(règle)** | Règle basée sur les attributs réelle générée pour cette condition. |
| **Include** | Case à cocher permettant de conserver ou de supprimer cette règle. |

**Niveaux de confiance :**

* **Degré de confiance élevé** les lignes sont correctement appariées et vérifiées par défaut.
* **Faible degré de confiance** les lignes (mappages approximatifs ou éléments marqués d’un indicateur) sont affichées avec un indicateur d’avertissement et ne sont pas cochées par défaut.
* Les lignes que le système n&#39;a pas pu mapper indiquent **« Aucun équivalent trouvé »** — elles n&#39;ont pas de règle et ne sont pas cochées.

Un _Résumé des conversions_ affiche _N degré de confiance élevé_ et _N degré de confiance faible_, avec un indice : les règles de confiance faible ne sont pas cochées par défaut ; cochez-les pour inclure, ou décrivez la modification que vous souhaitez apporter dans la conversation.

**Actions de carte :**

* **Continuer** — Crée la liste en utilisant uniquement les règles cochées.
* **Décrivez les modifications que vous souhaitez apporter dans la conversation** — Préremplit la saisie avec _« Je souhaite modifier : «_ pour que vous puissiez l’affiner ; l’assistant AI se régénère et affiche une nouvelle carte, en conservant les règles que vous avez déjà approuvées.

Vous pouvez également saisir un suivi à tout moment (par exemple, _« également limiter aux sociétés de plus de 500 employés »_) et l’assistant AI régénère la carte.

## Mappage des attributs {#attribute-mapping}

Lorsque vous décrivez des critères, l’assistant convertit chaque condition en un attribut réel et connu au niveau de la personne. Trois résultats peuvent apparaître sur la carte Révision :

1. **Correspondance (degré de confiance élevé)** — Votre condition correspond directement à un attribut (par exemple, _« email is acme.com »_ correspond à l’attribut `email`). Activé par défaut.
1. **Approximatif (faible degré de confiance)** — L’attribut disponible le plus proche diffère par son nom ou son modèle de données (par exemple, un filtre Marketo _Montant_ approximatif sous la forme _Score du lead_). Affiché avec une note expliquant la différence ; non coché par défaut.
1. **Introuvable** — La condition n&#39;a pu être mappée à aucun attribut connu. Affiché comme _« Aucun équivalent trouvé »_ ; aucune règle n’est générée.

C’est pourquoi une liste que vous décrivez peut comporter moins de règles que de conditions que vous n’en avez spécifiées. Les conditions non correspondantes sont affichées explicitement au lieu d’être supprimées silencieusement. Si des critères importants tombent comme « introuvables », reformulez-les en utilisant le nom réel de l’attribut et l’assistant tentera à nouveau de les remplir.

>[!NOTE]
>
>Si vous mappez des colonnes de feuille de calcul à des champs (une carte Mappage de champs avec _Colonne_, _Champ cible_, un pourcentage de confiance et une liste _Colonnes non mappées_), il s’agit du flux d’importation de prospect, et non de la création d’audience. Voir la compétence [import-leads](./skills.md#audiences-people).

## Modification des règles d’une liste existante {#edit-rules}

Lorsque vous demandez à modifier des règles sur une liste que vous avez déjà, l’assistant détermine la liste et le mode de modification :

* **Ajouter/ajouter** (par défaut pour _« ajouter des règles »_, _« ajouter plus de règles »_) — les nouvelles règles sont fusionnées avec les règles existantes.
* **Remplacer** (par défaut pour _« remplacer les règles »_, _« modifier les règles en »_) — les nouvelles règles remplacent toutes les règles existantes dans la liste.

L’assistant résume ce qui sera appliqué et indique clairement s’il ajoute ou remplace, puis vous demande de confirmer avant sa validation. Après l’application, il indique le nombre total de règles et le nombre de règles ajoutées ou remplacées.

>[!NOTE]
>
>Les modifications utilisent un chemin d’accès prenant en charge les fusions afin qu’une opération d’« ajout » ne remplace jamais silencieusement vos règles existantes.

## Chevauchement d’audiences {#overlap}

Demandez à l’assistant AI de comparer deux listes de personnes (par exemple, _« Afficher le chevauchement entre « Webinaire du 3e trimestre » et « Comptes d’entreprise »_) et il génère une carte _Chevauchement de listes de personnes_ :

* Badge d’en-tête affichant le nombre : **»{N} en commun. »**
* Une ligne de statistiques avec le nombre total de membres de chaque liste et le chevauchement comme **« X % de A · Y % de B »**
* Tableau des membres des personnes des deux listes, avec une colonne **Nom** et une seconde colonne que vous pouvez diriger : **E-mail** (par défaut), **Société** ou **Fonction** en fonction de ce que vous avez demandé.
* Cliquez sur un nom pour ouvrir cette personne dans l’espace de travail.
* S&#39;il n&#39;y a pas de chevauchement, la carte dit très clairement : _« Aucun membre en commun entre ces deux listes »_.

**Limitations :**

| Limite | Détail |
|---|---|
| **Taille du tableau** | Affiche jusqu’à 200 membres ; au-delà, il note _« Affichage de 200 sur N - demandez-moi d’affiner la requête pour limiter les résultats »_ |
| **Calcul de chevauchement** | Calculé sur l’adresse e-mail. Les personnes sans adresse e-mail sont exclues de l’intersection. |
| **Taille de la liste** | Lit jusqu’à environ 1 000 premiers membres de chaque liste. Pour les listes plus volumineuses, l’assistant indique que les résultats sont partiels. |
| **Brouillons de listes dynamiques** | Comparaison impossible : une liste qui n’a pas été publiée ne comporte aucun segment actif. L’assistant vous demande de le publier en premier ou d’utiliser une liste statique à la place. |

## Validation du contrôle qualité {#qa-validation}

Après avoir créé ou mis à jour une liste, l’assistant AI me propose : _« Voulez-vous que je vérifie que la liste est correctement configurée ? »_ Si vous acceptez, il récupère à nouveau la liste et signale les vérifications suivantes :

| Vérifier | Résultat |
|---|---|
| Liste trouvée sous le programme/dossier correct | Réussite/échec |
| Le nombre de filtres correspond à ce qui a été appliqué. | _N_ filtres / incompatibilité |
| Attributs Personalization présents (le cas échéant) | Présent/manquant |
| Le nom de la liste correspond à ce que vous avez demandé | Réussite/échec |
| Nombre estimé de membres | _count_ ou N/A |

## Limites {#limitations}

| Limite | Détail |
|---|---|
| **Adaptation de liste statique depuis[!DNL Marketo Engage]** | Vous ne pouvez pas adapter une liste statique [!DNL Marketo Engage] (ou un e-mail ou une autre ressource qui n’est pas une ressource de filtre) en liste de personnes. Les listes statiques sont des identifiants de membre explicites qui ne peuvent pas être exprimés en tant que filtres ; l’assistant demande plutôt une liste dynamique ou une campagne dynamique. |
| **Filtres basés sur les activités et les appartenances** | Lors de l’adaptation à partir de [!DNL Marketo Engage], des filtres tels que _E-mail ouvert_, _Page web visitée_, _Formulaire rempli_, _Membre de la liste_ et _Membre de la campagne intelligente_ n’ont pas d’équivalent dans la liste de personnes et sont renvoyés comme « Aucun équivalent trouvé ». |
| **Conditions au niveau de l’entreprise** | Traduit dans la mesure du possible dans l’attribut au niveau de la personne le plus proche (les listes de personnes fonctionnent sur les attributs de la personne) et marqué comme étant de faible confiance lorsque l’ajustement est lâche. |
| **Logique AND/OR profondément imbriquée** | Une logique imbriquée complexe peut se réduire en AND/OR de niveau supérieur ; l’assistant le remarque lorsque cela se produit. |
| **Collisions de noms** | Non résolu automatiquement — si le nom est pris, l&#39;assistant vous en demande un autre plutôt que d&#39;ajouter silencieusement un suffixe. |
| **Approbation requise** | L’assistant ne crée ou ne modifie pas de liste tant que vous n’avez pas cliqué sur **[!UICONTROL Continuer]**, confirmé ou donné une autorisation claire (_« approuvé »_, _« semble correct »_ _« créer »_). |
| **Population d’instantanés statiques** | L’appartenance à des listes statiques créées à partir de critères prend plus de quelques minutes, et non instantanément. |
