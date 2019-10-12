---
title: Procédure de création de packages configuration de société personnalisés | Microsoft Docs
description: À mesure que vous développez votre activité, vous êtes susceptible d'utiliser un ensemble de types de société pour la plupart de vos clients. Vous pouvez rationaliser votre processus d’implémentation en transformant ces types en packages configuration de société que vous pouvez réutiliser.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6fd35133d16056b947db6680cc9a76cfccaa6a3c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308107"
---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="cd2e6-104">Créer des packages configuration de société personnalisés</span><span class="sxs-lookup"><span data-stu-id="cd2e6-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="cd2e6-105">À mesure que vous développez votre activité, vous êtes susceptible d'utiliser un ensemble de types de société pour la plupart de vos clients.</span><span class="sxs-lookup"><span data-stu-id="cd2e6-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="cd2e6-106">Vous pouvez rationaliser votre processus d’implémentation en transformant ces types en packages configuration de société que vous pouvez réutiliser.</span><span class="sxs-lookup"><span data-stu-id="cd2e6-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="cd2e6-107">En général, créez un package configuration par domaine fonctionnel, par exemple, créez un package pour la fonctionnalité de fabrication.</span><span class="sxs-lookup"><span data-stu-id="cd2e6-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="cd2e6-108">Cela vous permet d’appliquer et de configurer de nouveaux domaines au sein d’une société en fonction de vos besoins</span><span class="sxs-lookup"><span data-stu-id="cd2e6-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="cd2e6-109">Autrement, vous pouvez créer un package qui inclut les tables qui définissent la configuration, par exemple :</span><span class="sxs-lookup"><span data-stu-id="cd2e6-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="cd2e6-110">Paramètres immobilisations</span><span class="sxs-lookup"><span data-stu-id="cd2e6-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="cd2e6-111">Paramètres comptabilité</span><span class="sxs-lookup"><span data-stu-id="cd2e6-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="cd2e6-112">Paramètres stock</span><span class="sxs-lookup"><span data-stu-id="cd2e6-112">Inventory Setup</span></span>  
-   <span data-ttu-id="cd2e6-113">Paramètres production</span><span class="sxs-lookup"><span data-stu-id="cd2e6-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="cd2e6-114">Paramètres achats</span><span class="sxs-lookup"><span data-stu-id="cd2e6-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="cd2e6-115">Paramètres marketing</span><span class="sxs-lookup"><span data-stu-id="cd2e6-115">Marketing Setup</span></span>  
-   <span data-ttu-id="cd2e6-116">Paramètres services</span><span class="sxs-lookup"><span data-stu-id="cd2e6-116">Service Setup</span></span>  
-   <span data-ttu-id="cd2e6-117">Paramètres ventes</span><span class="sxs-lookup"><span data-stu-id="cd2e6-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="cd2e6-118">Paramètres entrepôt</span><span class="sxs-lookup"><span data-stu-id="cd2e6-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="cd2e6-119">Paramètres comptabilisation</span><span class="sxs-lookup"><span data-stu-id="cd2e6-119">General Posting Setup</span></span>  
-   <span data-ttu-id="cd2e6-120">Paramètres comptabilisation TVA</span><span class="sxs-lookup"><span data-stu-id="cd2e6-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="cd2e6-121">Paramètres compta. stock</span><span class="sxs-lookup"><span data-stu-id="cd2e6-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="cd2e6-122">Pour visualiser la liste complète des tables de configuration, choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Configuration manuelle**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="cd2e6-122">To see a complete list of setup tables, Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Manual Setup**, and then choose the related link.</span></span>  

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="cd2e6-123">Pour créer un package configuration de société personnalisé</span><span class="sxs-lookup"><span data-stu-id="cd2e6-123">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="cd2e6-124">Créez une nouvelle société.</span><span class="sxs-lookup"><span data-stu-id="cd2e6-124">Create a new company.</span></span> <span data-ttu-id="cd2e6-125">Pour plus d'informations, voir [Création de sociétés dans Business Central](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="cd2e6-125">For more information, see [Creating New Companies in Business Central](about-new-company.md).</span></span>  
3.  <span data-ttu-id="cd2e6-126">Configurez la nouvelle société en tenant compte de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="cd2e6-126">Set up the new company in the way you need.</span></span> <span data-ttu-id="cd2e6-127">Renseignez toutes les tables de configuration nécessaires.</span><span class="sxs-lookup"><span data-stu-id="cd2e6-127">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="cd2e6-128">Ouvrez la nouvelle société.</span><span class="sxs-lookup"><span data-stu-id="cd2e6-128">Open the new company.</span></span>
5. <span data-ttu-id="cd2e6-129">Ouvrir la page **Feuille configuration**.</span><span class="sxs-lookup"><span data-stu-id="cd2e6-129">Open the **Configuration Worksheet** page.</span></span>  
6.  <span data-ttu-id="cd2e6-130">Ajoutez les tables que vous souhaitez transférer vers une autre société à la feuille.</span><span class="sxs-lookup"><span data-stu-id="cd2e6-130">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="cd2e6-131">Affectez les lignes feuille au package.</span><span class="sxs-lookup"><span data-stu-id="cd2e6-131">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="cd2e6-132">Créez un questionnaire pour les tables de configuration les plus souvent utilisées.</span><span class="sxs-lookup"><span data-stu-id="cd2e6-132">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="cd2e6-133">Créez des modèles de configuration pour faciliter la création de données de base, telles que les clients ou les articles.</span><span class="sxs-lookup"><span data-stu-id="cd2e6-133">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="cd2e6-134">Exportez votre package comme fichier .rapidstart.</span><span class="sxs-lookup"><span data-stu-id="cd2e6-134">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cd2e6-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd2e6-135">See Also</span></span>  
[<span data-ttu-id="cd2e6-136">Configuration d'une société avec RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="cd2e6-136">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="cd2e6-137">Administration</span><span class="sxs-lookup"><span data-stu-id="cd2e6-137">Administration</span></span>](admin-setup-and-administration.md)
