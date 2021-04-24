---
title: 'Procédure : suppression des écritures budget des coûts | Microsoft Docs'
description: Vous utilisez le traitement par lots Supprimer écritures budget des coûts pour annuler les écritures de budget des coûts à partir du registre du budget des coûts.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e2f05388149e9e6587f916db79b652e64ad5d02e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774854"
---
# <a name="delete-cost-budget-entries"></a><span data-ttu-id="324e1-103">Supprimer écritures budget des coûts</span><span class="sxs-lookup"><span data-stu-id="324e1-103">Delete Cost Budget Entries</span></span>
<span data-ttu-id="324e1-104">Vous utilisez le traitement par lots **Supprimer écritures budget des coûts** pour annuler les écritures de budget des coûts à partir du registre du budget des coûts.</span><span class="sxs-lookup"><span data-stu-id="324e1-104">You use the **Delete Cost Budget Entries** batch job to cancel cost budget entries from the cost budget register.</span></span>  

<span data-ttu-id="324e1-105">Pour empêcher tout écart dans les écritures du budget des coûts et les écritures du registre des coûts, vous ne pouvez pas supprimer une écriture unique ou un lot d’écritures dans la liste des écritures du registre.</span><span class="sxs-lookup"><span data-stu-id="324e1-105">To prevent any gaps in the cost budget entries and cost register entries, you cannot delete a single entry or a batch of entries in the middle of the list of register entries.</span></span>  

### <a name="to-delete-a-cost-budget-entry"></a><span data-ttu-id="324e1-106">Pour supprimer une écriture budget des coûts</span><span class="sxs-lookup"><span data-stu-id="324e1-106">To delete a cost budget entry</span></span>  

1.  <span data-ttu-id="324e1-107">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Supprimer écritures budget des coûts**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="324e1-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Cost Budget Entries**, and then choose the related link.</span></span>  

    <span data-ttu-id="324e1-108">Le champ **N° hist. transaction de destination**</span><span class="sxs-lookup"><span data-stu-id="324e1-108">The **To Register No.**</span></span> <span data-ttu-id="324e1-109">affiche le numéro de la dernière écriture du registre et n’est pas modifiable.</span><span class="sxs-lookup"><span data-stu-id="324e1-109">field contains the last register entry number and cannot be changed.</span></span>  

    <span data-ttu-id="324e1-110">Vous pouvez utiliser le champ **N° hist. transaction d’origine**</span><span class="sxs-lookup"><span data-stu-id="324e1-110">You can use the **From Register No.**</span></span> <span data-ttu-id="324e1-111">pour sélectionner un numéro d’écriture du registre à partir duquel commencer la suppression.</span><span class="sxs-lookup"><span data-stu-id="324e1-111">field to select a register entry number from which the deletion should begin.</span></span>  
2.  <span data-ttu-id="324e1-112">Cliquez sur le bouton **OK** pour supprimer les écritures du budget des coûts sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="324e1-112">Choose the **OK** button to delete the selected cost budget entries.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="324e1-113">Pour éviter une suppression accidentelle des écritures du budget des coûts, vous pouvez clôturer les écritures du registre en marquant les lignes comme **Clôturées** dans le champ **Clôturées** de la page **Registre du budget des coûts**.</span><span class="sxs-lookup"><span data-stu-id="324e1-113">To avoid an accidental deletion of cost budget entries, you can close register entries by marking the lines as **Closed** in the **Closed** field on the **Cost Budget Registers** page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="324e1-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="324e1-114">See Also</span></span>  
<span data-ttu-id="324e1-115">[Comptabilité pour les coûts](finance-manage-cost-accounting.md)
[Création des budgets des coûts](finance-create-cost-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="324e1-115">[Accounting for Costs](finance-manage-cost-accounting.md)
[Creating Cost Budgets](finance-create-cost-budgets.md)</span></span>  
<span data-ttu-id="324e1-116">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="324e1-116">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]