---
title: Activer les paiements client via les services de paiement| Microsoft Docs
description: Activez les services de paiement pour permettre aux clients de payer facilement leurs factures.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: e5d4d9fd0c6857c22f2b4c929a6e6ed528cadf26
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "931691"
---
# <a name="enable-customer-payments-through-payment-services"></a><span data-ttu-id="15eb9-103">Activer les paiements client via les services de paiement</span><span class="sxs-lookup"><span data-stu-id="15eb9-103">Enable Customer Payments Through Payment Services</span></span>
<span data-ttu-id="15eb9-104">Au lieu de collecter des paiements par l'intermédiaire de transferts bancaires ou de cartes de crédit, vos clients peuvent vous payer via leur compte avec des services de paiement, tels que Microsoft Pay, PayPal ou WorldPay.</span><span class="sxs-lookup"><span data-stu-id="15eb9-104">As an alternative to collecting payments through bank transfer or credit cards, your customers can pay you through their account with payment services, such as Microsoft Pay, PayPal, or WorldPay.</span></span>  

<span data-ttu-id="15eb9-105">Après avoir activé un service de paiement dans [!INCLUDE[d365fin](includes/d365fin_md.md)], un lien est disponible vers le service sur les documents vente que vous envoyez par e-mail à vos clients.</span><span class="sxs-lookup"><span data-stu-id="15eb9-105">After you enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)], a link to the service is available on sales documents that you send by email to your customers.</span></span> <span data-ttu-id="15eb9-106">Les clients peuvent utiliser le lien pour accéder au service de paiement et payer la facture, directement à partir du document vente.</span><span class="sxs-lookup"><span data-stu-id="15eb9-106">Customers can use the link to go to the payment service and pay the bill, directly from the sales document.</span></span> <span data-ttu-id="15eb9-107">Si vous ne souhaitez pas inclure le lien, par exemple, si un client paie en liquide, vous pouvez supprimer le service de paiement de la facture avant la validation.</span><span class="sxs-lookup"><span data-stu-id="15eb9-107">If you don't want to include the link, for example, if a customer will pay with cash, you can remove the payment service from the invoice before posting.</span></span>  

<span data-ttu-id="15eb9-108">Les extensions Microsoft Pay, PayPal Payments Standard et WorldPay Payments Standard sont installées dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et sont prêtes à être activées.</span><span class="sxs-lookup"><span data-stu-id="15eb9-108">The Microsoft Pay, PayPal Payments Standard, and WorldPay Payments Standard extensions are installed in [!INCLUDE[d365fin](includes/d365fin_md.md)], and are ready for you to enable.</span></span>  

## <a name="to-enable-a-payment-service-in-included365finincludesd365finmdmd"></a><span data-ttu-id="15eb9-109">Pour activer un service de paiement dans [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="15eb9-109">To enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
1. <span data-ttu-id="15eb9-110">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Services de paiement**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="15eb9-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="15eb9-111">Sur la page **Services de paiement**, sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="15eb9-111">On the **Payment Services** page, choose the **New** action.</span></span>  
3. <span data-ttu-id="15eb9-112">Sélectionnez le service de paiement, puis fermez la page.</span><span class="sxs-lookup"><span data-stu-id="15eb9-112">Select the payment service, and then close the page.</span></span>  
4. <span data-ttu-id="15eb9-113">Sur la page **Services de paiement**, sélectionnez l'action **Configuration**.</span><span class="sxs-lookup"><span data-stu-id="15eb9-113">On the **Payment Services** page, choose the **Setup** action.</span></span>  
5. <span data-ttu-id="15eb9-114">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="15eb9-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="15eb9-115">Fermez la page.</span><span class="sxs-lookup"><span data-stu-id="15eb9-115">Close the page.</span></span>  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a><span data-ttu-id="15eb9-116">Pour sélectionner un service de paiement dans une facture vente</span><span class="sxs-lookup"><span data-stu-id="15eb9-116">To select a payment service on a sales invoice</span></span>
1. <span data-ttu-id="15eb9-117">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Factures vente**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="15eb9-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="15eb9-118">Ouvrez la facture vente que vous souhaitez payer en utilisant le service de paiement.</span><span class="sxs-lookup"><span data-stu-id="15eb9-118">Open the sales invoice that you want to pay by using the payment service.</span></span>  
3. <span data-ttu-id="15eb9-119">Dans le champ **Service de paiement**, sélectionnez le service de paiement.</span><span class="sxs-lookup"><span data-stu-id="15eb9-119">In the **Payment Service** field, choose the payment service.</span></span>  

    > [!NOTE]  
    > <span data-ttu-id="15eb9-120">Le champ **Service de paiement** est uniquement disponible si vous avez activé le service de paiement.</span><span class="sxs-lookup"><span data-stu-id="15eb9-120">The **Payment Service** field is available only if you've enabled the payment service.</span></span>  

## <a name="see-also"></a><span data-ttu-id="15eb9-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15eb9-121">See Also</span></span>  
[<span data-ttu-id="15eb9-122">Définition des ventes</span><span class="sxs-lookup"><span data-stu-id="15eb9-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="15eb9-123">Ventes</span><span class="sxs-lookup"><span data-stu-id="15eb9-123">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="15eb9-124">[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide des extensions](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="15eb9-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="15eb9-125">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="15eb9-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
