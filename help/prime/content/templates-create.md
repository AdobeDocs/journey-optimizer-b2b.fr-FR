---
title: Créer des modèles d’e-mail
description: 'Découvrez comment créer des modèles d’e-mail dans Journey Optimizer B2B Prime : concevoir entièrement, enregistrer un e-mail à partir d’un parcours en tant que modèle ou convertir une image de conception en modèle d’e-mail.'
badgeBeta: label="Beta" type="informative" tooltip="Cette fonctionnalité fait partie d’une version bêta limitée."
source-git-commit: 2f19137465c71f2292d37bea5786533b1df6e286
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 1%

---


# Créer des modèles d’e-mail

Vous pouvez créer un modèle d’e-mail dans [!DNL Journey Optimizer B2B Edition Prime] de trois façons :

* **Créer en partant de zéro** — Créez un nouveau modèle dans la bibliothèque de modèles à l&#39;aide de l&#39;espace visuel de conception d&#39;e-mail.
* **Enregistrer à partir d’un e-mail de parcours** — Enregistrez un e-mail que vous avez créé dans un parcours en tant que modèle réutilisable.
* **Convertir une image** — Chargez une image de conception et utilisez l’IA générative pour la convertir en modèle d’e-mail modifiable.

>[!NOTE]
>
>Dans cette version de Beta, seuls les modèles d’e-mail sont pris en charge.

## Concevoir un modèle à partir de zéro {#design-from-scratch}

1. Accédez à **[!UICONTROL Gestion de contenu]** > **[!UICONTROL Modèles]**.
1. Cliquez sur **[!UICONTROL Créer un modèle]**.
1. Saisissez un **[!UICONTROL Nom du modèle]** et un **[!UICONTROL Description]** facultatif.
1. Vous pouvez éventuellement ajouter des balises pour catégoriser le modèle.
1. Cliquez sur **[!UICONTROL Créer]** pour ouvrir l’espace de conception d’e-mail.
1. Concevoir la disposition des e-mails à l’aide de structures et de composants de contenu. Pour une référence complète des outils disponibles, voir [Création d’e-mails](email-authoring.md).
1. Vous pouvez éventuellement configurer le [verrouillage de contenu](template-content-locking.md) pour limiter les parties du modèle que les auteurs peuvent modifier lors de son utilisation dans un parcours.
1. Cliquez sur **[!UICONTROL Enregistrer]**

## Enregistrer un e-mail de parcours en tant que modèle {#save-as-template}

Lorsque vous concevez un e-mail dans un parcours que vous souhaitez réutiliser, enregistrez-le directement dans la bibliothèque de modèles à partir de l’espace de conception d’e-mail.

1. Dans l’espace de conception d’e-mail, ouvrez la liste déroulante **[!UICONTROL Enregistrer]** située en haut de l’éditeur.
1. Sélectionnez **[!UICONTROL Enregistrer comme modèle de contenu]**.
1. Saisissez un **[!UICONTROL Nom du modèle]** et un **[!UICONTROL Description]** facultatif.
1. Vous pouvez éventuellement ajouter des balises et configurer le [verrouillage de contenu](template-content-locking.md).
1. Cliquez sur **[!UICONTROL Enregistrer]**

L’e-mail de parcours d’origine n’est pas affecté. Le modèle enregistré est disponible dans la bibliothèque de modèles pour tous les utilisateurs dans le sandbox.

## Convertir une image en modèle {#image-to-template}

[!DNL Journey Optimizer B2B Edition Prime] pouvez convertir une image statique, telle qu’une maquette de Figma ou de Photoshop, en modèle d’e-mail modifiable à l’aide de l’IA générative. Il n’est donc plus nécessaire de reconstruire manuellement les mises en page à partir des fichiers de conception.

### Exigences

Avant de commencer :

* Votre entreprise doit avoir signé l’addendum Generative AI avec Adobe.
* Vous devez disposer de l’autorisation **[!UICONTROL Générer du contenu]** en plus de l’autorisation **[!UICONTROL Gérer les modèles de contenu]**.
* Le fichier image doit répondre aux spécifications suivantes :
   * Format : JPEG (.jpg, .jpeg) ou PNG (.png)
   * Taille de fichier maximale : 10 Mo
   * Largeur recommandée : 600 à 800 pixels
   * Image claire et de haute qualité avec texte lisible et éléments visuels distincts

>[!IMPORTANT]
>
>L’image ne doit pas contenir d’informations d’identification personnelle (PII) ni de données sensibles.

### Convertir une image

1. Accédez à **[!UICONTROL Gestion de contenu]** > **[!UICONTROL Modèles]**.
1. Cliquez sur **[!UICONTROL Convertir l’image en modèle]** dans l’en-tête.
1. Saisissez un **[!UICONTROL Nom du modèle]** et un **[!UICONTROL Description]** facultatif.
1. Sélectionnez éventuellement un **[!UICONTROL thème de marque]** pour appliquer les couleurs, les polices et l’espacement de votre marque à la sortie générée.
1. Chargez l’image par glisser-déposer ou à l’aide de l’explorateur de fichiers.
1. Vérifiez que l’image ne contient aucune donnée personnelle.
1. Consultez et acceptez les Directives d’utilisation d’Adobe Generative AI (pour la première fois uniquement).
1. Cliquez sur **[!UICONTROL Convertir]**.

   La conversion se termine généralement dans les cinq minutes. Les images complexes ou volumineuses peuvent prendre jusqu’à dix minutes. Vous pouvez quitter la page : le processus se poursuit en arrière-plan.

1. Une fois la conversion terminée, cliquez sur le nom du modèle pour prévisualiser et modifier le contenu généré.

>[!NOTE]
>
>Le résultat ne s’affiche pas automatiquement. Actualisez la page ou revenez à la bibliothèque de modèles pour afficher le modèle terminé.

### Modifier après la conversion

Le modèle converti s’ouvre dans l’espace de conception des e-mails en tant qu’e-mail entièrement modifiable. Utilisez les outils de conception standard pour :

* Modifiez le texte et ajoutez des jetons [personnalisation](email-authoring.md#personalization).
* Mettez à jour ou remplacez des images et ajoutez des liens.
* Ajustez les couleurs, les polices et l’espacement.
* Ajouter, supprimer ou réorganiser des composants de contenu.
* Configurez [verrouillage de contenu](template-content-locking.md).

>[!IMPORTANT]
>
>L’IA générative produit une HTML statique basée sur l’image visuelle. Vérifiez tout le texte pour en assurer la précision et ajoutez manuellement la personnalisation, le contenu dynamique et le suivi après la conversion.

Le modèle converti est automatiquement enregistré dans la bibliothèque de modèles une fois la conversion terminée.

### Conseils pour obtenir de meilleurs résultats

Suivez les instructions suivantes pour obtenir les meilleurs résultats de la conversion d’une image en modèle :

**Avant la conversion :**

* Utilisez la version la plus haute résolution de votre fichier de conception.
* Concevez avec des largeurs d’e-mail standard (600 à 800 pixels) et incluez la disposition complète (de l’en-tête au pied de page) dans une seule image.
* Assurez-vous que le contraste entre le texte et l’arrière-plan est suffisant et utilisez des tailles de police lisibles.

**Concevoir pour une conversion précise :**

* Utilisez des dispositions simples et bien structurées, avec une séparation nette entre les sections.
* Suivez les modèles d’e-mail standard (en-tête, corps, appels à l’action, pied de page) plutôt que des conceptions à plusieurs couches complexes.
* Gardez les éléments visuels distincts afin que l’IA puisse identifier correctement les limites structurelles.

**Après la conversion :**

* Testez le rendu sur les clients de messagerie et les appareils avant d’utiliser le modèle dans un parcours.
* Vérifiez l’alignement avec les couleurs, les polices et les directives de style de la marque.
* Examiner et améliorer l’accessibilité, y compris le texte secondaire de l’image.
