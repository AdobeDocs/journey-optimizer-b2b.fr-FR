---
title: Création d’e-mails
description: Utilisez les outils de conception d’e-mail de Journey Optimizer B2B Prime, notamment les modèles d’e-mail, les fragments, la personnalisation, le mode sombre et la validation.
autotag-review: '2026-06-12T22:51:19.543Z'
TQID: 'https://experienceleague.adobe.com/-mtyiJ98caCTuTKaZbzYrYKiQoxolq-hMw7p5h7bNpY'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e666e996-b2cf-4c45-8fc2-1c625212ababid: f01b5556-e951-40ba-8625-2e3001864f2bid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: e7bdffdc-2950-4be5-8c23-84240a995090id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 579f36911af99308294726e91e80c5d08015d5cf
workflow-type: tm+mt
source-wordcount: 2753
ht-degree: 2%

---

# Création d’e-mails

En [!DNL Adobe Journey Optimizer B2B Prime], l’espace de conception d’e-mail fournit une zone de travail visuelle dans laquelle les spécialistes marketing créent des e-mails. Les outils de conception d’e-mail des panneaux de gauche et supérieur (structures, composants de contenu, modèles, fragments, etc.) prennent en charge la création à partir de zéro par glisser-déposer. Vous pouvez également choisir de commencer à partir d’un modèle, de coller des HTML brutes ou d’assembler des messages à partir de fragments visuels réutilisables.

>[!IMPORTANT]
>
>Pour la configuration par l&#39;administrateur des sous-domaines, de l&#39;authentification, des groupes d&#39;adresses IP et des canaux e-mail, voir [délivrabilité des e-mails et configuration des canaux](../admin/configuration-email-deliverability.md).

En [!DNL Journey Optimizer B2B Prime], chaque e-mail est associé à une action _[!UICONTROL Envoyer un e-mail]_ dans un parcours. Le workflow complet, de la conception du parcours à la définition de l’e-mail, se produit dans une expérience continue. Lorsque vous [ajoutez un nœud _Envoyer un e-mail_](../marketing/action-nodes.md#add-an-action-node) à un parcours de personne, cliquez sur **[!UICONTROL Créer un e-mail]** pour lancer le processus de conception du contenu de l’e-mail.

Cette action lance l’espace de conception d’e-mail, dans lequel vous pouvez choisir la manière de concevoir votre e-mail à l’aide des options suivantes :

* [Concevez entièrement votre e-mail](#build-from-scratch) à l’aide de l’interface de conception visuelle. Créez le composant Disposition d’e-mail par composant en effectuant un glisser-déposer sur une zone de travail vierge. Cette méthode est recommandée pour créer de nouveaux modèles ou des e-mails ponctuels.

* Importez HTML dans l’éditeur de code ou travaillez côte à côte avec la zone de travail visuelle. Le workflow d’importation complet d’HTML avec les chargements .html et .zip figure dans la feuille de route de Beta.

* [Sélectionnez un modèle existant](#create-from-template) dans une liste de modèles d’e-mail intégrés ou personnalisés. Cette méthode est recommandée pour les cas d’utilisation d’e-mails répétables.

<!-- * Upload a design prototype (JPG, PNG, PDF, or Figma export) and have AI Assitant convert it into a responsive HTML email. (Image to HTML (Img2HTML) -->

## Outils de conception d’e-mails {#email-design-tools}

* **Barre d’outils supérieure :** Enregistrer, Précédent, Basculer vers l’éditeur de code, prévisualiser les contrôles.
* **Rail de gauche :** Structures (dispositions de colonnes), Contenu (texte, bouton, image, séparateur, social, HTML), Fragments, Modèles, Arborescence de navigation (hiérarchie de style DOM de l’e-mail).
* **Zone de travail centrale :** éditeur WYSIWYG avec aperçu pour ordinateur de bureau et appareil mobile.
* **Rail de droite :** paramètres et styles du composant actuellement sélectionné, y compris les propriétés de contenu, l’arrière-plan, la bordure, la marge intérieure et la personnalisation.

## Bonnes pratiques en matière de conception d’e-mail {#design-best-practices}

Le respect des bonnes pratiques HTML et CSS permet d’assurer un rendu cohérent entre les clients de messagerie.

| Approche | Instructions |
| -------- | -------- |
| **Recommandé** | Mises en page statiques basées sur des tableaux · Tableaux HTML et tableaux imbriqués · Largeurs de modèle de 600 à 800 px · CSS intégré simple · Polices sécurisées pour le Web |
| **À utiliser avec précaution** | Images d’arrière-plan (prise en charge limitée des clients) · Polices web personnalisées (définissez toujours une police de secours) · Dispositions plus larges que 800 px · Cartes graphiques |
| **Éviter** | JavaScript, iFrames ou Flash · Contenu audio ou vidéo intégré · Formulaires HTML · Dispositions basées sur des div |

>[!NOTE]
>
>Le contenu des e-mails doit également répondre aux exigences applicables en matière d’accessibilité numérique. Structurez les en-têtes de manière logique, fournissez du texte secondaire pour toutes les images et vérifiez le contraste des couleurs dans les modes clair et sombre.

## Création d’un email à partir d’un parcours {#email-from-journey}

1. Cliquez sur le bouton **[!UICONTROL Modifier l’e-mail]** pour passer à l’étape de configuration de l’e-mail.
1. Dans l’écran suivant, sélectionnez une configuration de canal créée précédemment dans le menu déroulant **[!UICONTROL Configuration du canal e-mail]**. Seules les configurations actives sont répertoriées.
1. Saisissez un libellé pour l’action (visible sur le canevas de parcours) et un nom d’e-mail interne.
1. Saisissez la ligne d&#39;objet.
1. Basculez éventuellement **[!UICONTROL Activer le suivi des URL]** pour ce nœud d’e-mail.
1. Cliquez sur **[!UICONTROL Modifier le contenu]** pour ouvrir l’espace de conception d’e-mail.

### Écran Modifier le contenu {#edit-content-screen}

À partir de cet écran, vous confirmez les détails de l’expéditeur (hérités de la configuration du canal), définissez la ligne d’objet et ouvrez l’espace de conception d’e-mail pour créer le corps. Le pré-titre est configuré dans l’espace de conception d’e-mail (voir [Définition du pré-titre](#preheader)).

* **Nom de l’expéditeur, Adresse électronique de l’expéditeur, Cci:** hérité de la configuration du canal. Lecture seule sur cet écran.
* **Objet :** obligatoire. Personalization est pris en charge.
* **Modifier le corps de l’e-mail :** ouvre l’espace de conception des e-mails.

>[!NOTE]
>
>La taille des e-mails est limitée à 100 Ko selon les bonnes pratiques des FAI. Prime vous avertit dans l’éditeur si vous dépassez cette limite. Les erreurs (objet manquant, corps manquant, configuration de canal supprimée) empêchent l’activation du parcours jusqu’à ce qu’elles soient résolues.

## Concevoir en partant de zéro {#design-from-scratch}

### Procédure : créer entièrement un e-mail {#build-from-scratch}

1. Dans le nœud d’e-mail de parcours, cliquez sur **[!UICONTROL Modifier le contenu]** → **[!UICONTROL Modifier le corps de l’e-mail]**.
1. Sur l’écran Créer votre e-mail , cliquez sur **[!UICONTROL Créer en partant de zéro]**.
1. Cliquez sur **[!UICONTROL Confirmer]** pour ouvrir une zone de travail vide.
1. Dans le rail de gauche, faites glisser une **[!UICONTROL Structure]** (1 colonne, 1:1, 2:2, n:n colonne) sur la zone de travail.
1. Faites glisser les composants **[!UICONTROL Contenu]** dans les colonnes de la structure : Texte, Bouton, Image, Diviseur, Réseau social, HTML.
1. Cliquez sur un composant de la zone de travail pour le sélectionner. Le rail de droite affiche les onglets Paramètres et Styles .
1. Utilisez l’onglet **[!UICONTROL Paramètres]** pour configurer des options spécifiques au composant (contenu textuel, source de l’image, URL du bouton).
1. Utilisez l’onglet **[!UICONTROL Styles]** pour configurer la marge intérieure, la bordure, l’arrière-plan, la police et la couleur.
1. Utilisez l’icône **[!UICONTROL Arborescence de navigation]** dans le rail de gauche pour passer d’un composant à l’autre d’un e-mail profondément imbriqué.
1. Basculez entre l’aperçu pour ordinateur de bureau et mobile à l’aide des icônes de la barre d’outils supérieure.
1. Cliquez sur **[!UICONTROL Enregistrer]** (ou utilisez la liste déroulante Enregistrer pour d’autres options d’enregistrement).
1. Cliquez sur **[!UICONTROL Précédent]** pour revenir aux propriétés de l’e-mail.

### Composants de contenu disponibles {#content-components}

| Composant | Description |
| --------- | ----------- |
| **Texte** | Texte enrichi avec mise en forme (gras, italique, taille de police, couleur, alignement, listes, liens). |
| **Bouton** | CTA cliquable. Prend en charge la couleur d’arrière-plan, la bordure, la marge intérieure, le comportement du pointeur et les URL personnalisées. |
| **Image** | Insérer à partir de Marketo Design Studio (sélecteur de ressources). Prend en charge le texte secondaire, l’alignement, le suivi des liens et des clics. |
| **Diviseur** | Règle horizontale avec épaisseur et couleur configurables. |
| **Social** | Icônes de réseaux sociaux avec configuration de lien. |
| **HTML** | Bloc HTML brut pour le contenu avancé. Utile pour incorporer des balises codées à la main. |

### Structures et dispositions de colonnes {#structures}

Les structures définissent la grille des colonnes de l’e-mail. Les structures disponibles sont les suivantes : 1 colonne, 1 :1 (deux colonnes égales), 1 :2/2 :1 (deux colonnes asymétriques), 1:1:1 (trois colonnes égales) et n:n (plusieurs colonnes personnalisées). Utilisez des structures pour contrôler la façon dont le contenu est redistribué sur les appareils mobiles : la plupart des structures sont réduites à une seule colonne sur des écrans étroits par défaut.

>[!TIP]
>
>Simplifiez la structure de votre e-mail. Les dispositions à deux ou trois colonnes offrent un rendu cohérent sur tous les clients de messagerie (en particulier Outlook et Gmail). Les structures profondément imbriquées peuvent rendre imprévisible.

### Définir le pré-titre {#preheader}

Le pré-titre est l’extrait de texte affiché après la ligne d’objet dans les aperçus de boîte de réception. Dans Prime, le pré-titre est configuré sur la zone de travail visuelle dans l’espace de conception de l’e-mail, et non sur l’écran des propriétés de l’e-mail à côté de l’objet.

1. Ouvrez l’e-mail dans l’espace de conception d’e-mail.
1. Dans la zone de travail, recherchez la zone de pré-titre en haut du corps de l’e-mail.
1. Cliquez dans la zone de texte Pré-titre et saisissez la copie de pré-titre.
1. Appliquez des jetons de mise en forme et de personnalisation selon vos besoins à l’aide des contrôles de texte enrichi.
1. Cliquez sur **[!UICONTROL Enregistrer]**

>[!TIP]
>
>Conservez votre pré-titre entre 40 et 100 caractères. Elle doit compléter l’objet (et non le répéter) et donner au destinataire une raison supplémentaire d’ouvrir l’e-mail.

## Utilisation de modèles {#templates}

Les modèles sont des dispositions d’e-mail réutilisables. Ils accélèrent la création d’e-mails, assurent la cohérence de la marque et facilitent la collaboration entre les équipes.

### Types de modèles {#template-types}

* **Exemples de modèles (prêts à l’emploi).** Environ 20 modèles prêts à l’emploi couvrant des cas d’utilisation courants (sensibilisation sur les comptes, invitations à des événements, formations, annonces de produits). Disponible immédiatement pour chaque client.
* **Modèles enregistrés (personnalisés).** Modèles créés par votre équipe : créés entièrement sous **[!UICONTROL Gestion de contenu]** → **[!UICONTROL Modèles]** ou enregistrés à partir d’un e-mail existant à l’aide de l’option « Enregistrer en tant que modèle ».

### Création d’un e-mail à partir d’un modèle {#create-from-template}

1. Dans le nœud d’e-mail de parcours, cliquez sur **[!UICONTROL Modifier le contenu]** → **[!UICONTROL Modifier le corps de l’e-mail]**.
1. Sur l’écran Créer votre e-mail , l’onglet **[!UICONTROL Exemples de modèles]** est sélectionné par défaut.
1. Parcourir la galerie. Utilisez la zone de recherche pour filtrer par nom ou par catégorie.
1. Passez à l’onglet **[!UICONTROL Modèles enregistrés]** pour afficher les modèles créés par votre équipe.
1. Cliquez sur la miniature d’un modèle pour le prévisualiser.
1. Cliquez sur **[!UICONTROL Utiliser ce modèle]** pour l’appliquer. Le contenu du modèle s’ouvre sur la zone de travail dans l’espace de conception d’e-mail.
1. Personnalisez le texte, les images et les liens. La structure héritée du modèle peut être modifiée comme un e-mail de A à Z.
1. Cliquez sur **[!UICONTROL Enregistrer]** → **[!UICONTROL Précédent]** pour revenir aux propriétés de l’e-mail.

### Création d’un modèle réutilisable {#create-reusable-template}

1. Accédez à **[!UICONTROL Gestion de contenu]** → **[!UICONTROL Modèles]**.
1. Cliquez sur **[!UICONTROL Créer un modèle]**.
1. Saisissez un nom et une description. Sélectionnez **[!UICONTROL E-mail]** comme canal.
1. Cliquez sur **[!UICONTROL Créer]**. L’espace de conception d’e-mail s’ouvre pour être modifié.
1. Créez le modèle (à partir de zéro, d’un modèle existant ou en collant HTML).
1. Activez éventuellement les **[!UICONTROL paramètres de gouvernance]** :
   * Autoriser la modification de la structure et du contenu : permet de déterminer si les auteurs d&#39;e-mails peuvent modifier la structure du modèle ou uniquement son contenu.
   * Verrouiller des composants spécifiques : permet de rendre des composants individuels en lecture seule lorsqu’ils sont utilisés dans un e-mail.
1. Cliquez sur **[!UICONTROL Enregistrer]** Le modèle est désormais disponible pour tous les utilisateurs dans la galerie Modèles enregistrés .

### Enregistrer un e-mail en tant que modèle {#save-as-template}

1. Ouvrez un e-mail existant dans l’espace de conception d’e-mail.
1. Dans le menu déroulant **[!UICONTROL Enregistrer]**, cliquez sur **[!UICONTROL Enregistrer comme modèle]**.
1. Saisissez un nom et une description.
1. Configurez éventuellement les paramètres de gouvernance.
1. Cliquez sur **[!UICONTROL Enregistrer]**

>[!NOTE]
>
>Les modèles enregistrés et leur contenu d’e-mail sont indépendants. La modification d’un modèle ne met pas à jour rétroactivement les e-mails créés à partir de celui-ci. Pour propager les modifications dans de nombreux e-mails, utilisez Fragments visuels au lieu de modèles.

## Fragments visuels {#visual-fragments}

Un fragment visuel est un bloc de contenu réutilisable (en-tête, pied de page, CTA, clause de non-responsabilité, ensemble de liens sociaux) qui peut être inséré dans de nombreux e-mails. Lorsque vous mettez à jour un fragment, la modification se propage automatiquement à chaque e-mail qui l’utilise. Les fragments sont la méthode recommandée pour appliquer la cohérence de la marque et centraliser les mises à jour de contenu.

### Création d’un fragment visuel {#create-fragment}

1. Accédez à **[!UICONTROL Gestion de contenu]** → **[!UICONTROL Fragments]**.
1. Cliquez sur **[!UICONTROL Créer un fragment]**.
1. Sélectionnez **[!UICONTROL Fragment visuel]** comme type. Saisissez un nom et une description.
1. Cliquez sur **[!UICONTROL Créer]**. L’espace de conception d’e-mail s’ouvre pour être modifié.
1. Faites glisser des structures et des composants de contenu sur la zone de travail pour créer le fragment (par exemple, une structure à 1 colonne avec une image de logo, un en-tête et une liste de liens de navigation).
1. (Facultatif) Marquez les champs comme **[!UICONTROL modifiables]** pour les rendre personnalisables par utilisation :
   * Sélectionnez un composant, puis ouvrez la section **[!UICONTROL Champs modifiables]** dans le rail de droite.
   * Ajoutez des champs avec des valeurs par défaut (par exemple, un champ source d’image avec une URL de logo par défaut, un champ de texte avec un titre par défaut).
   * Les auteurs d’e-mails utilisant le fragment peuvent remplacer ces champs sans rompre la structure du fragment.
1. Cliquez sur **[!UICONTROL Enregistrer]**

### Insertion d’un fragment dans un e-mail {#insert-fragment}

1. Ouvrez l’e-mail dans l’espace de conception d’e-mail.
1. Dans le rail de gauche, cliquez sur **[!UICONTROL Fragments]**.
1. Recherchez ou recherchez le fragment souhaité.
1. Faites glisser le fragment sur la zone de travail à l’emplacement souhaité.
1. Si le fragment comporte des champs modifiables, configurez les valeurs dans le rail de droite.
1. Cliquez sur **[!UICONTROL Enregistrer]**

>[!TIP]
>
>Utilisez des fragments pour tout contenu qui doit rester cohérent dans tous les e-mails : en-tête de marque, pied de page légal, barre de lien social, bloc de désabonnement. Lorsque l’équipe juridique met à jour la clause de non-responsabilité, vous modifiez un fragment et chaque e-mail est mis à jour.

## Personnalisation {#personalization}

Prime utilise la syntaxe Handlebars pour la personnalisation. Les jetons sont remplacés au moment de l’envoi par des valeurs provenant des données de profil de chaque destinataire.

### Emplacement de personnalisation {#where-you-can-personalize}

* **Objet** — Point de personnalisation le plus courant.
* **Pré-titre** : défini dans la zone de travail visuelle ; prend en charge les jetons d’attribut de profil.
* **Corps du texte de l’e-mail** — Prénoms et autres attributs de profil insérés en ligne.
* **URL des boutons** — ajoutez des paramètres par destinataire.

>[!NOTE]
>
>Seuls les attributs de profil sont disponibles dans l’éditeur Personalization dans cette version.

### Insérer un jeton de personnalisation {#insert-token}

1. Dans l’espace de conception d’e-mail (ou dans l’écran des propriétés de l’e-mail pour l’objet), cliquez sur le champ dans lequel vous souhaitez insérer un jeton.
1. Cliquez sur l’icône de personnalisation (souvent appelée **[!UICONTROL Ouvrir la boîte de dialogue de personnalisation]** ou **[!UICONTROL Ajouter une expression]**).
1. Dans la boîte de dialogue de personnalisation, parcourez l’arborescence du schéma sur la gauche. Les attributs de profil (prénom, nom, e-mail, fonction et autres champs de profil) sont répertoriés.
1. Sélectionnez un attribut. Prime insère l’expression Handlebars correspondante, par exemple `{{profile.firstName}}`.
1. Ajoutez une valeur de secours pour gérer les données manquantes : `{{profile.firstName | default: "there"}}`.
1. Cliquez sur **[!UICONTROL Confirmer]** ou **[!UICONTROL Insérer]**. L’expression apparaît en ligne dans le champ.

### Modèles de personnalisation courants {#personalization-patterns}

Utilisez des expressions Handlebars telles que celles-ci (la personnalisation utilise la même syntaxe décrite dans [Procédure pas à pas : insérez un jeton de personnalisation](#insert-token)) :

* **`{{profile.lastName}}`** — Insérer le nom du destinataire.
* **`{{profile.jobTitle}}`** — Référencez la fonction du destinataire dans la copie du corps.
* **`{{profile.firstName}}, ready to take the next step?`** — Combiner le jeton et le texte statique en ligne.

Pour un message d’accueil avec un prénom de secours en cas d’absence de valeur, utilisez l’assistant `default` comme indiqué dans les étapes de personnalisation précédentes (par exemple, prénom avec `"there"` par défaut).

### Helpers Handlebars {#handlebars-helpers}

En plus de `default`, l’éditeur de personnalisation comprend des assistants Handlebars intégrés pour la logique conditionnelle, la transformation du texte et la mise en forme de date. Utilisez le navigateur de fonctions de l’éditeur pour explorer les assistants disponibles et les insérer avec la syntaxe correcte.

>[!TIP]
>
>Dans l’espace de conception d’e-mail, saisissez `{{` directement dans un champ de texte pour déclencher une liste déroulante de saisie automatique intégrée répertoriant les attributs de profil disponibles. Il n’est pas nécessaire d’ouvrir la boîte de dialogue de personnalisation complète pour les insertions rapides.

### Expressions assistées par l’IA {#ai-personalization}

L’assistant d’IA de l’éditeur de personnalisation peut générer des expressions Handlebars à partir d’une description en langage clair, expliquer le rôle d’une expression existante et identifier les problèmes potentiels. Utilisez-la pour accélérer la création d’expressions, en particulier pour la logique conditionnelle ou les assistants de formatage de date.

## Ajout de ressources à partir de Marketo Design Studio {#marketo-assets}

Prime rend vos ressources Marketo Design Studio existantes disponibles dans l’espace de conception d’e-mail. Vous pouvez parcourir et insérer ces images dans vos e-mails directement à partir du sélecteur de ressources.

>[!IMPORTANT]
>
>La disponibilité des ressources dans Prime repose sur une **copie unique** vos ressources à partir de Marketo Design Studio. La modification des ressources dans Marketo Engage après la copie initiale n’est **pas** reflétée dans [!DNL Journey Optimizer B2B Prime].

### Types de fichier pris en charge {#asset-file-types}

* **Entièrement pris en charge (visible dans le sélecteur, incorporable en ligne) :** JPG, PNG, GIF, WebP.
* **Accessible avec caveat :** SVG (avec un avertissement indiquant que certains clients de messagerie ne rendent pas SVG).
* **Non pris en charge dans cette version :** TIFF, PDF, DOCX, XLSX, PPTX, CSS, JS, HTML, TXT, fichiers binaires, PSD, AI, INDD.

### Insertion d’une image à partir de Marketo Design Studio {#insert-image}

1. Dans l’espace de conception d’e-mail, faites glisser un composant de contenu **[!UICONTROL Image]** sur la zone de travail (ou cliquez sur une image existante pour la remplacer).
1. Dans le rail de droite, cliquez sur **[!UICONTROL Marketo Engage Assets]**.
1. Le sélecteur de ressources s’ouvre. Parcourir les dossiers ou rechercher par nom de fichier.
1. Sélectionnez la ressource souhaitée.
1. Cliquez sur **[!UICONTROL Sélectionner]**. L’image est insérée dans votre e-mail à partir de la copie de la ressource disponible dans Prime.
1. Dans le rail de droite, configurez les éléments suivants :
   * Texte secondaire (recommandé pour l’accessibilité et pour les clients qui bloquent les images par défaut).
   * Alignement.
   * Cible du lien — Rendez l&#39;image cliquable.
1. Cliquez sur **[!UICONTROL Enregistrer]**

## Mode sombre {#dark-mode}

Le rendu en mode sombre est pris en charge par le biais de requêtes multimédias CSS `prefers-color-scheme`. Les outils de conception d’e-mail comprennent un aperçu en mode sombre et des options permettant de définir un style personnalisé pour la prise en charge des clients de messagerie. Vous pouvez ainsi vérifier que le texte reste lisible, que les logos sont visibles et que les couleurs de la marque s’affichent sur des arrière-plans sombres.

Pour obtenir des conseils détaillés sur la prévisualisation, la configuration des paramètres personnalisés du mode sombre, la prise en charge des clients de messagerie et les bonnes pratiques de test, voir [Mode sombre pour le contenu des e-mails](./email-dark-mode.md).

## Valider le contenu d’un e-mail {#validation}

Pour que votre parcours puisse être activé, le contenu de l’e-mail doit être valide. Prime affiche les alertes au niveau du contenu sur l’e-mail et sur la zone de travail du parcours. Cette section couvre les alertes que vous pouvez voir et la manière de les résoudre.

### Alertes de contenu courantes et comment les résoudre {#content-alerts}

| Alerte | Signification | Comment résoudre |
| ----- | ------------- | -------------- |
| **L’objet est manquant** | Le champ Objet est vide. | Ouvrez l’e-mail et saisissez une ligne d’objet dans l’écran Modifier le contenu . Les jetons Personalization sont autorisés, mais le champ ne peut pas être vide. |
| **Le corps de l’e-mail est vide** | La zone de travail de l’espace de conception d’e-mail n’a aucun contenu. | Cliquez sur **[!UICONTROL Modifier le corps de l’e-mail]** pour ouvrir l’espace de conception d’e-mail. Faites glisser au moins un composant de structure et un composant de contenu sur la zone de travail, puis cliquez sur Enregistrer. |
| **Configuration de canal non sélectionnée** | Aucune configuration d’e-mail n’a été choisie pour le nœud d’e-mail. | Sur l’écran des propriétés de l’e-mail, sélectionnez une configuration de canal actif dans le menu déroulant **[!UICONTROL Configuration du canal e-mail]**. |
| **Configuration de canal supprimée** | La configuration de canal précédemment sélectionnée a été supprimée ou n’est plus active. | Ouvrez les propriétés de l’e-mail et sélectionnez une autre configuration de canal actif . Si aucun n’est disponible, un administrateur doit en créer ou en réactiver un. |
| **La taille de l’e-mail dépasse 100 Ko** | La taille totale de l’e-mail (HTML, CSS intégré, contenu codé) est supérieure à la limite des bonnes pratiques des FAI de 100 Ko. | Réduisez la taille de l’e-mail : remplacez les images intégrées volumineuses par des images hébergées en externe à partir de Marketo Design Studio, supprimez les CSS intégrés inutilisés et simplifiez les structures imbriquées. |
| **Jeton de personnalisation non résolu** | Un jeton Handlebars fait référence à un attribut de profil sans solution de secours et l’attribut peut être manquant pour certains destinataires. | Ajoutez une version de secours à l’aide de l’assistant `default` Handlebars, comme décrit dans [Personalization](#personalization). Vous pouvez également limiter l’audience par parcours aux profils où l’attribut est garanti. |
| **Image non chargée** | Un composant d’image fait référence à une ressource qui n’est plus disponible. | Cliquez sur l’image, ouvrez le sélecteur de ressources, puis sélectionnez à nouveau la ressource dans Marketo Design Studio. |

### Vérifier et résoudre les alertes {#resolve-alerts}

1. Ouvrez le parcours contenant le nœud d’e-mail. Les nœuds d’e-mail contenant des alertes non résolues sont marqués d’un badge rouge sur la zone de travail.
1. Cliquez sur le nœud d’e-mail pour ouvrir le rail de propriétés.
1. Consultez la section **[!UICONTROL Alertes]** sur le rail des propriétés. Chaque alerte renvoie vers le champ ou l’écran où le problème peut être résolu.
1. Résolvez chaque alerte à tour de rôle. Par exemple, saisissez une ligne d’objet manquante, sélectionnez une configuration de canal ou ouvrez l’espace de conception d’e-mail pour corriger le contenu.
1. Après avoir résolu toutes les alertes, cliquez sur **[!UICONTROL Enregistrer]** sur le nœud d’e-mail.
1. Confirmez que le badge rouge sur le nœud d’e-mail s’efface.

>[!NOTE]
>
>Les alertes doivent être effacées pour que le parcours puisse continuer. Les avertissements ne sont pas bloquants, mais ils doivent être examinés (par exemple, un e-mail qui utilise un jeton sans solution de secours peut s’afficher avec des valeurs vides pour certains destinataires).
