---
title: 'Procédure : imprimer des rapports contenant les listes de paiements fournisseurs'
description: Le rapport Liste de paiements fournisseur fournit la liste des paiements pour chaque fournisseur. Le rapport peut trier les paiements par ordre chronologique ou groupés par fournisseur.
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
ms.openlocfilehash: e3d8e38ed8dfa9143c0436c366be1f090b18be55
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "930518"
---
# <a name="print-vendor-payments-list-reports"></a><span data-ttu-id="088bb-104">Imprimer des rapports contenant les listes de paiements fournisseurs</span><span class="sxs-lookup"><span data-stu-id="088bb-104">Print Vendor Payments List Reports</span></span>
<span data-ttu-id="088bb-105">Le rapport **Liste de paiements fournisseur** fournit la liste des paiements pour chaque fournisseur.</span><span class="sxs-lookup"><span data-stu-id="088bb-105">The **Vendor Payments List** report provides a list of payments for each vendor.</span></span> <span data-ttu-id="088bb-106">Le rapport peut trier les paiements par ordre chronologique ou groupés par fournisseur.</span><span class="sxs-lookup"><span data-stu-id="088bb-106">The report can sort payments chronologically or grouped by vendor.</span></span>  

## <a name="to-print-the-vendor-payments-list-report"></a><span data-ttu-id="088bb-107">Pour imprimer des rapports contenant les listes de paiements fournisseurs</span><span class="sxs-lookup"><span data-stu-id="088bb-107">To print the vendor payments list report</span></span>  

1.  <span data-ttu-id="088bb-108">Choisissez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Liste de paiements fournisseurs**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="088bb-108">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendor Payments List**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="088bb-109">Sous le raccourci **Options**, renseignez les champs comme indiqué dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="088bb-109">On the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="088bb-110">Champ</span><span class="sxs-lookup"><span data-stu-id="088bb-110">Field</span></span>|<span data-ttu-id="088bb-111">Désignation</span><span class="sxs-lookup"><span data-stu-id="088bb-111">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="088bb-112">**Tri**</span><span class="sxs-lookup"><span data-stu-id="088bb-112">**Sorting**</span></span>|<span data-ttu-id="088bb-113">Spécifie l'ordre de tri.</span><span class="sxs-lookup"><span data-stu-id="088bb-113">Specifies the sort order.</span></span> <span data-ttu-id="088bb-114">Vous pouvez effectuer un tri par fournisseur ou de façon chronologique.</span><span class="sxs-lookup"><span data-stu-id="088bb-114">You can sort by vendor or chronologically.</span></span> <span data-ttu-id="088bb-115">Si vous effectuez un tri par fournisseur, vous verrez un sous-total pour chaque fournisseur.</span><span class="sxs-lookup"><span data-stu-id="088bb-115">If you sort by vendor, you will see a subtotal for each vendor.</span></span> <span data-ttu-id="088bb-116">Si vous effectuez un tri chronologique, vous ne pourrez pas voir les sous-totaux.</span><span class="sxs-lookup"><span data-stu-id="088bb-116">If you sort chronologically, you will not see subtotals.</span></span>|  
    |<span data-ttu-id="088bb-117">**Mise en page**</span><span class="sxs-lookup"><span data-stu-id="088bb-117">**Layout**</span></span>|<span data-ttu-id="088bb-118">Spécifie la mise en page du rapport.</span><span class="sxs-lookup"><span data-stu-id="088bb-118">Specifies the layout of the report.</span></span><br /><br /> <span data-ttu-id="088bb-119">Les résultats peuvent être affichés dans les présentations suivantes :</span><span class="sxs-lookup"><span data-stu-id="088bb-119">The results can be displayed in the following layouts:</span></span><br /><br /> <span data-ttu-id="088bb-120">**Standard**</span><span class="sxs-lookup"><span data-stu-id="088bb-120">**Standard**</span></span><br /> <span data-ttu-id="088bb-121">Affiche le numéro du fournisseur et le nom du fournisseur, ainsi que les détails de la validation, tels que le numéro du document et le montant en devise locale.</span><span class="sxs-lookup"><span data-stu-id="088bb-121">Displays the vendor number and vendor name, together with posting details, such as the document number and the amount in local currency.</span></span><br /><br /> <span data-ttu-id="088bb-122">**Montants DE**</span><span class="sxs-lookup"><span data-stu-id="088bb-122">**FCY Amounts**</span></span><br /> <span data-ttu-id="088bb-123">Affiche le numéro du fournisseur, le nom du fournisseur, le numéro du document, le statut du paiement (O pour ouvert, PP pour paiement partiel et C pour clôturé) et le montant du paiement.</span><span class="sxs-lookup"><span data-stu-id="088bb-123">Displays the vendor number, vendor name, document number, payment status (O for open, PP for partial payment, and C for closed), and payment amount.</span></span><br /><br /> <span data-ttu-id="088bb-124">**Informations de validation**</span><span class="sxs-lookup"><span data-stu-id="088bb-124">**Posting Info**</span></span><br /> <span data-ttu-id="088bb-125">Affiche le numéro du fournisseur, le nom du fournisseur, le centre de coûts, les coûts associés, le code utilisateur et le montant règlement.</span><span class="sxs-lookup"><span data-stu-id="088bb-125">Displays the vendor number, vendor name, cost center, cost object, user ID, and payment amount.</span></span>|  

 <span data-ttu-id="088bb-126">À la fin du rapport, le nombre de paiements traités est affiché.</span><span class="sxs-lookup"><span data-stu-id="088bb-126">At the end of the report, the number of processed payments is displayed.</span></span>  

## <a name="see-also"></a><span data-ttu-id="088bb-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="088bb-127">See Also</span></span>  
[<span data-ttu-id="088bb-128">Effectuer des paiements</span><span class="sxs-lookup"><span data-stu-id="088bb-128">Making Payments</span></span>](../../payables-make-payments.md)
