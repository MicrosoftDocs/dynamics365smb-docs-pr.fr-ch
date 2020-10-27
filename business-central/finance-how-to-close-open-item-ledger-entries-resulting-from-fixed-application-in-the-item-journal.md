---
title: 'Procédure : clôturer les écritures comptables article ouvertes qui résultent d’un lettrage fixe dans la feuille article | Microsoft Docs'
description: Vous pouvez utiliser le champ **Lettrage à partir écriture** de la page **Feuille article** pour créer manuellement un lettrage fixe entre une transaction entrante et la transaction sortante initiale. Par exemple, pour corriger la transaction sortante ou pour traiter un retour.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 289c0aecbf45bbece3291edeed6e0e72aedb9a6b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924218"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a><span data-ttu-id="b2416-104">Clôturer les écritures comptables article ouvertes qui résultent d’un lettrage fixe dans la feuille article</span><span class="sxs-lookup"><span data-stu-id="b2416-104">Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>
<span data-ttu-id="b2416-105">Vous pouvez utiliser le champ **Lettrage à partir écriture** de la page **Feuille article** pour créer manuellement un lettrage fixe entre une transaction entrante et la transaction sortante initiale.</span><span class="sxs-lookup"><span data-stu-id="b2416-105">You can use the **Applies-from Entry** field on the **Item Journal** page to create a fixed application between an inbound transaction and the original outbound transaction.</span></span> <span data-ttu-id="b2416-106">Par exemple, pour corriger la transaction sortante ou pour traiter un retour.</span><span class="sxs-lookup"><span data-stu-id="b2416-106">For example, to correct the outbound transaction or to process its return.</span></span> <span data-ttu-id="b2416-107">Pour plus d’informations, voir Lettrage à partir écriture.</span><span class="sxs-lookup"><span data-stu-id="b2416-107">For more information, see Applies-from Entry.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="b2416-108">Les lettrages fixes exécutés de cette manière s’appliquent uniquement au coût, non à la quantité.</span><span class="sxs-lookup"><span data-stu-id="b2416-108">Fixed applications made in this manner only apply the cost, not the quantity.</span></span> <span data-ttu-id="b2416-109">Par conséquent, l’écriture comptable article positive enregistrée ne ferme pas l’écriture sortante rapprochée et demeure ouverte elle-même.</span><span class="sxs-lookup"><span data-stu-id="b2416-109">Accordingly, the posted positive item ledger entry will not close the applied outbound entry and will itself remain open.</span></span> <span data-ttu-id="b2416-110">Cela s’applique également lorsque vous validez un lettrage fixe pour une écriture positive vers une écriture négative qui n’a pas été clôturée par une écriture positive ordinaire ; les écritures négatives et positives restent ouvertes.</span><span class="sxs-lookup"><span data-stu-id="b2416-110">This also applies when you post a fixed application for a positive entry to a negative entry that has not been closed by a regular positive entry, then both the negative and the positive entries will remain open.</span></span>  
>   
>  <span data-ttu-id="b2416-111">Cela signifie également que vous ne pouvez pas clôturer une période inventaire si une telle écriture existe.</span><span class="sxs-lookup"><span data-stu-id="b2416-111">This also means that you cannot close an inventory period if such an entry exists.</span></span>  

<span data-ttu-id="b2416-112">La procédure suivante explique comment clôturer des écritures de ce genre au cours de deux validations de correction dans la feuille article.</span><span class="sxs-lookup"><span data-stu-id="b2416-112">The following procedure shows how to close such entries by performing two corrective postings in the item journal.</span></span>  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a><span data-ttu-id="b2416-113">Pour clôturer les écritures comptables article ouvertes qui résultent d’un lettrage fixe dans la feuille article</span><span class="sxs-lookup"><span data-stu-id="b2416-113">To close open item ledger entries that result from a fixed application in the item journal</span></span>  

1.  <span data-ttu-id="b2416-114">Utilisez le champ **Lettrage à partir écriture** pour valider un ajustement positif avec la quantité correspondante.</span><span class="sxs-lookup"><span data-stu-id="b2416-114">Use the **Applies-from Entry** field to post a positive adjustment with the corresponding quantity.</span></span> <span data-ttu-id="b2416-115">Cela permet de clôturer l’écriture négative initiale avec un lettrage fixe.</span><span class="sxs-lookup"><span data-stu-id="b2416-115">This closes the original negative entry with a fixed application.</span></span>  
2.  <span data-ttu-id="b2416-116">Utilisez le champ **Lettrage à partir écriture** pour valider un ajustement négatif.</span><span class="sxs-lookup"><span data-stu-id="b2416-116">Use the **Applies-to Entry** field to post a negative adjustment.</span></span> <span data-ttu-id="b2416-117">Cela permet de clôturer l’écriture positive de correction initiale avec un lettrage fixe.</span><span class="sxs-lookup"><span data-stu-id="b2416-117">This closes the original corrective positive entry with a fixed application.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b2416-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2416-118">See Also</span></span>  
[<span data-ttu-id="b2416-119">Supprimer et relettrer des écritures comptables article</span><span class="sxs-lookup"><span data-stu-id="b2416-119"> Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)  
 <span data-ttu-id="b2416-120">[Traiter les retours et annulations de ventes](sales-how-process-sales-returns-cancellations.md) </span><span class="sxs-lookup"><span data-stu-id="b2416-120">[Process Sales Returns and Cancellations](sales-how-process-sales-returns-cancellations.md) </span></span>  
 <span data-ttu-id="b2416-121">[Configuration de l’évaluation du stock](finance-set-up-inventory-valuation-and-costing.md) </span><span class="sxs-lookup"><span data-stu-id="b2416-121">[Setting Up Inventory Valuation and Costing](finance-set-up-inventory-valuation-and-costing.md) </span></span>  
 <span data-ttu-id="b2416-122">[Gestion des coûts ajustés](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="b2416-122">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 [<span data-ttu-id="b2416-123">Détails de conception : modes évaluation stock</span><span class="sxs-lookup"><span data-stu-id="b2416-123">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)
