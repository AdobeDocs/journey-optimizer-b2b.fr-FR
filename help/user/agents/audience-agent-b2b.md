---
title: Audience Agent pour B2B
description: Audience Agent B2B dans l’édition B2B de Parcours Optimizer utilise l’analyse d’intention et le mappage de persona pour créer des groupes d’achat et accélérer les workflows marketing B2B.
feature: Audiences, AI Assistant
role: User
source-git-commit: fa53458db4576af037dcf4b16ab1bf7b103b2fdd
workflow-type: tm+mt
source-wordcount: '3066'
ht-degree: 0%

---

# Audience Agent pour B2B

Optimisé par [Adobe Experience Platform Agent Orchestrator](https://experienceleague.adobe.com/fr/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator), Audience Agent B2B est disponible dans Journey Optimizer B2B edition. L’utilisation de cet agent améliore l’efficacité de l’exploration et de la mise à l’échelle des audiences, accélérant la création de groupes d’achats et les workflows transparents pour l’activation du parcours :

* **_Hiérarchiser les audiences cibles par intention_** : déduisez des rôles en fonction de l’intention du produit pour diverses audiences et rationalisez la planification des campagnes, en réduisant le temps consacré à la validation des audiences.

* **_Tirez parti de l’IA pour détecter les groupes d’achats_** : utilisez l’IA, les données structurées, non structurées et les données propriétaires unifiées pour rationaliser la découverte et la création de groupes d’achats.

![Audience Agent pour B2B en mode Pleine page](./assets/audience-agent-full.png){width="700" zoomable="yes"}

>[!PREREQUISITES]
>
>Pour utiliser Audience Agent pour le B2B, il existe des définitions et des mappages de données obligatoires <br/>
>
>* [Taxonomie/mappage des données intentionnelles](../admin/intent-data.md)
>* [taxonomie/mappage des champs XDM](#xdm-data-prerequisites)

## Fonctionnalités d’Audience Agent for B2B

| Zone | Ce qu&#39;il fait | Valeur commerciale |
| ---- | ------------ | -------------- |
| Analyse de l’intention | <li> Mesurez l’intensité de l’intention du compte (faible, moyenne et élevée, par exemple) pour des produits spécifiques. <li>Comparez les tendances d’intérêt des produits au fil du temps (par exemple, les meilleurs produits au cours des _n_ derniers jours). <li>Identifier les comptes présentant un intérêt actif pour des produits spécifiques. <li>Affichez les modèles d’engagement qui combinent l’activité du compte à la couverture personnelle. | <li>Permet aux équipes de se concentrer sur les bons comptes au bon moment. <li>Améliore la qualité du pipeline en donnant la priorité aux comptes avec des signaux d’achat authentiques. <li>Permet un engagement proactif avant que les concurrents n’agissent. |
| Mappage de persona | <li>Détecter et classer les principales personnes par intention de produit. <li>Identifiez les personnes impliquées dans l’achat d’un ou de plusieurs produits. <li>Mappez les rôles aux rôles fonctionnels (tels que _Champion_, _Décideur_ et _Influenceur_) avec une justification. <li>Validez pourquoi une personne donnée est considérée comme un champion. | <li>Veille à ce que l&#39;équipe des ventes engage les véritables décideurs et influenceurs. <li>Réduit les efforts perdus sur les contacts à faible impact. <li>Augmente les taux de gain en alignant la sensibilisation avec la dynamique du pouvoir d&#39;achat. |
| Évaluation d&#39;un groupe d&#39;achat | <li>Évaluez la taille du groupe d&#39;achat (par exemple, les groupes comportant plus de _n_ membres). <li>Mesurez la couverture personnelle sur tous les comptes (par exemple, sous _x_ %). <li>Suivez la répartition des rôles et les écarts de couverture au sein des groupes d&#39;achats. <li>Mettez en évidence les comptes avec les champions identifiés dans les accords récents. | <li>Révèle des lacunes de couverture qui pourraient bloquer les transactions. <li>Renforce les stratégies multi-threads en assurant une représentation complète des rôles. <li>Améliore le suivi de l’intégrité des contrats grâce à des informations d’engagement au niveau du groupe. |

## Exemples d’invites

Ces exemples d’invite montrent quelques façons d’utiliser l’agent :

* Afficher la fenêtre de tendance : première et dernière mise à jour pour l’intention de produit du compte par produit.
* Par `<product>`, répertoriez les groupes d’achats avec l’intention du produit et les scores.
* Par `<product>`, répertoriez les rôles et les rôles avec leurs mesures d’opportunité (taux de succès, taux d’abonnement, nombres).
* Pour les comptes en `<industry>`, quelle est la couverture moyenne du profil de compte pour `<product>` ?
* Quels comptes ont une faible intention pour un produit, mais ont toujours des opportunités ouvertes (qui valent la peine d’être encouragées) ?
* Quels comptes ont ajouté de nouveaux signaux d’intention pour `<account_name>` cette semaine ?

## Concepts

| Concept | Explication |
| ------- | ----------- |
| Détection d’audience | En coulisse, l’agent examine les signaux d’intention de la première partie en fonction de deux éléments : l’engagement des utilisateurs vis-à-vis de votre marque et le type de personnes qu’ils représentent. L’analyse revient sur les 18 derniers mois d’activité pour détecter l’intention des produits chez tous les utilisateurs du compte, en particulier pendant la période précédant la fermeture d’une opportunité. Cette analyse permet à l’agent de mettre en évidence les personnes les plus susceptibles d’influencer la transaction.<br/><br/>Parfois, les comptes n’ont pas toutes leurs données d’opportunité en parfait état, ce qui est correct et l’agent peut toujours détecter l’intention du produit à partir de modèles d’engagement uniquement. |
| Persona | Les personas représentent les types de personnes qui interagissent au sein d’un compte. L’agent le crée en examinant le titre de poste, la fonction et le niveau d’ancienneté, puis en normalisant ces informations afin qu’elles soient cohérentes entre les différents comptes. Ainsi, au lieu de vous perdre dans des titres désordonnés, vous pouvez rapidement voir si vous atteignez des décideurs, des influenceurs ou des rôles de soutien. Les personas vous aident à comprendre qui montre de l’intérêt, et pas seulement quel est le niveau d’intérêt. <br/><br/> Lorsque l’agent mappe des rôles à des rôles de groupe d’achat, il prend le type de rôles identifiés, en fonction de leur titre de poste, de leur fonction, de leur ancienneté et de tout autre attribut que vous choisissez d’ajouter, et les aligne sur les rôles qu’ils sont les plus susceptibles de jouer dans une décision d’achat, tels que _décideur_, _influenceur_ ou _champion_. Ces rôles sont pertinents pour le produit spécifique en question, de sorte que vous puissiez voir qui est le plus important pour cette opportunité. L’agent affiche également la couverture de chaque rôle, ce qui vous permet de comprendre rapidement quels rôles sont bien représentés et où il peut y avoir des lacunes à combler dans votre stratégie d’engagement. |
| Mapping des rôles de groupes d&#39;achat | Une fois les rôles mappés, vous les rassemblez dans un groupe d’achat. Considérez-le comme l’équipe complète au sein du compte qui est la plus susceptible d’influencer ou de décider de l’achat. Chaque rôle (tel que _décideur_, _influenceur_ ou _champion_) ajoute un élément du tableau, de sorte que vous ayez une vue claire de l’ensemble du comité qui dirige l’affaire. <br/><br/> Lorsque vous mappez des rôles à des rôles de groupe d’achat, vous prenez le type de rôles identifiés, en fonction de leur titre de poste, de leur fonction, de leur ancienneté et de tout autre attribut que vous choisissez d’ajouter, et vous les alignez sur le rôle qu’ils sont les plus susceptibles de jouer dans une décision d’achat, tel que _décideur_, _influenceur_ ou _champion_. Ces rôles sont pertinents pour le produit spécifique en question, de sorte que vous puissiez voir qui est le plus important pour cette opportunité. L’agent affiche la couverture de chaque rôle, ce qui vous permet de comprendre rapidement quels rôles sont bien représentés et où il peut y avoir des lacunes à combler dans votre stratégie d’engagement. |
| Groupes d’achat | Les groupes d’achats permettent aux spécialistes du marketing de gérer la véritable complexité des comités d’achats, et non des prospects ou des comptes isolés. Adobe Journey Optimizer B2B edition propose les outils (informations basées sur l’IA, parcours basés sur les rôles et suivi de l’exhaustivité) nécessaires pour apporter la structure, la personnalisation et la clarté analytique à ce processus, en alignant finalement plus étroitement le marketing et les ventes sur les résultats en matière de chiffre d’affaires.<br/><br/>La création d&#39;un groupe d&#39;achat consiste à réunir trois éléments clés : le bon public, le contexte du produit et les rôles du groupe d&#39;achat. Voici un aperçu détaillé de son fonctionnement : <ol><li>**Identifier votre audience** <ul><li>Tout d’abord, l’agent découvre les comptes les plus pertinents pour votre produit. Cette détection inclut les comptes qui présentent déjà un intérêt et les comptes présentant un potentiel.<li>Dans ces comptes, il identifie les personnes (vos rôles clés) qui peuvent influencer ou faire partie de la décision d’achat.<li>Il choisit parmi les comptes à faire apparaître : une liste de comptes ou une audience de compte.</ul><li>**Prenez le contexte du produit**<ul><li>Ensuite, il examine le produit ou la solution sur lequel vous vous concentrez, ce qui garantit que les personnes identifiées sont réellement pertinentes par rapport à ce que vous souhaitez vendre ou promouvoir.<li>Cela permet également de mettre en évidence les lacunes de couverture (certains rôles sont peut-être manquants pour le produit) afin que vous sachiez sur quoi vous concentrer.</ul> <li>**Mapper des rôles aux rôles du groupe d’achat** <ul><li>Enfin, l’agent associe ces personnages à des rôles spécifiques de groupes d’achat, tels que les décideurs, les influenceurs et les champions.<li>En fonction de ce mappage, l&#39;agent peut vous recommander une composition de groupe d&#39;achats que vous pouvez examiner, ajuster ou confirmer.</ul> </ol> Lorsque ces trois composants sont réunis, cela crée votre groupe d&#39;achat, avec les détails des membres, les rôles et les informations prêts à l&#39;emploi. |
| Achat de groupes dans un parcours | Dans un parcours, un groupe d’achats peut être utilisé comme unité centrale d’orchestration, ce qui permet aux spécialistes marketing de concevoir des expériences qui s’adaptent à la dynamique du groupe plutôt que de traiter les membres de manière isolée. Par exemple, vous pouvez cibler l’ensemble du groupe avec des messages coordonnés, tout en adaptant le contenu spécifique aux rôles aux décideurs, aux influenceurs ou aux utilisateurs finaux. À mesure que les signaux d’intention et les données d’engagement sont transmis, les parcours peuvent créer des branches en fonction de la préparation du groupe, afficher des alertes pour les ventes lorsque des rôles critiques sont engagés ou déclencher automatiquement des étapes de préparation si des rôles clés sont manquants. Ce flux permet de s’assurer que chaque point de contact (des e-mails aux annonces basées sur les comptes en passant par la sensibilisation aux ventes) travaille ensemble pour faire avancer le groupe dans son processus d’achat, accélérant le consensus et réduisant les frictions sur le chemin de l’achat. |
| Parcours dans Journey Optimizer B2B edition | Un parcours peut être construit avec ou sans un groupe d&#39;achat, mais le niveau de précision et d&#39;impact change considérablement :<ul><li>**En l’absence d’un groupe d’achat** les parcours sont généralement construits autour de comptes. Les marketeurs peuvent toujours utiliser des signaux tels que l&#39;intention, le comportement ou l&#39;intérêt du produit pour déclencher des flux de maturation et de sensibilisation. Cette méthode fonctionne pour des mouvements plus simples ou lorsque vous disposez de données limitées sur un compte. Cependant, il risque d’ignorer l’ensemble plus large des parties prenantes qui influencent l’accord, ce qui peut ralentir la conversion ou provoquer des lacunes dans l’engagement.<li>**Avec un groupe d’achats**, les parcours sont orchestrés autour de l’ensemble des personnes impliquées dans une décision d’achat. Vous pouvez aligner les étapes sur les jalons au niveau du groupe (par exemple lorsque le comité atteint un score d’exhaustivité ou affiche un engagement collectif), tout en personnalisant les points de contact pour chaque rôle. Cette méthode vous permet de concevoir un engagement multi-thread coordonné : un décideur peut recevoir du contenu stratégique de retour sur investissement, tandis que les influenceurs reçoivent des séances approfondies sur les produits, et les ventes sont alertées lorsque des rôles critiques sont engagés. En cartographiant les parcours individuels et collectifs, les professionnels du marketing et les vendeurs peuvent accélérer la création d&#39;un consensus et faire avancer les opportunités de manière plus efficace. </ul> |
| Utilisation des données d’opportunité pour détecter les personas | Pour vous donner la vue la plus précise de qui s’engage et de leurs intérêts, l’agent approche le classement personnel et l’intention du produit en fonction des éléments suivants : <ul><li>Scénario idéal : si vous pouvez fournir des données telles que _Étape de l’opportunité_, _Date de fermeture de l’opportunité_ et un _Mappage opportunité-produit_ clair, l’agent peut classer les personnes en toute confiance par produit.<li>Ce classement permet de comprendre précisément l’engagement et l’intérêt au sein du compte. </ul>Mais l’agent sait que les données ne sont pas toujours complètes, ce qui est correct. Il comprend des solutions de secours intelligentes pour faire avancer les choses :<ul><li>L&#39;agent analyse le volume des activités, en donnant plus de poids aux activités récentes en utilisant la décroissance temporelle.<li>Cette pondération permet à l’agent de différencier et de classer les rôles, même sans données d’opportunité complètes. </ul>Lorsqu’il s’agit de lier les opportunités aux produits, voici comment l’agent le gère :<ul><li>_Idéal_ : vous fournissez ou aidez l’agent à créer la table de mappage.<li>_Si non disponible_ : l’agent utilise la correspondance approximative pour connecter les points.<li>_Aucun lien du tout_ : l’agent déduit l’intention du produit en fonction des activités récentes antérieures à la date de clôture.</ul>Cette approche à plusieurs niveaux garantit que l’agent peut toujours fournir des informations significatives, même lorsque les données ne sont pas parfaites. |
| Analyse des opportunités | L’agent examine les données historiques sur les opportunités pour comprendre quels facteurs prédisent le plus fortement une victoire et il utilise trois dimensions principales pour ce faire :<ol><li>Taux de réussite : indique la fréquence à laquelle les affaires sont conclues avec succès lorsque certaines personnes sont impliquées. Si les comptes dotés d’un modèle de persona spécifique (comme un évaluateur technique ou un décideur au niveau du vice-président) ont tendance à convertir plus souvent, le modèle accorde plus de poids à ce modèle. Ces informations représentent un pourcentage du total des opportunités, par exemple les opportunités clôturées ou confirmées.<li>Taux d’adhésion : mesure la fréquence à laquelle un type de persona s’affiche parmi les opportunités pour un produit donné. Si certaines personnes apparaissent systématiquement dans les offres réussies, cela indique qu&#39;elles jouent un rôle essentiel dans le processus d&#39;achat.<li>Influence personnelle : quantifie la contribution d’une personne donnée au résultat, pas seulement sa présence, mais la corrélation entre son engagement ou son niveau d’activité et ses gains.</ol>Ensemble, ces signaux permettent de déduire quelles personnes ont le plus d’impact sur les résultats d’achat, même lorsque les données d’opportunité sont incomplètes. Au fil du temps, il permet au système de faire apparaître les rôles et les modèles à fort impact qui sont les plus prédictifs de la réussite de l’affaire, ce qui permet ensuite d’informer l’intention du compte, le mappage des rôles et les recommandations des groupes d’achat. |
| Intention | Lorsqu’une personne visite une page web ou clique sur un lien d’e-mail lié à un produit, cela indique qu’elle est intéressée, ce qui est appelé _intention_.<br/><br/>L’agent commence par une taxonomie, qui est essentiellement une liste des produits du client et des mots-clés qui les décrivent. Ces informations aident l’agent à comprendre en quoi consiste chaque élément de contenu ou interaction.<br/><br/>Ensuite, l’agent utilise cette taxonomie pour étiqueter l’activité des visiteurs, comme les mots-clés ou les produits auxquels leurs actions se rapportent.<br/><br/>Ensuite, l’agent examine à quel point une personne interagit, par exemple le nombre de pages qu’elle visite ou la fréquence de ses interactions. Il utilise ces informations pour calculer le score d’intention individuel de chaque produit pour des mots-clés, des catégories de produits ou des produits spécifiques. Il regroupe chaque score d’intention en _Élevé_, _Medium_ ou _Faible_ intention pour indiquer l’intérêt. (Intention faible : `<=0.2`, Intention de Medium : `0.2 < score <= 0.6`, Intention élevée : `0.6 < score <= 1`)<br/><br/>Enfin, l’agent combine les scores d’intention de toutes les personnes de la même société (compte) pour afficher l’intention globale au niveau du compte, en indiquant les produits ou les sujets qui semblent les plus intéressants pour cette société. |
| Rôles qui influencent un groupe d&#39;achat | Chaque groupe d’achat est composé de rôles qui contribuent différemment à la décision d’achat, tels que _Décideur_, _Influenceur_, _Champion_ et _Utilisateur final_. Chaque rôle a un degré d’impact variable.<br/><br/>Les décideurs ont le plus d’influence et contrôlent généralement les approbations budgétaires. Les influenceurs façonnent l&#39;évaluation et les recommandations. Les champions aident à établir un consensus interne, tandis que les utilisateurs finaux valident l’adéquation du produit.<br/><br/>En vous présentant ces rôles, l’agent vous aide à comprendre qui pilote la décision d’achat, où votre engagement est le plus fort et où des lacunes de couverture peuvent exister. Ces informations vous permettent de vous concentrer sur les rôles qui comptent le plus pour ce produit. |
| Couverture des rôles ou des rôles | Pour un produit donné, il existe généralement un ensemble de rôles et de rôles clés connus pour influencer l’achat (_N_ rôles ou rôles).<br/><br/>Pour chaque compte, l’agent calcule la couverture en vérifiant le nombre de ces _N_ rôles représentés par au moins une personne au sein de ce compte.<br/><br/>Si tous les rôles _N_ sont présents, le compte bénéficie d’une couverture complète. Si seuls certains rôles sont représentés, la couverture est partielle.<br/><br/>En termes simples, la couverture du rôle et de la personne mesure l’exhaustivité de votre groupe d’achat pour un produit, selon que tous les décideurs, influenceurs et champions importants sont inclus. |

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
          <span>  Profils </span>
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
          <span>  Profils </span>
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
          <span>  Comptes </span>
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
          <span>  Comptes </span>
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
      <td>si l’opportunité est gagnée (binaire)</td>
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
      <td>Uniquement à des fins de référence/tenue de livres ; Informations sur le nom de la campagne</td>
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
      <td>Uniquement à des fins de référence/de tenue de livres ; informations sur l’ID source auquel le courrier électronique est destiné.</td>
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
      <td>Uniquement à des fins de référence ou de tenue de livres. Informations sur l’instance source à laquelle l’e-mail est destiné.</td>
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
      <td>Utilisé pour récupérer le contenu de l’e-mail à partir du centre de données Marketo Engage ; il se compose de (SourceID@SourceInsatceID.SourceType)</td>
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
      <td>Uniquement à des fins de référence ou de tenue de livres ; Renseignements sur le type de source ou l’origine de la source </td>
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
      <td>Informations sur l’origine source ciblée par l’e-mail</td>
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
      <td>uniquement à titre de référence/tenue de livres</td>
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
      <td>Uniquement à des fins de référence/de tenue de livres ; informations sur l’ID source auquel le courrier électronique est destiné.</td>
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
      <td>Uniquement à des fins de référence ou de tenue de livres. Informations sur l’instance source à laquelle l’e-mail était destiné.</td>
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
      <td>Uniquement à des fins de référence/de tenue de livres ; il comprend (SourceID@SourceInsatceID.SourceType)</td>
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
      <td>Uniquement à des fins de référence ou de tenue de livres ; Renseignements sur le type de source ou l'origine de la source</td>
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
