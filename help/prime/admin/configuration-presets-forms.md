---
title: Configuration de Forms
description: Espace réservé
autotag-review: '2026-06-12T22:44:42.084Z'
TQID: 'https://experienceleague.adobe.com/aJKRaYBEdieyIUsuszVy4g2LANEVLQP9aQfhhrKOhx0'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
  - id: f2da1b69-6919-4386-a5d2-9c7b5c9033db
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
  - id: d57c4909-c813-470d-ac87-cdd2d6b5f9dc
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 0e90250101eef0572af0382cc7d24bca727d2b75
workflow-type: tm+mt
source-wordcount: 541
ht-degree: 22%

---

# Configurations de Forms

Avant que les marketeurs puissent créer et publier des formulaires à utiliser dans leurs pages de destination, un administrateur de produit doit créer un ou plusieurs paramètres prédéfinis dédiés. Chaque paramètre prédéfini définit le point d’entrée de connexion utilisé pour envoyer les données d’envoi du formulaire et le jeu de données utilisé pour stocker les données capturées.

Lorsque des données arrivent sur le point d’entrée de diffusion en continu, elles sont liées aux informations du jeu de données. À l’aide des connexions source/cible générées et du flux source, les données sont ensuite intégrées au jeu de données.

>[!BEGINSHADEBOX]

## Conditions préalables

Pour utiliser les formulaires web, vous devez disposer d’une ou de plusieurs connexions en continu d’API _&#x200B;**HTTP**&#x200B;_ définies dans Adobe Experience Platform. Assurez-vous que chaque connexion que vous souhaitez utiliser répond aux exigences suivantes :

* Le type de données doit être défini sur XDM (et non sur Données brutes).
* L&#39;authentification doit être désactivée (connexion non authentifiée)

Pour plus d’informations sur la création de connexions source par flux, consultez la documentation d’[__](https://experienceleague.adobe.com/fr/docs/experience-platform/sources/ui-tutorials/create/streaming/http).

<!-- 
permissions coming in GA

Forms channel configuration in Journey Optimizer B2B Edition requires the following [permissions](../start/user-management.md#b2b-product-permissions):

* _[!UICONTROL B2B Channel Configurations]_ > _[!UICONTROL View Forms Presets]_ - Required to view forms preset configurations.
* _[!UICONTROL B2B Channel Configurations]_ > _[!UICONTROL Manage Forms Presets]_ - Required to create, update, and delete forms preset configurations.
* _[!UICONTROL B2B Channel Configurations]_ > _[!UICONTROL Publish Forms Presets]_ - Required to publish forms preset configurations.
-->

>[!ENDSHADEBOX]

## Instructions de configuration relatives aux paramètres prédéfinis de formulaire

Lors de la création d’un paramètre prédéfini :

* Vous pouvez configurer plusieurs préréglages à l’aide de différentes combinaisons de jeux de données et de connexions en streaming.

* Vous pouvez réutiliser le même jeu de données ou la même connexion en continu sur plusieurs paramètres prédéfinis.

* Chaque connexion en continu génère automatiquement des ressources, telles que :

   * _Connexion Source_ - emplacement d’où proviennent les données.
   * _Connexion cible_ - emplacement de stockage ou d’utilisation des données.
   * _Flux Source_ - pipeline qui déplace les données de la connexion source vers Experience Platform. Il gère le mappage, la transformation et la validation.

## Créer un paramètres prédéfini de formulaire {#create-preset}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_form_connection"
>title="Sélectionner le point d’entrée à utiliser"
>abstract="Définissez le point d&#39;entrée de streaming où les données sont envoyées lors de l’envoi du formulaire."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-platform/sources/ui-tutorials/create/streaming/http" text="Créer une connexion de streaming d’API HTTP"

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_form_dataset"
>title="Sélectionner un jeu de données"
>abstract="Définissez un jeu de données dans lequel les réponses du formulaire sont stockées et reflétées. Saisissez du texte pour rechercher un jeu de données spécifique ou sélectionnez-le dans la liste."

1. Dans le volet de navigation de gauche, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]**.

1. Sous _[!UICONTROL Paramètres de formulaire]_ dans le panneau de navigation, sélectionnez **[!UICONTROL Paramètres prédéfinis de formulaire]**.

   <!-- ![Access the form configurations](./assets/config-channels-forms.png){width="800" zoomable="yes"} -->

1. Cliquez sur **[!UICONTROL Créer un paramètre prédéfini de formulaire]**.

1. Saisissez un **[!UICONTROL Nom]** unique (obligatoire) et un **[!UICONTROL Description]** (facultatif) pour la configuration.

   >[!NOTE]
   >
   >Les noms doivent commencer par une lettre (A-Z) et ne peuvent contenir que des caractères alphanumériques. Vous pouvez également utiliser des `_` de soulignement, des `.` de point et des tirets `-`.

1. Sélectionnez la **[!UICONTROL Connexion en continu]**.

   Cette connexion est le point d’entrée de diffusion en continu utilisé pour envoyer les données lorsqu’une visionneuse web envoie un formulaire. Si la connexion en continu nécessaire n’apparaît pas dans la liste, vérifiez que les exigences sont remplies.

1. Cliquez sur l’icône _Sélectionner un jeu de données_ ( ![Icône Sélectionner un jeu de données](../../user/assets/do-not-localize/icon-select-data.svg) ) pour lier un jeu de données au formulaire.

   Le jeu de données est l’endroit où les réponses du formulaire sont stockées et reflétées. Vous pouvez saisir une chaîne de texte pour rechercher un jeu de données spécifique ou le sélectionner dans la liste.

   <!-- ![Select datasets dialog](./assets/config-channel-forms-select-datasets.png){width="500" zoomable="yes"} -->

   >[!NOTE]
   >
   >Actuellement, seuls les jeux de données [Adobe Experience Platform activés et non activés pour Profil](https://experienceleague.adobe.com/fr/docs/experience-platform/catalog/datasets/overview) sont disponibles pour sélection. Vous pouvez sélectionner un jeu de données à la fois. Les jeux de données système ne peuvent pas être utilisés pour enregistrer les données de formulaire.

   Cochez la case du jeu de données et cliquez sur **[!UICONTROL Sélectionner]**.

1. Cliquez sur **[!UICONTROL Enregistrer comme brouillon]**.

## Publication d’un paramètre prédéfini de formulaire

1. Cliquez sur le nom du paramètre prédéfini de formulaire pour ouvrir la page de configuration.

   Si nécessaire, vous pouvez apporter des ajustements au brouillon.

1. Cliquez sur **[!UICONTROL Publier]**.

   Lorsque le paramètre prédéfini de formulaire est répertorié avec un statut _Publié_, il est disponible pour être utilisé lors de la création du formulaire.
<!-- -->
