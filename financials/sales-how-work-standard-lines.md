---
title: "Configurer et utiliser des lignes standard pour les ventes et achats récurrents| Microsoft"
description: "Vous pouvez définir des lignes vente et des lignes achat que vous utilisez fréquemment et les insérer dans des documents achat et vente pour remplir rapidement les lignes avec des informations standard."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7c5820db4d8aa65ddeddfd5ee27f0a7e89100abf
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="create-recurring-sales-and-purchase-lines"></a><span data-ttu-id="9b9dc-103">Créer des lignes ventes et achat récurrentes</span><span class="sxs-lookup"><span data-stu-id="9b9dc-103">Create Recurring Sales and Purchase Lines</span></span>
<span data-ttu-id="9b9dc-104">Si vous devez souvent créer des lignes ventes et des lignes achat comportant des informations similaires, vous pouvez configurer des lignes standard que vous pouvez ensuite insérer dans les documents vente et achat, par exemple, pour les commandes de réapprovisionnement récurrentes.</span><span class="sxs-lookup"><span data-stu-id="9b9dc-104">If you often need to create sales and purchase lines with similar information, you can set up standard lines that you can then insert on recurring sales and purchase documents, for example, for recurring replenishment orders.</span></span>  

<span data-ttu-id="9b9dc-105">La procédure suivante indique comment utiliser des lignes ventes standard.</span><span class="sxs-lookup"><span data-stu-id="9b9dc-105">The following procedure shows how to work with standard sales lines.</span></span> <span data-ttu-id="9b9dc-106">Elle est similaire pour les lignes achat standard.</span><span class="sxs-lookup"><span data-stu-id="9b9dc-106">It works in a similar way for standard purchase lines.</span></span>  

## <a name="to-set-up-standard-sales-lines"></a><span data-ttu-id="9b9dc-107">Configurer des lignes ventes standard</span><span class="sxs-lookup"><span data-stu-id="9b9dc-107">To set up standard sales lines</span></span>  
1. <span data-ttu-id="9b9dc-108">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Codes vente standard**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="9b9dc-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Standard Sales Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9b9dc-109">Dans la fenêtre **Lignes vente standard**, cliquez sur l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="9b9dc-109">In the **Standard Sales Lines** window, choose the **New** action.</span></span>  
3. <span data-ttu-id="9b9dc-110">Sur le raccourci **Général**, complétez les champs, comme nécessaire.</span><span class="sxs-lookup"><span data-stu-id="9b9dc-110">On the **General** FastTab, fill the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="9b9dc-111">Dans le raccourci **Lignes**, renseignez les champs pour préparer les lignes ventes qui répercutent les lignes standard que vous prévoyez d'utiliser comme lignes récurrentes sur les documents ventes.</span><span class="sxs-lookup"><span data-stu-id="9b9dc-111">On the **Lines** FastTab, enter information in the fields to prepare sales lines that reflect the standard lines that you expect to use as recurring lines on sales documents.</span></span>  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a><span data-ttu-id="9b9dc-112">Pour insérer des lignes vente standard dans une facture vente</span><span class="sxs-lookup"><span data-stu-id="9b9dc-112">To insert standard sales lines on a sales invoice</span></span>
1. <span data-ttu-id="9b9dc-113">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Factures**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="9b9dc-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="9b9dc-114">Ouvrez la facture vente que vous souhaitez pour insérer une ou plusieurs lignes ventes standard.</span><span class="sxs-lookup"><span data-stu-id="9b9dc-114">Open the sales invoice that you want to insert one or more standard sales lines on.</span></span>
3. <span data-ttu-id="9b9dc-115">Choisissez l'action **Extraire les lignes vente récurrentes**.</span><span class="sxs-lookup"><span data-stu-id="9b9dc-115">Choose the **Get Recurring Sales Lines** action.</span></span>
4. <span data-ttu-id="9b9dc-116">Dans la fenêtre **Lignes vente récurrentes**, cliquez sur le bouton de recherche du champ **Code**, puis sélectionnez un ensemble de lignes vente standard.</span><span class="sxs-lookup"><span data-stu-id="9b9dc-116">In the **Recurring Sales Lines** window, choose the lookup button in the **Code** field, and then select a set of standard sales lines.</span></span>
5. <span data-ttu-id="9b9dc-117">Choisissez le bouton **OK** pour insérer les lignes vente standard dans la facture, que vous pouvez réutiliser comme tels ou modifier les informations.</span><span class="sxs-lookup"><span data-stu-id="9b9dc-117">Choose the **OK** button to insert the standard sales lines on the invoice, where you can reuse as is or edit the information.</span></span>

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a><span data-ttu-id="9b9dc-118">Pour créer plusieurs factures vente basées sur des lignes vente standard</span><span class="sxs-lookup"><span data-stu-id="9b9dc-118">To create multiple sales invoices based on standard sales lines</span></span>
<span data-ttu-id="9b9dc-119">Vous pouvez utiliser le traitement par lots **Créer des factures vente récurrentes** pour créer des factures vente en fonction des lignes vente standard qui sont affectées aux clients et avec des dates comptabilisation comprises entre les dates de début et de fin de validité que vous spécifiez dans le code vente standard.</span><span class="sxs-lookup"><span data-stu-id="9b9dc-119">You can use the **Create Recurring Sales Inv.** batch job to create sales invoices according to standard sales lines that are assigned to the customers and with posting dates within the valid-from and valid-to dates that you specify on the standard sales code.</span></span>

<span data-ttu-id="9b9dc-120">Dans la fenêtre **Lignes vente récurrentes**, vous pouvez également spécifier un mode et un mandat de prélèvement.</span><span class="sxs-lookup"><span data-stu-id="9b9dc-120">In the **Recurring Sales Lines** window, you can also specify a direct-debit payment method and a direct-debit mandate.</span></span> <span data-ttu-id="9b9dc-121">Les factures vente qui sont créées avec le traitement par lots **Créer des factures vente récurrentes** incluront ensuite les informations requises pour collecter le paiement pour les factures vente par prélèvement automatique SEPA.</span><span class="sxs-lookup"><span data-stu-id="9b9dc-121">The sales invoices that are created with the **Create Recurring Sales Inv.** batch job will then include information required to collect payment for the sales invoices with SEPA direct debit.</span></span> <span data-ttu-id="9b9dc-122">Pour plus d'informations, voir [Recouvrement de paiements par prélèvement automatique SEPA](finance-collect-payments-with-sepa-direct-debit.md).</span><span class="sxs-lookup"><span data-stu-id="9b9dc-122">For more information, see [Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md).</span></span>

1. <span data-ttu-id="9b9dc-123">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Créer des factures vente récurrentes**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="9b9dc-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Create Recurring Sales Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="9b9dc-124">Dans la fenêtre **Créer des factures vente récurrentes**, renseignez les champs selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="9b9dc-124">In the **Create Recurring Sales Inv.** window, fill in the fields as necessary.</span></span>
3. <span data-ttu-id="9b9dc-125">Dans le champ **Code**, entrez le code des lignes vente standard associées à un client pour lequel vous souhaitez créer des factures vente.</span><span class="sxs-lookup"><span data-stu-id="9b9dc-125">In the **Code** field, enter the code for standard sales lines assigned to a customer that you want to create sales invoices for.</span></span>
4. <span data-ttu-id="9b9dc-126">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="9b9dc-126">Choose the **OK** button.</span></span>

<span data-ttu-id="9b9dc-127">Les factures vente sont créées pour les clients ayant le code vente client standard spécifié, et toute information de prélèvement automatique spécifiée, pour la validation à la date spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9b9dc-127">Sales invoices are created for the customers with the specified standard customer sales code, and any specified direct-debit information, for posting on the specified date.</span></span>

## <a name="see-also"></a><span data-ttu-id="9b9dc-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b9dc-128">See Also</span></span>  
[<span data-ttu-id="9b9dc-129">Ventes</span><span class="sxs-lookup"><span data-stu-id="9b9dc-129">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="9b9dc-130">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9b9dc-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

