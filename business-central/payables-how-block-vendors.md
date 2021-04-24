---
title: Comment bloquer les achats en provenance/vers des fournisseurs
description: Vous pouvez empêcher l’inclusion de fournisseurs dans des transactions, ou simplement bloquer de nouveaux paiements qui leur sont destinés.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: c6a8b290eb619002aac1deb5796430767e46004c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5780572"
---
# <a name="block-vendors"></a><span data-ttu-id="4bd61-103">Bloquer des fournisseurs</span><span class="sxs-lookup"><span data-stu-id="4bd61-103">Block Vendors</span></span>
<span data-ttu-id="4bd61-104">Vous pouvez bloquer un fournisseur, par exemple à cause de son insolvabilité, afin que ce fournisseur ne puisse pas être ajouté à des documents achat ou afin d’empêcher que des paiements puissent être validés pour ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4bd61-104">You can block a vendor, for example because of insolvency, so that the vendor cannot be added to purchase documents or so that no payments can be posted for the vendor.</span></span>

<span data-ttu-id="4bd61-105">Le tableau suivant décrit les options pour bloquer des fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="4bd61-105">The following table describes the options for blocking vendors.</span></span>  

|<span data-ttu-id="4bd61-106">Option</span><span class="sxs-lookup"><span data-stu-id="4bd61-106">Option</span></span>|<span data-ttu-id="4bd61-107">Description</span><span class="sxs-lookup"><span data-stu-id="4bd61-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="4bd61-108">**Vide**</span><span class="sxs-lookup"><span data-stu-id="4bd61-108">**Blank**</span></span>|<span data-ttu-id="4bd61-109">Les transactions sont autorisées pour ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4bd61-109">Transactions are allowed for this vendor.</span></span>|
|<span data-ttu-id="4bd61-110">**Paiement**</span><span class="sxs-lookup"><span data-stu-id="4bd61-110">**Payment**</span></span>|<span data-ttu-id="4bd61-111">Il est impossible de créer de nouveaux paiements pour ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4bd61-111">New payments cannot be created for this vendor.</span></span>|  
|<span data-ttu-id="4bd61-112">**Tous**</span><span class="sxs-lookup"><span data-stu-id="4bd61-112">**All**</span></span>|<span data-ttu-id="4bd61-113">Aucune transaction n’est autorisée pour ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4bd61-113">No transactions are allowed for this vendor.</span></span>|  

## <a name="to-block-a-vendor"></a><span data-ttu-id="4bd61-114">Pour bloquer un fournisseur</span><span class="sxs-lookup"><span data-stu-id="4bd61-114">To block a vendor</span></span>  
1. <span data-ttu-id="4bd61-115">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Fournisseurs**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="4bd61-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="4bd61-116">Sélectionnez le fournisseur que vous souhaitez bloquer.</span><span class="sxs-lookup"><span data-stu-id="4bd61-116">Select the vendor that you want to block.</span></span>
3. <span data-ttu-id="4bd61-117">Dans le champ **Bloqué**, choisissez l’une des options de blocage.</span><span class="sxs-lookup"><span data-stu-id="4bd61-117">In the **Blocked** field, choose one of the options for blocking.</span></span>

## <a name="see-also"></a><span data-ttu-id="4bd61-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bd61-118">See Also</span></span>  
[<span data-ttu-id="4bd61-119">Enregistrer un nouveau fournisseur</span><span class="sxs-lookup"><span data-stu-id="4bd61-119">Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
[<span data-ttu-id="4bd61-120">Effectuer des paiements</span><span class="sxs-lookup"><span data-stu-id="4bd61-120">Making Payments</span></span>](payables-make-payments.md)  
[<span data-ttu-id="4bd61-121">Gestion des comptes fournisseur</span><span class="sxs-lookup"><span data-stu-id="4bd61-121">Managing Payables</span></span>](payables-manage-payables.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]