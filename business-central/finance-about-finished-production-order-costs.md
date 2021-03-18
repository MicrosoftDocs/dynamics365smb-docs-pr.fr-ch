---
title: À propos des coûts des O.F. terminés | Microsoft Docs
description: L’achèvement de l’ordre de fabrication est une tâche importante de l’évaluation du cycle de vie de l’article en cours de production. Les coûts finaux, notamment les écarts dans un environnement de coût standard, les valeurs réelles dans un environnement de coût FIFO, moyen ou LIFO, sont calculés à l’aide du traitement par lots Ajuster coûts - Écr. article.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e1116d99a2893c3fef8fd2306b79cb2252c04d77
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389439"
---
# <a name="about-finished-production-order-costs"></a><span data-ttu-id="46bcb-104">À propos des coûts des O.F. terminés</span><span class="sxs-lookup"><span data-stu-id="46bcb-104">About Finished Production Order Costs</span></span>
<span data-ttu-id="46bcb-105">L’achèvement de l’ordre de fabrication est une tâche importante de l’évaluation du cycle de vie de l’article en cours de production.</span><span class="sxs-lookup"><span data-stu-id="46bcb-105">Finishing the production order is an important task in completing the costing lifecycle of the item that is being produced.</span></span> <span data-ttu-id="46bcb-106">Les coûts finaux, notamment les écarts dans un environnement de coût standard, valeurs réelles dans un environnement de coût FIFO, moyen ou LIFO, sont calculés à l’aide du traitement par lots **Ajuster coûts - Écr. article** qui permet d’opérer un rapprochement bancaire des coûts de production d’un article.</span><span class="sxs-lookup"><span data-stu-id="46bcb-106">Final costs, including variances in a standard cost environment, actuals in a FIFO, Average, or LIFO cost environment, are calculated using the **Adjust Cost - Item Entries** batch job, which allows for financial reconciliation of the costs of item production.</span></span> <span data-ttu-id="46bcb-107">Pour qu’un ordre de fabrication soit pris en considération pour un ajustement de coût, son statut doit être **Produit fini**.</span><span class="sxs-lookup"><span data-stu-id="46bcb-107">For a production order to be considered for cost adjustment, the status must be **Finished**.</span></span> <span data-ttu-id="46bcb-108">Il est donc essentiel qu’au moment de son achèvement, le statut d’un ordre de fabrication soit modifié en **Produit fini**.</span><span class="sxs-lookup"><span data-stu-id="46bcb-108">It is therefore critical that upon completion, the status of a production order is changed to **Finished**.</span></span>  

## <a name="example"></a><span data-ttu-id="46bcb-109">Exemple :</span><span class="sxs-lookup"><span data-stu-id="46bcb-109">Example</span></span>  
 <span data-ttu-id="46bcb-110">Dans un environnement de coût standard, lorsque vous consommez des matières pour produire un article, le coût de l’article, celui de la main-d’œuvre et celui des frais généraux sont répertoriés dans le TEC, pour définir simplement les choses.</span><span class="sxs-lookup"><span data-stu-id="46bcb-110">In a standard cost environment, when you consume material to produce an item, stated simply, the cost of the item plus labor and overhead go into WIP.</span></span> <span data-ttu-id="46bcb-111">Lorsque l’article est produit, son coût standard est retranché du TEC.</span><span class="sxs-lookup"><span data-stu-id="46bcb-111">When the item is produced, WIP is reduced by the amount of the standard cost of the item.</span></span> <span data-ttu-id="46bcb-112">Généralement, le résultat de l’opération n’est pas égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="46bcb-112">Typically, these costs do not net to zero.</span></span> <span data-ttu-id="46bcb-113">Pour que le résultat obtenu soit égal à zéro, vous devez exécuter le traitement par lots **Ajuster coûts - Écr. article** en sachant que seuls les ordres de fabrication dont l’état est **Produit fini** seront pris en considération pour l’ajustement.</span><span class="sxs-lookup"><span data-stu-id="46bcb-113">So that these costs can net to zero, you must run the **Adjust Cost - Item Entries** batch job, noting that only production orders with the status of **Finished** will be considered for adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="46bcb-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46bcb-114">See Also</span></span>  
[<span data-ttu-id="46bcb-115">Gestion des coûts ajustés</span><span class="sxs-lookup"><span data-stu-id="46bcb-115">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="46bcb-116">Production</span><span class="sxs-lookup"><span data-stu-id="46bcb-116">Manufacturing</span></span>](production-manage-manufacturing.md)  
<span data-ttu-id="46bcb-117">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="46bcb-117">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]