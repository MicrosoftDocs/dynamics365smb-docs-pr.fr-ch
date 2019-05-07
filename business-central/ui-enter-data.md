---
title: Procédure de saisie de données dans les champs | Microsoft Docs
description: En savoir plus sur les fonctions générales qui vous permettent de saisir les données dans les champs.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 00143454cf0b0da9b111f92bcdb7879c7e6743d2
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "929088"
---
# <a name="entering-data"></a>Saisie de données

Plusieurs fonctions générales vous permettent de saisir vos données de manière plus facile, rapide et précise. Les fonctions générales de saisie de données sont décrites dans cet article.  

<!-- The examples in this article use the demonstration data.-->

## <a name="keyboard-shortcuts"></a>Raccourcis clavier

Plusieurs raccourcis clavier vous permettent de travailler sans la souris, et d'accélérer la saisie de vos données, notamment avec des saisies à grande échelle et des tâches de saisie répétitives.

Pour plus d'informations sur les raccourcis, reportez-vous à la rubrique [Raccourcis clavier](keyboard-shortcuts.md). Certains raccourcis font l'objet de cet article.

## <a name="QuickEntry"></a>Accélérer la saisie de données à l'aide de la fonction Saisie rapide

La saisie rapide est une fonction conçue pour saisir les données avec le clavier. La fonction Saisie rapide fonctionne sur les champs (comme les pages Fiche) et dans les listes (lignes et colonnes). Cela est utile lors de l'exécution de tâches de saisie répétitives qui exigent de créer plusieurs enregistrements dans la séquence, comme un lot de commandes vente ou l'enregistrement de nouveaux articles.

Vous connaissez peut-être déjà l'utilisation de la touche Tab afin de naviguer d'un champ sur une page au champ suivant modifiable. L'inconvénient de l'utilisation de la touche Tab ? Elle passe toujours de façon séquentielle au champ suivant. <!-- even if the field is non-editable or seldom filled it in.-->La fonction Saisie rapide vous permet de modifier ce chemin d'accès. Avec la Saisie rapide, utilisez la touche Entrée pour naviguer uniquement à travers ces champs qui vous intéressent, en ignorant les champs non modifiables et les champs que vous ne renseignez généralement pas. Vous avez peut-être déjà remarqué ce comportement sur certaines pages. En effet, l'application désigne déjà quels champs inclure lors de l'activation de la touche Entrée et lesquels ignorer. Vous pouvez personnaliser la fonction Saisie rapide en personnalisant votre espace de travail et en optimisant la manière dont vous saisissez les données sur chaque page.

### <a name="how-quick-entry-works"></a>Fonction Saisie rapide : fonctionnement

Chaque champ peut être marqué comme *inclus dans la Saisie rapide* ou *exclus de la Saisie rapide*. Les champs inclus dans la Saisie rapide seront inclus dans le chemin d'accès lorsque vous appuyez sur la touche Entrée ; les champs exclus de la fonction Saisie rapide, ne le seront pas.

Lorsque vous avez fini de saisir les données dans un champ, appuyez simplement sur Entrée pour confirmer les changements et accéder au champ suivant. Si vous souhaitez inverser le sens, et accéder au champ précédent, appuyez sur Maj+Entrée. Pour plus d'informations sur les raccourcis, reportez-vous à [Raccourcis clavier Saisie rapide](keyboard-shortcuts.md#QuickEntry).

#### <a name="tips-and-tricks"></a>Conseils et astuces
Vous trouverez ci-après les informations utiles concernant la fonction Saisie rapide.

- Elle est disponible pour tout champ modifiable.
- Elle fonctionne également à travers les colonnes et les lignes.
- Elle n'empêche pas d'accéder à d'autres éléments d'une page, comme des actions. Ceux-ci restent accessibles en utilisant la touche Tab et la combinaison des touches Maj+Tab.  
- Les raccourcis ne doivent pas être développés pour le bon fonctionnement de Saisie rapide. Si le champ suivant Saisie rapide se situe dans un raccourci réduit, ce raccourci développe automatiquement et se concentre sur le champ désigné.
- La fonction Saisie rapide fonctionne peut importe si les champs sont obligatoires ou non. Ainsi, il est recommandé de veiller à ce que les champs obligatoires soient inclus dans la fonction Saisie rapide.
- Par défaut, la plupart des champs sont automatiquement inclus dans la fonction Saisie rapide. Ainsi, à la base, il est fort probable que votre tâche exclura les champs de la fonction Saisie rapide.

### <a name="how-to-change-quick-entry-fields"></a>Comment modifier les champs de saisie rapide

Pour modifier quels champs sont inclus ou exclus de la Saisie rapide sur une page, utilisez la personnalisation.

1. Commencez la personnalisation en sélectionnant l'icône ![Paramètres](media/ui-experience/settings_icon_small.png "Icône Paramètres du tableau de bord"), puis sélectionnez **Personnaliser**.
2. Sélectionnez un champ que vous souhaitez modifier, ou dans des listes, sélectionnez l'en-tête de colonne correspondante, puis choisissez **Inclure dans la saisie rapide** ou **Exclure de la saisie rapide**.

Pour plus d'informations sur la personnalisation, voir [Personnalisation de votre espace de travail et des pages](ui-personalization-user.md).

## <a name="mandatory-fields"></a>Champs obligatoires

Lorsque vous entrez des données sur les pages, certains champs sont marqués par un astérisque rouge. L'astérisque rouge signifie que le champ doit être renseigné pour terminer un processus qui utilise ce champ, par exemple, valider une transaction qui utilise la valeur du champ.  

Même si le champ contient un astérisque rouge, vous n'êtes pas forcé de remplir le champ avant de poursuivre avec les autres champs ou fermer la page. L'astérisque rouge sert uniquement à rappeler que la fin d'un certain processus restera bloquée.  

## <a name="finding-data-as-you-type"></a>Recherche immédiate

 Lorsque vous commencez à taper des caractères dans un champ, une liste déroulante affiche les valeurs de champ possibles. La liste change à mesure que vous tapez des caractères, et vous pouvez sélectionner la valeur correcte lorsqu'elle s'affiche.  

 De nombreux champs ont un bouton de Flèche vers le bas que vous pouvez choisir. sélectionnez la flèche pour obtenir la liste des données disponibles pour le champ. Selon le type de champ, le bouton peut être associé à l'une deux fonctions suivantes :  

-   Liste - Affiche les informations d'une autre table que vous pouvez entrer dans le champ. Vous pouvez sélectionner un élément à la fois.  

-   Consulter - Affiche les options qui existent pour le champ. Vous ne pouvez sélectionner qu'une des options.  

## <a name="copying-and-pasting-fields-and-lines"></a>Copier et coller des champs et des lignes

Vous pouvez copier une ou plusieurs lignes dans une liste ou un champ unique sur une page, puis collez ce que vous avez copié dans la même page, une autre page, ou un document externe (comme Microsoft Excel et un e-mail Outlook). En raccourci, pour copier, appuyez sur CTRL+C (cmd+C dans macOS) sur votre clavier. Pour coller, appuyez sur CTRL+V (cmd+V dans macOS).

Dans une liste, pour copier le champ dans la même colonne de la ligne précédente, et le coller dans la ligne actuelle, il vous suffit d'appuyer sur F8.

Pour plus d'informations, reportez-vous à la rubrique [Copier et coller dans Business Central](ui-copy-paste.md).

## <a name="Focus"></a>Se concentrer sur les articles de ligne

Lorsque vous travaillez sur des documents qui comprennent une pièce des articles de ligne, comme une page de commande vente ou de facture, vous pouvez basculer votre vue pour vous concentrer uniquement sur les articles de ligne, notamment en développant la pièce des articles de ligne de telle sorte qu'elle occupe la plupart de l'espace de travail, masquant les autres parties de la page, hormis la zone des actions en haut. Cela vous donne un meilleur aperçu des articles de ligne et offre un plus grand espace pour les exploiter. Cela est particulièrement utile lorsque vous utilisez de grandes listes d'articles de ligne et lorsque la saisie rapide des données est souhaitée.

Un autre avantage est que cela vous offre une fonctionnalité de filtre avancée, comme sur les autres listes, afin que la navigation et la recherche à travers les articles de ligne soient plus simples.

### <a name="switch-the-focus-on-and-off"></a>Activer/Désactiver le focus

Pour vous concentrer sur les articles de ligne, faites votre sélection n'importe où dans la partie des articles de ligne, puis sélectionnez ![icône mode Focalisation](media/focus-mode.png "icône mode Focalisation") dans l'angle supérieur droit ou appuyez sur Ctrl+Maj+F12.

Pour revenir à la vue normale, sélectionnez ![icône mode Focalisation](media/focus-mode.png "icône mode Focalisation") ou appuyez à nouveau sur Ctrl+Maj+F12.

### <a name="filtering-the-line-items"></a>Filtrage des articles de ligne

Pour commencer à filtrer, sélectionnez ![icône de volet Filtre](media/open-filter-pane-icon.png "icône de volet Filtre") en haut de la liste ou appuyez sur **Maj+F3** pour ouvrir le volet Filtrer. Vous travaillez avec le volet Filtrer comme vous le faites sur toute autre liste. Pour plus d'informations, reportez-vous à la rubrique [Filtrage](ui-enter-criteria-filters.md#Filtering).

La fonction Filtrage est utile notamment pour afficher et analyser de longs documents. Par exemple, supposez que vous ouvriez une facture de vente validée et que vous filtriez les articles de ligne pour afficher tous les articles de ligne qui ont une remise individuelle supérieure à 5 % ou que vous filtriez uniquement pour afficher les accessoires de vélo comportant la mention « pro » dans leur nom.

## <a name="entering-quantities-by-calculation"></a>Saisie de quantités par calcul

Lors de la saisie de nombres dans les champs de quantité, tels que le champ **Quantité** d'une ligne feuille article, vous pouvez entrer la formule plutôt que la somme des quantités.  

### <a name="examples"></a>Exemples  

-   Si vous entrez 19+19, le champ est renseigné à l'aide du nombre 38.  

-   Si vous entrez 41-9, le champ est renseigné à l'aide du nombre 32.  

-   Si vous entrez 12*4, le champ est renseigné à l'aide du nombre 48.  

-   Si vous entrez 12/4, le champ est renseigné à l'aide du nombre 3.  

## <a name="entering-negative-numbers"></a>Saisie de chiffres négatifs

Vous pouvez saisir des chiffres négatifs de deux manières. Le numéro -20,5 peut être saisi de la manière suivante :  

-   -20,5  

    Ou
-   20,5-  

 Dans les deux cas, le montant est enregistré comme -20,5.  

 Si le dernier caractère de l'expression est **+** ou **-**, l'expression entière est enregistrée avec ce caractère. Par exemple, **10-20+** aboutira à 10 et non -10.  

## <a name="entering-dates-and-times"></a>Saisie de dates et d'heures

Vous pouvez entrer des dates et des heures dans tous les champs affectés spécifiquement à des dates (champs Date). Vous pouvez saisir les dates avec ou sans séparateurs.

> [!NOTE]  
> Le mode de saisie des dates et heures dépend des paramètres **Région**. Pour plus d'informations, voir [Modification des paramètres de base](ui-change-basic-settings.md).  

### <a name="entering-dates"></a>Saisie de dates

Pour les champs de date, vous pouvez utiliser le sélecteur de date, qui vous permet de choisir une date depuis un calendrier, ou vous pouvez saisir les dates manuellement. Cette section offre un bref aperçu de la manière de saisir les dates. Pour plus d'informations, reportez-vous à la rubrique [Utilisation de dates civiles et les heures](ui-enter-date-ranges.md).

Pour la saisie manuelle de la date, saisissez deux, quatre, six ou huit chiffres :  

-   Si vous ne saisissez que deux chiffres, ils sont interprétés comme le jour, et le mois et l'année de la date de travail sont ajoutés.  

-   Si vous saisissez quatre chiffres, ils sont interprétés comme le jour et le mois, et l'année de la date de travail est ajoutée.  

-   Si la date que vous souhaitez saisir est comprise entre le 01/01/1930 et le 31/12/2029, vous pouvez saisir les deux chiffres de l'année ; sinon saisissez les quatre chiffres.  

Vous pouvez aussi saisir une date sous forme de jour de la semaine suivi par un numéro de semaine et, éventuellement, une année (par exemple, Lun25 ou lun25 signifie le lundi de la semaine 25).  

Plutôt que de saisir une date spécifique, vous pouvez saisir l'un de ces codes.  

|Code|Résultat|  
|--------------|----------------|  
|a|Il s'agit de la date du jour (la date système de l'ordinateur).|  
|p|Cela précise une période comptable où `p`signifie la première période comptable, `p2` indique la seconde période comptable, etc. |
|t|Il s'agit de la date de travail configurée dans l'application. Pour modifier la date de travail, voir [Modification des paramètres de base](ui-change-basic-settings.md). Vous souhaiterez peut-être utiliser une date de travail si vous avez beaucoup de transactions avec une date différente de la date d'aujourd'hui.|
|c|Cela spécifie que la date après `c`est une date de clôture, par exemple `C123101`.|  

## <a name="entering-times"></a>Saisie des heures

Lorsque vous saisissez des heures, vous pouvez insérer n'importe quel type de séparateur entre les unités, mais cette opération est facultative. Vous n'avez pas besoin d'ajouter la mention « minutes », « secondes » ou « AM/PM ».  

Le tableau suivant répertorie les différents formats de saisie possibles pour les heures, ainsi que leur interprétation.  

|Écriture|Interprétation|  
|---------------|------------------------|  
|5|05:00:00|  
|5:30|05:30:00|  
|0530|05:30:00|  
|5:30:5|05:30:05|  
|053005|05:30:05|  
|5:30:5,50|05:30:05.5|  
|053005050|05:30:05.05|  

 Vous devez saisir deux chiffres par unité temporelle si vous n'utilisez pas de séparateur.  

## <a name="entering-datetimes"></a>Saisie des dates/heures

Lors de la saisie des dates/heures, vous devez saisir un espace entre la date et l'heure.  

Le tableau suivant répertorie les différents formats de saisie possibles pour les dates/heures, ainsi que leur interprétation.  

|Écriture|Interprétation|  
|---------------|------------------------|  
|131202 132455|13-12-02 13:24:55|  
|1-12-02 10|01-12-02 10:00:00|  
|1.12.02 5|01/12/02 05:00:00|  
|1.12.02|01/12/02 00:00:00|  
|11/12|11-mois en cours-année en cours 12:00:00|  
|1112 12|11-12-année en cours 12:00:00|  
|a ou date du jour|date du jour 00:00:00|  
|heure h|date du jour heure réelle|  
|a 10:30|date du jour 10:30:00|  
|a 3:3:3|date du jour 03:03:03|  
|t ou date de travail|date de travail 00:00:00|  
|lu ou lundi|Lundi de la semaine en cours 00:00:00|  
|ma ou mardi|Mardi de la semaine en cours 00:00:00|  
|me ou mercredi|Mercredi de la semaine en cours 00:00:00|  
|je ou jeudi|Jeudi de la semaine en cours 00:00:00|  
|ve ou vendredi|Vendredi de la semaine en cours 00:00:00|  
|sa ou samedi|Samedi de la semaine en cours 00:00:00|  
|di ou dimanche|Dimanche de la semaine en cours 00:00:00|  
|ma 10:30|Mardi de la semaine en cours 10:30:00|  
|ma 3:3:3|Mardi de la semaine en cours 03:03:03|  

## <a name="entering-duration"></a>Saisie des durées

Vous devez saisir les durées sous la forme d'un chiffre suivi d'une unité de mesure.  

Voilà quelques exemples.  

|Durée|Unité**|  
|------------------|-------------------------|  
|2h|2 heures|  
|6h 30m|6 heures 30 minutes|  
|6,5h|6 heures 30 minutes|  
|90m|1 heure 30 minutes|  
|2j 6h 30m|2 jours 6 heures 30 minutes|  
|2j 6h 30m 56s 600ms|2 jours 6 h 30 m 56 s 600 ms|  

 Vous pouvez également saisir un nombre automatiquement converti en durée. Le nombre saisi est converti en fonction de l'unité de mesure par défaut spécifiée pour le champ de durée.  

 Pour connaître l'unité de mesure utilisée pour un champ de durée, saisissez un nombre et observez l'unité de mesure dans laquelle il est convertit.  

 Si l'unité est « heures », 5 est converti en 5h.  

<!--OnPrem  ##  <a name="BKMK_SettingDateRanges"></a> Setting Date Ranges  
 You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges.  

|**Meaning**|**Sample expression**|**Entries included**|  
|-----------------|---------------------------|--------------------------|  
|**Equal to**|12 15 00|Only those posted on 12 15 00.|  
|**Interval**|12 15 00..01 15 01<br /><br /> ..12 15 00|Those posted on dates between and including 12 15 00 and 01 15 01.<br /><br /> Those posted on 12 15 00 or earlier.|  
|**Either/or**|12 15 00&#124;12 16 00|Those posted on either 12 15 00 or 12 16 00. If there are entries posted on both days, they will all be displayed.|  

 You can also combine the various format types.  

|**Sample expression**|**Entries included**|  
|---------------------------|--------------------------|  
|12 15 00&#124;12 01 00..12 10 00|Entries posted either on 12 15 00 or on dates between and including 12 01 00 and 12 10 00.|  
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|

## Using Date Formulas

 A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.  

> [!NOTE]  
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, if you enter 1W, for example, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter 6D or 1W-1D.  

 Here are some examples of how date formulas can be used:  

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.  

-   The date formula in the Grace Period field for a specified reminder level determines the period of time that must pass from the due date (or from the date of the previous reminder) before a reminder will be created.  

-   The date formula in the Due Date Calculation field determines how to calculate the due date on the reminder.  

 The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.  

|||  
|-|-|  
|C|Current|  
|D|Day(s)|  
|W|Week(s)|  
|M|Month(s)|  
|Q|Quarter(s)|  
|Y|Year(s)|  

 You can construct a date formula in three ways.  

 The following example shows how current plus a time unit.  

|||  
|-|-|  
|CW|Current week|  
|CM|Current month|  

 The following example shows how a number and a time unit. A number cannot be larger than 9999.  

|||  
|-|-|  
|10D|10 days from today|  
|2W|2 weeks from today|  

 The following example shows how a time unit and a number.  

|||  
|-|-|  
|D10|The next 10th day of a month|  
|WD4|The next 4th day of a week (Thursday)|  

 The following example shows how you can combine these three forms as needed.  

|||  
|-|-|  
|CM+10D|Current month + 10 days|  

 The following example shows how you can use a minus sign to indicate a date in the past.  

|||  
|-|-|  
|-1Y|1 year ago from today|

[!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->

## <a name="see-also"></a>Voir aussi  
 [Tri, recherche et filtrage de listes](ui-enter-criteria-filters.md)  
 [Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
