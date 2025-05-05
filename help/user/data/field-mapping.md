---
title: Champs XDM
description: Passez en revue les champs d’attribut par défaut synchronisés entre Adobe Experience Platform et Journey Optimizer B2B edition.
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: 34ef9681b75ef1cd43d34e3f2836a60affb95b33
workflow-type: tm+mt
source-wordcount: '1342'
ht-degree: 22%

---

# Champs XDM

Les données d’audience de compte sont stockées sous forme d’attributs dans les classes XDM Business Account et XDM Business Person. Les données sont régulièrement synchronisées entre Adobe Experience Platform et Journey Optimizer B2B edition. Les sections suivantes répertorient les jeux d’attributs par défaut.

>[!TIP]
>
>Vous pouvez modéliser des classes de compte professionnel XDM et de compte professionnel XDM dans une relation multiple-à-multiple à l’aide de la classe de relation de personne avec compte professionnel XDM, comme décrit dans la [documentation XDM d’Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/xdm/tutorials/relationship-b2b).

## Attributs de relation de la personne avec le compte professionnel XDM

| [Propriété](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md) | Nom d’affichage | Nom d’affichage B2B de Journey Optimizer | Type de données | Description |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `personRoles` | Rôles de la personne | Rôle | Tableau de chaînes | Un tableau de rôles associés à la personne sur le compte, tels que `owner, accountant, designer` |

## Attributs d’homme d’affaires XDM

>[!IMPORTANT]
>
>L’attribut `workEmail.Address` est obligatoire. S’il est vide pour un membre de l’audience du compte, cette personne n’est pas ingérée et est omise des parcours de compte et des groupes d’achat qui font référence à l’audience.

| [Propriété](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md) | Nom d’affichage | Nom d’affichage B2B de Journey Optimizer | Type de données | Description |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `b2b.isMarketingSuspended` | Indicateur de marketing suspendu | Marketing interrompu | Booléen | La valeur indique si le marketing est suspendu pour la personne. |
| `b2b.marketingSuspendedCause` | Cause du marketing interrompu | Cause du marketing interrompu | Chaîne | Si le marketing est suspendu pour la personne, cette propriété en indique la raison. |
| `b2b.personStatus` | Statut Individu | Statut du lead | Chaîne | Champ d’enregistrement du statut de vente/marketing actuel de la personne. |
| `consents.marketing.email.reason` | Motif d’opt-out | Raison du désabonnement | Chaîne | Raison associée au processus d’opt-out des e-mails. |
| `consents.marketing.email.val` | Désabonné | Désabonné | Chaîne | Si le désabonnement est vrai (par exemple, valeur = 1), définissez `consents.marketing.email.val` comme (n). Si le désabonnement a la valeur false (par exemple, valeur = 0), définissez `consents.marketing.email.val` comme nul. |
| `extendedWorkDetails.jobTitle` | Intitulé du poste | Intitulé du poste | Chaîne | Fonction de la personne. |
| `faxPhone.number` | Nombre | Numéro de fax | Chaîne | Numéro de fax. |
| `mobilePhone.number` | Nombre | Numéro de téléphone mobile | Chaîne | Numéro de téléphone mobile associé à la personne. |
| `person.birthDate` | Date de naissance (AAAA-MM-JJ) | Date de naissance | Chaîne | Date de naissance complète d’une personne. AAAA-MM-JJ |
| `person.name.courtesyTitle` | Titre de courtoisie | Titre | Chaîne | Normalement, il s’agit de l’abréviation du titre, du titre honorifique ou de la qualification d’une personne. Le titre de courtoisie est utilisé devant le nom complet ou le nom de famille dans les textes d’ouverture. Par exemple, M., Mme ou Dr. |
| `person.name.firstName` | Prénom | Prénom | Chaîne | Premier segment du nom dans l’ordre écrit le plus couramment accepté dans la langue du nom. Dans de nombreuses cultures, il s’agit du prénom ou du nom personnel préféré. Les propriétés firstName et lastName ont été introduites pour maintenir la compatibilité avec les systèmes existants qui modélisent les noms d’une manière simplifiée, non sémantique et non internationalisable. L’utilisation de `xdm:fullName` est toujours préférable. |
| `person.name.lastName` | Nom | Nom | Chaîne | Dernier segment du nom dans l’ordre écrit le plus couramment accepté dans la langue du nom. Dans de nombreuses cultures, il s’agit du nom de famille, du nom de famille, du patronyme ou du nom matronymique hérités. Les propriétés firstName et lastName ont été introduites pour maintenir la compatibilité avec les systèmes existants qui modélisent les noms d’une manière simplifiée, non sémantique et non internationalisable. L’utilisation de `xdm:fullName` est toujours préférable. |
| `person.name.middleName` | Deuxième prénom | Deuxième prénom | Chaîne | Nom intermédiaire, nom alternatif ou noms supplémentaires présents entre le prénom et le nom. |
| `workAddress.city ` | Ville | Ville | Chaîne | Nom de la ville. |
| `workAddress.country` | Pays | Pays | Chaîne | Nom du territoire administré par un gouvernement. À l’exception de `xdm:countryCode`, il s’agit d’un champ à structure libre pouvant contenir le nom du pays dans n’importe quelle langue. |
| `workAddress.postalCode` | Code postal | Code postal | Chaîne | Code postal de l’emplacement. Les codes postaux ne sont pas disponibles pour tous les pays. Dans certains pays, il ne contient qu’une partie du code postal. |
| `workAddress.state` | État | État | Chaîne | Nom de l’État de l’adresse. C’est un champ de forme libre. |
| `workAddress.street1` | Rue 1 | Adresse | Chaîne | Informations principales sur le niveau de la rue, numéro de l’appartement, numéro de rue et nom de la rue. |
| `workEmail.address` | Adresse | Adresse e-mail | Chaîne | **Champ obligatoire** <br/>Adresse technique, par exemple, `<name@domain.com>` telle que définie communément dans les normes RFC2822 et suivantes. |
| `workEmail.status` | Statut | E-mail interrompu | Chaîne | Indication de la possibilité d’utiliser l’adresse électronique. |
| `workPhone.number` | Nombre | Numéro de téléphone | Chaîne | Numéro de téléphone professionnel. |

## Attributs du compte professionnel XDM

>[!IMPORTANT]
>
>L’attribut `accountName` est obligatoire. S’il est vide pour un compte dans une audience de compte, ce compte n’est pas ingéré et est omis des parcours de compte et des groupes d’achat qui référencent l’audience.

| [Propriété](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/account/account-details.schema.md) | Nom d’affichage | Nom d’affichage B2B de Journey Optimizer | Type de données | Description |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `accountBillingAddress.city` | Ville | Ville | Chaîne | Nom de la ville utilisé dans l’adresse de facturation. |
| `accountBillingAddress.country` | Pays | Pays | Chaîne | Nom du territoire administré par le gouvernement utilisé dans l’adresse de facturation. À l’exception de `xdm:countryCode`, il s’agit d’un champ à structure libre pouvant contenir le nom du pays dans n’importe quelle langue. |
| `accountBillingAddress.postalCode` | Code postal | Code postal de l’adresse | Chaîne | Code postal de l’emplacement de l’adresse de facturation. Les codes postaux ne sont pas disponibles pour tous les pays. Dans certains pays, il ne contient qu&#39;une partie du code postal. |
| `accountBillingAddress.region` | Région | Région de l’adresse | Chaîne | La partie région, comté ou district de l’adresse de facturation. |
| `accountBillingAddress.state` | État | État | Chaîne | Nom de l’état de l’adresse de facturation. Il s’agit d’un champ à structure libre. |
| `accountBillingAddress.street1` | Rue 1 | Rue 1 | Chaîne | Informations au niveau de la rue par Principal pour l’adresse de facturation, qui incluent généralement le numéro de l’appartement, le numéro de la rue et le nom de la rue. |
| `accountName` | Nom | Nom | Chaîne | **Champ obligatoire** <br/>Nom de la société. Ce champ peut contenir jusqu’à 255 caractères. |
| `accountOrganization.annualRevenue.amount` | Revenus annuels | Revenus annuels | Nombre | Montant estimé du chiffre d’affaires annuel de l’organisation. |
| `accountOrganization.industry` | Secteur industriel | Secteur industriel | Chaîne | L’industrie attribuée à l’organisation. Il s’agit d’un champ de forme libre et il est conseillé d’utiliser une valeur structurée pour les requêtes ou d’utiliser la `xdm:classifier` propriété. |
| `accountOrganization.logoUrl` | Logo URL | Logo URL | Chaîne | Chemin à associer à l’URL d’une instance Salesforce (par exemple, `https://yourInstance.salesforce.com/`) pour générer une URL afin de demander l’image de profil du réseau social associée au compte. L’URL générée renvoie une redirection HTTP (code 302) vers l’image de profil du réseau social pour le compte. |
| `accountOrganization.numberOfEmployees` | Nombre d&#39;employés | Nombre d&#39;employés | Nombre entier | Nombre d’employés dans l’organisation. |
| `accountOrganization.SICCode` | Code SIC | Code SIC | Chaîne | Le code SIC (Standard Industrial Classification) est un code à quatre chiffres qui classe les secteurs d’activité auxquels appartiennent les entreprises en fonction de leurs activités commerciales. |
| `accountOrganization.website` | URL du site web | Nom du domaine | Chaîne | URL du site web de l’organisation. |
| `accountPhone.number` | S/O | Numéro de téléphone du compte | Chaîne | Numéro de téléphone associé au compte. |
| `accountSourceType` | S/O | Type de source | Chaîne | Type de Source du compte. |

## Attributs d’opportunité commerciale XDM

En outre, les données d’opportunité sont stockées en tant qu’attributs dans la classe XDM Business Opportunity, qui peut être associée à la classe XDM Business Account par le biais d’une relation multiple-à-un, comme décrit [ici](https://experienceleague.adobe.com/fr/docs/experience-platform/xdm/tutorials/relationship-b2b#relationship-field).

| [Propriété](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/marketo/opportunity-marketo.schema.md) | Nom d’affichage | Nom d’affichage B2B de Journey Optimizer | Type de données | Description |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `expectedCloseDate` | Date de fermeture prévue | Date de fermeture prévue de l’opportunité | Chaîne | Date de fermeture prévue de l’opportunité. |
| `expectedRevenue.amount` | Chiffre d&#39;affaires souhaité | Total du chiffre d’affaires souhaité de l’opportunité | Chaîne | Chiffre d’affaires calculé, basé sur le montant et la probabilité. |
| `fiscalQuarter` | Trimestre d&#39;exercice | Trimestre fiscal de l’opportunité | Chaîne | Trimestre fiscal ciblé pour l’opportunité. |
| `fiscalYear` | Exercice annuel | Exercice de l’opportunité | Chaîne | Exercice fiscal ciblé pour l’opportunité. |
| `forecastCategory` | Type de prévision | Catégorie de prévision d’opportunité | Chaîne | Catégorie de prévision déterminée par la valeur Phase de l’opportunité. |
| `forecastCategoryName` | Nom du type de prévision | Nom de la catégorie des prévisions d’opportunités | Chaîne | Nom de la catégorie de prévision affiché dans les rapports pour une catégorie de prévision particulière. |
| `isClosed` | Drapeau fermé | Opportunité fermée | Chaîne | Indicateur qui indique si l’opportunité est fermée. |
| `isWon` | Drapeau Won | Opportunité remportée | Chaîne | Indicateur qui indique si l’opportunité est gagnée. |
| `lastActivityDate` | Date dernière activité | Dernière date d’activité | Chaîne | Date de la dernière activité pour l’opportunité. |
| `leadSource` | Source du lead | Source du prospect | Chaîne | Source de l’opportunité, par exemple publicité, partenaire ou web. |
| `nextStep` | Prochaine étape | Étape suivante de l’opportunité | Chaîne | Description de la tâche suivante pour fermer l’opportunité. |
| `opportunityAmount.amount` | Quantité d&#39;opportunités | Total du montant de l&#39;opportunité | Chaîne | Estimation du montant total des ventes pour l’opportunité. |
| `opportunityDescription` | Description de l’opportunité | Description de l’opportunité | Chaîne | Informations supplémentaires pour décrire l’opportunité, telles que des produits pouvant être vendus ou des achats précédents auprès du client. |
| `opportunityName` | Nom de l&#39;opportunité | Nom de l’opportunité | Chaîne | Objet ou nom descriptif, tel que le nom de commande ou de société attendu pour l’opportunité. |
| `opportunityQuantity` | Quantité de l’opportunité | Quantité de l’opportunité | Chaîne | Total de toutes les valeurs de champ de quantité pour tous les produits de la liste de produits associés pour l’opportunité. |
| `opportunityStage` | Étape de l’opportunité | Étape de l’opportunité | Chaîne | Étape de vente de l&#39;opportunité d&#39;aider l&#39;équipe de vente dans leurs efforts pour gagner. |
| `opportunityType` | Type de l&#39;opportunité | Type d’opportunité | Chaîne | Type affecté à l’opportunité, par exemple _Entreprise existante_ ou _Nouvelle entreprise_ |
| `probabilityPercentage` | Pourcentage de probabilité | Pourcentage de probabilité d’opportunité | Chaîne | Probabilité de fermeture de l’opportunité, exprimée sous la forme d’un pourcentage. |
