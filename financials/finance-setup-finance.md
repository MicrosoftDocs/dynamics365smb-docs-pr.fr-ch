---
title: Configurer les processus financiers| Microsoft Docs
description: "En savoir plus sur les tâches pour paramétrer les finances de votre société afin de les adapter à votre comptabilité ou vos audits."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 08/10/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b63e2e65f92edbbe10bcb5e2c340db31b1acda28
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-finance"></a><span data-ttu-id="6db04-103">Configuration de Finance</span><span class="sxs-lookup"><span data-stu-id="6db04-103">Setting Up Finance</span></span>
<span data-ttu-id="6db04-104">Pour vous aider à démarrer rapidement, [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] inclut des configurations standard pour la plupart des processus financiers.</span><span class="sxs-lookup"><span data-stu-id="6db04-104">To help you get going quickly, [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] includes standard configurations for most financial processes.</span></span> <span data-ttu-id="6db04-105">Si vous devez modifier les configurations en fonction de votre activité, n'hésitez pas.</span><span class="sxs-lookup"><span data-stu-id="6db04-105">If you need to change the configurations to suit your business, go right ahead.</span></span> <span data-ttu-id="6db04-106">Par exemple, à partir de la page d'accueil, vous pouvez utiliser un guide de configuration assistée pour configurer la taxe sur les ventes en fonction de votre situation géographique.</span><span class="sxs-lookup"><span data-stu-id="6db04-106">For example, from the Home page you can use an assisted setup guide to set up sales tax rate for your location.</span></span>  

<span data-ttu-id="6db04-107">Toutefois, il existe quelques éléments que vous devez configurer vous-même.</span><span class="sxs-lookup"><span data-stu-id="6db04-107">However, there are some things you need to set up yourself.</span></span> <span data-ttu-id="6db04-108">Par exemple, si vous souhaitez utiliser les axes analytiques comme base pour la veille économique.</span><span class="sxs-lookup"><span data-stu-id="6db04-108">For example, if you want to use dimensions as a basis for business intelligence.</span></span>  

<span data-ttu-id="6db04-109">Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.</span><span class="sxs-lookup"><span data-stu-id="6db04-109">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="6db04-110">À</span><span class="sxs-lookup"><span data-stu-id="6db04-110">To</span></span> | <span data-ttu-id="6db04-111">Voir</span><span class="sxs-lookup"><span data-stu-id="6db04-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="6db04-112">Choisissez la méthode pour payer vos fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="6db04-112">Choose how you pay your vendors.</span></span> |[<span data-ttu-id="6db04-113">Définition des modes de règlement</span><span class="sxs-lookup"><span data-stu-id="6db04-113">Defining Payment Methods</span></span>](finance-payment-methods.md) |
| <span data-ttu-id="6db04-114">Spécifiez les groupes comptabilisation qui mappent des entités telles que les clients, les fournisseurs, les éléments, les ressources et les documents vente et achat dans des comptes généraux.</span><span class="sxs-lookup"><span data-stu-id="6db04-114">Specify the posting groups that map entities like customers, vendors, items, resources, and sales and purchase documents to general ledger accounts.</span></span> |[<span data-ttu-id="6db04-115">Configuration de groupes comptabilisation</span><span class="sxs-lookup"><span data-stu-id="6db04-115">Setting Up Posting Groups</span></span>](finance-posting-groups.md)|
|<span data-ttu-id="6db04-116">Configurer une valeur de tolérance selon laquelle le système clôt une facture même si le règlement, tenant compte d'éventuelles remises, ne couvre pas intégralement le montant de la facture.</span><span class="sxs-lookup"><span data-stu-id="6db04-116">Set up a tolerance by which the system closes an invoice even though the payment, including any discount, does not fully cover the amount on the invoice.</span></span>|[<span data-ttu-id="6db04-117">Procédure : Utilisation des écarts de règlement et des écarts d'escompte</span><span class="sxs-lookup"><span data-stu-id="6db04-117">How to: Work with Payment Tolerances and Payment Discount Tolerances</span></span>](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| <span data-ttu-id="6db04-118">Définir les périodes fiscales.</span><span class="sxs-lookup"><span data-stu-id="6db04-118">Set up fiscal periods.</span></span> |[<span data-ttu-id="6db04-119">Procédure : ouverture d'un nouvel exercice comptable</span><span class="sxs-lookup"><span data-stu-id="6db04-119">How to: Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md) |
| <span data-ttu-id="6db04-120">Définissez comment déclarer les montants de taxe sur la valeur ajoutée que vous avez recueillis sur les ventes aux autorités fiscales.</span><span class="sxs-lookup"><span data-stu-id="6db04-120">Define how you report value-added tax amounts that you have collected for sales to the tax authorities.</span></span> |[<span data-ttu-id="6db04-121">Procédure : Déclarer la TVA aux autorités fiscales</span><span class="sxs-lookup"><span data-stu-id="6db04-121">How To: Report VAT to Tax Authorities</span></span>](finance-how-report-vat.md)|
| <span data-ttu-id="6db04-122">Définissez vos fonctionnalités Ventes et Achats pour gérer les paiements dans des devises étrangères.</span><span class="sxs-lookup"><span data-stu-id="6db04-122">Set your Sales and Purchases features up to handle payments in foreign currencies.</span></span>|[<span data-ttu-id="6db04-123">Procédure : activer le lettrage d'écritures comptables client en devises différentes</span><span class="sxs-lookup"><span data-stu-id="6db04-123">How to: Enable Application of Ledger Entries in Different Currencies</span></span>](finance-how-enable-application-ledger-entries-different-currencies.md)
| <span data-ttu-id="6db04-124">Ajouter de nouveaux comptes au plan comptable existant.</span><span class="sxs-lookup"><span data-stu-id="6db04-124">Add new accounts to the existing chart of accounts.</span></span> |[<span data-ttu-id="6db04-125">Configuration du plan comptable</span><span class="sxs-lookup"><span data-stu-id="6db04-125">Setting Up the Chart of Accounts</span></span>](finance-setup-chart-accounts.md) |
| <span data-ttu-id="6db04-126">Configurez les graphiques de veille économique pour analyser la trésorerie.</span><span class="sxs-lookup"><span data-stu-id="6db04-126">Set up business intelligence (BI) charts to analyze cash flow.</span></span> |[<span data-ttu-id="6db04-127">Configuration d'une analyse de trésorerie</span><span class="sxs-lookup"><span data-stu-id="6db04-127">Setting Up Cash Flow Analysis</span></span>](finance-setup-cash-flow-analyses.md) |
|<span data-ttu-id="6db04-128">Activer la facturation d'un client qui n'est pas configuré dans le système.</span><span class="sxs-lookup"><span data-stu-id="6db04-128">Enable invoicing of a customer who is not set up in the system.</span></span>|[<span data-ttu-id="6db04-129">Procédure : configurer des clients effectuant un achat au comptoir</span><span class="sxs-lookup"><span data-stu-id="6db04-129">How to: Set Up Cash Customers</span></span>](finance-how-to-set-up-cash-customers.md)|
| <span data-ttu-id="6db04-130">Configurer l'état intracommunautaire et envoyer-le à une administration</span><span class="sxs-lookup"><span data-stu-id="6db04-130">Set up Intrastat reporting, and submit the report to an authority</span></span> | [<span data-ttu-id="6db04-131">Procédure : configurer et enregistrer un état intracommunautaire</span><span class="sxs-lookup"><span data-stu-id="6db04-131">How to: Set Up and Report Intrastat</span></span>](finance-how-setup-report-intrastat.md)|

## <a name="see-also"></a><span data-ttu-id="6db04-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6db04-132">See Also</span></span>
<span data-ttu-id="6db04-133">[Finances](finance.md)]</span><span class="sxs-lookup"><span data-stu-id="6db04-133">[Finance](finance.md)]</span></span>  
[<span data-ttu-id="6db04-134">Gestion des comptes bancaires</span><span class="sxs-lookup"><span data-stu-id="6db04-134">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="6db04-135">Utilisation des axes analytiques</span><span class="sxs-lookup"><span data-stu-id="6db04-135">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="6db04-136">Importation des données métier à partir d'autres systèmes financiers</span><span class="sxs-lookup"><span data-stu-id="6db04-136">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
[<span data-ttu-id="6db04-137">Analyse de la trésorerie dans votre société</span><span class="sxs-lookup"><span data-stu-id="6db04-137">Analyzing Cash Flow in Your Company</span></span>](finance-analyze-cash-flow.md)  
<span data-ttu-id="6db04-138">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6db04-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

