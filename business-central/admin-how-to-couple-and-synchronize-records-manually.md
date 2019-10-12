---
title: Coupler et synchroniser manuellement des enregistrements | Microsoft Docs
description: Synchroniser un mappage de table d'intégration permet la synchronisation des données dans tous les enregistrements dans une table de Business Central ainsi que de l'entité Dynamics 365 Sales qui sont couplées.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 0c70b1ba34af32b7cf542149c8f15cb191761358
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308131"
---
# <a name="couple-and-synchronize-records-manually"></a><span data-ttu-id="73bd7-103">Coupler et synchroniser manuellement des enregistrements</span><span class="sxs-lookup"><span data-stu-id="73bd7-103">Couple and Synchronize Records Manually</span></span>
<span data-ttu-id="73bd7-104">Cette rubrique décrit comment coupler un ou plusieurs enregistrements dans [!INCLUDE[d365fin](includes/d365fin_md.md)] avec des enregistrements dans [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="73bd7-104">This topic describes how to couple one or more records in [!INCLUDE[d365fin](includes/d365fin_md.md)] with records in [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="73bd7-105">Le couplage d'enregistrements permet d'afficher les informations [!INCLUDE[crm_md](includes/crm_md.md)] depuis [!INCLUDE[d365fin](includes/d365fin_md.md)], et vice-versa.</span><span class="sxs-lookup"><span data-stu-id="73bd7-105">Coupling records lets you view [!INCLUDE[crm_md](includes/crm_md.md)] information from [!INCLUDE[d365fin](includes/d365fin_md.md)], and vice versa.</span></span> <span data-ttu-id="73bd7-106">Le couplage vous permet également de synchroniser les données entre les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="73bd7-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="73bd7-107">Vous pouvez coupler des enregistrements existants, ou créer et coupler de nouveaux enregistrements.</span><span class="sxs-lookup"><span data-stu-id="73bd7-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="73bd7-108">Le couplage et la synchronisation des données avec [!INCLUDE[crm_md](includes/crm_md.md)] sont disponibles uniquement si votre administrateur système a créé une connexion entre [!INCLUDE[d365fin](includes/d365fin_md.md)] et [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="73bd7-108">Coupling and synchronizing data with [!INCLUDE[crm_md](includes/crm_md.md)] is available only if your system administrator has created a connection between [!INCLUDE[d365fin](includes/d365fin_md.md)] and [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="73bd7-109">Une façon de vérifier consiste à ouvrir la fiche **Client** et à rechercher l'action **Configurer le couplage**.</span><span class="sxs-lookup"><span data-stu-id="73bd7-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="73bd7-110">Si l'action est disponible, les applications sont connectées.</span><span class="sxs-lookup"><span data-stu-id="73bd7-110">If the action is available, the apps are connected.</span></span>   

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a><span data-ttu-id="73bd7-111">Pour coupler un enregistrement</span><span class="sxs-lookup"><span data-stu-id="73bd7-111">To couple a record</span></span>  
1.  <span data-ttu-id="73bd7-112">Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], ouvrez la fiche pour l'enregistrement que vous souhaitez coupler.</span><span class="sxs-lookup"><span data-stu-id="73bd7-112">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="73bd7-113">Par exemple, la fiche Client ou Contact.</span><span class="sxs-lookup"><span data-stu-id="73bd7-113">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="73bd7-114">Vous pouvez également ouvrir la page de liste et sélectionner l'enregistrement à coupler.</span><span class="sxs-lookup"><span data-stu-id="73bd7-114">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="73bd7-115">Choisissez l'action **Configurer le couplage**.</span><span class="sxs-lookup"><span data-stu-id="73bd7-115">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="73bd7-116">Renseignez les champs, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="73bd7-116">Fill in the fields, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="73bd7-117">Pour synchroniser un enregistrement unique</span><span class="sxs-lookup"><span data-stu-id="73bd7-117">To synchronize a single record</span></span>  
1.  <span data-ttu-id="73bd7-118">Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], ouvrez la fiche pour l'enregistrement que vous souhaitez coupler.</span><span class="sxs-lookup"><span data-stu-id="73bd7-118">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="73bd7-119">Par exemple, la fiche Client ou Contact.</span><span class="sxs-lookup"><span data-stu-id="73bd7-119">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="73bd7-120">Choisissez l'action **Synchroniser maintenant**.</span><span class="sxs-lookup"><span data-stu-id="73bd7-120">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="73bd7-121">Si un enregistrement peut être synchronisé de [!INCLUDE[d365fin](includes/d365fin_md.md)] vers [!INCLUDE[crm_md](includes/crm_md.md)] ou de [!INCLUDE[crm_md](includes/crm_md.md)] vers [!INCLUDE[d365fin](includes/d365fin_md.md)], sélectionnez l'option qui affiche la direction de la mise à jour des données, puis cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="73bd7-121">If a record can be synchronized either from [!INCLUDE[d365fin](includes/d365fin_md.md)] to [!INCLUDE[crm_md](includes/crm_md.md)] or from [!INCLUDE[crm_md](includes/crm_md.md)] to [!INCLUDE[d365fin](includes/d365fin_md.md)], select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="73bd7-122">Pour synchroniser plusieurs enregistrements</span><span class="sxs-lookup"><span data-stu-id="73bd7-122">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="73bd7-123">Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], ouvrez la page de liste pour l'enregistrement, telle que Clients ou Contacts.</span><span class="sxs-lookup"><span data-stu-id="73bd7-123">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="73bd7-124">Sélectionnez l'enregistrement à synchroniser, puis l'action **Synchroniser maintenant**.</span><span class="sxs-lookup"><span data-stu-id="73bd7-124">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="73bd7-125">Si des enregistrements peuvent être synchronisés de [!INCLUDE[d365fin](includes/d365fin_md.md)] vers [!INCLUDE[crm_md](includes/crm_md.md)] ou de [!INCLUDE[crm_md](includes/crm_md.md)] vers [!INCLUDE[d365fin](includes/d365fin_md.md)], sélectionnez l'option qui affiche la direction de la mise à jour des données, puis cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="73bd7-125">If records can be synchronized either from [!INCLUDE[d365fin](includes/d365fin_md.md)] to [!INCLUDE[crm_md](includes/crm_md.md)] or from [!INCLUDE[crm_md](includes/crm_md.md)] to [!INCLUDE[d365fin](includes/d365fin_md.md)], select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="73bd7-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73bd7-126">See Also</span></span>  
[<span data-ttu-id="73bd7-127">Utilisation de Dynamics 365 Sales depuis Business Central</span><span class="sxs-lookup"><span data-stu-id="73bd7-127">Using Dynamics 365 Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
