---
title: Configurations de Forms
description: Découvrez comment configurer des paramètres prédéfinis de formulaire.
feature: Setup, Channels
role: Admin
autotag-review: '2026-05-27T16:06:59.553Z'
TQID: 'https://experienceleague.adobe.com/GFW5SZ5Z-phoEIE6jTVD7EgwcT1Vx647mjoLXJejbFg'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: d6e625c1-468f-4d73-9f32-fd1edb87f96bid: f01b5556-e951-40ba-8625-2e3001864f2b
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 955fac784a8f438ec2f9aaf66e9aaeefda58e2a7
workflow-type: tm+mt
source-wordcount: 542
ht-degree: 16%

---

# Configurations de Forms

Avant que les marketeurs puissent [créer et publier des formulaires](../content/forms.md) à utiliser dans leurs pages de destination, un administrateur de produit doit créer un ou plusieurs paramètres prédéfinis dédiés. Chaque paramètre prédéfini définit le point d’entrée de connexion utilisé pour envoyer les données d’envoi du formulaire et le jeu de données utilisé pour stocker les données capturées.

Lorsque des données arrivent sur le point d’entrée de diffusion en continu, elles sont liées aux informations du jeu de données. À l’aide des connexions source/cible générées et du flux source, les données sont ensuite intégrées au jeu de données.

>[!BEGINSHADEBOX]

## Conditions préalables

Pour utiliser les formulaires web, vous devez disposer d’une ou de plusieurs connexions en continu d’API _**HTTP**_ définies dans Adobe Experience Platform. Assurez-vous que chaque connexion que vous souhaitez utiliser répond aux exigences suivantes :

* Le type de données doit être défini sur XDM (et non sur Données brutes).
* L&#39;authentification doit être désactivée (connexion non authentifiée)

Pour plus d’informations sur la création de connexions source par flux, consultez la documentation d’[__](https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/streaming/http).

La configuration du canal Forms dans Journey Optimizer B2B edition nécessite les [autorisations](../admin/user-management.md#b2b-product-permissions) suivantes :

* _[!UICONTROL Configurations de canal B2B]_ > _[!UICONTROL Afficher les paramètres prédéfinis Forms]_ - Obligatoire pour afficher les configurations des paramètres prédéfinis de formulaire.
* _[!UICONTROL Configurations de canal B2B]_ > _[!UICONTROL Gérer les paramètres prédéfinis Forms]_ - Requis pour créer, mettre à jour et supprimer des configurations de paramètres prédéfinis de formulaires.
* _[!UICONTROL Configurations de canal B2B]_ > _[!UICONTROL Publication de paramètres prédéfinis Forms]_ - Obligatoire pour publier les configurations de paramètres prédéfinis de formulaires.

>[!ENDSHADEBOX]

## Instructions de configuration relatives aux paramètres prédéfinis de formulaire

Lors de la création d’un paramètre prédéfini :

* Vous pouvez configurer plusieurs préréglages à l’aide de différentes combinaisons de jeux de données et de connexions en streaming.

* Vous pouvez réutiliser le même jeu de données ou la même connexion en continu sur plusieurs paramètres prédéfinis.

* Chaque connexion en continu génère automatiquement des ressources, telles que :

   * _Connexion Source_ - emplacement d’où proviennent les données.
   * _Connexion cible_ - emplacement de stockage ou d’utilisation des données.
   * _Flux Source_ - pipeline qui déplace les données de la connexion source vers Experience Platform. Il gère le mappage, la transformation et la validation.

## Créer un paramètres prédéfini de formulaire

1. Dans le volet de navigation de gauche, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]**.

1. Sous _[!UICONTROL Paramètres de formulaire]_ dans le panneau de navigation, sélectionnez **[!UICONTROL Paramètres prédéfinis de formulaire]**.

   ![Accéder aux configurations de formulaire](./assets/config-channels-forms.png){width="800" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Créer un paramètre prédéfini de formulaire]**.

1. Saisissez un **[!UICONTROL Nom]** unique (obligatoire) et un **[!UICONTROL Description]** (facultatif) pour la configuration.

   >[!NOTE]
   >
   >Les noms doivent commencer par une lettre (A-Z) et ne peuvent contenir que des caractères alphanumériques. Vous pouvez également utiliser des `_` de soulignement, des `.` de point et des tirets `-`.

1. Sélectionnez la **[!UICONTROL Connexion en continu]**.

   Cette connexion est le point d’entrée de diffusion en continu utilisé pour envoyer les données lorsqu’une visionneuse web envoie un formulaire. Si la connexion en continu nécessaire n’apparaît pas dans la liste, vérifiez que les exigences sont remplies.

1. Cliquez sur l’icône _Sélectionner un jeu de données_ ( ![Icône Sélectionner un jeu de données](../assets/do-not-localize/icon-select-data.svg) ) pour lier un jeu de données au formulaire.

   Le jeu de données est l’endroit où les réponses du formulaire sont stockées et reflétées. Vous pouvez saisir une chaîne de texte pour rechercher un jeu de données spécifique ou le sélectionner dans la liste.

   ![Boîte de dialogue Sélectionner un jeu de données](./assets/config-channel-forms-select-datasets.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >Actuellement, seuls les jeux de données [Adobe Experience Platform activés et non activés pour Profil](https://experienceleague.adobe.com/fr/docs/experience-platform/catalog/datasets/overview) sont disponibles pour sélection. Un seul jeu de données peut être sélectionné à la fois. Les jeux de données système ne peuvent pas être utilisés pour enregistrer les données de formulaire.

   Cochez la case du jeu de données et cliquez sur **[!UICONTROL Sélectionner]**.

1. Cliquez sur **[!UICONTROL Enregistrer comme brouillon]**.

## Publication d’un paramètre prédéfini de formulaire

1. Cliquez sur le nom du paramètre prédéfini de formulaire pour ouvrir la page de configuration.

   Si nécessaire, vous pouvez apporter des ajustements au brouillon.

1. Cliquez sur **[!UICONTROL Publier]**.

   Lorsque le paramètre prédéfini de formulaire est répertorié avec un statut _Publié_, il est disponible pour être utilisé lors de la création du formulaire.
