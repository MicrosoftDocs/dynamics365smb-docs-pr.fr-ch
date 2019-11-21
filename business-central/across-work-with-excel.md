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
ms.date: 10/24/2019
ms.author: jswymer
ms.openlocfilehash: 71b4e5b7124f929255f1374b38cfbe28c9f12d2b
ms.sourcegitcommit: c6e28db8f78fa21db064c9b8a8d742f49d7db3ae
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/31/2019
ms.locfileid: "2692815"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="12ae5-103">Affichage et édition dans Excel depuis Business Central</span><span class="sxs-lookup"><span data-stu-id="12ae5-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="12ae5-104">Avec des pages qui affichent une liste d'enregistrements dans des lignes et des colonnes, comme une liste de clients, de commandes client ou de factures, vous pouvez également afficher les enregistrements à l'aide de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="12ae5-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="12ae5-105">Pour cela, vous avez deux possibilités.</span><span class="sxs-lookup"><span data-stu-id="12ae5-105">To do this, you have two options.</span></span> <span data-ttu-id="12ae5-106">Vous pouvez sélectionner l'action **Ouvrir dans Excel** ou l'action **Modifier dans Excel** sur la page.</span><span class="sxs-lookup"><span data-stu-id="12ae5-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="12ae5-107">Les différences entre les deux actions sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="12ae5-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="12ae5-108">Ouvrir dans Excel</span><span class="sxs-lookup"><span data-stu-id="12ae5-108">Open in Excel</span></span>

- <span data-ttu-id="12ae5-109">Avec cette action, Excel tient compte de tous les filtres de la page qui limitent les enregistrements affichés.</span><span class="sxs-lookup"><span data-stu-id="12ae5-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="12ae5-110">Cela signifie que le classeur Excel contiendra les mêmes lignes et colonnes figurant sur la page dans [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="12ae5-110">This means that the Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="12ae5-111">Vous pouvez apporter des modifications à des enregistrements dans Excel, mais vous ne pouvez pas publier les modifications dans [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="12ae5-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="12ae5-112">Vous ne pouvez enregistrer les modifications apportées au fichier Excel que sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="12ae5-112">You can only save the changes to Excel file on your computer.</span></span> 

- <span data-ttu-id="12ae5-113">Cette action fonctionne sur Windows et macOS.</span><span class="sxs-lookup"><span data-stu-id="12ae5-113">This action works on both on Windows and macOS.</span></span> 

> [!NOTE]
> <span data-ttu-id="12ae5-114">Pour [!INCLUDE[prodshort](includes/prodshort.md)] sur site, l'action **Ouvrir dans Excel** est disponible par défaut.</span><span class="sxs-lookup"><span data-stu-id="12ae5-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="12ae5-115">Cependant, si vous configurez [!INCLUDE [prodshort](includes/prodshort.md)]sur site pour la modification de données dans Excel, l'action **Ouvrir dans Excel** est alors remplacée par l'action **Modifier dans Excel**.</span><span class="sxs-lookup"><span data-stu-id="12ae5-115">However, if you set up [!INCLUDE [prodshort](includes/prodshort.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="12ae5-116">Modifier dans Excel</span><span class="sxs-lookup"><span data-stu-id="12ae5-116">Edit in Excel</span></span>

- <span data-ttu-id="12ae5-117">Avec cette action, Excel tient compte de la plupart des filtres de la page qui limitent les enregistrements affichés.</span><span class="sxs-lookup"><span data-stu-id="12ae5-117">With this action, Excel respects most filters on the page that limit the records shown.</span></span> <span data-ttu-id="12ae5-118">Cela signifie que le classeur Excel contiendra presque les mêmes enregistrements et colonnes.</span><span class="sxs-lookup"><span data-stu-id="12ae5-118">This means that the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="12ae5-119">L'avantage de l'action **Modifier dans Excel** est qu'elle vous permet d'apporter des modifications à des enregistrements dans Excel puis de les publier dans [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="12ae5-119">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="12ae5-120">Ceci fonctionne uniquement sur Windows, pas macOS.</span><span class="sxs-lookup"><span data-stu-id="12ae5-120">It only works on Windows; not macOS.</span></span>

<span data-ttu-id="12ae5-121">Cela a été amélioré dans la deuxième vague de publication 2019.</span><span class="sxs-lookup"><span data-stu-id="12ae5-121">This was enhanced in 2019 release wave 2.</span></span> <span data-ttu-id="12ae5-122">Pour plus d'informations, voir [Améliorations de l'intégration Excel](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span><span class="sxs-lookup"><span data-stu-id="12ae5-122">For more information, see [Enhancements to Excel integration](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span></span>

> [!NOTE]
> <span data-ttu-id="12ae5-123">Pour [!INCLUDE[prodshort](includes/prodshort.md)] sur site, l'action **Modifier dans Excel** est disponible uniquement si le module complémentaire Excel a été configuré par votre administrateur.</span><span class="sxs-lookup"><span data-stu-id="12ae5-123">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator.</span></span> <span data-ttu-id="12ae5-124">Pour les administrateurs, si vous souhaitez connaître la manière de configurer le module complémentaire Excel, consultez [Configuration du module complémentaire Excel pour modifier des données Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="12ae5-124">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

> [!NOTE]
> <span data-ttu-id="12ae5-125">Pour [!INCLUDE[prodshort](includes/prodshort.md)]sur site, cette fonctionnalité est uniquement disponible pour le client Web.</span><span class="sxs-lookup"><span data-stu-id="12ae5-125">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, this feature is only available for the Web client.</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="12ae5-126">Voir les différences entre les options</span><span class="sxs-lookup"><span data-stu-id="12ae5-126">See the differences between the options</span></span> 
> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-also"></a><span data-ttu-id="12ae5-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12ae5-127">See Also</span></span>
[<span data-ttu-id="12ae5-128">Utilisation de Business Central</span><span class="sxs-lookup"><span data-stu-id="12ae5-128">Working with Business Central</span></span>](ui-work-product.md)  
