---
title: Protocoles de tracking et de diffusion des e-mails
description: Découvrez comment configurer des protocoles dans Marketo Engage pour une utilisation par Journey Optimizer B2B Edition (fonctionnalités de tracking et de canal e-mail).
feature: Setup, Channels
role: Admin
exl-id: 3d56f147-ad0a-4686-b14e-375c2eca8806
source-git-commit: 4bbe641305065888a59b3e77357e9b39fa6d402e
workflow-type: ht
source-wordcount: '1798'
ht-degree: 100%

---

# Protocoles de tracking et de diffusion des e-mails

Adobe Journey Optimizer B2B Edition exploite les fonctions de canal e-mail et le suivi des événements dans Marketo Engage. Pour que la diffusion d’e-mails fonctionne comme prévu pour les organisations qui utilisent des paramètres de pare-feu ou de serveur proxy restrictifs, l’administration système doit ajouter certains domaines et plages d’adresses IP à la liste autorisée.

>[!NOTE]
>
>Si votre organisation utilise déjà l’instance Marketo Engage connectée pour exécuter ses opérations marketing, ces protocoles et configurations sont sans doute déjà en place.

Assurez-vous que les domaines suivants (y compris l’astérisque) sont ajoutés sur la liste autorisée pour activer toutes les ressources Marketo Engage et tous les web sockets :

* `*.experience.adobe.com`
* `*.adobe.net`
* `*.marketo.com`
* `*.marketodesigner.com`
* `*.mktoweb.com`

Suivez les étapes ci-après pour assurer le tracking et la diffusion des e-mails :

1. [Créer des enregistrements DNS pour ](#create-dns-records-for-landing-pages-and-email)
1. [Configurer SPF et DKIM](#set-up-spf-and-dkim)
1. [Configurer DMARC](#set-up-dmarc)
1. [Configurer des enregistrements MX pour votre domaine](#set-up-mx-records-for-your-domain)
1. [Ajouter des adresses IP sortantes sur les listes autorisées](#outbound-ip-addresses)

## Créer des enregistrements DNS pour les <!-- landing pages and --> l’e-mail

La connexion d’un enregistrement CNAME permet aux spécialistes du marketing d’héberger les versions web des e-mails, des pages de destination et des blogs avec une valorisation de branding cohérente qui améliore le trafic et les conversions. Il est vivement recommandé d’ajouter les CNAME à l’hôte de domaine racine pour que Marketo Engage héberge vos ressources web axées marketing. En tant qu’administrateur ou administratrice, vous devez travailler avec votre équipe marketing pour planifier et implémenter un enregistrement CNAME pour les liens de tracking inclus dans les e-mails envoyés via Marketo Engage.
<!-- As an administrator, you should work with your Marketing team to plan and implement two CNAME records. The first one is for landing page URLs, so that the landing pages appear in URLs that reflect your domain and not Adobe Marketo Engage (the actual host). The second one is for the tracking links that are included in the emails sent through Marketo Engage.

### Add the CNAME for landing pages

Add the landing page CNAME to your DNS record, so that `[YourLandingPageCNAME]` points to the unique account string that is assigned to your landing pages. Log in to your domain registrar's site and enter the landing page CNAME and account string. This entry usually involves three fields:

* Alias: Enter `[YourLandingPageCNAME]`
* Type: CNAME
* Point to: Enter `[MunchkinID].mktoweb.com`
-->

### Ajouter des CNAME pour les liens de tracking e-mail

Ajoutez le CNAME d’e-mail afin que `[YourEmailCNAME]` pointe vers `[MktoTrackingLink]`, qui est le lien de tracking par défaut attribué par Marketo Engage, au format suivant :

`[YourEmailCNAME].[YourDomain].com` DANS LE `[MktoTrackingLink]` CNAME

Par exemple :

`pages.abc.com IN CNAME mkto-a0244.com`

>[!NOTE]
>
>La valeur `[MktoTrackingLink]` doit être le [domaine de branding](../admin/configure-channels-emails.md#branding-domains) par défaut.

### Fournir le certificat SSL

Contactez l’[assistance Adobe](https://experienceleague.adobe.com/home?lang=fr&support-tab=home#support){target="_blank"} pour commencer le processus d’approvisionnement d’un certificat SSL.

Le traitement peut prendre jusqu’à trois jours ouvrables.

## Configurer SPF et DKIM

Votre équipe marketing doit fournir les informations DKIM (Domain Keys Identified Mail) à ajouter à votre enregistrement de ressource DNS. Pour configurer DKIM et SPF (Sender Policy Framework), procédez comme suit, puis avertissez votre équipe marketing une fois la mise à jour effectuée.

1. Pour configurer SPF, ajoutez la ligne suivante aux entrées DNS :

   ```
   [CompanyDomain] IN TXT v=spf1 mx ip4:[CorpIP]  
   include: mktomail.com ~all
   ```

   Si vous avez déjà un enregistrement SPF existant dans l’entrée DNS, ajoutez simplement ce qui suit :

   ```
   include: mktomail.com
   ```

   Remplacez `CompanyDomain` par le domaine principal de votre site web (tel que `company.com/`) et `CorpIP` par l’adresse IP du serveur de messagerie de votre entreprise (tel que `255.255.255.255`). Si vous envisagez d’envoyer des e-mails à partir de plusieurs domaines via Marketo Engage, ajoutez cette ligne pour chaque domaine (sur une seule ligne).

1. Pour DKIM, créez des enregistrements de ressources DNS pour chaque domaine.

   Ajoutez les enregistrements hôtes et les valeurs TXT pour chaque domaine :

   `[DKIMDomain1]` : l’enregistrement hôte est `[HostRecord1]` et la valeur TXT est `[TXTValue1]`.

   `[DKIMDomain2]` : l’enregistrement hôte est `[HostRecord2]` et la valeur TXT est `[TXTValue2]`.

   Copiez les valeurs `HostRecord` et `TXTValue` pour chaque domaine DKIM après avoir suivi les [instructions](https://experienceleague.adobe.com/fr/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"} de la documentation de Marketo Engage. Vous pouvez vérifier les domaines dans Journey Optimizer B2B Edition (voir [SPF/DKIM](../admin/configure-channels-emails.md#spfdkim)).

## Configurer DMARC

DMARC (Domain-based Message Authentication, Reporting, and Conformance) est un protocole d’authentification utilisé pour aider les organisations à protéger leur domaine contre une utilisation non autorisée. Il étend les protocoles d’authentification existants, tels que SPF et DKIM, pour informer les serveurs de destination des actions à entreprendre en cas d’échec d’authentification sur leur domaine. DMARC est facultatif, mais est vivement recommandé, car il permet de protéger votre marque et votre réputation. Les principaux fournisseurs, tels que Google et Yahoo, ont commencé à exiger l’utilisation de DMARC pour les expéditeurs en masse depuis février 2024.

Pour que DMARC fonctionne, vous devez disposer d’au moins l’un des enregistrements TXT DNS suivants :

* Un SPF valide
* Un enregistrement DKIM valide pour votre domaine FROM (recommandé pour Marketo Engage et Journey Optimizer B2B Edition)

Vous devez également disposer d’un enregistrement TXT de DNS spécifique à DMARC pour votre domaine `FROM:`. Vous pouvez éventuellement définir une adresse e-mail qui spécifie l’emplacement auquel les rapports DMARC doivent être envoyés au sein de votre organisation pour la surveillance des rapports.

### Exemple de workflow DMARC

>[!TIP]
>
>Il est recommandé d’implémenter DMARC en tant que _déploiement lent_. Faites passer votre politique DMARC de `p=none` à `p=quarantine`, puis à `p=reject` au fur et à mesure que vous comprenez l’impact potentiel, puis définissez votre politique DMARC sur un alignement relâché sur SPF et DKIM.

Si vous recevez des rapports DMARC, procédez comme suit :

1. Utilisez `p=none` et analysez les commentaires et les rapports que vous recevez. Les rapports indiquent à la personne destinataire de n’effectuer aucune action sur les messages qui ne passent pas l’authentification, tout en envoyant des rapports d’e-mail à l’expéditeur ou à l’expéditrice.

   * Si l’authentification des messages légitimes échoue, vérifiez et corrigez les problèmes liés à SPF/DKIM.

   * Déterminez si SPF ou DKIM sont alignés et réussissent l’authentification pour tous les e-mails légitimes.

   * Examinez les rapports pour vous assurer que les résultats sont conformes aux attentes en fonction de vos politiques SPF/DKIM.

1. Ajustez la politique sur `p=quarantine`, qui indique au serveur de messagerie de réception de mettre en quarantaine les e-mails dont l’authentification échoue (en plaçant généralement ces messages dans le dossier des spams).

   Examinez les rapports pour vous assurer que les résultats sont conformes à vos attentes.

1. Si le comportement des messages au niveau `p=quarantine` vous convient, vous pouvez ajuster la politique sur (`p=reject`).

   La politique de refus indique à la personne destinataire de refuser complètement (rebond) tout e-mail pour le domaine qui ne réussit pas l’authentification. Lorsque cette politique est activée, seul un e-mail qui est vérifié comme étant authentifié à 100 % par votre domaine a une chance d’être placé en boîte de réception.

   >[!CAUTION]
   >
   >Utilisez cette politique avec précaution et déterminez si elle est appropriée pour votre organisation.

### Création de rapports DMARC

DMARC permet de recevoir des rapports concernant les e-mails qui échouent l’authentification SPF/DKIM. Deux rapports différents sont générés par les services du FAI dans le cadre du processus d’authentification. Les expéditeurs et expéditrices peuvent recevoir ces rapports par le biais des balises RUA/RUF dans leur politique DMARC.

* **Rapports agrégés (RUA)** : ne contiennent aucune information d’identification personnelle (PII) susceptible d’être sensible au RGPD (Règlement général sur la protection des données).

* **Rapports judiciaires (RUF)** : contiennent des adresses e-mail sensibles au RGPD. Avant de mettre en œuvre ce rapport, vérifiez la politique de votre organisation en matière de traitement des informations devant être conforme au RGPD.

Ces rapports sont principalement utilisés pour recevoir une vue d’ensemble des e-mails faisant l’objet de tentatives d’usurpation. Il s’agit de rapports hautement techniques qui sont mieux gérés par un outil tiers.

### Exemples d’enregistrements DMARC

* Enregistrement minimum : `v=DMARC1; p=none`

* Enregistrement redirigé vers une adresse e-mail pour la réception des rapports : `v=DMARC1; p=none;  rua=mailto:emaill@domain.com;  ruf=mailto:email@domain.com`

### Balises DMARC

Les enregistrements DMARC comportent plusieurs composants appelés _balises DMARC_. Chaque balise possède une valeur qui spécifie un certain aspect de DMARC.

| Nom de la balise | Utilisation | Fonction | Exemple | Valeur par défaut |
|-----------|------------------------|-----------|----------|-----------------------------------|
| `v` | Obligatoire | Spécifie la version. Il n’existe qu’une seule version, elle a donc une valeur fixe de `v=DMARC1`. | V=DMARC1 DMARC1 | DMARC1 |
| `p` | Obligatoire | Spécifie la politique DMARC, qui ordonne à la personne destinataire de signaler, mettre en quarantaine ou rejeter les e-mails dont les contrôles d’authentification échouent. | `p=none`, `p=quarantine` ou `p=reject` | - |
| `fo` | Facultatif | Permet à la personne propriétaire du domaine de spécifier des options de création de rapports. | `0` : génération d’un rapport en cas d’échec de SPF et DKIM <br> `1` : génération d’un rapport en cas d’échec de SPF ou DKIM <br> `d` : génération d’un rapport en cas d’échec de DKIM <br> `s` : génération d’un rapport en cas d’échec de SPF | `1` (recommandé pour les rapports DMARC) |
| `pct` | Facultatif | Indique le pourcentage de messages soumis à un filtrage. | `pct=20` | `100` |
| `rua` | Facultatif (recommandé) | Désigne l’emplacement de diffusion des rapports agrégés. | `rua=mailto:aggrep@example.com` | - |
| `ruf` | Facultatif (recommandé) | Désigne l’emplacement de diffusion des rapports judiciaires. | `ruf=mailto:authfail@example.com` | - |
| `sp` | Facultatif | Indique la politique DMARC pour les sous-domaines du domaine parent. | `sp=reject` | - |
| `adkim` | Facultatif | Indique un alignement strict (`s`) ou relâché (`r`). L’alignement relâché signifie que le domaine est utilisé dans la signature DKIM et peut être un sous-domaine de l’adresse `From:`. Un alignement strict signifie que le domaine est utilisé dans la signature DKIM et doit correspondre exactement au domaine utilisé dans l’adresse `From:`. | `adkim=r` | `r` |
| `aspf` | Facultatif | Peut être strict (`s`) ou relâché (`r`). Le mode relâché signifie que le domaine Return-Path peut être un sous-domaine de l’adresse `From:`. Le mode strict signifie que le domaine Return-Path doit correspondre exactement à l’adresse `From:`. | `aspf=r` | `r` |

Pour plus d’informations sur DMARC et toutes ses options, consultez [https://dmarc.org/](https://dmarc.org/){target="_blank"}.

### Implémentation de DMARC pour Marketo Engage

Il existe deux types d’alignement pour DMARC :

* Alignement de **DKIM** (Domain Keys Identified Mail) : le domaine spécifié dans l’en-tête `From:` d’un e-mail correspond à la signature DKIM. La signature DKIM contient une valeur `d=` où le domaine est spécifié pour correspondre au domaine d’en-tête `From:`.

  L’alignement DKIM valide si l’expéditeur ou l’expéditrice a l’autorisation d’envoyer des e-mails à partir du domaine et vérifie qu’aucun contenu n’a été modifié pendant le transit des e-mails. Pour mettre en œuvre un DMARC aligné sur DKIM, procédez comme suit :

   * Configurez DKIM pour le domaine MAIL FROM de votre message. Suivez les [instructions](https://experienceleague.adobe.com/fr/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"} de la documentation de Marketo Engage.

   * Configurez DMARC pour le domaine DKIM MAIL FROM.

  >[!NOTE]
  >
  >L’alignement DKIM est recommandé pour Marketo Engage.

* Alignement **SPF** (Sender Policy Framework) : le domaine de l’en-tête `From:` doit correspondre au domaine de l’en-tête Return-Path:. Si les deux domaines DNS sont identiques, le SPF correspond (s’aligne) et donne un résultat positif. Pour mettre en œuvre le DMARC aligné sur SPF, procédez comme suit :

   * Configurez le domaine Return-Path de la marque.

      * Configurez l’enregistrement SPF approprié.
      * Modifiez l’enregistrement MX pour revenir au MX par défaut du centre de données à partir duquel votre courrier est envoyé.

   * Configurez DMARC pour le domaine Return-Path de la marque.

  >[!NOTE]
  >
  >L’alignement SPF strict n’est pas pris en charge ni recommandé pour Marketo Engage.

### Adresses IP dédiées et pool partagé

Si vous envoyez des e-mails via Marketo Engage sur une adresse IP dédiée et n’avez pas implémenté de Return-Path (ou ne savez pas si vous l’avez fait), ouvrez un ticket auprès de l’[assistance Adobe](https://experienceleague.adobe.com/home?lang=fr&support-tab=home#support){target="_blank"}.

Les adresses IP de confiance sont un groupe partagé d’adresses IP qui sont réservées aux personnes dont le volume d’envoi est inférieur à 75 000 par mois et qui ne remplissent pas les critères pour une adresse IP dédiée. Ces personnes doivent également répondre aux exigences des bonnes pratiques.

* Si vous envoyez des e-mails via Marketo Engage à l’aide d’un pool partagé d’adresses IP, vous pouvez vérifier si vous remplissez les critères pour les adresses IP de confiance en [demandant le programme de plage d’envoi d’adresses IP de confiance](https://na-sjg.marketo.com/lp/marketoprivacydemo/Trusted-IP-Sending-Range-Program.html){target="_blank"}. Le Return-Path de la marque est inclus lors de l’envoi à partir des adresses IP de confiance Marketo Engage. Si votre demande est approuvée pour ce programme, contactez l’assistance Adobe pour configurer le Return-Path de la marque.

* Si vous envoyez plus de 100 000 messages par mois et souhaitez envoyer un e-mail par le biais de Marketo Engage à l’aide d’adresses IP partagées, contactez l’équipe Adobe en charge des comptes (votre gestionnaire de compte) pour acheter une adresse IP dédiée.

## Configurer des enregistrements MX pour votre domaine

Un enregistrement MX vous permet de recevoir des e-mails du domaine depuis lequel vous envoyez des e-mails afin de traiter les réponses et les répondeurs automatiques. Si vous effectuez un envoi à partir de votre domaine d’entreprise, il est probablement déjà configuré. Si ce n’est pas le cas, vous pouvez généralement le configurer pour qu’il soit mappé à votre enregistrement MX de domaine d’entreprise.

## Adresses IP sortantes

Une connexion sortante est une connexion établie par Marketo Engage à un serveur sur Internet en votre nom. Votre service informatique et certains partenaires/fournisseurs peuvent utiliser des listes autorisées pour restreindre l’accès aux serveurs. Si tel est le cas, vous devez leur fournir des blocs d’adresses IP sortantes Marketo Engage à ajouter à leurs listes autorisées.

<!-- ### Webhooks

Marketo Engage webhooks are an outbound integration mechanism. When a Smart Campaign executes a _Call Webhook_ flow action, it makes an HTTP request to an external web service. If the web service publisher uses an allowlist on the firewall of the network where the external web service is located, the publisher must add the IP address blocks listed below to their allowlist. For more information, see [Create a webhook](https://experienceleague.adobe.com/fr/docs/marketo/using/product-docs/administration/additional-integrations/create-a-webhook){target="_blank"} and [Call Webhook](https://experienceleague.adobe.com/fr/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/call-webhook){target="_blank"} in the Marketo Engage documentation.

### CRM sync

Marketo Engage Salesforce CRM Sync and Microsoft Dynamics Sync are integration mechanisms that make outbound HTTP requests to APIs published by your CRM vendor. Ensure that your IT organization does not block any of the IP address blocks below from accessing your CRM vendor APIs. For more information, see [Add an Existing Salesforce Field to the Marketo Sync](https://experienceleague.adobe.com/fr/docs/marketo/using/product-docs/crm-sync/salesforce-sync/sfdc-sync-details/add-an-existing-salesforce-field-to-the-marketo-sync){target="_blank"} and [Understanding the Microsoft Dynamics Sync](https://experienceleague.adobe.com/fr/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/understanding-the-microsoft-dynamics-sync){target="_blank"} in the Marketo Engage documentation. -->

## Blocs d’adresses IP sortantes

Les listes suivantes couvrent tous les serveurs Marketo Engage qui effectuent des appels sortants. Consultez ces listes pour configurer une liste autorisée d’adresses IP, un serveur, un pare-feu, une liste de contrôle d’accès, un groupe de sécurité ou un service tiers afin de recevoir des connexions sortantes de Marketo Engage.

| Bloc d’adresses IP (notation CIDR) | Adresse IP individuelle |
| ------------------------ | --------------------- |
| <ul><li>`94.236.119.0/26`</li><li>`103.237.104.0/22`</li><li>`130.248.172.0/24`</li><li>`130.248.173.0/24`</li><li>`130.248.244.88/29`</li><li>`185.28.196.0/22`</li><li>`192.28.144.0/20`</li><li>`192.28.160.0/19`</li><li>`199.15.212.0/22`</li></ul> | <ul><li>`13.237.155.207`</li><li>`13.55.192.247`</li><li>`18.200.201.81`</li><li>`34.247.24.245`</li><li>`35.165.244.220`</li><li>`44.235.171.179`</li><li>`52.20.211.99`</li><li>`52.64.109.86`</li><li>`54.160.246.246`</li><li>`54.212.167.17`</li><li>`54.220.138.65`</li><li>`54.237.141.197`</li><li>`130.248.168.16`</li><li>`130.248.168.17`</li></ul> |
