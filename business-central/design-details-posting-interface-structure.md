---
title: Détails de conception- Structure de l’interface de validation | Microsoft Docs
description: Cette rubrique donne un aperçu des procédures globales dans la structure de l’interface de validation.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e306b0caeb58bfe7bd04f93ac64d8b593f70f695
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751270"
---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="a3a64-103">Détails de conception : Structure de l’interface de validation</span><span class="sxs-lookup"><span data-stu-id="a3a64-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="a3a64-104">Dans la structure de l’interface de validation [!INCLUDE[prod_short](includes/prod_short.md)], il y a plusieurs procédures globales utilisant la même structure :</span><span class="sxs-lookup"><span data-stu-id="a3a64-104">In the [!INCLUDE[prod_short](includes/prod_short.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="a3a64-105">Code de procédure d’appel RunWithCheck et RunWithoutCheck – interface de validation générique pour Gen.</span><span class="sxs-lookup"><span data-stu-id="a3a64-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen.</span></span> <span data-ttu-id="a3a64-106">Jnl Line.</span><span class="sxs-lookup"><span data-stu-id="a3a64-106">Jnl Line.</span></span>  
* <span data-ttu-id="a3a64-107">CustPostApplyCustLedgEntry – l’application du client de la validation, appelé à partir du codeunit 226 CustEntry-Appliquer les écritures validées.</span><span class="sxs-lookup"><span data-stu-id="a3a64-107">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="a3a64-108">VendPostApplyVendLedgEntry – validation de l’application du fournisseur, appelée à partir du codeunit 227 VendEntry-Appliquer les écritures validées.</span><span class="sxs-lookup"><span data-stu-id="a3a64-108">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="a3a64-109">UnapplyCustLedgEntry – validation de la désapplication de l’application du client, appelée à partir du codeunit 226 CustEntry-Appliquer les écritures validées</span><span class="sxs-lookup"><span data-stu-id="a3a64-109">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="a3a64-110">UnapplyVendLedgEntry – validation de la désapplication de l’application du fournisseur, appelée à partir du codeunit 227 VendEntry-Appliquer les écritures validées</span><span class="sxs-lookup"><span data-stu-id="a3a64-110">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a3a64-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3a64-111">See Also</span></span>  
[<span data-ttu-id="a3a64-112">Détails de conception : Structure du moteur de validation</span><span class="sxs-lookup"><span data-stu-id="a3a64-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)