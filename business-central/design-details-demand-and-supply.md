---
title: Détails de conception - Demande et approvisionnement | Microsoft Docs
description: Le mot demande désigne tout sorte de demande brute, par exemple une commande vente et un besoin composant d'un ordre de fabrication. En outre, le programme permet davantage de types techniques de demande, tels que le stock négatif et les retours achat.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/01/2017
ms.author: sgroespe
ms.openlocfilehash: c26e74cb2a362339b1e7c95809fb19e13869c61e
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242344"
---
# <a name="design-details-demand-and-supply"></a><span data-ttu-id="efd8f-104">Détails de conception : demande et approvisionnement</span><span class="sxs-lookup"><span data-stu-id="efd8f-104">Design Details: Demand and Supply</span></span>
<span data-ttu-id="efd8f-105">Le mot demande désigne tout sorte de demande brute, par exemple une commande vente et un besoin composant d'un ordre de fabrication.</span><span class="sxs-lookup"><span data-stu-id="efd8f-105">Demand is the common term used for any kind of gross demand, such as a sales order and component need from a production order.</span></span> <span data-ttu-id="efd8f-106">En outre, le programme permet davantage de types techniques de demande, tels que le stock négatif et les retours achat.</span><span class="sxs-lookup"><span data-stu-id="efd8f-106">In addition, the program allows more technical types of demand, such as negative inventory and purchase returns.</span></span>  
  
 <span data-ttu-id="efd8f-107">Approvisionnement est le terme courant utilisé pour désigner toute sorte de quantité positive ou d'entrée, telle qu'un stock, des achats, un assemblage, une production ou des transferts d'enlogement.</span><span class="sxs-lookup"><span data-stu-id="efd8f-107">Supply is the common term used for any kind of positive or inbound quantity, such as inventory, purchases, assembly, production, or inbound transfers.</span></span> <span data-ttu-id="efd8f-108">De plus, un retour vente peut également représenter un approvisionnement.</span><span class="sxs-lookup"><span data-stu-id="efd8f-108">In addition, a sales return may also represent supply.</span></span>  
  
 <span data-ttu-id="efd8f-109">Pour trier les nombreuses sources de demande et d'approvisionnement, le système de planification les organise sur deux chronologies appelées profils de stock.</span><span class="sxs-lookup"><span data-stu-id="efd8f-109">To sort out the many sources of demand and supply, the planning system organizes them on two time lines called inventory profiles.</span></span> <span data-ttu-id="efd8f-110">Un profil contient des événements de demande, ainsi l'autre contient les événements d'approvisionnement correspondants.</span><span class="sxs-lookup"><span data-stu-id="efd8f-110">One profile holds demand events, and the other holds the corresponding supply events.</span></span> <span data-ttu-id="efd8f-111">Chaque événement représente une entité réseau de commande, par exemple une ligne commande vente, une écriture comptable article ou une ligne O.F.</span><span class="sxs-lookup"><span data-stu-id="efd8f-111">Each event represents one order network entity, such as a sales order line, an item ledger entry, or a production order line.</span></span>  
  
 <span data-ttu-id="efd8f-112">Lorsque les profils de stock sont chargés, les différents ensembles demande-approvisionnement sont équilibrés pour produire un plan d'approvisionnement répondant aux objectifs répertoriés.</span><span class="sxs-lookup"><span data-stu-id="efd8f-112">When inventory profiles are loaded, the different demand-supply sets are balanced to output a supply plan that fulfills the listed goals.</span></span>  
  
 <span data-ttu-id="efd8f-113">Les paramètres de planification et les niveaux de stock sont d'autres types de demande et d'approvisionnement respectivement, qui subissent un équilibrage intégré pour réapprovisionner les articles en stock.</span><span class="sxs-lookup"><span data-stu-id="efd8f-113">Planning parameters and inventory levels are other types of demand and supply respectively, which undergo integrated balancing to replenish stock items.</span></span> <span data-ttu-id="efd8f-114">Pour plus d'informations, voir [Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md).</span><span class="sxs-lookup"><span data-stu-id="efd8f-114">For more information, see [Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="efd8f-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efd8f-115">See Also</span></span>  
 <span data-ttu-id="efd8f-116">[Détails de conception : équilibrage de la demande et de l'approvisionnement](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="efd8f-116">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
 <span data-ttu-id="efd8f-117">[Détails de conception : concepts centraux du système de planification](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="efd8f-117">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
 [<span data-ttu-id="efd8f-118">Détails de conception : planification de l'approvisionnement</span><span class="sxs-lookup"><span data-stu-id="efd8f-118">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)