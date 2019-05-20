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
ms.openlocfilehash: d55d8d5ab916cee6600deaf891702a625d76d7ee
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245700"
---
# <a name="view-the-status-of-a-synchronization"></a><span data-ttu-id="0c2e9-103">Afficher le statut d'une synchronisation</span><span class="sxs-lookup"><span data-stu-id="0c2e9-103">View the Status of a Synchronization</span></span>
<span data-ttu-id="0c2e9-104">Vous pouvez visualiser le statut des différents projets de synchronisation qui ont été exécutés pour l'intégration de [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="0c2e9-104">You can view the status of the individual synchronization jobs that have been run for [!INCLUDE[crm_md](includes/crm_md.md)] integration.</span></span> <span data-ttu-id="0c2e9-105">Cela inclut les projets de synchronisation qui ont été exécutés à partir de la file projets et les projets de synchronisation manuels qui ont été exécutés sur les enregistrements à partir du client [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="0c2e9-105">This includes synchronization jobs that have been run from the job queue and manual synchronization jobs that were performed on records from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="0c2e9-106">Cela est utile lors de la résolution des problèmes de synchronisation, car vous pouvez accéder aux détails sur les erreurs spécifiques qui se produisent.</span><span class="sxs-lookup"><span data-stu-id="0c2e9-106">This is helpful when troubleshooting synchronization problems because it gives you access to details about specific errors.</span></span>

### <a name="to-view-all-synchronization-issues"></a><span data-ttu-id="0c2e9-107">Pour visualiser tous les problèmes de synchronisation</span><span class="sxs-lookup"><span data-stu-id="0c2e9-107">To view all synchronization issues</span></span>
1. <span data-ttu-id="0c2e9-108">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Erreurs de synchronisation des données couplées**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="0c2e9-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Coupled Data Synchronization Errors**, and then choose the related link.</span></span>
2. <span data-ttu-id="0c2e9-109">Sur la page **Erreurs de synchronisation des données couplées**, affichez la vue de tous les problèmes survenus lors de la synchronisation des données entre [!INCLUDE[crm_md](includes/crm_md.md)] et [!INCLUDE[d365fin](includes/d365fin_md.md)], filtrez et triez les enregistrements dans la page par table, message d'erreur et sélectionnez des options telles que **Réessayer** ou **Supprimer le couplage** pour résoudre les problèmes tour à tour ou en bloc.</span><span class="sxs-lookup"><span data-stu-id="0c2e9-109">On the **Coupled Data Synchronization Errors** page you can view of all issues that occurred in synchronization of data between [!INCLUDE[crm_md](includes/crm_md.md)] and [!INCLUDE[d365fin](includes/d365fin_md.md)], filter and sort records in the page by table, error message and take actions such as **Retry** or **Remove Coupling** to resolve issues one by one or in bulk.</span></span>

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a><span data-ttu-id="0c2e9-110">Pour afficher le journal de synchronisation pour un enregistrement spécifique (synchronisé manuellement)</span><span class="sxs-lookup"><span data-stu-id="0c2e9-110">To view synchronization log for specific (manually synchronized) record</span></span>
1. <span data-ttu-id="0c2e9-111">Ouvrez, par exemple, le client, l'article ou tout autre enregistrement qui synchronise des données entre [!INCLUDE[d365fin](includes/d365fin_md.md)] et Sales.</span><span class="sxs-lookup"><span data-stu-id="0c2e9-111">Open, for example, customer, item or any other record that is synchronizing data between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Sales</span></span>
2. <span data-ttu-id="0c2e9-112">Sélectionnez l'action **Journal de synchronisation** pour afficher le journal de synchronisation pour l'enregistrement sélectionné, par exemple, le client spécifique que vous avez synchronisé manuellement.</span><span class="sxs-lookup"><span data-stu-id="0c2e9-112">Choose **Synchronization Log** action to view the synchronization log for selected record, for example, specific customer you synchronized manually</span></span>

## <a name="see-also"></a><span data-ttu-id="0c2e9-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c2e9-113">See Also</span></span>  
[<span data-ttu-id="0c2e9-114">Configuration de l'intégration de Dynamics 365 for Sales dans Business Central</span><span class="sxs-lookup"><span data-stu-id="0c2e9-114">Setting Up Dynamics 365 for Sales Integration in Business Central</span></span>](admin-setting-up-integration-with-dynamics-sales.md)  
[<span data-ttu-id="0c2e9-115">Utilisation de Dynamics 365 for Sales depuis Business Central</span><span class="sxs-lookup"><span data-stu-id="0c2e9-115">Using Dynamics 365 for Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
