---
title: Chemins de division de variante
description: Découvrez comment utiliser les nœuds de chemin de partage des variantes pour répartir les comptes de manière aléatoire sur plusieurs chemins de parcours à l’aide d’une allocation basée sur un pourcentage dans Journey Optimizer B2B edition.
feature: Account Journeys
solution: Journey Optimizer B2B Edition
role: User
badgeBeta: label="Beta" type="informative" tooltip="Cette fonctionnalité est actuellement en version bêta limitée"
autotag-review: '2026-07-06T23:50:12.985Z'
TQID: 'https://experienceleague.adobe.com/42lSbF7J-yEzFYbFFhs2sSQ4j4NfRtENlIz-R-HcPx8'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
subfeature_v2:
  - id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 11e6c1954e3a99f3da6fc0967038d1c316991d07
workflow-type: tm+mt
source-wordcount: 1439
ht-degree: 2%

---

# Variantes de chemins divisés

Utilisez un nœud _Chemins de division de variante_ pour répartir les comptes de manière aléatoire sur plusieurs chemins de parcours en fonction des allocations en pourcentage que vous définissez. Ce nœud est utile pour les tests exploratoires des différentes tactiques de messagerie, de minutage ou d’engagement sur les segments de l’audience de votre compte, sans appliquer de règles conditionnelles. Il ne convient pas aux expériences A/B contrôlées qui nécessitent une affectation de chemin cohérente par compte.

>[!AVAILABILITY]
>
>Le nœud de chemins de partage des variantes est actuellement disponible pour certains clients sous la forme d’une version bêta limitée, pour les parcours de compte uniquement _&#x200B;**.**&#x200B;_ La prise en charge des parcours de personne est prévue pour une version ultérieure. Pour obtenir l’accès, contactez votre représentant Adobe.

## Comparaison avec les chemins de division {#compare-split-paths}

Les deux _[chemins partagés](./split-merge-paths-nodes.md)_ et _chemins partagés de variante_ divisent les comptes en plusieurs branches de parcours, mais ils utilisent différents mécanismes :

| Aspect | Chemins partagés | Variantes de chemins divisés |
| -------- | ----------- | ------------------- |
| **Logique d’affectation** | _Conditionnel basé sur des règles_ - Chaque compte est évalué par rapport à des conditions définies et continue le premier chemin qu’il correspond. | _Affectation aléatoire basée sur un pourcentage_ - Les comptes sont répartis sur les chemins d’accès en fonction des pourcentages configurés, sans condition de filtrage. |
| **Déterminisme** | _Déterministe_ - Le même compte suit toujours le même chemin tant qu’il correspond aux mêmes conditions. | Non déterministe : le même compte peut suivre différents chemins lors de la rentrée. |
| **Cas d’utilisation** | Segmenter par attributs de compte ou de groupe d’achat connus ; évaluation par ordre de priorité. | Distribuez de manière aléatoire des comptes pour tester les messages, le timing ou les tactiques dans l’audience de votre compte. |
| **Chemin d’accès aux autres comptes** | _Pris en charge_ - Les comptes qui ne correspondent à aucun chemin défini peuvent être acheminés vers un chemin par défaut. | _Sans objet_ — Chaque compte est affecté à l’un des chemins définis. |

## Fractionner par compte {#split-by-account}

Lorsqu’un compte atteint un nœud de chemins de division de variante, le nœud l’affecte à un chemin exactement en fonction des pourcentages configurés. L’affectation utilise un algorithme basé sur les quotas qui permet de suivre le nombre de comptes affectés à chaque chemin d’accès et qui s’ajuste au fil du temps pour maintenir les ratios configurés.

* Chaque compte est affecté à un chemin d’accès exactement.
* L’affectation est aléatoire et basée sur un quota. L’algorithme ajuste les allocations de manière dynamique afin de s’approcher des pourcentages configurés sur l’ensemble de la population.
* Le nœud prend en charge 2 à 20 chemins d’accès. Chaque chemin possède un nom configurable et un pourcentage entier compris entre 1 et 99. La somme de tous les pourcentages de chemin doit être exactement égale à 100 %.

>[!IMPORTANT]
>
>**Algorithme basé sur les quotas : non déterministe**
>
>L&#39;algorithme de répartition utilise l&#39;affectation aléatoire basée sur les quotas. Cet algorithme n’est **_déterministe_** : le même compte peut être affecté à un chemin différent chaque fois qu’il entre ou rentre dans le parcours. L’affectation du chemin d’accès dépend de l’état actuel du quota au moment de l’évaluation, et non d’une propriété de compte fixe. Voir [Limites](#limitations) pour plus d’informations sur les cas d’utilisation concernés.

### Algorithme de répartition {#distribution-algorithm}

Le nœud de chemins de partage des variantes utilise un algorithme d’affectation aléatoire **_basé sur un quota_**. Lorsqu’un compte atteint le nœud , le système évalue les affectations de compte existantes pour chaque chemin d’accès et achemine le compte vers le chemin d’accès le plus éloigné en dessous de son quota configuré. Il existe deux propriétés de clé pour l’algorithme :

* La distribution suit de près les pourcentages configurés pour tous les volumes de compte. Comme l’algorithme maintient activement le nombre de quotas, la répartition réelle ne varie que d’un compte au maximum par chemin en raison de l’arrondi lorsque les totaux ne se divisent pas uniformément.
* L’algorithme utilise un verrou pessimiste lors de l’évaluation du quota pour sérialiser les affectations, ce qui garantit un suivi précis du nombre dans le cadre de l’exécution simultanée.

### Limites {#limitations}

Examinez ces limitations avant d’utiliser des chemins de division de variantes dans vos parcours.

>[!CAUTION]
>
>**L’affectation de chemin d’accès n’est pas déterministe.**
>
>L’algorithme basé sur les quotas ne garantit pas que le même compte suit toujours le même chemin. Si un compte quitte le parcours et y revient, il peut être affecté à un chemin différent en fonction de l’état du quota au moment de la rentrée. N’utilisez pas de chemins de partage de variantes pour les cas d’utilisation qui nécessitent une affectation de chemin cohérente par compte entre les instances de parcours.

| Limite | Description |
| ---------- | ----------- |
| **Ne convient pas aux expériences contrôlées** | Comme l’affectation de chemins n’est pas déterministe, les chemins de division des variantes ne sont **pas adaptés** pour les expériences A/B ou les scénarios d’attribution qui nécessitent un compte donné pour recevoir systématiquement le même traitement. Les cas d’utilisation qui dépendent de la cohérence par compte, comme la mesure des taux de réponse ou l’attribution des résultats à une expérience spécifique, peuvent produire des résultats non fiables. |
| **Dérive d’arrondi mineure** | Lorsque le nombre total de comptes n’est pas divisible de manière égale par les pourcentages configurés, la distribution peut être désactivée par un compte au maximum par chemin d’accès. Ce comportement d’arrondi est attendu et n’est pas une erreur. |
| **L’affectation de chemin n’est pas idempotent** | La rentrée dans le parcours peut générer une affectation de chemin d’accès différente pour le même compte. Si votre conception de parcours suppose qu’un compte suit toujours le même chemin d’accès après le nœud de partage, cette hypothèse ne tient pas. |
| parcours de compte uniquement **&#x200B;**&#x200B;| Les chemins de division des variantes sont pris en charge dans les parcours de compte uniquement. Les parcours de personne ne sont actuellement pas pris en charge. |
| **Aucun filtrage conditionnel** | Contrairement aux _chemins partagés_, les variantes de chemins partagés n’appliquent pas de conditions. Chaque compte qui atteint le nœud est affecté à un chemin d’accès. |

## Fractionner par personnes {#split-by-people}

Dans un parcours de compte, vous pouvez également utiliser une variante de nœud de chemins de partage pour répartir les _personnes au sein des comptes_ de manière aléatoire sur des chemins d’accès en fonction du pourcentage. Ce type de partage est utile lorsque vous souhaitez tester différents contenus ou expériences au niveau de la personne, car les comptes continuent de se déplacer dans le parcours. Le nœud de chemins de division des variantes par personnes fonctionne avec les mécanismes de sécurisation suivants :

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

## Ajouter une variante au nœud de chemins de partage {#add-variant-split-paths-node}

1. Accédez à la carte du parcours.

1. Cliquez sur l’icône plus ( **+** ) sur un chemin d’accès et choisissez **[!UICONTROL Chemins de division des variantes]**.

   ![Ajouter un nœud de parcours - Chemins de partage des variantes](./assets/node-variant-split-paths-add.png){width="300" zoomable="no"}

   Le nœud ajouté dispose de deux chemins d’accès pour commencer.

1. Dans les propriétés de nœud sur la droite, choisissez **[!UICONTROL Comptes]** ou **[!UICONTROL Personnes]** pour la division.

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

### Règles de validation {#validation-rules}

Les règles suivantes s’appliquent à la configuration du chemin de partage des variantes. Les violations bloquent la publication du parcours.

| Règle | Exigence |
| ---- | ----------- |
| Chemins minimaux | 2 |
| Nombre maximal de chemins d’accès | 20 |
| Pourcentage par chemin | Entier de 1 à 99 |
| Pourcentage total | Doit être exactement égal à 100 % |
