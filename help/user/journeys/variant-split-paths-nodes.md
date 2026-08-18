---
title: Chemins de division de variante
description: Découvrez comment utiliser les nœuds de chemin de partage des variantes pour distribuer des comptes ou des personnes sur plusieurs chemins de parcours à l’aide d’une allocation basée sur un pourcentage dans Journey Optimizer B2B edition.
feature: Account Journeys, Person Journeys
solution: Journey Optimizer B2B Edition
role: User
badgeBeta: label="Beta" type="informative" tooltip="Cette fonctionnalité est actuellement en version Beta limitée."
autotag-review: '2026-08-17T19:14:54.674Z'
TQID: 'https://experienceleague.adobe.com/42lSbF7J-yEzFYbFFhs2sSQ4j4NfRtENlIz-R-HcPx8'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
subfeature_v2:
  - id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
  - id: ba367494-9862-4596-bd6f-299c7e10a46b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
source-git-commit: b9abc88d05d5863ad57a19118fb905c394dbc76e
workflow-type: tm+mt
source-wordcount: 2018
ht-degree: 2%

---

# Variantes de chemins divisés

Utilisez un nœud _Chemins de division de variante_ pour répartir les comptes ou les personnes sur plusieurs chemins de parcours en fonction des allocations en pourcentage que vous définissez. Ce nœud est utile lorsque vous souhaitez tester différentes tactiques de messagerie, de minutage ou d’engagement sur des segments de votre audience sans appliquer de règles conditionnelles.

>[!AVAILABILITY]
>
>Le nœud _Chemins de partage des variantes_ pour les parcours de compte et de personne est disponible pour sélectionner les clients et clientes en tant que fonctionnalité à disponibilité limitée. Pour obtenir l’accès, contactez votre représentant Adobe.

## Comparaison par type de parcours {#journey-type-comparison}

Le nœud de chemins de division des variantes utilise différents algorithmes d’affectation en fonction du type de parcours. Il est important de comprendre cette différence pour choisir le cas d’utilisation approprié pour chaque type de parcours.

| | Parcours de compte | Parcours de personne |
| - | ---------------- | --------------- |
| **Algorithme** | Attribution aléatoire basée sur un quota | Affectation de hachage déterministe |
| **Déterminisme** | Non déterministe — Le même compte peut être affecté à un chemin différent lors de la rentrée, selon l&#39;état actuel du quota. | Déterministe : la même personne est toujours affectée au même chemin pour un parcours publié donné, quel que soit le nombre de fois où elle entre ou entre à nouveau. |
| **Tests AB** | Non approprié — l’affectation de chemin n’est pas stable entre les nouvelles entrées. | Approprié : l’affectation cohérente de chemins par personne prend en charge les expériences contrôlées et l’attribution. |
| **Comportement de rentrée** | Le compte peut suivre un chemin différent chaque fois qu’il entre dans le parcours. | La personne suit toujours le même chemin d’accès qui lui a été attribué lors de sa première entrée. |
| **Précision de la répartition** | Dans un compte par chemin en raison de l’application des quotas. | Converge vers dans les ±2 % des pourcentages configurés à 1 000 entrées de parcours ou plus. |

## Comparaison avec les chemins de division {#compare-split-paths}

Les deux _[chemins fractionnés](./split-merge-paths-nodes.md)_ et _chemins fractionnés par les variantes_ divisent un parcours en plusieurs branches (chemins), mais ils utilisent différents mécanismes :

| Aspect | Chemins partagés | Variantes de chemins divisés |
| -------- | ----------- | ------------------- |
| **Logique d’affectation** | _Conditionnel basé sur des règles_ — Chaque entité est évaluée par rapport à des conditions définies et continue sur le premier chemin correspondant. | _Affectation basée sur un pourcentage_ — Les entités sont réparties sur les chemins d’accès en fonction des pourcentages configurés, sans condition de filtrage. |
| **Déterminisme** | _Déterministe_ — La même entité suit toujours le même chemin tant qu&#39;elle correspond aux mêmes conditions. | _Dépend du type de parcours_ - Les parcours de personne sont déterministes (la même personne suit toujours le même chemin pour un parcours publié). Les parcours de compte ne sont pas déterministes (basés sur des quotas). |
| **Chemin d’accès d’autres comptes/personnes** | _Pris en charge_ — Les entités qui ne correspondent à aucun chemin défini peuvent être acheminées vers un chemin par défaut. | _Non applicable_ — Chaque entité qui atteint le nœud est affectée à un chemin d’accès. |
| **Cas d’utilisation** | Segmenter par attributs de compte ou de personne connus ; évaluer par ordre de priorité. | Distribuez des entités pour tester la messagerie, le timing ou les tactiques. Parcours de personne : adapté aux expériences A/B. Parcours de compte : adapté à une répartition aléatoire sans cohérence par compte. |

## Parcours de compte {#account-journeys}

Pour les parcours de compte, l’algorithme de répartition utilise l’[affectation aléatoire basée sur un quota](#account-journeys--quota-based-random-assignment). Cet algorithme n’est **_déterministe_** : le même compte peut être affecté à un chemin différent chaque fois qu’il entre ou rentre dans le parcours. L’affectation du chemin d’accès dépend de l’état actuel du quota au moment de l’évaluation, et non d’une propriété de compte fixe.

### Fractionner par compte {#split-by-account}

Lorsqu’un compte atteint un nœud de chemins de partage de variante, le runtime évalue le nombre de comptes déjà affectés à chaque chemin d’accès au cours de l’instance de parcours active et achemine le compte vers le chemin d’accès le plus en dessous de son quota configuré.

* Chaque compte est affecté à un chemin d’accès exactement.
* L&#39;affectation est basée sur un quota. L’algorithme ajuste les allocations de manière dynamique afin de s’approcher des pourcentages configurés sur l’ensemble de la population.
* Comme l’algorithme effectue le suivi des nombres de quotas, la répartition réelle ne dérive que d’un compte au maximum par chemin en raison de l’arrondi lorsque les totaux ne se divisent pas uniformément.

### Fractionner par personnes {#split-by-people}

Dans un parcours de compte, vous pouvez également utiliser une variante de nœud de chemins de partage pour répartir les _personnes au sein des comptes_ de manière aléatoire sur des chemins d’accès en fonction du pourcentage. Ce type de partage est utile lorsque vous souhaitez tester différents contenus ou expériences au niveau de la personne. Les comptes continuent de se déplacer dans le parcours. Le nœud de chemins de division des variantes par personnes fonctionne avec les mécanismes de sécurisation suivants :

* Le nœud fonctionne comme un _nœud groupé_, qui est une combinaison de fusion et de partage. Les chemins de division se ferment automatiquement au niveau d’un nœud de fusion correspondant afin que tous les utilisateurs puissent avancer sans perdre le contexte de leur compte.
* Chaque personne du compte est affectée à un chemin d’accès exact en fonction des pourcentages configurés.
* Le même algorithme basé sur les quotas que celui utilisé pour les comptes s’applique aux personnes. L’affectation de chemin n’est pas déterministe et la même personne peut suivre un chemin différent lors de la rentrée.
* Seuls les nœuds _[!UICONTROL Agir]_ pour les personnes sont pris en charge dans les chemins d’accès. Les chemins ne peuvent pas être divisés davantage.

>[!BEGINSHADEBOX « Comportement de distribution parmi les personnes »]

Les personnes d’un compte sont traitées par lots. Le nombre affecté à chaque chemin est calculé comme `floor(percentage / 100 × people_in_account)`, et le **dernier chemin configuré reçoit toutes les personnes restantes**. Autrement dit :

* Lorsqu’un compte comporte un nombre impair de personnes, le dernier chemin reçoit une personne de plus que les chemins précédents.
* Pour les comptes comportant une seule personne, cette personne est toujours affectée au premier chemin, quels que soient les pourcentages configurés.
* Pour les comptes comportant très peu de personnes (moins de 10), la distribution par compte peut différer sensiblement des pourcentages configurés. La distribution converge vers les ratios configurés lorsqu’ils sont mesurés sur de nombreux comptes.

>[!NOTE]
>
>Ce comportement d’arrondi s’applique par lot de comptes, et non à tous les comptes du parcours. Le dernier chemin d’accès reçoit systématiquement un peu plus de personnes que configuré lorsque les tailles de compte sont impaires. C’est un comportement normal.

>[!ENDSHADEBOX]

## Parcours de personne {#person-journeys}

Lorsqu’une personne atteint un nœud de chemins partagés de variante, le runtime la mappe à un chemin d’accès en fonction d’un hachage de son identifiant et de l’identifiant de parcours.

* Chaque personne est affectée à un chemin d’accès exactement.
* L’affectation est déterministe : une même personne reçoit toujours la même affectation de chemin d’accès pour un parcours publié donné, quel que soit le nombre de fois où elle entre ou entre à nouveau.
* Le hachage est calculé à partir de l’ID de personne et de l’ID de parcours uniquement. Elle ne dépend pas de la position du nœud, de l’heure d’entrée ou de tout état de quota. Cela signifie que la rentrée dans le parcours produit à chaque fois la même affectation de chemin d’accès.

>[!NOTE]
>
>**La division des variantes de parcours de personne est appropriée pour les tests A/B et les expériences.**
>
>L’affectation étant déterministe et cohérente entre les nouvelles entrées, les chemins de division de variantes dans les parcours de personne prennent en charge les expériences contrôlées où la même personne doit systématiquement recevoir la même expérience. Utilisez la vue [Détails du parcours &#x200B;](./journey-details.md) pour surveiller la distribution entre les chemins d’accès une fois le parcours actif.

## Algorithme de répartition

L’algorithme de répartition appliqué dépend du type de parcours.

### Parcours de compte — affectation aléatoire basée sur un quota

Le nœud de chemins de partage des variantes dans les parcours de compte utilise un algorithme d’affectation aléatoire **basé sur un quota**. Lorsqu’un compte atteint le nœud , le runtime évalue le nombre de comptes déjà affectés à chaque chemin d’accès au cours de l’instance de parcours active et achemine le compte vers le chemin d’accès le plus en dessous de son quota configuré.

**Propriété de clé de l’algorithme basé sur les quotas :**

* La distribution suit de près les pourcentages configurés pour tous les volumes de compte. Comme l&#39;algorithme maintient activement le nombre de quotas, la distribution réelle ne dérive que d&#39;un compte au maximum par chemin en raison de l&#39;arrondi lorsque les totaux ne se divisent pas uniformément.

### Parcours de personne — affectation de hachage déterministe

Le nœud de chemins de division de variante dans les parcours de personne utilise un algorithme **affectation de hachage déterministe**. Lorsqu’une personne atteint le nœud , l’exécution calcule une valeur de hachage à partir de l’ID de personne et de l’ID de parcours, puis mappe le résultat à un chemin d’accès en fonction des plages de pourcentage configurées. L’algorithme est appliqué à l’aide du workflow suivant :

1. Le runtime calcule un hachage MurmurHash3 32 bits à partir d’une clé composite qui combine l’ID de personne et l’ID de parcours.
1. La valeur de hachage est mappée à une position dans une plage de 10 000 compartiments de taille égale.
1. Les compartiments sont partitionnés en fonction des pourcentages de chemin configurés. Par exemple, avec des chemins de 30 %, 30 % et 40 %, les 3 000 premiers compartiments correspondent au chemin 1, les 3 000 suivants au chemin 2 et les 4 000 restants au chemin 3.
1. La personne est affectée au chemin d’accès dont la plage de compartiment contient sa position de hachage.

L’algorithme de hachage déterministe possède deux propriétés clés :

* **_Cohérence_** — La même personne est toujours affectée au même compartiment pour un ID de parcours donné. La rentrée dans le parcours produit la même affectation de chemin d’accès à chaque fois.
* **_Répartition statistique_** — La répartition converge vers ±2 % des pourcentages configurés lorsqu’au moins 1 000 personnes uniques sont entrées sur le parcours. Avec des audiences plus petites, le nombre par chemin peut différer plus sensiblement des ratios configurés.

## Limites {#limitations}

Examinez ces limitations avant d’utiliser des chemins de division de variantes dans vos parcours.

### Limites du parcours de compte {#account-journey-limitations}

>[!IMPORTANT]
>
>**L’affectation de chemin d’accès n’est pas déterministe.**
>
>L’algorithme basé sur les quotas ne garantit pas que le même compte suit toujours le même chemin. Si un compte quitte le parcours et y revient, il peut être affecté à un chemin différent en fonction de l’état du quota au moment de la rentrée. N’utilisez pas de chemins de partage de variantes de parcours de compte pour les cas d’utilisation qui nécessitent une affectation de chemin cohérente par compte entre les instances de parcours.

| Limite | Description |
| ---------- | ----------- |
| **Ne convient pas aux expériences contrôlées** | Comme l’affectation de chemins d’accès n’est pas déterministe, les chemins d’accès partagés de variantes dans les parcours de compte ne sont **pas adaptés** pour les expériences A/B ou les scénarios d’attribution qui nécessitent qu’un compte donné reçoive systématiquement le même traitement. |
| **Dérive d’arrondi mineure** | Lorsque le nombre total de comptes n’est pas divisible de manière égale par les pourcentages configurés, la distribution peut être désactivée par un compte au maximum par chemin d’accès. Ce comportement d’arrondi est attendu et n’est pas une erreur. |
| **L’affectation de chemin n’est pas idempotent** | La rentrée dans le parcours peut générer une affectation de chemin d’accès différente pour le même compte. |
| **Aucun filtrage conditionnel** | Contrairement aux _chemins partagés_, les variantes de chemins partagés n’appliquent pas de conditions. Chaque compte qui atteint le nœud est affecté à un chemin d’accès. |

### Limites du parcours de personnes {#person-journey-limitations}

| Limite | Description |
| ---------- | ----------- |
| **Variance statistique à petite échelle** | La répartition converge vers les pourcentages configurés à environ ±2 % lorsqu’au moins 1 000 personnes uniques sont entrées sur le parcours. Avec moins d’entrées, le nombre par chemin peut différer plus sensiblement des ratios configurés. Il s’agit d’un comportement attendu de la distribution de hachage et il ne s’agit pas d’une erreur. |
| **Aucun filtrage conditionnel** | Contrairement aux _chemins partagés_, les variantes de chemins partagés n’appliquent pas de conditions. Chaque personne qui atteint le nœud est affectée à un chemin d’accès. |

## Ajouter une variante au nœud de chemins de partage {#add-variant-split-paths-node}

Les étapes d’ajout et de configuration d’un nœud de chemin de partage de variante sont identiques pour les parcours de compte et de personne.

1. Accédez à la carte du parcours.

1. Cliquez sur l’icône _Ajouter_ ( **+** ) sur un chemin d’accès et choisissez **[!UICONTROL Chemins de division des variantes]**.

   ![Ajouter un nœud de parcours - Chemins de partage des variantes](./assets/node-variant-split-paths-add.png){width="300" zoomable="no"}

   Sur la carte par parcours, le nœud comporte deux chemins par défaut.

1. (parcours de compte uniquement _) Dans les propriétés de nœud sur la droite, choisissez **[!UICONTROL Comptes]**&#x200B;ou **[!UICONTROL Personnes]**&#x200B;pour la division._

   Si vous utilisez le type _[!UICONTROL Personnes]_, un nœud _Fermer les chemins de division des variantes_ est automatiquement inséré pour fermer la division regroupée.

   ![Zone de travail de Parcours - variante fractionnée par les personnes avec le nœud de fermeture inséré automatiquement](./assets/node-variant-split-paths-people-canvas.png){width="700" zoomable="yes"}

1. Vérifiez ou mettez à jour le **[!UICONTROL Libellé]** pour chaque chemin d’accès.

   Les libellés de chemin apparaissent comme des libellés de périphérie sur la zone de travail de parcours et permettent de distinguer les chemins dans l’analyse de parcours.

   ![Nœud de chemins de division des variantes - Configuration du nom du chemin](./assets/node-variant-split-paths-names.png){width="600" zoomable="yes"}

1. Définissez le **[!UICONTROL Pourcentage]** pour chaque chemin d’accès.

   Les valeurs doivent être des entiers compris entre 1 et 99.

   ![Nœud de chemins de division des variantes - Configuration du pourcentage de chemin](./assets/node-variant-split-paths-config.png){width="500" zoomable="yes"}

   L’indicateur Total en cours affiche la somme de tous les pourcentages de chemin. Le total doit être exactement égal à 100 % avant que vous puissiez publier le parcours. Un état d’erreur s’affiche lorsque le total n’est pas égal à 100 %.

   ![Nœud de chemins de division des variantes - erreur de validation lorsque le total n’est pas égal à 100 %](./assets/node-variant-split-paths-validation-error.png){width="500" zoomable="yes"}

   Pour répartir les pourcentages de manière égale sur tous les chemins, cliquez sur **[!UICONTROL Répartir proportionnellement]**. Le système calcule les parts égales et ajuste les arrondissements pour garantir que le total est égal à 100 %.

1. Pour définir des chemins supplémentaires, cliquez sur **[!UICONTROL Ajouter un chemin]** pour chacun d’eux.

   Le nœud prend en charge jusqu’à 20 chemins. À mesure que vous ajoutez d’autres chemins d’accès, ajustez le _[!UICONTROL Pourcentage]_ de sorte que le total soit égal à 100 %.

   Vous pouvez supprimer un chemin d’accès en cliquant sur l’icône _Supprimer_ ( ![Icône Supprimer](../assets/do-not-localize/icon-delete-outline.svg) ) dans la carte de chemin d’accès. Un chemin ne peut être supprimé que s’il en reste au moins deux.

   Les règles suivantes s’appliquent à la configuration du chemin de partage des variantes. Les violations bloquent la publication du parcours.

   | Règle | Exigence |
   | ---- | ----------- |
   | Chemins minimaux | 2 |
   | Nombre maximal de chemins d’accès | 20 |
   | Pourcentage par chemin | Entier de 1 à 99 |
   | Pourcentage total | Doit être exactement égal à 100 % |
