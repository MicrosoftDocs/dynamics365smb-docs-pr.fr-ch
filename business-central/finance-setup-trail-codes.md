---
title: Configurer des codes pistes d’audit | Microsoft Docs
description: Découvrez les tâches de configuration des codes source et des codes motif que vous pouvez utiliser pour suivre les pistes d’audit.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 6c20c57f05d17b0b52fcc1d4c9b1234cf03c6e97
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5773854"
---
# <a name="setting-up-source-codes-and-reason-codes-for-audit-trails"></a><span data-ttu-id="589b0-103">Configuration des codes source et des codes de motif pour les pistes d’audit</span><span class="sxs-lookup"><span data-stu-id="589b0-103">Setting Up Source Codes and Reason Codes for Audit Trails</span></span>

<span data-ttu-id="589b0-104">Un code journal est affecté automatiquement à toutes les écritures validées, de sorte que les transactions puissent être suivies jusqu’à leur origine.</span><span class="sxs-lookup"><span data-stu-id="589b0-104">All posted entries are automatically assigned a source code so that transactions can be traced to their origin.</span></span> <span data-ttu-id="589b0-105">Pour attribuer un autre code journal aux écritures, vous pouvez utiliser les codes motif.</span><span class="sxs-lookup"><span data-stu-id="589b0-105">If you want to give entries a supplementary source code, you can use reason codes.</span></span> <span data-ttu-id="589b0-106">Ces derniers permettent d’indiquer le motif de création d’une écriture.</span><span class="sxs-lookup"><span data-stu-id="589b0-106">Reason codes are used to indicate why an entry was created.</span></span> <span data-ttu-id="589b0-107">Lorsque vous les configurez, vous pouvez les affecter à des modèles ou des noms de feuilles, ainsi qu’à des lignes feuille et documents spécifiques.</span><span class="sxs-lookup"><span data-stu-id="589b0-107">When you set up reason codes, you can assign them to entire journal templates and journal batches, and you can assign them to individual journal lines and documents.</span></span>  

<span data-ttu-id="589b0-108">Pour les codes source et les codes motif, utilisez des codes faciles à mémoriser et descriptifs.</span><span class="sxs-lookup"><span data-stu-id="589b0-108">For both source codes and reason codes, use codes that are easy to remember and descriptive.</span></span> <span data-ttu-id="589b0-109">Le code doit être unique et vous pouvez configurer autant de codes que vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="589b0-109">The code must be unique, and you can set up as many codes as you like.</span></span>

## <a name="define-source-codes"></a><span data-ttu-id="589b0-110">Définir des codes journaux</span><span class="sxs-lookup"><span data-stu-id="589b0-110">Define source codes</span></span>

<span data-ttu-id="589b0-111">Parfois, vous souhaitez savoir comment une écriture particulière a été créée, par exemple si elle vient de la validation d’une feuille ou d’une facture achat.</span><span class="sxs-lookup"><span data-stu-id="589b0-111">Sometimes, you want see how a particular entry arose, such as whether it came from posting a general journal or a purchase invoice.</span></span> <span data-ttu-id="589b0-112">Un code journal indique l’emplacement de création d’une écriture.</span><span class="sxs-lookup"><span data-stu-id="589b0-112">A source code indicates where an entry was created.</span></span> <span data-ttu-id="589b0-113">Les écritures sont créées lors de la validation des feuilles et des factures et lors de l’exécution de certains traitements par lots.</span><span class="sxs-lookup"><span data-stu-id="589b0-113">Entries are created when journals and invoices are posted and when certain batch jobs are executed.</span></span> <span data-ttu-id="589b0-114">Un code journal spécifique existe pour chaque type compta. et est affecté lors de la création d’écritures individuelles.</span><span class="sxs-lookup"><span data-stu-id="589b0-114">Each posting type has a specific source code that is assigned when individual entries are created.</span></span>  

<span data-ttu-id="589b0-115">La validation de feuilles, de commandes, de factures ou d’avoirs, et l’exécution de divers traitement par lots, crée des écritures dans les états financiers.</span><span class="sxs-lookup"><span data-stu-id="589b0-115">Posting journals, orders, invoices, or credit memos, and running various batch jobs, creates entries in the financial statements.</span></span> <span data-ttu-id="589b0-116">La page **Paramètres codes journaux** comporte plusieurs raccourcis, un pour chaque domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="589b0-116">The **Source Code Setup** page contains several FastTabs, one for each application area.</span></span> <span data-ttu-id="589b0-117">Chaque raccourci indique les codes journaux applicables pour ce module.</span><span class="sxs-lookup"><span data-stu-id="589b0-117">Each FastTab contains the source codes that are applicable for that application area.</span></span>

<span data-ttu-id="589b0-118">Lorsque vous validez ou exécutez un traitement par lots, le bon code journal est relié automatiquement à l’écriture.</span><span class="sxs-lookup"><span data-stu-id="589b0-118">When you post or run a batch job, the correct source code is automatically attached to the entry.</span></span> <span data-ttu-id="589b0-119">Par exemple, lorsque vous validez à partir de la feuille, l’écriture est codifiée en tant que *JNLCOMPTA*.</span><span class="sxs-lookup"><span data-stu-id="589b0-119">For example, when you post from the general journal, the entry is coded as *GENJNL*.</span></span> <span data-ttu-id="589b0-120">Vous pouvez ensuite filtrer la page **Écritures comptables** pour afficher les écritures qui ont été publiées à partir de la feuille comptabilité ou des documents de vente, par exemple</span><span class="sxs-lookup"><span data-stu-id="589b0-120">You can then filter the **General Ledger Entries** page to show which entries were posted from the general journal or from sales documents, for example</span></span>

### <a name="to-define-source-codes"></a><span data-ttu-id="589b0-121">Pour définir des codes journaux</span><span class="sxs-lookup"><span data-stu-id="589b0-121">To define source codes</span></span>

1. <span data-ttu-id="589b0-122">Sélectionnez l’icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), saisissez **Paramètres codes journaux**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="589b0-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Source Code Setup**, and then choose the related link.</span></span>  

2. <span data-ttu-id="589b0-123">Dans la fenêtre **Paramètres codes journaux**, pour chaque type de validation et travail par lots, spécifiez le code source approprié.</span><span class="sxs-lookup"><span data-stu-id="589b0-123">In the **Source Code Setup** window, for each each posting type and batch job, specify the relevant source code.</span></span>  

<span data-ttu-id="589b0-124">Vous pouvez modifier le contenu d’un champ ultérieurement, et cette modification aura alors un impact sur les publications futures.</span><span class="sxs-lookup"><span data-stu-id="589b0-124">You can change the contents of a field later, and that change will then impact future postings.</span></span>

## <a name="change-source-codes"></a><span data-ttu-id="589b0-125">Modifier les codes journaux</span><span class="sxs-lookup"><span data-stu-id="589b0-125">Change source codes</span></span>

<span data-ttu-id="589b0-126">Vous pouvez modifier un code journal.</span><span class="sxs-lookup"><span data-stu-id="589b0-126">You may want to change a source code.</span></span> <span data-ttu-id="589b0-127">Par exemple, vous pouvez remplacer le code journal *GENJNL* par *GNJ*.</span><span class="sxs-lookup"><span data-stu-id="589b0-127">For example, you want to change the source code *GENJNL* to *GNJ*.</span></span>

### <a name="to-change-source-codes"></a><span data-ttu-id="589b0-128">Pour modifier des codes journaux</span><span class="sxs-lookup"><span data-stu-id="589b0-128">To change source codes</span></span>

1. <span data-ttu-id="589b0-129">Sélectionnez l’icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), saisissez **Codes journaux**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="589b0-129">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Source Codes**, and then choose the related link.</span></span>

2. <span data-ttu-id="589b0-130">Sur la ligne du code à modifier, sélectionnez le code dans le champ **Code**.</span><span class="sxs-lookup"><span data-stu-id="589b0-130">On the line with the code to be changed, select the code in the **Code** field.</span></span>

3. <span data-ttu-id="589b0-131">Saisissez le nouveau code, puis cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="589b0-131">Enter the new code, and then choose the **Yes** button.</span></span> <span data-ttu-id="589b0-132">Vous pouvez également modifier la valeur du champ **Description**.</span><span class="sxs-lookup"><span data-stu-id="589b0-132">You can also change the contents of the **Description** field.</span></span>

<span data-ttu-id="589b0-133">Toutes les nouvelles écritures qui sont validées à partir de la feuille comptabilité, se verront attribuer un nouveau code journal.</span><span class="sxs-lookup"><span data-stu-id="589b0-133">All new entries that are posted from the general journal will have the new source code.</span></span>

## <a name="define-reason-codes"></a><span data-ttu-id="589b0-134">Définir des codes motif</span><span class="sxs-lookup"><span data-stu-id="589b0-134">Define reason codes</span></span>

<span data-ttu-id="589b0-135">Les codes de motif complètent les codes source et sont utilisés pour indiquer la raison pour laquelle une écriture a été créée.</span><span class="sxs-lookup"><span data-stu-id="589b0-135">Reason codes supplement the source codes and are used to indicate why an entry was created.</span></span> <span data-ttu-id="589b0-136">Vous pouvez affecter des codes motif à chaque écriture, et vous pouvez affecter des codes permanents à des modèles feuille et à des feuilles spécifiques.</span><span class="sxs-lookup"><span data-stu-id="589b0-136">You can assign reason codes on individual entries, and you can assign permanent codes to specific journal templates and journal batches.</span></span> <span data-ttu-id="589b0-137">Lorsqu’un code motif est lié à une ligne feuille ou à un en-tête vente ou achat, toutes les écritures sont marquées avec le code motif lorsqu’elles sont enregistrées.</span><span class="sxs-lookup"><span data-stu-id="589b0-137">When a reason code is linked to a journal line or a sales or purchase header, all entries are marked with the reason code when they are posted.</span></span>  

### <a name="to-set-up-reason-codes"></a><span data-ttu-id="589b0-138">Pour configurer des codes motif</span><span class="sxs-lookup"><span data-stu-id="589b0-138">To set up reason codes</span></span>

1. <span data-ttu-id="589b0-139">Sélectionnez l’icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), saisissez **Codes motif**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="589b0-139">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon")  icon, enter **Reason Codes**, and then choose the related link.</span></span>

2. <span data-ttu-id="589b0-140">Dans la fenêtre **Codes motif**, saisissez le premier code dans le champ **Code**.</span><span class="sxs-lookup"><span data-stu-id="589b0-140">In the **Reason Codes** window, enter the first code in the **Code** field.</span></span> <span data-ttu-id="589b0-141">Dans le champ **Désignation**, saisissez un texte explicatif.</span><span class="sxs-lookup"><span data-stu-id="589b0-141">In the **Description** field, enter an explanatory text.</span></span>

<span data-ttu-id="589b0-142">Répétez cette procédure pour chaque code à utiliser.</span><span class="sxs-lookup"><span data-stu-id="589b0-142">Repeat the procedure for each code you want to use.</span></span> <span data-ttu-id="589b0-143">Vous pouvez configurer autant de codes que vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="589b0-143">You can set up any number of codes.</span></span>

<span data-ttu-id="589b0-144">La procédure suivante décrit comment ajouter un code motif à un modèle feuille, mais des étapes similaires s’appliquent à l’ajout d’un code motif à une ligne feuille ou à une feuille.</span><span class="sxs-lookup"><span data-stu-id="589b0-144">The following procedure describes how to add a reason code to a journal template, but similar steps apply to adding a reason code to a journal line or journal batch.</span></span>  

### <a name="to-assign-reason-codes-to-journal-templates"></a><span data-ttu-id="589b0-145">Pour affecter des codes motif à des modèles feuille</span><span class="sxs-lookup"><span data-stu-id="589b0-145">To assign reason codes to journal templates</span></span>

1. <span data-ttu-id="589b0-146">Sélectionnez l’icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Modèles feuille comptabilité**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="589b0-146">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon")  icon, enter **General Journal Templates**, and then choose the related link.</span></span>

2. <span data-ttu-id="589b0-147">Sur la ligne du modèle feuille sélectionné, renseignez le champ **Code motif** avec le code souhaité.</span><span class="sxs-lookup"><span data-stu-id="589b0-147">On the line with the selected journal template, in the **Reason Code** field, specify the relevant code.</span></span>

3. <span data-ttu-id="589b0-148">Fermez le modèle feuille.</span><span class="sxs-lookup"><span data-stu-id="589b0-148">Close the journal template.</span></span>

<span data-ttu-id="589b0-149">Le code motif sélectionné est copié dans les nouvelles feuilles créées sous le modèle feuille.</span><span class="sxs-lookup"><span data-stu-id="589b0-149">The selected reason code will be copied to new journal batches created under this journal template.</span></span> <span data-ttu-id="589b0-150">Pour affecter des codes motif à des modèles feuille dans les autres modules, procédez de la même manière.</span><span class="sxs-lookup"><span data-stu-id="589b0-150">You assign reason codes to journal templates in the other application areas in the same way.</span></span>

### <a name="to-use-reason-codes-on-sales-and-purchase-documents"></a><span data-ttu-id="589b0-151">Pour utiliser des codes motif dans les documents achat et vente</span><span class="sxs-lookup"><span data-stu-id="589b0-151">To use reason codes on sales and purchase documents</span></span>

1. <span data-ttu-id="589b0-152">Ouvrez le document achat ou vente approprié.</span><span class="sxs-lookup"><span data-stu-id="589b0-152">Open the relevant sales or purchase document.</span></span>

2. <span data-ttu-id="589b0-153">Dans l’en-tête achat ou vente, entrez le code dans le champ **Code motif**.</span><span class="sxs-lookup"><span data-stu-id="589b0-153">On the sales or purchase header, enter the code in the **Reason Code** field.</span></span>

<span data-ttu-id="589b0-154">Lors de la validation de la facture, le code motif est copié dans chaque écriture comptable, client et fournisseur.</span><span class="sxs-lookup"><span data-stu-id="589b0-154">When the invoice is posted, the reason code is copied to each general ledger, customer, and vendor entry.</span></span> <span data-ttu-id="589b0-155">Vous ne pouvez pas affecter un code motif différent à chacune des lignes achat et vente, car toutes les lignes sont validées sous la forme d’une écriture unique.</span><span class="sxs-lookup"><span data-stu-id="589b0-155">You cannot assign different reason codes to the individual purchase and sales lines because all lines are posted as one entry.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="589b0-156">Voir la formation associée sur [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="589b0-156">See Related Training at [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="589b0-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="589b0-157">See Also</span></span>

[<span data-ttu-id="589b0-158">Finances</span><span class="sxs-lookup"><span data-stu-id="589b0-158">Finance</span></span>](finance.md)  
[<span data-ttu-id="589b0-159">Rapprochement de comptes bancaires</span><span class="sxs-lookup"><span data-stu-id="589b0-159">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="589b0-160">Utilisation des axes analytiques</span><span class="sxs-lookup"><span data-stu-id="589b0-160">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="589b0-161">Importation des données métier à partir d’autres systèmes financiers</span><span class="sxs-lookup"><span data-stu-id="589b0-161">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="589b0-162">Analyse de la trésorerie dans votre société</span><span class="sxs-lookup"><span data-stu-id="589b0-162">Analyzing Cash Flow in Your Company</span></span>](finance-analyze-cash-flow.md)  
<span data-ttu-id="589b0-163">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="589b0-163">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]