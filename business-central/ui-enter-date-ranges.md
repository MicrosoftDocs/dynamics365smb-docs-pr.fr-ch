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
# <a name="entering-date-ranges"></a><span data-ttu-id="d0694-103">Saisie de plages de dates</span><span class="sxs-lookup"><span data-stu-id="d0694-103">Entering Date Ranges</span></span>
<span data-ttu-id="d0694-104">Vous pouvez définir des filtres contenant une date de début et une date de fin pour afficher uniquement les données contenues dans cette plage de données ou cet intervalle de temps.</span><span class="sxs-lookup"><span data-stu-id="d0694-104">You can set filters containing a start date and an end date to display only the data contained in that date range or time interval.</span></span> <span data-ttu-id="d0694-105">Des règles spéciales s'appliquent à la définition des plages de dates.</span><span class="sxs-lookup"><span data-stu-id="d0694-105">Special rules apply to the way you set date ranges.</span></span> <span data-ttu-id="d0694-106">Prenons par exemple **Palmarès des clients** :</span><span class="sxs-lookup"><span data-stu-id="d0694-106">Let's take the **Customer Top 10** as an example:</span></span>

![Définition d'une plage de dates dans la page de demande de la liste du palmarès des clients](./media/ui-enter-date-ranges/customer-top10-list.png)

<span data-ttu-id="d0694-108">Vous pouvez limiter ici l'état à une plage de dates telles que les 2 dernières semaines, ou un total de 6 semaines, ou toute plage de votre choix.</span><span class="sxs-lookup"><span data-stu-id="d0694-108">Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want.</span></span> <span data-ttu-id="d0694-109">Pour définir les plages de dates, vous entrez des dates puis utilisez **..**</span><span class="sxs-lookup"><span data-stu-id="d0694-109">To set date ranges, you enter dates and then use either **..**</span></span> <span data-ttu-id="d0694-110">ou **|** pour définir la plage.</span><span class="sxs-lookup"><span data-stu-id="d0694-110">or **|** to set the range.</span></span> <span data-ttu-id="d0694-111">Dans notre exemple, pour afficher les 10 clients principaux des deux premières semaines de mai, vous devez définir le filtre de date sur *05 01 17..05 14 17*.</span><span class="sxs-lookup"><span data-stu-id="d0694-111">In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.</span></span>
<span data-ttu-id="d0694-112">Voici d'autres exemples :</span><span class="sxs-lookup"><span data-stu-id="d0694-112">Here are a couple of other examples:</span></span>

| <span data-ttu-id="d0694-113">Signification</span><span class="sxs-lookup"><span data-stu-id="d0694-113">Meaning</span></span> | <span data-ttu-id="d0694-114">Exemple :</span><span class="sxs-lookup"><span data-stu-id="d0694-114">Example</span></span> | <span data-ttu-id="d0694-115">Ecritures incluses</span><span class="sxs-lookup"><span data-stu-id="d0694-115">Entries included</span></span> |
|---|---|---|
|<span data-ttu-id="d0694-116">Egal à</span><span class="sxs-lookup"><span data-stu-id="d0694-116">Equal to</span></span>| <span data-ttu-id="d0694-117">15 12 16</span><span class="sxs-lookup"><span data-stu-id="d0694-117">12 15 16</span></span> |<span data-ttu-id="d0694-118">Uniquement les écritures validées le 15 décembre 2016.</span><span class="sxs-lookup"><span data-stu-id="d0694-118">Only those posted on December 15 2016.</span></span>|
|<span data-ttu-id="d0694-119">Intervalle</span><span class="sxs-lookup"><span data-stu-id="d0694-119">Interval</span></span>| <span data-ttu-id="d0694-120">15 12 16..15 17 17</span><span class="sxs-lookup"><span data-stu-id="d0694-120">12 15 16..01 15 17</span></span><br /><br /><span data-ttu-id="d0694-121">..12 15 16</span><span class="sxs-lookup"><span data-stu-id="d0694-121">..12 15 16</span></span>|<span data-ttu-id="d0694-122">Celles validées entre le 15 décembre 2016 et le 15 janvier 2017 inclus.</span><span class="sxs-lookup"><span data-stu-id="d0694-122">Those posted on dates between and including December 15 2016 and January 15 2017.</span></span><br /><br /><span data-ttu-id="d0694-123">Écritures validées le 15 décembre 2016 ou à une date antérieure.</span><span class="sxs-lookup"><span data-stu-id="d0694-123">Those posted on December 15 2016 or earlier.</span></span>|
|<span data-ttu-id="d0694-124">Et/ou</span><span class="sxs-lookup"><span data-stu-id="d0694-124">Either/or</span></span>|<span data-ttu-id="d0694-125">12 15 16&#124;12 16 16</span><span class="sxs-lookup"><span data-stu-id="d0694-125">12 15 16&#124;12 16 16</span></span>|<span data-ttu-id="d0694-126">Celles validées le 15 ou le 16 décembre 2016.</span><span class="sxs-lookup"><span data-stu-id="d0694-126">Those posted on either December 15 or December 16 2016.</span></span> <span data-ttu-id="d0694-127">Les écritures validées aux deux dates sont également affichées.</span><span class="sxs-lookup"><span data-stu-id="d0694-127">If there are entries posted on both days, they will all be displayed.</span></span>|

<span data-ttu-id="d0694-128">Vous pouvez aussi combiner les divers types de format.</span><span class="sxs-lookup"><span data-stu-id="d0694-128">You can also combine the various format types.</span></span>

| <span data-ttu-id="d0694-129">Exemple :</span><span class="sxs-lookup"><span data-stu-id="d0694-129">Example</span></span> | <span data-ttu-id="d0694-130">Ecritures incluses</span><span class="sxs-lookup"><span data-stu-id="d0694-130">Entries included</span></span> |
|---|---|
|<span data-ttu-id="d0694-131">12 15 16&#124;12 01 16..05 31 17</span><span class="sxs-lookup"><span data-stu-id="d0694-131">12 15 16&#124;12 01 16..05 31 17</span></span> | <span data-ttu-id="d0694-132">Écritures validées le 15 décembre 2016 ou à des dates situées entre le 1er décembre 2016 et le 31 mai 2017 inclus.</span><span class="sxs-lookup"><span data-stu-id="d0694-132">Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017.</span></span> |
|<span data-ttu-id="d0694-133">..12 14 16&#124;12 30 16..</span><span class="sxs-lookup"><span data-stu-id="d0694-133">..12 14 16&#124;12 30 16..</span></span> | <span data-ttu-id="d0694-134">Les écritures validées le 14 décembre ou avant, ou écritures validées le 30 décembre ou après, c.-à-d. toutes les écritures à l'exception de celles validées à des dates situées entre le 15 et le 29 décembre.</span><span class="sxs-lookup"><span data-stu-id="d0694-134">Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29.</span></span> |

<span data-ttu-id="d0694-135">Remarquez que nous avons utilisé le format de date américaine MMJJAA.</span><span class="sxs-lookup"><span data-stu-id="d0694-135">Note that we have used the US date format MMDDYY here.</span></span> <span data-ttu-id="d0694-136">A mesure que [!INCLUDE[d365fin](includes/d365fin_md.md)] deviendra disponible sur d'autres marché, vous pourrez utiliser les formats auxquels vous êtes habitué.</span><span class="sxs-lookup"><span data-stu-id="d0694-136">As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.</span></span>

## <a name="using-date-formulas"></a><span data-ttu-id="d0694-137">Utilisation de formules date</span><span class="sxs-lookup"><span data-stu-id="d0694-137">Using Date Formulas</span></span>
<span data-ttu-id="d0694-138">Une formule date est une combinaison abrégée de lettres et de nombres qui spécifie comment calculer les dates.</span><span class="sxs-lookup"><span data-stu-id="d0694-138">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="d0694-139">Vous pouvez entrer des formules date dans divers champs de calcul de date et dans les champs périodicité récurrente des feuilles récurrentes.</span><span class="sxs-lookup"><span data-stu-id="d0694-139">You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.</span></span>

> [!NOTE]
>  <span data-ttu-id="d0694-140">Dans tous les champs formule de données, un jour est automatiquement inclus pour couvrir le jour de début de la période.</span><span class="sxs-lookup"><span data-stu-id="d0694-140">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="d0694-141">Par conséquent, si vous saisissez **1s**, par exemple, la période est bien huit jours parce que aujourd'hui est inclus.</span><span class="sxs-lookup"><span data-stu-id="d0694-141">Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="d0694-142">Pour définir une période de sept jours (une vraie semaine) avec la date début de la période, vous devez saisir **6j** ou **1s\-1j**.</span><span class="sxs-lookup"><span data-stu-id="d0694-142">To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.</span></span>

<span data-ttu-id="d0694-143">Voici quelques exemples d'utilisation de formules date :</span><span class="sxs-lookup"><span data-stu-id="d0694-143">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="d0694-144">La formule date du champ périodicité d'abonnement des feuilles abonnement détermine la fréquence de validation de l'écriture de la ligne feuille.</span><span class="sxs-lookup"><span data-stu-id="d0694-144">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="d0694-145">La formule date du champ **Période de carence** pour un niveau de relance précis détermine la période qui doit se passer entre la date d'échéance (ou la date d'échéance de la relance précédente) avant la création d'une nouvelle relance.</span><span class="sxs-lookup"><span data-stu-id="d0694-145">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.</span></span>

-   <span data-ttu-id="d0694-146">La formule date du champ **Calcul date échéance** détermine la manière dont la date d'échéance de la relance est calculée.</span><span class="sxs-lookup"><span data-stu-id="d0694-146">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="d0694-147">La formule de calcul de la date peut comprendre un maximum de 20 caractères, des chiffres et des lettres.</span><span class="sxs-lookup"><span data-stu-id="d0694-147">The date calculation formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="d0694-148">Vous pouvez utiliser les lettres suivantes qui sont des abréviations de spécifications de temps.</span><span class="sxs-lookup"><span data-stu-id="d0694-148">You can use the following letters, which are abbreviations for time specifications.</span></span>

|  <span data-ttu-id="d0694-149">Lettre</span><span class="sxs-lookup"><span data-stu-id="d0694-149">Letter</span></span>  |  <span data-ttu-id="d0694-150">Spécification de l'heure</span><span class="sxs-lookup"><span data-stu-id="d0694-150">Time specification</span></span>  |
|----------|----------------------|
|<span data-ttu-id="d0694-151">C</span><span class="sxs-lookup"><span data-stu-id="d0694-151">C</span></span>|<span data-ttu-id="d0694-152">Actuellement</span><span class="sxs-lookup"><span data-stu-id="d0694-152">Current</span></span>|
|<span data-ttu-id="d0694-153">J</span><span class="sxs-lookup"><span data-stu-id="d0694-153">D</span></span>|<span data-ttu-id="d0694-154">Jour\(s\)</span><span class="sxs-lookup"><span data-stu-id="d0694-154">Day\(s\)</span></span>|
|<span data-ttu-id="d0694-155">O</span><span class="sxs-lookup"><span data-stu-id="d0694-155">W</span></span>|<span data-ttu-id="d0694-156">Week\(s\) (Semaines)</span><span class="sxs-lookup"><span data-stu-id="d0694-156">Week\(s\)</span></span>|
|<span data-ttu-id="d0694-157">C</span><span class="sxs-lookup"><span data-stu-id="d0694-157">M</span></span>|<span data-ttu-id="d0694-158">Mois</span><span class="sxs-lookup"><span data-stu-id="d0694-158">Month\(s\)</span></span>|
|<span data-ttu-id="d0694-159">T</span><span class="sxs-lookup"><span data-stu-id="d0694-159">Q</span></span>|<span data-ttu-id="d0694-160">Trimestre\(s\)</span><span class="sxs-lookup"><span data-stu-id="d0694-160">Quarter\(s\)</span></span>|
|<span data-ttu-id="d0694-161">A</span><span class="sxs-lookup"><span data-stu-id="d0694-161">Y</span></span>|<span data-ttu-id="d0694-162">Année\(s\)</span><span class="sxs-lookup"><span data-stu-id="d0694-162">Year\(s\)</span></span>|

<span data-ttu-id="d0694-163">Vous pouvez construire la formule date de trois manières.</span><span class="sxs-lookup"><span data-stu-id="d0694-163">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="d0694-164">L'exemple suivant indique comment utiliser **C** pour en cours et une unité temporelle.</span><span class="sxs-lookup"><span data-stu-id="d0694-164">The following example shows how to use **C**, for current, and a time unit.</span></span>

|  <span data-ttu-id="d0694-165">Expression</span><span class="sxs-lookup"><span data-stu-id="d0694-165">Expression</span></span>  |  <span data-ttu-id="d0694-166">Signification</span><span class="sxs-lookup"><span data-stu-id="d0694-166">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="d0694-167">CS</span><span class="sxs-lookup"><span data-stu-id="d0694-167">CW</span></span>|<span data-ttu-id="d0694-168">Semaine en cours</span><span class="sxs-lookup"><span data-stu-id="d0694-168">Current week</span></span>|
|<span data-ttu-id="d0694-169">FM</span><span class="sxs-lookup"><span data-stu-id="d0694-169">CM</span></span>|<span data-ttu-id="d0694-170">Mois en cours</span><span class="sxs-lookup"><span data-stu-id="d0694-170">Current month</span></span>|

<span data-ttu-id="d0694-171">L'exemple suivant indique comment utiliser un chiffre et une unité de temps.</span><span class="sxs-lookup"><span data-stu-id="d0694-171">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="d0694-172">Un chiffre ne peut pas être supérieur à 9999.</span><span class="sxs-lookup"><span data-stu-id="d0694-172">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="d0694-173">Expression</span><span class="sxs-lookup"><span data-stu-id="d0694-173">Expression</span></span>  |  <span data-ttu-id="d0694-174">Signification</span><span class="sxs-lookup"><span data-stu-id="d0694-174">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="d0694-175">10J</span><span class="sxs-lookup"><span data-stu-id="d0694-175">10D</span></span>|<span data-ttu-id="d0694-176">10 jours à dater d'aujourd'hui</span><span class="sxs-lookup"><span data-stu-id="d0694-176">10 days from today</span></span>|
|<span data-ttu-id="d0694-177">2S</span><span class="sxs-lookup"><span data-stu-id="d0694-177">2W</span></span>|<span data-ttu-id="d0694-178">2 semaines à dater d'aujourd'hui</span><span class="sxs-lookup"><span data-stu-id="d0694-178">2 weeks from today</span></span>|

<span data-ttu-id="d0694-179">L'exemple suivant indique comment utiliser une unité de temps et un chiffre.</span><span class="sxs-lookup"><span data-stu-id="d0694-179">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="d0694-180">Expression</span><span class="sxs-lookup"><span data-stu-id="d0694-180">Expression</span></span>  |  <span data-ttu-id="d0694-181">Signification</span><span class="sxs-lookup"><span data-stu-id="d0694-181">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="d0694-182">J10</span><span class="sxs-lookup"><span data-stu-id="d0694-182">D10</span></span>|<span data-ttu-id="d0694-183">Le dixième jour du mois suivant</span><span class="sxs-lookup"><span data-stu-id="d0694-183">The next 10th day of a month</span></span>|
|<span data-ttu-id="d0694-184">JS4</span><span class="sxs-lookup"><span data-stu-id="d0694-184">WD4</span></span>|<span data-ttu-id="d0694-185">Le quatrième jour de la semaine \(jeudi\)</span><span class="sxs-lookup"><span data-stu-id="d0694-185">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="d0694-186">L'exemple suivant indique comment combiner ces trois formules.</span><span class="sxs-lookup"><span data-stu-id="d0694-186">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="d0694-187">Expression</span><span class="sxs-lookup"><span data-stu-id="d0694-187">Expression</span></span>  |  <span data-ttu-id="d0694-188">Signification</span><span class="sxs-lookup"><span data-stu-id="d0694-188">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="d0694-189">CM\+10J</span><span class="sxs-lookup"><span data-stu-id="d0694-189">CM\+10D</span></span>|<span data-ttu-id="d0694-190">Mois en cours \+ 10 jours</span><span class="sxs-lookup"><span data-stu-id="d0694-190">Current month \+ 10 days</span></span>|

<span data-ttu-id="d0694-191">L'exemple ci-dessous illustre comment vous pouvez utiliser le signe moins pour indiquer une date du passé.</span><span class="sxs-lookup"><span data-stu-id="d0694-191">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="d0694-192">Expression</span><span class="sxs-lookup"><span data-stu-id="d0694-192">Expression</span></span>  |  <span data-ttu-id="d0694-193">Signification</span><span class="sxs-lookup"><span data-stu-id="d0694-193">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="d0694-194">-1A</span><span class="sxs-lookup"><span data-stu-id="d0694-194">-1Y</span></span>|<span data-ttu-id="d0694-195">Il y a 1 an à dater d'aujourd'hui</span><span class="sxs-lookup"><span data-stu-id="d0694-195">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="d0694-196">Si le magasin utilise un calendrier principal, la formule de date que vous entrez par exemple le champ **Délai d'expédition**, est interprétée en fonction des jours ouvrés du calendrier.</span><span class="sxs-lookup"><span data-stu-id="d0694-196">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="d0694-197">Par exemple, **1s** un signifie sept jours ouvrés.</span><span class="sxs-lookup"><span data-stu-id="d0694-197">For example, **1W**  means seven working days.</span></span>

## <a name="see-also"></a><span data-ttu-id="d0694-198">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0694-198">See Also</span></span>
<span data-ttu-id="d0694-199">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d0694-199">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="d0694-200">Calcul de la date des achats</span><span class="sxs-lookup"><span data-stu-id="d0694-200">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="d0694-201">Saisir les critères pour les filtres</span><span class="sxs-lookup"><span data-stu-id="d0694-201">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  

