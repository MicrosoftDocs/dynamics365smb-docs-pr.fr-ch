---
title: 'Procédure : corriger des acomptes | Microsoft Docs'
description: Vous pouvez apporter une correction à une commande après avoir validé une facture acompte pour la commande. Vous pouvez ajouter des lignes à une commande après avoir émis un acompte, puis vous pouvez valider une autre facture acompte, mais vous ne pouvez pas supprimer une ligne d'une commande après avoir facturé un acompte pour la ligne.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 93a93bac30f2d958039974f75c8aca9a5227f3ce
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306139"
---
# <a name="correct-prepayments"></a><span data-ttu-id="243fc-104">Corriger des acomptes</span><span class="sxs-lookup"><span data-stu-id="243fc-104">Correct Prepayments</span></span>
<span data-ttu-id="243fc-105">Vous pouvez apporter une correction à une commande après avoir validé une facture acompte pour la commande.</span><span class="sxs-lookup"><span data-stu-id="243fc-105">You can make a correction to an order after you have posted a prepayment invoice for the order.</span></span> <span data-ttu-id="243fc-106">Vous pouvez ajouter des lignes à une commande après avoir émis un acompte, puis vous pouvez valider une autre facture acompte, mais vous ne pouvez pas supprimer une ligne d'une commande après avoir facturé un acompte pour la ligne.</span><span class="sxs-lookup"><span data-stu-id="243fc-106">You can add new lines to an order after issuing a prepayment, and then you can post another prepayment invoice, but you cannot delete a line from an order after a prepayment has been invoiced for the line.</span></span>  

## <a name="to-correct-a-prepayment"></a><span data-ttu-id="243fc-107">Pour corriger des acomptes</span><span class="sxs-lookup"><span data-stu-id="243fc-107">To correct a prepayment</span></span>
<span data-ttu-id="243fc-108">La procédure suivante explique comment émettre un avoir acompte pour annuler tous les acomptes facturés pour une commande vente.</span><span class="sxs-lookup"><span data-stu-id="243fc-108">The following procedure shows how to issue a prepayment credit memo to cancel all invoiced prepayments for a sales order.</span></span>  
1. <span data-ttu-id="243fc-109">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Commandes vente**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="243fc-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="243fc-110">Ouvrez la commande vente appropriée.</span><span class="sxs-lookup"><span data-stu-id="243fc-110">Open the relevant sales order.</span></span>
3. <span data-ttu-id="243fc-111">Choisissez l'action **Acompte**, puis l'action **Valider avoir acompte** ou **Valider et imprimer avoir acompte**.</span><span class="sxs-lookup"><span data-stu-id="243fc-111">Choose the **Prepayment** action, and then choose the **Post Prepayment Credit Memo** action or the **Post and Print Prepmt. Cr. Memo** action.</span></span>  
4. <span data-ttu-id="243fc-112">Sur la page **Avoir vente**, continuez à corriger les écritures appropriées, comme pour toute avoir vente.</span><span class="sxs-lookup"><span data-stu-id="243fc-112">On the **Sales Credit Memo** page, proceed to correct the relevant entries, as for any sales credit memo.</span></span> <span data-ttu-id="243fc-113">Pour plus d'informations, reportez-vous à [Traiter les retours ou annulations de ventes](sales-how-process-sales-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="243fc-113">For more information, see [Process Sales Returns or Cancellations](sales-how-process-sales-returns-cancellations.md).</span></span>     

    > [!NOTE]  
    > <span data-ttu-id="243fc-114">Pour réduire le montant dans le champ **Montant ligne**, vous devez commencer par augmenter le pourcentage d'acompte sur la ligne afin que la valeur du champ **Montant ligne acompte** ne soit pas réduite au point d'être inférieure à la valeur du champ **Fact. montant acompte**.</span><span class="sxs-lookup"><span data-stu-id="243fc-114">To Reduce the amount in the **Line Amount** field, you must first increase the prepayment percentage on the line so that the value in the **Prepmt. Line Amount** field is not decreased below the value in the **Prepmt. Amt. Inv.** field.</span></span>

5. <span data-ttu-id="243fc-115">Pour valider une facture acompte pour les nouvelles lignes dans l'avoir vente, sélectionnez l'action **Acompte**, puis l'action **Valider facture acompte** ou **Publier et imprimer facture acompte**.</span><span class="sxs-lookup"><span data-stu-id="243fc-115">To make a prepayment invoice for any new lines in the sales credit memo, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action or the **Post and Print Prepmt. Invoice** action.</span></span>  
6. <span data-ttu-id="243fc-116">Pour émettre une autre facture acompte, augmentez le montant d'acompte sur une ou plusieurs lignes, puis validez la facture acompte.</span><span class="sxs-lookup"><span data-stu-id="243fc-116">To issue an additional prepayment invoice, increase the prepayment amount on one or more lines and post the prepayment invoice.</span></span> <span data-ttu-id="243fc-117">Une nouvelle facture est créée pour la différence entre les montants d'acompte facturés et le nouveau montant d'acompte.</span><span class="sxs-lookup"><span data-stu-id="243fc-117">A new invoice will be created for the difference between the prepayment amounts invoiced and the new prepayment amounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="243fc-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="243fc-118">See Also</span></span>  
[<span data-ttu-id="243fc-119">Facturation d'acomptes</span><span class="sxs-lookup"><span data-stu-id="243fc-119">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="243fc-120">Procédure pas à pas : configuration et facturation d'acomptes</span><span class="sxs-lookup"><span data-stu-id="243fc-120">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="243fc-121">Finances</span><span class="sxs-lookup"><span data-stu-id="243fc-121">Finance</span></span>](finance.md)  
<span data-ttu-id="243fc-122">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="243fc-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
