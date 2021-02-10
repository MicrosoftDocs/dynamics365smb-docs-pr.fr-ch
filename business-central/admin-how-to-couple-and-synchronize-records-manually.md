---
title: Couplage et synchronisation | Microsoft Docs
description: Synchroniser un mappage de table d’intégration permet la synchronisation des données dans tous les enregistrements dans une table de Business Central ainsi que de la table Dynamics 365 Sales qui sont couplées.
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
ms.openlocfilehash: fa4d6cfe13662613a73c14d68542f8319798ea80
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752690"
---
# <a name="coupling-and-synchronizing"></a><span data-ttu-id="42c22-103">Couplage et synchronisation</span><span class="sxs-lookup"><span data-stu-id="42c22-103">Coupling and Synchronizing</span></span>
<span data-ttu-id="42c22-104">Cette rubrique décrit comment coupler un ou plusieurs enregistrements dans [!INCLUDE[prod_short](includes/prod_short.md)] avec des enregistrements dans Dataverse ou [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="42c22-104">This topic describes how to couple one or more records in [!INCLUDE[prod_short](includes/prod_short.md)] with records in Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="42c22-105">Le couplage d’enregistrements permet d’afficher les informations Dataverse depuis [!INCLUDE[prod_short](includes/prod_short.md)], et vice-versa.</span><span class="sxs-lookup"><span data-stu-id="42c22-105">Coupling records lets you view Dataverse information from [!INCLUDE[prod_short](includes/prod_short.md)], and vice versa.</span></span> <span data-ttu-id="42c22-106">Le couplage vous permet également de synchroniser les données entre les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="42c22-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="42c22-107">Vous pouvez coupler des enregistrements existants, ou créer et coupler de nouveaux enregistrements.</span><span class="sxs-lookup"><span data-stu-id="42c22-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="42c22-108">Le couplage et la synchronisation des données sont disponibles seulement si votre administrateur système a créé une connexion entre [!INCLUDE[prod_short](includes/prod_short.md)] et Dataverse ou [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="42c22-108">Coupling and synchronizing data is available only if your system administrator has created a connection between [!INCLUDE[prod_short](includes/prod_short.md)] and Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="42c22-109">Une façon de vérifier consiste à ouvrir la fiche **Client** et à rechercher l’action **Configurer le couplage**.</span><span class="sxs-lookup"><span data-stu-id="42c22-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="42c22-110">Si l’action est disponible, les applications sont connectées.</span><span class="sxs-lookup"><span data-stu-id="42c22-110">If the action is available, the apps are connected.</span></span>   

## <a name="video-example"></a><span data-ttu-id="42c22-111">Exemple vidéo</span><span class="sxs-lookup"><span data-stu-id="42c22-111">Video Example</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a><span data-ttu-id="42c22-112">Pour coupler un enregistrement</span><span class="sxs-lookup"><span data-stu-id="42c22-112">To couple a record</span></span>  
1.  <span data-ttu-id="42c22-113">Dans [!INCLUDE[prod_short](includes/prod_short.md)], ouvrez la fiche pour l’enregistrement que vous souhaitez coupler.</span><span class="sxs-lookup"><span data-stu-id="42c22-113">In [!INCLUDE[prod_short](includes/prod_short.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="42c22-114">Par exemple, la fiche Client ou Contact.</span><span class="sxs-lookup"><span data-stu-id="42c22-114">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="42c22-115">Vous pouvez également ouvrir la page de liste et sélectionner l’enregistrement à coupler.</span><span class="sxs-lookup"><span data-stu-id="42c22-115">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="42c22-116">Choisissez l’action **Configurer le couplage**.</span><span class="sxs-lookup"><span data-stu-id="42c22-116">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="42c22-117">Renseignez les champs, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="42c22-117">Fill in the fields, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="42c22-118">Pour synchroniser un enregistrement unique</span><span class="sxs-lookup"><span data-stu-id="42c22-118">To synchronize a single record</span></span>  
1.  <span data-ttu-id="42c22-119">Dans [!INCLUDE[prod_short](includes/prod_short.md)], ouvrez la fiche pour l’enregistrement que vous souhaitez coupler.</span><span class="sxs-lookup"><span data-stu-id="42c22-119">In [!INCLUDE[prod_short](includes/prod_short.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="42c22-120">Par exemple, la fiche Client ou Contact.</span><span class="sxs-lookup"><span data-stu-id="42c22-120">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="42c22-121">Choisissez l’action **Synchroniser maintenant**.</span><span class="sxs-lookup"><span data-stu-id="42c22-121">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="42c22-122">Si un enregistrement peut être synchronisé dans une direction, sélectionnez l’option qui affiche la direction de la mise à jour des données, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="42c22-122">If a record can be synchronized in one direction, select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record-from-crm_md"></a><span data-ttu-id="42c22-123">Pour synchroniser un enregistrement unique à partir de [!INCLUDE[crm_md](includes/crm_md.md)]</span><span class="sxs-lookup"><span data-stu-id="42c22-123">To synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)]</span></span>  
1.  <span data-ttu-id="42c22-124">Dans [!INCLUDE[crm_md](includes/crm_md.md)], ouvrez le formulaire pour l’enregistrement que vous souhaitez coupler.</span><span class="sxs-lookup"><span data-stu-id="42c22-124">In [!INCLUDE[crm_md](includes/crm_md.md)], open the form for the record you want to couple.</span></span> <span data-ttu-id="42c22-125">Par exemple, le formulaire Fiche Compte ou Fiche Contact.</span><span class="sxs-lookup"><span data-stu-id="42c22-125">For example, the Account card or Contact card form.</span></span>  
2.  <span data-ttu-id="42c22-126">Choisissez l’action **[!INCLUDE[prod_short](includes/prod_short.md)]** dans le ruban pour ouvrir et coupler l’enregistrement automatiquement.</span><span class="sxs-lookup"><span data-stu-id="42c22-126">Choose the **[!INCLUDE[prod_short](includes/prod_short.md)]** action in the ribbon to open and couple record automatically.</span></span>

> [!Note]
> <span data-ttu-id="42c22-127">Vous pouvez synchroniser automatiquement un enregistrement unique depuis [!INCLUDE[crm_md](includes/crm_md.md)] seulement si l’option **Synch. uniquement les enregistrements couplés** est désactivée et si la direction de synchronisation est définie sur Bidirectionnelle ou À partir de la table d’intégration sur la page **Mappage de table d’intégration** pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="42c22-127">You can synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)] automatically only when **Sync. Only Coupled Records** is disabled and the synchronization direction is set to Bidirectional or From Integration Table on the **Integration Table Mapping** page for the record.</span></span> <span data-ttu-id="42c22-128">Pour en savoir plus, consultez [Mappage des tables et des champs à synchroniser](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span><span class="sxs-lookup"><span data-stu-id="42c22-128">For more information, see [Mapping the Tables and Fields to Synchronize](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span></span>     

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="42c22-129">Pour synchroniser plusieurs enregistrements</span><span class="sxs-lookup"><span data-stu-id="42c22-129">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="42c22-130">Dans [!INCLUDE[prod_short](includes/prod_short.md)], ouvrez la page de liste pour l’enregistrement, telle que Clients ou Contacts.</span><span class="sxs-lookup"><span data-stu-id="42c22-130">In [!INCLUDE[prod_short](includes/prod_short.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="42c22-131">Sélectionnez l’enregistrement à synchroniser, puis l’action **Synchroniser maintenant**.</span><span class="sxs-lookup"><span data-stu-id="42c22-131">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="42c22-132">Si des enregistrements peuvent être synchronisés dans une direction, sélectionnez l’option qui affiche la direction, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="42c22-132">If records can be synchronized in one direction, select the option that specifies the direction, and then choose **OK**.</span></span>  

## <a name="uncoupling-records"></a><span data-ttu-id="42c22-133">Découplage des enregistrements</span><span class="sxs-lookup"><span data-stu-id="42c22-133">Uncoupling Records</span></span>
<span data-ttu-id="42c22-134">Vous pouvez découpler un ou plusieurs enregistrements des pages de liste ou sur la page **Erreurs de synchronisation de données couplées** en choisissant une ou plusieurs lignes et en choisissant **Supprimer le couplage**.</span><span class="sxs-lookup"><span data-stu-id="42c22-134">You can uncouple one or more records from list pages or the **Coupled Data Synchronization Errors** page by choosing one or more lines and choosing **Delete Coupling**.</span></span> <span data-ttu-id="42c22-135">Vous pouvez également supprimer tous les couplages pour un ou plusieurs mappages de table sur la page **Mappages de table d’intégration**.</span><span class="sxs-lookup"><span data-stu-id="42c22-135">You can also remove all couplings for one or more table mappings on the **Integration Table Mappings** page.</span></span>

## <a name="see-also"></a><span data-ttu-id="42c22-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42c22-136">See Also</span></span>  
[<span data-ttu-id="42c22-137">Utilisation de Dynamics 365 Sales depuis Business Central</span><span class="sxs-lookup"><span data-stu-id="42c22-137">Using Dynamics 365 Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
