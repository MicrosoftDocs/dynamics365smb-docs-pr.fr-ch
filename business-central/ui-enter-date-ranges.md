---
title: "Définition des plages de dates dans Business Central | Microsoft Docs"
description: "En savoir plus pour obtenir un état affichant les données de périodes spécifiques à l'aide de plages de dates dans Business Central."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 07/05/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7664360941313da6ea0b797ef00df2e9810ad62
ms.openlocfilehash: ff63ae71a78f956dddb7b5247ee66f9416cf7cf1
ms.contentlocale: fr-ch
ms.lasthandoff: 07/09/2018

---
# <a name="entering-date-ranges"></a>Saisie de plages de dates
Vous pouvez définir des filtres contenant une date de début et une date de fin pour afficher uniquement les données contenues dans cette plage de données ou cet intervalle de temps. Des règles spéciales s'appliquent à la définition des plages de dates. Prenons par exemple **Palmarès des clients** :

![Définition d'une plage de dates dans la page de demande de la liste du palmarès des clients](./media/ui-enter-date-ranges/customer-top10-list.png)

Vous pouvez limiter ici l'état à une plage de dates telles que les 2 dernières semaines, ou un total de 6 semaines, ou toute plage de votre choix. Pour définir les plages de dates, vous entrez des dates puis utilisez **..** ou **|** pour définir la plage. Dans notre exemple, pour afficher les 10 clients principaux des deux premières semaines de mai, vous devez définir le filtre de date sur *05 01 17..05 14 17*.
Voici d'autres exemples :

| Signification | Exemple : | Ecritures incluses |
|---|---|---|
|Egal à| 15 12 16 |Uniquement les écritures validées le 15 décembre 2016.|
|Intervalle| 15 12 16..15 17 17<br /><br />..12 15 16|Celles validées entre le 15 décembre 2016 et le 15 janvier 2017 inclus.<br /><br />Écritures validées le 15 décembre 2016 ou à une date antérieure.|
|Et/ou|12 15 16&#124;12 16 16|Celles validées le 15 ou le 16 décembre 2016. Les écritures validées aux deux dates sont également affichées.|

Vous pouvez aussi combiner les divers types de format.

| Exemple : | Ecritures incluses |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Écritures validées le 15 décembre 2016 ou à des dates situées entre le 1er décembre 2016 et le 31 mai 2017 inclus. |
|..12 14 16&#124;12 30 16.. | Les écritures validées le 14 décembre ou avant, ou écritures validées le 30 décembre ou après, c.-à-d. toutes les écritures à l'exception de celles validées à des dates situées entre le 15 et le 29 décembre. |

Remarquez que nous avons utilisé le format de date américaine MMJJAA. A mesure que [!INCLUDE[d365fin](includes/d365fin_md.md)] deviendra disponible sur d'autres marché, vous pourrez utiliser les formats auxquels vous êtes habitué.

## <a name="using-date-formulas"></a>Utilisation de formules date
Une formule date est une combinaison abrégée de lettres et de nombres qui spécifie comment calculer les dates. Vous pouvez entrer des formules date dans divers champs de calcul de date et dans les champs périodicité récurrente des feuilles récurrentes.

> [!NOTE]
>  Dans tous les champs formule de données, un jour est automatiquement inclus pour couvrir le jour de début de la période. Par conséquent, si vous saisissez **1s**, par exemple, la période est bien huit jours parce que aujourd'hui est inclus. Pour définir une période de sept jours (une vraie semaine) avec la date début de la période, vous devez saisir **6j** ou **1s\-1j**.

Voici quelques exemples d'utilisation de formules date :

-   La formule date du champ périodicité d'abonnement des feuilles abonnement détermine la fréquence de validation de l'écriture de la ligne feuille.

-   La formule date du champ **Période de carence** pour un niveau de relance précis détermine la période qui doit se passer entre la date d'échéance (ou la date d'échéance de la relance précédente) avant la création d'une nouvelle relance.

-   La formule date du champ **Calcul date échéance** détermine la manière dont la date d'échéance de la relance est calculée.

La formule de calcul de la date peut comprendre un maximum de 20 caractères, des chiffres et des lettres. Vous pouvez utiliser les lettres suivantes qui sont des abréviations de spécifications de temps.

|  Lettre  |  Spécification de l'heure  |
|----------|----------------------|
|C|Actuellement|
|J|Jour\(s\)|
|O|Week\(s\) (Semaines)|
|C|Mois|
|T|Trimestre\(s\)|
|A|Année\(s\)|

Vous pouvez construire la formule date de trois manières.

L'exemple suivant indique comment utiliser **C** pour en cours et une unité temporelle.

|  Expression  |  Signification  |
|--------------|-----------|
|CS|Semaine en cours|
|FM|Mois en cours|

L'exemple suivant indique comment utiliser un chiffre et une unité de temps. Un chiffre ne peut pas être supérieur à 9999.

|  Expression  |  Signification  |
|--------------|-----------|
|10J|10 jours à dater d'aujourd'hui|
|2S|2 semaines à dater d'aujourd'hui|

L'exemple suivant indique comment utiliser une unité de temps et un chiffre.

|  Expression  |  Signification  |
|--------------|-----------|
|J10|Le dixième jour du mois suivant|
|JS4|Le quatrième jour de la semaine \(jeudi\)|

L'exemple suivant indique comment combiner ces trois formules.

|  Expression  |  Signification  |
|--------------|-----------|
|CM\+10J|Mois en cours \+ 10 jours|

L'exemple ci-dessous illustre comment vous pouvez utiliser le signe moins pour indiquer une date du passé.

|  Expression  |  Signification  |
|--------------|-----------|
|-1A|Il y a 1 an à dater d'aujourd'hui|

> [!IMPORTANT]
>  Si le magasin utilise un calendrier principal, la formule de date que vous entrez par exemple le champ **Délai d'expédition**, est interprétée en fonction des jours ouvrés du calendrier. Par exemple, **1s** un signifie sept jours ouvrés.

## <a name="see-also"></a>Voir aussi
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Calcul de la date des achats](purchasing-date-calculation-for-purchases.md)  
[Saisir les critères pour les filtres](ui-enter-criteria-filters.md)  

