---
title: "À propos de la fonctionnalité Planification | Microsoft Docs"
description: "Le système de planification prend en compte toutes les données d'offre et de demande, ajuste les résultats et génère des suggestions pour l'équilibrage de l'offre en fonction de la demande."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0910760881decc98ba1bfa6e8753566316386b2c
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="about-planning-functionality"></a><span data-ttu-id="ca959-103">À propos de la fonctionnalité Planification</span><span class="sxs-lookup"><span data-stu-id="ca959-103">About Planning Functionality</span></span>
<span data-ttu-id="ca959-104">Le système de planification prend en compte toutes les données d'offre et de demande, ajuste les résultats et génère des suggestions pour l'équilibrage de l'offre en fonction de la demande.</span><span class="sxs-lookup"><span data-stu-id="ca959-104">The planning system takes all demand and supply data into account, nets the results, and creates suggestions for balancing the supply to meet the demand.</span></span>  

<span data-ttu-id="ca959-105">Pour plus d'informations, voir [Détails de conception : planification de l'approvisionnement](design-details-supply-planning.md).</span><span class="sxs-lookup"><span data-stu-id="ca959-105">For detailed information, see [Design Details: Supply Planning](design-details-supply-planning.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="ca959-106">Pour tous les champs mentionnés dans cette rubrique, lisez l'info-bulles pour comprendre leur fonction.</span><span class="sxs-lookup"><span data-stu-id="ca959-106">For all the fields that are mentioned in this topic, read the tooltip to understand their function.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="demand-and-supply"></a><span data-ttu-id="ca959-107">Offre et demande</span><span class="sxs-lookup"><span data-stu-id="ca959-107">Demand and Supply</span></span>  
<span data-ttu-id="ca959-108">La planification comporte deux volets : l'offre et la demande.</span><span class="sxs-lookup"><span data-stu-id="ca959-108">Planning has two elements: demand and supply.</span></span> <span data-ttu-id="ca959-109">Ces derniers doivent être équilibrés pour garantir que la demande soit satisfaite rapidement et efficacement.</span><span class="sxs-lookup"><span data-stu-id="ca959-109">These must be held in balance to ensure that the demand is met in a timely and cost-efficient manner.</span></span>  

- <span data-ttu-id="ca959-110">Le mot demande désigne tout sorte de besoin brut, tel qu'une commande vente, une commande service, un besoin composant d'un ordre d'assemblage ou de fabrication, un désenlogement transfert, une commande ouverte ou une prévision.</span><span class="sxs-lookup"><span data-stu-id="ca959-110">Demand is the common term used for any kind of gross requirement such as a sales order, service order, component need from assembly or production orders, outbound transfer, blanket order or forecast.</span></span> <span data-ttu-id="ca959-111">En outre, le programme autorise d'autres types techniques de demande - tels qu'un ordre de fabrication ou une commande achat négatif, un stock négatif et un retour achat.</span><span class="sxs-lookup"><span data-stu-id="ca959-111">In addition to these, the program allows some other technical types of demand - such as a negative production or purchase order, negative inventory, and purchase return.</span></span>  
- <span data-ttu-id="ca959-112">Le mot offre désigne toute sorte de réapprovisionnement telle qu'un stock, une commande achat, un ordre d'assemblage, un ordre de fabrication ou un enlogement transfert.</span><span class="sxs-lookup"><span data-stu-id="ca959-112">Supply is the common word used for any kind of replenishment such as inventory, a purchase order, assembly order, production order, or inbound transfer.</span></span> <span data-ttu-id="ca959-113">Par conséquent, il peut y avoir une commande vente ou une commande service négative, un besoin de composant ou un retour vente négatif – tous représentant aussi l'offre d'une certaine façon.</span><span class="sxs-lookup"><span data-stu-id="ca959-113">Correspondingly, there can be a negative sales or service order, negative component need or sales return – all of which in some way also represent supply.</span></span>  

<span data-ttu-id="ca959-114">Un autre objectif du système de planification est de garantir que le stock ne croisse pas inutilement.</span><span class="sxs-lookup"><span data-stu-id="ca959-114">Another goal of the planning system is to ensure that the inventory does not grow unnecessarily.</span></span> <span data-ttu-id="ca959-115">En cas de baisse de la demande, le système de planification suggère de reporter, de réduire ou d'annuler des ordres de réapprovisionnement existants.</span><span class="sxs-lookup"><span data-stu-id="ca959-115">In the case of decreasing demand, the planning system will suggest that you postpone, decrease in quantity, or cancel existing replenishment orders.</span></span>  

## <a name="planning-calculation"></a><span data-ttu-id="ca959-116">Calcul de planification</span><span class="sxs-lookup"><span data-stu-id="ca959-116">Planning Calculation</span></span>  
<span data-ttu-id="ca959-117">Le système de planification est guidé par la demande prévue et réelle des clients ainsi que par les paramètres de réapprovisionnement de stock.</span><span class="sxs-lookup"><span data-stu-id="ca959-117">The planning system is driven by anticipated and actual customer demand, as well as inventory reordering parameters.</span></span> <span data-ttu-id="ca959-118">L'exécution du calcul de planification a pour effet que le programme suggère des mesures spécifiques (messages d'action) à prendre concernant le réapprovisionnement possible auprès de fournisseurs, les transferts entre entrepôts ou la production.</span><span class="sxs-lookup"><span data-stu-id="ca959-118">Running the planning calculation will result in the program suggesting specific actions (Action Messages) to take concerning possible replenishment from vendors, transfers between warehouses, or production.</span></span> <span data-ttu-id="ca959-119">S'il y a déjà des ordres de réapprovisionnement, les mesures suggérées peuvent être d'augmenter ou d'accélérer les commandes pour répondre à l'évolution de la demande.</span><span class="sxs-lookup"><span data-stu-id="ca959-119">If replenishment orders already exist, the suggested actions could be to increase or expedite the orders to meet the changes in demand.</span></span>  

<span data-ttu-id="ca959-120">La base de la routine de planification réside dans le calcul gros/net.</span><span class="sxs-lookup"><span data-stu-id="ca959-120">The basis of the planning routine is in the gross-to-net calculation.</span></span> <span data-ttu-id="ca959-121">Les besoins nets déterminent les lancements de commandes planifiées, qui sont programmés sur la base des informations de gamme (articles fabriqués) ou du délai de réapprovisionnement de la fiche article (articles achetés).</span><span class="sxs-lookup"><span data-stu-id="ca959-121">Net requirements drive planned order releases, which are scheduled based on the routing information (manufactured items) or the item card lead time (purchased items).</span></span> <span data-ttu-id="ca959-122">Les quantités de lancement de commandes planifiées sont basées sur le calcul de planification et affectées par les paramètres définis sur les fiches article individuelles.</span><span class="sxs-lookup"><span data-stu-id="ca959-122">Planned order release quantities are based on the planning calculation, and are affected by the parameters set on the individual item cards.</span></span>  

## <a name="planning-with-manual-transfer-orders"></a><span data-ttu-id="ca959-123">Planification à l'aide d'ordres de transfert manuels</span><span class="sxs-lookup"><span data-stu-id="ca959-123">Planning with Manual Transfer Orders</span></span>
<span data-ttu-id="ca959-124">Comme l'indique le champ **Système réappro** d'une fiche point de stock, le système de planification peut être configuré pour créer des ordres de transfert destinés à équilibrer l'offre et la demande dans tous les magasins.</span><span class="sxs-lookup"><span data-stu-id="ca959-124">As you can see from the **Replenishment System** field on a SKU card, the planning system can be set up to create transfer orders to balance supply and demand across locations.</span></span>  

<span data-ttu-id="ca959-125">Outre ce type d'ordre de transfert automatique, vous devrez parfois effectuer un mouvement général des quantités en stock vers un autre magasin, quelle que soit la demande existante.</span><span class="sxs-lookup"><span data-stu-id="ca959-125">In addition to such automatic transfer orders, you may sometimes need to perform a general move of inventory quantities to another location, irrespective of existing demand.</span></span> <span data-ttu-id="ca959-126">Vous créez pour cela un ordre de transfert manuel correspondant à la quantité à déplacer.</span><span class="sxs-lookup"><span data-stu-id="ca959-126">For this purpose you would manually create a transfer order for the quantity to move.</span></span> <span data-ttu-id="ca959-127">Pour être sûr que le système de planification ne tente pas de manipuler cet ordre de transfert manuel, vous devez paramétrer le champ **Flexibilité planification** des lignes transfert sur Aucune.</span><span class="sxs-lookup"><span data-stu-id="ca959-127">To ensure that the planning system does not try to manipulate this manual transfer order, you must set the **Planning Flexibility** on the transfer line(s) to None.</span></span>  

<span data-ttu-id="ca959-128">À l'inverse, si vous souhaitez que le système de planification ajuste les quantités de l'ordre de transfert et les dates en fonction de la demande existante, vous devez paramétrer le champ **Flexibilité planification** sur la valeur Illimitée.</span><span class="sxs-lookup"><span data-stu-id="ca959-128">Contrarily, if you do want the planning system to adjust the transfer order quantities and dates to existing demand, you must set the **Planning Flexibility** field to the default value, Unlimited.</span></span>

## <a name="planning-parameters"></a><span data-ttu-id="ca959-129">Paramètres de planification</span><span class="sxs-lookup"><span data-stu-id="ca959-129">Planning Parameters</span></span>  
<span data-ttu-id="ca959-130">Le paramètres de planification déterminent le moment, la quantité et la méthode de réapprovisionnement en fonction des divers paramètres de la fiche article (ou point de stock - SKU) et des paramètres de production.</span><span class="sxs-lookup"><span data-stu-id="ca959-130">The planning parameters control when, how much, and how to replenish based on the various settings on the item card (or stockkeeping unit - SKU), and the manufacturing setup.</span></span>  

<span data-ttu-id="ca959-131">Les paramètres de planification suivants existent pour l'article ou la fiche point de stock :</span><span class="sxs-lookup"><span data-stu-id="ca959-131">The following planning parameters exist on the item or SKU card:</span></span>  

-   <span data-ttu-id="ca959-132">Période tampon</span><span class="sxs-lookup"><span data-stu-id="ca959-132">Dampener Period</span></span>  
-   <span data-ttu-id="ca959-133">Quantité tampon</span><span class="sxs-lookup"><span data-stu-id="ca959-133">Dampener Quantity</span></span>  
-   <span data-ttu-id="ca959-134">Méthode réapprovisionnement</span><span class="sxs-lookup"><span data-stu-id="ca959-134">Reordering Policy</span></span>  
-   <span data-ttu-id="ca959-135">Point de commande</span><span class="sxs-lookup"><span data-stu-id="ca959-135">Reorder Point</span></span>
-   <span data-ttu-id="ca959-136">Stock maximum</span><span class="sxs-lookup"><span data-stu-id="ca959-136">Maximum Inventory</span></span>  
-   <span data-ttu-id="ca959-137">Niveau de dépassement de capacité</span><span class="sxs-lookup"><span data-stu-id="ca959-137">Overflow Level</span></span>  
-   <span data-ttu-id="ca959-138">Intervalle de planification</span><span class="sxs-lookup"><span data-stu-id="ca959-138">Time Bucket</span></span>  
-   <span data-ttu-id="ca959-139">Période de groupement de lots</span><span class="sxs-lookup"><span data-stu-id="ca959-139">Lot Accumulation Period</span></span>  
-   <span data-ttu-id="ca959-140">Période de replanification</span><span class="sxs-lookup"><span data-stu-id="ca959-140">Rescheduling Period</span></span>  
-   <span data-ttu-id="ca959-141">Quantité de réappro.</span><span class="sxs-lookup"><span data-stu-id="ca959-141">Reorder Quantity</span></span>  
-   <span data-ttu-id="ca959-142">Délai de sécurité</span><span class="sxs-lookup"><span data-stu-id="ca959-142">Safety Lead Time</span></span>  
-   <span data-ttu-id="ca959-143">Stock de sécurité</span><span class="sxs-lookup"><span data-stu-id="ca959-143">Safety Stock Quantity</span></span>  
-   <span data-ttu-id="ca959-144">Stratégie d'assemblage</span><span class="sxs-lookup"><span data-stu-id="ca959-144">Assembly Policy</span></span>  
-   <span data-ttu-id="ca959-145">Mode de lancement</span><span class="sxs-lookup"><span data-stu-id="ca959-145">Manufacturing Policy</span></span>  

<span data-ttu-id="ca959-146">Les les modificateurs d'ordre suivants existent pour l'article ou la fiche point de stock :</span><span class="sxs-lookup"><span data-stu-id="ca959-146">The following order modifiers exist on the item or SKU card:</span></span>  

-   <span data-ttu-id="ca959-147">Qté minimum commande</span><span class="sxs-lookup"><span data-stu-id="ca959-147">Minimum Order Quantity</span></span>  
-   <span data-ttu-id="ca959-148">Qté maximum commande</span><span class="sxs-lookup"><span data-stu-id="ca959-148">Maximum Order Quantity</span></span>  
-   <span data-ttu-id="ca959-149">Commandé par</span><span class="sxs-lookup"><span data-stu-id="ca959-149">Order Multiple</span></span>  

<span data-ttu-id="ca959-150">Les champs de paramètres de planning figurant dans la fenêtre **Paramètres production** sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="ca959-150">Global planning setup fields on the **Manufacturing Setup** window include:</span></span>  

-   <span data-ttu-id="ca959-151">Code plus bas niv. dyn.</span><span class="sxs-lookup"><span data-stu-id="ca959-151">Dynamic Low-Level Code]</span></span>  
-   <span data-ttu-id="ca959-152">Prévision courante</span><span class="sxs-lookup"><span data-stu-id="ca959-152">Current Production Forecast</span></span>  
-   <span data-ttu-id="ca959-153">Prévision sur magasin</span><span class="sxs-lookup"><span data-stu-id="ca959-153">Use Forecast on Locations</span></span>  
-   <span data-ttu-id="ca959-154">Délai de sécurité par défaut</span><span class="sxs-lookup"><span data-stu-id="ca959-154">Default Safety Lead Time</span></span>  
-   <span data-ttu-id="ca959-155">Niveau de dépassement de capacité vide</span><span class="sxs-lookup"><span data-stu-id="ca959-155">Blank Overflow Level</span></span>  
-   <span data-ttu-id="ca959-156">Calcul PDP/MRP combiné</span><span class="sxs-lookup"><span data-stu-id="ca959-156">Combined MPS/MRP Calculation</span></span>   
-   <span data-ttu-id="ca959-157">Mag. composant par déf.</span><span class="sxs-lookup"><span data-stu-id="ca959-157">Components at Location</span></span>  
-   <span data-ttu-id="ca959-158">Période tampon par défaut</span><span class="sxs-lookup"><span data-stu-id="ca959-158">Default Dampener Period</span></span>  
-   <span data-ttu-id="ca959-159">Quantité tampon par défaut</span><span class="sxs-lookup"><span data-stu-id="ca959-159">Default Dampener Quantity</span></span>  

<span data-ttu-id="ca959-160">Pour plus d'informations, voir [Détails de conception : paramètres de planification](design-details-planning-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="ca959-160">For more information, see [Design Details: Planning Parameters](design-details-planning-parameters.md)</span></span>  

## <a name="other-important-planning-fields"></a><span data-ttu-id="ca959-161">Autres champs de planification importants</span><span class="sxs-lookup"><span data-stu-id="ca959-161">Other Important Planning Fields</span></span>
### <a name="planning-flexibility"></a><span data-ttu-id="ca959-162">Flexibilité planification</span><span class="sxs-lookup"><span data-stu-id="ca959-162">Planning Flexibility</span></span>
<span data-ttu-id="ca959-163">Dans la plupart des commandes approvisionnement, comme les ordres de fabrication, vous pouvez sélectionner **Illimité** ou **Aucun** dans le champ **Flexibilité planification** des lignes.</span><span class="sxs-lookup"><span data-stu-id="ca959-163">On most supply orders, such as production orders, you can select **Unlimited** or **None** in the **Planning Flexibility** field on the lines.</span></span>

<span data-ttu-id="ca959-164">Cela spécifie si l'approvisionnement représenté par la ligne O.F. est pris en compte par le système de planification lors du calcul des messages d'action.</span><span class="sxs-lookup"><span data-stu-id="ca959-164">This specifies whether the supply represented by the production order line is considered by the planning system when calculating action messages.</span></span>
<span data-ttu-id="ca959-165">Si le champ affiche l'option **Illimitée**, le système de planification inclut la ligne lors du calcul des messages d'action.</span><span class="sxs-lookup"><span data-stu-id="ca959-165">If the field contains **Unlimited**, then the planning system includes the line when calculating action messages.</span></span> <span data-ttu-id="ca959-166">S'il est paramétré sur **Aucune**, la ligne est ferme et définitive, et le système de planification n'inclut pas la ligne dans le calcul des messages d'action.</span><span class="sxs-lookup"><span data-stu-id="ca959-166">If the field contains **None**, then the line is firm and unchangeable, and the planning system does not include the line when calculating action messages.</span></span>

### <a name="warning"></a><span data-ttu-id="ca959-167">Alerte</span><span class="sxs-lookup"><span data-stu-id="ca959-167">Warning</span></span>
<span data-ttu-id="ca959-168">Le champ d'informations **Alerte** dans la fenêtre **Feuille planning** vous informe lorsqu'une ligne planning est créée pour une situation inhabituelle avec un texte. L'utilisateur peut cliquer sur ce texte pour lire des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="ca959-168">The **Warning** information field in the **Planning Worksheet** window informs you of any planning line created for an unusual situation with a text, which the user can choose to read additional information.</span></span> <span data-ttu-id="ca959-169">Les types d'alerte suivants existent :</span><span class="sxs-lookup"><span data-stu-id="ca959-169">The following warning types exist:</span></span>

- <span data-ttu-id="ca959-170">Urgence</span><span class="sxs-lookup"><span data-stu-id="ca959-170">Emergency</span></span>
- <span data-ttu-id="ca959-171">Exception</span><span class="sxs-lookup"><span data-stu-id="ca959-171">Exception</span></span>
- <span data-ttu-id="ca959-172">Attention</span><span class="sxs-lookup"><span data-stu-id="ca959-172">Attention</span></span>
- <span data-ttu-id="ca959-173">Urgence</span><span class="sxs-lookup"><span data-stu-id="ca959-173">Emergency</span></span>

<span data-ttu-id="ca959-174">L'avertissement Urgence est affiché dans deux situations :</span><span class="sxs-lookup"><span data-stu-id="ca959-174">The emergency warning is displayed in two situations:</span></span>

- <span data-ttu-id="ca959-175">Le stock est négatif à la date de début de la planification.</span><span class="sxs-lookup"><span data-stu-id="ca959-175">The inventory is negative on the planning starting date.</span></span>
- <span data-ttu-id="ca959-176">Des événements d'offre ou de demande rétroactifs existent.</span><span class="sxs-lookup"><span data-stu-id="ca959-176">Back-dated supply or demand events exist.</span></span>

<span data-ttu-id="ca959-177">Si le stock d'un article est négatif à la date de début de la planification, le système de planification suggère une commande approvisionnement d'urgence afin que la quantité négative arrive à la date de début de la planification.</span><span class="sxs-lookup"><span data-stu-id="ca959-177">If an item’s inventory is negative on the planning starting date, the planning system suggests an emergency supply order for the negative quantity to arrive on the planning starting date.</span></span> <span data-ttu-id="ca959-178">Le texte d'avertissement indique la date de début et la quantité de la commande d'urgence.</span><span class="sxs-lookup"><span data-stu-id="ca959-178">The warning text states the starting date and the quantity of the emergency order.</span></span>

<span data-ttu-id="ca959-179">Les lignes document avec une date d'échéance antérieure à la date de début de la planification sont consolidées dans une commande approvisionnement d'urgence pour que l'article arrive à la date de début de la planification.</span><span class="sxs-lookup"><span data-stu-id="ca959-179">Any document lines with due dates before the planning starting date are consolidated into one emergency supply order for the item to arrive on the planning starting date.</span></span>

### <a name="exception"></a><span data-ttu-id="ca959-180">Exception</span><span class="sxs-lookup"><span data-stu-id="ca959-180">Exception</span></span>
<span data-ttu-id="ca959-181">L'avertissement Exception s'affiche si le stock disponible prévu descend en dessous du stock de sécurité.</span><span class="sxs-lookup"><span data-stu-id="ca959-181">The exception warning is displayed if the projected available inventory drops below the safety stock quantity.</span></span>

<span data-ttu-id="ca959-182">Le système de planification suggère une commande approvisionnement pour répondre aux besoins à la date d'échéance.</span><span class="sxs-lookup"><span data-stu-id="ca959-182">The planning system will suggest a supply order to meet the demand on its due date.</span></span> <span data-ttu-id="ca959-183">Le texte d'avertissement indique la quantité du stock de sécurité et la date à laquelle elle est entamée.</span><span class="sxs-lookup"><span data-stu-id="ca959-183">The warning text states the item’s safety stock quantity and the date on which it is violated.</span></span>

<span data-ttu-id="ca959-184">Entamer le stock de sécurité est considéré comme une exception car cela ne doit pas se produire si le point de commande a été correctement défini.</span><span class="sxs-lookup"><span data-stu-id="ca959-184">Violating the safety stock level is considered an exception because it should not occur if the reorder point has been set correctly.</span></span>

> [!NOTE]
> <span data-ttu-id="ca959-185">L'approvisionnement pour les lignes planning avec les alertes Exception n'est normalement pas modifié en fonction des paramètres de planification.</span><span class="sxs-lookup"><span data-stu-id="ca959-185">Supply on planning lines with Exception warnings is normally not modified according to planning parameters.</span></span> <span data-ttu-id="ca959-186">Au lieu de cela, le système de planification propose uniquement un approvisionnement pour couvrir la quantité de demande exacte.</span><span class="sxs-lookup"><span data-stu-id="ca959-186">Instead, the planning system only suggests a supply to cover the exact demand quantity.</span></span> <span data-ttu-id="ca959-187">Cependant, vous pouvez définir l'exécution de la planification pour respecter certains paramètres de planification pour les lignes planning à respecter avec certaines alertes.</span><span class="sxs-lookup"><span data-stu-id="ca959-187">However, you can set the planning run up to respect certain planning parameters for planning lines with certain warnings.</span></span> <span data-ttu-id="ca959-188">Pour plus d'informations, voir « Respecter les paramètres de planning pour les avertissements d'exception » dans Calc. planning - F.</span><span class="sxs-lookup"><span data-stu-id="ca959-188">For more information, see “Respect Planning Parameters for Exception Warnings” in Calculate Plan - Plan.</span></span> <span data-ttu-id="ca959-189">planning.</span><span class="sxs-lookup"><span data-stu-id="ca959-189">Wksh.</span></span>

### <a name="attention"></a><span data-ttu-id="ca959-190">Attention</span><span class="sxs-lookup"><span data-stu-id="ca959-190">Attention</span></span>
<span data-ttu-id="ca959-191">L'avertissement Attention est affiché dans deux situations :</span><span class="sxs-lookup"><span data-stu-id="ca959-191">The attention warning is displayed in two situations:</span></span>

- <span data-ttu-id="ca959-192">La date de début de la planification est antérieure à la date de travail.</span><span class="sxs-lookup"><span data-stu-id="ca959-192">The planning starting date is earlier than the work date.</span></span>
- <span data-ttu-id="ca959-193">La ligne planification suggère de changer une commande achat lancée ou un O.F.</span><span class="sxs-lookup"><span data-stu-id="ca959-193">The planning line suggests to change a released purchase or production order.</span></span>

> [!NOTE]
> <span data-ttu-id="ca959-194">Dans les lignes planning comportant des avertissements, le champ **Accepter message d'action** n'est pas sélectionné, car le gestionnaire doit poursuivre l'étude de ces lignes avant de mettre en application ce plan.</span><span class="sxs-lookup"><span data-stu-id="ca959-194">In planning lines with warnings, the **Accept Action Message** field is not selected, because the planner is expected to further investigate these lines before carrying out the plan.</span></span>

## <a name="see-also"></a><span data-ttu-id="ca959-195">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca959-195">See Also</span></span>  
[<span data-ttu-id="ca959-196">Détails de conception : planification de l'approvisionnement</span><span class="sxs-lookup"><span data-stu-id="ca959-196">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)  
<span data-ttu-id="ca959-197">[Planifié](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="ca959-197">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="ca959-198">Paramétrage de la production</span><span class="sxs-lookup"><span data-stu-id="ca959-198">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="ca959-199">[Production](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="ca959-199">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="ca959-200">STOCKS ET EN-COURS</span><span class="sxs-lookup"><span data-stu-id="ca959-200">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="ca959-201">Achats</span><span class="sxs-lookup"><span data-stu-id="ca959-201">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="ca959-202">Pratiques de configuration recommandées : planification de l'approvisionnement</span><span class="sxs-lookup"><span data-stu-id="ca959-202">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="ca959-203">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ca959-203">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

