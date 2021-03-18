---
title: Statut commande service et statut réparation
description: Le champ Statut de la page Commande service et le statut réparation de l’article de service, qui est représenté par le champ Code du statut de réparation sur la page Commande service ont une certaine relation dans le module Service management. Le statut commande service reflète l’état réparation de tous les articles de service de la commande service.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/15/2020
ms.author: edupont
ms.openlocfilehash: b9095cbfd1b8a55f525f0a3c4dcfad6cf56fc449
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386839"
---
# <a name="service-order-status-and-repair-status"></a><span data-ttu-id="c537a-104">Statut commande service et statut réparation</span><span class="sxs-lookup"><span data-stu-id="c537a-104">Service Order Status and Repair Status</span></span>

<span data-ttu-id="c537a-105">Le champ **Statut** de la page **Commande service** et le statut réparation de l’article de service, qui est représenté par le champ **Code du statut de réparation** sur la page **Commande service** ont une certaine relation dans le module Service management.</span><span class="sxs-lookup"><span data-stu-id="c537a-105">The **Status** field on the **Service Order** page and the service item repair status, which is represented by the **Repair Status Code** field on the **Service Order** page have a certain relationship in Service Management.</span></span> <span data-ttu-id="c537a-106">Le statut commande service reflète l’état réparation de tous les articles de service de la commande service.</span><span class="sxs-lookup"><span data-stu-id="c537a-106">The service order status reflects the repair status of all the service items in the service order.</span></span>  

> [!NOTE]  
> <span data-ttu-id="c537a-107">Ces deux champs de statut ne sont pas liés au champ **Statut de lancement** de l’en\-tête de commande de service, qui détermine la gestion des articles de service au niveau de l’entrepôt.</span><span class="sxs-lookup"><span data-stu-id="c537a-107">These two status field are not related to the **Release Status** field on the service order header, which determines how the warehouse handles service items.</span></span>  

<span data-ttu-id="c537a-108">Chaque fois que le statut réparation d’un article de service d’une commande service est modifié, le programme met à jour le statut de la commande.</span><span class="sxs-lookup"><span data-stu-id="c537a-108">Each time the repair status of a service item is changed in a service order, the status of the order is updated.</span></span> <span data-ttu-id="c537a-109">Pour afficher l’état réparation général des articles de service, vous devez préciser les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c537a-109">To display the status that reflects the overall repair status of the individual service items, you must specify the following:</span></span>  

* <span data-ttu-id="c537a-110">Le statut commande service auquel chaque état réparation est lié.</span><span class="sxs-lookup"><span data-stu-id="c537a-110">The service order status that each repair status is linked to.</span></span>  
* <span data-ttu-id="c537a-111">Le niveau de priorité de chaque option statut commande service.</span><span class="sxs-lookup"><span data-stu-id="c537a-111">The level of priority of each service order status option.</span></span>  

<span data-ttu-id="c537a-112">Lorsque vous convertissez un devis service en commande service, l’état réparation de chaque article de service de la commande est modifié à **Initial** et le statut de la commande service passe à **Suspendu**.</span><span class="sxs-lookup"><span data-stu-id="c537a-112">When you convert a service quote to a service order, the repair status of each service item is changed in the order to **Initial** and the service order status is changed to **Pending**.</span></span>  

> [!NOTE]
> <span data-ttu-id="c537a-113">Avant de pouvoir créer des commandes service, vous devez définir des statuts de réparation et des priorités de statut de service.</span><span class="sxs-lookup"><span data-stu-id="c537a-113">Before you can create service orders, you must set up repair statuses and service status priorities.</span></span> <span data-ttu-id="c537a-114">Pour plus d’informations, voir [Paramétrer les statuts des commandes service et des réparations](service-order-repair-status.md).</span><span class="sxs-lookup"><span data-stu-id="c537a-114">For more information, see [Set Up Statuses for Service Orders and Repairs](service-order-repair-status.md).</span></span>

## <a name="specifying-service-order-status-for-repair-status"></a><span data-ttu-id="c537a-115">Spécification du statut commande service pour l’état réparation</span><span class="sxs-lookup"><span data-stu-id="c537a-115">Specifying Service Order Status for Repair Status</span></span>

<span data-ttu-id="c537a-116">Chaque état réparation est lié à un statut commande service précis.</span><span class="sxs-lookup"><span data-stu-id="c537a-116">Each repair status is linked to a particular service order status.</span></span> <span data-ttu-id="c537a-117">Les options pour le statut commande service sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="c537a-117">The options for the service order status are as follows:</span></span>

* <span data-ttu-id="c537a-118">**Suspendu**</span><span class="sxs-lookup"><span data-stu-id="c537a-118">**Pending**</span></span>
* <span data-ttu-id="c537a-119">**En cours**</span><span class="sxs-lookup"><span data-stu-id="c537a-119">**In Process**</span></span>
* <span data-ttu-id="c537a-120">**En attente**</span><span class="sxs-lookup"><span data-stu-id="c537a-120">**On Hold**</span></span>
* <span data-ttu-id="c537a-121">**Terminé**</span><span class="sxs-lookup"><span data-stu-id="c537a-121">**Finished**</span></span>

<span data-ttu-id="c537a-122">Les options du statut de réparation sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="c537a-122">The repair status options are as follows:</span></span>

* <span data-ttu-id="c537a-123">**Initial**</span><span class="sxs-lookup"><span data-stu-id="c537a-123">**Initial**</span></span>
* <span data-ttu-id="c537a-124">**En cours**</span><span class="sxs-lookup"><span data-stu-id="c537a-124">**In Process**</span></span>
* <span data-ttu-id="c537a-125">**Expertisé**</span><span class="sxs-lookup"><span data-stu-id="c537a-125">**Referred**</span></span>
* <span data-ttu-id="c537a-126">**Service en partie réalisé**</span><span class="sxs-lookup"><span data-stu-id="c537a-126">**Partly Serviced**</span></span>
* <span data-ttu-id="c537a-127">**Devis terminé**</span><span class="sxs-lookup"><span data-stu-id="c537a-127">**Quote Finished**</span></span>
* <span data-ttu-id="c537a-128">**Attente réponse client**</span><span class="sxs-lookup"><span data-stu-id="c537a-128">**Waiting for Customer**</span></span>
* <span data-ttu-id="c537a-129">**Pièce de rechange commandée**</span><span class="sxs-lookup"><span data-stu-id="c537a-129">**Spare Part Ordered**</span></span>
* <span data-ttu-id="c537a-130">**Pièce de rechange reçue**</span><span class="sxs-lookup"><span data-stu-id="c537a-130">**Spare Part Received**</span></span>
* <span data-ttu-id="c537a-131">**Terminé**</span><span class="sxs-lookup"><span data-stu-id="c537a-131">**Finished**</span></span>  

### <a name="pending"></a><span data-ttu-id="c537a-132">Suspendu</span><span class="sxs-lookup"><span data-stu-id="c537a-132">Pending</span></span>

<span data-ttu-id="c537a-133">Le statut commande service **Suspendu** indique que le service peut démarrer ou continuer à n’importe quel moment.</span><span class="sxs-lookup"><span data-stu-id="c537a-133">The service order status **Pending** indicates that the service can start or continue at any time.</span></span> <span data-ttu-id="c537a-134">Pour cette raison, les quatre options d’état réparation **Initial**, **Expertisé**, **Service en partie réalisé** et **Pièce de rechange reçue** peuvent toutes être liées à ce statut commande service.</span><span class="sxs-lookup"><span data-stu-id="c537a-134">Therefore, the repair status options of **Initial**, **Referred**, **Partly Serviced**, and **Spare Part Received** can be linked to this service order status.</span></span>  

### <a name="in-process"></a><span data-ttu-id="c537a-135">En cours</span><span class="sxs-lookup"><span data-stu-id="c537a-135">In Process</span></span>

<span data-ttu-id="c537a-136">Le statut commande service **En cours** indique que le service est en cours.</span><span class="sxs-lookup"><span data-stu-id="c537a-136">The service order status **In Process** indicates that the service is in process.</span></span> <span data-ttu-id="c537a-137">Par conséquent, les deux options d’état de réparation **En cours** et **Pièce de rechange commandée** peuvent être liées à ce statut commande service.</span><span class="sxs-lookup"><span data-stu-id="c537a-137">Therefore, the repair status options **In Process** and **Spare Part Ordered** can both be linked to this service order status.</span></span> <span data-ttu-id="c537a-138">Si vous liez le statut **Pièce de rechange commandée** au statut commande service **En cours,** vous devez aussi lier le statut **Pièce de rechange reçue** à ce statut commande service.</span><span class="sxs-lookup"><span data-stu-id="c537a-138">If you link the **Spare Part Ordered** status to an **In Process** service order status, you must also link the **Spare Part Received** status to this service order status.</span></span>  

### <a name="on-hold"></a><span data-ttu-id="c537a-139">En attente</span><span class="sxs-lookup"><span data-stu-id="c537a-139">On Hold</span></span>

<span data-ttu-id="c537a-140">Le statut commande service **En attente** indique que le service est momentanément en attente, parce que vous attendez une réponse du client ou des pièces de rechange pour que le service puisse commencer.</span><span class="sxs-lookup"><span data-stu-id="c537a-140">The service order status **On Hold** indicates that the service is temporarily on hold because you are waiting for a customer response or spare parts before the service can start.</span></span> <span data-ttu-id="c537a-141">Pour cette raison, les trois options d’état réparation **Devis terminé**, **Pièce de rechange commandée** et **Attente réponse client** peuvent toutes être liées à ce statut commande service.</span><span class="sxs-lookup"><span data-stu-id="c537a-141">Therefore, the repair status options of **Quote Finished**, **Spare Part Ordered**, and **Waiting for Customer** can be linked to this service order status.</span></span>  

### <a name="finished"></a><span data-ttu-id="c537a-142">Terminé</span><span class="sxs-lookup"><span data-stu-id="c537a-142">Finished</span></span>

<span data-ttu-id="c537a-143">Le statut commande service **Terminé** indique que la maintenance est terminée.</span><span class="sxs-lookup"><span data-stu-id="c537a-143">The service order status **Finished** indicates that the service has been completed.</span></span> <span data-ttu-id="c537a-144">Pour cette raison, l’état réparation **Terminé** est lié à ce statut.</span><span class="sxs-lookup"><span data-stu-id="c537a-144">Therefore, the **Finished** repair status is linked to this status.</span></span>  

## <a name="assigning-priority-to-service-order-status"></a><span data-ttu-id="c537a-145">Affectation de priorité à des statuts commande service</span><span class="sxs-lookup"><span data-stu-id="c537a-145">Assigning Priority to Service Order Status</span></span>

<span data-ttu-id="c537a-146">Lorsque l’état réparation d’un article de service est modifié, les options statut commande service liées aux différentes options d’état réparation de tous les articles service de la commande sont identifiés.</span><span class="sxs-lookup"><span data-stu-id="c537a-146">When a repair status of a service item is changed, the service order status options linked to the different repair status options of all the service items in the order are identified.</span></span> <span data-ttu-id="c537a-147">Si les articles de service sont liés à plusieurs options de statut commande service, l’option de statut commande service dont la priorité est la plus élevée est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="c537a-147">If the service items are linked to two or more service order status options, the service order status option with the highest priority is selected.</span></span>  

<span data-ttu-id="c537a-148">Choisissez le statut commande service comportant les informations les plus importantes et affectez à ce statut la priorité la plus élevée, etc.</span><span class="sxs-lookup"><span data-stu-id="c537a-148">You must decide which service order status contains the most important information about the status of the service order and assign that status the highest priority, and so on.</span></span>  

<span data-ttu-id="c537a-149">Ensuite, lorsque vous créez une nouvelle commande service et que vous y ajoutez des articles de service, le champ **Priorité** sur l’en-tête commande service est mis à jour en fonction des priorités des articles de service.</span><span class="sxs-lookup"><span data-stu-id="c537a-149">Then, when you create a new service order and you add service items to it, the **Priority** field on the service order header is updated based on the priorities on the service items.</span></span>  

### <a name="example"></a><span data-ttu-id="c537a-150">Exemple :</span><span class="sxs-lookup"><span data-stu-id="c537a-150">Example</span></span>

<span data-ttu-id="c537a-151">Voici ci-après un exemple d’affectation de niveau de priorité :</span><span class="sxs-lookup"><span data-stu-id="c537a-151">A typical priority level assignment could be as follows:</span></span>  

* <span data-ttu-id="c537a-152">En cours - Très haute</span><span class="sxs-lookup"><span data-stu-id="c537a-152">In Process - High</span></span>  
* <span data-ttu-id="c537a-153">Suspendu - Haute</span><span class="sxs-lookup"><span data-stu-id="c537a-153">Pending - Medium high</span></span>  
* <span data-ttu-id="c537a-154">En attente - Moyenne</span><span class="sxs-lookup"><span data-stu-id="c537a-154">On Hold - Medium low</span></span>  
* <span data-ttu-id="c537a-155">Terminé - Basse</span><span class="sxs-lookup"><span data-stu-id="c537a-155">Finished - Low</span></span>  

<span data-ttu-id="c537a-156">Par exemple, si un article de service présente l’état réparation **Initial** (lié au statut commande service **Suspendu**), qu’un autre présente le statut **En cours** (lié au statut commande service **En cours**) et que le troisième présente le statut **Pièce de rechange commandée** (lié au statut commande service **En attente**), le statut commande service est **En cours** car il correspond au niveau de priorité le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="c537a-156">For example, if one service item has the repair status **Initial**, linked to the service order status **Pending**, another has the repair status **In Process**, linked to the service order status **In Process**, and a third has the repair status **Spare Part Ordered**, linked to the service order status **On Hold**, the resulting service order status will be **In Process** because this has the highest priority.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c537a-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c537a-157">See Also</span></span>

[<span data-ttu-id="c537a-158">Paramétrer les statuts des commandes service et des réparations</span><span class="sxs-lookup"><span data-stu-id="c537a-158">Set Up Statuses for Service Orders and Repairs</span></span>](service-order-repair-status.md)  
[<span data-ttu-id="c537a-159">Paramétrage de la gestion des services</span><span class="sxs-lookup"><span data-stu-id="c537a-159">Setting Up Service Management</span></span>](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]