---
title: 'Procédure : corriger des acomptes | Microsoft Docs'
description: Vous pouvez apporter une correction à une commande après avoir validé une facture acompte pour la commande. Vous pouvez ajouter des lignes à une commande après avoir émis un acompte, puis vous pouvez valider une autre facture acompte, mais vous ne pouvez pas supprimer une ligne d’une commande après avoir facturé un acompte pour la ligne.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1be1ba8d59567fdf9ba2adfeceeaa23c9cf63778
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750745"
---
# <a name="correct-prepayments"></a><span data-ttu-id="24f07-104">Corriger des acomptes</span><span class="sxs-lookup"><span data-stu-id="24f07-104">Correct Prepayments</span></span>

<span data-ttu-id="24f07-105">Vous pouvez apporter une correction à une commande après avoir validé une facture acompte pour la commande.</span><span class="sxs-lookup"><span data-stu-id="24f07-105">You can make a correction to an order after you have posted a prepayment invoice for the order.</span></span> <span data-ttu-id="24f07-106">Vous pouvez ajouter des lignes à une commande après avoir émis un acompte, puis vous pouvez valider une autre facture acompte, mais vous ne pouvez pas supprimer une ligne d’une commande après avoir facturé un acompte pour la ligne.</span><span class="sxs-lookup"><span data-stu-id="24f07-106">You can add new lines to an order after issuing a prepayment, and then you can post another prepayment invoice, but you cannot delete a line from an order after a prepayment has been invoiced for the line.</span></span>  

> [!TIP]
> <span data-ttu-id="24f07-107">Si vous avez enregistré une facture de prépaiement pour une facture vente que vous corrigez ou annulez ensuite, vous devez également corriger ou annuler le prépaiement.</span><span class="sxs-lookup"><span data-stu-id="24f07-107">If you have posted a prepayment invoice for a sales invoice that you then correct or cancel, you must correct or cancel the prepayment as well.</span></span>

## <a name="to-correct-a-prepayment"></a><span data-ttu-id="24f07-108">Pour corriger des acomptes</span><span class="sxs-lookup"><span data-stu-id="24f07-108">To correct a prepayment</span></span>

<span data-ttu-id="24f07-109">La procédure suivante explique comment émettre un avoir acompte pour annuler tous les acomptes facturés pour une commande vente.</span><span class="sxs-lookup"><span data-stu-id="24f07-109">The following procedure shows how to issue a prepayment credit memo to cancel all invoiced prepayments for a sales order.</span></span>  

1. <span data-ttu-id="24f07-110">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Commandes vente**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="24f07-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="24f07-111">Ouvrez la commande vente appropriée.</span><span class="sxs-lookup"><span data-stu-id="24f07-111">Open the relevant sales order.</span></span>
3. <span data-ttu-id="24f07-112">Choisissez l’action **Acompte**, puis l’action **Valider avoir acompte** ou **Valider et imprimer avoir acompte**.</span><span class="sxs-lookup"><span data-stu-id="24f07-112">Choose the **Prepayment** action, and then choose the **Post Prepayment Credit Memo** action or the **Post and Print Prepmt. Cr. Memo** action.</span></span>  
4. <span data-ttu-id="24f07-113">Sur la page **Avoir vente**, continuez à corriger les écritures appropriées, comme pour toute avoir vente.</span><span class="sxs-lookup"><span data-stu-id="24f07-113">On the **Sales Credit Memo** page, proceed to correct the relevant entries, as for any sales credit memo.</span></span> <span data-ttu-id="24f07-114">Pour plus d’informations, reportez-vous à [Traiter les retours ou annulations de ventes](sales-how-process-sales-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="24f07-114">For more information, see [Process Sales Returns or Cancellations](sales-how-process-sales-returns-cancellations.md).</span></span>  

    > [!NOTE]  
    > <span data-ttu-id="24f07-115">Pour réduire le montant dans le champ **Montant ligne**, vous devez commencer par augmenter le pourcentage d’acompte sur la ligne afin que la valeur du champ **Montant ligne acompte** ne soit pas réduite au point d’être inférieure à la valeur du champ **Fact. montant acompte**.</span><span class="sxs-lookup"><span data-stu-id="24f07-115">To reduce the amount in the **Line Amount** field, you must first increase the prepayment percentage on the line so that the value in the **Prepmt. Line Amount** field is not decreased below the value in the **Prepmt. Amt. Inv.** field.</span></span>

5. <span data-ttu-id="24f07-116">Pour valider une facture acompte pour les nouvelles lignes dans l’avoir vente, sélectionnez l’action **Acompte**, puis l’action **Valider facture acompte** ou **Publier et imprimer facture acompte**.</span><span class="sxs-lookup"><span data-stu-id="24f07-116">To make a prepayment invoice for any new lines in the sales credit memo, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action or the **Post and Print Prepmt. Invoice** action.</span></span>  
6. <span data-ttu-id="24f07-117">Pour émettre une autre facture acompte, augmentez le montant d’acompte sur une ou plusieurs lignes, puis validez la facture acompte.</span><span class="sxs-lookup"><span data-stu-id="24f07-117">To issue an additional prepayment invoice, increase the prepayment amount on one or more lines and post the prepayment invoice.</span></span> <span data-ttu-id="24f07-118">Une nouvelle facture est créée pour la différence entre les montants d’acompte facturés et le nouveau montant d’acompte.</span><span class="sxs-lookup"><span data-stu-id="24f07-118">A new invoice will be created for the difference between the prepayment amounts invoiced and the new prepayment amounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="24f07-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24f07-119">See Also</span></span>

[<span data-ttu-id="24f07-120">Facturation d’acomptes</span><span class="sxs-lookup"><span data-stu-id="24f07-120">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="24f07-121">Procédure pas à pas : configuration et facturation d’acomptes</span><span class="sxs-lookup"><span data-stu-id="24f07-121">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="24f07-122">Finances</span><span class="sxs-lookup"><span data-stu-id="24f07-122">Finance</span></span>](finance.md)  
<span data-ttu-id="24f07-123">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="24f07-123">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
