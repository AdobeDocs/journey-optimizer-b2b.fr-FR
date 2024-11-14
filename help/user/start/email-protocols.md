---
title: Protocoles de tracking et de diffusion email
description: Découvrez comment configurer des protocoles en Marketo Engage pour que Journey Optimizer B2B edition les utilise pour le suivi et les fonctionnalités de canal de courrier électronique.
feature: Setup
role: Admin
source-git-commit: a8ca8b99ddf33b4a64b42b751f7be798274d0084
workflow-type: tm+mt
source-wordcount: '1798'
ht-degree: 0%

---

# Protocoles de tracking et de diffusion email

Adobe Journey Optimizer B2B edition exploite les fonctions de canal de courrier électronique et le suivi des événements dans Marketo Engage. Pour s’assurer que la diffusion par courrier électronique fonctionne comme prévu pour les organisations qui utilisent un pare-feu restrictif ou des paramètres de serveur proxy, un administrateur système doit ajouter à la liste autorisée certains domaines et plages d’adresses IP.

>[!NOTE]
>
>Si votre entreprise utilise déjà l’instance de Marketo Engage connectée pour exécuter ses opérations marketing, ces protocoles et configurations doivent déjà être en place.

Assurez-vous que les domaines suivants (y compris l’astérisque) sont ajoutés à la liste autorisée pour activer toutes les ressources du Marketo Engage et toutes les sockets web :

* `*.experience.adobe.com`
* `*.adobe.net`
* `*.marketo.com`
* `*.marketodesigner.com`
* `*.mktoweb.com`

Pour assurer le suivi et la diffusion des emails, procédez comme suit :

1. [Création d’enregistrements DNS pour ](#create-dns-records-for-landing-pages-and-email)
1. [Configuration de SPF et DKIM](#set-up-spf-and-dkim)
1. [Configuration de DMARC](#set-up-dmarc)
1. [Configuration des enregistrements MX pour votre domaine](#set-up-mx-records-for-your-domain)
1. [Ajout d’adresses IP sortantes aux listes autorisées](#outbound-ip-addresses)

## Créer des enregistrements DNS pour le <!-- landing pages and --> email

La connexion à un enregistrement CNAME permet aux marketeurs d’héberger des versions web d’emails, de landing pages et de blogs avec une valorisation de marque cohérente qui améliore le trafic et les conversions. Il est vivement recommandé d’ajouter les CNAME à l’hôte de domaine racine pour que Marketo Engage héberge vos ressources web axées sur le marketing. En tant qu’administrateur, vous devez travailler avec votre équipe marketing pour planifier et mettre en oeuvre un enregistrement CNAME pour les liens de suivi inclus dans les emails envoyés par le biais de Marketo Engage.
<!-- As an administrator, you should work with your Marketing team to plan and implement two CNAME records. The first one is for landing page URLs, so that the landing pages appear in URLs that reflect your domain and not Adobe Marketo Engage (the actual host). The second one is for the tracking links that are included in the emails sent through Marketo Engage.

### Add the CNAME for landing pages

Add the landing page CNAME to your DNS record, so that `[YourLandingPageCNAME]` points to the unique account string that is assigned to your landing pages. Log in to your domain registrar's site and enter the landing page CNAME and account string. This entry usually involves three fields:

* Alias: Enter `[YourLandingPageCNAME]`
* Type: CNAME
* Point to: Enter `[MunchkinID].mktoweb.com`
-->

### Ajout du CNAME pour les liens de suivi des emails

Ajoutez le CNAME de messagerie de sorte que `[YourEmailCNAME]` pointe vers `[MktoTrackingLink]`, qui est le lien de suivi par défaut attribué par le Marketo Engage, au format :

`[YourEmailCNAME].[YourDomain].com` DANS CNAME `[MktoTrackingLink]`

Par exemple :

`pages.abc.com IN CNAME mkto-a0244.com`

>[!NOTE]
>
>La valeur `[MktoTrackingLink]` doit être le domaine de valorisation de marque par défaut.

### Configuration du certificat SSL

Contactez le [service d’Adobe](https://experienceleague.adobe.com/home?lang=en&amp;support-tab=home#support){target="_blank"} pour lancer le processus de mise en service d’un certificat SSL.

Ce processus peut prendre jusqu’à trois jours ouvrables.

## Configuration de SPF et DKIM

Votre équipe marketing doit fournir les informations DKIM (Domain Keys Identified Mail) à ajouter à votre enregistrement de ressource DNS. Suivez ces étapes pour configurer DKIM et SPF (Sender Policy Framework), puis informez votre équipe marketing de la mise à jour.

1. Pour configurer SPF, ajoutez la ligne suivante aux entrées DNS :

   ```
   [CompanyDomain] IN TXT v=spf1 mx ip4:[CorpIP]  
   include: mktomail.com ~all
   ```

   Si vous disposez déjà d’un enregistrement SPF dans l’entrée DNS, ajoutez-y simplement les éléments suivants :

   ```
   include: mktomail.com
   ```

   Remplacez `CompanyDomain` par le domaine principal de votre site web (par exemple `company.com/`) et `CorpIP` par l’adresse IP de votre serveur de messagerie d’entreprise (par exemple `255.255.255.255`). Si vous prévoyez d’envoyer des emails à partir de plusieurs domaines par le biais de Marketo Engage, ajoutez cette ligne pour chaque domaine (sur une seule ligne).

1. Pour DKIM, créez des enregistrements de ressource DNS pour chaque domaine.

   Ajoutez les enregistrements d’hôte et les valeurs TXT pour chaque domaine :

   `[DKIMDomain1]` : l’enregistrement hôte est `[HostRecord1]` et la valeur TXT est `[TXTValue1]`.

   `[DKIMDomain2]` : l’enregistrement hôte est `[HostRecord2]` et la valeur TXT est `[TXTValue2]`.

   Copiez `HostRecord` et `TXTValue` pour chaque domaine DKIM après avoir suivi les [instructions](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"} de la documentation du Marketo Engage. Vous pouvez vérifier les domaines dans Journey Optimizer B2B edition (voir [SPF/DKIM](../admin/configure-channels-emails.md#spfdkim)).

## Configuration de DMARC

DMARC (Domain-based Message Authentication, Reporting, and Conformance) est un protocole d’authentification utilisé pour aider les entreprises à protéger leur domaine contre toute utilisation non autorisée. Il étend les protocoles d’authentification existants, tels que SPF et DKIM, pour informer les serveurs des destinataires des actions à entreprendre en cas d’échec de l’authentification sur leur domaine. DMARC est facultatif, mais est vivement recommandé car il permet de protéger votre marque et votre réputation. À compter de février 2024, les principaux fournisseurs tels que Google et Yahoo ont commencé à exiger l’utilisation de DMARC pour les expéditeurs en masse.

Pour que DMARC fonctionne, vous devez disposer d’au moins un des enregistrements TXT DNS suivants :

* Un SPF valide
* Un enregistrement DKIM valide pour votre formulaire FROM : domaine (recommandé pour Marketo Engage et Journey Optimizer B2B edition)

Vous devez également disposer d’un enregistrement TXT DNS spécifique à DMARC pour votre domaine `FROM:`. Vous pouvez éventuellement définir une adresse électronique qui spécifie l’emplacement des rapports DMARC au sein de votre organisation pour la surveillance des rapports.

### Exemple de workflow DMARC

>[!TIP]
>
>Il est recommandé d’implémenter DMARC en tant que _déploiement lent_. Transférez votre stratégie DMARC de `p=none` à `p=quarantine`, puis à `p=reject` lorsque vous comprendrez l’impact potentiel, et définissez votre stratégie DMARC pour assouplir l’alignement sur SPF et DKIM.

Si vous recevez des rapports DMARC, procédez comme suit :

1. Utilisez `p=none` et analysez les commentaires et les rapports que vous recevez. Les rapports indiquent au destinataire d’effectuer aucune action contre les messages dont l’authentification échoue et d’envoyer des rapports par courrier électronique à l’expéditeur.

   * Si les messages légitimes échouent à l’authentification, passez en revue et corrigez les problèmes avec SPF/DKIM.

   * Déterminez si SPF ou DKIM sont harmonisés et transmettent une authentification pour tous les emails légitimes.

   * Consultez les rapports pour vous assurer que les résultats correspondent aux attentes en fonction de vos stratégies SPF/DKIM.

1. Réglez la stratégie sur `p=quarantine`, ce qui indique au serveur de messagerie de réception de mettre en quarantaine les emails qui ne parviennent pas à s’authentifier (en plaçant généralement ces messages dans le dossier spam).

   Consultez les rapports pour vous assurer que les résultats correspondent à vos attentes.

1. Si vous êtes satisfait du comportement des messages au niveau `p=quarantine`, vous pouvez ajuster la stratégie à (`p=reject`).

   La stratégie de rejet indique au destinataire de refuser (rebond) tout courrier électronique pour le domaine qui échoue à l’authentification. Lorsque cette stratégie est activée, seul le courrier électronique vérifié comme authentifié à 100 % par votre domaine peut être placé dans une boîte de réception.

   >[!CAUTION]
   >
   >Utilisez cette stratégie avec précaution et déterminez si elle convient à votre entreprise.

### Rapports DMARC

DMARC permet de recevoir des rapports sur les emails qui échouent SPF/DKIM. Dans le cadre du processus d’authentification, il existe deux rapports différents générés par les services de FAI. Les expéditeurs peuvent recevoir ces rapports par le biais des balises RUA/RUF dans leur stratégie DMARC.

* **Rapports agrégés (RUA)** : ne contient aucune information d’identification personnelle pouvant être sensible au RGPD (Règlement général sur la protection des données).

* **Rapports médico-légaux (RUF)** : contiennent des adresses électroniques sensibles au RGPD. Avant de mettre en oeuvre ce rapport, vérifiez votre politique organisationnelle de gestion des informations qui doivent être conformes au RGPD.

L’utilisation principale de ces rapports consiste à recevoir un aperçu des emails qui ont fait l’objet d’une tentative d’usurpation. Il s’agit de rapports hautement techniques qui sont mieux digérés à l’aide d’un outil tiers.

### Exemples d’enregistrements DMARC

* Enregistrement minimum nu : `v=DMARC1; p=none`

* Enregistrement redirigeant vers une adresse électronique pour recevoir des rapports : `v=DMARC1; p=none;  rua=mailto:emaill@domain.com;  ruf=mailto:email@domain.com`

### Balises DMARC

Les enregistrements DMARC ont plusieurs composants appelés _Balises DMARC_. Chaque balise a une valeur qui spécifie un certain aspect de DMARC.

| Nom de la balise | Utilisation | Fonction | Exemple | Valeur par défaut |
|-----------|------------------------|-----------|----------|-----------------------------------|
| `v` | Obligatoire | Indique la version. Il n’y a qu’une seule version, elle a donc une valeur fixe `v=DMARC1`. | V=DMARC1 DMARC1 | DMARC1 |
| `p` | Obligatoire | Spécifie la stratégie DMARC, qui demande au destinataire de signaler, mettre en quarantaine ou rejeter les emails qui ne parviennent pas aux vérifications d’authentification. | `p=none`, `p=quarantine` ou `p=reject` | - |
| `fo` | Facultatif | Permet au propriétaire du domaine de spécifier des options de création de rapports. | `0` : générer un rapport si SPF et DKIM échouent tous deux <br> `1` - Générer un rapport si SPF ou DKIM échoue <br> `d` - Générer un rapport si DKIM échoue <br> `s` - Générer un rapport en cas d’échec du SPF | `1` (recommandé pour les rapports DMARC) |
| `pct` | Facultatif | Indique le pourcentage de messages soumis au filtrage. | `pct=20` | `100` |
| `rua` | Facultatif (recommandé) | Désigne l’endroit où les rapports agrégés sont distribués. | `rua=mailto:aggrep@example.com` | - |
| `ruf` | Facultatif (recommandé) | Désigne l’endroit où les rapports médico-légaux sont remis. | `ruf=mailto:authfail@example.com` | - |
| `sp` | Facultatif | Spécifie la stratégie DMARC pour les sous-domaines du domaine parent. | `sp=reject` | - |
| `adkim` | Facultatif | Spécifie un alignement strict (`s`) ou relâché (`r`). L&#39;alignement décontracté signifie que le domaine est utilisé dans la signature DKIM et peut être un sous-domaine de l&#39;adresse `From:`. Un alignement strict signifie que le domaine est utilisé dans la signature DKIM et doit être une correspondance exacte avec le domaine utilisé dans l’adresse `From:`. | `adkim=r` | `r` |
| `aspf` | Facultatif | Peut être strict (`s`) ou détendu (`r`). Le mode relâché signifie que le domaine Return-Path peut être un sous-domaine de l’adresse `From:`. Le mode strict signifie que le domaine Return-Path doit correspondre exactement à l’adresse `From:`. | `aspf=r` | `r` |

Pour plus d&#39;informations sur DMARC et toutes ses options, consultez la page [https://dmarc.org/](https://dmarc.org/){target="_blank"}.

### Mise en oeuvre de DMARC pour Marketo Engage

Il existe deux types d’alignement pour DMARC :

* Alignement **DKIM** (Domain Keys Identified Mail) : le domaine spécifié dans l’en-tête `From:` d’un email correspond à la DKIM-Signature. La signature DKIM contient une valeur `d=` où le domaine est spécifié pour la correspondance avec le domaine d’en-tête `From:`.

  L&#39;alignement DKIM valide si l&#39;expéditeur est autorisé à envoyer des mails à partir du domaine et vérifie qu&#39;aucun contenu n&#39;a été modifié lors du transit des emails. Pour mettre en oeuvre DMARC aligné sur DKIM :

   * Configurez DKIM pour le domaine MAIL FROM de votre message. Utilisez les [instructions](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"} de la documentation du Marketo Engage.

   * Configurez DMARC pour le domaine DKIM MAIL FROM.

  >[!NOTE]
  >
  >L&#39;alignement DKIM est recommandé pour Marketo Engage.

* Alignement **SPF** (Sender Policy Framework) : le domaine dans l’en-tête `From:` doit correspondre au domaine dans l’en-tête Return-Path: . Si les deux domaines DNS sont identiques, le SPF correspond (s’aligne) et donne un résultat &quot;pass&quot;. Pour mettre en oeuvre DMARC aligné sur SPF :

   * Configurez le domaine Return-Path de marque.

      * Configurez l’enregistrement SPF approprié.
      * Modifiez l’enregistrement MX pour qu’il revienne au MX par défaut du centre de données à partir duquel votre courrier est envoyé.

   * Configurez DMARC pour le domaine Return-Path de marque.

  >[!NOTE]
  >
  >L’alignement SPF strict n’est pas pris en charge ni recommandé pour Marketo Engage.

### Adresses IP dédiées et pool partagé

Si vous envoyez des courriers électroniques par le biais d’un Marketo Engage sur une adresse IP dédiée et que vous n’avez pas implémenté de chemin de retour de marque (ou que vous ne savez pas si vous en avez), ouvrez un ticket avec l’[assistance Adobe](https://experienceleague.adobe.com/home?lang=en&amp;support-tab=home#support){target="_blank"}.

Les adresses IP approuvées sont un groupe partagé d’adresses IP réservées aux utilisateurs à faible volume qui envoient moins de 75 000 par mois et qui ne remplissent pas les critères d’une adresse IP dédiée. Ces utilisateurs doivent également respecter les exigences relatives aux bonnes pratiques.

* Si vous envoyez du courrier électronique par l’intermédiaire d’un Marketo Engage à l’aide d’un pool partagé d’adresses IP, vous pouvez vérifier si vous êtes admissible pour les adresses IP approuvées en [postulant au programme de plage d’adresses IP approuvées](https://na-sjg.marketo.com/lp/marketoprivacydemo/Trusted-IP-Sending-Range-Program.html){target="_blank"}. Le chemin d’accès retour de marque est inclus lors de l’envoi à partir d’adresses IP approuvées du Marketo Engage. Si elle est approuvée pour ce programme, contactez le support Adobe pour configurer le chemin de retour de marque.

* Si vous envoyez plus de 100 000 messages par mois et souhaitez envoyer des emails par Marketo Engage à l’aide d’adresses IP partagées, contactez l’équipe du compte d’Adobe (votre gestionnaire de compte) pour acheter une adresse IP dédiée.

## Configuration des enregistrements MX pour votre domaine

Un enregistrement MX vous permet de recevoir du courrier électronique vers le domaine à partir duquel vous envoyez le courrier électronique pour traiter les réponses et les réponses automatiques. Si vous envoyez depuis votre domaine d’entreprise, il est probablement déjà configuré. Si ce n’est pas le cas, vous pouvez généralement le configurer pour mapper l’enregistrement MX de votre domaine d’entreprise.

## Adresses IP sortantes

Une connexion sortante est une connexion établie par un Marketo Engage à un serveur sur Internet en votre nom. Votre entreprise informatique et certains partenaires/fournisseurs peuvent utiliser des listes autorisées pour restreindre l’accès aux serveurs. Si tel est le cas, vous devez leur fournir des blocs d’adresses IP sortantes Marketo Engage à ajouter à leurs listes autorisées.

<!-- ### Webhooks

Marketo Engage webhooks are an outbound integration mechanism. When a Smart Campaign executes a _Call Webhook_ flow action, it makes an HTTP request to an external web service. If the web service publisher uses an allowlist on the firewall of the network where the external web service is located, the publisher must add the IP address blocks listed below to their allowlist. For more information, see [Create a webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/create-a-webhook){target="_blank"} and [Call Webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/call-webhook){target="_blank"} in the Marketo Engage documentation.

### CRM sync

Marketo Engage Salesforce CRM Sync and Microsoft Dynamics Sync are integration mechanisms that make outbound HTTP requests to APIs published by your CRM vendor. Ensure that your IT organization does not block any of the IP address blocks below from accessing your CRM vendor APIs. For more information, see [Add an Existing Salesforce Field to the Marketo Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/salesforce-sync/sfdc-sync-details/add-an-existing-salesforce-field-to-the-marketo-sync){target="_blank"} and [Understanding the Microsoft Dynamics Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/understanding-the-microsoft-dynamics-sync){target="_blank"} in the Marketo Engage documentation. -->

## Blocs d’adresses IP sortantes

Les listes suivantes couvrent tous les serveurs Marketo Engage qui effectuent des appels sortants. Consultez ces listes pour configurer une liste autorisée IP, un serveur, un pare-feu, une liste de contrôle d’accès, un groupe de sécurité ou un service tiers afin de recevoir les connexions sortantes de Marketo Engage.

| Bloc d’adresse IP (notation CIDR) | Adresse IP individuelle |
| ------------------------ | --------------------- |
| <ul><li>`94.236.119.0/26`</li><li>`103.237.104.0/22`</li><li>`130.248.172.0/24`</li><li>`130.248.173.0/24`</li><li>`130.248.244.88/29`</li><li>`185.28.196.0/22`</li><li>`192.28.144.0/20`</li><li>`192.28.160.0/19`</li><li>`199.15.212.0/22`</li></ul> | <ul><li>`13.237.155.207`</li><li>`13.55.192.247`</li><li>`18.200.201.81`</li><li>`34.247.24.245`</li><li>`35.165.244.220`</li><li>`44.235.171.179`</li><li>`52.20.211.99`</li><li>`52.64.109.86`</li><li>`54.160.246.246`</li><li>`54.212.167.17`</li><li>`54.220.138.65`</li><li>`54.237.141.197`</li><li>`130.248.168.16`</li><li>`130.248.168.17`</li></ul> |
