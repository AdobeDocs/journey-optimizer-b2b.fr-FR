---
title: Champs XDM
description: Examinez les champs d’attribut par défaut synchronisés entre Adobe Experience Platform et Journey Optimizer Édition B2B.
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: b38878ca063967e6c1ae56617674af52c10913df
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 25%

---

# Champs XDM

Les données d’audience de compte sont stockées en tant qu’attributs dans les classes XDM Business Account et XDM Business Person. Les données sont régulièrement synchronisées entre Adobe Experience Platform et Journey Optimizer Édition B2B. Les sections suivantes répertorient les jeux d’attributs par défaut.

## Attributs de personne active XDM

| [Propriété](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md) | Nom d’affichage | Nom d’affichage Journey Optimizer B2B | Type de données | Description |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `b2b.companyName` | Nom de la société | Nom de la société | Chaîne | Nom de la société à laquelle est associé un homme d’affaires. |
| `b2b.companyWebsite` | Site Web de la société | Site web | Chaîne | Site Web de la société à laquelle est associé un homme d’affaires. |
| `b2b.isMarketingSuspended` | Indicateur de suspension marketing | Marketing interrompu | Booléen | La valeur indique si le marketing est suspendu pour la personne. |
| `b2b.marketingSuspendedCause` | Cause du marketing interrompu | Cause du marketing interrompu | Chaîne | Si le marketing est suspendu pour la personne, cette propriété en fournit la raison. |
| `b2b.personStatus` | Statut Individu | Statut du lead | Chaîne | Champ enregistrant l’état actuel du marketing/des ventes de la Personne. |
| `consents.marketing.email.reason` | Motif d’exclusion | Raison du désabonnement | Chaîne | Motif associé à l’exclusion de l’email. |
| `consents.marketing.email.val` | Désabonné | Désabonné | Chaîne | Si unsubscribed est true (par exemple, value = 1), définissez `consents.marketing.email.val` sur (n). Si le désabonnement est false (par exemple, valeur = 0), définissez `consents.marketing.email.val` comme nul. |
| `extendedWorkDetails.jobTitle` | Intitulé du poste | Intitulé du poste | Chaîne | Fonction de la personne. |
| `faxPhone.number` | Nombre | Numéro de fax | Chaîne | Numéro de fax. |
| `mobilePhone.number` | Nombre | Numéro de téléphone mobile | Chaîne | Numéro de téléphone portable associé à la personne. |
| `person.birthDate` | Date de naissance (AAAA-MM-JJ) | Date de naissance | Chaîne | Date complète de naissance d’une personne. AAAA-MM-JJ |
| `person.name.courtesyTitle` | Avec l&#39;autorisation de Title | Titre | Chaîne | En règle générale, abréviation du titre, de l’honneur ou de la formule de salutation d’une personne. courtesyTitle est utilisé devant le nom complet ou le nom de famille dans les textes d&#39;ouverture. Par exemple, M., Mme ou Dr. |
| `person.name.firstName` | Prénom | Prénom | Chaîne | Premier segment du nom dans l’ordre écrit le plus communément accepté dans la langue du nom. Dans de nombreuses cultures, il s’agit du prénom personnel préféré. Les propriétés firstName et lastName ont été introduites afin de maintenir la compatibilité avec les systèmes existants qui modélisent les noms de manière simplifiée, non sémantique et non internationalisable. L’utilisation de `xdm:fullName` est toujours préférable. |
| `person.name.lastName` | Nom | Nom | Chaîne | Dernier segment du nom dans l’ordre écrit le plus communément accepté dans la langue du nom. Dans de nombreuses cultures, il s&#39;agit du nom de famille, du nom de famille, du patronyme ou du matronyme hérités. Les propriétés firstName et lastName ont été introduites afin de maintenir la compatibilité avec les systèmes existants qui modélisent les noms de manière simplifiée, non sémantique et non internationalisable. L’utilisation de `xdm:fullName` est toujours préférable. |
| `person.name.middleName` | Deuxième prénom | Deuxième prénom | Chaîne | Nom intermédiaire, nom alternatif ou noms supplémentaires présents entre le prénom et le nom. |
| `workAddress.city ` | Ville | Ville | Chaîne | Nom de la ville. |
| `workAddress.country` | Pays | Pays | Chaîne | Nom du territoire administré par un gouvernement. Outre `xdm:countryCode`, il s’agit d’un champ de forme libre qui peut avoir le nom du pays dans n’importe quelle langue. |
| `workAddress.postalCode` | Code postal | Code postal | Chaîne | Code postal de l’emplacement. Les codes postaux ne sont pas disponibles pour tous les pays. Dans certains pays, il ne contient qu’une partie du code postal. |
| `workAddress.state` | État | État | Chaîne | Nom de l’état de l’adresse. C&#39;est un champ de forme libre. |
| `workAddress.street1` | Rue 1 | Adresse | Chaîne | Informations au niveau de la rue par Principal, numéro d’appartement, numéro de rue et nom de rue. |
| `workEmail.address` | Adresse | Adresse e-mail | Chaîne | Adresse technique, par exemple, `<name@domain.com>` telle que généralement définie dans la norme RFC2822 et les normes ultérieures. |
| `workEmail.status` | Statut | E-mail interrompu | Chaîne | Une indication sur la possibilité d’utiliser l’adresse électronique. |
| `workPhone.number` | Nombre | Numéro de téléphone | Chaîne | Numéro de téléphone professionnel. |

## Attributs du compte commercial XDM

| [Propriété](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/account/account-details.schema.md) | Nom d’affichage | Nom d’affichage Journey Optimizer B2B | Type de données | Description |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `accountBillingAddress.city` | Ville | Ville | Chaîne | Nom de la ville utilisé dans l’adresse de facturation. |
| `accountBillingAddress.country` | Pays | Pays | Chaîne | Nom du territoire géré par le gouvernement et utilisé dans l’adresse de facturation. Outre `xdm:countryCode`, il s’agit d’un champ de forme libre qui peut avoir le nom du pays dans n’importe quelle langue. |
| `accountBillingAddress.postalCode` | Code postal | Code postal de l’adresse | Chaîne | Code postal de l’emplacement de l’adresse de facturation. Les codes postaux ne sont pas disponibles pour tous les pays. Dans certains pays, il ne contient qu’une partie du code postal. |
| `accountBillingAddress.region` | Région | Région d’adresse | Chaîne | Partie de la région, du département ou du district de l’adresse de facturation. |
| `accountBillingAddress.state` | État | État | Chaîne | Nom de l’état de l’adresse de facturation. C&#39;est un champ de forme libre. |
| `accountBillingAddress.street1` | Rue 1 | Rue 1 | Chaîne | Informations au niveau de la rue par Principal pour l’adresse de facturation, qui comprennent généralement le numéro de l’appartement, le numéro de la rue et le nom de la rue. |
| `accountName` | Nom | Nom | Chaîne | Nom de la société. Ce champ peut contenir jusqu’à 255 caractères. |
| `accountOrganization.annualRevenue.amount` | Chiffre d&#39;affaires annuel | Chiffre d&#39;affaires annuel | Nombre | Montant estimé des recettes annuelles de l’organisation. |
| `accountOrganization.industry` | Secteur industriel | Secteur industriel | Chaîne | L’industrie est attribuée à l’organisation. Il s’agit d’un champ de forme libre, et il est conseillé d’utiliser une valeur structurée pour les requêtes ou d’utiliser la propriété `xdm:classifier`. |
| `accountOrganization.logoUrl` | Logo URL | Logo URL | Chaîne | Chemin à combiner avec l’URL d’une instance Salesforce (par exemple, `https://yourInstance.salesforce.com/`) pour générer une URL afin de demander l’image de profil de réseau social associée au compte. L’URL générée renvoie une redirection HTTP (code 302) vers l’image de profil de réseau social pour le compte. |
| `accountOrganization.numberOfEmployees` | Nombre d&#39;employés | Nombre d&#39;employés | Nombre entier | Nombre d’employés de l’organisation. |
| `accountOrganization.SICCode` | Code SIC | Code SIC | Chaîne | Le code SIC (Standard Industrial Classification), qui est un code à quatre chiffres qui classe les secteurs auxquels appartiennent les entreprises en fonction de leurs activités commerciales. |
| `accountOrganization.website` | URL du site Web | Nom du domaine | Chaîne | URL du site web de l’organisation. |
| `accountPhone.number` | S/O | Numéro de téléphone du compte | Chaîne | Numéro de téléphone associé au compte. |
| `accountSourceType` | S/O | Type de source | Chaîne | Type Source du compte. |
