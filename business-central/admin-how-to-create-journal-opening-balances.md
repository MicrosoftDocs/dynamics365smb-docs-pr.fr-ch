---
title: "Procédure de création des soldes ouverts feuille | Microsoft Docs"
description: "Business Central inclut plusieurs traitements par lots qui sont livrés pour aider au transfert des soldes de compte hérité vers une société nouvellement configurée. Vous pouvez facilement transférer ces données avec des validations de feuille."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 612eb9cfa5c6cd45bf154f4813efa3b349f44841
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="create-journal-opening-balances"></a><span data-ttu-id="8dbaa-104">Créer des soldes ouverts feuille</span><span class="sxs-lookup"><span data-stu-id="8dbaa-104">Create Journal Opening Balances</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="8dbaa-105">inclut plusieurs traitements par lots qui sont livrés pour aider au transfert des soldes de compte hérité vers une société nouvellement configurée.</span><span class="sxs-lookup"><span data-stu-id="8dbaa-105"> includes several batch jobs that are provided to help in the transfer of legacy account balances to a newly configured company.</span></span> <span data-ttu-id="8dbaa-106">Vous pouvez facilement transférer ces données avec le journal comptes clients, le journal comptes fournisseurs, la feuille article ou la feuille comptabilisation.</span><span class="sxs-lookup"><span data-stu-id="8dbaa-106">You can easily transfer this data with the customer journal, the vendor journal, the item journal, or the G/L journal.</span></span>

<span data-ttu-id="8dbaa-107">La première étape consiste à créer un package configuration incluant les tables de paramétrage pour ces feuilles.</span><span class="sxs-lookup"><span data-stu-id="8dbaa-107">The first step is to create a configuration package that includes the setup tables for those journals.</span></span> <span data-ttu-id="8dbaa-108">La procédure suivante est basée sur l’hypothèse que cette étape est terminée.</span><span class="sxs-lookup"><span data-stu-id="8dbaa-108">The following procedure assumes that this step is completed.</span></span> <span data-ttu-id="8dbaa-109">Pour plus d'informations, voir [Configurer une société](admin-set-up-company-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="8dbaa-109">For more information, see [Set Up Company Configuration](admin-set-up-company-configuration.md).</span></span> <span data-ttu-id="8dbaa-110">Cette procédure explique les étapes suivantes, comme le lettrage du package qui est fourni par un partenaire.</span><span class="sxs-lookup"><span data-stu-id="8dbaa-110">This procedure describes the subsequent steps, which include applying the package that is provided by a partner.</span></span>  

<span data-ttu-id="8dbaa-111">Avant de commencer, vérifiez que vous vous trouvez sur la page du tableau de bord Responsable de l'implémentation de RapidStart Services, car elle fournit le contexte correct pour votre travail de configuration.</span><span class="sxs-lookup"><span data-stu-id="8dbaa-111">Before you start, make sure that you are on the RapidStart Services Implementer Role Center page as it provides the correct context for your configuration work.</span></span> <span data-ttu-id="8dbaa-112">Pour plus d'informations, voir [Modification des paramètres de base](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="8dbaa-112">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a><span data-ttu-id="8dbaa-113">Pour lettrer des écritures dans une feuille à une société</span><span class="sxs-lookup"><span data-stu-id="8dbaa-113">To apply the entries in a journal to a new company</span></span>  
1. <span data-ttu-id="8dbaa-114">Configurez une nouvelle société et appliquez-lui un package configuration.</span><span class="sxs-lookup"><span data-stu-id="8dbaa-114">Configure a new company and apply a configuration package to it.</span></span> <span data-ttu-id="8dbaa-115">Pour plus d'informations, voir [Configurer une société avec l’assistant RapidStart](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="8dbaa-115">For more information, see [Configure a Company with the RapidStart Wizard](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span></span>  

    <span data-ttu-id="8dbaa-116">La nouvelle société ne contient pas d’informations sur les soldes ouverts feuille.</span><span class="sxs-lookup"><span data-stu-id="8dbaa-116">The new company does not contain information about journal opening balances.</span></span>  

2. <span data-ttu-id="8dbaa-117">Ouvrez la feuille configuration et importez les données existantes à propos des clients, des articles, des fournisseurs et de la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="8dbaa-117">Open the configuration worksheet and import existing data about customers, items, vendors, and the general ledger.</span></span> <span data-ttu-id="8dbaa-118">Pour plus d'informations, voir [Migrer des données client](admin-migrate-customer-data.md).</span><span class="sxs-lookup"><span data-stu-id="8dbaa-118">For more information, see [Migrate Customer Data](admin-migrate-customer-data.md).</span></span>  
3. <span data-ttu-id="8dbaa-119">Choisissez, par exemple, l'action **Créer lignes feuille compta**.</span><span class="sxs-lookup"><span data-stu-id="8dbaa-119">Choose, for example, the **Create G/L Journal Lines** action.</span></span>  
4. <span data-ttu-id="8dbaa-120">Renseignez le raccourci **Options** de la manière appropriée, puis définissez les filtres selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="8dbaa-120">Fill in the **Options** FastTab as appropriate, and set filters as needed.</span></span> <span data-ttu-id="8dbaa-121">Par exemple, dans le champ **Modèle feuille**, entrez un nom.</span><span class="sxs-lookup"><span data-stu-id="8dbaa-121">For example, in the **Journal Template** field, enter a name.</span></span>  
5. <span data-ttu-id="8dbaa-122">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="8dbaa-122">Choose the **OK** button.</span></span> <span data-ttu-id="8dbaa-123">Les enregistrements se trouvent maintenant dans la feuille, mais les montants sont vides.</span><span class="sxs-lookup"><span data-stu-id="8dbaa-123">The records are now in the journal, but the amounts are empty.</span></span>  
6. <span data-ttu-id="8dbaa-124">Exportez la table feuille vers Excel et entrez manuellement les informations sur le compte contrepartie et validation à partir des données héritées.</span><span class="sxs-lookup"><span data-stu-id="8dbaa-124">Export the journal table to Excel and manually enter the posting and balancing account information from the legacy data.</span></span>
7. <span data-ttu-id="8dbaa-125">Importez et appliquez les informations de table dans la nouvelle société.</span><span class="sxs-lookup"><span data-stu-id="8dbaa-125">Import and apply the table information into the new company.</span></span> <span data-ttu-id="8dbaa-126">Les lignes feuille sont prêtes pour la validation.</span><span class="sxs-lookup"><span data-stu-id="8dbaa-126">The journal lines are ready for posting.</span></span>  
8. <span data-ttu-id="8dbaa-127">Dans la feuille configuration, sélectionnez la table ligne feuille, puis sélectionnez l'action **Données de base de données**.</span><span class="sxs-lookup"><span data-stu-id="8dbaa-127">In the configuration worksheet, select the journal line table, and then choose the **Database Data** action.</span></span>  
9. <span data-ttu-id="8dbaa-128">Examinez les informations, puis sélectionnez l'action **Valider**.</span><span class="sxs-lookup"><span data-stu-id="8dbaa-128">Review the information, and then choose the **Post** action.</span></span>  
10. <span data-ttu-id="8dbaa-129">Répétez les étapes pour importer et valider les autres soldes ouverts.</span><span class="sxs-lookup"><span data-stu-id="8dbaa-129">Repeat the steps to import and post any other opening balances.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8dbaa-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8dbaa-130">See Also</span></span>  
[<span data-ttu-id="8dbaa-131">Appliquer des configurations aux nouvelles sociétés</span><span class="sxs-lookup"><span data-stu-id="8dbaa-131">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="8dbaa-132">Configuration d'une société avec RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="8dbaa-132">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="8dbaa-133">Administration</span><span class="sxs-lookup"><span data-stu-id="8dbaa-133">Administration</span></span>](admin-setup-and-administration.md)

