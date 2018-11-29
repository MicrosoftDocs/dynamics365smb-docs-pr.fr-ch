---
title: Forum Aux Questions sur Tell Me | Microsoft Docs
description: "Cet article fournit des réponses aux questions que nos partenaires et clients posent souvent sur Tell Me."
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 74cd6b136cf5785237640b124472cd26aeff97de
ms.openlocfilehash: 70ab7fb07cda5ce9d86b3f39dd14321829e85a52
ms.contentlocale: fr-ch
ms.lasthandoff: 11/29/2018

---
# <a name="tell-me-faq"></a><span data-ttu-id="76287-103">FAQ Tell Me</span><span class="sxs-lookup"><span data-stu-id="76287-103">Tell Me FAQ</span></span>
<span data-ttu-id="76287-104">Cette rubrique répond aux questions que nos utilisateurs avancés posent souvent sur la nouvelle fonction Tell Me, qui a remplacé la fonction Recherche de page précédente connue comme **Recherche de pages et d'états**.</span><span class="sxs-lookup"><span data-stu-id="76287-104">This topic answers questions that our advanced users often ask about the new Tell Me feature, which has replaced the previous Page Search feature known as **Find Pages and Reports**.</span></span>

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a><span data-ttu-id="76287-105">Toutes les actions de ma page actuelle sont-elles détectables dans Tell Me ?</span><span class="sxs-lookup"><span data-stu-id="76287-105">Are all actions from my current page discoverable in Tell Me?</span></span>
<span data-ttu-id="76287-106">Non.</span><span class="sxs-lookup"><span data-stu-id="76287-106">No.</span></span> <span data-ttu-id="76287-107">Les actions dans les parties, telles que la partie Lignes vente ou Récapitulatifs, ne sont pas affichées dans Tell Me.</span><span class="sxs-lookup"><span data-stu-id="76287-107">Actions in parts, such as the Sales Lines part or FactBoxes, are not displayed in Tell Me.</span></span>

### <a name="are-the-results-in-tell-me-filtered-by-permissions"></a><span data-ttu-id="76287-108">Les résultats dans Tell Me sont-ils filtrés par autorisations ?</span><span class="sxs-lookup"><span data-stu-id="76287-108">Are the results in Tell Me filtered by permissions?</span></span>
<span data-ttu-id="76287-109">Si l'utilisateur n'a pas AccessByPermissions, les actions ne s'affichent pas.</span><span class="sxs-lookup"><span data-stu-id="76287-109">If the user does not have AccessByPermissions then actions are not displayed.</span></span> <span data-ttu-id="76287-110">Cependant, les pages et les états sont visibles dans les résultats mais nécessitent que l'utilisateur soit autorisé à y accéder.</span><span class="sxs-lookup"><span data-stu-id="76287-110">However, pages and reports appear in the results but require that the user has permission to access them.</span></span> <span data-ttu-id="76287-111">Un message s'affiche si l'utilisateur n'est pas autorisé à afficher l'objet.</span><span class="sxs-lookup"><span data-stu-id="76287-111">A message will display if the user does not have permission to view the object.</span></span>

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a><span data-ttu-id="76287-112">La fonction Tell Me affiche-t-elle le contenu de mes personnalisations ou des extensions tierces installées ?</span><span class="sxs-lookup"><span data-stu-id="76287-112">Does Tell Me display content from my customizations or installed third-party extensions?</span></span>
<span data-ttu-id="76287-113">Les actions, les pages, et les états qui proviennent d'extensions sont extraits par Tell Me, mais la documentation d'aide personnalisée ne l'est pas.</span><span class="sxs-lookup"><span data-stu-id="76287-113">Actions, pages, and reports that originate from extensions are picked up by Tell Me, but custom help documentation is not.</span></span> <span data-ttu-id="76287-114">Pour des informations techniques sur la manière rédiger des pages et des états personnalisés détectables, voir [Ajout de pages et d'états à rechercher](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).</span><span class="sxs-lookup"><span data-stu-id="76287-114">For technical information about how to make custom pages and reports discoverable, see [Adding Pages and Reports to Search](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).</span></span>

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a><span data-ttu-id="76287-115">Quelles sont les différences avec la recherche de page précédente ?</span><span class="sxs-lookup"><span data-stu-id="76287-115">What makes this different from what was previously known as Page Search?</span></span>
<span data-ttu-id="76287-116">La recherche de page s'est transformée en Tell Me pour vous aider à obtenir rapidement des résultats.</span><span class="sxs-lookup"><span data-stu-id="76287-116">Page Search has evolved into Tell Me to help you get work done quickly.</span></span> <span data-ttu-id="76287-117">La recherche de page pouvait uniquement vous aider à accéder aux pages ou aux états.</span><span class="sxs-lookup"><span data-stu-id="76287-117">Page Search could only help you navigate to pages or reports.</span></span> <span data-ttu-id="76287-118">À un niveau technique, Tell Me n'est plus basé sur le concept MenuSuite hérité.</span><span class="sxs-lookup"><span data-stu-id="76287-118">At a technical level, Tell Me is no longer based on the legacy MenuSuite concept.</span></span>

### <a name="i-use-on-premises-included365finincludesd365finmdmd-does-that-include-tell-me"></a><span data-ttu-id="76287-119">J'utilise [!INCLUDE[d365fin](includes/d365fin_md.md)] local.</span><span class="sxs-lookup"><span data-stu-id="76287-119">I use on-premises [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="76287-120">La fonction Tell Me est-elle incluse ?</span><span class="sxs-lookup"><span data-stu-id="76287-120">Does that include Tell Me?</span></span>
<span data-ttu-id="76287-121">Vous pouvez utiliser Tell Me dans le client Web local pour trouver des actions, des pages, et des états, mais pas la documentation.</span><span class="sxs-lookup"><span data-stu-id="76287-121">You can use Tell Me in the on-premises Web Client to find actions, pages, and reports, but not documentation.</span></span> <span data-ttu-id="76287-122">Les utilisateurs se connectant à [!INCLUDE[d365fin](includes/d365fin_md.md)] depuis le client Dynamics NAV continuent d'utiliser la recherche de page.</span><span class="sxs-lookup"><span data-stu-id="76287-122">Users connecting to [!INCLUDE[d365fin](includes/d365fin_md.md)] from the Dynamics NAV client continue to use Page Search.</span></span>

### <a name="is-tell-me-available-for-all-form-factors"></a><span data-ttu-id="76287-123">La fonction Tell Me est-elle disponible pour tous les facteurs d'écrans ?</span><span class="sxs-lookup"><span data-stu-id="76287-123">Is Tell Me available for all form factors?</span></span>
<span data-ttu-id="76287-124">Tell Me est uniquement disponible dans le client Web ou l'application de bureau Windows.</span><span class="sxs-lookup"><span data-stu-id="76287-124">Tell Me is only available in the Web Client or Windows desktop app.</span></span>

### <a name="are-the-documentation-results-available-in-any-language"></a><span data-ttu-id="76287-125">Les résultats de la documentation sont-ils disponibles dans toutes les langues ?</span><span class="sxs-lookup"><span data-stu-id="76287-125">Are the documentation results available in any language?</span></span>
<span data-ttu-id="76287-126">Les articles de l'aide s'affichent dans la langue spécifiée dans **Mes paramètres**, si l'aide est disponible dans cette langue.</span><span class="sxs-lookup"><span data-stu-id="76287-126">The help articles display in the language you have specified in **My Settings**, if help is available in that language.</span></span>

## <a name="see-also"></a><span data-ttu-id="76287-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76287-127">See Also</span></span>  
[<span data-ttu-id="76287-128">Recherche de fonctions et d'informations</span><span class="sxs-lookup"><span data-stu-id="76287-128">Finding Features and Information</span></span>](ui-search.md)

