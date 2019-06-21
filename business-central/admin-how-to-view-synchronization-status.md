---
title: Afficher le statut d'une synchronisation | Microsoft Docs
description: Découvrez comment afficher le statut d'un projet de synchronisation individuelle.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 11e29674c2d12031fdf4e7f66e767be4fcc74795
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 06/06/2019
ms.locfileid: "1620899"
---
# <a name="view-the-status-of-a-synchronization"></a><span data-ttu-id="bbf94-103">Afficher le statut d'une synchronisation</span><span class="sxs-lookup"><span data-stu-id="bbf94-103">View the Status of a Synchronization</span></span>
<span data-ttu-id="bbf94-104">Vous pouvez visualiser le statut des différents projets de synchronisation qui ont été exécutés pour l'intégration de [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="bbf94-104">You can view the status of the individual synchronization jobs that have been run for [!INCLUDE[crm_md](includes/crm_md.md)] integration.</span></span> <span data-ttu-id="bbf94-105">Cela inclut les projets de synchronisation qui ont été exécutés à partir de la file projets et les projets de synchronisation manuels qui ont été exécutés sur les enregistrements à partir du client [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="bbf94-105">This includes synchronization jobs that have been run from the job queue and manual synchronization jobs that were performed on records from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="bbf94-106">Cela est utile lors de la résolution des problèmes de synchronisation, car vous pouvez accéder aux détails sur les erreurs spécifiques qui se produisent.</span><span class="sxs-lookup"><span data-stu-id="bbf94-106">This is helpful when troubleshooting synchronization problems because it gives you access to details about specific errors.</span></span>

### <a name="to-view-synchronization-issues-for-coupled-records"></a><span data-ttu-id="bbf94-107">Pour afficher les problèmes de synchronisation des enregistrements couplés</span><span class="sxs-lookup"><span data-stu-id="bbf94-107">To view synchronization issues for coupled records</span></span>
1. <span data-ttu-id="bbf94-108">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Erreurs de synchronisation des données couplées**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="bbf94-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Coupled Data Synchronization Errors**, and then choose the related link.</span></span>
2. <span data-ttu-id="bbf94-109">La page **Erreurs de synchronisation des données couplées** affiche les problèmes qui se produisent lorsque vous avez synchronisé des enregistrements couplés.</span><span class="sxs-lookup"><span data-stu-id="bbf94-109">The **Coupled Data Synchronization Errors** page shows issues that occurred when you synchronized coupled records.</span></span> <span data-ttu-id="bbf94-110">Vous pouvez filtrer et trier des enregistrements et effectuer des actions comme **Restaurer** ou **Supprimer des enregistrements** pour résoudre les problèmes un par un.</span><span class="sxs-lookup"><span data-stu-id="bbf94-110">You can filter and sort records and take actions such as **Restore** or **Delete Records** to resolve issues one by one.</span></span>

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a><span data-ttu-id="bbf94-111">Pour afficher le journal de synchronisation pour un enregistrement spécifique (synchronisé manuellement)</span><span class="sxs-lookup"><span data-stu-id="bbf94-111">To view synchronization log for specific (manually synchronized) record</span></span>
1. <span data-ttu-id="bbf94-112">Ouvrez, par exemple, un client, un article ou tout autre enregistrement qui synchronise des données entre [!INCLUDE[d365fin](includes/d365fin_md.md)] et Sales.</span><span class="sxs-lookup"><span data-stu-id="bbf94-112">Open, for example, a customer, item or any other record that is synchronizing data between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Sales.</span></span>
2. <span data-ttu-id="bbf94-113">Choisissez l'action **Journal de synchronisation** pour afficher le journal de synchronisation pour un enregistrement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="bbf94-113">Choose the **Synchronization Log** action to view the synchronization log for a selected record.</span></span> <span data-ttu-id="bbf94-114">Par exemple, un client spécifique que vous avez synchronisé manuellement.</span><span class="sxs-lookup"><span data-stu-id="bbf94-114">For example, a specific customer you synchronized manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="bbf94-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbf94-115">See Also</span></span>  
[<span data-ttu-id="bbf94-116">Configuration de l'intégration de Dynamics 365 for Sales dans Business Central</span><span class="sxs-lookup"><span data-stu-id="bbf94-116">Setting Up Dynamics 365 for Sales Integration in Business Central</span></span>](admin-setting-up-integration-with-dynamics-sales.md)  
[<span data-ttu-id="bbf94-117">Utilisation de Dynamics 365 for Sales depuis Business Central</span><span class="sxs-lookup"><span data-stu-id="bbf94-117">Using Dynamics 365 for Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
