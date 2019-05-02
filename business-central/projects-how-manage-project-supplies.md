---
title: Acheter des articles ou des services pour un projet et gérer les fournitures| Microsoft Docs
description: Décrit comment gérer l'approvisionnement et l'achat de matériel et de services pour les projets.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, material, purchase
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 68505a6507901511578dc3672de013175a3e36ef
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820296"
---
# <a name="manage-job-supplies"></a><span data-ttu-id="efc51-103">Gérer les fournitures pour un projet</span><span class="sxs-lookup"><span data-stu-id="efc51-103">Manage Job Supplies</span></span>
<span data-ttu-id="efc51-104">La gestion des fournitures des projets relatifs à des articles, services et dépenses est l'un des aspects essentiels de l'exécution d'un projet.</span><span class="sxs-lookup"><span data-stu-id="efc51-104">Managing project supplies of items, services, and expenses is an integral and critical aspect of the execution of all jobs.</span></span> <span data-ttu-id="efc51-105">Vous pouvez utiliser les quantités de stock ou effectuer des achats spécifiques au projet en utilisant des commandes achat ou des factures achat.</span><span class="sxs-lookup"><span data-stu-id="efc51-105">You can use inventory quantities or make job-specific purchases using purchase orders or purchase invoices.</span></span> <span data-ttu-id="efc51-106">Par exemple, un projet de service sur un ordinateur requiert un nouveau disque.</span><span class="sxs-lookup"><span data-stu-id="efc51-106">For example, a service job on a computer requires a new disk.</span></span> <span data-ttu-id="efc51-107">Vous devez donc créer une facture achat pour l'acheter et pour enregistrer le projet pour lequel il sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="efc51-107">You create a purchase invoice to buy a new disk and record the job that it will be used on.</span></span>

<span data-ttu-id="efc51-108">Si le processus d'achat ne requiert pas d'enregistrement séparé de la transaction physique, un achat peut être traité sur la page **Feuille compta. projet**.</span><span class="sxs-lookup"><span data-stu-id="efc51-108">If the purchase process does not require that the physical transaction be recorded separately, then a purchase may be processed on the **Job G/L Journal** page.</span></span> <span data-ttu-id="efc51-109">Pour plus d'informations, voir [Enregistrer l'utilisation pour les projets](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="efc51-109">For more information, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

## <a name="to-purchase-items-or-services-for-a-job"></a><span data-ttu-id="efc51-110">Pour acheter des articles ou des services pour un projet</span><span class="sxs-lookup"><span data-stu-id="efc51-110">To purchase items or services for a job</span></span>
<span data-ttu-id="efc51-111">La procédure suivante indique comment utiliser une facture achat pour acheter des produits pour un projet.</span><span class="sxs-lookup"><span data-stu-id="efc51-111">The following procedure shows how to use a purchase invoice to purchase products for a job.</span></span> <span data-ttu-id="efc51-112">Les mêmes étapes s'appliquent lors de l'utilisation d'une commande achat.</span><span class="sxs-lookup"><span data-stu-id="efc51-112">The same steps apply when using a purchase order.</span></span>  

1. <span data-ttu-id="efc51-113">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Factures achat**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="efc51-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="efc51-114">Sélectionnez l'action **Nouveau**, puis renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="efc51-114">Choose the **New** action and fill in the fields as necessary.</span></span> <span data-ttu-id="efc51-115">Pour plus d'informations, voir [Enregistrer des achats](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="efc51-115">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
3. <span data-ttu-id="efc51-116">Dans les champs **N° projet** et **N° tâche projet**, sélectionnez les informations du projet pour lequel vous souhaitez acheter des articles ou des services.</span><span class="sxs-lookup"><span data-stu-id="efc51-116">In the **Job No.** and **Job Task No.** fields, select the information of the job that you want to purchase items or services for.</span></span> <span data-ttu-id="efc51-117">Utilisez la fonction **Choisir les colonnes** si le champ n'est pas visible.</span><span class="sxs-lookup"><span data-stu-id="efc51-117">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="efc51-118">Pour plus d'informations, voir [Personnalisation de votre espace de travail](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="efc51-118">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>

    <span data-ttu-id="efc51-119">La valeur que vous sélectionnez dans le champ **Type ligne projet** définit si une ligne planning est créée lorsque vous validez l'activité de l'article.</span><span class="sxs-lookup"><span data-stu-id="efc51-119">The value that you select in the **Job Line Type** field defines whether a planning line is created when you post the usage of the item.</span></span> <span data-ttu-id="efc51-120">Si le champ indique **Facturable**, les lignes planning projet prêtes pour facturation sont créées.</span><span class="sxs-lookup"><span data-stu-id="efc51-120">If the field contains **Billable**, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="efc51-121">Pour plus d'informations, voir [Facturation des projets](projects-how-invoice-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="efc51-121">For more information, see [Invoice Jobs](projects-how-invoice-jobs.md).</span></span>
4. <span data-ttu-id="efc51-122">Sélectionnez l'action **Valider**.</span><span class="sxs-lookup"><span data-stu-id="efc51-122">Choose the **Post** action.</span></span>

## <a name="to-view-the-value-of-purchases-for-a-job"></a><span data-ttu-id="efc51-123">Pour afficher la valeur des achats pour un projet</span><span class="sxs-lookup"><span data-stu-id="efc51-123">To view the value of purchases for a job</span></span>
1. <span data-ttu-id="efc51-124">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Projets**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="efc51-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="efc51-125">Ouvrez la fiche projet appropriée.</span><span class="sxs-lookup"><span data-stu-id="efc51-125">Open a relevant job card.</span></span>

    <span data-ttu-id="efc51-126">Dans le raccourci **Tâches**, le champ **Commandes ouvertes** affiche le montant total en commande, en devise société, des articles en stock et des services sur les documents achat pour la tâche projet ligne.</span><span class="sxs-lookup"><span data-stu-id="efc51-126">On the **Tasks** FastTab, the **Outstanding Orders** field shows the total outstanding amount, in local currency, of inventory items and services on purchase documents for the job task line.</span></span>  

    <span data-ttu-id="efc51-127">Le champ **Montant reçu non facturé** affiche la valeur des articles livrés sur les documents achat mais non facturés.</span><span class="sxs-lookup"><span data-stu-id="efc51-127">The **Amt. Rec. Not Invoiced** field shows the value of items delivered on purchase documents, but not yet invoiced.</span></span>  
3. <span data-ttu-id="efc51-128">Choisissez l'un des champs pour ouvrir la page **Lignes achat** dans laquelle vous pouvez consulter des informations sur les lignes de document achat associées, incluant les articles ou les services qui ont été réceptionnés.</span><span class="sxs-lookup"><span data-stu-id="efc51-128">Choose either of the fields to open the **Purchase Lines** page where you can review information about the related purchase document lines, including which items or services have been received.</span></span>

## <a name="to-post-a-job-related-expense"></a><span data-ttu-id="efc51-129">Pour valider des frais liés à un projet</span><span class="sxs-lookup"><span data-stu-id="efc51-129">To post a job-related expense</span></span>
<span data-ttu-id="efc51-130">Si vous supportez les dépenses extraordinaires ou exceptionnelles du projet, vous pouvez utiliser la page **Feuille compta. projet** pour les valider directement dans le compte projet approprié.</span><span class="sxs-lookup"><span data-stu-id="efc51-130">If you incur extraordinary or one-time job expenses, you can use the **Job G/L Journal** page to post them directly to the relevant job account.</span></span>

1. <span data-ttu-id="efc51-131">Choisissez l'icône de ![l'ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles compta. projet**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="efc51-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="efc51-132">Créez une ligne et renseignez les informations concernant les frais, notamment les informations dans les champs **N° projet** et **N° tâche projet**.</span><span class="sxs-lookup"><span data-stu-id="efc51-132">Create a new line and enter information about the expense, including information in the **Job No.** and **Job Task No** fields.</span></span>  
3. <span data-ttu-id="efc51-133">Lorsque la feuille est renseignée, cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="efc51-133">When the journal is complete, choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="efc51-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efc51-134">See Also</span></span>
[<span data-ttu-id="efc51-135">Gestion de projets</span><span class="sxs-lookup"><span data-stu-id="efc51-135">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="efc51-136">Finances</span><span class="sxs-lookup"><span data-stu-id="efc51-136">Finance</span></span>](finance.md)  
<span data-ttu-id="efc51-137">[Achats](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="efc51-137">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="efc51-138">[Ventes](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="efc51-138">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="efc51-139">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="efc51-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  