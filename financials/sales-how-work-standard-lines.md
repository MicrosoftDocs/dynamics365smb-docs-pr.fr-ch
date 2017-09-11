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
ms.translationtype: Human Translation
ms.sourcegitcommit: 85d15de13739e944ff8817b402b37ae1c7e1b144
ms.openlocfilehash: 980a0646317c2b5c02c0eadcde9ba984c11580c4
ms.contentlocale: fr-ch
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-create-recurring-sales-and-purchase-lines"></a><span data-ttu-id="2a65f-103">Procédure : Créer des lignes ventes et achat récurrentes</span><span class="sxs-lookup"><span data-stu-id="2a65f-103">How to: Create Recurring Sales and Purchase Lines</span></span>
<span data-ttu-id="2a65f-104">Si vous devez souvent créer des lignes ventes et des lignes achat comportant des informations similaires, vous pouvez configurer des lignes standard que vous pouvez ensuite insérer dans les documents vente et achat, par exemple, pour les commandes de réapprovisionnement récurrentes.</span><span class="sxs-lookup"><span data-stu-id="2a65f-104">If you often need to create sales and purchase lines with similar information, you can set up standard lines that you can then insert on recurring sales and purchase documents, for example, for recurring replenishment orders.</span></span>  

<span data-ttu-id="2a65f-105">La procédure suivante indique comment utiliser des lignes ventes standard.</span><span class="sxs-lookup"><span data-stu-id="2a65f-105">The following procedure shows how to work with standard sales lines.</span></span> <span data-ttu-id="2a65f-106">Elle est similaire pour les lignes achat standard.</span><span class="sxs-lookup"><span data-stu-id="2a65f-106">It works in a similar way for standard purchase lines.</span></span>  

## <a name="to-set-up-standard-sales-lines"></a><span data-ttu-id="2a65f-107">Configurer des lignes ventes standard</span><span class="sxs-lookup"><span data-stu-id="2a65f-107">To set up standard sales lines</span></span>  
1. <span data-ttu-id="2a65f-108">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Codes vente standard**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="2a65f-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Standard Sales Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2a65f-109">Dans la fenêtre **Lignes vente standard**, cliquez sur l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="2a65f-109">In the **Standard Sales Lines** window, choose the **New** action.</span></span>  
3. <span data-ttu-id="2a65f-110">Sur le raccourci **Général**, complétez les champs, comme nécessaire.</span><span class="sxs-lookup"><span data-stu-id="2a65f-110">On the **General** FastTab, fill the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="2a65f-111">Dans le raccourci **Lignes**, renseignez les champs pour préparer les lignes ventes qui répercutent les lignes standard que vous prévoyez d'utiliser comme lignes récurrentes sur les documents ventes.</span><span class="sxs-lookup"><span data-stu-id="2a65f-111">On the **Lines** FastTab, enter information in the fields to prepare sales lines that reflect the standard lines that you expect to use as recurring lines on sales documents.</span></span>  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a><span data-ttu-id="2a65f-112">Pour insérer des lignes vente standard dans une facture vente</span><span class="sxs-lookup"><span data-stu-id="2a65f-112">To insert standard sales lines on a sales invoice</span></span>
1. <span data-ttu-id="2a65f-113">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Factures**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="2a65f-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="2a65f-114">Ouvrez la facture vente que vous souhaitez pour insérer une ou plusieurs lignes ventes standard.</span><span class="sxs-lookup"><span data-stu-id="2a65f-114">Open the sales invoice that you want to insert one or more standard sales lines on.</span></span>
3. <span data-ttu-id="2a65f-115">Choisissez l'action **Extraire les lignes vente récurrentes**.</span><span class="sxs-lookup"><span data-stu-id="2a65f-115">Choose the **Get Recurring Sales Lines** action.</span></span>
4. <span data-ttu-id="2a65f-116">Dans la fenêtre **Lignes vente récurrentes**, cliquez sur le bouton de recherche du champ **Code**, puis sélectionnez un ensemble de lignes vente standard.</span><span class="sxs-lookup"><span data-stu-id="2a65f-116">In the **Recurring Sales Lines** window, choose the lookup button in the **Code** field, and then select a set of standard sales lines.</span></span>
5. <span data-ttu-id="2a65f-117">Choisissez le bouton **OK** pour insérer les lignes vente standard dans la facture, que vous pouvez réutiliser comme tels ou modifier les informations.</span><span class="sxs-lookup"><span data-stu-id="2a65f-117">Choose the **OK** button to insert the standard sales lines on the invoice, where you can reuse as is or edit the information.</span></span>

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a><span data-ttu-id="2a65f-118">Pour créer plusieurs factures vente basées sur des lignes vente standard</span><span class="sxs-lookup"><span data-stu-id="2a65f-118">To create multiple sales invoices based on standard sales lines</span></span>
<span data-ttu-id="2a65f-119">Vous pouvez utiliser le traitement par lots **Créer des factures vente récurrentes**</span><span class="sxs-lookup"><span data-stu-id="2a65f-119">You can use the **Create Recurring Sales Inv.**</span></span> <span data-ttu-id="2a65f-120">pour créer des factures vente en fonction des lignes vente standard qui sont affectés aux clients et avec des dates comptabilisation comprises entre les dates de début et de fin de validité que vous spécifiez dans le code vente standard.</span><span class="sxs-lookup"><span data-stu-id="2a65f-120">batch job to create sales invoices according to standard sales lines that are assigned to the customers and with posting dates within the valid-from and valid-to dates that you specify on the standard sales code.</span></span>

<span data-ttu-id="2a65f-121">Dans la fenêtre **Lignes vente récurrentes**, vous pouvez également spécifier un mode et un mandat de prélèvement.</span><span class="sxs-lookup"><span data-stu-id="2a65f-121">In the **Recurring Sales Lines** window, you can also specify a direct-debit payment method and a direct-debit mandate.</span></span> <span data-ttu-id="2a65f-122">Les factures vente créées avec le traitement par lots **Créer des factures vente récurrentes**</span><span class="sxs-lookup"><span data-stu-id="2a65f-122">The sales invoices that are created with the **Create Recurring Sales Inv.**</span></span> <span data-ttu-id="2a65f-123">comprend alors les informations requises pour effectuer le recouvrement des factures vente par prélèvement automatique SEPA.</span><span class="sxs-lookup"><span data-stu-id="2a65f-123">batch job will then include information required to collect payment for the sales invoices with SEPA direct debit.</span></span> <span data-ttu-id="2a65f-124">Pour plus d'informations, voir Recouvrement de paiements par prélèvement automatique SEPA.</span><span class="sxs-lookup"><span data-stu-id="2a65f-124">For more information, see Collect Payments with SEPA Direct Debit.</span></span>

1. <span data-ttu-id="2a65f-125">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Créer des factures vente récurrentes**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="2a65f-125">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Create Recurring Sales Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="2a65f-126">Dans **Créer des factures vente récurrentes**</span><span class="sxs-lookup"><span data-stu-id="2a65f-126">In the **Create Recurring Sales Inv.**</span></span> <span data-ttu-id="2a65f-127">renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="2a65f-127">window, fill in the fields as necessary.</span></span>
3. <span data-ttu-id="2a65f-128">Dans le champ **Code**, entrez le code des lignes vente standard associées à un client pour lequel vous souhaitez créer des factures vente.</span><span class="sxs-lookup"><span data-stu-id="2a65f-128">In the **Code** field, enter the code for standard sales lines assigned to a customer that you want to create sales invoices for.</span></span>
4. <span data-ttu-id="2a65f-129">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a65f-129">Choose the **OK** button.</span></span>

<span data-ttu-id="2a65f-130">Les factures vente sont créées pour les clients ayant le code vente client standard spécifié, et toute information de prélèvement automatique spécifiée, pour la validation à la date spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2a65f-130">Sales invoices are created for the customers with the specified standard customer sales code, and any specified direct-debit information, for posting on the specified date.</span></span>

## <a name="see-also"></a><span data-ttu-id="2a65f-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a65f-131">See Also</span></span>  
[<span data-ttu-id="2a65f-132">Ventes</span><span class="sxs-lookup"><span data-stu-id="2a65f-132">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="2a65f-133">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2a65f-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

