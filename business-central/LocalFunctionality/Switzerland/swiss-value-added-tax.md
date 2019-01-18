---
title: "Taxe sur la valeur ajoutée, Suisse"
description: "Les améliorations comprennent les fonctions spéciales de déclaration de TVA en Suisse."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/15/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 7db6bce91246e2b76240f6641790ff44294c3522
ms.contentlocale: fr-ch
ms.lasthandoff: 11/26/2018

---
# <a name="swiss-value-added-tax"></a><span data-ttu-id="a179c-103">Taxe sur la valeur ajoutée, Suisse</span><span class="sxs-lookup"><span data-stu-id="a179c-103">Swiss Value Added Tax</span></span>
[!INCLUDE[d365fin](../../includes/d365fin_md.md)] <span data-ttu-id="a179c-104">inclut les améliorations suivantes à la déclaration de TVA en Suisse :</span><span class="sxs-lookup"><span data-stu-id="a179c-104">includes the following enhancements to Swiss VAT reporting:</span></span>  

- <span data-ttu-id="a179c-105">Ajustement automatique des montants de TVA pour les factures, en fonction des comptes.</span><span class="sxs-lookup"><span data-stu-id="a179c-105">Automatic adjustment of VAT amounts for invoices, according to payment discounts.</span></span>  
- <span data-ttu-id="a179c-106">Taux de change de la TVA supplémentaires pour les factures en devises étrangères.</span><span class="sxs-lookup"><span data-stu-id="a179c-106">Additional VAT exchange rates for invoices in foreign currencies.</span></span>  

<span data-ttu-id="a179c-107">Pour plus d'informations sur la déclaration et les exigences de codage de TVA en Suisse, voir [Informations sur la TVA en Suisse](https://www.estv.admin.ch/estv/en/home/estv-suissetax/sw-hersteller.html).</span><span class="sxs-lookup"><span data-stu-id="a179c-107">For more information about Swiss VAT reporting and coding requirements, see [Swiss VAT Information](https://www.estv.admin.ch/estv/en/home/estv-suissetax/sw-hersteller.html).</span></span> <span data-ttu-id="a179c-108">Ces informations sont disponibles en français, allemand et italien.</span><span class="sxs-lookup"><span data-stu-id="a179c-108">The information is available in French, German, and Italian.</span></span>  

## <a name="vat-amounts-and-vat-exchange-rates"></a><span data-ttu-id="a179c-109">Montants TVA et taux de change TVA</span><span class="sxs-lookup"><span data-stu-id="a179c-109">VAT Amounts and VAT Exchange Rates</span></span>  
<span data-ttu-id="a179c-110">Conformément aux lois locales sur la TVA, le montant de base de TVA pour une facture peut être réduit de l'escompte accordé si une remise est accordée.</span><span class="sxs-lookup"><span data-stu-id="a179c-110">According to local VAT laws, the VAT base amount for an invoice can be reduced by the payment discount if a discount is granted.</span></span> <span data-ttu-id="a179c-111">Pour autoriser l'ajustement automatique de TVA pour un escompte sur une facture, le champ **Ajuster pour escompte** est activé par défaut dans la page **Paramètres comptabilité**.</span><span class="sxs-lookup"><span data-stu-id="a179c-111">To allow automatic VAT adjustment for a payment discount on an invoice, the **Adjust for Payment Discount** field is activated by default on the **General Ledger Setup** page.</span></span> <span data-ttu-id="a179c-112">Vous pouvez également activer cette fonction dans les paramètres comptabilisation TVA.</span><span class="sxs-lookup"><span data-stu-id="a179c-112">You can also activate this function in the VAT posting setup.</span></span> <span data-ttu-id="a179c-113">Pour plus d'informations, voir la table Paramètres comptabilité et la table Paramètres comptabilisation TVA.</span><span class="sxs-lookup"><span data-stu-id="a179c-113">For more information, see the General Ledger Setup table and the VAT Posting Setup table.</span></span>  

### <a name="currency-exchange-rates-for-vat-reporting"></a><span data-ttu-id="a179c-114">Taux de change pour la déclaration de la TVA</span><span class="sxs-lookup"><span data-stu-id="a179c-114">Currency Exchange Rates for VAT Reporting</span></span>  
<span data-ttu-id="a179c-115">Pour les factures en devise étrangère, vous devez utiliser le taux de change fourni par le gouvernement pour le calcul de la TVA proprement dit.</span><span class="sxs-lookup"><span data-stu-id="a179c-115">For invoices in foreign currency, you must use the official exchange rate provided by the government for the VAT calculation itself.</span></span> <span data-ttu-id="a179c-116">Vous pouvez également définir des taux de change supplémentaires pour la TVA, que vous pouvez utiliser pour d'autres aspects de la facture que le calcul de la TVA.</span><span class="sxs-lookup"><span data-stu-id="a179c-116">You can also set up additional exchange rates for VAT, which you can use for aspects of the invoice other than the VAT calculation.</span></span> <span data-ttu-id="a179c-117">Vous pouvez indiquer le taux de change de TVA gouvernemental correct pour chaque devise étrangère pertinente dans la configuration du taux de change pour les factures.</span><span class="sxs-lookup"><span data-stu-id="a179c-117">You can provide the correct government VAT exchange rate for each relevant foreign currency in the exchange rate setup for invoices.</span></span> <span data-ttu-id="a179c-118">Pour plus d'informations, voir la table Taux de change devise.</span><span class="sxs-lookup"><span data-stu-id="a179c-118">For more information, see the Currency Exchange Rate table.</span></span>  

<span data-ttu-id="a179c-119">Vous pouvez ajuster tous les montants TVA dans les écritures TVA qui résultent des transactions en devise étrangère.</span><span class="sxs-lookup"><span data-stu-id="a179c-119">You can also adjust all VAT amounts in VAT entries that result from foreign currency transactions.</span></span> <span data-ttu-id="a179c-120">Lorsque vous activez la fonction Ajuster le taux de change de la TVA, les taux de change de la TVA sont ajustés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="a179c-120">When you activate the adjust VAT exchange rate function, VAT exchange rates are adjusted automatically.</span></span> <span data-ttu-id="a179c-121">Les différences positives qui résultent des taux de change sont validées dans les comptes de gain de change.</span><span class="sxs-lookup"><span data-stu-id="a179c-121">The positive differences that result from exchange rates are posted to exchange rate gain accounts.</span></span> <span data-ttu-id="a179c-122">Les différences négatives qui résultent des taux de change sont validées dans les comptes de perte de change.</span><span class="sxs-lookup"><span data-stu-id="a179c-122">The negative differences that result from exchange rates are posted to exchange rate loss accounts.</span></span> <span data-ttu-id="a179c-123">Pour plus d'informations, reportez-vous au traitement par lots Ajuster taux de change.</span><span class="sxs-lookup"><span data-stu-id="a179c-123">For more information, see the Adjust Exchange Rates batch job.</span></span>  

<span data-ttu-id="a179c-124">Des informations supplémentaires, telles que le taux de TVA et le montant en devise d'origine, sont transférées vers les écritures de TVA.</span><span class="sxs-lookup"><span data-stu-id="a179c-124">Additional information, such as VAT rate and original currency amount, is transferred to the VAT entries.</span></span> <span data-ttu-id="a179c-125">Pour plus d'informations, voir la table Écriture TVA.</span><span class="sxs-lookup"><span data-stu-id="a179c-125">For more information, see the VAT Entry table.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a179c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a179c-126">See Also</span></span>  
 <span data-ttu-id="a179c-127">[Taux de TVA pour la Suisse](vat-rates-for-switzerland.md) </span><span class="sxs-lookup"><span data-stu-id="a179c-127">[VAT Rates for Switzerland](vat-rates-for-switzerland.md) </span></span>  
 <span data-ttu-id="a179c-128">[Créer et imprimer une déclaration de TVA, Suisse](how-to-create-and-print-a-swiss-vat-statement.md) </span><span class="sxs-lookup"><span data-stu-id="a179c-128">[Create and Print a Swiss VAT Statement](how-to-create-and-print-a-swiss-vat-statement.md) </span></span>  
 [<span data-ttu-id="a179c-129">Fonctionnalité locale, Suisse</span><span class="sxs-lookup"><span data-stu-id="a179c-129">Switzerland Local Functionality</span></span>](switzerland-local-functionality.md)   

