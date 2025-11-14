---
title: Fonctions d'assistance
description: Guide de référence des fonctions d’assistance à la personnalisation dans Journey Optimizer B2B edition. Elle comprend une syntaxe et des exemples pour les chaînes, les dates, les mathématiques, etc.
feature: Personalization, Content Design Tools
topic: Personalization
role: Developer
level: Intermediate
keywords: expression, éditeur, syntaxe, personnalisation
source-git-commit: fee5bddcce11b3035da6ab93b18bcc7006b4b554
workflow-type: tm+mt
source-wordcount: '4857'
ht-degree: 44%

---

# Fonctions d&#39;assistance

Utilisez les fonctions d’assistance de l’éditeur de personnalisation pour définir des expériences de contenu personnalisées avec précision et efficacité en manipulant les données, en effectuant des calculs et en formatant le contenu. Explorez et testez ces fonctions, opérateurs et assistants pour découvrir comment ils fonctionnent ensemble pour vous aider à créer des parcours sur mesure et pilotés par les données.

>[!AVAILABILITY]
>
>Les fonctions d’assistance sont disponibles pour les environnements B2B edition Journey Optimizer configurés sur l’[architecture simplifiée](../simplified-architecture.md).

## Fonctions d’agrégation

Utilisez des fonctions d’agrégation pour regrouper plusieurs valeurs afin de former une seule valeur de synthèse. Vous pouvez également utiliser des fonctions de tableau et de liste pour définir plus facilement des interactions avec des tableaux, des listes et des chaînes.

### moyenne {#average}

Utilisez la fonction `average` pour renvoyer la moyenne arithmétique de toutes les valeurs sélectionnées dans le tableau.

+++Syntaxe

```sql
{%= average(array) %}
```

**Exemple**

L&#39;opération suivante renvoie le prix moyen de toutes les commandes.

```sql
{%=average(orders.order.price)%}
```

+++

### count {#count}

Utilisez la fonction `count` pour renvoyer le nombre d&#39;éléments dans le tableau donné.

+++Syntaxe

```sql
{%= count(array) %}
```

**Exemple**

L&#39;opération suivante renvoie le nombre de commandes dans le tableau.

```sql
{%= count(orders) %}
```

+++

### max {#max}

Utilisez la fonction `max` pour renvoyer la plus grande de toutes les valeurs sélectionnées dans le tableau.

+++Syntaxe

```sql
{%= max(array) %}
```

**Exemple**

L&#39;opération suivante renvoie le prix le plus élevé de toutes les commandes.

```sql
{%=max(orders.order.price)%}
```

+++

### min {#min}

Utilisez la fonction `min` pour renvoyer la plus petite de toutes les valeurs sélectionnées dans le tableau.

+++Syntaxe

```sql
{%= min(array) %}
```

**Exemple**

L&#39;opération suivante renvoie le prix le plus bas de toutes les commandes.

```sql
{%=min(orders.order.price) %}
```

+++

### sum {#sum}

Utilisez la fonction `sum` pour renvoyer la somme de toutes les valeurs sélectionnées dans le tableau.

+++Syntaxe

```sql
{%= sum(array) %}
```

**Exemple**

L&#39;opération suivante renvoie la somme des prix de toutes les commandes.

```sql
 {%=sum(orders.order.price)%}
```

+++

## Fonctions arithmétiques {#maths}

Utilisez des fonctions arithmétiques pour effectuer des calculs de base sur des valeurs.

### ajouter {#add}

Utilisez la fonction `+` (addition) pour trouver la somme de deux expressions d&#39;argument.

+++Syntaxe

```sql
{%= double + double %}
```

**Exemple**

L&#39;opération suivante additionne le prix de deux produits différents.

```sql
{%= product1.price + product2.price %}
```

+++

### multiplier {#multiply}

Utilisez la fonction `*` (multiplication) pour trouver le produit de deux expressions d&#39;argument.

+++Syntaxe

```sql
{%= double * double %}
```

**Exemple**

L&#39;opération suivante trouve le produit de l&#39;inventaire et du prix d&#39;un produit pour obtenir la valeur brute du produit.

```sql
{%= product.inventory * product.price %}
```

+++

### soustraire {#substract}

Utilisez la fonction `-` (soustraction) pour trouver la différence entre deux expressions d&#39;argument.

+++Syntaxe

```sql
{%= double - double %}
```

**Exemple**

L&#39;opération suivante trouve la différence de prix entre deux produits différents.

```sql
{%= product1.price - product2.price %}
```

+++

### diviser {#divide}

Utilisez la fonction `/` (division) pour trouver le quotient de deux expressions d&#39;argument.

+++Syntaxe

```sql
{%= double / double %}
```

**Exemple**

L&#39;opération suivante trouve le quotient entre le total des produits vendus et le total des revenus obtenus pour déterminer le coût moyen par article.

```sql
{%= totalProduct.price / totalProduct.sold %}
```

+++

### reste {#remainder}

Utilisez la fonction `%` (reste) pour trouver le reste après la division des deux expressions d&#39;argument.

+++Syntaxe

```sql
{%= double % double %}
```

**Exemple**

L&#39;opération suivante vérifie si l&#39;âge de la personne est divisible par cinq.

```sql
{%= person.age % 5 = 0 %}
```

+++

## Fonctions de liste et de tableau {#arrays}

Utilisez ces fonctions pour faciliter l&#39;interaction avec des tableaux, des listes et des chaînes.

### countOnlyNull {#count-only-null}

Utilisez la fonction `countOnlyNull` pour compter le nombre de valeurs nulles dans une liste.

+++Syntaxe

```sql
{%= countOnlyNull(array) %}
```

**Exemple**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Renvoie 3.

+++

### countWithNull {#count-with-null}

Utilisez la fonction `countWithNull` pour compter tous les éléments d’une liste, y compris les valeurs nulles.

+++Syntaxe

```sql
{%= countWithNull(array) %}
```

**Exemple**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Renvoie 6.

+++

### distinct {#distinct}

Utilisez la fonction `distinct` pour obtenir les valeurs d&#39;un tableau ou d&#39;une liste dont les valeurs en double sont supprimées.

+++Syntaxe

```sql
{%= distinct(array) %}
```

**Exemple**

L&#39;opération suivante définit les personnes qui ont passé des commandes dans plusieurs magasins.

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

+++

### distinctCountWithNull {#distinct-count-with-null}

Utilisez la fonction `distinctCountWithNull` pour compter le nombre de valeurs différentes dans une liste, y compris les valeurs nulles.

+++Syntaxe

```sql
{%= distinctCountWithNull(array) %}
```

**Exemple**

```sql
{%= distinctCountWithNull([10,2,10,null]) %}
```

Renvoie 3.

+++

### tête {#head}

Utilisez la fonction `head` pour renvoyer le premier élément dans un tableau ou une liste.

+++Syntaxe

```sql
{%= head(array) %}
```

**Exemple**

L&#39;opération suivante renvoie la première des cinq principales commandes au prix le plus élevé. Vous trouverez plus d&#39;informations sur la fonction `topN` dans la section [First `n` in array](#first-n).

```sql
{%= head(topN(orders,price, 5)) %}
```

+++

### topN {#first-n}

La fonction `topN` trie un tableau dans l’ordre décroissant en fonction de l’expression numérique donnée et renvoie les premiers éléments `N`. Si la taille du tableau est inférieure à `N`, il renvoie l’ensemble du tableau trié.

+++Syntaxe

```sql
{%= topN(array, value, amount) %}
```

| Argument | Description |
| --------- | ----------- |
| `{ARRAY}` | Tableau ou liste à trier. |
| `{VALUE}` | Propriété utilisée pour trier le tableau ou la liste. |
| `{AMOUNT}` | Nombre d’éléments à renvoyer. |

**Exemple**

L’opération suivante renvoie les cinq premières commandes au prix le plus bas.

```sql
{%= topN(orders,price, 5) %}
```

+++

### in {#in}

Utilisez la fonction `in` pour déterminer si un élément est un membre d&#39;un tableau ou d&#39;une liste.

+++Syntaxe

```sql
{%= in(value, array) %}
```

**Exemple**

L&#39;opération suivante définit les personnes dont l&#39;anniversaire est en mars, juin ou septembre.

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

+++

### inclut {#includes}

Utilisez la fonction `includes` pour déterminer si un tableau ou une liste contient un élément donné.

+++Syntaxe

```sql
{%= includes(array,item) %}
```

**Exemple**

L&#39;opération suivante définit les personnes dont le rouge est l&#39;une des couleurs préférées.

```sql
{%= includes(person.favoriteColors,"red") %}
```

+++

### intersectes {#intersects}

La fonction `intersects` permet de déterminer si deux tableaux ou deux listes ont au moins un membre commun.

+++Syntaxe

```sql
{%= intersects(array1, array2) %}
```

**Exemple**

L&#39;opération suivante définit les personnes dont les couleurs préférées comprennent au moins le rouge, le bleu ou le vert.

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```

+++

<!-- ## Intersection{#intersection}

The `intersection` function is used to determine the common members of two arrays or lists.

**Syntax**

```sql
intersection({ARRAY},{ARRAY})
```

**Example**

The following operation defines if person 1 and person 2 both have favorite colors of red, blue, and green.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```
-->

### bottomN {#last-n}

La fonction `bottomN` trie un tableau dans l’ordre croissant en fonction de l’expression numérique donnée et renvoie les premiers éléments `N`. Si la taille du tableau est inférieure à `N`, il renvoie l’ensemble du tableau trié.

+++Syntaxe

```sql
{%= bottomN(array, value, amount) %}
```

| Argument | Description |
| --------- | ----------- | 
| `{ARRAY}` | Tableau ou liste à trier. |
| `{VALUE}` | Propriété utilisée pour trier le tableau ou la liste. |
| `{AMOUNT}` | Nombre d’éléments à renvoyer. |

**Exemple**

L’opération suivante renvoie les cinq dernières commandes au prix le plus élevé.

```sql
{%= bottomN(orders,price, 5) %}
```

+++

### notIn {#notin}

Utilisez la fonction `notIn` pour déterminer si un élément n&#39;est pas membre d&#39;un tableau ou d&#39;une liste.

>[!NOTE]
>
>La fonction `notIn` assure *également* qu&#39;aucune valeur n&#39;est nulle. Par conséquent, les résultats ne sont pas une négation exacte de la fonction `in`.

+++Syntaxe

```sql
{%= notIn(value, array) %}
```

**Exemple**

L&#39;opération suivante définit les personnes dont l&#39;anniversaire n&#39;est ni en mars, ni en juin, ni en septembre.

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```

+++

### subsetOf {#subset}

Utilisez la fonction `subsetOf` pour déterminer si un tableau spécifique (tableau A) est un sous-ensemble d&#39;un autre tableau (tableau B). En d&#39;autres termes, elle permet de déterminer si tous les éléments du tableau A sont des éléments du tableau B.

+++Syntaxe

```sql
{%= subsetOf(array1, array2) %}
```

**Exemple**

L&#39;opération suivante définit les personnes qui ont visité toutes leurs villes préférées.

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

+++

### sur-ensemble de {#superset}

Utilisez la fonction `supersetOf` pour déterminer si un tableau spécifique (tableau A) est un sur-ensemble d&#39;un autre tableau (tableau B). En d&#39;autres termes, elle permet de déterminer si le tableau A contient tous les éléments du tableau B.

+++Syntaxe

```sql
{%= supersetOf(array1, array2) %}
```

**Exemple**

L&#39;opération suivante définit les personnes qui ont mangé des sushis et de la pizza au moins une fois.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"]) %}
```

+++

## Fonctions de date et d’heure {#date-time}

Utilisez les fonctions de date et d’heure pour effectuer des opérations de date et d’heure sur des valeurs.

### addDays {#add-days}

La fonction `addDays` ajuste une date donnée d’un nombre de jours spécifié, en utilisant des valeurs positives pour incrémenter et des valeurs négatives pour diminuer.

+++Syntaxe

```sql
{%= addDays(date, number) %}
```

**Exemple**

* Entrée : `{%= addDays(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Sortie : `2024-11-11T17:19:51Z`

+++

### addHours {#add-hours}

La fonction `addHours` ajuste une date donnée d’un nombre d’heures spécifié, en utilisant des valeurs positives pour incrémenter et des valeurs négatives pour diminuer.

+++Syntaxe

```sql
{%= addHours(date, number) %}
```

**Exemple**

* Entrée : `{%= addHours(stringToDate("2024-11-01T17:19:51Z"),1) %}`
* Sortie : `2024-11-01T18:19:51Z`

+++

### addMinutes {#add-minutes}

La fonction `addMinutes` ajuste une date donnée d’un nombre de minutes spécifié, en utilisant des valeurs positives pour incrémenter et des valeurs négatives pour diminuer.

+++Syntaxe

```sql
{%= addMinutes(date, number) %}
```

**Exemple**

* Entrée : `{%= addMinutes(stringToDate("2024-11-01T17:59:51Z"),10) %}`
* Sortie : `2024-11-01T18:09:51Z`

+++

### addMonths {#add-months}

La fonction `addMonths` ajuste une date donnée d’un nombre de mois spécifié, en utilisant des valeurs positives pour incrémenter et des valeurs négatives pour diminuer.

+++Syntaxe

```sql
{%= addMonths(date, number) %}
```

**Exemple**

* Entrée : `{%= addMonths(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Sortie : `2025-01-01T17:19:51Z`

+++

### addSeconds {#add-seconds}

La fonction `addSeconds` ajuste une date donnée d’un nombre de secondes spécifié, en utilisant des valeurs positives pour incrémenter et des valeurs négatives pour diminuer.

+++Syntaxe

```sql
{%= addSeconds(date, number) %}
```

**Exemple**

* Entrée : `{%= addSeconds(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Sortie : `2024-11-01T17:20:01Z`

+++

### addYears {#add-years}

La fonction `addYears` ajuste une date donnée d’un nombre d’années spécifié, en utilisant des valeurs positives pour incrémenter et des valeurs négatives pour diminuer.

+++Syntaxe

```sql
{%= addYears(date, number) %}
```

**Exemple**

* Entrée : `{%= addYears(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Sortie : `2026-11-01T17:19:51Z`

+++

### âge {#age}

Utilisez la fonction `age` pour récupérer l’âge à partir d’une date donnée.

+++Syntaxe

```sql
 {%= age(datetime) %}
```

<!--
**Example**

The following operation gets the value of the identity map for the key `example@example.com`.

```sql
 {%= age(datetime) %}
```
-->

+++

### ageInDays {#age-days}

La fonction `ageInDays` calcule le nombre de jours écoulés entre la date donnée et la date actuelle. Il utilise une valeur négative pour les dates futures et une valeur positive pour les dates passées.

+++Syntaxe

```sql
{%= ageInDays(date) %}
```

**Exemple**

currentDate = 2025-01-07T12:17:10.720122+05:30 (Asie/Calcutta)

* Entrée : `{%= ageInDays(stringToDate("2025-01-01T17:19:51Z"))%}`
* Sortie : `5`

+++

### ageInMonths {#age-months}

La fonction `ageInMonths` calcule le nombre de mois écoulés entre la date donnée et la date actuelle. Il utilise une valeur négative pour les dates futures et une valeur positive pour les dates passées.

+++Syntaxe

```sql
{%= ageInMonths(date) %}
```

**Exemple**

currentDate = 2025-01-07T12:22:46.993748+05:30(Asie/Calcutta)

* Entrée : `{%=ageInMonths(stringToDate("2024-01-01T00:00:00Z"))%}`
* Sortie : `12`

+++

### compareDates {#compare-dates}

La fonction `compareDates` compare la première date d’entrée à l’autre. Elle renvoie 0 si date1 est égale à date2, -1 si date1 est antérieure à date2 et 1 si date1 est postérieure à date2.

+++Syntaxe

```sql
{%= compareDates(date1, date2) %}
```

**Exemple**

* Entrée : `{%=compareDates(stringToDate("2024-12-02T00:00:00Z"), stringToDate("2024-12-03T00:00:00Z"))%}`
* Sortie : `-1`

+++

### convertZonedDateTime {#convert-zoned-date-time}

La fonction `convertZonedDateTime` convertit une date-heure en un fuseau horaire donné.

+++Syntaxe

```sql
{%= convertZonedDateTime(dateTime, timezone) %}
```

**Exemple**

* Entrée : `{%=convertZonedDateTime(stringToDate("2019-02-19T08:09:00Z"), "Asia/Tehran")%}`
* Sortie : `2019-02-19T11:39+03:30[Asia/Tehran]`

+++

### currentTimeInMillis {#current-time}

Utilisez la fonction `currentTimeInMillis` pour récupérer l’heure actuelle en millisecondes Epoch.

+++Syntaxe

```sql
{%= currentTimeInMillis() %}
```

<!--
**Example**

The following operation gets all the keys for the map `identityMap`.

```sql
{%= keys(identityMap) %}
```
-->

+++

### dateDiff {#date-diff}

Utilisez la fonction `dateDiff` pour récupérer la différence entre deux dates en nombre de jours.

+++Syntaxe

```sql
{%= dateDiff(datetime,datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### dayOfMonth {#day-month}

La fonction `dayOfMonth` renvoie le nombre représentant le jour du mois.

+++Syntaxe

```sql
{%= dayOfMonth(datetime) %}
```

**Exemple**

* Entrée : `{%= dayOfMonth(stringToDate("2024-11-05T17:19:51Z")) %}`
* Sortie : `5`

+++

### Jour de la semaine {#day-week}

Utilisez la fonction `dayOfWeek` pour récupérer le jour de la semaine.

+++Syntaxe

```sql
{%= dayOfWeek(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### dayOfYear {#day-year}

Utilisez la fonction `dayOfYear` pour récupérer le jour de l’année.

+++Syntaxe

```sql
{%= dayOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### diffInSeconds {#diff-seconds}

La fonction `diffInSeconds` renvoie la différence entre deux dates en nombre de secondes.

+++Syntaxe

```sql
{%= diffInSeconds(endDate, startDate) %}
```

**Exemple**

* Entrée : `{%=diffInSeconds(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T17:19:01Z"))%}`
* Sortie : `50`

+++

### extractHours {#extract-hours}

La fonction `extractHours` extrait le composant des heures d’un horodatage donné.

+++Syntaxe

```sql
{%= extractHours(date) %}
```

**Exemple**

* Entrée : `{%= extractHours(stringToDate("2024-11-01T17:19:51Z"))%}`
* Sortie : `17`

+++

### extractMinutes {#extract-minutes}

La fonction `extractMinutes` extrait le composant des minutes d’un horodatage donné.

+++Syntaxe

```sql
{%= extractMinutes(date) %}
```

**Exemple**

* Entrée : `{%= extractMinutes(stringToDate("2024-11-01T17:19:51Z"))%}`
* Sortie : `19`

+++

### extractMonths {#extract-months}

La fonction `extractMonth` extrait le composant des mois d’un horodatage donné.

+++Syntaxe

```sql
{%= extractMonths(date) %}
```

**Exemple**

* Entrée : `{%=extractMonth(stringToDate("2024-11-01T17:19:51Z"))%}`
* Sortie : `11`

+++

### extractSeconds {#extract-seconds}

La fonction `extractSeconds` extrait le composant des secondes d’un horodatage donné.

+++Syntaxe

```sql
{%= extractSeconds(date) %}
```

**Exemple**

* Entrée : `{%=extractSeconds(stringToDate("2024-11-01T17:19:51Z"))%}`
* Sortie : `51`

+++

### formatDate {#format-date}

Utilisez la fonction `formatDate` pour formater une valeur de date et d’heure. Le format doit être un modèle de `DateTimeFormat` Java valide.

+++Syntaxe

```sql
{%= formatDate(datetime, format) %}
```

Où la première chaîne correspond à l’attribut date et la seconde à la manière dont vous souhaitez que la date soit convertie et affichée.

>[!NOTE]
>
> Si un modèle de date n’est pas valide, la date revient au format ISO standard.
>
> Vous pouvez utiliser des fonctions de mise en forme des dates de Java, tel que cela est résumé dans la [documentation Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}.

**Exemple**

L’opération suivante renvoie la date au format suivant : MM/JJ/AA.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}
```

+++

#### Caractères de motif {#pattern-characters}

Certaines lettres motifs peuvent ressembler à d’autres, mais représentent des concepts différents.

| Modèle | Signification | Exemple (par `2023-12-31T10:15:30Z`) |
|---------|---------|--------------------------------------|
| `y` | Année civile (année standard) | `2023` |
| `Y` | Année basée sur une semaine (ISO 8601). Il peut varier selon les limites de l&#39;année. | `2024` (le 31 décembre 2023 tombe dans la première semaine de 2024) |
| `M` | Mois de l’année (1-12 ou texte comme `Jan`, `January`) | `12` ou `Dec`. |
| `m` | Minute de l’heure (0-59) | `15` |
| `d` | Jour du mois (1-31) | `31` |
| `D` | Jour de l’année (1-366) | `365` |

#### Formater la date avec la prise en charge des paramètres régionaux {#format-date-locale}

Vous pouvez utiliser la fonction `formatDate` pour formater une valeur d’heure et de date au format de la langue correspondante, par exemple pour un paramètre régional souhaité. Le format doit être un modèle de `DateTimeFormat` Java valide.

+++Syntaxe

```sql
{%= formatDate(datetime, format, locale) %}
```

Lorsque la première chaîne correspond à l’attribut date, la deuxième valeur correspond à la manière dont vous souhaitez que la date soit convertie et affichée, et la troisième valeur représente le paramètre régional au format chaîne.

>[!NOTE]
>
> Si un modèle de date n’est pas valide, la date revient au format ISO standard.
>
> Vous pouvez utiliser des fonctions de formatage des dates Java comme résumé dans la documentation [Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html).
>
> Vous pouvez utiliser la mise en forme et des paramètres régionaux valides comme indiqué dans la documentation [Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) et [Paramètres régionaux pris en charge](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html).

**Exemple**

L’opération suivante renvoie la date au format suivant : MM/jj/AA, dans le paramètre régional FRANCE.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY", "fr_FR") %}
```

+++

### getCurrentZonedDateTime {#get-current-zoned-date-time}

La fonction `getCurrentZonedDateTime` renvoie la date et l’heure actuelles avec les informations de fuseau horaire.

+++Syntaxe

```sql
{%= getCurrentZonedDateTime() %}
```

**Exemple**

* Entrée : `{%= getCurrentZonedDateTime() %}`
* Sortie : `2024-12-06T17:22:02.281067+05:30[Asia/Kolkata]`

+++

### diffInHours {#hours-difference}

La fonction `diffInHours` renvoie la différence entre deux dates en nombre d’heures.

+++Syntaxe

```sql
{%= diffInHours(endDate, startDate) %}
```

**Exemple**

* Entrée : `{%= diffInHours(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T07:19:51Z"))%}`
* Sortie : `10`

+++

### diffInMinutes {#diff-minutes}

La fonction `diffInMinutes` renvoie la différence entre deux dates en termes de minutes.

+++Syntaxe

```sql
{%= diffInMinutes(endDate, startDate) %}
```

**Exemple**

* Entrée : `{%= diffInMinutes(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T16:19:51Z"))%}`
* Sortie : `60`

+++

### diffInMonths {#months-difference}

La fonction `diffInMonths` renvoie la différence entre deux dates en nombre de mois.

+++Syntaxe

```sql
{%= diffInMonths(endDate, startDate) %}
```

**Exemple**

* Entrée : `{%=diffInMonths(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-08-01T17:19:51Z"))%}`
* Sortie : `3`

+++

### setDays {#set-days}

Utilisez la fonction `setDays` pour définir le jour du mois pour la date et l’heure données.

+++Syntaxe

```sql
{%= setDays(datetime, day) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### setHours {#set-hours}

Utilisez la fonction `setHours` pour définir l’heure de la date et de l’heure.

+++Syntaxe

```sql
{%= setHours(datetime, hour) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### toDateTime {#string-to-date-time}

La fonction `toDateTime` convertit une chaîne en date. Elle renvoie la date de l’époque comme sortie pour une entrée non valide.

+++Syntaxe

```sql
{%= toDateTime(string, string) %}
```

**Exemple**

* Entrée : `{%=toDateTime("2024-11-01T17:19:51Z")%}`
* Sortie : `2024-11-01T17:19:51Z`

+++

### toUTC {#to-utc}

Utilisez la fonction `toUTC` pour convertir une heure en UTC.

+++Syntaxe

```sql
{%= toUTC(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### truncateToStartOfDay {#truncate-day}

Utilisez la fonction `truncateToStartOfDay` pour modifier une date-heure donnée en définissant au début de la journée l&#39;heure à 00:00.

+++Syntaxe

```sql
{%= truncateToStartOfDay(date) %}
```

**Exemple**

* Entrée : `{%= truncateToStartOfDay(stringToDate("2024-11-01T17:19:51Z")) %}`
* Sortie : `2024-11-01T00:00Z`

+++

### truncateToStartOfQuarter {#truncate-quarter}

Utilisez la fonction `truncateToStartOfQuarter` pour tronquer une date-heure au premier jour de son trimestre (par exemple, le 1er janvier, le 1er avril, le 1er juillet et le 1er octobre) à 00:00.

+++Syntaxe

```sql
{%= truncateToStartOfQuarter(dateTime) %}
```

**Exemple**

* Entrée : `{%=truncateToStartOfQuarter(stringToDate("2024-11-01T17:19:51Z"))%}`
* Sortie : `2024-10-01T00:00Z`

+++

### truncateToStartOfWeek {#truncate-week}

La fonction `truncateToStartOfWeek` modifie une date-heure donnée en la définissant sur le début de la semaine (lundi à 00:00).

+++Syntaxe

```sql
{%= truncateToStartOfWeek(dateTime) %}
```

**Exemple**

* Entrée : `{%= truncateToStartOfWeek(stringToDate("2024-11-19T17:19:51Z"))%} // tuesday`
* Sortie : `2024-11-18T00:00Z // monday`

+++

### truncateToStartOfYear {#truncate-year}

Utilisez la fonction `truncateToStartOfYear` pour modifier une date-heure donnée en la tronquant au premier jour de l’année (1er janvier) à 00:00.

+++Syntaxe

```sql
{%= truncateToStartOfYear(dateTime) %}
```

**Exemple**

* Entrée : `{%=truncateToStartOfYear(stringToDate("2024-11-01T17:19:51Z"))%}`
* Sortie : `2024-01-01T00:00Z`

+++

### weekOfYear {#week-of-year}

Utilisez la fonction `weekOfYear` pour récupérer la semaine de l’année.

+++Syntaxe

```sql
{%= weekOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### diffInYears {#diff-years}

Utilisez la fonction `diffInYears` pour renvoyer la différence entre deux dates en termes d&#39;années.

+++Syntaxe

```sql
{%= diffInYears(endDate, startDate) %}: int
```

**Exemple**

* Entrée : `{%=diffInYears(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2019-10-01T17:19:51Z"))%}`
* Sortie : `5`

+++

## Fonctions de l’opérateur {#operators}

Utilisez les fonctions booléenne et de comparaison pour effectuer des évaluations logiques.

### and {#and}

La fonction `and` est utilisée pour convertir un nombre en pourcentage.

+++Syntaxe

```sql
{%= query1 and query2 %}
```

**Exemple**

L&#39;opération suivante renvoie toutes les personnes ayant leur pays d&#39;origine (France) et leur année de naissance (1985).

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

+++

### ou {#or}

La fonction `or` est utilisée pour créer une disjonction logique.

+++Syntaxe

```sql
{%= query1 or query2 %}
```

**Exemple**

L&#39;opération suivante renvoie toutes les personnes ayant leur pays d&#39;origine (France) ou leur année de naissance (1985).

```sql
{%= profile.homeAddress.country = "France" or profile.person.birthYear = 1985 %}
```

+++

<!--
## Not{#not}

The `not` (or `!`) function is used to create a logical negation.

**Syntax**

```sql
not ({QUERY})
!({QUERY})
```

**Example**

The following operation will return all people who do not have their home country as Canada.

```sql
not (homeAddress.countryISO = "CA")
```
-->

### est égal à {#operator-equals}

La fonction `=` (égal à) vérifie si une valeur ou expression est égale à une autre valeur ou expression.

+++Syntaxe

```sql
{%= expression = value %}
```

**Exemple**

L&#39;opération suivante vérifie si le pays de l&#39;adresse du domicile est la France.

```sql
{%= profile.homeAddress.country = "France" %}
```

+++

### différent de {#notequal}

La fonction `!=` (différent de) vérifie si une valeur ou expression est **différente** d&#39;une autre valeur ou expression.

+++Syntaxe

```sql
{%= expression != value %}
```

**Exemple**

L&#39;opération suivante vérifie si le pays de l&#39;adresse du domicile n&#39;est pas la France.

```sql
{%= profile.homeAddress.country != "France" %}
```

+++

### supérieur à {#greaterthan}

Utilisez la fonction `>` (supérieur à) pour vérifier si la première valeur est supérieure à la seconde.

+++Syntaxe

```sql
{%= expression1 > expression2 %}
```

**Exemple**

L&#39;opération suivante définit les personnes nées strictement après 1970.

```sql
{%= profile.person.birthYear > 1970 %}
```

+++

### supérieur ou égal à {#greaterthanorequal}

Utilisez la fonction `>=` (supérieur ou égal à) pour vérifier si la première valeur est supérieure ou égale à la seconde.

+++Syntaxe

```sql
{%= expression1 >= expression2 %}
```

**Exemple**

L&#39;opération suivante définit les personnes nées en 1970 ou après.

```sql
{%= profile.person.birthYear >= 1970 %}
```

+++

### inférieur à {#lessthan}

Utilisez la fonction de comparaison `<` (inférieur à) pour vérifier si la première valeur est inférieure à la seconde.

+++Syntaxe

```sql
{%= expression1 < expression2 %}
```

**Exemple**

L&#39;opération suivante définit les personnes nées avant 2000.

```sql
{%= profile.person.birthYear < 2000 %}
```

+++

### inférieur ou égal à{#lessthanorequal}

Utilisez la fonction de comparaison `<=` (inférieur ou égal à) pour vérifier si la première valeur est inférieure ou égale à la seconde.

+++Syntaxe

```sql
{%= expression1 <= expression2 %}
```

**Exemple**

L&#39;opération suivante définit les personnes nées en 2000 ou avant.

```sql
{%= profile.person.birthYear <= 2000 %}
```

+++

## Fonctions dynamiques {#dynamic-helpers}

Utilisez les fonctions d’assistance dynamique pour utiliser des évaluations conditionnelles, une itération et des affectations de variables pour la personnalisation dynamique.

### Valeur de secours par défaut {#default-value}

L’helper `Default Fallback Value` est utilisé pour renvoyer une valeur de secours par défaut si un attribut est vide ou nul. Ce mécanisme fonctionne pour les attributs de profil et les événements de parcours.

+++Syntaxe

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

Dans cet exemple, la valeur `there` s&#39;affiche si l&#39;attribut `firstName` de ce profil est vide ou nul.

+++

### if (conditions) {#if-function}

L&#39;helper `if` est utilisé pour définir un bloc conditionnel.
Si l&#39;évaluation de l&#39;expression renvoie true, le bloc est rendu, sinon il est ignoré.

+++Syntaxe

```sql
{%#if contains(account.accountOrganization.primaryEmailDomain, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

À la suite de l&#39;helper `if`, vous pouvez saisir une instruction `else` pour spécifier un bloc de code à exécuter, si la même condition est false.
L&#39;instruction `elseif` spécifie une nouvelle condition à tester si la première instruction renvoie false.


**Format**

```sql
{
    {
        {%#if condition1%} element_1 
        {%else if condition2%} element_2 
        {%else%} default_element 
        {%/if%}
    }
}
```

<!-- 
**Examples**

* **Render different store links based on conditional expressions**

    ```sql
    {%#if profile.homeAddress.countryCode = "FR"%}
    <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
    {%else%}
    <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
    {%/if%}
    ```

* **Determine email address extension**

    ```sql
    {%#if contains(profile.personalEmail.address, ".edu")%}
    <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
    {%else if contains(profile.personalEmail.address, ".org")%}
    <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
    {%else%}
    <a href="https://www.adobe.com/users">Checkout our page</a>
    {%/if%}
    ```

* **Add a conditional link**

    The following operation adds a link to the `www.adobe.com/academia` website for profiles with '.edu' email addresses only, the `www.adobe.com/org` website for profiles with '.org' email addresses, and the default URL `www.adobe.com/users` for all other profiles:

    ```sql
    {%#if contains(profile.personalEmail.address, ".edu")%}
    <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
    {%else if contains(profile.personalEmail.address, ".org")%}
    <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
    {%else%}
    <a href="https://www.adobe.com/users">Checkout our page</a>
    {%/if%}
    ```

* **Conditional content based on audience membership**

    ```sql
    {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
    Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
    {%else if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"%}
    Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
    {%/if%}
    ```
-->

+++

### sauf si {#unless}

Utilisez l&#39;assistant `unless` pour définir un bloc conditionnel. Par opposition à l’assistant `if`, si l’évaluation de l’expression renvoie false, le bloc est rendu.

+++Syntaxe

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**Exemple**

Générer du contenu en fonction de l’extension d’adresse e-mail :

```sql
{%#unless endsWith(account.accountOrganization.primaryEmailDomain}, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content
{%/unless%}
```

+++

### each {#each}

Utilisez l&#39;assistant `each` pour effectuer une itération sur un tableau.

La structure d’assistance est ```{{#each ArrayName}}``` YourContent `{{/each}}`

Vous pouvez utiliser le mot-clé `this` à l’intérieur du bloc pour faire référence aux éléments individuels du tableau. Utilisez `{{@index}}` pour effectuer le rendu de l’index de l’élément du tableau .

+++Syntaxe

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
{{/each}}
```

**Exemple**

```sql
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**Exemple**

Générer une liste de produits que cet utilisateur a dans son panier :

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
{{/each}}
```

+++

### avec {#with}

Utilisez l&#39;assistant `with` pour modifier le jeton d&#39;évaluation d&#39;une partie de modèle.

+++Syntaxe

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

L&#39;helper `with` est utile pour définir également une variable de raccourci.

**Exemple**

Utilisez `with` pour créer des alias entre les noms de variables longs et les noms plus courts :

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

+++

### let {#let}

La fonction `let` permet à une expression d&#39;être stockée en tant que variable et d&#39;être utilisé ultérieurement dans une requête.

+++Syntaxe

```sql
{% let variable = expression %} {{variable}}
```

**Exemple**

L&#39;exemple suivant permet de calculer la somme totale des prix des produits du panier dont les prix sont compris entre 100 et 1 000.

```sql
{% let sum = 0%}
    {{#each profile.productsInCart as |p|}}
        {%#if p.price>100 and p.price<1000%}
            {%let sum = sum + p.price %}
        {%/if%}
    {{/each}}
{{sum}}
```

+++

## Métadonnées d’exécution {#execution-metadata}

>[!AVAILABILITY]
>
>Cette fonctionnalité est en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour en obtenir l’accès.

Utilisez le `executionMetadata` pour capturer et stocker dynamiquement des paires clé-valeur personnalisées dans le contexte d’exécution du message.

Cette fonction vous permet d’ajouter des informations contextuelles à toute action native de vos campagnes ou parcours. Utilisez-les pour exporter des données contextuelles de diffusion en temps réel vers des systèmes externes à diverses fins, telles que le suivi, l’analyse, la personnalisation et le traitement en aval.

>[!NOTE]
>
>Les actions personnalisées ne prennent pas en charge la fonction `executionMetadata`.

Vous pouvez, par exemple, utiliser l’assistant `executionMetadata` pour ajouter un identifiant spécifique à chaque diffusion envoyée à chaque profil. Ces informations sont générées lors de l’exécution, puis vous pouvez importer les métadonnées d’exécution enrichies pour la réconciliation en aval à l’aide d’une plateforme de création de rapports externe.

+++Syntaxe

```
{{executionMetadata key="your_key" value="your_value"}}
```

Dans cette syntaxe, `key` fait référence au nom des métadonnées et `value` correspond aux métadonnées à conserver.

**Fonctionnement**

Sélectionnez n’importe quel élément du contenu de votre canal dans une campagne ou un parcours et, à l’aide de l’éditeur de personnalisation, ajoutez l’assistant `executionMetadata` à cet élément.

>[!NOTE]
>
>La fonction `executionMetadata` n’est pas visible lorsque le contenu lui-même est affiché.

Au moment de l’exécution, la valeur des métadonnées est ajoutée au **[!UICONTROL jeu de données d’événement de retour de message]** existant avec le schéma suivant :

```
"_experience": {
  "customerJourneyManagement": {
    "messageExecution": {
      "metadata": {
        "your_key": "your_value"
      }
    }
  }
}
```

>[!IMPORTANT]
>
>La limite supérieure est de 2 Ko sur les paires clé-valeur par action. Si vous dépassez la limite de 2 Ko, le message est toujours diffusé, mais toutes les paires clé-valeur peuvent être tronquées.

**Exemple**

```
{{executionMetadata key="firstName" value=profile.person.name.firstName}}
```

Dans cet exemple, en supposant que `profile.person.name.firstName` = « Alex », l’entité obtenue est :

```
{
  "key": "firstName",
  "value": "Alex"
}
```

+++

## Fonctions de mappage {#maps}

Utilisez les fonctions de mappage dans la personnalisation pour faciliter l&#39;interaction avec les mappages.

### get {#get}

Utilisez la fonction `get` pour récupérer la valeur d’un mappage pour une clé donnée.

+++Syntaxe

```sql
{%= get(map, string) %}
```

**Exemple**

L&#39;opération suivante renvoie la valeur de la carte d&#39;identité pour la clé `example@example.com`.

```sql
{%= get(identityMap,"example@example.com") %}
```

+++

### keys {#keys}

Utilisez la fonction `keys` pour récupérer toutes les clés d&#39;une carte donnée.

+++Syntaxe

```sql
{%= keys(map) %}
```

**Exemple**

L&#39;opération suivante récupère toutes les clés pour le mappage `identityMap`.

```sql
{%= keys(identityMap) %}
```

+++

### valeurs {#values}

La fonction `values` est utilisée pour récupérer toutes les valeurs d&#39;une carte donnée.

+++Syntaxe

```sql
{%= values(map) %}
```

**Exemple**

L’opération suivante récupère toutes les valeurs du `identityMap` de mappage.

```sql
{%= values(identityMap) %}
```

+++

## Fonctions mathématiques {#math}

Découvrez comment utiliser des fonctions mathématiques dans l’éditeur de personnalisation.

### absolu {#absolute}

Utilisez la fonction `absolute` pour convertir un nombre en valeur absolue.

+++Syntaxe

```sql
{%= absolute(int) %}: int
```

+++

### formatNumber {#format-number}

Utilisez la fonction `formatNumber` pour formater n’importe quel nombre dans sa représentation sensible à la langue.

Elle accepte un nombre et une chaîne représentant les paramètres régionaux et renvoie une chaîne formatée du nombre dans les paramètres régionaux souhaités.

+++Syntaxe

```sql
{%= formatNumber(number/double,string) %}: string
```

Vous pouvez utiliser la mise en forme et des paramètres régionaux valides comme indiqué dans la documentation d’[Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) et [Paramètres régionaux pris en charge](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}

**Exemple**

Cette requête renvoie une chaîne formatée en arabe correspondant à 123456,789 comme nombre d’entrée.

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

+++

### random {#random}

Utilisez la fonction `random` pour renvoyer une valeur aléatoire comprise entre 0 et 1.

+++Syntaxe

```sql
{%= random() %}: double
```

+++

### roundDown {#round-down}

Utilisez la fonction `roundDown` pour arrondir un nombre à l’unité inférieure.

+++Syntaxe

```sql
{%= roundDown(double) %}: double
```

+++

### roundUp {#round-up}

Utilisez la fonction `roundUp` pour arrondir un nombre à l’unité supérieure.

+++Syntaxe

```sql
{%= roundUp(double) %}: double
```

+++

### toHexString {#to-hex-string}

La fonction `toHexString` convertit n’importe quel nombre en sa chaîne hexadécimale.

+++Syntaxe

```sql
{%= toHexString(number) %}: string
```

**Exemple**

Cette requête renvoie la valeur hexadécimale de 158 sous la forme 9e.

```sql
{%= toHexString(158) %}
```

+++

### toInt {#to-int}

Utilisez la fonction `toInt` pour convertir des types (nombre, double, entier, long, flottant, court, octet, booléen, chaîne) en nombres entiers.

+++Syntaxe

```sql
{%= toInt(<valueToConvert>) %}: integer
```

**Exemple**

Cette requête renvoie la valeur entière de 42,6 comme 42.

```sql
{%= toInt(42.6) %}: integer
```

+++

### toPercentage {#to-percentage}

Utilisez la fonction `toPercentage` pour convertir un nombre en pourcentage.

+++Syntaxe

```sql
{%= toPercentage(double) %}: string
```

+++

### toPrecision {#to-precision}

Utilisez la fonction `toPrecision` pour convertir un nombre à la précision requise.

+++Syntaxe

```sql
{%= toPrecision(double,int) %}: string
```

+++

### toString {#to-string}

La fonction `toString` convertit n’importe quel nombre en sa représentation sous forme de chaîne.

+++Syntaxe

```sql
{%= toString(string) %}: string
```

**Exemple**

Cette requête renvoie `"12"`.

```sql
{%= toString(12) %} 
```

+++

## Fonctions d’objet {#objects}

Fonctions d’objet permettant d’interroger les propriétés ou les attributs d’objet.

### isNull {#isNull}

La fonction `isNull` détermine si une référence d&#39;objet n&#39;existe pas.

+++Syntaxe

```sql
{%= isNull(object) %}
```

**Exemple**

L&#39;opération suivante vérifie si l&#39;adresse de la personne n&#39;existe pas.

```sql
{%= isNull(person.homeAddress) %}
```

+++

### isNotNull {#isNotNull}

La fonction `isNotNull` détermine si une référence d&#39;objet existe.

+++Syntaxe

```sql
{%= isNotNull(object) %}
```

**Exemple**

L&#39;opération suivante vérifie si l&#39;adresse de la personne existe.

```sql
{%= isNotNull(person.homeAddress) %}
```

+++

## Fonctions de chaîne {#string-functions}

Découvrez comment utiliser les fonctions de chaîne dans l’éditeur de personnalisation.

### camelCase {#camelCase}

La fonction `camelCase` met en majuscule la première lettre de chaque mot d&#39;une chaîne.

+++Syntaxe

```sql
{%= camelCase(string)%}
```

**Exemple**

La fonction suivante met en majuscule la première lettre d&#39;un mot de l&#39;adresse postale du profil.

```sql
{%= camelCase(profile.homeAddress.street) %}
```

+++

### charCodeAt {#char-code-at}

La fonction `charCodeAt` renvoie la valeur ASCII d’un caractère, comme la fonction `charCodeAt` dans JavaScript. Elle prend une chaîne et un entier (définissant la position d’un caractère) comme arguments d’entrée et renvoie sa valeur ASCII correspondante.

+++Syntaxe

```sql
{%= charCodeAt(string,int) %}: int
```

**Exemple**

La fonction suivante renvoie la valeur ASCII de `o` (111).

```sql
{%= charCodeAt("some", 1)%}
```

+++

### concat {#concate}

La fonction `concat` combine deux chaînes en une seule.

+++Syntaxe

```sql
{%= concat(string,string) %}
```

**Exemple**

La fonction suivante combine la ville et le pays du profil dans une seule chaîne.

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

+++

### contient {#contains}

Utilisez la fonction `contains` pour déterminer si une chaîne contient une sous-chaîne spécifiée.

+++Syntaxe

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Description |
| --------- | ----------- |
| `STRING_1` | La chaîne à vérifier. |
| `STRING_2` | La chaîne à rechercher dans la première chaîne. |
| `CASE_SENSITIVE` | Un paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Valeurs possibles : true (par défaut)/false. |

**Exemples**

* La fonction suivante vérifie si le prénom du profil contient la lettre A (en majuscule ou en minuscule). Si c’est le cas, le profil renvoie `true`. Si ce n’est pas le cas, il renvoie `false`.

  ```sql
  {%= contains(profile.person.name.firstName, "A", false) %}
  ```

* La requête suivante détermine si l’adresse e-mail de la personne contient la chaîne `2010@gm` en respectant la casse.

  ```sql
  {%= contains(profile.person.emailAddress,"2010@gm") %}
  ```

+++

### neContientPas {#doesNotContain}

Utilisez la fonction `doesNotContain` pour déterminer si une chaîne ne contient pas une sous-chaîne spécifiée.

+++Syntaxe

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Description |
| --------- | ----------- |
| `STRING_1` | La chaîne à vérifier. |
| `STRING_2` | La chaîne à rechercher dans la première chaîne. |
| `CASE_SENSITIVE` | Un paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Valeurs possibles : true (par défaut)/false. |

**Exemple**

La requête suivante détermine si l’adresse e-mail de la personne ne contient pas la chaîne `2010@gm` en respectant la casse.

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```

+++

### doNotEndWith {#doesNotEndWith}

Utilisez la fonction `doesNotEndWith` pour déterminer si une chaîne ne se termine pas par une sous-chaîne spécifiée.

+++Syntaxe

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | La chaîne à rechercher dans la première chaîne. |
| `{CASE_SENSITIVE}` | Un paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Valeurs possibles : true (par défaut)/false. |

**Exemple**

La requête suivante détermine si l’adresse e-mail de la personne ne se termine pas par `.com` en respectant la casse.

```sql
doesNotEndWith(person.emailAddress,".com")
```

+++

### doNotStartWith {#doesNotStartWith}

Utilisez la fonction `doesNotStartWith` pour déterminer si une chaîne ne commence pas par une sous-chaîne spécifiée.

+++Syntaxe

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | La chaîne à rechercher dans la première chaîne. |
| `{CASE_SENSITIVE}` | Un paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Valeurs possibles : true (par défaut)/false. |

**Exemple**

La requête suivante détermine si le nom de la personne ne commence pas par `Joe` en respectant la casse.

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

+++

### encode64 {#encode64}

Utilisez la fonction `encode64` pour coder une chaîne afin de conserver les informations personnelles (PI), telles que pour les inclure dans une URL.

+++Syntaxe

```sql
{%= encode64(string) %}
```

+++

### se termine par {#endsWith}

Utilisez la fonction `endsWith` pour déterminer si une chaîne se termine par une sous-chaîne spécifiée.

+++Syntaxe

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | La chaîne à rechercher dans la première chaîne. |
| `{CASE_SENSITIVE}` | Un paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Valeurs possibles : true (par défaut)/false. |

**Exemple**

La requête suivante détermine si l’adresse e-mail de la personne se termine par `.com` en respectant la casse.

```sql
{%= endsWith(person.emailAddress,".com") %}
```

+++

### est égal à {#equals}

Utilisez la fonction `equals` pour déterminer si une chaîne est égale à la chaîne spécifiée, en respectant la casse.

+++Syntaxe

```sql
{%= equals(STRING_1, STRING_2) %}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | La chaîne à comparer à la première chaîne. |

**Exemple**

La requête suivante détermine si le nom de la personne est `John` en respectant la casse.

```sql
{%=equals(profile.person.name,"John") %}
```

+++

### equalsIgnoreCase {#equalsIgnoreCase}

Utilisez la fonction `equalsIgnoreCase` pour déterminer si une chaîne est égale à la chaîne spécifiée, sans respect de la casse.

+++Syntaxe

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | La chaîne à comparer à la première chaîne. |

**Exemple**

La requête suivante détermine si le nom de la personne est `John` sans respect de la casse.

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

+++

### extractEmailDomain {#extractEmailDomain}

Utilisez la fonction `extractEmailDomain` pour extraire le domaine d&#39;une adresse e-mail.

+++Syntaxe

```sql
{%= extractEmailDomain(string) %}
```

**Exemple**

La requête suivante extrait le domaine de l&#39;adresse e-mail personnelle.

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

+++

### formatCurrency {#format-currency}

Utilisez la fonction `formatCurrency` pour convertir n’importe quel nombre en sa représentation monétaire sensible à la langue correspondante en fonction du paramètre régional transmis sous forme de chaîne dans le deuxième argument.

+++Syntaxe

```sql
{%= formatCurrency(number/double,string) %}: string
```

**Exemple**

Cette requête renvoie 56.00 £.

```sql
{%= formatCurrency(56L,"en_GB") %}
```

+++

### getUrlHost {#get-url-host}

Utilisez la fonction `getUrlHost` pour récupérer le nom d’hôte d’une URL.

+++Syntaxe

```sql
{%= getUrlHost(string) %}: string
```

**Exemple**

```sql
{%= getUrlHost("https://www.myurl.com/contact") %}
```

Renvoie « www.myurl.com »

+++

### getUrlPath {#get-url-path}

Utilisez la fonction `getUrlPath` pour récupérer le chemin d’accès d’après le nom de domaine d’une URL.

+++Syntaxe

```sql
{%= getUrlPath(string) %}: string
```

**Exemple**

```sql
{%= getUrlPath("https://www.myurl.com/contact.html") %}
```

Renvoie « /contact.html »

+++

### getUrlProtocol {#get-url-protocol}

Utilisez la fonction `getUrlProtocol` pour récupérer le protocole d’une URL.

+++Syntaxe

```sql
{%= getUrlProtocol(string) %}: string
```

**Exemple**

```sql
{%= getUrlProtocol("https://www.myurl.com/contact.html") %}
```

Renvoie « http »

+++

### indexOf {#index-of}

Utilisez la fonction `indexOf` pour renvoyer la position (dans le premier argument) de la première occurrence du deuxième paramètre. Renvoie -1 s’il n’existe aucune correspondance.

+++Syntaxe

```sql
{%= indexOf(STRING_1, STRING_2) %}: integer
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | Chaîne à rechercher dans le premier paramètre |

**Exemple**

```sql
{%= indexOf("hello world","world" ) %}
```

Renvoie 6.

+++

### isEmpty {#isEmpty}

Utilisez la fonction `isEmpty` pour déterminer si une chaîne est vide.

+++Syntaxe

```sql
{%= isEmpty(string) %}
```

**Exemple**

La fonction suivante renvoie &quot;true&quot; si le numéro de téléphone mobile du profil est vide. Sinon, elle renvoie `false`.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

+++

### isNotEmpty {#is-not-empty}

Utilisez la fonction `isNotEmpty` pour déterminer si une chaîne n’est pas vide.

+++Syntaxe

```sql
{= isNotEmpty(string) %}: boolean
```

**Exemple**

La fonction suivante renvoie &quot;true&quot; si le numéro de téléphone mobile du profil n’est pas vide. Sinon, elle renvoie `false`.

```sql
{%= isNotEmpty(profile.mobilePhone.number) %}
```

+++

### lastIndexOf {#last-index-of}

Utilisez la fonction `lastIndexOf` pour renvoyer la position (dans le premier argument) de la dernière occurrence du deuxième paramètre. Renvoie -1 s’il n’existe aucune correspondance.

+++Syntaxe

```sql
{= lastIndexOf(STRING_1, STRING_2) %}: integer
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | Chaîne à rechercher dans le premier paramètre |

**Exemple**

```sql
{%= lastIndexOf("hello world","o" ) %}
```

Renvoie 7.

+++

### leftTrim {#leftTrim}

Utilisez la fonction `leftTrim` pour supprimer les espaces blancs au début d’une chaîne.

+++Syntaxe

```sql
{%= leftTrim(string) %}
```

+++

### length {#length}

Utilisez la fonction `length` pour obtenir le nombre de caractères d&#39;une chaîne ou d&#39;une expression.

+++Syntaxe

```sql
{%= length(string) %}
```

**Exemple**

La fonction suivante renvoie la longueur du nom de ville du profil.

```sql
{%= length(profile.homeAddress.city) %}
```

+++

### J&#39;aime {#like}

Utilisez la fonction `like` pour déterminer si une chaîne correspond à un modèle donné.

+++Syntaxe

```sql
{%= like(STRING_1, STRING_2) %}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | L&#39;expression à laquelle comparer la première chaîne. Les deux caractères spéciaux pris en charge pour créer une expression sont `%` et `_`. <ul><li>`%` est utilisé pour représenter aucun ou plusieurs caractères.</li><li>`_` est utilisé pour représenter exactement un caractère.</li></ul> |

**Exemple**

La requête suivante récupère toutes les villes où vivent les profils contenant les `es` du modèle.

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

+++

### lowerCase {#lower}

Utilisez la fonction `lowerCase` pour convertir une chaîne en minuscules.

+++Syntaxe

```sql
{%= lowerCase(string) %}
```

**Exemple**

Cette fonction convertit le prénom du profil en minuscules.

```sql
{%= lowerCase(profile.person.name.firstName) %}
```

+++

### matches {#matches}

Utilisez la fonction `matches` pour déterminer si une chaîne correspond à une expression régulière spécifique. Pour plus d’informations sur les modèles correspondants dans les expressions régulières, consultez [documentation d’Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html).

+++Syntaxe

```sql
{%= matches(STRING_1, STRING_2) %}
```

**Exemple**

La requête suivante détermine si le nom de la personne commence par `John` sans respect de la casse.

```sql
{%= matches(person.name.,"(?i)^John") %}
```

+++

### masque {#mask}

Utilisez la fonction `mask` pour remplacer une partie d’une chaîne par des caractères « X ».

+++Syntaxe

```sql
{%= mask(string,integer,integer) %}
```

**Exemple**

La requête suivante remplace la chaîne « 123456789 » par des caractères « X », à l’exception des deux premiers et derniers caractères.

```sql
{%= mask("123456789",1,2) %}
```

La requête renvoie `1XXXXXX89`.

+++

### md5 {#md5}

Utilisez la fonction `md5` pour calculer et renvoyer le hachage md5 d’une chaîne.

+++Syntaxe

```sql
{%= md5(string) %}: string
```

**Exemple**

```sql
{%= md5("hello world") %}
```

Renvoie « 5eb63bbe01eeed093cb22bb8f5acdc3 »

+++

### notEqualTo {#notEqualTo}

Utilisez la fonction `notEqualTo` pour déterminer si une chaîne n’est pas égale à la chaîne spécifiée.

+++Syntaxe

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | La chaîne à comparer à la première chaîne. |

**Exemple**

La requête suivante détermine si le nom de la personne n’est pas `John` en respectant la casse.

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

+++

### notEqualWithIgnoreCase {#not-equal-with-ignore-case}

Utilisez la fonction `notEqualWithIgnoreCase` pour comparer deux chaînes qui ne respectent pas la casse.

+++Syntaxe

```sql
{= notEqualWithIgnoreCase(STRING_1,STRING_2) %}: boolean
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | La chaîne à comparer à la première chaîne. |

**Exemple**

La requête suivante détermine si le nom de la personne n’est pas `john`, sans respect de la casse.

```sql
{%= notEqualTo(profile.person.name,"john") %}
```

+++

### regexGroup {#regexGroup}

Utilisez la fonction `regexGroup` pour extraire des informations spécifiques en fonction de l&#39;expression régulière fournie.

+++Syntaxe

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING}` | La chaîne à vérifier. |
| `{EXPRESSION}` | L&#39;expression régulière avec laquelle comparer la première chaîne. |
| `{GROUP}` | Groupe d&#39;expressions à comparer. |

**Exemple**

La requête suivante extrait le nom de domaine d’une adresse e-mail.

```sql
{%= regexGroup(emailAddress,"@(\\w+)", 1) %}
```

+++

### replace {#replace}

Utilisez la fonction `replace` pour remplacer une sous-chaîne donnée dans une chaîne par une autre sous-chaîne.

+++Syntaxe

```sql
{%= replace(STRING_1,STRING_2,STRING_3) %}:string
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | Chaîne dans laquelle la sous-chaîne doit être remplacée. |
| `{STRING_2}` | Sous-chaîne à remplacer. |
| `{STRING_3}` | Sous-chaîne de remplacement. |

**Exemple**

```sql
{%= replace("Hello John, here is your monthly newsletter!","John","Mark") %}
```

Renvoie `Hello Mark, here is your monthly newsletter!`

+++

### replaceAll {#replaceAll}

Utilisez la fonction `replaceAll` pour remplacer toutes les sous-chaînes d’un texte correspondant à l’expression RegEx par la chaîne de remplacement littérale spécifiée. Les expressions régulières (RegEx) ont une gestion spéciale des `\` et des `+`, et toutes les expressions RegEx suivent la stratégie d’échappement PQL. Le remplacement s’effectue du début à la fin de la chaîne. Par exemple, le remplacement de `aa` par `b` dans la chaîne `aaa` entraîne une `ba` plutôt qu’une `ab`.

+++Syntaxe

```sql
{%= replaceAll(string,string,string) %}
```

>[!NOTE]
>
> Lorsque l’expression utilisée comme second argument est un caractère RegEx spécial, utilisez une double barre oblique inverse (`//`).  Les caractères RegEx spéciaux sont les suivants : [., +, *, ?, ^, $, (, ), [, ], {, }, |, \].
> 
> En savoir plus dans la [documentation Oracle](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html){_blank}.
>

+++

### rightTrim {#rightTrim}

La fonction `rightTrim` supprime les espaces blancs de la fin d&#39;une chaîne.

+++Syntaxe

```sql
{%= rightTrim(string) %}
```

+++

### sha256 {#sha256}

La fonction `sha256` calcule et renvoie le hachage sha256 d’une chaîne.

+++Syntaxe

```sql
{%= sha256(string) %} : string
```

**Exemple**

```sql
{%= sha256("Eliechxh")%}
```

Renvoie `0b0b207880b999adaad6231026abf87caa30760b6f326b21727b61139332257d`

+++

### split {#split}

Utilisez la fonction `split` pour fractionner une chaîne selon un caractère donné.

+++Syntaxe

```sql
{%= split(string,string) %}
```

+++

### startsWith {#startsWith}

Utilisez la fonction `startsWith` pour déterminer si une chaîne commence par une sous-chaîne donnée.

+++Syntaxe

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | La chaîne à rechercher dans la première chaîne. |
| `{CASE_SENSITIVE}` | Un paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Par défaut, elle est définie sur true. |

**Exemple**

La requête suivante détermine si le nom de la personne commence par `Joe` en respectant la casse.

```sql
{%= startsWith(person.name,"Joe") %}
```

+++

### stringToDate {#string-to-date}

La fonction `stringToDate` convertit une valeur de chaîne en valeur date / heure. Elle comporte deux arguments : représentation sous forme de chaîne d’une date et d’une heure et sous forme de chaîne du formateur.

+++Syntaxe

```sql
{= stringToDate("date-time value","formatter" %}
```

**Exemple**

```sql
{= stringToDate("2023-01-10 23:13:26", "yyyy-MM-dd HH:mm:ss") %}
```

+++

### string_to_integer {#string-to-integer}

Utilisez la fonction `string_to_integer` pour convertir une valeur de chaîne en valeur entière.

+++Syntaxe

```sql
{= string_to_integer(string) %}: int
```

+++

### stringToNumber {#string-to-number}

Utilisez la fonction `stringToNumber` pour convertir une chaîne en nombre. Elle renvoie la même chaîne que la sortie pour une entrée non valide.

+++Syntaxe

```sql
{%= stringToNumber(string) %}: double
```

+++

### substr {#sub-string}

Utilisez la fonction `substr` pour renvoyer la sous-chaîne de l’expression de chaîne entre l’index de début et l’index de fin.

+++Syntaxe

```sql
{= substr(string, integer, integer) %}: string
```

+++

### titleCase {#titleCase}

Utilisez la fonction `titleCase` pour mettre en majuscules les premières lettres de chaque mot d&#39;une chaîne.

+++Syntaxe

```sql
{%= titleCase(string) %}
```

**Exemple**

Si la personne vit dans Washington high street, cette fonction renvoie `Washington High Street`.

```sql
{%= titleCase(profile.person.location.Street) %}
```

+++

### toBool {#to-bool}

Utilisez la fonction `toBool` pour convertir une valeur d’argument en valeur booléenne, selon son type.

+++Syntaxe

```sql
{= toBool(string) %}: boolean
```

+++

### toDateTime {#to-date-time}

Utilisez la fonction `toDateTime` pour convertir une chaîne en date. Elle renvoie la date de l’époque comme sortie pour une entrée non valide.

+++Syntaxe

```sql
{%= toDateTime(string, string) %}: date-time
```

+++

### toDateTimeOnly {#to-date-time-only}

Utilisez la fonction `toDateTimeOnly` pour convertir une valeur d’argument en une valeur de date et d’heure uniquement. Elle renvoie la date de l’époque comme sortie pour une entrée non valide. Cette fonction accepte les types de champs chaîne, date, long et entier.

+++Syntaxe

```sql
{%= toDateTimeOnly(string/date/long/int) %}: date-time
```

+++

### trim {#trim}

La fonction `trim` supprime tous les espaces blancs du début et de la fin d&#39;une chaîne.

+++Syntaxe

```sql
{%= trim(string) %}
```

+++

### upperCase {#upper}

La fonction `upperCase` convertit une chaîne en majuscules.

+++Syntaxe

```sql
{%= upperCase(string) %}
```

**Exemple**

Cette fonction convertit le nom du profil en majuscules.

```sql
{%= upperCase(profile.person.name.lastName) %}
```

+++

### urlDecode {#url-decode}

Utilisez la fonction `urlDecode` pour décoder une chaîne codée en URL.

+++Syntaxe

```sql
{%= urlDecode(string) %}: string
```

+++

### urlEncode {#url-encode}

Utilisez la fonction `urlEncode` pour coder une chaîne en tant qu’URL.

+++Syntaxe

```sql
{%= urlEncode(string) %}: string
```

+++
