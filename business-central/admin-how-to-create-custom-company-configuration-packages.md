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
ms.date: 12/07/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: a51628085e640cc2e5f022272eccb89d5cec38b7
ms.contentlocale: fr-ch
ms.lasthandoff: 12/11/2018

---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="627bc-104">Créer des packages configuration de société personnalisés</span><span class="sxs-lookup"><span data-stu-id="627bc-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="627bc-105">À mesure que vous développez votre activité, vous êtes susceptible d'utiliser un ensemble de types de société pour la plupart de vos clients.</span><span class="sxs-lookup"><span data-stu-id="627bc-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="627bc-106">Vous pouvez rationaliser votre processus d’implémentation en transformant ces types en packages configuration de société que vous pouvez réutiliser.</span><span class="sxs-lookup"><span data-stu-id="627bc-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="627bc-107">En général, créez un package configuration par domaine fonctionnel, par exemple, créez un package pour la fonctionnalité de fabrication.</span><span class="sxs-lookup"><span data-stu-id="627bc-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="627bc-108">Cela vous permet d’appliquer et de configurer de nouveaux domaines au sein d’une société en fonction de vos besoins</span><span class="sxs-lookup"><span data-stu-id="627bc-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="627bc-109">Autrement, vous pouvez créer un package qui inclut les tables qui définissent la configuration, par exemple :</span><span class="sxs-lookup"><span data-stu-id="627bc-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="627bc-110">Paramètres immobilisations</span><span class="sxs-lookup"><span data-stu-id="627bc-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="627bc-111">Paramètres comptabilité</span><span class="sxs-lookup"><span data-stu-id="627bc-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="627bc-112">Paramètres stock</span><span class="sxs-lookup"><span data-stu-id="627bc-112">Inventory Setup</span></span>  
-   <span data-ttu-id="627bc-113">Paramètres production</span><span class="sxs-lookup"><span data-stu-id="627bc-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="627bc-114">Paramètres achats</span><span class="sxs-lookup"><span data-stu-id="627bc-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="627bc-115">Paramètres marketing</span><span class="sxs-lookup"><span data-stu-id="627bc-115">Marketing Setup</span></span>  
-   <span data-ttu-id="627bc-116">Paramètres services</span><span class="sxs-lookup"><span data-stu-id="627bc-116">Service Setup</span></span>  
-   <span data-ttu-id="627bc-117">Paramètres ventes</span><span class="sxs-lookup"><span data-stu-id="627bc-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="627bc-118">Paramètres entrepôt</span><span class="sxs-lookup"><span data-stu-id="627bc-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="627bc-119">Paramètres comptabilisation</span><span class="sxs-lookup"><span data-stu-id="627bc-119">General Posting Setup</span></span>  
-   <span data-ttu-id="627bc-120">Paramètres comptabilisation TVA</span><span class="sxs-lookup"><span data-stu-id="627bc-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="627bc-121">Paramètres compta. stock</span><span class="sxs-lookup"><span data-stu-id="627bc-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="627bc-122">Pour visualiser la liste complète des tables de configuration, choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Configuration manuelle**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="627bc-122">To see a complete list of setup tables, Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Manual Setup**, and then choose the related link.</span></span>  

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="627bc-123">Pour créer un package configuration de société personnalisé</span><span class="sxs-lookup"><span data-stu-id="627bc-123">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="627bc-124">Créez une nouvelle société.</span><span class="sxs-lookup"><span data-stu-id="627bc-124">Create a new company.</span></span> <span data-ttu-id="627bc-125">Pour plus d'informations, voir [Création de sociétés dans Business Central](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="627bc-125">For more information, see [Creating New Companies in Business Central](about-new-company.md).</span></span>  
3.  <span data-ttu-id="627bc-126">Configurez la nouvelle société en tenant compte de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="627bc-126">Set up the new company in the way you need.</span></span> <span data-ttu-id="627bc-127">Renseignez toutes les tables de configuration nécessaires.</span><span class="sxs-lookup"><span data-stu-id="627bc-127">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="627bc-128">Ouvrez la nouvelle société.</span><span class="sxs-lookup"><span data-stu-id="627bc-128">Open the new company.</span></span>
5. <span data-ttu-id="627bc-129">Ouvrir la page **Feuille configuration**.</span><span class="sxs-lookup"><span data-stu-id="627bc-129">Open the **Configuration Worksheet** page.</span></span>  
6.  <span data-ttu-id="627bc-130">Ajoutez les tables que vous souhaitez transférer vers une autre société à la feuille.</span><span class="sxs-lookup"><span data-stu-id="627bc-130">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="627bc-131">Affectez les lignes feuille au package.</span><span class="sxs-lookup"><span data-stu-id="627bc-131">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="627bc-132">Créez un questionnaire pour les tables de configuration les plus souvent utilisées.</span><span class="sxs-lookup"><span data-stu-id="627bc-132">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="627bc-133">Créez des modèles de configuration pour faciliter la création de données de base, telles que les clients ou les articles.</span><span class="sxs-lookup"><span data-stu-id="627bc-133">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="627bc-134">Exportez votre package comme fichier .rapidstart.</span><span class="sxs-lookup"><span data-stu-id="627bc-134">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="627bc-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="627bc-135">See Also</span></span>  
[<span data-ttu-id="627bc-136">Configuration d'une société avec RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="627bc-136">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="627bc-137">Administration</span><span class="sxs-lookup"><span data-stu-id="627bc-137">Administration</span></span>](admin-setup-and-administration.md)

