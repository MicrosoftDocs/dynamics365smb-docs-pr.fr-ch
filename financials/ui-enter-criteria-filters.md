---
title: "Définir les critères de recherche pour les filtres | Microsoft Docs"
description: "Décrit comment utiliser les filtres, par exemple le filtre rapide, pour préciser les résultats que vous obtenez lorsque vous recherchez des données."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 86ca45493081d9dbd229548f7c560e1df4e1c7c3
ms.contentlocale: fr-ch
ms.lasthandoff: 09/11/2017

---
# <a name="entering-criteria-in-filters"></a><span data-ttu-id="1f208-103">Saisir les critères pour les filtres</span><span class="sxs-lookup"><span data-stu-id="1f208-103">Entering Criteria in Filters</span></span>
<span data-ttu-id="1f208-104">Lorsque vous souhaitez rechercher des données, telles que des noms de client, des adresses ou des groupes de produits, vous saisissez des critères.</span><span class="sxs-lookup"><span data-stu-id="1f208-104">When you want to search for data, such as customer names, addresses, or product groups, you enter criteria.</span></span> <span data-ttu-id="1f208-105">Dans vos critères de recherche, vous pouvez utiliser tous les chiffres et toutes les lettres que vous utilisez habituellement dans ce champ spécifique.</span><span class="sxs-lookup"><span data-stu-id="1f208-105">In search criteria you can use all the numbers and letters that you normally use in the specific field.</span></span> <span data-ttu-id="1f208-106">En plus, vous pouvez utiliser des symboles spéciaux pour filtrer davantage les résultats.</span><span class="sxs-lookup"><span data-stu-id="1f208-106">In addition, you can use special symbols to further filter the results.</span></span>

## <a name="searching-using-the-quick-filter"></a><span data-ttu-id="1f208-107">Rechercher à l'aide du filtre rapide</span><span class="sxs-lookup"><span data-stu-id="1f208-107">Searching using the Quick Filter</span></span>
<span data-ttu-id="1f208-108">Vous pouvez ajouter des filtres pour l'ensemble des pages en utilisant le filtre rapide.</span><span class="sxs-lookup"><span data-stu-id="1f208-108">You can add filters to all pages by using the Quick Filter.</span></span> <span data-ttu-id="1f208-109">Vous activez le filtre rapide sélectionnant l'icône de loupe dans le coin supérieur droit d'une page.</span><span class="sxs-lookup"><span data-stu-id="1f208-109">The Quick Filter is enabled by choosing the magnifier icon in the top right corner of a page.</span></span> <span data-ttu-id="1f208-110">Ce type de filtre est utilisé pour une saisie rapide des critères.</span><span class="sxs-lookup"><span data-stu-id="1f208-110">This filtering type is used for a fast entry of criteria.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="1f208-111">Le Filtre rapide facilite l'accès aux données de filtre par la saisie de texte simple, mais fournit également un grand nombre d'options de critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="1f208-111">The Quick Filter provides an easy access to filter data by entering plain text, but does also provide a lot of search criteria options.</span></span> <span data-ttu-id="1f208-112">Selon que vous saisissez du texte simple ou du texte comprenant des symboles, le Filtre rapide se comporte de façon différente.</span><span class="sxs-lookup"><span data-stu-id="1f208-112">Depending on whether you enter plain text or text including symbols, the Quick Filter behaves differently.</span></span>  

* <span data-ttu-id="1f208-113">Si vous saisissez du texte simple dans les critères de recherche, le critère de recherche est interprété comme une recherche insensible à la casse qui contient un certain texte.</span><span class="sxs-lookup"><span data-stu-id="1f208-113">If you enter plain text in the search criteria, the search criteria is interpreted as a case insensitive search that contains certain text.</span></span>  
* <span data-ttu-id="1f208-114">Si vous saisissez du texte comprenant des symboles dans les critères de recherche, le critère de recherche est interprété exactement comme vous l'avez saisi, et la recherche distingue les majuscules et les minuscules.</span><span class="sxs-lookup"><span data-stu-id="1f208-114">If you enter text including symbols in the search criteria, the search criteria is interpreted exactly as you entered it, and the search is case sensitive.</span></span>

### <a name="quick-filter-criteria"></a><span data-ttu-id="1f208-115">Critères de filtre rapide</span><span class="sxs-lookup"><span data-stu-id="1f208-115">Quick filter criteria</span></span>
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH><span data-ttu-id="1f208-116">Critères de recherche</span><span class="sxs-lookup"><span data-stu-id="1f208-116">Search Criteria</span></span></TH>
    <TH><span data-ttu-id="1f208-117">Interprété comme...</span><span class="sxs-lookup"><span data-stu-id="1f208-117">Interpreted as...</span></span></TH>
    <TH><span data-ttu-id="1f208-118">Renvoie...</span><span class="sxs-lookup"><span data-stu-id="1f208-118">Returns...</span></span></TH>
  </TR>
  <TR>
    <TD><span data-ttu-id="1f208-119">man</span><span class="sxs-lookup"><span data-stu-id="1f208-119">man</span></span></TD>
    <TD><span data-ttu-id="1f208-120">@&#42;man&#42;</span><span class="sxs-lookup"><span data-stu-id="1f208-120">@&#42;man&#42;</span></span></TD>
    <TD><span data-ttu-id="1f208-121">Tous les enregistrements qui contiennent le texte <b>man</b> et ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="1f208-121">All records that contain the text <b>man</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="1f208-122">se</span><span class="sxs-lookup"><span data-stu-id="1f208-122">se</span></span></TD>
    <TD><span data-ttu-id="1f208-123">@&#42;se&#42;</span><span class="sxs-lookup"><span data-stu-id="1f208-123">@&#42;se&#42;</span></span></TD>
    <TD><span data-ttu-id="1f208-124">Tous les enregistrements qui contiennent le texte <b>se</b> et ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="1f208-124">All records that contain the text <b>se</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="1f208-125">Man&#42;</span><span class="sxs-lookup"><span data-stu-id="1f208-125">Man&#42;</span></span></TD>
    <TD><span data-ttu-id="1f208-126">Commence par <b>Man</b> avec respect de la casse.</span><span class="sxs-lookup"><span data-stu-id="1f208-126">Starts with <b>Man</b> and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="1f208-127">Tous les enregistrements qui commencent par le texte <b>Man</b>.</span><span class="sxs-lookup"><span data-stu-id="1f208-127">All records that start with the text <b>Man</b>.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="1f208-128">'man'</span><span class="sxs-lookup"><span data-stu-id="1f208-128">'man'</span></span></TD>
    <TD><span data-ttu-id="1f208-129">Texte exact avec respect de la casse.</span><span class="sxs-lookup"><span data-stu-id="1f208-129">An exact text and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="1f208-130">Tous les enregistrements qui correspondent exactement à <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="1f208-130">All records that match <b>man</b> exactly.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="1f208-131">@man*</span><span class="sxs-lookup"><span data-stu-id="1f208-131">@man*</span></span> </TD>
    <TD><span data-ttu-id="1f208-132">Commence par et ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="1f208-132">Starts with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="1f208-133">Tous les enregistrements qui commencent par <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="1f208-133">All records that start with <b>man</b>.</span></span></TD>
  </TR>
    <TR>
    <TD><span data-ttu-id="1f208-134">@&#42;man</span><span class="sxs-lookup"><span data-stu-id="1f208-134">@&#42;man</span></span></TD>
    <TD><span data-ttu-id="1f208-135">Se termine par et respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="1f208-135">Ends with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="1f208-136">Tous les enregistrements qui se terminent par <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="1f208-136">All records that end with <b>man</b>.</span></span></TD>
  </TR>
</TABLE>

> [!NOTE]  
>   <span data-ttu-id="1f208-137">Vous ne pouvez pas utiliser de caractères génériques lors du filtrage des champs d'énumération, tels que le champ **Statut** sur les commandes vente.</span><span class="sxs-lookup"><span data-stu-id="1f208-137">You cannot use a wildcard when filtering on enumeration fields, such as the **Status** field on sales orders.</span></span> <span data-ttu-id="1f208-138">Pour entrer un filtre pour ce type de champ, vous pouvez saisir la valeur numérique comme paramètre de filtre.</span><span class="sxs-lookup"><span data-stu-id="1f208-138">To enter a filter for this type of field, you can enter the numeric value as a filtering parameter.</span></span> <span data-ttu-id="1f208-139">Par exemple, dans le champ **Statut** sur une commande vente qui a les valeurs **Ouvert**, **Lancé**, **Approbation suspendue** et **Acompte suspendu**, utilisez les valeurs **0**, **1**, **2** et **3** pour filtrer ces options.</span><span class="sxs-lookup"><span data-stu-id="1f208-139">For example, in the **Status** field on a sales order that has the values **Open**, **Released**, **Pending Approval**, and **Pending Prepayment**, use the values **0**, **1**, **2**, and **3** to filter for these options.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1f208-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f208-140">See Also</span></span>
<span data-ttu-id="1f208-141">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1f208-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

