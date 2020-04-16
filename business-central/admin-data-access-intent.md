---
title: Gérer l'accès intentionnel à la base de données dans Business Central | Microsoft Docs
description: Modifiez l'accès intentionnel à la base de données pour les états, les pages API et les requêtes.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 33b5a3ff604b0ddf7525b89d7a8a82bcfdd7f653
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196411"
---
# <a name="managing-database-access-intent"></a><span data-ttu-id="cdeb3-103">Gestion de l'accès intentionnel à la base de données</span><span class="sxs-lookup"><span data-stu-id="cdeb3-103">Managing Database Access Intent</span></span> 

<span data-ttu-id="cdeb3-104">En tant que superutilisateur ou administrateur, vous pouvez modifier l'accès intentionnel à la base de données pour les états, les pages du type API et les requêtes pour améliorer les performances du service.</span><span class="sxs-lookup"><span data-stu-id="cdeb3-104">As a super user or administrator, you can change the database access intent on reports, pages of the type API, and queries to improve performance of the service.</span></span>

## <a name="overview"></a><span data-ttu-id="cdeb3-105">Aperçu</span><span class="sxs-lookup"><span data-stu-id="cdeb3-105">Overview</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="cdeb3-106">peut être configuré pour utiliser des répliques en lecture seule de la base de données principale (en lecture-écriture).</span><span class="sxs-lookup"><span data-stu-id="cdeb3-106">can be set up to use read-only replicas of the primary (read-write) database.</span></span> <span data-ttu-id="cdeb3-107">L'utilisation de répliques de la base de données réduit la charge sur la base de données principale.</span><span class="sxs-lookup"><span data-stu-id="cdeb3-107">Using the database replica reduces the load on the primary database.</span></span> <span data-ttu-id="cdeb3-108">Dans certains cas, cela améliore également les performances lors de l'affichage des données dans le client.</span><span class="sxs-lookup"><span data-stu-id="cdeb3-108">In some cases, it will also improve the performance when viewing data in the client.</span></span> <span data-ttu-id="cdeb3-109">Les répliques sont avantageuses pour les objets tels que les états, les requêtes et les pages API, qui permettent uniquement d'afficher les données, et non de les modifier.</span><span class="sxs-lookup"><span data-stu-id="cdeb3-109">Replicas are beneficial for objects, like reports, queries, and API pages, that are used for viewing data only, not modifying data.</span></span>

<span data-ttu-id="cdeb3-110">Lors de l'exécution des objets, l'accès intentionnel à la base de données détermine s'il faut utiliser une réplique en lecture seule, en cas de disponibilité, ou la base de données principale.</span><span class="sxs-lookup"><span data-stu-id="cdeb3-110">When objects run, the database access intent determines whether to use a read-only replica, if one is available, or the primary database.</span></span> <span data-ttu-id="cdeb3-111">Les états, les pages API et les requêtes sont développés avec un accès intentionnel à la base de données prédéfini (voir [Propriété DatabaseAccessIntent](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).</span><span class="sxs-lookup"><span data-stu-id="cdeb3-111">Reports, API pages, and queries are developed with a predefined database access intent (see [DatabaseAccessIntent property](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).</span></span>

<span data-ttu-id="cdeb3-112">La page **Liste d'accès intentionnels à la base de données** vous permet de remplacer l'accès intentionnel à la base de données prédéfini pour les objets lors de leur exécution.</span><span class="sxs-lookup"><span data-stu-id="cdeb3-112">The **Database Access Intent List** page lets you override the predefined database access intent for objects when they're run.</span></span>

<span data-ttu-id="cdeb3-113">En termes de base de données, cette fonction est communément appelée *échelle horizontale en lecture*. Pour en savoir plus sur l'échelle horizontale en lecture et l'accès intentionnel aux données dans [!INCLUDE[d365fin](includes/d365fin_md.md)], consultez [Utilisation de l'échelle horizontale en lecture pour de meilleures performances](https://review.docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview?branch=tfs337368-readscaleout) dans l'aide [!INCLUDE[d365fin](includes/d365fin_md.md)] sur Developer and IT Pro.</span><span class="sxs-lookup"><span data-stu-id="cdeb3-113">In database terms, this feature is commonly known as *read scale-out*. For more information about read-scale out and data access intent in [!INCLUDE[d365fin](includes/d365fin_md.md)], see [Utilizing Read Scale-Out for Better Performance](https://review.docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview?branch=tfs337368-readscaleout) in the [!INCLUDE[d365fin](includes/d365fin_md.md)] Developer and IT Pro help.</span></span>

## <a name="to-change-the-database-access-intent"></a><span data-ttu-id="cdeb3-114">Pour modifier l'accès intentionnel à la base de données</span><span class="sxs-lookup"><span data-stu-id="cdeb3-114">To change the database access intent</span></span>

1. <span data-ttu-id="cdeb3-115">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Liste d'accès intentionnels à la base de données**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="cdeb3-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Database Access Intent List**, and then choose the related link.</span></span>

    <span data-ttu-id="cdeb3-116">La page répertorie l'ensemble des états, pages et requêtes.</span><span class="sxs-lookup"><span data-stu-id="cdeb3-116">The page lists all reports, pages, and queries.</span></span> <span data-ttu-id="cdeb3-117">La colonne **Accès intentionnel** comprend l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="cdeb3-117">The **Access Intent** column includes one of the following values:</span></span>

    |<span data-ttu-id="cdeb3-118">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="cdeb3-118">**Setting**</span></span>|<span data-ttu-id="cdeb3-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="cdeb3-119">**Description**</span></span>|  
    |------------|-------------|  
    |<span data-ttu-id="cdeb3-120">**Par défaut**</span><span class="sxs-lookup"><span data-stu-id="cdeb3-120">**Default**</span></span>|<span data-ttu-id="cdeb3-121">Indique que l'objet utilise l'accès intentionnel à la base de données prédéfini.</span><span class="sxs-lookup"><span data-stu-id="cdeb3-121">Indicates that the object uses the predefined database access intent.</span></span>|
    |<span data-ttu-id="cdeb3-122">**Autoriser écriture**</span><span class="sxs-lookup"><span data-stu-id="cdeb3-122">**Allow Write**</span></span>|<span data-ttu-id="cdeb3-123">Définit l'objet pour utiliser la base de données principale, permettant à l'utilisateur de modifier les données.</span><span class="sxs-lookup"><span data-stu-id="cdeb3-123">Sets the object to use the primary database, allowing the user to modify data.</span></span>|
    |<span data-ttu-id="cdeb3-124">**Lecture seule**</span><span class="sxs-lookup"><span data-stu-id="cdeb3-124">**Read Only**</span></span>|<span data-ttu-id="cdeb3-125">Définit l'objet pour utiliser la réplique de la base de données ; autrement dit, l'utilisateur peut uniquement afficher les données, et non les modifier.</span><span class="sxs-lookup"><span data-stu-id="cdeb3-125">Sets the object to use the database replica, which means that the user can only view data, not change data.</span></span>|

2. <span data-ttu-id="cdeb3-126">Choisissez l'action **Modifier la liste**.</span><span class="sxs-lookup"><span data-stu-id="cdeb3-126">Choose the **Edit List** action.</span></span>

3. <span data-ttu-id="cdeb3-127">Sur la page **Modifier : liste d'accès intentionnels à la base de données**, modifiez le champ **Accès intentionnel** pour les objets.</span><span class="sxs-lookup"><span data-stu-id="cdeb3-127">On the **Edit - Database Access Intent List** page, change the **Access Intent** field for the objects.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cdeb3-128">Si un objet modifiable, comme la fiche client, est défini sur **Lecture seule**, la base de données principale est toujours utilisée, quelle que soit l'accès intentionnel, permettant aux utilisateurs d'apporter des modifications comme d'habitude.</span><span class="sxs-lookup"><span data-stu-id="cdeb3-128">If an object that is editable, like the Customer Card, is set to **Read Only**, the primary database will still be used, regardless of the access intent, allowing users to make changes as normal.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="cdeb3-129">Voir la formation associée sur [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="cdeb3-129">See Related Training at [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="cdeb3-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cdeb3-130">See Also</span></span>
[<span data-ttu-id="cdeb3-131">Fonctionnalités d'entreprise</span><span class="sxs-lookup"><span data-stu-id="cdeb3-131">Business Functionality</span></span>](across-business-functionality.md)  
[<span data-ttu-id="cdeb3-132">Fonctionnalités marché</span><span class="sxs-lookup"><span data-stu-id="cdeb3-132">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="cdeb3-133">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cdeb3-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="cdeb3-134">Mise en route</span><span class="sxs-lookup"><span data-stu-id="cdeb3-134">Getting Started</span></span>](product-get-started.md)    

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
