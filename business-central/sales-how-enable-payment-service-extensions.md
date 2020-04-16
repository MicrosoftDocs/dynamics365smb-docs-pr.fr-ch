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
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 18ed3b77ffa369d4d9f3bd66ea54b81adb0c88e3
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191826"
---
# <a name="enable-customer-payments-through-payment-services"></a><span data-ttu-id="8481d-103">Activer les paiements client via les services de paiement</span><span class="sxs-lookup"><span data-stu-id="8481d-103">Enable Customer Payments Through Payment Services</span></span>
<span data-ttu-id="8481d-104">Au lieu de collecter des paiements par l'intermédiaire de transferts bancaires ou de cartes de crédit, vos clients peuvent vous payer via leur compte avec des services de paiement, tels que Microsoft Pay, PayPal ou WorldPay.</span><span class="sxs-lookup"><span data-stu-id="8481d-104">As an alternative to collecting payments through bank transfer or credit cards, your customers can pay you through their account with payment services, such as Microsoft Pay, PayPal, or WorldPay.</span></span>  

<span data-ttu-id="8481d-105">Après avoir activé un service de paiement dans [!INCLUDE[d365fin](includes/d365fin_md.md)], un lien est disponible vers le service sur les documents vente que vous envoyez par e-mail à vos clients.</span><span class="sxs-lookup"><span data-stu-id="8481d-105">After you enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)], a link to the service is available on sales documents that you send by email to your customers.</span></span> <span data-ttu-id="8481d-106">Les clients peuvent utiliser le lien pour accéder au service de paiement et payer la facture, directement à partir du document vente.</span><span class="sxs-lookup"><span data-stu-id="8481d-106">Customers can use the link to go to the payment service and pay the bill, directly from the sales document.</span></span> <span data-ttu-id="8481d-107">Si vous ne souhaitez pas inclure le lien, par exemple, si un client paie en liquide, vous pouvez supprimer le service de paiement de la facture avant la validation.</span><span class="sxs-lookup"><span data-stu-id="8481d-107">If you don't want to include the link, for example, if a customer will pay with cash, you can remove the payment service from the invoice before posting.</span></span>  

<span data-ttu-id="8481d-108">Les extensions Microsoft Pay, PayPal Payments Standard et WorldPay Payments Standard sont installées dans [!INCLUDE[d365fin](includes/d365fin_md.md)] et sont prêtes à être activées.</span><span class="sxs-lookup"><span data-stu-id="8481d-108">The Microsoft Pay, PayPal Payments Standard, and WorldPay Payments Standard extensions are installed in [!INCLUDE[d365fin](includes/d365fin_md.md)], and are ready for you to enable.</span></span>  

## <a name="to-enable-a-payment-service-in-d365fin"></a><span data-ttu-id="8481d-109">Pour activer un service de paiement dans [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="8481d-109">To enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
1. <span data-ttu-id="8481d-110">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Services de paiement**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="8481d-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8481d-111">Sur la page **Services de paiement**, sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="8481d-111">On the **Payment Services** page, choose the **New** action.</span></span>  
3. <span data-ttu-id="8481d-112">Sélectionnez le service de paiement, puis fermez la page.</span><span class="sxs-lookup"><span data-stu-id="8481d-112">Select the payment service, and then close the page.</span></span>  
4. <span data-ttu-id="8481d-113">Sur la page **Services de paiement**, sélectionnez l'action **Configuration**.</span><span class="sxs-lookup"><span data-stu-id="8481d-113">On the **Payment Services** page, choose the **Setup** action.</span></span>  
5. <span data-ttu-id="8481d-114">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="8481d-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="8481d-115">Fermez la page.</span><span class="sxs-lookup"><span data-stu-id="8481d-115">Close the page.</span></span>  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a><span data-ttu-id="8481d-116">Pour sélectionner un service de paiement dans une facture vente</span><span class="sxs-lookup"><span data-stu-id="8481d-116">To select a payment service on a sales invoice</span></span>
1. <span data-ttu-id="8481d-117">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Factures vente**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="8481d-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8481d-118">Ouvrez la facture vente que vous souhaitez payer en utilisant le service de paiement.</span><span class="sxs-lookup"><span data-stu-id="8481d-118">Open the sales invoice that you want to pay by using the payment service.</span></span>  
3. <span data-ttu-id="8481d-119">Dans le champ **Service de paiement**, sélectionnez le service de paiement.</span><span class="sxs-lookup"><span data-stu-id="8481d-119">In the **Payment Service** field, choose the payment service.</span></span>  

    > [!NOTE]  
    > <span data-ttu-id="8481d-120">Le champ **Service de paiement** est uniquement disponible si vous avez activé le service de paiement.</span><span class="sxs-lookup"><span data-stu-id="8481d-120">The **Payment Service** field is available only if you've enabled the payment service.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8481d-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8481d-121">See Also</span></span>  
[<span data-ttu-id="8481d-122">Définition des ventes</span><span class="sxs-lookup"><span data-stu-id="8481d-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="8481d-123">Ventes</span><span class="sxs-lookup"><span data-stu-id="8481d-123">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="8481d-124">[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide d'extensions](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="8481d-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="8481d-125">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8481d-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
