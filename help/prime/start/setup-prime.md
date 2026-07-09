---
title: Liste de contrôle d'installation
description: Effectuez les tâches de configuration initiales pour votre instance Journey Optimizer B2B Prime, y compris la configuration de l’accès utilisateur et l’infrastructure de délivrabilité des e-mails.
badgeBeta: label="Beta" type="informative" tooltip="Cette fonctionnalité fait partie d’une version bêta limitée."
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
source-git-commit: 0f264f00c8018324abf1d409ddc381c6dcc9c08a
workflow-type: tm+mt
source-wordcount: 261
ht-degree: 10%

---

# Liste de contrôle de configuration

Effectuez ces tâches pour activer la fonctionnalité dans votre instance [!DNL Journey Optimizer B2B Prime] configurée.

## Activer l’accès utilisateur {#enable-user-access}

Une fois la mise en service terminée et les sandbox liés, configurez l’accès [!DNL Journey Optimizer B2B Edition] pour votre équipe et les utilisateurs.

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
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher de la tâche"/></td>
<td>Création d’un profil de produit Journey Optimizer B2B edition dans Admin Console (configuration unique/initiale uniquement)</td>
<td><a href="./user-management.md#create-profile">Créer un profil</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher de la tâche"/></td>
<td>Ajout d’un groupe d’utilisateurs dans Admin Console</td>
<td><a href="./user-management.md#add-user-group">Ajouter un groupe d’utilisateurs</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher de la tâche"/></td>
<td>Affectez le profil de produit au groupe d’utilisateurs dans l’Admin Console</td>
<td><a href="./user-management.md#assign-profile">Attribuer un profil de produit</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher de la tâche"/></td>
<td>Ajout d’utilisateurs au groupe d’utilisateurs dans Admin Console</td>
<td><a href="./user-management.md#add-users">Ajouter des utilisateurs et utilisatrices</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher de la tâche"/></td>
<td>Modifier les rôles intégrés ou créer un rôle personnalisé avec des autorisations de produit</td>
<td><a href="./user-management.md#edit-role-permissions">Modifier les rôles</a> <br/> <a href="./user-management.md#create-a-custom-role">Créer un rôle personnalisé</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher de la tâche"/></td>
<td>Ajout d’utilisateurs, d’utilisatrices ou de groupes à des rôles dans Adobe Experience Platform</td>
<td><a href="./user-management.md#add-users-to-a-role">Ajouter des utilisateurs</a> <br/><a href="./user-management.md#add-user-groups-to-a-role">Ajouter des groupes</a></td>
</tr>
</tbody>
</table>

## Délivrabilité des e-mails {#email-deliverability}

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
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher de la tâche"/></td>
<td>Déléguer un sous-domaine à Adobe (entièrement délégué ou CNAME)</td>
<td><a href="./email-deliverability.md#delegate-fully-delegated">Délégation complète</a> <br/> <a href="./email-deliverability.md#delegate-cname">CNAME</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher de la tâche"/></td>
<td>Configuration de DMARC pour le sous-domaine</td>
<td><a href="./email-deliverability.md#configure-dmarc">Configuration de DMARC</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher de la tâche"/></td>
<td>Vérification et affectation d’un groupe d’adresses IP</td>
<td><a href="./email-deliverability.md#review-ip-pool">Vérifier le groupe d’adresses IP</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher de la tâche"/></td>
<td>Créer une configuration de canal e-mail</td>
<td><a href="../admin/email-channel-configuration.md#create-email-channel-configuration">Configurer le canal e-mail</a></td>
</tr>
</tbody>
