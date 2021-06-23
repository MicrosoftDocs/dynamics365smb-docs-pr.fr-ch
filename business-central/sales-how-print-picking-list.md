---
title: Imprimer la liste des prélèvements de stock d’une commande vente
description: Vous pouvez imprimer une liste des prélèvements des stocks directement à partir d'une commande client, des ventes, de la facture et d'autres documents de vente sortants.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4cddce48df3be0a3fadaa74ed751b274ccce7f31
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115476"
---
# <a name="print-the-picking-list"></a><span data-ttu-id="94af1-103">Imprimer la liste des prélèvements</span><span class="sxs-lookup"><span data-stu-id="94af1-103">Print the Picking List</span></span>

<span data-ttu-id="94af1-104">Vous pouvez imprimer une liste des prélèvements de stock directement à partir d’une commande client ou d’autres documents qui déclenchent l’expédition des articles.</span><span class="sxs-lookup"><span data-stu-id="94af1-104">You can print an inventory picking list directly from a sales order and other documents that initiate the shipment of items.</span></span>

<span data-ttu-id="94af1-105">Ce rapport est généralement utilisé dans les entreprises sans fonctionnalité dédiée à la gestion des entrepôts, de sorte qu'un stock peut simplement afficher ou imprimer la liste des prélèvements à partir du document de vente associé.</span><span class="sxs-lookup"><span data-stu-id="94af1-105">This report is typically used in companies without dedicated functionality for warehouse management, so that an inventory worker can simply view or print the picking list from the related sales document.</span></span> <span data-ttu-id="94af1-106">Dans les entreprises avec un volume plus élevé ou des processus plus complexes, le prélèvement est planifié et effectué dans des documents d'entrepôt dédiés.</span><span class="sxs-lookup"><span data-stu-id="94af1-106">In companies with higher volume or more complex processes, picking is planned and performed in dedicated warehouse documents.</span></span> <span data-ttu-id="94af1-107">Pour plus d'informations, voir [Prélèvement d'articles](warehouse-pick-items.md).</span><span class="sxs-lookup"><span data-stu-id="94af1-107">For more information, see [Pick Items](warehouse-pick-items.md).</span></span>

## <a name="to-print-a-picking-list-from-a-sales-order"></a><span data-ttu-id="94af1-108">Pour imprimer la liste des prélèvements à partir d'une commande vente</span><span class="sxs-lookup"><span data-stu-id="94af1-108">To print a picking list from a sales order</span></span>

<span data-ttu-id="94af1-109">La procédure suivante se base sur une commande vente.</span><span class="sxs-lookup"><span data-stu-id="94af1-109">The following procedure is based on a sales order.</span></span> <span data-ttu-id="94af1-110">Les étapes sont similaires pour tous les autres documents pouvant être utilisés pour lancer l’expédition d’articles, par exemple un ordre transfert.</span><span class="sxs-lookup"><span data-stu-id="94af1-110">The steps are similar for all other documents that can be used to initiate shipment of items, such as a transfer order.</span></span>

1. <span data-ttu-id="94af1-111">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), saisissez **Commandes vente**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="94af1-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="94af1-112">Ouvrez une commande vente pour laquelle vous souhaitez sélectionner des articles.</span><span class="sxs-lookup"><span data-stu-id="94af1-112">Open the sales order that you want to pick items for.</span></span>  
3. <span data-ttu-id="94af1-113">Choisir l'action **Rapport**, puis choisissez l'action **Liste de prélèvement par ordre**.</span><span class="sxs-lookup"><span data-stu-id="94af1-113">Choose the **Report** action, and then choose the **Picking List by Order** action.</span></span>  
4. <span data-ttu-id="94af1-114">Sélectionnez le bouton **Imprimer** pour imprimer la liste de prélèvements, ou le bouton **Aperçu** pour l'afficher à l'écran.</span><span class="sxs-lookup"><span data-stu-id="94af1-114">Choose the **Print** button to print the picking list or choose the **Preview** button to view it on the screen.</span></span>

<span data-ttu-id="94af1-115">Vous pouvez également enregistrer la liste des prélèvements en tant que document, par exemple, pour l'envoyer à quelqu'un ou pour l'ajouter en tant que pièce jointe à la commande client.</span><span class="sxs-lookup"><span data-stu-id="94af1-115">You can also save the picking list as a document, for example, to send to someone or to add as an attachment to the sales order.</span></span> <span data-ttu-id="94af1-116">Pour plus d'informations, voir [Gérer les pièces jointes, les liens et les notes sur les fiches et les documents](ui-how-add-link-to-record.md).</span><span class="sxs-lookup"><span data-stu-id="94af1-116">For more information, see [Manage Attachments, Links, and Notes on Cards and Documents](ui-how-add-link-to-record.md).</span></span>

> [!NOTE]
> <span data-ttu-id="94af1-117">Si vous avez utilisé la fonction **Éclater nomenclature** sur la commande client, seuls les composants de l'élément d'assemblage associé sont affichés dans le rapport.</span><span class="sxs-lookup"><span data-stu-id="94af1-117">If you used the **Explode BOM** function on the sales order, then only the components of the related assembly item are shown in the report.</span></span> <span data-ttu-id="94af1-118">Pour plus d'informations, reportez-vous à [Utiliser les nomenclatures](inventory-how-work-BOMs.md).</span><span class="sxs-lookup"><span data-stu-id="94af1-118">For more information, see [Work with Bills of Material](inventory-how-work-BOMs.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="94af1-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94af1-119">See Also</span></span>

[<span data-ttu-id="94af1-120">Stock</span><span class="sxs-lookup"><span data-stu-id="94af1-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="94af1-121">Prélèvement d'articles</span><span class="sxs-lookup"><span data-stu-id="94af1-121">Pick Items</span></span>](warehouse-pick-items.md)  
<span data-ttu-id="94af1-122">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="94af1-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  

[!INCLUDE[footer-include](includes/footer-banner.md)]