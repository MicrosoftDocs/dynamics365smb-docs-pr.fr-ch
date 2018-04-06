---
title: "Procédure de configuration des transporteurs | Microsoft Docs"
description: "Vous pouvez définir un code pour chacun de vos transporteurs et saisir les informations qui les concernent."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b6ab539048f3f802cc4575e023c43632025dccf5
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-shipping-agents"></a><span data-ttu-id="06856-103">Configurer des transporteurs</span><span class="sxs-lookup"><span data-stu-id="06856-103">Set Up Shipping Agents</span></span>
<span data-ttu-id="06856-104">Vous pouvez définir un code pour chacun de vos transporteurs et saisir les informations qui les concernent.</span><span class="sxs-lookup"><span data-stu-id="06856-104">You can set up a code for each of your shipping agents and enter information about them.</span></span>  

<span data-ttu-id="06856-105">Si vous saisissez une adresse Internet pour le transporteur, et que le transporteur fournit des prestations de traçabilité des colis sur Internet, vous pouvez utiliser la fonction de récépissé automatique.</span><span class="sxs-lookup"><span data-stu-id="06856-105">If you enter an Internet address for the shipping agent, and the agent provides package tracking services on the Internet, you can use the automatic package tracking feature.</span></span> <span data-ttu-id="06856-106">Pour plus d'informations, voir [Suivre des colis](sales-how-track-packages.md).</span><span class="sxs-lookup"><span data-stu-id="06856-106">For more information, see [Track Packages](sales-how-track-packages.md).</span></span>

<span data-ttu-id="06856-107">Lorsque vous configurez des transporteurs dans vos commandes vente, vous pouvez également spécifier les services proposés par chaque transporteur.</span><span class="sxs-lookup"><span data-stu-id="06856-107">When you set up shipping agents on your sales orders, you can also specify the services that each shipping agent offers.</span></span>  
<span data-ttu-id="06856-108">Pour chaque transporteur, vous pouvez définir un nombre illimité de services et spécifier un délai d'expédition pour chaque service.</span><span class="sxs-lookup"><span data-stu-id="06856-108">For each shipping agent, you can set up an unlimited number of services, and you can specify a shipping time for each service.</span></span>  

<span data-ttu-id="06856-109">Lorsque vous avez affecté une prestation transporteur à une ligne commande vente, le délai d'expédition de la prestation est inclus dans le calcul de la promesse de livraison, pour cette ligne.</span><span class="sxs-lookup"><span data-stu-id="06856-109">When you have assigned a shipping agent service to a sales order line, the shipping time of the service will be included in the order promising calculation, for that line.</span></span> <span data-ttu-id="06856-110">Pour plus d'informations, voir [Calculer des dates promesse livraison](sales-how-to-calculate-order-promising-dates.md).</span><span class="sxs-lookup"><span data-stu-id="06856-110">For more information, see [Calculate Order Promising Dates](sales-how-to-calculate-order-promising-dates.md).</span></span>

## <a name="to-set-up-a-shipping-agent"></a><span data-ttu-id="06856-111">Pour configurer des transporteurs</span><span class="sxs-lookup"><span data-stu-id="06856-111">To set up a shipping agent</span></span>  
1.  <span data-ttu-id="06856-112">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Transporteurs**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="06856-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Shipping Agents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="06856-113">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="06856-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="06856-114">.</span><span class="sxs-lookup"><span data-stu-id="06856-114">.</span></span>  
3.  <span data-ttu-id="06856-115">Sélectionnez l'action **Prestations transporteur**.</span><span class="sxs-lookup"><span data-stu-id="06856-115">Choose the **Shipping Agent Services** action.</span></span>
4. <span data-ttu-id="06856-116">Dans la fenêtre **Prestations transporteur**, renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="06856-116">In the **Shipping Agent Services**, fill in the fields as necessary.</span></span>

> [!NOTE]  
>  <span data-ttu-id="06856-117">Si vous supprimez le transporteur de la ligne commande, le code prestation transporteur est également supprimé de la ligne.</span><span class="sxs-lookup"><span data-stu-id="06856-117">If you delete the shipping agent on the order line, the shipping agent service code is also deleted.</span></span> <span data-ttu-id="06856-118">La valeur des champs basée en partie sur la prestation transporteur est ensuite recalculée.</span><span class="sxs-lookup"><span data-stu-id="06856-118">The contents of fields that were based in part on the shipping agent service are recalculated.</span></span>  

## <a name="see-also"></a><span data-ttu-id="06856-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06856-119">See Also</span></span>
<span data-ttu-id="06856-120">[Suivre des colis](sales-how-track-packages.md)  </span><span class="sxs-lookup"><span data-stu-id="06856-120">[Track Packages](sales-how-track-packages.md)  </span></span>  
[<span data-ttu-id="06856-121">Gestion d’entrepôt</span><span class="sxs-lookup"><span data-stu-id="06856-121">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="06856-122">STOCKS ET EN-COURS</span><span class="sxs-lookup"><span data-stu-id="06856-122">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="06856-123">[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="06856-123">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="06856-124">[Gestion des assemblages](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="06856-124">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="06856-125">Détails de conception : gestion d'entrepôt</span><span class="sxs-lookup"><span data-stu-id="06856-125">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="06856-126">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="06856-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

