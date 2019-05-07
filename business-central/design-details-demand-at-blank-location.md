---
title: Détails de conception - Demande et approvisionnement | Microsoft Docs
description: Cette rubrique présente le concept de demande, qui désigne toute sorte de demande brute, par exemple une commande vente et un besoin composant d'un ordre de fabrication.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 23e941b3ab6fc8e2176268f38647630419453d23
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "933901"
---
# <a name="design-details-demand-and-supply"></a><span data-ttu-id="cb88b-103">Détails de conception : demande et approvisionnement</span><span class="sxs-lookup"><span data-stu-id="cb88b-103">Design Details: Demand and Supply</span></span>
<span data-ttu-id="cb88b-104">Le mot demande désigne tout sorte de demande brute, par exemple une commande vente et un besoin composant d'un ordre de fabrication.</span><span class="sxs-lookup"><span data-stu-id="cb88b-104">Demand is the common term used for any kind of gross demand, such as a sales order and component need from a production order.</span></span> <span data-ttu-id="cb88b-105">En outre, le programme permet davantage de types techniques de demande, tels que le stock négatif et les retours achat.</span><span class="sxs-lookup"><span data-stu-id="cb88b-105">In addition, the program allows more technical types of demand, such as negative inventory and purchase returns.</span></span>  
  
<span data-ttu-id="cb88b-106">Approvisionnement est le terme courant utilisé pour désigner toute sorte de quantité positive ou d'entrée, telle qu'un stock, des achats, un assemblage, une production ou des transferts d'enlogement.</span><span class="sxs-lookup"><span data-stu-id="cb88b-106">Supply is the common term used for any kind of positive or inbound quantity, such as inventory, purchases, assembly, production, or inbound transfers.</span></span> <span data-ttu-id="cb88b-107">De plus, un retour vente peut également représenter un approvisionnement.</span><span class="sxs-lookup"><span data-stu-id="cb88b-107">In addition, a sales return may also represent supply.</span></span>  
  
<span data-ttu-id="cb88b-108">Pour trier les nombreuses sources de demande et d'approvisionnement, le système de planification les organise sur deux chronologies appelées profils de stock.</span><span class="sxs-lookup"><span data-stu-id="cb88b-108">To sort out the many sources of demand and supply, the planning system organizes them on two time lines called inventory profiles.</span></span> <span data-ttu-id="cb88b-109">Un profil contient des événements de demande, ainsi l'autre contient les événements d'approvisionnement correspondants.</span><span class="sxs-lookup"><span data-stu-id="cb88b-109">One profile holds demand events, and the other holds the corresponding supply events.</span></span> <span data-ttu-id="cb88b-110">Chaque événement représente une entité réseau de commande, par exemple une ligne commande vente, une écriture comptable article ou une ligne O.F.</span><span class="sxs-lookup"><span data-stu-id="cb88b-110">Each event represents one order network entity, such as a sales order line, an item ledger entry, or a production order line.</span></span>  
  
<span data-ttu-id="cb88b-111">Lorsque les profils de stock sont chargés, les différents ensembles demande-approvisionnement sont équilibrés pour produire un plan d'approvisionnement répondant aux objectifs répertoriés.</span><span class="sxs-lookup"><span data-stu-id="cb88b-111">When inventory profiles are loaded, the different demand-supply sets are balanced to output a supply plan that fulfills the listed goals.</span></span>  
  
<span data-ttu-id="cb88b-112">Les paramètres de planification et les niveaux de stock sont d'autres types de demande et d'approvisionnement respectivement, qui subissent un équilibrage intégré pour réapprovisionner les articles en stock.</span><span class="sxs-lookup"><span data-stu-id="cb88b-112">Planning parameters and inventory levels are other types of demand and supply respectively, which undergo integrated balancing to replenish stock items.</span></span> <span data-ttu-id="cb88b-113">Pour plus d'informations, voir [Détails de conception : gestion des méthodes de réapprovisionnement](design-details-handling-reordering-policies.md).</span><span class="sxs-lookup"><span data-stu-id="cb88b-113">For more information, see [Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cb88b-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb88b-114">See Also</span></span>  
<span data-ttu-id="cb88b-115">[Détails de conception : équilibrage de la demande et de l'approvisionnement](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="cb88b-115">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="cb88b-116">[Détails de conception : concepts centraux du système de planification](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="cb88b-116">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="cb88b-117">Détails de conception : planification de l'approvisionnement</span><span class="sxs-lookup"><span data-stu-id="cb88b-117">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)