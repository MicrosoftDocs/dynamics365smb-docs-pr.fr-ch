---
title: "Détails de conception - Traçabilité | Microsoft Docs"
description: "Cette rubrique donne un aperçu des détails de conception pour la traçabilité."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/12/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 1dce0ea658a2083c3d896fe6324751f63aabce06
ms.contentlocale: fr-ch
ms.lasthandoff: 11/22/2018

---
# <a name="design-details-item-tracking"></a><span data-ttu-id="2177a-103">Détails de conception : traçabilité</span><span class="sxs-lookup"><span data-stu-id="2177a-103">Design Details: Item Tracking</span></span>
<span data-ttu-id="2177a-104">Étant donné que le flux de biens dans la chaîne d'approvisionnement moderne devient de plus en plus complexe, la capacité à effectuer le suivi des articles est de plus en plus importante pour les sociétés concernées.</span><span class="sxs-lookup"><span data-stu-id="2177a-104">As the flow of goods in today’s supply chain becomes more and more complex, the ability to keep track of items is increasingly important to the companies involved.</span></span> <span data-ttu-id="2177a-105">La surveillance du flux de transaction d'un article est une obligation légale dans le secteur de l'approvisionnement médical et chimique, mais d'autres sociétés peuvent souhaiter contrôler les produits avec des garanties ou des dates d'expiration pour des raisons de service client.</span><span class="sxs-lookup"><span data-stu-id="2177a-105">Monitoring an item’s transaction flow is a legal requirement in the business of medical and chemical supply, but other businesses may want to monitor products with warranties or expiration dates for customer service reasons.</span></span>  

<span data-ttu-id="2177a-106">Un système de traçabilité doit permettre à une société de traiter facilement les numéros de série et les numéros de lot, en considérant chaque marchandise comme étant unique : date et lieu de réception, lieu de stockage, date et lieu de vente.</span><span class="sxs-lookup"><span data-stu-id="2177a-106">An item tracking system should provide a company with easy handling of serial and lot numbers, considering each unique piece of merchandise: when and where received, where stored, when and where sold.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="2177a-107">a progressivement étendu sa prise en charge de ce besoin de l'entreprise et fournit actuellement des fonctionnalités à l'échelle de l'application, ainsi qu'une base solide pour le développement d'extensions.</span><span class="sxs-lookup"><span data-stu-id="2177a-107">has gradually expanded its coverage of this business requirement and today provides application-wide functionality and a solid core on which to develop extensions.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="2177a-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="2177a-108">In This Section</span></span>  
[<span data-ttu-id="2177a-109">Détails de conception : création de traçabilité</span><span class="sxs-lookup"><span data-stu-id="2177a-109">Design Details: Item Tracking Design</span></span>](design-details-item-tracking-design.md)  
[<span data-ttu-id="2177a-110">Détails de conception : structure de validation de traçabilité</span><span class="sxs-lookup"><span data-stu-id="2177a-110">Design Details: Item Tracking Posting Structure</span></span>](design-details-item-tracking-posting-structure.md)  
[<span data-ttu-id="2177a-111">Détails de conception : comparaison entre écritures traçabilité actives et historiques</span><span class="sxs-lookup"><span data-stu-id="2177a-111">Design Details: Active versus Historic Item Tracking Entries</span></span>](design-details-active-versus-historic-item-tracking-entries.md)  
[<span data-ttu-id="2177a-112">Détails de conception : page Lignes traçabilité</span><span class="sxs-lookup"><span data-stu-id="2177a-112">Design Details: Item Tracking Lines Page</span></span>](design-details-item-tracking-lines-window.md)  
[<span data-ttu-id="2177a-113">Détails de conception : disponibilité traçabilité</span><span class="sxs-lookup"><span data-stu-id="2177a-113">Design Details: Item Tracking Availability</span></span>](design-details-item-tracking-availability.md)  
[<span data-ttu-id="2177a-114">Détails de conception : traçabilité et planification d'article</span><span class="sxs-lookup"><span data-stu-id="2177a-114">Design Details: Item Tracking and Planning</span></span>](design-details-item-tracking-and-planning.md)  
[<span data-ttu-id="2177a-115">Détails de conception : traçabilité et réservations</span><span class="sxs-lookup"><span data-stu-id="2177a-115">Design Details: Item Tracking and Reservations</span></span>](design-details-item-tracking-and-reservations.md)  
[<span data-ttu-id="2177a-116">Détails de conception : traçabilité dans l'entrepôt</span><span class="sxs-lookup"><span data-stu-id="2177a-116">Design Details: Item Tracking in the Warehouse</span></span>](design-details-item-tracking-in-the-warehouse.md)

