---
title: Utilisation de l'extension QuickBooks Data Migration | Microsoft Docs
description: "Décrit comment utiliser l'extension pour importer des clients, des fournisseurs, des articles, et des comptes de QuickBooks Desktop à Dynamics 365 for Financials."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 4775c945a7721b8f4e52a187840a585396611e47
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="the-quickbooks-data-migration-extension-for-dynamics-365-for-financials"></a><span data-ttu-id="d2b8a-103">Extension QuickBooks Data Migration pour Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="d2b8a-103">The QuickBooks Data Migration Extension for Dynamics 365 for Financials</span></span>
<span data-ttu-id="d2b8a-104">Cette extension facilite la migration des clients, des fournisseurs, des articles et des comptes de QuickBooks Desktop vers [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d2b8a-104">This extension makes it easy to migrate customers, vendors, items, and accounts from QuickBooks Desktop to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="d2b8a-105">Si votre entreprise utilise QuickBooks aujourd'hui, vous pouvez exporter les informations appropriées puis ouvrir un guide de configuration assistée pour télécharger les données vers [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d2b8a-105">If your business uses QuickBooks today, you can export the relevant information and then open an assisted setup guide to upload the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
<span data-ttu-id="d2b8a-106">Pour plus d'informations, voir [Importation des données métier à partir d'autres systèmes financiers](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="d2b8a-106">For more information, see [Importing Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-quickbooks-desktop"></a><span data-ttu-id="d2b8a-107">Exportation des données à partir de QuickBooks Desktop</span><span class="sxs-lookup"><span data-stu-id="d2b8a-107">Exporting Data from QuickBooks Desktop</span></span>
<span data-ttu-id="d2b8a-108">Vous devez avoir exporté une partie ou la totalité de vos clients, fournisseurs, articles en stock et comptes existants vers un fichier IIF (Intuit Interchange Format).</span><span class="sxs-lookup"><span data-stu-id="d2b8a-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to an Intuit Interchange Format (IIF) file.</span></span> <span data-ttu-id="d2b8a-109">L'extension QuickBooks Data Migration inclut un mappage par défaut des données QuickBooks, ce qui vous permet d'utiliser vos données existantes pour tester votre nouvelle société [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d2b8a-109">The QuickBooks Data Migration extension includes a default mapping of QuickBooks data so that you can use your existing data to test your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="d2b8a-110">Le mappage par défaut est suffisant dans l'immense majorité des cas, mais vous pouvez le modifier dans le guide de configuration assistée.</span><span class="sxs-lookup"><span data-stu-id="d2b8a-110">The default mapping will be sufficient in the vast majority of cases, but you can change the mapping in the assisted setup guide.</span></span>  
<span data-ttu-id="d2b8a-111">Dans QuickBooks, le menu Fichier comprend un utilitaire permettant d'exporter les listes.</span><span class="sxs-lookup"><span data-stu-id="d2b8a-111">In QuickBooks, the File menu includes a utility to export lists.</span></span> <span data-ttu-id="d2b8a-112">Pour les besoins de [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez exporter les listes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d2b8a-112">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following lists:</span></span>

* <span data-ttu-id="d2b8a-113">Liste des clients</span><span class="sxs-lookup"><span data-stu-id="d2b8a-113">Customer List</span></span>  
* <span data-ttu-id="d2b8a-114">Liste des fournisseurs</span><span class="sxs-lookup"><span data-stu-id="d2b8a-114">Vendor List</span></span>  
* <span data-ttu-id="d2b8a-115">Liste des articles</span><span class="sxs-lookup"><span data-stu-id="d2b8a-115">Item List</span></span>  
* <span data-ttu-id="d2b8a-116">Liste des comptes</span><span class="sxs-lookup"><span data-stu-id="d2b8a-116">Account List</span></span>  

<span data-ttu-id="d2b8a-117">Les données exportées sont enregistrées en tant que fichier IIF que vous pouvez ensuite télécharger vers [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d2b8a-117">The exported data is saved as an IIF file that you can then upload to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="finding-the-quickbooks-data-migration-extension"></a><span data-ttu-id="d2b8a-118">Recherche de l'extension QuickBooks Data Migration</span><span class="sxs-lookup"><span data-stu-id="d2b8a-118">Finding the QuickBooks Data Migration Extension</span></span>
<span data-ttu-id="d2b8a-119">L'extension QuickBooks Data Migration est installée et prête à être utilisée comme partie intégrante du guide de configuration assistée Migration des données.</span><span class="sxs-lookup"><span data-stu-id="d2b8a-119">The QuickBooks Data Migration extension is installed and ready to go as an integrated part of the Data Migration assisted setup guide.</span></span> <span data-ttu-id="d2b8a-120">Si vous êtes prêt à commencer et que vous avez exporté vos données depuis QuickBooks, sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Configuration assistée**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="d2b8a-120">If you are ready to get started now, and have exported your data from QuickBooks, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Assisted Setup**, and then choose the related link.</span></span> <span data-ttu-id="d2b8a-121">Choisissez **Migrer des données métier**, puis suivez les étapes du guide.</span><span class="sxs-lookup"><span data-stu-id="d2b8a-121">Choose **Migrate business data**, and then follow the steps in the guide.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d2b8a-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2b8a-122">See Also</span></span>
[<span data-ttu-id="d2b8a-123">Importation des données métier à partir d'autres systèmes financiers</span><span class="sxs-lookup"><span data-stu-id="d2b8a-123">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="d2b8a-124">[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide des extensions ](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="d2b8a-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

