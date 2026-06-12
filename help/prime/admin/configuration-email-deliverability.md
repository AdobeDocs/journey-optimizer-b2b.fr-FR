---
title: Délivrabilité des e-mails et configuration des canaux
description: Configurez la délégation de sous-domaine, DMARC, SPF, DKIM, les pools d'adresses IP et les configurations de canal e-mail pour Journey Optimizer B2B Prime.
autotag-review: '2026-06-12T22:43:42.799Z'
TQID: 'https://experienceleague.adobe.com/RKZSQkjSRvHixOm2faRT5D-yB00IykXfPO06vvIUQ6k'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: d6e625c1-468f-4d73-9f32-fd1edb87f96bid: f01b5556-e951-40ba-8625-2e3001864f2bid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: cb3217c9fd7beb712d0c61638d143b798010d2b7
workflow-type: tm+mt
source-wordcount: 3414
ht-degree: 1%

---

# Délivrabilité des e-mails et configuration des canaux

[!DNL Adobe Journey Optimizer B2B Edition] Prime offre aux spécialistes du marketing B2B une expérience moderne de création et de diffusion d’e-mails de niveau professionnel. Cette version introduit des outils de conception d’e-mail repensés et un ensemble complet de contrôles de délivrabilité des e-mails.

Les informations suivantes sont destinées aux administrateurs qui configurent l’infrastructure d’envoi pour prendre en charge les spécialistes marketing et les auteurs d’e-mails. Il décrit les fonctionnalités de délivrabilité, les rôles et autorisations, ainsi que la manière de configurer des sous-domaines, une authentification, des groupes d’adresses IP et des configurations de canal.

Pour plus d’informations sur la création d’e-mails et de contenu d’e-mail dans l’espace de conception des e-mails, voir [Création d’e-mails](../content/email-authoring.md).

## Présentation du canal e-mail {#overview}

* **Outils visuels de conception d’e-mail par glisser-déposer** - Concevez le contenu de votre e-mail avec des structures, des composants de contenu, des thèmes, une prise en charge du mode sombre et des fragments visuels réutilisables.
* **Configurations du canal e-mail** - Gérez l’identité de l’expéditeur, le comportement de réponse, les types de messages marketing par rapport aux messages transactionnels et le suivi.
* **Contrôles de délivrabilité des e-mails** - Configurez votre canal de délivrabilité des e-mails, y compris la délégation de sous-domaines (méthodes Fully Delegated et CNAME), DMARC, la configuration automatique SPF/DKIM et la prise en charge du pool d’adresses IP partagées.
* **Action Envoyer un e-mail** - À partir d’un parcours, ajoutez une action Envoyer un e-mail , y compris la personnalisation à l’aide d’attributs de profil (syntaxe Handlebars).
* **Ressources Marketo Design Studio** — choisissez des images et des ressources à partir d’une copie ponctuelle de votre bibliothèque de ressources Marketo Engage directement dans la zone de travail d’e-mail.
* **Modèles et fragments réutilisables** — Enregistrez les en-têtes, pieds de page, CTA et dispositions complètes d&#39;e-mail courants et réutilisez-les dans les parcours.
* **Contrôle d’accès en fonction du rôle (RBAC)** — Appliquez des autorisations granulaires pour la création, la modification, l’approbation et l’envoi d’e-mails.

## Principaux concepts {#key-concepts}

Avant de configurer les e-mails, passez en revue ces concepts qui s’appliquent aux fonctionnalités du canal e-mail dans l’ensemble du produit.

| Concept | Signification dans [!DNL Journey Optimizer B2B Edition] Prime |
| ------- | ---------------------- |
| **_Configuration du canal_** | Ensemble réutilisable de paramètres d’envoi d’e-mail, notamment l’identité de l’expéditeur, l’adresse de réponse, le sous-domaine, le groupe d’adresses IP, le type d’e-mail (marketing ou transactionnel) et le suivi, que vous joignez aux actions d’e-mail dans parcours. Vous pouvez avoir plusieurs configurations de canal nommé pour différentes marques, unités opérationnelles ou types d’envoi. |
| **_Sous-domaine_** | Partie déléguée de votre domaine d’envoi (par exemple, `mail.contoso.com`) utilisée pour envoyer des e-mails via Prime. Les sous-domaines isolent votre réputation marketing B2B des e-mails d’entreprise ou transactionnels. |
| **_Groupe d’adresses IP_** | Groupe d’adresses IP associées à un ou plusieurs sous-domaines. Prime prend en charge un groupe d’adresses IP partagé géré par Adobe dans cette version. Les groupes d’adresses IP dédiés figurent sur la feuille de route GA. |
| **_Espace de conception des emails_** | Canevas visuel et outils de conception utilisés pour composer du contenu d’e-mail. Il comprend des composants de disposition à glisser-déposer, des modèles, des fragments, des thèmes et un éditeur de personnalisation. |
| **_Modèle_** | Disposition d’e-mail réutilisable disponible pour la création d’un e-mail. Il peut s’agir d’un modèle type intégré fourni par Adobe ou d’un modèle personnalisé créé par votre équipe. |
| **_Fragment visuel_** | Bloc de contenu réutilisable (par exemple, en-tête, pied de page, CTA, clause de non-responsabilité) pouvant être inséré dans plusieurs e-mails. La mise à jour d’un fragment propage la modification à chaque e-mail qui l’utilise. |
| **_Thème_** | Paramètre prédéfini de style réutilisable (couleurs, typographie, espacement, styles de bouton) appliqué à un e-mail. |
| **_Jeton_** | Une expression Handlebars, par exemple `{{profile.firstName}}`, résolue au moment de l’envoi à l’aide des données de profil de chaque destinataire. |
| **_Action Envoyer un e-mail_** | Nœud d’action de parcours qui utilise une configuration de canal et du contenu d’e-mail pour diffuser un e-mail. |

## Rôles et autorisations {#roles-permissions}

[!DNL Journey Optimizer B2B Edition] Prime utilise le contrôle d’accès basé sur les rôles (RBAC) pour les fonctionnalités d’e-mail. Les autorisations sont gérées dans Adobe Admin Console (IMS) et synchronisées lors de la connexion. Les administrateurs de produit attribuent des autorisations granulaires aux profils de produit, puis joignent ces profils de produit aux utilisateurs.

L’accès à la fonctionnalité d’e-mail dans [!DNL Journey Optimizer B2B Edition] Prime est contrôlé par deux couches :

1. **Indicateur de fonctionnalité (LD).** Un indicateur LaunchDarkly contrôle si la fonctionnalité entière est activée pour votre organisation. La création et la délivrabilité des emails sont contrôlées par `dx_ajo_btob_channel_foundation`. Sans cet indicateur, la fonctionnalité est masquée, quelles que soient les autorisations.
2. **Autorisation fonctionnelle.** Autorisation au niveau de l’utilisateur qui contrôle si un utilisateur spécifique peut lire ou écrire dans une fonction.

La plupart des fonctionnalités d’e-mail suivent un modèle `view-*` (lecture) et `manage-*` (écriture). Un utilisateur a besoin des autorisations de lecture pour voir une fonctionnalité dans la navigation, et des autorisations d’écriture pour créer, modifier ou supprimer cette fonctionnalité.

### Autorisations de création d’e-mails {#email-authoring-permissions}

| Fonctionnalité | Autorisation | Ce que cela permet |
| ---------- | ---------- | -------------- |
| **Afficher les e-mails** | `view-b2b-emails` | Afficher la liste des e-mails, ouvrir les e-mails, afficher le contenu (lecture seule). |
| **Créer / modifier / supprimer des e-mails** | `manage-b2b-emails` | Tous les accès en lecture et la création, la modification, la duplication et la suppression des e-mails. Obligatoire pour créer du contenu d’e-mail dans un parcours. |
| **Afficher les modèles** | `view-b2b-templates` | Parcourez et prévisualisez des modèles dans la Galerie de modèles (lecture seule). |
| **Créer / modifier / supprimer des modèles** | `manage-b2b-templates` | Tous les accès en lecture et la création, la modification et la suppression des modèles enregistrés. |
| **Affichage des fragments** | `view-b2b-fragments` | Parcourez et prévisualisez des fragments visuels (lecture seule). |
| **Créer/modifier des fragments** | `manage-b2b-fragments` | Tous les accès en lecture, ainsi que la création et la modification de fragments visuels. |
| **Publication de fragments** | `publish-b2b-fragments` | Publiez un fragment afin qu’il soit disponible pour les auteurs d’e-mails dans l’ensemble de l’organisation. |
| **Gestion des ressources partagées et des éléments de bibliothèque** | `manage-b2b-library-items` | Gérez la bibliothèque partagée sous-jacente utilisée par les modèles, les fragments et les e-mails. Souvent accordée avec les autorisations de gestion des modèles/fragments. |
| **Gérer les libellés d’utilisation** | `manage-b2b-delete-usage-labels` | Gérez les libellés d’utilisation des données (DULE) associés aux éléments de bibliothèque à des fins de gouvernance. |
| **Gérer les packages** | `manage-b2b-packages` | Regroupez et déplacez des modèles, des fragments et des e-mails entre les sandbox. |
| **Affichage des ressources (ressources de Marketo Design Studio dans Prime)** | `view-b2b-assets` | Parcourez le sélecteur de ressources et prévisualisez des images. Lecture seule. |
| **Gérer les ressources** | `manage-b2b-assets` | Tous les accès en lecture plus les futures actions de gestion des ressources (portée de Beta). |
| **Exporter les données du message** | `manage-b2b-message-export` | Exportez les données et les rapports des messages au niveau des e-mails. |

Dans un parcours, l’action **Envoyer un e-mail** nécessite une `manage-b2b-person-journeys` (pour ajouter l’action et activer le parcours). Un utilisateur disposant uniquement d’autorisations de messagerie peut créer du contenu, mais ne peut pas ajouter d’e-mail à un parcours.

### Autorisations de délivrabilité des emails {#email-deliverability-permissions}

Les fonctionnalités de délivrabilité (sous-domaines, DMARC, groupes d’adresses IP, listes de suppression, listes autorisées, plans de préchauffage d’adresses IP et listes de contrôle) sont configurées au niveau de l’administrateur. Ils sont régis par deux autorisations couvrant l’ensemble de la zone **[!UICONTROL Canaux]** > **[!UICONTROL Paramètres d’e-mail]** :

| Fonctionnalité | Autorisation | Ce que cela permet |
| ---------- | ---------- | -------------- |
| **Afficher les paramètres d’e-mail** | `view-b2b-email-settings` | Affichez les sous-domaines, les enregistrements PTR, les pools d&#39;adresses IP, la liste de suppression, la liste autorisée, les plans de préchauffage d&#39;adresses IP et les listes de contrôle (lecture seule). |
| **Gérer les paramètres d’e-mail** | `manage-b2b-email-settings` | Tous les accès en lecture plus la délégation de sous-domaines, la configuration de DMARC, la gestion de la suppression et des listes autorisées, la gestion des plans de préchauffage d’adresses IP et des listes de contrôle. |

Certaines sous-fonctionnalités des paramètres d’e-mail sont protégées par des indicateurs LaunchDarkly supplémentaires : Liste de suppression (`enable-suppression`), Liste autorisée (`enable-allow-list`), Listes de contrôle (`enable-seedlist-ui`). Si une sous-fonctionnalité n’est pas visible dans votre organisation, contactez votre représentant Adobe pour savoir si l’indicateur est activé.

### Autorisations de configuration des canaux {#channel-configuration-permissions}

Les configurations de canal se trouvent sous **[!UICONTROL Canaux]** → **[!UICONTROL Paramètres généraux]**. Ils lient les primitives de délivrabilité (sous-domaine, groupe d’adresses IP, identité de l’expéditeur) à un objet réutilisable auquel les auteurs du parcours font référence. Elles sont régies par une seule autorisation :

| Fonctionnalité | Autorisation | Ce que cela permet |
| ---------- | ---------- | -------------- |
| **Gérer les configurations de canal** | `manage-b2b-channels-configurations` | Affichez, créez, modifiez et supprimez des configurations de canal e-mail. |

## Présentation de la délivrabilité des e-mails {#deliverability-overview}

La délivrabilité des emails dans [!DNL Journey Optimizer B2B Edition] Prime est l’ensemble des configurations d’infrastructure et d’authentification qui permettent aux emails d’atteindre la boîte de réception du destinataire, et non le dossier des spams, et qui ne sont pas bloqués par les FAI (fournisseurs d’accès Internet).

Il utilise les blocs de création suivants, configurés par un administrateur, généralement dans l’ordre suivant :

1. Déléguez un ou plusieurs sous-domaines à Adobe.
1. Configurez les enregistrements DMARC, SPF et DKIM sur chaque sous-domaine.
1. Confirmez le groupe d’adresses IP qui enverra un e-mail pour votre sous-domaine.
1. Créez une ou plusieurs configurations de canal e-mail qui lient un sous-domaine, un groupe d’adresses IP et une identité d’expéditeur.
1. Utilisez ces configurations de canal dans les actions d’e-mail de parcours.

>[!TIP]
>
>Traiter la configuration de la délivrabilité comme une activité administrative unique par unité opérationnelle ou marque. Une fois configurés, les professionnels du marketing et les auteurs d’e-mails n’ont pas besoin de les revoir.

## Délégation de sous-domaines {#subdomain-delegation}

La délégation de sous-domaine indique à Internet qu’Adobe est autorisé à envoyer des e-mails au nom d’un sous-domaine spécifique (par exemple, `mail.contoso.com`) de votre domaine. La délégation d’un sous-domaine dédié, plutôt que votre domaine racine, protège votre messagerie d’entreprise et aboutit à un

* **Isolement de la réputation.** Les envois marketing sont séparés du courrier d’entreprise. Si la réputation marketing se détériore, vos e-mails transactionnels et d’entreprise ne sont pas affectés.
* **Préchauffage d’adresses IP plus rapide.** Des sous-domaines dédiés permettent d&#39;établir plus rapidement une réputation positive de l&#39;expéditeur avec les FAI.
* **Authentification moderne.** SPF, DKIM et DMARC peuvent être configurés de manière propre par sous-domaine sans affecter les autres flux d’e-mails.
* **Conformité.** Permet de répondre aux exigences en matière d’expéditeurs en masse de Gmail, Yahoo et d’autres principaux FAI.

>[!NOTE]
>
>Chaque sous-domaine de Prime ne peut être utilisé que par un seul produit Adobe. Vous ne pouvez pas partager le même sous-domaine d’envoi entre Prime et un autre produit tel que Adobe Marketo Engage ou Adobe Campaign. Vous devez utiliser des sous-domaines distincts.

### Méthodes prises en charge

Prime prend en charge deux des trois méthodes de délégation de sous-domaine dans Alpha. La troisième méthode (délégation personnalisée) figure sur la feuille de route.

| Méthode | Quand l’utiliser | Ce que cela implique |
| ------ | ----------- | ---------------- |
| **Entièrement délégué** | Recommandé | Déléguez l’autorité DNS complète du sous-domaine à Adobe. Adobe crée et gère les enregistrements MX, SPF, DKIM, DMARC, A et CNAME. Frais généraux d’exploitation les plus faibles. Adobe gère les modifications DNS pour vous. |
| **CNAME** | Pour les politiques restreintes | Conservez l’autorité DNS de votre côté et créez des enregistrements CNAME pointant vers des enregistrements gérés par Adobe. Utilisez cette option lorsque la politique DNS de votre organisation n’autorise pas la délégation complète. Vous êtes responsable de la gestion des enregistrements DNS. |
| **Délégation personnalisée** | Feuille de route (GA) | Conservez la pleine propriété des certificats DNS et SSL. Offre un contrôle maximal, notamment la possibilité d’utiliser vos propres certificats. Il est destiné à la version mise à jour en disponibilité générale. |

### Délégation d’un sous-domaine (méthode entièrement déléguée) {#delegate-fully-delegated}

>[!PREREQUISITES]
>
>* Choisissez une convention de nommage des sous-domaines (par exemple, `mail.contoso.com` pour le marketing, `alerts.contoso.com` pour le transactionnel).
>* Vérifiez auprès de votre équipe informatique/DNS qu’elle peut déléguer le sous-domaine (enregistrements DNS) à Adobe.
>* Créez le nouveau sous-domaine dans votre fournisseur DNS, puis attendez 24 à 48 heures pour la propagation DNS avant de déléguer à Adobe.
>* Vérifiez que vous disposez du rôle Administrateur dans Prime.

1. [!DNL Adobe Journey Optimizer B2B Edition] Prime, accédez à **[!UICONTROL Administration]** → **[!UICONTROL Canaux]** → **[!UICONTROL Paramètres d’e-mail]** → **[!UICONTROL Sous-domaines]**.
1. Cliquez sur **[!UICONTROL Configurer un sous-domaine]**.
1. Saisissez le nom complet du sous-domaine (par exemple, `mail.contoso.com`).
1. Choisissez **[!UICONTROL Délégation complète]** comme méthode de délégation.
1. Configurez DMARC pour le sous-domaine (voir [DMARC, SPF et DKIM](#dmarc-spf-dkim)).

   Au minimum, configurez un enregistrement DMARC avec une politique de démarrage de `none` afin de pouvoir surveiller les rapports sans affecter la diffusion.

1. Consultez la liste des enregistrements DNS à gérer par Adobe.

   Ils comprennent généralement des enregistrements MX, SPF, DKIM, DMARC, A et CNAME (pour le suivi et les URL de page miroir).

1. Téléchargez les enregistrements DNS au format CSV à l’aide du bouton **[!UICONTROL Télécharger les enregistrements]**. Partagez ce fichier avec votre équipe DNS.

1. Votre équipe DNS ajoute les enregistrements DNS de votre solution d’hébergement de domaine qui délèguent le sous-domaine à Adobe.

1. Une fois que votre équipe DNS a confirmé que les enregistrements sont en place, revenez à [!DNL Journey Optimizer B2B Edition] Prime et cochez la case confirmant que vous avez créé les enregistrements requis sur le site d’hébergement.

1. Cliquez sur **[!UICONTROL Envoyer]** pour lancer une série de contrôles de validation (pré-validation, MX, SPF, DKIM, DMARC, enregistrement FBL).

1. Attendez que le statut du sous-domaine passe à **[!UICONTROL Succès]**.

   Cela prend généralement quelques minutes une fois la propagation DNS terminée.

>[!NOTE]
>
>Si la validation échoue, le statut passe à **[!UICONTROL Échec]** et [!DNL Journey Optimizer B2B Edition] Prime affiche la raison (par exemple, enregistrement NS introuvable, enregistrement MX manquant ou DMARC mal configuré). Corrigez le problème DNS sous-jacent, puis réessayez l’envoi.

### Délégation d’un sous-domaine (méthode CNAME) {#delegate-cname}

Utilisez cette méthode uniquement si la politique DNS de votre organisation interdit la délégation complète. Avec CNAME, vous conservez les enregistrements DNS de votre côté.

1. Dans [!DNL Adobe Journey Optimizer B2B Edition] Prime, accédez à **[!UICONTROL Administration]** → **[!UICONTROL Canaux]** → **[!UICONTROL Paramètres d’e-mail]** → **[!UICONTROL Sous-domaines]**.
1. Cliquez sur **[!UICONTROL Configurer un sous-domaine]**.
1. Saisissez le nom de sous-domaine complet.
1. Choisissez **[!UICONTROL CNAME]** comme méthode de délégation.
1. Configurez DMARC pour le sous-domaine ([DMARC, SPF et DKIM](#dmarc-spf-dkim)).
1. Consultez la liste des enregistrements CNAME générée par Prime qui pointent les composants de votre sous-domaine vers des enregistrements gérés par Adobe.
1. Téléchargez les enregistrements au format CSV et partagez-les avec votre équipe DNS.
1. Votre équipe DNS ajoute chaque enregistrement CNAME à votre solution d’hébergement DNS.
1. Une fois les enregistrements en place et propagés, revenez à Prime et confirmez. Cliquez sur **[!UICONTROL Envoyer]**.
1. Attendez que le statut atteigne **[!UICONTROL Succès]**.

>[!IMPORTANT]
>
>Avec CNAME, Adobe ne peut pas vous aider à modifier, gérer ou résoudre les problèmes de DNS pour le sous-domaine. Toute modification ultérieure (par exemple, l’ajout d’un nouveau CNAME pour une mise à jour de fonctionnalité) doit être effectuée par votre équipe DNS.

### Mécanismes de sécurisation de sous-domaine {#subdomain-guardrails}

* **Limite par défaut :** 10 sous-domaines par organisation. Contactez votre représentant Adobe si vous en avez besoin (jusqu’à 100 selon le contrat).
* **Propagation DNS :** patientez entre 24 et 48 heures pour que les modifications se propagent globalement. La validation peut échouer simplement parce que le DNS ne s’est pas encore propagé.
* **Réutilisation de sous-domaine :** un sous-domaine déjà utilisé par un autre produit Adobe (Marketo Engage, Adobe Campaign) ne peut pas être réutilisé dans Prime.

## DMARC, SPF et DKIM {#dmarc-spf-dkim}

DMARC, SPF et DKIM sont des normes d’authentification de messagerie. Ensemble, ils prouvent aux serveurs de messagerie de réception que votre message est réellement envoyé au nom de votre domaine et n&#39;a pas été falsifié. Les FAI modernes — Gmail, Yahoo, Microsoft — ont besoin de ces normes pour les expéditeurs en masse.

| Enregistrement | Signifie | But |
| ------ | ---------- | ------- |
| **SPF** | Cadre de la politique de l&#39;expéditeur | Répertorie les adresses IP de serveur de messagerie autorisées à envoyer des e-mails à partir de votre domaine. Les serveurs de réception rejettent les e-mails provenant d’adresses IP qui ne figurent pas sur cette liste. Adobe crée et conserve automatiquement l’enregistrement SPF lorsque vous déléguez un sous-domaine (Délégation complète). |
| **** | Message identifié DomainKeys | Une signature cryptographique ajoutée à chaque e-mail sortant. Le serveur de réception vérifie la signature par rapport à une clé publique publiée dans le DNS. Adobe génère automatiquement des clés DKIM et des enregistrements DNS lors de la délégation de sous-domaine. |
| **** | Authentification, reporting et conformité des messages basés sur des domaines | Indique aux serveurs de réception ce qu’ils doivent faire en cas d’échec de SPF ou de DKIM et fournit des rapports sur les résultats de l’authentification. DMARC comporte trois modes de stratégie : aucun, mise en quarantaine et rejet. |

### Modes de stratégie DMARC

| Stratégie | Action | Quand l’utiliser |
| ------ | ------ | ----------- |
| `none` | Surveiller | Le serveur de réception ne fait rien en cas d’échec de DMARC, mais envoie tout de même un rapport. Utilisez cette option lors de la première délégation d’un sous-domaine pour confirmer que l’authentification fonctionne sans risque de perte de message. |
| `quarantine` | Quarantaine | Le serveur de réception place les messages en échec dans le dossier des courriers indésirables. |
| `reject` | Rejeter | Le serveur de réception rejette (bounces) les messages dont l&#39;authentification a échoué. Mode le plus strict. Recommandé une fois que vous êtes sûr de votre configuration d’authentification. |

### Configuration de DMARC {#configure-dmarc}

DMARC est configuré au moment de la délégation de sous-domaine, mais vous pouvez également ajouter ou mettre à jour DMARC pour un sous-domaine déjà délégué.

1. Accédez à **[!UICONTROL Administration]** → **[!UICONTROL Canaux]** → **[!UICONTROL Paramètres d’e-mail]** → **[!UICONTROL Sous-domaines]**.

1. Dans la liste Sous-domaines , recherchez votre sous-domaine et vérifiez la colonne Enregistrement DMARC .

   Si un enregistrement est manquant, une alerte s’affiche.

1. Ouvrez le sous-domaine et accédez à la section Enregistrement DMARC .

   * Si un enregistrement DMARC existe déjà sur le domaine parent, [!DNL Journey Optimizer B2B Edition] Prime récupère automatiquement les valeurs. Vous pouvez les conserver ou les remplacer.
   * S’il n’existe aucun enregistrement, choisissez **[!UICONTROL Gérer avec Adobe]** afin qu’Adobe crée et héberge l’enregistrement DMARC.

1. Définissez la politique : `none`, `quarantine` ou `reject`. Commencez par `none`, sauf si vous disposez déjà d’une posture DMARC mature sur votre domaine parent.

1. (Facultatif) Configurez des balises DMARC supplémentaires (`sp` pour la politique de sous-domaine, `pct` pour le pourcentage, `rua` et `ruf` pour les adresses de rapport).

1. Si vous utilisez Délégation complète, cliquez sur **[!UICONTROL Enregistrer]**.

   Adobe applique automatiquement l’enregistrement. Si vous utilisez CNAME, copiez l’enregistrement DNS et demandez à votre équipe DNS de l’ajouter, puis confirmez-le dans [!DNL Journey Optimizer B2B Edition] Prime.

1. Patientez jusqu’à 48 heures pour la propagation DNS, puis vérifiez que l’indicateur de statut DMARC sur la page du sous-domaine est vert/sain.

>[!TIP]
>
>Commencez par `policy=none` pour surveiller les rapports d’authentification, puis passez à `quarantine` et enfin à `reject` une fois que vos rapports affichent un alignement SPF et DKIM sain. Le passage direct à `reject` sans surveillance peut entraîner le rejet d’e-mails légitimes.

## Groupes d’adresses IP {#ip-pools}

Un groupe d’adresses IP est un groupe nommé d’adresses IP utilisées pour envoyer votre e-mail. Les pools d&#39;adresses IP sont essentiels pour la réputation de l&#39;expéditeur : chaque pool a sa propre réputation auprès des FAI, de sorte qu&#39;un problème lié à un pool (par exemple, une rafale marketing qui déclenche des plaintes contre le spam) n&#39;en contamine pas un autre (par exemple, des confirmations transactionnelles).

### Types de pool

| Type de pool | Disponibilité | Description |
| --------- | ------------ | ----------- |
| **Groupe d’adresses IP partagées** | Disponible sur Alpha | Groupe d’adresses IP gérées par Adobe et partagées par de nombreux clients. La réputation est préservée par Adobe dans le pool. Idéal pour les e-mails de faible à moyen volume et les clients qui ne souhaitent pas gérer le préchauffage d’adresses IP. |
| **Groupe d’adresses IP dédié** | Feuille de route (GA) | Une ou plusieurs adresses IP attribuées exclusivement à votre organisation. La réputation t&#39;appartient. Recommandé pour les expéditeurs et expéditrices à volume élevé. Inclut la planification du réchauffement des adresses IP et la gestion des enregistrements PTR. |

### Vérification et affectation d’un groupe d’adresses IP {#review-ip-pool}

Dans cette version, les groupes d’adresses IP sont préconfigurés pour votre organisation. Vous attribuez un groupe d’adresses IP lors de la création d’une configuration de canal e-mail.

1. Accédez à **[!UICONTROL Administration]** → **[!UICONTROL Canaux]** → **[!UICONTROL Paramètres d’e-mail]** → **[!UICONTROL Groupes d’adresses IP]**.
1. Vérifiez qu’un groupe d’adresses IP avec le statut **[!UICONTROL Actif]** est disponible pour votre organisation.
1. Passez la souris sur le pool pour afficher les adresses IP et leurs enregistrements PTR (DNS inversé).
1. Si votre organisation compte plusieurs unités commerciales ou marques, planifiez l’utilisation des pools d’adresses IP (par exemple, pool marketing ou pool de webinaires) avant de créer des configurations de canal.

>[!IMPORTANT]
>
>Ne mélangez pas le trafic marketing et transactionnel sur le même groupe d’adresses IP, même si le groupe partagé est disponible. Le paramètre Type d’e-mail sur la configuration du canal (Marketing par rapport à Transactionnel) régit le comportement de suppression, mais vos configurations de canal doivent toujours utiliser des pools distincts dans la mesure du possible.

## Configurations du canal e-mail {#email-channel-configurations}

Une configuration de canal est l’objet central qui lie votre identité d’expéditeur, votre sous-domaine, votre groupe d’adresses IP et vos paramètres de suivi. Les actions d’e-mail dans les parcours font référence à une configuration de canal pour savoir comment envoyer le message :

* **Canal:** E-mail.
* **Type d’e-mail :** marketing ou transactionnel. Ce paramètre détermine si des règles de suppression s’appliquent (Marketing les applique ; Transactionnel contourne par défaut la suppression des plaintes pour spam pour les messages transactionnels légitimes).
* **Paramètres d’en-tête :** Nom de l’expéditeur, Adresse électronique de l’expéditeur, Nom de la personne à laquelle répondre, Adresse électronique de la personne à laquelle répondre, Adresse électronique d’erreur.
* **Sous-domaine :** sous-domaine délégué utilisé pour l’envoi. L’e-mail de l’expéditeur doit utiliser ce sous-domaine.
* **Groupe d’adresses IP :** groupe d’adresses IP utilisé pour diffuser le message.
* **Tracking des URL :** activer ou désactiver le tracking des clics et des ouvertures ; configurer le domaine de tracking.
* **Balises :** balises pour l’organisation et la recherche.

### Créer une configuration de canal e-mail {#create-email-channel-configuration}

>[!PREREQUISITES]
>
>* Au moins un sous-domaine doit être délégué et actif.
>* Au moins un groupe d’adresses IP doit être affecté à votre organisation.
>* Vous avez besoin du rôle Administrateur.

1. Accédez à **[!UICONTROL Canaux]** → **[!UICONTROL Paramètres généraux]** → **[!UICONTROL Configurations de canal]**.
1. Cliquez sur **[!UICONTROL Créer une configuration de canal]**.
1. Saisissez un Nom (par exemple, « Marketing B2B Contoso - Amérique du Nord ») et une Description facultative.
1. Sélectionnez le canal **[!UICONTROL e-mail]**.
1. Vous pouvez éventuellement sélectionner des balises pour catégoriser la configuration.
1. Dans la section **[!UICONTROL Type d’e-mail]**, choisissez Marketing ou Transactionnel.
1. Dans la section **[!UICONTROL Sous-domaine]**, sélectionnez un sous-domaine précédemment délégué.
1. Dans la section **[!UICONTROL Groupe d’adresses IP]**, sélectionnez un groupe d’adresses IP actives. Vous pouvez pointer sur les adresses IP pour afficher les enregistrements PTR.
1. Configurez les **[!UICONTROL paramètres d’en-tête]** :
   * Nom de l’expéditeur (par exemple, « Marketing Contoso »).
   * E-mail de l&#39;expéditeur — doit utiliser le sous-domaine sélectionné (par exemple, `marketing@mail.contoso.com`).
   * Nom de la réponse et Adresse électronique de la réponse : si ce champ est vide, la valeur par défaut est De.
   * E-mail d&#39;erreur : adresse qui reçoit les notifications de non-diffusion.
1. Activez le **[!UICONTROL tracking des URL]** et sélectionnez le domaine de tracking.
1. Cliquez sur **[!UICONTROL Envoyer]**.
1. Validation des exécutions de Prime : statut du sous-domaine, enregistrement MX, alignement SPF/DKIM/DMARC, préparation du groupe d’adresses IP, enregistrement FBL. La configuration passe par le statut Brouillon → Traitement → actif.

>[!NOTE]
>
>Si la validation échoue, la configuration passe au statut **[!UICONTROL Échec]**. Ouvrez la configuration pour afficher la raison de l’échec : les causes courantes sont l’échec de la validation des enregistrements MX, des adresses IP du pool ne correspondant pas à la configuration ou un mauvais alignement du DMARC. Résoudre et renvoyer.

### Modification ou suppression d’une configuration de canal {#edit-channel-configuration}

Vous pouvez modifier les configurations de canal après leur création, mais avec une contrainte importante :

* **Le canal ne peut pas être modifié.** Une configuration est liée à son canal .

Lorsque vous modifiez une configuration en cours d’utilisation :

* **Pour les parcours publiés :** la modification est appliquée à la prochaine périodicité ou à la prochaine exécution. Les exécutions en cours se poursuivent avec les paramètres précédents.
* **Pour les messages transactionnels ou en temps réel :** modifications se propagent en cinq minutes environ.

Pour supprimer une configuration, supprimez ou mettez à jour chaque action d’e-mail qui y fait référence. [!DNL Journey Optimizer B2B Edition] Prime ne supprime pas une configuration actuellement utilisée par un parcours actif.

### Configurations de plusieurs canaux {#multiple-channel-configurations}

La plupart des entreprises B2B utilisent plusieurs configurations de canal pour séparer les marques, les régions ou les types d’envoi. Modèles courants :

* Une configuration marketing distincte par unité opérationnelle (par exemple, *Marketing BU-A*, *Marketing BU-B*).
* Une configuration transactionnelle dédiée avec Type d’e-mail = Transactionnel pour les notifications de produit ou de contrat.
* Configurations spécifiques à une région utilisant des sous-domaines spécifiques à une région (par exemple, `mail.eu.contoso.com`, `mail.us.contoso.com`) pour s’aligner sur les FAI régionaux et la conformité.

>[!TIP]
>
>Nommez vos configurations selon une convention claire et structurée, par exemple : *[Marque] - [Région] - [Type]*. Cela devient critique une fois que vous disposez d’une douzaine de configurations ou plus.

### Limites connues {#known-limitations}

* **Méthode de délégation personnalisée** pour la délégation de sous-domaine, n’est pas encore disponible — utilisez Fully Delegated ou CNAME. La délégation personnalisée est destinée à la disponibilité générale.
* **Les pools d&#39;adresses IP dédiés** ne sont pas disponibles dans Alpha. Le pool d’adresses IP partagées est la seule option. Les adresses IP dédiées sont livrées à GA, y compris la planification du préchauffage des adresses IP et la gestion des enregistrements PTR.
* L’importation de **HTML par chargement .html ou .zip** est limitée dans Alpha. L’importation complète d’HTML (y compris l’éditeur de code + la zone de travail visuelle avec un affichage double, la validation et la conversion automatique CSS en ligne) est fournie sous Beta.
* **Le chargement d’images natives et la gestion des ressources numériques dans Prime** (chargement, organisation, modification) figurent sur la feuille de route de Beta. Utilisez les ressources de Marketo Design Studio dans cette version. Les rechargements dans Marketo ne sont pas répercutés dans Prime.
* **Les profils de test, Simuler du contenu et Envoyer un BAT** ne sont pas disponibles dans cette version. Le rendu Litmus et les rapports de spam basés sur SpamAssassin figurent sur la feuille de route de Beta.
* **La personnalisation au niveau du compte et les données d’objet personnalisé** ne sont pas disponibles dans cette version. Utilisez les attributs de profil.
* **La migration automatisée Velocity-to-Handlebars** des modèles Marketo existants est fournie en disponibilité générale.
* **Les commentaires et la collaboration sur les e-mails** (commentaires intégrés, @mentions, workflow de demande-révision) sont fournis dans la version de suivi rapide.
* **Les intégrations d’AEM Assets, des fragments de contenu AEM et d’Adobe Express** sont sur la feuille de route du suivi rapide.

<!--

### Frequently asked questions {#faq}

| Question | Answer |
| -------- | ------ |
| **Can I reuse the subdomain I already use in Marketo Engage?** | No. A subdomain can only be associated with one Adobe product at a time. Create a new subdomain (for example, mail2.contoso.com) for Prime. |
| **Why does my channel configuration show Failed?** | The most common reasons are: MX record validation failed (your subdomain DNS isn't fully configured); DMARC misalignment; or an IP pool that is in Processing and has never been associated with the selected subdomain. Open the configuration to see the specific reason. |
| **What happens if a personalization token has no value at send time?** | If you defined a fallback with the Handlebars `default` helper, the fallback is used. If not, the token resolves to an empty string. Prime warns you when a token has no fallback and the underlying attribute is not guaranteed by the audience definition. |
| **Can I personalize using account-level attributes?** | Not in this release. Personalization in Prime today supports profile attributes only. |
| **What's the maximum email size?** | 100 KB is the recommended best-practice cap for inbox rendering. Prime warns you in the editor if you exceed it. |
| **Can I migrate existing Marketo email templates into Prime?** | A guided self-serve migration tool — including Velocity-to-Handlebars conversion — is delivered at GA. In this release, you can manually rebuild templates or paste raw HTML. |
| **Will my updates to Marketo assets show up in Prime?** | No. Asset availability in Prime is based on a one-time copy from Marketo Design Studio. Re-uploaded or modified Marketo assets are not reflected in Prime today. Native asset upload and management within Prime is on the Beta roadmap. |

## Glossary {#glossary}

| Term | Definition |
| ---- | ---------- |
| **DKIM** | DomainKeys Identified Mail — cryptographic email signature. |
| **DMARC** | Domain-based Message Authentication, Reporting & Conformance. |
| **FBL** | Feedback Loop — a service ISPs offer to receive spam-complaint reports back to senders. |
| **Handlebars** | JavaScript templating language used in Prime for personalization expressions. |
| **IP pool** | Group of IP addresses used to send email. |
| **MX record** | Mail Exchange DNS record — directs incoming mail to the correct mail servers. |
| **NS record** | Name Server DNS record — used to delegate a subdomain. |
| **PTR record** | Pointer record — reverse DNS that maps an IP address back to a hostname. |
| **RBAC** | Role-Based Access Control. |
| **SPF** | Sender Policy Framework — DNS record listing authorized sending IPs. |
| **Subdomain delegation** | Granting Adobe authority over a portion of your domain (a subdomain) for sending email. |

-->
