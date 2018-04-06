---
title: "Procédure de saisie de données dans les champs | Microsoft Docs"
description: "Il existe un grand nombre de fonctions générales qui vous permettent d’entrer des données de façon rapide et simple. Les fonctions générales d’entrée des données sont décrites dans cette rubrique."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/19/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 86e50b0fc2e07dd8598fe19883103b4a54c611a5
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---

# <a name="entering-data"></a>Saisie de données
Il existe un grand nombre de fonctions générales qui vous permettent d’entrer des données de façon rapide et simple. Les fonctions générales de saisie de données sont décrites dans cet article.  

Les exemples contenus dans cet article utilisent les données de démonstration.

## <a name="mandatory-fields"></a>Champs obligatoires
Lorsque vous entrez des données sur les pages, certains champs sont marqués par un astérisque rouge. L'astérisque rouge signifie que le champ doit être renseigné pour terminer un processus qui utilise ce champ, par exemple, valider une transaction qui utilise la valeur du champ.  

Même si le champ contient un astérisque rouge, vous n'êtes pas forcé de remplir le champ avant de poursuivre avec les autres champs ou fermer la page. L'astérisque rouge sert uniquement à rappeler que la fin d'un certain processus restera bloquée.  


## <a name="finding-data-as-you-type"></a>Recherche immédiate  
 Lorsque vous commencez à taper des caractères dans un champ, une liste déroulante affiche les valeurs de champ possibles. La liste change à mesure que vous tapez des caractères, et vous pouvez sélectionner la valeur correcte lorsqu'elle s'affiche.  

 De nombreux champs ont un bouton de Flèche vers le bas que vous pouvez choisir. sélectionnez la flèche pour obtenir la liste des données disponibles pour le champ. Selon le type de champ, le bouton peut être associé à l'une deux fonctions suivantes :  

-   Liste - Affiche les informations d'une autre table que vous pouvez entrer dans le champ. Vous pouvez sélectionner un élément à la fois.  

-   Consulter - Affiche les options qui existent pour le champ. Vous ne pouvez sélectionner qu'une des options.  

<!--Onprem ## Copy Fields or Lines  
 Depending on the type of writable document, you can copy individual line fields or whole lines to other lines in the document. Read-only data, such as posted entries, cannot be copied.  

 Several database dependencies are used to determine if fields or lines can be copied. One way to determine these dependencies is to view the shortcut menu. The content of the shortcut menu indicates which copy functions are supported by displaying either of these functions:  

-   Copy Cell  

-   Copy Rows  

-   Paste Rows  

 For example, database records, such as lines on a sales order, and master data, such as cards in the **Items** window, cannot be duplicated. For this kind of data, the shortcut menu typically has the **Copy Cell** or **Copy Rows**  functions. If the **Paste** function is not available this indicates that you can only paste the data into external documents. Single fields on a sales line, however, can be copied to the same column in other sales lines.  

 Journal lines are very flexible and can be copied freely in the same journal, indicated by the presence of **Paste** on the shortcut menu.  

> [!NOTE]  
>   If you copy a journal line or document line, the fields that are not in your view are not copied to the new line.

#### To copy previous field  

-   To enter the value of the field immediately above the active field, select **Copy Previous** from the shortcut menu.-->

## <a name="entering-quantities-by-calculation"></a>Saisie de quantités par calcul  
 Lors de la saisie de nombres dans les champs de quantité, tels que le champ **Quantité** d'une ligne feuille article, vous pouvez entrer la formule plutôt que la somme des quantités.  

## <a name="examples"></a>Exemples  

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
 Vous pouvez saisir deux, quatre, six ou huit chiffres dans un champ date :  

-   Si vous ne saisissez que deux chiffres, ils sont interprétés comme le jour, et le mois et l'année de la date de travail sont ajoutés.  

-   Si vous saisissez quatre chiffres, ils sont interprétés comme le jour et le mois, et l'année de la date de travail est ajoutée.  

-   Si la date que vous souhaitez saisir est comprise entre le 01/01/1930 et le 31/12/2029, vous pouvez saisir les deux chiffres de l'année ; sinon saisissez les quatre chiffres.  

 Vous pouvez aussi saisir une date sous forme de jour de la semaine suivi par un numéro de semaine et, éventuellement, une année (par exemple, Lun25 ou lun25 signifie le lundi de la semaine 25).  

 Au lieu de saisir une date spécifique, vous pouvez saisir l'un des deux codes suivants.  

|Code|Résultat|  
|--------------|----------------|  
|a|Il s'agit de la date du jour (la date système de l'ordinateur).|  
|t|Il s'agit de la date de travail configurée dans l'application. Pour modifier la date de travail, voir [Modification des paramètres de base](ui-change-basic-settings.md). Vous souhaiterez peut-être utiliser une date de travail si vous avez beaucoup de transactions avec une date différente de la date d'aujourd'hui.|  

<!--Onprem ## Closing Date  
 When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry. A closing date technically is between two dates, for example between Dec 31 and Jan 1.  

 To specify that a date is a closing date, put C just before the date: C123101. -->

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
|5:30:5,50|05:30:05,5|  
|053005050|05:30:05,05|  

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
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|  -->

## <a name="using-date-formulas"></a>Utilisation de formules date  
 Une formule date est une combinaison abrégée de lettres et de nombres qui spécifie comment calculer les dates. Vous pouvez entrer des formules date dans divers champs de calcul de date et dans les champs périodicité récurrente des feuilles récurrentes.  

> [!NOTE]  
>  Dans tous les champs formule de données, un jour est automatiquement inclus pour couvrir le jour de début de la période. Par conséquent, si vous saisissez 1s, par exemple, la période est bien huit jours parce que aujourd'hui est inclus. Pour définir une période de sept jours (une vraie semaine) avec la date début de la période, vous devez saisir 6D ou 1W-1D.  

 Voici quelques exemples d'utilisation de formules date :  

-   La formule date du champ périodicité récurrente des feuilles récurrentes détermine la fréquence de validation de l'écriture de la ligne feuille.  

-   La formule date du champ Période de carence pour un niveau de relance précis détermine la période qui doit se passer entre la date d'échéance (ou la date de la relance précédente) avant la création d'une nouvelle relance.  

-   La formule date du champ Calcul date échéance détermine la manière dont la date d'échéance de la relance est calculée.  

 La formule de calcul de la date peut comprendre un maximum de 20 caractères, des chiffres et des lettres. Vous pouvez utiliser les lettres suivantes qui sont des abréviations de spécifications de temps.  

|||  
|-|-|  
|C|Courant|  
|J|Jour(s)|  
|S|Semaine(s)|  
|M|Mois|  
|T|Trimestre(s)|  
|A|Année(s)|  

 Vous pouvez construire la formule date de trois manières.  

 L'exemple suivant indique comment définir un courant plus unité temporelle.  

|||  
|-|-|  
|CS|Semaine en cours|  
|CM|Mois en cours|  

 L'exemple suivant indique comment définir un chiffre et une unité de temps. Un chiffre ne peut pas être supérieur à 9999.  

|||  
|-|-|  
|10J|10 jours à dater d'aujourd'hui|  
|2S|2 semaines à dater d'aujourd'hui|  

 L'exemple suivant indique comment définir une unité de temps et un chiffre.  

|||  
|-|-|  
|J10|Le dixième jour du mois suivant|  
|JS4|Le quatrième jour de la semaine (jeudi)|  

 L'exemple suivant indique comment combiner ces trois formules.  

|||  
|-|-|  
|CM+10J|Mois en cours + 10 jours|  

 L'exemple ci-dessous illustre comment vous pouvez utiliser le signe moins pour indiquer une date du passé.  

|||  
|-|-|  
|-1A|Il y a 1 an à dater d'aujourd'hui|  

<!--OnPrem > [!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->  
## <a name="see-also"></a>Voir aussi  
 [Recherche, filtrage et tri de données](ui-enter-criteria-filters.md)  
 [Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

