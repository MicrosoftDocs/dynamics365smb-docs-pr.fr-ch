---
title: En savoir plus sur les écritures comptables et le COA| Microsoft Docs
description: Décrit les écritures comptables, le plan comptable, et les catégories de compte.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 054f21756d5c6587bbdb718f7d068933198878c1
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2302324"
---
# <a name="understanding-the-general-ledger-and-the-coa"></a><span data-ttu-id="53209-103">Familiarisation avec les écritures comptables et les COA</span><span class="sxs-lookup"><span data-stu-id="53209-103">Understanding the General Ledger and the COA</span></span>
<span data-ttu-id="53209-104">Les écritures comptables stockent vos données financières, et le plan comptable affiche les comptes sur lesquels toutes les écritures comptables sont validées.</span><span class="sxs-lookup"><span data-stu-id="53209-104">The general ledger stores your financial data, and the chart of accounts shows the accounts that all general ledger entries are posted to.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="53209-105">inclut un plan comptable standard prêt à prendre en charge votre société.</span><span class="sxs-lookup"><span data-stu-id="53209-105">includes a standard chart of accounts that is ready to support your business.</span></span>

## <a name="general-ledger-setup-and-general-posting-setup"></a><span data-ttu-id="53209-106">Configuration des écritures comptable et configuration de la comptabilisation</span><span class="sxs-lookup"><span data-stu-id="53209-106">General Ledger Setup and General Posting Setup</span></span>
<span data-ttu-id="53209-107">La configuration des écritures comptables est le composant principal des processus financiers car elle définit comment vous validez les données.</span><span class="sxs-lookup"><span data-stu-id="53209-107">The setup of the general ledger is at the core of financial processes because it defines how you post data.</span></span>  

<span data-ttu-id="53209-108">Sur la page **Paramètres comptabilité**, vous spécifiez comment gérer certains problèmes comptables dans votre société, par exemple :</span><span class="sxs-lookup"><span data-stu-id="53209-108">On the **General Ledger Setup** page, you specify how to handle certain accounting issues in your company, such as:</span></span>  

* <span data-ttu-id="53209-109">Les détails arrondi facture</span><span class="sxs-lookup"><span data-stu-id="53209-109">Invoice rounding details</span></span>  
* <span data-ttu-id="53209-110">Les formats d'adresse</span><span class="sxs-lookup"><span data-stu-id="53209-110">Address formats</span></span>  
* <span data-ttu-id="53209-111">Les états financiers</span><span class="sxs-lookup"><span data-stu-id="53209-111">Financial reporting</span></span>  

<span data-ttu-id="53209-112">De même, sur la page **Paramètres comptabilisation**, vous spécifiez comment vous souhaitez configurer les combinaisons de groupes généraux comptabilisation marché et de groupes généraux comptabilisation produit.</span><span class="sxs-lookup"><span data-stu-id="53209-112">Similarly, on the **General Posting Setup** page, you specify how you want to set up combinations of general business and general product posting groups.</span></span> <span data-ttu-id="53209-113">Les groupes comptabilisation mappent des entités telles que les clients, les fournisseurs, les éléments, les ressources et les documents vente et achat dans des comptes généraux.</span><span class="sxs-lookup"><span data-stu-id="53209-113">Posting groups map entities like customers, vendors, items, resources, and sales and purchase documents to general ledger accounts.</span></span> <span data-ttu-id="53209-114">Saisissez une ligne pour chaque combinaison de groupes comptabilisation marché et de groupes comptabilisation produit.</span><span class="sxs-lookup"><span data-stu-id="53209-114">You fill in a line for each combination of business posting group and product posting group.</span></span> <span data-ttu-id="53209-115">Pour plus d'informations, voir [Paramètres du groupe comptabilisation](finance-posting-groups.md)</span><span class="sxs-lookup"><span data-stu-id="53209-115">For more information, see [Posting Group Setups](finance-posting-groups.md)</span></span>  

## <a name="the-chart-of-accounts"></a><span data-ttu-id="53209-116">Le plan comptable</span><span class="sxs-lookup"><span data-stu-id="53209-116">The Chart of Accounts</span></span>
<span data-ttu-id="53209-117">Le plan comptable affiche tous les comptes généraux.</span><span class="sxs-lookup"><span data-stu-id="53209-117">The chart of accounts shows all general ledger accounts.</span></span> <span data-ttu-id="53209-118">Vous pouvez effectuer les opérations suivantes à partir du plan comptable :</span><span class="sxs-lookup"><span data-stu-id="53209-118">From the chart of accounts, you can do things like:</span></span>  

* <span data-ttu-id="53209-119">Afficher les états qui affichent les écritures comptables et les soldes.</span><span class="sxs-lookup"><span data-stu-id="53209-119">View reports that show general ledger entries and balances.</span></span>  
* <span data-ttu-id="53209-120">Clôturer votre exercice comptable.</span><span class="sxs-lookup"><span data-stu-id="53209-120">Close your income statement.</span></span>  
* <span data-ttu-id="53209-121">Ouvrir la fiche compte général pour ajouter ou modifier des paramètres.</span><span class="sxs-lookup"><span data-stu-id="53209-121">Open the G/L account card to add or change settings.</span></span>  
* <span data-ttu-id="53209-122">Consulter la liste des groupes comptabilisation qui effectuent les validations vers ce compte.</span><span class="sxs-lookup"><span data-stu-id="53209-122">See a list of posting groups that post to that account.</span></span>
* <span data-ttu-id="53209-123">Afficher les soldes débit et crédit d'un seul compte</span><span class="sxs-lookup"><span data-stu-id="53209-123">View separate debit and credit balances for a single account</span></span>  

<span data-ttu-id="53209-124">Vous pouvez ajouter, modifier ou supprimer des comptes généraux.</span><span class="sxs-lookup"><span data-stu-id="53209-124">You can add, change, or delete general ledger accounts.</span></span> <span data-ttu-id="53209-125">Toutefois, pour éviter les différences, vous ne pouvez pas supprimer un compte général si ses données sont utilisées dans le plan comptable.</span><span class="sxs-lookup"><span data-stu-id="53209-125">However, to prevent discrepancies, you can't delete a general ledger account if it's data is used in the chart of accounts.</span></span>  

## <a name="account-categories"></a><span data-ttu-id="53209-126">Catégories de compte</span><span class="sxs-lookup"><span data-stu-id="53209-126">Account Categories</span></span>
<span data-ttu-id="53209-127">Vous pouvez personnaliser la structure de vos états financiers en mappant les comptes généraux aux catégories de comptes.</span><span class="sxs-lookup"><span data-stu-id="53209-127">You can personalize the structure of your financial statements by mapping general ledger accounts to account categories.</span></span>  

<span data-ttu-id="53209-128">La page **Catégories de compte général** affiche vos catégories et sous-catégories et les comptes généraux que leurs sont affectés.</span><span class="sxs-lookup"><span data-stu-id="53209-128">The **G/L Account Categories** page shows your categories and subcategories, and the G/L accounts that are assigned to them.</span></span> <span data-ttu-id="53209-129">Vous pouvez créer des sous-catégories et affecter ces catégories à des comptes existants.</span><span class="sxs-lookup"><span data-stu-id="53209-129">You can create new subcategories and assign those categories to existing accounts.</span></span>  

<span data-ttu-id="53209-130">Vous créez un groupe des catégories en effectuant une indentation d'autres sous-catégories sous une ligne de la page **Catégories de compte général**.</span><span class="sxs-lookup"><span data-stu-id="53209-130">You create a category group by indenting other subcategories under a line on the **G/L Account Categories** page.</span></span> <span data-ttu-id="53209-131">Cela vous facilite l'obtention d'une vue d'ensemble, car chaque groupement affiche un solde final.</span><span class="sxs-lookup"><span data-stu-id="53209-131">This makes it easy for you to get an overview, because each grouping shows a total balance.</span></span> <span data-ttu-id="53209-132">Par exemple, vous pouvez créer des sous-catégories pour différents types d'actifs puis créer des groupes des catégories pour différencier les immobilisations des actifs à court terme, par exemple.</span><span class="sxs-lookup"><span data-stu-id="53209-132">For example, you can create subcategories for different types of assets, and then create category groups for fixed assets versus current assets.</span></span>  

<span data-ttu-id="53209-133">Vous pouvez spécifier si les comptes de chaque sous-catégorie doivent être inclus dans des types spécifiques d'états.</span><span class="sxs-lookup"><span data-stu-id="53209-133">You can specify whether the accounts in each subcategory must be included in specific types of reports.</span></span> <span data-ttu-id="53209-134">Les catégories de compte vous aident à définir la présentation de vos états financiers.</span><span class="sxs-lookup"><span data-stu-id="53209-134">The account categories help define the layout of your financial statements.</span></span>  

<span data-ttu-id="53209-135">Par exemple, le solde relevé par défaut solde est doté d'une sous-catégorie pour la trésorerie dans Actifs à court terme.</span><span class="sxs-lookup"><span data-stu-id="53209-135">For example, the default balance statement has a subcategory for Cash under Current Assets.</span></span> <span data-ttu-id="53209-136">Si vous souhaitez que le solde relevé tienne compte du fonds de caisse et du compte chèque, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="53209-136">If you want the balance statement consider petty cash and checking, you can:</span></span>  

1. <span data-ttu-id="53209-137">Ajouter deux nouvelles sous-catégories.</span><span class="sxs-lookup"><span data-stu-id="53209-137">Add two new subcategories.</span></span> <span data-ttu-id="53209-138">Une pour le fonds de caisse, et l'autre pour le compte chèque.</span><span class="sxs-lookup"><span data-stu-id="53209-138">One for petty cash, and one for your checking account.</span></span>  
2. <span data-ttu-id="53209-139">Spécifier la définition d'état supplémentaire **Comptes de trésorerie** pour ces sous-catégories.</span><span class="sxs-lookup"><span data-stu-id="53209-139">Specify the additional report definition **Cash Accounts** for these subcategories.</span></span>  
3. <span data-ttu-id="53209-140">Effectuer une indentation sous la sous-catégorie **Trésorerie**.</span><span class="sxs-lookup"><span data-stu-id="53209-140">Indent them under the **Cash** subcategory.</span></span>  

<span data-ttu-id="53209-141">À la prochaine génération des tableaux d'analyse, votre relevé solde suivant affichera un solde final pour la trésorerie et deux lignes avec les soldes pour le fonds de caisse et le compte chèque.</span><span class="sxs-lookup"><span data-stu-id="53209-141">The next time you generate account schedules your balance statement will show a total balance for cash and two lines with balances for petty cash and the checking account.</span></span>  

## <a name="see-also"></a><span data-ttu-id="53209-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53209-142">See Also</span></span>
[<span data-ttu-id="53209-143">Finances</span><span class="sxs-lookup"><span data-stu-id="53209-143">Finance</span></span>](finance.md)  
[<span data-ttu-id="53209-144">Configuration ou modification du plan comptable</span><span class="sxs-lookup"><span data-stu-id="53209-144">Setting Up or Changing the Chart of Accounts</span></span>](finance-setup-chart-accounts.md)  
[<span data-ttu-id="53209-145">Veille économique</span><span class="sxs-lookup"><span data-stu-id="53209-145">Business Intelligence</span></span>](bi.md)  
