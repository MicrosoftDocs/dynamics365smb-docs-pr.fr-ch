---
title: Affichage et édition dans Excel depuis Business Central | Microsoft Docs
description: En savoir plus sur la manière dont vous pouvez ouvrir les pages dans Microsoft Excel à partir de Business Central pour une meilleure analyse de données.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 68139f258595bcca2658e394a4251e30dfbe6510
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "925055"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="36a26-103">Affichage et édition dans Excel depuis Business Central</span><span class="sxs-lookup"><span data-stu-id="36a26-103">Viewing and Editing in Excel From Business Central</span></span> 

<span data-ttu-id="36a26-104">Avec des pages qui affichent une liste d'enregistrements dans des lignes et des colonnes, comme une liste de clients, de commandes client ou de factures, vous pouvez également afficher les enregistrements à l'aide de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="36a26-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="36a26-105">Pour cela, vous avez deux possibilités.</span><span class="sxs-lookup"><span data-stu-id="36a26-105">To do this, you have two options.</span></span> <span data-ttu-id="36a26-106">Vous pouvez sélectionner l'action **Ouvrir dans Excel** ou l'action **Modifier dans Excel** sur la page.</span><span class="sxs-lookup"><span data-stu-id="36a26-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="36a26-107">Les différences entre les deux actions sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="36a26-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="36a26-108">Ouvrir dans Excel</span><span class="sxs-lookup"><span data-stu-id="36a26-108">Open in Excel</span></span>

-    <span data-ttu-id="36a26-109">Avec cette action, Excel tient compte de tous les filtres de la page qui limitent les enregistrements affichés.</span><span class="sxs-lookup"><span data-stu-id="36a26-109">With this action, Excel respects any filters on the page the limit the records shown.</span></span> <span data-ttu-id="36a26-110">Cela signifie que le classeur Excel contiendra les mêmes lignes et colonnes figurant sur la page dans [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="36a26-110">This means that the Excel workbook will contain the same rows and columns that appear on the the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

-    <span data-ttu-id="36a26-111">Vous pouvez apporter des modifications à des enregistrements dans Excel, mais vous ne pouvez pas publier les modifications dans [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="36a26-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="36a26-112">Vous ne pouvez enregistrer les modifications apportées au fichier Excel que sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="36a26-112">You can only save the changes to Excel file on your computer.</span></span> 

-    <span data-ttu-id="36a26-113">Cette action fonctionne sur Windows et macOS.</span><span class="sxs-lookup"><span data-stu-id="36a26-113">This action works on both on Windows and macOS.</span></span> 

>[!NOTE]
><span data-ttu-id="36a26-114">Pour [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, l'action **Ouvrir dans Excel** n'est pas disponible si l'action **Modifier dans Excel** l'est.</span><span class="sxs-lookup"><span data-stu-id="36a26-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is not available if the **Edit in Excel** action is.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="36a26-115">Modifier dans Excel</span><span class="sxs-lookup"><span data-stu-id="36a26-115">Edit in Excel</span></span>

-    <span data-ttu-id="36a26-116">Avec cette action, le classeur Excel ne tient pas compte des filtres de la page qui limitent les enregistrements affichés.</span><span class="sxs-lookup"><span data-stu-id="36a26-116">With this action, the Excel workbook does not respect filters on the page the limit the records shown.</span></span> <span data-ttu-id="36a26-117">Cela signifie que le classeur Excel contiendra tous les enregistrements et colonnes disponibles, indépendamment de ce qui est affiché sur la page.</span><span class="sxs-lookup"><span data-stu-id="36a26-117">This means that the Excel workbook will contain all the available records and columns, regardless of what is shown on the page.</span></span> 

-    <span data-ttu-id="36a26-118">L'avantage de l'action **Modifier dans Excel** est qu'elle vous permet d'apporter des modifications à des enregistrements dans Excel puis de les publier dans [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="36a26-118">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

-    <span data-ttu-id="36a26-119">Ceci fonctionne uniquement sur Windows, pas macOS.</span><span class="sxs-lookup"><span data-stu-id="36a26-119">It only works on Windows; not macOS.</span></span>

>[!NOTE]
><span data-ttu-id="36a26-120">Pour [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, l'action **Modifier dans Excel** est disponible uniquement si le module complémentaire Excel a été installé par votre administrateur.</span><span class="sxs-lookup"><span data-stu-id="36a26-120">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been installed by your administrator.</span></span> <span data-ttu-id="36a26-121">Pour les administrateurs, si vous souhaitez connaître la manière de configurer le module complémentaire Excel, consultez [Configuration du module complémentaire Excel](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="36a26-121">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="36a26-122">Voir les différences entre les options</span><span class="sxs-lookup"><span data-stu-id="36a26-122">See the differences between the options</span></span> 
> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-also"></a><span data-ttu-id="36a26-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36a26-123">See Also</span></span>
[<span data-ttu-id="36a26-124">Utilisation de Business Central</span><span class="sxs-lookup"><span data-stu-id="36a26-124">Working with Business Central</span></span>](ui-work-product.md)  
