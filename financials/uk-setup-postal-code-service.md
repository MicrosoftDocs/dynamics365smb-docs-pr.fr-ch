---
title: "Procédure : Configurer l'extension GetAddress.io UK Postcodes | Microsoft Docs"
description: "Décrit la fonctionnalité générale que vous utilisez pour interagir avec des données dans Financials, par exemple entrer les valeurs, trier les données, et modifier les vues."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: getaddress.io, postcodes, extension
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c5a99f7a90b2f832bba3eb088d0faa7514c14708
ms.contentlocale: fr-ch
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-set-up-the-getaddressio-uk-postcodes-extension"></a><span data-ttu-id="e3956-103">Procédure : Configurer l'extension GetAddress.io UK Postcodes</span><span class="sxs-lookup"><span data-stu-id="e3956-103">How to: Set Up the GetAddress.io UK Postcodes Extension</span></span>
<span data-ttu-id="e3956-104">Cette extension facilite la saisie des adresses au Royaume-Uni pour les entités comme les clients, les contacts, les salariés, les fournisseurs, les comptes bancaires, etc.</span><span class="sxs-lookup"><span data-stu-id="e3956-104">This extension makes it easy to enter addresses in the UK for entities like customers, contacts, employees, vendors, bank accounts, and so on.</span></span> 

<span data-ttu-id="e3956-105">L'extension GetAddress.io UK Postcodes utilise l'API getAddress pour rechercher des adresses dans les codes postaux au Royaume-Uni.</span><span class="sxs-lookup"><span data-stu-id="e3956-105">The GetAddress.io UK Postcodes extension uses the getAddress API to find addresses in postcodes in the UK.</span></span> <span data-ttu-id="e3956-106">Pour utiliser l'extension, vous devez obtenir un plan et une clé API pour l'API getAddress.</span><span class="sxs-lookup"><span data-stu-id="e3956-106">To use the extension, you need to get a plan and an API Key for the getAddress API.</span></span> <span data-ttu-id="e3956-107">C'est facile, et nous pouvons vous aider à le faire lorsque vous configurez l'extension GetAddress.io UK Postcodes.</span><span class="sxs-lookup"><span data-stu-id="e3956-107">That's easy, and we help you do that when you set up the GetAddress.io UK Postcodes extension.</span></span> <span data-ttu-id="e3956-108">Les plans sont basés sur l'utilisation ou sur ce qui est parfois désigné sous le nom d'appels.</span><span class="sxs-lookup"><span data-stu-id="e3956-108">Plans are based on use, or what's sometimes referred to as calls.</span></span> <span data-ttu-id="e3956-109">Un appel, dans ce cas, a lieu lorsque [!INCLUDE[d365fin](includes/d365fin_md.md)] affiche la liste des adresses dans un code postal.</span><span class="sxs-lookup"><span data-stu-id="e3956-109">A call, in this case, is when [!INCLUDE[d365fin](includes/d365fin_md.md)] displays a list of addresses in a postcode.</span></span> <span data-ttu-id="e3956-110">Selon la fréquence à laquelle vous ajoutez des adresses, choisissez le plan qui vous convient le mieux.</span><span class="sxs-lookup"><span data-stu-id="e3956-110">Depending on how often you add addresses, choose the plan that is best for you.</span></span> <span data-ttu-id="e3956-111">Si vous choisissez **Obtenir clé API** dans la page, vous allez utiliser le plan **Libre**, qui vous permet d'ajouter 20 adresses par jour, et qui est valable 30 jours.</span><span class="sxs-lookup"><span data-stu-id="e3956-111">If you just choose **Get API Key** in the page, you'll use the **Free** plan, which lets you add 20 addresses per day, and is valid for 30 days.</span></span> 

##<a name="to-set-up-the-getaddressio-uk-postcodes-extension"></a><span data-ttu-id="e3956-112">Pour configurer l'extension GetAddress.io UK Postcodes</span><span class="sxs-lookup"><span data-stu-id="e3956-112">To set up the GetAddress.io UK Postcodes extension</span></span> 
1. <span data-ttu-id="e3956-113">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Connexions au service**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="e3956-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Connections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e3956-114">Dans la fenêtre **Connexions au service**, choisissez **Service code postal R-U**.</span><span class="sxs-lookup"><span data-stu-id="e3956-114">In the **Service Connections** window, choose **UK Postcode Service**.</span></span>
3. <span data-ttu-id="e3956-115">Dans la page **Configuration fournisseur code postal**, choisissez **Désactivé**.</span><span class="sxs-lookup"><span data-stu-id="e3956-115">In the **Postcode provider configuration** page, choose **Disabled**.</span></span>
4. <span data-ttu-id="e3956-116">Dans la fenêtre **Sélection du service de code postal**, choisissez **GetAddress.io**.</span><span class="sxs-lookup"><span data-stu-id="e3956-116">In the **Postal code service selection** window, choose **GetAddress.io**.</span></span>
5. <span data-ttu-id="e3956-117">Dans la fenêtre **GetAddress.io Config**, choisissez **Obtenir clé API** pour ouvrir la page **Plans** sur le site Web pour obtenir l'API getAddress.</span><span class="sxs-lookup"><span data-stu-id="e3956-117">In the **GetAddress.io Config** window, choose **Get API Key** to open the **Plans** page on the website for the getAddress API.</span></span>  

    > [!NOTE]  
>   <span data-ttu-id="e3956-118">Vous pouvez être amené à autoriser les messages contextuels dans votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="e3956-118">You might need to allow pop-ups in your browser.</span></span>
6. <span data-ttu-id="e3956-119">Vous pouvez acheter un plan ou simplement choisir **Obtenir clé API**, et fournir ensuite votre adresse e-mail.</span><span class="sxs-lookup"><span data-stu-id="e3956-119">Purchase a plan, or just choose **Get API Key**, and then provide your email address.</span></span>
7. <span data-ttu-id="e3956-120">Ouvrez l'e-mail à partir de getAddress.io, et copiez la clé d'API.</span><span class="sxs-lookup"><span data-stu-id="e3956-120">Open the email from getAddress.io, and copy the API key.</span></span> <span data-ttu-id="e3956-121">La clé se trouve sous l'en-tête **Votre clé API**.</span><span class="sxs-lookup"><span data-stu-id="e3956-121">The key is under the **Your API Key** heading.</span></span>
8. <span data-ttu-id="e3956-122">Dans la fenêtre **GetAddress.io Config**, collez la clé API dans le champ **Clé API** et choisissez **OK**.</span><span class="sxs-lookup"><span data-stu-id="e3956-122">In the **GetAddress.io Config** window, paste the API key in the **API Key** field, and then choose **OK**.</span></span>
9. <span data-ttu-id="e3956-123">Dans la page **Connexions au service**, vérifiez que le champ **Fournisseur adresse** contient bien **GetAddress.io**.</span><span class="sxs-lookup"><span data-stu-id="e3956-123">In the **Service Connections** page, verify that the **Address Provider** field shows **GetAddress.io**.</span></span> <span data-ttu-id="e3956-124">Si c'est le cas, le service est activé.</span><span class="sxs-lookup"><span data-stu-id="e3956-124">If it does, the service is enabled.</span></span>

## <a name="see-also"></a><span data-ttu-id="e3956-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3956-125">See Also</span></span>
<span data-ttu-id="e3956-126">[GetAddress.io UK Postcodes](ui-extensions-getaddressio.md)
[Personnalisatoin de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide d'extensions](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="e3956-126">[GetAddress.io UK Postcodes](ui-extensions-getaddressio.md)
[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="e3956-127">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e3956-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
