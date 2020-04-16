---
title: Fonctionnalités d'assistance
description: Raccourcis clavier et autres fonctionnalités d'assistance.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 1098e0998369e15bd9484ba33b808b9b435b538c
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3192138"
---
# <a name="accessibility-and-keyboard-shortcuts"></a><span data-ttu-id="4fbd0-103">Accessibilité et raccourcis clavier</span><span class="sxs-lookup"><span data-stu-id="4fbd0-103">Accessibility and Keyboard Shortcuts</span></span>
<span data-ttu-id="4fbd0-104">Cette rubrique fournit des informations sur les fonctionnalités qui rendent [!INCLUDE[d365fin](includes/d365fin_md.md)] accessible aux personnes handicapées.</span><span class="sxs-lookup"><span data-stu-id="4fbd0-104">This topic provides information about the features that make [!INCLUDE[d365fin](includes/d365fin_md.md)] readily available to people with disabilities.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="4fbd0-105">prend en charge les fonctionnalités d'accessibilité suivantes :</span><span class="sxs-lookup"><span data-stu-id="4fbd0-105">supports the following accessibility features:</span></span>  

-   <span data-ttu-id="4fbd0-106">raccourcis clavier ;</span><span class="sxs-lookup"><span data-stu-id="4fbd0-106">Keyboard shortcuts</span></span>

    <span data-ttu-id="4fbd0-107">Pour plus d'informations, reportez-vous à [Raccourcis clavier](keyboard-shortcuts.md)</span><span class="sxs-lookup"><span data-stu-id="4fbd0-107">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md)</span></span>

-   <span data-ttu-id="4fbd0-108">Navigation</span><span class="sxs-lookup"><span data-stu-id="4fbd0-108">Navigation</span></span>  

-   <span data-ttu-id="4fbd0-109">En-têtes</span><span class="sxs-lookup"><span data-stu-id="4fbd0-109">Headings</span></span>  

-   <span data-ttu-id="4fbd0-110">Texte secondaire pour les images et les liens</span><span class="sxs-lookup"><span data-stu-id="4fbd0-110">Alternative text for images and links</span></span>  

-   <span data-ttu-id="4fbd0-111">Prise en charge des technologies d'assistance courantes</span><span class="sxs-lookup"><span data-stu-id="4fbd0-111">Support for common assistive technologies</span></span>  

<!-- moved to separate article
##  <a name="Keyboard"></a> Keyboard Shortcuts in the browser
 [!INCLUDE[d365fin](includes/d365fin_md.md)] supports the keyboard shortcuts that are supported by most web browsers. The keyboard shortcuts described here refer to the U.S. keyboard layout. The layout of the keys on other keyboards may not correspond exactly to the keys on a U.S. keyboard.  

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

##  <a name="navigation"></a><a name="Navigation"></a> <span data-ttu-id="4fbd0-112">Navigation</span><span class="sxs-lookup"><span data-stu-id="4fbd0-112">Navigation</span></span>  
 <span data-ttu-id="4fbd0-113">Vous pouvez naviguer entre les onglets et les actions du ruban, les éléments de la barre de navigation et d'autres contrôles sur les pages et états [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide du clavier.</span><span class="sxs-lookup"><span data-stu-id="4fbd0-113">You can navigate between the tabs and actions in the ribbon, elements in the navigation bar, and other controls on [!INCLUDE[d365fin](includes/d365fin_md.md)] pages and reports using the keyboard.</span></span> <span data-ttu-id="4fbd0-114">Pour déplacer le focus d'un onglet, d'une action ou d'un contrôle vers un autre, appuyez sur la touche Tab pour avancer.</span><span class="sxs-lookup"><span data-stu-id="4fbd0-114">To move the focus from one tab, action, or control to another, press the Tab key to move forward.</span></span> <span data-ttu-id="4fbd0-115">Appuyez sur Maj+Tab pur reculer.</span><span class="sxs-lookup"><span data-stu-id="4fbd0-115">Press Shift+Tab to move backward.</span></span>  

 <span data-ttu-id="4fbd0-116">À l'aide de l'ordre de tabulation, vous pouvez également permuter entre la page principale du navigateur et les boîtes de dialogue de demande de confirmation, par exemple, ou la page de connexion.</span><span class="sxs-lookup"><span data-stu-id="4fbd0-116">By using the tab order, you can also switch between the main browser page and dialog boxes that request confirmation, for example, or the login page.</span></span>  

##  <a name="headings"></a><a name="Headings"></a> <span data-ttu-id="4fbd0-117">En-têtes</span><span class="sxs-lookup"><span data-stu-id="4fbd0-117">Headings</span></span>  
 <span data-ttu-id="4fbd0-118">La source HTML du contenu [!INCLUDE[d365fin](includes/d365fin_md.md)] utilise des balises pour aider les utilisateurs de la technologie d'assistance à comprendre la structure et le contenu de la page.</span><span class="sxs-lookup"><span data-stu-id="4fbd0-118">The HTML source for [!INCLUDE[d365fin](includes/d365fin_md.md)] content uses tags to help users of assistive technology to understand the structure and content of the page.</span></span> <span data-ttu-id="4fbd0-119">Par exemple, sur les pages de liste, les colonnes sont définies dans les balises TH et les en-têtes de colonne sont définies avec l'attribut TITLE au sein de la balise.</span><span class="sxs-lookup"><span data-stu-id="4fbd0-119">For example, on list pages, the columns are defined in TH tags and the column headings are set with TITLE attribute inside the tag.</span></span> <span data-ttu-id="4fbd0-120">Les légendes des éléments, tels que les raccourcis, récapitulatifs et champs sont incluses dans les balises d'en-tête (H1, H2, H3 et H4).</span><span class="sxs-lookup"><span data-stu-id="4fbd0-120">Captions for elements, such as FastTabs, FactBoxes, and fields are included in heading tags (H1, H2, H3, and H4).</span></span>  

##  <a name="image-and-links"></a><a name="Images"></a> <span data-ttu-id="4fbd0-121">Image et liens</span><span class="sxs-lookup"><span data-stu-id="4fbd0-121">Image and Links</span></span>  
 <span data-ttu-id="4fbd0-122">Un texte descriptif pour les images est défini avec l'attribut ALT au sein de la balise IMG.</span><span class="sxs-lookup"><span data-stu-id="4fbd0-122">A descriptive text for images is set with the ALT attribute inside the IMG tag.</span></span> <span data-ttu-id="4fbd0-123">Un texte descriptif pour les liens hypertexte est défini avec l'attribut title au sein de la balise A.</span><span class="sxs-lookup"><span data-stu-id="4fbd0-123">A descriptive text for hyperlinks is set with the title attribute inside the A tag.</span></span>  

##  <a name="assistive-technologies"></a><a name="AssistiveTech"></a> <span data-ttu-id="4fbd0-124">Technologies d'assistance</span><span class="sxs-lookup"><span data-stu-id="4fbd0-124">Assistive Technologies</span></span>  
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="4fbd0-125">prend en charge différentes technologies d'assistance, telles que le contraste élevé, les lecteurs d'écran et les logiciels de reconnaissance vocale.</span><span class="sxs-lookup"><span data-stu-id="4fbd0-125">supports various assistive technologies, such as high contrast, screen readers, and voice recognition software.</span></span> <span data-ttu-id="4fbd0-126">Certaines technologies d'assistance ne fonctionnent pas correctement avec certains éléments des pages [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="4fbd0-126">Some assistive technologies may not work well with certain elements in [!INCLUDE[d365fin](includes/d365fin_md.md)] pages.</span></span>  

## <a name="for-more-accessibility-information"></a><span data-ttu-id="4fbd0-127">Informations supplémentaires sur l'accessibilité</span><span class="sxs-lookup"><span data-stu-id="4fbd0-127">For more accessibility information</span></span>  
<span data-ttu-id="4fbd0-128">Vous trouverez des informations supplémentaires sur l'accessibilité des produits Microsoft et les technologies d'assistance sur le site [Accessibilité Microsoft](https://go.microsoft.com/fwlink/?LinkId=262160).</span><span class="sxs-lookup"><span data-stu-id="4fbd0-128">You can find additional information about accessibility with Microsoft products and assistive technologies on the [Microsoft Accessibility](https://go.microsoft.com/fwlink/?LinkId=262160) site.</span></span>

## <a name="see-also"></a><span data-ttu-id="4fbd0-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fbd0-129">See Also</span></span>
[<span data-ttu-id="4fbd0-130">Mise en route</span><span class="sxs-lookup"><span data-stu-id="4fbd0-130">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="4fbd0-131">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4fbd0-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="4fbd0-132">Forum Aux Questions</span><span class="sxs-lookup"><span data-stu-id="4fbd0-132">Frequently Asked Questions</span></span>](across-faq.md)  
