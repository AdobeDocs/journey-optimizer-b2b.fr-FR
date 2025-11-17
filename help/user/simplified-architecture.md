---
title: Configuration de l’architecture simplifiée
description: Configurez Journey Optimizer B2B edition sur l’architecture simplifiée. Configurez les schémas XDM, les canaux e-mail/SMS, les actions de parcours Marketo Engage et les utilisateurs et utilisatrices.
feature: Setup, Administration
role: Admin, Data Engineer
hide: true
hidefromtoc: true
source-git-commit: 3f91b2cc92a1ce42d2c62dcfe7eb9de332116023
workflow-type: tm+mt
source-wordcount: '1385'
ht-degree: 7%

---

# Configuration de l’architecture simplifiée

Adobe Journey Optimizer B2B Edition est désormais disponible avec une architecture simplifiée. Grâce à cette architecture mise à jour, Journey Optimizer B2B Edition et Marketo Engage ne sont plus sur le même système et le même magasin de données. Journey Optimizer B2B Edition reçoit des données uniquement d’Adobe Experience Platform. Cependant, il continue de dépendre des droits Marketo Engage et de certaines fonctionnalités de configuration pour approvisionner et configurer le système.

L’architecture simplifiée est la base qui débloque de nouvelles fonctionnalités dans Adobe Journey Optimizer B2B edition :

* **Unifiez et mettez à l’échelle facilement vos données :** la nouvelle plateforme prend en charge des modèles de données complexes, notamment des objets personnalisés, des groupes d’achats et des événements de compte. 

* **Connecter plusieurs instances Adobe Marketo Engage :** gérez et unifiez les données de plusieurs environnements Adobe Marketo Engage en un seul endroit.

* **Protection des données :** fonctionnalités avancées de confidentialité et de sécurité qui permettent de protéger les informations de vos clients. (_Bientôt disponible_)

* **Conçu pour l’avenir :** cette mise à niveau vous permet de bénéficier d’améliorations et d’innovations continues. 

Pour les environnements configurés pour cette architecture, suivez les instructions de configuration suivantes.

## Espaces de noms et schéma

Consultez Espaces de noms et schémas [B2B](https://experienceleague.adobe.com/fr/docs/experience-platform/sources/connectors/adobe-applications/marketo/marketo-namespaces) dans la documentation d’Experience Platform pour une présentation.

### Configuration de l’environnement

Configurez un environnement Postman pour prendre en charge l’utilitaire de génération automatique de schémas et d’espaces de noms B2B.

* Vous pouvez télécharger l’environnement et la collection de l’utilitaire de génération automatique de schémas et d’espaces de noms à partir du [référentiel GitHub](https://github.com/adobe/experience-platform-postman-samples/tree/master/Postman%20Collections/CDP%20Namespaces%20and%20Schemas%20Utility).

* Pour plus d’informations sur l’utilisation des API Experience Platform, notamment sur la manière de collecter les valeurs des en-têtes requis et de lire des exemples d’appels d’API, consultez le guide [Prise en main des API Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/landing/platform-apis/api-guide).

* Pour plus d’informations sur la génération de vos informations d’identification pour les API Experience Platform, consultez le tutoriel sur l’[authentification et accès aux API Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/landing/platform-apis/api-authentication).

* Pour plus d’informations sur la configuration de Postman pour les API Experience Platform, consultez les étapes détaillées dans [Postman sous Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/landing/platform-apis/postman).

Grâce à la console de développement Experience Platform et à la configuration de Postman, vous pouvez maintenant commencer à appliquer les valeurs d’environnement appropriées à votre environnement Postman.

### Exécution des scripts

Avec la configuration de votre collection Postman et de votre environnement, vous pouvez exécuter le script via l’interface Postman.

Dans l’interface de Postman, sélectionnez le dossier racine de l’utilitaire de génération automatique, puis sélectionnez **Exécuter** dans l’en-tête supérieur.

Lorsque l’interface de Runner s’affiche, assurez-vous que toutes les cases à cocher sont sélectionnées, puis sélectionnez **Exécuter l’utilitaire d’auto-génération de schémas et d’espaces de noms**.

Une requête réussie crée les espaces de noms et les schémas requis pour B2B.

## Sélection de champ XDM

Vous pouvez gérer les champs XDM disponibles dans l’ensemble de l’application dans l’interface utilisateur de Journey Optimizer B2B edition. Ces champs permettent de rationaliser votre instance en n’exposant que les champs pertinents pour la création de **_parcours_**, de **_groupes d’achat_** ou de **_personnalisations d’e-mail_**.

### Classes XDM

#### Classes standard

Suivez les étapes ci-dessous pour définir des champs pour les classes XDM standard :

1. Accédez à **[!UICONTROL Administration &#x200B;] > [!UICONTROL &#x200B; Configurations]**.

1. Dans le panneau de navigation, sélectionnez **[!UICONTROL Classes XDM]**.

1. Sélectionnez l’onglet **[!UICONTROL Standard]** pour afficher les classes XDM disponibles :

   * Profil individuel XDM

   * Compte professionnel XDM

#### Champs gérés

Définissez les champs disponibles dans l’ensemble de l’application.

1. Cliquez sur l’icône _Plus de menu_ (**...**) et sélectionnez **[!UICONTROL Modifier les champs gérés]**.

1. Consultez la liste des champs disponibles (cliquez sur l’icône _Informations_ pour les métadonnées de champ).

1. Sélectionnez les champs à inclure et effacez les sélections pour les champs dont vous n’avez pas besoin.

1. Utilisez le curseur **[!UICONTROL Afficher uniquement les champs sélectionnés]** pour passer en revue vos sélections.

1. Cliquez sur **[!UICONTROL Enregistrer]**

#### Champs modifiables

Choisissez les champs qui peuvent être modifiés par le biais d’actions de parcours **[!UICONTROL Mettre à jour le profil de compte]** ou **[!UICONTROL Mettre à jour le profil de personne]**.

1. Cliquez sur l’icône _Plus de menu_ (**...**) et sélectionnez **[!UICONTROL Modifier les champs modifiables]**.

1. Sélectionnez **[!UICONTROL Schéma]** puis **[!UICONTROL Jeu de données]**.

   Ces schémas et jeux de données sont fournis par votre organisation.

1. Consultez la liste des champs pouvant être mis à jour (cliquez sur l’icône _Informations_ pour les métadonnées).

   Seuls les champs gérés sont modifiables.

1. Sélectionnez les champs que vous souhaitez rendre disponibles pour mise à jour à partir des parcours.

1. Cliquez sur **Enregistrer**.

### Schémas relationnels

Sélectionnez [schémas relationnels](https://experienceleague.adobe.com/fr/docs/experience-platform/xdm/schema/relational) à utiliser dans la **_prise de décision de parcours_** et **_personnalisation_**. Actuellement, ces schémas sont destinés aux cas d’utilisation d’objets personnalisés. À l’avenir, les schémas relationnels pourront également être utilisés pour d’autres cas d’utilisation d’objets.

1. Sélectionnez l’onglet **[!UICONTROL Relationnel]**.

1. Cliquez sur **[!UICONTROL Sélectionner la classe XDM relationnelle]**.

   Actuellement, seul l’objet personnalisé plusieurs-à-un du compte est pris en charge.

1. Consultez la liste des champs de schéma (cliquez sur l’icône _informations_ pour afficher les métadonnées).

1. Sélectionnez les champs à inclure.

1. Utilisez le curseur **[!UICONTROL Afficher uniquement les champs sélectionnés]** pour passer en revue vos sélections.

1. Cliquez sur **[!UICONTROL Enregistrer]**

>[!NOTE]
>
>Notez que les schémas relationnels doivent avoir les configurations suivantes :
>
><li>Comportement : enregistrement
>&gt; <li>Segmentation : activée
>&gt; <li>Type de relation : plusieurs à un
>&gt; <li>Schéma de référence : <a href="https://experienceleague.adobe.com/fr/docs/platform-learn/tutorials/schemas/create-schemas-for-b2b-data">Compte B2B - Schéma de compte professionnel XDM</a>
>&gt; <li>Champs obligatoires : clé de Principal, clé étrangère et descripteur de version
>&gt; <li>Jeu de données associé : défini et mappé au schéma

### Événements

Sélectionnez les événements d&#39;expérience à utiliser dans la prise de décision de parcours **__**.

1. Sélectionnez l’onglet **[!UICONTROL Événements]**.

1. Cliquez sur **[!UICONTROL Sélectionner un événement d’expérience]**.

1. Cliquez sur **[!UICONTROL Sélectionner le type d’événement]**, choisissez le type d’événement, puis cliquez sur **[!UICONTROL Sélectionner]**.

1. Cliquez sur **[!UICONTROL Sélectionner les champs]**, choisissez les champs dont vous avez besoin, puis cliquez sur **[!UICONTROL Sélectionner]**.

1. Cliquez sur **[!UICONTROL Enregistrer]**

## Configuration du canal e-mail

Les éléments suivants doivent être configurés pour envoyer des e-mails en dehors de Journey Optimizer B2B edition.  

[https://experienceleague.adobe.com/fr/docs/journey-optimizer-b2b/user/get-started/email-protocols](https://experienceleague.adobe.com/fr/docs/journey-optimizer-b2b/user/get-started/email-protocols)

### Protocoles de tracking et de diffusion des e-mails

1. [Créer des enregistrements DNS pour l’e-mail](https://experienceleague.adobe.com/fr/docs/journey-optimizer-b2b/user/get-started/email-protocols#create-dns-records-for-landing-pages-and-email)

1. [Configurer SPF et DKIM](https://experienceleague.adobe.com/fr/docs/journey-optimizer-b2b/user/get-started/email-protocols#set-up-spf-and-dkim)

1. [Configurer DMARC](https://experienceleague.adobe.com/fr/docs/journey-optimizer-b2b/user/get-started/email-protocols#set-up-dmarc)

1. [Configurer des enregistrements MX pour votre domaine](https://experienceleague.adobe.com/fr/docs/journey-optimizer-b2b/user/get-started/email-protocols#set-up-mx-records-for-your-domain)

1. [Ajouter des adresses IP sortantes aux places sur la liste autorisée &#x200B;](https://experienceleague.adobe.com/fr/docs/journey-optimizer-b2b/user/get-started/email-protocols#outbound-ip-addresses)

1. Si vous devez partager le pool d’adresses IP dédié, contactez l’équipe en charge de la délivrabilité pour en savoir plus sur la faisabilité et la configuration assistée.

### Configurations du canal e-mail

Dans l’architecture simplifiée, les paramètres d’e-mail sont configurés à partir de l’interface utilisateur de Marketo Engage. Suivez les étapes de configuration liées à l’e-mail : [https://experienceleague.adobe.com/fr/docs/marketo/using/getting-started/initial-setup/setup-steps](https://experienceleague.adobe.com/fr/docs/marketo/using/getting-started/initial-setup/setup-steps)

[https://experienceleague.adobe.com/fr/docs/journey-optimizer-b2b/user/admin/channels/configure-channels-emails](https://experienceleague.adobe.com/fr/docs/journey-optimizer-b2b/user/admin/channels/configure-channels-emails)

### Limites de communication

1. Dans le volet de navigation de gauche, choisissez **[!UICONTROL Administration]** > **[!UICONTROL Canaux]**.

1. Dans le panneau de navigation, sélectionnez **[!UICONTROL Limite de communication]**.

1. Créez un ensemble de règles de limite de communication globale (cet ensemble de règles est créé par défaut dans chaque instance Journey Optimizer B2B edition).

   Il n’existe aucune limite de communication si l’ensemble de règles global n’est pas créé.

<!-- In the future, you can also add local communication limit rule sets (AJO B2C doc can be found here [https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets](https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets). We may need a small update for our B2B version.) -->

### Limites de communication partagées

Dans la nouvelle architecture, Journey Optimizer B2B edition et Marketo Engage disposent par défaut de limites de communication indépendantes.

Si vous souhaitez que l’instance Marketo Engage partage la limite de communication définie dans l’instance Journey Optimizer B2B edition, contactez l’assistance Adobe pour obtenir de l’aide sur la configuration ou ouvrez un ticket d’assistance. Sur demande, l’équipe d’ingénieurs peut activer le partage des limites de communication entre Journey Optimizer B2B edition et une ou plusieurs instances Marketo Engage.

Actuellement, la limite de communication partagée dans l’instance Marketo Engage doit être configurée par le biais d’un appel API.

Par exemple, lorsque :

* Le munchkinId de l’instance Journey Optimizer B2B edition est `JKL-567-MNO`.
* Le munchkinId de l’instance Marketo Engage est `ABC-123-DEF` et se trouve dans le centre de données SJ

La requête d’API doit ressembler à ce qui suit :

```
curl --location --request POST 'http://sjrest2a.marketo.org/rest/v1/fm.json?_munchkinId=ABC-123-DEF&featureName=Mktmail%20Config&paramName=ajoB2bMappingMunchkinId&dataType=string&value=JKL-567-MNO'
```

## Configuration du canal SMS

Voir [_Configurations SMS_](https://experienceleague.adobe.com/fr/docs/journey-optimizer-b2b/user/admin/channels/configure-channels-sms) pour plus d’informations.

## Actions de Marketo Engage à partir des parcours

Vous pouvez configurer une ou plusieurs instances distantes **_Marketo Engage_** à utiliser avec les actions de parcours suivantes :

* Ajouter à la liste Marketo
* Supprimer de la liste Marketo
* Ajouter à la campagne de demande Marketo

Procédez comme suit pour configurer ces connexions :

1. Accédez à **[!UICONTROL Administration &#x200B;] > [!UICONTROL &#x200B; Configurations]**.

1. Dans le panneau de navigation, sélectionnez **[!UICONTROL Classes XDM]**.

1. Sélectionnez l’onglet **[!UICONTROL Intégrations]**.

1. Cliquez sur **[!UICONTROL Créer une connexion]**.

1. Saisissez les **[!UICONTROL Nom]** et **[!UICONTROL Description]**.

1. Sélectionnez **[!UICONTROL Mettre à jour la politique]** pour mettre en correspondance les enregistrements de personne.

1. Saisissez **[!UICONTROL Munchkin ID]**, **[!UICONTROL ID client]**, **[!UICONTROL Secret client]**, puis cliquez sur **[!UICONTROL Se connecter à Marketo]**.

1. Cliquez sur **[!UICONTROL Créer]**.

## Intégration des utilisateurs

Consultez la page [Gestion des utilisateurs](https://experienceleague.adobe.com/fr/docs/journey-optimizer-b2b/user/admin/user-management) pour obtenir un aperçu.

### Groupes d’utilisateurs existants

Si tous les utilisateurs Journey Optimizer B2B edition existants doivent accéder à la nouvelle architecture, utilisez le groupe d’utilisateurs Journey Optimizer B2B edition existant. Un administrateur système ou un administrateur de produit peut effectuer les étapes suivantes.

1. Créez un profil de produit dans le Marketo Engage dédié.

1. Ajoutez un groupe d’utilisateurs existant au profil de produit créé.

Les profils accordent tous les rôles et autorisations déjà attribués à ce groupe d’utilisateurs, qui doit déjà être configuré pour que les utilisateurs puissent accéder à Journey Optimizer B2B edition. Si seul un sous-ensemble d’utilisateurs doit accéder à la nouvelle architecture, effectuez les étapes décrites ci-dessous. Pour plus d’informations, consultez la [documentation actuelle](https://experienceleague.adobe.com/fr/docs/journey-optimizer-b2b/user/admin/user-management).

### Créer un groupe d’utilisateurs

1. Créez un profil de produit dans l’instance Marketo Engage dédiée.
1. Créez un groupe d’utilisateurs pour les nouveaux utilisateurs.
1. Sélectionnez et affectez les profils de produit requis au groupe d’utilisateurs :

   * Profil Marketo Engage créé
   * Profils Adobe Experience Platform
      * AEP-Default-All-Users
      * Collecte de données dʼAdobe Experience Platform
      * Accès complet à la collecte de données

1. Ajoutez les utilisateurs au groupe d’utilisateurs .
1. Ajoutez un nouveau groupe d’utilisateurs aux rôles de Journey Optimizer B2B edition dans Experience Platform.
