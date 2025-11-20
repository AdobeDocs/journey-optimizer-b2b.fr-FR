---
title: Champs XDM
description: Passez en revue les champs d’attribut par défaut synchronisés entre Adobe Experience Platform et Journey Optimizer B2B edition.
feature: Data Management, Integrations
role: User
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: de7f5620556a48fe6f12ed1c70e925e11ec770f1
workflow-type: tm+mt
source-wordcount: '1153'
ht-degree: 20%

---

# Champs XDM

Les données d’audience de compte sont stockées sous forme d’attributs dans les classes XDM Business Account et XDM Business Person. Les données sont régulièrement synchronisées entre Adobe Experience Platform et Journey Optimizer B2B edition. Les sections suivantes répertorient les jeux d’attributs par défaut.

>[!TIP]
>
>Vous pouvez modéliser des classes de compte professionnel XDM et de compte professionnel XDM dans une relation multiple-à-multiple à l’aide de la classe de relation de personne avec compte professionnel XDM, comme décrit dans la [documentation XDM d’Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/xdm/tutorials/relationship-b2b){target="_blank"}.

>[!NOTE]
>Les schémas Data Mirror et relationnels sont disponibles pour les détenteurs de licence des campagnes orchestrées Adobe Journey Optimizer. Ils sont également disponibles en tant que version limitée pour les utilisateurs de Customer Journey Analytics, selon votre licence et l’activation de la fonctionnalité. Contactez votre représentant Adobe pour obtenir l’accès. Les schémas relationnels sont également disponibles dans une version limitée de Adobe Journey Optimizer B2B edition.
>


## Attributs de relation de la personne avec le compte professionnel XDM

| [Propriété](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md){target="_blank"} | Nom d’affichage | Nom d’affichage B2B de Journey Optimizer | Type de données | Description |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `personRoles` | Rôles de la personne | Rôle | Tableau de chaînes | Tableau des rôles associés à la personne sur le compte, par exemple `owner, accountant, designer`. |

## Attributs de professionnel XDM

>[!IMPORTANT]
>
>L’attribut d’adresse e-mail est obligatoire et doit être renseigné pour une fonctionnalité correcte. Par défaut, le système utilise `workEmail.Address`. Si vous envisagez d’utiliser un autre attribut, contactez l’assistance Adobe avant de publier des parcours afin d’assurer une configuration correcte.<br/>
>
>Assurez-vous que l’attribut d’e-mail n’est pas nul, car cela peut avoir une incidence sur la synchronisation des données et les processus en aval.
><ul><li>Si l’attribut d’e-mail est nul dans Real-time CDP B2B et que la personne existe dans Journey Optimizer B2B edition, l’attribut dans est remplacé dans Journey Optimizer B2B edition par une valeur nulle lors de la synchronisation. Il est ensuite conservé dans Marketo Engage comme nul.<li>Si l’attribut d’e-mail est nul dans Real-time CDP B2B et que la personne n’existe pas dans Journey Optimizer B2B edition, l’enregistrement de la personne n’est pas synchronisé.<ul/>

| [Propriété](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md){target="_blank"} | Nom d’affichage | Nom d’affichage B2B de Journey Optimizer | Type de données | Description |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `b2b.isMarketingSuspended` | Indicateur de suspension marketing | Marketing interrompu | Booléen | La valeur indique si le marketing est suspendu pour la personne. |
| `b2b.marketingSuspendedCause` | Cause du marketing interrompu | Cause du marketing interrompu | Chaîne | Si le marketing est suspendu pour la personne, cette propriété en indique la raison. |
| `b2b.personStatus` | Statut Individu | Statut du lead | Chaîne | Champ d’enregistrement du statut de vente/marketing actuel de la personne. |
| `consents.marketing.email.reason` | Motif d’opt-out | Raison du désabonnement | Chaîne | Raison associée au processus d’opt-out des e-mails. |
| `consents.marketing.email.val` | Désabonné ou désabonnée | Désabonné ou désabonnée | Chaîne | Si le désabonnement est vrai (par exemple, valeur = 1), définissez `consents.marketing.email.val` comme (n). Si le désabonnement a la valeur false (par exemple, valeur = 0), définissez `consents.marketing.email.val` comme nul. |
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
| `workAddress.postalCode` | Code postal | Code postal | Chaîne | Code postal de l’emplacement. Les codes postaux ne sont pas disponibles pour tous les pays. Dans certains pays, il ne contient qu&#39;une partie du code postal. |
| `workAddress.state` | État | État | Chaîne | Nom de l’état de l’adresse. Il s’agit d’un champ à structure libre. |
| `workAddress.street1` | Rue 1 | Adresse | Chaîne | Informations au niveau de la rue du Principal, numéro de l’appartement, numéro de la rue et nom de la rue. |
| `workEmail.address` | Adresse | Adresse e-mail | Chaîne | **Champ obligatoire** <br/>Adresse technique, par exemple, `<name@domain.com>` telle que définie communément dans les normes RFC2822 et suivantes. |
| `workEmail.status` | Statut | E-mail interrompu | Chaîne | Indication quant à la possibilité d’utiliser l’adresse e-mail. |
| `workPhone.number` | Nombre | Numéro de téléphone | Chaîne | Numéro de téléphone professionnel. |

## Attributs du compte professionnel XDM

>[!IMPORTANT]
>
>L’attribut `accountName` est obligatoire. S’il est vide pour un compte dans une audience de compte, ce compte n’est pas ingéré et est omis des parcours de compte et des groupes d’achat qui référencent l’audience.

| [Propriété](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/account/account-details.schema.md){target="_blank"} | Nom d’affichage | Nom d’affichage B2B de Journey Optimizer | Type de données | Description |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `accountBillingAddress.city` | Ville | Ville | Chaîne | Nom de la ville utilisé dans l’adresse de facturation. |
| `accountBillingAddress.country` | Pays | Pays | Chaîne | Nom du territoire administré par le gouvernement utilisé dans l’adresse de facturation. À l’exception de `xdm:countryCode`, il s’agit d’un champ à structure libre pouvant contenir le nom du pays dans n’importe quelle langue. |
| `accountBillingAddress.postalCode` | Code postal | Code postal de l’adresse | Chaîne | Code postal de l’emplacement de l’adresse de facturation. Les codes postaux ne sont pas disponibles pour tous les pays. Dans certains pays, il ne contient qu&#39;une partie du code postal. |
| `accountBillingAddress.region` | Région | Région de l’adresse | Chaîne | Partie de l’adresse de facturation correspondant à la région, au pays ou au district. |
| `accountBillingAddress.state` | État | État | Chaîne | Nom de l’état de l’adresse de facturation. Il s’agit d’un champ à structure libre. |
| `accountBillingAddress.street1` | Rue 1 | Rue 1 | Chaîne | Informations au niveau de la rue par Principal pour l’adresse de facturation, qui incluent généralement le numéro de l’appartement, le numéro de la rue et le nom de la rue. |
| `accountName` | Nom | Nom | Chaîne | **Champ obligatoire** <br/>Nom de la société. Ce champ peut contenir jusqu’à 255 caractères. |
| `accountOrganization.annualRevenue.amount` | Revenus annuels | Revenus annuels | Nombre | Montant estimé du chiffre d’affaires annuel de l’organisation. |
| `accountOrganization.industry` | Secteur industriel | Secteur industriel | Chaîne | L&#39;industrie attribuée à l&#39;organisation. Il s’agit d’un champ à structure libre et il est conseillé d’utiliser une valeur structurée pour les requêtes ou d’utiliser la propriété `xdm:classifier`. |
| `accountOrganization.logoUrl` | Logo URL | Logo URL | Chaîne | Chemin à associer à l’URL d’une instance Salesforce (par exemple, `https://yourInstance.salesforce.com/`) pour générer une URL afin de demander l’image de profil du réseau social associée au compte. L’URL générée renvoie une redirection HTTP (code 302) vers l’image de profil du réseau social pour le compte. |
| `accountOrganization.numberOfEmployees` | Nombre d&#39;employés | Nombre d&#39;employés | Nombre entier | Nombre d’employés dans l’organisation. |
| `accountOrganization.SICCode` | Code SIC | Code SIC | Chaîne | Le code SIC (Standard Industrial Classification) est un code à quatre chiffres qui classe les secteurs d’activité auxquels appartiennent les entreprises en fonction de leurs activités commerciales. |
| `accountOrganization.website` | URL du site web | Nom du domaine | Chaîne | URL du site web de l’organisation. |
| `accountPhone.number` | S/O | Numéro de téléphone du compte | Chaîne | Numéro de téléphone associé au compte. |
| `accountSourceType` | S/O | Type de source | Chaîne | Type de Source du compte. |

<!-- ## XDM Business Opportunity attributes

Additionally, opportunity data is stored as attributes in the XDM Business Opportunity class, which can be associated with the XDM Business Account class through a many-to-one relationship, as described in the [Exerience Platform documentation](https://experienceleague.adobe.com/fr/docs/experience-platform/xdm/tutorials/relationship-b2b#relationship-field){target="_blank"}.

|[Property](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/marketo/opportunity-marketo.schema.md){target="_blank"} |Display name |Journey Optimizer B2B display name |Data type |Description |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
|`expectedCloseDate` | Expected Close Date  | Expected opportunity close date   | String | Expected date of closure for the opportunity.   |
|`expectedRevenue.amount` | Expected Revenue  | Total opportunity expected revenue   | String | Calculated revenue based on the Amount and Probability.   |
|`fiscalQuarter` | Fiscal Quarter   | Opportunity fiscal quarter  | String | The targeted fiscal quarter for the opportunity.   |
|`fiscalYear` | Fiscal Year   | Opportunity fiscal year   | String | The targeted fiscal year for the opportunity.   |
|`forecastCategory`|Forecast Category | Opportunity Forecast category | String | Forecast Category determined by the opportunity Stage value. |
|`forecastCategoryName`|Forecast Category Name | Opportunity forecast category name | String | Forecast category name that is displayed in reports for a particular forecast category. |
|`isClosed` | Closed Flag  | Opportunity closed   | String | Flag that indicates if the opportunity is closed.   |
|`isWon` | Won Flag  | Opportunity won   | String | Flag that indicates if the opportunity is won.  |
|`lastActivityDate` | Last Activity Date  | Last activity date   | String | Last activity date for the opportunity.  |
|`leadSource` | Lead Source  | Lead source   | String | Source of the opportunity, such as Advertisement, Partner, or Web.   |
|`nextStep` | Next Step  | Opportunity next step   | String | Description of the next task for closing the opportunity.   |
|`opportunityAmount.amount` | Opportunity Amount  | Total Opportunity Amount | String | Estimated total sale amount for the opportunity.   |
|`opportunityDescription` | Opportunity Description   | Opportunity description  |String  | Additional information to describe the opportunity, such as possible products to sell or past purchases from the customer. |
|`opportunityName` | Opportunity Name   | Opportunity name |String  | Subject or descriptive name, such as the expected order or company name, for the opportunity. |
|`opportunityQuantity` | Opportunity Quantity  | Opportunity quantity   | String | Total of all quantity field values for all products in the related Products list for the opportunity.   |
|`opportunityStage` | Opportunity Stage   | Opportunity stage   | String | Sales stage of the opportunity to aid the sales team in their efforts to win it.  |
|`opportunityType` | Opportunity Type   | Opportunity type   | String | Type assigned to the opportunity, such as _Existing Business_ or _New Business_  |
|`probabilityPercentage` | Probability Percentage  | Opportunity probability percentage  | String | Likelihood of closing the opportunity, stated as a percentage.  |
 -->