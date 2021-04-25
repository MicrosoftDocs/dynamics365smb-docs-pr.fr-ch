---
title: Microsoft Pay Standard | Microsoft Docs
description: Fournit des informations sur l’extension Microsoft Pay
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 58c7ff08a7359b4f577b7ba40b23bc1f6310da4c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787342"
---
# <a name="the-microsoft-pay-extension"></a><span data-ttu-id="8a019-103">Extension Microsoft Pay</span><span class="sxs-lookup"><span data-stu-id="8a019-103">The Microsoft Pay Extension</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8a019-104">À compter du 8 février 2020, les changements dans le service Microsoft Pay affecteront l’extension Microsoft Pay dans Microsoft [!INCLUDE[prod_short](includes/prod_long.md)].</span><span class="sxs-lookup"><span data-stu-id="8a019-104">Effective February 8 2020, changes in the Microsoft Pay service will affect the Microsoft Pay extension in Microsoft [!INCLUDE[prod_short](includes/prod_long.md)].</span></span> <span data-ttu-id="8a019-105">En raison des changements, après le 8 février, les liens de paiement **Payer maintenant** que l’extension Microsoft Pay génère pour les factures dans [!INCLUDE[prod_short](includes/prod_short.md)] n’ouvriront pas Microsoft Pay.</span><span class="sxs-lookup"><span data-stu-id="8a019-105">Due to the changes, after February 8, the **Pay now** payment links that the Microsoft Pay extension generates for invoices in [!INCLUDE[prod_short](includes/prod_short.md)] will not open Microsoft Pay.</span></span> <span data-ttu-id="8a019-106">Les clients qui utilisent l’extension doivent modifier la configuration de leurs services de paiement pour qu’ils démarrent plutôt avec l’extension PayPal.</span><span class="sxs-lookup"><span data-stu-id="8a019-106">Customers who are using the extension should change their Payment Services setup to start using the PayPal extension instead.</span></span><br /></br>
>
> <span data-ttu-id="8a019-107">À partir du 8 janvier, nous afficherons une notification dans [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="8a019-107">From January 8, we will display a notification in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="8a019-108">La notification contiendra un lien vers les paramètres que vous devez modifier et vers un complément d’informations.</span><span class="sxs-lookup"><span data-stu-id="8a019-108">The notification will contain a link to the settings that you need to change and to more information.</span></span> <span data-ttu-id="8a019-109">Après le 8 février, l’extension Microsoft Pay ne sera plus disponible dans [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="8a019-109">After February 8, the Microsoft Pay extension will no longer be available in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span><br /></br>
>
> <span data-ttu-id="8a019-110">Les modifications affectent les versions suivantes de Business Central :</span><span class="sxs-lookup"><span data-stu-id="8a019-110">The changes impact the following versions of Business Central:</span></span>
> - <span data-ttu-id="8a019-111">Microsoft Dynamics 365 Business Central, octobre 2018</span><span class="sxs-lookup"><span data-stu-id="8a019-111">Microsoft Dynamics 365 Business Central October 2018</span></span>
> - <span data-ttu-id="8a019-112">Microsoft Dynamics 365 Business Central, avril 2019</span><span class="sxs-lookup"><span data-stu-id="8a019-112">Microsoft Dynamics 365 Business Central April 2019</span></span>
> - <span data-ttu-id="8a019-113">Microsoft Dynamics 365 Business Central, deuxième vague de publication 2019</span><span class="sxs-lookup"><span data-stu-id="8a019-113">Microsoft Dynamics 365 Business Central 2019 Release Wave 2</span></span>

<span data-ttu-id="8a019-114">Les clients sont toujours plus exigeants en ce qui concerne le service clientèle, en termes de qualité des produits mais aussi en termes de services de livraison et de paiement.</span><span class="sxs-lookup"><span data-stu-id="8a019-114">Customers continuously require higher customer service, both in terms of the quality of product but also in terms of delivery and payment services.</span></span> <span data-ttu-id="8a019-115">Le service Microsoft Pay vous aide à développer votre service clientèle.</span><span class="sxs-lookup"><span data-stu-id="8a019-115">The Microsoft Pay service helps you increase your customer service.</span></span>

<span data-ttu-id="8a019-116">L’extension Microsoft Pay ajoute un lien Microsoft Pay à vos documents de vente afin que les clients peuvent facilement effectuer des paiements à l’aide de Microsoft Pay.</span><span class="sxs-lookup"><span data-stu-id="8a019-116">The Microsoft Pay extension adds a Microsoft Pay link to your sales documents so customers can easily pay using Microsoft Pay.</span></span> <span data-ttu-id="8a019-117">Vous pouvez alors envoyer les documents par e-mail pour fournir un meilleure service client et raccourcir le temps nécessaire pour que les paiements des clients parviennent sur votre compte bancaire.</span><span class="sxs-lookup"><span data-stu-id="8a019-117">Then you can send the documents by email to provide higher customer service and shorten the time it takes for customers’ payments to arrive on your bank account.</span></span>

<span data-ttu-id="8a019-118">L’extension Microsoft Pay offre les avantages suivants :</span><span class="sxs-lookup"><span data-stu-id="8a019-118">The Microsoft Pay extension provides the following benefits:</span></span>
- <span data-ttu-id="8a019-119">Les paiements client apparaissent plus rapidement sur votre compte bancaire.</span><span class="sxs-lookup"><span data-stu-id="8a019-119">Customer payments appear faster on your bank account.</span></span>
- <span data-ttu-id="8a019-120">Les clients disposent de davantage de méthodes de paiement de leurs factures.</span><span class="sxs-lookup"><span data-stu-id="8a019-120">Customers have more ways to pay invoices.</span></span>
- <span data-ttu-id="8a019-121">Microsoft Pay offre un service de paiement fiable, que les clients apprécient plutôt que de devoir saisir leurs données de carte de crédit sur des sites Web inconnus.</span><span class="sxs-lookup"><span data-stu-id="8a019-121">Microsoft Pay offers a trustworthy payment service, which customers prefer to entering credit card information on unknown web sites.</span></span>
- <span data-ttu-id="8a019-122">Microsoft Pay propose plusieurs méthodes de gestion des paiements, y compris le traitement de cartes de crédit, comme PayPal et Stripe.</span><span class="sxs-lookup"><span data-stu-id="8a019-122">Microsoft Pay offers multiple ways of handling payments, including credit card processing, such as PayPal and Stripe.</span></span>
- <span data-ttu-id="8a019-123">Le lien Microsoft Pay peut être incorporé automatiquement ou par l’utilisateur sur chaque document facture.</span><span class="sxs-lookup"><span data-stu-id="8a019-123">The Microsoft Pay link can be embedded automatically on every invoice document or by the user.</span></span>
- <span data-ttu-id="8a019-124">Comme cette fonctionnalité est conçus comme une extension, elle vous donne le contrôle complet et vous permet de l’activer quand et si vos processus d’entreprise le nécessitent.</span><span class="sxs-lookup"><span data-stu-id="8a019-124">Because this functionality is built as an extension, it gives you full control to enable it when and if your business processes require it.</span></span>

<span data-ttu-id="8a019-125">L’activation des extensions de service de paiement est gratuite dans [!INCLUDE[prod_short](includes/prod_short.md)], toutefois, vous devez contacter le service de paiement pour obtenir un compte.</span><span class="sxs-lookup"><span data-stu-id="8a019-125">Enabling payment service extensions is free in [!INCLUDE[prod_short](includes/prod_short.md)], however, you will need to contact the payment service to get an account.</span></span> <span data-ttu-id="8a019-126">Pour plus d’informations, voir [Activer les paiements client via les services de paiement](sales-how-enable-payment-service-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="8a019-126">For more information, see [Enable Customer Payment Through Payment Services](sales-how-enable-payment-service-extensions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8a019-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a019-127">See Also</span></span>
<span data-ttu-id="8a019-128">[Personnalisation de [!INCLUDE[prod_short](includes/prod_short.md)] à l’aide des extensions](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="8a019-128">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="8a019-129">Définition des ventes</span><span class="sxs-lookup"><span data-stu-id="8a019-129">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="8a019-130">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8a019-130">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]