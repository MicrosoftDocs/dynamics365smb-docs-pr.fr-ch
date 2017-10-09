---
title: "Migrer des données de Dynamics GP avec l'extension Data Migration | Microsoft Docs"
description: "Utilisez l'extension Dynamics GP Data Migration pour migrer des clients, des fournisseurs, des articles en stock, et des comptes de Dynamics GP vers Dynamics 365 for Financials."
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
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 31b698aea884da162cc18f16a912ebd57e35aed9
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="the-dynamics-gp-data-migration-extension-for-dynamics-365-for-financials"></a><span data-ttu-id="a22c2-103">Extension Dynamics GP Data Migration pour Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="a22c2-103">The Dynamics GP Data Migration Extension for Dynamics 365 for Financials</span></span>
<span data-ttu-id="a22c2-104">Cette extension facilite la migration des clients, des fournisseurs, des articles en stock et des comptes à partir de Dynamics GP vers [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a22c2-104">This extension makes it easy to migrate customers, vendors, inventory items, and accounts from Dynamics GP to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="a22c2-105">Si votre entreprise utilise Dynamics GP aujourd'hui, vous pouvez exporter les principaux enregistrements appropriés, puis ouvrir un guide de configuration assistée pour ajouter les données vers [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a22c2-105">If your business uses Dynamics GP today, you can export the relevant master records and then open an assisted setup guide to add the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="a22c2-106">Pour plus d'informations, voir [Migrer des données métier à partir d'autres systèmes financiers](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="a22c2-106">For more information, see [Migrate Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-dynamics-gp"></a><span data-ttu-id="a22c2-107">Exportation de données à partir de Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="a22c2-107">Exporting Data from Dynamics GP</span></span>
<span data-ttu-id="a22c2-108">Vous devez avoir exporté certains ou tous vos clients, fournisseurs, articles de stock, et comptes dans un fichier à l'aide de la fonctionnalité Dynamics GP pour l'exportation de données.</span><span class="sxs-lookup"><span data-stu-id="a22c2-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to a file, using the Dynamics GP functionality for data export.</span></span> <span data-ttu-id="a22c2-109">Pour les besoins de [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez exporter les types de données suivants :</span><span class="sxs-lookup"><span data-stu-id="a22c2-109">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following types of data:</span></span>

* <span data-ttu-id="a22c2-110">Compte</span><span class="sxs-lookup"><span data-stu-id="a22c2-110">Account</span></span>  
* <span data-ttu-id="a22c2-111">Client</span><span class="sxs-lookup"><span data-stu-id="a22c2-111">Customer</span></span>  
* <span data-ttu-id="a22c2-112">Article</span><span class="sxs-lookup"><span data-stu-id="a22c2-112">Item</span></span>  
* <span data-ttu-id="a22c2-113">Fournisseur</span><span class="sxs-lookup"><span data-stu-id="a22c2-113">Vendor</span></span>  

<span data-ttu-id="a22c2-114">L'extension Dynamics GP Data Migration mappe automatiquement les données exportées afin qu'elles soient rapidement disponibles dans votre nouvelle société [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a22c2-114">The Dynamics GP Data Migration extension automatically maps the exported data so that your data is quickly available to you in your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="a22c2-115">Au cours de ce processus, la prise en charge des informations de configuration est créée, comme des groupes comptabilisation.</span><span class="sxs-lookup"><span data-stu-id="a22c2-115">During the process, supporting setup information is created, such as posting groups.</span></span> <span data-ttu-id="a22c2-116">Les articles en stock sont transmis au système avec FIFO comme méthode d'évaluation du coût.</span><span class="sxs-lookup"><span data-stu-id="a22c2-116">Inventory items will be brought into the system with FIFO as the cost valuation method.</span></span> <span data-ttu-id="a22c2-117">Les comptes sont configurés comme segment principal à partir de Dynamics GP avec des axes, car [!INCLUDE[d365fin](includes/d365fin_long_md.md)] n'a pas de segments de compte.</span><span class="sxs-lookup"><span data-stu-id="a22c2-117">Accounts will be set up as the main account segment from Dynamics GP with dimensions, because [!INCLUDE[d365fin](includes/d365fin_long_md.md)] does not have account segments.</span></span>

## <a name="see-also"></a><span data-ttu-id="a22c2-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a22c2-118">See Also</span></span>
[<span data-ttu-id="a22c2-119">Importation des données métier à partir d'autres systèmes financiers</span><span class="sxs-lookup"><span data-stu-id="a22c2-119">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="a22c2-120">[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide des extensions ](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="a22c2-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

