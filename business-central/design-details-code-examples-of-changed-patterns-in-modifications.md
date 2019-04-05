---
title: Détails de conception - Exemples de code de motifs modifiés dans les modifications | Microsoft Docs
description: Exemples de code montrant les motifs modifiés dans la modification et la migration de code de dimension pour cinq scénarios différents. Elle compare les exemples de code dans les versions antérieures aux exemples de code dans Business Central.
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
ms.openlocfilehash: 3a5806711b693dadbbaf033ffd769c5eabebe8de
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820720"
---
# <a name="design-details-code-examples-of-changed-patterns-in-modifications"></a><span data-ttu-id="93aea-104">Détails de conception : exemples de code de motifs modifiés dans les modifications</span><span class="sxs-lookup"><span data-stu-id="93aea-104">Design Details: Code Examples of Changed Patterns in Modifications</span></span>
<span data-ttu-id="93aea-105">Cette rubrique fournit des exemples de code pour montrer les motifs modifiés dans la modification et la migration de code de dimension pour cinq scénarios différents.</span><span class="sxs-lookup"><span data-stu-id="93aea-105">This topic provides code examples to show changed patterns in dimension code modification and migration for five different scenarios.</span></span> <span data-ttu-id="93aea-106">Elle compare les exemples de code dans les versions antérieures aux exemples de code dans Business Central.</span><span class="sxs-lookup"><span data-stu-id="93aea-106">It compares the code examples in earlier versions to the code examples in Business Central.</span></span>

## <a name="posting-a-journal-line"></a><span data-ttu-id="93aea-107">Validation d'une ligne feuille</span><span class="sxs-lookup"><span data-stu-id="93aea-107">Posting a Journal Line</span></span>  
<span data-ttu-id="93aea-108">Les modifications principales sont répertoriées comme suit :</span><span class="sxs-lookup"><span data-stu-id="93aea-108">Key changes are listed as follows:</span></span>  
  
- <span data-ttu-id="93aea-109">Les tables analytiques ligne feuille sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="93aea-109">Journal line dimension tables are removed.</span></span>  
  
- <span data-ttu-id="93aea-110">Un ID d'ensemble de dimensions est créé dans le champ **ID ensemble de dimensions**.</span><span class="sxs-lookup"><span data-stu-id="93aea-110">A dimension set ID is created in the **Dimension Set ID** field.</span></span>  
  
<span data-ttu-id="93aea-111">**Versions antérieures**</span><span class="sxs-lookup"><span data-stu-id="93aea-111">**Earlier Versions**</span></span>  
  
```  
ResJnlLine."Qty. per Unit of Measure" :=   
  SalesLine."Qty. per Unit of Measure";  
  
TempJnlLineDim.DELETEALL;  
TempDocDim.RESET;  
TempDocDim.SETRANGE(  
  "Table ID",DATABASE::"Sales Line");  
TempDocDim.SETRANGE(  
  "Line No.",SalesLine."Line No.");  
DimMgt.CopyDocDimToJnlLineDim(  
  TempDocDim,TempJnlLineDim);  
ResJnlPostLine.RunWithCheck(  
  ResJnlLine,TempJnlLineDim);  
  
```  
  
 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  
  
```  
  
ResJnlLine."Qty. per Unit of Measure" :=   
  SalesLine."Qty. per Unit of Measure";  
  
ResJnlLine."Dimension Set ID" :=   
  SalesLine." Dimension Set ID ";  
ResJnlPostLine.Run(ResJnlLine);  
  
```  
  
## <a name="posting-a-document"></a><span data-ttu-id="93aea-112">Validation d'un document</span><span class="sxs-lookup"><span data-stu-id="93aea-112">Posting a Document</span></span>  
 <span data-ttu-id="93aea-113">Lorsque vous validez un document dans [!INCLUDE[d365fin](includes/d365fin_md.md)], vous ne devez plus copier les dimensions du document.</span><span class="sxs-lookup"><span data-stu-id="93aea-113">When you post a document in [!INCLUDE[d365fin](includes/d365fin_md.md)], you no longer have to copy the document dimensions.</span></span>  
  
 <span data-ttu-id="93aea-114">**Versions antérieures**</span><span class="sxs-lookup"><span data-stu-id="93aea-114">**Earlier Versions**</span></span>  
  
```  
DimMgt.MoveOneDocDimToPostedDocDim(  
  TempDocDim,DATABASE::"Sales Line",  
  "Document Type",  
  "No.",  
  SalesShptLine."Line No.",  
  DATABASE::"Sales Shipment Line",  
  SalesShptHeader."No.");  
```  
  
 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  
  
```  
SalesShptLine."Dimension Set ID”  
  := SalesLine."Dimension Set ID”  
```  
  
## <a name="editing-dimensions-from-a-document"></a><span data-ttu-id="93aea-115">Modification des axes analytiques d'un document</span><span class="sxs-lookup"><span data-stu-id="93aea-115">Editing Dimensions from a Document</span></span>  
 <span data-ttu-id="93aea-116">Vous pouvez modifier les dimensions d'un document.</span><span class="sxs-lookup"><span data-stu-id="93aea-116">You can edit dimensions from a document.</span></span> <span data-ttu-id="93aea-117">Par exemple, vous pouvez modifier une ligne commande vente.</span><span class="sxs-lookup"><span data-stu-id="93aea-117">For example, you can edit a sales order line.</span></span>  
  
 <span data-ttu-id="93aea-118">**Versions antérieures**</span><span class="sxs-lookup"><span data-stu-id="93aea-118">**Earlier Versions**</span></span>  
  
```  
Table 37, function ShowDimensions:  
TESTFIELD("Document No.");  
TESTFIELD("Line No.");  
DocDim.SETRANGE("Table ID",DATABASE::"Sales Line");  
DocDim.SETRANGE("Document Type","Document Type");  
DocDim.SETRANGE("Document No.","Document No.");  
DocDim.SETRANGE("Line No.","Line No.");  
DocDimensions.SETTABLEVIEW(DocDim);  
DocDimensions.RUNMODAL;  
```  
  
 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  
  
```  
Table 37, function ShowDimensions:  
"Dimension ID" :=   
  DimSetEntry.EditDimensionSet(  
    "Dimension ID");  
```  
  
## <a name="showing-dimensions-from-posted-entries"></a><span data-ttu-id="93aea-119">Affichage des axes analytiques des écritures validées</span><span class="sxs-lookup"><span data-stu-id="93aea-119">Showing Dimensions from Posted Entries</span></span>  
 <span data-ttu-id="93aea-120">Vous pouvez afficher les dimensions à partir des écritures validées, comme les lignes d'expédition vente.</span><span class="sxs-lookup"><span data-stu-id="93aea-120">You can show dimensions from posted entries, such as sales shipment lines.</span></span>  
  
 <span data-ttu-id="93aea-121">**Versions antérieures**</span><span class="sxs-lookup"><span data-stu-id="93aea-121">**Earlier Versions**</span></span>  
  
```  
Table 111, function ShowDimensions:  
TESTFIELD("No.");  
TESTFIELD("Line No.");  
PostedDocDim.SETRANGE(  
  "Table ID",DATABASE::"Sales Shipment Line");  
PostedDocDim.SETRANGE(  
  "Document No.","Document No.");  
PostedDocDim.SETRANGE("Line No.","Line No.");  
PostedDocDimensions.SETTABLEVIEW(PostedDocDim);  
PostedDocDimensions.RUNMODAL;  
```  
  
 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  
  
```  
Table 111, function ShowDimensions:  
DimSetEntry.ShowDimensionSet(  
  "Dimension ID");  
```  
  
## <a name="getting-default-dimensions-for-a-document"></a><span data-ttu-id="93aea-122">Affichage des affectations analytiques pour un document</span><span class="sxs-lookup"><span data-stu-id="93aea-122">Getting Default Dimensions for a Document</span></span>  
 <span data-ttu-id="93aea-123">Vous pouvez obtenir des dimensions par défaut, comme une ligne commande vente.</span><span class="sxs-lookup"><span data-stu-id="93aea-123">You can get default dimensions for a document, such as a sales order line.</span></span>  
  
 <span data-ttu-id="93aea-124">**Versions antérieures**</span><span class="sxs-lookup"><span data-stu-id="93aea-124">**Earlier Versions**</span></span>  
  
```  
Table 37, function CreateDim()  
SourceCodeSetup.GET;  
TableID[1] := Type1;  
No[1] := No1;  
TableID[2] := Type2;  
No[2] := No2;  
TableID[3] := Type3;  
No[3] := No3;  
"Shortcut Dimension 1 Code" := '';  
"Shortcut Dimension 2 Code" := '';  
DimMgt.GetPreviousDocDefaultDim(  
  DATABASE::"Sales Header","Document Type",  
  "Document No.",0,  
  DATABASE::Customer,  
  "Shortcut Dimension 1 Code",  
  "Shortcut Dimension 2 Code");  
DimMgt.GetDefaultDim(  
  TableID,No,SourceCodeSetup.Sales,  
  "Shortcut Dimension 1 Code",  
  "Shortcut Dimension 2 Code");  
IF "Line No." <> 0 THEN  
  DimMgt.UpdateDocDefaultDim(  
    DATABASE::"Sales Line","Document Type",  
    "Document No.","Line No.",  
    "Shortcut Dimension 1 Code",  
    "Shortcut Dimension 2 Code");  
```  
  
 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  
  
```  
Table 37, function CreateDim()  
SourceCodeSetup.GET;  
TableID[1] := Type1;  
No[1] := No1;  
TableID[2] := Type2;  
No[2] := No2;  
TableID[3] := Type3;  
No[3] := No3;  
"Shortcut Dimension 1 Code" := '';  
"Shortcut Dimension 2 Code" := '';  
GetSalesHeader;  
"Dimension ID" :=  
  DimMgt.GetDefaultDimID(  
    TableID,No,SourceCodeSetup.Sales,  
    "Shortcut Dimension 1 Code",  
    "Shortcut Dimension 2 Code",  
    SalesHeader."Dimension ID",  
    DATABASE::"Sales Header");

```  

## <a name="see-also"></a><span data-ttu-id="93aea-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93aea-125">See Also</span></span>  
<span data-ttu-id="93aea-126">[Détails de conception : écritures d'ensemble de dimensions](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="93aea-126">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
<span data-ttu-id="93aea-127">[Détails de conception : structure de la table](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="93aea-127">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
[<span data-ttu-id="93aea-128">Détails de conception : Codeunit 408 Gestion des axes analytiques</span><span class="sxs-lookup"><span data-stu-id="93aea-128">Design Details: Codeunit 408 Dimension Management</span></span>](design-details-codeunit-408-dimension-management.md)