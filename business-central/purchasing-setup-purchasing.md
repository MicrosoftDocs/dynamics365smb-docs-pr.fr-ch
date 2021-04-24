---
title: Aperçu des tâches permettant de paramétrer vos achats | Microsoft Docs
description: Décrit les tâches permettant de définir les stratégies d’approvisionnement de votre société et de déterminer vos processus d’achat.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement, supply, vendor order
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 81bbb013cba1039bfe6bb76e8489d5b8ed7c9831
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772519"
---
# <a name="setting-up-purchasing"></a><span data-ttu-id="5afc5-103">Définition des achats</span><span class="sxs-lookup"><span data-stu-id="5afc5-103">Setting Up Purchasing</span></span>
<span data-ttu-id="5afc5-104">Avant de pouvoir gérer les processus achat, vous devez configurer les règles et valeurs qui définissent les stratégies d’achat de la société.</span><span class="sxs-lookup"><span data-stu-id="5afc5-104">Before you can manage purchase processes, you must configure the rules and values that define the company's purchase policies.</span></span>

<span data-ttu-id="5afc5-105">Vous devez définir la configuration générale, notamment les documents achat requis et le mode de validation des valeurs correspondantes.</span><span class="sxs-lookup"><span data-stu-id="5afc5-105">You must define the general setup, such as which purchase documents are required and how their values are posted.</span></span> <span data-ttu-id="5afc5-106">Celle-ci a généralement lieu une seule fois au cours de la phase initiale de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="5afc5-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="5afc5-107">Une série de tâches distincte en relation avec l’enregistrement de nouveaux fournisseurs consiste à enregistrer les prix spéciaux ou les accords de remise établis avec chaque fournisseur.</span><span class="sxs-lookup"><span data-stu-id="5afc5-107">A separate series of tasks related to registering new vendors is to record any special price or discount agreements that you have with each vendor.</span></span>

<span data-ttu-id="5afc5-108">Les configurations relatives à la finance, telles que les modes de règlement et les devises, sont traitées dans la section Paramètres financiers.</span><span class="sxs-lookup"><span data-stu-id="5afc5-108">Finance-related purchase setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="5afc5-109">Pour plus d’informations, reportez-vous à [Configuration de Finance](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="5afc5-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="5afc5-110">Pour</span><span class="sxs-lookup"><span data-stu-id="5afc5-110">To</span></span> | <span data-ttu-id="5afc5-111">Voir</span><span class="sxs-lookup"><span data-stu-id="5afc5-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="5afc5-112">Créer une fiche fournisseur pour chaque fournisseur auquel vous achetez des biens</span><span class="sxs-lookup"><span data-stu-id="5afc5-112">Create a vendor card for each vendor that you purchase from</span></span>|[<span data-ttu-id="5afc5-113">Enregistrer un nouveau fournisseur</span><span class="sxs-lookup"><span data-stu-id="5afc5-113">Register New Vendors</span></span>](purchasing-how-register-new-vendors.md) |
| <span data-ttu-id="5afc5-114">Entrer les différents remises et prix spéciaux que vous accordent les fournisseurs en fonction de l’article, des quantités et/ou de la date</span><span class="sxs-lookup"><span data-stu-id="5afc5-114">Enter the different discounts and special prices that vendors grant you depending on item, quantities, and/or date</span></span> |[<span data-ttu-id="5afc5-115">Enregistrer des accords sur les prix d’achat, les remises et les paiements</span><span class="sxs-lookup"><span data-stu-id="5afc5-115">Record Purchase Price, Discount, and Payment Agreements</span></span>](purchasing-how-record-purchase-price-discount-payment-agreements.md) |
| <span data-ttu-id="5afc5-116">Octroyer une priorité aux fournisseurs</span><span class="sxs-lookup"><span data-stu-id="5afc5-116">Prioritize vendors</span></span> |[<span data-ttu-id="5afc5-117">Octroyer une priorité aux fournisseurs</span><span class="sxs-lookup"><span data-stu-id="5afc5-117">Prioritize Vendors</span></span>](purchasing-how-prioritize-vendors.md) |
| <span data-ttu-id="5afc5-118">Configurer les acheteurs</span><span class="sxs-lookup"><span data-stu-id="5afc5-118">Set up purchasers</span></span> |[<span data-ttu-id="5afc5-119">Configurer les acheteurs</span><span class="sxs-lookup"><span data-stu-id="5afc5-119">Set Up Purchasers</span></span>](purchasing-how-setup-purchasers.md) |
|<span data-ttu-id="5afc5-120">Spécifiez les états par défaut à utiliser pour différents types de documents.</span><span class="sxs-lookup"><span data-stu-id="5afc5-120">Specify default reports to be used for different document types.</span></span>|[<span data-ttu-id="5afc5-121">Sélection des états dans Business Central</span><span class="sxs-lookup"><span data-stu-id="5afc5-121">Report Selection in Business Central</span></span>](across-report-selections.md)|

> [!TIP]
> <span data-ttu-id="5afc5-122">En fonction de votre emplacement géographique, certaines pages peuvent contenir des champs qui ne sont pas décrits dans les articles répertoriés ici, car ils s’appliquent à des fonctionnalités locales ou à des personnalisations.</span><span class="sxs-lookup"><span data-stu-id="5afc5-122">Depending on your geographical location, some pages can contain fields that are not described in the articles that are listed here because they apply to local functionality or customizations.</span></span> [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="5afc5-123">Voir la formation associée sur [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="5afc5-123">See Related Training at [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="5afc5-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5afc5-124">See Also</span></span>

[<span data-ttu-id="5afc5-125">Achats</span><span class="sxs-lookup"><span data-stu-id="5afc5-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="5afc5-126">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5afc5-126">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]