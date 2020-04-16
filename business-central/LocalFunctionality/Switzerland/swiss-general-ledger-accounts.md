---
title: Comptes généraux, Suisse
description: Les améliorations suisses comprennent des fonctions spéciales liées aux comptes généraux.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: a0e79bf9880a627d2f6707da6b69c1610d54a91f
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3189085"
---
# <a name="swiss-general-ledger-accounts"></a><span data-ttu-id="f0a0f-103">Comptes généraux, Suisse</span><span class="sxs-lookup"><span data-stu-id="f0a0f-103">Swiss General Ledger Accounts</span></span>
[!INCLUDE[d365fin](../../includes/d365fin_md.md)] <span data-ttu-id="f0a0f-104">inclut les améliorations suisses apportées aux fonctions spéciales liées aux comptes généraux.</span><span class="sxs-lookup"><span data-stu-id="f0a0f-104">includes Swiss enhancements to general ledger accounts.</span></span>

- <span data-ttu-id="f0a0f-105">Conserver les soldes en devises d'un compte bancaire dans les comptes généraux.</span><span class="sxs-lookup"><span data-stu-id="f0a0f-105">Maintain the foreign currency balances of a bank account in the general ledger.</span></span>  
- <span data-ttu-id="f0a0f-106">Trier les numéros de comptes généraux dans la page **Plan comptable**.</span><span class="sxs-lookup"><span data-stu-id="f0a0f-106">Sort general ledger account numbers on the **Chart of Accounts** page.</span></span>  
- <span data-ttu-id="f0a0f-107">Prévisualiser les effets que la validation des feuilles comptabilité auraient sur les soldes de certains comptes généraux avant leur validation réelle.</span><span class="sxs-lookup"><span data-stu-id="f0a0f-107">Preview the effects that posting general journals would have on the balances of certain general ledger accounts before actually posting them.</span></span>  

## <a name="general-ledger-accounts-and-general-journals"></a><span data-ttu-id="f0a0f-108">Comptes généraux et feuilles comptabilité</span><span class="sxs-lookup"><span data-stu-id="f0a0f-108">General Ledger Accounts and General Journals</span></span>  
<span data-ttu-id="f0a0f-109">Les entreprises ont souvent des comptes bancaires différents pour les devises étrangères et disposent d'un compte général pour chaque compte bancaire.</span><span class="sxs-lookup"><span data-stu-id="f0a0f-109">Companies often have different bank accounts for foreign currencies, and have a general ledger account for each bank account.</span></span> <span data-ttu-id="f0a0f-110">Dans [!INCLUDE[d365fin](../../includes/d365fin_md.md)], vous pouvez définir un code devise et les informations de solde en devise étrangère dans la page **Plan comptable**.</span><span class="sxs-lookup"><span data-stu-id="f0a0f-110">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can set up currency code and foreign currency balance information on the **Chart of Accounts** page.</span></span> <span data-ttu-id="f0a0f-111">Cela vous permet de conserver le solde de départ en devises d'un compte bancaire.</span><span class="sxs-lookup"><span data-stu-id="f0a0f-111">This allows you to maintain the original foreign currency balance of a bank account.</span></span> <span data-ttu-id="f0a0f-112">Pour plus d'informations, voir [Description des écritures comptables et du plan comptable](../../finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="f0a0f-112">For more information, see [Understanding the General Ledger and the COA](../../finance-general-ledger.md).</span></span>  

<span data-ttu-id="f0a0f-113">Par exemple, une société a deux comptes bancaires : une pour la devise société (DS) et une pour les euros (EUR).</span><span class="sxs-lookup"><span data-stu-id="f0a0f-113">For example, a company has two bank accounts: one for local currency (LCY) and one for euros (EUR).</span></span> <span data-ttu-id="f0a0f-114">Vous devez créer des écritures comptables pour chaque compte bancaire.</span><span class="sxs-lookup"><span data-stu-id="f0a0f-114">You must create a general ledger account for each bank account.</span></span> <span data-ttu-id="f0a0f-115">Pour le compte en euros, définissez le code devise **EUR** et validez les feuilles en EUR ou DS.</span><span class="sxs-lookup"><span data-stu-id="f0a0f-115">For the EUR account, define the currency code as **EUR** and post journals in EUR or LCY.</span></span>  

<span data-ttu-id="f0a0f-116">Lorsque le taux de change pour EUR et DS change, vous pouvez mettre à jour et ajuster le solde de la devise locale pour le grand livre EUR à l'aide du traitement par lots Ajuster taux de change.</span><span class="sxs-lookup"><span data-stu-id="f0a0f-116">When the exchange rate for EUR and LCY changes, you can update and adjust the local currency balance for the EUR general ledger account using the adjust exchange rates batch job.</span></span> <span data-ttu-id="f0a0f-117">Ce traitement par lots crée et valide des écritures d'ajustement de devise dans le grand livre et met à jour le solde DS.</span><span class="sxs-lookup"><span data-stu-id="f0a0f-117">This batch job creates and posts currency adjustment entries to the general ledger and updates the LCY balance.</span></span>  

## <a name="data-type-for-general-ledger-accounts"></a><span data-ttu-id="f0a0f-118">Type de données pour les comptes du grand livre général</span><span class="sxs-lookup"><span data-stu-id="f0a0f-118">Data Type for General Ledger Accounts</span></span>  
<span data-ttu-id="f0a0f-119">Le type de données est défini en texte pour le numéro de compte du grand livre général ou le code de compte afin de prendre en charge les exigences de tri pour le plan comptable standardisé Swiss Kontenrahmen Käfer (KMU).</span><span class="sxs-lookup"><span data-stu-id="f0a0f-119">The data type is set to text for the general ledger account number or account code to support the sorting requirements for the standardized Swiss Kontenrahmen Käfer (KMU) common chart of accounts.</span></span> <span data-ttu-id="f0a0f-120">La liste des numéros de compte est triée selon le type de données de texte.</span><span class="sxs-lookup"><span data-stu-id="f0a0f-120">The account numbers list is sorted based on the text data type.</span></span> <span data-ttu-id="f0a0f-121">Le plan comptable KMU indique les numéros de compte suivants :</span><span class="sxs-lookup"><span data-stu-id="f0a0f-121">The KMU chart of accounts contains the following account numbers:</span></span>  

- <span data-ttu-id="f0a0f-122">1176</span><span class="sxs-lookup"><span data-stu-id="f0a0f-122">1176</span></span>  
- <span data-ttu-id="f0a0f-123">119.0</span><span class="sxs-lookup"><span data-stu-id="f0a0f-123">119.0</span></span>  
- <span data-ttu-id="f0a0f-124">1190</span><span class="sxs-lookup"><span data-stu-id="f0a0f-124">1190</span></span>  

## <a name="viewing-temporary-balances-in-general-journals"></a><span data-ttu-id="f0a0f-125">Affichage des soldes temporaires dans les feuilles comptabilité</span><span class="sxs-lookup"><span data-stu-id="f0a0f-125">Viewing Temporary Balances in General Journals</span></span>  
<span data-ttu-id="f0a0f-126">Avant de valider une feuille comptabilité, vous pouvez prévisualiser l'effet que cette validation aurait sur les soldes de certains comptes généraux.</span><span class="sxs-lookup"><span data-stu-id="f0a0f-126">Before posting a general journal you can preview the effect that posting would have on the balances of certain general ledger accounts.</span></span> <span data-ttu-id="f0a0f-127">Vous pouvez ouvrir une page de statistiques qui affiche les soldes des comptes et les soldes des lignes actives qui incluaient les valeurs non intégrées pour le journal en cours.</span><span class="sxs-lookup"><span data-stu-id="f0a0f-127">You can open a statistics page that shows the balances of the accounts, and the balances of the active lines that included the unposted values for the current journal.</span></span> <span data-ttu-id="f0a0f-128">Pour plus d'informations, voir [Affichage des soldes temporaires dans les feuilles comptabilisation immobilisation](how-to-view-temporary-balances-in-general-ledger-journals.md).</span><span class="sxs-lookup"><span data-stu-id="f0a0f-128">For more information, see [View Temporary Balances in General Ledger Journals](how-to-view-temporary-balances-in-general-ledger-journals.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="f0a0f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0a0f-129">See Also</span></span>

[<span data-ttu-id="f0a0f-130">Afficher les soldes temporaires dans les feuilles comptabilisation immobilisation</span><span class="sxs-lookup"><span data-stu-id="f0a0f-130">View Temporary Balances in General Ledger Journals</span></span>](how-to-view-temporary-balances-in-general-ledger-journals.md)  
[<span data-ttu-id="f0a0f-131">Fonctionnalité locale, Suisse</span><span class="sxs-lookup"><span data-stu-id="f0a0f-131">Switzerland Local Functionality</span></span>](switzerland-local-functionality.md)  
