---
title: Compétences en audience pour les comptes B2B et les personnes
description: Découvrez les compétences en matière d’audience pour les comptes et les personnes B2B. Explorez l'intention du produit, identifiez les personnes, évaluez la couverture des rôles et créez des modèles de groupe d'achats.
feature: Agentic AI, Audiences
role: User
exl-id: c1210912-66ba-4b5f-8f3b-96eb6280c926
autotag-review: '2026-06-05T16:43:42.459Z'
TQID: 'https://experienceleague.adobe.com/d7KMYbH0NpoYGnBdTCmCpzLgpGIYfNP-YIFCQUjZpIg'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: afadf741-c5fe-42cd-8013-23bb6ff2d1bc
    internal-label: Buying Groups
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
  - id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
    internal-label: AI Assistant
subfeature_v2:
  - id: ff10f619-348f-47e3-99bf-3ce4c817cf2c
    internal-label: Agentic AI
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
    internal-label: Artificial intelligence
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: f8667931-f646-4dd3-af2a-b9d0cb8098ad
    internal-label: Taxonomy
source-git-commit: ce5504e7a539c38b489fddc103358029edf1cfba
workflow-type: tm+mt
source-wordcount: '1692'
ht-degree: 1%
---
# Compétences en audience pour les comptes et les personnes B2B

Utilisation des compétences d’audience pour B2B dans l’interface [!DNL CX Coworker]. Explorez l’intention du produit sur plusieurs comptes et personnes. Identifiez les personnes pertinentes, évaluez la couverture du groupe d&#39;achat et créez des modèles de rôles pour le groupe d&#39;achat.

* Évaluez l’intérêt du compte pour des produits spécifiques et comparez les tendances d’intention.
* Identifier les personnes et les rôles associés à l’intérêt du produit.
* Examinez les rôles des groupes d&#39;achat et cernez les lacunes en matière de couverture.
* Générer et affiner des modèles de rôle de groupe d&#39;achat.

>[!PREREQUISITES]
>
>Avant d’utiliser les compétences d’audience pour les comptes et les personnes B2B, configurez les définitions et mappages de données suivants :
>
>* [Taxonomie et mappage des données intentionnelles](../admin/intent-data.md)
>* [Mappage de champs XDM](#xdm-data-prerequisites)

Cliquez sur l’icône _Demander le[!DNL Coworker]_ ( ![Demander le [!DNL Coworker]](../assets/do-not-localize/icon-ask-coworker.svg) ) en haut de l’application pour ouvrir l’application [!DNL Coworker]. Entrez votre invite en langage naturel dans l&#39;interface de chat.

![Invite d’audience dans [!DNL CX Coworker]](./assets/audience-skills-prompt.png){width="800" zoomable="yes"}

## Compétences des audiences dans les domaines prioritaires

Utilisez les domaines de compétence d’audience pour explorer l’intention du compte, comprendre les personnes et les rôles et préparer des modèles de groupes d’achats.

| Focus | Tâches |
| ----- | ----- |
| Intention du compte | Évaluez l’intention de compte pour des produits spécifiques à l’aide des niveaux d’intention faible, moyen et élevé. Comparez les tendances des intérêts des produits au fil du temps et identifiez les comptes présentant un intérêt pour des produits spécifiques. Examinez les modèles d’engagement ainsi que la couverture personnelle. |
| Personnes et personnages | Identifier et classer les utilisateurs par intention de produit pour un ou plusieurs produits. Examinez les mesures de l’opportunité, y compris le taux de succès, le taux d’abonnement et le nombre. Mappez les personnages à des rôles tels que _Champion_, _Décideur_ et _Influenceur_, et examinez les explications pour l’attribution des rôles. |
| Couverture du groupe d&#39;achat | Évaluez la taille du groupe d&#39;achat et la couverture personnelle sur tous les comptes. Examinez la répartition des rôles et identifiez les rôles ou les personnes manquants. Trouvez des comptes avec des champions identifiés dans les offres récentes. |
| Modèles de groupe d&#39;achat | Générer des modèles de rôle de groupe d&#39;achat pour des produits spécifiques et passer en revue les mappages de personnages recommandés. Affinez les modèles en incluant ou en excluant les rôles et les rôles. Validez les rôles requis avant de créer des groupes d&#39;achats. |

## Limites

Les informations sur les audiences dépendent de la taxonomie d’intention configurée, des mappages de champs XDM et des données d’événement d’expérience. Des données d’opportunité incomplètes, une taxonomie manquante ou obsolète, ou des identifiants de profil et de compte manquants peuvent réduire la fiabilité d’insight.

Le calcul de l’intention utilise uniquement ces événements d’expérience : `directMarketing.emailClicked`, `directMarketing.emailOpened`, `directMarketing.emailUnsubscribed` et `web.webpagedetails.pageViews`.

## Exemples de prompts

Saisissez les invites suivantes dans l&#39;interface [!DNL CX Coworker] pour explorer l&#39;intention du compte, comprendre les personnes et les rôles et préparer les modèles de groupe d&#39;achats.

### Intention du compte

Explorez l’intérêt du compte pour les produits et passez en revue les modifications d’intention.

* Afficher la fenêtre de tendance : premières et dernières mises à jour de l’intention du produit du compte par produit.
* Quels comptes ont une faible intention pour un produit, mais ont toujours des opportunités ouvertes (qui valent la peine d’être encouragées) ?
* Quels nouveaux signaux d&#39;intention ont été enregistrés pour `<account_name>` cette semaine ?

### Personnes et personnages

Identifiez les personnes associées à l&#39;intérêt du produit et passez en revue les rôles de groupe d&#39;achat recommandés.

* Montrez-moi les personnes associées à `<product>`.
* Me montrer la recommandation de mappage de rôle à persona pour `<product>`.
* Par `<product>`, répertoriez les rôles et les rôles avec leurs mesures d’opportunité (taux de succès, taux d’abonnement, nombres).

### Groupes d&#39;achat et modèles

Vérifiez l&#39;intention et la couverture du groupe d&#39;achat, puis générez ou affinez des modèles.

* Par `<product>`, répertoriez les groupes d’achats avec l’intention du produit et les scores.
* Pour les comptes en `<industry>`, quelle est la couverture moyenne du profil de compte pour `<product>` ?
* Créez un modèle de groupe d&#39;achats pour `<product>`.
* Créez un modèle de groupe d&#39;achats pour les `<product>` sans le rôle `<persona>` et supprimez le rôle `<role>`.

## Concepts

Utilisez ces concepts pour interpréter l’intention du compte, les classements des personas et les recommandations des groupes d’achat.

| Concept | Explication |
| ------- | ----------- |
| Détection d’audience | Analysez les signaux d’engagement propriétaires sur les personnes d’un compte afin d’identifier l’intérêt du produit et les personnes pertinentes. L’analyse prend en compte les 18 mois d’activité précédents, y compris l’activité avant la fermeture de l’opportunité. Les modèles d’engagement peuvent indiquer l’intention du produit lorsque les données d’opportunité sont incomplètes, mais les données manquantes peuvent réduire la fiabilité d’insight. |
| Persona | Les personas regroupent les gens selon leur fonction, fonction et ancienneté normalisées. Utilisez les personnes pour comprendre qui s’engage dans un compte, y compris les décideurs, les influenceurs et les rôles de support. |
| Mapping des rôles de groupes d&#39;achat | Mappez les rôles aux rôles des groupes d’achats spécifiques aux produits en fonction du titre de la fonction, de l’ancienneté et des attributs configurés. Ces rôles représentent les personnes au sein d’un compte qui influencent ou décident d’un achat. Examinez la couverture pour identifier les rôles manquants. |
| Données d’opportunité pour le classement des personas | L’étape de l’opportunité, la date de fermeture et les mappages opportunité-produit prennent en charge le classement personnel pour chaque produit. Lorsque les données d’opportunité sont incomplètes, le classement utilise le volume d’activité et la décroissance temporelle pour donner plus de poids à l’activité récente.<br/><br/>La liaison de produits utilise un tableau de correspondance opportunité-produit fourni ou généré, le cas échéant. Dans le cas contraire, les correspondances approximatives relient les opportunités aux produits. Si aucun lien n’est disponible, l’intention du produit est déduite de l’activité récente avant la date de fermeture de l’opportunité. Ces méthodes de secours n’éliminent pas les limites de fiabilité des données incomplètes. |
| Analyse des opportunités | L’analyse historique des opportunités utilise trois dimensions pour identifier les modèles de persona associés aux résultats d’achat :<ul><li>Taux de réussite : mesure la fréquence à laquelle des opportunités sont gagnées lorsque des personnes spécifiques sont impliquées. Les profils personnels associés à des taux de gain plus élevés reçoivent plus de poids.</li><li>Taux d’adhésion : mesure la fréquence à laquelle une personne apparaît dans les opportunités d’un produit donné.</li><li>Influence personnelle : mesure la façon dont l’engagement ou l’activité personnel est corrélé aux gains, au-delà de la présence du persona.</li></ul>Ces signaux renseignent sur l’intention du compte, le mappage des rôles et les recommandations des groupes d’achat. |
| Intention | L’intention indique l’intérêt du produit par l’engagement, comme les visites de page web ou les clics sur les liens des e-mails. La taxonomie du produit connecte l’activité d’engagement aux mots-clés, aux produits et aux catégories de produits. La profondeur et la fréquence de l’engagement déterminent les scores d’intention individuels pour chaque mot-clé, produit ou catégorie de produits.<br/><br/>Les scores indiquent la force d’intérêt : intention faible : `<=0.2`, intention de Medium : `0.2 < score <= 0.6`, intention élevée : `0.6 < score <= 1`.<br/><br/>Les scores d’intention individuels sont agrégés entre les personnes d’un même compte afin de déterminer l’intention du compte. |
| Rôles qui influencent un groupe d&#39;achat | Les rôles de groupe d’achat représentent différentes contributions à une décision d’achat. _Décideurs_ contrôlez généralement les approbations de budget. _Influenceurs_ façonnez l’évaluation et les recommandations. _Champions_ construisez un consensus interne. _Utilisateurs finaux_ valider l’adéquation du produit.<br/><br/>Examinez les affectations et la couverture des rôles pour comprendre qui influence la décision et où subsistent des lacunes en matière d’engagement. |
| Couverture des rôles ou des rôles | La couverture mesure le nombre de personnes ou de rôles attendus ayant au moins un représentant au sein d’un compte. Pour un produit avec _N_ rôles ou rôles attendus, une couverture complète signifie que tous les _N_ sont représentés. Une couverture partielle signifie que certains sont absents. Utilisez la couverture pour évaluer l&#39;exhaustivité du groupe d&#39;achat et identifier les lacunes. |

## Conditions préalables relatives aux données XDM

Configurez les mappages de champs XDM suivants pour prendre en charge l’analyse des intentions de compte, l’identification des personnes et le mappage des rôles des groupes d’achats.

### Mappage des champs XDM

<table>
  <tbody>
    <tr>
      <th>Champ XDM</th>
      <th>Entité</th>
      <th>Définition de l’entreprise</th>
      <th>Détail additionnel</th>
    </tr>
    <tr>
      <td>
        <p>
          <span>b2b.accountKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Profils</span>
        </p>
      </td>
      <td>Identifiant de compte, utilisé dans les jointures pour les données d’opportunité, d’événement et d’intention</td>
      <td rowspan="2">Analyse des opportunités<br/>Exploration des comptes<br/>
        <br/>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>b2b.personKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Profils</span>
        </p>
      </td>
      <td>Identifiant de personne, utilisé dans les jointures impliquant des données d’événement aux données de profil</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>extendedWorkDetails.department</span>
        </p>
      </td>
      <td>
        <p>
          <span> des profils</span>
        </p>
      </td>
      <td>Département de la fonction du profil/de la personne</td>
      <td rowspan="5">
        <p>
          <br/>
        </p>
        <p>Mappage de persona</p>
      </td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>extendedWorkDetails.jobTitle</span>
        </p>
      </td>
      <td>
        <p>
          <span> des profils</span>
        </p>
      </td>
      <td>Fonction du profil/de la personne utilisé(e) dans le calcul des personas</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>person.name.firstName</span>
        </p>
      </td>
      <td>
        <p>
          <span >Profils</span>
        </p>
      </td>
      <td>Affiche le prénom de la personne dans les résultats correspondant à votre requête.</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>person.name.fullName</span>
        </p>
      </td>
      <td>
        <p>
          <span> des profils</span>
        </p>
      </td>
      <td>Affiche le nom complet de la personne dans les résultats correspondant à votre requête.</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>personne.nom.nom</span>
        </p>
      </td>
      <td>
        <p>
          <span> des profils</span>
        </p>
      </td>
      <td>Affiche le nom de la personne dans les résultats correspondant à votre requête.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span> comptes</span>
        </p>
      </td>
      <td>Identifiant de compte, utilisé dans les jointures pour les données d’opportunité, d’événement et d’intention</td>
      <td>Analyse des opportunités<br/>Exploration des comptes</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountName</span>
        </p>
      </td>
      <td>
        <p>
          <span>Comptes</span>
        </p>
      </td>
      <td>Affiche le nom du compte dans les résultats correspondant à votre requête.</td>
      <td rowspan="4">
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>Exploration de compte</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountDescription</span>
        </p>
      </td>
      <td>
        <p>
          <span>Comptes</span>
        </p>
      </td>
      <td>Prend en charge le filtrage de compte par description de compte en fonction de votre requête.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountOrganization.industry</span>
        </p>
      </td>
      <td>
        <p>
          <span> comptes</span>
        </p>
      </td>
      <td>Prend en charge le filtrage de compte par secteur d’activité en fonction de votre requête.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountBillingAddress.region</span>
        </p>
      </td>
      <td>
        <p>
          <span> comptes</span>
        </p>
      </td>
      <td>Prend en charge le filtrage de compte par région d’adresse de facturation en fonction de votre requête.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunité</span>
        </p>
      </td>
      <td>Identifiant de compte, utilisé dans les jointures pour les données d’opportunité, d’événement et d’intention</td>
      <td rowspan="2">
        <p>Analyse des opportunités<br/>exploration des comptes</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>opportunitéKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunité</span>
        </p>
      </td>
      <td>Identifiant d’opportunité, utilisé dans les jointures pour les données de compte</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>nomOpportunité</span>
        </p>
      </td>
      <td>
        <p>
          <span> Opportunité</span>
        </p>
      </td>
      <td>Nom de l’opportunité utilisé dans l’analyse d’opportunité.</td>
      <td rowspan="5">
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>Analyse d'opportunité</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>isWon</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunité</span>
        </p>
      </td>
      <td>Si l’opportunité est gagnée (binaire)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>opportunitéDescription</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunité</span>
        </p>
      </td>
      <td>Description de l’opportunité utilisée dans l’analyse des opportunités.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>quantitéopportunité</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunité</span>
        </p>
      </td>
      <td>Montant de $ impliqué dans l’opportunité</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>typeOpportunité</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunité</span>
        </p>
      </td>
      <td>Type d’opportunité</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>opportunitéStage</span>
        </p>
      </td>
      <td>
        <p>
          <span> Opportunité</span>
        </p>
      </td>
      <td>Étape de l’opportunité (close et confirmée, close et perdue ou l’une des étapes intermédiaires) </td>
      <td rowspan="4">
        <p>Analyse des opportunités<br/>Exploration des comptes</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>realCloseDate</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunité</span>
        </p>
      </td>
      <td>Date de fermeture effective de l’opportunité</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>expectedCloseDate</span>
        </p>
      </td>
      <td>
        <p>
          <span> Opportunité</span>
        </p>
      </td>
      <td>Date de fermeture prévue de l’opportunité</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>extSourceSystemAudit.createdDate</span>
        </p>
      </td>
      <td>
        <p>
          <span>Opportunité</span>
        </p>
      </td>
      <td>Date de création de cette opportunité</td>
    </tr>
  </tbody>
</table>

### Données de taxonomie

Les compétences d’audience utilisent des données d’intention propriétaires provenant de [!DNL Adobe Journey Optimizer B2B Edition]. Le calcul de l’intention connecte la taxonomie du produit à l’activité d’engagement et agrège les scores individuels au niveau du compte.

1. Le calcul de l’intention nécessite des données de taxonomie (produits client et mots-clés correspondants) de Clients > Taxonomie
1. Les données de taxonomie sont utilisées pour étiqueter les données d’événement (étiquetage des ressources). Ces données fournissent des informations sur les mots-clés et les produits qui intéressent les visiteurs en fonction de leurs données d’événement > Étiquetage des ressources 
1. Les ressources libellées (données d’événement) sont combinées aux comportements des visiteurs (nombre de pages visitées) pour déterminer l’intention d’un visiteur au niveau du mot-clé, du produit et de la catégorie de produit → calcul de l’intention
1. Les scores d’intention au niveau du profil du visiteur sont agrégés au niveau du compte afin de déterminer l’intention du compte dans un mot-clé, produit et catégorie de produits donnés > Agrégation des comptes d’intention

Les champs suivants sont requis en plus de la [configuration de la taxonomie d’intention](../admin/intent-data.md) :

<table>
  <tbody>
    <tr>
      <th>Champ XDM</th>
      <th>Entité</th>
      <th>Définition de l’entreprise</th>
    </tr>
    <tr>
      <th>
        <br/>
      </th>
      <th>
        <br/>
      </th>
      <td>profil de la personne</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>_acp_system_metadata.primaryIdentity.namespace.code<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Profil</span>
        </p>
      </td>
      <td>Permet d’identifier une personne (e-mail ou b2b_person)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>_acp_system_metadata.primaryIdentity.id
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Profil</span>
        </p>
      </td>
      <td>namespace_id</td>
    </tr>
    <tr>
      <td>
        <ul>
          <li>keyword_id</li>
          <li>nom_mot_clé</li>
          <li>product_id</li>
          <li>product_name</li>
          <li>product_category_id</li>
          <li>product_category_name</li>
        </ul>
      </td>
      <td>
        <p>
          <br/>
        </p>
      </td>
      <td>Utilisé comme taxonomie pour étiqueter les ressources (événements d’expérience, tels que les e-mails cliqués, les pages web visitées).</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>horodatage</span>
        </p>
      </td>
      <td>
        <p>
          <span> Événement d’expérience </span>
        </p>
      </td>
      <td>Utilisé pour le temps nécessaire au renvoi et à l’exécution incrémentielle</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>eventType</span>
        </p>
      </td>
      <td>
        <p>
          <span> Événement d’expérience </span>
        </p>
      </td>
      <td>Identifie le type d’événement. Le calcul de l’intention utilise uniquement <code>directMarketing.emailClicked</code>, <code>directMarketing.emailOpened</code>, <code>directMarketing.emailUnsubscribed</code> et <code>web.webpagedetails.pageViews</code>.
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingName</span>
        </p>
      </td>
      <td>
        <p>
          <span> Événement d’expérience </span>
        </p>
      </td>
      <td>Uniquement à titre de référence/comptabilité ; Informations sur le nom de la campagne</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceID</span>
        </p>
      </td>
      <td>
        <p>
          <span> Événement d’expérience </span>
        </p>
      </td>
      <td>Uniquement à titre de référence/comptabilité ; informations sur l’ID source auquel le courrier électronique est destiné.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceInstanceID<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span> Événement d’expérience </span>
        </p>
      </td>
      <td>Uniquement à titre de référence/comptabilité ; informations sur l’instance source à laquelle l’e-mail est destiné.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceKey<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span> Événement d’expérience </span>
        </p>
      </td>
      <td>Utilisé pour récupérer le contenu d’e-mail du centre de données [!DNL Adobe Marketo Engage]. Il comprend (SourceID@SourceInstanceID.SourceType).</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceType<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span> Événement d’expérience </span>
        </p>
      </td>
      <td>Uniquement à des fins de référence ou de comptabilité ; Renseignements sur le type de source ou l’origine de la source </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span> Événement d’expérience </span>
        </p>
      </td>
      <td>Informations sur l’origine de la source de la visite de la page web</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.name<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span> Événement d’expérience </span>
        </p>
      </td>
      <td>URL réelle utilisée pour obtenir le contenu</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.queryParameters</span>
        </p>
      </td>
      <td>
        <p>
          <span> Événement d’expérience </span>
        </p>
      </td>
      <td>Paramètre de requête additionnel pour l’URL de récupération du contenu ciblé </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.isPersonalizedURL</span>
        </p>
      </td>
      <td>
        <p>
          <span> Événement d’expérience </span>
        </p>
      </td>
      <td>uniquement à titre de référence/comptabilité</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceID<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span> Événement d’expérience </span>
        </p>
      </td>
      <td>Uniquement à titre de référence/comptabilité ; informations sur l’ID source auquel le courrier électronique est destiné.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceInstanceID<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span> Événement d’expérience </span>
        </p>
      </td>
      <td>Uniquement à titre de référence/comptabilité. Informations sur l’instance source à laquelle l’e-mail a été destiné.</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceKey<br/>
          </span>
        </p>
      </td>
      <td>
        <span> Événement d’expérience </span>
      </td>
      <td>Uniquement à titre de référence/comptabilité ; il comprend (SourceID@SourceInstanceID.SourceType)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceType</span>
        </p>
      </td>
      <td>
        <span> Événement d’expérience </span>
      </td>
      <td>Uniquement à des fins de référence ou de comptabilité ; Renseignements sur le type de source ou l'origine de la source</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.URL</span>
        </p>
      </td>
      <td>
        <span> Événement d’expérience </span>
      </td>
      <td>Utilisé pour récupérer l’URL réelle si web.webPageDetails.name ne l’a pas.</td>
    </tr>
  </tbody>
</table>
