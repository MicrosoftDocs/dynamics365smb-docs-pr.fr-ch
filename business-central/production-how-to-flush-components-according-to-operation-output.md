---
title: Procédure de consommation en aval des composants en fonction de la production réalisée | Microsoft Docs
description: Pour les articles créés avec la méthode de consommation en amont le comportement par défaut est de calculer et de valider la consommation de composants lorsque vous affectez à l'ordre de fabrication lancé le statut **Terminé**. Pour plus d'informations, voir Méthode consommation.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 1198cb269e0864a6a8b45380d293c3d05290f269
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "921138"
---
# <a name="flush-components-according-to-operation-output"></a><span data-ttu-id="10cf7-104">Consommer en aval des composants en fonction de la production réalisée</span><span class="sxs-lookup"><span data-stu-id="10cf7-104">Flush Components According to Operation Output</span></span>
<span data-ttu-id="10cf7-105">Pour les articles créés avec la méthode de consommation en amont le comportement par défaut est de calculer et de valider la consommation de composants lorsque vous affectez à l'ordre de fabrication lancé le statut **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="10cf7-105">For items that are set up with backward flushing method, the default behavior is to calculate and post component consumption when you change the status of a released production order to **Finished**.</span></span>  

<span data-ttu-id="10cf7-106">Si vous définissez également les codes lien gamme, le calcul et la validation ont lieu lorsque chaque opération est terminée et la quantité effectivement consommée au cours de l'opération est validée.</span><span class="sxs-lookup"><span data-stu-id="10cf7-106">If you also define routing link codes, then calculation and posting occurs when each operation is finished, and the quantity that was actually consumed in the operation is posted.</span></span> <span data-ttu-id="10cf7-107">Pour plus d'informations, reportez-vous à [Créer des gammes](production-how-to-create-routings.md).</span><span class="sxs-lookup"><span data-stu-id="10cf7-107">For more information, see [Create Routings](production-how-to-create-routings.md).</span></span>  

<span data-ttu-id="10cf7-108">Par exemple, si un ordre de fabrication de 800 mètres nécessite pour son exécution 8 kilogrammes d'un composant, lorsque vous validez 200 mètres de production, 2 kilogrammes sont automatiquement validés comme étant consommés.</span><span class="sxs-lookup"><span data-stu-id="10cf7-108">For example, if a production order to produce 800 meters requires 8 kg of a component, then when you post 200 meters as output, 2 kg are automatically posted as consumption.</span></span>  

<span data-ttu-id="10cf7-109">Cette fonctionnalité est utile pour les motifs suivants :</span><span class="sxs-lookup"><span data-stu-id="10cf7-109">This functionality is useful for the following reasons:</span></span>  

-   <span data-ttu-id="10cf7-110">**Évaluation du stock** - Les écritures de valeur de production et de consommation sont créées parallèlement à l'état d'exécution de l'ordre de fabrication.</span><span class="sxs-lookup"><span data-stu-id="10cf7-110">**Inventory Valuation** - Value entries for output and consumption are created in parallel as the production order progresses.</span></span> <span data-ttu-id="10cf7-111">Sans les codes lien gamme, la valeur du stock augmente lorsque la production est validée, puis réduit ultérieurement lorsque la valeur de la consommation des composants est validée en même temps que l'ordre de fabrication terminé.</span><span class="sxs-lookup"><span data-stu-id="10cf7-111">Without routing link codes, the inventory value will increase as output is posted and then decrease at a later point in time when the value of component consumption is posted together with the finished production order.</span></span>  
-   <span data-ttu-id="10cf7-112">**Disponibilité du stock** - Avec une validation progressive de la consommation, la disponibilité des composants est mieux actualisée, ce qui est important pour conserver l'équilibre interne entre l'offre et la demande.</span><span class="sxs-lookup"><span data-stu-id="10cf7-112">**Inventory Availability** - With gradual consumption posting, the availability of component items is more up-to-date, which is important to maintain the internal balance between demand and supply.</span></span> <span data-ttu-id="10cf7-113">Sans les codes lien gamme, les autres demandeurs du composant peuvent croire qu'il est disponible tant que la validation de sa consommation reste en attente.</span><span class="sxs-lookup"><span data-stu-id="10cf7-113">Without routing link codes, other demands for the component may believe that it is available as long as it is pending a delayed consumption posting.</span></span>  
-   <span data-ttu-id="10cf7-114">**Just-in-Time** - Si vous pouvez personnaliser les produits en fonction des demandes client, vous pouvez réduire les rebuts en vous organisant pour que les procédures de travail et les systèmes ne soient modifiés que lorsque c'est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="10cf7-114">**Just-in-Time** – With the ability to customize products to customer requests, you can minimize waste by making sure that work and system changes only occur when it is necessary.</span></span>  

<span data-ttu-id="10cf7-115">La procédure suivante montre comment combiner la consommation en amont et les codes lien gamme pour que la quantité consommée par chaque opération soit proportionnelle à la production réelle de cette opération terminée.</span><span class="sxs-lookup"><span data-stu-id="10cf7-115">The following procedure shows how to combine backward flushing and routing link codes so that the quantity that is flushed for each operation is proportional to the actual output of the finished operation.</span></span>  

## <a name="to-flush-components-according-to-operation-output"></a><span data-ttu-id="10cf7-116">Pour consommer en aval des composants en fonction de la production réalisée</span><span class="sxs-lookup"><span data-stu-id="10cf7-116">To flush components according to operation output</span></span>  
1.  <span data-ttu-id="10cf7-117">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Articles**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="10cf7-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="10cf7-118">Choisissez l'action **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="10cf7-118">Choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="10cf7-119">Sur le raccourci **Réapprovisionnement**, dans le champ **Méthode consommation**, sélectionnez **En aval**.</span><span class="sxs-lookup"><span data-stu-id="10cf7-119">On the **Replenishment** FastTab, in the **Flushing Method** field, select **Forward**.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="10cf7-120">Sélectionnez **Prélèvement + Aval** si le composant est utilisé dans un magasin configuré pour un prélèvement et un rangement suggérés.</span><span class="sxs-lookup"><span data-stu-id="10cf7-120">Select **Pick+ Forward** if the component is used in a location that is set up for directed put-away and pick.</span></span>  

4.  <span data-ttu-id="10cf7-121">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Gammes**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="10cf7-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Routings**, and then choose the related link.</span></span>  
5.  <span data-ttu-id="10cf7-122">Définir les codes lien gamme pour chaque opération qui consomme le composant.</span><span class="sxs-lookup"><span data-stu-id="10cf7-122">Define routing link codes for every operation that consumes the component.</span></span> <span data-ttu-id="10cf7-123">Pour plus d'informations, reportez-vous à [Créer des gammes](production-how-to-create-routings.md).</span><span class="sxs-lookup"><span data-stu-id="10cf7-123">For more information, see [Create Routings ](production-how-to-create-routings.md).</span></span>  
6.  <span data-ttu-id="10cf7-124">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Nomenclature de production**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="10cf7-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Production BOM**, and then choose the related link.</span></span>  
7.  <span data-ttu-id="10cf7-125">Associe aux codes lien gamme de chaque instance du composant l'opération dans laquelle il est consommé.</span><span class="sxs-lookup"><span data-stu-id="10cf7-125">Define routing link codes from each instance of the component to the operation where it is consumed.</span></span>

    > [!IMPORTANT]  
    >  <span data-ttu-id="10cf7-126">Le composant doit avoir un lien gamme l'associant à la dernière opération de la gamme.</span><span class="sxs-lookup"><span data-stu-id="10cf7-126">The component must have a routing link to the last operation in the routing.</span></span>  

## <a name="see-also"></a><span data-ttu-id="10cf7-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10cf7-127">See Also</span></span>  
[<span data-ttu-id="10cf7-128">Créer des nomenclatures de production</span><span class="sxs-lookup"><span data-stu-id="10cf7-128">Create Production BOMs</span></span>](production-how-to-create-production-boms.md)  
[<span data-ttu-id="10cf7-129">Paramétrage de la production</span><span class="sxs-lookup"><span data-stu-id="10cf7-129">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="10cf7-130">[Production](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="10cf7-130">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="10cf7-131">[Planifié](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="10cf7-131">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="10cf7-132">STOCKS ET EN-COURS</span><span class="sxs-lookup"><span data-stu-id="10cf7-132">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="10cf7-133">Achats</span><span class="sxs-lookup"><span data-stu-id="10cf7-133">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="10cf7-134">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="10cf7-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
