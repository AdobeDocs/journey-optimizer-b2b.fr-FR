---
title: Détails du compte
description: Découvrez comment accéder à des informations détaillées et à des résumés d’IA génératifs pour les comptes dans Journey Optimizer B2B edition.
feature: Account Insights
role: User
exl-id: 12be33de-0a43-43d9-90b8-fe4411a50599
source-git-commit: 31c79208503e01964475230ea950eb8bdfadd176
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 6%

---

# Détails du compte

Lorsque vous cliquez sur le nom d’un compte n’importe où dans Journey Optimizer B2B edition, la page _Détails du compte_ s’affiche. Cette page fournit des informations utiles sur le compte, y compris des résumés d’IA génératifs. Vous pouvez également exécuter des [actions](#account-actions) pour les contacts associés au compte.

![Accéder aux détails du compte](./assets/account-details.png){width="700" zoomable="yes"}

Utilisez l’onglet **[!UICONTROL Aperçu]** pour consulter des informations sur le compte, et l’onglet **[!UICONTROL Contacts]** pour accéder à une liste de contacts de compte.

## Onglet [!UICONTROL Aperçu]

La page Détails du compte se compose de trois sections principales :

### Présentation du compte

![Présentation du compte](./assets/details-page-account-overview.png){zoomable="yes"}

La section de présentation du compte comprend les informations de compte suivantes :

* Nom de compte
* Nombre de personnes dans le compte
* Secteur industriel
* Opportunités ouvertes
* Les trois parcours de compte les plus récents sur lesquels le compte est actuellement utilisé (cliquez sur le nom du parcours pour afficher la présentation du parcours [&#128279;](../journeys/journey-overview.md))
* Résumé IA générative du compte, qui comprend des informations sur les principaux groupes d’achats engagés.

### Données d’intention

Dans Journey Optimizer B2B edition, le modèle de détection des intentions prédit une solution/un produit ciblé avec un degré de confiance suffisamment élevé en fonction de l’activité du contact du compte. L’intention des contacts de compte peut être interprétée comme la probabilité d’avoir un intérêt pour un produit.

{{intent-data-note}}

![Données d’intention - détails du compte](./assets/intent-data-panel.png){width="700" zoomable="yes"}

* Niveaux d’intention
* Types de signal d’intention : mots-clés, produit et solution


### Couverture des contacts

![Couverture de contact du compte](./assets/details-page-contact-coverage.png){width="800" zoomable="yes"}

La section _[!UICONTROL Couverture des contacts]_ affiche le nombre de contacts du compte avec un rôle spécifique associé à un intérêt pour la solution. L&#39;affectation du rôle et de l&#39;intérêt de la solution est basée sur le modèle rôles du groupe d&#39;achat. Cliquez sur une cellule pour afficher les détails suivants :

* Description, au format suivant : _x personnes ont le rôle y pour z intérêt pour la solution_
* Colonnes
* Nom
* Compte
* Titre du traitement
* Groupe d’achat
* Score d’engagement de la personne
* Dernière activité
* Détails

Cliquez sur l’icône _Filtrer_ ( ![Icône Filtrer](../assets/do-not-localize/icon-filter.svg) ) en haut à gauche pour filtrer l’affichage des données à l’aide de l’un des attributs suivants :

* Intérêt de la solution
* Période

### Chevauchement des contacts

![Chevauchement des contacts de compte](./assets/details-page-contact-overlap.png){width="800" zoomable="yes"}

La section _[!UICONTROL Chevauchement des contacts]_ affiche les contacts du compte qui font partie de plusieurs groupes d’achat parce qu’ils sont associés à plusieurs centres d’intérêt pour la solution. Ces informations se présentent sous la forme d’un tableau avec les colonnes suivantes :

* Nom
* Titre du traitement
* Compte
* Intérêt de la solution

Cliquez sur l’_Informations_ ( ![icône Informations](../assets/do-not-localize/icon-info.svg) ) en regard du nom du contact pour afficher un tableau contenant les détails suivants :

* Groupe d&#39;achat (cliquez sur le nom pour ouvrir le [détails du groupe d&#39;achat](../buying-groups/buying-group-details.md))
* Rôle
* Intérêt de la solution
* Intention du produit (si [configuré](../admin/intent-data.md))
* Produit

Cliquez sur l’icône _Filtrer_ ( ![Icône Filtrer](../assets/do-not-localize/icon-filter.svg) ) en haut à gauche pour filtrer l’affichage des données à l’aide de l’un des attributs suivants :

* Intérêt de la solution
* Rôles

## Onglet [!UICONTROL Contacts]

Sélectionnez l’onglet **[!UICONTROL Contacts]** pour afficher la liste de toutes les personnes associées au compte qui se synchronise dans Experience Platform. Chaque contact répertorié inclut le nom, l’adresse e-mail et le score d’engagement.

![Détails du compte - Onglet Contacts](./assets/account-details-contacts-tab.png){width="700" zoomable="yes"}

## Envoyer un e-mail

Vous pouvez envoyer un e-mail approuvé par le spécialiste marketing à un ou plusieurs contacts sélectionnés (jusqu’à 50 à la fois) ou à tous les contacts du compte. La liste des e-mails disponibles se limite aux e-mails approuvés provenant de l’instance Marketo Engage connectée.

>[!BEGINTABS]

>[!TAB Tous les contacts de compte]

1. Dans l’onglet _[!UICONTROL Aperçu]_, cliquez sur **[!UICONTROL Envoyer un e-mail]** en haut à droite.

   ![Détails du compte - Sélectionner l’adresse e-mail](../accounts/assets/account-details-send-email.png){width="700" zoomable="yes"}

1. Dans la boîte de dialogue _[!UICONTROL Envoyer un e-mail]_, sélectionnez l’espace de travail Marketo Engage, puis cochez la case de l’e-mail à envoyer.

   ![Sélectionnez un e-mail à envoyer aux membres du groupe d’achat](../accounts/assets/account-details-send-email-dialog.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Envoyer]**.

>[!TAB Contacts sélectionnés ]

1. Dans l’onglet _[!UICONTROL Contacts]_, cochez les cases des contacts qui doivent recevoir l’e-mail.

1. En haut à droite ou dans la barre de sélection en bas, cliquez sur **[!UICONTROL Envoyer un e-mail]**.

   ![Onglet Membres - Envoyer un e-mail](../accounts/assets/account-details-send-email-selections.png){width="700" zoomable="yes"}

1. Dans la boîte de dialogue _[!UICONTROL Envoyer un e-mail]_, sélectionnez l’espace de travail Marketo Engage, puis cochez la case de l’e-mail à envoyer.

   ![Sélectionnez un e-mail à envoyer aux membres du groupe d’achat](../accounts/assets/account-details-send-email-dialog.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Envoyer]**.

>[!ENDTABS]
