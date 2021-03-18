---
title: Clôture des écritures comptables article provenant de l’utilisation d’une application fixe
description: Découvrez comment vous pouvez créer un lettrage fixe entre une transaction entrante et la transaction sortante initiale dans la feuille article.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/14/2020
ms.author: edupont
ms.openlocfilehash: 9aa24653d4ae957ff741e85a99c13e0c9a8f7173
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5381971"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a><span data-ttu-id="7fd41-103">Clôturer les écritures comptables article ouvertes qui résultent d’un lettrage fixe dans la feuille article</span><span class="sxs-lookup"><span data-stu-id="7fd41-103">Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>

<span data-ttu-id="7fd41-104">Vous pouvez utiliser le champ **Lettrage à partir écriture** de la page **Feuille article** pour créer manuellement un lettrage fixe entre une transaction entrante et la transaction sortante initiale.</span><span class="sxs-lookup"><span data-stu-id="7fd41-104">You can use the **Applies-from Entry** field on the **Item Journal** page to create a fixed application between an inbound transaction and the original outbound transaction.</span></span> <span data-ttu-id="7fd41-105">Par exemple, pour corriger la transaction sortante ou pour traiter un retour.</span><span class="sxs-lookup"><span data-stu-id="7fd41-105">For example, to correct the outbound transaction or to process its return.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="7fd41-106">Les lettrages fixes exécutés de cette manière s’appliquent uniquement au coût, non à la quantité.</span><span class="sxs-lookup"><span data-stu-id="7fd41-106">Fixed applications made in this manner only apply the cost, not the quantity.</span></span> <span data-ttu-id="7fd41-107">Par conséquent, l’écriture comptable article positive enregistrée ne ferme pas l’écriture sortante rapprochée et demeure ouverte elle-même.</span><span class="sxs-lookup"><span data-stu-id="7fd41-107">Accordingly, the posted positive item ledger entry will not close the applied outbound entry and will itself remain open.</span></span> <span data-ttu-id="7fd41-108">Cela s’applique également lorsque vous validez un lettrage fixe pour une écriture positive vers une écriture négative qui n’a pas été clôturée par une écriture positive ordinaire ; les écritures négatives et positives restent ouvertes.</span><span class="sxs-lookup"><span data-stu-id="7fd41-108">This also applies when you post a fixed application for a positive entry to a negative entry that has not been closed by a regular positive entry, then both the negative and the positive entries will remain open.</span></span>  
>
> <span data-ttu-id="7fd41-109">Cela signifie également que vous ne pouvez pas clôturer une période inventaire si une telle écriture existe.</span><span class="sxs-lookup"><span data-stu-id="7fd41-109">This also means that you cannot close an inventory period if such an entry exists.</span></span>  

<span data-ttu-id="7fd41-110">Vous pouvez modifier et relettrer des écritures lettrage dans certaines conditions à l’aide de la page **Feuille lettrage**.</span><span class="sxs-lookup"><span data-stu-id="7fd41-110">You can change and reapply application entries under certain conditions by using the **Application Worksheet** page.</span></span>  

<span data-ttu-id="7fd41-111">La procédure suivante explique comment clôturer des écritures de ce genre au cours de deux validations de correction dans la feuille article.</span><span class="sxs-lookup"><span data-stu-id="7fd41-111">The following procedure shows how to close such entries by performing two corrective postings in the item journal.</span></span>  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a><span data-ttu-id="7fd41-112">Pour clôturer les écritures comptables article ouvertes qui résultent d’un lettrage fixe dans la feuille article</span><span class="sxs-lookup"><span data-stu-id="7fd41-112">To close open item ledger entries that result from a fixed application in the item journal</span></span>  

1. <span data-ttu-id="7fd41-113">Utilisez le champ **Lettrage à partir écriture** pour valider un ajustement positif avec la quantité correspondante.</span><span class="sxs-lookup"><span data-stu-id="7fd41-113">Use the **Applies-from Entry** field to post a positive adjustment with the corresponding quantity.</span></span> <span data-ttu-id="7fd41-114">Cela permet de clôturer l’écriture négative initiale avec un lettrage fixe.</span><span class="sxs-lookup"><span data-stu-id="7fd41-114">This closes the original negative entry with a fixed application.</span></span>  

    <span data-ttu-id="7fd41-115">Le champ **Lettrage à partir d’écritures** spécifie le numéro de l’écriture comptable article sortant dont le coût est transmis à l’écriture comptable article entrant lorsque vous validez une transaction entrante de type **Ajustement positif** ou **Achats** avec la feuille article.</span><span class="sxs-lookup"><span data-stu-id="7fd41-115">The **Applies-from Entry** field specifies the number of the outbound item ledger entry whose cost is forwarded to the inbound item ledger entry when you post an inbound transaction of type **Positive Adjmt.** or **Purchase** with the item journal.</span></span>  
2. <span data-ttu-id="7fd41-116">Utilisez le champ **Lettrage à partir écriture** pour valider un ajustement négatif.</span><span class="sxs-lookup"><span data-stu-id="7fd41-116">Use the **Applies-to Entry** field to post a negative adjustment.</span></span> <span data-ttu-id="7fd41-117">Cela permet de clôturer l’écriture positive de correction initiale avec un lettrage fixe.</span><span class="sxs-lookup"><span data-stu-id="7fd41-117">This closes the original corrective positive entry with a fixed application.</span></span>  

    <span data-ttu-id="7fd41-118">Le champ **Lettrage à partir d’écritures** spécifie si la quantité dans la ligne feuille article doit être lettrée dans un document déjà validé.</span><span class="sxs-lookup"><span data-stu-id="7fd41-118">The **Applies-to Entry** field specifies if the quantity in the item journal line should be applied to an already-posted document.</span></span> <span data-ttu-id="7fd41-119">Si c’est le cas, entrez le numéro de l’écriture comptable article dans laquelle la ligne feuille article doit être lettrée.</span><span class="sxs-lookup"><span data-stu-id="7fd41-119">If this is the case, enter the entry number of the item ledger entry to which the item journal line should be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="7fd41-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fd41-120">See Also</span></span>

[<span data-ttu-id="7fd41-121">Supprimer et relettrer des écritures comptables article</span><span class="sxs-lookup"><span data-stu-id="7fd41-121">Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)  
[<span data-ttu-id="7fd41-122">Traiter les retours et annulations de ventes</span><span class="sxs-lookup"><span data-stu-id="7fd41-122">Process Sales Returns and Cancellations</span></span>](sales-how-process-sales-returns-cancellations.md)  
[<span data-ttu-id="7fd41-123">Configuration de l’évaluation du stock</span><span class="sxs-lookup"><span data-stu-id="7fd41-123">Setting Up Inventory Valuation and Costing</span></span>](finance-set-up-inventory-valuation-and-costing.md)  
[<span data-ttu-id="7fd41-124">Gestion des coûts ajustés</span><span class="sxs-lookup"><span data-stu-id="7fd41-124">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="7fd41-125">Détails de conception : modes évaluation stock</span><span class="sxs-lookup"><span data-stu-id="7fd41-125">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]