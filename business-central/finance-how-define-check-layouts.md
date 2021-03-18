---
title: Spécifier la mise en page d’un chèque| Microsoft Docs
description: Vous pouvez concevoir et imprimer vos chèques dans différents formats pour respecter des normes.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ac980cb4b64a39b7ed912a49b06c179ffc7219d9
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386514"
---
# <a name="select-a-check-layout"></a><span data-ttu-id="04760-103">Sélectionner une mise en page de chèque</span><span class="sxs-lookup"><span data-stu-id="04760-103">Select a Check Layout</span></span>
<span data-ttu-id="04760-104">Vous pouvez concevoir vos chèques de sorte à respecter les normes fixées par les autorités locales.</span><span class="sxs-lookup"><span data-stu-id="04760-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="04760-105">Vous pouvez imprimer des images de chèques en anglais, en français ou en espagnol.</span><span class="sxs-lookup"><span data-stu-id="04760-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="04760-106">Les chèques sont conçus pour être imprimés aux formats d’image de chèques américains et canadiens, soit au format chèque-talon-chèque, soit au format talon-talon-chèque.</span><span class="sxs-lookup"><span data-stu-id="04760-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-select-a-check-layout"></a><span data-ttu-id="04760-107">Pour sélectionner une mise en page de chèque</span><span class="sxs-lookup"><span data-stu-id="04760-107">To select a check layout</span></span>
1. <span data-ttu-id="04760-108">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Sélection des états : Compte bancaire**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="04760-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="04760-109">Sur la page **Sélection des états : Banque**, dans le champ **Utilisation**, sélectionnez **Chèque**</span><span class="sxs-lookup"><span data-stu-id="04760-109">On the **Report Selection - Bank Acc.** page, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="04760-110">Sélectionnez l’un des ID état suivants.</span><span class="sxs-lookup"><span data-stu-id="04760-110">Select one of the following report IDs.</span></span>

| <span data-ttu-id="04760-111">ID état</span><span class="sxs-lookup"><span data-stu-id="04760-111">Report ID</span></span> | <span data-ttu-id="04760-112">Nom état</span><span class="sxs-lookup"><span data-stu-id="04760-112">Report Name</span></span> | <span data-ttu-id="04760-113">Description</span><span class="sxs-lookup"><span data-stu-id="04760-113">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="04760-114">1401</span><span class="sxs-lookup"><span data-stu-id="04760-114">1401</span></span> |<span data-ttu-id="04760-115">Activer</span><span class="sxs-lookup"><span data-stu-id="04760-115">Check</span></span> |<span data-ttu-id="04760-116">Il s’agit de l’état par défaut.</span><span class="sxs-lookup"><span data-stu-id="04760-116">This is the default report.</span></span> |
| <span data-ttu-id="04760-117">10411</span><span class="sxs-lookup"><span data-stu-id="04760-117">10411</span></span> |<span data-ttu-id="04760-118">Chèque (Talon/Talon/Chèque)</span><span class="sxs-lookup"><span data-stu-id="04760-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="04760-119">Cet état est conçu pour imprimer des chèques au format talon/talon/chèque.</span><span class="sxs-lookup"><span data-stu-id="04760-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="04760-120">10412</span><span class="sxs-lookup"><span data-stu-id="04760-120">10412</span></span> |<span data-ttu-id="04760-121">Chèque (Talon/Chèque/Talon)</span><span class="sxs-lookup"><span data-stu-id="04760-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="04760-122">Cet état est conçu pour imprimer des chèques au format talon/chèque/talon.</span><span class="sxs-lookup"><span data-stu-id="04760-122">This report is designed to print checks in a stub/check/stub format.</span></span> |
| <span data-ttu-id="04760-123">10413</span><span class="sxs-lookup"><span data-stu-id="04760-123">10413</span></span> |<span data-ttu-id="04760-124">Trois chèques par page</span><span class="sxs-lookup"><span data-stu-id="04760-124">Three Checks per Page</span></span> |<span data-ttu-id="04760-125">Cet état est conçu pour imprimer trois chèques sur chaque page.</span><span class="sxs-lookup"><span data-stu-id="04760-125">This report is designed to print three checks on each page.</span></span> |

<span data-ttu-id="04760-126">Une fois que vous avez défini les mises en page de chèques, vous pouvez imprimer des chèques à partir de la page **Feuille paiement**.</span><span class="sxs-lookup"><span data-stu-id="04760-126">When you have set up check layouts, you can print checks from the **Payment Journal** page.</span></span> <span data-ttu-id="04760-127">Pour plus d’informations, reportez-vous à [Utilisation des chèques](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="04760-127">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

<span data-ttu-id="04760-128">Pour modifier l’une de ces mises en page de chèque par défaut, utilisez l’intégration Word ou RDLC.</span><span class="sxs-lookup"><span data-stu-id="04760-128">To change one of these default check layouts, use either the Word or the RDLC integration to do so.</span></span> <span data-ttu-id="04760-129">Pour plus d’informations, voir [Créer et modifier des présentations de rapport personnalisées](ui-how-create-custom-report-layout.md).</span><span class="sxs-lookup"><span data-stu-id="04760-129">For more information, see [Create and Modify Custom Report Layouts](ui-how-create-custom-report-layout.md).</span></span>

## <a name="using-micr-and-security-fonts"></a><span data-ttu-id="04760-130">Utilisation des polices de sécurité et MICR</span><span class="sxs-lookup"><span data-stu-id="04760-130">Using MICR and Security Fonts</span></span>
<span data-ttu-id="04760-131">La version en ligne de [!INCLUDE[prod_short](includes/prod_short.md)] contient des polices préinstallées sur les serveurs qui peuvent être utilisées lors de la définition des mises en page de chèque.</span><span class="sxs-lookup"><span data-stu-id="04760-131">The online version of [!INCLUDE[prod_short](includes/prod_short.md)] contains pre-installed fonts on the servers that can be used when defining check layouts.</span></span> <span data-ttu-id="04760-132">Ci-après, découvrez les polices disponibles et des liens vers des informations détaillées fournies par les fournisseurs tiers de polices.</span><span class="sxs-lookup"><span data-stu-id="04760-132">The following outlines which fonts are available and has links to detailed information by the 3rd-party suppliers of the fonts.</span></span>

> [!Important]
> <span data-ttu-id="04760-133">Les polices de sécurité de chèque et MICR de Microsoft Dynamics [!INCLUDE[prod_short](includes/prod_short.md)] sont concédées sous licence dans un package de polices d’IDAutomation.com, Inc. Ces produits ne peuvent être utilisés que dans le cadre et en relation avec Microsoft Dynamics [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="04760-133">MICR and check security fonts in Microsoft Dynamics [!INCLUDE[prod_short](includes/prod_short.md)] are licensed in a font package from IDAutomation.com, Inc. These products may only be used as part of and in connection with Microsoft Dynamics [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

<span data-ttu-id="04760-134">Dans la mise à jour 15.3 et les versions ultérieures, les polices MICR sont installées et disponibles à l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="04760-134">In update 15.3 and newer, Magnetic Ink Character Recognition (MICR) fonts are installed and available to use.</span></span> <span data-ttu-id="04760-135">Les normes E-13B et CMC-7 sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="04760-135">Both the E-13B and the CMC-7 standards are supported.</span></span> <span data-ttu-id="04760-136">En plus des polices MICR, des polices de sécurité spéciales sont disponibles pour générer du texte, des noms, des montants et les symboles monétaires Dollar, Euro, Pound et Yen, qui sont difficiles à modifier une fois qu’un chèque a été imprimé.</span><span class="sxs-lookup"><span data-stu-id="04760-136">In addition to MICR fonts, special security fonts are available to generate text, names, amounts, and the currency symbols Dollar, Euro, Pound, and Yen, which are hard to tamper with once a check has been printed.</span></span>

> [!NOTE]
> <span data-ttu-id="04760-137">Pour des raisons de sécurité et juridiques, vous ne pouvez pas télécharger de polices personnalisées sur l’environnement [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="04760-137">For security and legal reasons, you cannot upload custom fonts to the [!INCLUDE[prod_short](includes/prod_short.md)] environment.</span></span>

### <a name="micr-e-13b-specifications"></a><span data-ttu-id="04760-138">Spécifications MICR E-13B</span><span class="sxs-lookup"><span data-stu-id="04760-138">MICR E-13B Specifications</span></span>
<span data-ttu-id="04760-139">Voici un résumé des spécifications des polices MICR E-13B qui peuvent se révéler utiles lors du calibrage des polices sur les mises en page de chèque avec des imprimantes MICR spécifiques.</span><span class="sxs-lookup"><span data-stu-id="04760-139">The following summarizes specifications for the MICR E-13B fonts that may be useful when calibrating fonts to be on check layouts with specific MICR printers.</span></span>

<span data-ttu-id="04760-140">![Spécifications MICR E-13B](media/font_MICR_E-13B_Specifications.png "Spécifications MICR E-13B")</span><span class="sxs-lookup"><span data-stu-id="04760-140">![MICR E-13B Specifications](media/font_MICR_E-13B_Specifications.png "MICR E-13B Specifications")</span></span>

### <a name="delimiter-characters"></a><span data-ttu-id="04760-141">Caractères séparateurs</span><span class="sxs-lookup"><span data-stu-id="04760-141">Delimiter characters</span></span>
<span data-ttu-id="04760-142">![Caractères séparateurs](media/font-micr-letters.png "Caractères séparateurs")</span><span class="sxs-lookup"><span data-stu-id="04760-142">![Delimiter characters](media/font-micr-letters.png "Delimiter characters")</span></span>

<span data-ttu-id="04760-143">La spécification complète des polices MICR E-13B est disponible dans la documentation du fournisseur ici : (https://www.idautomation.com/micr-fonts/e13b/).</span><span class="sxs-lookup"><span data-stu-id="04760-143">The full specification of MICR E-13B fonts can be found in the supplier's documentation here: (https://www.idautomation.com/micr-fonts/e13b/).</span></span>

### <a name="micr-cmc-7-specifications"></a><span data-ttu-id="04760-144">Spécifications MICR CMC-7</span><span class="sxs-lookup"><span data-stu-id="04760-144">MICR CMC-7 Specifications</span></span>
<span data-ttu-id="04760-145">Les polices CMC-7 suivantes sont disponibles dans [!INCLUDE[prod_short](includes/prod_short.md)] en ligne :</span><span class="sxs-lookup"><span data-stu-id="04760-145">The following CMC-7 fonts are available in [!INCLUDE[prod_short](includes/prod_short.md)] online:</span></span>

- <span data-ttu-id="04760-146">IDAutomationCMC7</span><span class="sxs-lookup"><span data-stu-id="04760-146">IDAutomationCMC7</span></span>
- <span data-ttu-id="04760-147">IDAutomationCMC7n10</span><span class="sxs-lookup"><span data-stu-id="04760-147">IDAutomationCMC7n10</span></span>
- <span data-ttu-id="04760-148">IDAutomationCMC7n25</span><span class="sxs-lookup"><span data-stu-id="04760-148">IDAutomationCMC7n25</span></span>
-   <span data-ttu-id="04760-149">IDAutomationCMC7n40</span><span class="sxs-lookup"><span data-stu-id="04760-149">IDAutomationCMC7n40</span></span>

<span data-ttu-id="04760-150">Voici un résumé des spécifications des polices MICR CMC-7 qui peuvent se révéler utiles lors du calibrage des polices sur les mises en page de chèque avec des imprimantes MICR spécifiques.</span><span class="sxs-lookup"><span data-stu-id="04760-150">The following summarizes specifications for the MICR CMC-7 fonts that may be useful when calibrating fonts to be on check layouts with specific MICR printers.</span></span>

<span data-ttu-id="04760-151">![Spécifications MICR CMC-7](media/font_MICR_CMC-7_Specifications.png "Spécifications MICR CMC-7")</span><span class="sxs-lookup"><span data-stu-id="04760-151">![MICR CMC-7 Specifications](media/font_MICR_CMC-7_Specifications.png "MICR CMC-7 Specifications")</span></span>

### <a name="delimiter-characters"></a><span data-ttu-id="04760-152">Caractères séparateurs</span><span class="sxs-lookup"><span data-stu-id="04760-152">Delimiter characters</span></span>
<span data-ttu-id="04760-153">![Caractères séparateurs](media/font-cmc7-letters.png "Caractères séparateurs")</span><span class="sxs-lookup"><span data-stu-id="04760-153">![Delimiter characters](media/font-cmc7-letters.png "Delimiter characters")</span></span>

<span data-ttu-id="04760-154">La spécification complète des polices MICR CMC-7 est disponible dans la documentation du fournisseur ici : (http://www.idautomation.com/micr-fonts/cmc7/).</span><span class="sxs-lookup"><span data-stu-id="04760-154">The full specification of MICR CMC-7 fonts can be found in the supplier's documentation here: (http://www.idautomation.com/micr-fonts/cmc7/).</span></span>

### <a name="secure-font-specifications"></a><span data-ttu-id="04760-155">Spécifications des polices sécurisées</span><span class="sxs-lookup"><span data-stu-id="04760-155">Secure Font Specifications</span></span>
<span data-ttu-id="04760-156">Voici un résumé des spécifications des polices de sécurité des chèques qui peuvent se révéler utiles lors du calibrage des polices sur les mises en page de chèque avec des imprimantes MICR spécifiques.</span><span class="sxs-lookup"><span data-stu-id="04760-156">The following summarizes specifications for check security fonts that may be useful when calibrating fonts to be on check layouts with specific MICR printers.</span></span>

<span data-ttu-id="04760-157">![Spécifications des polices de sécurité des chèques](media/font_check-security-font_Specifications.png "Spécifications des polices de sécurité des chèques")</span><span class="sxs-lookup"><span data-stu-id="04760-157">![Check Security Font Specifications](media/font_check-security-font_Specifications.png "Check Security Font Specifications")</span></span>

<span data-ttu-id="04760-158">La spécification complète des polices de sécurité des chèques est disponible dans la documentation du fournisseur ici : (https://www.idautomation.com/security-fonts/).</span><span class="sxs-lookup"><span data-stu-id="04760-158">The full specification of check security fonts can be found in the supplier's documentation here: (https://www.idautomation.com/security-fonts/).</span></span>

<span data-ttu-id="04760-159">Les polices à d’autres fins sont également disponibles dans [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="04760-159">Fonts for other purposes are also available in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="04760-160">Pour plus d’informations, voir [Polices disponibles](ui-fonts.md)</span><span class="sxs-lookup"><span data-stu-id="04760-160">For more information, see [Available Fonts](ui-fonts.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="04760-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04760-161">See Also</span></span>
[<span data-ttu-id="04760-162">Créer et modifier des présentations de rapport personnalisées</span><span class="sxs-lookup"><span data-stu-id="04760-162">Create and Modify Custom Report Layouts</span></span>](ui-how-create-custom-report-layout.md)  
[<span data-ttu-id="04760-163">Polices de Business Central</span><span class="sxs-lookup"><span data-stu-id="04760-163">Fonts in Business Central</span></span>](ui-fonts.md)  
[<span data-ttu-id="04760-164">Gestion des comptes fournisseur</span><span class="sxs-lookup"><span data-stu-id="04760-164">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="04760-165">[Rapprochement de comptes bancaires](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="04760-165">[Reconciling Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="04760-166">Exécution des processus de clôture d’exercice</span><span class="sxs-lookup"><span data-stu-id="04760-166">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="04760-167">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="04760-167">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="04760-168">Fonctionnalités marché</span><span class="sxs-lookup"><span data-stu-id="04760-168">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]