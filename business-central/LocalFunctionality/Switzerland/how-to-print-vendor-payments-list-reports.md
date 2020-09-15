---
title: 'Procédure : imprimer des rapports contenant les listes de paiements fournisseurs'
description: Le rapport Liste de paiements fournisseur fournit la liste des paiements pour chaque fournisseur. Le rapport peut trier les paiements par ordre chronologique ou groupés par fournisseur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 35f867b1aaf62ee41abc96a4caa1d8ce32730edb
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778211"
---
# <a name="print-vendor-payments-list-reports"></a><span data-ttu-id="16e16-104">Imprimer des rapports contenant les listes de paiements fournisseurs</span><span class="sxs-lookup"><span data-stu-id="16e16-104">Print Vendor Payments List Reports</span></span>
<span data-ttu-id="16e16-105">Le rapport **Liste de paiements fournisseur** fournit la liste des paiements pour chaque fournisseur.</span><span class="sxs-lookup"><span data-stu-id="16e16-105">The **Vendor Payments List** report provides a list of payments for each vendor.</span></span> <span data-ttu-id="16e16-106">Le rapport peut trier les paiements par ordre chronologique ou groupés par fournisseur.</span><span class="sxs-lookup"><span data-stu-id="16e16-106">The report can sort payments chronologically or grouped by vendor.</span></span>  

## <a name="to-print-the-vendor-payments-list-report"></a><span data-ttu-id="16e16-107">Pour imprimer des rapports contenant les listes de paiements fournisseurs</span><span class="sxs-lookup"><span data-stu-id="16e16-107">To print the vendor payments list report</span></span>  

1.  <span data-ttu-id="16e16-108">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Liste de paiements fournisseur**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="16e16-108">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendor Payments List**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="16e16-109">Sous le raccourci **Options**, renseignez les champs comme indiqué dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="16e16-109">On the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="16e16-110">Champ</span><span class="sxs-lookup"><span data-stu-id="16e16-110">Field</span></span>|<span data-ttu-id="16e16-111">Désignation</span><span class="sxs-lookup"><span data-stu-id="16e16-111">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="16e16-112">**Tri**</span><span class="sxs-lookup"><span data-stu-id="16e16-112">**Sorting**</span></span>|<span data-ttu-id="16e16-113">Spécifie l'ordre de tri.</span><span class="sxs-lookup"><span data-stu-id="16e16-113">Specifies the sort order.</span></span> <span data-ttu-id="16e16-114">Vous pouvez effectuer un tri par fournisseur ou de façon chronologique.</span><span class="sxs-lookup"><span data-stu-id="16e16-114">You can sort by vendor or chronologically.</span></span> <span data-ttu-id="16e16-115">Si vous effectuez un tri par fournisseur, vous verrez un sous-total pour chaque fournisseur.</span><span class="sxs-lookup"><span data-stu-id="16e16-115">If you sort by vendor, you will see a subtotal for each vendor.</span></span> <span data-ttu-id="16e16-116">Si vous effectuez un tri chronologique, vous ne pourrez pas voir les sous-totaux.</span><span class="sxs-lookup"><span data-stu-id="16e16-116">If you sort chronologically, you will not see subtotals.</span></span>|  
    |<span data-ttu-id="16e16-117">**Mise en page**</span><span class="sxs-lookup"><span data-stu-id="16e16-117">**Layout**</span></span>|<span data-ttu-id="16e16-118">Spécifie la mise en page du rapport.</span><span class="sxs-lookup"><span data-stu-id="16e16-118">Specifies the layout of the report.</span></span><br /><br /> <span data-ttu-id="16e16-119">Les résultats peuvent être affichés dans les présentations suivantes :</span><span class="sxs-lookup"><span data-stu-id="16e16-119">The results can be displayed in the following layouts:</span></span><br /><br /> <span data-ttu-id="16e16-120">**Standard**</span><span class="sxs-lookup"><span data-stu-id="16e16-120">**Standard**</span></span><br /> <span data-ttu-id="16e16-121">Affiche le numéro du fournisseur et le nom du fournisseur, ainsi que les détails de la validation, tels que le numéro du document et le montant en devise locale.</span><span class="sxs-lookup"><span data-stu-id="16e16-121">Displays the vendor number and vendor name, together with posting details, such as the document number and the amount in local currency.</span></span><br /><br /> <span data-ttu-id="16e16-122">**Montants DE**</span><span class="sxs-lookup"><span data-stu-id="16e16-122">**FCY Amounts**</span></span><br /> <span data-ttu-id="16e16-123">Affiche le numéro du fournisseur, le nom du fournisseur, le numéro du document, le statut du paiement (O pour ouvert, PP pour paiement partiel et C pour clôturé) et le montant du paiement.</span><span class="sxs-lookup"><span data-stu-id="16e16-123">Displays the vendor number, vendor name, document number, payment status (O for open, PP for partial payment, and C for closed), and payment amount.</span></span><br /><br /> <span data-ttu-id="16e16-124">**Informations de validation**</span><span class="sxs-lookup"><span data-stu-id="16e16-124">**Posting Info**</span></span><br /> <span data-ttu-id="16e16-125">Affiche le numéro du fournisseur, le nom du fournisseur, le centre de coûts, les coûts associés, le code utilisateur et le montant règlement.</span><span class="sxs-lookup"><span data-stu-id="16e16-125">Displays the vendor number, vendor name, cost center, cost object, user ID, and payment amount.</span></span>|  

 <span data-ttu-id="16e16-126">À la fin du rapport, le nombre de paiements traités est affiché.</span><span class="sxs-lookup"><span data-stu-id="16e16-126">At the end of the report, the number of processed payments is displayed.</span></span>  

## <a name="see-also"></a><span data-ttu-id="16e16-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16e16-127">See Also</span></span>  
[<span data-ttu-id="16e16-128">Effectuer des paiements</span><span class="sxs-lookup"><span data-stu-id="16e16-128">Making Payments</span></span>](../../payables-make-payments.md)
