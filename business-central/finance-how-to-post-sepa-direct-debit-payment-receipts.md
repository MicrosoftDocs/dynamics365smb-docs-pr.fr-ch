---
title: Valider des paiements par prélèvement SEPA | Microsoft Docs
description: Lorsqu'une collection prélèvement automatique est correctement traitée par votre banque, vous pouvez procéder à la validation de la réception du paiement pour les factures vente impliquées.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-collect-payments-with-sepa-direct-debit
ms.openlocfilehash: 6c646575ba803358aa00309ce02742423bcc7de8
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "930770"
---
# <a name="post-sepa-direct-debit-payment-receipts"></a><span data-ttu-id="461ab-103">Valider des réceptions règlement de prélèvement SEPA</span><span class="sxs-lookup"><span data-stu-id="461ab-103">Post SEPA Direct Debit Payment Receipts</span></span>
<span data-ttu-id="461ab-104">Lorsqu'une collection prélèvement automatique est correctement traitée par votre banque, vous pouvez procéder à la validation de la réception du paiement pour les factures vente impliquées.</span><span class="sxs-lookup"><span data-stu-id="461ab-104">When a direct debit collection is successfully processed by your bank, you can proceed to post receipt of the payment for the involved sales invoices.</span></span> <span data-ttu-id="461ab-105">Pour plus d'informations, voir [Créer des écritures de collection prélèvement automatique SEPA et les exporter vers un fichier bancaire](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="461ab-105">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  

<span data-ttu-id="461ab-106">Vous pouvez valider la réception paiement directement à partir de la page **Recouvrements prélèvement** ou de la page **Écritures recouvrement prélèvement**.</span><span class="sxs-lookup"><span data-stu-id="461ab-106">You can post the payment receipt directly from the **Direct Debit Collections** page or the **Direct Debit Collect. Entries** page.</span></span> <span data-ttu-id="461ab-107">Vous pouvez également relayer le travail à un autre utilisateur en préparant les lignes feuille associées.</span><span class="sxs-lookup"><span data-stu-id="461ab-107">Alternatively, you can relay the work to another user by preparing the related journal lines.</span></span>  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-page"></a><span data-ttu-id="461ab-108">Pour valider une réception de paiement de prélèvement automatique à partir de la page Collections prélèvement automatique</span><span class="sxs-lookup"><span data-stu-id="461ab-108">To post a direct-debit payment receipt from the Direct Debit Collections page</span></span>  
1. <span data-ttu-id="461ab-109">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Recouvrements prélèvement**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="461ab-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Direct Debit Collections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="461ab-110">Sélectionnez une ligne pour une collection prélèvement automatique qui a été exportée vers un fichier bancaire et traitée avec succès par la banque.</span><span class="sxs-lookup"><span data-stu-id="461ab-110">Select a line for a direct debit collection that has been exported to a bank file and successfully processed by the bank.</span></span> <span data-ttu-id="461ab-111">Pour plus d'informations, voir [Créer des écritures de collection prélèvement automatique SEPA et les exporter vers un fichier bancaire](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="461ab-111">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  
3. <span data-ttu-id="461ab-112">Sélectionnez l'action **Valider reçus paiement**.</span><span class="sxs-lookup"><span data-stu-id="461ab-112">Choose the **Post Payment Receipts** action.</span></span>  
4. <span data-ttu-id="461ab-113">Sur la page **Valider recouvrement prélèvement**, renseignez les champs comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="461ab-113">On the **Post Direct Debit Collection** page, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="461ab-114">Champ</span><span class="sxs-lookup"><span data-stu-id="461ab-114">Field</span></span>|<span data-ttu-id="461ab-115">Désignation</span><span class="sxs-lookup"><span data-stu-id="461ab-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="461ab-116">**N° recouvrement prélèvement**</span><span class="sxs-lookup"><span data-stu-id="461ab-116">**Direct Debit Collection No.**</span></span>|<span data-ttu-id="461ab-117">Spécifie la collection prélèvement automatique pour laquelle vous souhaitez valider la réception paiement.</span><span class="sxs-lookup"><span data-stu-id="461ab-117">Specify the direct debit collection that you want to post payment receipt for.</span></span>|  
    |<span data-ttu-id="461ab-118">**Modèle feuille comptabilité**</span><span class="sxs-lookup"><span data-stu-id="461ab-118">**General Journal Template**</span></span>|<span data-ttu-id="461ab-119">Spécifie le modèle de feuille comptabilité à utiliser pour la validation de la réception du paiement, comme le modèle pour les encaissements.</span><span class="sxs-lookup"><span data-stu-id="461ab-119">Specify which general journal template to use for posting the payment receipt, such as the template for cash receipts.</span></span>|  
    |<span data-ttu-id="461ab-120">**Nom feuille comptabilité**</span><span class="sxs-lookup"><span data-stu-id="461ab-120">**General Journal Batch Name**</span></span>|<span data-ttu-id="461ab-121">Spécifie la feuille comptabilité à utiliser pour la validation de la réception du paiement.</span><span class="sxs-lookup"><span data-stu-id="461ab-121">Specify which general journal batch to use for posting the payment receipt.</span></span>|  
    |<span data-ttu-id="461ab-122">**Créer feuille uniquement**</span><span class="sxs-lookup"><span data-stu-id="461ab-122">**Create Journal Only**</span></span>|<span data-ttu-id="461ab-123">Activez cette case à cocher si vous ne souhaitez pas valider la réception règlement lorsque vous cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="461ab-123">Select this check box if you do not want to post the payment receipt when you choose the **OK** button.</span></span> <span data-ttu-id="461ab-124">La réception de paiements est préparée dans la feuille spécifiée et n'est pas validée jusqu'à ce qu'une personne valide les lignes feuille en question.</span><span class="sxs-lookup"><span data-stu-id="461ab-124">The payment receipt will be prepared in the specified journal and will not be posted until someone posts the journal lines in question.</span></span>|  

5. <span data-ttu-id="461ab-125">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="461ab-125">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="461ab-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="461ab-126">See Also</span></span>  
 <span data-ttu-id="461ab-127">[Recouvrement de paiements par prélèvement automatique SEPA](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="461ab-127">[Collect Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
 [<span data-ttu-id="461ab-128">Ventes</span><span class="sxs-lookup"><span data-stu-id="461ab-128">Sales</span></span>](sales-manage-sales.md)
