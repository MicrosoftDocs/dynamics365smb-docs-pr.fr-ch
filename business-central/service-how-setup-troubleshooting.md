---
title: Configurer des processus incident | Microsoft Docs
description: "Découvrez comment configurer des processus qui aident les conseillers du service clientèle à identifier et à résoudre les problèmes liés aux articles de service."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, troubleshoot, repairs, maintenance
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 611ed0f5306dc03c3016aa720ea203c983064ebe
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---

# <a name="setting-up-troubleshooting-for-service-items"></a><span data-ttu-id="5d3ec-103">Configuration des processus incident pour les articles de service</span><span class="sxs-lookup"><span data-stu-id="5d3ec-103">Setting Up Troubleshooting for Service Items</span></span>
<span data-ttu-id="5d3ec-104">Vous pouvez configurer des instructions incident qui aident les conseillers du service clientèle à résoudre les problèmes lors de la fourniture de services.</span><span class="sxs-lookup"><span data-stu-id="5d3ec-104">You can set up troubleshooting guidelines that help technicians solve problems when providing service.</span></span> <span data-ttu-id="5d3ec-105">Par exemple, les instructions peuvent être une liste d'étapes pour effectuer une réparation, ou une série de questions à poser sur les articles.</span><span class="sxs-lookup"><span data-stu-id="5d3ec-105">For example, guidelines might be a list of steps to perform a repair, or a series of questions to ask about the items.</span></span> <span data-ttu-id="5d3ec-106">Une fois que vous avez configuré les instructions incident, vous pouvez les affecter à des groupes articles de service, des articles de service et des articles.</span><span class="sxs-lookup"><span data-stu-id="5d3ec-106">After you set up troubleshooting guidelines, you can assign them to service item groups, service items, and items.</span></span> <span data-ttu-id="5d3ec-107">Il existe une hiérarchie d'héritage pour les instructions.</span><span class="sxs-lookup"><span data-stu-id="5d3ec-107">There is an inheritance hierarchy for guidelines.</span></span> <span data-ttu-id="5d3ec-108">Si vous les affectez à un groupe articles de service, les articles inclus dans le groupe héritent des instructions sauf si vous les spécifiez pour les articles.</span><span class="sxs-lookup"><span data-stu-id="5d3ec-108">If you assign them to a service item group, the items included in the group will inherit the guidelines unless you specify them for the items.</span></span> <span data-ttu-id="5d3ec-109">De même, les articles de service héritent des instructions des articles.</span><span class="sxs-lookup"><span data-stu-id="5d3ec-109">Similarly, service items will inherit guidelines from items.</span></span>  

## <a name="to-set-up-troubleshooting-guidelines"></a><span data-ttu-id="5d3ec-110">Pour configurer des instructions incident</span><span class="sxs-lookup"><span data-stu-id="5d3ec-110">To set up troubleshooting guidelines</span></span>
1. <span data-ttu-id="5d3ec-111">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Incident**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="5d3ec-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Troubleshooting**, and then choose the related link.</span></span>  
2. <span data-ttu-id="5d3ec-112">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="5d3ec-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-troubleshooting-guidelines-to-items-service-items-or-service-item-groups"></a><span data-ttu-id="5d3ec-113">Pour affecter des instructions incident à des articles, des articles de service ou des groupes articles de service</span><span class="sxs-lookup"><span data-stu-id="5d3ec-113">To assign troubleshooting guidelines to items, service items, or service item groups</span></span>
1. <span data-ttu-id="5d3ec-114">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Articles**, **Articles de service** ou **Groupe articles de service**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="5d3ec-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, **Service Items**, or **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="5d3ec-115">Sélectionnez l'entité appropriée, puis l'action **Incident**.</span><span class="sxs-lookup"><span data-stu-id="5d3ec-115">Choose the relevant entity, and then choose the **Troubleshooting** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5d3ec-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d3ec-116">See Also</span></span>
[<span data-ttu-id="5d3ec-117">Gestion des services</span><span class="sxs-lookup"><span data-stu-id="5d3ec-117">Service Management</span></span>](service-service.md)
