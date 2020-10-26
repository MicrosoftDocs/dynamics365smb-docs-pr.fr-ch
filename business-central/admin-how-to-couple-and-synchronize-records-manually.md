---
title: Coupler et synchroniser manuellement des enregistrements | Microsoft Docs
description: Synchroniser un mappage de table d’intégration permet la synchronisation des données dans tous les enregistrements dans une table de Business Central ainsi que de l’entité Dynamics 365 Sales qui sont couplées.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: d8140f71709208a271eff5c8de415b0e95736072
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911420"
---
# <a name="couple-and-synchronize-records-manually"></a><span data-ttu-id="5d2de-103">Coupler et synchroniser manuellement des enregistrements</span><span class="sxs-lookup"><span data-stu-id="5d2de-103">Couple and Synchronize Records Manually</span></span>
<span data-ttu-id="5d2de-104">Cette rubrique décrit comment coupler un ou plusieurs enregistrements dans [!INCLUDE[d365fin](includes/d365fin_md.md)] avec des enregistrements dans Common Data Service ou [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5d2de-104">This topic describes how to couple one or more records in [!INCLUDE[d365fin](includes/d365fin_md.md)] with records in Common Data Service or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="5d2de-105">Le couplage d’enregistrements permet d’afficher les informations Common Data Service depuis [!INCLUDE[d365fin](includes/d365fin_md.md)], et vice-versa.</span><span class="sxs-lookup"><span data-stu-id="5d2de-105">Coupling records lets you view Common Data Service information from [!INCLUDE[d365fin](includes/d365fin_md.md)], and vice versa.</span></span> <span data-ttu-id="5d2de-106">Le couplage vous permet également de synchroniser les données entre les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="5d2de-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="5d2de-107">Vous pouvez coupler des enregistrements existants, ou créer et coupler de nouveaux enregistrements.</span><span class="sxs-lookup"><span data-stu-id="5d2de-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="5d2de-108">Le couplage et la synchronisation des données sont disponibles seulement si votre administrateur système a créé une connexion entre [!INCLUDE[d365fin](includes/d365fin_md.md)] et Common Data Service ou [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5d2de-108">Coupling and synchronizing data is available only if your system administrator has created a connection between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Common Data Service or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="5d2de-109">Une façon de vérifier consiste à ouvrir la fiche **Client** et à rechercher l’action **Configurer le couplage** .</span><span class="sxs-lookup"><span data-stu-id="5d2de-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="5d2de-110">Si l’action est disponible, les applications sont connectées.</span><span class="sxs-lookup"><span data-stu-id="5d2de-110">If the action is available, the apps are connected.</span></span>   

## <a name="video-example"></a><span data-ttu-id="5d2de-111">Exemple vidéo</span><span class="sxs-lookup"><span data-stu-id="5d2de-111">Video Example</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a><span data-ttu-id="5d2de-112">Pour coupler un enregistrement</span><span class="sxs-lookup"><span data-stu-id="5d2de-112">To couple a record</span></span>  
1.  <span data-ttu-id="5d2de-113">Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], ouvrez la fiche pour l’enregistrement que vous souhaitez coupler.</span><span class="sxs-lookup"><span data-stu-id="5d2de-113">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="5d2de-114">Par exemple, la fiche Client ou Contact.</span><span class="sxs-lookup"><span data-stu-id="5d2de-114">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="5d2de-115">Vous pouvez également ouvrir la page de liste et sélectionner l’enregistrement à coupler.</span><span class="sxs-lookup"><span data-stu-id="5d2de-115">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="5d2de-116">Choisissez l’action **Configurer le couplage** .</span><span class="sxs-lookup"><span data-stu-id="5d2de-116">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="5d2de-117">Renseignez les champs, puis cliquez sur **OK** .</span><span class="sxs-lookup"><span data-stu-id="5d2de-117">Fill in the fields, and then choose **OK** .</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="5d2de-118">Pour synchroniser un enregistrement unique</span><span class="sxs-lookup"><span data-stu-id="5d2de-118">To synchronize a single record</span></span>  
1.  <span data-ttu-id="5d2de-119">Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], ouvrez la fiche pour l’enregistrement que vous souhaitez coupler.</span><span class="sxs-lookup"><span data-stu-id="5d2de-119">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="5d2de-120">Par exemple, la fiche Client ou Contact.</span><span class="sxs-lookup"><span data-stu-id="5d2de-120">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="5d2de-121">Choisissez l’action **Synchroniser maintenant** .</span><span class="sxs-lookup"><span data-stu-id="5d2de-121">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="5d2de-122">Si un enregistrement peut être synchronisé dans une direction, sélectionnez l’option qui affiche la direction de la mise à jour des données, puis cliquez sur **OK** .</span><span class="sxs-lookup"><span data-stu-id="5d2de-122">If a record can be synchronized in one direction, select the option that specifies the direction of data update, and then choose **OK** .</span></span>  

## <a name="to-synchronize-a-single-record-from-crm_md"></a><span data-ttu-id="5d2de-123">Pour synchroniser un enregistrement unique à partir de [!INCLUDE[crm_md](includes/crm_md.md)]</span><span class="sxs-lookup"><span data-stu-id="5d2de-123">To synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)]</span></span>  
1.  <span data-ttu-id="5d2de-124">Dans [!INCLUDE[crm_md](includes/crm_md.md)], ouvrez le formulaire pour l’enregistrement que vous souhaitez coupler.</span><span class="sxs-lookup"><span data-stu-id="5d2de-124">In [!INCLUDE[crm_md](includes/crm_md.md)], open the form for the record you want to couple.</span></span> <span data-ttu-id="5d2de-125">Par exemple, le formulaire Fiche Compte ou Fiche Contact.</span><span class="sxs-lookup"><span data-stu-id="5d2de-125">For example, the Account card or Contact card form.</span></span>  
2.  <span data-ttu-id="5d2de-126">Choisissez l’action **[!INCLUDE[d365fin](includes/d365fin_md.md)]** dans le ruban pour ouvrir et coupler l’enregistrement automatiquement.</span><span class="sxs-lookup"><span data-stu-id="5d2de-126">Choose the **[!INCLUDE[d365fin](includes/d365fin_md.md)]** action in the ribbon to open and couple record automatically.</span></span>

> [!Note]
> <span data-ttu-id="5d2de-127">Vous pouvez synchroniser automatiquement un enregistrement unique depuis [!INCLUDE[crm_md](includes/crm_md.md)] seulement si l’option **Synch. uniquement les enregistrements couplés** est désactivée et si la direction de synchronisation est définie sur Bidirectionnelle ou À partir de la table d’intégration sur la page **Mappage de table d’intégration** pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="5d2de-127">You can synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)] automatically only when **Sync. Only Coupled Records** is disabled and the synchronization direction is set to Bidirectional or From Integration Table on the **Integration Table Mapping** page for the record.</span></span> <span data-ttu-id="5d2de-128">Pour en savoir plus, consultez [Mappage des tables et des champs à synchroniser](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span><span class="sxs-lookup"><span data-stu-id="5d2de-128">For more information, see [Mapping the Tables and Fields to Synchronize](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span></span>     

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="5d2de-129">Pour synchroniser plusieurs enregistrements</span><span class="sxs-lookup"><span data-stu-id="5d2de-129">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="5d2de-130">Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], ouvrez la page de liste pour l’enregistrement, telle que Clients ou Contacts.</span><span class="sxs-lookup"><span data-stu-id="5d2de-130">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="5d2de-131">Sélectionnez l’enregistrement à synchroniser, puis l’action **Synchroniser maintenant** .</span><span class="sxs-lookup"><span data-stu-id="5d2de-131">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="5d2de-132">Si des enregistrements peuvent être synchronisés dans une direction, sélectionnez l’option qui affiche la direction, puis cliquez sur **OK** .</span><span class="sxs-lookup"><span data-stu-id="5d2de-132">If records can be synchronized in one direction, select the option that specifies the direction, and then choose **OK** .</span></span>  

## <a name="see-also"></a><span data-ttu-id="5d2de-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d2de-133">See Also</span></span>  
[<span data-ttu-id="5d2de-134">Utilisation de Dynamics 365 Sales depuis Business Central</span><span class="sxs-lookup"><span data-stu-id="5d2de-134">Using Dynamics 365 Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
