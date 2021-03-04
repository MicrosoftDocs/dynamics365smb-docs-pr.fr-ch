---
title: Entrée des dates et des heures dans Business Central | Microsoft Docs
description: Apprendre comment entrer des dates et des heures avec diverses astuces de productivité telles que la sténographie, les expressions et les plages. Filtrez les listes ou les états à des dates ou périodes spécifiques.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter, calendar, shorthand, range
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 853a45dc32907c2d9b69f7b2e592dc164c20a094
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757382"
---
# <a name="working-with-calendar-dates-and-times"></a>Utilisation de dates civiles et les heures

[!INCLUDE[prod_short](includes/prod_long.md)] offre plusieurs méthodes principales de saisie des dates et des heures, y compris des fonctions puissantes qui accélèrent la saisie de données, ou vous permettent de saisir des expressions de calendrier complexes. Il existe différents emplacements tout au long de l’application où vous pouvez entrer des dates et des heures dans les champs. Par exemple, dans une commande client, vous pouvez également définir la date d’expédition. En filtrant les données de liste ou d’état, vous pouvez entrer des dates et des heures pour désigner uniquement les données que vous intéressent.

## <a name="check-your-region-and-language-settings"></a>Vérifiez les paramètres de zone et de langue
La page **Mes paramètres** spécifie la **Région** et la **Langue** que vous utilisez dans l’application. Ces paramètres ont une incidence sur la manière dont vous saisissez des dates et des heures.

-   Le paramètre **Région** détermine la manière dont les dates, heures, nombres et devises sont affichés ou mis en forme.

-   Pour des modèles de date qui impliquent des mots, la langue des mots utilisée doit correspondre au paramètre **Langue**.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_long.md)] utilise le système du calendrier grégorien.

<!--
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->

## <a name="entering-dates"></a>Saisie de dates

Dans un champ de date, vous pouvez saisir une date à l’aide du format standard pour votre paramètre de zone. Les différentes régions peuvent utiliser différents séparateurs entre les jours, mois et années. Par exemple, certaines régions utilisent les tirets (mm-jj-aaaa) et d’autres les barres obliques (mm/jj/aaaa). Cependant, vous pouvez utiliser tous les séparateurs, même un espace, et la date est modifiée automatiquement pour utiliser les séparateurs correspondant à votre région.

Notez que le format des dates affichées sur les états imprimés ou les documents envoyés par e-mail n’est pas influencé par votre choix personnel de paramètre d’une zone.

Pour travailler plus productivement avec des dates et des heures, vous pouvez utiliser les méthodes ou les formats décrits dans les sections suivantes.

### <a name="picking-dates-from-the-calendar"></a>Choisir des dates dans le calendrier

Tout champ affichant une icône de calendrier peut être paramétré à l’aide du sélecteur de date civile. Pour afficher le sélecteur de date civile, activer l’icône de calendrier ou appuyer sur le raccourci clavier Ctrl+Début dans le champ.

![Champs de date](media/ui-date-field.png "Exemple de champ de date")

Voir aussi [Raccourcis clavier du sélecteur de date civile](keyboard-shortcuts.md#calendarshortcuts).

### <a name="day-week-year-pattern"></a>Modèle jour\-semaine\-année

Vous pouvez saisir une date comme un jour de la semaine suivi d’un numéro de semaine et, éventuellement, une année. Par exemple, Lun25 ou lun25 signifie le lundi de la semaine 25. Si vous ne saisissez pas une année, l’année de la date de travail est utilisée.

Au lieu de saisir le mot entier du jour de la semaine, vous pouvez saisir une partie du mot, en commençant du début. Dans le cas de conflits (par exemple avec m qui peut être mardi ou mercredi), les jours sont évalués en fonction du paramètre d’une zone. L’entrée est d’abord évaluée par rapport à la date de travail et à la date du jour, ne l’oubliez pas en abrégeant. Par exemple, m signifie déjà maintenant, ce qui ne peut pas être mardi ou mercredi.

Le schéma de numéros de semaine est toujours ISO 8601, où la semaine 1 est la semaine avec le 4 janvier dans celle-ci, ou la semaine avec le premier jeudi de l’exercice.

### <a name="digit-patterns"></a>Modèles de chiffres

Vous pouvez saisir deux, quatre, six ou huit chiffres dans un champ date :

-   Si vous ne saisissez que deux chiffres, ils sont interprétés comme le jour, et le mois et l’année de la date de travail sont ajoutés.

-   Si vous saisissez quatre chiffres, ils sont interprétés comme le jour et le mois, et l’année de la date de travail est ajoutée. L’ordre du jour et du mois est déterminé par les paramètres de région. Même si vos paramètres de région ont l’année avant le jour et le mois, quatre chiffres sont interprétés en tant que jour et mois.

-   Si la date que vous souhaitez saisir est comprise entre le 01/01/1930 et le 31/12/2029, vous pouvez saisir les deux chiffres de l’année ; sinon saisissez les quatre chiffres.

### <a name="today"></a>Aujourd’hui

Entrez le mot pour aujourd’hui, dans la langue définie par le paramètre **Langue**, qui définit la date à la date actuelle. Au lieu de saisir le mot entier, vous pouvez saisir une partie du mot, en commençant par le début par exemple a ou auj, tant que ce n’est pas également le début d’un autre mot.

### <a name="period"></a>Période.

Pour filtrer une période comptable spécifique, dans un champ de date saisissez la lettre p, ou le mot période, suivi par un numéro qui identifie la période comptable, comme p2 ou période4. La période comptable est relative à l’exercice comptable de la date de travail en cours défini dans votre tableau de bord. Par exemple, si la date de travail est **21/03/20**, alors p1 ou simplement p filtre la première période comptable de l’exercice comptable 2020 (par exemple 01/01/20..31/01/20). p15 filtre la quinzième période comptable depuis le début de l’exercice comptable 2020 (par exemple 01/03/21..31/03/21).

Les périodes comptables sont définies sur la page **Périodes comptables**. Pour visualiser ou modifier les périodes comptables, ouvrez la page [ici](https://businesscentral.dynamics.com/?page=100).

### <a name="current-work-date"></a>Date de travail actuelle

La fonction de date de travail vous permet d’enregistrer des transactions en utilisant une date qui est différente de la date du jour.

Le mot « date de travail », dans la langue définie par le paramètre **Langue**, définit la date à laquelle la date de travail configurée actuellement est spécifiée sur la page **Mes paramètres**. Au lieu de saisir le mot entier, vous pouvez saisir une partie du mot, en commençant du début, comme "t" pour travail.

Si vous ne définissez pas de date de travail, la date actuelle sera utilisée comme date de travail. Vous souhaiterez peut-être utiliser une date de travail si vous avez beaucoup de transactions avec une date différente de la date d’aujourd’hui.

Voir aussi [Modifier les paramètres de base, comme la date de travail](ui-change-basic-settings.md#work-date).

### <a name="closing-date"></a>Date de clôture

Lorsque vous clôturez un exercice comptable, vous pouvez utiliser des dates de clôture pour indiquer qu’une écriture est une écriture de clôture. Techniquement, une date de clôture se trouve entre deux dates, par exemple le 31 décembre et le 1er janvier.

Pour spécifier qu’une date est une date de clôture, placez un C devant cette date, comme C123101. Ceci peut être utilisé avec tous les modèles de date.

### <a name="examples"></a>Exemples

Le tableau suivant affiche des exemples de dates à l’aide de tous les formats. Il considère les paramètres de région selon lesquels format les dates : **année.mois.jour.**, une semaine commençant lundi, et l’anglais.

|**Écriture**      |**Interprétation**      |
|---------------|------------------------|
|2018.12.31.|31/12/2018.|
|181231|31/12/2018.|
|18.12.31.|31/12/2018.|
|18.12.31.|31/12/2018.|
|20181231|31/12/2018.|
|18/12,31|31/12/2018.|
|11|11/mois date travail/année date travail.|
|1112|11/12/année date travail.|
|a ou date du jour|date du jour|
|p4|plage de dates qui comprend la quatrième la période comptable, par exemple 01/04/20..30/04/20|
|t ou date de travail|date de travail|
|lu ou lundi|Lundi de la semaine de date de travail|
|ma ou mardi|Mardi de la semaine de date de travail|
|sa ou samedi|Samedi de la semaine de date de travail|
|di ou dimanche|Dimanche de la semaine de date de travail|
|m23|Mardi de la semaine 23 de l’année de date de travail|
|m 23|Mardi de la semaine 23 de l’année de date de travail|
|m-1|Mardi de la semaine 1 de l’année de date de travail|

##  <a name="setting-ranges"></a><a name="BKMK_SettingDateRanges"></a> Définition des plages

Sous Listes, totaux et états, vous pouvez définir des filtres sur les dates, heures et dates/heures contenant une valeur de début et éventuellement une valeur de fin pour afficher uniquement les données contenues dans cette plage. Les règles standard s’appliquent à la définition des plages de dates.

|**Signification**|**Exemple d’expression (Date)**|**Données incluses dans le filtre**|
|-----------|---------------------|--------------------|
|Intervalle|15 12 00..15 01 01<br /><br />..15 12 00<br /><br />p1..p4|Enregistrements dont les dates sont comprises entre le 15/12/00 et le 15/01/01 inclusivement.<br /><br />Enregistrements dont les dates sont le 12/15/00 ou avant.<br /><br />Plage de dates qui comprend la deuxième, la troisième et la quatrième période comptable, par exemple 01/01/20..30/04/20.|
|Et/ou|12 15 00\|12 16 00|Enregistrement dont les dates sont le 15/12/00 ou 16/12/00. Si des enregistrements comportent des dates pendant ces deux jours, ils sont tous affichés.|
|Combinaison|12 15 00\|12 01 00..12 10 00  <br /><br />..12 14 00\|12 30 00..|Enregistrements avec pour dates le 15/12/00 ou entre le 01/12/00 et le 10/12/00 inclus.  <br /><br />Enregistrements avec dates le 14/12/00 ou avant, ou le 30/12/00 ou après, c’est-à-dire tous les enregistrements exceptés ceux avec des dates comprises entre le 15/12/00 et le 29/12/00 inclusivement.|

Vous pouvez utiliser l’un des formats valides dans les filtres Plage de dates. Par exemple, lun14 3..t 4p appliqué pour un champ Date/heure débouche sur un filtre à partir de 3h du matin le lundi de la semaine 14 de l’année de date de travail en cours, incluse, jusqu’à aujourd’hui à 16h, inclus.

## <a name="using-date-formulas"></a>Utilisation de formules date
Une formule date est une combinaison abrégée de lettres et de nombres qui spécifie comment calculer les dates. Vous pouvez entrer des formules date dans différents champs ou filtres de calcul de date.

> [!NOTE]
>  Dans tous les champs formule de données, un jour est automatiquement inclus pour couvrir le jour de début de la période. Par conséquent, si vous saisissez 1S, par exemple, la période est bien huit jours parce qu’aujourd’hui est inclus. Pour définir une période de sept jours \(une vraie semaine\) avec la date début de la période, vous devez saisir 6J ou 1S-1J.

Voici quelques exemples d’utilisation de formules date :

-   La formule date du champ périodicité récurrente des feuilles récurrentes détermine la fréquence de validation de l’écriture de la ligne feuille.

-   La formule date du champ **Période de carence** pour un niveau de relance précis détermine la période qui doit se passer entre la date d’échéance \(ou la date de la relance précédente\) avant la création d’une nouvelle relance.

-   La formule date du champ **Calcul date échéance** détermine la manière dont la date d’échéance de la relance est calculée.

La formule de la date peut comprendre un maximum de 20 caractères, des chiffres et des lettres. Vous pouvez utiliser les lettres suivantes qui sont des abréviations d’unités de calendrier.

|  Lettre  |  Signification  |
|----------|----------------------|
|A|Actuellement|
|J|Jour\(s\)|
|S|Week\(s\) (Semaines)|
|M|Mois\(s\)|
|T|Trimestre\(s\)|
|A|Année\(s\)|

Vous pouvez construire la formule date de trois manières.

L’exemple suivant indique comment utiliser C pour en cours et une unité temporelle.

|  Expression  |  Signification  |
|--------------|-----------|
|CS|Semaine en cours|
|MC|Mois en cours|

L’exemple suivant indique comment utiliser un chiffre et une unité de temps. Un chiffre ne peut pas être supérieur à 9999.

|  Expression  |  Signification  |
|--------------|-----------|
|10J|10 jours à dater d’aujourd’hui|
|2S|2 semaines à dater d’aujourd’hui|

L’exemple suivant indique comment utiliser une unité de temps et un chiffre.

|  Expression  |  Signification  |
|--------------|-----------|
|J10|Le dixième jour du mois suivant|
|JS4|Le quatrième jour de la semaine \(jeudi\)|

L’exemple suivant indique comment combiner ces trois formules.

|  Expression  |  Signification  |
|--------------|-----------|
|MC+10J|Mois en cours \+ 10 jours|

L’exemple ci-dessous illustre comment vous pouvez utiliser le signe moins pour indiquer une date du passé.

|  Expression  |  Signification  |
|--------------|-----------|
|-1A|Il y a 1 an à dater d’aujourd’hui|

> [!IMPORTANT]
>  Si le magasin utilise un calendrier principal, la formule de date que vous entrez par exemple le champ **Délai d’expédition**, est interprétée en fonction des jours ouvrés du calendrier. Par exemple, 1S un signifie sept jours ouvrés.
<!--
# Entering Date Ranges
You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges. Let's take the **Customer Top 10** as an example:

![Setting a date range in the request page for the Customer Top 10 list](./media/ui-enter-date-ranges/customer-top10-list.png)

Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want. To set date ranges, you enter dates and then use either **..** or **|** to set the range. In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.
Here are a couple of other examples:

| Meaning | Example | Entries included |
|---|---|---|
|Equal to| 12 15 16 |Only those posted on December 15 2016.|
|Interval| 12 15 16..01 15 17<br /><br />..12 15 16|Those posted on dates between and including December 15 2016 and January 15 2017.<br /><br />Those posted on December 15 2016 or earlier.|
|Either/or|12 15 16&#124;12 16 16|Those posted on either December 15 or December 16 2016. If there are entries posted on both days, they will all be displayed.|

You can also combine the various format types.

| Example | Entries included |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017. |
|..12 14 16&#124;12 30 16.. | Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29. |

Note that we have used the US date format MMDDYY here. As [!INCLUDE[prod_short](includes/prod_short.md)] becomes available in other markets, you'll be able to use the formats that you are used to.

## Using Date Formulas
A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.

> [!NOTE]
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.

Here are some examples of how date formulas can be used:

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.

-   The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.

-   The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.

The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.

|  Letter  |  Time specification  |
|----------|----------------------|
|C|Current|
|D|Day\(s\)|
|W|Week\(s\)|
|M|Month\(s\)|
|Q|Quarter\(s\)|
|Y|Year\(s\)|

You can construct a date formula in three ways.

The following example shows how to use **C**, for current, and a time unit.

|  Expression  |  Meaning  |
|--------------|-----------|
|CW|Current week|
|CM|Current month|

The following example shows how to use a number and a time unit. A number cannot be larger than 9999.

|  Expression  |  Meaning  |
|--------------|-----------|
|10D|10 days from today|
|2W|2 weeks from today|

The following example shows how to use a time unit and a number.

|  Expression  |  Meaning  |
|--------------|-----------|
|D10|The next 10th day of a month|
|WD4|The next 4th day of a week \(Thursday\)|

The following example shows how you can combine these three forms as needed.

|  Expression  |  Meaning  |
|--------------|-----------|
|CM\+10D|Current month \+ 10 days|

The following example shows how you can use a minus sign to indicate a date in the past.

|  Expression  |  Meaning  |
|--------------|-----------|
|-1Y|1 year ago from today|

> [!IMPORTANT]
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, **1W**  means seven working days.

-->

## <a name="entering-times"></a>Saisie des heures
Lorsque vous saisissez des heures, vous pouvez insérer n’importe quel type de séparateur entre les unités, mais si vous utilisez des chiffres doubles pour chaque unité jusqu’aux millisecondes, ce n’est pas requis.

Vous n’avez qu’à entrer les plus grandes unités souhaitées ; les autres sont remis à zéro. Vous pouvez également omettre l’indicateur AM/PM.

Le tableau suivant répertorie les différents formats de saisie possibles pour les heures, ainsi que leur interprétation. Il considère les paramètres de zone qui formatent les périodes : **Heures:Minutes:Secondes.Millisecondes.** et utilisent les indicateurs AM et PM « AM » et « PM », respectivement.

|**Écriture**      |**Interprétation**      |
|---------------|------------------------|
|05:23:17|05:23:17|
|5|05:00:00|
|5AM|05:00:00|
|5P|17:00:00|
|12|12:00:00|
|12A|00:00:00|
|12P|12:00:00|
|17|17:00:00|
|5:30|05:30:00|
|0530|05:30:00|
|5:30:5|05:30:05|
|053005|05:30:05|
|5:30:5,50|05:30:05.5|
|053005050|05:30:05.05|

Tenez compte que les millisecondes sont interprétées comme des notations de décimales. Ainsi, par exemple 3, 30 et 300 signifient tous 300 millisecondes, alors que 03 signifie 30 et 003 signifie 3 millisecondes.

Vous ne pouvez pas utiliser 24:00 pour dire minuit, ou utiliser une valeur supérieure à 24:00.

Le mot pour « time » (heure) dans la langue utilisée par [!INCLUDE[prod_short](includes/prod_long.md)] est évalué sur l’heure actuelle sur votre ordinateur ou appareil mobile. Vous pouvez saisir n’importe quel partie du mot, en commençant au début, par exemple h ou HEU.

## <a name="entering-combined-dates-and-times"></a>Saisie de dates et d’heures combinées
Lorsque vous saisissez les dates/heures, qui sont une date et heure combinées en un champ, vous devez saisir un espace entre la date et l’heure. La partie de la date ne peut contenir des espaces sous forme de séparateur de date officiel de vos paramètres de région. L’heure peut contenir des espaces autour de l’indicateur AM/PM.

Il est également possible de saisir qu’une date dans un champ Date/heure, mais il n’est pas possible d’entrer seulement une heure.

Le tableau suivant répertorie quelques exemples de combinaisons Date/heure. Les paramètres de région dans les exemples affichent les dates au format jour\-mois\-année, en utilisant les indicateurs AM/PM, l’anglais, et le dimanche comme début de la semaine.

|**Écriture**      |**Interprétation**      |
|---------------|------------------------|
|08-01-2016 05:48:12 PM|08/01/2016 17:48:12|
|131202 132455|13/12/2002 13:24:55|
|1-12-02 10|01/12/2002 10:00:00|
|1.12.02 5|01/12/2002 05:00:00|
|1.12.02|01/12/2002 00:00:00|
|11 12|11/mois date de travail/année date de travail 12:00:00|
|1112 12|11/12/année date de travail 12:00:00|
|a ou date du jour|date du jour 00:00:00|
|a 10:30|date du jour 10:30:00|
|a 3:3:3|date du jour 03:03:03|
|t ou date de travail|date de travail 00:00:00|
|lu ou lundi|Lundi de la semaine de date de travail 00:00:00|
|ma ou mardi|Mardi de la semaine de date de travail 00:00:00|
|sa ou samedi|Samedi de la semaine de date de travail 00:00:00|
|di ou dimanche|Dimanche de la semaine de date de travail 00:00:00|
|ma 10:30|Mardi de la semaine de date de travail 10:30:00|
|ma 3:3:3|Mardi de la semaine de date de travail 03:03:03|
|m23 a|Mardi de la semaine 23 de l’année de date de travail, heure actuelle|
|m23|Mardi de la semaine 23 de l’année de date de travail|
|m 23|Aujourd’hui 23:00:00|
|m-1|Mardi de la semaine 1 de l’année de date de travail|

## <a name="entering-duration"></a>Saisie des durées
Certains champs de l’application représentent une durée, ou la quantité de temps écoulé, au lieu d’une date ou d’une heure spécifique. Vous devez saisir les durées sous la forme d’un chiffre suivi d’une unité de mesure.

Voilà quelques exemples.

|**Durée**|**Unité**|
|------------|-------------------|
|2h|2 heures|
|6h 30m|6 heures 30 minutes|
|6,5h|6 heures 30 minutes|
|90m|1 heure 30 minutes|
|2j 6h 30m|2 jours 6 heures 30 minutes|
|2j 6h 30m 56s 600ms|2 jours 6 h 30 m 56 s 600 ms|

Vous pouvez également saisir un nombre automatiquement converti en durée. Le nombre saisi est converti en fonction de l’unité de mesure par défaut spécifiée pour le champ de durée.

Pour connaître l’unité de mesure utilisée pour un champ de durée, saisissez un nombre et observez l’unité de mesure dans laquelle il est convertit.

Par exemple, si l’unité est « heures », le chiffre 5 est converti en 5 h.

## <a name="see-also"></a>Voir aussi
[Utilisation de [!INCLUDE[prod_short](includes/prod_long.md)]](ui-work-product.md)  
[Calcul de la date des achats](purchasing-date-calculation-for-purchases.md)  
[Saisir les critères pour les filtres](ui-enter-criteria-filters.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]