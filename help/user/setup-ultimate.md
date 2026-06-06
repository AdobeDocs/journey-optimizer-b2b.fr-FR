---
title: Liste de contrôle de configuration
description: Configurez Journey Optimizer B2B edition. Configurez les schémas XDM, les canaux e-mail/SMS, les actions de parcours Marketo Engage et les utilisateurs et utilisatrices.
feature: Setup, Administration
role: Admin, Developer
exl-id: 81232976-09d6-4e10-a034-5c193a63b7df
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
  - id: f467931a-9b22-4ca8-869f-adfbd64061ce
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
autotag-review: '2026-03-27T22:15:07.682Z'
source-git-commit: ca0c6b10cf6a979249901d514116f373014544ad
workflow-type: tm+mt
source-wordcount: 849
ht-degree: 74%

---

# Liste de contrôle de configuration

Adobe Journey Optimizer B2B edition repose sur Adobe Experience Platform. Avec cette implémentation, Journey Optimizer B2B edition et Marketo Engage ne sont pas sur le même système ou le même magasin de données. Journey Optimizer B2B edition reçoit des données de Adobe Experience Platform. Cependant, il continue de dépendre des droits de Marketo Engage et de certaines fonctionnalités principales, telles que la diffusion d’e-mails, pour configurer le système.

<!-- 
>>[!NOTE]
>
>Earlier documentation referred to this deployment as the *simplified architecture*. That model is now the Journey Optimizer B2B Edition Ultimate implementation. 
-->

Cette implémentation est la base qui active des fonctionnalités dans Journey Optimizer B2B edition :

* **Unifier et mettre à l’échelle vos données :** le système prend en charge des modèles de données complexes, y compris les objets personnalisés, les groupes d’achats et les événements de compte.

* **Connexion de plusieurs instances Adobe Marketo Engage :** permet de gérer et d’unifier les données de plusieurs environnements Marketo Engage.

* **Protection des données :** fonctionnalités avancées de confidentialité et de sécurité qui permettent de protéger les informations de vos clients. (_Bientôt disponible_)

* **Conception évolutive :** cette configuration prend en charge les améliorations et innovations continues.

Suivez les instructions ci-dessous pour configurer .

Utilisez cette liste de contrôle pour terminer la configuration de Journey Optimizer B2B edition.

## &#x200B;1. Générer des espaces de noms et des schémas B2B

<table>
<thead>
<tr>
<th colspan="2">Tâche</th>
<th>Détails et instructions</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Configuration de l’environnement :</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Téléchargez l’utilitaire de génération automatique d’espace de noms et de schéma depuis GitHub .</td>
<td><a href="./data/namespaces-schemas.md#set-up-the-auto-generation-utility">En savoir plus</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Rassemblez les informations d’identification de l’API Experience Platform et les en-têtes requis.</td>
<td><a href="https://experienceleague.adobe.com/fr/docs/experience-platform/landing/platform-apis/api-guide">En savoir plus</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Appliquez des valeurs d’environnement à votre environnement Postman.</td>
<td><a href="./data/namespaces-schemas.md#environment-values">En savoir plus</a></td>
</tr>
<tr>
<td colspan="2"><strong>Exécutez les scripts :</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Exécutez l’utilitaire de génération <em> Espaces de noms et schémas </em> dans Postman et vérifiez que les espaces de noms et les schémas sont créés.</td>
<td><a href="./data/namespaces-schemas.md#run-the-scripts">En savoir plus</a></td>
</tr>
</tbody>
</table>

## &#x200B;2. Configuration des champs et événements XDM

<table>
<thead>
<tr>
<th colspan="2">Tâche</th>
<th>Détails et instructions</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Configurations XDM standard</strong> : configurez les schémas XDM Individual Profile et XDM Business Account.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Sélectionnez les champs gérés à exposer pour les parcours, les groupes d’achats et la personnalisation des e-mails.</td>
<td><a href="./admin/xdm-field-management.md#standard-classes">En savoir plus</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Modifiez les champs pouvant être mis à jour pour les schémas.</td>
<td><a href="./admin/xdm-field-management.md#updatable-fields">En savoir plus</a></td>
</tr>
<tr>
<td colspan="2"><strong>Schémas relationnels</strong> : sélectionnez les champs XDM relationnels (objet personnalisé plusieurs-à-un du compte).</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Assurez-vous que les schémas possèdent les valeurs de configuration requises.</td>
<td><a href="./admin/xdm-field-management.md#relational-schemas">En savoir plus</a></td>
</tr>
<tr>
<td colspan="2"><strong>Événements</strong> : configurez les types d’événements et les champs Experience Platform.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Configurez chaque type d’événement Experience Platform avec des champs à prendre en charge dans les chemins de prise de décision/partage de parcours.</td>
<td><a href="./admin/configure-aep-events.md">En savoir plus</a></td>
</tr>
</tbody>
</table>

## &#x200B;3. Configuration du tracking et de la délivrabilité des e-mails

Pour envoyer des e-mails depuis [!DNL Journey Optimizer B2B Edition], configurez le suivi et la délivrabilité des e-mails dans l’instance de production [!DNL Marketo Engage] jointe et dans l’application [!DNL Journey Optimizer B2B Edition].

<table>
<thead>
<tr>
<th colspan="2">Tâche</th>
<th>Détails et instructions</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Configuration initiale</strong> pour l’instance Marketo Engage jointe</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Configurer un nouveau CNAME pour les liens de suivi dans les enregistrements DNS</td>
<td><a href="./start/email-protocols.md#create-dns-records-for-landing-pages-and-email">En savoir plus</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Configuration des domaines de branding pour l’instance Marketo Engage associée</td>
<td><a href="./start/branding-domains.md">En savoir plus</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Configurez DKIM et SPF sur l’instance Marketo Engage jointe.</td>
<td><a href="./start/email-protocols.md#set-up-spf-and-dkim">En savoir plus</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Configurer DMARC</td>
<td><a href="./start/email-protocols.md#set-up-dmarc">En savoir plus</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Configurer des enregistrements MX pour votre domaine</td>
<td><a href="./start/email-protocols.md#set-up-mx-records-for-your-domain">En savoir plus</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Ajout d’adresses IP sortantes aux places sur la liste autorisée</td>
<td><a href="./start/email-protocols.md#outbound-ip-addresses">En savoir plus</a></td>
</tr>
<tr>
<td colspan="2"><strong>Configuration du canal e-mail</strong> pour l’instance Marketo Engage jointe</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Configurer <em>À partir de l’e-mail</em> et <em>À partir du libellé</em> (facultatif)</td>
<td><a href="./start/email-setup.md#from-email-and-label">En savoir plus</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Configurez <em>Désabonnement d’HTML</em> et <em>Texte de désabonnement</em></td>
<td><a href="./start/email-setup.md#unsubscribe-messaging">En savoir plus</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Configurez <em>Afficher en tant que page Web HTML</em> et <em>Afficher en tant que texte de page Web</em></td>
<td><a href="./start/email-setup.md#view-as-web-page">En savoir plus</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Configurez <em>Limites de récupération d’objet personnalisées</em></td>
<td><a href="./start/email-setup.md#custom-object-retrieval-limits">En savoir plus</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Configurez <em>Options d’en-tête personnalisées</em></td>
<td><a href="./start/email-setup.md#custom-header-options">En savoir plus</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Configuration du filtrage <em>Activité des robots</em></td>
<td><a href="./start/email-setup.md#filter-email-bots">En savoir plus</a></td>
</tr>
<tr>
<td colspan="2"><strong>Configuration du canal e-mail</strong> pour Journey Optimizer B2B edition</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Configuration des <em>limites de communication</em> dans Journey Optimizer B2B edition</td>
<td><a href="./admin/configure-channels-emails.md#communication-limits">En savoir plus</a></td>
</tr>
</tbody>
</table>

<!--
 TBD for later

<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Configure <em>Email CC Settings</em></td>
<td>[Learn more](TBD)</td>
</tr>

<tr>
<td colspan="2"><strong>Additional configurations</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Configure <em>Location Settings</em> for the attached Marketo Engage instance</td>
<td>< [Learn more](TBD)</td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Define and configure which Binding Groups / IPs to move over</td>
<td>[Learn more](TBD)</td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Test Email Send</td>
<td>[Learn more](TBD)</td>
</tr>
-->

## &#x200B;4. Configuration de canaux de contenu supplémentaires

Pour prendre en charge les équipes marketing qui incluent d’autres canaux dans leurs parcours, configurez des canaux supplémentaires.

<table>
<thead>
<tr>
<th colspan="2">Tâche</th>
<th>Détails et instructions</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>SMS</strong> configuration du canal pour Journey Optimizer B2B edition.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Configurez chaque compte SMS à prendre en charge.</td>
<td><a href="./admin/configure-channels-sms.md">En savoir plus</a></td>
</tr>
<tr>
<td colspan="2">Configuration du canal <strong>Pages de destination</strong> (Beta) pour Journey Optimizer B2B edition.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Renseignez les paramètres de la page de destination pour prendre en charge les marketeurs qui créent et publient ces pages</td>
<td><a href="./admin/landing-page-settings.md">En savoir plus</a></td>
</tr>
<tr>
<td colspan="2">Configuration du canal <strong>Web</strong> (Beta) pour Journey Optimizer B2B edition</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Configurez le site web de votre entreprise pour prendre en charge Adobe Experience Platform Web SDK.</td>
<td><a href="https://experienceleague.adobe.com/fr/docs/experience-platform/collection/js/js-overview">En savoir plus</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Ajoutez des propriétés web via une URL où le contenu est diffusé.</td>
<td><a href="./admin/configure-channels-web.md">En savoir plus</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Demandez aux auteurs et autrices d’expérience web d’installer l’extension de navigateur Visual Editing Helper de Adobe Experience Cloud.</td>
<td><a href="./content/web-experiences.md#install-the-visual-editing-helper-extension">En savoir plus</a></td>
</tr>
</tbody>
</table>

## &#x200B;5. Connecter une instance Marketo Engage pour prendre en charge les actions de parcours (facultatif)

Si vous prévoyez de compléter les fonctionnalités de Journey Optimizer B2B edition avec des campagnes et des programmes dans Marketo Engage, configurez la prise en charge des actions Marketo Engage. Ces actions permettent à vos équipes marketing de coordonner leurs efforts marketing _basés sur un compte_ dans Journey Optimizer B2B edition et _basés sur un prospect_ dans Marketo Engage.

<table>
<thead>
<tr>
<th colspan="2">Tâche</th>
<th>Détails et instructions</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Pour chaque instance Marketo Engage</strong> pour prendre en charge les actions de parcours</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Création du service personnalisé Marketo Engage</td>
<td><a href="./admin/marketo-actions-connect.md#create-the-marketo-engage-custom-service">En savoir plus</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Ajouter l’intégration dans Journey Optimizer B2B edition</td>
<td><a href="./admin/marketo-actions-connect.md#add-the-integration">En savoir plus</a></td>
</tr>
</tbody>
</table>

## &#x200B;6. Activer l’accès utilisateur

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
<td><a href="./admin/user-management.md#marketo-engage-profile">En savoir plus</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Ajouter un groupe d’utilisateurs pour le profil</td>
<td><a href="./admin/user-management.md#add-user-group">En savoir plus</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Configurer les rôles utilisateur B2B</td>
<td><a href="./admin/user-management.md#b2b-built-in-roles">En savoir plus</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher"/></td>
<td>Ajouter des utilisateurs et utilisatrices ou des groupes aux rôles</td>
<td><a href="./admin/user-management.md#add-users-to-a-role">En savoir plus</a></td>
</tr>
</tbody>
</table>
