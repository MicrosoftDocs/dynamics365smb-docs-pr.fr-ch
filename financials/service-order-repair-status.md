---
title: "Paramétrer les statuts des commandes service et des réparations | Microsoft Docs"
description: "Vous devez paramétrer neuf états réparation qui identifient la progression de la réparation et de la maintenance des articles de service des commandes service."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 36925a08f7fdfffedf13902a5c6feaaa8b0929a4
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-statuses-for-service-orders-and-repairs"></a><span data-ttu-id="2e143-103">Procédure : paramétrer les statuts des commandes service et des réparations</span><span class="sxs-lookup"><span data-stu-id="2e143-103">How to: Set Up Statuses for Service Orders and Repairs</span></span>
<span data-ttu-id="2e143-104">Vous devez paramétrer des états réparation qui identifient la progression de la réparation et de la maintenance des articles de service des commandes service.</span><span class="sxs-lookup"><span data-stu-id="2e143-104">You must set up repair status options that identify the progress of repair and maintenance of service items in service orders.</span></span> <span data-ttu-id="2e143-105">Vous devez configurer au moins neuf options de statut réparation identifiant les situations ou les actions effectuées lors de la maintenance des articles de service.</span><span class="sxs-lookup"><span data-stu-id="2e143-105">You must set up at least nine repair status options that identify situations or actions taken when servicing service items.</span></span>  

<span data-ttu-id="2e143-106">Vous pouvez définir le niveau de priorité des options de statut commande service.</span><span class="sxs-lookup"><span data-stu-id="2e143-106">You can set the priority level for service order status options.</span></span> <span data-ttu-id="2e143-107">Quatre niveaux de priorité sont disponibles : Très haute, Haute, Moyenne et Basse.</span><span class="sxs-lookup"><span data-stu-id="2e143-107">There four priorities are High, Medium High, Medium Low, and Low.</span></span>  
  
<span data-ttu-id="2e143-108">Lorsque vous modifiez le statut réparation d'un article de service d'une commande service, le statut commande service est mis à jour.</span><span class="sxs-lookup"><span data-stu-id="2e143-108">When you change the repair status of a service item in a service order, the service order status is updated.</span></span> <span data-ttu-id="2e143-109">Le statut réparation de chaque article de service est lié au statut commande service.</span><span class="sxs-lookup"><span data-stu-id="2e143-109">The repair status of each service item is linked to the service order status.</span></span> <span data-ttu-id="2e143-110">Si les articles de service sont liés à plusieurs options de statut commande service, le statut de commande service dont la priorité est la plus élevée est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="2e143-110">If the service items are linked to two or more service order status options, the service order status with the highest priority is selected.</span></span>  

## <a name="to-set-up-a-repair-status"></a><span data-ttu-id="2e143-111">Pour configurer le statut réparation</span><span class="sxs-lookup"><span data-stu-id="2e143-111">To set up a repair status</span></span>  
1. <span data-ttu-id="2e143-112">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Etat de la réparation**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="2e143-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Repair Status**, and then choose the related link.</span></span> <span data-ttu-id="2e143-113">2.</span><span class="sxs-lookup"><span data-stu-id="2e143-113">2.</span></span> <span data-ttu-id="2e143-114">Créez un état réparation.</span><span class="sxs-lookup"><span data-stu-id="2e143-114">Create a new repair status.</span></span>  
3. <span data-ttu-id="2e143-115">Renseignez les champs **Code** et **Désignation**.</span><span class="sxs-lookup"><span data-stu-id="2e143-115">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="2e143-116">Dans le champ **Statut commande service**, choisissez le statut de la commande auquel lier l'état de réparation.</span><span class="sxs-lookup"><span data-stu-id="2e143-116">In the **Service Order Status** field, choose the order status to link the repair status to.</span></span> <span data-ttu-id="2e143-117">Le champ **Priorité** affiche la priorité du statut commande service que vous avez choisie.</span><span class="sxs-lookup"><span data-stu-id="2e143-117">The **Priority** field displays the priority of the service order status you have chosen.</span></span>  
5. <span data-ttu-id="2e143-118">Choisissez un état réparation.</span><span class="sxs-lookup"><span data-stu-id="2e143-118">Choose a repair status.</span></span> <span data-ttu-id="2e143-119">Vous ne pouvez en choisir qu'un.</span><span class="sxs-lookup"><span data-stu-id="2e143-119">You can choose only one.</span></span>  
6. <span data-ttu-id="2e143-120">Pour valider des commandes service comprenant des articles de service avec cet état réparation, choisissez le champ **Validation autorisée**.</span><span class="sxs-lookup"><span data-stu-id="2e143-120">To be able to post service orders, including service items, with this repair status, choose the **Posting Allowed** field.</span></span>  
7. <span data-ttu-id="2e143-121">Pour pouvoir faire passer manuellement l'option de statut commande service sur **Suspendu** dans des commandes service comprenant des articles de service avec ce statut réparation, choisissez la case à cocher **Statut Suspendu autorisé**.</span><span class="sxs-lookup"><span data-stu-id="2e143-121">To be able to manually change the service order status option to **Pending** in service orders including service items with this repair status, choose the **Pending Status Allowed** check box.</span></span>  
8. <span data-ttu-id="2e143-122">Choisissez de la même manière les cases à cocher **Statut En cours autorisé**, **Statut Terminé autorisé** et **Statut En attente autorisé**.</span><span class="sxs-lookup"><span data-stu-id="2e143-122">Choose the **In Process Status Allowed**, **Finished Status Allowed**, and **On Hold Status Allowed** check boxes in the same way.</span></span>
  
## <a name="to-set-up-service-status-priorities"></a><span data-ttu-id="2e143-123">Pour configurer les priorités statut service</span><span class="sxs-lookup"><span data-stu-id="2e143-123">To set up service status priorities</span></span>  
1. <span data-ttu-id="2e143-124">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Statut commande service**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="2e143-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Order Status**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2e143-125">Sélectionnez le statut commande service pour lequel vous voulez configurer une priorité.</span><span class="sxs-lookup"><span data-stu-id="2e143-125">Select the service order status you want to set a priority for.</span></span>  
3. <span data-ttu-id="2e143-126">Dans le champ **Priorité**, choisissez la priorité souhaitée pour ce statut commande service.</span><span class="sxs-lookup"><span data-stu-id="2e143-126">In the **Priority** field, choose the priority you want for this service order status.</span></span> <span data-ttu-id="2e143-127">Répétez cette étape pour chaque statut.</span><span class="sxs-lookup"><span data-stu-id="2e143-127">Repeat this step for each status.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2e143-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e143-128">See Also</span></span>  
[<span data-ttu-id="2e143-129">Description des commandes service et de l'état réparation</span><span class="sxs-lookup"><span data-stu-id="2e143-129">Understanding Service Order Status and Repair Status</span></span>]()  
[<span data-ttu-id="2e143-130">Paramétrage de la gestion des services</span><span class="sxs-lookup"><span data-stu-id="2e143-130">Setting Up Service Management</span></span>](service-setup-service.md)  

