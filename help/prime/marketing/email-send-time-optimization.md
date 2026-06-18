---
title: Optimisation de l’heure d’envoi des e-mails
description: L’optimisation de l’heure d’envoi (STO) dans Adobe Journey Optimizer B2B Prime personnalise la diffusion d’e-mails pour les parcours de personne. Découvrez comment activer la STO et améliorer l’engagement.
autotag-review: '2026-06-17T20:52:02.535Z'
TQID: 'https://experienceleague.adobe.com/wlxhS7E8DnbThm5ge-wzTkMcn-eBzFUXfw3ZGrfcRHA'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: bef5003b-cad2-4f40-bdb2-a80426d52ef5id: f01b5556-e951-40ba-8625-2e3001864f2bid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
source-git-commit: 951d9ceaa95656952e36b6d8f238348b08c796ca
workflow-type: tm+mt
source-wordcount: 403
ht-degree: 0%

---

# Optimisation de l’heure d’envoi des e-mails

Utilisez la fonctionnalité d’optimisation de l’heure d’envoi (STO) pour personnaliser le délai de diffusion des e-mails pour les parcours de personne](./person-journeys.md) en prédisant le moment où chaque profil est le plus susceptible d’interagir. [Au lieu d’une heure d’envoi fixe, STO utilise des signaux d’engagement historiques des e-mails pour planifier la diffusion à l’heure optimale pour chaque destinataire, améliorant ainsi l’engagement global.

STO analyse l&#39;engagement historique de chaque profil à l&#39;aide d&#39;un grand modèle linguistique. Il prédit et classe les heures d’envoi potentielles, puis planifie la diffusion au moment le plus élevé de la fenêtre d’optimisation.

<!-- Performance insights, such as usage, engagement lift, and STO vs. non-STO comparisons, are available through natural language queries in the AI Assistant. -->

>[!BEGINSHADEBOX]

De nombreuses **_améliorations futures_** sont prévues pour la STO :

* Configuration globale de la STO dans la zone _[!UICONTROL Admin]_
* Activation de la STO de parcours niveau
* Partage de test/contrôle configurable

>[!ENDSHADEBOX]

## Configuration {#configuration}

Vous pouvez configurer l’optimisation de l’heure d’envoi lorsque vous [ajoutez un nœud _[!UICONTROL Prendre une action]_](./action-nodes.md) à un parcours de personne et choisissez l’action **[!UICONTROL Envoyer un e-mail]**.

1. Sélectionnez le nœud d’action de parcours _Envoyer un e-mail_.

1. Dans les propriétés de nœud sur la droite, activez l’option **[!UICONTROL Optimisation de l’heure d’envoi]**.

   ![Nœud de parcours Envoyer un e-mail - Options d’optimisation de l’heure d’envoi](./assets/email-node-send-time-optimization.png){width="450" zoomable="no"}

1. Pour spécifier la fenêtre et la distribution de test, définissez les options STO :

   * **[!UICONTROL Envoyer dans les prochains]** - Cette valeur détermine la fenêtre d’optimisation (en jours), qui correspond à la période pendant laquelle les e-mails peuvent être diffusés. Par exemple, pour un webinaire ayant lieu dans cinq jours, vous pouvez définir une fenêtre de quatre ou cinq jours. STO sélectionne l’heure d’envoi la mieux prévue pour chaque profil dans cette fenêtre.

   * **Distribution STO/Fixe** - La distribution STO crée automatiquement une _répartition de test et de contrôle_ pour diviser les profils éligibles entre les heures d&#39;envoi optimisées et fixes. La division permet une comparaison directe des performances. (De futures améliorations sont prévues pour autoriser les pourcentages de partage personnalisés.)

   >[!NOTE]
   >
   >Les profils ayant un historique d’engagement solide sont divisés de manière égale en groupes de contrôle et de test afin de mesurer l’impact de la STO. Afin de garantir des résultats statistiquement fiables, la répartition entre STO et non-STO est limitée entre 30 % et 70 %. Cela permet d’éviter que des cohortes plus petites biaisent les résultats et d’assurer des comparaisons significatives.

1. Directement après le nœud _[!UICONTROL Envoyer un e-mail]_, [ajoutez un nœud _Attente_](./wait-nodes.md).

   Un nœud d’attente doit immédiatement suivre une action e-mail compatible avec STO. L’ajout de ce nœud permet de s’assurer que les profils restent dans le parcours jusqu’à ce que la fenêtre d’optimisation complète soit effacée et que tous les envois STO soient terminés. Si vous omettez ce nœud, le système signale la configuration comme non valide.

1. Une fois le parcours de la personne terminé, passez à [publication](./person-journeys.md#publish).

## Production de rapports


