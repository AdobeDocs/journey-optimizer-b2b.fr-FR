---
title: Optimisation de l’heure d’envoi des e-mails
description: L’optimisation de l’heure d’envoi (STO) dans Adobe Journey Optimizer personnalise la diffusion d’e-mails pour les parcours de personne. Découvrez comment activer la STO et améliorer l’engagement.
feature: Person Journeys, Channels
role: User
exl-id: a0423bdc-f2ad-450b-9dc6-b9f2f7a1ef8c
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
subfeature_v2:
  - id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
  - id: af7eab5e-3580-4254-9f56-3c20b4f6ef42
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
autotag-review: '2026-04-29T23:21:59.633Z'
source-git-commit: 2c6aafd07cf033df8801621f7e5275dbeeb2768e
workflow-type: tm+mt
source-wordcount: 483
ht-degree: 0%

---

# Optimisation de l’heure d’envoi des e-mails

Utilisez la fonctionnalité d’optimisation de l’heure d’envoi (STO) pour personnaliser le délai de diffusion des e-mails pour les parcours de personne[&#128279;](../journeys/journeys-overview.md) en prédisant le moment où chaque profil est le plus susceptible d’interagir. Au lieu d’une heure d’envoi fixe, STO utilise des signaux d’engagement historiques des e-mails pour planifier la diffusion à l’heure optimale pour chaque destinataire, améliorant ainsi l’engagement global.

STO analyse l&#39;engagement historique de chaque profil à l&#39;aide d&#39;un grand modèle linguistique. Il prédit et classe les heures d’envoi potentielles, puis planifie la diffusion au moment le plus élevé de la fenêtre d’optimisation.

## Disponibilité et portée actuelles

L’optimisation de l’heure d’envoi est actuellement prise en charge pour :

* **Type de Parcours** : Parcours de personne
* **Canal** : e-mail
* **Configuration** : nœud d’action _Envoyer un e-mail_
* **Reporting** : assistant AI grâce à la compétence Observability du Parcours

  Des informations sur les performances, telles que l’utilisation, l’effet élévateur d’engagement et les comparaisons STO/non-STO, sont disponibles par le biais de requêtes en langage naturel dans l’assistant d’IA.

>[!BEGINSHADEBOX]

De nombreuses **_améliorations futures_** sont prévues pour la STO :

* Prise en charge de Parcours de compte __
* Configuration globale de la STO dans la zone _[!UICONTROL Admin]_
* Activation de la STO de parcours niveau
* Partage de test/contrôle configurable
* Un tableau de bord de reporting STO dédié

>[!ENDSHADEBOX]

## Configuration

Vous pouvez configurer l’optimisation de l’heure d’envoi lorsque vous [ajoutez un nœud _[!UICONTROL Prendre une action]_](../journeys/action-nodes.md) à un parcours de personne.

1. Pour _[!UICONTROL Sélectionner une action]_, choisissez **[!UICONTROL Envoyer un e-mail]**.

1. Utilisez le bouton (bascule) **[!UICONTROL Optimisation de l’heure d’envoi]** pour activer la fonctionnalité.

1. Pour spécifier la fenêtre et la distribution de test, définissez les options STO :

   * **[!UICONTROL Envoyer dans les prochains]** - Cette valeur détermine la fenêtre d’optimisation (en jours), qui correspond à la période pendant laquelle les e-mails peuvent être diffusés. Par exemple, pour un webinaire ayant lieu dans cinq jours, vous pouvez définir une fenêtre de quatre ou cinq jours. STO sélectionne l’heure d’envoi la mieux prévue pour chaque profil dans cette fenêtre.

   * **Distribution STO/Fixe** - La distribution STO crée automatiquement une _répartition de test et de contrôle_ pour diviser les profils éligibles entre les heures d&#39;envoi optimisées et fixes. La division permet une comparaison directe des performances. (De futures améliorations sont prévues pour autoriser les pourcentages de partage personnalisés.)

   >[!NOTE]
   >
   >Les profils ayant un historique d’engagement solide sont divisés de manière égale en groupes de contrôle et de test afin de mesurer l’impact de la STO. Afin de garantir des résultats statistiquement fiables, la répartition entre STO et non-STO est limitée entre 30 % et 70 %. Cela permet d’éviter que des cohortes plus petites biaisent les résultats et d’assurer des comparaisons significatives.

   ![Nœud de parcours Envoyer un e-mail - Options d’optimisation de l’heure d’envoi](./assets/email-node-send-time-optimization.png){width="700" zoomable="no"}

1. Directement après le nœud _[!UICONTROL Envoyer un e-mail]_, [ajoutez un nœud _Attente_](../journeys/wait-nodes.md).

   Un nœud d’attente doit immédiatement suivre une action e-mail compatible avec STO. L’ajout de ce nœud permet de s’assurer que les profils restent dans le parcours jusqu’à ce que la fenêtre d’optimisation complète soit effacée et que tous les envois STO soient terminés. Si vous omettez ce nœud, le système signale la configuration comme non valide.

1. Une fois le parcours de la personne terminé, passez à [publication](../journeys/create-publish-journey.md#publish-a-journey).

## Informations sur l’arrêt

Les informations STO sont fournies par l’intermédiaire de l’_assistant AI_ à l’aide de la compétence Journey Agent [_observabilité_](../agents/journey-agent.md#journey-observability-skill). Vous pouvez interroger l’utilisation, les mesures d’engagement, les résultats des tests/contrôles, les performances des nœuds et l’impact global du parcours.
