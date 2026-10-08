---
applyTo: "**/*.md"
source-git-commit: 0f90b37c1ed8e4da0840f64179a0e99e0fe786d7
workflow-type: tm+mt
source-wordcount: '5174'
ht-degree: 1%
---

# Documentation d’Adobe Experience League : instructions de code Claude

Vous assistez un rédacteur technique dans le référentiel de documentation publique Adobe Experience League (`journey-optimizer-b2b.en`). Chaque élément de contenu que vous rédigez, modifiez ou révisez DOIT respecter toutes les règles ci-dessous. En cas de doute sur la terminologie, consultez les wikis référencés en utilisant l&#39;outil Confluence MCP (`mcp__adobe-wiki-confluence`).

---

## &#x200B;1. Voix, ton et style

### Écriture axée sur l’utilisateur

Centrez l’utilisateur et non la fonction. Écrivez ce que l’utilisateur ou l’utilisatrice peut **faire**, et non ce que la fonction fait.

- Utiliser la deuxième personne (« vous ») et l&#39;humeur impérative pour les instructions.
- Utilisez « vous » lorsque vous parlez d’eux-mêmes à l’audience, et non « les utilisateurs ». Le terme « utilisateurs » est acceptable lorsqu’il fait référence à un rôle (par exemple, un administrateur gérant les utilisateurs).
- ÉVITEZ « La fonction X vous permet de... » ou « La fonction X vous permet de... ». Mettez l&#39;utilisateur comme sujet ou utilisez l&#39;humeur impérative.
  - Mauvais : « L’API du serveur peut être utilisée sur les serveurs ».
  - Méthode acceptable : « Utiliser l’API du serveur sur les serveurs ».
  - Mauvais : « Les champs calculés permettent de créer des valeurs... »
  - Méthode acceptable : « Utiliser des champs calculés pour créer des valeurs... »
- Soyez attentif à « vous pouvez ». Elle est appropriée mais peut être utilisée à l&#39;excès, créant des phrases répétitives ou verbeuses.
- Utilisez « select » pour choisir des options dans une liste ou mettre le texte en surbrillance. N’utilisez le « clic » que pour les actions explicites de la souris. Évitez de nommer le type de contrôle (bouton, lien), sauf si cela est nécessaire pour la levée de l’ambiguïté.
- Utilisez « Ouvrir » / « Fermer » pour les applications et les fenêtres ou panneaux principaux.
- Utilisez « Quitter » pour quitter un site ou une expérience (par exemple, « Quitter Report Builder »).
- Utilisez « accéder à » ou « accéder à » pour la navigation.
- Utilisez « Lire la vidéo » et non « Regarder la vidéo ». Tout le monde ne regarde pas.
- Utilisez « Afficher », « Afficher » ou « Tout afficher », et non « Tout voir ». Tout le monde ne voit pas.
- Utilisez « connexion » / « déconnexion », et non « connexion » / « déconnexion ».
- Évitez d’utiliser « afin de ». Utilisez « to » à la place.
- Évitez « utiliser ». Utilisez plutôt « use ».
- Évitez les adjectifs vagues tels que « rapide » ou « facile ». Soyez précis : « Ce processus prend généralement 5 minutes. »
- Évitez les adverbes faibles : très, extrêmement, incroyablement.

### Structure de phrase et de paragraphe

- Cible ≤20 mots par phrase (le guide de création indique ≤35 max). Une pensée par phrase.
- Paragraphes : 125 mots au maximum, idéalement 100 ≤. 4 à 5 phrases maximum. Pas de murs de texte.
- Utilisez une voix active. Évitez les constructions et les nominalisations passives (par exemple, utilisez « créer » et non « création »).
- Utilisez une structure objet-verbe-objet simple.
- Evitez les faux sujets (« C&#39;est... », « Il y a... »).
- Utilisez le même mot de manière cohérente. Ne faites pas pivoter les synonymes.
- Pas d&#39;humour, d&#39;argot, de jargon, ou d&#39;exemples spécifiques à la culture (doit bien se localiser).
- Utilisez la virgule Oxford dans les listes de trois éléments ou plus.
- Écrivez les nombres entiers de zéro à neuf ; utilisez les chiffres de 10 et plus.
- Pas de point-virgule. Utilisez plutôt un point et une nouvelle phrase.

### Scannabilité

- Les lecteurs doivent saisir la portée de l’article uniquement à partir du titre, des en-têtes et des légendes.
- 2 à 5 sous-sections maximum par section.
- Cible 7 étapes par tâche ; 10 est le maximum pratique. Diviser les procédures plus longues en sous-tâches.
- 8 éléments maximum par liste à puces.
- Utilisez des tableaux lorsqu’ils facilitent l’analyse des listes de termes/définitions.
- Le contenu doit avoir une note inférieure à la 10e année lors d’un test de lisibilité (après avoir supprimé les noms et titres appropriés).

### Écriture pour la découverte de l’IA

Les assistants d’IA et les outils de recherche font de plus en plus apparaître le contenu Experience League dans les réponses générées.

- Insérez des termes clés (noms de produits, noms de fonctionnalités, tâches) dans le corps du texte et le texte du lien, pas seulement dans les images ou les tableaux complexes. Les systèmes d’IA reposent sur du texte lisible.
- Écrivez des en-têtes et des premiers paragraphes clairs et autonomes. Les outils de l&#39;IA les extraient souvent de manière isolée : ils doivent avoir un sens sans contexte environnant.
- Faites des phrases courtes et directes. Une prose concise est plus facile à analyser et à citer avec précision pour l’IA.
- Utilisez des formats structurés (étapes numérotées, puces courtes, en-têtes de style définition) pour les procédures et les comparaisons. La structure aide l’IA à identifier la bonne réponse.
- Incluez des synonymes ou d’autres termes lors de la première utilisation (par exemple, « ECID (Experience Cloud ID) ») pour améliorer la récupération des expressions de requête variées.
- Assurez-vous que les champs de métadonnées (titre, description, balises de fonctionnalité) sont complets et précis.

---

## &#x200B;2. Syntaxe d’Adobe Markdown (Experience League)

### FrontMATTER (obligatoire sur chaque fichier)

```yaml
---
title: Title Case Title Here
description: Learn how to... or Learn about... (150-160 chars, sentence case).
---
```

Champs facultatifs supplémentaires utilisés dans ce référentiel : `solution`, `type`, `role`, `exl-id`. Correspond au modèle des fichiers existants.

**IMPORTANT :** N’ajoutez PAS de `exl-id` lors de la création d’une page. Il est généré automatiquement au moment de la publication. Seuls les champs `exl-id` qui existent déjà sur les pages existantes doivent être conservés.

**Règles de métadonnées de titre :**

- Casse du titre (placez uniquement la casse du titre sur Experience League).
- 60 caractères maximum (anglais). Le système ajoute automatiquement des `| Adobe Experience Platform`. Fais entrer ça dans la longueur.
- N’ajoutez PAS le canal ou le nom du produit. Il est ajouté automatiquement.
- Considérez-le comme la version SEO du nom de votre page (ce que les utilisateurs recherchent).
- Titre du concept : substantif (par exemple, « Rapport Pages vues »).
- Titre de la tâche : expression verbale (par exemple, « Créer un segment pour les pages vues »).
- Les acronymes ne sont pas approuvés par Marketing pour la plupart des utilisations, mais une utilisation limitée est acceptable pour l’optimisation du moteur de recherche, les entrées de table des matières, les métadonnées de description et les en-têtes dont la longueur pose problème.

**Règles de métadonnées de description :**

- Cas de condamnation. 150 à 160 caractères idéalement ; 160 caractères max.
- Une à deux phrases concises. La première phrase résume ; la seconde est un call to action.
- Commencez les descriptions de concept par « En savoir plus sur... ». ou « Comprendre... ».
- Commencez la description des tâches par « Découvrez comment... » ou un verbe impératif.
- Ne commencez PAS par le nom du produit. Commencez par le verbe SEO.
- Ne copiez PAS le premier paragraphe mot pour mot (objectif différent).
- Si un champ de métadonnées commence par une balise `[!DNL]` ou ``, placez la valeur entière du champ entre guillemets ou la validation échoue.

### Titres

- `#` = H1 (titre de l’article, un par page). `##` = sections principales H2. `###` = H3, etc.
- Ne sautez PAS les niveaux de cap (p. ex., ne sautez pas de H2 à H4).
- Cible ≤5 mots. 69 caractères maximum (anglais).
- Ligne vide avant ET après chaque en-tête.
- Chaque titre doit être suivi d&#39;au moins une phrase du corps du texte. N’empilez JAMAIS deux en-têtes ou ne placez jamais une note, une liste ou un tableau directement sous un en-tête sans paragraphe au préalable.
- Identifiants d’ancre personnalisée : `## Section title {#section-id}` (minuscules, avec traits d’union, pas de points).
- Évitez les noms d’ancre entrant en conflit avec JavaScript/CSS : recherche, résultats, contenu, en-tête, pied de page, navigation, barre latérale, pagination, etc.
- Ne placez PAS de badges ou d’éléments Markdown dans le texte de titre.
- N’utilisez PAS de titres abstraits composés d’un seul mot tels que « Présentation » ou « Introduction ». Décrivez toujours le sujet de la présentation ou de l’introduction.
- Ne PAS numéroter les H1s. Pour les tutoriels, utilisez « Étape 1 : ... » dans des sous-positions plutôt que dans des ancres numérotées.
- Cas de phrase pour tous les en-têtes (sauf les noms propres et les éléments d’IU).
- En-têtes de concept : noms et groupes nominaux (par exemple, « Présentation de la segmentation »).
- En-têtes de tâche : verbes impératifs (par exemple, « Créer un workflow de ciblage »). Évitez les rebonds (-ing forms).
- Évitez de nouer des verbes avec -ment ou -ion (utilisez « Créer une feuille de route » et non « Création d’une feuille de route »).
- Maintenir la structure de titre parallèle dans les sections.
- Aucun ID d’ancre d’en-tête en double dans un document.
- Si un en-tête comprend des chiffres, spécifiez un identifiant d’en-tête explicite qui ne commence pas par un nombre (par exemple, `## Release notes for 2016 {#release-notes-2016}`).

### Liens

- Références croisées internes : chemins relatifs à la racine commençant par `/help/` : `[link text](/help/path/to/file.md)`
- Liens profonds vers les ancres : `[text](/help/path/to/file.md#anchor-id)`
- Liens externes (hors de ce référentiel) : URL de `https://` absolues. Celles-ci s’ouvrent automatiquement dans un nouvel onglet.
- Ouvrez explicitement dans un nouvel onglet : ajoutez `{target="_blank"}` (utilisez pour les liens entre guides).
- Liens de référence (à l’aide du style `[1]: url`) : ne fonctionnent qu’avec des URL absolues.
- N’ajoutez PAS le même fichier plusieurs fois dans une table des matières.
- Évitez les URL brutes dans le corps du texte. Utilisez toujours un texte de lien descriptif.
- N’utilisez jamais « cliquer ici » ou « lien » comme texte du lien. Les lecteurs d’écran font apparaître les liens hors contexte et ne peuvent pas distinguer plusieurs instances « cliquez ici ».
- Le texte du lien doit rendre la destination claire par lui-même.
- Pour les listes de renvois « Plus d’informations », utilisez un sous-titre `More help on this topic` avec une liste à puces.

### Images

- Syntaxe : `![alt text](path/to/image.png)`
- Redimensionner : `{width="300"}` ou `{width="50%"}`
- Aligner : `{align="center"}` ou `{align="right"}`
- Zoomable : `{zoomable="yes"}`
- Affichage modal : `{modal="regular"}`. Ne PAS combiner avec un lien.
- Largeur recommandée : 640 à 2000 px. Taille de fichier maximale : 5 Mo recommandé ; limite de 100 Mo. 100 images maximum par article.
- Les images se trouvent dans un sous-dossier `assets/` relatif au fichier Markdown.
- Les images qui NE DOIVENT PAS être localisées se trouvent dans un sous-dossier `do-not-localize/`.
- Prenez toujours des captures d’écran à l’aide du thème **Clair** dans l’interface utilisateur du produit Experience Cloud, et non du thème Sombre.
- Ne PAS afficher les données client dans les captures d’écran
- Ne documentez PAS les interfaces tierces dans les captures d’écran. Créez plutôt un lien vers la documentation du tiers.
- N’utilisez PAS de captures d’écran uniquement pour suivre la progression sur les écrans ou afficher des éléments d’interface évidents.
- N’incluez PAS d’illustrations d’icônes facilement identifiables plus d’une fois par article.
- N’utilisez PAS d’images de code. Utilisez plutôt des blocs de code.
- N’utilisez PAS la couleur seule pour véhiculer l’information (non accessible aux utilisateurs daltoniens).
- N&#39;utilisez PAS de graphiques animés qui flashent plus de trois fois par seconde (risque de crise).
- Assurez-vous que les images sont bien contrastées et claires.
- Instructions relatives à la taille en pixels d’une capture d’écran : 2 000 px max. pour les grands, 672 px pour les moyens, 300 px pour les petits, 30 à 35 px pour les icônes.
- Pour les légendes : utilisez une hexadécimale rouge n° EB1000, un épaisseur de ligne de 3 px, un rayon de coin de 8 px.

### Texte alternatif

Le texte secondaire est indexé par Google et lu par les lecteurs d’écran. Écrivez-le toujours avec soin.

- Décrivez ce que l’image montre, pas seulement le nom de l’écran.
- Utilisez des phrases complètes avec une grammaire et une ponctuation correctes.
- Incluez le texte approprié de l’image.
- Utilisez des mots complets, et non des abréviations. Les lecteurs d’écran épellent des abréviations.
- Ne commencez PAS par « Cette image montre... ». Décrivez simplement le contenu directement.
- Le texte secondaire n’est généralement pas nécessaire pour les images purement décoratives, mais il est utile en cas de doute.

| Texte de remplacement adapté | Éviter |
|---|---|
| Copie d’écran du Créateur d’audience présentant les filtres démographiques géographiques et âge sélectionnés. | Créateur d’audience |
| Sélectionnez une extension dans le catalogue d’extensions. | Bibliothèque des extensions |

### Vidéos

- Syntaxe : `>[!VIDEO](https://video.tv.adobe.com/v/xxxxx/?quality=12&learn=on)`
- Ajoutez des `?quality=12&learn=on` à la fin de toutes les URL de vidéo pour une lecture optimale.
- Les vidéos ne doivent PAS être lues automatiquement. N’ajoutez pas de `?autoplay=true` dans la documentation.
- Fournissez toujours un texte de remplacement, une transcription ou un lien vers des instructions écrites : « Pour les instructions écrites, voir [lien]. »
- Utilisez des légendes significatives.
- Activez les transcriptions avec des `{transcript=true}` sur des vidéos individuelles ou ajoutez des `auto-video-transcripts: true` aux `TOC.md` pour un guide entier.

### Remarques et avertissements

```markdown
>[!NOTE]
>
>Note content here.

>[!TIP]
>
>Tip content here.

>[!IMPORTANT]
>
>Important content here.

>[!WARNING]
>
>Warning content here.

>[!CAUTION]
>
>Caution content here.
```

Types supplémentaires : `[!ADMIN]`, `[!AVAILABILITY]`, `[!PREREQUISITES]`, `[!INFO]`, `[!ERROR]`, `[!SUCCESS]`.

Règles de syntaxe CRITIQUES :
- Il DOIT y avoir une ligne de `>` vide entre la ligne de balise et le contenu.
- Chaque ligne de suite doit commencer par `>`.
- La syntaxe de citation en bloc (`>` sans balise ) est prise en charge, mais le rendu est effectué en tant que citation en bloc simple. Ne l’utilisez PAS en attendant des légendes stylisées.
- N’ajoutez PAS de commentaires dans les composants de bloc tels que les listes à puces, en particulier les listes à puces imbriquées. Le commentaire peut modifier le rendu de la liste.

### Onglets

```markdown
>[!BEGINTABS]

>[!TAB Tab label]

Tab content here.

>[!TAB Another tab]

More content.

>[!ENDTABS]
```

- N’imbriquez PAS les onglets.
- N’imbriquez PAS les ensembles d’onglets dans des listes.
- Les titres des onglets ne peuvent pas être formatés en gras ou en italique.
- La recherche sur la page (Ctrl+F) ne trouve pas de contenu dans les onglets masqués.

### Sections réductibles

```markdown
+++Click to expand
Content here.

* Bullet one
* Bullet two

+++
```

- Ajoutez des lignes vides au-dessus et en dessous des listes et des blocs de code dans les réductibles.
- N’imbriquez PAS les sections réductibles dans des sections réductibles.
- Les en-têtes à l’intérieur des éléments réductibles sont autorisés, mais pas recommandés.
- Remarque : la fonction Rechercher dans la page (Ctrl+F) détecte le texte réduit dans Chrome, mais pas dans Safari.

### Boîtes de dialogue

```markdown
>[!BEGINSHADEBOX "Optional Title"]

Content with gray background.

>[!ENDSHADEBOX]
```

### Blocs de code

- En ligne : `` `code` `` de backticks simples. À utiliser pour les noms de cookies, les noms de fichiers, les valeurs, les paramètres, les commandes et les exemples d’URL qui ne doivent pas être validés.
- Blocs clôturés : triple backticks avec identifiant de langue (active la mise en surbrillance de la syntaxe et un bouton Copier).
- Attributs facultatifs : `{line-numbers="true"}`, `{start-line="7"}`, `{highlight="11-13, 16"}`
- Les blocs de code ne sont PAS localisés. Pas besoin d&#39;y ajouter DNL ou UICONTROL.
- Utilisez des accents graves (et non des guillemets) pour le code, les noms de fichier, les paramètres et le texte saisi.
- N’utilisez PAS d’images de code. Utilisez toujours des blocs de code.

### Badges

- En ligne : `[!BADGE Beta]{type=Informative}`
- Métadonnées (au-dessus de H1) : `badgePremium: label="Premium" type="Positive"`
- Types : `Informative` (bleu), `Positive` (vert), `Negative` (rouge), `Neutral` (gris foncé), `Caution` (jaune)
- 2 badges maximum dans les métadonnées par article.
- Ne placez PAS de badges dans les en-têtes.
- N&#39;utilisez PAS de badges pour les renseignements qui deviennent rapidement obsolètes (p. ex., « Nouveau »).
- Les libellés des badges sont localisés. Soyez concis.
- Pour le badge Beta, utilisez uniquement l’`badgeBeta` frontMATTER. Ne placez PAS de badge intégré dans le H1.
- Si vous souhaitez qu’une URL de badge s’ouvre dans un nouvel onglet, ajoutez `newtab=true` à la syntaxe du badge.

### Listes

- Utilisez `*` ou `-` de manière cohérente dans un seul article. Vérifiez la convention du fichier existant. Le mélange des marqueurs entraîne une erreur de validation.
- Pour les listes numérotées, utilisez `1.` pour chaque élément. GitHub/EDS les numérote automatiquement correctement.
- Listes à puces : lorsque l’ordre n’est pas important. Listes numérotées : pour les étapes et les procédures ordonnées.
- Pour une procédure en une seule étape, utilisez une puce (`*`) au lieu de `1.`.
- Conserver les entrées de liste brèves. Généralement une phrase ou moins.
- Utilisez des points pour les phrases complètes ; omettez des points pour les entrées d’un seul mot ou d’une phrase incomplète (appliquez la règle de manière cohérente dans une liste).
- Ne terminez PAS les éléments de liste par des points-virgules, des virgules ou des conjonctions telles que « and » ou « or » lorsque les éléments sont destinés à être lus comme une simple série.
- Toutes les entrées de liste doivent être grammaticalement parallèles.
- Mettre en retrait le contenu imbriqué : 3 espaces pour les listes numérotées et 2 espaces pour les listes à puces.
- Entourez les listes de lignes vides.
- N’utilisez PAS de listes de tâches (cases à cocher `- [ ]` de style GitHub). Elles ne sont pas prises en charge dans Experience League.

### Tableaux

- Utilisez des tableaux Markdown standard.
- Pour les mises en page complexes (cellules fusionnées, bordures désactivées), HTML `<table>` est autorisé.
- Entourez les tableaux avec des lignes vides.
- Utilisez des `{style="table-layout:auto"}` pour les tableaux à largeur automatique si nécessaire.
- Évitez les captures d’écran dans les cellules du tableau. De petites icônes ou miniatures sont acceptables dans les cellules.

### Aperçu de la mise en surbrillance des fonctionnalités

Utilisez une plage pour le contenu de prévisualisation en ligne et une balise div pour le contenu de prévisualisation multi-paragraphes :

```markdown
<span class="preview">This feature is in limited availability.</span>
```

```markdown
<div class="preview">

Multiple paragraphs of preview content here.

</div>
```

### Fragments de code et inclusions

```markdown
{{$include /path/to/snippet.md}}
```

Utilisez pour les blocs de contenu réutilisables partagés dans plusieurs articles.

### Caractères spéciaux

- Échappez les caractères spéciaux du corps de texte avec une barre oblique inverse : `\#`, `\*`, `\[`, `\]`.
- Utilisez des entités HTML pour les chevrons : `&lt;`, `&gt;`, `&amp;`.
- Utilisez des entités HTML pour les symboles spéciaux : `&reg;`, `&mdash;`, `&ndash;`.

### Commentaires

Utilisez les commentaires d’HTML pour le texte de brouillon ou les notes d’autres auteurs :

```markdown
<!-- This is a comment. Not rendered in the published doc. -->
```

Les commentaires sont visibles pour les utilisateurs qui les modifient sur GitHub.com. N’incluez PAS d’informations confidentielles dans les commentaires.

N’ajoutez PAS de commentaires à l’intérieur des composants de bloc tels que les listes à puces (en particulier les listes imbriquées). Les commentaires peuvent interrompre le rendu de la liste. Dans les fichiers TOC.md, ne commentez pas les lignes au milieu de la liste de table des matières : déplacez plutôt les commentaires à la fin du fichier.

### Actions au clavier

Mettez en gras chaque touche individuelle dans un raccourci clavier : **cmd** + **shift** + **p**.

### Dénomination des fichiers et des dossiers

- Noms de fichier Markdown : minuscules avec des tirets. Pas de majuscules, de traits de soulignement, de points ou d’espaces.
- Utilisez des slugs descriptifs : `create-calculated-metric.md`, `calculated-metric-overview.md`. Évitez les noms de fichier tels que `overview.md` ou `introduction.md`, sauf si l’IA requiert un nom fixe.
- Évitez les noms de fichier en conflit avec JavaScript/CSS : `metadata.md`, `search.md`.
- Noms de fichiers de ressources : minuscules préférées ; majuscules et traits de soulignement autorisés, mais non recommandés.

---

## &#x200B;3. Balises de localisation (CRITIQUE)

Appliquez toujours des balises de localisation. La traduction automatique s’exécute automatiquement à chaque validation dans la version principale.

### `[!DNL Product Name]` : Ne Pas Localiser

Utilisez pour les noms de produits de marque qui doivent rester en anglais.

**Appliquer à:**
- Noms de produits Adobe : `[!DNL Analytics]`, `[!DNL Target]`, `[!DNL Campaign]`, `[!DNL Experience Platform]`
- Noms de produits tiers : `[!DNL Mozilla Firefox]`, `[!DNL Workfront]`
- Noms fonctionnels qui peuvent perturber la traduction : `[!DNL Pass]`, `[!DNL Campaign]`
- Opérateurs booléens utilisés comme termes logiques : `[!DNL AND]`, `[!DNL OR]`

**Ne pas appliquer à :**
- URL, noms de fichiers ou noms de répertoires
- blocs de code (non localisés par défaut)
- Acronymes (rester en anglais automatiquement)
- Termes déjà présents dans la base de données Ne pas traduire

**Dans le texte du lien :** supprimez les crochets de balise pour éviter les problèmes de rendu. Utiliser `[Adobe](https://www.adobe.com)` non `[[!DNL Adobe]](https://www.adobe.com)`.

### `[!UICONTROL Label]` : contrôles de l’interface utilisateur

À utiliser pour les éléments d’interface : options, champs, onglets, pages, menus, boutons et noms de fonctionnalités tels qu’ils apparaissent dans l’interface utilisateur. Il s’agit de la balise la plus critique pour la qualité de la traduction. Traitez-la comme obligatoire dans les procédures.

**Appliquer à:**
- Chaque élément d’interface utilisateur cliquable dans les étapes de la procédure (obligatoire)
- Noms des fonctionnalités et éléments de navigation, tels qu’affichés dans le produit
- Noms de page, options, champs et onglets tels qu’ils sont libellés dans l’interface.

**Formatage:**
- Gras dans les étapes et la navigation : `Select **[!UICONTROL Destinations]** from the left navigation.`
- Italique acceptable dans le texte conceptuel (sans étape) pour plus de clarté.
- Dans les tableaux HTML : utilisez `<span class="uicontrol">term</span>` au lieu de ``.
- Dans le texte du lien : supprimez les crochets de balise.

**Majuscules :** faites correspondre exactement l’interface.

**Ne pas appliquer à :**
- Termes génériques utilisés conceptuellement : « segment », « mesure », « campagne » (balise uniquement lorsqu’elle fait explicitement référence à un élément de l’interface utilisateur)
- Phrases longues (sauf si le nom de l’élément d’interface utilisateur est lui-même une expression longue)
- Blocs de code ou acronymes
- Descriptions des icônes. Utilisez le nom de l’icône en forme de pointeur ou d’info-bulle s’il est disponible ; ne balisez pas les descriptions génériques telles que « icône de crayon ».

### `[!DONOTLOCALIZE]` : exclure des sections entières

Développez le contenu qui doit rester en anglais dans tous les paramètres régionaux :

```markdown
>[!DONOTLOCALIZE]
>
>Content that must not be translated.
```

Non nécessaire dans les blocs de code. Ils ne sont pas localisés par défaut.

### Où les balises peuvent et ne peuvent pas être utilisées

**Peut être utilisé dans** paragraphes, listes, titres, tableaux, badges, texte secondaire et métadonnées.

**Ne peut pas être utilisé dans :** blocs de code, acronymes.

**Règle de métadonnées :** si un champ de métadonnées (titre ou description) commence par une balise `[!DNL]` ou ``, placez toute la valeur du champ entre guillemets ou la validation échoue.

---

## &#x200B;4. Structure des informations et types de contenu

### Trois types de contenu : conservez-les séparés

- **Concept** : Quoi et pourquoi. Présentations, aperçus, contexte. Utilisez des en-têtes de nom/substantif-expression.
- **Tâche** : Comment. Procédures détaillées. Utilisez des en-têtes de verbe impératif. Toujours précédée d&#39;un concept.
- **Référence** : champs, paramètres, options, codes d’erreur. Utilisez des tableaux. Collecter avec d’autres documents de référence.

### Structure de l’article

- Ouvrez avec un contexte conceptuel qui oriente le lecteur.
- Ensuite, passez aux tâches, puis aux documents de référence.
- Répondez à une question précise par page. Pas trop large, pas trop étroit.
- Page de concept avec pages de tâches enfants (plusieurs pages) OU Concept H1 + Sous-titres de tâches H2 (une seule page).
- Introduisez une fois des synonymes ou d’anciens noms (par exemple, « ECID (Experience Cloud ID) ») pour connecter les termes de recherche.

### Étapes

- Chaque étape est une commande unique : une phrase complète avec un point (ou deux points si vous introduisez une sous-liste).
- Les étapes commencent toujours par un verbe ou l’objectif précédant l’action : « Pour exécuter le rapport, sélectionnez Exécuter ».
- Combinez de petites actions qui se produisent au même endroit dans l’interface utilisateur en une seule étape lorsque la phrase reste claire.
- Cible 7 étapes par tâche ; 10 est le maximum pratique. Diviser les tâches plus longues en sous-tâches.
- Utilisez une seule puce (non `1.`) pour une procédure qui ne comporte qu’une seule étape.
- N’utilisez PAS de titres comme étapes dans la documentation du produit. Pour les longs tutoriels de plusieurs pages, utilisez des sous-titres de style « Étape 1 : ... » si nécessaire.
- Placez les informations de l’étape (texte explicatif) en retrait sur une nouvelle ligne après l’étape.
- Placez des captures d’écran mises en retrait après l’étape ou l’action qui entraîne l’affichage de l’écran.
- Répétez les noms de pages, d’onglets ou de panneaux par étapes pour que les lecteurs sachent où ils se trouvent.

### Fichiers de table des matières (TOC.md)

- Cas de phrase pour toutes les entrées (noms propres et éléments d’IU exceptés).
- Entrées de concept : noms et groupes nominaux.
- Entrées de tâche : verbes impératifs (non redondants).
- Gardez les entrées parallèles.
- Chaque en-tête de section de la table des matières doit avoir un ID d’ancrage valide : `+ Processing rules {#processing-rules}`
- Un en-tête de section (parent) dans la table des matières ne peut pas être un lien. Il doit avoir un ID d’ancrage.
- N’ajoutez PAS le même fichier plusieurs fois dans une table des matières.
- Ne commentez PAS les lignes au milieu d’une liste de table des matières. Déplacez les commentaires vers la fin du fichier.

### Masquage des fichiers dans la navigation

Utilisez la méthode **V2** pour toutes les nouvelles tâches. La méthode V1 est obsolète.

**V2 (actuel) : `{hide-from-toc}` dans TOC.md**

Placez le `{hide-from-toc}` directement dans `TOC.md` avant l’article ou la section à masquer. Ne l’ajoutez PAS à l’article frontMATTER.

```
+ {hide-from-toc} [Article title](filename.md)
+ {hide-from-toc} Section name {#section-id}
  + [Nested article](nested.md)
```

- Les articles masqués restent accessibles via une URL directe.
- Une section dont les entrées sont toutes masquées disparaît elle-même du volet de navigation de gauche.

**V1 (obsolète) : `hidefromtoc: yes` dans le frontMATTER**

```yaml
hidefromtoc: yes
```

Ne l’utilisez PAS sur les nouvelles pages. L’article doit toujours apparaître dans `TOC.md` pour être publié, mais il ne s’affichera pas dans le volet de navigation de gauche.

**Se cacher des moteurs de recherche : `hide: yes` dans le front**

```yaml
hide: yes
```

Cela exclut la page de la recherche externe et interne. La définition de `hide: yes` définit automatiquement les `index: no`. Utilisez cette fonction en plus de la `{hide-from-toc}` lorsque vous souhaitez masquer une page de la navigation et de la recherche.

---

## &#x200B;5. Terminologie et valorisation de marque

Source faisant autorité : [wiki de terminologie AEP destinée aux utilisateurs](https://wiki.corp.adobe.com/spaces/DMSArchitecture/pages/1230620427/Adobe+Experience+Platform+User-Facing+Terminology). Consultez toujours l&#39;outil Confluence MCP (`mcp__adobe-wiki-confluence`) pour obtenir la dernière version.

### Noms de produits

Utilisez toujours ces formulaires exacts. Insérez « Adobe » à la première référence d’un guide ; vous pouvez le laisser tomber dans les mentions suivantes lorsque la politique le permet.

NE FAITES PAS précéder les noms de produits de « le », à moins que le nom officiel ne l&#39;indique.
- Correct : « Prise en main de l’assistant AI ».
- Incorrect : « Prise en main de l’assistant AI ».

| Correct | NE JAMAIS utiliser |
|---|---|
| Adobe Experience Platform | AEP, AXP, Adobe XP, Adobe Cloud Platform |
| Experience Platform (référence secondaire) | Platform (seule, sauf si le contexte est sans ambiguïté) |
| Adobe Real-Time CDP | RTCDP, ARTCDP |
| Real-Time CDP (secondaire) | Real-Time CDP (en minuscules « t ») |
| Adobe Real-Time Customer Data Platform | — |
| Real-time Customer Profile | Profil client en temps réel, profil unifié |
| Adobe Journey Optimizer | AJO |
| Adobe Journey Optimizer B2B Edition | AJO B2B |
| Prime B2B Adobe Journey Optimizer | Prime B2B AJO |
| Adobe Marketo Optimizer | AMO |
| Adobe Marketo Engage | Marketo (peut être utilisé comme adjectif) |
| Adobe Customer Journey Analytics | CJA |
| Customer Journey Analytics (secondaire) | — |
| Adobe Real-Time CDP Collaboration | RTCDP Collaboration, RTCDP Collab, Collab |
| Connexions Adobe Real-Time CDP | Connexions RTCDP, Connexions AEP, Connexions (seules) |
| Adobe Experience Platform Edge Network | Platform Edge Network, Platform Edge, Adobe Experience Edge |
| Balises (nom du produit) | Launch (obsolète) |
| Gestion des décisions | Offer Decisioning (entre parenthèses uniquement : « anciennement Offer Decisioning ») |
| flux de données (un mot, en minuscules) | flux de données, configuration edge |
| Analysis Workspace | analysis workspace, workspace, Workspace |
| Adobe AI | Sensei (obsolète) |
| Adobe GenAI | — |
| Adobe GenStudio for Performance Marketing | — |

**« Temps réel »** utilise toujours le R majuscule et le T majuscule lorsqu’ils font partie d’un nom de produit (Real-Time CDP, profil client en temps réel, Real-Time Customer Data Platform).

**Éditions** : « éditions » est en minuscules de manière générique ; « Édition » est mis en majuscules dans le cadre du nom d’une édition de produit (par exemple, « Adobe Real-Time CDP B2C Edition »).

**Abréviations dans les communications externes** : n’abrégez PAS les noms de produit dans la documentation destinée aux utilisateurs. Pas d’AEP, de CJA, d’AJO ou de RTCDP dans les documents. Exceptions limitées : les acronymes peuvent apparaître entre parenthèses lors de la première utilisation lorsqu’ils facilitent l’optimisation pour les moteurs de recherche, ou dans les entrées de table des matières, les métadonnées de description et les en-têtes lorsque la longueur pose problème.

### Terminologie des fonctionnalités et des concepts

| Correct | NE PAS utiliser |
|---|---|
| transfert d’événement | transfert côté serveur, Launch côté serveur |
| placer sur la liste autorisée | whitelist |
| PLACE SUR LA LISTE BLOQUÉE / | mettre sur liste noire |
| principal/réplica OU principal/secondaire (serveurs) | maître/esclave |
| principal (branche GitHub) | maître |
| pirate éthique | pirate à chapeau blanc |
| remarketing | reciblage |
| groupe de champs | mixin (obsolète), extensions, mixins |
| expiration automatique des données | TTL, durée de vie, expiration |
| sandbox hors production | évaluation (comme nom d’environnement) |
| définition de segment | segment (seul, au sens de la définition) |
| ID (toujours en majuscules) | ID |
| ingestion / ingérer / ingérer | intégration (pour ajouter des données à Platform) |
| jeu de données / jeux de données | Fichier de données, fichiers de jeux de données |
| contrôle d’accès | autorisations (pour la fonctionnalité Platform) ; |
| widget | carte de mesures (obsolète) |
| variable d’espace réservé | variable factice |
| indisponible/verrouillé/désactivé/désactivé | grisé |
| contrôle de cohérence | contrôle de santé mentale |
| intégré | natif (comme synonyme de natif) |
| priorité élevée | clouer |
| hérité | clause de droits acquis |
| principal/principal/source | maître (comme descripteur) |

**Majuscules spécifiques à Analytics :**
- Les noms des panneaux sont en minuscules : vide, attribution, expérimentation, à structure libre (exception : « zone de travail de Parcours »).
- Les noms des visualisations sont en minuscules : barre, anneau, histogramme, ligne, arborescence, texte

### Termes internes uniquement : NE JAMAIS utiliser dans les documents publics

Ces termes apparaissent dans Jira, les wikis et les discussions internes, mais ne doivent jamais apparaître dans la documentation :

| Terme interne | Utiliser plutôt |
|---|---|
| AEP | Adobe Experience Platform |
| PALMIER | gestion des sandbox/contrôle d’accès |
| BIOME | environment |
| Hydrate / hydratation | créer/remplir |
| Profil unifié | Real-time Customer Profile |
| Évaluation (environnement) | sandbox hors production |
| DTM | Balises |
| Locataire | Organisation/organisation IMS |
| CRUD | créer, lire, mettre à jour et supprimer (épeler) |
| Siphon, BSO, Ethos | noms de code internes, jamais externes |
| Houblon | RGPD interne/condition de contrôle d’accès |
| Fréquence | terme publicitaire non visible par l&#39;utilisateur |
| Pipeline | terme interne de l’infrastructure Adobe |

---

## &#x200B;6. Langue inclusive et accessibilité

### Principes linguistiques inclusifs

- Utilisez des termes non sexistes : « représentant commercial » et non « vendeur », « modérateur » et non « président ».
- Préférez la deuxième personne (« vous ») pour éviter les pronoms de genre.
- Utilisez le singulier « they » pour une personne dont le genre est inconnu. NE PAS l’utiliser.
- Incluez des noms de cultures non blanches dans des exemples (par exemple, Ayesha, Ibrahim, Vignesh, Quynh). N&#39;utilisez PAS uniquement des noms culturellement blancs (John, Bill, Karen, Amy).
- NE PAS confondre le sexe (homme/femme) avec le sexe (homme/femme).
- Capitalisez les nationalités, les peuples, les races (autres que les « blancs », selon l’API Stylebook) et les tribus.
- Utilisez le langage « personne d’abord » : « personnes qui utilisent la technologie d’assistance », et non « personnes handicapées ».
- Évitez les euphémismes comme « incapables ». Évitez les descripteurs utilisés comme noms : « aveugle », « sourd ».
- Évitez les termes qui reflètent l&#39;identité (appropriation culturelle) : animal spirituel, sherpa, pow-wow, gourou, ninja, tribu.

### Terminologie non exhaustive à éviter

| Utilisation | Non |
|---|---|
| / PLACER SUR LA LISTE AUTORISÉE / | liste blanche/liste noire |
| principal/réplica OU principal/secondaire | maître/esclave |
| principal (branche git) | maître |
| priorité élevée | clouer |
| variable d’espace réservé | variable factice |
| indisponible/verrouillé/désactivé/désactivé | grisé |
| contrôle de cohérence | contrôle de santé mentale |
| intégré | natif (comme synonyme) |
| autorité / expert | guru / ninja |
| membres de votre groupe | membres de votre tribu |
| réunion | pow wow / encerclez les wagons |
| modèle / esprit de parenté | animal spiritueux |
| guide | Sherpa |
| hérité | clause de droits acquis |
| entreprise futile | marche de la mort |
| ridicule / incompétent / imprévisible | stupide / boiteux / fou |
| pirate éthique / non éthique | chapeau blanc / chapeau noir hacker |
| Lire la vidéo | Regarder la vidéo |
| Afficher / Afficher / Tout accéder | Tout voir |

### Accessibilité : description de l’interface utilisateur

Ne décrivez PAS les éléments de l’interface utilisateur par couleur ou position de l’écran. La couleur ne fonctionne pas pour les utilisateurs daltoniens ou les lecteurs d’écran. La position de l’écran n’est pas fiable avec les technologies d’assistance.

**Utiliser un langage chronologique, pas un langage spatial :**

| Utilisation | Non |
|---|---|
| D&#39;Abord, Ensuite, Enfin | Au-Dessus, En Dessous |
| Dans la barre de menus | À gauche |
| Avant / Après | En haut/en bas de l’écran |

**Décrivez ce que font les commandes, et non leur apparence :**

| Utilisation | Non |
|---|---|
| Sélectionner une recherche | Cliquez sur l’icône de loupe |
| Modifier | L’icône en forme de crayon |
| Activé/Désactivé | Basculer / basculer / activer |
| Menu | Tiroir latéral |
| Saisir e-mail | Saisissez votre adresse e-mail |
| Enregistrez. | Le bouton « Enregistrer » |
| Annuler | Fermer |

N’utilisez PAS uniquement la couleur pour véhiculer l’information. Associez toujours la couleur au texte ou à la forme.

### Accessibilité : texte secondaire

- Décrivez ce que l’image montre, pas seulement son nom d’écran.
- Utilisez des phrases complètes avec une grammaire et une ponctuation correctes.
- Incluez le texte approprié de l’image.
- Utilisez des mots complets, et non des abréviations. Les lecteurs d’écran épellent des abréviations à haute voix.
- Les images qui véhiculent des informations indépendantes du texte environnant DOIVENT comporter du texte secondaire.
- Les images purement décoratives peuvent omettre le texte secondaire, mais il est recommandé de l’inclure.
- Testez des images avec un simulateur de daltonisme lorsque la couleur est utilisée pour donner du sens.
- N&#39;utilisez PAS de graphiques animés qui flashent plus de trois fois par seconde (risque de crise).

### Accessibilité : liens

- N’utilisez jamais « cliquer ici » ou « lien » comme texte du lien.
- Effacez la destination à partir du texte du lien uniquement.
  - Bonne : « Consultez les conditions préalables de RTCDP dans le Guide de l’utilisateur de RTCDP ».
  - Mauvais : « Cliquez ici pour consulter les conditions préalables. »

### Accessibilité : vidéos

- Les vidéos ne doivent PAS être lues automatiquement.
- Fournissez toujours un texte de remplacement, une transcription ou un lien vers des instructions écrites.
- Incluez des légendes significatives sur toutes les vidéos.
- Si possible, lien vers des instructions écrites : « Pour obtenir des instructions écrites, voir [lien]. »

---

## &#x200B;7. Orthographe et ponctuation

### Orthographe de l&#39;anglais américain

| Utilisation | Non |
|---|---|
| couleur | couleur |
| reconnaître | reconnaître |
| licence | licence |
| alors que | alors que |
| expiration | expiration |
| compteur | compteur |
| parmi | entre |

### Règles de ponctuation

- Les guillemets fermants se placent en dehors des virgules et des points.
- Réservez des guillemets pour citer des personnes. Ne mettez pas les chaînes de l’interface utilisateur entre guillemets (utilisez UICONTROL et gras dans les étapes).
- Utilisez l’italique pour les termes utilisés comme termes (et non les guillemets) : *profil*, et non « profil ».
- Utilisez des accents graves pour le code, les paramètres, les noms de fichier et le texte saisi : `datasetId`.
- Gras : uniquement pour les éléments de l’interface utilisateur dans les procédures (avec UICONTROL) et les termes clés lors de la première introduction. Les lignes de lead en gras sont acceptables dans les dispositions de FAQ qui n’utilisent pas de questions de niveau titre.
- Italique : pour mettre en évidence les mots étrangers, les termes définis ou les noms conceptuels dans un texte qui n’est pas une étape.
- Gras + italique combinés : `***text***`.
- N’utilisez PAS de règles horizontales (`---` ou `***`). Elles ne sont pas prises en charge dans Experience League.
- N’utilisez PAS de tirets cadratin (—), de tirets (-) ou de tirets en prose. Reformuler la phrase à la place. Les tirets ne sont autorisés que dans les adjectifs composés qui apparaissent dans l’interface utilisateur, les noms de fichier et le code.
- Deux-points : permet d’introduire une liste. Mettez une majuscule au premier mot après deux points lorsqu’une phrase complète suit (ou le mot est un nom propre).
- Pas de point-virgule. Utilisez plutôt un point et une nouvelle phrase.

---

## &#x200B;8. Optimisation du moteur de recherche et facilité de recherche

- Incluez des termes de recherche (mots-clés) dans les premiers paragraphes.
- Utilisez des termes que les lecteurs recherchent. Incluez des synonymes et des noms de termes précédents si nécessaire.
- Mots-clés dans les en-têtes : incluez les noms des fonctionnalités, les éléments d’interface et la tâche en cours d’exécution.
- Le texte secondaire sur les images est indexé par Google. Rendez-le descriptif et significatif.
- Évitez de placer des termes essentiels uniquement dans des tableaux ou des images complexes (non indexés de manière fiable par l’IA ou la recherche).
- Métadonnées de description : utilisez le langage naturel avec des mots-clés. N’entassez PAS de mots-clés aléatoires. Google peut rétrograder le contenu pour le remplissage de mots-clés.
- Veillez à ce que les champs de métadonnées (titre, description, balises de fonctionnalité) soient complets et précis. Les surfaces de découverte utilisent des métadonnées pour filtrer et classer les résultats avant de lire le contenu de la page.

---

## &#x200B;9. Conventions de fichier et de référentiel

- FrontMATTER est requis sur chaque fichier `.md`.
- Les images se trouvent dans un sous-dossier `assets/` relatif au fichier Markdown.
- Les images qui ne doivent pas être localisées sont placées dans un sous-dossier `do-not-localize/`.
- Les fichiers de table des matières (`TOC.md`) définissent la structure de navigation de gauche. Mettez-les à jour lors de l’ajout ou de la suppression de pages.
- Utilisez des liens relatifs à la racine (`/help/...`) pour les références croisées entre les documents de ce référentiel.
- Pour les liens vers des documents en dehors de ce référentiel, utilisez des URL de `https://experienceleague.adobe.com/...` absolus.
- Dénomination de la branche : aucun préfixe de nom d’utilisateur. Utilisez le numéro de ticket Jira et un titre avec titre (par exemple, `PLAT-12345-Update-Guardrail-Limits`). Nommez la branche et le titre de la requête de tirage au même format.
- Les composants discrets (en-têtes, blocs de code clôturés, listes) doivent être entourés de lignes vides.
- Un seul H1 (`#`) par document. La première ligne après le front doit être le H1.

---

## &#x200B;10. Vérifier la liste de contrôle

Lors de la révision ou de la modification de la documentation, vérifiez chaque élément ci-dessous.

**Voix et style**

- [ ] voix axée sur l’utilisateur. Aucun « vous permet de », « vous permet de »
- [ ] « vous » a utilisé au lieu de « utilisateurs » lors de l’adressage direct de l’audience
- [ ] Deuxième personne et humeur impérative dans les procédures
- [ ] Voix active dans
- [ ] Phrases ciblent ≤20 mots
- [ ] Pas d&#39;adjectifs vagues (« rapide », « facile »). Remplacez par des descriptions précises.
- [ ] Termes clés apparaissent dans le corps du texte (pas seulement dans les images ou les tableaux) pour la découverte de l’IA

**Structure et titres**
- [ ] en-têtes : casse de phrase, ≤5 mots/69 caractères, suivi du corps du texte, pas d’en-têtes empilés
- [ ] Aucun niveau d’en-tête ignoré
- [ ] en-têtes de concept sont des substantifs ; les en-têtes de tâche sont des verbes impératifs
- [ ] Target 7 étapes par tâche ; 10 max. Les procédures en une seule étape utilisent une puce, pas `1.`
- [ ] max. 8 éléments par liste à puces

**Terminologie**
- [ ] Noms et formulaires de produits corrects (section 5)
- [ ] Aucun terme obsolète : mixin, TTL, Offer Decisioning, Launch, profil unifié, temps réel (t minuscule), Sensei
- [ ] Aucun terme interne uniquement : AEP, PALM, BIOME, hydrate, staging, DTM, tenant, pipeline
- [ ] Aucun terme non inclusif : liste blanche, liste noire, maître/esclave, contrôle de la santé mentale, factice, grisé, indigène, gourou, ninja, animal spirituel, sherpa, marche de la mort, pow wow, tribu
- [ ] Non « le » avant les noms de produit (par exemple, pas « le Adobe Experience Platform »).

**Balises de localisation**
- [ ] `` sur tous les noms d’éléments de l’interface utilisateur ; en gras dans les étapes
- [ ] `[!DNL]` sur tous les noms de produits et de tiers
- [ ] opérateurs booléens identifiés : `[!DNL AND]`, `[!DNL OR]`
- [ ] Aucune balise dans les blocs de code
- [ ] Les champs de métadonnées commençant par une balise sont placés entre guillemets

**Syntaxe Markdown**
- [ ] Syntaxe correcte des avertissements (ligne de `>` vide entre la balise et le contenu)
- [ Les listes ] utilisent des marqueurs cohérents ; les listes numérotées utilisent des `1.` pour chaque élément
- [ ] Aucune liste de tâches (`- [ ]`)
- [ ] Aucune règle horizontale (`---` entre les contenus)
- [ ] Lignes vides entourant les en-têtes, blocs de code, listes et tableaux
- [ ] Aucune image de code. Utilisez des blocs de code.
- [ ] les captures d’écran utilisent le thème Clair ; aucune donnée client ; aucune interface utilisateur tierce

**Accessibilité**
- [ ] Texte secondaire : phrases complètes, mots complets, décrit le contenu (pas seulement le nom de l’écran)
- [ ] Pas de langage directionnel/spatial : pas de « au-dessus », « en dessous », « à gauche », « en haut à droite »
- [ ] texte du lien décrit la destination. Pas de « click here »
- [ ] vidéos non définies pour la lecture automatique ; transcriptions ou alternatives écrites fournies
- [ ] Aucune couleur utilisée seule pour véhiculer l’information

**Fichiers et liens**

- [ ] Matière première requise : titre (casse du titre, ≤60 caractères), description (150 à 160 caractères)
- [ ] Aucune URL nue dans le corps du texte. Utilisez toujours un texte de lien descriptif.
- [ ] liens internes relatifs à la racine ; liens absolus pour les références entre référentiels
- [ ] Les noms de fichier sont en minuscules, avec des tirets et des lignes de rappel descriptives (non `overview.md`)
- [ ] des images dans `assets/` ; images non localisées dans `do-not-localize/`

---

## &#x200B;11. Références externes

Utilisez l’outil MCP approprié en fonction du type de ressource :

- **tickets et événements Jira** (`jira.corp.adobe.com`) : utilisez l’outil MCP Jira Corp (`mcp__corp-jira`)
- **Pages Wiki / Confluence** (`wiki.corp.adobe.com`) : utilisez l&#39;outil Confluence MCP (`mcp__adobe-wiki-confluence`)
- **Pages web/Experience League publiques** : utilisez WebFetch

**Pages wiki internes (utilisez l’outil Confluence MCP) :**
- **wiki de terminologie** : https://wiki.corp.adobe.com/spaces/DMSArchitecture/pages/1230620427/Adobe+Experience+Platform+User-Facing+Terminology
- **Guide de style de Platform** : https://wiki.corp.adobe.com/spaces/DMSArchitecture/pages/1938986972/Platform+style+guide
- **Guide de l’accessibilité et de l’inclusivité** : https://wiki.corp.adobe.com/spaces/DMSArchitecture/pages/2234798784/Writing+for+accessibility+and+inclusivity
- **Guide des fenêtres contextuelles d’aide** : https://wiki.corp.adobe.com/spaces/DMSArchitecture/pages/2575057078/How+to+add+contextual+help+popovers+to+the+Experience+Platform+documentation+and+UI

**Public (utiliser WebFetch) :**
- **Présentation de la localisation** : https://experienceleague.adobe.com/en/docs/authoring-guide/using/authoring/localization/localization-overview
- **Référence des balises de localisation** : https://experienceleague.adobe.com/en/docs/authoring-guide/using/authoring/localization/localize
- **Syntaxe Experience League markdown**: https://experienceleague.adobe.com/en/docs/authoring-guide/using/markdown/markdown-syntax
- **Aide-mémoire de Markdown** : https://experienceleague.adobe.com/en/docs/authoring-guide/using/markdown/cheatsheet
- **Référence de style des notes de mise à jour** : https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/latest

**Clone local :**
- **Référentiel du guide de création :** utilisez une extraction disponible du guide de création d’Adobe Experience League ou de sa documentation publique.
