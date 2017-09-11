---
title: "Mise à jour des taux de change des devises| Microsoft Docs"
description: "Pour utiliser plusieurs devises dans votre société, vous pouvez définir un code pour chaque devise et utiliser un service externe de taux de change, par exemple Yahoo."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, Yahoo
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: cc60569091b3aa37d17e981f1fae8f46c4a004df
ms.contentlocale: fr-ch
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-update-currency-exchange-rates"></a><span data-ttu-id="c939a-103">Procédure : mettre à jour les taux de change des devises</span><span class="sxs-lookup"><span data-stu-id="c939a-103">How to: Update Currency Exchange Rates</span></span>
<span data-ttu-id="c939a-104">Vous devez définir un code pour chaque devise utilisée si vous achetez ou vendez dans des devises différentes de votre devise locale, si vous disposez de comptes client ou fournisseur dans d'autres devises, ou si vous enregistrez des transactions comptables dans des devises différentes.</span><span class="sxs-lookup"><span data-stu-id="c939a-104">You must set up a code for each currency you use if you buy or sell in currencies other than your local currency, have receivables or payables in other currencies, or record G/L transactions in different currencies.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="c939a-105">Cette fonctionnalité nécessite que votre expérience soit définie sur **Suite**.</span><span class="sxs-lookup"><span data-stu-id="c939a-105">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="c939a-106">Pour plus d'informations, voir [Personnalisation de votre expérience [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="c939a-106">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

<span data-ttu-id="c939a-107">Vous pouvez utiliser un service externe pour tenir vos taux de change des devises à jour.</span><span class="sxs-lookup"><span data-stu-id="c939a-107">You can use an external service to keep your currency exchange rates up to date.</span></span> <span data-ttu-id="c939a-108">Le service Configuration des taux de change devise Yahoo est préinstallé et prêt à être activé.</span><span class="sxs-lookup"><span data-stu-id="c939a-108">The Yahoo Currency Exchange Rates service is preinstalled and ready to enable.</span></span>

## <a name="to-set-up-a-currency-exchange-rate-service"></a><span data-ttu-id="c939a-109">Configurer un service de taux de change des devises</span><span class="sxs-lookup"><span data-stu-id="c939a-109">To set up a currency exchange rate service</span></span>
1. <span data-ttu-id="c939a-110">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Services de taux de change devise**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="c939a-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currency Exchange Rate Services**, and then choose the related link.</span></span>
2. <span data-ttu-id="c939a-111">Sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="c939a-111">Choose the **New** action.</span></span>
3. <span data-ttu-id="c939a-112">Dans la fenêtre **Service de taux de change devise**, renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="c939a-112">In the **Currency Exchange Rate Service** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="c939a-113">Activez la case à cocher **Activé** pour activer le service.</span><span class="sxs-lookup"><span data-stu-id="c939a-113">Choose the **Enabled** check box to enable the service.</span></span>

## <a name="to-update-currency-exchange-rates-through-a-service"></a><span data-ttu-id="c939a-114">Pour mettre à jour les taux de change des devises à partir d'un service</span><span class="sxs-lookup"><span data-stu-id="c939a-114">To update currency exchange rates through a service</span></span>
1. <span data-ttu-id="c939a-115">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Devises**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="c939a-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currencies**, and then choose the related link.</span></span>
2. <span data-ttu-id="c939a-116">Choisissez l'option **Mettre à jour les taux de change**.</span><span class="sxs-lookup"><span data-stu-id="c939a-116">Choose the **Update Exchange Rates** action.</span></span>

<span data-ttu-id="c939a-117">La valeur dans le champ **Taux de change** de la fenêtre **Devises** est mise à jour avec le dernier taux de change des devises.</span><span class="sxs-lookup"><span data-stu-id="c939a-117">The value in the **Exchange Rate** field in the **Currencies** window is updated with the latest currency exchange rate.</span></span>

## <a name="see-also"></a><span data-ttu-id="c939a-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c939a-118">See Also</span></span>
[<span data-ttu-id="c939a-119">Clôture des exercices et des périodes</span><span class="sxs-lookup"><span data-stu-id="c939a-119">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="c939a-120">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c939a-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

