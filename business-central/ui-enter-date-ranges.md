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
ms.date: 09/17/2019
ms.author: sgroespe
ms.openlocfilehash: 96471b07d48120db7fda5e48a14c9ca0147688fb
ms.sourcegitcommit: 7ce8005806465417c7040c61da1d6cada29cd9c0
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/17/2019
ms.locfileid: "2000778"
---
# <a name="working-with-calendar-dates-and-times"></a><span data-ttu-id="bee47-104">Utilisation de dates civiles et les heures</span><span class="sxs-lookup"><span data-stu-id="bee47-104">Working with Calendar Dates and Times</span></span>

[!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="bee47-105">offre plusieurs méthodes principales de saisie des dates et des heures, y compris des fonctions puissantes qui accélèrent la saisie de données, ou vous permettent de saisir des expressions de calendrier complexes.</span><span class="sxs-lookup"><span data-stu-id="bee47-105">offers multiple ways to enter dates and times, including powerful features that accelerate data entry, or help you write complex calendar expressions.</span></span> <span data-ttu-id="bee47-106">Il existe différents emplacements tout au long de l'application où vous pouvez entrer des dates et des heures dans les champs.</span><span class="sxs-lookup"><span data-stu-id="bee47-106">There are various places throughout the application where you can enter dates and times in fields.</span></span> <span data-ttu-id="bee47-107">Par exemple, dans une commande client, vous pouvez également définir la date d'expédition.</span><span class="sxs-lookup"><span data-stu-id="bee47-107">For example, on a sales order, you can set the shipment date.</span></span> <span data-ttu-id="bee47-108">En filtrant les données de liste ou d'état, vous pouvez entrer des dates et des heures pour désigner uniquement les données que vous intéressent.</span><span class="sxs-lookup"><span data-stu-id="bee47-108">When filtering lists or report data, you can enter dates and times to pinpoint only the data that you are interested in.</span></span>

## <a name="check-your-region-and-language-settings"></a><span data-ttu-id="bee47-109">Vérifiez les paramètres de zone et de langue</span><span class="sxs-lookup"><span data-stu-id="bee47-109">Check your region and language settings</span></span>

<span data-ttu-id="bee47-110">La page [**Mes paramètres**](https://businesscentral.dynamics.com?page=9176 "Accéder directement à votre page de paramètres utilisateurs dans Business Central") spécifie **Région** et **Langue** que vous utilisez dans l'application.</span><span class="sxs-lookup"><span data-stu-id="bee47-110">The [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central") page specifies the **Region** and **Language** that you are using in the application.</span></span> <span data-ttu-id="bee47-111">Ces paramètres ont une incidence sur la manière dont vous saisissez des dates et des heures.</span><span class="sxs-lookup"><span data-stu-id="bee47-111">These settings influence how you enter dates and times.</span></span>

-   <span data-ttu-id="bee47-112">Le paramètre **Région** détermine la manière dont les dates, heures, nombres et devises sont affichés ou mis en forme.</span><span class="sxs-lookup"><span data-stu-id="bee47-112">The **Region** setting determines how dates, times, numbers, and currencies are shown or formatted.</span></span>

-   <span data-ttu-id="bee47-113">Pour des modèles de date qui impliquent des mots, la langue des mots utilisée doit correspondre au paramètre **Langue**.</span><span class="sxs-lookup"><span data-stu-id="bee47-113">For date patterns that involve words, the language of the words that you use must correspond to the **Language** setting.</span></span>

> [!NOTE]
> [!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="bee47-114">utilise le système du calendrier grégorien.</span><span class="sxs-lookup"><span data-stu-id="bee47-114">uses the Gregorian calendar system.</span></span>

<!--
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->

## <a name="entering-dates"></a><span data-ttu-id="bee47-115">Saisie de dates</span><span class="sxs-lookup"><span data-stu-id="bee47-115">Entering Dates</span></span>

<span data-ttu-id="bee47-116">Dans un champ de date, vous pouvez saisir une date à l'aide du format standard pour votre paramètre de zone.</span><span class="sxs-lookup"><span data-stu-id="bee47-116">In a date field, you can enter a date using the standard format for your region setting.</span></span> <span data-ttu-id="bee47-117">Les différentes régions peuvent utiliser différents séparateurs entre les jours, mois et années.</span><span class="sxs-lookup"><span data-stu-id="bee47-117">Different regions can use different separators between the days, months and years.</span></span> <span data-ttu-id="bee47-118">Par exemple, certaines régions utilisent les tirets (mm-jj-aaaa) et d'autres les barres obliques (mm/jj/aaaa).</span><span class="sxs-lookup"><span data-stu-id="bee47-118">For example, some regions use dashes (mm-dd-yyyy) and others use forward slashes (mm/dd/yyyy).</span></span> <span data-ttu-id="bee47-119">Cependant, vous pouvez utiliser tous les séparateurs, même un espace, et la date est modifiée automatiquement pour utiliser les séparateurs correspondant à votre région.</span><span class="sxs-lookup"><span data-stu-id="bee47-119">However, you can use any separators, even a space, and the date will automatically be changed to use separators that match your region.</span></span>

<span data-ttu-id="bee47-120">Notez que le format des dates affichées sur les états imprimés ou les documents envoyés par e-mail n'est pas influencé par votre choix personnel de paramètre d'une zone.</span><span class="sxs-lookup"><span data-stu-id="bee47-120">Note that the format in which dates are displayed on printed reports or emailed documents is not influenced by your personal choice of region setting.</span></span>

<span data-ttu-id="bee47-121">Pour travailler plus productivement avec des dates et des heures, vous pouvez utiliser les méthodes ou les formats décrits dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="bee47-121">To work more productively with dates and times, you can use any of the methods or formats that are described in the following sections.</span></span>

### <a name="picking-dates-from-the-calendar"></a><span data-ttu-id="bee47-122">Choisir des dates dans le calendrier</span><span class="sxs-lookup"><span data-stu-id="bee47-122">Picking dates from the calendar</span></span>

<span data-ttu-id="bee47-123">Tout champ affichant une icône de calendrier peut être paramétré à l'aide du sélecteur de date civile.</span><span class="sxs-lookup"><span data-stu-id="bee47-123">Any field displaying a calendar icon can be set using the calendar date picker.</span></span> <span data-ttu-id="bee47-124">Pour afficher le sélecteur de date civile, activer l'icône de calendrier ou appuyer sur le raccourci clavier Ctrl+Début dans le champ.</span><span class="sxs-lookup"><span data-stu-id="bee47-124">To display the calendar date picker, activate the calendar icon or press the Ctrl + Home keyboard shortcut in the field.</span></span>

<span data-ttu-id="bee47-125">![Champs de date](media/ui-date-field.png "Exemple d'un champ de date")</span><span class="sxs-lookup"><span data-stu-id="bee47-125">![Date fields](media/ui-date-field.png "Example of a date field")</span></span>

<span data-ttu-id="bee47-126">Voir aussi [Raccourcis clavier du sélecteur de date civile](keyboard-shortcuts.md#calendarshortcuts)</span><span class="sxs-lookup"><span data-stu-id="bee47-126">See also [Keyboard Shortcuts in the calendar date picker](keyboard-shortcuts.md#calendarshortcuts)</span></span>

### <a name="day-week-year-pattern"></a><span data-ttu-id="bee47-127">Modèle jour\-semaine\-année</span><span class="sxs-lookup"><span data-stu-id="bee47-127">Day\-week\-year pattern</span></span>

<span data-ttu-id="bee47-128">Vous pouvez saisir une date comme un jour de la semaine suivi d'un numéro de semaine et, éventuellement, une année.</span><span class="sxs-lookup"><span data-stu-id="bee47-128">You can enter a date as a weekday followed by a week number and, optionally, a year.</span></span> <span data-ttu-id="bee47-129">Par exemple, Lun25 ou lun25 signifie le lundi de la semaine 25.</span><span class="sxs-lookup"><span data-stu-id="bee47-129">For example, Mon25 or mon25 means Monday in week 25.</span></span> <span data-ttu-id="bee47-130">Si vous ne saisissez pas une année, l'année de la date de travail est utilisée.</span><span class="sxs-lookup"><span data-stu-id="bee47-130">If you do not enter a year, the year of the work date is used.</span></span>

<span data-ttu-id="bee47-131">Au lieu de saisir le mot entier du jour de la semaine, vous pouvez saisir une partie du mot, en commençant du début.</span><span class="sxs-lookup"><span data-stu-id="bee47-131">Instead of entering the entire word for the day of the week, you can enter part of the word, starting from the beginning.</span></span> <span data-ttu-id="bee47-132">Dans le cas de conflits (par exemple avec m qui peut être mardi ou mercredi), les jours sont évalués en fonction du paramètre d'une zone.</span><span class="sxs-lookup"><span data-stu-id="bee47-132">In case of conflicts (such as with s which could be Saturday or Sunday), the days are evaluated according to the region setting.</span></span> <span data-ttu-id="bee47-133">L'entrée est d'abord évaluée par rapport à la date de travail et à la date du jour, ne l'oubliez pas en abrégeant.</span><span class="sxs-lookup"><span data-stu-id="bee47-133">The input is first evaluated against workdate and today as well, so keep this in mind when abbreviating.</span></span> <span data-ttu-id="bee47-134">Par exemple, m signifie déjà maintenant, ce qui ne peut pas être mardi ou mercredi.</span><span class="sxs-lookup"><span data-stu-id="bee47-134">For example, t already means today, so it cannot mean Tuesday or Thursday.</span></span>

<span data-ttu-id="bee47-135">Le schéma de numéros de semaine est toujours ISO 8601, où la semaine 1 est la semaine avec le 4 janvier dans celle-ci, ou la semaine avec le premier jeudi de l'exercice.</span><span class="sxs-lookup"><span data-stu-id="bee47-135">The week number scheme is always ISO 8601, where week 1 is the week with 4 January in it, or the week with the first Thursday of the year.</span></span>

### <a name="digit-patterns"></a><span data-ttu-id="bee47-136">Modèles de chiffres</span><span class="sxs-lookup"><span data-stu-id="bee47-136">Digit patterns</span></span>

<span data-ttu-id="bee47-137">Vous pouvez saisir deux, quatre, six ou huit chiffres dans un champ date :</span><span class="sxs-lookup"><span data-stu-id="bee47-137">In a date field you can enter two, four, six, or eight digits:</span></span>

-   <span data-ttu-id="bee47-138">Si vous ne saisissez que deux chiffres, ils sont interprétés comme le jour, et le mois et l'année de la date de travail sont ajoutés.</span><span class="sxs-lookup"><span data-stu-id="bee47-138">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>

-   <span data-ttu-id="bee47-139">Si vous saisissez quatre chiffres, ils sont interprétés comme le jour et le mois, et l'année de la date de travail est ajoutée.</span><span class="sxs-lookup"><span data-stu-id="bee47-139">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span> <span data-ttu-id="bee47-140">L'ordre du jour et du mois est déterminé par les paramètres de région.</span><span class="sxs-lookup"><span data-stu-id="bee47-140">The order of the day and month is determined by your region settings.</span></span> <span data-ttu-id="bee47-141">Même si vos paramètres de région ont l'année avant le jour et le mois, quatre chiffres sont interprétés en tant que jour et mois.</span><span class="sxs-lookup"><span data-stu-id="bee47-141">Even if your region settings have the year before the day and month, four digits are interpreted as the day and month.</span></span>

-   <span data-ttu-id="bee47-142">Si la date que vous souhaitez saisir est comprise entre le 01/01/1930 et le 31/12/2029, vous pouvez saisir les deux chiffres de l'année ; sinon saisissez les quatre chiffres.</span><span class="sxs-lookup"><span data-stu-id="bee47-142">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>

### <a name="today"></a><span data-ttu-id="bee47-143">Aujourd'hui</span><span class="sxs-lookup"><span data-stu-id="bee47-143">Today</span></span>

<span data-ttu-id="bee47-144">Entrez le mot pour aujourd'hui, dans la langue définie par le paramètre **Langue**, qui définit la date à la date actuelle.</span><span class="sxs-lookup"><span data-stu-id="bee47-144">Enter the word for today, in the language set by **Language** setting, that will set the date to the current date.</span></span> <span data-ttu-id="bee47-145">Au lieu de saisir le mot entier, vous pouvez saisir une partie du mot, en commençant par le début par exemple a ou auj, tant que ce n'est pas également le début d'un autre mot.</span><span class="sxs-lookup"><span data-stu-id="bee47-145">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as t or tod, as long as it is not also the start of another word.</span></span>

### <a name="period"></a><span data-ttu-id="bee47-146">Période.</span><span class="sxs-lookup"><span data-stu-id="bee47-146">Period</span></span>

<span data-ttu-id="bee47-147">Pour filtrer une période comptable spécifique, dans un champ de date saisissez la lettre p, ou le mot période, suivi par un numéro qui identifie la période comptable, comme p2 ou période4.</span><span class="sxs-lookup"><span data-stu-id="bee47-147">To filter on a specific accounting period, in a date field enter the letter p, or the word period, followed by a number that identifies the accounting period, like p2 or period4.</span></span> <span data-ttu-id="bee47-148">La période comptable est relative à l'exercice comptable de la date de travail en cours défini dans votre tableau de bord.</span><span class="sxs-lookup"><span data-stu-id="bee47-148">The accounting period is relative to the fiscal year of the current work date that set in your Role Center.</span></span> <span data-ttu-id="bee47-149">Par exemple, si la date de travail est **21/03/20**, alors p1 ou simplement p filtre la première période comptable de l'exercice comptable 2020 (par exemple 01/01/20..31/01/20).</span><span class="sxs-lookup"><span data-stu-id="bee47-149">For example, if the work date is **03/21/20**, then p1, or just p, filters on the first accounting period of the fiscal year 2020 (such as 01/01/20..01/31/20).</span></span> <span data-ttu-id="bee47-150">p15 filtre la quinzième période comptable depuis le début de l'exercice comptable 2020 (par exemple 01/03/21..31/03/21).</span><span class="sxs-lookup"><span data-stu-id="bee47-150">p15 filters on the fifteenth accounting period from the start of fiscal year 2020 (such as 03/01/21..03/31/21).</span></span>

<span data-ttu-id="bee47-151">Les périodes comptables sont définies sur la page **Périodes comptables**.</span><span class="sxs-lookup"><span data-stu-id="bee47-151">The accounting periods are defined on the **Accounting Periods** page.</span></span> <span data-ttu-id="bee47-152">Pour visualiser ou modifier les périodes comptables, ouvrez la page [ici](https://businesscentral.dynamics.com/?page=100).</span><span class="sxs-lookup"><span data-stu-id="bee47-152">To view or change the accounting periods, open the page [here](https://businesscentral.dynamics.com/?page=100).</span></span>

### <a name="current-work-date"></a><span data-ttu-id="bee47-153">Date de travail actuelle</span><span class="sxs-lookup"><span data-stu-id="bee47-153">Current work date</span></span>

<span data-ttu-id="bee47-154">La fonction de date de travail vous permet d'enregistrer des transactions en utilisant une date qui est différente de la date du jour.</span><span class="sxs-lookup"><span data-stu-id="bee47-154">The work date feature allows you to record transactions using a date that is different from the current date.</span></span>

<span data-ttu-id="bee47-155">Le mot « date de travail », dans la langue définie par le paramètre **Langue**, définit la date à laquelle la date de travail configurée actuellement est spécifiée sur la page [**Mes paramètres**](https://businesscentral.dynamics.com?page=9176 "Accéder directement à votre page de paramètres utilisateurs dans Business Central").</span><span class="sxs-lookup"><span data-stu-id="bee47-155">The word for 'workdate', in the language set by **Language** setting, will set the date to the currently set work date that is specified on the [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central") page.</span></span> <span data-ttu-id="bee47-156">Au lieu de saisir le mot entier, vous pouvez saisir une partie du mot, en commençant du début, comme "t" pour travail.</span><span class="sxs-lookup"><span data-stu-id="bee47-156">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as 'w' or 'work'.</span></span>

<span data-ttu-id="bee47-157">Si vous ne définissez pas de date de travail, la date actuelle sera utilisée comme date de travail.</span><span class="sxs-lookup"><span data-stu-id="bee47-157">If you have not defined a work date, the current date will be used as the work date.</span></span> <span data-ttu-id="bee47-158">Vous souhaiterez peut-être utiliser une date de travail si vous avez beaucoup de transactions avec une date différente de la date d'aujourd'hui.</span><span class="sxs-lookup"><span data-stu-id="bee47-158">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>

<span data-ttu-id="bee47-159">Voir aussi [Modification des paramètres de base, comme la date de travail](ui-change-basic-settings.md#work-date).</span><span class="sxs-lookup"><span data-stu-id="bee47-159">See also [Changing Basic Settings, such as the Work Date](ui-change-basic-settings.md#work-date).</span></span>

### <a name="closing-date"></a><span data-ttu-id="bee47-160">Date de clôture</span><span class="sxs-lookup"><span data-stu-id="bee47-160">Closing Date</span></span>

<span data-ttu-id="bee47-161">Lorsque vous clôturez un exercice comptable, vous pouvez utiliser des dates de clôture pour indiquer qu'une écriture est une écriture de clôture.</span><span class="sxs-lookup"><span data-stu-id="bee47-161">When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry.</span></span> <span data-ttu-id="bee47-162">Techniquement, une date de clôture se trouve entre deux dates, par exemple le 31 décembre et le 1er janvier.</span><span class="sxs-lookup"><span data-stu-id="bee47-162">A closing date technically is between two dates, for example between Dec 31 and Jan 1.</span></span>

<span data-ttu-id="bee47-163">Pour spécifier qu'une date est une date de clôture, placez un C devant cette date, comme C123101.</span><span class="sxs-lookup"><span data-stu-id="bee47-163">To specify that a date is a closing date, put C just before the date, such as C123101.</span></span> <span data-ttu-id="bee47-164">Ceci peut être utilisé avec tous les modèles de date.</span><span class="sxs-lookup"><span data-stu-id="bee47-164">This can be used in combination with all the date patterns.</span></span>

### <a name="examples"></a><span data-ttu-id="bee47-165">Exemples</span><span class="sxs-lookup"><span data-stu-id="bee47-165">Examples</span></span>

<span data-ttu-id="bee47-166">Le tableau suivant affiche des exemples de dates à l'aide de tous les formats.</span><span class="sxs-lookup"><span data-stu-id="bee47-166">The following table contains examples of dates using all the formats.</span></span> <span data-ttu-id="bee47-167">Il considère les paramètres de région selon lesquels format les dates : **année.mois.jour.**, une semaine commençant lundi, et l'anglais.</span><span class="sxs-lookup"><span data-stu-id="bee47-167">It assumes region settings that format dates according to: **year.month.day.**, a week starting on Monday, and the English language.</span></span>

|<span data-ttu-id="bee47-168">**Écriture**</span><span class="sxs-lookup"><span data-stu-id="bee47-168">**Entry**</span></span>      |<span data-ttu-id="bee47-169">**Interprétation**</span><span class="sxs-lookup"><span data-stu-id="bee47-169">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="bee47-170">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="bee47-170">2018.12.31.</span></span>|<span data-ttu-id="bee47-171">31/12/2018.</span><span class="sxs-lookup"><span data-stu-id="bee47-171">2018.12.31.</span></span>|
|<span data-ttu-id="bee47-172">181231</span><span class="sxs-lookup"><span data-stu-id="bee47-172">181231</span></span>|<span data-ttu-id="bee47-173">31/12/2018.</span><span class="sxs-lookup"><span data-stu-id="bee47-173">2018.12.31.</span></span>|
|<span data-ttu-id="bee47-174">18.12.31.</span><span class="sxs-lookup"><span data-stu-id="bee47-174">18.12.31.</span></span>|<span data-ttu-id="bee47-175">31/12/2018.</span><span class="sxs-lookup"><span data-stu-id="bee47-175">2018.12.31.</span></span>|
|<span data-ttu-id="bee47-176">18.12.31.</span><span class="sxs-lookup"><span data-stu-id="bee47-176">18.12.31.</span></span>|<span data-ttu-id="bee47-177">31/12/2018.</span><span class="sxs-lookup"><span data-stu-id="bee47-177">2018.12.31.</span></span>|
|<span data-ttu-id="bee47-178">20181231</span><span class="sxs-lookup"><span data-stu-id="bee47-178">20181231</span></span>|<span data-ttu-id="bee47-179">31/12/2018.</span><span class="sxs-lookup"><span data-stu-id="bee47-179">2018.12.31.</span></span>|
|<span data-ttu-id="bee47-180">18/12,31</span><span class="sxs-lookup"><span data-stu-id="bee47-180">18/12,31</span></span>|<span data-ttu-id="bee47-181">31/12/2018.</span><span class="sxs-lookup"><span data-stu-id="bee47-181">2018.12.31.</span></span>|
|<span data-ttu-id="bee47-182">11</span><span class="sxs-lookup"><span data-stu-id="bee47-182">11</span></span>|<span data-ttu-id="bee47-183">11/mois date travail/année date travail.</span><span class="sxs-lookup"><span data-stu-id="bee47-183">work date year.work date month.11.</span></span>|
|<span data-ttu-id="bee47-184">1112</span><span class="sxs-lookup"><span data-stu-id="bee47-184">1112</span></span>|<span data-ttu-id="bee47-185">11/12/année date travail.</span><span class="sxs-lookup"><span data-stu-id="bee47-185">work date year.11.12.</span></span>|
|<span data-ttu-id="bee47-186">a ou date du jour</span><span class="sxs-lookup"><span data-stu-id="bee47-186">t or today</span></span>|<span data-ttu-id="bee47-187">date du jour</span><span class="sxs-lookup"><span data-stu-id="bee47-187">today's date</span></span>|
|<span data-ttu-id="bee47-188">p4</span><span class="sxs-lookup"><span data-stu-id="bee47-188">p4</span></span>|<span data-ttu-id="bee47-189">plage de dates qui comprend la quatrième la période comptable, par exemple 01/04/20..30/04/20</span><span class="sxs-lookup"><span data-stu-id="bee47-189">date range that includes the fourth accounting period, such as 04/01/20..04/30/20</span></span>|
|<span data-ttu-id="bee47-190">t ou date de travail</span><span class="sxs-lookup"><span data-stu-id="bee47-190">w or workdate</span></span>|<span data-ttu-id="bee47-191">date de travail</span><span class="sxs-lookup"><span data-stu-id="bee47-191">the working date</span></span>|
|<span data-ttu-id="bee47-192">lu ou lundi</span><span class="sxs-lookup"><span data-stu-id="bee47-192">m or Monday</span></span>|<span data-ttu-id="bee47-193">Lundi de la semaine de date de travail</span><span class="sxs-lookup"><span data-stu-id="bee47-193">Monday of the work date week</span></span>|
|<span data-ttu-id="bee47-194">ma ou mardi</span><span class="sxs-lookup"><span data-stu-id="bee47-194">tu or Tuesday</span></span>|<span data-ttu-id="bee47-195">Mardi de la semaine de date de travail</span><span class="sxs-lookup"><span data-stu-id="bee47-195">Tuesday of the work date week</span></span>|
|<span data-ttu-id="bee47-196">sa ou samedi</span><span class="sxs-lookup"><span data-stu-id="bee47-196">sa or Saturday</span></span>|<span data-ttu-id="bee47-197">Samedi de la semaine de date de travail</span><span class="sxs-lookup"><span data-stu-id="bee47-197">Saturday of the work date week</span></span>|
|<span data-ttu-id="bee47-198">di ou dimanche</span><span class="sxs-lookup"><span data-stu-id="bee47-198">s or Sunday</span></span>|<span data-ttu-id="bee47-199">Dimanche de la semaine de date de travail</span><span class="sxs-lookup"><span data-stu-id="bee47-199">Sunday of the work date week</span></span>|
|<span data-ttu-id="bee47-200">m23</span><span class="sxs-lookup"><span data-stu-id="bee47-200">t23</span></span>|<span data-ttu-id="bee47-201">Mardi de la semaine 23 de l'année de date de travail</span><span class="sxs-lookup"><span data-stu-id="bee47-201">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="bee47-202">m 23</span><span class="sxs-lookup"><span data-stu-id="bee47-202">t 23</span></span>|<span data-ttu-id="bee47-203">Mardi de la semaine 23 de l'année de date de travail</span><span class="sxs-lookup"><span data-stu-id="bee47-203">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="bee47-204">m-1</span><span class="sxs-lookup"><span data-stu-id="bee47-204">t-1</span></span>|<span data-ttu-id="bee47-205">Mardi de la semaine 1 de l'année de date de travail</span><span class="sxs-lookup"><span data-stu-id="bee47-205">Tuesday of week 1 of the work date year</span></span>|

##  <a name="BKMK_SettingDateRanges"></a> <span data-ttu-id="bee47-206">Définition des plages</span><span class="sxs-lookup"><span data-stu-id="bee47-206">Setting Ranges</span></span>

<span data-ttu-id="bee47-207">Sous Listes, totaux et états, vous pouvez définir des filtres sur les dates, heures et dates/heures contenant une valeur de début et éventuellement une valeur de fin pour afficher uniquement les données contenues dans cette plage.</span><span class="sxs-lookup"><span data-stu-id="bee47-207">On lists, totals and reports, you can set filters on dates, times and datetimes containing a start value and optionally an end value to display only the data contained in that range.</span></span> <span data-ttu-id="bee47-208">Les règles standard s'appliquent à la définition des plages de dates.</span><span class="sxs-lookup"><span data-stu-id="bee47-208">The standard rules apply to the way you set date ranges.</span></span>

|<span data-ttu-id="bee47-209">**Signification**</span><span class="sxs-lookup"><span data-stu-id="bee47-209">**Meaning**</span></span>|<span data-ttu-id="bee47-210">**Exemple d'expression (Date)**</span><span class="sxs-lookup"><span data-stu-id="bee47-210">**Sample expression (Date)**</span></span>|<span data-ttu-id="bee47-211">**Données incluses dans le filtre**</span><span class="sxs-lookup"><span data-stu-id="bee47-211">**Data included in the filter**</span></span>|
|-----------|---------------------|--------------------|
|<span data-ttu-id="bee47-212">Intervalle</span><span class="sxs-lookup"><span data-stu-id="bee47-212">Interval</span></span>|<span data-ttu-id="bee47-213">15 12 00..15 01 01</span><span class="sxs-lookup"><span data-stu-id="bee47-213">12 15 00..01 15 01</span></span><br /><br /><span data-ttu-id="bee47-214">..15 12 00</span><span class="sxs-lookup"><span data-stu-id="bee47-214">..12 15 00</span></span><br /><br /><span data-ttu-id="bee47-215">p1..p4</span><span class="sxs-lookup"><span data-stu-id="bee47-215">p1..p4</span></span>|<span data-ttu-id="bee47-216">Enregistrements dont les dates sont comprises entre le 15/12/00 et le 15/01/01 inclusivement.</span><span class="sxs-lookup"><span data-stu-id="bee47-216">Records with dates between and including 12 15 00 and 01 15 01.</span></span><br /><br /><span data-ttu-id="bee47-217">Enregistrements dont les dates sont le 12/15/00 ou avant.</span><span class="sxs-lookup"><span data-stu-id="bee47-217">Records with dates of 12 15 00 or earlier.</span></span><br /><br /><span data-ttu-id="bee47-218">Plage de dates qui comprend la deuxième, la troisième et la quatrième période comptable, par exemple 01/01/20..30/04/20.</span><span class="sxs-lookup"><span data-stu-id="bee47-218">Date range that includes the second, third, and fourth accounting periods, such as 01/01/20..04/30/20.</span></span>|
|<span data-ttu-id="bee47-219">Et/ou</span><span class="sxs-lookup"><span data-stu-id="bee47-219">Either/or</span></span>|<span data-ttu-id="bee47-220">15 12 00</span><span class="sxs-lookup"><span data-stu-id="bee47-220">12 15 00</span></span>|<span data-ttu-id="bee47-221">16 12 00</span><span class="sxs-lookup"><span data-stu-id="bee47-221">12 16 00</span></span>|<span data-ttu-id="bee47-222">Enregistrement dont les dates sont le 15/12/00 ou 16/12/00.</span><span class="sxs-lookup"><span data-stu-id="bee47-222">Records with dates of either 12 15 00 or 12 16 00.</span></span> <span data-ttu-id="bee47-223">Si des enregistrements comportent des dates pendant ces deux jours, ils sont tous affichés.</span><span class="sxs-lookup"><span data-stu-id="bee47-223">If there are records with dates on both days, they will all be displayed.</span></span>|
|<span data-ttu-id="bee47-224">Combinaison</span><span class="sxs-lookup"><span data-stu-id="bee47-224">Combination</span></span>|<span data-ttu-id="bee47-225">15 12 00</span><span class="sxs-lookup"><span data-stu-id="bee47-225">12 15 00</span></span>|<span data-ttu-id="bee47-226">12 01 00..12 10 00  \n..12 14 00</span><span class="sxs-lookup"><span data-stu-id="bee47-226">12 01 00..12 10 00  \n..12 14 00</span></span>|<span data-ttu-id="bee47-227">12 30 00..</span><span class="sxs-lookup"><span data-stu-id="bee47-227">12 30 00..</span></span>|<span data-ttu-id="bee47-228">Enregistrements avec pour dates le 15/12/00 ou entre le 01/12/00 et le 10/12/00 inclus.</span><span class="sxs-lookup"><span data-stu-id="bee47-228">Records with dates of 12 15 00 or on dates between and including 12 01 00 and 12 10 00.</span></span>  <span data-ttu-id="bee47-229">\Enregistrements avec dates le 14/12/00 ou avant, ou le 30/12/00 ou après, c'est-à-dire tous les enregistrements exceptés ceux avec des dates comprises entre le 15/12/00 et le 29/12/00 inclusivement.</span><span class="sxs-lookup"><span data-stu-id="bee47-229">\Records with dates of 12 14 00 or earlier, or dates of 12 30 00 or later, that is, all records except those with dates between and including 12 15 00 and 12 29 00.</span></span>|

<span data-ttu-id="bee47-230">Vous pouvez utiliser l'un des formats valides dans les filtres Plage de dates.</span><span class="sxs-lookup"><span data-stu-id="bee47-230">You can use any of the valid formats in date range filters.</span></span> <span data-ttu-id="bee47-231">Par exemple, lun14 3..t 4p appliqué pour un champ Date/heure débouche sur un filtre à partir de 3h du matin le lundi de la semaine 14 de l'année de date de travail en cours, incluse, jusqu'à aujourd'hui à 16h, inclus.</span><span class="sxs-lookup"><span data-stu-id="bee47-231">For example, mon14 3..t 4p applied on a datetime field results in a filter from 3 AM on Monday in week 14 of the current work date year, inclusive, until today at 4PM, inclusive.</span></span>

## <a name="using-date-formulas"></a><span data-ttu-id="bee47-232">Utilisation de formules date</span><span class="sxs-lookup"><span data-stu-id="bee47-232">Using Date Formulas</span></span>
<span data-ttu-id="bee47-233">Une formule date est une combinaison abrégée de lettres et de nombres qui spécifie comment calculer les dates.</span><span class="sxs-lookup"><span data-stu-id="bee47-233">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="bee47-234">Vous pouvez entrer des formules date dans différents champs ou filtres de calcul de date.</span><span class="sxs-lookup"><span data-stu-id="bee47-234">You can enter date formulas in various date calculation fields or filters.</span></span>

> [!NOTE]
>  <span data-ttu-id="bee47-235">Dans tous les champs formule de données, un jour est automatiquement inclus pour couvrir le jour de début de la période.</span><span class="sxs-lookup"><span data-stu-id="bee47-235">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="bee47-236">Par conséquent, si vous saisissez 1S, par exemple, la période est bien huit jours parce que aujourd'hui est inclus.</span><span class="sxs-lookup"><span data-stu-id="bee47-236">Accordingly, for example, if you enter 1W, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="bee47-237">Pour définir une période de sept jours \(une vraie semaine\) avec la date début de la période, vous devez saisir 6J ou 1S-1J.</span><span class="sxs-lookup"><span data-stu-id="bee47-237">To specify a period of seven days \(one true week\) including the period starting date, then you must enter 6D or 1W-1D.</span></span>

<span data-ttu-id="bee47-238">Voici quelques exemples d'utilisation de formules date :</span><span class="sxs-lookup"><span data-stu-id="bee47-238">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="bee47-239">La formule date du champ périodicité récurrente des feuilles récurrentes détermine la fréquence de validation de l'écriture de la ligne feuille.</span><span class="sxs-lookup"><span data-stu-id="bee47-239">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="bee47-240">La formule date du champ **Période de carence** pour un niveau de relance précis détermine la période qui doit se passer entre la date d'échéance \(ou la date de la relance précédente\) avant la création d'une nouvelle relance.</span><span class="sxs-lookup"><span data-stu-id="bee47-240">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date \(or from the date of the previous reminder\) before a reminder will be created.</span></span>

-   <span data-ttu-id="bee47-241">La formule date du champ **Calcul date échéance** détermine la manière dont la date d'échéance de la relance est calculée.</span><span class="sxs-lookup"><span data-stu-id="bee47-241">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="bee47-242">La formule de la date peut comprendre un maximum de 20 caractères, des chiffres et des lettres.</span><span class="sxs-lookup"><span data-stu-id="bee47-242">The date formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="bee47-243">Vous pouvez utiliser les lettres suivantes qui sont des abréviations d'unités de calendrier.</span><span class="sxs-lookup"><span data-stu-id="bee47-243">You can use the following letters, which are abbreviations for calendar units.</span></span>

|  <span data-ttu-id="bee47-244">Lettre</span><span class="sxs-lookup"><span data-stu-id="bee47-244">Letter</span></span>  |  <span data-ttu-id="bee47-245">Signification</span><span class="sxs-lookup"><span data-stu-id="bee47-245">Meaning</span></span>  |
|----------|----------------------|
|<span data-ttu-id="bee47-246">A</span><span class="sxs-lookup"><span data-stu-id="bee47-246">C</span></span>|<span data-ttu-id="bee47-247">Actuellement</span><span class="sxs-lookup"><span data-stu-id="bee47-247">Current</span></span>|
|<span data-ttu-id="bee47-248">J</span><span class="sxs-lookup"><span data-stu-id="bee47-248">D</span></span>|<span data-ttu-id="bee47-249">Jour\(s\)</span><span class="sxs-lookup"><span data-stu-id="bee47-249">Day\(s\)</span></span>|
|<span data-ttu-id="bee47-250">S</span><span class="sxs-lookup"><span data-stu-id="bee47-250">W</span></span>|<span data-ttu-id="bee47-251">Week\(s\) (Semaines)</span><span class="sxs-lookup"><span data-stu-id="bee47-251">Week\(s\)</span></span>|
|<span data-ttu-id="bee47-252">M</span><span class="sxs-lookup"><span data-stu-id="bee47-252">M</span></span>|<span data-ttu-id="bee47-253">Mois\(s\)</span><span class="sxs-lookup"><span data-stu-id="bee47-253">Month\(s\)</span></span>|
|<span data-ttu-id="bee47-254">T</span><span class="sxs-lookup"><span data-stu-id="bee47-254">Q</span></span>|<span data-ttu-id="bee47-255">Trimestre\(s\)</span><span class="sxs-lookup"><span data-stu-id="bee47-255">Quarter\(s\)</span></span>|
|<span data-ttu-id="bee47-256">A</span><span class="sxs-lookup"><span data-stu-id="bee47-256">Y</span></span>|<span data-ttu-id="bee47-257">Année\(s\)</span><span class="sxs-lookup"><span data-stu-id="bee47-257">Year\(s\)</span></span>|

<span data-ttu-id="bee47-258">Vous pouvez construire la formule date de trois manières.</span><span class="sxs-lookup"><span data-stu-id="bee47-258">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="bee47-259">L'exemple suivant indique comment utiliser C pour en cours et une unité temporelle.</span><span class="sxs-lookup"><span data-stu-id="bee47-259">The following example shows how to use C, for current, and a time unit.</span></span>

|  <span data-ttu-id="bee47-260">Expression</span><span class="sxs-lookup"><span data-stu-id="bee47-260">Expression</span></span>  |  <span data-ttu-id="bee47-261">Signification</span><span class="sxs-lookup"><span data-stu-id="bee47-261">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="bee47-262">CS</span><span class="sxs-lookup"><span data-stu-id="bee47-262">CW</span></span>|<span data-ttu-id="bee47-263">Semaine en cours</span><span class="sxs-lookup"><span data-stu-id="bee47-263">Current week</span></span>|
|<span data-ttu-id="bee47-264">MC</span><span class="sxs-lookup"><span data-stu-id="bee47-264">CM</span></span>|<span data-ttu-id="bee47-265">Mois en cours</span><span class="sxs-lookup"><span data-stu-id="bee47-265">Current month</span></span>|

<span data-ttu-id="bee47-266">L'exemple suivant indique comment utiliser un chiffre et une unité de temps.</span><span class="sxs-lookup"><span data-stu-id="bee47-266">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="bee47-267">Un chiffre ne peut pas être supérieur à 9999.</span><span class="sxs-lookup"><span data-stu-id="bee47-267">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="bee47-268">Expression</span><span class="sxs-lookup"><span data-stu-id="bee47-268">Expression</span></span>  |  <span data-ttu-id="bee47-269">Signification</span><span class="sxs-lookup"><span data-stu-id="bee47-269">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="bee47-270">10J</span><span class="sxs-lookup"><span data-stu-id="bee47-270">10D</span></span>|<span data-ttu-id="bee47-271">10 jours à dater d'aujourd'hui</span><span class="sxs-lookup"><span data-stu-id="bee47-271">10 days from today</span></span>|
|<span data-ttu-id="bee47-272">2S</span><span class="sxs-lookup"><span data-stu-id="bee47-272">2W</span></span>|<span data-ttu-id="bee47-273">2 semaines à dater d'aujourd'hui</span><span class="sxs-lookup"><span data-stu-id="bee47-273">2 weeks from today</span></span>|

<span data-ttu-id="bee47-274">L'exemple suivant indique comment utiliser une unité de temps et un chiffre.</span><span class="sxs-lookup"><span data-stu-id="bee47-274">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="bee47-275">Expression</span><span class="sxs-lookup"><span data-stu-id="bee47-275">Expression</span></span>  |  <span data-ttu-id="bee47-276">Signification</span><span class="sxs-lookup"><span data-stu-id="bee47-276">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="bee47-277">J10</span><span class="sxs-lookup"><span data-stu-id="bee47-277">D10</span></span>|<span data-ttu-id="bee47-278">Le dixième jour du mois suivant</span><span class="sxs-lookup"><span data-stu-id="bee47-278">The next 10th day of a month</span></span>|
|<span data-ttu-id="bee47-279">JS4</span><span class="sxs-lookup"><span data-stu-id="bee47-279">WD4</span></span>|<span data-ttu-id="bee47-280">Le quatrième jour de la semaine \(jeudi\)</span><span class="sxs-lookup"><span data-stu-id="bee47-280">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="bee47-281">L'exemple suivant indique comment combiner ces trois formules.</span><span class="sxs-lookup"><span data-stu-id="bee47-281">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="bee47-282">Expression</span><span class="sxs-lookup"><span data-stu-id="bee47-282">Expression</span></span>  |  <span data-ttu-id="bee47-283">Signification</span><span class="sxs-lookup"><span data-stu-id="bee47-283">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="bee47-284">MC+10J</span><span class="sxs-lookup"><span data-stu-id="bee47-284">CM+10D</span></span>|<span data-ttu-id="bee47-285">Mois en cours \+ 10 jours</span><span class="sxs-lookup"><span data-stu-id="bee47-285">Current month \+ 10 days</span></span>|

<span data-ttu-id="bee47-286">L'exemple ci-dessous illustre comment vous pouvez utiliser le signe moins pour indiquer une date du passé.</span><span class="sxs-lookup"><span data-stu-id="bee47-286">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="bee47-287">Expression</span><span class="sxs-lookup"><span data-stu-id="bee47-287">Expression</span></span>  |  <span data-ttu-id="bee47-288">Signification</span><span class="sxs-lookup"><span data-stu-id="bee47-288">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="bee47-289">-1A</span><span class="sxs-lookup"><span data-stu-id="bee47-289">-1Y</span></span>|<span data-ttu-id="bee47-290">Il y a 1 an à dater d'aujourd'hui</span><span class="sxs-lookup"><span data-stu-id="bee47-290">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="bee47-291">Si le magasin utilise un calendrier principal, la formule de date que vous entrez par exemple le champ **Délai d'expédition**, est interprétée en fonction des jours ouvrés du calendrier.</span><span class="sxs-lookup"><span data-stu-id="bee47-291">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="bee47-292">Par exemple, 1S un signifie sept jours ouvrés.</span><span class="sxs-lookup"><span data-stu-id="bee47-292">For example, 1W  means seven working days.</span></span>
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

Note that we have used the US date format MMDDYY here. As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.

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

## <a name="entering-times"></a><span data-ttu-id="bee47-293">Saisie des heures</span><span class="sxs-lookup"><span data-stu-id="bee47-293">Entering Times</span></span>
<span data-ttu-id="bee47-294">Lorsque vous saisissez des heures, vous pouvez insérer n'importe quel type de séparateur entre les unités, mais si vous utilisez des chiffres doubles pour chaque unité jusqu'aux millisecondes, ce n'est pas requis.</span><span class="sxs-lookup"><span data-stu-id="bee47-294">When you enter times, you can insert any non-space separators that you want between the units, but if you use double digits for each unit up to milliseconds, then it is not required.</span></span>

<span data-ttu-id="bee47-295">Vous n'avez qu'à entrer les plus grandes unités souhaitées ; les autres sont remis à zéro.</span><span class="sxs-lookup"><span data-stu-id="bee47-295">You only have to write the largest units that you require; the rest will be set to zero.</span></span> <span data-ttu-id="bee47-296">Vous pouvez également omettre l'indicateur AM/PM.</span><span class="sxs-lookup"><span data-stu-id="bee47-296">You can also leave out any AM/PM indicator.</span></span>

<span data-ttu-id="bee47-297">Le tableau suivant répertorie les différents formats de saisie possibles pour les heures, ainsi que leur interprétation.</span><span class="sxs-lookup"><span data-stu-id="bee47-297">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span> <span data-ttu-id="bee47-298">Il considère les paramètres de zone qui formatent les périodes : **Heures:Minutes:Secondes.Millisecondes.**</span><span class="sxs-lookup"><span data-stu-id="bee47-298">It assumes region settings that format times according to: **Hours:Minutes:Seconds.Milliseconds.**</span></span> <span data-ttu-id="bee47-299">et utilisent les indicateurs AM et PM « AM » et « PM », respectivement.</span><span class="sxs-lookup"><span data-stu-id="bee47-299">and use the AM and PM indicators of 'AM' and 'PM', respectively.</span></span>

|<span data-ttu-id="bee47-300">**Écriture**</span><span class="sxs-lookup"><span data-stu-id="bee47-300">**Entry**</span></span>      |<span data-ttu-id="bee47-301">**Interprétation**</span><span class="sxs-lookup"><span data-stu-id="bee47-301">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="bee47-302">05:23:17</span><span class="sxs-lookup"><span data-stu-id="bee47-302">05:23:17</span></span>|<span data-ttu-id="bee47-303">05:23:17</span><span class="sxs-lookup"><span data-stu-id="bee47-303">05:23:17</span></span>|
|<span data-ttu-id="bee47-304">5</span><span class="sxs-lookup"><span data-stu-id="bee47-304">5</span></span>|<span data-ttu-id="bee47-305">05:00:00</span><span class="sxs-lookup"><span data-stu-id="bee47-305">05:00:00</span></span>|
|<span data-ttu-id="bee47-306">5AM</span><span class="sxs-lookup"><span data-stu-id="bee47-306">5AM</span></span>|<span data-ttu-id="bee47-307">05:00:00</span><span class="sxs-lookup"><span data-stu-id="bee47-307">05:00:00</span></span>|
|<span data-ttu-id="bee47-308">5P</span><span class="sxs-lookup"><span data-stu-id="bee47-308">5P</span></span>|<span data-ttu-id="bee47-309">17:00:00</span><span class="sxs-lookup"><span data-stu-id="bee47-309">17:00:00</span></span>|
|<span data-ttu-id="bee47-310">12</span><span class="sxs-lookup"><span data-stu-id="bee47-310">12</span></span>|<span data-ttu-id="bee47-311">12:00:00</span><span class="sxs-lookup"><span data-stu-id="bee47-311">12:00:00</span></span>|
|<span data-ttu-id="bee47-312">12A</span><span class="sxs-lookup"><span data-stu-id="bee47-312">12A</span></span>|<span data-ttu-id="bee47-313">00:00:00</span><span class="sxs-lookup"><span data-stu-id="bee47-313">00:00:00</span></span>|
|<span data-ttu-id="bee47-314">12P</span><span class="sxs-lookup"><span data-stu-id="bee47-314">12P</span></span>|<span data-ttu-id="bee47-315">12:00:00</span><span class="sxs-lookup"><span data-stu-id="bee47-315">12:00:00</span></span>|
|<span data-ttu-id="bee47-316">17</span><span class="sxs-lookup"><span data-stu-id="bee47-316">17</span></span>|<span data-ttu-id="bee47-317">17:00:00</span><span class="sxs-lookup"><span data-stu-id="bee47-317">17:00:00</span></span>|
|<span data-ttu-id="bee47-318">5:30</span><span class="sxs-lookup"><span data-stu-id="bee47-318">5:30</span></span>|<span data-ttu-id="bee47-319">05:30:00</span><span class="sxs-lookup"><span data-stu-id="bee47-319">05:30:00</span></span>|
|<span data-ttu-id="bee47-320">0530</span><span class="sxs-lookup"><span data-stu-id="bee47-320">0530</span></span>|<span data-ttu-id="bee47-321">05:30:00</span><span class="sxs-lookup"><span data-stu-id="bee47-321">05:30:00</span></span>|
|<span data-ttu-id="bee47-322">5:30:5</span><span class="sxs-lookup"><span data-stu-id="bee47-322">5:30:5</span></span>|<span data-ttu-id="bee47-323">05:30:05</span><span class="sxs-lookup"><span data-stu-id="bee47-323">05:30:05</span></span>|
|<span data-ttu-id="bee47-324">053005</span><span class="sxs-lookup"><span data-stu-id="bee47-324">053005</span></span>|<span data-ttu-id="bee47-325">05:30:05</span><span class="sxs-lookup"><span data-stu-id="bee47-325">05:30:05</span></span>|
|<span data-ttu-id="bee47-326">5:30:5,50</span><span class="sxs-lookup"><span data-stu-id="bee47-326">5:30:5,50</span></span>|<span data-ttu-id="bee47-327">05:30:05.5</span><span class="sxs-lookup"><span data-stu-id="bee47-327">05:30:05.5</span></span>|
|<span data-ttu-id="bee47-328">053005050</span><span class="sxs-lookup"><span data-stu-id="bee47-328">053005050</span></span>|<span data-ttu-id="bee47-329">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="bee47-329">05:30:05.05</span></span>|

<span data-ttu-id="bee47-330">Tenez compte que les millisecondes sont interprétées comme des notations de décimales.</span><span class="sxs-lookup"><span data-stu-id="bee47-330">You should be aware that milliseconds are interpreted as decimal notation.</span></span> <span data-ttu-id="bee47-331">Ainsi, par exemple 3, 30 et 300 signifient tous 300 millisecondes, alors que 03 signifie 30 et 003 signifie 3 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="bee47-331">So, for example, 3, 30, and 300 all mean 300 milliseconds, while 03 means 30 and 003 means 3 milliseconds.</span></span>

<span data-ttu-id="bee47-332">Vous ne pouvez pas utiliser 24:00 pour dire minuit, ou utiliser une valeur supérieure à 24:00.</span><span class="sxs-lookup"><span data-stu-id="bee47-332">You cannot use 24:00 to mean midnight, or use any value greater than 24:00.</span></span>

<span data-ttu-id="bee47-333">Le mot pour « time » (heure) dans la langue utilisée par [!INCLUDE[d365fin](includes/d365fin_long_md.md)] est évalué sur l'heure actuelle sur votre ordinateur ou appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="bee47-333">The word for 'time' in the language used by [!INCLUDE[d365fin](includes/d365fin_long_md.md)] will be evaluated to the current time on your computer or mobile device.</span></span> <span data-ttu-id="bee47-334">Vous pouvez saisir n'importe quel partie du mot, en commençant au début, par exemple h ou HEU.</span><span class="sxs-lookup"><span data-stu-id="bee47-334">You can enter any part of the word, starting from the beginning, such as t or TIM.</span></span>

## <a name="entering-combined-dates-and-times"></a><span data-ttu-id="bee47-335">Saisie de dates et d'heures combinées</span><span class="sxs-lookup"><span data-stu-id="bee47-335">Entering combined Dates and Times</span></span>
<span data-ttu-id="bee47-336">Lorsque vous saisissez les dates/heures, qui sont une date et heure combinées en un champ, vous devez saisir un espace entre la date et l'heure.</span><span class="sxs-lookup"><span data-stu-id="bee47-336">When you enter datetimes, which are a date and time combined into one field, you must enter a space between the date and the time.</span></span> <span data-ttu-id="bee47-337">La partie de la date ne peut contenir des espaces sous forme de séparateur de date officiel de vos paramètres de région.</span><span class="sxs-lookup"><span data-stu-id="bee47-337">The date part can only contain spaces in the form of the official date separator of your region settings.</span></span> <span data-ttu-id="bee47-338">L'heure peut contenir des espaces autour de l'indicateur AM/PM.</span><span class="sxs-lookup"><span data-stu-id="bee47-338">The time can contain spaces around the AM/PM indicator.</span></span>

<span data-ttu-id="bee47-339">Il est également possible de saisir qu'une date dans un champ Date/heure, mais il n'est pas possible d'entrer seulement une heure.</span><span class="sxs-lookup"><span data-stu-id="bee47-339">It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.</span></span>

<span data-ttu-id="bee47-340">Le tableau suivant répertorie quelques exemples de combinaisons Date/heure.</span><span class="sxs-lookup"><span data-stu-id="bee47-340">The following table lists some examples of date/time combinations.</span></span> <span data-ttu-id="bee47-341">Les paramètres de région dans les exemples affichent les dates au format jour\-mois\-année, en utilisant les indicateurs AM/PM, l'anglais, et le dimanche comme début de la semaine.</span><span class="sxs-lookup"><span data-stu-id="bee47-341">The region settings in the examples displays dates in the day\-month\-year format, using AM/PM designators, English language, and Sunday as the start of the week.</span></span>

|<span data-ttu-id="bee47-342">**Écriture**</span><span class="sxs-lookup"><span data-stu-id="bee47-342">**Entry**</span></span>      |<span data-ttu-id="bee47-343">**Interprétation**</span><span class="sxs-lookup"><span data-stu-id="bee47-343">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="bee47-344">08-01-2016 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="bee47-344">08-01-2016 05:48:12 PM</span></span>|<span data-ttu-id="bee47-345">08/01/2016 17:48:12</span><span class="sxs-lookup"><span data-stu-id="bee47-345">08\-01\-2016 05:48:12 PM</span></span>|
|<span data-ttu-id="bee47-346">131202 132455</span><span class="sxs-lookup"><span data-stu-id="bee47-346">131202 132455</span></span>|<span data-ttu-id="bee47-347">13/12/2002 13:24:55</span><span class="sxs-lookup"><span data-stu-id="bee47-347">13\-12\-2002 13:24:55</span></span>|
|<span data-ttu-id="bee47-348">1-12-02 10</span><span class="sxs-lookup"><span data-stu-id="bee47-348">1-12-02 10</span></span>|<span data-ttu-id="bee47-349">01/12/2002 10:00:00</span><span class="sxs-lookup"><span data-stu-id="bee47-349">01\-12\-2002 10:00:00</span></span>|
|<span data-ttu-id="bee47-350">1.12.02 5</span><span class="sxs-lookup"><span data-stu-id="bee47-350">1.12.02 5</span></span>|<span data-ttu-id="bee47-351">01/12/2002 05:00:00</span><span class="sxs-lookup"><span data-stu-id="bee47-351">01\-12\-2002 05:00:00</span></span>|
|<span data-ttu-id="bee47-352">1.12.02</span><span class="sxs-lookup"><span data-stu-id="bee47-352">1.12.02</span></span>|<span data-ttu-id="bee47-353">01/12/2002 00:00:00</span><span class="sxs-lookup"><span data-stu-id="bee47-353">01\-12\-2002 00:00:00</span></span>|
|<span data-ttu-id="bee47-354">11 12</span><span class="sxs-lookup"><span data-stu-id="bee47-354">11 12</span></span>|<span data-ttu-id="bee47-355">11/mois date de travail/année date de travail 12:00:00</span><span class="sxs-lookup"><span data-stu-id="bee47-355">11\-work date month\-work date year 12:00:00</span></span>|
|<span data-ttu-id="bee47-356">1112 12</span><span class="sxs-lookup"><span data-stu-id="bee47-356">1112 12</span></span>|<span data-ttu-id="bee47-357">11/12/année date de travail 12:00:00</span><span class="sxs-lookup"><span data-stu-id="bee47-357">11\-12\-work date year 12:00:00</span></span>|
|<span data-ttu-id="bee47-358">a ou date du jour</span><span class="sxs-lookup"><span data-stu-id="bee47-358">t or today</span></span>|<span data-ttu-id="bee47-359">date du jour 00:00:00</span><span class="sxs-lookup"><span data-stu-id="bee47-359">today's date 00:00:00</span></span>|
|<span data-ttu-id="bee47-360">a 10:30</span><span class="sxs-lookup"><span data-stu-id="bee47-360">t 10:30</span></span>|<span data-ttu-id="bee47-361">date du jour 10:30:00</span><span class="sxs-lookup"><span data-stu-id="bee47-361">today's date 10:30:00</span></span>|
|<span data-ttu-id="bee47-362">a 3:3:3</span><span class="sxs-lookup"><span data-stu-id="bee47-362">t 3:3:3</span></span>|<span data-ttu-id="bee47-363">date du jour 03:03:03</span><span class="sxs-lookup"><span data-stu-id="bee47-363">today's date 03:03:03</span></span>|
|<span data-ttu-id="bee47-364">t ou date de travail</span><span class="sxs-lookup"><span data-stu-id="bee47-364">w or workdate</span></span>|<span data-ttu-id="bee47-365">date de travail 00:00:00</span><span class="sxs-lookup"><span data-stu-id="bee47-365">the working date 00:00:00</span></span>|
|<span data-ttu-id="bee47-366">lu ou lundi</span><span class="sxs-lookup"><span data-stu-id="bee47-366">m or Monday</span></span>|<span data-ttu-id="bee47-367">Lundi de la semaine de date de travail 00:00:00</span><span class="sxs-lookup"><span data-stu-id="bee47-367">Monday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="bee47-368">ma ou mardi</span><span class="sxs-lookup"><span data-stu-id="bee47-368">tu or Tuesday</span></span>|<span data-ttu-id="bee47-369">Mardi de la semaine de date de travail 00:00:00</span><span class="sxs-lookup"><span data-stu-id="bee47-369">Tuesday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="bee47-370">sa ou samedi</span><span class="sxs-lookup"><span data-stu-id="bee47-370">sa or Saturday</span></span>|<span data-ttu-id="bee47-371">Samedi de la semaine de date de travail 00:00:00</span><span class="sxs-lookup"><span data-stu-id="bee47-371">Saturday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="bee47-372">di ou dimanche</span><span class="sxs-lookup"><span data-stu-id="bee47-372">s or Sunday</span></span>|<span data-ttu-id="bee47-373">Dimanche de la semaine de date de travail 00:00:00</span><span class="sxs-lookup"><span data-stu-id="bee47-373">Sunday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="bee47-374">ma 10:30</span><span class="sxs-lookup"><span data-stu-id="bee47-374">tu 10:30</span></span>|<span data-ttu-id="bee47-375">Mardi de la semaine de date de travail 10:30:00</span><span class="sxs-lookup"><span data-stu-id="bee47-375">Tuesday of the work date week 10:30:00</span></span>|
|<span data-ttu-id="bee47-376">ma 3:3:3</span><span class="sxs-lookup"><span data-stu-id="bee47-376">tu 3:3:3</span></span>|<span data-ttu-id="bee47-377">Mardi de la semaine de date de travail 03:03:03</span><span class="sxs-lookup"><span data-stu-id="bee47-377">Tuesday of the work date week 03:03:03</span></span>|
|<span data-ttu-id="bee47-378">m23 a</span><span class="sxs-lookup"><span data-stu-id="bee47-378">t23 t</span></span>|<span data-ttu-id="bee47-379">Mardi de la semaine 23 de l'année de date de travail, heure actuelle</span><span class="sxs-lookup"><span data-stu-id="bee47-379">Tuesday of week 23 of the work date year, current time of day</span></span>|
|<span data-ttu-id="bee47-380">m23</span><span class="sxs-lookup"><span data-stu-id="bee47-380">t23</span></span>|<span data-ttu-id="bee47-381">Mardi de la semaine 23 de l'année de date de travail</span><span class="sxs-lookup"><span data-stu-id="bee47-381">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="bee47-382">m 23</span><span class="sxs-lookup"><span data-stu-id="bee47-382">t 23</span></span>|<span data-ttu-id="bee47-383">Aujourd'hui 23:00:00</span><span class="sxs-lookup"><span data-stu-id="bee47-383">Today 23:00:00</span></span>|
|<span data-ttu-id="bee47-384">m-1</span><span class="sxs-lookup"><span data-stu-id="bee47-384">t-1</span></span>|<span data-ttu-id="bee47-385">Mardi de la semaine 1 de l'année de date de travail</span><span class="sxs-lookup"><span data-stu-id="bee47-385">Tuesday of week 1 of the work date year</span></span>|

## <a name="entering-duration"></a><span data-ttu-id="bee47-386">Saisie des durées</span><span class="sxs-lookup"><span data-stu-id="bee47-386">Entering Duration</span></span>
<span data-ttu-id="bee47-387">Certains champs de l'application représentent une durée, ou la quantité de temps écoulé, au lieu d'une date ou d'une heure spécifique.</span><span class="sxs-lookup"><span data-stu-id="bee47-387">Some fields in the application represent a duration, or amount of elapsed time, instead of a specific date or time.</span></span> <span data-ttu-id="bee47-388">Vous devez saisir les durées sous la forme d'un chiffre suivi d'une unité de mesure.</span><span class="sxs-lookup"><span data-stu-id="bee47-388">You enter a duration as a number followed by its unit of measure.</span></span>

<span data-ttu-id="bee47-389">Voilà quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="bee47-389">Here are some examples.</span></span>

|<span data-ttu-id="bee47-390">**Durée**</span><span class="sxs-lookup"><span data-stu-id="bee47-390">**Duration**</span></span>|<span data-ttu-id="bee47-391">**Unité**</span><span class="sxs-lookup"><span data-stu-id="bee47-391">**Unit of measure**</span></span>|
|------------|-------------------|
|<span data-ttu-id="bee47-392">2h</span><span class="sxs-lookup"><span data-stu-id="bee47-392">2h</span></span>|<span data-ttu-id="bee47-393">2 heures</span><span class="sxs-lookup"><span data-stu-id="bee47-393">2 hrs</span></span>|
|<span data-ttu-id="bee47-394">6h 30m</span><span class="sxs-lookup"><span data-stu-id="bee47-394">6h 30 m</span></span>|<span data-ttu-id="bee47-395">6 heures 30 minutes</span><span class="sxs-lookup"><span data-stu-id="bee47-395">6 hrs 30 mins</span></span>|
|<span data-ttu-id="bee47-396">6,5h</span><span class="sxs-lookup"><span data-stu-id="bee47-396">6.5h</span></span>|<span data-ttu-id="bee47-397">6 heures 30 minutes</span><span class="sxs-lookup"><span data-stu-id="bee47-397">6 hrs 30 mins</span></span>|
|<span data-ttu-id="bee47-398">90m</span><span class="sxs-lookup"><span data-stu-id="bee47-398">90m</span></span>|<span data-ttu-id="bee47-399">1 heure 30 minutes</span><span class="sxs-lookup"><span data-stu-id="bee47-399">1 hr 30 mins</span></span>|
|<span data-ttu-id="bee47-400">2j 6h 30m</span><span class="sxs-lookup"><span data-stu-id="bee47-400">2d 6h 30m</span></span>|<span data-ttu-id="bee47-401">2 jours 6 heures 30 minutes</span><span class="sxs-lookup"><span data-stu-id="bee47-401">2 days 6 hrs 30 mins</span></span>|
|<span data-ttu-id="bee47-402">2j 6h 30m 56s 600ms</span><span class="sxs-lookup"><span data-stu-id="bee47-402">2d 6h 30m 56s 600ms</span></span>|<span data-ttu-id="bee47-403">2 jours 6 h 30 m 56 s 600 ms</span><span class="sxs-lookup"><span data-stu-id="bee47-403">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|

<span data-ttu-id="bee47-404">Vous pouvez également saisir un nombre automatiquement converti en durée.</span><span class="sxs-lookup"><span data-stu-id="bee47-404">You can also enter a number, which will be automatically converted to a duration.</span></span> <span data-ttu-id="bee47-405">Le nombre saisi est converti en fonction de l'unité de mesure par défaut spécifiée pour le champ de durée.</span><span class="sxs-lookup"><span data-stu-id="bee47-405">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>

<span data-ttu-id="bee47-406">Pour connaître l'unité de mesure utilisée pour un champ de durée, saisissez un nombre et observez l'unité de mesure dans laquelle il est convertit.</span><span class="sxs-lookup"><span data-stu-id="bee47-406">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>

<span data-ttu-id="bee47-407">Par exemple, si l'unité est « heures », le chiffre 5 est converti en 5 h.</span><span class="sxs-lookup"><span data-stu-id="bee47-407">For example, if the unit of measure is hours, the number 5 is converted to 5 hrs.</span></span>

## <a name="see-also"></a><span data-ttu-id="bee47-408">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bee47-408">See Also</span></span>
<span data-ttu-id="bee47-409">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bee47-409">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="bee47-410">Calcul de la date des achats</span><span class="sxs-lookup"><span data-stu-id="bee47-410">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="bee47-411">Saisir les critères pour les filtres</span><span class="sxs-lookup"><span data-stu-id="bee47-411">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  
