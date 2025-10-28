---
title: Mappage de persona
description: Découvrez comment configurer le mappage des rôles pour le marketing B2B. Mappez les attributs de personne dans Journey Optimizer B2B edition pour créer des modèles de rôle et optimiser le ciblage des groupes d’achats.
feature: Setup, Buying Groups
role: Admin
source-git-commit: 6df235bc73066463e5fcfa71dc994f34e13e3ac0
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 1%

---

# Mappage de persona

Les personas sont un aspect clé dans une approche de marketing basé sur les comptes (ABM), car ils aident les spécialistes marketing à ajuster leurs stratégies en fonction des besoins, des préférences et des problèmes spécifiques des individus au sein des comptes cibles. Les marketeurs peuvent créer des profils détaillés pour chaque persona, y compris son passé, ses responsabilités, ses points faibles et ses canaux de communication préférés. Grâce à ces définitions, les administrateurs et administratrices peuvent configurer les rôles en fonction des attributs de personne dans Journey Optimizer B2B edition, de sorte que les modèles de rôles puissent utiliser des conditions de rôle rationalisées et cohérentes qui capturent ces rôles.

<!-- Currently there is no insight into what persona goes into what role. With buying group agent, when asked questions about, what should be the size of the buying group, what persona should be in that buying group, what role do they play, etc, then agent will analyze all the data, (opportunity data, engagement data, sales conversation, etc) and informs the user that the buying group needs 7 persona, e.g.CMO, VP of marketing, marketing leader, Marketing ops, etc. 

Then based on what agent informed, users can create a template with those personas. -->
Définition des rôles et limites d’utilisation :

* Vous pouvez définir jusqu’à 20 personnes dans la liste _[!UICONTROL Mappage des personnes]_.
* Chaque personnage peut inclure jusqu’à cinq attributs dans sa définition.
* Pour tous les rôles définis, vous pouvez utiliser jusqu’à dix attributs de personne différents.

>[!BEGINSHADEBOX]

**Cas d’utilisation : variations d’intitulé de la fonction**

De nombreuses équipes marketing et commerciales utilisent les intitulés de poste pour identifier différentes personnes au sein d’un compte. Mais les titres des contacts peuvent être incohérents et utiliser de nombreuses variations pour des rôles similaires. Lors de la création de modèles de rôles de groupe d&#39;achats, vous devrez peut-être définir toutes les fonctions associées possibles pour un rôle donné. Vous pouvez simplifier ces définitions et regrouper des personnes ayant des titres de poste similaires sous une seule persona déduite, que vous pouvez ensuite exploiter dans différents modèles de rôles pour les groupes d&#39;achat.

Par exemple, vous pouvez configurer une persona appelée _Gestion des produits_ et la définir à l’aide de l’attribut de titre de tâche pour les valeurs de _Gestionnaire des produits_, _Sr. Chef de produit_, _chef de produit principal_, _PM_, _Sr. PM_, _PM principal_ et _chef de produit principal_. Utilisez ensuite ce persona dans un modèle Rôles où la condition correspond sur _Persona est la gestion des produits_. En utilisant le persona configuré, la création de chaque modèle de rôle est rationalisée et ne nécessite pas de condition compliquée qui puisse correspondre à chaque fonction possible.

>[!ENDSHADEBOX]

## Accéder aux personnages configurés

1. Dans le volet de navigation de gauche, choisissez **[!UICONTROL Administration]** > **[!UICONTROL Configurations]**.

1. Cliquez sur **[!UICONTROL Mappage de personas]** dans le panneau intermédiaire pour afficher la liste des personas.

   ![Accéder aux rôles configurés](./assets/configuration-engagement-scoring-list.png){width="800" zoomable="yes"}

   À partir de cette page, vous pouvez [créer](#create-an-engagement-score-model), [modifier](#change-the-engagement-weighting-settings) ou [supprimer](#delete-a-persona) des personnages.

   La liste de mappage des personas. est organisé sous la forme d’un tableau et affiche en haut les personnages les plus récemment mis à jour (triés par _[!UICONTROL Dernière mise à jour]_). Vous pouvez personnaliser le tableau affiché en cliquant sur l’icône _Paramètres des colonnes_ ( ![Paramètres des colonnes](../assets/do-not-localize/icon-column-settings.svg) ) dans le coin supérieur droit, puis en cochant ou décochant les cases des colonnes.

![Colonnes à afficher dans la liste de mappage des rôles](./assets/configuration-engagement-scoring-list-columns.png){width="300"}

1. Pour accéder aux détails d’un persona, cliquez sur son nom.

### Personnages par défaut

La liste _Mappage de personas_ comprend cinq personnages par défaut définis en fonction de l’attribut de titre de la tâche. Vous pouvez modifier l’un de ces rôles par défaut en fonction des besoins de votre entreprise :

| Persona | Titres de poste |
| ------- | ---------- |
| Directeur exécutif / Vice-président exécutif - Directeur exécutif | PDG, DPI, directeur des technologies de l’information, directeur financier, vice-président exécutif de la stratégie |
| Vice-président principal/vice-président | Vice-président principal du marketing, vice-président directeur des ventes, vice-président directeur des opérations, vice-président directeur des produits, vice-président directeur informatique |
| Directeur principal / Directeur - Directeur principal / Directeur | Directeur de l’ingénierie, directeur principal des produits, directeur des finances, directeur du succès client |
| Gestionnaire principal / Gestionnaire - Gestionnaire principal / Gestionnaire | Responsable marketing principal, responsable informatique, responsable des opérations, responsable des ventes, responsable des ressources humaines |
| Contributeur individuel - Contributeur individuel | Responsable de compte, Ingénieur logiciel, Spécialiste marketing, Représentant du succès client |
| Analyste - Analyste | Analyste commercial, Analyste des données, Analyste des études de marché, Analyste financier, Analyste des opérations |
| Développeur - Développeur | Développeur front-end, Développeur back-end, Développeur full-stack, Développeur d’applications mobiles, Ingénieur DevOps |
| Professionnels - Professionnels | Spécialiste RH, Conseiller juridique, Responsable de la conformité, Chef de projet, Spécialiste des achats |
| Consultant - Consultant | Consultant en gestion, conseiller en TI, consultant en processus d&#39;affaires, consultant en marketing |
| Autres - Autres | Spécialiste de l&#39;industrie, conseiller indépendant, consultant indépendant, expert en la matière |

### Filtrage de liste

Pour localiser la personne de votre choix, utilisez les outils de recherche et de filtrage :

* Saisissez une chaîne de texte dans la barre de recherche pour faire correspondre les profils par nom,

  ![Filtrer les définitions d’événement affichées](./assets/configuration-events-defs-list-filtered.png){width="700" zoomable="yes"}

* Cliquez sur l’icône _Filtrer_ ( ![Icône Filtrer](../assets/do-not-localize/icon-filter.svg) ) en haut à gauche pour filtrer la liste affichée par attribut.

## Créer une persona

1. Dans le volet de navigation de gauche, choisissez **[!UICONTROL Administration]** > **[!UICONTROL Configuration]**.

1. Cliquez sur **[!UICONTROL Mappage de persona]** dans le panneau intermédiaire.

1. Cliquez sur **[!UICONTROL Créer une persona]**.

1. Saisissez un **[!UICONTROL Nom]** et un **[!UICONTROL Description]** uniques (facultatif) pour le persona.

1. Sélectionnez les attributs à utiliser pour faire correspondre le persona.

   * Cliquez sur **[!UICONTROL Sélectionner les attributs de personne]**.

   * Dans la boîte de dialogue, cochez la case de chaque attribut à mapper (cinq au maximum).

     Vous pouvez personnaliser le tableau affiché en cliquant sur l’icône _Paramètres de colonne_ ( ![Paramètres de colonne](../assets/do-not-localize/icon-column-settings.svg) ) dans le coin supérieur droit.

     Pour filtrer la liste des attributs par nom, saisissez une chaîne de texte dans la barre de recherche. Vous pouvez également cliquer sur l’icône _Filtrer_ ( ![Icône Filtrer](../assets/do-not-localize/icon-filter.svg) ) en haut à gauche pour filtrer la liste affichée par type, _Standard_ ou _Personnalisé_.

   * Cliquez sur **[!UICONTROL Enregistrer]**

     Les attributs sélectionnés sont renseignés dans la section _[!UICONTROL Attributs de persona]_.

1. Pour chaque attribut, saisissez les valeurs séparées par des virgules que vous souhaitez mettre en correspondance pour l’attribut.

   À la place d’une valeur, vous pouvez également ajouter une invite qui peut être utilisée pour identifier une correspondance. Par exemple, vous pouvez saisir :

1. Cliquez sur **[!UICONTROL Créer]**.

## Modifier une persona

Cliquez sur le nom du persona pour accéder aux détails du persona et les modifier,

## Supprimer une persona

La suppression d’un persona le supprime de la liste _Mappage des personas_ et il n’est plus disponible pour être utilisé dans les modèles de rôles.

1. Sur la page _[!UICONTROL Mappage de personas]_, recherchez le persona à supprimer.

1. En regard du nom, cliquez sur l’icône représentant des points de suspension (**...**) et choisissez **[!UICONTROL Supprimer]**.

1. Dans la boîte de dialogue de confirmation, cliquez sur **[!UICONTROL Supprimer]**.
