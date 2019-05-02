---
title: "Procédure : Vente d'articles à assembler pour commande | Microsoft Docs"
description: Si l'article est paramétré pour l'assemblage pour commande, alors l'article ne devrait pas être en stock, et doit être assemblé spécifiquement à une commande vente. Lorsque vous entrez l'article dans une ligne commande vente, un ordre d'assemblage est automatiquement créé et lié à la commande vente.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 5540c45eefb1272c5dfa5c790586f6b33b4f4848
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "821220"
---
# <a name="sell-items-assembled-to-order"></a><span data-ttu-id="0c571-104">Vente d'articles à assembler pour commande</span><span class="sxs-lookup"><span data-stu-id="0c571-104">Sell Items Assembled to Order</span></span>
<span data-ttu-id="0c571-105">Si le champ **Stratégie d'assemblage** de la fiche article d'un élément d'assemblage est **Assembler pour commande**, alors l'article n'est pas supposé être en stock et doit être assemblé spécifiquement dans une commande vente.</span><span class="sxs-lookup"><span data-stu-id="0c571-105">If the **Assembly Policy** field on the item card of an assembly item is **Assemble-to-Order**, then the item is not expected to be in inventory, and it must be assembled specifically to a sales order.</span></span> <span data-ttu-id="0c571-106">Lorsque vous entrez l'article dans une ligne commande vente, un ordre d'assemblage est automatiquement créé et lié à la commande vente.</span><span class="sxs-lookup"><span data-stu-id="0c571-106">When you enter the item on a sales order line, then an assembly order is automatically created and linked to the sales order.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0c571-107">Si certains articles à assembler pour commande sont déjà en stock, vous pouvez déduire cette quantité de l'ordre d'assemblage et la réserver dans le stock.</span><span class="sxs-lookup"><span data-stu-id="0c571-107">If some assemble-to-order items are already in inventory, then you can deduct that quantity from the assembly order and reserve it from inventory.</span></span> <span data-ttu-id="0c571-108">Pour plus d’informations, voir [Vente d'articles en stock dans des flux à assembler pour commande](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).</span><span class="sxs-lookup"><span data-stu-id="0c571-108">For more information, see [Sell Inventory Items in Assemble-to-Order Flows](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).</span></span>  

<span data-ttu-id="0c571-109">Dans cette procédure, vous effectuez la vente d'un article que vous assemblez selon les spécifications qui sont demandées par le client.</span><span class="sxs-lookup"><span data-stu-id="0c571-109">In this procedure, you process the sale of an item that will be assembled according to specifications that are requested by the customer.</span></span> <span data-ttu-id="0c571-110">Les étapes consistent à initier la ligne commande vente, personnaliser l'élément d'assemblage en modifiant ses composants et ressources, vérifier la disponibilité pour établir une date de livraison et lancer la commande vente à assembler et livrer immédiatement.</span><span class="sxs-lookup"><span data-stu-id="0c571-110">The steps include initiating the sales order line, customizing the assembly item by editing its components and resources, checking availability to establish a delivery date, and releasing the sales order to be assembled and immediately shipped.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0c571-111">La procédure suivante n'inclut pas les étapes standard de commande vente avant l'étape où vous entrez l'article à assembler pour commande dans une ligne commande vente.</span><span class="sxs-lookup"><span data-stu-id="0c571-111">The following procedure does not include the standard sales order steps before the step where you enter the assemble-to-order item on a sales order line.</span></span>  

## <a name="to-sell-an-item-that-is-assembled-to-order"></a><span data-ttu-id="0c571-112">Vendre un article qui est assemblé pour commande</span><span class="sxs-lookup"><span data-stu-id="0c571-112">To sell an item that is assembled to order</span></span>  
1.  <span data-ttu-id="0c571-113">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Commandes vente**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="0c571-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="0c571-114">Créez une commande client.</span><span class="sxs-lookup"><span data-stu-id="0c571-114">Create a sales order.</span></span> <span data-ttu-id="0c571-115">Pour en savoir plus, voir [Vendre des produits](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="0c571-115">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>  
3.  <span data-ttu-id="0c571-116">Dans le champ **N°**,</span><span class="sxs-lookup"><span data-stu-id="0c571-116">In the **No.**</span></span> <span data-ttu-id="0c571-117">, entrez un article qui est configuré pour l'assemblage pour commande.</span><span class="sxs-lookup"><span data-stu-id="0c571-117">field, enter an item that is set up to be assembled to order.</span></span>  
4.  <span data-ttu-id="0c571-118">Dans le champ **Code magasin**, définissez le magasin à partir duquel l'article sera vendu.</span><span class="sxs-lookup"><span data-stu-id="0c571-118">In the **Location Code** field, define which location the item will be sold from.</span></span> <span data-ttu-id="0c571-119">Le processus d'assemblage a lieu dans ce magasin.</span><span class="sxs-lookup"><span data-stu-id="0c571-119">The assembly process will occur at that location.</span></span>  
5.  <span data-ttu-id="0c571-120">Dans le champ **Quantité**, entrez le nombre d'unités à vendre.</span><span class="sxs-lookup"><span data-stu-id="0c571-120">In the **Quantity** field, enter how many units to sell.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="0c571-121">Si un ou plusieurs composants de la quantité d'éléments d'assemblage demandée ne sont pas disponibles, une page détaillée d'avertissement de disponibilité s'ouvre.</span><span class="sxs-lookup"><span data-stu-id="0c571-121">If one or more components of the requested assembly item quantity are not available, then a detailed availability warning page opens.</span></span> <span data-ttu-id="0c571-122">Pour plus d'informations, voir Disponibilité assemblage.</span><span class="sxs-lookup"><span data-stu-id="0c571-122">For more information, see Assembly Availability.</span></span>  

    <span data-ttu-id="0c571-123">Un ordre d'assemblage est maintenant automatiquement créé et est lié à la ligne commande vente.</span><span class="sxs-lookup"><span data-stu-id="0c571-123">An assembly order is now automatically created and linked to the sales order line.</span></span> <span data-ttu-id="0c571-124">La date d'échéance de cet ordre d'assemblage est synchronisée avec la date d'expédition de la ligne commande vente.</span><span class="sxs-lookup"><span data-stu-id="0c571-124">The due date of this assembly order is synchronized with the shipment date of the sales order line.</span></span>  

    <span data-ttu-id="0c571-125">La quantité à vendre est copiée dans le champ **Quantité à assembler pour commande**, ce qui indique que d'après la configuration la quantité totale de la ligne vente doit être assemblée à la commande.</span><span class="sxs-lookup"><span data-stu-id="0c571-125">The quantity to sell is copied to the **Qty. to Assemble to Order** field, which indicates that the item setup expects the full quantity on the sales line to be assembled to the order.</span></span> <span data-ttu-id="0c571-126">Vous pouvez réduire la quantité à assembler pour commande, par exemple si vous savez que certains articles sont déjà disponibles.</span><span class="sxs-lookup"><span data-stu-id="0c571-126">You can decrease the quantity to assemble to order, such as if you know that some items are already available.</span></span> <span data-ttu-id="0c571-127">Pour plus d’informations, voir [Vente d'articles en stock dans des flux à assembler pour commande](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).</span><span class="sxs-lookup"><span data-stu-id="0c571-127">For more information, see [Sell Inventory Items in Assemble-to-Order Flows](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).</span></span>  

6.  <span data-ttu-id="0c571-128">Pour indiquer que le client souhaite un article supplémentaire dans un kit, sur le raccourci **Lignes**, sélectionnez l'action **Ligne**, sélectionnez l'action **Assembler pour commande**, puis sélectionnez l'action **Lignes d'assemblage pour commande** pour visualiser et modifier les composants d'assemblage standard.</span><span class="sxs-lookup"><span data-stu-id="0c571-128">To reflect that the customer wants an additional item in a kit, on the **Lines** FastTab, choose the **Line** action, choose the **Assemble to Order** action, and then choose the **Assemble-to-Order Lines** action to view and change the standard assembly components.</span></span> <span data-ttu-id="0c571-129">Sinon, choisissez le champ **Quantité à assembler pour commande**.</span><span class="sxs-lookup"><span data-stu-id="0c571-129">Alternatively, choose the **Qty. to Assemble to Order** field.</span></span>  
7.  <span data-ttu-id="0c571-130">Sur la page **Lignes d'assemblage pour commande**, créez une nouvelle ligne de type **Article** pour le contenu du kit supplémentaire demandé.</span><span class="sxs-lookup"><span data-stu-id="0c571-130">On the **Assemble-to-Order Lines** page, create a new line of type **Item** for the requested additional kit content.</span></span> <span data-ttu-id="0c571-131">La ligne représente un composant supplémentaire d'assemblage.</span><span class="sxs-lookup"><span data-stu-id="0c571-131">The line represents an additional assembly component.</span></span>  

    <span data-ttu-id="0c571-132">Vous pouvez également personnaliser la commande en augmentant la quantité d'un article standard dans le kit.</span><span class="sxs-lookup"><span data-stu-id="0c571-132">You could also customize the order by increasing the quantity of one standard item in the kit.</span></span> <span data-ttu-id="0c571-133">Vous pouvez effectuer cette opération en augmentant la valeur du champ **Quantité par** de la ligne d'ordre d'assemblage spécifique.</span><span class="sxs-lookup"><span data-stu-id="0c571-133">You can do this by increasing the value in the **Quantity Per** field on the specific assembly order line.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="0c571-134">La page **Lignes d'assemblage pour commande** contient seulement les champs de base qu'un vendeur est supposé utiliser pour personnaliser la liste de composants, ajouter des numéros de traçabilité ou pour résoudre des problèmes de disponibilité des composants.</span><span class="sxs-lookup"><span data-stu-id="0c571-134">The **Assemble-to-Order Lines** page only contains the basic fields that a salesperson is expected to use to customize the component list, add item tracking numbers, or to solve component availability issues.</span></span> <span data-ttu-id="0c571-135">Pour plus d'informations en matière d'ordre d'assemblage, telles que la date de début d'ordre d'assemblage, choisissez l'action **Afficher documents**.</span><span class="sxs-lookup"><span data-stu-id="0c571-135">To see more assembly order information, such as the assembly order starting date, choose the **Show Documents** action.</span></span> <span data-ttu-id="0c571-136">Ceci ouvre l'affichage complet de l'ordre d'assemblage lié à la ligne commande vente.</span><span class="sxs-lookup"><span data-stu-id="0c571-136">This opens a full view of the assembly order that is linked to the sales order line.</span></span> <span data-ttu-id="0c571-137">Vous ne pouvez pas modifier les contenus de la plupart des champs de l'en-tête d'ordre d'assemblage et vous ne pouvez pas valider les résultats d'assemblage parce que vous devez utiliser la validation d'expédition de la ligne commande vente.</span><span class="sxs-lookup"><span data-stu-id="0c571-137">You cannot change the contents of most fields on the assembly order header, and you cannot post assembly output from it because you must use shipment posting of the sales order line.</span></span>  
    >   
    >  <span data-ttu-id="0c571-138">Sur l'en-tête des ordres d'assemblage associé, seul le champ **Date début** peut être modifié pour permettre aux employés d'assemblage de spécifier une date antérieure à la date d'échéance lorsqu'ils commencent le processus.</span><span class="sxs-lookup"><span data-stu-id="0c571-138">On the header of linked assembly orders, only the **Starting Date** field can be changed to enable assembly workers to specify a date that is earlier than the due date when they will start the process.</span></span> <span data-ttu-id="0c571-139">Tous les champs des lignes de l'ordre d'assemblage associé peuvent être modifiés afin que les magasiniers puissent entrer les chiffres de consommation pendant le processus.</span><span class="sxs-lookup"><span data-stu-id="0c571-139">All fields on the lines of the linked assembly order can be changed so that warehouse workers can enter consumption figures during the process.</span></span>  

8.  <span data-ttu-id="0c571-140">Examinez les problèmes de disponibilité des composants ou réagissez face à eux.</span><span class="sxs-lookup"><span data-stu-id="0c571-140">Review or react to component availability issues.</span></span> <span data-ttu-id="0c571-141">Par exemple, sélectionnez un article de substitution disponible ou définissez une date d'échéance ultérieure.</span><span class="sxs-lookup"><span data-stu-id="0c571-141">For example, select an available substitute item or establish a later due date.</span></span>  
9. <span data-ttu-id="0c571-142">Fermez la page **Lignes d'assemblage pour commande**.</span><span class="sxs-lookup"><span data-stu-id="0c571-142">Close the **Assemble-to-Order Lines** page.</span></span> <span data-ttu-id="0c571-143">L'ordre d'assemblage lié est maintenant prêt à commencer à assembler les articles personnalisés au plus tard à la date d'échéance.</span><span class="sxs-lookup"><span data-stu-id="0c571-143">The linked assembly order is now ready to start to assemble the customized items by the due date.</span></span>  
10. <span data-ttu-id="0c571-144">Sur la commande vente, choisissez l'action **Lancer** pour informer le département d’assemblage que le processus d’assemblage peut démarrer.</span><span class="sxs-lookup"><span data-stu-id="0c571-144">On the sales order, choose the **Release** action to notify the assembly department that the assembly process can start.</span></span>  
11. <span data-ttu-id="0c571-145">Dans le département d'assemblage, suivez la procédure d'assemblage des articles qui sont vendus au cours de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="0c571-145">In the assembly department, perform the steps of assembling the items that are sold in this procedure.</span></span> <span data-ttu-id="0c571-146">Pour plus d'informations, voir [Assembler des articles](assembly-how-to-assemble-items.md).</span><span class="sxs-lookup"><span data-stu-id="0c571-146">For more information, see [Assemble Items](assembly-how-to-assemble-items.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="0c571-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c571-147">See Also</span></span>  
[<span data-ttu-id="0c571-148">Gestion des assemblages</span><span class="sxs-lookup"><span data-stu-id="0c571-148">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="0c571-149">Utiliser les nomenclatures</span><span class="sxs-lookup"><span data-stu-id="0c571-149">Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)  
[<span data-ttu-id="0c571-150">STOCKS ET EN-COURS</span><span class="sxs-lookup"><span data-stu-id="0c571-150">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="0c571-151">Détails de conception : gestion d'entrepôt</span><span class="sxs-lookup"><span data-stu-id="0c571-151">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="0c571-152">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0c571-152">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>