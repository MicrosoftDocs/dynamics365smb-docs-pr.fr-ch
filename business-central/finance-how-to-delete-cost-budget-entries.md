---
title: "Procédure : suppression des écritures budget des coûts | Microsoft Docs"
description: "Vous utilisez le traitement par lots **Supprimer écritures budget des coûts** pour annuler les écritures de budget des coûts à partir du registre du budget des coûts."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: cdd7f7cfb2645d780df47bfb75ec7392c1739843
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="delete-cost-budget-entries"></a><span data-ttu-id="ee7b9-103">Supprimer écritures budget des coûts</span><span class="sxs-lookup"><span data-stu-id="ee7b9-103">Delete Cost Budget Entries</span></span>
<span data-ttu-id="ee7b9-104">Vous utilisez le traitement par lots **Supprimer écritures budget des coûts** pour annuler les écritures de budget des coûts à partir du registre du budget des coûts.</span><span class="sxs-lookup"><span data-stu-id="ee7b9-104">You use the **Delete Cost Budget Entries** batch job to cancel cost budget entries from the cost budget register.</span></span>  

<span data-ttu-id="ee7b9-105">Pour empêcher tout écart dans les écritures du budget des coûts et les écritures du registre des coûts, vous ne pouvez pas supprimer une écriture unique ou un lot d'écritures dans la liste des écritures du registre.</span><span class="sxs-lookup"><span data-stu-id="ee7b9-105">To prevent any gaps in the cost budget entries and cost register entries, you cannot delete a single entry or a batch of entries in the middle of the list of register entries.</span></span>  

### <a name="to-delete-a-cost-budget-entry"></a><span data-ttu-id="ee7b9-106">Pour supprimer une écriture budget des coûts</span><span class="sxs-lookup"><span data-stu-id="ee7b9-106">To delete a cost budget entry</span></span>  

1.  <span data-ttu-id="ee7b9-107">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Supprimer écritures budget des coûts**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="ee7b9-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Cost Budget Entries**, and then choose the related link.</span></span>  

    <span data-ttu-id="ee7b9-108">Le champ **N° hist. transaction de destination**</span><span class="sxs-lookup"><span data-stu-id="ee7b9-108">The **To Register No.**</span></span> <span data-ttu-id="ee7b9-109">affiche le numéro de la dernière écriture du registre et n'est pas modifiable.</span><span class="sxs-lookup"><span data-stu-id="ee7b9-109">field contains the last register entry number and cannot be changed.</span></span>  

    <span data-ttu-id="ee7b9-110">Vous pouvez utiliser le champ **N° hist. transaction d'origine**</span><span class="sxs-lookup"><span data-stu-id="ee7b9-110">You can use the **From Register No.**</span></span> <span data-ttu-id="ee7b9-111">pour sélectionner un numéro d'écriture du registre à partir duquel commencer la suppression.</span><span class="sxs-lookup"><span data-stu-id="ee7b9-111">field to select a register entry number from which the deletion should begin.</span></span>  
2.  <span data-ttu-id="ee7b9-112">Cliquez sur le bouton **OK** pour supprimer les écritures du budget des coûts sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="ee7b9-112">Choose the **OK** button to delete the selected cost budget entries.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ee7b9-113">Pour éviter une suppression accidentelle des écritures du budget des coûts, vous pouvez clôturer les écritures du registre en marquant les lignes comme **Clôturées** dans le champ **Clôturées** de la fenêtre **Registre du budget des coûts**.</span><span class="sxs-lookup"><span data-stu-id="ee7b9-113">To avoid an accidental deletion of cost budget entries, you can close register entries by marking the lines as **Closed** in the **Closed** field in the **Cost Budget Registers** window.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ee7b9-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee7b9-114">See Also</span></span>  
<span data-ttu-id="ee7b9-115">[Comptabilité pour les coûts](finance-manage-cost-accounting.md)
[Création des budgets des coûts](finance-create-cost-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="ee7b9-115">[Accounting for Costs](finance-manage-cost-accounting.md)
[Creating Cost Budgets](finance-create-cost-budgets.md)</span></span>  
<span data-ttu-id="ee7b9-116">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ee7b9-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

