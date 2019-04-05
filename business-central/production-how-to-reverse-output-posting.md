---
title: Procédure de contrepassation de la validation de production | Microsoft Docs
description: Il arrive qu'une validation de production doive être contrepassée. C'est le cas, par exemple, si une erreur de saisie de données a été commise et qu'une quantité de production incorrecte a été validée pour un ordre de fabrication.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: fb107d6d165ede233799ab165d735c030c0c8bba
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820540"
---
# <a name="reverse-output-posting"></a><span data-ttu-id="1bc33-104">Contrepasser la validation de production</span><span class="sxs-lookup"><span data-stu-id="1bc33-104">Reverse Output Posting</span></span>
<span data-ttu-id="1bc33-105">Il arrive qu'une validation de production doive être contrepassée.</span><span class="sxs-lookup"><span data-stu-id="1bc33-105">There are times when output posting must be reversed.</span></span> <span data-ttu-id="1bc33-106">C'est le cas, par exemple, si une erreur de saisie de données a été commise et qu'une quantité de production incorrecte a été validée pour un ordre de fabrication.</span><span class="sxs-lookup"><span data-stu-id="1bc33-106">An example of this would be if a data entry error occurred and an incorrect amount of output is posted to a production order.</span></span>  

## <a name="to-reverse-an-output-posting"></a><span data-ttu-id="1bc33-107">Pour contrepasser une validation de production</span><span class="sxs-lookup"><span data-stu-id="1bc33-107">To reverse an output posting</span></span>  
1.  <span data-ttu-id="1bc33-108">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuille production**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="1bc33-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span> <span data-ttu-id="1bc33-109">Sélectionnez votre lot.</span><span class="sxs-lookup"><span data-stu-id="1bc33-109">Select your batch.</span></span>  
2. <span data-ttu-id="1bc33-110">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="1bc33-110">Fill in the fields as necessary.</span></span> <span data-ttu-id="1bc33-111">Pour plus d'informations, voir [Valider par lots la production et les temps d'exécution](production-how-to-post-output-quantity.md).</span><span class="sxs-lookup"><span data-stu-id="1bc33-111">For more information, see [Batch Post Output and Run Times](production-how-to-post-output-quantity.md).</span></span>
3.  <span data-ttu-id="1bc33-112">Dans le champ **Ecriture lettrage**, sélectionnez l'écriture comptable article associée.</span><span class="sxs-lookup"><span data-stu-id="1bc33-112">In the **Applies-To Entry** field, select the associated item ledger entry.</span></span> <span data-ttu-id="1bc33-113">Cette action contrepasse les écritures comptables capacité et article.</span><span class="sxs-lookup"><span data-stu-id="1bc33-113">This reverses the capacity and item ledger entries.</span></span>  
4. <span data-ttu-id="1bc33-114">Validez la contrepassation en validant la feuille.</span><span class="sxs-lookup"><span data-stu-id="1bc33-114">Post the reversal by posting the journal.</span></span>  

<span data-ttu-id="1bc33-115">Les écritures de la feuille production sont validées dans les écritures article comme un ajustement positif.</span><span class="sxs-lookup"><span data-stu-id="1bc33-115">The output journal entries are posted to the item ledger as a positive adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1bc33-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1bc33-116">See Also</span></span>  
 <span data-ttu-id="1bc33-117">[Production](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="1bc33-117">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
 [<span data-ttu-id="1bc33-118">Paramétrage de la production</span><span class="sxs-lookup"><span data-stu-id="1bc33-118">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
 <span data-ttu-id="1bc33-119">[Planifié](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="1bc33-119">[Planning](production-planning.md)    </span></span>  
 [<span data-ttu-id="1bc33-120">STOCKS ET EN-COURS</span><span class="sxs-lookup"><span data-stu-id="1bc33-120">Inventory</span></span>](inventory-manage-inventory.md)  
 [<span data-ttu-id="1bc33-121">Achats</span><span class="sxs-lookup"><span data-stu-id="1bc33-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="1bc33-122">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1bc33-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
