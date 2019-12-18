---
title: Procédure de configuration des calendriers usine | Microsoft Docs
description: Les calendriers de centre de charge spécifient les jours ouvrés et les heures de travail, les équipes, les jours fériés et les absences déterminant la capacité disponible brute du centre de charge, mesurée en unités de temps, en fonction des valeurs d'efficacité et de capacité définies. La création et l'activation d'un calendrier de centre de charge nécessite plusieurs étapes préliminaires.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: cc40361150d8368c46f9045451c0d542eff13779
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877966"
---
# <a name="set-up-shop-calendars"></a><span data-ttu-id="81482-104">Paramétrer des calendriers usine</span><span class="sxs-lookup"><span data-stu-id="81482-104">Set Up Shop Calendars</span></span>
<span data-ttu-id="81482-105">Les calendriers de centre de charge ou de poste de charge spécifient les jours ouvrés et les heures de travail, les équipes, les jours fériés et les absences déterminant la capacité disponible brute du centre de charge, mesurée en unités de temps, en fonction des valeurs d'efficacité et de capacité définies.</span><span class="sxs-lookup"><span data-stu-id="81482-105">A work center or machine calendar specifies the working days and hours, shifts, holidays, and absences that determine the center’s gross available capacity, measured in time, according to its defined efficiency and capacity values.</span></span>

<span data-ttu-id="81482-106">Avant de calculer un calendrier de centre de charge ou de poste de charge spécifique, vous devez définir un ou plusieurs calendriers usine généraux.</span><span class="sxs-lookup"><span data-stu-id="81482-106">As a foundation for calculating a specific work or machine center calendar, you must first set up one or more general shop calendars.</span></span> <span data-ttu-id="81482-107">Les calendriers usine définissent la semaine de travail standard en fonction des heures de début et de fin de chaque jour ouvré et des changements d'équipe.</span><span class="sxs-lookup"><span data-stu-id="81482-107">A shop calendar defines a standard work week according to start and end times of each working day and the work shift relation.</span></span> <span data-ttu-id="81482-108">En outre, ils déterminent les jours fériés fixes de l'année.</span><span class="sxs-lookup"><span data-stu-id="81482-108">In addition, the shop calendar defines the fixed holidays during a year.</span></span>  

<span data-ttu-id="81482-109">La procédure suivante décrit comment configurer des calendriers de centre de charge.</span><span class="sxs-lookup"><span data-stu-id="81482-109">The following describes how to set up work center calendars.</span></span> <span data-ttu-id="81482-110">Les étapes sont similaires lorsque vous configurez des calendriers de poste de charge.</span><span class="sxs-lookup"><span data-stu-id="81482-110">The steps are similar when setting up machine center calendars.</span></span>  

## <a name="to-create-work-shifts"></a><span data-ttu-id="81482-111">Pour créer des équipes</span><span class="sxs-lookup"><span data-stu-id="81482-111">To create work shifts</span></span>  
1.  <span data-ttu-id="81482-112">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Équipes**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="81482-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Work Shifts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="81482-113">Sur une ligne blanche, entrez le numéro d'identification de l'équipe, par exemple, **1**, dans le champ **Code**.</span><span class="sxs-lookup"><span data-stu-id="81482-113">On a blank line, enter a number in the **Code** field to identify the work shift, for example, **1**.</span></span>  
3.  <span data-ttu-id="81482-114">Dans le champ **Désignation**, entrez la désignation de l'équipe, par exemple, **1ère équipe**.</span><span class="sxs-lookup"><span data-stu-id="81482-114">Describe the work shift in the **Description** field, for example, **1st shift**.</span></span>  
4.  <span data-ttu-id="81482-115">Vous pouvez également renseignez les lignes d'une deuxième ou troisième équipe.</span><span class="sxs-lookup"><span data-stu-id="81482-115">Optionally, fill in lines for a second or third work shift.</span></span>  

<span data-ttu-id="81482-116">Même si vos centres de charge n'ont pas recours à diverses équipes, entrez au moins un code équipe.</span><span class="sxs-lookup"><span data-stu-id="81482-116">Even if your work centers do not work in different work shifts, enter at least one work shift code.</span></span>  

## <a name="to-set-up-a-shop-calendar"></a><span data-ttu-id="81482-117">Pour configurer un calendrier usine</span><span class="sxs-lookup"><span data-stu-id="81482-117">To set up a shop calendar</span></span>  
1.  <span data-ttu-id="81482-118">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Calendriers usine**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="81482-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shop Calendars**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="81482-119">Sur une ligne blanche, entrez le numéro d'identification du calendrier usine dans le champ **Code**.</span><span class="sxs-lookup"><span data-stu-id="81482-119">On a blank line, enter a number in the **Code** field to identify the shop calendar.</span></span>  
3.  <span data-ttu-id="81482-120">Dans le champ **Désignation**, entrez la désignation du calendrier usine.</span><span class="sxs-lookup"><span data-stu-id="81482-120">Describe the shop calendar in the **Description** field.</span></span>  
4.  <span data-ttu-id="81482-121">Choisissez l'action **Jours ouvrés**.</span><span class="sxs-lookup"><span data-stu-id="81482-121">Choose the **Working Days** action.</span></span>
5.  <span data-ttu-id="81482-122">Sur la page **Jours ouvrés calendrier usine**, définissez une semaine de travail complète, avec les heures de début et de fin pour chaque jour.</span><span class="sxs-lookup"><span data-stu-id="81482-122">On the **Shop Calendar Working Days** page, define a complete work week, with the start and end times for each day.</span></span>  

    <span data-ttu-id="81482-123">Dans le champ **Code équipe**, sélectionnez l'une des équipes que vous avez défini précédemment.</span><span class="sxs-lookup"><span data-stu-id="81482-123">In the **Work Shift Code** field, select one of the shifts that you previously defined.</span></span> <span data-ttu-id="81482-124">Ajoutez une ligne pour chaque jour ouvré et chaque équipe.</span><span class="sxs-lookup"><span data-stu-id="81482-124">Add a line for every working day and every shift.</span></span> <span data-ttu-id="81482-125">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="81482-125">For example:</span></span>  

    <span data-ttu-id="81482-126">Lundi 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="81482-126">Monday  07:00 15:00 1</span></span>   
    <span data-ttu-id="81482-127">Mardi 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="81482-127">Tuesday 07:00 15:00 1</span></span>  

    <span data-ttu-id="81482-128">Si vous avez besoin d'un calendrier usine intégrant deux équipes, vous devez le remplir de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="81482-128">If you need a shop calendar with two work shifts, you must fill it in in this manner:</span></span>  

    <span data-ttu-id="81482-129">Lundi 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="81482-129">Monday 07:00 15:00 1</span></span>   
    <span data-ttu-id="81482-130">Lundi 15:00 23:00 2</span><span class="sxs-lookup"><span data-stu-id="81482-130">Monday 15:00 23:00 2</span></span>  
    <span data-ttu-id="81482-131">Mardi 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="81482-131">Tuesday 07:00 15:00 1</span></span>  
    <span data-ttu-id="81482-132">Mardi 15:00 23:00 2</span><span class="sxs-lookup"><span data-stu-id="81482-132">Tuesday 15:00 23:00 2</span></span>  

    <span data-ttu-id="81482-133">Les jours non définis dans le calendrier usine, comme le samedi et le dimanche, sont considérés comme des jours chômés : une capacité disponible nulle leur est attribuée dans le calendrier de centre de charge.</span><span class="sxs-lookup"><span data-stu-id="81482-133">Any week days that you do not define in the shop calendar, such as Saturday and Sunday, are considered non-working days and will have zero available capacity in a work center calendar.</span></span>  

    <span data-ttu-id="81482-134">Une fois tous les jours ouvrés de la semaine définis, fermez la page **Jours ouvrés calendrier usine** et passez aux jours fériés.</span><span class="sxs-lookup"><span data-stu-id="81482-134">When all the working days of a week are defined, you can close the **Shop Calendar Working Days** page and proceed to enter holidays.</span></span>  

6.  <span data-ttu-id="81482-135">Sur la page **Calendriers usine**, sélectionnez le calendrier usine, puis choisissez l'action **Jours fériés**.</span><span class="sxs-lookup"><span data-stu-id="81482-135">On the **Shop Calendars** page, select the shop calendar, and then choose the **Holidays** action.</span></span>
7. <span data-ttu-id="81482-136">Sur la page **Jours fériés calendrier usine**, définissez les jours fériés de l'année en indiquant la date et l'heure de début, l'heure de fin et la description de chaque jour férié sur une ligne distincte.</span><span class="sxs-lookup"><span data-stu-id="81482-136">On the **Shop Calendar Holidays** page, define the holidays of the year by entering the start date and time, the end time, and description of each holiday on individual lines.</span></span> <span data-ttu-id="81482-137">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="81482-137">For example:</span></span>  

    <span data-ttu-id="81482-138">04/07/14 0:00:00 23:59:00 Vacances d'été</span><span class="sxs-lookup"><span data-stu-id="81482-138">04/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  
    <span data-ttu-id="81482-139">05/07/14 0:00:00 23:59:00 Vacances d'été</span><span class="sxs-lookup"><span data-stu-id="81482-139">05/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  
    <span data-ttu-id="81482-140">06/07/14 0:00:00 23:59:00 Vacances d'été</span><span class="sxs-lookup"><span data-stu-id="81482-140">06/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  

<span data-ttu-id="81482-141">Une capacité disponible nulle est attribuée aux jours fériés définis dans le calendrier du centre de charge.</span><span class="sxs-lookup"><span data-stu-id="81482-141">The defined holidays will have zero available capacity in a work center calendar.</span></span>  

<span data-ttu-id="81482-142">Le calendrier usine peut ensuite être attribué à un centre de charge pour calculer le calendrier usine qui régira la planification de toutes les opérations dans le temps au centre de charge.</span><span class="sxs-lookup"><span data-stu-id="81482-142">The shop calendar can now be assigned to a work center to calculate the work shop calendar that will govern all operation scheduling at that work center.</span></span>  

## <a name="to-calculate-a-work-center-calendar"></a><span data-ttu-id="81482-143">Pour calculer un calendrier de centre de charge</span><span class="sxs-lookup"><span data-stu-id="81482-143">To calculate a work center calendar</span></span>  

1.  <span data-ttu-id="81482-144">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Centres de charge**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="81482-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Work Centers**, and then choose the related link.</span></span>
2. <span data-ttu-id="81482-145">Ouvrez le centre de charge que vous voulez mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="81482-145">Open the work center that you want to update.</span></span>  
3. <span data-ttu-id="81482-146">Dans le champ **Code calendrier usine**, sélectionnez le calendrier usine à utiliser comme base pour le calendrier du centre de charge.</span><span class="sxs-lookup"><span data-stu-id="81482-146">In the **Shop Calendar Code** field, select which shop calendar to use as the foundation for a work center calendar.</span></span>  
4. <span data-ttu-id="81482-147">Sélectionnez l'action **Calendrier**.</span><span class="sxs-lookup"><span data-stu-id="81482-147">Choose the **Calendar** action.</span></span>  
5. <span data-ttu-id="81482-148">Sur la page **Calendrier centre de charge**, choisissez l'action **Afficher matrice**.</span><span class="sxs-lookup"><span data-stu-id="81482-148">On the **Work Center Calendar** page, choose the **Show Matrix** action.</span></span>  

    <span data-ttu-id="81482-149">Le côté gauche de la page de matrice répertorie les centres de charge configurés.</span><span class="sxs-lookup"><span data-stu-id="81482-149">The left side of the matrix page lists the work centers that are set up.</span></span> <span data-ttu-id="81482-150">Le côté droit contient un calendrier horaire indiquant les capacités disponibles pour chaque jour ouvré dans l'unité de mesure choisie, par exemple, **480** (minutes).</span><span class="sxs-lookup"><span data-stu-id="81482-150">The right side shows a calendar displaying the available capacity values for each working day in the defined unit of measure, for example, **480** minutes.</span></span> <span data-ttu-id="81482-151">Chaque ligne correspond au calendrier d'un centre de charge.</span><span class="sxs-lookup"><span data-stu-id="81482-151">Each line represents the calendar of one work center.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="81482-152">Vous pouvez également choisir d'afficher les valeurs de capacité pour chaque semaine ou mois en modifiant la sélection dans le champ **Afficher par** de la page **Calendrier centre de charge**.</span><span class="sxs-lookup"><span data-stu-id="81482-152">You can also select to view the capacity values for each week or month by changing the selection in the **View By** field on the **Work Center Calendar** page.</span></span>  

    <span data-ttu-id="81482-153">Le nouveau calendrier usine doit d'abord être calculé pour être répercuté dans une ligne du centre de charge sélectionné.</span><span class="sxs-lookup"><span data-stu-id="81482-153">To reflect the new shop calendar as a line on the selected work center, it must first be calculated.</span></span>  

6.  <span data-ttu-id="81482-154">Choisissez l'action **Calculer**.</span><span class="sxs-lookup"><span data-stu-id="81482-154">Choose the **Calculate** action.</span></span>  
7.  <span data-ttu-id="81482-155">Sur le raccourci **Centre de charge**, vous pouvez définir un filtre de manière à n'effectuer le calcul que pour un centre de charge.</span><span class="sxs-lookup"><span data-stu-id="81482-155">On the **Work Center** FastTab, you can set a filter to only calculate for one work center.</span></span> <span data-ttu-id="81482-156">Si vous ne définissez pas de filtre, tous les calendriers de centre de charge existants seront calculés.</span><span class="sxs-lookup"><span data-stu-id="81482-156">If you do not set a filter, all existing work center calendars will be calculated.</span></span>  
8.  <span data-ttu-id="81482-157">Définissez les dates début et fin de la période de calendrier à calculer, par exemple, une année comprise entre le 01/01/14 et le 31/12/14.</span><span class="sxs-lookup"><span data-stu-id="81482-157">Define the starting and ending dates of the calendar period that should be calculated, for example, one year from 01/01/14 to 31/12/14.</span></span>
9. <span data-ttu-id="81482-158">Cliquez sur le bouton **OK** pour calculer la capacité.</span><span class="sxs-lookup"><span data-stu-id="81482-158">Choose the **OK** button to calculate capacity.</span></span>  

<span data-ttu-id="81482-159">Vous venez de créer ou de mettre à jour les écritures calendrier. Elles indiquent la capacité disponible pour chaque période en fonction des trois ensembles de données de base suivants :</span><span class="sxs-lookup"><span data-stu-id="81482-159">Calendar entries are now created or updated displaying the available capacity for each period according to the following three sets of master data:</span></span>  

- <span data-ttu-id="81482-160">L'équipe et les jours ouvrés définis dans le calendrier usine attribué.</span><span class="sxs-lookup"><span data-stu-id="81482-160">The working days and shift defined in the assigned shop calendar.</span></span>  
- <span data-ttu-id="81482-161">la valeur du champ **Capacité** de la fiche centre de charge.</span><span class="sxs-lookup"><span data-stu-id="81482-161">The value in the **Capacity** field on the work center card.</span></span>  
- <span data-ttu-id="81482-162">la valeur du champ **Rendement** de la fiche centre de charge.</span><span class="sxs-lookup"><span data-stu-id="81482-162">The value in the **Efficiency** field on the work center card.</span></span>  

<span data-ttu-id="81482-163">Le calendrier de centre de charge calculé définit ensuite la période de disponibilité et la quantité de la capacité du centre de charge.</span><span class="sxs-lookup"><span data-stu-id="81482-163">The calculated work center calendar will now define when and how much capacity is available at this work center.</span></span> <span data-ttu-id="81482-164">Il contrôle la planification détaillée des opérations effectuées dans le centre de charge.</span><span class="sxs-lookup"><span data-stu-id="81482-164">This controls the detailed scheduling of operations performed at the work center.</span></span>  

## <a name="to-record-work-center-absence"></a><span data-ttu-id="81482-165">Pour enregistrer les absences du centre de charge</span><span class="sxs-lookup"><span data-stu-id="81482-165">To record work center absence</span></span>  
1.  <span data-ttu-id="81482-166">Sur la page **Calendrier centre de charge**, choisissez l'action **Afficher matrice**.</span><span class="sxs-lookup"><span data-stu-id="81482-166">On the **Work Center Calendar** page, choose the **Show Matrix** action.</span></span>
2. <span data-ttu-id="81482-167">Sur la page **Matrice Calendrier centre de charge**, sélectionnez le centre de charge et le jour de calendrier correspondant au moment où l'absence doit être enregistrée, puis choisissez l'action **Indisponibilité**.</span><span class="sxs-lookup"><span data-stu-id="81482-167">On the **Work Center Calendar Matrix** page, select the work center and calendar day when the absence time should be recorded, and then choose the **Absence** action.</span></span>  
3.  <span data-ttu-id="81482-168">Sur la page **Indisponibilité**, définissez les heures de début et de fin, et la description de l'absence du jour.</span><span class="sxs-lookup"><span data-stu-id="81482-168">On the **Absence** page, define the starting time, ending time, and description of that day’s absence.</span></span> <span data-ttu-id="81482-169">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="81482-169">For example:</span></span>  

    <span data-ttu-id="81482-170">25/01/01 08:00 10:00 Maintenance</span><span class="sxs-lookup"><span data-stu-id="81482-170">25/01/01 08:00 10:00 Maintenance</span></span>  

4.  <span data-ttu-id="81482-171">Choisissez l'action **Mettre à jour**, puis fermez la page **Indisponibilité**.</span><span class="sxs-lookup"><span data-stu-id="81482-171">Choose the **Update** action, and then close the **Absence** page.</span></span>  

<span data-ttu-id="81482-172">La capacité du jour sélectionné est réduite conformément aux heures d'absence enregistrées.</span><span class="sxs-lookup"><span data-stu-id="81482-172">The capacity of the selected day has now decreased by the recorded absence time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="81482-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81482-173">See Also</span></span>  
[<span data-ttu-id="81482-174">Configurer des calendriers principaux</span><span class="sxs-lookup"><span data-stu-id="81482-174">Set Up Base Calendars</span></span>](across-how-to-assign-base-calendars.md)  
[<span data-ttu-id="81482-175">Configurer les centres de charge et les postes de charge</span><span class="sxs-lookup"><span data-stu-id="81482-175">Set Up Work Centers and Machine Centers</span></span>](production-how-to-set-up-work-and-machine-centers.md)  
[<span data-ttu-id="81482-176">Paramétrage de la production</span><span class="sxs-lookup"><span data-stu-id="81482-176">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
[<span data-ttu-id="81482-177">Production</span><span class="sxs-lookup"><span data-stu-id="81482-177">Manufacturing</span></span>](production-manage-manufacturing.md)  
<span data-ttu-id="81482-178">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="81482-178">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
