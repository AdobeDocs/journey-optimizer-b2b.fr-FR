---
title: Configuration
description: Effectuez les tâches de configuration initiales pour votre instance Journey Optimizer B2B Prime, y compris la configuration de l’accès utilisateur et l’infrastructure de délivrabilité des e-mails.
autotag-review: '2026-06-12T23:06:52.179Z'
TQID: 'https://experienceleague.adobe.com/D8qXM-F4anA8IVYmdlaclUoxgTwqQptN36xYFpsuvHY'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
  - id: f467931a-9b22-4ca8-869f-adfbd64061ce
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
  - id: f6df9def-cdf7-4728-9ec8-3f65716828c7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: e849c9406dc83c6dc7c22ff56de32d6a73fed07d
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 55%

---

# Configuration

Effectuez ces tâches pour activer la fonctionnalité dans votre instance Prime B2B de Parcours mise en service.

## Activer l’accès utilisateur

Une fois la mise en service terminée, les sandbox sont liés et les tâches de configuration initiales terminées, configurez l’accès de Journey Optimizer B2B edition et Marketo Engage pour votre équipe et les utilisateurs.

<table>
<thead>
<tr>
<th colspan="2">Tâche</th>
<th>Détails et instructions</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Fournir un accès et des autorisations de produit</strong> pour les utilisateurs</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Création d’un profil de produit Marketo Engage dans Adobe Admin Console (nouvelle instance Marketo Engage uniquement)</td>
<td><a href="./user-management.md#create-profile">En savoir plus</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Ajouter un groupe d’utilisateurs pour le profil</td>
<td><a href="./user-management.md#add-user-group">En savoir plus</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Configurer les rôles utilisateur B2B</td>
<td><a href="./user-management.md#edit-roles-for-product-permissions">En savoir plus</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Ajouter des utilisateurs et utilisatrices ou des groupes aux rôles</td>
<td><a href="./user-management.md#add-users-to-a-role">En savoir plus</a></td>
</tr>
</tbody>
</table>

## Délivrabilité des e-mails

Avant que les professionnels du marketing puissent envoyer des e-mails à partir de parcours, configurez l’infrastructure d’envoi pour votre organisation, y compris la délégation de sous-domaines, l’authentification des e-mails et les paramètres de canal.

<table>
<thead>
<tr>
<th colspan="2">Tâche</th>
<th>Détails et instructions</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Configurer les paramètres de canal et de délivrabilité des e-mails</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Délégation d’un sous-domaine à Adobe</td>
<td><a href="./admin/configuration-email-deliverability.md#delegate-fully-delegated">Délégation complète</a> ou <a href="./admin/configuration-email-deliverability.md#delegate-cname">CNAME</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Configuration de DMARC pour le sous-domaine</td>
<td><a href="./admin/configuration-email-deliverability.md#configure-dmarc">En savoir plus</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Vérification et affectation d’un groupe d’adresses IP</td>
<td><a href="./admin/configuration-email-deliverability.md#review-ip-pool">En savoir plus</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Créer une configuration de canal e-mail</td>
<td><a href="./admin/configuration-email-deliverability.md#create-email-channel-configuration">En savoir plus</a></td>
</tr>
</tbody>
</table>

