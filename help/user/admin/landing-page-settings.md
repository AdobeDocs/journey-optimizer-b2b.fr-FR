---
title: Configuration des pages de destination
description: Configurez les sous-domaines de page de destination, les paramètres de préremplissage de formulaire et les flux de données pour activer la publication de pages web Campaign dans Journey Optimizer B2B edition.
feature: Setup, Landing Pages, Content
role: Admin
hide: true
hidefromtoc: true
badgeBeta: label="Beta" type="informative" tooltip="Cette fonctionnalité est actuellement en version bêta limitée"
exl-id: 54b812cb-0129-4253-8e9e-538c25fc4709
source-git-commit: 9ed2d2a36dbdaf39c107a18632d951003c86197b
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 34%

---

# Configuration des pages de destination

Les administrateurs doivent s’assurer que les paramètres de la page de destination sont configurés pour les marketeurs qui créent et publient ces pages.

## Paramètres

Pour passer en revue la configuration de la page de destination, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]**. Sous _[!UICONTROL Pages de destination]_ dans le panneau de navigation, sélectionnez **[!UICONTROL Paramètres]**.

![Paramètres de la page de destination](./assets/config-landing-pages-settings.png){width="800" zoomable="yes"}

### Chaîne de compte {#account-string}

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_account_string"
>title="Chaîne de compte des pages de destination"
>abstract="La chaîne de compte identifie l’instance Adobe Journey Optimizer B2B Edition qui héberge les pages de destination."

La chaîne de compte identifie l’instance Adobe Journey Optimizer B2B edition qui héberge les pages de destination. Assurez-vous que votre équipe Systèmes ajoute et configure l’entrée DNS.

### Préremplissage de formulaire {#form-prefill}

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_form_prefill"
>title="Paramètres de préremplissage des formulaires de page de destination"
>abstract="Vous pouvez activer l’option de préremplissage de formulaire pour permettre aux formulaires de vos pages de destination d’utiliser des informations préremplies pour les utilisateurs et utilisatrices connus."

Activez l&#39;option **[!UICONTROL Préremplissage de formulaire]** pour permettre aux formulaires de vos pages de destination d&#39;utiliser des informations préremplies pour des utilisateurs connus. Lorsque cette option est désactivée, les auteurs de page de destination ne peuvent pas inclure de champs de formulaire préremplis.

### Train de données {#datastream}

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_datastream"
>title="Exigence en matière de train de données"
>abstract="Un train de données est nécessaire pour collecter les événements des pages de destination sur ce domaine."

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_missing_datastream"
>title="ID de train de données manquant"
>abstract="Le sous-domaine ne comporte pas d’ID de train de données, qui est requis pour un routage correct. Configurez-le dans Paramètres pour continuer."

Définissez l’option **[!UICONTROL Flux de données]** pour configurer un flux de données pour la collecte d’événements de page de destination.

## Sous-domaines {#add-subdomain}

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_add_subdomain"
>title="Ajouter un sous-domaine de page de destination"
>abstract="Vous pouvez ajouter 50 sous-domaines au maximum. Configurez un nouveau sous-domaine pour chaque URL de marque unique que vous souhaitez héberger sur Adobe Journey Optimizer B2B Edition."

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_configure_subdomain"
>title="Configurer les sous-domaines de page de destination"
>abstract="Un sous-domaine configuré est requis pour publier des pages de destination. Vous pouvez utiliser un sous-domaine déjà délégué à Adobe ou en configurer un nouveau."

Un sous-domaine de page de destination doit vous aider à identifier le type de contenu, le nom de produit ou la campagne, et à renforcer l’authenticité de la page. Avant de configurer les sous-domaines, définissez un ou plusieurs CNAME à utiliser pour vos pages de destination. Par exemple :

* **produit**.[CompanyDomain].com
* **allez**.[CompanyDomain].com
* **inscription**.[CompanyDomain].com

Dans ces exemples, la première partie (en gras) est la `LandingPageCNAME`.

Ajoutez un nouveau sous-domaine pour chaque URL de marque unique que vous souhaitez héberger sur Adobe Journey Optimizer B2B edition. Vous pouvez ajouter un nombre maximal de 50 sous-domaines.

>[!IMPORTANT]
>
>La délégation d’un sous-domaine non valide à Adobe n’est pas autorisée. Assurez-vous de saisir un sous-domaine valide détenu par votre organisation, tel que _marketing.votreentreprise.com_.

Pour passer en revue vos sous-domaines et en ajouter de nouveaux, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]**. Sous _[!UICONTROL Pages de destination]_ dans le panneau de navigation, sélectionnez **[!UICONTROL Sous-domaines]**.

![Sous-domaines de la page de destination](./assets/config-landing-pages-settings.png){width="800" zoomable="yes"}

_Pour ajouter un sous-domaine de page de destination :_

1. Cliquez sur **[!UICONTROL Ajouter un sous-domaine]** en haut à droite.

1. Dans les _[!UICONTROL Détails du sous-domaine]_, saisissez les informations du sous-domaine :

   * **[!UICONTROL Sous-domaine]** - URL du sous-domaine à utiliser, par exemple `marketing.yourcompany.com`
   * **[!UICONTROL Page par défaut]** - URL de la page de sous-domaine par défaut, telle que `marketing.yourcompany.com/products`
   * **[!UICONTROL Page de secours]** - URL de la page de secours à utiliser si une page de destination du sous-domaine n’est pas active, par exemple `marketing.yourcompany.com/expired`

   ![Ajouter un sous-domaine de page de destination](./assets/config-landing-pages-add-subdomain.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Enregistrer]**
