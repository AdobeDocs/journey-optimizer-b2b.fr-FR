---
title: Mappage des champs XDM
description: Examinez le mappage des champs entre le schéma XDM AEP, Marketo Engage et Journey Optimizer B2B Edition.
source-git-commit: af287825508b2372f51aa8ea629cc6eda0a50b35
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 20%

---

# Mappage des champs XDM

Le service de transfert de données (DTS) de est chargé de synchroniser les données de Adobe Experience Platform vers Journey Optimizer B2B Edition. DTS repose sur les mappages entre les champs de schéma XDM Experience Platform et leurs équivalents dans Marketo Engage.

## Mappages des champs par défaut de la personne active XDM

| Personne commerciale XDM | Nom d’affichage de la personne Marketo Engage | Nom d’affichage de la personne AJO B2B | Type XDM | Type de Marketo | Description XDM |
|------------------- |---------------------------------- |--------------------------- |-------- |------------ |--------------- |
| `workAddress.street1` | Adresse | ? | Chaîne | Texte | Informations au niveau de la rue par Principal, numéro d’appartement, numéro de rue et nom de rue. |
| `workAddress.city ` | Ville | Ville | Chaîne | Chaîne | Nom de la ville. |
| `b2b.companyName` | Nom de l’entreprise | ? | Chaîne | Chaîne | Nom de la société à laquelle est associé un homme d’affaires. |
| `workAddress.country` | Pays | Pays | Chaîne | Chaîne | Nom du territoire administré par le gouvernement. À l’exception de `xdm:countryCode`, il s’agit d’un champ de forme libre qui peut avoir le nom du pays dans n’importe quelle langue. |
| `person.birthDate` | Date De Naissance | Date de naissance | Chaîne | Date | Date complète de naissance d’une personne.  AAAA-MM-JJ |
| `workEmail.address` | Adresse e-mail | Adresse e-mail | Chaîne | E-mail | Adresse technique, par exemple, &#39;<name@domain.com>&#39;, telle que généralement définie dans la norme RFC2822 et les normes ultérieures. |
| `workEmail.status` | E-mail interrompu | E-mail interrompu | Chaîne | Booléen | Une indication sur la possibilité d’utiliser l’adresse électronique. |
| `faxPhone.number` | Numéro de fax | ? | Chaîne | téléphone | Fax. |
| `person.name.firstName` | Prénom | Prénom | Chaîne | Chaîne | Premier segment du nom dans l’ordre d’écriture le plus communément accepté dans la langue du nom. Dans de nombreuses cultures, il s’agit du prénom personnel ou du prénom préféré. Les propriétés firstName et lastName ont été introduites afin de maintenir la compatibilité avec les systèmes existants qui modélisent les noms de manière simplifiée, non sémantique et non internationalisable. L’utilisation de xdm:fullName est toujours préférable. |
| `extendedWorkDetails.jobTitle` | Intitulé du poste | Intitulé du poste | Chaîne | Chaîne | Fonction de la personne. |
| `person.name.lastName` | Nom | Nom | Chaîne | Chaîne | Dernier segment du nom dans l’ordre d’écriture le plus communément accepté dans la langue du nom. Dans de nombreuses cultures, il s&#39;agit du nom de famille, du nom de famille, du patronyme ou du matronyme hérités. Les propriétés firstName et lastName ont été introduites afin de maintenir la compatibilité avec les systèmes existants qui modélisent les noms de manière simplifiée, non sémantique et non internationalisable. L’utilisation de xdm:fullName est toujours préférable. |
| `b2b.personStatus` | Statut du lead | ? | Chaîne | Chaîne | Champ enregistrant l’état actuel du marketing/des ventes de la Personne. |
| `b2b.isMarketingSuspended` | Marketing interrompu | ? | Booléen | Booléen | Indique si le marketing est suspendu pour la personne. |
| `b2b.marketingSuspendedCause` | Cause du marketing interrompu | ? | Chaîne | Chaîne | Si le marketing est suspendu pour la personne, cette propriété en fournit la raison. |
| `person.name.middleName` | Deuxième prénom | ? | Chaîne | téléphone | Nom intermédiaire, nom alternatif ou noms supplémentaires fournis entre le prénom et le nom. |
| `mobilePhone.number` | Numéro de téléphone mobile | Numéro de téléphone mobile | Chaîne | téléphone | Numéro de téléphone portable. |
| `workPhone.number` | Numéro de téléphone | Numéro de téléphone | Chaîne | téléphone | Numéro de téléphone professionnel. |
| `workAddress.postalCode` | Code postal | Code postal | Chaîne | Chaîne | Code postal de l’emplacement. Les codes postaux ne sont pas disponibles pour tous les pays. Dans certains pays, ce champ ne contiendra qu&#39;une partie du code postal. |
| `person.name.courtesyTitle` | Titre | ? | Chaîne | Chaîne | En général, abréviation du titre d’une personne, du titre honorifique ou de la formule de salutation. courtesyTitle est utilisé devant le nom complet ou le nom de famille dans les textes d&#39;ouverture. Par exemple, M., Mme ou Dr. |
| `workAddress.state` | État | État | Chaîne | Chaîne | Nom de l’État. C&#39;est un champ de forme libre. |
| `consents.marketing.email.val` | Désabonné | Désabonné | Chaîne | Booléen | Si unsubscribed est true (par exemple, value = 1), définissez `consents.marketing.email.val` sur (n). Si le désabonnement est false (par exemple, valeur = 0), définissez consents.marketing.email.val sur null. |
| `consents.marketing.email.reason` | Raison du désabonnement | Raison du désabonnement | Chaîne | Chaîne |  |
| `b2b.companyWebsite` | Site web | ? | Chaîne | url | Site Web de la société à laquelle est associé un homme d’affaires. |

