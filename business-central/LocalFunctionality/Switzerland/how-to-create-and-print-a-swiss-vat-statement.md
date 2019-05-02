---
title: 'Procédure : Créer et imprimer une déclaration de TVA, Suisse'
description: Selon les informations spécifiées dans la page Paramètres compta. TVA, Business Central peut créer automatiquement une nouvelle configuration de relevé de TVA pour le report TVA réalisé. Avant de continuer avec les procédures de cette rubrique, assurez-vous que vous avez configuré les paramètres comptabilisation TVA ayant des valeurs spécifiées pour les champs de chiffre d'affaires ventes et achats.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: cb555b9fccc4a39acd629878818dd0301e1b034b
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "827305"
---
# <a name="create-and-print-a-swiss-vat-statement"></a><span data-ttu-id="ff75b-104">Créer et imprimer une déclaration de TVA, Suisse</span><span class="sxs-lookup"><span data-stu-id="ff75b-104">Create and Print a Swiss VAT Statement</span></span>
<span data-ttu-id="ff75b-105">Selon les informations spécifiées dans la page **Paramètres compta. TVA**, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] peut créer automatiquement une nouvelle configuration de relevé de TVA pour le report TVA réalisé.</span><span class="sxs-lookup"><span data-stu-id="ff75b-105">Based on the information that you have specified on the **VAT Posting Setup** page, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] can automatically create a new VAT Statement Setup for realized VAT reporting.</span></span> <span data-ttu-id="ff75b-106">Avant de continuer avec les procédures de cette rubrique, assurez-vous que vous avez configuré les paramètres comptabilisation TVA ayant des valeurs spécifiées pour les champs de chiffre d'affaires ventes et achats.</span><span class="sxs-lookup"><span data-stu-id="ff75b-106">Before proceeding with the procedures in this topic, make sure that you have set up VAT posting setup with values specified for the sales and purchase cipher fields.</span></span>  

## <a name="to-set-up-a-swiss-vat-statement-template"></a><span data-ttu-id="ff75b-107">Pour configurer un modèle de déclaration de TVA suisse</span><span class="sxs-lookup"><span data-stu-id="ff75b-107">To set up a Swiss VAT statement template</span></span>  

1.  <span data-ttu-id="ff75b-108">Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "icône Page ou état pour la recherche"), entrez **Mettre à jour le modèle de déclaration de TVA**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="ff75b-108">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Update VAT Statement Template**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ff75b-109">Sélectionnez un modèle dans le champ **Nom modèle déclaration de TVA**.</span><span class="sxs-lookup"><span data-stu-id="ff75b-109">Select a template in the **VAT Statement Template Name** field.</span></span>
3.  <span data-ttu-id="ff75b-110">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff75b-110">Choose the **OK** button.</span></span> <span data-ttu-id="ff75b-111">Cliquez sur **Oui** pour confirmer que vous souhaitez créer un modèle.</span><span class="sxs-lookup"><span data-stu-id="ff75b-111">Choose the **Yes** button to confirm that you want to create a new template.</span></span>  
4.  <span data-ttu-id="ff75b-112">Vérifiez la déclaration TVA qui en résulte et ajustez-la autant que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ff75b-112">Check the resulting VAT Statement and adjust as needed.</span></span>  

     <span data-ttu-id="ff75b-113">La page de déclaration TVA indique le champ **Chiffre de déclaration TVA**, qui indique dans quel zone de la déclaration le résultat sera imprimé.</span><span class="sxs-lookup"><span data-stu-id="ff75b-113">he VAT Statement page contains the **VAT Statement Cipher** field, which indicates in which cipher of the report the result will be printed.</span></span> <span data-ttu-id="ff75b-114">Ce champ est automatiquement renseigné par le traitement par lots selon les informations de la page **Paramètres compta. TVA**.</span><span class="sxs-lookup"><span data-stu-id="ff75b-114">This field is automatically populated by the batch job based on the information on the **VAT Posting Setup** page.</span></span> <span data-ttu-id="ff75b-115">Le champ peut être modifié, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ff75b-115">The field can be edited if needed.</span></span>  

## <a name="to-print-the-swiss-vat-statement"></a><span data-ttu-id="ff75b-116">Pour imprimer la déclaration TVA suisse</span><span class="sxs-lookup"><span data-stu-id="ff75b-116">To print the Swiss VAT statement</span></span>  

1.  <span data-ttu-id="ff75b-117">Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Déclaration TVA suisse**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="ff75b-117">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Swiss VAT Statement**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ff75b-118">Sous le raccourci **Options**, renseignez les champs comme indiqué dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="ff75b-118">On the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="ff75b-119">Champ</span><span class="sxs-lookup"><span data-stu-id="ff75b-119">Field</span></span>|<span data-ttu-id="ff75b-120">Désignation</span><span class="sxs-lookup"><span data-stu-id="ff75b-120">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="ff75b-121">**Date début**</span><span class="sxs-lookup"><span data-stu-id="ff75b-121">**Starting Date**</span></span>|<span data-ttu-id="ff75b-122">Saisissez la date à laquelle vous souhaitez que l'intervalle de temps des lignes déclaration de TVA figurant sur l'état commence.</span><span class="sxs-lookup"><span data-stu-id="ff75b-122">Enter the date that you want the time interval for VAT statement lines that appear in the report to start.</span></span>|  
    |<span data-ttu-id="ff75b-123">**Date fin**</span><span class="sxs-lookup"><span data-stu-id="ff75b-123">**Ending Date**</span></span>|<span data-ttu-id="ff75b-124">Saisissez la date à laquelle vous souhaitez que l'intervalle de temps des lignes déclaration de TVA figurant sur l'état se termine.</span><span class="sxs-lookup"><span data-stu-id="ff75b-124">Enter the date that you want the time interval for VAT statement lines that appear in the report to end.</span></span>|  
    |<span data-ttu-id="ff75b-125">**Clôture avec n° de déclaration de TVA**</span><span class="sxs-lookup"><span data-stu-id="ff75b-125">**Closed with VAT Register No.**</span></span>|<span data-ttu-id="ff75b-126">Sélectionnez le registre de TVA qui contient la source de comptabilisation des écritures d'ajustement de la TVA.</span><span class="sxs-lookup"><span data-stu-id="ff75b-126">Select the VAT Register that contains the posting source of the VAT adjusting entries.</span></span> <span data-ttu-id="ff75b-127">Cette option évalue les périodes comptables qui ont déjà établies.</span><span class="sxs-lookup"><span data-stu-id="ff75b-127">This option evaluates accounting periods that have already been settled.</span></span> <span data-ttu-id="ff75b-128">Lorsque vous choisissez cette option, vous ne spécifiez pas les options dans les champs **Inclure écritures TVA** suivants.</span><span class="sxs-lookup"><span data-stu-id="ff75b-128">When you choose this option, you do not specify options in the following **Include VAT Entries** fields.</span></span>|  
    |<span data-ttu-id="ff75b-129">**Inclure écritures TVA**</span><span class="sxs-lookup"><span data-stu-id="ff75b-129">**Include VAT Entries**</span></span>|<span data-ttu-id="ff75b-130">Sélectionnez l'une des options disponibles.</span><span class="sxs-lookup"><span data-stu-id="ff75b-130">Select one of the available options.</span></span>|  
    |<span data-ttu-id="ff75b-131">**Inclure écritures TVA**</span><span class="sxs-lookup"><span data-stu-id="ff75b-131">**Include VAT Entries**</span></span>|<span data-ttu-id="ff75b-132">Sélectionnez l'une des options disponibles.</span><span class="sxs-lookup"><span data-stu-id="ff75b-132">Select one of the available options.</span></span>|  
    |<span data-ttu-id="ff75b-133">**% taux normal**</span><span class="sxs-lookup"><span data-stu-id="ff75b-133">**Normal Rate %**</span></span>|<span data-ttu-id="ff75b-134">Entrez le taux de TVA standard s'appliquant à la période.</span><span class="sxs-lookup"><span data-stu-id="ff75b-134">Enter the standard VAT rate that applies to the time period.</span></span>|  
    |<span data-ttu-id="ff75b-135">**% taux réduit**</span><span class="sxs-lookup"><span data-stu-id="ff75b-135">**Reduced Rate %**</span></span>|<span data-ttu-id="ff75b-136">Saisissez la taxe de TVA réduite pour certains biens et services.</span><span class="sxs-lookup"><span data-stu-id="ff75b-136">Enter the reduced VAT tax for certain goods and services.</span></span>|  
    |<span data-ttu-id="ff75b-137">\***% taux hôtel**</span><span class="sxs-lookup"><span data-stu-id="ff75b-137">**Hotel Rate %**</span></span>|<span data-ttu-id="ff75b-138">Entrez le taux de TVA pour l'hébergement s'appliquant à la période.</span><span class="sxs-lookup"><span data-stu-id="ff75b-138">Enter the VAT rate for accommodation that applies to the time period.</span></span>|  
    |<span data-ttu-id="ff75b-139">**% normal (autre taux)**</span><span class="sxs-lookup"><span data-stu-id="ff75b-139">**Normal (Other Rate) %**</span></span>|<span data-ttu-id="ff75b-140">Saisissez un taux TVA secondaire pour des transactions standard s'appliquant à certaines transactions au cours de la période.</span><span class="sxs-lookup"><span data-stu-id="ff75b-140">Enter an alternative VAT rate for standard transactions that applies to certain transactions during the time period.</span></span>|  
    |<span data-ttu-id="ff75b-141">**% réduit (autre taux)**</span><span class="sxs-lookup"><span data-stu-id="ff75b-141">**Reduced (Other Rate) %**</span></span>|<span data-ttu-id="ff75b-142">Saisissez un taux TVA secondaire pour d'autres transactions s'appliquant à certaines transactions au cours de la période.</span><span class="sxs-lookup"><span data-stu-id="ff75b-142">Enter an alternative VAT rate for other transactions that applies to certain transactions during the time period.</span></span>|  
    |<span data-ttu-id="ff75b-143">**% Hôtel (Autre taux)**</span><span class="sxs-lookup"><span data-stu-id="ff75b-143">**Hotel (Other Rate) %**</span></span>|<span data-ttu-id="ff75b-144">Saisissez un taux TVA secondaire pour l'hébergement s'appliquant à certaines transactions au cours de la période.</span><span class="sxs-lookup"><span data-stu-id="ff75b-144">Enter an alternative VAT rate for accommodation that applies to certain transactions during the time period.</span></span>|  
    |<span data-ttu-id="ff75b-145">**Afficher montants en devise report**</span><span class="sxs-lookup"><span data-stu-id="ff75b-145">**Show Amounts in Add. Reporting Currency**</span></span>|<span data-ttu-id="ff75b-146">Choisissez d'afficher les montants dans une devise de report supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="ff75b-146">Select to show amounts in an additional reporting currency.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="ff75b-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff75b-147">See Also</span></span>  
 [<span data-ttu-id="ff75b-148">Taxe sur la valeur ajoutée, Suisse</span><span class="sxs-lookup"><span data-stu-id="ff75b-148">Swiss Value Added Tax</span></span>](swiss-value-added-tax.md)