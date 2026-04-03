---
title: Création WhatsApp
description: Créez des messages WhatsApp pour les parcours de compte à l’aide de modèles Meta approuvés, de jetons de personnalisation et de paramètres de diffusion dans Journey Optimizer B2B edition.
feature: Content, Channels, Account Journeys
role: User
source-git-commit: a9077a4fb5c90166433204d7a0a124f4f2e5ab92
workflow-type: tm+mt
source-wordcount: '813'
ht-degree: 21%

---

# Création WhatsApp

Utilisez Adobe Journey Optimizer B2B edition pour envoyer des messages WhatsApp aux membres du compte sur leurs appareils mobiles. Vous pouvez créer, personnaliser et prévisualiser des messages en utilisant des modèles de messages Meta approuvés à partir de l&#39;éditeur WhatsApp. <!-- Test your WhatsApp messages before publishing the account journey to ensure your intended rendering, accurate personalization, and proper configuration of all settings. -->

Avant de créer des messages WhatsApp pour les parcours de compte, assurez-vous que le canal [WhatsApp](../admin/configure-channels-whatsapp.md) nécessaire est configuré dans les paramètres _[!UICONTROL Administrateur]_.

>[!NOTE]
>
>Seuls les éléments de message _sortant_ WhatsApp sont pris en charge dans Journey Optimizer B2B edition.

+++ Éléments de message pris en charge et options d’appels à l’action

Les types de messages pris en charge dans WhatsApp sont les suivants :

| Élément de message | Description |
| - | - |
| En-têtes | Texte facultatif qui apparaît au-dessus du corps de votre message. |
| Texte | Prend en charge le contenu dynamique par le biais de paramètres. |
| Images (JPEG, PNG) | Doivent être au format RGB ou RGBA 8 bits et d’une taille inférieure à 5 Mo. |
| Vidéos | Doit être 3GPP ou MP4, de moins de 16 Mo, et hébergé par URL. |
| Audio | Disponible uniquement pour les messages de réponse. Doit être au format AAC, AMR, MP3, MP4 audio ou OGG, hébergé via une URL et d’une taille inférieure à 16 Mo. |
| Documents | Doit être inférieur à 100 Mo, hébergé sur une URL et dans l’un des formats suivants : `.txt`, `.xls`/`.xlsx`, `.doc`/`.docx`, `.ppt`/`.pptx` ou `.pdf`. |
| Corps de texte | Prend en charge le contenu dynamique par le biais de paramètres. |
| Texte du pied de page | Prend en charge le contenu dynamique par le biais de paramètres. |

Les options call-to-action suivantes sont disponibles pour vos messages WhatsApp :

| Call to action | Description |
| - | - |
| Visiter le site web | Un seul bouton est autorisé, avec les paramètres de variable inclus. |
| Appeler sur WhatsApp | Fournit un bouton qui ouvre une conversation WhatsApp avec le numéro de téléphone spécifié directement à partir du message. |
| Appeler le numéro de téléphone | Fournit un bouton qui déclenche un appel téléphonique vers le numéro spécifié lorsque l’utilisateur ou l’utilisatrice appuie dessus. |

+++

## Ajouter une action WhatsApp dans un parcours de compte

Vous pouvez configurer des diffusions de messages WhatsApp dans un parcours de compte lorsque vous [ajoutez un nœud _[!UICONTROL Agir]_](../journeys/action-nodes.md) et que vous effectuez les opérations suivantes :

1. Pour la cible _[!UICONTROL Action sur]_, choisissez **[!UICONTROL Personnes]**.

1. Pour le _[!UICONTROL Action sur les personnes]_, choisissez **[!UICONTROL Envoyer WhatsApp]**.

   ![Agir - Envoyer WhatsApp](./assets/whatsapp-journey-node.png){width="500" zoomable="yes"}

## Créer le message WhatsApp

1. Au bas du panneau _[!UICONTROL Agir]_, cliquez sur **[!UICONTROL Créer WhatsApp]**.

1. Dans la boîte de dialogue, entrez un **[!UICONTROL Nom]** (obligatoire) et un **[!UICONTROL Description]** (facultatif) uniques pour le message WhatsApp.

   ![Boîte de dialogue Créer un message WhatsApp](./assets/whatsapp-create-dialog.png){width="400"}

1. Cliquez sur **[!UICONTROL Créer]**.

   L&#39;espace de conception _WhatsApp_ s&#39;ouvre où vous pouvez définir les actions WhatsApp et créer le contenu pour envoyer le message.

### Sélection de la configuration des actions

1. Dans l&#39;espace de conception _WhatsApp_, sélectionnez l&#39;onglet **[!UICONTROL Actions]**.

1. Pour **[!UICONTROL Configuration de WhatsApp]**, sélectionnez la [configuration](../admin/configure-channels-whatsapp.md#create-channel-configuration) qui prend en charge les actions marketing et les paramètres de diffusion des messages selon vos besoins.

   ![Créer WhatsApp - Onglet Actions](./assets/whatsapp-create-actions-tab.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Modifier le contenu]** pour passer aux paramètres et au texte du message.

### Sélectionner un modèle de message

>[!IMPORTANT]
>
>**Gestion du consentement de WhatsApp** : conformément aux politiques de Meta et aux réglementations applicables, tous les messages marketing de WhatsApp doivent être envoyés uniquement aux destinataires ayant accepté de recevoir des communications. Les destinataires de WhatsApp peuvent se désinscrire à tout moment en répondant avec un mot-clé de désinscription. Les réponses d’opt-out sont automatiquement honorées et les profils correspondants sont supprimés des audiences de messages marketing futures.

Les messages WhatsApp sont envoyés à l&#39;aide de modèles de messages préapprouvés depuis votre compte professionnel Meta WhatsApp. **Les modèles doivent être examinés et approuvés par Meta** avant de pouvoir les utiliser dans Journey Optimizer B2B edition. Demandez à l’administrateur de votre compte [!DNL Meta Business Manager] de gérer et d’envoyer des modèles à approuver.

1. Pour **[!UICONTROL Sélectionner une catégorie de modèles]**, choisissez l’une des options suivantes :

   * Marketing
   * Utilitaire
   * Authentification

1. Pour **[!UICONTROL Sélectionner le modèle WhatsApp]**, choisissez un modèle approuvé pour le compte professionnel de configuration.

   Le contenu du modèle se charge dans l’éditeur de messages, affichant la structure du modèle et les champs de variable disponibles pour la personnalisation.

   ![Modèle de message WhatsApp sélectionné avec le message chargé dans la fenêtre de prévisualisation](./assets/whatsapp-create-select-template.png){width="700" zoomable="yes"}

   Les modèles sont organisés par catégorie (_Marketing_, _Utilitaire_ et _Authentification_) et par statut. Seuls les modèles **_Approuvés_** peuvent être sélectionnés. Pour plus d&#39;informations sur la création de modèles WhatsApp, voir [_Création de modèles de messages pour votre compte d&#39;entreprise WhatsApp_](https://www.facebook.com/business/help/2055875911147364?id=2129163877102343) dans la documentation de Meta.

### URL des images

Si votre modèle comprend des images, utilisez le champ **[!UICONTROL URL de l’image]** pour ajouter des URL de média afin de remplacer tous les espaces réservés dans votre modèle. Les médias de modèles Meta ne sont que des espaces réservés. Pour afficher correctement des images, des données audio ou vidéo, vous devez utiliser des URL externes provenant d’Adobe Experience Manager ou d’autres sources.

### Personnaliser le contenu du message

Les modèles WhatsApp approuvés peuvent inclure des espaces réservés de variable que vous définissez à l’aide de données de profil ou de valeurs dynamiques.

Pour chaque champ de variable affiché dans le modèle, cliquez sur l’icône _Personnaliser_ ( ![Icône Personnaliser](../assets/do-not-localize/icon-personalize.svg) ) en regard du champ.

![Variables dans le modèle WhatsApp](./assets/whatsapp-create-variables.png){width="700" zoomable="yes"}

La boîte de dialogue permet d’accéder aux jetons de compte, de personne et de système. Des jetons standard et personnalisés sont inclus. Vous pouvez utiliser la barre _Rechercher_ pour localiser le jeton dont vous avez besoin ou parcourir l’arborescence de dossiers pour rechercher et sélectionner l’un des jetons.

Pour plus d’informations sur l’utilisation de jetons pour la personnalisation, voir [Personnalisation de contenu](./personalization.md).

Lorsque vos jetons de personnalisation sont définis, cliquez sur **[!UICONTROL Enregistrer]** pour enregistrer les modifications et revenir à l&#39;espace de travail principal des messages WhatsApp.
