---
title: Nœud du meilleur chemin suivant
description: Utilisez la prise de décision pilotée par l’IA pour acheminer les personnes le long du chemin de parcours le plus pertinent en fonction des invites de langage naturel, des données comportementales et du contexte de profil en temps réel dans Journey Optimizer B2B edition.
feature: Account Journeys, AI Assistant
role: User
autotag-review: '2026-05-20T18:52:08.227Z'
TQID: 'https://experienceleague.adobe.com/idPaG-ZNnNwJjN8yVC3Ay1FZ2XPgtQgrSMNIus4fReI'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
subfeature_v2: id: ba367494-9862-4596-bd6f-299c7e10a46b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
source-git-commit: 78e4ecfbaf8eab98878f9c92dac6524fc8b30c41
workflow-type: tm+mt
source-wordcount: 1912
ht-degree: 0%

---

# Nœud du meilleur chemin suivant

Le nœud _Meilleur chemin suivant_ apporte la prise de décision de chemin partagé pilotée par l’IA directement dans la zone de travail du parcours. Au lieu de configurer des conditions de filtrage sur un nœud [chemins partagés](./split-merge-paths-nodes.md), vous décrivez votre intention en langage naturel et laissez le système déterminer le chemin le plus pertinent pour chaque personne.

>[!NOTE]
>
>Les nœuds de meilleur chemin suivants sont disponibles uniquement dans les parcours de personne. Ils ne sont pas pris en charge dans les parcours de compte.

Dans l’achat B2B, un profil peut sembler être un type d’acheteur, mais son comportement, ses données micrographiques et son contexte d’engagement révèlent une histoire plus nuancée. Le nœud de meilleur chemin suivant évalue ce contexte pour prendre une décision de routage intelligente, tout en vous permettant de réviser, de modifier ou de remplacer toute recommandation d’IA avant d’activer le parcours.

L’IA évalue chaque personne par rapport aux invites de chemin d’accès définies à l’aide d’une combinaison d’entrées :

* **Historique d’engagement** - Ouvertures d’e-mails, clics sur les liens, visites de pages web et autres signaux comportementaux provenant des parcours actuels et précédents
* **Signaux en temps réel** - Événements à forte intention tels que le remplissage de formulaires et la tarification des visites de pages
* **Attributs de profil** - Données démographiques, intitulé de la fonction, persona et firmographic
* **Attributs du compte** - Données micrographiques et technographiques associées au compte de la personne

Lorsqu’une personne atteint le nœud, le système récupère le contexte du profil, applique des contraintes et utilise un LLM pour sélectionner le chemin le mieux adapté. Chaque décision est consignée avec un score de confiance et un raisonnement en langage naturel pour la transparence et l’observabilité.

Si aucun chemin d’accès n’est une correspondance forte ou si l’invite référence des données non disponibles pour un profil, la personne est acheminée vers le chemin d’accès de secours par défaut.

## Ajouter un nœud de meilleur chemin suivant {#add-next-best-path-node}

1. Ouvrez le parcours de la personne et accédez à la carte du parcours.

1. Cliquez sur l’icône plus ( **+** ) d’un chemin et choisissez **[!UICONTROL Meilleur chemin suivant]**.

   ![Ajouter un nœud de parcours - meilleur chemin suivant](./assets/add-node-next-best-path.png){width="350" zoomable="no"}

   Le nœud est ajouté à la zone de travail et le panneau de configuration du partage de l’IA s’affiche à droite. Elle commence par un chemin et un chemin par défaut _Autres personnes_ pour acheminer les personnes qui ne remplissent les critères d’aucun des chemins définis.

   ![Meilleur nœud de chemin suivant](./assets/node-next-best-path-new.png){width="500"}

## Configuration des chemins d’accès {#configure-paths}

Pour chaque chemin, définissez un nom et une invite en langage naturel qui décrit qui doit y être acheminé. L’invite remplace entièrement l’interface utilisateur des conditions de filtre ; il n’existe aucune condition d’attribut à configurer.

1. Cliquez sur **[!UICONTROL Ajouter un chemin]** pour chaque chemin supplémentaire que vous souhaitez inclure pour le nœud.

   Pour supprimer un chemin d’accès, cliquez sur l’icône _Supprimer_ ( ![Icône Supprimer](../assets/do-not-localize/icon-delete-outline.svg) ) sur la carte de chemin d’accès.

1. Pour chaque carte de chemin d’accès du panneau de droite :

   * Saisissez un **[!UICONTROL Libellé]** qui reflète l’audience ou l’intention de ce segment.

   * Saisissez une **[!UICONTROL Invite]** en langage naturel décrivant qui appartient à ce chemin. Concentrez-vous sur l’intention et le résultat, et non sur des valeurs d’attribut spécifiques.

     <!-- To get prompt ideas, click **[!UICONTROL Suggest prompts]**. The system provides several example prompts tailored to the path context that you can use as-is or adapt. -->

     ![Nœud du meilleur chemin suivant - exemples de chemins](./assets/node-next-best-path-new.png){width="500"}

     **Exemple d’invite de division en trois chemins :**

      * _Chemin 1 - Chefs des RH :_Identifiez les personnes occupant des rôles de leadership dans les RH les plus susceptibles de participer à la gestion des talents et au contenu de l&#39;expérience des employés.
      * _Chemin 2 - Évaluateurs techniques :_identifiez les parties prenantes techniques les plus susceptibles d’interagir avec l’architecture du produit, les intégrations et le contenu de mise en œuvre.
      * _Chemin 3 - Décideurs d’entreprise :_identifiez les parties prenantes les plus susceptibles d’impliquer le retour sur investissement, les résultats commerciaux et le contenu d’études de cas.

1. Si nécessaire, réorganisez les chemins pour définir l’ordre de priorité de la correspondance.

   Le filtrage des chemins d’accès est évalué dans l’ordre décroissant. Chaque personne suit le premier chemin correspondant.

   Cliquez sur les flèches vers le haut et vers le bas en haut à droite de chaque carte de chemin pour la déplacer vers le haut ou le bas dans la liste des chemins.

   ![Nœud du meilleur chemin suivant - Réorganiser les chemins](./assets/node-next-best-path-reorder-paths.png){width="500"}

1. Vérifiez le chemin par défaut (dernier dans la liste des chemins) et modifiez le libellé si nécessaire.

   Le chemin par défaut est utilisé lorsque l’IA ne peut pas affecter en toute confiance une personne à un chemin défini ou lorsque les données pertinentes ne sont pas disponibles. Lorsqu’une invite fait référence à des données qui n’existent pas dans le jeu de données pour un profil donné, le système achemine ce profil vers le chemin d’accès par défaut et signale l’écart de données.

### Commandes dans la boucle humaine {#human-in-the-loop}

Les recommandations de l’IA ne sont pas contraignantes. Avant d’activer le parcours, vous pouvez :

* Modifiez une invite de chemin d’accès pour affiner la logique de routage.
* Ajouter, supprimer ou réorganiser des chemins d’accès.
* Remplacez les suggestions de l’IA par des conditions personnalisées si nécessaire.

Les affectations de chemins pilotés par l’IA ne prennent effet que lorsque vous publiez le parcours.

## Exemples d’invites par cas d’utilisation {#examples}

Les exemples suivants montrent comment écrire des invites de chemin efficaces dans les cas d’utilisation marketing B2B courants. Utilisez-les comme points de départ et adaptez la langue en fonction du contexte du parcours et des données d’audience.

### Signaux de recherche et d&#39;achat actifs {#active-research}

+++Chemin 1 - Chercheurs actifs sur les produits

_Identifier les personnes qui recherchent activement un logiciel de CRM. Recherchez les visites répétées de pages produit, l’engagement avec le contenu de comparaison, les visites renouvelées fréquentes et les signaux d’intention de tiers élevés au cours des 30 derniers jours._

+++

+++Chemin 2 - Comportement de comparaison des prix

_Identifiez les utilisateurs qui ont consulté des pages de tarification ou de comparaison de plans plusieurs fois au cours des 14 derniers jours, en particulier ceux qui alternent entre les pages de tarification et de documentation sur les fonctionnalités._

+++

+++Chemin 3 : intention élevée, aucune conversion

_Identifiez les visiteurs à forte intention qui ont participé aux démonstrations de produit, aux pages de tarification ou à la documentation d’intégration au cours des 21 derniers jours, mais qui n’ont pas envoyé de formulaire ou converti_.

+++

+++Chemin 4 - Comportement de passage en caisse hésitant

_Identifiez les utilisateurs qui ont commencé les flux de réservation de passage en caisse ou de démonstration mais ne les ont pas terminés et qui sont revenus au moins une fois par la suite sans effectuer de conversion._

+++

### Risque de perte et de rétention {#churn-retention}

+++Chemin 1 - Signaux de risque de résiliation

_Identifiez les clients présentant des signes de perte de clientèle en raison de la baisse de l’utilisation des produits, de la réduction de la fréquence de connexion, des pics de tickets d’assistance et de la diminution de l’engagement marketing au cours des 60 derniers jours._

+++

+++Chemin 2 - Désengager les utilisateurs expérimentés

_Identifier les utilisateurs précédemment engagés dont la vitesse d’engagement a considérablement diminué au cours des 30 derniers jours par rapport à leur ligne de base historique._

+++

### Lacunes en matière d&#39;éducation à l&#39;évaluation {#education-evaluation}

+++Chemin 1 - Recherche de la séquence de tarification

_Identifiez les utilisateurs qui ont téléchargé un livre électronique, puis qui ont visité la page de tarification dans les 7 jours, mais qui n’ont pas demandé de démonstration._

+++

+++Parcours 2 - Webinaire sans suivi

_Identifiez les personnes qui ont assisté à un webinaire et qui sont ensuite retournées sur les pages produit, mais qui n’ont jamais réservé de démonstration ou contacté les ventes._

+++

+++Chemin 3 - Évaluation basée sur la comparaison

_Identifiez les visiteurs qui ont consulté un article de comparaison de concurrents, puis qui ont consulté la documentation sur l’intégration ou la migration dans les 14 jours._

+++

### Séquences d’engagement des e-mails {#email-engagement}

+++Chemin 1 - S’ouvre sans clics

_Identifier les prospects qui ont ouvert trois e-mails marketing ou plus dans les 30 jours mais n’ont jamais cliqué sur le site web._

+++

+++Chemin 2 - Clic, mais pas d’engagement plus approfondi

_Identifier les utilisateurs qui ont cliqué d’un e-mail vers une page produit, mais n’ont pas exploré de pages supplémentaires ou ne sont pas revenus dans les 7 jours._

+++

### Modèles d’évaluation et de conversion {#trial-conversion}

+++Chemin 1 - Convertisseurs rapides

_Identifier les clients qui ont effectué une mise à niveau dans les 30 jours suivant le début d’un essai et qui ont montré un engagement élevé du produit au cours de la période d’essai._

+++

+++Chemin 2 - Utilisateurs bloqués pour la version d’essai

_Identifier les utilisateurs de l’évaluation qui se sont connectés au cours de la première semaine mais qui ont présenté une activité minimale par la suite et qui n’ont pas effectué de conversion avant l’expiration de l’évaluation._

+++

### Acheteurs multicanaux {#multi-channel}

+++Chemin 1 - Convergence publicitaire et organique

_Identifiez les utilisateurs qui ont d’abord contacté par le biais d’annonces payantes, puis qui sont revenus par le biais de canaux directs ou organiques dans les 14 jours._

+++

+++Chemin 2 - Évaluation de l’événement en produit

_Identifier les comptes qui ont participé à un événement en personne ou virtuel et qui ont ensuite augmenté le comportement de recherche de produits dans les 30 jours._

+++

+++Parcours 3 - Les chercheurs sur site

_Identifiez les utilisateurs qui ont interagi avec du contenu social et qui ont ensuite visité des pages à forte intention telles que les prix ou les réservations de démonstration._

+++

### Signaux d&#39;achat régionaux {#regional-buying}

+++Chemin 1 - Surtension dans une région spécifique

_Identifier les comptes en Amérique du Nord montrant une activité de recherche de produits accrue et des signaux d’intention de tiers élevés au cours des 30 derniers jours par rapport à leur référence historique._

+++

+++Trajectoire 2 - Dynamique des marchés émergents

_Identifier les comptes dans APAC où la vitesse d’engagement a considérablement augmenté au cours des 14 derniers jours, même si le volume d’engagement global est toujours modéré._

+++

+++Chemin 3 - Intérêt de l’entreprise spécifique à une région

_Identifiez les comptes d’entreprise dans la zone EMEA ayant participé à la mise en conformité, au traitement des données ou à la documentation sur la sécurité au cours des 21 derniers jours._

+++

+++Chemin 4 - Territoire sous-pénétré

_Identifier les comptes les plus performants dans les territoires de vente attribués qui ont montré des signaux d&#39;intention mais que les ventes n&#39;ont pas encore contactés._

+++

### Signaux de synchronisation comportementale {#behavioral-timing}

+++Chemin 1 - Chercheurs en dehors des heures de travail

_Identifier les utilisateurs qui interagissent de manière répétée avec les pages de produits et de prix en dehors des heures de bureau normales dans leur fuseau horaire local._

+++

+++Chemin 2 - Fenêtre de recherche compressée

_Identifiez les comptes présentant une densité d’engagement exceptionnellement élevée dans une courte fenêtre de 72 heures sur plusieurs domaines de produits._

+++

+++Chemin 3 - Pic d’activité de fin de trimestre

_Identifier les comptes avec une forte augmentation de l’activité au stade de l’évaluation au cours des 30 derniers jours du trimestre fiscal._

+++

## Simuler la prise de décision avant la publication {#simulate}

Utilisez la simulation pour tester la manière dont l’IA évalue vos invites par rapport à une audience réelle avant que le parcours ne soit activé. Elle est disponible uniquement lorsque le parcours a le statut _Brouillon_ et n’a aucun effet sur les parcours publiés. Utilisez-la pour valider la logique de routage et créer un degré de confiance dans les recommandations de l’IA.

### Exécuter une simulation {#run-simulation}

1. Sélectionnez le nœud de meilleur chemin suivant et cliquez sur l’icône _Simuler_ ( ![Icône Simuler](../../assets/do-not-localize/icon-simulate-outline.svg) ) en haut du panneau de droite.

   ![Meilleur chemin suivant - cliquez sur l’icône Simuler](./assets/node-next-best-path-simulate-select.png){width="500"}

1. Dans la boîte de dialogue, choisissez l&#39;audience à utiliser pour la simulation :

   * **[!UICONTROL Listes de personnes d’origine]** - Utilisez l’audience à partir du nœud d’audience. Spécifiez une taille d’échantillon lorsque l’audience complète dépasse le seuil de simulation.
   * **[!UICONTROL Listes dynamiques et statiques]** - Utilisez une liste [!DNL Marketo Engage] statique ou dynamique.
   * **[!UICONTROL Enregistrements de test]** - Utilisez des profils de test suggérés par l’IA.

   ![Meilleur chemin suivant - Simuler - choisir l’audience](./assets/node-next-best-path-simulate-dialog.png){width="300"}

   >[!NOTE]
   >
   >Si l’audience sélectionnée dépasse le seuil de simulation, le système exécute la simulation sur un échantillon de 100 profils. Un indicateur dans l’interface utilisateur indique que les résultats sont basés sur des échantillons.
   >
   >Si l&#39;audience sélectionnée n&#39;est pas encore matérialisée, la simulation est bloquée. Un avertissement intégré vous demande de matérialiser d’abord l’audience.

1. Cliquez sur **[!UICONTROL Simuler]**.

### Consulter les résultats de la simulation {#review-simulation-results}

Une fois la simulation exécutée, le panneau de droite affiche la manière dont les profils ont été distribués sur chaque chemin d’accès et le raisonnement de l’IA derrière ces affectations :

| Résultat | Description |
| ------ | ----------- |
| **Profils** | Nombre de profils acheminés vers le chemin d’accès. |
| **Fractionner** | Pourcentage de profils acheminés vers le chemin d’accès. |
| **Confiance** | Niveau de confiance de l’IA pour l’affectation de chemin. Le degré de confiance reflète la fraîcheur des données, l’intensité et la cohérence du signal, ainsi que le succès historique de modèles de routage similaires. |
| **Invite** | Invite évaluée pour le chemin d’accès. |
| **Raisonnement IA** | Explication en langage naturel de l’affectation collective des profils à ce chemin d’accès. |

![Meilleur chemin suivant - Simuler - Résultats pour le chemin](./assets/node-next-best-path-simulate-path-result.png){width="400"}

>[!NOTE]
>
>Lorsque les données disponibles ou la portée limitent une décision, les résultats incluent des informations sur la limitation. Par exemple, lorsqu’un attribut obligatoire n’est pas présent dans le jeu de données, les résultats incluent un indicateur explicite expliquant comment les données manquantes ont affecté les résultats.

Utilisez les résultats pour affiner les invites et confirmer que le routage reflète le résultat prévu. Vous pouvez modifier les invites de chemin et réexécuter la simulation autant de fois que nécessaire avant de la publier.

## Publication et surveillance du parcours {#publish-and-monitor}

Après validation des résultats de la simulation :

1. Connectez l’audience de personnes au nœud d’entrée de parcours.

1. [Publiez le parcours](./create-publish-journey.md#publish-a-journey).

Une fois le parcours actif, le nœud de meilleur chemin suivant s’exécute au moment de l’exécution. Lorsque chaque personne atteint le nœud, l’IA les évalue en temps réel à l’aide des derniers signaux et les achemine vers le chemin le plus pertinent.

Pour un parcours publié, ouvrez la carte des parcours et sélectionnez le nœud de meilleur chemin suivant pour afficher la section **[!UICONTROL Résultats en direct]** dans le panneau de droite. Les résultats en direct affichent :

* Répartition en pourcentage des profils sur chaque chemin d’accès
* Score de confiance pour chaque affectation de chemin
* Raisonnement au niveau du chemin et du profil, avec des détails extensibles pour les profils individuels

Les résultats en direct sont également disponibles dans la console de Parcours et via la compétence [Observabilité du Parcours ](../agents/journey-agent.md#journey-observability-skill) dans le hub d’IA.
