---
title: Comment bloquer les ventes de clients
description: Si nécessaire, vous pouvez empêcher qu'un client soit ajouté aux documents de vente et d'autres transactions de vente.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 720eb2d5899ba067dbcee8dc97492ebcd01b1abd
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3779200"
---
# <a name="block-customers"></a><span data-ttu-id="d8a46-103">Bloquer des clients</span><span class="sxs-lookup"><span data-stu-id="d8a46-103">Block Customers</span></span>
<span data-ttu-id="d8a46-104">Vous pouvez bloquer un client, par exemple à cause de son insolvabilité, afin que le client ne puisse pas être ajouté aux documents vente ou afin d'empêcher que d'autres transactions soient validées pour ce client.</span><span class="sxs-lookup"><span data-stu-id="d8a46-104">You can block a customer, for example because of insolvency, so that the customer cannot be added to sales documents or so that no transactions can be posted for the customer.</span></span>

<span data-ttu-id="d8a46-105">En plus de bloquer un client, vous pouvez définir des transactions Comptabilité client pour le client soit en attente en association avec les relances.</span><span class="sxs-lookup"><span data-stu-id="d8a46-105">In addition to blocking a customer, you can set receivable transactions for the customer to be on hold in connection with reminders.</span></span> <span data-ttu-id="d8a46-106">Pour plus d'informations, voir [Collecte des soldes restants](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="d8a46-106">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>   

<span data-ttu-id="d8a46-107">Le tableau suivant décrit les options pour bloquer des clients.</span><span class="sxs-lookup"><span data-stu-id="d8a46-107">The following table describes the options for blocking customers.</span></span>  

|<span data-ttu-id="d8a46-108">Option</span><span class="sxs-lookup"><span data-stu-id="d8a46-108">Option</span></span>|<span data-ttu-id="d8a46-109">Description</span><span class="sxs-lookup"><span data-stu-id="d8a46-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="d8a46-110">**Vide**</span><span class="sxs-lookup"><span data-stu-id="d8a46-110">**Blank**</span></span>|<span data-ttu-id="d8a46-111">Les transactions sont autorisés pour ce client.</span><span class="sxs-lookup"><span data-stu-id="d8a46-111">Transactions are allowed for this customer.</span></span>|
|<span data-ttu-id="d8a46-112">**Expédier**</span><span class="sxs-lookup"><span data-stu-id="d8a46-112">**Ship**</span></span>|<span data-ttu-id="d8a46-113">Vous ne pouvez pas créer des commandes et des expéditions pour ce client.</span><span class="sxs-lookup"><span data-stu-id="d8a46-113">New orders and new shipments cannot be created for this customer.</span></span> <span data-ttu-id="d8a46-114">Vous pouvez facturer les expéditions existantes qui ne l'ont pas encore été.</span><span class="sxs-lookup"><span data-stu-id="d8a46-114">Existing shipments not yet invoiced can be invoiced.</span></span>|  
|<span data-ttu-id="d8a46-115">**Facture**</span><span class="sxs-lookup"><span data-stu-id="d8a46-115">**Invoice**</span></span>|<span data-ttu-id="d8a46-116">Vous ne pouvez pas créer de commandes, d'expéditions ni de factures pour ce client.</span><span class="sxs-lookup"><span data-stu-id="d8a46-116">New orders, new shipments, and new invoices cannot be created for this customer.</span></span> <span data-ttu-id="d8a46-117">Vous ne pouvez pas facturer les expéditions existantes qui ne l'ont pas encore été.</span><span class="sxs-lookup"><span data-stu-id="d8a46-117">Existing shipments not yet invoiced cannot be invoiced.</span></span> <span data-ttu-id="d8a46-118">Vous pouvez toujours envoyer des rappels et des factures d'intérêts au client.</span><span class="sxs-lookup"><span data-stu-id="d8a46-118">You can still send reminders and finance charge memos to the customer.</span></span>|  
|<span data-ttu-id="d8a46-119">**Tous**</span><span class="sxs-lookup"><span data-stu-id="d8a46-119">**All**</span></span>|<span data-ttu-id="d8a46-120">Ce client n'est autorisé à effectuer aucune transaction, pas même un paiement.</span><span class="sxs-lookup"><span data-stu-id="d8a46-120">No transaction is allowed for this customer, including payments.</span></span>|  

## <a name="to-block-a-customer"></a><span data-ttu-id="d8a46-121">Pour bloquer un client</span><span class="sxs-lookup"><span data-stu-id="d8a46-121">To block a customer</span></span>  
1. <span data-ttu-id="d8a46-122">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Clients**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="d8a46-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="d8a46-123">Sélectionnez un client, puis cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="d8a46-123">Select a customer, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="d8a46-124">Dans le champ **Bloqué**, choisissez ce que vous souhaitez bloquer, comme décrit dans le tableau ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="d8a46-124">In the **Blocked** field, choose what to block, as described in the table above.</span></span>

## <a name="see-also"></a><span data-ttu-id="d8a46-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8a46-125">See Also</span></span>  
[<span data-ttu-id="d8a46-126">Enregistrer de nouveaux clients</span><span class="sxs-lookup"><span data-stu-id="d8a46-126">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="d8a46-127">Collecte des soldes restants</span><span class="sxs-lookup"><span data-stu-id="d8a46-127">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="d8a46-128">Gestion des comptes client</span><span class="sxs-lookup"><span data-stu-id="d8a46-128">Managing Receivables</span></span>](receivables-manage-receivables.md)  
