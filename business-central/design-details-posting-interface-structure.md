---
title: Détails de conception- Structure de l'interface de validation | Microsoft Docs
description: Cette rubrique donne un aperçu des procédures globales dans la structure de l'interface de validation.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: c50f045cf1a379d4fb908e0c17d7b9775fd1a9ee
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3184883"
---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="773a3-103">Détails de conception : Structure de l'interface de validation</span><span class="sxs-lookup"><span data-stu-id="773a3-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="773a3-104">Dans la structure de l'interface de validation [!INCLUDE[d365fin](includes/d365fin_md.md)], il y a plusieurs procédures globales utilisant la même structure :</span><span class="sxs-lookup"><span data-stu-id="773a3-104">In the [!INCLUDE[d365fin](includes/d365fin_md.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="773a3-105">Code de procédure d'appel RunWithCheck et RunWithoutCheck – interface de validation générique pour Gen.</span><span class="sxs-lookup"><span data-stu-id="773a3-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen.</span></span> <span data-ttu-id="773a3-106">Jnl Line.</span><span class="sxs-lookup"><span data-stu-id="773a3-106">Jnl Line.</span></span>  
* <span data-ttu-id="773a3-107">CustPostApplyCustLedgEntry – l'application du client de la validation, appelé à partir du codeunit 226 CustEntry-Appliquer les écritures validées.</span><span class="sxs-lookup"><span data-stu-id="773a3-107">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="773a3-108">VendPostApplyVendLedgEntry – validation de l'application du fournisseur, appelée à partir du codeunit 227 VendEntry-Appliquer les écritures validées.</span><span class="sxs-lookup"><span data-stu-id="773a3-108">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="773a3-109">UnapplyCustLedgEntry – validation de la désapplication de l'application du client, appelée à partir du codeunit 226 CustEntry-Appliquer les écritures validées</span><span class="sxs-lookup"><span data-stu-id="773a3-109">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="773a3-110">UnapplyVendLedgEntry – validation de la désapplication de l'application du fournisseur, appelée à partir du codeunit 227 VendEntry-Appliquer les écritures validées</span><span class="sxs-lookup"><span data-stu-id="773a3-110">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="773a3-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="773a3-111">See Also</span></span>  
[<span data-ttu-id="773a3-112">Détails de conception : Structure du moteur de validation</span><span class="sxs-lookup"><span data-stu-id="773a3-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)