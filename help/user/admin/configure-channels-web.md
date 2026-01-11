---
title: Configurations du canal web
description: Découvrez comment configurer les paramètres du canal web pour définir les propriétés web et les règles de correspondance de page pour la diffusion de contenu dans Journey Optimizer B2B edition.
feature: Setup, Channels
role: Admin
badgeBeta: label="Beta" type="informative" tooltip="Cette fonctionnalité est actuellement en version bêta limitée"
source-git-commit: 2f9b007df233cf8a233c3646bf691b7cff139f86
workflow-type: tm+mt
source-wordcount: '1064'
ht-degree: 3%

---

# Configurations du canal web

Une configuration web est une propriété web identifiée par une URL où le contenu est diffusé. Elle peut correspondre à l’URL d’une ou de plusieurs pages, de sorte que les expériences web puissent diffuser des modifications sur une ou plusieurs pages web. Ces configurations sont requises pour que les spécialistes marketing [ajoutent des nœuds d’action de personnalisation web dans les parcours &#x200B;](../content/web-experiences.md#create-a-web-experience) et [conçoivent les modifications d’expérience](../content/web-experience-design.md) pour une campagne.

>[!BEGINSHADEBOX]

**Conditions préalables**

Pour utiliser les canaux web, le [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/js-overview) (`alloy.js`) doit être implémenté pour l’identification des visiteurs et la diffusion de contenu sur votre site web. Assurez-vous que la version de Adobe Experience Platform Web SDK est la version 2.16 ou ultérieure.

La configuration du canal web dans Journey Optimizer B2B edition nécessite les [autorisations](../admin/user-management.md#b2b-product-permissions) suivantes :

* _[!UICONTROL Configurations de canal]_ > _[!UICONTROL Gérer les préréglages de message]_ - Obligatoire pour créer, mettre à jour et supprimer des configurations de canal web.
* _[!UICONTROL Configurations de canal]_ > _[!UICONTROL Afficher les préréglages de message]_ - Obligatoire pour afficher les configurations de canal web.

>[!ENDSHADEBOX]

## Création d’une configuration de canal web

1. Dans le volet de navigation de gauche, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]**.

1. Sous _[!UICONTROL Web]_ dans le panneau de navigation, sélectionnez **[!UICONTROL Configurations de canal]**.

   ![Accéder aux configurations du canal web](./assets/config-web-channels.png){width="800" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Créer une configuration de canal]** en haut à droite.

1. Saisissez un **[!UICONTROL Nom]** (obligatoire) et un **[!UICONTROL Description]** (facultatif) pour la configuration.

   >[!NOTE]
   >
   >Les noms doivent commencer par une lettre (A-Z) et ne peuvent contenir que des caractères alphanumériques. Vous pouvez également utiliser des `_` de soulignement, des `.` de point et des tirets `-`.

1. Dans la section **[!UICONTROL Paramètres Web]**, sélectionnez l’une des options suivantes :

   * **[!UICONTROL Une seule page]** - Si vous souhaitez appliquer les modifications à une seule page uniquement, saisissez ou sélectionnez une **[!UICONTROL URL de la page]**.

     ![Sélection d’une URL de page pour une configuration de canal web monopage](./assets/config-web-channel-create-single-page.png){width="600" zoomable="yes"}

   * **[!UICONTROL Règle de correspondance de pages]** - Pour cibler plusieurs URL correspondant à la même règle, créez une [règle de correspondance de pages](#build-a-pages-matching-rule) et saisissez une **[!UICONTROL URL de création et d’aperçu par défaut]**.

1. Cliquez sur **[!UICONTROL Envoyer]** pour enregistrer vos modifications.

Une fois la configuration enregistrée, elle passe au statut _Brouillon_ et est disponible pour les marketeurs lorsqu’ils utilisent un canal web dans leurs parcours. Vous pouvez continuer à modifier la configuration tant qu’elle reste à l’état de brouillon. Vous pouvez également supprimer un brouillon de configuration de canal web en cliquant sur l’icône _Plus_ (**...**) à côté du nom et en choisissant **[!UICONTROL Supprimer]**.

Dès que le canal web est utilisé dans un parcours, il passe à un statut _Actif_. Dans cet état, vous pouvez modifier le nom et la description de la configuration. Vous ne pouvez pas modifier les paramètres web ni supprimer la configuration.

## Règles de correspondance de pages {#pages-matching-rule}

Lors de la création d’une configuration web, vous pouvez créer une _[!UICONTROL règle de correspondance de pages]_ pour cibler plusieurs URL correspondant à la même règle. Ces règles vous permettent d’appliquer les mêmes modifications de contenu sur plusieurs pages.

Par exemple, vous pouvez appliquer des modifications à une bannière principale sur l’ensemble d’un site web ou ajouter une image principale affichée sur toutes les pages de produits.

### Créer une règle

1. Lorsque vous [créez une configuration de canal web](#create-a-web-channel-configuration), choisissez **[!UICONTROL Règle de correspondance de page]**.

1. Définissez vos critères pour les champs **[!UICONTROL Domaine]** et **[!UICONTROL Page]** en utilisant les différents opérateurs de chaque section pour créer la règle.

   +++Opérateurs de domaine

   Utilisez les opérateurs suivants pour les domaines correspondants en fonction de la valeur de chaîne que vous saisissez :

   | Opérateur | Description | Exemples |
   | --- | --- | --- |
   | [!UICONTROL Est égal à] | Correspondance exacte du domaine. | |
   | [!UICONTROL Commence par] | Correspond à tous les domaines (y compris les sous-domaines) commençant par la chaîne saisie. | `Starts with: dev` correspond à tous les domaines et sous-domaines commençant par `dev`, tels que `dev.example.com`, `dev.products.example.com` et `developer.example.com` |
   | [!UICONTROL Se termine par] | Correspond à tous les domaines (y compris les sous-domaines) qui se terminent par la chaîne saisie. | `Ends with: example.com` correspond à tous les domaines et sous-domaines qui se terminent par `example.com`, tels que `stage.example.com`, `prod.example.com` et `myexample.com` |
   | [!UICONTROL Correspondance des caractères génériques] | Permet de définir une correspondance de caractère générique au milieu de la chaîne, telle que `dev.*.example.com`. Les règles de validation exigent que la valeur contienne un et un seul caractère générique (astérisque) lorsque l’opérateur est _correspondance de caractères génériques_. | `Wildcard matching: dev.*.example.com` correspond à des domaines tels que `dev.products.example.com`, `dev.mytest.products.example.com` et `dev.blog.example.com` |
   | [!UICONTROL Any] | Correspond à tous les domaines. Cela s’avère utile lors du test d’un chemin particulier sur plusieurs domaines. | |

   +++

   +++Opérateurs de chemin

   Utilisez les opérateurs suivants pour faire correspondre les chemins d’accès en fonction de la valeur de chaîne que vous saisissez :

   | Opérateur | Description | Exemples |
   | --- | --- | --- |
   | [!UICONTROL Est égal à] | Correspondance exacte du chemin. | |
   | [!UICONTROL Commence par] | Correspond à tous les chemins (y compris les sous-chemins) commençant par la chaîne. | |
   | [!UICONTROL Se termine par] | Correspond à tous les chemins (y compris les sous-chemins) qui se terminent par la chaîne. | |
   | [!UICONTROL Any] | Correspond à tous les chemins d’accès. Cette approche est utile pour cibler tous les chemins d’accès sous un ou plusieurs domaines. | |
   | [!UICONTROL Correspondance des caractères génériques] | Permet de définir un caractère générique interne dans le chemin d’accès, tel que `/products/*/detail`. Le caractère générique `*` dans le composant de chemin d’accès correspond à n’importe quelle séquence de caractères jusqu’au premier caractère `/`.  Et `/*/` correspond à n’importe quelle séquence de caractères (y compris les sous-chemins). | `Wildcard matching: /products/*/detail` correspond à des chemins tels que `example.com/products/yoga/detail`, `example.com/products/surf/detail`, `example.com/products/tennis/detail` et `example.com/products/yoga/pants/detail` |
   | [!UICONTROL Contient] | La valeur est traduite en caractère générique, tel que `*mystring*`, et correspond à tous les chemins qui contiennent la séquence de caractères. | `Contains: product` correspond à tous les chemins contenant les `product` de chaîne, tels que `example.com/products`, `example.com/yoga/perfproduct`, `example.com/surf/productdescription` et `example.com/home/product/page` |

   +++

   Par exemple, pour prendre en charge les modifications de contenu sur toutes les pages de solution _LumaSecure_ de votre site web _Bodea_, sélectionnez **[!UICONTROL Domaine]** > **[!UICONTROL Commence par]** > `bodea` et **[!UICONTROL Page]** > **[!UICONTROL Contains]** > `lumasecure`.

   ![Définir une règle de correspondance de pages pour une configuration de canal web](./assets/config-web-channel-pages-matching-rules.png){width="600" zoomable="yes"}

1. Si votre cas d’utilisation nécessite plusieurs règles, cliquez sur **[!UICONTROL Ajouter une autre règle de page]** et répétez l’étape précédente.

   * Vous pouvez définir jusqu’à 10 règles.

   * Utilisez les opérateurs **[!UICONTROL Or]** ou **[!UICONTROL Exclude]** entre les différentes règles.

     _[!UICONTROL Or]_ est l’opérateur par défaut pour définir plusieurs règles et est utile pour ajouter plusieurs définitions de critères qui peuvent être mises en correspondance.

     L’option _[!UICONTROL Exclure]_ est utile lorsque l’une des pages correspondant à la règle définie ne doit pas être ciblée. Vous pouvez, par exemple, cibler toutes les pages `bodea.com` qui contiennent des `lumasecure`, mais en excluant les pages de blog (comme les `bodea.com/blogs/lumasecure/latest-release`).

   ![Règles de correspondance de pages avec exclusion](./assets/config-web-channel-pages-matching-rules-exclude.png){width="600" zoomable="yes"}

1. Saisissez l’**[!UICONTROL URL de création et d’aperçu par défaut]**.

   Cette étape permet de s’assurer que les pages générées ou mises en correspondance par la règle possèdent une URL désignée à des fins de conception de contenu d’expérience web et de prévisualisation.

## Dupliquer un canal web

Vous pouvez dupliquer une configuration de canal web existante et la modifier pour créer un canal web basé sur un canal existant. Une configuration de canal web active enregistrée dans la bibliothèque ne peut pas être modifiée.

1. Cliquez sur l’icône _Plus de menu_ (**...**) de la variante et choisissez **[!UICONTROL Dupliquer]**.

   ![Cliquez sur l’icône plus de menu pour dupliquer une configuration de canal web existante](./assets/config-web-channels-more-menu.png){width="450"}

   Cette action crée un canal web dupliqué avec `_Copy_nnn` ajouté au nom.

1. Cliquez sur le nom du canal web dupliqué pour modifier les paramètres.

   * Modifiez le nom et la description pour qu’ils correspondent à l’objectif ou aux éléments de la règle.
   * Si nécessaire, modifiez l’URL d’une seule page.
   * Si nécessaire, modifiez la règle de correspondance de pages en fonction de vos besoins.

1. Une fois la configuration terminée, cliquez sur **[!UICONTROL Envoyer]**.
