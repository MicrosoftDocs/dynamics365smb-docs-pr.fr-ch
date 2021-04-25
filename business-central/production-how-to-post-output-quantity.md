---
title: Validation par lots de la production et des temps d'exécution
description: La quantité de sortie représente l'avancement du travail sous la forme de la quantité finie et de la capacité utilisée du travail ou du poste de charge.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 923f68b13619013dd54062438c66192a682868bc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787892"
---
# <a name="batch-post-output-and-run-times"></a><span data-ttu-id="22fd2-103">Valider par lots la production et les temps d’exécution</span><span class="sxs-lookup"><span data-stu-id="22fd2-103">Batch Post Output and Run Times</span></span>
<span data-ttu-id="22fd2-104">La quantité de sortie représente l'avancement du travail sous la forme de la quantité finie et de la capacité utilisée du travail ou du poste de charge.</span><span class="sxs-lookup"><span data-stu-id="22fd2-104">The output quantity represents the work progress in the form of the finished quantity and used capacity of work or machine center.</span></span>

<span data-ttu-id="22fd2-105">Vous pouvez utiliser la feuille production pour :</span><span class="sxs-lookup"><span data-stu-id="22fd2-105">You can use the output journal to:</span></span>
*  <span data-ttu-id="22fd2-106">Ajustez le stock en fonction de la production des articles finis émanant de la production.</span><span class="sxs-lookup"><span data-stu-id="22fd2-106">Adjust inventory in connection with output of finished items from production.</span></span>
*  <span data-ttu-id="22fd2-107">Enregistrez les quantités et les rebuts pour chaque opération dans la gamme de production.</span><span class="sxs-lookup"><span data-stu-id="22fd2-107">Register quantities and scrap for each operation in production routing.</span></span>
*  <span data-ttu-id="22fd2-108">Enregistrez la configuration et le temps d'exécution pour les centres de travail et les postes de charge.</span><span class="sxs-lookup"><span data-stu-id="22fd2-108">Register setup and run time for work and machine centers.</span></span>

> [!NOTE]
> <span data-ttu-id="22fd2-109">Si le routage de production est utilisé, le stock est mis à jour uniquement lorsque vous validez la quantité produite durant la dernière opération.</span><span class="sxs-lookup"><span data-stu-id="22fd2-109">If production routing are used, the inventory is updated only when you post output quantity on the last operation.</span></span>

<span data-ttu-id="22fd2-110">La fenêtre **Feuille production** vous permet d’exécuter les mêmes tâches que celles de la fenêtre **Feuille production** et exécuter en même temps les tâches connexes de validation de la consommation.</span><span class="sxs-lookup"><span data-stu-id="22fd2-110">With the **Production Journal** window, you can perform the same tasks as in the **Output Journal** window and at the same time perform the related consumption posting tasks.</span></span> <span data-ttu-id="22fd2-111">Pour plus d'informations, voir [Enregistrer la consommation et la production pour une ligne ordre de fabrication lancé](production-how-to-register-consumption-and-output.md).</span><span class="sxs-lookup"><span data-stu-id="22fd2-111">For more information, see [Register Consumption and Output for One Released Production order line](production-how-to-register-consumption-and-output.md).</span></span>

## <a name="to-post-output-quantities-andor-register-run-times-for-one-or-more-production-order-lines"></a><span data-ttu-id="22fd2-112">Pour valider les quantités produites et/ou enregistrer les temps d’exécution pour une ou plusieurs lignes ordre de fabrication</span><span class="sxs-lookup"><span data-stu-id="22fd2-112">To post output quantities and/or register run times for one or more production order lines</span></span>
1. <span data-ttu-id="22fd2-113">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Feuille production**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="22fd2-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="22fd2-114">Renseignez les champs en indiquant les données relatives à la fabrication et/ou les temps d’exécution.</span><span class="sxs-lookup"><span data-stu-id="22fd2-114">Fill in the fields with the production order data and the output data and/or run time.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
  
    <span data-ttu-id="22fd2-115">Vous pouvez utiliser la fonction **Éclater gamme** pour générer des lignes feuille à partir des ordres de fabrication.</span><span class="sxs-lookup"><span data-stu-id="22fd2-115">You can use the **Explode Routing** function to generate journal lines from production orders.</span></span>
  
4. <span data-ttu-id="22fd2-116">Si l’opération est achevée, sélectionnez le champ **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="22fd2-116">If the operation has been completed, select the **Finished** field.</span></span>  
5. <span data-ttu-id="22fd2-117">Choisissez l’action **Valider** pour valider les opérations.</span><span class="sxs-lookup"><span data-stu-id="22fd2-117">Choose the **Post** action to post the operations.</span></span> 
 
<span data-ttu-id="22fd2-118">Les écritures comptables de capacité sont mises à jour pour les postes de charge ou centres de travail utilisés avec des informations sur le temps et la quantité de production et de rebut.</span><span class="sxs-lookup"><span data-stu-id="22fd2-118">Capacity ledger entries are updated for the used work or machine centers with information about time and quantity of output and scrap.</span></span> <span data-ttu-id="22fd2-119">Si vous avez validé la dernière opération, l'article sera ajouté au stock.</span><span class="sxs-lookup"><span data-stu-id="22fd2-119">If you posted the last operation, the item will be added to the inventory.</span></span> 

## <a name="see-also"></a><span data-ttu-id="22fd2-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22fd2-120">See Also</span></span>  
<span data-ttu-id="22fd2-121">[Valider la mise au rebut manuellement](production-how-to-post-scrap.md)
[Validation de sortie inversée](production-how-to-reverse-output-posting.md)
[Fabrication](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="22fd2-121">[Post Scrap Manually](production-how-to-post-scrap.md)
[Reverse Output Posting](production-how-to-reverse-output-posting.md)
[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="22fd2-122">Paramétrage de la production</span><span class="sxs-lookup"><span data-stu-id="22fd2-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="22fd2-123">[Planifié](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="22fd2-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="22fd2-124">Stock</span><span class="sxs-lookup"><span data-stu-id="22fd2-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="22fd2-125">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="22fd2-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
