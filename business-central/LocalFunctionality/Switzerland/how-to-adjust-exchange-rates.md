---
title: 'Procédure : Ajuster les taux de change devise'
description: Si vous avez des ventes imposables en devise étrangère, vous devez utiliser le taux officiel pour la conversion de devise TVA telle que définie par l'administration fiscale.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 3662736f462e488d1ac2c42e2195accf4352dcff
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "937914"
---
# <a name="adjust-exchange-rates"></a><span data-ttu-id="171cd-103">Ajuster taux de change</span><span class="sxs-lookup"><span data-stu-id="171cd-103">Adjust Exchange Rates</span></span>
<span data-ttu-id="171cd-104">Si vous avez des ventes imposables en devise étrangère, vous devez utiliser le taux officiel pour la conversion de devise TVA telle que définie par l'administration fiscale.</span><span class="sxs-lookup"><span data-stu-id="171cd-104">If you have taxable sales in a foreign currency, you must use the official rate for VAT currency conversion as set by the Federal Tax Administration.</span></span>  

<span data-ttu-id="171cd-105">Si ces taux ne correspondent pas aux taux de change utilisés dans les factures d'achat ou de vente, vous devrez ultérieurement ajuster les taux de TVA à l'aide d'un traitement par lots.</span><span class="sxs-lookup"><span data-stu-id="171cd-105">If these rates do not match the currency rates used in the purchase or sales invoices, you will have to adjust the VAT rates with a batch job later.</span></span> <span data-ttu-id="171cd-106">Ces ajustements peuvent uniquement être exécutés en utilisant un taux de TVA autorisé.</span><span class="sxs-lookup"><span data-stu-id="171cd-106">These adjustments can only be run using an authorized VAT rate.</span></span>  

<span data-ttu-id="171cd-107">Vous pouvez exécuter ce traitement par lots aussi souvent que vous le souhaitez, cependant assurez-vous que vous l'exécutez toujours avant de créer une déclaration TVA.</span><span class="sxs-lookup"><span data-stu-id="171cd-107">You can run this batch job as often as you like, however make sure that you always run it before creating a VAT statement.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="171cd-108">Lorsque vous utilisez une devise report, assurez-vous que le champ **Ajustement tx de change TVA** dans la page **Paramètres comptabilité** est défini sur **Aucun ajustement**.</span><span class="sxs-lookup"><span data-stu-id="171cd-108">When using a report currency, make sure that the **VAT Exchange Rate Adjustment** field on the **General Ledger Setup** page is set to **No Adjustment**.</span></span>  

<span data-ttu-id="171cd-109">Pour plus d'informations sur la TVA et les devises étrangères, voir le site Web [ESTV](https://go.microsoft.com/fwlink/?LinkId=285999).</span><span class="sxs-lookup"><span data-stu-id="171cd-109">For more information about VAT and foreign currencies, see the [ESTV](https://go.microsoft.com/fwlink/?LinkId=285999) website.</span></span>  

## <a name="to-adjust-an-exchange-rate"></a><span data-ttu-id="171cd-110">Pour ajuster un taux de change</span><span class="sxs-lookup"><span data-stu-id="171cd-110">To adjust an exchange rate</span></span>  

1.  <span data-ttu-id="171cd-111">Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Devises**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="171cd-111">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currencies**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="171cd-112">Sélectionnez l'option **Taux de change**.</span><span class="sxs-lookup"><span data-stu-id="171cd-112">Choose the **Exch. Rates** action.</span></span>  
3.  <span data-ttu-id="171cd-113">Dans la page **Taux de change devise**, saisissez le taux de TVA officiel par période pour chaque devise dans les champs **Montant taux change TVA** et **Montant taux change TVA lié**.</span><span class="sxs-lookup"><span data-stu-id="171cd-113">On the **Currency Exchange Rates** page, enter the official VAT rate per period for each currency in the **VAT Exch. Rate Amount** and the **Relational VAT Exch. Rate Amt** fields.</span></span>  
4.  <span data-ttu-id="171cd-114">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="171cd-114">Choose the **OK** button.</span></span>  
5.  <span data-ttu-id="171cd-115">Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Ajuster taux de change**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="171cd-115">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Adjust Exchange Rates**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="171cd-116">Sous le raccourci **Options**, renseignez les champs comme indiqué dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="171cd-116">On the **Options** FastTab, fill in the fields as described in the following table.</span></span>   

    |<span data-ttu-id="171cd-117">Champ</span><span class="sxs-lookup"><span data-stu-id="171cd-117">Field</span></span>|<span data-ttu-id="171cd-118">Désignation</span><span class="sxs-lookup"><span data-stu-id="171cd-118">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="171cd-119">**Date début**</span><span class="sxs-lookup"><span data-stu-id="171cd-119">**Starting Date**</span></span>|<span data-ttu-id="171cd-120">Saisissez une date pour spécifier le début de la période pendant laquelle les écritures seront ajustées.</span><span class="sxs-lookup"><span data-stu-id="171cd-120">Enter a date to specify the beginning of the period for which entries will be adjusted.</span></span>|  
    |<span data-ttu-id="171cd-121">**Date fin**</span><span class="sxs-lookup"><span data-stu-id="171cd-121">**Ending Date**</span></span>|<span data-ttu-id="171cd-122">Saisissez la dernière date à laquelle les écritures seront ajustées.</span><span class="sxs-lookup"><span data-stu-id="171cd-122">Enter the last date for which entries will be adjusted.</span></span> <span data-ttu-id="171cd-123">Cette date est habituellement identique à la date du champ **Date comptabilisation**.</span><span class="sxs-lookup"><span data-stu-id="171cd-123">This date is typically the same as the posting date in the **Posting Date** field.</span></span>|  
    |<span data-ttu-id="171cd-124">**Ajuster taux de change TVA**</span><span class="sxs-lookup"><span data-stu-id="171cd-124">**Adjust VAT exch. rate**</span></span>|<span data-ttu-id="171cd-125">Indiquez si vous souhaitez ajuster le taux de change TVA.</span><span class="sxs-lookup"><span data-stu-id="171cd-125">Specify if you want to adjust the VAT exchange rate.</span></span>|  

7.  <span data-ttu-id="171cd-126">Pour démarrer le traitement par lots, cliquez sur le bouton **Imprimer**.</span><span class="sxs-lookup"><span data-stu-id="171cd-126">Choose the **Print** button to start the batch job.</span></span> <span data-ttu-id="171cd-127">Ce traitement par lots contrôle si les entrées de TVA doivent être ajustées et prépare une écriture d'ajustement pour chacune de ces écritures pour les comptes Ajustement de taux de change non réalisés/réalisés.</span><span class="sxs-lookup"><span data-stu-id="171cd-127">This batch job controls whether VAT entries have to be adjusted and prepares an adjusting entry for each of these entries for the Unrealized/Realized Exchange Rate Adjustment accounts.</span></span> <span data-ttu-id="171cd-128">Les écritures TVA existantes sont également corrigées.</span><span class="sxs-lookup"><span data-stu-id="171cd-128">The existing VAT entries are also corrected.</span></span>  

## <a name="see-also"></a><span data-ttu-id="171cd-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="171cd-129">See Also</span></span>  
 <span data-ttu-id="171cd-130">[Taxe sur la valeur ajoutée, Suisse](swiss-value-added-tax.md) </span><span class="sxs-lookup"><span data-stu-id="171cd-130">[Swiss Value Added Tax](swiss-value-added-tax.md) </span></span>  
 <span data-ttu-id="171cd-131">[Taux de TVA pour la Suisse](vat-rates-for-switzerland.md) </span><span class="sxs-lookup"><span data-stu-id="171cd-131">[VAT Rates for Switzerland](vat-rates-for-switzerland.md) </span></span>  
[<span data-ttu-id="171cd-132">Mettre à jour des taux de change devise</span><span class="sxs-lookup"><span data-stu-id="171cd-132">Update Currency Exchange Rates</span></span>](../../finance-how-update-currencies.md)  
[<span data-ttu-id="171cd-133">Configurer une devise report supplémentaire</span><span class="sxs-lookup"><span data-stu-id="171cd-133">Set Up an Additional Reporting Currency</span></span>](../../finance-how-setup-additional-currencies.md)
