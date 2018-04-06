---
title: "Procédure de création de packages configuration de société personnalisés | Microsoft Docs"
description: "À mesure que vous développez votre activité, vous êtes susceptible d'utiliser un ensemble de types de société pour la plupart de vos clients. Vous pouvez rationaliser votre processus d’implémentation en transformant ces types en packages configuration de société que vous pouvez réutiliser."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7feaa0e41cf5800ffd51d5807a90f6929492804e
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="41e58-104">Créer des packages configuration de société personnalisés</span><span class="sxs-lookup"><span data-stu-id="41e58-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="41e58-105">À mesure que vous développez votre activité, vous êtes susceptible d'utiliser un ensemble de types de société pour la plupart de vos clients.</span><span class="sxs-lookup"><span data-stu-id="41e58-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="41e58-106">Vous pouvez rationaliser votre processus d’implémentation en transformant ces types en packages configuration de société que vous pouvez réutiliser.</span><span class="sxs-lookup"><span data-stu-id="41e58-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="41e58-107">En général, créez un package configuration par domaine fonctionnel, par exemple, créez un package pour la fonctionnalité de fabrication.</span><span class="sxs-lookup"><span data-stu-id="41e58-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="41e58-108">Cela vous permet d’appliquer et de configurer de nouveaux domaines au sein d’une société en fonction de vos besoins</span><span class="sxs-lookup"><span data-stu-id="41e58-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="41e58-109">Autrement, vous pouvez créer un package qui inclut les tables qui définissent la configuration, par exemple :</span><span class="sxs-lookup"><span data-stu-id="41e58-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="41e58-110">Paramètres immobilisations</span><span class="sxs-lookup"><span data-stu-id="41e58-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="41e58-111">Paramètres comptabilité</span><span class="sxs-lookup"><span data-stu-id="41e58-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="41e58-112">Paramètres stock</span><span class="sxs-lookup"><span data-stu-id="41e58-112">Inventory Setup</span></span>  
-   <span data-ttu-id="41e58-113">Paramètres production</span><span class="sxs-lookup"><span data-stu-id="41e58-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="41e58-114">Paramètres achats</span><span class="sxs-lookup"><span data-stu-id="41e58-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="41e58-115">Paramètres marketing</span><span class="sxs-lookup"><span data-stu-id="41e58-115">Marketing Setup</span></span>  
-   <span data-ttu-id="41e58-116">Paramètres services</span><span class="sxs-lookup"><span data-stu-id="41e58-116">Service Setup</span></span>  
-   <span data-ttu-id="41e58-117">Paramètres ventes</span><span class="sxs-lookup"><span data-stu-id="41e58-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="41e58-118">Paramètres entrepôt</span><span class="sxs-lookup"><span data-stu-id="41e58-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="41e58-119">Paramètres comptabilisation</span><span class="sxs-lookup"><span data-stu-id="41e58-119">General Posting Setup</span></span>  
-   <span data-ttu-id="41e58-120">Paramètres comptabilisation TVA</span><span class="sxs-lookup"><span data-stu-id="41e58-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="41e58-121">Paramètres compta. stock</span><span class="sxs-lookup"><span data-stu-id="41e58-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="41e58-122">Pour afficher la liste complète des tables de configuration, choisissez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Paramètres**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="41e58-122">To see a complete list of setup tables, Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Setup**, and then choose the related link.</span></span>  

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="41e58-123">Pour créer un package configuration de société personnalisé</span><span class="sxs-lookup"><span data-stu-id="41e58-123">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="41e58-124">Créez une [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="41e58-124">Create a new [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="41e58-125">***Lien NON POSSIBLE pour aider à la « création d'un abonné »***.</span><span class="sxs-lookup"><span data-stu-id="41e58-125">***NOT POSSIBLE Link to help for "Creating a New Tenant"***.</span></span>   
2.  <span data-ttu-id="41e58-126">Créez une société pour le modèle solution ou secteur d'activité.</span><span class="sxs-lookup"><span data-stu-id="41e58-126">Create a new company for the industry or solution template.</span></span> <span data-ttu-id="41e58-127">Pour plus d’informations, voir [Créer une société](admin-how-to-create-a-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="41e58-127">For more information, see [Create a New Company](admin-how-to-create-a-new-company.md).</span></span>  
3.  <span data-ttu-id="41e58-128">Configurez la nouvelle société en tenant compte de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="41e58-128">Setup the new company in the way you need.</span></span> <span data-ttu-id="41e58-129">Renseignez toutes les tables de configuration nécessaires.</span><span class="sxs-lookup"><span data-stu-id="41e58-129">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="41e58-130">Ouvrez la nouvelle société.</span><span class="sxs-lookup"><span data-stu-id="41e58-130">Open the new company.</span></span>
5. <span data-ttu-id="41e58-131">Ouvrez la fenêtre **Feuille configuration**.</span><span class="sxs-lookup"><span data-stu-id="41e58-131">Open the **Configuration Worksheet** window.</span></span>  
6.  <span data-ttu-id="41e58-132">Ajoutez les tables que vous souhaitez transférer vers une autre société à la feuille.</span><span class="sxs-lookup"><span data-stu-id="41e58-132">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="41e58-133">Affectez les lignes feuille au package.</span><span class="sxs-lookup"><span data-stu-id="41e58-133">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="41e58-134">Créez un questionnaire pour les tables de configuration les plus souvent utilisées.</span><span class="sxs-lookup"><span data-stu-id="41e58-134">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="41e58-135">Créez des modèles de configuration pour faciliter la création de données de base, telles que les clients ou les articles.</span><span class="sxs-lookup"><span data-stu-id="41e58-135">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="41e58-136">Exportez votre package comme fichier .rapidstart.</span><span class="sxs-lookup"><span data-stu-id="41e58-136">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="41e58-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41e58-137">See Also</span></span>  
[<span data-ttu-id="41e58-138">Configuration d'une société avec RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="41e58-138">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="41e58-139">Administration</span><span class="sxs-lookup"><span data-stu-id="41e58-139">Administration</span></span>](admin-setup-and-administration.md)

