---
title: Nœuds d’audience de personne
description: Configurez les nœuds d’audience de personne avec des audiences basées sur des segments ou des événements afin de définir des points d’entrée de parcours de personne pour l’orchestration ciblée dans Journey Optimizer B2B edition.
feature: Audiences
role: User
badgeBeta: label="Beta" type="informative" tooltip="Cette fonctionnalité est actuellement en version bêta limitée"
source-git-commit: f5170767a6df14874fab5de203264a5a5e3e245a
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 0%

---

# Nœuds du parcours d’audience de la personne

Le nœud _audience personne_ spécifie les profils de personnes qui rejoignent le parcours. Lorsque vous [créez un parcours de personne](./create-publish-journey.md#create-a-journey), le parcours commence toujours par un nœud d’audience de personne qui définit son entrée. Le nœud d’audience de personne peut avoir l’un des deux types d’entrée d’audience suivants : segments CDP ou abonnement basé sur un événement. Les définitions d’audience basées sur un segment et un événement ne peuvent pas être combinées.

Utilisez l’une des options d’entrée suivantes pour le nœud de parcours d’audience de personne :

* **Audience du profil** - Utilisez des audiences de segment définies dans une plateforme CDP. Tous les profils qui remplissent les critères de l’audience sont ajoutés en tant que membres au parcours. Les profils nouvellement qualifiés pour le segment sont ajoutés au parcours au cours des tâches quotidiennes [ingestion de profils](#profile-ingestion). Si un profil n’est plus qualifié pour le segment, il n’est **_pas_** supprimé du parcours.

* **Audience de l’événement** - Utilisez les événements admissibles pour définir l’audience. Ces événements sont définis dans la configuration du nœud et doivent utiliser les événements [XDM configurés dans les paramètres d’administration](../admin/configure-aep-events.md). Jusqu’à 10 événements sont pris en charge pour l’adhésion d’audience basée sur un événement. Un profil est immédiatement éligible pour le parcours après le premier événement correspondant qu’il prend.

  >[!NOTE]
  >
  >Les événements ne peuvent pas être combinés avec des attributs de profil pour réduire les définitions d’audience. Des améliorations visant à résoudre cette limitation sont prévues pour les prochaines versions.

## Ingestion de profil

Dans Journey Optimizer B2B edition, une tâche d’ingestion d’audience chaque nuit synchronise les profils avec Experience Platform. Bien que les parcours de personne basés sur un événement puissent qualifier des profils qui ne font pas partie d’une audience de profil ou de compte ingérée/utilisée par Journey Optimizer B2B edition, les profils ingérés restent obsolètes, sauf s’ils font partie d’une audience utilisée par un parcours de personne, un parcours de compte ou un groupe d’achat. Si un profil est ingéré et ajouté ultérieurement à une audience, la combinaison de profils est effectuée et le profil reste synchronisé avec Experience Platform. Des améliorations de cette synchronisation des données de profil sont prévues pour les prochaines versions.

Un profil nouvellement créé ingéré par un parcours de personne basé sur un événement peut ne pas disposer des informations de profil mises à jour au moment de l’ingestion. Par exemple, si un profil est créé par le biais d’un événement de remplissage de formulaire et qu’une personne parcours les ingère à partir de l’événement de remplissage de formulaire éligible, les données envoyées dans le formulaire peuvent ne pas encore être synchronisées avec le profil lorsque le parcours les a ingérées. Il peut en résulter des données incomplètes à personnaliser (comme dans le contenu des e-mails). Des améliorations de cette synchronisation des données d’événement de profil sont prévues pour les prochaines versions.

Les parcours de personne basés sur un événement peuvent qualifier des profils qui sont toujours anonymes/sans adresses e-mail et qui contiennent uniquement des ECID. Cela se produit le plus souvent lorsque vous disposez d’une logique de qualification pour l’activité de page web. Une logique d’audience basée sur un événement trop large peut entraîner l’atteinte de la limite de 40 millions de profils de l’instance si trop de profils sont qualifiés. Limitez la portée possible de votre audience pour empêcher ce scénario.

>[!IMPORTANT]
>
>Au cours du programme bêta actuel, l’utilisation idéale des parcours de personne consiste à qualifier uniquement les profils que vous ciblez également dans les parcours de compte et les définitions de groupes d’achats. Cette utilisation garantit un profil complet qui reste synchronisé avec Experience Platform.

## Définissez l’audience pour le nœud audience de la personne .

1. Cliquez sur le nœud **[!UICONTROL Audience de la personne]**.

   Cette action affiche les propriétés du nœud sur la droite.

   ![Nœud de parcours d’audience de personne](./assets/person-journey-person-audience-node.png){width="700" zoomable="yes"}

1. Choisissez le type de saisie pour les personnes qui entrent dans le parcours :

   * **[!UICONTROL Audience du profil]**

     Choisissez l’option _[!UICONTROL Audience du profil]_. Cliquez ensuite sur **[!UICONTROL Ajouter une audience de profil]**.

     Dans la boîte de dialogue _[!UICONTROL Ajouter une audience]_, sélectionnez un segment d’audience créé précédemment. Cliquez ensuite sur **[!UICONTROL Ajouter une audience]**.

     ![Sélectionnez une audience de profil pour le nœud](./assets/node-person-audience-add-audience-dialog.png){width="700" zoomable="yes"}

   * **[!UICONTROL Audience de l’événement]**

     Sélectionnez l’option _[!UICONTROL Audience de l’événement]_. Cliquez ensuite sur **[!UICONTROL Ajouter des critères d’événement]**.

     Dans la boîte de dialogue _[!UICONTROL Modifier les critères d’événement]_, ajoutez un ou plusieurs événements que vous souhaitez utiliser pour la qualification des membres de l’audience. Pour chaque événement que vous ajoutez, cliquez sur **[!UICONTROL Ajouter une contrainte]** afin de choisir un attribut d’événement pour une correspondance. Définissez l’évaluation que vous souhaitez utiliser pour une correspondance. Vous pouvez ajouter plusieurs contraintes pour correspondre à l’événement.

     ![Ajouter des événements et des critères de correspondance pour qualifier un profil de personne](./assets/node-person-audience-edit-event-criteria-dialog.png){width="700" zoomable="yes"}

     Lorsque les critères d’événement sont définis, cliquez sur **[!UICONTROL Enregistrer]**.

     Pour plus d’informations sur la configuration des événements pris en charge par le parcours, voir [Gestion des événements d’expérience](../admin/configure-aep-events.md#manage-experience-events).
