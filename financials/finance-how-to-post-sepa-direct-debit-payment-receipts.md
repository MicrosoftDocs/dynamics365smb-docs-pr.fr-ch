---
title: "Valider des paiements par prélèvement SEPA | Microsoft Docs"
description: "Lorsqu'une collection prélèvement automatique est correctement traitée par votre banque, vous pouvez procéder à la validation de la réception du paiement pour les factures vente impliquées."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 0031017c96172dca76b50542e52c6a437c01427a
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="post-sepa-direct-debit-payment-receipts"></a><span data-ttu-id="7bc9c-103">Valider des réceptions règlement de prélèvement SEPA</span><span class="sxs-lookup"><span data-stu-id="7bc9c-103">Post SEPA Direct Debit Payment Receipts</span></span>
<span data-ttu-id="7bc9c-104">Lorsqu'une collection prélèvement automatique est correctement traitée par votre banque, vous pouvez procéder à la validation de la réception du paiement pour les factures vente impliquées.</span><span class="sxs-lookup"><span data-stu-id="7bc9c-104">When a direct debit collection is successfully processed by your bank, you can proceed to post receipt of the payment for the involved sales invoices.</span></span> <span data-ttu-id="7bc9c-105">Pour plus d'informations, voir [Créer des écritures de collection prélèvement automatique SEPA et les exporter vers un fichier bancaire](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="7bc9c-105">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  

<span data-ttu-id="7bc9c-106">Vous pouvez valider la réception paiement directement à partir de la fenêtre **Recouvrements prélèvement** ou de la fenêtre **Écritures recouvrement prélèvement**.</span><span class="sxs-lookup"><span data-stu-id="7bc9c-106">You can post the payment receipt directly from the **Direct Debit Collections** window or the **Direct Debit Collect. Entries** window.</span></span> <span data-ttu-id="7bc9c-107">Vous pouvez également relayer le travail à un autre utilisateur en préparant les lignes feuille associées.</span><span class="sxs-lookup"><span data-stu-id="7bc9c-107">Alternatively, you can relay the work to another user by preparing the related journal lines.</span></span>  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-window"></a><span data-ttu-id="7bc9c-108">Pour valider une réception de paiement de prélèvement automatique à partir de la fenêtre Collections prélèvement automatique</span><span class="sxs-lookup"><span data-stu-id="7bc9c-108">To post a direct-debit payment receipt from the Direct Debit Collections window</span></span>  
1. <span data-ttu-id="7bc9c-109">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), saisissez **Recouvrements prélèvement**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="7bc9c-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Direct Debit Collections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7bc9c-110">Sélectionnez une ligne pour une collection prélèvement automatique qui a été exportée vers un fichier bancaire et traitée avec succès par la banque.</span><span class="sxs-lookup"><span data-stu-id="7bc9c-110">Select a line for a direct debit collection that has been exported to a bank file and successfully processed by the bank.</span></span> <span data-ttu-id="7bc9c-111">Pour plus d'informations, voir [Créer des écritures de collection prélèvement automatique SEPA et les exporter vers un fichier bancaire](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="7bc9c-111">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  
3. <span data-ttu-id="7bc9c-112">Sélectionnez l'action **Valider reçus paiement**.</span><span class="sxs-lookup"><span data-stu-id="7bc9c-112">Choose the **Post Payment Receipts** action.</span></span>  
4. <span data-ttu-id="7bc9c-113">Dans la fenêtre **Valider recouvrement prélèvement**, renseignez les champs comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7bc9c-113">In the **Post Direct Debit Collection** window, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="7bc9c-114">Champ</span><span class="sxs-lookup"><span data-stu-id="7bc9c-114">Field</span></span>|<span data-ttu-id="7bc9c-115">Désignation</span><span class="sxs-lookup"><span data-stu-id="7bc9c-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="7bc9c-116">**N° recouvrement prélèvement**</span><span class="sxs-lookup"><span data-stu-id="7bc9c-116">**Direct Debit Collection No.**</span></span>|<span data-ttu-id="7bc9c-117">Spécifie la collection prélèvement automatique pour laquelle vous souhaitez valider la réception paiement.</span><span class="sxs-lookup"><span data-stu-id="7bc9c-117">Specify the direct debit collection that you want to post payment receipt for.</span></span>|  
    |<span data-ttu-id="7bc9c-118">**Modèle feuille comptabilité**</span><span class="sxs-lookup"><span data-stu-id="7bc9c-118">**General Journal Template**</span></span>|<span data-ttu-id="7bc9c-119">Spécifie le modèle de feuille comptabilité à utiliser pour la validation de la réception du paiement, comme le modèle pour les encaissements.</span><span class="sxs-lookup"><span data-stu-id="7bc9c-119">Specify which general journal template to use for posting the payment receipt, such as the template for cash receipts.</span></span>|  
    |<span data-ttu-id="7bc9c-120">**Nom feuille comptabilité**</span><span class="sxs-lookup"><span data-stu-id="7bc9c-120">**General Journal Batch Name**</span></span>|<span data-ttu-id="7bc9c-121">Spécifie la feuille comptabilité à utiliser pour la validation de la réception du paiement.</span><span class="sxs-lookup"><span data-stu-id="7bc9c-121">Specify which general journal batch to use for posting the payment receipt.</span></span>|  
    |<span data-ttu-id="7bc9c-122">**Créer feuille uniquement**</span><span class="sxs-lookup"><span data-stu-id="7bc9c-122">**Create Journal Only**</span></span>|<span data-ttu-id="7bc9c-123">Activez cette case à cocher si vous ne souhaitez pas valider la réception règlement lorsque vous cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="7bc9c-123">Select this check box if you do not want to post the payment receipt when you choose the **OK** button.</span></span> <span data-ttu-id="7bc9c-124">La réception de paiements est préparée dans la feuille spécifiée et n'est pas validée jusqu'à ce qu'une personne valide les lignes feuille en question.</span><span class="sxs-lookup"><span data-stu-id="7bc9c-124">The payment receipt will be prepared in the specified journal and will not be posted until someone posts the journal lines in question.</span></span>|  

5. <span data-ttu-id="7bc9c-125">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="7bc9c-125">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7bc9c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7bc9c-126">See Also</span></span>  
 <span data-ttu-id="7bc9c-127">[Recouvrement de paiements par prélèvement automatique SEPA](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="7bc9c-127">[Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
 [<span data-ttu-id="7bc9c-128">Ventes</span><span class="sxs-lookup"><span data-stu-id="7bc9c-128">Sales</span></span>](sales-manage-sales.md)

