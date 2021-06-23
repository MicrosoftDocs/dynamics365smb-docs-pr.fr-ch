---
title: Aperçu des écritures de l’ensemble de dimensions | Microsoft Docs
description: Cette rubrique décrit comment les écritures de l’ensemble de dimensions sont stockées et validées dans Dynamics 365.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: c6e3df748269e2f40e3acf0a28ce0f6bc48ca944
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215318"
---
# <a name="dimension-set-entries-overview"></a><span data-ttu-id="68a48-103">Aperçu des écritures de l’ensemble de dimensions</span><span class="sxs-lookup"><span data-stu-id="68a48-103">Dimension Set Entries Overview</span></span>
<span data-ttu-id="68a48-104">Cette rubrique décrit comment les écritures de l’ensemble de dimensions sont stockées et validées dans [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="68a48-104">This topic describes how dimension set entries are stored and posted in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

## <a name="dimension-sets"></a><span data-ttu-id="68a48-105">Ensembles de dimensions</span><span class="sxs-lookup"><span data-stu-id="68a48-105">Dimension Sets</span></span>  
<span data-ttu-id="68a48-106">Un ensemble de dimensions est une combinaison unique de sections analytiques.</span><span class="sxs-lookup"><span data-stu-id="68a48-106">A dimension set is a unique combination of dimension values.</span></span> <span data-ttu-id="68a48-107">Il est stocké comme des écritures de l’ensemble de dimensions dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="68a48-107">It is stored as dimension set entries in the database.</span></span> <span data-ttu-id="68a48-108">Chaque écriture de l’ensemble de dimensions représente une section analytique unique.</span><span class="sxs-lookup"><span data-stu-id="68a48-108">Each dimension set entry represents a single dimension value.</span></span> <span data-ttu-id="68a48-109">L’ensemble de dimensions est identifié par un ID courant, qui est affecté à chaque écriture correspondante qui appartient à l’ensemble de dimensions.</span><span class="sxs-lookup"><span data-stu-id="68a48-109">The dimension set is identified by a common dimension set ID that is assigned to each dimension set entry that belongs to the dimension set.</span></span>  

<span data-ttu-id="68a48-110">L’exemple suivant présente un ensemble de dimensions constitué de trois écritures.</span><span class="sxs-lookup"><span data-stu-id="68a48-110">The following example shows a dimension set that has three dimension set entries.</span></span> <span data-ttu-id="68a48-111">L’ensemble de dimensions est identifié par l’ID 108.</span><span class="sxs-lookup"><span data-stu-id="68a48-111">The dimension set is identified by a dimension set ID, which is 108.</span></span>  

|<span data-ttu-id="68a48-112">ID ensemble de dimensions</span><span class="sxs-lookup"><span data-stu-id="68a48-112">Dimension Set ID</span></span>|<span data-ttu-id="68a48-113">Code axe</span><span class="sxs-lookup"><span data-stu-id="68a48-113">Dimension Code</span></span>|<span data-ttu-id="68a48-114">Code section</span><span class="sxs-lookup"><span data-stu-id="68a48-114">Dimension Value Code</span></span>|<span data-ttu-id="68a48-115">Nom de la section analytique</span><span class="sxs-lookup"><span data-stu-id="68a48-115">Dimension Value Name</span></span>|  
|----------------------|--------------------|--------------------------|--------------------------|  
|<span data-ttu-id="68a48-116">108</span><span class="sxs-lookup"><span data-stu-id="68a48-116">108</span></span>|<span data-ttu-id="68a48-117">ZONE</span><span class="sxs-lookup"><span data-stu-id="68a48-117">AREA</span></span>|<span data-ttu-id="68a48-118">70</span><span class="sxs-lookup"><span data-stu-id="68a48-118">70</span></span>|<span data-ttu-id="68a48-119">Amérique du Nord</span><span class="sxs-lookup"><span data-stu-id="68a48-119">America North</span></span>|  
|<span data-ttu-id="68a48-120">108</span><span class="sxs-lookup"><span data-stu-id="68a48-120">108</span></span>|<span data-ttu-id="68a48-121">GROUPE COMPTABILISATION MARCHÉ</span><span class="sxs-lookup"><span data-stu-id="68a48-121">BUSINESSGROUP</span></span>|<span data-ttu-id="68a48-122">DÉBUT</span><span class="sxs-lookup"><span data-stu-id="68a48-122">HOME</span></span>|<span data-ttu-id="68a48-123">Accueil</span><span class="sxs-lookup"><span data-stu-id="68a48-123">Home</span></span>|  
|<span data-ttu-id="68a48-124">108</span><span class="sxs-lookup"><span data-stu-id="68a48-124">108</span></span>|<span data-ttu-id="68a48-125">DÉPARTEMENT</span><span class="sxs-lookup"><span data-stu-id="68a48-125">DEPARTMENT</span></span>|<span data-ttu-id="68a48-126">VENTES</span><span class="sxs-lookup"><span data-stu-id="68a48-126">SALES</span></span>|<span data-ttu-id="68a48-127">Ventes</span><span class="sxs-lookup"><span data-stu-id="68a48-127">Sales</span></span>|  

## <a name="dimension-set-entries"></a><span data-ttu-id="68a48-128">Écritures de l’ensemble de dimensions</span><span class="sxs-lookup"><span data-stu-id="68a48-128">Dimension Set Entries</span></span>  
<span data-ttu-id="68a48-129">Les ensembles de dimensions sont stockés dans la table **Écriture de l’ensemble de dimensions** telles des écritures de l’ensemble de dimensions avec le même ID.</span><span class="sxs-lookup"><span data-stu-id="68a48-129">Dimension sets are stored in the **Dimension Set Entry** table as dimension set entries with the same dimension set ID.</span></span>  

<span data-ttu-id="68a48-130">![Flux des écritures de l’ensemble de dimensions](media/dimensionentrynav7.png "Flux des écritures de l’ensemble de dimensions")</span><span class="sxs-lookup"><span data-stu-id="68a48-130">![Flow of dimension set entries](media/dimensionentrynav7.png "Flow of dimension set entries")</span></span>  

<span data-ttu-id="68a48-131">Lorsque vous créez une ligne de feuille, un en-tête de document ou une ligne de document, vous pouvez spécifier une combinaison de sections analytiques.</span><span class="sxs-lookup"><span data-stu-id="68a48-131">When you create a new journal line, document header, or document line, you can specify a combination of dimension values.</span></span> <span data-ttu-id="68a48-132">Au lieu d’enregistrer explicitement chaque section analytique dans la base de données, un ID d’ensemble de dimensions est affecté à la ligne de feuille, à l’en-tête du document ou à la ligne du document pour spécifier l’ensemble de dimensions.</span><span class="sxs-lookup"><span data-stu-id="68a48-132">Instead of explicitly storing each dimension value in the database, a dimension set ID is assigned to the journal line, document header, or document line to specify the dimension set.</span></span>  

<span data-ttu-id="68a48-133">Lorsque vous modifiez et fermez la page **Modifier les écritures de l’ensemble de dimensions**, une vérification est exécutée pour voir si la combinaison de sections analytiques existe comme un ensemble de dimensions dans la table.</span><span class="sxs-lookup"><span data-stu-id="68a48-133">When you edit and close the **Edit Dimension Set Entries** page, a check is performed to see whether the combination of dimension values exists as a dimension set in the table.</span></span> <span data-ttu-id="68a48-134">Si la combinaison se produit dans la table, l’ID d’ensemble de dimensions correspondant est affecté à la ligne de feuille, à l’en-tête du document ou à la ligne du document.</span><span class="sxs-lookup"><span data-stu-id="68a48-134">If the combination occurs in the table, then the corresponding dimension set ID is assigned to the journal line, document header, or document line.</span></span> <span data-ttu-id="68a48-135">Sinon, un nouvel ensemble de dimensions est ajouté à la table, et le nouvel ID d’ensemble de dimensions est affecté à la ligne de feuille, à l’en-tête du document ou à la ligne du document.</span><span class="sxs-lookup"><span data-stu-id="68a48-135">Otherwise, a new dimension set is added to the table, and the new dimension set ID is assigned to the journal line, document header, or document line.</span></span>

## <a name="codeunit-408-dimension-management"></a><span data-ttu-id="68a48-136">Codeunit 408 Gestion des axes analytiques</span><span class="sxs-lookup"><span data-stu-id="68a48-136">Codeunit 408 Dimension Management</span></span>
<span data-ttu-id="68a48-137">Codeunit 408 Gestion des axes analytiques est une bibliothèque de fonctions qui gère les tâches courantes qui sont liées aux axes analytiques, tels que copier d’une table à une autre ou d’un document à un autre.</span><span class="sxs-lookup"><span data-stu-id="68a48-137">Codeunit 408, Dimension Management, is a function library that handles common tasks that are related to dimensions, such as copying from one table to another or from one document to another.</span></span>

## <a name="performance-improvement"></a><span data-ttu-id="68a48-138">Amélioration des performances</span><span class="sxs-lookup"><span data-stu-id="68a48-138">Performance Improvement</span></span>  
<span data-ttu-id="68a48-139">Pour enregistrer les axes analytiques dans la base de données, l’espace de la base de données est conservé et les performances globales sont améliorées.</span><span class="sxs-lookup"><span data-stu-id="68a48-139">By storing dimension sets once in the database, database space is preserved and overall performance is improved.</span></span>  

## <a name="see-also"></a><span data-ttu-id="68a48-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68a48-140">See Also</span></span>
<span data-ttu-id="68a48-141">[Détails de conception : recherche des croisements analytiques](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="68a48-141">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
<span data-ttu-id="68a48-142">[Détails de conception : structure de la table](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="68a48-142">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
[<span data-ttu-id="68a48-143">Détails de conception : écritures d’ensemble de dimensions</span><span class="sxs-lookup"><span data-stu-id="68a48-143">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]
