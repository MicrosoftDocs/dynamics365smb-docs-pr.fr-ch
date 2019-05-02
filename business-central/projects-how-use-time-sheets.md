---
title: Utilisation de feuilles de temps pour des projets| Microsoft Docs
description: Décrit comment créer une feuille de temps pour un projet, copier des lignes planning dans celle-ci, définir les types de travaux, renseigner la feuille de temps, et la soumettre pour approbation.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 70d63dcc678a49fa1854b88bc3ca1f9ec8ecc69f
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820582"
---
# <a name="use-time-sheets-for-jobs"></a><span data-ttu-id="08f82-103">Utiliser des feuilles de temps pour des projets</span><span class="sxs-lookup"><span data-stu-id="08f82-103">Use Time Sheets for Jobs</span></span>
<span data-ttu-id="08f82-104">Vous devez utiliser le traitement par lots **Créer des feuilles de temps** pour configurer des feuilles de temps pour un nombre donné de périodes ou de semaines.</span><span class="sxs-lookup"><span data-stu-id="08f82-104">You use the **Create Time Sheets** batch job to set up time sheets for a specified number of time periods or weeks.</span></span> <span data-ttu-id="08f82-105">Vous devez disposer d'autorisations pour pouvoir créer des feuilles de temps.</span><span class="sxs-lookup"><span data-stu-id="08f82-105">You must have permissions to be able to create time sheets.</span></span>

<span data-ttu-id="08f82-106">Vous pouvez copier et utiliser vos lignes planning projet dans une feuille de temps.</span><span class="sxs-lookup"><span data-stu-id="08f82-106">You can copy and use your job planning lines in a time sheet.</span></span> <span data-ttu-id="08f82-107">Vous n'avez ainsi à entrer les informations qu'à un seul emplacement et les informations de ligne sont toujours correctes.</span><span class="sxs-lookup"><span data-stu-id="08f82-107">In that way, you must only enter the information in one place and the line information is always correct.</span></span>

<span data-ttu-id="08f82-108">Une fois que vous avez approuvé les écritures des feuilles de temps d'un projet, vous pouvez les valider dans la feuille ressource ou projet correspondante.</span><span class="sxs-lookup"><span data-stu-id="08f82-108">After you have approved time sheet entries for a job, you can post them to the relevant job journal or resource journal.</span></span>

<span data-ttu-id="08f82-109">Avant de pouvoir utiliser des feuilles de temps, vous devez définir des informations générales et spécifier un administrateur et un ou plusieurs approbateurs de feuilles de temps.</span><span class="sxs-lookup"><span data-stu-id="08f82-109">Before you can use time sheets, you must set up general information and specify an administrator and one or more approvers of time sheets.</span></span> <span data-ttu-id="08f82-110">Pour plus d'informations, voir [Paramétrer des feuilles de temps](projects-how-setup-time-sheets.md).</span><span class="sxs-lookup"><span data-stu-id="08f82-110">For more information, see [Set Up Time Sheets](projects-how-setup-time-sheets.md).</span></span>

## <a name="to-create-a-time-sheet"></a><span data-ttu-id="08f82-111">Pour créer une feuille de temps</span><span class="sxs-lookup"><span data-stu-id="08f82-111">To create a time sheet</span></span>
<span data-ttu-id="08f82-112">Vous pouvez utiliser le traitement par lots **Créer des feuilles de temps** pour configurer des feuilles de temps pour un nombre donné de périodes ou de semaines.</span><span class="sxs-lookup"><span data-stu-id="08f82-112">You can use the **Create Time Sheets** batch job to set up time sheets for a specified number of time periods or weeks.</span></span> <span data-ttu-id="08f82-113">Une fois qu'une feuille de temps est créée, son propriétaire peut l'ouvrir et y enregistrer le temps consacré à une tâche.</span><span class="sxs-lookup"><span data-stu-id="08f82-113">Then, the time sheet owner can open it and record time that has been spent on a task.</span></span>

1. <span data-ttu-id="08f82-114">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles de temps**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="08f82-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Time Sheets**, and then choose the related link.</span></span>
2. <span data-ttu-id="08f82-115">Sur la page **Liste des feuilles de temps**, cliquez sur l'action **Créer des feuilles de temps**.</span><span class="sxs-lookup"><span data-stu-id="08f82-115">On the **Time Sheet List** page, choose the **Create Time Sheets** action.</span></span>
3. <span data-ttu-id="08f82-116">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="08f82-116">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="08f82-117">Les champs **Utiliser la feuille de temps** et **ID utilisateur du propriétaire de la feuille de temps** doivent être renseignés sur la fiche de la ressource de la feuille de temps.</span><span class="sxs-lookup"><span data-stu-id="08f82-117">The **Use Time Sheet** and **Time Sheet Owner User ID** fields must be filled in on the card for the resource of the time sheet.</span></span>

1. <span data-ttu-id="08f82-118">Choisissez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="08f82-118">Choose the **OK** button.</span></span>  

<span data-ttu-id="08f82-119">Vous pouvez afficher les feuilles de temps que vous avez créées sur la page **Liste des feuilles de temps**.</span><span class="sxs-lookup"><span data-stu-id="08f82-119">You can view the time sheets that you have created on the **Time Sheet list** page.</span></span>

## <a name="to-copy-job-planning-lines-to-a-time-sheet"></a><span data-ttu-id="08f82-120">Pour copier des lignes planning projet dans une feuille de temps</span><span class="sxs-lookup"><span data-stu-id="08f82-120">To copy job planning lines to a time sheet</span></span>
<span data-ttu-id="08f82-121">La procédure suivante indique comment ajouter rapidement des lignes planning projet à une feuille de temps.</span><span class="sxs-lookup"><span data-stu-id="08f82-121">The following procedure describes how to quickly add job planning lines to a time sheet.</span></span>

1. <span data-ttu-id="08f82-122">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles de temps**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="08f82-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Time Sheets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="08f82-123">Sur la page **Liste des feuilles de temps**, sélectionnez une feuille de temps pour la période de référence, puis cliquez sur **Modifier feuille de temps**.</span><span class="sxs-lookup"><span data-stu-id="08f82-123">On the **Time Sheet List** page, select a time sheet for the relevant time period, and then choose the **Edit Time Sheet** action.</span></span>  
3. <span data-ttu-id="08f82-124">Cliquez sur **Créer des lignes à partir du planning projet**.</span><span class="sxs-lookup"><span data-stu-id="08f82-124">Choose the **Create lines from job planning** action.</span></span> <span data-ttu-id="08f82-125">Toutes les lignes planning projet de la période de feuille de temps sont copiées dans la feuille de temps de la personne ou du poste du champ **N° ressource** sur la feuille de temps.</span><span class="sxs-lookup"><span data-stu-id="08f82-125">Any job planning lines in the time sheet time period are copied to the time sheet for the person or machine in the **Resource No.** field on the time sheet.</span></span>

## <a name="to-define-work-types-and-add-one-to-a-time-sheet"></a><span data-ttu-id="08f82-126">Pour définir les types de travaux et en ajouter un à une feuille de temps</span><span class="sxs-lookup"><span data-stu-id="08f82-126">To define work types and add one to a time sheet</span></span>
<span data-ttu-id="08f82-127">Vous pouvez définir le type de travail pour toutes les lignes feuille de temps des projets.</span><span class="sxs-lookup"><span data-stu-id="08f82-127">You can define the work type for all time sheet lines for jobs.</span></span> <span data-ttu-id="08f82-128">Vous pouvez ainsi ajouter les informations dont vous avez besoin pour facturer le client en fonction des différents types de travaux.</span><span class="sxs-lookup"><span data-stu-id="08f82-128">In this way, you can add information that you need to bill the customer for different types of work.</span></span>

1. <span data-ttu-id="08f82-129">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles de temps**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="08f82-129">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Time Sheets**, and then choose the related link.</span></span>   
2. <span data-ttu-id="08f82-130">Ouvrez la feuille de temps correspondante.</span><span class="sxs-lookup"><span data-stu-id="08f82-130">Open the relevant time sheet.</span></span>
3. <span data-ttu-id="08f82-131">Choisissez le champ **Description**.</span><span class="sxs-lookup"><span data-stu-id="08f82-131">Choose the **Description** field.</span></span>  
4. <span data-ttu-id="08f82-132">Sur la page **Détails des tâches - ligne feuille de temps**, cliquez sur le champ **Code type travail**, puis sélectionnez un type de travail dans la liste, par exemple **Miles**.</span><span class="sxs-lookup"><span data-stu-id="08f82-132">On the **Time Sheet Line Job Detail** page, choose the **Work Type Code** field, and select a work type from the list, such as **Miles**.</span></span>  
5. <span data-ttu-id="08f82-133">S'il n'existe aucun type de travail, cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="08f82-133">If no work types exist, chose the **New** action.</span></span>
6. <span data-ttu-id="08f82-134">Sur la page **Types de travaux**, renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="08f82-134">On the **Work Types** page, fill in the fields as necessary.</span></span>
7. <span data-ttu-id="08f82-135">Répétez l'étape 4 pour affecter le nouveau type de travail à la feuille de temps.</span><span class="sxs-lookup"><span data-stu-id="08f82-135">Repeat step 4 to assign the new work type to the time sheet.</span></span>

## <a name="to-reuse-time-sheet-lines-in-other-time-sheets"></a><span data-ttu-id="08f82-136">Pour réutiliser des lignes feuille de temps dans d'autres feuilles de temps par la suite</span><span class="sxs-lookup"><span data-stu-id="08f82-136">To reuse time sheet lines in other time sheets</span></span>
<span data-ttu-id="08f82-137">Si les informations de votre feuille de temps ne changent pas d'une période à une autre, vous pouvez gagner du temps en copiant les lignes de la période précédente.</span><span class="sxs-lookup"><span data-stu-id="08f82-137">If your time sheet information remains the same from time period to time period, you can save time by copying the lines from the previous time period.</span></span> <span data-ttu-id="08f82-138">Il vous suffit ensuite d'entrer votre temps d'utilisation pour la nouvelle période.</span><span class="sxs-lookup"><span data-stu-id="08f82-138">Then, you just enter your time usage for the new period.</span></span>

1. <span data-ttu-id="08f82-139">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles de temps**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="08f82-139">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Time Sheets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="08f82-140">Ouvrez la feuille de temps pour une période ultérieure à la période d'une feuille de temps existante avec des lignes.</span><span class="sxs-lookup"><span data-stu-id="08f82-140">Open the time sheet for a period later than the period for an existing time sheet with lines.</span></span>  
3. <span data-ttu-id="08f82-141">Cliquez sur **Copier les lignes de la feuille de temps précédente**.</span><span class="sxs-lookup"><span data-stu-id="08f82-141">Choose the **Copy Lines from Previous Time Sheet** action.</span></span>

<span data-ttu-id="08f82-142">Les lignes sont copiées, y compris les détails comme le type et la description.</span><span class="sxs-lookup"><span data-stu-id="08f82-142">The lines are copied, including details such as type and description.</span></span> <span data-ttu-id="08f82-143">Par exemple, si la ligne est associée à un projet, le **N° projet** est copié.</span><span class="sxs-lookup"><span data-stu-id="08f82-143">For example, if the line is related to a job, the **Job No.** is copied.</span></span> <span data-ttu-id="08f82-144">Toutes les lignes copiées ont le statut **En cours**.</span><span class="sxs-lookup"><span data-stu-id="08f82-144">All copied lines have the status **Open**.</span></span> <span data-ttu-id="08f82-145">Vous pouvez à présent modifier les lignes selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="08f82-145">You can now modify the lines as needed.</span></span>

## <a name="to-fill-in-a-time-sheet-lines-and-submit-for-approval"></a><span data-ttu-id="08f82-146">Pour renseigner les lignes d'une feuille de temps lignes et l'envoyer pour approbation</span><span class="sxs-lookup"><span data-stu-id="08f82-146">To fill in a time sheet lines and submit for approval</span></span>
<span data-ttu-id="08f82-147">L'enregistrement des feuilles de temps est assuré en heures, qui est l'unité de mesure standard pour les ressources.</span><span class="sxs-lookup"><span data-stu-id="08f82-147">Time sheet registration is tracked in hours, the standard base unit of measure for resources.</span></span> <span data-ttu-id="08f82-148">Par défaut, une feuille de temps indique les jours de travail ouvrés du lundi au vendredi.</span><span class="sxs-lookup"><span data-stu-id="08f82-148">By default, a time sheet shows the common work days of Monday through Friday.</span></span>

1. <span data-ttu-id="08f82-149">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles de temps**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="08f82-149">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Time Sheets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="08f82-150">Sélectionnez une feuille de temps pour la période de référence, puis cliquez sur **Modifier feuille de temps**.</span><span class="sxs-lookup"><span data-stu-id="08f82-150">Select a time sheet for the relevant time period, and then choose the **Edit Time Sheet** action.</span></span>  
3. <span data-ttu-id="08f82-151">Renseignez les champs d'une ligne selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="08f82-151">Fill in the fields on a line as necessary.</span></span> <span data-ttu-id="08f82-152">Saisissez le nombre d'heures utilisées par la ressource chaque jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="08f82-152">Enter the number of hours used by the resource on each day of the week.</span></span>

    > [!TIP]  
    >   <span data-ttu-id="08f82-153">Vous pouvez consulter dans le récapitulatif **Totalisation réelle/budgétée** la somme des heures des feuilles de temps que vous avez entrées.</span><span class="sxs-lookup"><span data-stu-id="08f82-153">You can review the sum of time sheet hours that you have entered in the **Actual/Budgeted Summary** FactBox.</span></span>  
4. <span data-ttu-id="08f82-154">Répétez l'étape 3 pour d'autres types de travaux que la ressource effectue.</span><span class="sxs-lookup"><span data-stu-id="08f82-154">Repeat step 3 for other work types that the resource performs.</span></span>
5. <span data-ttu-id="08f82-155">Cliquez sur **Envoyer**, puis sur **Toutes les lignes ouvertes** pour envoyer toutes les lignes ou sur **Ligne(s) sélectionnée(s) uniquement** pour envoyer uniquement les lignes qui sont sélectionnées sur la page **Feuille de temps**.</span><span class="sxs-lookup"><span data-stu-id="08f82-155">Choose the **Submit** action, and then choose the **All open lines** action to submit all lines or the **Selected lines only** action to submit only the lines that are selected on the **Time Sheet** page.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="08f82-156">Vous ne pouvez toutefois soumettre que des lignes pour lesquelles vous avez entré du temps.</span><span class="sxs-lookup"><span data-stu-id="08f82-156">You can only submit time sheet lines for which you have entered time.</span></span>  
6. <span data-ttu-id="08f82-157">Pour modifier les informations d'une ligne qui a pour valeur **Soumis**, sélectionnez la ligne en question, puis cliquez sur **Rouvrir**.</span><span class="sxs-lookup"><span data-stu-id="08f82-157">To modify information on a line that has been set to **Submitted**, select the line, and then choose the **Reopen** action.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="08f82-158">Un administrateur peut rejeter une ligne feuille de temps qui est envoyée pour approbation.</span><span class="sxs-lookup"><span data-stu-id="08f82-158">A manager may reject a time sheet line that is submitted for approval.</span></span> <span data-ttu-id="08f82-159">Si une ligne a le statut **Rejeté**, vous pouvez modifier cette ligne et choisir de nouveau **Soumettre**.</span><span class="sxs-lookup"><span data-stu-id="08f82-159">If a line has a status of **Rejected**, you can make changes to the line, and then choose **Submit** again.</span></span>  
7. <span data-ttu-id="08f82-160">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="08f82-160">Choose the **OK** button.</span></span>

## <a name="to-approve-or-reject-a-time-sheet"></a><span data-ttu-id="08f82-161">Pour approuver ou rejeter une feuille de temps</span><span class="sxs-lookup"><span data-stu-id="08f82-161">To approve or reject a time sheet</span></span>
<span data-ttu-id="08f82-162">Une feuille de temps doit être soumise pour approbation avant de pouvoir être utilisée.</span><span class="sxs-lookup"><span data-stu-id="08f82-162">A time sheet must be submitted for approval before it can be used.</span></span> <span data-ttu-id="08f82-163">Vous pouvez approuver et rejeter chacune des lignes d'une feuille de temps ou les renvoyer à la personne à l'origine de leur soumission pour qu'elle effectue d'autres actions.</span><span class="sxs-lookup"><span data-stu-id="08f82-163">You can approve and reject individual lines on a time sheet or send them back to the submitter for additional action.</span></span> <span data-ttu-id="08f82-164">Une feuille de temps peut être approuvée de deux manières :</span><span class="sxs-lookup"><span data-stu-id="08f82-164">A time sheet can be approved in two ways:</span></span>

* <span data-ttu-id="08f82-165">Un administrateur de feuille de temps peut approuver n'importe quelle feuille de temps.</span><span class="sxs-lookup"><span data-stu-id="08f82-165">A time sheet administrator can approve any time sheet.</span></span>
* <span data-ttu-id="08f82-166">La personne qui est indiquée dans le champ **ID utilisateur de l'approbateur de la feuille de temps** d'une fiche ressource peut approuver les feuilles de temps de cette ressource.</span><span class="sxs-lookup"><span data-stu-id="08f82-166">The person who is specified in the **Time Sheet Approver User ID** field on a resource card can approve that resource's time sheets.</span></span> <span data-ttu-id="08f82-167">Pour plus d'informations, voir [Paramétrer des feuilles de temps](projects-how-setup-time-sheets.md).</span><span class="sxs-lookup"><span data-stu-id="08f82-167">For more information, see [Set Up Time Sheets](projects-how-setup-time-sheets.md).</span></span>

1. <span data-ttu-id="08f82-168">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles de temps administrateur**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="08f82-168">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Manager Time Sheets**, and then choose the related link.</span></span>
2. <span data-ttu-id="08f82-169">Sélectionnez une feuille de temps dans la liste.</span><span class="sxs-lookup"><span data-stu-id="08f82-169">Select a time sheet from the list.</span></span>  
3. <span data-ttu-id="08f82-170">Sur la page **Feuille de temps**, cliquez sur **Approuver**, puis sur **Toutes les lignes soumises** pour approuver toutes les lignes ou sur **Ligne(s) sélectionnée(s) uniquement** pour envoyer uniquement les lignes qui sont sélectionnées sur la page **Feuille de temps**.</span><span class="sxs-lookup"><span data-stu-id="08f82-170">On the **Time Sheet** page, choose the **Approve** action, and then choose the **All submitted lines** action to approve all lines or the **Selected lines only** action to approve only the lines that are selected on the **Time Sheet** page.</span></span>
4. <span data-ttu-id="08f82-171">Choisissez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="08f82-171">Choose the **OK** button.</span></span>  
5. <span data-ttu-id="08f82-172">Sinon, cliquez sur **Rejeter** et suivez les étapes 4 à 5.</span><span class="sxs-lookup"><span data-stu-id="08f82-172">Alternatively, choose the **Reject** action and follow steps 4 through 5.</span></span>  

> [!TIP]  
>   <span data-ttu-id="08f82-173">Utilisez les récapitulatifs **Statut feuille de temps** et **Totalisation réelle/budgétée** pour obtenir un aperçu des informations des feuilles de temps.</span><span class="sxs-lookup"><span data-stu-id="08f82-173">Use the **Time Sheet Status** and **Actual/Budgeted Summary** FactBoxes to get an overview of time sheet information.</span></span>

<span data-ttu-id="08f82-174">Une fois qu'une feuille de temps est approuvée ou rejetée, elle ne peut plus être modifiée à moins d'être rouverte au préalable.</span><span class="sxs-lookup"><span data-stu-id="08f82-174">After you have approved or rejected a time sheet, it cannot be modified unless it is first reopened.</span></span> <span data-ttu-id="08f82-175">La procédure suivante explique comment rouvrir une feuille de temps approuvée ou rejetée.</span><span class="sxs-lookup"><span data-stu-id="08f82-175">The following procedure explains how to reopen an approved or rejected time sheet.</span></span>

## <a name="to-reopen-a-time-sheet"></a><span data-ttu-id="08f82-176">Pour rouvrir une feuille de temps</span><span class="sxs-lookup"><span data-stu-id="08f82-176">To reopen a time sheet</span></span>
1. <span data-ttu-id="08f82-177">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles de temps administrateur** ou **Feuilles de temps**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="08f82-177">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Manager Time Sheets** or **Time Sheets**, and then choose the related link.</span></span>
2. <span data-ttu-id="08f82-178">Ouvrez une feuille de temps à partir de la liste.</span><span class="sxs-lookup"><span data-stu-id="08f82-178">Open a time sheet from the list.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="08f82-179">Vous ne pouvez rouvrir que les lignes dont le statut est **Approuvé**.</span><span class="sxs-lookup"><span data-stu-id="08f82-179">You can only reopen lines that have the status **Approved**.</span></span> <span data-ttu-id="08f82-180">Vous ne pouvez pas rouvrir les lignes dont le statut est **Rejeté**.</span><span class="sxs-lookup"><span data-stu-id="08f82-180">You cannot reopen lines that have the status **Rejected**.</span></span> <span data-ttu-id="08f82-181">Vous ne pouvez pas rouvrir une feuille de temps qui a été validée.</span><span class="sxs-lookup"><span data-stu-id="08f82-181">You cannot reopen a time sheet if it has been posted.</span></span>  
3. <span data-ttu-id="08f82-182">Sur la page **Feuille de temps**, cliquez sur **Rouvrir**, puis sur **Toutes les lignes soumises** pour rouvrir toutes les lignes ou sur **Ligne(s) sélectionnée(s) uniquement** pour rouvrir uniquement les lignes sélectionnées sur la page **Feuille de temps**.</span><span class="sxs-lookup"><span data-stu-id="08f82-182">On the **Time Sheet** page, choose the **Reopen** action, and then choose the **All submitted lines** action to reopen all lines or the **Selected lines only** action to reopen only the lines that are selected on the **Time Sheet** page.</span></span>
4. <span data-ttu-id="08f82-183">Choisissez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="08f82-183">Choose the **OK** button.</span></span> <span data-ttu-id="08f82-184">Le statut de la ou des lignes des feuilles de temps devient **Soumis**.</span><span class="sxs-lookup"><span data-stu-id="08f82-184">The status of the time sheets line or lines is changes to **Submitted**.</span></span>  

## <a name="to-post-time-sheet-lines-in-a-resource-journal"></a><span data-ttu-id="08f82-185">Pour valider des lignes feuille de temps dans une feuille ressource</span><span class="sxs-lookup"><span data-stu-id="08f82-185">To post time sheet lines in a resource journal</span></span>
<span data-ttu-id="08f82-186">Une fois que vous avez approuvé les écritures des feuilles de temps d'une ressource, vous pouvez les valider dans la feuille ressource correspondante.</span><span class="sxs-lookup"><span data-stu-id="08f82-186">After you have approved time sheet entries for a resource, you can post them to the relevant resource journal.</span></span>

1. <span data-ttu-id="08f82-187">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuille ressource**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="08f82-187">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resource Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="08f82-188">Cliquez sur **Proposer des lignes à partir des feuilles de temps**.</span><span class="sxs-lookup"><span data-stu-id="08f82-188">Choose the **Suggest Lines from Time Sheets** action.</span></span>  
3. <span data-ttu-id="08f82-189">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="08f82-189">Fill in the fields as necessary.</span></span>  
4. <span data-ttu-id="08f82-190">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="08f82-190">Choose the **OK** button.</span></span> <span data-ttu-id="08f82-191">Les écritures de l'activité sont créées dans la feuille ressource, dans laquelle vous pouvez modifier les informations selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="08f82-191">Entries for usage are created in the resource journal, where you can modify the information as needed.</span></span>  
5. <span data-ttu-id="08f82-192">Sélectionnez l'action **Valider**.</span><span class="sxs-lookup"><span data-stu-id="08f82-192">Choose the **Post** action.</span></span>  
6. <span data-ttu-id="08f82-193">Pour vérifier la validation, cliquez sur **Écritures comptables**.</span><span class="sxs-lookup"><span data-stu-id="08f82-193">To verify the posting, choose the **Ledger Entries** action.</span></span> <span data-ttu-id="08f82-194">La page **Écritures comptables ressource** s'ouvre et affiche le résultat de la validation de la feuille ressource.</span><span class="sxs-lookup"><span data-stu-id="08f82-194">The **Resource Ledger Entries** page opens showing the result of posting the resource journal.</span></span>

## <a name="to-post-time-sheet-lines-in-a-job-journal"></a><span data-ttu-id="08f82-195">Pour valider des lignes feuille de temps dans une feuille projet</span><span class="sxs-lookup"><span data-stu-id="08f82-195">To post time sheet lines in a job journal</span></span>
<span data-ttu-id="08f82-196">Une fois que vous avez approuvé les écritures des feuilles de temps d'un projet, vous pouvez les valider dans la feuille projet correspondante.</span><span class="sxs-lookup"><span data-stu-id="08f82-196">After you have approved time sheet entries for a job, you can post them to the relevant job journal.</span></span>

1. <span data-ttu-id="08f82-197">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuille projet**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="08f82-197">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="08f82-198">Cliquez sur **Proposer des lignes à partir des feuilles de temps**.</span><span class="sxs-lookup"><span data-stu-id="08f82-198">Choose the **Suggest Lines from Time Sheets** action.</span></span>  
3. <span data-ttu-id="08f82-199">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="08f82-199">Fill in the fields as necessary.</span></span>  
4. <span data-ttu-id="08f82-200">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="08f82-200">Choose the **OK** button.</span></span> <span data-ttu-id="08f82-201">Les écritures de l'activité sont créées dans la feuille projet, dans laquelle vous pouvez modifier les informations selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="08f82-201">Entries for usage are created in the job journal, where you can modify the information as needed.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="08f82-202">Les informations sur le type de travail et la facturabilité du travail sont copiées à partir de la ligne feuille de temps.</span><span class="sxs-lookup"><span data-stu-id="08f82-202">Information about work type and whether the work is chargeable is copied from the time sheet line.</span></span> <span data-ttu-id="08f82-203">Si nécessaire, vous pouvez réduire le nombre d'heures et procéder à une validation partielle.</span><span class="sxs-lookup"><span data-stu-id="08f82-203">If needed, you can reduce the quantity of hours and do a partial posting.</span></span> <span data-ttu-id="08f82-204">Si vous réduisez la quantité, la prochaine fois que vous cliquerez sur **Proposer des lignes à partir des feuilles de temps**, la ligne qui sera créée contiendra la quantité d'heures restante.</span><span class="sxs-lookup"><span data-stu-id="08f82-204">If you reduce the quantity, then the next time that you choose the **Suggest Lines From Time Sheets** action, the line that is created will contain the remaining quantity of hours.</span></span>  
5. <span data-ttu-id="08f82-205">Sélectionnez l'action **Valider**.</span><span class="sxs-lookup"><span data-stu-id="08f82-205">Choose the **Post** action.</span></span>  
6. <span data-ttu-id="08f82-206">Pour vérifier la validation, cliquez sur **Écritures comptables**.</span><span class="sxs-lookup"><span data-stu-id="08f82-206">To verify the posting, choose the **Ledger Entries** action.</span></span> <span data-ttu-id="08f82-207">La page **Écritures comptables projet** s'ouvre et affiche le résultat de la validation de la feuille ressource.</span><span class="sxs-lookup"><span data-stu-id="08f82-207">The **Job Ledger Entries** page opens showing the result of posting the resource journal.</span></span>

## <a name="to-archive-time-sheets"></a><span data-ttu-id="08f82-208">Pour archiver des feuilles de temps</span><span class="sxs-lookup"><span data-stu-id="08f82-208">To archive time sheets</span></span>
<span data-ttu-id="08f82-209">Une fois les feuilles de temps validées, vous pouvez les archiver pour vous y référer par la suite.</span><span class="sxs-lookup"><span data-stu-id="08f82-209">After you have posted time sheets, you can archive them for future reference.</span></span> <span data-ttu-id="08f82-210">Toutes les lignes des feuilles de temps doivent être validées avant qu'une feuille de temps puisse être archivée.</span><span class="sxs-lookup"><span data-stu-id="08f82-210">All time sheets lines must be posted before a time sheet can be archived.</span></span>

> [!NOTE]  
>   <span data-ttu-id="08f82-211">Lorsque vous archivez une feuille de temps, elle est supprimée des listes de la page **Feuilles de temps** et **Feuilles de temps administrateur**.</span><span class="sxs-lookup"><span data-stu-id="08f82-211">When you archive a time sheet, it is removed from the lists in both the **Time Sheets** page and the **Manager Time Sheets** page.</span></span>

1. <span data-ttu-id="08f82-212">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles de temps de transfert vers archive**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="08f82-212">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Move Time Sheets to Archive**, and then choose the related link.</span></span>  
2. <span data-ttu-id="08f82-213">Renseignez les champs selon vos besoins, puis cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="08f82-213">Fill in the fields as necessary, and then choose the **OK** button.</span></span>  
3. <span data-ttu-id="08f82-214">Pour vérifier les feuilles de temps archivées, choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Archives des feuilles de temps** ou **Archives des feuilles de temps administrateur**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="08f82-214">To review archived time sheets, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Time Sheet Archives** or **Manager Time Sheet Archives**, and then choose the related link.</span></span>

## <a name="see-also"></a><span data-ttu-id="08f82-215">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08f82-215">See Also</span></span>
[<span data-ttu-id="08f82-216">Gestion de projets</span><span class="sxs-lookup"><span data-stu-id="08f82-216">Project Management</span></span>](projects-manage-projects.md)  
<span data-ttu-id="08f82-217">[Configuration de la gestion de projet](projects-setup-projects.md)  </span><span class="sxs-lookup"><span data-stu-id="08f82-217">[Setting Up Project Management](projects-setup-projects.md)  </span></span>  
[<span data-ttu-id="08f82-218">Finances</span><span class="sxs-lookup"><span data-stu-id="08f82-218">Finance</span></span>](finance.md)  
<span data-ttu-id="08f82-219">[Achats](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="08f82-219">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="08f82-220">[Ventes](sales-manage-sales.md)   </span><span class="sxs-lookup"><span data-stu-id="08f82-220">[Sales](sales-manage-sales.md)   </span></span>  
<span data-ttu-id="08f82-221">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="08f82-221">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  