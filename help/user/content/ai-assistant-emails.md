---
title: Assistant IA pour la création d’emails
description: Découvrez comment utiliser l’assistant d’IA pour optimiser le contenu d’email utilisé dans les Parcours de compte.
feature: AI Assistant, Email Authoring, Content
exl-id: b66d72e4-3afc-49ad-9bc2-bedc047ecca4
source-git-commit: 78d82aa8b3bb8b8d432eeb187d75e2354dbff3ee
workflow-type: tm+mt
source-wordcount: '3072'
ht-degree: 0%

---

# Assistant IA pour la création d’emails

Le secteur du marketing devenant plus compétitif, les marques cherchent des moyens efficaces de générer rapidement et efficacement du contenu ayant un impact. L’assistant d’IA pour la création d’emails dans Adobe Journey Optimizer B2B Edition est la fonctionnalité de génération de contenu optimisée par l’IA de l’Adobe qui révolutionne la manière dont les marketeurs créent des contenus d’email professionnels et cohérents par leur marque. Grâce aux modèles avancés de GenAI et à une compréhension approfondie des directives de la marque, l’assistant d’IA génère automatiquement du contenu personnalisé, attrayant et efficace en fonction de l’objectif marketing, avec un contenu optimisé pour les styles, les mises en page, le ton et bien plus encore. L’assistant d’IA rend la création et l’exécution de campagnes de marketing par e-mail intuitives, simples et faciles à réaliser. L’ajout de cette fonctionnalité à vos workflows peut vous faire gagner du temps, améliorer votre efficacité et générer de meilleurs résultats.

Cette nouvelle fonctionnalité offre une génération rapide de texte, une génération complète d’emails et une génération de contenu dans les structures d’email. Les images ne sont pas générées, mais sont recommandées à partir du catalogue des images de la ressource de marque d’entrée vers le modèle. Vous pouvez également utiliser cette fonctionnalité pour générer des objets et des en-têtes optimaux qui impactent le taux d’ouverture.

>[!NOTE]
>
>Cette fonctionnalité est disponible dans sa version Beta et peut être modifiée sans préavis.

## Instructions et limites

Avant de commencer à utiliser l’assistant d’IA dans l’édition B2B de Adobe Journey Optimizer pour la génération de contenu d’email, consultez les instructions suivantes :

* L’objectif/l’invite marketing que vous définissez est un déterminant clé de la qualité du contenu généré. Utilisez une invite correctement définie pour que le modèle GenAI interprète correctement.
* Chargez des ressources de marque pour les rendre précises sur le contenu de la marque. Sans ces ressources, le contenu est basé sur des informations disponibles publiquement.
   * Les ressources chargées peuvent se présenter sous les formats suivants : fichiers PDF, JPEG, PNG ou ZIP (contenant les formats de fichiers pris en charge).
   * La taille maximale d’une ressource de marque chargée est de 50 Mo. Des fichiers plus volumineux ou de grandes quantités d’images peuvent fonctionner, mais le temps de traitement est augmenté.
* Utilisez les modèles d’email créés par Adobe Journey Optimizer B2B Edition, de préférence les modèles intégrés ou d’exemple, un modèle spécifique à la marque ou un modèle personnalisé pour créer le contenu de votre email. Il est recommandé d’utiliser des modèles d’email pouvant contenir jusqu’à huit à dix images.
* Veillez à signaler toute sortie problématique à l’aide des icônes de défilement ou d’indicateur par rapport à une variante générée.
* Votre utilisation de l’assistant d’IA est soumise aux [ instructions d’utilisation de l’API générique d’Adobe](https://www.adobe.com/fr/legal/licenses-terms/adobe-gen-ai-user-guidelines.html).

Les restrictions suivantes s’appliquent à l’assistant d’IA dans Adobe Journey Optimizer B2B Edition pour la génération de contenu d’email :

* L’anglais est la seule langue prise en charge.
* Il est uniquement disponible pour le canal email.
* Le contenu de GenAI peut ne pas être précis : partagez vos commentaires afin que les ingénieurs d’Adobe puissent affiner les modèles.
* Vous pouvez charger plusieurs ressources de marque, mais vous ne pouvez en exploiter qu’une seule pour une génération spécifique.

>[!BEGINSHADEBOX]

## Invite Library

Une invite efficace est essentielle pour générer le meilleur contenu possible. Si vous avez besoin d’aide pour concevoir votre invite, accédez à la _bibliothèque d’invites_. Cette bibliothèque offre un large éventail d’idées pour améliorer la génération de contenu.

![Assistant d’IA - Accès à la bibliothèque d’appels](./assets/email-designer-ai-assistant-prompt-library.png){width="500" zoomable="no"}

Sélectionnez l’invite qui correspond le mieux à vos objectifs et ajoutez les valeurs nécessaires pour spécifier votre marque, votre offre, votre campagne et vos cas d’utilisation.

>[!ENDSHADEBOX]

## Rôles des groupes d’achat

Adobe Journey Optimizer Édition B2B offre cinq rôles de groupe d’achat B2B standard prêts à l’emploi. Chaque rôle de groupe d’achat a une cible de messagerie distincte :

| Rôle | Ciblage de la messagerie |
| ---- | --------------- |
| Comité directeur exécutif | Informations sur le produit <br/>Tarification <br/>Informations sur l&#39;intégration technique <br/>Fonctionnalités et fonctions du produit |
| Personne influente | Bon à tirer <br/>Facilité de mise en oeuvre <br/>expertise en matière <br/>Avantages compétitifs |
| Décideur | Retour sur investissement <br/>Valeur financière (RoI) <br/>Histoires client |
| Praticien | Facilité d&#39;utilisation <br/>Fonctionnalités et fonctionnalités du produit <br/>Compatibilité des produits <br/>Facilité d&#39;intégration des produits |
| Champion | Contenu pédagogique <br/>Contenu du leadership pensé <br/> Articles client |

Le choix de l’un de ces rôles de groupe d’achat personnalise automatiquement la sortie en fonction des caractéristiques et des sujets d’intérêt pour chacun de ces rôles.

## Génération des propriétés des emails à l’aide de l’assistant d’IA

Lorsque vous [ajoutez une action de courrier électronique](./email-authoring.md#add-an-email-action-in-an-account-journey) à un parcours de compte, vous définissez un ensemble de propriétés de courrier électronique utilisées pour envoyer le courrier électronique. L’assistant d’IA peut vous aider à obtenir un meilleur engagement des courriers électroniques en générant le contenu recommandé pour l’ **objet** et l’ **pré-titre** de l’email.

1. Créez un email à partir d’un parcours de compte ou ouvrez un email existant à partir d’un noeud de parcours.

   La page d’aperçu de l’email s’affiche avec les _[!UICONTROL propriétés de l’email]_ à droite.

1. Sélectionnez l’un des onglets suivants pour savoir comment utiliser l’assistant d’IA dans la création de propriétés d’un email.

>[!BEGINTABS]

>[!TAB Génération de lignes d’objet]

Les étapes suivantes décrivent l’ordre des tâches permettant d’utiliser l’assistant d’IA pour générer un objet optimisé pour votre email :

1. Dans les _[!UICONTROL Propriétés de l’email]_, cliquez sur l’icône de l’assistant d’IA ( ![Icône d’accès de l’assistant d’IA](./assets/email-properties-ai-assistant-button.png){width="30" zoomable="no"} ) à droite du champ **[!UICONTROL Objet]**.

   ![Accès à l’assistant d’IA pour l’objet du courrier électronique](./assets/email-properties-ai-assistant-subject-line-icon.png){width="600" zoomable="yes"}

   La fenêtre contextuelle Assistant d’IA s’ouvre avec les paramètres de génération de l’objet du courrier électronique.

   Selon le contenu d’email associé à l’email ou la manière dont vous souhaitez utiliser l’objet pour répondre à vos besoins, il existe plusieurs options pour générer le texte de l’objet :

   * Vous pouvez cliquer immédiatement sur **[!UICONTROL Générer]** sans invite ni ressource de marque pour utiliser le corps de l’email existant comme contexte de génération de ligne d’objet.

   * (Recommandé) Vous pouvez fournir une invite, une ressource de marque et d’autres valeurs de paramètre afin de fournir un contexte pour générer le texte d’objet optimal en fonction de vos besoins. (étapes 2 à 7)

1. Dans le champ **[!UICONTROL Invite]**, saisissez une description de ce que vous souhaitez générer.

   Utilisez la [&#128279;](#prompt-library) si vous avez besoin d’aide pour créer une invite efficace.

1. Spécifiez une ressource de marque contenant du contenu qui servira de source pour la génération de texte.

   * Sélectionnez la ressource dans le catalogue.

   * Cliquez sur **[!UICONTROL Télécharger la ressource de marque]** pour ajouter le fichier de ressource de marque.

   ![Assistant d’IA - ligne d’objet](./assets/email-properties-ai-assistant-subject-line.png){width="600" zoomable="yes"}

1. Faites défiler l’écran si nécessaire et sélectionnez le **[!UICONTROL rôle de groupe d’achat]** à utiliser comme audience cible pour le texte généré.

1. Si nécessaire, utilisez les options de messagerie pour personnaliser votre contenu :

   * **[!UICONTROL Stratégie de communication]** - Choisissez le style de communication le plus adapté à votre texte généré.
   * **[!UICONTROL Langue]** - Sélectionnez la langue dans laquelle vous souhaitez générer votre contenu.
   * **[!UICONTROL Tone]** - Choisissez une tonalité qui convient à votre audience. Si vous indiquez que vous souhaitez émettre des sons informatifs, ludique ou persuasifs, l’assistant d’IA peut adapter le message en conséquence.

1. Si nécessaire, utilisez le curseur pour définir la longueur de texte à générer.

1. Modifiez l’option **[!UICONTROL Utiliser des émoticônes]** (activée ou désactivée) selon vos préférences.

1. Lorsque l’invite et les paramètres sont prêts, cliquez sur **[!UICONTROL Générer]**.

1. Faites défiler le panneau de l’assistant d’IA et parcourez les variations générées pour déterminer celle qui convient le mieux.

   * Cliquez sur **[!UICONTROL Aperçu]** pour afficher une version plein écran d’une variation sélectionnée.

   * Fournissez un commentaire pour les variantes générées en cliquant sur l’icône _Thumbs Up_, _Thumbs Down_ ou _Flag_ et sélectionnez la raison qui résume le mieux vos commentaires.

1. Accédez aux options _Affiner_ dans la fenêtre Aperçu pour accéder à des fonctionnalités de personnalisation supplémentaires :

   * **[!UICONTROL Utiliser comme contenu de référence]** - Sélectionnez cette option pour utiliser la variante comme contenu de référence pour générer d’autres résultats.

   * **[!UICONTROL Actualiser]** - L’assistant d’IA peut reformuler votre message de différentes manières, en préservant l’actualité et l’engagement de votre public.

   * **[!UICONTROL Utiliser un langage plus simple]** - Utilisez l’assistant d’IA pour simplifier votre langue, en assurant clarté et accessibilité pour une audience plus large.

   ![Assistant d’IA - affinage de la ligne d’objet](./assets/email-properties-ai-assistant-subject-line-refine.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Sélectionner]** pour remplacer le texte de l’objet par la variante sélectionnée et revenir aux propriétés de l’email.

>[!TAB Génération du pré-en]

Un pré-titre de courrier électronique est le texte de résumé court qui suit l’objet d’un message lorsqu’un message électronique est affiché dans la boîte de réception. Il s’agit d’un élément facultatif pour un email, mais d’une excellente opportunité d’améliorer l’engagement. Les étapes suivantes décrivent l’ordre des tâches pour l’utilisation de l’assistant d’IA afin de générer un pré-titre optimisé pour votre email :

1. Dans les Propriétés de l’email, cochez la case **[!UICONTROL Prétitre]** et cliquez sur l’icône de l’assistant d’IA ( ![Icône d’accès de l’assistant d’IA](./assets/email-properties-ai-assistant-button.png){width="30" zoomable="no"} ) à droite.

   ![Accès à l’assistant AI pour le pré-titre de courrier électronique](./assets/email-properties-ai-assistant-preheader-icon.png){width="600" zoomable="yes"}

   La fenêtre contextuelle de l’assistant d’IA s’ouvre avec les paramètres de génération du pré-titre de l’email.

   Selon le contenu d’email associé à l’email ou la manière dont vous souhaitez cibler l’email, il existe deux options pour générer le pré-titre :

   * Vous pouvez cliquer immédiatement sur **[!UICONTROL Générer]** sans invite ni ressource de marque pour utiliser le corps de l’email existant comme contexte de génération de pré-en-tête.

   * (Recommandé) Vous pouvez fournir une invite, une ressource de marque et d’autres valeurs de paramètre afin de fournir un contexte pour générer le pré-titre le plus optimal pour vos besoins. (étapes 2 à 7)

1. Dans le champ **[!UICONTROL Invite]**, saisissez une description de ce que vous souhaitez générer.

   Utilisez la [&#128279;](#prompt-library) si vous avez besoin d’aide pour créer une invite efficace.

1. Spécifiez une ressource de marque contenant du contenu qui servira de source pour la génération de texte.

   * Sélectionnez la ressource dans le catalogue.

   * Cliquez sur **[!UICONTROL Télécharger la ressource de marque]** pour ajouter le fichier de ressource de marque.

   ![Assistant IA - pré-titre](./assets/email-properties-ai-assistant-preheader.png){width="600" zoomable="yes"}

1. Faites défiler l’écran si nécessaire et sélectionnez le **[!UICONTROL rôle de groupe d’achat]** à utiliser comme audience cible pour le texte généré.

1. Si nécessaire, utilisez les options de messagerie pour personnaliser votre contenu :

   * **[!UICONTROL Stratégie de communication]** - Choisissez le style de communication le plus adapté à votre texte généré.
   * **[!UICONTROL Langue]** - Sélectionnez la langue dans laquelle vous souhaitez générer votre contenu.
   * **[!UICONTROL Tone]** - Choisissez une tonalité qui convient à votre audience. Si vous indiquez que vous souhaitez émettre des sons informatifs, ludique ou persuasifs, l’assistant d’IA peut adapter le message en conséquence.

1. Si nécessaire, utilisez le curseur pour définir la longueur de texte à générer.

1. Modifiez l’option **[!UICONTROL Utiliser des émoticônes]** (activée ou désactivée) selon vos préférences.

1. Lorsque l’invite et les paramètres sont prêts, cliquez sur **[!UICONTROL Générer]**.

1. Faites défiler le panneau de l’assistant d’IA et parcourez les variations générées pour déterminer celle qui convient le mieux.

   * Cliquez sur **[!UICONTROL Aperçu]** pour afficher une version plein écran d’une variation sélectionnée.

   * Fournissez un commentaire pour les variantes générées en cliquant sur l’icône _Thumbs Up_, _Thumbs Down_ ou _Flag_ et sélectionnez la raison qui résume le mieux vos commentaires.

1. Accédez aux options _Affiner_ dans la fenêtre Aperçu pour accéder à des fonctionnalités de personnalisation supplémentaires :

   * **[!UICONTROL Utiliser comme contenu de référence]** - Sélectionnez cette option pour utiliser la variante comme contenu de référence pour générer d’autres résultats.

   * **[!UICONTROL Actualiser]** - L’assistant d’IA peut reformuler votre message de différentes manières, en préservant l’actualité et l’engagement de votre public.

   * **[!UICONTROL Utiliser un langage plus simple]** - Utilisez l’assistant d’IA pour simplifier votre langue, en assurant clarté et accessibilité pour une audience plus large.

   ![Assistant d’IA - amélioration du pré-titre](./assets/email-properties-ai-assistant-preheader-refine.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Sélectionner]** pour remplacer le pré-titre par la variante sélectionnée et revenir aux propriétés de l&#39;email.

>[!ENDTABS]

## Génération de contenu du corps de courrier électronique à l’aide de l’assistant AI

Après avoir [créé et personnalisé votre email](./email-authoring.md#create-the-email-content), utilisez l’assistant d’IA dans l’édition B2B de Adobe Journey Optimizer, optimisée par l’IA générative, pour élever le contenu de votre corps d’email au niveau suivant.

Dans le Concepteur d’email, l’assistant d’IA peut vous aider à optimiser l’impact de vos diffusions en générant le corps complet de l’email, le contenu textuel ciblé et les recommandations d’images qui résonnent auprès de votre audience. Cette optimisation de vos campagnes par e-mail est conçue pour générer un meilleur engagement.

1. Créez un email à partir d’un parcours de compte et cliquez sur **[!UICONTROL Ouvrir le Designer de messagerie]** ou **[!UICONTROL Ajouter du contenu de messagerie]**.

1. Sélectionnez et ouvrez un modèle d’email dans le concepteur visuel d’email.

1. Personnalisez l&#39;email selon vos besoins pour le noeud de parcours.

1. Sélectionnez l’un des onglets suivants pour savoir comment utiliser l’assistant d’IA dans la création de contenu du corps de votre email.

>[!BEGINTABS]

>[!TAB Génération d’e-mail complet]

Les étapes suivantes décrivent l’ordre des tâches pour l’utilisation de l’assistant AI afin d’affiner un modèle de courrier électronique existant :

1. Dans le concepteur d’email, accédez au menu de l’assistant d’IA en cliquant sur l’icône ( ![bascule du menu Assistant d’IA](../assets/button-ai-assistant.png){width="30" zoomable="no"} ) à droite.

   ![Bascule de l’assistant d’IA dans le concepteur d’email](./assets/email-designer-ai-assistant-button.png){width="600" zoomable="yes"}

   Les paramètres de l’assistant d’IA à droite reflètent les _paramètres de génération (adresse électronique complète)_.

1. Dans le champ **[!UICONTROL Invite]**, saisissez une description de ce que vous souhaitez générer.

   Utilisez la [&#128279;](#prompt-library) si vous avez besoin d’aide pour créer une invite efficace.

   ![Assistant d’IA - paramètres de texte](./assets/email-designer-ai-assistant-full.png){width="600" zoomable="yes"}

1. Spécifiez une ressource de marque qui contient du contenu pouvant fournir un contexte supplémentaire pour l’assistant d’IA.

   * Sélectionnez la ressource dans le catalogue.

   * Cliquez sur **[!UICONTROL Télécharger la ressource de marque]** pour ajouter le fichier de ressource de marque.

   Cette ressource d’entrée sert de source pour la génération de contenu et la recommandation d’image dans le courrier électronique.

1. Sélectionnez le **[!UICONTROL rôle de groupe d’achats]** à utiliser comme audience cible pour la communication par e-mail.

1. Si nécessaire, utilisez les options de messagerie pour personnaliser votre contenu :

   * **[!UICONTROL Stratégie de communication]** - Choisissez le style de communication le plus adapté à votre texte généré.
   * **[!UICONTROL Langue]** - Sélectionnez la langue dans laquelle vous souhaitez générer votre contenu.
   * **[!UICONTROL Tone]** - Choisissez une tonalité qui convient à votre audience. Si vous indiquez que vous souhaitez émettre des sons informatifs, ludique ou persuasifs, l’assistant d’IA peut adapter le message en conséquence.
   * **Type de contenu** - Choisissez une option qui reflète la nature des éléments visuels. Ce paramètre fait la distinction entre différentes formes de représentation visuelle telles que les photos, les graphiques ou les illustrations.

1. Lorsque votre invite est prête, cliquez sur **[!UICONTROL Générer]**.

1. Faites défiler le panneau de l’assistant d’IA et parcourez les variations générées pour déterminer celle qui convient le mieux.

   * Cliquez sur **[!UICONTROL Aperçu]** pour afficher une version plein écran d’une variation sélectionnée.

   * Fournissez un commentaire pour les variantes générées en cliquant sur l’icône _Thumbs Up_, _Thumbs Down_ ou _Flag_ et sélectionnez la raison qui résume le mieux vos commentaires.

     ![Assistant d’IA - paramètres de texte](./assets/email-designer-ai-assistant-feedback.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Sélectionner]** pour remplacer le contenu du modèle par la variante sélectionnée et revenir au concepteur d&#39;email.

   Dans le concepteur d&#39;email, vous pouvez utiliser les outils d&#39;édition et de formatage de la zone de travail pour modifier le contenu, ainsi que les options _[!UICONTROL Paramètres]_ et _[!UICONTROL Style]_ sur la droite.

>[!TAB Génération de texte]

Les étapes suivantes décrivent l’ordre des tâches pour l’utilisation de l’assistant AI afin d’affiner ou d’améliorer le contenu texte d’un email existant :

1. Dans le concepteur d’email, accédez au menu de l’assistant d’IA en cliquant sur l’icône ( ![bascule du menu Assistant d’IA](../assets/button-ai-assistant.png){width="30" zoomable="no"} ) à droite.

   ![Bascule de l’assistant d’IA dans le concepteur d’email](./assets/email-designer-ai-assistant-button.png){width="600" zoomable="yes"}

1. Sélectionnez un composant _Texte_ pour cibler le contenu spécifique.

   Les paramètres de l’assistant d’IA à droite reflètent les _paramètres de génération (texte)_.

1. Dans le champ **[!UICONTROL Invite]**, saisissez une description de ce que vous souhaitez générer.

   ![Assistant d’IA - paramètres de texte](./assets/email-designer-ai-assistant-text.png){width="600" zoomable="yes"}

   Utilisez la [&#128279;](#prompt-library) si vous avez besoin d’aide pour créer une invite efficace.

1. Spécifiez une ressource de marque contenant du contenu qui servira de source pour la génération de texte.

   * Sélectionnez la ressource dans le catalogue.

   * Cliquez sur **[!UICONTROL Télécharger la ressource de marque]** pour ajouter le fichier de ressource de marque.

1. Sélectionnez le **[!UICONTROL rôle de groupe d’achat]** à utiliser comme audience cible pour le texte généré.

1. Si nécessaire, utilisez la langue et les options de messagerie pour personnaliser votre contenu :

   * **[!UICONTROL Stratégie de communication]** - Choisissez le style de communication le plus adapté à votre texte généré.
   * **[!UICONTROL Langue]** - Sélectionnez la langue dans laquelle vous souhaitez générer votre contenu.
   * **[!UICONTROL Tone]** - Choisissez une tonalité qui convient à votre audience. Si vous indiquez que vous souhaitez émettre des sons informatifs, ludique ou persuasifs, l’assistant d’IA peut adapter le message en conséquence.

1. Si nécessaire, utilisez le curseur pour définir la longueur de texte à générer.

1. Lorsque votre invite est prête, cliquez sur **[!UICONTROL Générer]**.

1. Parcourez les _variations_ générées et cliquez sur **[!UICONTROL Aperçu]** pour afficher une version plein écran de la variation sélectionnée.

1. Accédez aux options _Affiner_ dans la fenêtre Aperçu pour accéder à des fonctionnalités de personnalisation supplémentaires :

   * **[!UICONTROL Utiliser comme contenu de référence]** - Sélectionnez cette option pour utiliser la variante comme contenu de référence pour générer d’autres résultats.

   * **[!UICONTROL Elaborate]** - L’assistant d’IA peut vous aider à développer des sujets spécifiques, en fournissant des détails supplémentaires pour une meilleure compréhension et un meilleur engagement.

   * **[!UICONTROL Résumer]** - De longues informations peuvent surcharger les destinataires des emails. Utilisez l’assistant d’IA pour condenser des points clés en résumés clairs et concis qui attirent l’attention et les encourager à lire plus.

   * **[!UICONTROL Actualiser]** - L’assistant d’IA peut reformuler votre message de différentes manières, en préservant l’actualité et l’engagement de votre public.

   * **[!UICONTROL Utiliser un langage plus simple]** - Utilisez l’assistant d’IA pour simplifier votre langue, en assurant clarté et accessibilité pour une audience plus large.

   ![Aperçu de l’assistant d’IA des options de variation et d’amélioration de texte](./assets/email-designer-ai-assistant-text-refine.png){width="700" zoomable="yes"}

1. Lorsque vous avez le contenu que vous souhaitez, cliquez sur **[!UICONTROL Sélectionner]** pour remplacer le texte par la variante sélectionnée et revenir au concepteur d&#39;email.

   Dans le concepteur d&#39;email, vous pouvez utiliser les outils d&#39;édition et de formatage de la zone de travail pour modifier le texte, ainsi que les options _[!UICONTROL Paramètres]_ et _[!UICONTROL Style]_ sur la droite.

>[!TAB Recommandations d’images]

Vous pouvez utiliser l’assistant d’IA pour optimiser et améliorer vos ressources et garantir une expérience plus conviviale. Les étapes suivantes décrivent l’ordre des tâches pour l’utilisation de l’assistant d’IA afin d’améliorer le contenu de l’image de l’email :

1. Accédez au menu de l’assistant d’IA en cliquant sur l’icône ( ![bascule du menu Assistant d’IA](../assets/button-ai-assistant.png){width="30" zoomable="no"} ) à droite.

   ![Bascule de l’assistant d’IA dans le concepteur d’email](./assets/email-designer-ai-assistant-button.png){width="600" zoomable="yes"}

1. Sélectionnez un composant _Image_ pour cibler le contenu spécifique et accéder au menu de l’assistant d’IA.

   Les paramètres sur la droite reflètent les _[!UICONTROL Paramètres de génération (image)]_.

1. Pour affiner la ressource, saisissez une description de ce que vous souhaitez dans le champ **[!UICONTROL Invite]**.

   ![Assistant d’IA - paramètres de texte](./assets/email-designer-ai-assistant-image.png){width="600" zoomable="yes"}

   Utilisez la [&#128279;](#prompt-library) si vous avez besoin d’aide pour créer une invite efficace.

1. Cliquez sur **[!UICONTROL Télécharger la ressource de marque]** pour ajouter toute ressource de marque contenant du contenu pouvant fournir un contexte supplémentaire pour l’assistant d’IA.

   Si la ressource nécessaire est déjà disponible, développez **[!UICONTROL Ressources de marque chargées]** et sélectionnez la ressource.

   Votre invite doit toujours être liée à une ressource existante.

1. Utilisez les paramètres d’image pour affiner votre invite :

   * **[!UICONTROL Format]** - Ce paramètre détermine la largeur et la hauteur de la ressource. Vous avez la possibilité de choisir parmi des rapports communs tels que 16:9, 4:3, 3:2 ou 1:1, ou vous pouvez saisir une taille personnalisée.
   * **[!UICONTROL Couleur et ton]** - Ce paramètre influence l’aspect général des couleurs dans une image ainsi que l’humeur ou l’atmosphère qu’elle véhicule.
   * **[!UICONTROL Type de contenu]** - Ce paramètre classe la nature de l’élément visuel en faisant la distinction entre les différentes formes de représentation visuelle, telles que les photos, les graphiques ou les illustrations.
   * **[!UICONTROL Éclairage]** - Ce paramètre ajuste l’éclair présent dans une image, ce qui modifie son atmosphère et met en évidence des éléments spécifiques.
   * **[!UICONTROL Composition]** - Ce paramètre détermine la disposition des éléments dans le cadre d’une image.

1. Lorsque vous êtes satisfait de votre configuration rapide, cliquez sur **[!UICONTROL Générer]**.

   L’assistant d’IA traite la demande et recommande les images les mieux adaptées à partir de la ressource de marque d’entrée et en fonction de l’invite et des autres entrées.

   >[!IMPORTANT]
   >
   >S’il n’y a pas d’images dans la ressource de marque d’entrée ou si aucune image n’est pertinente pour l’invite d’entrée, la sortie est vide.

1. Parcourez les _[!UICONTROL Variations]_ et sélectionnez celle qui convient le mieux à l’email.

   Pour afficher une version plein écran de la variation sélectionnée, cliquez sur **[!UICONTROL Aperçu]**.

1. Mettez en surbrillance l’image de votre choix et cliquez sur **[!UICONTROL Sélectionner]** pour remplacer l’image ou l’espace réservé par l’élément sélectionné et revenir au concepteur d’email.

   Dans le concepteur d&#39;email, vous pouvez utiliser les outils d&#39;édition et de formatage de la zone de travail pour modifier le contenu, ainsi que les options _[!UICONTROL Paramètres]_ et _[!UICONTROL Style]_ sur la droite.

>[!ENDTABS]
