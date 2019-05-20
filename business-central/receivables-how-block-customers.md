---
title: Comment bloquer les ventes aux articles clients depuis les ventes ou les achats
description: Dans Business Central, un article peut être signalé comme bloqué pour la vente, bloqué pour l'achat ou bloqué dans tous les cas.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a2dee70270df135bc61ddef38e661758431b02a9
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251369"
---
# <a name="block-customers"></a><span data-ttu-id="8cf1e-103">Bloquer des clients</span><span class="sxs-lookup"><span data-stu-id="8cf1e-103">Block Customers</span></span>
<span data-ttu-id="8cf1e-104">Vous pouvez bloquer un client, par exemple à cause de son insolvabilité, afin que le client ne puisse pas être ajouté aux documents vente ou afin d'empêcher que d'autres transactions soient validées pour ce client.</span><span class="sxs-lookup"><span data-stu-id="8cf1e-104">You can block a customer, for example because of insolvency, so that the customer cannot be added to sales documents or so that no transactions can be posted for the customer.</span></span>

<span data-ttu-id="8cf1e-105">En plus de bloquer un client, vous pouvez définir des transactions Comptabilité client pour le client soit en attente en association avec les relances.</span><span class="sxs-lookup"><span data-stu-id="8cf1e-105">In addition to blocking a customer, you can set receivable transactions for the customer to be on hold in connection with reminders.</span></span> <span data-ttu-id="8cf1e-106">Pour plus d'informations, voir [Collecte des soldes restants](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="8cf1e-106">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>   

<span data-ttu-id="8cf1e-107">Le tableau suivant décrit les différentes options de blocage.</span><span class="sxs-lookup"><span data-stu-id="8cf1e-107">The following table describes the different blocking options.</span></span>  

|<span data-ttu-id="8cf1e-108">Option</span><span class="sxs-lookup"><span data-stu-id="8cf1e-108">Option</span></span>|<span data-ttu-id="8cf1e-109">Désignation</span><span class="sxs-lookup"><span data-stu-id="8cf1e-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="8cf1e-110">**Vide**</span><span class="sxs-lookup"><span data-stu-id="8cf1e-110">**Blank**</span></span>|<span data-ttu-id="8cf1e-111">Les transactions sont autorisés pour ce client.</span><span class="sxs-lookup"><span data-stu-id="8cf1e-111">Transactions are allowed for this customer.</span></span>|
|<span data-ttu-id="8cf1e-112">**Expédier**</span><span class="sxs-lookup"><span data-stu-id="8cf1e-112">**Ship**</span></span>|<span data-ttu-id="8cf1e-113">Vous ne pouvez pas créer des commandes et des expéditions pour ce client.</span><span class="sxs-lookup"><span data-stu-id="8cf1e-113">New orders and new shipments cannot be created for this customer.</span></span> <span data-ttu-id="8cf1e-114">Vous pouvez facturer les expéditions existantes qui ne l'ont pas encore été.</span><span class="sxs-lookup"><span data-stu-id="8cf1e-114">Existing shipments not yet invoiced can be invoiced.</span></span>|  
|<span data-ttu-id="8cf1e-115">**Facture**</span><span class="sxs-lookup"><span data-stu-id="8cf1e-115">**Invoice**</span></span>|<span data-ttu-id="8cf1e-116">Vous ne pouvez pas créer de commandes, d'expéditions ni de factures pour ce client.</span><span class="sxs-lookup"><span data-stu-id="8cf1e-116">New orders, new shipments, and new invoices cannot be created for this customer.</span></span> <span data-ttu-id="8cf1e-117">Vous ne pouvez pas facturer les expéditions existantes qui ne l'ont pas encore été.</span><span class="sxs-lookup"><span data-stu-id="8cf1e-117">Existing shipments not yet invoiced cannot be invoiced.</span></span>|  
|<span data-ttu-id="8cf1e-118">**Tous**</span><span class="sxs-lookup"><span data-stu-id="8cf1e-118">**All**</span></span>|<span data-ttu-id="8cf1e-119">Ce client n'est autorisé à effectuer aucune transaction, pas même un paiement.</span><span class="sxs-lookup"><span data-stu-id="8cf1e-119">No transaction is allowed for this customer, including payments.</span></span>|  

## <a name="to-block-a-customer"></a><span data-ttu-id="8cf1e-120">Pour bloquer un client</span><span class="sxs-lookup"><span data-stu-id="8cf1e-120">To block a customer</span></span>  
1. <span data-ttu-id="8cf1e-121">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Clients**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="8cf1e-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="8cf1e-122">Sélectionnez un client, puis cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="8cf1e-122">Select a customer, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="8cf1e-123">Renseignez le champ **Bloqué** avec l'une des options décrites ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="8cf1e-123">Fill in the **Blocked** field with one of the options described above.</span></span>

## <a name="see-also"></a><span data-ttu-id="8cf1e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8cf1e-124">See Also</span></span>  
[<span data-ttu-id="8cf1e-125">Enregistrer de nouveaux clients</span><span class="sxs-lookup"><span data-stu-id="8cf1e-125">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="8cf1e-126">Collecte des soldes restants</span><span class="sxs-lookup"><span data-stu-id="8cf1e-126">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="8cf1e-127">Gestion des comptes client</span><span class="sxs-lookup"><span data-stu-id="8cf1e-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
