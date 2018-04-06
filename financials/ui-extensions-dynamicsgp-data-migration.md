---
title: "Migrer des données de Dynamics GP avec l'extension Data Migration | Microsoft Docs"
description: Utilisez l'extension Dynamics GP Data Migration pour migrer des clients, des fournisseurs, des articles en stock, et des comptes de Dynamics GP vers Finance and Operations, Business edition.
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: bfd3ca3e28b6eb3efa2a16cc131b508db6bd1590
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="the-dynamics-gp-data-migration-extension-for-finance-and-operations-business-edition"></a><span data-ttu-id="60fd4-103">L'extension Dynamics GP Data Migration pour Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="60fd4-103">The Dynamics GP Data Migration Extension for Finance and Operations, Business edition</span></span> 
<span data-ttu-id="60fd4-104">Cette extension facilite la migration des clients, des fournisseurs, des articles en stock et des comptes à partir de Dynamics GP vers [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="60fd4-104">This extension makes it easy to migrate customers, vendors, inventory items, and accounts from Dynamics GP to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="60fd4-105">Si votre entreprise utilise Dynamics GP aujourd'hui, vous pouvez exporter les principaux enregistrements appropriés, puis ouvrir un guide de configuration assistée pour ajouter les données vers [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="60fd4-105">If your business uses Dynamics GP today, you can export the relevant master records and then open an assisted setup guide to add the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="60fd4-106">Pour plus d'informations, voir [Migrer des données métier à partir d'autres systèmes financiers](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="60fd4-106">For more information, see [Migrate Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-dynamics-gp"></a><span data-ttu-id="60fd4-107">Exportation de données à partir de Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="60fd4-107">Exporting Data from Dynamics GP</span></span>
<span data-ttu-id="60fd4-108">Vous devez avoir exporté certains ou tous vos clients, fournisseurs, articles de stock, et comptes dans un fichier à l'aide de la fonctionnalité Dynamics GP pour l'exportation de données.</span><span class="sxs-lookup"><span data-stu-id="60fd4-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to a file, using the Dynamics GP functionality for data export.</span></span> <span data-ttu-id="60fd4-109">Pour les besoins de [!INCLUDE[d365fin](includes/d365fin_md.md)], vous pouvez exporter les types de données suivants :</span><span class="sxs-lookup"><span data-stu-id="60fd4-109">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following types of data:</span></span>

* <span data-ttu-id="60fd4-110">Compte</span><span class="sxs-lookup"><span data-stu-id="60fd4-110">Account</span></span>  
* <span data-ttu-id="60fd4-111">Client</span><span class="sxs-lookup"><span data-stu-id="60fd4-111">Customer</span></span>  
* <span data-ttu-id="60fd4-112">Article</span><span class="sxs-lookup"><span data-stu-id="60fd4-112">Item</span></span>  
* <span data-ttu-id="60fd4-113">Fournisseur</span><span class="sxs-lookup"><span data-stu-id="60fd4-113">Vendor</span></span>  

<span data-ttu-id="60fd4-114">L'extension Dynamics GP Data Migration mappe automatiquement les données exportées afin qu'elles soient rapidement disponibles dans votre nouvelle société [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="60fd4-114">The Dynamics GP Data Migration extension automatically maps the exported data so that your data is quickly available to you in your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="60fd4-115">Au cours de ce processus, la prise en charge des informations de configuration est créée, comme des groupes comptabilisation.</span><span class="sxs-lookup"><span data-stu-id="60fd4-115">During the process, supporting setup information is created, such as posting groups.</span></span> <span data-ttu-id="60fd4-116">Les articles en stock sont transmis au système avec FIFO comme méthode d'évaluation du coût.</span><span class="sxs-lookup"><span data-stu-id="60fd4-116">Inventory items will be brought into the system with FIFO as the cost valuation method.</span></span> <span data-ttu-id="60fd4-117">Les comptes sont configurés comme segment principal à partir de Dynamics GP avec des axes, car [!INCLUDE[d365fin](includes/d365fin_long_md.md)] n'a pas de segments de compte.</span><span class="sxs-lookup"><span data-stu-id="60fd4-117">Accounts will be set up as the main account segment from Dynamics GP with dimensions, because [!INCLUDE[d365fin](includes/d365fin_long_md.md)] does not have account segments.</span></span>

## <a name="see-also"></a><span data-ttu-id="60fd4-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60fd4-118">See Also</span></span>
[<span data-ttu-id="60fd4-119">Importation des données métier à partir d'autres systèmes financiers</span><span class="sxs-lookup"><span data-stu-id="60fd4-119">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="60fd4-120">[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide des extensions ](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="60fd4-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

