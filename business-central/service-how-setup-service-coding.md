---
title: Configurer des codes prestations standard | Microsoft Docs
description: "Découvrez comment configurer des codes pour les activités de service que vous effectuez souvent."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, service order, repairs, maintenance
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: f73f5b9d74e7b6a75be6320697aa1a4ad84fb4a1
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---

# <a name="set-up-standard-service-codes"></a><span data-ttu-id="7a9fc-103">Configurer des codes prestation standard</span><span class="sxs-lookup"><span data-stu-id="7a9fc-103">Set Up Standard Service Codes</span></span>
<span data-ttu-id="7a9fc-104">Lorsque vous exécutez un service courant, il est fréquent que vous deviez créer des documents service qui utilisent des lignes service contenant des informations similaires.</span><span class="sxs-lookup"><span data-stu-id="7a9fc-104">When you perform typical service, you often have to create service documents that use service lines that contain similar information.</span></span> <span data-ttu-id="7a9fc-105">Pour faciliter la création de ces lignes, vous pouvez configurer des codes prestation standard avec un ensemble prédéfini de lignes service.</span><span class="sxs-lookup"><span data-stu-id="7a9fc-105">To make it easy to create these lines, you can set up standard service codes that have a predefined set of service lines.</span></span> <span data-ttu-id="7a9fc-106">Lorsque vous sélectionnez le code sur un document service, les lignes sont saisies automatiquement.</span><span class="sxs-lookup"><span data-stu-id="7a9fc-106">When you choose the code on a service document, the lines are entered automatically.</span></span> <span data-ttu-id="7a9fc-107">Vous pouvez configurer autant de codes prestation standard que vous le souhaitez, et chaque code peut avoir un nombre illimité de lignes service de différents types, notamment l'article, la ressource, le coût ou le texte standard qui lui est associé.</span><span class="sxs-lookup"><span data-stu-id="7a9fc-107">You can set up any number of standard service codes, and each code can have an unlimited number of service lines of different types, including item, resource, cost, or standrd text linked to it.</span></span> <span data-ttu-id="7a9fc-108">Créez des lignes service pour chaque code prestation standard dans la fiche **Code prestation standard**.</span><span class="sxs-lookup"><span data-stu-id="7a9fc-108">You create service lines of each standard serice code on the **Standard Service Code** card.</span></span> <span data-ttu-id="7a9fc-109">Vous pouvez ensuite affecter les codes prestation standard à des groupes articles de service dans la fenêtre **Codes gpe articles de service standard**.</span><span class="sxs-lookup"><span data-stu-id="7a9fc-109">You then assign standard service codes to service item groups in the **Standard Serv. Item Gr. Codes** window.</span></span> <span data-ttu-id="7a9fc-110">Par la suite, lorsque vous créez un document service, vous pouvez utiliser l'action **Extraire codes prestation std** pour ajouter des lignes service.</span><span class="sxs-lookup"><span data-stu-id="7a9fc-110">Later, when you create a service document, you can use the **Get Standard Service Codes** action to add service lines.</span></span>  
  
> [!Tip]
>  <span data-ttu-id="7a9fc-111">Vous pouvez utiliser le même concept pour créer des lignes dans les documents achat et vente.</span><span class="sxs-lookup"><span data-stu-id="7a9fc-111">You can use the same concept to create lines on sales and purchase documents.</span></span> <span data-ttu-id="7a9fc-112">Pour plus d'informations, voir [Créer des lignes vente et achat récurrentes](sales-how-work-standard-lines.md).</span><span class="sxs-lookup"><span data-stu-id="7a9fc-112">For more information, see [Create Recurring Sales and Purchase Lines](sales-how-work-standard-lines.md).</span></span>    
  
## <a name="to-set-up-a-standard-service-code"></a><span data-ttu-id="7a9fc-113">Pour configurer un code prestation standard</span><span class="sxs-lookup"><span data-stu-id="7a9fc-113">To set up a standard service code</span></span>    
1. <span data-ttu-id="7a9fc-114">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Codes prestation standard**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="7a9fc-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Standard Service Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7a9fc-115">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="7a9fc-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="7a9fc-116">Renseignez les lignes service liées à ce code prestation.</span><span class="sxs-lookup"><span data-stu-id="7a9fc-116">Fill in the service lines linked to this service code.</span></span>  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a><span data-ttu-id="7a9fc-117">Pour affecter un code prestation standard à un groupe articles de service</span><span class="sxs-lookup"><span data-stu-id="7a9fc-117">To assign a standard service code to a service item group</span></span>
1. <span data-ttu-id="7a9fc-118">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Groupes articles de service**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="7a9fc-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7a9fc-119">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="7a9fc-119">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="7a9fc-120">Renseignez les lignes service liées à ce code prestation.</span><span class="sxs-lookup"><span data-stu-id="7a9fc-120">Fill in the service lines linked to this service code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7a9fc-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a9fc-121">See Also</span></span>
[<span data-ttu-id="7a9fc-122">Gestion des services</span><span class="sxs-lookup"><span data-stu-id="7a9fc-122">Service Management</span></span>](service-service.md)
