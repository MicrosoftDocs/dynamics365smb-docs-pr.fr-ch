---
title: Comment configurer des employés d'entrepôt | Microsoft Docs
description: Chaque utilisateur exerçant une activité dans un entrepôt doit être configuré en tant qu'employé d'entrepôt affecté à un magasin par défaut, et éventuellement à d'autres magasins.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 823ff60b27f1454b84b0096606e9175a15b261c9
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "922400"
---
# <a name="set-up-warehouse-employees"></a><span data-ttu-id="b8246-103">Configurer des employés d'entrepôt</span><span class="sxs-lookup"><span data-stu-id="b8246-103">Set Up Warehouse Employees</span></span>
<span data-ttu-id="b8246-104">Chaque utilisateur exerçant une activité dans un entrepôt doit être configuré en tant qu'employé d'entrepôt affecté à un magasin par défaut, et éventuellement à d'autres magasins.</span><span class="sxs-lookup"><span data-stu-id="b8246-104">Each user who performs warehouse activities must be set up as a warehouse employee assigned to one default location and potentially more non-default locations.</span></span> <span data-ttu-id="b8246-105">Cette configuration d'utilisateur filtre toutes les activités entrepôt dans la base de donnée pour le magasin de l'employé, de sorte que l'employé peut uniquement effectuer les activités entrepôt dans le magasin par défaut.</span><span class="sxs-lookup"><span data-stu-id="b8246-105">This user setup filters all warehouse activities across the database to the employee's location so that the employee can only perform the warehouse activities at the default location.</span></span> <span data-ttu-id="b8246-106">Un utilisateur peut être affecté à d'autres magasins pour lesquels il peut consulter les lignes activité sans pour autant exécuter les activités.</span><span class="sxs-lookup"><span data-stu-id="b8246-106">A user can be assigned to additional non-default locations for which the employee can view activity lines but not perform the activities.</span></span>

## <a name="to-set-up-warehouse-employees"></a><span data-ttu-id="b8246-107">Pour configurer des employés d'entrepôt</span><span class="sxs-lookup"><span data-stu-id="b8246-107">To set up warehouse employees</span></span>  
1.  <span data-ttu-id="b8246-108">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Magasiniers**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="b8246-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b8246-109">Sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="b8246-109">Choose the **New** action.</span></span>  
3. <span data-ttu-id="b8246-110">Sélectionnez le champ **Code utilisateur**, puis sélectionnez l'utilisateur à ajouter comme magasinier.</span><span class="sxs-lookup"><span data-stu-id="b8246-110">Select the **User ID** field, and then select the user to be added as a warehouse employee.</span></span> <span data-ttu-id="b8246-111">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8246-111">Choose the **OK** button.</span></span>  
6.  <span data-ttu-id="b8246-112">Dans le champ **Code magasin**, entrez le code du magasin dans lequel va travailler l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b8246-112">In the **Location Code** field, enter the code of the location where the user will be working.</span></span>  
7.  <span data-ttu-id="b8246-113">Activez la case à cocher **Par défaut** pour définir le magasin comme seul emplacement pour les activités entrepôt de l'employé.</span><span class="sxs-lookup"><span data-stu-id="b8246-113">Select the **Default** check box to define the location as the only location where the employee can perform warehouse activities.</span></span>  
8.  <span data-ttu-id="b8246-114">Répétez ces étapes pour affecter d'autres employés à des magasins ou affecter d'autres magasins à des employés d'entrepôt existants.</span><span class="sxs-lookup"><span data-stu-id="b8246-114">Repeat these steps to assign other employees to locations or assign non-default locations to existing warehouse employees.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b8246-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8246-115">See Also</span></span>  
[<span data-ttu-id="b8246-116">Gestion d'entrepôt</span><span class="sxs-lookup"><span data-stu-id="b8246-116">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="b8246-117">STOCKS ET EN-COURS</span><span class="sxs-lookup"><span data-stu-id="b8246-117">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="b8246-118">[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="b8246-118">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="b8246-119">[Gestion des assemblages](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="b8246-119">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="b8246-120">Détails de conception : gestion d'entrepôt</span><span class="sxs-lookup"><span data-stu-id="b8246-120">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="b8246-121">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b8246-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
