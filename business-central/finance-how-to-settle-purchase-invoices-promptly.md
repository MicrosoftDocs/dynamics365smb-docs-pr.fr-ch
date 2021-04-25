---
title: Établir rapidement des factures achat
description: Si vous devez payer le fournisseur en liquide ou par chèque, vous pouvez effectuer toutes les opérations nécessaires lorsque vous validez la facture.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: d7962031aa7dda7dafa96ade8e11339c06ebb305
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784607"
---
# <a name="settle-purchase-invoices-promptly"></a><span data-ttu-id="4c85c-103">Établir rapidement des factures achat</span><span class="sxs-lookup"><span data-stu-id="4c85c-103">Settle Purchase Invoices Promptly</span></span>

<span data-ttu-id="4c85c-104">Si vous devez payer le fournisseur en liquide ou par chèque, vous pouvez valider le paiement lorsque vous validez la facture.</span><span class="sxs-lookup"><span data-stu-id="4c85c-104">If you need to pay the vendor by cash or check, you can post the payment when you post the invoice.</span></span>  

> [!NOTE]  
> <span data-ttu-id="4c85c-105">Si vous payez fréquemment les factures par chèques, par transfert bancaire ou en espèces, il est conseillé de configurer un mode de règlement spécifique avec un compte contrepartie et de saisir ce mode dans le champ **Mode de règlement** sur la fiche fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4c85c-105">If you frequently pay purchase invoices in cash, check, or bank transfer, it is a good idea to set up a specific payment method with a balancing account and enter this method in the **Payment Method** field on the vendor card.</span></span> <span data-ttu-id="4c85c-106">Le programme insère automatiquement le numéro du compte contrepartie sur l’en-tête facture à chaque fois que vous créez une facture.</span><span class="sxs-lookup"><span data-stu-id="4c85c-106">The balancing account number is inserted automatically on the invoice header every time you create a new invoice.</span></span> <span data-ttu-id="4c85c-107">Pour plus d’informations, consultez [Définir les modes de règlement](finance-payment-methods.md).</span><span class="sxs-lookup"><span data-stu-id="4c85c-107">For more information, see [Defining Payment Methods](finance-payment-methods.md).</span></span>  

## <a name="to-settle-purchase-invoices-promptly"></a><span data-ttu-id="4c85c-108">Pour établir rapidement des factures achat</span><span class="sxs-lookup"><span data-stu-id="4c85c-108">To settle purchase invoices promptly</span></span>

1. <span data-ttu-id="4c85c-109">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Factures achat**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="4c85c-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4c85c-110">Sélectionnez l’action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="4c85c-110">Choose the **New** action.</span></span>  
3. <span data-ttu-id="4c85c-111">Pour payer en liquide ou par virement bancaire, saisissez le numéro du compte général règlement ou du compte bancaire dans le champ **N° compte contrepartie**.</span><span class="sxs-lookup"><span data-stu-id="4c85c-111">To pay either in cash or by bank transfer, enter the number of the general ledger cash account or the bank account in the **Bal. Account No.** field.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="4c85c-112">Les champs **Type compte contrepartie** et **N° compte contrepartie** ne font pas partie de la présentation standard de l’en-tête facture.</span><span class="sxs-lookup"><span data-stu-id="4c85c-112">The **Bal. Account Type** and **Bal. Account No.** fields are not included in the standard layout of the invoice header.</span></span> <span data-ttu-id="4c85c-113">Afin de valider le paiement d’une facture, vous devez contacter un partenaire Microsoft qui peut ajouter les champs par code.</span><span class="sxs-lookup"><span data-stu-id="4c85c-113">In order to post the payment of an invoice, you must contact a Microsoft partner who can add the fields through code.</span></span>  
>
> <span data-ttu-id="4c85c-114">Cette personnalisation n’est requise que si vous ne spécifiez pas de comptes contrepartie sur les modes de paiement comme décrit ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="4c85c-114">This customization is only required if you do not specify balancing accounts on the payment methods as describe above.</span></span>

## <a name="see-also"></a><span data-ttu-id="4c85c-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c85c-115">See Also</span></span>

[<span data-ttu-id="4c85c-116">Gestion des comptes fournisseur</span><span class="sxs-lookup"><span data-stu-id="4c85c-116">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="4c85c-117">Achats</span><span class="sxs-lookup"><span data-stu-id="4c85c-117">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="4c85c-118">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4c85c-118">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]