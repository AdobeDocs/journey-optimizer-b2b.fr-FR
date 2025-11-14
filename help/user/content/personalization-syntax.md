---
title: Syntaxe de personnalisation
description: Découvrez la syntaxe de personnalisation basée sur les barres de contrôle dans Journey Optimizer B2B edition, y compris les expressions, les assistants, les types littéraux et les règles de mise en forme.
feature: Personalization, Content Design Tools
topic: Personalization
role: Developer
level: Intermediate
keywords: expression, éditeur, syntaxe, personnalisation
source-git-commit: fee5bddcce11b3035da6ab93b18bcc7006b4b554
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 44%

---

# Syntaxe de personnalisation {#personalization-syntax}

Les expressions dans l’[!DNL Journey Optimizer B2B Edition] [éditeur de personnalisation](./personalization.md#personalization-editor) sont basées sur la syntaxe de modèle _Handlebars_. Cette syntaxe utilise un modèle et un objet d&#39;entrée pour générer du code HTML ou d&#39;autres formats de texte. Les modèles Handlebars ressemblent à du texte normal avec des expressions Handlebars incorporées.

Pour plus d’informations sur Handlebars et son fonctionnement, reportez-vous à la [documentation HandlebarsJS](https://handlebarsjs.com/){target="_blank"}.

## Règles générales

Exemple d’expression simple :

```
{{account.accountName}}
```

Où ce qui suit est vrai :

* `account` est un espace de noms.
* `accountName` est un jeton composé par des attributs.

  >[!NOTE]
  >
  >La structure des attributs est définie dans un schéma XDM Adobe Experience Platform [](https://experienceleague.adobe.com/fr/docs/experience-platform/xdm/home){target="_blank"}.

* Les identifiants peuvent être n’importe quel caractère Unicode, à l’exception des caractères suivants :

  ```
  Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
  ```

* La syntaxe est sensible à la casse.

* Les mots **true**, **false**, **null** et **undefined** ne sont autorisés que dans la première partie d&#39;une expression de chemin.

* Dans Handlebars, les valeurs renvoyées par {\{expression}\} ont un échappement _HTML_. Si l’expression contient `&`, la sortie avec échappement HTML renvoyée est générée comme `&amp;`. Si vous ne souhaitez pas que Handlebars réalisent l’échappement d’une valeur, utilisez le signe +triple-stash_.

<!-- For example:

    If the value of the field `profile.person.name` is _Mark & Mary_, the `{\{profile.person.name}\}` value generates as `Mark &amp; Mary` and `{\{\{profile.person.name}}}` renders as `Mark & Mary`. -->

* Pour les arguments de fonctions littérales, l’analyseur de langage de modèle ne prend pas en charge le symbole barre oblique inverse (`\`) sans échappement. Ce caractère doit être placé dans une séquence d’échappement avec une barre oblique inverse (`\`) supplémentaire. Par exemple :

  ```
  {%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}
  ```

## Assistants {#helpers-all}

Une fonction d’assistance Handlebars est un identifiant simple qui peut être ajouté avec des paramètres. Chaque paramètre est une expression Handlebars. Ces assistants sont accessibles depuis n’importe quel contexte dans un modèle d’e-mail.

```sql
{{#each account.accountOrganization.annualRevenue.amount}}
    <li>{{this.name}}</li>
{{/each }}
```

<!-- These block helpers are identified with a `#` preceding the helper name and require a matching closing `/`, of the same name. 

Blocks are expressions that have a block opening ( {\{# }\} ) and closing ( {\{/} } ). -->

Pour plus d’informations sur ces fonctions, voir [Fonctions d’assistance](./personalization-helper-functions.md).

## Types littéraux {#literal-types}

[!DNL Adobe Journey Optimizer B2B Edition] prend en charge les types littéraux suivants :

| Littéral | Définition |
| ------- | ---------- |
| Chaîne | Un type de données composé de caractères entourés par des guillemets doubles. <br>Exemples : `"prospect"`, `"jobs"`, `"articles"` |
| Booléen | Un type de données qui est soit vrai soit faux. |
| Entier | Un type de données représentant un nombre entier. Ce nombre peut être positif, négatif ou nul. <br>Exemples : `-201`, `0`, `412` |
| Tableau | Un type de données composé d’un groupe d’autres valeurs littérales. Elle utilise des crochets pour regrouper et des virgules pour délimiter les différentes valeurs. <br> **Remarque :** vous ne pouvez pas accéder directement aux propriétés des éléments d’un tableau. <br> Exemples : `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>L&#39;utilisation de la variable **xEvent** n&#39;est pas disponible dans les expressions de personnalisation. Toute référence à xEvent entraîne des échecs de validation.
