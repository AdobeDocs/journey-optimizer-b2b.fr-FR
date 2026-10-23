---
title: Contrôle du trafic parcours
description: Découvrez comment le contrôle du trafic du parcours inscrit chaque personne dans le parcours le mieux adapté lorsqu’elle se qualifie pour plusieurs, et comment ajuster les poids et réviser les décisions.
hide: true
autotag-review: '2026-10-16T18:41:12.165Z'
TQID: 'https://experienceleague.adobe.com/oD1nTkrgqGZ-nzfHNFS66XvjQkn5FmOZ-cI3EDKnb4U'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: 4515ee43-e3ce-55db-9ba1-60b2b42b9d75
    internal-label: Privacy
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
subfeature_v2:
  - id: c3d6e661-d372-4e98-9fd9-eac771e7e4ee
    internal-label: Decisioning
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: d9b663ab-b785-4c49-8fc3-d3dda520c908
    internal-label: Automated decisioning
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 050fcccbef4e84a540d415cfabc65f25310c062f
workflow-type: tm+mt
source-wordcount: '2692'
ht-degree: 0%
---
# contrôle de la circulation des parcours

En [!DNL Adobe Journey Optimizer B2B Edition], les audiences se chevauchent souvent. Un directeur du marketing dans une société de services financiers pourrait être admissible à votre parcours de l&#39;industrie, à votre parcours d&#39;intérêt sur les produits et à votre parcours de compte d&#39;entreprise le même jour. Sans coordination, cette personne est inscrite dans les trois et reçoit des messages concurrents ou redondants. Utilisez le contrôle de trafic de Parcours __ pour inscrire chaque personne dans le parcours une personne qui lui convient le mieux lorsqu’elle remplit les critères de plusieurs parcours à la fois.

Le contrôle de la circulation des parcours examine chaque personne admissible à plus d&#39;un parcours participant. Il compare ce que vous savez sur la personne à chaque objectif de parcours et inscrit la personne qui correspond le mieux. Une personne qui ne remplit les critères que pour un seul parcours est inscrite à ce parcours. Une personne qui remplit les conditions pour aucun n&#39;est pas inscrite.

## Avantages du contrôle de la circulation des parcours {#benefits}

Le contrôle du trafic parcours remplace la gestion manuelle des chevauchements par une décision enregistrée et adaptée à chaque personne.

| Sans contrôle du trafic parcours | Avec contrôle du trafic parcours |
|---|---|
| Une personne qui correspond à plusieurs audiences est inscrite à plusieurs parcours et reçoit des messages qui se chevauchent. | Chaque personne est inscrite à au plus un parcours participant pour chaque évaluation. |
| Les équipes gèrent manuellement le chevauchement avec les segments d’exclusion et les règles d’audience. Ces règles deviennent plus difficiles à gérer à chaque nouveau parcours. | Le système choisit en fonction de l’ajustement. Vous ne créez ni ne conservez de logique d’exclusion. |
| Il est difficile d&#39;expliquer pourquoi une personne a reçu un parcours donné. | Chaque décision est enregistrée et visible, y compris le score de chaque parcours concurrent. |
| La fatigue des messages et les messages mixtes réduisent l’engagement. | Chaque personne bénéficie d’une expérience pertinente et cohérente. |

## Exemples d’utilisation {#examples}

Utilisez le contrôle du trafic de parcours lorsque vos parcours ciblent des audiences qui se chevauchent. Par exemple :

* **Programmes de soutien à l’industrie** : vous gérez des parcours distincts pour les services financiers, les soins de santé et la fabrication. Un contact n’a aucune valeur industrielle, mais son profil est lié au compte d’une banque. Le contrôle du trafic du parcours associe le contact au parcours des services financiers au lieu de les inscrire aux trois.
* **Campagnes d’intérêt pour le produit** : vous exécutez un parcours pour chaque ligne de produit. Un prospect ayant des signes d’intérêt récents pour deux produits est inscrit sur le parcours pour le produit qui suscite le plus d’intérêt.
* **Messages basés sur les rôles** : vous exécutez un parcours pour les évaluateurs techniques et un autre pour les sponsors exécutifs. Fonction et fonction d’une personne déterminant le parcours auquel elle adhère.
* **Programmes Entreprise et PME** : vous exécutez des parcours différents en fonction de la taille de la société. Le segment client et les informations de compte d’un contact décident du parcours qu’ils rejoignent.
* **Nouveaux lancements de parcours** : vous publiez un nouveau parcours dans une audience que d’autres parcours couvrent déjà. Le contrôle du trafic de parcours évalue le chevauchement, de sorte que vous ne reconcevez pas les règles d’audience existantes.

## Sélection par ajustement {#dimensions}

Lorsqu’une personne est admissible pour plusieurs parcours, le contrôle de la circulation des parcours compare le profil de la personne au nom et à la description de chaque parcours candidat. La comparaison couvre quatre dimensions.

| Dimension | Éléments comparés |
|---|---|
| Secteur industriel | L&#39;industrie de la personne. Si le secteur est manquant, le secteur du compte lié. |
| Ajustement fonctionnel | Rôle et fonction de la personne. |
| Taille de l&#39;entreprise | Segment client de la personne, type de compte et contexte de dépenses. |
| Intention | Produit pour lequel la personne a récemment manifesté le plus d’intérêt. |

Gardez à l’esprit les points suivants :

* **Les noms et descriptions de Parcours sont importants.** Ils indiquent au système à quoi sert chaque parcours. Des descriptions spécifiques et précises produisent de meilleures correspondances.
* **Les données manquantes sont ignorées, et non devinées.** Si une personne n’a aucune valeur pour une dimension, le contrôle de trafic parcours exclut cette dimension pour cette personne. Il prend la décision sur les dimensions qui contiennent des données.

L’enregistrement de décision pour chaque personne dans les vues de rapports affiche le score de chaque parcours concurrent et les dimensions utilisées. Une dimension sans données est marquée comme exclue.

### Comparaisons {#comparisons}

Pour chaque dimension, le contrôle du trafic sur les parcours compare le texte approprié de la personne, tel qu’un titre de poste, à la description de chaque parcours. Il utilise deux méthodes :

* **Signification de la similarité** : le texte signifie-t-il quelque chose de proche de la description ?
* **Correspondance de mots-clés** : le texte utilise-t-il les mêmes termes que la description ?

Le résultat le plus fort des deux méthodes devient le score du parcours pour cette dimension.

Chaque dimension propose ensuite son parcours de meilleure notation, mais uniquement si la notation efface un seuil de qualité minimum. Les parcours sans proposition admissible sont abandonnés. Les poids que vous configurez classent les parcours restants en fonction de leurs scores pondérés combinés. Le parcours ayant le score le plus élevé est sélectionné. Le gagnant n&#39;est pas nécessairement le parcours qui a le plus de propositions. Une correspondance forte sur une seule dimension est plus significative que plusieurs correspondances plus faibles.

Chaque enregistrement de décision stocke les informations suivantes :

* Le parcours sélectionné et les parcours concurrents
* Les scores de chaque dimension et le score combiné
* Une valeur de confiance
* Niveau d’accord élevé, Medium ou faible, qui indique le nombre de dimensions prises en charge par le gagnant

<!-- CONFIRM with Engineering: whether to describe the fallback when no dimension produces a qualifying match. The source says the person is still enrolled in one eligible journey, selected consistently, with a 0% (Low) confidence decision record. Also confirm how "consistent" should be phrased. -->

## Configuration {#configuration}

Pour définir les poids des dimensions de contrôle du trafic du parcours et simuler la notation :

1. Dans le volet de navigation de gauche, accédez à **[!UICONTROL Gestion des Parcours]** > **[!UICONTROL Contrôle du trafic des Parcours]**.

1. Sélectionnez l’onglet **[!UICONTROL Configuration]**.

![Onglet Configuration du contrôle du trafic de Parcours avec quatre cartes de poids de dimension, chacune définie sur Medium à 25 %, et le bouton Enregistrer les poids](./assets/journey-traffic-control-configuration.png){width="800" zoomable="yes"}

### Ajuster les poids des dimensions {#weights}

Par défaut, les quatre dimensions ont un poids de __ et contribuent de manière égale, à 25 % chacune. Ajustez les poids pour modifier l’influence de chaque dimension sur les décisions.

1. Pour chaque dimension, définissez le niveau de pondération :

   * **[!UICONTROL Désactivé]**
   * **[!UICONTROL Faible]**
   * ****
   * **[!UICONTROL Élevé]**

   Le pourcentage sur chaque carte indique la part de cette dimension une fois vos paramètres combinés. Pour supprimer une dimension des décisions, définissez-la sur **[!UICONTROL Désactivé]**.

   ![Cartes de poids Dimension avec intention définie sur Élevé à 55 %, Medium de l’industrie à 27 % et Ajustement fonctionnel et Taille de l’entreprise faible à 9 %](./assets/journey-traffic-control-dimensions.png){width="600"}

   Le pourcentage affiché sur chaque carte correspond à la contribution normalisée de cette dimension après la combinaison de toutes vos sélections, atteignant toujours 100 %. Si vous augmentez une dimension, le système re-normalise automatiquement les autres de sorte que le total reste à 100%.

   Vous pouvez cliquer sur **[!UICONTROL Réinitialiser sur égal à]** pour rétablir toutes les dimensions à une pondération égale.

1. Lorsque vous souhaitez appliquer les poids ajustés, sélectionnez **[!UICONTROL Enregistrer les poids]**.

   >[!NOTE]
   >
   >Pour enregistrer les modifications apportées aux poids des dimensions, vous devez disposer de l’autorisation _[!UICONTROL Gérer les configurations d’administration B2B]_ [produit](../admin/user-management.md#b2b-product-permissions).

### Simuler la notation {#simulate-scoring}

Avant de valider le poids en production, vous pouvez simuler le comportement du contrôle du trafic avec ces modifications. La simulation ne nécessite pas l’activation du contrôle du trafic parcours. Il évalue les profils qui se trouvent déjà dans vos parcours actifs et leur applique la logique de contrôle du trafic. Ensuite, vous pouvez juger si les résultats semblent appropriés pour les paramètres de poids.

Cliquez sur **[!UICONTROL Simuler la notation]**.

L’en-tête des résultats résume l’exécution :

* **Profils évalués** — le nombre de profils notés et le nombre de parcours.
* **Nombre moyen de conflits/profil** — Nombre moyen de parcours concurrents par profil.
* **Score moyen de correspondance** — degré de confiance moyen des parcours sélectionnés.

![Simulez les résultats de notation avec 20 profils évalués sur 5 parcours, 1,0 conflit moyen et 70 % de score de correspondance moyen](./assets/journey-traffic-control-simulate-scoring.png){width="700" zoomable="yes"}

Chaque profil évalué s’affiche sous la forme d’une carte indiquant le parcours sélectionné, la justification principale, les signaux d’intention et le score de correspondance. Sélectionnez un profil pour ouvrir une vue détaillée avec :

* **Score de correspondance** — La correspondance globale, avec une répartition par dimension avec code de couleur.
* **Scores par parcours** — parcours pour lesquels cette personne s&#39;est qualifiée, lesquels ont été sélectionnés et pourquoi.
* **Dimensions prises en compte** — Données de dimension qui ont motivé la décision, extensibles pour afficher les signaux sous-jacents.

![Panneau de détails du profil avec un score de correspondance de 77 %, des scores par parcours avec un parcours sélectionné et les dimensions prises en compte](./assets/journey-traffic-control-simulate-scoring-profile-details.png){width="450" zoomable="yes"}

Si nécessaire, ajustez les poids des dimensions et cliquez sur **[!UICONTROL Exécuter à nouveau]** pour relancer la simulation.

Vous pouvez également cliquer sur **[!UICONTROL Échantillonner de nouvelles personnes]** pour relancer la simulation à l&#39;aide d&#39;un nouvel échantillon aléatoire.

Lorsque le résultat vous satisfait, vous pouvez cliquer sur **[!UICONTROL Enregistrer les poids]** pour valider les poids. Les nouvelles décisions de contrôle du trafic utilisent immédiatement les nouveaux paramètres, mais les décisions antérieures ne sont pas affectées. Les poids que vous avez testés apparaissent dans l’onglet principal _[!UICONTROL Configuration]_ et sont utilisés pour toute évaluation du contrôle de trafic parcours dans votre environnement en ligne.

Vous pouvez également quitter la page sans appliquer les poids.

## Vérifier les rapports {#reporting}

Utilisez les vues de rapports pour voir comment le contrôle du trafic du parcours a inscrit des personnes. Examinez les décisions par parcours ou par exécution.

### Rapports par parcours {#reporting-by-journey}

La vue **[!UICONTROL Par Parcours]** résume les parcours soumis au contrôle du trafic.

| Mesure | Description |
|---|---|
| Parcours régis | Parcours qui participent au contrôle de la circulation. |
| Parcours contestés | Parcours qui partagent des personnes avec au moins un autre parcours. |
| Profils contestés | Personnes distinctes revendiquées par plusieurs parcours. |
| Personnes inscrites | Personnes distinctes inscrites. |

Pour chaque parcours, la vue affiche également les valeurs suivantes :

* **[!UICONTROL Inscrits]** : nombre total de personnes inscrites.
* **[!UICONTROL Incontesté]** : personnes qui remplissent les critères pour ce parcours uniquement.
* **[!UICONTROL Gagné]** : personnes qui se sont qualifiées pour plusieurs parcours et qui ont été inscrites à celui-ci.
* **[!UICONTROL Taux de victoire]** : Fréquence à laquelle le parcours a gagné lorsque des personnes se sont affrontées pour l’obtenir.

![Vue de création de rapports par Parcours avec des mesures récapitulatives et un tableau de parcours indiquant les valeurs de taux d’inscription, d’absence de contestation, de confirmation et de confirmation](./assets/journey-traffic-control-reporting-by-journey.png){width="700" zoomable="yes"}

Filtrer la liste par statut de parcours [](./journeys-overview.md#journey-status) : [!UICONTROL En ligne], [!UICONTROL Terminé], [!UICONTROL Abandonné] ou [!UICONTROL Tout].

Pour savoir où en sont les contestataires d&#39;un parcours, ouvrez le parcours. La vue détaillée affiche les parcours auxquels les personnes ont été inscrites à la place. Pour afficher le score de correspondance, les parcours concurrents, le score de chacun et les dimensions utilisées, développez l’enregistrement de décision de toute personne inscrite. Effectuez une recherche par nom, ID de prospect ou ID de profil.

![Vue détaillée du Parcours avec des mesures d’inscription, un graphique de l’endroit où les profils contestés ont atterri et un tableau des personnes inscrites](./assets/journey-traffic-control-reporting-by-journey-detail.png){width="700" zoomable="yes"}

Pour comparer la distribution du secteur ou du produit d’intention sur les parcours, sélectionnez **[!UICONTROL Comparer les parcours]** et choisissez au moins deux et jusqu’à 20 parcours en ligne.

<!-- Figure placeholders: By Journey overview, journey detail "Where contested profiles landed", and a decision record. Redact person names and use clean sample journey names without test prefixes. Choose runs with healthy enrollment counts. -->

### Création de rapports par exécution {#reporting-by-run}

Sélectionnez **[!UICONTROL Par exécution]** pour afficher la liste de chaque exécution d’évaluation avec les informations suivantes :

* Heure de l’exécution
* Comment l’exécution a été déclenchée : *planifiée*, *sur publication* ou *manuelle*
* Le nombre de personnes évaluées, inscrites et non inscrites

![Par Exécuter la vue de rapports avec des filtres de période et de déclenchement et une table des exécutions avec des nombres évalués, inscrits et non inscrits](./assets/journey-traffic-control-reporting-by-run.png){width="700" zoomable="yes"}

Filtrez la liste par période (24 heures, 7 jours, 30 jours ou à toute heure) et type de déclencheur.

Pour afficher un diagramme de flux reliant les personnes évaluées aux parcours auxquels elles étaient inscrites, lancez une exécution. Une répartition pour chaque parcours indique le nombre de personnes **[!UICONTROL non inscrites]**, **[!UICONTROL inscrites]**, **[!UICONTROL arbitrées]** (choisies parmi les parcours concurrents) et **[!UICONTROL non contestées]**. Pour n’importe quel parcours d’une exécution, vous pouvez également afficher les personnes évaluées, leurs résultats, les parcours avec lesquels elles ont été en concurrence et leurs scores de correspondance.

![Diagramme de flux présentant les personnes évaluées et leurs résultats d’inscription dans les parcours ](./assets/journey-traffic-control-reporting-by-run-flow-chart.png){width="500" zoomable="yes"}

<!-- CONFIRM with Product: what the scheduled and on-publish triggers mean for customers, and the content of the Not enrolled tooltip. -->

## Processus d’exécution de l’évaluation {#run-process}

Chaque exécution suit la même séquence. Le contrôle du trafic de parcours lit uniquement les données déjà présentes dans votre environnement [!DNL Journey Optimizer B2B Edition] et ne nécessite pas de sources de données supplémentaires.

1. Le contrôle de trafic de parcours attend que l’actualisation de profil [personne et compte](../data/data-availability-timing.md#daily-refresh) de votre environnement se termine correctement. Si l’actualisation échoue, aucune exécution ne démarre sur les données obsolètes.

1. L’appartenance à une audience est calculée en [!DNL Adobe Experience Platform] et [ synchronisée ](../data/data-availability-timing.md#platform-sync) en [!DNL Journey Optimizer B2B Edition]. Une fois la segmentation terminée, le système attend la fin de la synchronisation, pendant 30 minutes au maximum. Si la synchronisation se termine plus tôt, le traitement commence immédiatement. Si 30 minutes se sont écoulées en premier, le traitement commence quand même. Si la synchronisation se termine plus tard, une nouvelle exécution commence sur les données mises à jour.

1. Le système assemble les parcours candidats. Seuls les parcours actifs et activés pour le contrôle du trafic y participent. Le système lit le statut, le nom et la description de chaque parcours.

1. Le système lit le contexte d’appartenance à l’audience et de profil par petits lots.

1. Le système vérifie l’éligibilité. Une personne n’est éligible à un parcours que lorsque tous les éléments suivants sont vrais :

   * Le parcours est actif et activé pour le contrôle du trafic.
   * La personne est actuellement membre de l’audience du parcours.
   * La personne n’a pas encore été inscrite à ce parcours.
   * La personne n’est actuellement pas inscrite à ce parcours.

1. Le système sélectionne un parcours. Une personne disposant d’un parcours éligible y est inscrite. Une personne sans parcours éligible n’est pas inscrite. Pour une personne ayant plusieurs parcours éligibles, le système compare le profil de la personne au nom et à la description de chaque parcours dans les [quatre dimensions](#dimensions).

1. Le système envoie l’inscription au parcours sélectionné par le biais du mécanisme d’inscription de parcours standard.

1. Le système enregistre chaque décision et chaque résultat d’inscription pour le compte rendu des performances et l’audit.

1. Le système effectue des points de contrôle au fur et à mesure que les lots se terminent, enregistre le résultat et envoie une notification d’achèvement.

## Données utilisées et stockées {#data}

Le contrôle du trafic de parcours utilise les données suivantes de votre environnement.

| Données | Source | Utilisation |
|---|---|---|
| Statut, nom et description du parcours | Vos parcours | Déterminez les parcours qui participent et l’objectif de chaque parcours. |
| Appartenance à une audience | [!DNL Experience Platform] des audiences synchronisées dans [!DNL Journey Optimizer B2B Edition] | Identifier les personnes qualifiées pour chaque parcours. |
| Profil de personne, tel que le secteur d’activité, la fonction et le segment client | Vos données de personne | Fournissez des dimensions relatives au secteur, à l’adéquation fonctionnelle et à la taille de l’entreprise. |
| Profil de compte lié, tel que le secteur et le type de compte | Les données de votre compte | Renseignez le secteur lorsque la propre valeur de la personne est manquante et fournissez le contexte du compte. |
| Intérêt du produit | Vos [données d’intention](../admin/intent-data.md) | Fournissez la dimension d’intention. Le produit qui présente l’intérêt le plus fort et le plus récent est utilisé. |
| Enrollment history | Enregistrements écrits par les exécutions précédentes | Évitez d’inscrire à plusieurs reprises la même personne dans le même parcours. |
| Statut d’inscription actuel | [!DNL Journey Optimizer B2B Edition] | Évitez d’inscrire une personne qui se trouve déjà dans le parcours. |

Pour chaque exécution, le contrôle du trafic du parcours stocke un résumé d’exécution. Pour chaque personne inscrite, il stocke un enregistrement de décision d’inscription. Les deux sont stockés dans les entrepôts de données gérés par Adobe de votre environnement. Ils alimentent les rapports et empêchent les inscriptions répétées.

<!-- 
CONFIRM with Engineering, Security, and Legal before publishing. The source material does not state any of the following data handling commitments:
- Where processing occurs and data residency.
- Whether meaning similarity comparison uses a third-party or externally hosted AI service, and whether profile text leaves the Adobe environment.
- Whether customer data is used to train models shared with other customers.
- The retention period for decision and enrollment records, and how they are deleted when a person is erased (link to privacy requests).
- Encryption in transit and at rest, role-based access to the reports, and tenant isolation. 
-->

## Configurer le contrôle du trafic parcours {#setup}

Vous pouvez activer le contrôle du trafic de parcours directement sur un parcours individuel [personne](./create-publish-journey.md) lorsqu’il a le statut _Brouillon_.

1. Assurez-vous que le parcours de personne possède un nom et une description qui fournissent un objectif et un but clairs pour le parcours.

   Ces noms et descriptions constituent la base de la correspondance.

1. Cliquez sur **[!UICONTROL ... Plus]** en haut à droite de la zone de travail du parcours et choisissez **[!UICONTROL Paramètres de contrôle du trafic du Parcours]**.

   ![Le menu Plus de brouillon de parcours de personne s’ouvre, répertoriant les paramètres Dupliquer, Supprimer, Parcours des paramètres de contrôle de la circulation et Rentrée](./assets/person-journey-draft-more-menu.png){width="400"}

1. Dans la boîte de dialogue, activez l’option **[!UICONTROL Activer le contrôle du trafic de parcours]**.

   La boîte de dialogue des paramètres explique le comportement : lorsqu’elle est activée, le parcours devient candidat et il évalue et recommande le parcours le plus adapté pour une personne éligible à plusieurs parcours actifs.

   ![Boîte de dialogue des paramètres de contrôle du trafic Parcours avec le bouton (bascule) Activer le contrôle du trafic parcours activé, ainsi que les boutons Annuler et Enregistrer](./assets/journey-traffic-control-enable-dialog.png){width="450"}

   >[!IMPORTANT]
   >
   >Le bouton (bascule) peut être modifié à tout moment tant que le parcours conserve le statut _Brouillon_. Une fois que vous avez publié le parcours avec le contrôle de trafic de parcours activé, il évalue l’entrée dans ce parcours et vous ne pouvez plus désactiver le paramètre.

1. Cliquez sur **[!UICONTROL Enregistrer]**

1. [Publier](./create-publish-journey.md#publish-a-journey) le parcours de la personne.

## Limites et dépendances {#limitations}

Les dépendances suivantes affectent le moment et le fonctionnement du contrôle du trafic de parcours :

* **Synchronisation des audiences** : les décisions reposent sur une adhésion à l’audience à jour synchronisée de [!DNL Experience Platform] à [!DNL Journey Optimizer B2B Edition]. Le minutage d’exécution suit la segmentation et la fin de la synchronisation. Il ne s&#39;agit pas d&#39;un calendrier fixe.
* **Actualisation du profil** : une exécution ne commence qu’une fois l’actualisation du profil de la personne et du compte réussie.
* **Métadonnées de Parcours** : seuls les parcours en direct activés pour le contrôle du trafic participent. La qualité de la correspondance dépend des noms et descriptions que vous écrivez.
* **Exhaustivité du profil** : la qualité dépend des données relatives à la personne, au compte et à l’intention que vous conservez. Les dimensions manquantes sont ignorées.

Le contrôle du trafic parcours présente les limitations suivantes :

* **Un parcours pour chaque personne** : une personne est inscrite à au plus un parcours pour chaque exécution.
* **La sélection ne garantit pas l’inscription** : jusqu’à la fin de la synchronisation depuis [!DNL Experience Platform], certains profils peuvent être évalués sans ID de personne Marketo correspondant. Le parcours est sélectionné, mais l’inscription risque de ne pas réussir. Ces personnes apparaissent comme *Non inscrites* dans les rapports d’exécution.
* **Pas d’inscription répétée** : le contrôle du trafic du Parcours n’inscrit pas une personne dans un parcours auquel elle était précédemment inscrite. Pour permettre aux personnes de se requalifier pour un parcours, utilisez les paramètres de rentrée de [parcours ](./journey-re-entry.md).
* **Pas en temps réel** : les décisions sont prises lorsqu’une exécution se produit, et non lorsqu’un profil change.
* **Quatre dimensions fixes** : vous pouvez ajuster l’importance du secteur, l’adéquation fonctionnelle, la taille de l’entreprise et l’intention, mais vous ne pouvez pas ajouter de dimensions.
* **Correspondance textuelle** : les noms et descriptions de Parcours sont comparés au texte du profil. Les parcours dont la description est vague, vide ou similaire sont plus difficiles à distinguer. Des parcours faiblement différenciés peuvent produire des résultats de confiance faibles.

Le contrôle du trafic de parcours décide uniquement du parcours éligible dans lequel une personne est inscrite. Elle ne modifie pas vos parcours ni vos audiences.

<!-- CONFIRM with Product and Engineering: the maximum number of governed journeys, maximum audience size for each run, supported editions and regions, and any language limitations for text matching. -->
