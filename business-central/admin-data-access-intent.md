---
title: Gérer l’accès intentionnel à la base de données dans Business Central | Microsoft Docs
description: Modifiez l’accès intentionnel à la base de données pour les états, les pages API et les requêtes.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 502add82d2f70f6ffd13ae04f7eb6d214105fb63
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378613"
---
# <a name="managing-database-access-intent"></a><span data-ttu-id="238cd-103">Gestion de l’accès intentionnel à la base de données</span><span class="sxs-lookup"><span data-stu-id="238cd-103">Managing Database Access Intent</span></span> 

<span data-ttu-id="238cd-104">En tant que superutilisateur ou administrateur, vous pouvez modifier l’accès intentionnel à la base de données pour les états, les pages du type API et les requêtes pour améliorer les performances du service.</span><span class="sxs-lookup"><span data-stu-id="238cd-104">As a super user or administrator, you can change the database access intent on reports, pages of the type API, and queries to improve performance of the service.</span></span>

## <a name="overview"></a><span data-ttu-id="238cd-105">Aperçu</span><span class="sxs-lookup"><span data-stu-id="238cd-105">Overview</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="238cd-106">peut être configuré pour utiliser des répliques en lecture seule de la base de données principale (en lecture-écriture).</span><span class="sxs-lookup"><span data-stu-id="238cd-106">can be set up to use read-only replicas of the primary (read-write) database.</span></span> <span data-ttu-id="238cd-107">L’utilisation de répliques de la base de données réduit la charge sur la base de données principale.</span><span class="sxs-lookup"><span data-stu-id="238cd-107">Using the database replica reduces the load on the primary database.</span></span> <span data-ttu-id="238cd-108">Dans certains cas, cela améliore également les performances lors de l’affichage des données dans le client.</span><span class="sxs-lookup"><span data-stu-id="238cd-108">In some cases, it will also improve the performance when viewing data in the client.</span></span> <span data-ttu-id="238cd-109">Les répliques sont avantageuses pour les objets tels que les états, les requêtes et les pages API, qui permettent uniquement d’afficher les données, et non de les modifier.</span><span class="sxs-lookup"><span data-stu-id="238cd-109">Replicas are beneficial for objects, like reports, queries, and API pages, that are used for viewing data only, not modifying data.</span></span>

<span data-ttu-id="238cd-110">Lors de l’exécution des objets, l’accès intentionnel à la base de données détermine s’il faut utiliser une réplique en lecture seule, en cas de disponibilité, ou la base de données principale.</span><span class="sxs-lookup"><span data-stu-id="238cd-110">When objects run, the database access intent determines whether to use a read-only replica, if one is available, or the primary database.</span></span> <span data-ttu-id="238cd-111">Les états, les pages API et les requêtes sont développés avec un accès intentionnel à la base de données prédéfini (voir [Propriété DatabaseAccessIntent](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).</span><span class="sxs-lookup"><span data-stu-id="238cd-111">Reports, API pages, and queries are developed with a predefined database access intent (see [DatabaseAccessIntent property](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).</span></span>

<span data-ttu-id="238cd-112">La page **Liste d’accès intentionnels à la base de données** vous permet de remplacer l’accès intentionnel à la base de données prédéfini pour les objets lors de leur exécution.</span><span class="sxs-lookup"><span data-stu-id="238cd-112">The **Database Access Intent List** page lets you override the predefined database access intent for objects when they're run.</span></span>

<span data-ttu-id="238cd-113">En termes de base de données, cette fonction est communément appelée *échelle horizontale en lecture*. Pour en savoir plus sur l’échelle horizontale en lecture et l’accès intentionnel aux données dans [!INCLUDE[prod_short](includes/prod_short.md)], consultez [Utilisation de l’échelle horizontale en lecture pour de meilleures performances](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) dans l’aide [!INCLUDE[prod_short](includes/prod_short.md)] sur Developer and Administration.</span><span class="sxs-lookup"><span data-stu-id="238cd-113">In database terms, this feature is commonly known as *read scale-out*. For more information about read-scale out and data access intent in [!INCLUDE[prod_short](includes/prod_short.md)], see [Utilizing Read Scale-Out for Better Performance](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) in the [!INCLUDE[prod_short](includes/prod_short.md)] Developer and Administration help.</span></span>

## <a name="to-change-the-database-access-intent"></a><span data-ttu-id="238cd-114">Pour modifier l’accès intentionnel à la base de données</span><span class="sxs-lookup"><span data-stu-id="238cd-114">To change the database access intent</span></span>

1. <span data-ttu-id="238cd-115">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Liste d’accès intentionnels à la base de données**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="238cd-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Database Access Intent List**, and then choose the related link.</span></span>

    <span data-ttu-id="238cd-116">La page répertorie l’ensemble des états, pages et requêtes.</span><span class="sxs-lookup"><span data-stu-id="238cd-116">The page lists all reports, pages, and queries.</span></span> <span data-ttu-id="238cd-117">La colonne **Accès intentionnel** comprend l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="238cd-117">The **Access Intent** column includes one of the following values:</span></span>

    |<span data-ttu-id="238cd-118">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="238cd-118">**Setting**</span></span>|<span data-ttu-id="238cd-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="238cd-119">**Description**</span></span>|  
    |------------|-------------|  
    |<span data-ttu-id="238cd-120">**Par défaut**</span><span class="sxs-lookup"><span data-stu-id="238cd-120">**Default**</span></span>|<span data-ttu-id="238cd-121">Indique que l’objet utilise l’accès intentionnel à la base de données prédéfini.</span><span class="sxs-lookup"><span data-stu-id="238cd-121">Indicates that the object uses the predefined database access intent.</span></span>|
    |<span data-ttu-id="238cd-122">**Autoriser écriture**</span><span class="sxs-lookup"><span data-stu-id="238cd-122">**Allow Write**</span></span>|<span data-ttu-id="238cd-123">Définit l’objet pour utiliser la base de données principale, permettant à l’utilisateur de modifier les données.</span><span class="sxs-lookup"><span data-stu-id="238cd-123">Sets the object to use the primary database, allowing the user to modify data.</span></span>|
    |<span data-ttu-id="238cd-124">**Lecture seule**</span><span class="sxs-lookup"><span data-stu-id="238cd-124">**Read Only**</span></span>|<span data-ttu-id="238cd-125">Définit l’objet pour utiliser la réplique de la base de données ; autrement dit, l’utilisateur peut uniquement afficher les données, et non les modifier.</span><span class="sxs-lookup"><span data-stu-id="238cd-125">Sets the object to use the database replica, which means that the user can only view data, not change data.</span></span>|

2. <span data-ttu-id="238cd-126">Choisissez l’action **Modifier la liste**.</span><span class="sxs-lookup"><span data-stu-id="238cd-126">Choose the **Edit List** action.</span></span>

3. <span data-ttu-id="238cd-127">Sur la page **Modifier : liste d’accès intentionnels à la base de données**, modifiez le champ **Accès intentionnel** pour les objets.</span><span class="sxs-lookup"><span data-stu-id="238cd-127">On the **Edit - Database Access Intent List** page, change the **Access Intent** field for the objects.</span></span>

    > [!NOTE]
    > <span data-ttu-id="238cd-128">Si un objet modifiable, comme la fiche client, est défini sur **Lecture seule**, la base de données principale est toujours utilisée, quelle que soit l’accès intentionnel, permettant aux utilisateurs d’apporter des modifications comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="238cd-128">If an object that is editable, like the Customer Card, is set to **Read Only**, the primary database will still be used, regardless of the access intent, allowing users to make changes as normal.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="238cd-129">Voir la formation associée sur [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="238cd-129">See Related Training at [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="238cd-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="238cd-130">See Also</span></span>
[<span data-ttu-id="238cd-131">Fonctionnalités d’entreprise</span><span class="sxs-lookup"><span data-stu-id="238cd-131">Business Functionality</span></span>](across-business-functionality.md)  
[<span data-ttu-id="238cd-132">Fonctionnalités marché</span><span class="sxs-lookup"><span data-stu-id="238cd-132">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="238cd-133">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="238cd-133">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="238cd-134">Mise en route</span><span class="sxs-lookup"><span data-stu-id="238cd-134">Getting Started</span></span>](product-get-started.md)    

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]