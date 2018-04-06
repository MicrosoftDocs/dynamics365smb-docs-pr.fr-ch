---
title: "Comptes généraux, Suisse"
description: "Les améliorations suisses comprennent des fonctions spéciales liées aux comptes généraux."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 96ab1080c5417ce1fc7721730963559cf7e90514
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="swiss-general-ledger-accounts"></a><span data-ttu-id="536fb-103">Comptes généraux, Suisse</span><span class="sxs-lookup"><span data-stu-id="536fb-103">Swiss General Ledger Accounts</span></span>
[!INCLUDE[d365fin](../../includes/d365fin_md.md)]<span data-ttu-id="536fb-104"> inclut les améliorations suisses apportées aux fonctions spéciales liées aux comptes généraux.</span><span class="sxs-lookup"><span data-stu-id="536fb-104"> includes Swiss enhancements to general ledger accounts.</span></span>

- <span data-ttu-id="536fb-105">Conserver les soldes en devises d'un compte bancaire dans les comptes généraux.</span><span class="sxs-lookup"><span data-stu-id="536fb-105">Maintain the foreign currency balances of a bank account in the general ledger.</span></span>  
- <span data-ttu-id="536fb-106">Trier les numéros de comptes généraux dans la fenêtre **Plan comptable**.</span><span class="sxs-lookup"><span data-stu-id="536fb-106">Sort general ledger account numbers in the **Chart of Accounts** window.</span></span>  
- <span data-ttu-id="536fb-107">Prévisualiser les effets que la validation des feuilles comptabilité auraient sur les soldes de certains comptes généraux avant leur validation réelle.</span><span class="sxs-lookup"><span data-stu-id="536fb-107">Preview the effects that posting general journals would have on the balances of certain general ledger accounts before actually posting them.</span></span>  

## <a name="general-ledger-accounts-and-general-journals"></a><span data-ttu-id="536fb-108">Comptes généraux et feuilles comptabilité</span><span class="sxs-lookup"><span data-stu-id="536fb-108">General Ledger Accounts and General Journals</span></span>  
<span data-ttu-id="536fb-109">Les entreprises ont souvent des comptes bancaires différents pour les devises étrangères et disposent d'un compte général pour chaque compte bancaire.</span><span class="sxs-lookup"><span data-stu-id="536fb-109">Companies often have different bank accounts for foreign currencies, and have a general ledger account for each bank account.</span></span> <span data-ttu-id="536fb-110">Dans [!INCLUDE[d365fin](../../includes/d365fin_md.md)], vous pouvez définir un code devise et les informations de solde en devise étrangère dans la fenêtre **Plan comptable**.</span><span class="sxs-lookup"><span data-stu-id="536fb-110">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can set up currency code and foreign currency balance information in the **Chart of Accounts** window.</span></span> <span data-ttu-id="536fb-111">Cela vous permet de conserver le solde de départ en devises d'un compte bancaire.</span><span class="sxs-lookup"><span data-stu-id="536fb-111">This allows you to maintain the original foreign currency balance of a bank account.</span></span> <span data-ttu-id="536fb-112">Pour plus d'informations, voir [Fenêtre Plan comptable](assetId:///fa407624-b670-44b6-8397-91aa606e4c39) et [Table Compte général](assetId:///a65c2b09-9bb2-43db-8c53-c047bfc49777).</span><span class="sxs-lookup"><span data-stu-id="536fb-112">For more information, see [Chart of Accounts Window](assetId:///fa407624-b670-44b6-8397-91aa606e4c39) and [G/L Account Table](assetId:///a65c2b09-9bb2-43db-8c53-c047bfc49777).</span></span>  

<span data-ttu-id="536fb-113">Par exemple, une société a deux comptes bancaires : une pour la devise société (DS) et une pour les euros (EUR).</span><span class="sxs-lookup"><span data-stu-id="536fb-113">For example, a company has two bank accounts: one for local currency (LCY) and one for euros (EUR).</span></span> <span data-ttu-id="536fb-114">Vous devez créer des écritures comptables pour chaque compte bancaire.</span><span class="sxs-lookup"><span data-stu-id="536fb-114">You must create a general ledger account for each bank account.</span></span> <span data-ttu-id="536fb-115">Pour le compte en euros, définissez le code devise **EUR** et validez les feuilles en EUR ou DS.</span><span class="sxs-lookup"><span data-stu-id="536fb-115">For the EUR account, define the currency code as **EUR** and post journals in EUR or LCY.</span></span>  

<span data-ttu-id="536fb-116">Lorsque le taux de change pour EUR et DS change, vous pouvez mettre à jour et ajuster le solde de la devise locale pour le grand livre EUR à l'aide du traitement par lots Ajuster taux de change.</span><span class="sxs-lookup"><span data-stu-id="536fb-116">When the exchange rate for EUR and LCY changes, you can update and adjust the local currency balance for the EUR general ledger account using the adjust exchange rates batch job.</span></span> <span data-ttu-id="536fb-117">Ce traitement par lots crée et valide des écritures d'ajustement de devise dans le grand livre et met à jour le solde DS.</span><span class="sxs-lookup"><span data-stu-id="536fb-117">This batch job creates and posts currency adjustment entries to the general ledger and updates the LCY balance.</span></span>  

## <a name="data-type-for-general-ledger-accounts"></a><span data-ttu-id="536fb-118">Type de données pour les comptes du grand livre général</span><span class="sxs-lookup"><span data-stu-id="536fb-118">Data Type for General Ledger Accounts</span></span>  
<span data-ttu-id="536fb-119">Le type de données est défini en texte pour le numéro de compte du grand livre général ou le code de compte afin de prendre en charge les exigences de tri pour le plan comptable standardisé Swiss Kontenrahmen Käfer (KMU).</span><span class="sxs-lookup"><span data-stu-id="536fb-119">The data type is set to text for the general ledger account number or account code to support the sorting requirements for the standardized Swiss Kontenrahmen Käfer (KMU) common chart of accounts.</span></span> <span data-ttu-id="536fb-120">Pour plus d'informations, reportez-vous à [Fenêtre Plan comptable](assetId:///fa407624-b670-44b6-8397-91aa606e4c39).</span><span class="sxs-lookup"><span data-stu-id="536fb-120">For more information, see [Chart of Accounts Window](assetId:///fa407624-b670-44b6-8397-91aa606e4c39).</span></span> <span data-ttu-id="536fb-121">La liste des numéros de compte est triée selon le type de données de texte.</span><span class="sxs-lookup"><span data-stu-id="536fb-121">The account numbers list is sorted based on the text data type.</span></span> <span data-ttu-id="536fb-122">Le plan comptable KMU indique les numéros de compte suivants :</span><span class="sxs-lookup"><span data-stu-id="536fb-122">The KMU chart of accounts contains the following account numbers:</span></span>  

- <span data-ttu-id="536fb-123">1176</span><span class="sxs-lookup"><span data-stu-id="536fb-123">1176</span></span>  
- <span data-ttu-id="536fb-124">119.0</span><span class="sxs-lookup"><span data-stu-id="536fb-124">119.0</span></span>  
- <span data-ttu-id="536fb-125">1190</span><span class="sxs-lookup"><span data-stu-id="536fb-125">1190</span></span>  

## <a name="viewing-temporary-balances-in-general-journals"></a><span data-ttu-id="536fb-126">Affichage des soldes temporaires dans les feuilles comptabilité</span><span class="sxs-lookup"><span data-stu-id="536fb-126">Viewing Temporary Balances in General Journals</span></span>  
<span data-ttu-id="536fb-127">Avant de valider une feuille comptabilité, vous pouvez prévisualiser l'effet que cette validation aurait sur les soldes de certains comptes généraux.</span><span class="sxs-lookup"><span data-stu-id="536fb-127">Before posting a general journal you can preview the effect that posting would have on the balances of certain general ledger accounts.</span></span> <span data-ttu-id="536fb-128">Vous pouvez ouvrir une fenêtre de statistiques qui affiche les soldes des comptes et les soldes des lignes actives qui incluaient les valeurs non intégrées pour le journal en cours.</span><span class="sxs-lookup"><span data-stu-id="536fb-128">You can open a statistics window that shows the balances of the accounts, and the balances of the active lines that included the unposted values for the current journal.</span></span> <span data-ttu-id="536fb-129">Pour plus d'informations, voir [Affichage des soldes temporaires dans les feuilles comptabilisation immobilisation](how-to-view-temporary-balances-in-general-ledger-journals.md).</span><span class="sxs-lookup"><span data-stu-id="536fb-129">For more information, see [View Temporary Balances in General Ledger Journals](how-to-view-temporary-balances-in-general-ledger-journals.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="536fb-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="536fb-130">See Also</span></span>  
 <span data-ttu-id="536fb-131">[Afficher les soldes temporaires dans les feuilles comptabilisation immobilisation](how-to-view-temporary-balances-in-general-ledger-journals.md) </span><span class="sxs-lookup"><span data-stu-id="536fb-131">[View Temporary Balances in General Ledger Journals](how-to-view-temporary-balances-in-general-ledger-journals.md) </span></span>  
 [<span data-ttu-id="536fb-132">Fonctionnalité locale, Suisse</span><span class="sxs-lookup"><span data-stu-id="536fb-132">Switzerland Local Functionality</span></span>](switzerland-local-functionality.md)

