---
title: "Aperçu des écritures de l'ensemble de dimensions | Microsoft Docs"
description: "Cette rubrique décrit comment les écritures de l'ensemble de dimensions sont stockées et validées dans [!INCLUDE[d365fin](includes/d365fin_md.md)]."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 53c85ecbb42db92e95921203d24781bcb82f942d
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="dimension-set-entries-overview"></a><span data-ttu-id="6d965-103">Aperçu des écritures de l'ensemble de dimensions</span><span class="sxs-lookup"><span data-stu-id="6d965-103">Dimension Set Entries Overview</span></span>
<span data-ttu-id="6d965-104">Cette rubrique décrit comment les écritures de l'ensemble de dimensions sont stockées et validées dans [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6d965-104">This topic describes how dimension set entries are stored and posted in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
  
## <a name="dimension-sets"></a><span data-ttu-id="6d965-105">Ensembles de dimensions</span><span class="sxs-lookup"><span data-stu-id="6d965-105">Dimension Sets</span></span>  
<span data-ttu-id="6d965-106">Un ensemble de dimensions est une combinaison unique de sections analytiques.</span><span class="sxs-lookup"><span data-stu-id="6d965-106">A dimension set is a unique combination of dimension values.</span></span> <span data-ttu-id="6d965-107">Il est stocké comme des écritures de l'ensemble de dimensions dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="6d965-107">It is stored as dimension set entries in the database.</span></span> <span data-ttu-id="6d965-108">Chaque écriture de l'ensemble de dimensions représente une section analytique unique.</span><span class="sxs-lookup"><span data-stu-id="6d965-108">Each dimension set entry represents a single dimension value.</span></span> <span data-ttu-id="6d965-109">L'ensemble de dimensions est identifié par un ID courant, qui est affecté à chaque écriture correspondante qui appartient à l'ensemble de dimensions.</span><span class="sxs-lookup"><span data-stu-id="6d965-109">The dimension set is identified by a common dimension set ID that is assigned to each dimension set entry that belongs to the dimension set.</span></span>  
  
<span data-ttu-id="6d965-110">L'exemple suivant présente un ensemble de dimensions constitué de trois écritures.</span><span class="sxs-lookup"><span data-stu-id="6d965-110">The following example shows a dimension set that has three dimension set entries.</span></span> <span data-ttu-id="6d965-111">L'ensemble de dimensions est identifié par l'ID 108.</span><span class="sxs-lookup"><span data-stu-id="6d965-111">The dimension set is identified by a dimension set ID, which is 108.</span></span>  
  
|<span data-ttu-id="6d965-112">ID ensemble de dimensions</span><span class="sxs-lookup"><span data-stu-id="6d965-112">Dimension Set ID</span></span>|<span data-ttu-id="6d965-113">Code axe</span><span class="sxs-lookup"><span data-stu-id="6d965-113">Dimension Code</span></span>|<span data-ttu-id="6d965-114">Code section</span><span class="sxs-lookup"><span data-stu-id="6d965-114">Dimension Value Code</span></span>|<span data-ttu-id="6d965-115">Nom de la section analytique</span><span class="sxs-lookup"><span data-stu-id="6d965-115">Dimension Value Name</span></span>|  
|----------------------|--------------------|--------------------------|--------------------------|  
|<span data-ttu-id="6d965-116">108</span><span class="sxs-lookup"><span data-stu-id="6d965-116">108</span></span>|<span data-ttu-id="6d965-117">ZONE</span><span class="sxs-lookup"><span data-stu-id="6d965-117">AREA</span></span>|<span data-ttu-id="6d965-118">70</span><span class="sxs-lookup"><span data-stu-id="6d965-118">70</span></span>|<span data-ttu-id="6d965-119">Amérique du Nord</span><span class="sxs-lookup"><span data-stu-id="6d965-119">America North</span></span>|  
|<span data-ttu-id="6d965-120">108</span><span class="sxs-lookup"><span data-stu-id="6d965-120">108</span></span>|<span data-ttu-id="6d965-121">GROUPE COMPTABILISATION MARCHÉ</span><span class="sxs-lookup"><span data-stu-id="6d965-121">BUSINESSGROUP</span></span>|<span data-ttu-id="6d965-122">DÉBUT</span><span class="sxs-lookup"><span data-stu-id="6d965-122">HOME</span></span>|<span data-ttu-id="6d965-123">Accueil</span><span class="sxs-lookup"><span data-stu-id="6d965-123">Home</span></span>|  
|<span data-ttu-id="6d965-124">108</span><span class="sxs-lookup"><span data-stu-id="6d965-124">108</span></span>|<span data-ttu-id="6d965-125">DÉPARTEMENT</span><span class="sxs-lookup"><span data-stu-id="6d965-125">DEPARTMENT</span></span>|<span data-ttu-id="6d965-126">VENTES</span><span class="sxs-lookup"><span data-stu-id="6d965-126">SALES</span></span>|<span data-ttu-id="6d965-127">Ventes</span><span class="sxs-lookup"><span data-stu-id="6d965-127">Sales</span></span>|  
  
## <a name="dimension-set-entries"></a><span data-ttu-id="6d965-128">Écritures de l'ensemble de dimensions</span><span class="sxs-lookup"><span data-stu-id="6d965-128">Dimension Set Entries</span></span>  
<span data-ttu-id="6d965-129">Les ensembles de dimensions sont stockés dans la table **Écriture de l'ensemble de dimensions** telles des écritures de l'ensemble de dimensions avec le même ID.</span><span class="sxs-lookup"><span data-stu-id="6d965-129">Dimension sets are stored in the **Dimension Set Entry** table as dimension set entries with the same dimension set ID.</span></span>  
  
<span data-ttu-id="6d965-130">![Aperçu Ecriture analytique](media/dimensionentrynav7.png "DimensionEntryNAV7")</span><span class="sxs-lookup"><span data-stu-id="6d965-130">![Dimension Entry overview](media/dimensionentrynav7.png "DimensionEntryNAV7")</span></span>  
  
<span data-ttu-id="6d965-131">Lorsque vous créez une ligne de feuille, un en-tête de document ou une ligne de document, vous pouvez spécifier une combinaison de sections analytiques.</span><span class="sxs-lookup"><span data-stu-id="6d965-131">When you create a new journal line, document header, or document line, you can specify a combination of dimension values.</span></span> <span data-ttu-id="6d965-132">Au lieu d'enregistrer explicitement chaque section analytique dans la base de données, un ID d'ensemble de dimensions est affecté à la ligne de feuille, à l'en-tête du document ou à la ligne du document pour spécifier l'ensemble de dimensions.</span><span class="sxs-lookup"><span data-stu-id="6d965-132">Instead of explicitly storing each dimension value in the database, a dimension set ID is assigned to the journal line, document header, or document line to specify the dimension set.</span></span>  
  
<span data-ttu-id="6d965-133">Lorsque vous modifiez et fermez la fenêtre **Modifier les écritures de l'ensemble de dimensions**, une vérification est exécutée pour voir si la combinaison de sections analytiques existe comme un ensemble de dimensions dans la table.</span><span class="sxs-lookup"><span data-stu-id="6d965-133">When you edit and close the **Edit Dimension Set Entries** window, a check is performed to see whether the combination of dimension values exists as a dimension set in the table.</span></span> <span data-ttu-id="6d965-134">Si la combinaison se produit dans la table, l'ID d'ensemble de dimensions correspondant est affecté à la ligne de feuille, à l'en-tête du document ou à la ligne du document.</span><span class="sxs-lookup"><span data-stu-id="6d965-134">If the combination occurs in the table, then the corresponding dimension set ID is assigned to the journal line, document header, or document line.</span></span> <span data-ttu-id="6d965-135">Sinon, un nouvel ensemble de dimensions est ajouté à la table, et le nouvel ID d'ensemble de dimensions est affecté à la ligne de feuille, à l'en-tête du document ou à la ligne du document.</span><span class="sxs-lookup"><span data-stu-id="6d965-135">Otherwise, a new dimension set is added to the table, and the new dimension set ID is assigned to the journal line, document header, or document line.</span></span>  
  
## <a name="performance-improvement"></a><span data-ttu-id="6d965-136">Amélioration des performances</span><span class="sxs-lookup"><span data-stu-id="6d965-136">Performance Improvement</span></span>  
<span data-ttu-id="6d965-137">Pour enregistrer les axes analytiques dans la base de données, l'espace de la base de données est conservé et les performances globales sont améliorées.</span><span class="sxs-lookup"><span data-stu-id="6d965-137">By storing dimension sets once in the database, database space is preserved, and overall performance is improved.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6d965-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d965-138">See Also</span></span>  
<span data-ttu-id="6d965-139">[Détails de conception : recherche des croisements analytiques](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="6d965-139">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
<span data-ttu-id="6d965-140">[Détails de conception : structure de la table](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="6d965-140">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
<span data-ttu-id="6d965-141">[Détails de conception : Codeunit 408 Gestion des axes analytiques](design-details-codeunit-408-dimension-management.md) </span><span class="sxs-lookup"><span data-stu-id="6d965-141">[Design Details: Codeunit 408 Dimension Management](design-details-codeunit-408-dimension-management.md) </span></span>  
<span data-ttu-id="6d965-142">[Détails de conception : exemples de code de motifs modifiés dans les modifications](design-details-code-examples-of-changed-patterns-in-modifications.md) </span><span class="sxs-lookup"><span data-stu-id="6d965-142">[Design Details: Code Examples of Changed Patterns in Modifications](design-details-code-examples-of-changed-patterns-in-modifications.md) </span></span>  
[<span data-ttu-id="6d965-143">Détails de conception : écritures d'ensemble de dimensions</span><span class="sxs-lookup"><span data-stu-id="6d965-143">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries.md)   

