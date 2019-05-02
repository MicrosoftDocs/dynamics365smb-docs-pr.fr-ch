---
title: Procédure de saisie de données dans les champs | Microsoft Docs
description: Il existe un grand nombre de fonctions générales qui vous permettent d’entrer des données de façon rapide et simple. Les fonctions générales d’entrée des données sont décrites dans cette rubrique.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: jswymer
ms.openlocfilehash: f1bd2fb92f787d52c5bbab8c2210b9d424c1ffd5
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/19/2019
ms.locfileid: "852508"
---
# <a name="entering-data"></a><span data-ttu-id="e865c-104">Saisie de données</span><span class="sxs-lookup"><span data-stu-id="e865c-104">Entering Data</span></span>
<span data-ttu-id="e865c-105">Il existe un grand nombre de fonctions générales qui vous permettent d’entrer des données de façon rapide et simple.</span><span class="sxs-lookup"><span data-stu-id="e865c-105">There are many general functions that help you enter data  in a quick and easy way.</span></span> <span data-ttu-id="e865c-106">Les fonctions générales de saisie de données sont décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="e865c-106">The general functions for entering data are described in this article.</span></span>  

<span data-ttu-id="e865c-107">Les exemples contenus dans cet article utilisent les données de démonstration.</span><span class="sxs-lookup"><span data-stu-id="e865c-107">The examples in this article use the demonstration data.</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="e865c-108">Champs obligatoires</span><span class="sxs-lookup"><span data-stu-id="e865c-108">Mandatory Fields</span></span>
<span data-ttu-id="e865c-109">Lorsque vous entrez des données sur les pages, certains champs sont marqués par un astérisque rouge.</span><span class="sxs-lookup"><span data-stu-id="e865c-109">When you enter data on pages, certain fields are marked with a red asterisk.</span></span> <span data-ttu-id="e865c-110">L'astérisque rouge signifie que le champ doit être renseigné pour terminer un processus qui utilise ce champ, par exemple, valider une transaction qui utilise la valeur du champ.</span><span class="sxs-lookup"><span data-stu-id="e865c-110">The red asterisk means that the field must be filled to complete a certain process that uses the field, such as posting a transaction that uses the value in the field.</span></span>  

<span data-ttu-id="e865c-111">Même si le champ contient un astérisque rouge, vous n'êtes pas forcé de remplir le champ avant de poursuivre avec les autres champs ou fermer la page.</span><span class="sxs-lookup"><span data-stu-id="e865c-111">Even though the field contains a red asterisk, you are not forced to fill the field before you continue to other fields or close the page.</span></span> <span data-ttu-id="e865c-112">L'astérisque rouge sert uniquement à rappeler que la fin d'un certain processus restera bloquée.</span><span class="sxs-lookup"><span data-stu-id="e865c-112">The red asterisk only serves as a reminder that you will be blocked from completing a certain process.</span></span>  


## <a name="finding-data-as-you-type"></a><span data-ttu-id="e865c-113">Recherche immédiate</span><span class="sxs-lookup"><span data-stu-id="e865c-113">Finding Data As You Type</span></span>  
 <span data-ttu-id="e865c-114">Lorsque vous commencez à taper des caractères dans un champ, une liste déroulante affiche les valeurs de champ possibles.</span><span class="sxs-lookup"><span data-stu-id="e865c-114">When you start to type characters in a field, a drop-down list is displayed and shows possible field values.</span></span> <span data-ttu-id="e865c-115">La liste change à mesure que vous tapez des caractères, et vous pouvez sélectionner la valeur correcte lorsqu'elle s'affiche.</span><span class="sxs-lookup"><span data-stu-id="e865c-115">The list changes as you type more characters, and you can select the correct value when it is displayed.</span></span>  

 <span data-ttu-id="e865c-116">De nombreux champs ont un bouton de Flèche vers le bas que vous pouvez choisir.</span><span class="sxs-lookup"><span data-stu-id="e865c-116">Many fields have a down arrow button that you can choose.</span></span> <span data-ttu-id="e865c-117">sélectionnez la flèche pour obtenir la liste des données disponibles pour le champ.</span><span class="sxs-lookup"><span data-stu-id="e865c-117">You choose the arrow to get a list of data that is available to enter in the field.</span></span> <span data-ttu-id="e865c-118">Selon le type de champ, le bouton peut être associé à l'une deux fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="e865c-118">The button has two functions depending on the type of field:</span></span>  

-   <span data-ttu-id="e865c-119">Liste - Affiche les informations d'une autre table que vous pouvez entrer dans le champ.</span><span class="sxs-lookup"><span data-stu-id="e865c-119">Lookup - Displays information from another table that you can enter in the field.</span></span> <span data-ttu-id="e865c-120">Vous pouvez sélectionner un élément à la fois.</span><span class="sxs-lookup"><span data-stu-id="e865c-120">You can select one piece of data at a time.</span></span>  

-   <span data-ttu-id="e865c-121">Consulter - Affiche les options qui existent pour le champ.</span><span class="sxs-lookup"><span data-stu-id="e865c-121">Drop-down - Displays the set of options that exist for the field.</span></span> <span data-ttu-id="e865c-122">Vous ne pouvez sélectionner qu'une des options.</span><span class="sxs-lookup"><span data-stu-id="e865c-122">You can select only one of the options.</span></span>  

<!--Onprem ## Copy Fields or Lines  
 Depending on the type of writable document, you can copy individual line fields or whole lines to other lines in the document. Read-only data, such as posted entries, cannot be copied.  

 Several database dependencies are used to determine if fields or lines can be copied. One way to determine these dependencies is to view the shortcut menu. The content of the shortcut menu indicates which copy functions are supported by displaying either of these functions:  

-   Copy Cell  

-   Copy Rows  

-   Paste Rows  

 For example, database records, such as lines on a sales order, and master data, such as cards on the **Items** page, cannot be duplicated. For this kind of data, the shortcut menu typically has the **Copy Cell** or **Copy Rows**  functions. If the **Paste** function is not available this indicates that you can only paste the data into external documents. Single fields on a sales line, however, can be copied to the same column in other sales lines.  

 Journal lines are very flexible and can be copied freely in the same journal, indicated by the presence of **Paste** on the shortcut menu.  

> [!NOTE]  
>   If you copy a journal line or document line, the fields that are not in your view are not copied to the new line.

#### To copy previous field  

-   To enter the value of the field immediately above the active field, select **Copy Previous** from the shortcut menu.-->

## <a name="entering-quantities-by-calculation"></a><span data-ttu-id="e865c-123">Saisie de quantités par calcul</span><span class="sxs-lookup"><span data-stu-id="e865c-123">Entering Quantities by Calculation</span></span>  
 <span data-ttu-id="e865c-124">Lors de la saisie de nombres dans les champs de quantité, tels que le champ **Quantité** d'une ligne feuille article, vous pouvez entrer la formule plutôt que la somme des quantités.</span><span class="sxs-lookup"><span data-stu-id="e865c-124">When entering numbers into quantity fields, such as the **Quantity** field on an item journal line, you can enter the formula instead of the sum quantity.</span></span>  

## <a name="examples"></a><span data-ttu-id="e865c-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="e865c-125">Examples</span></span>  

-   <span data-ttu-id="e865c-126">Si vous entrez 19+19, le champ est renseigné à l'aide du nombre 38.</span><span class="sxs-lookup"><span data-stu-id="e865c-126">If you enter 19+19, the field is calculated to 38.</span></span>  

-   <span data-ttu-id="e865c-127">Si vous entrez 41-9, le champ est renseigné à l'aide du nombre 32.</span><span class="sxs-lookup"><span data-stu-id="e865c-127">If you enter 41-9, the field is calculated to 32.</span></span>  

-   <span data-ttu-id="e865c-128">Si vous entrez 12\*4, le champ est renseigné à l'aide du nombre 48.</span><span class="sxs-lookup"><span data-stu-id="e865c-128">If you enter 12\*4, the field is calculated to 48.</span></span>  

-   <span data-ttu-id="e865c-129">Si vous entrez 12/4, le champ est renseigné à l'aide du nombre 3.</span><span class="sxs-lookup"><span data-stu-id="e865c-129">If you enter 12/4, the field is calculated to 3.</span></span>  

## <a name="entering-negative-numbers"></a><span data-ttu-id="e865c-130">Saisie de chiffres négatifs</span><span class="sxs-lookup"><span data-stu-id="e865c-130">Entering Negative Numbers</span></span>
<span data-ttu-id="e865c-131">Vous pouvez saisir des chiffres négatifs de deux manières.</span><span class="sxs-lookup"><span data-stu-id="e865c-131">You can enter negative numbers in two ways.</span></span> <span data-ttu-id="e865c-132">Le numéro -20,5 peut être saisi de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="e865c-132">The number -20.5 can be entered as:</span></span>  

-   <span data-ttu-id="e865c-133">-20,5</span><span class="sxs-lookup"><span data-stu-id="e865c-133">-20.5</span></span>  

    <span data-ttu-id="e865c-134">Ou</span><span class="sxs-lookup"><span data-stu-id="e865c-134">or</span></span>
-   <span data-ttu-id="e865c-135">20,5-</span><span class="sxs-lookup"><span data-stu-id="e865c-135">20.5-</span></span>  

 <span data-ttu-id="e865c-136">Dans les deux cas, le montant est enregistré comme -20,5.</span><span class="sxs-lookup"><span data-stu-id="e865c-136">In both cases, the amount will be recorded in as -20.5.</span></span>  

 <span data-ttu-id="e865c-137">Si le dernier caractère de l'expression est **+** ou **-**, l'expression entière est enregistrée avec ce caractère.</span><span class="sxs-lookup"><span data-stu-id="e865c-137">If the last character of the expression is a **+** or a **-**, the entire expression will be recorded with that sign.</span></span> <span data-ttu-id="e865c-138">Par exemple, **10-20+** aboutira à 10 et non -10.</span><span class="sxs-lookup"><span data-stu-id="e865c-138">An example, **10-20+** will result in 10 and not -10.</span></span>  

## <a name="entering-dates-and-times"></a><span data-ttu-id="e865c-139">Saisie de dates et d'heures</span><span class="sxs-lookup"><span data-stu-id="e865c-139">Entering Dates and Times</span></span>
<span data-ttu-id="e865c-140">Vous pouvez entrer des dates et des heures dans tous les champs affectés spécifiquement à des dates (champs Date).</span><span class="sxs-lookup"><span data-stu-id="e865c-140">You can enter dates and times in all the fields that are specifically assigned to dates (date fields).</span></span> <span data-ttu-id="e865c-141">Vous pouvez saisir les dates avec ou sans séparateurs.</span><span class="sxs-lookup"><span data-stu-id="e865c-141">You can enter dates with or without separators.</span></span>

> [!NOTE]  
> <span data-ttu-id="e865c-142">Le mode de saisie des dates et heures dépend des paramètres **Région**.</span><span class="sxs-lookup"><span data-stu-id="e865c-142">How you enter dates and times depends on your **Region** settings.</span></span> <span data-ttu-id="e865c-143">Pour plus d'informations, voir [Modification des paramètres de base](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="e865c-143">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>  

### <a name="entering-dates"></a><span data-ttu-id="e865c-144">Saisie de dates</span><span class="sxs-lookup"><span data-stu-id="e865c-144">Entering Dates</span></span>  
 <span data-ttu-id="e865c-145">Vous pouvez saisir deux, quatre, six ou huit chiffres dans un champ date :</span><span class="sxs-lookup"><span data-stu-id="e865c-145">In a date field you can enter two, four, six, or eight digits:</span></span>  

-   <span data-ttu-id="e865c-146">Si vous ne saisissez que deux chiffres, ils sont interprétés comme le jour, et le mois et l'année de la date de travail sont ajoutés.</span><span class="sxs-lookup"><span data-stu-id="e865c-146">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>  

-   <span data-ttu-id="e865c-147">Si vous saisissez quatre chiffres, ils sont interprétés comme le jour et le mois, et l'année de la date de travail est ajoutée.</span><span class="sxs-lookup"><span data-stu-id="e865c-147">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span>  

-   <span data-ttu-id="e865c-148">Si la date que vous souhaitez saisir est comprise entre le 01/01/1930 et le 31/12/2029, vous pouvez saisir les deux chiffres de l'année ; sinon saisissez les quatre chiffres.</span><span class="sxs-lookup"><span data-stu-id="e865c-148">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>  

 <span data-ttu-id="e865c-149">Vous pouvez aussi saisir une date sous forme de jour de la semaine suivi par un numéro de semaine et, éventuellement, une année (par exemple, Lun25 ou lun25 signifie le lundi de la semaine 25).</span><span class="sxs-lookup"><span data-stu-id="e865c-149">You can also enter a date as a weekday followed by a week number and, optionally, a year (for example, Mon25 or mon25 means Monday in week 25).</span></span>  

 <span data-ttu-id="e865c-150">Au lieu de saisir une date spécifique, vous pouvez saisir l'un des deux codes suivants.</span><span class="sxs-lookup"><span data-stu-id="e865c-150">Instead of entering a specific date, you can enter one of two codes.</span></span>  

|<span data-ttu-id="e865c-151">Code</span><span class="sxs-lookup"><span data-stu-id="e865c-151">Code</span></span>|<span data-ttu-id="e865c-152">Résultat</span><span class="sxs-lookup"><span data-stu-id="e865c-152">Result</span></span>|  
|--------------|----------------|  
|<span data-ttu-id="e865c-153">a</span><span class="sxs-lookup"><span data-stu-id="e865c-153">t</span></span>|<span data-ttu-id="e865c-154">Il s'agit de la date du jour (la date système de l'ordinateur).</span><span class="sxs-lookup"><span data-stu-id="e865c-154">This is today's date (the system date for the computer).</span></span>|  
|<span data-ttu-id="e865c-155">t</span><span class="sxs-lookup"><span data-stu-id="e865c-155">w</span></span>|<span data-ttu-id="e865c-156">Il s'agit de la date de travail configurée dans l'application.</span><span class="sxs-lookup"><span data-stu-id="e865c-156">This is the work date that is setup in the application.</span></span> <span data-ttu-id="e865c-157">Pour modifier la date de travail, voir [Modification des paramètres de base](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="e865c-157">To change the work date, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span> <span data-ttu-id="e865c-158">Vous souhaiterez peut-être utiliser une date de travail si vous avez beaucoup de transactions avec une date différente de la date d'aujourd'hui.</span><span class="sxs-lookup"><span data-stu-id="e865c-158">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>|  

<!--Onprem ## Closing Date  
 When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry. A closing date technically is between two dates, for example between Dec 31 and Jan 1.  

 To specify that a date is a closing date, put C just before the date: C123101. -->

## <a name="entering-times"></a><span data-ttu-id="e865c-159">Saisie des heures</span><span class="sxs-lookup"><span data-stu-id="e865c-159">Entering Times</span></span>  
 <span data-ttu-id="e865c-160">Lorsque vous saisissez des heures, vous pouvez insérer n'importe quel type de séparateur entre les unités, mais cette opération est facultative.</span><span class="sxs-lookup"><span data-stu-id="e865c-160">When you enter times, you can insert any separator sign that you want between the units, but it is not required.</span></span> <span data-ttu-id="e865c-161">Vous n'avez pas besoin d'ajouter la mention « minutes », « secondes » ou « AM/PM ».</span><span class="sxs-lookup"><span data-stu-id="e865c-161">You do not have to write minutes, seconds, or AM/PM.</span></span>  

 <span data-ttu-id="e865c-162">Le tableau suivant répertorie les différents formats de saisie possibles pour les heures, ainsi que leur interprétation.</span><span class="sxs-lookup"><span data-stu-id="e865c-162">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span>  

|<span data-ttu-id="e865c-163">Écriture</span><span class="sxs-lookup"><span data-stu-id="e865c-163">Entry</span></span>|<span data-ttu-id="e865c-164">Interprétation</span><span class="sxs-lookup"><span data-stu-id="e865c-164">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="e865c-165">5</span><span class="sxs-lookup"><span data-stu-id="e865c-165">5</span></span>|<span data-ttu-id="e865c-166">05:00:00</span><span class="sxs-lookup"><span data-stu-id="e865c-166">05:00:00</span></span>|  
|<span data-ttu-id="e865c-167">5:30</span><span class="sxs-lookup"><span data-stu-id="e865c-167">5:30</span></span>|<span data-ttu-id="e865c-168">05:30:00</span><span class="sxs-lookup"><span data-stu-id="e865c-168">05:30:00</span></span>|  
|<span data-ttu-id="e865c-169">0530</span><span class="sxs-lookup"><span data-stu-id="e865c-169">0530</span></span>|<span data-ttu-id="e865c-170">05:30:00</span><span class="sxs-lookup"><span data-stu-id="e865c-170">05:30:00</span></span>|  
|<span data-ttu-id="e865c-171">5:30:5</span><span class="sxs-lookup"><span data-stu-id="e865c-171">5:30:5</span></span>|<span data-ttu-id="e865c-172">05:30:05</span><span class="sxs-lookup"><span data-stu-id="e865c-172">05:30:05</span></span>|  
|<span data-ttu-id="e865c-173">053005</span><span class="sxs-lookup"><span data-stu-id="e865c-173">053005</span></span>|<span data-ttu-id="e865c-174">05:30:05</span><span class="sxs-lookup"><span data-stu-id="e865c-174">05:30:05</span></span>|  
|<span data-ttu-id="e865c-175">5:30:5,50</span><span class="sxs-lookup"><span data-stu-id="e865c-175">5:30:5,50</span></span>|<span data-ttu-id="e865c-176">05:30:05.5</span><span class="sxs-lookup"><span data-stu-id="e865c-176">05:30:05.5</span></span>|  
|<span data-ttu-id="e865c-177">053005050</span><span class="sxs-lookup"><span data-stu-id="e865c-177">053005050</span></span>|<span data-ttu-id="e865c-178">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="e865c-178">05:30:05.05</span></span>|  

 <span data-ttu-id="e865c-179">Vous devez saisir deux chiffres par unité temporelle si vous n'utilisez pas de séparateur.</span><span class="sxs-lookup"><span data-stu-id="e865c-179">You must enter two digits for each unit of time if you do not enter a separator.</span></span>  

## <a name="entering-datetimes"></a><span data-ttu-id="e865c-180">Saisie des dates/heures</span><span class="sxs-lookup"><span data-stu-id="e865c-180">Entering Datetimes</span></span>  
 <span data-ttu-id="e865c-181">Lors de la saisie des dates/heures, vous devez saisir un espace entre la date et l'heure.</span><span class="sxs-lookup"><span data-stu-id="e865c-181">When you enter datetimes you must enter a space between the date and the time.</span></span>  

 <span data-ttu-id="e865c-182">Le tableau suivant répertorie les différents formats de saisie possibles pour les dates/heures, ainsi que leur interprétation.</span><span class="sxs-lookup"><span data-stu-id="e865c-182">The following table lists the various ways in which you can enter datetimes and how they are interpreted.</span></span>  

|<span data-ttu-id="e865c-183">Écriture</span><span class="sxs-lookup"><span data-stu-id="e865c-183">Entry</span></span>|<span data-ttu-id="e865c-184">Interprétation</span><span class="sxs-lookup"><span data-stu-id="e865c-184">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="e865c-185">131202 132455</span><span class="sxs-lookup"><span data-stu-id="e865c-185">131202 132455</span></span>|<span data-ttu-id="e865c-186">13-12-02 13:24:55</span><span class="sxs-lookup"><span data-stu-id="e865c-186">13-12-02 13:24:55</span></span>|  
|<span data-ttu-id="e865c-187">1-12-02 10</span><span class="sxs-lookup"><span data-stu-id="e865c-187">1-12-02 10</span></span>|<span data-ttu-id="e865c-188">01-12-02 10:00:00</span><span class="sxs-lookup"><span data-stu-id="e865c-188">01-12-02 10:00:00</span></span>|  
|<span data-ttu-id="e865c-189">1.12.02 5</span><span class="sxs-lookup"><span data-stu-id="e865c-189">1.12.02 5</span></span>|<span data-ttu-id="e865c-190">01/12/02 05:00:00</span><span class="sxs-lookup"><span data-stu-id="e865c-190">01-12-02 05:00:00</span></span>|  
|<span data-ttu-id="e865c-191">1.12.02</span><span class="sxs-lookup"><span data-stu-id="e865c-191">1.12.02</span></span>|<span data-ttu-id="e865c-192">01/12/02 00:00:00</span><span class="sxs-lookup"><span data-stu-id="e865c-192">01-12-02 00:00:00</span></span>|  
|<span data-ttu-id="e865c-193">11/12</span><span class="sxs-lookup"><span data-stu-id="e865c-193">11 12</span></span>|<span data-ttu-id="e865c-194">11-mois en cours-année en cours 12:00:00</span><span class="sxs-lookup"><span data-stu-id="e865c-194">11-current month-current year 12:00:00</span></span>|  
|<span data-ttu-id="e865c-195">1112 12</span><span class="sxs-lookup"><span data-stu-id="e865c-195">1112 12</span></span>|<span data-ttu-id="e865c-196">11-12-année en cours 12:00:00</span><span class="sxs-lookup"><span data-stu-id="e865c-196">11-12-current year 12:00:00</span></span>|  
|<span data-ttu-id="e865c-197">a ou date du jour</span><span class="sxs-lookup"><span data-stu-id="e865c-197">t or today</span></span>|<span data-ttu-id="e865c-198">date du jour 00:00:00</span><span class="sxs-lookup"><span data-stu-id="e865c-198">today's date 00:00:00</span></span>|  
|<span data-ttu-id="e865c-199">heure h</span><span class="sxs-lookup"><span data-stu-id="e865c-199">t time</span></span>|<span data-ttu-id="e865c-200">date du jour heure réelle</span><span class="sxs-lookup"><span data-stu-id="e865c-200">today's date actual time</span></span>|  
|<span data-ttu-id="e865c-201">a 10:30</span><span class="sxs-lookup"><span data-stu-id="e865c-201">t 10:30</span></span>|<span data-ttu-id="e865c-202">date du jour 10:30:00</span><span class="sxs-lookup"><span data-stu-id="e865c-202">today's date 10:30:00</span></span>|  
|<span data-ttu-id="e865c-203">a 3:3:3</span><span class="sxs-lookup"><span data-stu-id="e865c-203">t 3:3:3</span></span>|<span data-ttu-id="e865c-204">date du jour 03:03:03</span><span class="sxs-lookup"><span data-stu-id="e865c-204">today's date 03:03:03</span></span>|  
|<span data-ttu-id="e865c-205">t ou date de travail</span><span class="sxs-lookup"><span data-stu-id="e865c-205">w or workdate</span></span>|<span data-ttu-id="e865c-206">date de travail 00:00:00</span><span class="sxs-lookup"><span data-stu-id="e865c-206">the working date 00:00:00</span></span>|  
|<span data-ttu-id="e865c-207">lu ou lundi</span><span class="sxs-lookup"><span data-stu-id="e865c-207">m or Monday</span></span>|<span data-ttu-id="e865c-208">Lundi de la semaine en cours 00:00:00</span><span class="sxs-lookup"><span data-stu-id="e865c-208">Monday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="e865c-209">ma ou mardi</span><span class="sxs-lookup"><span data-stu-id="e865c-209">tu or Tuesday</span></span>|<span data-ttu-id="e865c-210">Mardi de la semaine en cours 00:00:00</span><span class="sxs-lookup"><span data-stu-id="e865c-210">Tuesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="e865c-211">me ou mercredi</span><span class="sxs-lookup"><span data-stu-id="e865c-211">we or Wednesday</span></span>|<span data-ttu-id="e865c-212">Mercredi de la semaine en cours 00:00:00</span><span class="sxs-lookup"><span data-stu-id="e865c-212">Wednesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="e865c-213">je ou jeudi</span><span class="sxs-lookup"><span data-stu-id="e865c-213">th or Thursday</span></span>|<span data-ttu-id="e865c-214">Jeudi de la semaine en cours 00:00:00</span><span class="sxs-lookup"><span data-stu-id="e865c-214">Thursday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="e865c-215">ve ou vendredi</span><span class="sxs-lookup"><span data-stu-id="e865c-215">f or Friday</span></span>|<span data-ttu-id="e865c-216">Vendredi de la semaine en cours 00:00:00</span><span class="sxs-lookup"><span data-stu-id="e865c-216">Friday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="e865c-217">sa ou samedi</span><span class="sxs-lookup"><span data-stu-id="e865c-217">s or Saturday</span></span>|<span data-ttu-id="e865c-218">Samedi de la semaine en cours 00:00:00</span><span class="sxs-lookup"><span data-stu-id="e865c-218">Saturday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="e865c-219">di ou dimanche</span><span class="sxs-lookup"><span data-stu-id="e865c-219">su or Sunday</span></span>|<span data-ttu-id="e865c-220">Dimanche de la semaine en cours 00:00:00</span><span class="sxs-lookup"><span data-stu-id="e865c-220">Sunday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="e865c-221">ma 10:30</span><span class="sxs-lookup"><span data-stu-id="e865c-221">tu 10:30</span></span>|<span data-ttu-id="e865c-222">Mardi de la semaine en cours 10:30:00</span><span class="sxs-lookup"><span data-stu-id="e865c-222">Tuesday of the current week 10:30:00</span></span>|  
|<span data-ttu-id="e865c-223">ma 3:3:3</span><span class="sxs-lookup"><span data-stu-id="e865c-223">tu 3:3:3</span></span>|<span data-ttu-id="e865c-224">Mardi de la semaine en cours 03:03:03</span><span class="sxs-lookup"><span data-stu-id="e865c-224">Tuesday of the current week 03:03:03</span></span>|  

## <a name="entering-duration"></a><span data-ttu-id="e865c-225">Saisie des durées</span><span class="sxs-lookup"><span data-stu-id="e865c-225">Entering Duration</span></span>  
 <span data-ttu-id="e865c-226">Vous devez saisir les durées sous la forme d'un chiffre suivi d'une unité de mesure.</span><span class="sxs-lookup"><span data-stu-id="e865c-226">You enter a duration as a number followed by its unit of measure.</span></span>  

 <span data-ttu-id="e865c-227">Voilà quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="e865c-227">Here are some examples.</span></span>  

|<span data-ttu-id="e865c-228">Durée</span><span class="sxs-lookup"><span data-stu-id="e865c-228">Duration</span></span>|<span data-ttu-id="e865c-229">Unité\*\*</span><span class="sxs-lookup"><span data-stu-id="e865c-229">Unit of measure\*\*</span></span>|  
|------------------|-------------------------|  
|<span data-ttu-id="e865c-230">2h</span><span class="sxs-lookup"><span data-stu-id="e865c-230">2h</span></span>|<span data-ttu-id="e865c-231">2 heures</span><span class="sxs-lookup"><span data-stu-id="e865c-231">2 hrs</span></span>|  
|<span data-ttu-id="e865c-232">6h 30m</span><span class="sxs-lookup"><span data-stu-id="e865c-232">6h 30 m</span></span>|<span data-ttu-id="e865c-233">6 heures 30 minutes</span><span class="sxs-lookup"><span data-stu-id="e865c-233">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="e865c-234">6,5h</span><span class="sxs-lookup"><span data-stu-id="e865c-234">6.5h</span></span>|<span data-ttu-id="e865c-235">6 heures 30 minutes</span><span class="sxs-lookup"><span data-stu-id="e865c-235">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="e865c-236">90m</span><span class="sxs-lookup"><span data-stu-id="e865c-236">90m</span></span>|<span data-ttu-id="e865c-237">1 heure 30 minutes</span><span class="sxs-lookup"><span data-stu-id="e865c-237">1 hr 30 mins</span></span>|  
|<span data-ttu-id="e865c-238">2j 6h 30m</span><span class="sxs-lookup"><span data-stu-id="e865c-238">2d 6h 30m</span></span>|<span data-ttu-id="e865c-239">2 jours 6 heures 30 minutes</span><span class="sxs-lookup"><span data-stu-id="e865c-239">2 days 6 hrs 30 mins</span></span>|  
|<span data-ttu-id="e865c-240">2j 6h 30m 56s 600ms</span><span class="sxs-lookup"><span data-stu-id="e865c-240">2d 6h 30m 56s 600ms</span></span>|<span data-ttu-id="e865c-241">2 jours 6 h 30 m 56 s 600 ms</span><span class="sxs-lookup"><span data-stu-id="e865c-241">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|  

 <span data-ttu-id="e865c-242">Vous pouvez également saisir un nombre automatiquement converti en durée.</span><span class="sxs-lookup"><span data-stu-id="e865c-242">You can also enter a number and it is automatically converted to a duration.</span></span> <span data-ttu-id="e865c-243">Le nombre saisi est converti en fonction de l'unité de mesure par défaut spécifiée pour le champ de durée.</span><span class="sxs-lookup"><span data-stu-id="e865c-243">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>  

 <span data-ttu-id="e865c-244">Pour connaître l'unité de mesure utilisée pour un champ de durée, saisissez un nombre et observez l'unité de mesure dans laquelle il est convertit.</span><span class="sxs-lookup"><span data-stu-id="e865c-244">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>  

 <span data-ttu-id="e865c-245">Si l'unité est « heures », 5 est converti en 5h.</span><span class="sxs-lookup"><span data-stu-id="e865c-245">The number 5 is converted to 5 hrs, if the unit of measure is hours.</span></span>  

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

## <a name="using-date-formulas"></a><span data-ttu-id="e865c-246">Utilisation de formules date</span><span class="sxs-lookup"><span data-stu-id="e865c-246">Using Date Formulas</span></span>  
 <span data-ttu-id="e865c-247">Une formule date est une combinaison abrégée de lettres et de nombres qui spécifie comment calculer les dates.</span><span class="sxs-lookup"><span data-stu-id="e865c-247">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="e865c-248">Vous pouvez entrer des formules date dans divers champs de calcul de date et dans les champs périodicité récurrente des feuilles récurrentes.</span><span class="sxs-lookup"><span data-stu-id="e865c-248">You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="e865c-249">Dans tous les champs formule de données, un jour est automatiquement inclus pour couvrir le jour de début de la période.</span><span class="sxs-lookup"><span data-stu-id="e865c-249">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="e865c-250">Par conséquent, si vous saisissez 1s, par exemple, la période est bien huit jours parce que aujourd'hui est inclus.</span><span class="sxs-lookup"><span data-stu-id="e865c-250">Accordingly, if you enter 1W, for example, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="e865c-251">Pour définir une période de sept jours (une vraie semaine) avec la date début de la période, vous devez saisir 6D ou 1W-1D.</span><span class="sxs-lookup"><span data-stu-id="e865c-251">To specify a period of seven days (one true week) including the period starting date, then you must enter 6D or 1W-1D.</span></span>  

 <span data-ttu-id="e865c-252">Voici quelques exemples d'utilisation de formules date :</span><span class="sxs-lookup"><span data-stu-id="e865c-252">Here are some examples of how date formulas can be used:</span></span>  

-   <span data-ttu-id="e865c-253">La formule date du champ périodicité récurrente des feuilles récurrentes détermine la fréquence de validation de l'écriture de la ligne feuille.</span><span class="sxs-lookup"><span data-stu-id="e865c-253">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>  

-   <span data-ttu-id="e865c-254">La formule date du champ Période de carence pour un niveau de relance précis détermine la période qui doit se passer entre la date d'échéance (ou la date de la relance précédente) avant la création d'une nouvelle relance.</span><span class="sxs-lookup"><span data-stu-id="e865c-254">The date formula in the Grace Period field for a specified reminder level determines the period of time that must pass from the due date (or from the date of the previous reminder) before a reminder will be created.</span></span>  

-   <span data-ttu-id="e865c-255">La formule date du champ Calcul date échéance détermine la manière dont la date d'échéance de la relance est calculée.</span><span class="sxs-lookup"><span data-stu-id="e865c-255">The date formula in the Due Date Calculation field determines how to calculate the due date on the reminder.</span></span>  

 <span data-ttu-id="e865c-256">La formule de calcul de la date peut comprendre un maximum de 20 caractères, des chiffres et des lettres.</span><span class="sxs-lookup"><span data-stu-id="e865c-256">The date calculation formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="e865c-257">Vous pouvez utiliser les lettres suivantes qui sont des abréviations de spécifications de temps.</span><span class="sxs-lookup"><span data-stu-id="e865c-257">You can use the following letters, which are abbreviations for time specifications.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="e865c-258">C</span><span class="sxs-lookup"><span data-stu-id="e865c-258">C</span></span>|<span data-ttu-id="e865c-259">Courant</span><span class="sxs-lookup"><span data-stu-id="e865c-259">Current</span></span>|  
|<span data-ttu-id="e865c-260">J</span><span class="sxs-lookup"><span data-stu-id="e865c-260">D</span></span>|<span data-ttu-id="e865c-261">Jour(s)</span><span class="sxs-lookup"><span data-stu-id="e865c-261">Day(s)</span></span>|  
|<span data-ttu-id="e865c-262">S</span><span class="sxs-lookup"><span data-stu-id="e865c-262">W</span></span>|<span data-ttu-id="e865c-263">Semaine(s)</span><span class="sxs-lookup"><span data-stu-id="e865c-263">Week(s)</span></span>|  
|<span data-ttu-id="e865c-264">M</span><span class="sxs-lookup"><span data-stu-id="e865c-264">M</span></span>|<span data-ttu-id="e865c-265">Mois</span><span class="sxs-lookup"><span data-stu-id="e865c-265">Month(s)</span></span>|  
|<span data-ttu-id="e865c-266">T</span><span class="sxs-lookup"><span data-stu-id="e865c-266">Q</span></span>|<span data-ttu-id="e865c-267">Trimestre(s)</span><span class="sxs-lookup"><span data-stu-id="e865c-267">Quarter(s)</span></span>|  
|<span data-ttu-id="e865c-268">A</span><span class="sxs-lookup"><span data-stu-id="e865c-268">Y</span></span>|<span data-ttu-id="e865c-269">Année(s)</span><span class="sxs-lookup"><span data-stu-id="e865c-269">Year(s)</span></span>|  

 <span data-ttu-id="e865c-270">Vous pouvez construire la formule date de trois manières.</span><span class="sxs-lookup"><span data-stu-id="e865c-270">You can construct a date formula in three ways.</span></span>  

 <span data-ttu-id="e865c-271">L'exemple suivant indique comment définir un courant plus unité temporelle.</span><span class="sxs-lookup"><span data-stu-id="e865c-271">The following example shows how current plus a time unit.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="e865c-272">CS</span><span class="sxs-lookup"><span data-stu-id="e865c-272">CW</span></span>|<span data-ttu-id="e865c-273">Semaine en cours</span><span class="sxs-lookup"><span data-stu-id="e865c-273">Current week</span></span>|  
|<span data-ttu-id="e865c-274">CM</span><span class="sxs-lookup"><span data-stu-id="e865c-274">CM</span></span>|<span data-ttu-id="e865c-275">Mois en cours</span><span class="sxs-lookup"><span data-stu-id="e865c-275">Current month</span></span>|  

 <span data-ttu-id="e865c-276">L'exemple suivant indique comment définir un chiffre et une unité de temps.</span><span class="sxs-lookup"><span data-stu-id="e865c-276">The following example shows how a number and a time unit.</span></span> <span data-ttu-id="e865c-277">Un chiffre ne peut pas être supérieur à 9999.</span><span class="sxs-lookup"><span data-stu-id="e865c-277">A number cannot be larger than 9999.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="e865c-278">10J</span><span class="sxs-lookup"><span data-stu-id="e865c-278">10D</span></span>|<span data-ttu-id="e865c-279">10 jours à dater d'aujourd'hui</span><span class="sxs-lookup"><span data-stu-id="e865c-279">10 days from today</span></span>|  
|<span data-ttu-id="e865c-280">2S</span><span class="sxs-lookup"><span data-stu-id="e865c-280">2W</span></span>|<span data-ttu-id="e865c-281">2 semaines à dater d'aujourd'hui</span><span class="sxs-lookup"><span data-stu-id="e865c-281">2 weeks from today</span></span>|  

 <span data-ttu-id="e865c-282">L'exemple suivant indique comment définir une unité de temps et un chiffre.</span><span class="sxs-lookup"><span data-stu-id="e865c-282">The following example shows how a time unit and a number.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="e865c-283">J10</span><span class="sxs-lookup"><span data-stu-id="e865c-283">D10</span></span>|<span data-ttu-id="e865c-284">Le dixième jour du mois suivant</span><span class="sxs-lookup"><span data-stu-id="e865c-284">The next 10th day of a month</span></span>|  
|<span data-ttu-id="e865c-285">JS4</span><span class="sxs-lookup"><span data-stu-id="e865c-285">WD4</span></span>|<span data-ttu-id="e865c-286">Le quatrième jour de la semaine (jeudi)</span><span class="sxs-lookup"><span data-stu-id="e865c-286">The next 4th day of a week (Thursday)</span></span>|  

 <span data-ttu-id="e865c-287">L'exemple suivant indique comment combiner ces trois formules.</span><span class="sxs-lookup"><span data-stu-id="e865c-287">The following example shows how you can combine these three forms as needed.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="e865c-288">CM+10J</span><span class="sxs-lookup"><span data-stu-id="e865c-288">CM+10D</span></span>|<span data-ttu-id="e865c-289">Mois en cours + 10 jours</span><span class="sxs-lookup"><span data-stu-id="e865c-289">Current month + 10 days</span></span>|  

 <span data-ttu-id="e865c-290">L'exemple ci-dessous illustre comment vous pouvez utiliser le signe moins pour indiquer une date du passé.</span><span class="sxs-lookup"><span data-stu-id="e865c-290">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="e865c-291">-1A</span><span class="sxs-lookup"><span data-stu-id="e865c-291">-1Y</span></span>|<span data-ttu-id="e865c-292">Il y a 1 an à dater d'aujourd'hui</span><span class="sxs-lookup"><span data-stu-id="e865c-292">1 year ago from today</span></span>|  

<!--OnPrem > [!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->  
## <a name="see-also"></a><span data-ttu-id="e865c-293">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e865c-293">See Also</span></span>  
 [<span data-ttu-id="e865c-294">Tri, recherche et filtrage de listes</span><span class="sxs-lookup"><span data-stu-id="e865c-294">Sorting, Searching, and Filtering Lists</span></span>](ui-enter-criteria-filters.md)  
 <span data-ttu-id="e865c-295">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e865c-295">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>