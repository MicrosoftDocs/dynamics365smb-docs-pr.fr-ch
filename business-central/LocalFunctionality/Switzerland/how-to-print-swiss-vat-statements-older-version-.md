---
title: 'Procédure : Imprimer les relevés de TVA suisse (ancienne version)'
description: La Déclaration TVA suisse est l'état de calcul standard pour la réalisation de la TVA. Vous pouvez imprimer cet état et l'utiliser avec la déclaration de taxe trimestrielle.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: f7b0962740a05172f8a228d8e5f70c7b9b209c00
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778208"
---
# <a name="print-swiss-vat-statements-older-version"></a><span data-ttu-id="83d12-104">Imprimer les relevés de TVA suisse (ancienne version)</span><span class="sxs-lookup"><span data-stu-id="83d12-104">Print Swiss VAT Statements (older version)</span></span>

> [!NOTE]  
>  <span data-ttu-id="83d12-105">Cette rubrique est conservée pour une rétrocompatibilité avec l'état **Déclaration TVA suisse**.</span><span class="sxs-lookup"><span data-stu-id="83d12-105">This topic is retained for backward compatibility with the **Swiss VAT Statement** report.</span></span> <span data-ttu-id="83d12-106">Pour plus d'informations sur l'utilisation de la dernière déclaration TVA suisse, voir Déclaration de TVA en Suisse.</span><span class="sxs-lookup"><span data-stu-id="83d12-106">For information about using the newer Swiss VAT Statement, see Swiss VAT Statement.</span></span>  

<span data-ttu-id="83d12-107">La **Déclaration TVA suisse** est l'état de calcul standard pour la réalisation de la TVA.</span><span class="sxs-lookup"><span data-stu-id="83d12-107">The **Swiss VAT Statement** is the standard calculation report for realizing VAT.</span></span> <span data-ttu-id="83d12-108">Vous pouvez imprimer cet état et l'utiliser avec la déclaration de taxe trimestrielle.</span><span class="sxs-lookup"><span data-stu-id="83d12-108">You can print this report, and use it for quarterly tax reporting.</span></span> <span data-ttu-id="83d12-109">La **Déclaration TVA suisse** inclut les points suivants :</span><span class="sxs-lookup"><span data-stu-id="83d12-109">The **Swiss VAT Statement** includes the following:</span></span>  

- <span data-ttu-id="83d12-110">Écriture TVA</span><span class="sxs-lookup"><span data-stu-id="83d12-110">A VAT entry.</span></span>  
- <span data-ttu-id="83d12-111">Écritures d'ajustement de la TVA</span><span class="sxs-lookup"><span data-stu-id="83d12-111">VAT adjusting entries.</span></span>  
- <span data-ttu-id="83d12-112">Feuille de comptabilité</span><span class="sxs-lookup"><span data-stu-id="83d12-112">An accounting sheet.</span></span>  

## <a name="to-print-the-swiss-vat-statement"></a><span data-ttu-id="83d12-113">Pour imprimer la déclaration TVA suisse</span><span class="sxs-lookup"><span data-stu-id="83d12-113">To print the Swiss VAT statement</span></span>  

1.  <span data-ttu-id="83d12-114">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Déclaration TVA suisse**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="83d12-114">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Swiss VAT Statement**, and then choose the related link.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="83d12-115">Vous recevrez un message indiquant que **Déclaration TVA suisse** s'ouvre dans la langue locale.</span><span class="sxs-lookup"><span data-stu-id="83d12-115">You will receive a message stating that the **Swiss VAT Statement** will open in the local language.</span></span>  

2.  <span data-ttu-id="83d12-116">Sous le raccourci **Options**, renseignez les champs comme indiqué dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="83d12-116">On the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="83d12-117">Champ</span><span class="sxs-lookup"><span data-stu-id="83d12-117">Field</span></span>|<span data-ttu-id="83d12-118">Désignation</span><span class="sxs-lookup"><span data-stu-id="83d12-118">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="83d12-119">**Clôturé avec n° feuille**</span><span class="sxs-lookup"><span data-stu-id="83d12-119">**Closed with Journal no.**</span></span>|<span data-ttu-id="83d12-120">Sélectionnez les feuilles grand livre contenant la source de comptabilisation des écritures d'ajustement de la TVA.</span><span class="sxs-lookup"><span data-stu-id="83d12-120">Select the general ledger journals that contain the posting source of the VAT adjusting entries.</span></span> <span data-ttu-id="83d12-121">Ce champ évalue les périodes comptables qui ont déjà établies.</span><span class="sxs-lookup"><span data-stu-id="83d12-121">This field evaluates accounting periods that have already been settled.</span></span>|  
    |<span data-ttu-id="83d12-122">**Ouvrir jusqu'à la date**</span><span class="sxs-lookup"><span data-stu-id="83d12-122">**Open until date**</span></span>|<span data-ttu-id="83d12-123">Sélectionnez la dernière date pour régler les écritures TVA ouvertes ou non définies.</span><span class="sxs-lookup"><span data-stu-id="83d12-123">Select the last date for settling open or unsettled VAT entries.</span></span>|  
    |<span data-ttu-id="83d12-124">**Afficher les validations**</span><span class="sxs-lookup"><span data-stu-id="83d12-124">**Show Postings**</span></span>|<span data-ttu-id="83d12-125">Spécifie si toutes les écritures TVA pour chaque groupe sont imprimées.</span><span class="sxs-lookup"><span data-stu-id="83d12-125">Specifies if all of the VAT entries for each group will be printed.</span></span>|  
    |<span data-ttu-id="83d12-126">**Afficher rétrofacturation**</span><span class="sxs-lookup"><span data-stu-id="83d12-126">**Show Chargeback**</span></span>|<span data-ttu-id="83d12-127">Indique si les écritures TVA et les écritures comptables avec des résumés fermés ou des taxes republiées seront imprimées.</span><span class="sxs-lookup"><span data-stu-id="83d12-127">Specifies if VAT entries and general ledger entries with closed summaries or reposted tax will be printed.</span></span>|  
    |<span data-ttu-id="83d12-128">**% TVA taux normal**</span><span class="sxs-lookup"><span data-stu-id="83d12-128">**Normal rate VAT %**</span></span>|<span data-ttu-id="83d12-129">Sélectionnez les taux de TVA courants actuels utilisés pour affecter les tarifs corrects aux groupes d'activités et de produits définis dans les paramètres de TVA.</span><span class="sxs-lookup"><span data-stu-id="83d12-129">Select the current typical VAT rates used to assign the correct rates to the business and product groups defined in the VAT settings.</span></span>|  
    |<span data-ttu-id="83d12-130">**% TVA taux réduit**</span><span class="sxs-lookup"><span data-stu-id="83d12-130">**Reduced rate VAT %**</span></span>|<span data-ttu-id="83d12-131">Sélectionnez les taux d'imposition réduits actuels utilisés pour affecter les taux corrects aux groupes d'activités et de produits définis dans les paramètres de TVA.</span><span class="sxs-lookup"><span data-stu-id="83d12-131">Select the current reduced tax rates used to assign the correct rates to the business and product groups defined in the VAT settings.</span></span>|  
    |<span data-ttu-id="83d12-132">**% TVA Taux spécial**</span><span class="sxs-lookup"><span data-stu-id="83d12-132">**Special rate VAT %**</span></span>|<span data-ttu-id="83d12-133">Sélectionnez les taux d'imposition spéciaux actuels utilisés pour affecter les taux corrects aux groupes d'activités et de produits définis dans les paramètres de TVA.</span><span class="sxs-lookup"><span data-stu-id="83d12-133">Select the current special tax rates used to assign the correct rates to the business and product groups defined in the VAT settings.</span></span>|  
    |<span data-ttu-id="83d12-134">**Compte général TVA achat investissements/opérations**</span><span class="sxs-lookup"><span data-stu-id="83d12-134">**Investment/Operating Purchase VAT G/L Account**</span></span>|<span data-ttu-id="83d12-135">Sélectionnez le compte général TVA.</span><span class="sxs-lookup"><span data-stu-id="83d12-135">Select the VAT general ledger account.</span></span>|  
    |<span data-ttu-id="83d12-136">**Groupe activités consom. perso.**</span><span class="sxs-lookup"><span data-stu-id="83d12-136">**Own Consumption Bus. Group**</span></span>|<span data-ttu-id="83d12-137">Sélectionnez le groupe d'activités et de produits pour votre propre consommation.</span><span class="sxs-lookup"><span data-stu-id="83d12-137">Select the business and product group for own consumptions.</span></span>|  
    |<span data-ttu-id="83d12-138">**Groupe activ. serv. étrang.**</span><span class="sxs-lookup"><span data-stu-id="83d12-138">**Service Foreign Bus. Group**</span></span>|<span data-ttu-id="83d12-139">Sélectionnez le groupe d'activités de service et de produits étrangers.</span><span class="sxs-lookup"><span data-stu-id="83d12-139">Select the foreign service business and product group.</span></span>|  
    |<span data-ttu-id="83d12-140">**Groupe activ. export.**</span><span class="sxs-lookup"><span data-stu-id="83d12-140">**Export Bus. Group**</span></span>|<span data-ttu-id="83d12-141">Sélectionnez le groupe d'activités et de produits pour les exportations.</span><span class="sxs-lookup"><span data-stu-id="83d12-141">Select the business and product group for exports.</span></span>|  

3.  <span data-ttu-id="83d12-142">Sélectionnez le bouton **Imprimer** pour imprimer la déclaration de TVA, ou le bouton **Aperçu** pour l'afficher à l'écran.</span><span class="sxs-lookup"><span data-stu-id="83d12-142">Choose the **Print** button to print the VAT statement or choose the **Preview** button to view it on the screen.</span></span>  

## <a name="see-also"></a><span data-ttu-id="83d12-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83d12-143">See Also</span></span>  
 <span data-ttu-id="83d12-144">[Taxe sur la valeur ajoutée, Suisse](swiss-value-added-tax.md) </span><span class="sxs-lookup"><span data-stu-id="83d12-144">[Swiss Value Added Tax](swiss-value-added-tax.md) </span></span>  
 [<span data-ttu-id="83d12-145">Taux de TVA pour la Suisse</span><span class="sxs-lookup"><span data-stu-id="83d12-145">VAT Rates for Switzerland</span></span>](vat-rates-for-switzerland.md)
