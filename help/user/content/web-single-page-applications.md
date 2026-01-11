---
title: Applications Monopages
description: 'Créer des expériences web pour les applications monopages (SPA) : configurez le suivi des vues, gérez le contenu dynamique et la navigation côté client dans Journey Optimizer B2B edition.'
feature: Channels, Personalization
role: User
badgeBeta: label="Beta" type="informative" tooltip="Cette fonctionnalité est actuellement en version bêta limitée"
source-git-commit: e50b6830736bf763d3aae6a58595e868bbac36e0
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 1%

---

# Applications monopages

Les applications d’une seule page (SPA) présentent des défis uniques en termes de personnalisation web, car elles mettent à jour le contenu des pages de manière dynamique sans rechargement complet des pages. Journey Optimizer B2B edition fournit des outils spécialisés pour gérer efficacement la personnalisation des SPA.

## Présentation des SPA

Contrairement aux sites web multi-pages traditionnels où chaque navigation déclenche un chargement de page complet, les SPA utilisent JavaScript pour mettre à jour le contenu de manière dynamique tout en conservant une seule page HTML. Cette approche crée plusieurs considérations pour les expériences web :

* **Pas de rechargement de page** - Les modifications de contenu se produisent sans déclencher d’événements de chargement de page traditionnels.
* **Vues virtuelles** - Différentes _vues_ ou _écrans_ au sein de la SPA qui doivent être suivies en tant que pages distinctes.
* **Routage côté client** - Les routeurs JavaScript (tels que React Router, Vue Router et Angular Router) gèrent la navigation plutôt que les requêtes de serveur.
* **Dynamic DOM** - Les éléments de page peuvent être créés, modifiés ou supprimés après le chargement initial de la page.

## Configuration de la prise en charge SPA

Pour personnaliser efficacement les SPA, vous devez configurer le suivi des vues afin que Journey Optimizer B2B edition puisse identifier quand les utilisateurs naviguent entre les vues virtuelles.

### Configurer les déclarations de vue

Collaborez avec votre équipe de développement pour implémenter des déclarations d’affichage à l’aide du SDK Web Adobe. L’utilisation de ces déclarations d’affichage implique l’appel de la commande `sendEvent` avec des informations d’affichage chaque fois que la SPA accède à une nouvelle vue.

**Exemple d’implémentation :**

```javascript
// When a new view is rendered in your SPA
alloy("sendEvent", {
  "xdm": {
    "web": {
      "webPageDetails": {
        "viewName": "product-detail",
        "URL": window.location.href
      }
    }
  },
  "data": {
    "__adobe": {
      "target": {
        "viewName": "product-detail"
      }
    }
  }
});
```

### Afficher les conventions de nommage

Utilisez des noms de vue cohérents et descriptifs qui correspondent à la structure logique de votre application :

| Affichage | Exemple de nom |
| ---- | ------------ |
| Page d’accueil | `home` |
| Liste des produits | `product-list` |
| Détails du produit | `product-detail` |
| Panier | `cart` |
| Extraire | `checkout` |
| Tableau de bord du compte | `account-dashboard` |

>[!NOTE]
>
>Les noms des vues respectent la casse. Utilisez une convention de nommage cohérente (les minuscules avec des tirets sont recommandées) dans votre implémentation.

## Créer des expériences web pour les SPA

Lors de la création d’expériences web pour les SPA, tenez compte des bonnes pratiques suivantes :

### Vues spécifiques à Target

* Dans la [configuration du canal web](../admin/configure-channels-web.md), configurez les règles de correspondance d’URL qui s’alignent sur votre structure de routage SPA.

* Lors de la création de modifications, spécifiez la vue où la modification doit s&#39;appliquer.

* Utilisez des sélecteurs CSS qui ciblent les éléments spécifiques à chaque vue.

### Gestion du contenu dynamique

Les SPA chargent souvent le contenu de manière dynamique après le rendu initial de la page. Utilisez ces techniques pour vous assurer que les modifications s’appliquent correctement :

#### Attendre les éléments

Configurez les modifications pour attendre que les éléments cibles existent avant d’appliquer :

1. Dans l’éditeur non visuel, ajoutez une modification avec un sélecteur CSS.

1. Activez **[!UICONTROL Attendre l’élément]** et spécifiez la durée d’attente maximale.

1. La modification s’applique une fois que l’élément cible apparaît dans le DOM.

#### Utilisation d’observateurs de mutation

Pour un contenu hautement dynamique, le Web SDK inclut des observateurs de mutation intégrés qui détectent lorsque de nouveaux éléments sont ajoutés à la page. Ces observateurs s’assurent que les modifications sont appliquées même lorsque les éléments se chargent de manière asynchrone.

### Structures SPA

Les expériences web Journey Optimizer B2B edition fonctionnent avec les frameworks SPA populaires :

| Framework | Considérations |
| --------- | -------------- |
| **React** | Les modifications s’appliquent une fois que React a rendu les composants dans le DOM. Utilisez des noms de classe ou des attributs de données pour le ciblage. |
| **Angular** | Éléments cibles après l’exécution de la détection des modifications d’Angular. Évitez de cibler les éléments avec des `*ngIf` avant leur rendu. |
| **Vue.js** | Attendez la `nextTick` de Vue pour vous assurer que les éléments sont dans le DOM. Utilisez des références ou des attributs personnalisés pour un ciblage stable. |
| **Next.js / Nuxt.js** | Pour les pages SSR/SSG, assurez-vous que l’hydratation de Web SDK est terminée avant d’attendre des modifications. |

## Bonnes pratiques relatives à la personnalisation des SPA

### Utilisation de sélecteurs stables

Les SPA génèrent souvent des noms ou des identifiants de classe dynamiques (en particulier avec les solutions CSS-in-JS). Vous pouvez également utiliser les méthodes suivantes :

* **Attributs de données** - Ajoutez des attributs de données personnalisés (`data-testid`, `data-section`, etc.) aux éléments que vous souhaitez cibler.
* **Semantic HTML** - Cible basée sur la structure HTML et les éléments sémantiques.
* **Attributs d’ID** - Utilisez des attributs d’ID stables lorsque cela est possible.

**Exemple :**

```html
<!-- Instead of targeting dynamic class names -->
<button class="css-1a2b3c4d">Sign Up</button>

<!-- Add a stable data attribute -->
<button class="css-1a2b3c4d" data-action="signup">Sign Up</button>
```

**Sélecteur CSS :** `[data-action="signup"]`

### Tester les vues

Lors du test des expériences web SPA :

1. Parcourez toutes les vues où des modifications s’appliquent.

1. Testez le flux utilisateur complet, notamment :
   * Navigation directe vers une vue (liens profonds)
   * Navigation à partir d’autres vues dans la SPA
   * Navigation avant et arrière du navigateur

1. Vérifiez que les modifications sont réappliquées lors du retour à une vue précédemment visitée.

### Gérer les transitions de vue

Certaines SPA utilisent des animations ou des transitions entre les vues. Pensez-y :

* **Minutage** - Assurez-vous que les modifications s’appliquent une fois les animations de transition terminées.
* **Visibilité des éléments** - Les éléments peuvent exister mais être masqués lors des transitions.
* **Scintillement** - Appliquez les modifications suffisamment tôt pour éviter les changements de contenu visibles.

## Dépannage

Lorsque vous passez en revue les modifications de conception de la SPA, suivez les recommandations ci-après pour résoudre certains problèmes courants :

* **Les modifications n’apparaissent pas** - Si les modifications n’apparaissent pas sur votre SPA :

   1. **Vérification du suivi des vues** - Vérifiez que les appels `sendEvent` incluent le nom de vue correct.

   1. **Vérifier l’existence de l’élément** - Assurez-vous que les éléments cibles sont dans le DOM lorsque des modifications s’appliquent.

   1. **Vérifier les sélecteurs** - Confirmez que les sélecteurs CSS correspondent à la structure DOM réelle.

   1. **Vérifier la console** - Recherchez les erreurs JavaScript qui pourraient empêcher les modifications.

* **Les modifications apparaissent brièvement, puis disparaissent** - Ce problème se produit généralement lorsque la SPA effectue un nouveau rendu et remplace les éléments modifiés :

   1. Utilisez des sélecteurs CSS plus spécifiques qui restent stables sur l’ensemble des rendus.

   1. Activez les observateurs de mutation pour réappliquer les modifications lorsque des éléments sont recréés.

   1. Contactez votre équipe de développement pour ajouter des attributs stables aux éléments cibles.

* **Dupliquer les modifications** - Si les modifications apparaissent plusieurs fois :

   1. Vérifiez que les événements de suivi des vues ne se déclenchent qu’une seule fois par transition de vue.

   1. Vérifiez que les modifications sont limitées à des vues spécifiques plutôt qu&#39;à des vues globales.

## Rubriques connexes

* [Présentation des expériences web](./web-experiences.md)
* [Conception d’expériences web](./web-experience-design.md)
* [Configurations du canal web](../admin/configure-channels-web.md)