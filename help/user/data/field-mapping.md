---
title: Mappage des champs XDM
description: Examinez le mappage des champs entre le schéma XDM AEP, Marketo Engage et Journey Optimizer B2B Edition.
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: 78d82aa8b3bb8b8d432eeb187d75e2354dbff3ee
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 27%

---

# Mappage des champs XDM

Le service de transfert de données (DTS) est chargé de synchroniser les données de Adobe Experience Platform vers Journey Optimizer B2B Edition. DTS repose sur les mappages entre les champs de schéma XDM Experience Platform et leurs équivalents dans Marketo Engage.

## Mappages des champs par défaut de la personne active XDM

| [Personne travaillant dans XDM](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md) | Nom d’affichage XDM | Nom d’affichage du Marketo Engage | Type XDM | Type Marketo | Description XDM |
|------------------- |---------------------------------- |--------------------------- |-------- |------------ |--------------- |
| `b2b.companyName` | Nom de la société | Nom de la société | Chaîne | Chaîne | Nom de la société à laquelle est associé un homme d’affaires. |
| `b2b.companyWebsite` | Site Web de la société | Site web | Chaîne | url | Site Web de la société à laquelle est associé un homme d’affaires. |
| `b2b.isMarketingSuspended` | Indicateur de suspension marketing | Marketing interrompu | Booléen | Booléen | La valeur indique si le marketing est suspendu pour la personne. |
| `b2b.marketingSuspendedCause` | Cause du marketing interrompu | Cause du marketing interrompu | Chaîne | Chaîne | Si le marketing est suspendu pour la personne, cette propriété en fournit la raison. |
| `b2b.personStatus` | Statut Individu | Statut du lead | Chaîne | Chaîne | Champ enregistrant l’état actuel du marketing/des ventes de la Personne. |
| `consents.marketing.email.reason` | Motif d’exclusion | Raison du désabonnement | Chaîne | Chaîne | Motif associé à l’exclusion de l’email. |
| `consents.marketing.email.val` | Désabonné | Désabonné | Chaîne | Booléen | Si unsubscribed est true (par exemple, value = 1), définissez `consents.marketing.email.val` sur (n). Si le désabonnement est false (par exemple, valeur = 0), définissez consents.marketing.email.val sur null. |
| `extendedWorkDetails.jobTitle` | Intitulé du poste | Intitulé du poste | Chaîne | Chaîne | Fonction de la personne. |
| `faxPhone.number` | Nombre | Numéro de fax | Chaîne | téléphone | Numéro de fax. |
| `mobilePhone.number` | Nombre | Numéro de téléphone mobile | Chaîne | téléphone | Numéro de téléphone portable associé à la personne. |
| `person.birthDate` | Date de naissance (AAAA-MM-JJ) | Date de naissance | Chaîne | Date | Date complète de naissance d’une personne. AAAA-MM-JJ |
| `person.name.courtesyTitle` | Avec l&#39;autorisation de Title | Titre | Chaîne | Chaîne | En règle générale, abréviation du titre, de l’honneur ou de la formule de salutation d’une personne. courtesyTitle est utilisé devant le nom complet ou le nom de famille dans les textes d&#39;ouverture. Par exemple, M., Mme ou Dr. |
| `person.name.firstName` | Prénom | Prénom | Chaîne | Chaîne | Premier segment du nom dans l’ordre écrit le plus communément accepté dans la langue du nom. Dans de nombreuses cultures, il s’agit du prénom personnel préféré. Les propriétés firstName et lastName ont été introduites afin de maintenir la compatibilité avec les systèmes existants qui modélisent les noms de manière simplifiée, non sémantique et non internationalisable. L’utilisation de `xdm:fullName` est toujours préférable. |
| `person.name.lastName` | Nom | Nom | Chaîne | Chaîne | Dernier segment du nom dans l’ordre écrit le plus communément accepté dans la langue du nom. Dans de nombreuses cultures, il s&#39;agit du nom de famille, du nom de famille, du patronyme ou du matronyme hérités. Les propriétés firstName et lastName ont été introduites afin de maintenir la compatibilité avec les systèmes existants qui modélisent les noms de manière simplifiée, non sémantique et non internationalisable. L’utilisation de `xdm:fullName` est toujours préférable. |
| `person.name.middleName` | Deuxième prénom | Deuxième prénom | Chaîne | téléphone | Nom intermédiaire, nom alternatif ou noms supplémentaires présents entre le prénom et le nom. |
| `workAddress.city ` | Ville | Ville | Chaîne | Chaîne | Nom de la ville. |
| `workAddress.country` | Pays | Pays | Chaîne | Chaîne | Nom du territoire administré par un gouvernement. Outre `xdm:countryCode`, il s’agit d’un champ de forme libre qui peut avoir le nom du pays dans n’importe quelle langue. |
| `workAddress.postalCode` | Code postal | Code postal | Chaîne | Chaîne | Code postal de l’emplacement. Les codes postaux ne sont pas disponibles pour tous les pays. Dans certains pays, il ne contient qu’une partie du code postal. |
| `workAddress.state` | État | État | Chaîne | Chaîne | Nom de l’état de l’adresse. C&#39;est un champ de forme libre. |
| `workAddress.street1` | Rue 1 | Adresse | Chaîne | texte | Informations au niveau de la rue par Principal, numéro d’appartement, numéro de rue et nom de rue. |
| `workEmail.address` | Adresse | Adresse e-mail | Chaîne | E-mail | Adresse technique, par exemple, `<name@domain.com>` telle que généralement définie dans la norme RFC2822 et les normes ultérieures. |
| `workEmail.status` | Statut | E-mail interrompu | Chaîne | Booléen | Une indication sur la possibilité d’utiliser l’adresse électronique. |
| `workPhone.number` | Nombre | Numéro de téléphone | Chaîne | téléphone | Numéro de téléphone professionnel. |

## Mappages des champs par défaut du compte commercial XDM

| [Compte professionnel XDM](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/account/account-details.schema.md) | Nom d’affichage XDM | Nom d’affichage du Marketo Engage | Type XDM | type de Marketo Engage | Description XDM |
|------------------- |---------------------------------- |--------------------------- |-------- |------------ |--------------- |
| `accountBillingAddress.city` | Ville | Ville | Chaîne | Chaîne | Nom de la ville utilisé dans l’adresse de facturation. |
| `accountBillingAddress.country` | Pays | Pays | Chaîne | Chaîne | Nom du territoire géré par le gouvernement et utilisé dans l’adresse de facturation. Outre `xdm:countryCode`, il s’agit d’un champ de forme libre qui peut avoir le nom du pays dans n’importe quelle langue. |
| `accountBillingAddress.postalCode` | Code postal | Code postal de l’adresse | Chaîne | Chaîne | Code postal de l’emplacement de l’adresse de facturation. Les codes postaux ne sont pas disponibles pour tous les pays. Dans certains pays, il ne contient qu’une partie du code postal. |
| `accountBillingAddress.region` | Région | Région d’adresse | Chaîne | Chaîne | Partie de la région, du département ou du district de l’adresse de facturation. |
| `accountBillingAddress.state` | État | État | Chaîne | Chaîne | Nom de l’état de l’adresse de facturation. C&#39;est un champ de forme libre. |
| `accountBillingAddress.street1` | Rue 1 | Rue 1 | Chaîne | Chaîne | Informations au niveau de la rue par Principal pour l’adresse de facturation, qui comprennent généralement le numéro de l’appartement, le numéro de la rue et le nom de la rue. |
| `accountName` | Nom | Nom | Chaîne | Chaîne | Nom de la société. Ce champ peut contenir jusqu’à 255 caractères. |
| `accountOrganization.annualRevenue.amount` | Chiffre d&#39;affaires annuel | Chiffre d&#39;affaires annuel | Nombre | currency | Montant estimé des recettes annuelles de l’organisation. |
| `accountOrganization.industry` | Secteur industriel | Secteur industriel | Chaîne | Chaîne | L’industrie est attribuée à l’organisation. Il s’agit d’un champ de forme libre, et il est conseillé d’utiliser une valeur structurée pour les requêtes ou d’utiliser la propriété `xdm:classifier`. |
| `accountOrganization.logoUrl` | Logo URL | Logo URL | Chaîne | Chaîne | Chemin à combiner avec l’URL d’une instance Salesforce (par exemple, `https://yourInstance.salesforce.com/`) pour générer une URL afin de demander l’image de profil de réseau social associée au compte. L’URL générée renvoie une redirection HTTP (code 302) vers l’image de profil de réseau social pour le compte. |
| `accountOrganization.numberOfEmployees` | Nombre d&#39;employés | Nombre d&#39;employés | Entier | Entier | Nombre d’employés de l’organisation. |
| `accountOrganization.SICCode` | Code SIC | Code SIC | Chaîne | Chaîne | Le code SIC (Standard Industrial Classification), qui est un code à quatre chiffres qui classe les secteurs auxquels appartiennent les entreprises en fonction de leurs activités commerciales. |
| `accountOrganization.website` | URL du site Web | Nom du domaine | Chaîne | Chaîne | URL du site web de l’organisation. |
| `accountPhone.number` | S/O | Numéro de téléphone du compte | Chaîne | Chaîne | Numéro de téléphone associé au compte. |
| `accountSourceType` | S/O | Type de source | Chaîne | Chaîne | Type Source du compte. |
