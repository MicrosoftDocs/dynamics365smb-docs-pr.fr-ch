---
title: 'Procédure : suppression des écritures budget des coûts | Microsoft Docs'
description: Vous utilisez le traitement par lots Supprimer écritures budget des coûts pour annuler les écritures de budget des coûts à partir du registre du budget des coûts.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2ff0ede7bd5d90607a04b1037f5b6c6d092c1c33
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3916158"
---
# <a name="delete-cost-budget-entries"></a><span data-ttu-id="5261d-103">Supprimer écritures budget des coûts</span><span class="sxs-lookup"><span data-stu-id="5261d-103">Delete Cost Budget Entries</span></span>
<span data-ttu-id="5261d-104">Vous utilisez le traitement par lots **Supprimer écritures budget des coûts** pour annuler les écritures de budget des coûts à partir du registre du budget des coûts.</span><span class="sxs-lookup"><span data-stu-id="5261d-104">You use the **Delete Cost Budget Entries** batch job to cancel cost budget entries from the cost budget register.</span></span>  

<span data-ttu-id="5261d-105">Pour empêcher tout écart dans les écritures du budget des coûts et les écritures du registre des coûts, vous ne pouvez pas supprimer une écriture unique ou un lot d’écritures dans la liste des écritures du registre.</span><span class="sxs-lookup"><span data-stu-id="5261d-105">To prevent any gaps in the cost budget entries and cost register entries, you cannot delete a single entry or a batch of entries in the middle of the list of register entries.</span></span>  

### <a name="to-delete-a-cost-budget-entry"></a><span data-ttu-id="5261d-106">Pour supprimer une écriture budget des coûts</span><span class="sxs-lookup"><span data-stu-id="5261d-106">To delete a cost budget entry</span></span>  

1.  <span data-ttu-id="5261d-107">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Supprimer écritures budget des coûts** , puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="5261d-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Cost Budget Entries** , and then choose the related link.</span></span>  

    <span data-ttu-id="5261d-108">Le champ **N° hist. transaction de destination**</span><span class="sxs-lookup"><span data-stu-id="5261d-108">The **To Register No.**</span></span> <span data-ttu-id="5261d-109">affiche le numéro de la dernière écriture du registre et n’est pas modifiable.</span><span class="sxs-lookup"><span data-stu-id="5261d-109">field contains the last register entry number and cannot be changed.</span></span>  

    <span data-ttu-id="5261d-110">Vous pouvez utiliser le champ **N° hist. transaction d’origine**</span><span class="sxs-lookup"><span data-stu-id="5261d-110">You can use the **From Register No.**</span></span> <span data-ttu-id="5261d-111">pour sélectionner un numéro d’écriture du registre à partir duquel commencer la suppression.</span><span class="sxs-lookup"><span data-stu-id="5261d-111">field to select a register entry number from which the deletion should begin.</span></span>  
2.  <span data-ttu-id="5261d-112">Cliquez sur le bouton **OK** pour supprimer les écritures du budget des coûts sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="5261d-112">Choose the **OK** button to delete the selected cost budget entries.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="5261d-113">Pour éviter une suppression accidentelle des écritures du budget des coûts, vous pouvez clôturer les écritures du registre en marquant les lignes comme **Clôturées** dans le champ **Clôturées** de la page **Registre du budget des coûts** .</span><span class="sxs-lookup"><span data-stu-id="5261d-113">To avoid an accidental deletion of cost budget entries, you can close register entries by marking the lines as **Closed** in the **Closed** field on the **Cost Budget Registers** page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5261d-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5261d-114">See Also</span></span>  
<span data-ttu-id="5261d-115">[Comptabilité pour les coûts](finance-manage-cost-accounting.md)
[Création des budgets des coûts](finance-create-cost-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="5261d-115">[Accounting for Costs](finance-manage-cost-accounting.md)
[Creating Cost Budgets](finance-create-cost-budgets.md)</span></span>  
<span data-ttu-id="5261d-116">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5261d-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
