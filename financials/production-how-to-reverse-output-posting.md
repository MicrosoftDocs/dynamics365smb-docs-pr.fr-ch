---
title: "Procédure de contrepassation de la validation de production | Microsoft Docs"
description: "Il arrive qu'une validation de production doive être contrepassée. C'est le cas, par exemple, si une erreur de saisie de données a été commise et qu'une quantité de production incorrecte a été validée pour un ordre de fabrication."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7ac453ff87d78e6be0567ba93b58c0f8938f4052
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-reverse-output-posting"></a><span data-ttu-id="38419-104">Procédure : contrepasser la validation de production</span><span class="sxs-lookup"><span data-stu-id="38419-104">How to: Reverse Output Posting</span></span>
<span data-ttu-id="38419-105">Il arrive qu'une validation de production doive être contrepassée.</span><span class="sxs-lookup"><span data-stu-id="38419-105">There are times when output posting must be reversed.</span></span> <span data-ttu-id="38419-106">C'est le cas, par exemple, si une erreur de saisie de données a été commise et qu'une quantité de production incorrecte a été validée pour un ordre de fabrication.</span><span class="sxs-lookup"><span data-stu-id="38419-106">An example of this would be if a data entry error occurred and an incorrect amount of output is posted to a production order.</span></span>  

## <a name="to-reverse-an-output-posting"></a><span data-ttu-id="38419-107">Pour contrepasser une validation de production</span><span class="sxs-lookup"><span data-stu-id="38419-107">To reverse an output posting</span></span>  
1.  <span data-ttu-id="38419-108">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Feuille production**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="38419-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Output Journal**, and then choose the related link.</span></span> <span data-ttu-id="38419-109">Sélectionnez votre lot.</span><span class="sxs-lookup"><span data-stu-id="38419-109">Select your batch.</span></span>  
2. <span data-ttu-id="38419-110">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="38419-110">Fill in the fields as necessary.</span></span> <span data-ttu-id="38419-111">Pour plus d'informations, voir [Procédure : valider par lots la production et les temps d'exécution](production-how-to-post-output-quantity.md).</span><span class="sxs-lookup"><span data-stu-id="38419-111">For more information, see [How to: Batch Post Output and Run Times](production-how-to-post-output-quantity.md).</span></span>
3.  <span data-ttu-id="38419-112">Dans le champ **Ecriture lettrage**, sélectionnez l'écriture comptable article associée.</span><span class="sxs-lookup"><span data-stu-id="38419-112">In the **Applies-To Entry** field, select the associated item ledger entry.</span></span> <span data-ttu-id="38419-113">Cette action contrepasse les écritures comptables capacité et article.</span><span class="sxs-lookup"><span data-stu-id="38419-113">This reverses the capacity and item ledger entries.</span></span>  
4. <span data-ttu-id="38419-114">Validez la contrepassation en validant la feuille.</span><span class="sxs-lookup"><span data-stu-id="38419-114">Post the reversal by posting the journal.</span></span>  

<span data-ttu-id="38419-115">Les écritures de la feuille production sont validées dans les écritures article comme un ajustement positif.</span><span class="sxs-lookup"><span data-stu-id="38419-115">The output journal entries are posted to the item ledger as a positive adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="38419-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38419-116">See Also</span></span>  
 <span data-ttu-id="38419-117">[Production](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="38419-117">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
 [<span data-ttu-id="38419-118">Paramétrage de la production</span><span class="sxs-lookup"><span data-stu-id="38419-118">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
 <span data-ttu-id="38419-119">[Planifié](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="38419-119">[Planning](production-planning.md)    </span></span>  
 [<span data-ttu-id="38419-120">STOCKS ET EN-COURS</span><span class="sxs-lookup"><span data-stu-id="38419-120">Inventory</span></span>](inventory-manage-inventory.md)  
 [<span data-ttu-id="38419-121">Achats</span><span class="sxs-lookup"><span data-stu-id="38419-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="38419-122">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="38419-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

