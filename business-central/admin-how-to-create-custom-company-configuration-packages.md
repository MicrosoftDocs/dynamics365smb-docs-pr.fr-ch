---
title: Procédure de création de packages configuration de société personnalisés | Microsoft Docs
description: À mesure que vous développez votre activité, vous êtes susceptible d’utiliser un ensemble de types de société pour la plupart de vos clients. Vous pouvez rationaliser votre processus d’implémentation en transformant ces types en packages configuration de société que vous pouvez réutiliser.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9e1cf9d530c8af95373cfbdef8a3f6822cbba938
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915799"
---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="189da-104">Créer des packages configuration de société personnalisés</span><span class="sxs-lookup"><span data-stu-id="189da-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="189da-105">À mesure que vous développez votre activité, vous êtes susceptible d’utiliser un ensemble de types de société pour la plupart de vos clients.</span><span class="sxs-lookup"><span data-stu-id="189da-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="189da-106">Vous pouvez rationaliser votre processus d’implémentation en transformant ces types en packages configuration de société que vous pouvez réutiliser.</span><span class="sxs-lookup"><span data-stu-id="189da-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="189da-107">En général, créez un package configuration par domaine fonctionnel, par exemple, créez un package pour la fonctionnalité de fabrication.</span><span class="sxs-lookup"><span data-stu-id="189da-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="189da-108">Cela vous permet d’appliquer et de configurer de nouveaux domaines au sein d’une société en fonction de vos besoins</span><span class="sxs-lookup"><span data-stu-id="189da-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="189da-109">Autrement, vous pouvez créer un package qui inclut les tables qui définissent la configuration, par exemple :</span><span class="sxs-lookup"><span data-stu-id="189da-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="189da-110">Paramètres immobilisations</span><span class="sxs-lookup"><span data-stu-id="189da-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="189da-111">Paramètres comptabilité</span><span class="sxs-lookup"><span data-stu-id="189da-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="189da-112">Paramètres stock</span><span class="sxs-lookup"><span data-stu-id="189da-112">Inventory Setup</span></span>  
-   <span data-ttu-id="189da-113">Paramètres production</span><span class="sxs-lookup"><span data-stu-id="189da-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="189da-114">Paramètres achats</span><span class="sxs-lookup"><span data-stu-id="189da-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="189da-115">Paramètres marketing</span><span class="sxs-lookup"><span data-stu-id="189da-115">Marketing Setup</span></span>  
-   <span data-ttu-id="189da-116">Paramètres services</span><span class="sxs-lookup"><span data-stu-id="189da-116">Service Setup</span></span>  
-   <span data-ttu-id="189da-117">Paramètres ventes</span><span class="sxs-lookup"><span data-stu-id="189da-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="189da-118">Paramètres entrepôt</span><span class="sxs-lookup"><span data-stu-id="189da-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="189da-119">Paramètres comptabilisation</span><span class="sxs-lookup"><span data-stu-id="189da-119">General Posting Setup</span></span>  
-   <span data-ttu-id="189da-120">Paramètres comptabilisation TVA</span><span class="sxs-lookup"><span data-stu-id="189da-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="189da-121">Paramètres compta. stock</span><span class="sxs-lookup"><span data-stu-id="189da-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="189da-122">Pour visualiser la liste complète des tables de configuration, choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), entrez **Configuration manuelle** , puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="189da-122">To see a complete list of setup tables, Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Manual Setup** , and then choose the related link.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="189da-123">Soyez prudent si vous choisissez des tables ou des champs qui portent le même nom temporel mais sont différenciés par des caractères spéciaux, tels que %, &, <, >, (, et ).</span><span class="sxs-lookup"><span data-stu-id="189da-123">Use caution if you choose tables or fields that have the same temporal name but are differentiated by special characters, such as %, &, <, >, (, and ).</span></span> <span data-ttu-id="189da-124">Par exemple, la table « XYZ » peut contenir les champs « Champ 1 » et « Champ 1 % ».</span><span class="sxs-lookup"><span data-stu-id="189da-124">For example, table "XYZ" might contain the "Field 1" and "Field 1%" fields.</span></span>
>
> <span data-ttu-id="189da-125">Le processeur XML n’accepte que certains caractères spéciaux et supprime ceux qu’il n’accepte pas.</span><span class="sxs-lookup"><span data-stu-id="189da-125">The XML processor accepts only some special characters, and will remove those it does not.</span></span> <span data-ttu-id="189da-126">Si la suppression d’un caractère spécial, tel que le signe % dans « Champ 1 % », génère deux ou plusieurs tables ou champs avec le même nom, une erreur se produit lorsque vous exportez ou importez un package de configuration.</span><span class="sxs-lookup"><span data-stu-id="189da-126">If removing a special character, such as the % sign in "Field 1%," results in two or more tables or fields with the same name an error will occur when you export or import a configuration package.</span></span>

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="189da-127">Pour créer un package configuration de société personnalisé</span><span class="sxs-lookup"><span data-stu-id="189da-127">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="189da-128">Créez une nouvelle société.</span><span class="sxs-lookup"><span data-stu-id="189da-128">Create a new company.</span></span> <span data-ttu-id="189da-129">Pour plus d’informations, voir [Création de sociétés dans Business Central](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="189da-129">For more information, see [Creating New Companies in Business Central](about-new-company.md).</span></span>  
3.  <span data-ttu-id="189da-130">Configurez la nouvelle société en tenant compte de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="189da-130">Set up the new company in the way you need.</span></span> <span data-ttu-id="189da-131">Renseignez toutes les tables de configuration nécessaires.</span><span class="sxs-lookup"><span data-stu-id="189da-131">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="189da-132">Ouvrez la nouvelle société.</span><span class="sxs-lookup"><span data-stu-id="189da-132">Open the new company.</span></span>
5. <span data-ttu-id="189da-133">Ouvrir la page **Feuille configuration** .</span><span class="sxs-lookup"><span data-stu-id="189da-133">Open the **Configuration Worksheet** page.</span></span>  
6.  <span data-ttu-id="189da-134">Ajoutez les tables que vous souhaitez transférer vers une autre société à la feuille.</span><span class="sxs-lookup"><span data-stu-id="189da-134">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="189da-135">Affectez les lignes feuille au package.</span><span class="sxs-lookup"><span data-stu-id="189da-135">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="189da-136">Créez un questionnaire pour les tables de configuration les plus souvent utilisées.</span><span class="sxs-lookup"><span data-stu-id="189da-136">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="189da-137">Créez des modèles de configuration pour faciliter la création de données de base, telles que les clients ou les articles.</span><span class="sxs-lookup"><span data-stu-id="189da-137">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="189da-138">Exportez votre package comme fichier .rapidstart.</span><span class="sxs-lookup"><span data-stu-id="189da-138">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="189da-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="189da-139">See Also</span></span>  
[<span data-ttu-id="189da-140">Configuration d’une société avec RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="189da-140">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="189da-141">Administration</span><span class="sxs-lookup"><span data-stu-id="189da-141">Administration</span></span>](admin-setup-and-administration.md)
