---
title: "Paramétrer et gérer un budget pour un projet| Microsoft Docs"
description: "Décrit comment planifier des ressources et prévoir et contrôler les coûts d'un projet en définissant un budget pour chaque projet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project budget, forecast
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 995d181496dc1827f21c0b3edd9e52dd6c15c297
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="manage-job-budgets"></a><span data-ttu-id="86f4f-103">Gérer les budgets de projets</span><span class="sxs-lookup"><span data-stu-id="86f4f-103">Manage Job Budgets</span></span>
<span data-ttu-id="86f4f-104">Vous pouvez configurer un budget pour chaque projet.</span><span class="sxs-lookup"><span data-stu-id="86f4f-104">You can set up a budget for each job.</span></span> <span data-ttu-id="86f4f-105">Le budget permet de planifier les ressources que vous affectez à un projet.</span><span class="sxs-lookup"><span data-stu-id="86f4f-105">The budget is used to plan the resources that you allocate to a job.</span></span> <span data-ttu-id="86f4f-106">Il peut s'agir d'un budget général avec peu d'écritures ou plus détaillé avec des écritures réparties par niveau d'activité.</span><span class="sxs-lookup"><span data-stu-id="86f4f-106">The budget can be either general with few entries or it can contain more entries that are divided into activity levels.</span></span> <span data-ttu-id="86f4f-107">Vous pouvez alors comparer les montants budgétés avec l'activité réelle telle qu'elle a été enregistrée dans la feuille projet.</span><span class="sxs-lookup"><span data-stu-id="86f4f-107">You can then compare the budgeted amounts with the actual usage as recorded in the job journal.</span></span> <span data-ttu-id="86f4f-108">En surveillant les différences entre l'activité réelle et celle budgétée, vous pouvez contrôler un projet en cours et améliorer la qualité des projets futurs en réduisant le risque de sous-estimation des coûts.</span><span class="sxs-lookup"><span data-stu-id="86f4f-108">By monitoring differences between actual usage and budgeted usage, you can control an ongoing project and improve the quality of future jobs by reducing the risk of underestimating costs.</span></span>

<span data-ttu-id="86f4f-109">La procédure suivante décrit comment estimer les coûts budgétés lors de la planification.</span><span class="sxs-lookup"><span data-stu-id="86f4f-109">The following procedure describes how to estimate budgeted costs during planning.</span></span> <span data-ttu-id="86f4f-110">Pour plus d'informations sur l'enregistrement budgété par rapport aux prix et aux coûts réels du projet, voir [Enregistrer l'utilisation pour les projets](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="86f4f-110">For information about recording budgeted versus actual job prices and costs, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>  

## <a name="JobBudgetCosts"></a> <span data-ttu-id="86f4f-111">Pour estimer les coûts budgétés d'un projet</span><span class="sxs-lookup"><span data-stu-id="86f4f-111">To estimate the budgeted costs for a job</span></span>
<span data-ttu-id="86f4f-112">Lorsqu'un client souhaite connaître le prix d'un projet qui sera facturé en fonction de l'activité, vous devez déterminer les coûts budgétés du projet.</span><span class="sxs-lookup"><span data-stu-id="86f4f-112">When a customer wants to know the price of a job that will be invoiced based on usage, you must have to determine the budgeted costs for the job.</span></span> <span data-ttu-id="86f4f-113">Réalisez cette opération dans la fenêtre **Lignes tâche projet**.</span><span class="sxs-lookup"><span data-stu-id="86f4f-113">You use the **Job Task Lines** window to do this.</span></span>

1. <span data-ttu-id="86f4f-114">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Projets**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="86f4f-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="86f4f-115">Ouvrez le projet approprié.</span><span class="sxs-lookup"><span data-stu-id="86f4f-115">Open a relevant job.</span></span>
3. <span data-ttu-id="86f4f-116">Sélectionnez une ligne tâche de type Validation, puis cliquez sur **Lignes planning projet**.</span><span class="sxs-lookup"><span data-stu-id="86f4f-116">Select a task line of type Posting, and then choose the **Job Planning Lines** action.</span></span>
4. <span data-ttu-id="86f4f-117">Sur une nouvelle ligne, renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="86f4f-117">On a new line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

<span data-ttu-id="86f4f-118">Reportez-vous aux informations suivantes pour le champ **Type ligne**.</span><span class="sxs-lookup"><span data-stu-id="86f4f-118">For the **Line Type** field, refer to the following information.</span></span>  

| <span data-ttu-id="86f4f-119">Type ligne</span><span class="sxs-lookup"><span data-stu-id="86f4f-119">Line Type</span></span> | <span data-ttu-id="86f4f-120">Désignation</span><span class="sxs-lookup"><span data-stu-id="86f4f-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="86f4f-121">**Budget et Facturable**</span><span class="sxs-lookup"><span data-stu-id="86f4f-121">**Both Budget and Billable**</span></span> |<span data-ttu-id="86f4f-122">Les montants coût et prix entrés sur la ligne planning sont les coûts budgétés pour la ligne planning donnée.</span><span class="sxs-lookup"><span data-stu-id="86f4f-122">The cost and price amounts entered on the planning line are the budgeted costs for the particular planning line.</span></span> <span data-ttu-id="86f4f-123">Le prix sera facturé.</span><span class="sxs-lookup"><span data-stu-id="86f4f-123">The price amount will be invoiced.</span></span> |
| <span data-ttu-id="86f4f-124">**Budget**</span><span class="sxs-lookup"><span data-stu-id="86f4f-124">**Budget**</span></span> |<span data-ttu-id="86f4f-125">Le client ne doit pas payer l'utilisation.</span><span class="sxs-lookup"><span data-stu-id="86f4f-125">The customer is not charged for usage.</span></span> <span data-ttu-id="86f4f-126">L'activité n'est pas transférée à une facture, mais sera encore utilisée dans le calcul de TEC.</span><span class="sxs-lookup"><span data-stu-id="86f4f-126">Usage is not transferred to an invoice, but will still be used in the calculation of WIP.</span></span> |
| <span data-ttu-id="86f4f-127">**Facturable**</span><span class="sxs-lookup"><span data-stu-id="86f4f-127">**Billable**</span></span> |<span data-ttu-id="86f4f-128">Le client doit payer l'utilisation.</span><span class="sxs-lookup"><span data-stu-id="86f4f-128">The customer is charged for usage.</span></span> <span data-ttu-id="86f4f-129">L'activité est transférée à la facture, sur la base de la quantité spécifiée dans le champ Qté à transférer à facturer.</span><span class="sxs-lookup"><span data-stu-id="86f4f-129">Usage is transferred to the invoice, based on the quantity specified in the Qty. to Transfer to Invoice field.</span></span> |

> [!NOTE]  
>   <span data-ttu-id="86f4f-130">Le champ **Date planning** de la ligne planning contient la date prévue de l'achèvement et de la validation de l'activité associée à cette ligne planning.</span><span class="sxs-lookup"><span data-stu-id="86f4f-130">The **Planning Date** field for the planning line contains the date when usage related to the planning line is expected to be completed.</span></span> <span data-ttu-id="86f4f-131">C'est aussi la date à laquelle la ligne planning peut être transférée à une facture vente et être validée.</span><span class="sxs-lookup"><span data-stu-id="86f4f-131">It is also the date when the planning line may be transferred to a sales invoice and posted.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="86f4f-132">Quand vous renseignez le champ **Quantité**, toutes les informations prix total et coût total seront désormais calculées et renseignées pour cette ligne planning.</span><span class="sxs-lookup"><span data-stu-id="86f4f-132">When you fill in the **Quantity** field, all total price and total cost information will be calculated and filled in for that planning line.</span></span> <span data-ttu-id="86f4f-133">Vous pouvez modifier ces informations à tout moment.</span><span class="sxs-lookup"><span data-stu-id="86f4f-133">You can edit them at any time.</span></span>

<span data-ttu-id="86f4f-134">Dans la fenêtre **Fiche projet**, vous pouvez désormais voir un résumé des coûts budgétés totaux, des prix budgétés, du coût facturable et du prix facturable pour chaque tâche.</span><span class="sxs-lookup"><span data-stu-id="86f4f-134">In the **Job Card** window, you can now see a summary of the total budgeted costs, budgeted price, billable cost and billable price for each task.</span></span>

<span data-ttu-id="86f4f-135">Pour plus d'informations sur l'enregistrement budgété par rapport aux prix et aux coûts réels du projet, voir [Enregistrer l'utilisation pour les projets](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="86f4f-135">For information about recording budgeted versus actual job prices and costs, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="86f4f-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86f4f-136">See Also</span></span>
[<span data-ttu-id="86f4f-137">Gestion de projets</span><span class="sxs-lookup"><span data-stu-id="86f4f-137">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="86f4f-138">Finances</span><span class="sxs-lookup"><span data-stu-id="86f4f-138">Finance</span></span>](finance.md)  
<span data-ttu-id="86f4f-139">[Achats](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="86f4f-139">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="86f4f-140">[Ventes](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="86f4f-140">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="86f4f-141">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="86f4f-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

