---
title: Paramétrer les modes de paiement
description: Vous utilisez des modes de règlement, par exemple, les chèques, le transfert bancaire, les espèces, ou Paypal, pour définir la façon dont les factures vente et achat sont payées.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, bank transfer, cash, PayPal
ms.date: 01/21/2021
ms.author: bholtorf
ms.openlocfilehash: 7132f96327e468c200ebd1f41c0a1e5b767dea6b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5376852"
---
# <a name="set-up-payment-methods"></a><span data-ttu-id="fcf5c-103">Paramétrer les modes de paiement</span><span class="sxs-lookup"><span data-stu-id="fcf5c-103">Set Up Payment Methods</span></span>

<span data-ttu-id="fcf5c-104">Les modes de règlement définissent le mode de paiement que vous souhaitez voir vos clients utiliser, et comment vous souhaitez payer les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-104">Payment methods define the way you prefer for customers to pay you, and how you like to pay your vendors.</span></span> <span data-ttu-id="fcf5c-105">Le mode peut varier pour chaque client ou fournisseur.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-105">The method can vary for each customer or vendor.</span></span> <span data-ttu-id="fcf5c-106">Les exemples de modes de règlement courants sont **virement**, **espèces**, **chèque** ou **dépôt**.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-106">Examples of typical payment methods are **bank**, **cash**, **check**, or **account**.</span></span>

<span data-ttu-id="fcf5c-107">Vous pouvez affecter un mode de règlement aux clients et aux fournisseurs pour que le même mode soit toujours utilisé dans les documents achat et vente que vous créez pour eux.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-107">You can assign a payment method to customers and vendors so that the same method is always used on the sales and purchase documents you create for them.</span></span> <span data-ttu-id="fcf5c-108">Si nécessaire, vous pouvez modifier le mode du document vente ou achat.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-108">If needed, you can change the method on the sales or purchase document.</span></span> <span data-ttu-id="fcf5c-109">Par exemple, si vous souhaitez payer une facture achat donnée en espèces plutôt que par le chèque.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-109">For example, if you want to pay a particular purchase invoice in cash rather than by check.</span></span> <span data-ttu-id="fcf5c-110">Cela ne modifie pas le mode de règlement par défaut affecté au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-110">This does not change the default payment method assigned to the vendor.</span></span>

<span data-ttu-id="fcf5c-111">Les mêmes modes de règlement sont utilisés pour les documents vente et achat.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-111">The same payment methods are used for sales and purchase documents.</span></span> <span data-ttu-id="fcf5c-112">Par exemple, un mode de règlement _espèces_ est utilisé lorsque vous effectuez des paiements et lorsque vous recevez les.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-112">For example, a _cash_ payment method is used both when you make payments and when you receive them.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="fcf5c-113">sait que lorsque vous créez une facture vente vous pensez recevoir le paiement, et inversement pour les factures achat.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-113">knows that when you are creating a sales invoice you expect to receive payment, and the opposite for purchase invoices.</span></span>

<span data-ttu-id="fcf5c-114">Les avoirs pour les retours, cependant, sont des exceptions parce que le règlement s’effectue dans le sens inverse, de vous à votre client et de votre fournisseur à vous.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-114">Credit memos for returns, however, are exceptions because money is flowing in the opposite directions, from you to your customer and from your vendor to you.</span></span> <span data-ttu-id="fcf5c-115">Par conséquent, un mode de règlement par défaut n’est pas affecté aux avoirs.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-115">Therefore, a default payment method is not assigned to credit memos.</span></span> <span data-ttu-id="fcf5c-116">Il existe, cependant, une solution si vous avez spécifié des conditions de paiement pour le client ou le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-116">There is, however, a workaround if you have specified terms of payment for the customer or vendor.</span></span> <span data-ttu-id="fcf5c-117">Bien que le champ **Calculer escompte sur les avoirs** ne soit pas prévu pour cela, si vous activez la case à cocher sur la page **Conditions de paiement**, un mode de règlement par défaut est ajouté lorsque vous créez un avoir.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-117">Though the **Calc. Pmt. Disc. on Cr. Memos** field is not intended for this, if you choose the check box on the **Payment Terms** page a default payment method will be added when you create a credit memo.</span></span> <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE476Ys?rel=0]

## <a name="to-set-up-a-payment-method"></a><span data-ttu-id="fcf5c-118">Pour configurer un mode de règlement</span><span class="sxs-lookup"><span data-stu-id="fcf5c-118">To set up a payment method</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="fcf5c-119">fournit des modes de règlement que les entreprises utilisent souvent.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-119">provides a few payment methods that businesses often use.</span></span> <span data-ttu-id="fcf5c-120">Vous pouvez cependant en ajouter autant que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-120">You can, however, add as many as you need.</span></span>

1. <span data-ttu-id="fcf5c-121">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Modes de règlement**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="fcf5c-122">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-122">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="fcf5c-123">Vous pouvez éventuellement ajouter des conditions de paiement à votre mode de paiement.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-123">Optionally, add payment terms to your payment method.</span></span> <span data-ttu-id="fcf5c-124">Pour plus d’informations, voir [Paramétrer des conditions de paiement](finance-payment-terms.md).</span><span class="sxs-lookup"><span data-stu-id="fcf5c-124">For more information, see [Set Up Payment Terms](finance-payment-terms.md).</span></span>  

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a><span data-ttu-id="fcf5c-125">Pour affecter un mode de règlement à un client ou fournisseur</span><span class="sxs-lookup"><span data-stu-id="fcf5c-125">To assign a payment method to a customer or vendor</span></span>

1. <span data-ttu-id="fcf5c-126">Choisissez l’icône d’![ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Client** ou **Fournisseur**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer** or **Vendor**, and then choose the related link.</span></span>
2. <span data-ttu-id="fcf5c-127">Dans le champ **Code mode de règlement**, choisissez le mode à utiliser par défaut pour le client ou le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-127">In the **Payment Method Code** field, choose the method to use by default for the customer or vendor.</span></span>

## <a name="see-also"></a><span data-ttu-id="fcf5c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fcf5c-128">See Also</span></span>

[<span data-ttu-id="fcf5c-129">Enregistrer de nouveaux clients</span><span class="sxs-lookup"><span data-stu-id="fcf5c-129">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="fcf5c-130">Configurer des conditions de paiement</span><span class="sxs-lookup"><span data-stu-id="fcf5c-130">Set Up Payment Terms</span></span>](finance-payment-terms.md)  
[<span data-ttu-id="fcf5c-131">Finances</span><span class="sxs-lookup"><span data-stu-id="fcf5c-131">Finance</span></span>](finance.md)  
<span data-ttu-id="fcf5c-132">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fcf5c-132">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]