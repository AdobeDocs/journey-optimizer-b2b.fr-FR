---
title: Audience Agent B2B
description: Audience Agent B2B dans Journey Optimizer B2B edition utilise l’analyse d’intention et le mappage de persona pour créer des groupes d’achats et accélérer les workflows marketing B2B.
feature: Agentic AI, Audiences
role: User
exl-id: c1210912-66ba-4b5f-8f3b-96eb6280c926
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
  - id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
subfeature_v2:
  - id: ff10f619-348f-47e3-99bf-3ce4c817cf2c
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
autotag-review: '2026-04-29T23:21:59.633Z'
source-git-commit: 97417ae1fcb017d4fcb7128e3fc0b61c829f867e
workflow-type: tm+mt
source-wordcount: 2500
ht-degree: 2%

---

# Audience Agent B2B

Optimisé par [&#128279;](https://experienceleague.adobe.com/fr/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator), Audience Agent B2B est disponible dans Journey Optimizer B2B edition. L’utilisation de cet agent améliore l’efficacité de l’exploration et de la mise à l’échelle des audiences, accélérant la création de groupes d’achats et les workflows transparents pour l’activation du parcours :

* **_Hiérarchiser les audiences cibles par intention_** : déduisez des rôles en fonction de l’intention du produit pour diverses audiences et rationalisez la planification des campagnes, en réduisant le temps consacré à la validation des audiences.

* **_Utiliser l’IA pour détecter et créer des groupes d’achats_** : utilisez l’IA, les données structurées, non structurées et les données propriétaires unifiées pour rationaliser la découverte et la création de groupes d’achats.

![Audience Agent B2B en mode Pleine page](./assets/audience-agent-full.png){width="700" zoomable="yes"}

>[!PREREQUISITES]
>
>Pour utiliser Audience Agent B2B, il existe des définitions et des mappages de données obligatoires <br/>
>
>* [Taxonomie/mappage des données intentionnelles](../admin/intent-data.md)
>* [taxonomie/mappage des champs XDM](#xdm-data-prerequisites)

## Fonctionnalités B2B d’Audience Agent

| Zone | Ce qu&#39;il fait | Valeur commerciale |
| ---- | ------------ | -------------- |
| Analyse de l’intention | <li> Mesurez l’intensité de l’intention du compte (faible, moyenne et élevée, par exemple) pour des produits spécifiques. <li>Comparez les tendances d’intérêt des produits au fil du temps (par exemple, les meilleurs produits au cours des _n_ derniers jours). <li>Identifier les comptes présentant un intérêt actif pour des produits spécifiques. <li>Affichez les modèles d’engagement qui combinent l’activité du compte à la couverture personnelle. | <li>Permet aux équipes de se concentrer sur les bons comptes au bon moment. <li>Améliore la qualité du pipeline en donnant la priorité aux comptes avec des signaux d’achat authentiques. <li>Permet un engagement proactif avant que les concurrents n’agissent. |
| Mappage de persona | <li>Détecter et classer les principales personnes par intention de produit. <li>Identifiez les personnes impliquées dans l’achat d’un ou de plusieurs produits. <li>Mappez les rôles aux rôles fonctionnels (tels que _Champion_, _Décideur_ et _Influenceur_) avec une justification. <li>Validez pourquoi une personne donnée est considérée comme un champion. | <li>Veille à ce que l&#39;équipe des ventes engage les véritables décideurs et influenceurs. <li>Réduit les efforts perdus sur les contacts à faible impact. <li>Augmente les taux de gain en alignant la sensibilisation avec la dynamique du pouvoir d&#39;achat. |
| Évaluation d&#39;un groupe d&#39;achat | <li>Évaluez la taille du groupe d&#39;achat (par exemple, les groupes comportant plus de _n_ membres). <li>Mesurez la couverture personnelle sur tous les comptes (par exemple, sous _x_ %). <li>Suivez la répartition des rôles et les écarts de couverture au sein des groupes d&#39;achats. <li>Mettez en évidence les comptes avec les champions identifiés dans les accords récents. | <li>Révèle des lacunes de couverture qui pourraient bloquer les transactions. <li>Renforce les stratégies multi-threads en assurant une représentation complète des rôles. <li>Améliore le suivi de l’intégrité des contrats grâce à des informations d’engagement au niveau du groupe. |
| Création et exploitabilité d&#39;un groupe d&#39;achat | <li>Recommandez des mappages rôle à rôle en fonction des rôles et des modèles de rôle observés. <li>Générer un modèle de rôle de groupe d&#39;achats pour un produit spécifié. <li>Prise en charge de la personnalisation des modèles en incluant ou en excluant des rôles et des rôles spécifiques. <li>Vérifiez que les rôles requis sont définis avant la création des groupes d&#39;achats. | <li>Réduit l&#39;effort manuel et le risque de modèles de groupe d&#39;achat incomplets. <li>Garantit que la couverture des rôles est validée avant la création, ce qui réduit le risque de lacunes de couverture. <li>Transforme les informations d’analyse en prochaines étapes immédiates et opérationnelles. |

## Limites

Le B2B d’Audience Agent dépend de la taxonomie d’intention configurée, des mappages de champs XDM et des données d’événement d’expérience. Les informations sont moins fiables lorsque les données de l’opportunité sont incomplètes, que la taxonomie de l’intention est manquante ou obsolète, ou que les identifiants de profil et de compte requis ne sont pas mappés. Pour le calcul de l’intention, l’agent traite uniquement ces événements d’expérience : `directMarketing.emailClicked`, `directMarketing.emailOpened`, `directMarketing.emailUnsubscribed` et `web.webpagedetails.pageViews`.

## Exemples de prompts

Ces exemples d’invite montrent quelques-unes des façons dont vous pouvez utiliser l’agent :

* Afficher la fenêtre de tendance : première et dernière mise à jour pour l’intention de produit du compte par produit.
* Par `<product>`, répertoriez les groupes d’achats avec l’intention du produit et les scores.
* Par `<product>`, répertoriez les rôles et les rôles avec leurs mesures d’opportunité (taux de succès, taux d’abonnement, nombres).
* Pour les comptes en `<industry>`, quelle est la couverture moyenne du profil de compte pour `<product>` ?
* Quels comptes ont une faible intention pour un produit, mais ont toujours des opportunités ouvertes (qui valent la peine d’être encouragées) ?
* Quels comptes ont ajouté de nouveaux signaux d’intention pour `<account_name>` cette semaine ?
* Montrez-moi les personnes associées à `<product>`.
* Me montrer la recommandation de mappage de rôle à persona pour `<product>`.
* Créez un modèle de groupe d&#39;achats pour `<product>`.
* Créez un modèle de groupe d&#39;achats pour les `<product>` sans le rôle `<persona>` et supprimez le rôle `<role>`.

## Concepts

| Concept | Explication |
| ------- | ----------- |
| Détection d’audience | En coulisse, l’agent examine les signaux d’intention de la première partie en fonction de deux éléments : l’engagement des utilisateurs vis-à-vis de votre marque et le type de personnes qu’ils représentent. L’analyse revient sur les 18 derniers mois d’activité pour détecter l’intention des produits chez tous les utilisateurs du compte, en particulier pendant la période précédant la fermeture d’une opportunité. Cette analyse permet à l’agent de mettre en évidence les personnes les plus susceptibles d’influencer la transaction.<br/><br/>Parfois, les comptes n’ont pas toutes leurs données d’opportunité en parfait état, ce qui est correct et l’agent peut toujours détecter l’intention du produit à partir de modèles d’engagement uniquement. |
| Persona | Les personas représentent les types de personnes qui interagissent au sein d’un compte. L’agent les crée en examinant le titre de poste, la fonction et le niveau d’ancienneté, puis en normalisant ces informations afin qu’elles soient cohérentes entre les différents comptes. Ainsi, au lieu de vous perdre dans des titres désordonnés, vous pouvez rapidement voir si vous atteignez des décideurs, des influenceurs ou des rôles de soutien. Les personas vous aident à comprendre qui montre de l’intérêt, et pas seulement le degré d’intérêt. |
| Mapping des rôles de groupes d&#39;achat | Une fois les rôles mappés, vous les rassemblez dans un groupe d’achat, c’est-à-dire l’équipe complète au sein du compte qui est la plus susceptible d’influencer ou de décider de l’achat. Chaque rôle (tel que _décideur_, _influenceur_ ou _champion_) ajoute un élément du tableau afin que vous ayez une vue claire du comité qui dirige l’affaire.<br/><br/> L’agent mappe chaque personnage identifié au rôle qu’il est le plus susceptible de jouer pour un produit spécifique, en fonction du titre de la fonction, de l’ancienneté et des autres attributs que vous configurez. Il indique également la couverture de chaque rôle afin que vous puissiez voir quels rôles sont bien représentés et quelles sont les lacunes restantes dans votre stratégie d’engagement. |
| Utilisation des données d’opportunité pour détecter les personas | Pour vous donner la vue la plus précise de qui s’engage et de leurs intérêts, l’agent approche le classement personnel et l’intention du produit en fonction des éléments suivants : <ul><li>Scénario idéal : si vous pouvez fournir des données telles que _Étape de l’opportunité_, _Date de fermeture de l’opportunité_ et un _Mappage opportunité-produit_ clair, l’agent peut classer les personnes en toute confiance par produit.<li>Ce classement permet de comprendre précisément l’engagement et l’intérêt au sein du compte. </ul>Mais l’agent sait que les données ne sont pas toujours complètes, ce qui est correct. Il comprend des solutions de secours intelligentes pour faire avancer les choses :<ul><li>L&#39;agent analyse le volume des activités, en donnant plus de poids aux activités récentes en utilisant la décroissance temporelle.<li>Cette pondération permet à l’agent de différencier et de classer les rôles, même sans données d’opportunité complètes. </ul>Lorsqu’il s’agit de lier les opportunités aux produits, voici comment l’agent le gère :<ul><li>_Idéal_ : vous fournissez ou aidez l’agent à créer la table de mappage.<li>_Si non disponible_ : l’agent utilise la correspondance approximative pour connecter les points.<li>_Aucun lien du tout_ : l’agent déduit l’intention du produit en fonction des activités récentes antérieures à la date de clôture.</ul>Cette approche à plusieurs niveaux garantit que l’agent peut toujours fournir des informations significatives, même lorsque les données ne sont pas parfaites. |
| Analyse des opportunités | L’agent examine les données historiques sur les opportunités pour comprendre quels facteurs prédisent le plus fortement une victoire et il utilise trois dimensions principales pour ce faire :<ol><li>Taux de réussite : indique la fréquence à laquelle les affaires sont conclues avec succès lorsque certaines personnes sont impliquées. Si les comptes dotés d’un modèle de persona spécifique (comme un évaluateur technique ou un décideur au niveau du vice-président) ont tendance à convertir plus souvent, le modèle accorde plus de poids à ce modèle. Ces informations représentent un pourcentage du total des opportunités, par exemple les opportunités clôturées ou confirmées.<li>Taux d’adhésion : mesure la fréquence à laquelle un type de persona s’affiche parmi les opportunités pour un produit donné. Si certaines personnes apparaissent systématiquement dans les offres réussies, cela indique qu&#39;elles jouent un rôle essentiel dans le processus d&#39;achat.<li>Influence personnelle : quantifie la contribution d’une personne donnée au résultat, pas seulement sa présence, mais la corrélation entre son engagement ou son niveau d’activité et ses gains.</ol>Ensemble, ces signaux permettent de déduire quelles personnes ont le plus d’impact sur les résultats d’achat, même lorsque les données d’opportunité sont incomplètes. Au fil du temps, il permet au système de faire apparaître les rôles et les modèles à fort impact qui sont les plus prédictifs de la réussite de l’affaire, ce qui permet ensuite d’informer l’intention du compte, le mappage des rôles et les recommandations des groupes d’achat. |
| Intention | Lorsqu’une personne visite une page web ou clique sur un lien d’e-mail lié à un produit, cela indique qu’elle est intéressée, ce qui est appelé _intention_.<br/><br/>L’agent commence par une taxonomie, qui est essentiellement une liste des produits du client et des mots-clés qui les décrivent. Ces informations aident l’agent à comprendre en quoi consiste chaque élément de contenu ou interaction.<br/><br/>Ensuite, l’agent utilise cette taxonomie pour étiqueter l’activité des visiteurs, comme les mots-clés ou les produits auxquels leurs actions se rapportent.<br/><br/>Ensuite, l’agent examine à quel point une personne interagit, comme le nombre de pages qu’elle visite ou la fréquence de ses interactions. Il utilise ces informations pour calculer le score d’intention individuel de chaque produit pour des mots-clés, des catégories de produits ou des produits spécifiques. Il regroupe chaque score d’intention en _Élevé_, _Medium_ ou _Faible_ intention pour indiquer l’intérêt. (Intention faible : `<=0.2`, Intention de Medium : `0.2 < score <= 0.6`, Intention élevée : `0.6 < score <= 1`)<br/><br/>Enfin, l’agent combine les scores d’intention de toutes les personnes de la même société (compte) pour afficher l’intention globale au niveau du compte, en indiquant les produits ou les sujets qui semblent les plus intéressants pour cette société. |
| Rôles qui influencent un groupe d&#39;achat | Chaque groupe d’achat est composé de rôles qui contribuent différemment à la décision d’achat, tels que _Décideur_, _Influenceur_, _Champion_ et _Utilisateur final_. Chaque rôle a un degré d’impact variable.<br/><br/>Les décideurs ont le plus d’influence et contrôlent généralement les approbations budgétaires. Les influenceurs façonnent l&#39;évaluation et les recommandations. Les champions aident à établir un consensus interne, tandis que les utilisateurs finaux valident l’adéquation du produit.<br/><br/>En vous présentant ces rôles, l’agent vous aide à comprendre qui pilote la décision d’achat, où votre engagement est le plus fort et où des lacunes de couverture peuvent exister. Ces informations vous permettent de vous concentrer sur les rôles qui comptent le plus pour ce produit. |
| Couverture des rôles ou des rôles | Pour un produit donné, il existe généralement un ensemble de rôles et de rôles clés connus pour influencer l’achat (_N_ rôles ou rôles). <br/><br/>Pour chaque compte, l’agent calcule la couverture en vérifiant le nombre de ces _N_ rôles représentés par au moins une personne au sein de ce compte.<br/><br/>Si tous les rôles _N_ sont présents, le compte bénéficie d’une couverture complète. Si seuls certains rôles sont représentés, la couverture est partielle.<br/><br/>En termes simples, la couverture du rôle et de la personne mesure l’exhaustivité de votre groupe d’achat pour un produit, selon que tous les décideurs, influenceurs et champions importants sont inclus. |

## Conditions préalables relatives aux données XDM

Audience Agent fournit des informations sur les comptes présentant l’intention propriétaire pour les produits et calcule les rôles et les rôles en fonction des données définies. Assurez-vous que les données préalables suivantes sont configurées pour utiliser les fonctionnalités d’Audience Agent :

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
      <td>Prénom de la personne, utilisé par Audience Agent pour afficher les noms dans l’interface utilisateur lorsqu’il répond à un critère.</td>
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
      <td>Nom complet de la personne, utilisé par Audience Agent pour afficher les noms dans l’interface utilisateur lorsqu’ils répondent à un critère.</td>
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
      <td>Nom de la personne, utilisé par Audience Agent pour afficher les noms dans l’interface utilisateur lorsqu’il répond à un critère</td>
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
      <td>Nom du compte utilisé par Audience Agent pour s’afficher dans l’interface utilisateur lorsqu’il est satisfait avec tout critère posé dans la requête utilisateur</td>
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
      <td>Description du compte/de la société utilisé(e) par Audience Agent pour appliquer un filtre sur les comptes en fonction de la requête utilisateur dans l’interface utilisateur </td>
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
      <td>Secteur de compte/société utilisé par Audience Agent pour appliquer un filtre sur les comptes en fonction des requêtes des utilisateurs dans l’interface utilisateur </td>
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
      <td>Adresse de facturation du compte/de la société utilisé(e) par Audience Agent pour appliquer un filtre sur les comptes en fonction de la requête utilisateur dans l’interface utilisateur </td>
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
      <td>Nom de l’opportunité utilisée par Audience Agent </td>
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
      <td>Description de l’opportunité utilisée par Audience Agent </td>
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

Audience Agent exploite l’intention propriétaire détectée dans Journey Optimizer B2B edition :

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
      <td>Obtenez le type d’événement, car l’agent ne traite que quatre événements (<span>directMarketing.emailClicked, directMarketing.emailOpened, directMarketing.emailUnsubscribed, web.webpagedetails.pageViews)</span>
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
      <td>Utilisé pour récupérer le contenu de l’e-mail à partir du centre de données Marketo Engage ; il se compose de (SourceID@SourceInstanceID.SourceType)</td>
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
