---
title: IA générative pour le contenu
description: Découvrez comment créer des e-mails et des pages de destination personnalisés avec l’IA générative dans  [!DNL Journey Optimizer B2B Edition], y compris les bonnes pratiques en matière d’invite.
feature: AI Assistant, Generative AI, Content
level: Beginner
topic: Artificial Intelligence
role: User
source-git-commit: d3238fa94f28c6d7e3fc0dce5b59fd70d8e74e34
workflow-type: tm+mt
source-wordcount: '2506'
ht-degree: 32%

---

# IA générative pour le contenu {#generative-ai-content}

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai-generation-settings"
>title="Génération de contenu AI"
>abstract="Après avoir conçu votre mise en page, vous pouvez utiliser des outils d’IA génératifs dans [!DNL Journey Optimizer B2B Edition] pour améliorer votre contenu. Cette fonctionnalité simplifie le processus de personnalisation et d’amélioration du contenu en affinant le contenu en fonction de votre invite descriptive."

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai-generation-reference-context"
>title="Contenu de référence"
>abstract="Utilisez _Contenu de référence_ pour charger un fichier de ressource contenant du contenu qui fournit un contexte supplémentaire pour l’IA générative dans [!DNL Journey Optimizer B2B Edition], ou pour sélectionner un fichier précédemment chargé. Cette option permet de s’assurer que tous les documents nécessaires sont disponibles pour améliorer la qualité et la pertinence du contenu généré."

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai-generation-start"
>title="Termes d’IA génératifs Adobe"
>abstract="L’accès à cette fonctionnalité est soumis à votre acceptation des directives d’utilisation de l’IA générative d’Adobe Experience Cloud. Passez en revue toutes les sorties de cette fonctionnalité à des fins d’exactitude et assurez-vous qu’elles sont appropriées à votre cas d’utilisation."
>additional-url="https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html" text="Directives à l’intention des utilisateurs de l’IA générative Adobe"

L’IA générative pour le contenu en [!DNL Adobe Journey Optimizer B2B Edition], optimisée par Microsoft Azure OpenAI et Adobe Firefly, fournit des suggestions proactives de variation de contenu pour le texte et les images. Optimisez l’impact de votre contenu en expérimentant avec différents titres et images principaux.

Utilisez les fonctionnalités d’IA générative pour la création de contenu dans [!DNL Journey Optimizer B2B Edition] pour exploiter les fonctionnalités d’IA générative d’Adobe. Créez du texte et des visuels personnalisés pour les e-mails, les SMS, les pages de destination, etc. Lorsque vous créez une campagne complète ou que vous affinez simplement des ressources spécifiques, ces fonctionnalités vous permettent d’aligner facilement le contenu avec les directives de votre marque tout en gagnant un temps précieux.

<!--
Generate multiple variants and build an experiment to compare them. Leveraging Journey Optimizer Content Experiment, you can define multiple message treatments to measure which one performs best for your target audience. You can choose to vary the delivery content, or subject. The message audience is randomly allocated to each treatment to determine which one works best in terms of the specified metric. Learn more about Content Experiment in this section. -->

>[!IMPORTANT]
>
>Pour accéder à ces fonctionnalités dans [!DNL Journey Optimizer B2B Edition], vous devez disposer de l’autorisation _[!UICONTROL Assistant IA]_ > _[!UICONTROL Générer du contenu]_. Pour plus d’informations sur la manière dont un administrateur de produit peut accorder des autorisations de fonctionnalité, voir [Modifier les rôles pour les autorisations de produit](../admin/user-management.md#edit-roles-for-product-permissions).

Les outils de l’assistant AI pour la génération de contenu sont pris en charge avec les types de ressources suivants :

* [E-mails](../content/ai-assistant-emails.md)
* [!BADGE Beta] [Pages de destination](../content/ai-assistant-landing-pages.md)

## Directives générales et restrictions {#general-guidelines-and-limitations}

Votre utilisation des fonctionnalités d’IA générative est soumise aux [Directives d’utilisation de l’IA générative de Adobe Experience Cloud](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}. Avec l’engagement d’Adobe en matière de transparence dans l’utilisation des outils d’IA génératifs pour la création de médias, Adobe applique les [ informations d’identification de contenu ](https://helpx.adobe.com/firefly/web/get-started/learn-the-basics/content-credentials-overview.html){target="_blank"} à tout contenu ou projet qui inclut une ressource générée par [!DNL Firefly] lorsqu’elle est téléchargée ou exportée.

Consultez ces instructions générales pour l’utilisation de l’IA générative pour le contenu dans [!DNL Journey Optimizer B2B Edition] :

* Utilisez des invites bien définies pour que le modèle d’IA générative l’interprète avec précision. L’objectif ou l’invite marketing que vous fournissez affecte fortement la qualité du contenu généré.

* Chargez des fichiers de référence de contenu pour obtenir du contenu précis et intégré à la marque. Dans le cas contraire, le contenu est basé sur des informations accessibles au public. Le contenu chargé peut se présenter sous les formats de fichiers suivants : PDF, JPEG, PNG ou ZIP (contenant les formats de fichiers pris en charge). La taille maximale d’un fichier chargé est de 50 Mo. Des fichiers plus volumineux ou un grand nombre d’images peuvent fonctionner, mais cela augmente le temps de traitement.

* Utilisez un modèle personnalisé ou spécifique à la marque pour créer le contenu de votre e-mail. Il est recommandé d’utiliser des modèles d’e-mail contenant entre 8 et 10 images.

* Veillez à signaler les sorties problématiques à l&#39;aide des icônes de pouces vers le haut, vers le bas ou d&#39;indicateurs lors de la sélection de variantes.

## Bonnes pratiques d’invite pour l’IA générative {#generative-ai-prompting-guide}

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai_content_prompt"
>title="Invite de guidage"
>abstract="Consultez [!DNL Journey Optimizer B2B Edition] documentation pour savoir comment créer des invites efficaces qui génèrent du contenu marketing de marque à conversion élevée."

Ce guide vous aide à structurer vos requêtes, à communiquer l’intention avec clarté et à vous assurer que l’IA produit un message qui correspond aux directives de votre marque, aux besoins de l’audience et aux objectifs de votre campagne.

Découvrez comment rédiger des prompts efficaces qui permettent à l’assistant IA de générer du contenu marketing de grande qualité, conforme à la marque et adapté à vos objectifs.

### Utiliser le framework CO-STAR {#costar-framework}

Pour obtenir de meilleurs résultats avec le contenu généré, organisez vos invites à l&#39;aide du framework CO-STAR. Cette approche structurée clarifie exactement ce dont vous avez besoin.

| Composant | Signification | Importance de ces éléments |
| --- | ---- | ------ |
| **C - Contexte** | Contexte de votre campagne, produit ou situation | Permet de mieux comprendre le contexte dans son ensemble |
| **O - Objectif** | Votre objectif marketing spécifique | Détermine l’objectif du contenu. |
| **S - Style** | Comment vous voulez communiquer | Définit l’approche. |
| **T - Ton** | Style émotionnel et voix | Détermine comment votre message est perçu. |
| **A - Audience** | L’audience ciblée | Garantit que le message trouve un écho auprès des personnes appropriées |
| **R - Exigences** | Contraintes spécifiques ou exigences | Définit les limites et les éléments critiques. |

{style="table-layout:fixed"}

### Invite Essentiels {#key-takeaways}

<table style="table-layout: fixed; width: 100%; border: 0;">
<thead style="border: 0; background-color: #FFFFFF;">
<tr>
<th>Conseils</th>
<th>Erreurs à éviter</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul><li>Utiliser le framework CO-STAR pour la structure
<li>Distinguer le nouveau contenu du contenu existant
<li>Orienter l’utilisation des documents avec des conseils d’extraction spécifiques
<li>Effectuer des sélections pour le ton, la stratégie et le paramètre régional
<li>Adapter les objectifs marketing aux fonctionnalités de type de contenu
<li>Générer plusieurs variantes pour les tests A/B</ul>
</td>
<td>
<ul><li>Demander des modifications structurelles, de style ou de modification d’image dans les prompts
<li>Mentionner le ton/la stratégie dans les invites si disponible dans les options
<li>Utiliser des objectifs vagues comme _promouvoir le produit_
<li>Demander des sélections d’éléments conditionnels
<li>S’attendre à des modifications de la disposition via des prompts</ul>
</td>
</tr>
</tbody>
</table>

### Contenu non pris en charge dans les prompts

>[!TIP]
>
>Utilisez les outils ou les [!DNL Adobe Express] de conception pour apporter des modifications visuelles ou d’image.

Les requêtes suivantes ne sont **_pas prises en charge_** et doivent être traitées par d’autres outils :

<table style="table-layout: fixed; border: 0;">
<thead style="border: 0; background-color: #FFFFFF">
<tr>
<th><img src="../../assets/do-not-localize/check-box-red.svg" alt="Croix rouge">  Modifications de la structure de l'email</th>
<th><img src="../../assets/do-not-localize/check-box-red.svg" alt="Croix rouge">  Modifications visuelles du style</th>
<th><img src="../../assets/do-not-localize/check-box-red.svg" alt="Croix rouge">  Opérations d’édition d’images</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul>
<li>Sélection des sections spécifiques à modifier</li>
<li>Suppression ou clonage d’éléments</li>
<li>Sélections conditionnelles</li>
<li>Ajout ou suppression de sections de disposition</li>
</ul>
</td>
<td>
<ul>
<li>Mise en forme du texte (gras, italique, taille de police)</li>
<li>Modifications de couleur</li>
<li>Style de disposition (bordures, marge intérieure, marges)</li>
<li>Effets visuels (ombres)</li>
</ul>
</td>
<td>
<ul>
<li>Modifications d’arrière-plan</li>
<li>Ajout de superpositions de texte ou de logos</li>
<li>Recadrage ou redimensionnement d’image</li>
<li>Réglages des couleurs</li>
<li>Remplacement d’image</li>
</ul>
</td>
</tr>
</tbody>
</table>

### Liste de contrôle de qualité {#quality-checklist}

Avant de générer du contenu, vérifiez les points suivants :

![Coche verte](../../assets/do-not-localize/check-box-green.svg){width="20"} **Objectif clair** : indique clairement l’action, le produit/service, la valeur et le contexte.

![Coche verte](../../assets/do-not-localize/check-box-green.svg){width="20"} **Audience cible définie** : indique le groupe démographique, le rôle ou le segment.

![Coche verte](../../assets/do-not-localize/check-box-green.svg){width="20"} **Alignement du type de contenu** : l’objectif correspond au canal ou au format sélectionné.

![Coche verte](../../assets/do-not-localize/check-box-green.svg){width="20"} **Vérifier les sélections** : la tonalité, la stratégie et le paramètre régional sont sélectionnés, ne les incluez pas dans l’invite.

![Coche verte](../../assets/do-not-localize/check-box-green.svg){width="20"} **La sélection du document est spécifiée** : met en surbrillance le contenu ou les sections à référencer.

![Coche verte](../../assets/do-not-localize/check-box-green.svg){width="20"} **Marque appliquée** : les directives de marque appropriées sont sélectionnées.

![Coche verte](../../assets/do-not-localize/check-box-green.svg){width="20"} **Portée réaliste** : évitez les demandes de modifications de disposition, de style ou de structure.

### Objectifs marketing efficaces {#marketing-objectives}

Lors de l’élaboration des objectifs marketing, assurez-vous qu’ils sont clairs, exploitables et mesurables. Évitez les énoncés vagues ou génériques.

**Exemples de bons objectifs :**

![Coche verte](../../assets/do-not-localize/check-box-green.svg){width="20"} « Encouragez les inscriptions à l’essai gratuit de 30 jours du nouveau tableau de bord d’analyses optimisé par l’IA »

![Coche verte](../../assets/do-not-localize/check-box-green.svg){width="20"} « Générer des pistes pour le webinaire B2B sur la réduction de 40 % des coûts du cloud » qui aura lieu le 15 mars. »

![Coche verte](../../assets/do-not-localize/check-box-green.svg){width="20"} « Promouvoir la réduction limitée de 25 % sur les abonnements Premium, jusqu’au 25 décembre »

**Exemples à éviter :**

![Croix rouge](../../assets/do-not-localize/check-box-red.svg){width="20"} « Promouvoir le produit » (trop vague)

![Croix rouge](../../assets/do-not-localize/check-box-red.svg){width="20"} « Faites signer des contrats » (valeur non précisée)

![Croix rouge](../../assets/do-not-localize/check-box-red.svg){width="20"} « E-mail à propos des nouvelles fonctionnalités » (manque d’objectif)

#### Structurez votre objectif.

Fournissez toujours le contexte et la proposition de valeur pour produire du contenu pertinent. Utilisez la formule suivante pour vous aider à définir des objectifs efficaces : **Action + Produit/Service + Valeur/Avantage + Urgence/Contexte**

**Exemples de bons objectifs :**

![Coche verte](../../assets/do-not-localize/check-box-green.svg){width="20"} « Encouragez les téléchargements de la nouvelle application mobile qui aide les utilisateurs à suivre les habitudes de vie durables avec des recommandations personnalisées et respectueuses de l’environnement »

![Coche verte](../../assets/do-not-localize/check-box-green.svg){width="20"} « Promouvoir l’inscription à l’atelier exclusif sur les techniques avancées de visualisation de données pour les professionnels du marketing »

![Coche verte](../../assets/do-not-localize/check-box-green.svg){width="20"} « Augmentez la participation à l’événement de lancement du produit présentant l’assistant d’écriture d’IA révolutionnaire qui vous permet de gagner plus de 5 heures par semaine »

**Exemples à éviter :**

![Croix rouge](../../assets/do-not-localize/check-box-red.svg){width="20"} « Annoncer une nouvelle application » (proposition de valeur et contexte manquants)

![Barre rouge](../../assets/do-not-localize/check-box-red.svg){width="20"} « Inciter les gens à s’inscrire à l’atelier » (manque de précision concernant le public et l’avantage)

![Croix rouge](../../assets/do-not-localize/check-box-red.svg){width="20"} « Promouvoir l’événement » (aucune action, valeur ou urgence claire)

#### Exemples d’invites par type de canal {#channel-type-practices}

<table style="table-layout: auto; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Canal</th>
<th>Exemple</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>E-mail</strong></td>
<td>« Développez les prospects des entreprises en présentant trois témoignages de clients avec des mesures détaillées de retour sur investissement (Oracle : réduction des coûts de 45 %, Accenture : augmentation de 200 % des prospects, Microsoft : économie de temps de 60 %). Cibler les directeurs informatiques dans les entreprises de plus de 1 000 salariés »</td>
</tr>
<tr>
<td><strong>Pages de destination</strong></td>
<td>« Convertissez les visiteurs B2B en prospects qualifiés en démontrant comment la solution de sécurité d’entreprise prévient 99,9 % des cyberattaques, grâce aux témoignages Fortune 500 et à un audit de sécurité gratuit »</td>
</tr>
</tbody>
</table>

<!-- channels not yet supported
<tr>
<td><strong>SMS</strong></td>
<td>"Alert VIP customers about a 4-hour flash sale on premium electronics with 40% discount, limited to the first 100 customers"</td>
</tr>
<tr>
<td><strong>Push Notifications</strong></td>
<td>"Re-engage users who haven't opened the app in 7 days with personalized content recommendations based on their reading history"</td>
</tr> -->

<!-- Wait on more B2B specific examples

### Industry-specific approaches {#industry-approaches}

<table style="table-layout: fixed; border-collapse: collapse; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Industry</th>
<th>Example Prompt</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>B2B Technology</strong></td>
<td>"Demonstrate ROI and technical specifications while addressing security concerns for IT decision-makers evaluating our cloud infrastructure solution, emphasizing 99.9% uptime SLA, SOC 2 compliance, and 40% cost savings."</td>
</tr>
<tr>
<td><strong>E-commerce Retail</strong></td>
<td>"Create urgency around limited-stock holiday items while highlighting free shipping and easy returns for last-minute shoppers, emphasizing limited quantities (less than 50 remaining) and 24-hour shipping cutoff."</td>
</tr>
<tr>
<td><strong>Financial Services</strong></td>
<td>"Educate clients about investment portfolio diversification strategies while maintaining regulatory compliance, featuring certified financial advisor insights and risk disclaimers."</td>
</tr>
<tr>
<td><strong>Healthcare & Wellness</strong></td>
<td>"Promote preventive care benefits and annual health screenings while maintaining medical accuracy, featuring board-certified physician recommendations and patient privacy assurances."</td>
</tr>
<tr>
<td><strong>Education & Training</strong></td>
<td>"Emphasize career advancement outcomes and industry certifications while showcasing instructor expertise, highlighting 92% job placement rate and project-based curriculum."</td>
</tr>
<tr>
<td><strong>SaaS Platforms</strong></td>
<td>"Highlight time savings and automation benefits with specific metrics while addressing integration concerns, featuring average 25-hour weekly time savings and integration with 200+ popular tools."</td>
</tr>
</tbody>
</table>
 -->

### Nouveau contenu ou modification de contenu existant {#new-vs-modify}

Indiquez clairement si votre demande implique la génération de nouveau contenu ou la mise à jour de contenu existant. Cette distinction est importante, car elle guide l’IA dans le choix de l’approche appropriée et garantit un résultat plus précis et pertinent.

#### Création de nouveau contenu

Appliquez cette stratégie lorsque vous lancez des campagnes marketing, dévoilez de nouvelles solutions ou lancez une communication mise à jour/actualisée. Cela garantit que votre message commence fort et s’aligne sur vos objectifs.

**Quels prompts utiliser** ➤ Lors de la création d’un nouveau contenu, concentrez-vous sur votre objectif marketing sans référencer de contenu existant.

>[!BEGINSHADEBOX « Exemples »]

* **Essai SaaS** : « Lancez le nouveau logiciel CRM aux propriétaires de petites entreprises, en leur permettant de gagner 50 % de temps, de se qualifier 90 % plus rapidement pour les prospects et d’effectuer un essai gratuit de 30 jours avec intégration personnalisée »
* **Annonce des fonctionnalités** : « Annonce de nouvelles fonctionnalités d’intégration d’API qui réduisent de 60 % le temps de développement pour les entreprises clientes, en ciblant les décideurs et décideuses techniques. »
* **Promotion d’événement** : « Organisez les inscriptions au webinaire sur les « Tendances du marketing numérique 2024 », avec des experts de Google, Meta et Adobe, en mettant l’accent sur les informations exploitables et les places limitées (500 max.) »

>[!ENDSHADEBOX]

#### Modification du contenu existant

>[!TIP]
>
>Pour des modifications standard telles que développer, résumer ou simplifier, sélectionnez **_Affiner_** au lieu d’écrire des invites personnalisées.

Utilisez une invite de modification lorsque vous devez mettre à jour, actualiser ou adapter vos campagnes marketing actuelles. Elle favorise les améliorations progressives, afin que vos messages restent pertinents sans avoir à repartir de zéro.

**Quels prompts utiliser** ➤ Lors de la modification d’un contenu existant, indiquez clairement ce que vous souhaitez modifier et comment le modifier.

>[!BEGINSHADEBOX « Exemples »]

* **Actualisation de Campaign** : « Modifiez l’e-mail de lancement du programme pour vous concentrer sur les fonctionnalités de sécurité de l’entreprise plutôt que sur les avantages généraux en matière de productivité, en ciblant les décideurs informatiques avec des certifications de conformité »
* **Audience pivot** : « Adaptez l’invitation de démonstration du logiciel pour cibler les soins de santé en particulier, en remplaçant les exemples génériques par des cas d’utilisation des soins de santé et des avantages en termes de conformité HIPAA »
* **Mise à jour saisonnière** : « Mettez à jour la campagne promotionnelle du T3 pour les achats du T4 pour les vacances, en passant de la rentrée des classes au cadeau de vacances avec une priorité d’expédition rapide »

>[!ENDSHADEBOX]

## Paramètres de texte avancés {#text-settings}

Outre l’utilisation d’une invite claire et bien formée, les paramètres de texte dans les outils de contenu de l’assistant d’IA incluent des paramètres de texte que vous pouvez utiliser pour optimiser les sorties générées.

>[!TIP]
>
>Utilisez les options _[!UICONTROL Stratégie de communication]_ et _[!UICONTROL Ton]_ dans les paramètres _[!UICONTROL Texte]_ au lieu de mentionner ces caractéristiques dans votre invite.

### Types de stratégie de communication

Votre stratégie de communication détermine la manière dont vous présentez votre message afin de maximiser l’impact. Différentes stratégies fonctionnent mieux selon les objectifs, que vous cherchiez à créer un sentiment d’urgence, à instaurer la confiance ou à déclencher une action immédiate. Choisissez la stratégie qui correspond le mieux à vos objectifs de campagne et à l’état d’esprit de votre audience.

| **Stratégie** | **Idéal pour** | **Style de message** | **Exemples** |
| ------------ | ------------ | ------------------- | ------------ |
| **Urgent** | Offres à durée limitée, échéances, action immédiate | Crée une pression immédiate avec un langage axé sur le facteur temporel. | <li>« Agir maintenant : l’offre expire à minuit » <li>« Inscrivez-vous dès aujourd’hui avant que les places ne se remplissent » <li>« La vente flash de 48 heures commence maintenant » |
| **FOMO (peur de passer à côté)** | Offres limitées, événements, accès exclusif | Utilise des signaux d’urgence, de rareté et de pression temporelle. | <li>« Plus que 24 heures ! Stock limité à 40 % de remise » <li>« Dernière chance : les tarifs anticipés se terminent demain » <li>« Il ne reste que 100 points bêta » |
| **Preuve sociale** | Création de confiance, témoignages, produits populaires | Tire parti des expériences et de la validation des autres personnes. | <li>« Rejoignez plus de 50 000 clients satisfaits » <li>« Classé 4,9/5 étoiles par les professionnels du secteur » <li>« Des entreprises dignes de confiance selon le classement Fortune 500 » |
| **Pénurie** | Stock limité, versions exclusives, articles à forte demande | Souligne la disponibilité limitée et l’exclusivité. | <li>« Il n&#39;en reste que 5 en stock » <li>« Edition limitée : 100 unités disponibles » <li>« Version exclusive : premier arrivé, premier servi » |
| **Avantage incitatif** | Promotions, programmes de récompense, offres spéciales | Met en évidence les avantages et les récompenses tangibles. | <li>« Obtenez 20 % de réduction sur votre première commande » <li>« Gagnez deux points ce week-end » <li>« Livraison gratuite sur les commandes de plus de 50 $ » |
| **Exclusivité** | Produits premium, expériences VIP, offres réservées aux membres | Utilise le positionnement premium et le langage mettant en avant un accès privilégié. | <li>« Invitation exclusive à un aperçu privé » <li>« L’adhésion Elite déverrouille l’analyse avancée » <li>« Rejoignez certaines entreprises du Fortune 500 qui nous utilisent déjà » |
| **Gamification** | Campagnes d’engagement, programmes de fidélité, contenu interactif | Utilise les mécaniques de jeu et le langage de réussite. | <li>« Déverrouiller votre prochain niveau de récompense » <li>« Défis complets pour gagner des badges » <li>« Grimper le classement pour des prix exclusifs » |
| **Informatif** | Formation, recherche, produits complexes, expertise reconnue | Utilise des faits, des données, des informations et des explications. | <li>« 5 informations à partir de l’analyse de plus de 10 000 interactions » <li>« Une nouvelle recherche révèle 3 approches révolutionnaires » <li>« Guide complet d’implémentation de l’IA dans le marketing » |
| **Formation et informations** | Contenu d’apprentissage, tendances du secteur, bonnes pratiques | Fournit des connaissances précieuses et des points à retenir exploitables. | <li>« Découvrir les techniques avancées avec un guide expert » <li>« Découvrez les 7 stratégies utilisées par les principaux professionnels du marketing » <li>« Découvrez comment optimiser votre workflow en 5 étapes » |

### Définissez le bon ton. {#tone}

Le ton influence la perception et la réaction de votre audience face à votre message. Sélectionnez toujours un ton qui correspond à l’image de votre marque et à l’étape du parcours des profils.

Passez en revue les options de tonalité disponibles, y compris le moment où chacune fonctionne le mieux et des exemples de contenu adaptés à chaque style.

| Ton | Idéal pour | Exemple de contenu |
| ---- | ----- | ----- |
| Professionnel | Communications B2B, annonces formelles | « Nous avons le plaisir d’annoncer notre partenariat stratégique… » |
| Empathique | Assistance clientèle, sujets sensibles | « Nous comprenons à quel point cette question doit être frustrante pour vous... » |
| Humoristique | Campagnes attrayantes, contenu léger | « Avertissement : peut entraîner de sérieux gains de productivité ! » |
| Enthousiaste | Lancements de produits, promotions d’événements | « C&#39;est le moment que vous attendiez ! » |
| Inspirant | Campagnes de motivation, objectif de la marque | « Ensemble, nous pouvons changer le monde… » |
| Persuasif | Campagnes commerciales, conversions | « Ne manquez pas cette occasion unique de… » |
| Amical | Engagement des clientes et clients, messages de bienvenue | « Heureux d&#39;être ici avec nous ! » |
| Formel | Communications juridiques, notifications officielles | « Il s’agit d’une notification des modifications suivantes... » |
| D’excuse | Rétablissement du service, résolution des problèmes | « Bodea s’excuse sincèrement pour tout désagrément causé... » |
| Affirmé | Contenu de leadership, messages faisant autorité | « Voici ce que vous devez faire maintenant… » |
| Storytelling | Narrations sur la marque, liens émotionnels | « Tout a commencé par une simple question… » |
| Conversationnel | Campagnes d’accompagnement, création de relations | « Parlons de la façon dont ce programme peut vous aider... » |

## Contenu de référence optimisé {#reference-content}

>[!TIP]
>
>Si vous avez déjà chargé une ressource par l’intermédiaire du menu **[!UICONTROL Référencer le contenu]**, vous n’avez pas besoin de la référencer dans votre invite. Le système utilise automatiquement tous les documents sélectionnés.

Les fichiers de contenu de référence fournissent des informations factuelles qui enrichissent votre contenu généré avec des détails spécifiques et précis. Lorsque vous chargez des documents, tels que des brochures de produit ou des livres blancs, modifiez votre invite pour indiquer les parties ciblées :

* **Au lieu de** _« Utilise la brochure produit »,_ **écrivez** _« Concentre-toi sur les fonctionnalités de sécurité avancées et les certifications de conformité, en particulier la conformité à la norme SOC 2 et le chiffrement des données »_

* **Au lieu de** _« Référence les études de cas »_ **écrivez** _« Mets en évidence les résultats du retour sur investissement des clientes et clients du secteur de la santé, en particulier la réduction de 40 % des coûts au centre médical régional »_

* **Au lieu de** _« Inclus les détails techniques »_ **écrivez** _« Mets l’accent sur les fonctionnalités d’intégration d’API et les avantages pour l’équipe de développement, en te concentrant sur les points d’entrée de l’API REST et le SLA à 99,9 % de disponibilité »_

### Raffinement du contenu

Une fois le contenu généré, utilisez la fonction **_[!UICONTROL Affiner]_** pour l’itérer et l’améliorer avec les options suivantes :

* **[!UICONTROL Développer]** - L’assistant d’IA peut vous aider à développer des sujets spécifiques, en fournissant des détails supplémentaires pour une meilleure compréhension et un meilleur engagement.

* **[!UICONTROL Résumer]** - La longueur des informations peut surcharger les visionneuses de pages. Utilisez l’Assistant IA pour condenser des points clés en résumés clairs et concis qui attirent l’attention et incitent à poursuivre la lecture.

* **[!UICONTROL Reformuler]** - Réécrivez le message tout en préservant sa signification. Cette option vous permet de générer une autre formulation, d’améliorer le flux ou d’ajuster les expressions sans modifier le message principal.

* **[!UICONTROL Utiliser un langage plus simple]** - Simplifiez le langage, en assurant la clarté et l’accessibilité pour une audience plus large.

* **[!UICONTROL Traduire]** - Traduisez le texte dans une autre langue. (Actuellement, l’anglais est la seule langue prise en charge.)

* **[!UICONTROL Modifier le ton]** - Ajustez le ton du message pour l’aligner sur votre style de communication, par exemple en le rendant plus convivial, professionnel, urgent ou inspirant.

* **[!UICONTROL Modifier la stratégie de communication]** - Modifiez l’approche de messagerie en fonction de vos objectifs, tels que la création d’une urgence ou l’accentuation d’un appel passionnant.
