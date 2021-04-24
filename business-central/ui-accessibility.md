---
title: Fonctionnalités d’assistance
description: Raccourcis clavier et autres fonctionnalités d’assistance.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c303c39850e22d3df375838d42703133428b4c7d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772369"
---
# <a name="accessibility-and-keyboard-shortcuts"></a><span data-ttu-id="c83ea-103">Accessibilité et raccourcis clavier</span><span class="sxs-lookup"><span data-stu-id="c83ea-103">Accessibility and Keyboard Shortcuts</span></span>

<span data-ttu-id="c83ea-104">Cette rubrique fournit des informations sur les fonctionnalités qui rendent [!INCLUDE[prod_short](includes/prod_short.md)] accessible aux personnes handicapées.</span><span class="sxs-lookup"><span data-stu-id="c83ea-104">This topic provides information about the features that make [!INCLUDE[prod_short](includes/prod_short.md)] readily available to people with disabilities.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="c83ea-105">prend en charge les fonctionnalités d’accessibilité suivantes :</span><span class="sxs-lookup"><span data-stu-id="c83ea-105">supports the following accessibility features:</span></span>  

- <span data-ttu-id="c83ea-106">raccourcis clavier ;</span><span class="sxs-lookup"><span data-stu-id="c83ea-106">Keyboard shortcuts</span></span>

    <span data-ttu-id="c83ea-107">Pour plus d’informations, reportez-vous à [Raccourcis clavier](keyboard-shortcuts.md)</span><span class="sxs-lookup"><span data-stu-id="c83ea-107">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md)</span></span>

- <span data-ttu-id="c83ea-108">Navigation</span><span class="sxs-lookup"><span data-stu-id="c83ea-108">Navigation</span></span>  

- <span data-ttu-id="c83ea-109">En-têtes</span><span class="sxs-lookup"><span data-stu-id="c83ea-109">Headings</span></span>  

- <span data-ttu-id="c83ea-110">Texte secondaire pour les images et les liens</span><span class="sxs-lookup"><span data-stu-id="c83ea-110">Alternative text for images and links</span></span>  

- <span data-ttu-id="c83ea-111">Prise en charge des technologies d’assistance courantes</span><span class="sxs-lookup"><span data-stu-id="c83ea-111">Support for common assistive technologies</span></span>  

- <span data-ttu-id="c83ea-112">Utilisez les raccourcis clavier pour effectuer un zoom avant ou arrière sur n’importe quelle page</span><span class="sxs-lookup"><span data-stu-id="c83ea-112">Use keyboard shortcuts to zoom in or out on any page</span></span>

<!-- moved to separate article
##  <a name="Keyboard"></a> Keyboard Shortcuts in the browser
 [!INCLUDE[prod_short](includes/prod_short.md)] supports the keyboard shortcuts that are supported by most web browsers. The keyboard shortcuts described here refer to the U.S. keyboard layout. The layout of the keys on other keyboards may not correspond exactly to the keys on a U.S. keyboard.  

|To do this|Press|  
|----------------|-----------|  
|To move focus to the next or previous control or element on a page, such as buttons, fields, or items in a list.|Tab, Shift+Tab|  
|To enable or access the element or control that is in focus.|Enter|  
|To scroll items up and down in a list.|Up Arrow, Down Arrow|  
|To scroll columns of an item left and right in a list.|Left Arrow, Right Arrow|  
|To open a drop-down list or look up a value for a field.|Alt+Down Arrow|  
|To move focus to the next element outside the list.|Ctrl + Enter|  
|To see the transactions that resulted in a calculated value in a field.|Alt+Right Arrow|  

-->

## <a name="navigation"></a><a name="Navigation"></a> <span data-ttu-id="c83ea-113">Navigation</span><span class="sxs-lookup"><span data-stu-id="c83ea-113">Navigation</span></span>  
 <span data-ttu-id="c83ea-114">Vous pouvez naviguer entre les onglets et les actions du ruban, les éléments de la barre de navigation et d’autres contrôles sur les pages et états [!INCLUDE[prod_short](includes/prod_short.md)] à l’aide du clavier.</span><span class="sxs-lookup"><span data-stu-id="c83ea-114">You can navigate between the tabs and actions in the ribbon, elements in the navigation bar, and other controls on [!INCLUDE[prod_short](includes/prod_short.md)] pages and reports using the keyboard.</span></span> <span data-ttu-id="c83ea-115">Pour déplacer le focus d’un onglet, d’une action ou d’un contrôle vers un autre, appuyez sur la touche Tab pour avancer.</span><span class="sxs-lookup"><span data-stu-id="c83ea-115">To move the focus from one tab, action, or control to another, press the Tab key to move forward.</span></span> <span data-ttu-id="c83ea-116">Appuyez sur Maj+Tab pur reculer.</span><span class="sxs-lookup"><span data-stu-id="c83ea-116">Press Shift+Tab to move backward.</span></span>  

 <span data-ttu-id="c83ea-117">À l’aide de l’ordre de tabulation, vous pouvez également permuter entre la page principale du navigateur et les boîtes de dialogue de demande de confirmation, par exemple, ou la page de connexion.</span><span class="sxs-lookup"><span data-stu-id="c83ea-117">By using the tab order, you can also switch between the main browser page and dialog boxes that request confirmation, for example, or the login page.</span></span>  

## <a name="headings-in-content"></a><a name="Headings"></a> <span data-ttu-id="c83ea-118">En-têtes dans le contenu</span><span class="sxs-lookup"><span data-stu-id="c83ea-118">Headings in Content</span></span>
 
 <span data-ttu-id="c83ea-119">La source HTML du contenu [!INCLUDE[prod_short](includes/prod_short.md)] utilise des balises pour aider les utilisateurs de la technologie d’assistance à comprendre la structure et le contenu de la page.</span><span class="sxs-lookup"><span data-stu-id="c83ea-119">The HTML source for [!INCLUDE[prod_short](includes/prod_short.md)] content uses tags to help users of assistive technology to understand the structure and content of the page.</span></span> <span data-ttu-id="c83ea-120">Par exemple, sur les pages de liste, les colonnes sont définies dans les balises TH et les en-têtes de colonne sont définies avec l’attribut TITLE au sein de la balise.</span><span class="sxs-lookup"><span data-stu-id="c83ea-120">For example, on list pages, the columns are defined in TH tags and the column headings are set with TITLE attribute inside the tag.</span></span> <span data-ttu-id="c83ea-121">Les légendes des éléments, tels que les raccourcis, récapitulatifs et champs sont incluses dans les balises d’en-tête (H1, H2, H3 et H4).</span><span class="sxs-lookup"><span data-stu-id="c83ea-121">Captions for elements, such as FastTabs, FactBoxes, and fields are included in heading tags (H1, H2, H3, and H4).</span></span>  

## <a name="image-and-links"></a><a name="Images"></a> <span data-ttu-id="c83ea-122">Image et liens</span><span class="sxs-lookup"><span data-stu-id="c83ea-122">Image and Links</span></span>

 <span data-ttu-id="c83ea-123">Un texte descriptif pour les images est défini avec l’attribut ALT au sein de la balise IMG.</span><span class="sxs-lookup"><span data-stu-id="c83ea-123">A descriptive text for images is set with the ALT attribute inside the IMG tag.</span></span> <span data-ttu-id="c83ea-124">Un texte descriptif pour les liens hypertexte est défini avec l’attribut title au sein de la balise A.</span><span class="sxs-lookup"><span data-stu-id="c83ea-124">A descriptive text for hyperlinks is set with the title attribute inside the A tag.</span></span>  

## <a name="assistive-technologies"></a><a name="AssistiveTech"></a> <span data-ttu-id="c83ea-125">Technologies d’assistance</span><span class="sxs-lookup"><span data-stu-id="c83ea-125">Assistive Technologies</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="c83ea-126">prend en charge différentes technologies d’assistance, telles que le contraste élevé, les lecteurs d’écran et les logiciels de reconnaissance vocale.</span><span class="sxs-lookup"><span data-stu-id="c83ea-126">supports various assistive technologies, such as high contrast, screen readers, and voice recognition software.</span></span> <span data-ttu-id="c83ea-127">Certaines technologies d’assistance ne fonctionnent pas correctement avec certains éléments des pages [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="c83ea-127">Some assistive technologies may not work well with certain elements in [!INCLUDE[prod_short](includes/prod_short.md)] pages.</span></span>  

## <a name="zoom"></a><a name="zoom"></a> <span data-ttu-id="c83ea-128">Zoom</span><span class="sxs-lookup"><span data-stu-id="c83ea-128">Zoom</span></span>

<span data-ttu-id="c83ea-129">La plupart des navigateurs utilisent des raccourcis clavier standard pour effectuer un zoom avant et arrière sur la page en cours.</span><span class="sxs-lookup"><span data-stu-id="c83ea-129">Most browsers use standard keyboard shortcuts to zoom in and out on the current page.</span></span> <span data-ttu-id="c83ea-130">Ces raccourcis clavier ne sont pas spécifiques à [!INCLUDE [prod_short](includes/prod_short.md)], mais ils fonctionnent lorsque vous utilisez [!INCLUDE [prod_short](includes/prod_short.md)] dans un navigateur.</span><span class="sxs-lookup"><span data-stu-id="c83ea-130">These keyboard shortcuts are not specific to [!INCLUDE [prod_short](includes/prod_short.md)], but they work when you use [!INCLUDE [prod_short](includes/prod_short.md)] in a browser.</span></span> <span data-ttu-id="c83ea-131">Pour obtenir la liste des raccourcis clavier pris en charge, voir [Raccourcis clavier pour le zoom avant et arrière](keyboard-shortcuts.md#zoomshortcuts).</span><span class="sxs-lookup"><span data-stu-id="c83ea-131">For a list of supported keyboard shortcuts, see [Keyboard Shortcuts for Zooming In and Out](keyboard-shortcuts.md#zoomshortcuts).</span></span>  

## <a name="for-more-accessibility-information"></a><span data-ttu-id="c83ea-132">Informations supplémentaires sur l’accessibilité</span><span class="sxs-lookup"><span data-stu-id="c83ea-132">For more accessibility information</span></span>

<span data-ttu-id="c83ea-133">Vous trouverez des informations supplémentaires sur l’accessibilité des produits Microsoft et les technologies d’assistance sur le site [Accessibilité Microsoft](https://go.microsoft.com/fwlink/?LinkId=262160).</span><span class="sxs-lookup"><span data-stu-id="c83ea-133">You can find additional information about accessibility with Microsoft products and assistive technologies on the [Microsoft Accessibility](https://go.microsoft.com/fwlink/?LinkId=262160) site.</span></span>

## <a name="see-also"></a><span data-ttu-id="c83ea-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c83ea-134">See Also</span></span>

[<span data-ttu-id="c83ea-135">Préparation aux activités commerciales</span><span class="sxs-lookup"><span data-stu-id="c83ea-135">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
<span data-ttu-id="c83ea-136">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c83ea-136">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="c83ea-137">Forum Aux Questions</span><span class="sxs-lookup"><span data-stu-id="c83ea-137">Frequently Asked Questions</span></span>](across-faq.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]