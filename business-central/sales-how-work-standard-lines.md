---
title: "Configurer des lignes standard pour les ventes et achats récurrents| Microsoft"
description: "Vous pouvez définir des lignes vente et des lignes achat que vous utilisez fréquemment et les insérer dans des documents achat et vente pour remplir rapidement les lignes avec des informations standard."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: df4f093ded0a55d45c40be15c5888035d6e3b2df
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="create-recurring-sales-and-purchase-lines"></a><span data-ttu-id="70e33-103">Créer des lignes ventes et achat récurrentes</span><span class="sxs-lookup"><span data-stu-id="70e33-103">Create Recurring Sales and Purchase Lines</span></span>
<span data-ttu-id="70e33-104">Si vous devez souvent créer des lignes ventes et des lignes achat comportant des informations similaires, vous pouvez configurer des lignes standard que vous pouvez ensuite insérer dans les documents vente et achat, par exemple, pour les commandes de réapprovisionnement récurrentes.</span><span class="sxs-lookup"><span data-stu-id="70e33-104">If you often need to create sales and purchase lines with similar information, you can set up standard lines that you can then insert on recurring sales and purchase documents, for example, for recurring replenishment orders.</span></span>  

<span data-ttu-id="70e33-105">La procédure suivante indique comment utiliser des lignes ventes standard.</span><span class="sxs-lookup"><span data-stu-id="70e33-105">The following procedure shows how to work with standard sales lines.</span></span> <span data-ttu-id="70e33-106">Elle est similaire pour les lignes achat standard.</span><span class="sxs-lookup"><span data-stu-id="70e33-106">It works in a similar way for standard purchase lines.</span></span>  

## <a name="to-set-up-standard-sales-lines"></a><span data-ttu-id="70e33-107">Configurer des lignes ventes standard</span><span class="sxs-lookup"><span data-stu-id="70e33-107">To set up standard sales lines</span></span>  
1. <span data-ttu-id="70e33-108">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Lignes vente standard**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="70e33-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Standard Sales Lines**, and then choose the related link.</span></span>  
2. <span data-ttu-id="70e33-109">Dans la fenêtre **Lignes vente standard**, cliquez sur l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="70e33-109">In the **Standard Sales Lines** window, choose the **New** action.</span></span>  
3. <span data-ttu-id="70e33-110">Sur le raccourci **Général**, complétez les champs, comme nécessaire.</span><span class="sxs-lookup"><span data-stu-id="70e33-110">On the **General** FastTab, fill the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="70e33-111">Dans le raccourci **Lignes**, renseignez les champs pour préparer les lignes ventes qui répercutent les lignes standard que vous prévoyez d'utiliser comme lignes récurrentes sur les documents ventes.</span><span class="sxs-lookup"><span data-stu-id="70e33-111">On the **Lines** FastTab, enter information in the fields to prepare sales lines that reflect the standard lines that you expect to use as recurring lines on sales documents.</span></span>  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a><span data-ttu-id="70e33-112">Pour insérer des lignes vente standard dans une facture vente</span><span class="sxs-lookup"><span data-stu-id="70e33-112">To insert standard sales lines on a sales invoice</span></span>
1. <span data-ttu-id="70e33-113">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Factures**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="70e33-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="70e33-114">Ouvrez la facture vente que vous souhaitez pour insérer une ou plusieurs lignes ventes standard.</span><span class="sxs-lookup"><span data-stu-id="70e33-114">Open the sales invoice that you want to insert one or more standard sales lines on.</span></span>
3. <span data-ttu-id="70e33-115">Choisissez l'action **Extraire les lignes vente récurrentes**.</span><span class="sxs-lookup"><span data-stu-id="70e33-115">Choose the **Get Recurring Sales Lines** action.</span></span>
4. <span data-ttu-id="70e33-116">Dans la fenêtre **Lignes vente récurrentes**, cliquez sur le bouton de recherche du champ **Code**, puis sélectionnez un ensemble de lignes vente standard.</span><span class="sxs-lookup"><span data-stu-id="70e33-116">In the **Recurring Sales Lines** window, choose the lookup button in the **Code** field, and then select a set of standard sales lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="70e33-117">Pour utiliser les lignes vente récurrentes définies avec le traitement par lots **Créer des factures vente récurrentes**, vous devez également renseigner les champs **Date début validité** et **Date fin validité** dans la fenêtre **Lignes vente récurrentes**.</span><span class="sxs-lookup"><span data-stu-id="70e33-117">To use the recurring sales lines set together with the **Create Recurring Sales Invoices** batch job, you must also fill in the **Valid From Date** and **Valid To Date** fields in the **Recurring Sales Lines** window.</span></span> <span data-ttu-id="70e33-118">Pour plus d'informations, voir la section « Pour créer plusieurs factures vente basées sur des lignes vente standard ».</span><span class="sxs-lookup"><span data-stu-id="70e33-118">For more information, see the "To create multiple sales invoices based on standard sales lines" section.</span></span>

5. <span data-ttu-id="70e33-119">Cliquez sur le bouton **OK** pour insérer les lignes vente standard dans la facture, que vous pouvez réutiliser comme tels ou modifier les informations.</span><span class="sxs-lookup"><span data-stu-id="70e33-119">Choose the **OK** button to insert the standard sales lines on the invoice where you can reuse them as is or edit the information.</span></span>

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a><span data-ttu-id="70e33-120">Pour créer plusieurs factures vente basées sur des lignes vente standard</span><span class="sxs-lookup"><span data-stu-id="70e33-120">To create multiple sales invoices based on standard sales lines</span></span>
<span data-ttu-id="70e33-121">Vous pouvez utiliser le traitement par lots **Créer des factures vente récurrentes** pour créer des factures vente en fonction des lignes vente standard qui sont affectées aux clients et avec des dates comptabilisation comprises entre les dates de début et de fin de validité que vous spécifiez dans les lignes vente standard.</span><span class="sxs-lookup"><span data-stu-id="70e33-121">You can use the **Create Recurring Sales Invoices** batch job to create sales invoices according to standard sales lines that are assigned to the customers and with posting dates within the valid-from and valid-to dates that you specify on the standard sales lines.</span></span>

> [!NOTE]
> <span data-ttu-id="70e33-122">Dans la fenêtre **Lignes vente récurrentes**, vous pouvez également spécifier un mode et un mandat de prélèvement.</span><span class="sxs-lookup"><span data-stu-id="70e33-122">In the **Recurring Sales Lines** window, you can also specify a direct-debit payment method and a direct-debit mandate.</span></span> <span data-ttu-id="70e33-123">Les factures vente qui sont créées avec le traitement par lots **Créer des factures vente récurrentes** incluront ensuite les informations requises pour collecter le paiement pour les factures vente par prélèvement automatique SEPA.</span><span class="sxs-lookup"><span data-stu-id="70e33-123">The sales invoices that are created with the **Create Recurring Sales Inv.** batch job will then include information required to collect payment for the sales invoices with SEPA direct debit.</span></span> <span data-ttu-id="70e33-124">Pour plus d'informations, voir [Recouvrement de paiements par prélèvement automatique SEPA](finance-collect-payments-with-sepa-direct-debit.md).</span><span class="sxs-lookup"><span data-stu-id="70e33-124">For more information, see [Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md).</span></span>

1. <span data-ttu-id="70e33-125">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Créer des factures vente récurrentes**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="70e33-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Create Recurring Sales Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="70e33-126">Dans la fenêtre **Créer des factures vente récurrentes**, renseignez les champs selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="70e33-126">In the **Create Recurring Sales Invoices** window, fill in the fields as necessary.</span></span>
3. <span data-ttu-id="70e33-127">Dans le champ de filtre **Code**, entrez le code des lignes vente standard associées à un client pour lequel vous souhaitez créer des factures vente.</span><span class="sxs-lookup"><span data-stu-id="70e33-127">In the **Code** filter field, enter the code for standard sales lines that are assigned to a customer that you want to create sales invoices for.</span></span>
4. <span data-ttu-id="70e33-128">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="70e33-128">Choose the **OK** button.</span></span>

<span data-ttu-id="70e33-129">Les factures vente sont créées pour les clients ayant le code vente client standard spécifié, et toute information de prélèvement automatique spécifiée, pour la validation à la date spécifiée.</span><span class="sxs-lookup"><span data-stu-id="70e33-129">Sales invoices are created for the customers with the specified standard customer sales code, and any specified direct-debit information, for posting on the specified date.</span></span>

## <a name="see-also"></a><span data-ttu-id="70e33-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70e33-130">See Also</span></span>  
[<span data-ttu-id="70e33-131">Ventes</span><span class="sxs-lookup"><span data-stu-id="70e33-131">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="70e33-132">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="70e33-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

