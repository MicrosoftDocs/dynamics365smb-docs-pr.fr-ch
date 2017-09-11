---
title: Utilisation de l'extension QuickBooks Data Migration | Microsoft Docs
description: "Décrit comment utiliser l'extension pour importer des clients, des fournisseurs, des articles, et des comptes de QuickBooks Desktop à Dynamics 365 for Financials."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 37d90316ea0be5489fb5abe33645de3fe0d3cf90
ms.contentlocale: fr-ch
ms.lasthandoff: 09/11/2017

---
# <a name="the-quickbooks-data-migration-extension-for-dynamics-365-for-financials"></a><span data-ttu-id="d539d-103">Extension QuickBooks Data Migration pour Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="d539d-103">The QuickBooks Data Migration Extension for Dynamics 365 for Financials</span></span>
<span data-ttu-id="d539d-104">Cette extension facilite la migration des clients, des fournisseurs, des articles et des comptes de QuickBooks vers [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d539d-104">This extension makes it easy to migrate customers, vendors, items, and accounts from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="d539d-105">Si votre entreprise utilise QuickBooks aujourd'hui, vous pouvez exporter les informations appropriées puis ouvrir un guide de configuration assistée pour télécharger les données vers [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d539d-105">If your business uses QuickBooks today, you can export the relevant information and then open an assisted setup guide to upload the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
<span data-ttu-id="d539d-106">Pour plus d'informations, voir [Importation des données métier à partir d'autres systèmes financiers](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="d539d-106">For more information, see [Importing Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-quickbooks"></a><span data-ttu-id="d539d-107">Exportation des données à partir de QuickBooks</span><span class="sxs-lookup"><span data-stu-id="d539d-107">Exporting Data from QuickBooks</span></span>
<span data-ttu-id="d539d-108">Vous devez avoir exporté une partie ou la totalité de vos clients, fournisseurs, articles en stock et comptes existants vers un fichier IIF (Intuit Interchange Format).</span><span class="sxs-lookup"><span data-stu-id="d539d-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to an Intuit Interchange Format (IIF) file.</span></span> <span data-ttu-id="d539d-109">L'extension QuickBooks Data Migration inclut un mappage par défaut des données QuickBooks, ce qui vous permet d'utiliser vos données existantes pour tester votre nouvelle société [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d539d-109">The QuickBooks Data Migration extension includes a default mapping of QuickBooks data so that you can use your existing data to test your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="d539d-110">Le mappage par défaut est suffisant dans l'immense majorité des cas, mais vous pouvez le modifier dans le guide de configuration assistée.</span><span class="sxs-lookup"><span data-stu-id="d539d-110">The default mapping will be sufficient in the vast majority of cases, but you can change the mapping in the assisted setup guide.</span></span>  
<span data-ttu-id="d539d-111">Dans QuickBooks, le menu Fichier comprend un utilitaire permettant d'exporter les listes.</span><span class="sxs-lookup"><span data-stu-id="d539d-111">In QuickBooks, the File menu includes a utility to export lists.</span></span> <span data-ttu-id="d539d-112">Pour les besoins de [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez exporter les listes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d539d-112">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following lists:</span></span>

* <span data-ttu-id="d539d-113">Liste des clients</span><span class="sxs-lookup"><span data-stu-id="d539d-113">Customer List</span></span>  
* <span data-ttu-id="d539d-114">Liste des fournisseurs</span><span class="sxs-lookup"><span data-stu-id="d539d-114">Vendor List</span></span>  
* <span data-ttu-id="d539d-115">Liste des articles</span><span class="sxs-lookup"><span data-stu-id="d539d-115">Item List</span></span>  
* <span data-ttu-id="d539d-116">Liste des comptes</span><span class="sxs-lookup"><span data-stu-id="d539d-116">Account List</span></span>  

<span data-ttu-id="d539d-117">Les données exportées sont enregistrées en tant que fichier IIF que vous pouvez ensuite télécharger vers [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d539d-117">The exported data is saved as an IIF file that you can then upload to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="d539d-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d539d-118">See Also</span></span>
[<span data-ttu-id="d539d-119">Importation des données métier à partir d'autres systèmes financiers</span><span class="sxs-lookup"><span data-stu-id="d539d-119">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="d539d-120">[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide des extensions ](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="d539d-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

