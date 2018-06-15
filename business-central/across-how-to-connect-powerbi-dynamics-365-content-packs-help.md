---
title: "Procédure de connexion de Power BI à Business Central | Microsoft Docs"
description: "Il est facile d'obtenir des informations exploitables, de la veille économique et des KPI de vos données Business Central grâce à Power BI et aux packs de contenu Business Central."
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/03/2018
ms.author: solsen
redirect_url: admin-powerbi
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 0196bff5dedb878884fd3d6e0208022faa968dfd
ms.contentlocale: fr-ch
ms.lasthandoff: 05/17/2018

---
# <a name="connecting-power-bi-to-dynamics-365-business-central-content-packs"></a><span data-ttu-id="3a492-103">Connexion de Power BI aux packs de contenu Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="3a492-103">Connecting Power BI to Dynamics 365 Business Central Content Packs</span></span>
<span data-ttu-id="3a492-104">Il est facile d'obtenir des informations exploitables de vos données [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Microsoft grâce à Power BI et aux packs de contenu [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3a492-104">Getting insights into your Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data is easy with Power BI and the Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] content packs.</span></span> <span data-ttu-id="3a492-105">Power BI extrait vos données, puis génère un tableau de bord prêt à l'emploi et des états basés sur ces données.</span><span class="sxs-lookup"><span data-stu-id="3a492-105">Power BI retrieves your data then builds an out-of-the-box dashboard and reports based on that data.</span></span>

<span data-ttu-id="3a492-106">Remarque : vous devez disposer d'un compte valide avec Dynamics 365 et avec Power BI.</span><span class="sxs-lookup"><span data-stu-id="3a492-106">You must have a valid account with Dynamics 365 and with Power BI.</span></span> <span data-ttu-id="3a492-107">En outre, vous devez télécharger [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) si vous souhaitez créer vos propres états Power BI.</span><span class="sxs-lookup"><span data-stu-id="3a492-107">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) if you wish to create your own Power BI reports.</span></span> <span data-ttu-id="3a492-108">Les packs de contenu Power BI nécessitent des autorisations vers les tables d'où sont extraites les données.</span><span class="sxs-lookup"><span data-stu-id="3a492-108">Power BI content packs require permissions to the tables where data is retrieved from.</span></span> <span data-ttu-id="3a492-109">Vous trouverez plus d'informations sur les besoins ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="3a492-109">More details on the requirements are described below.</span></span>  

## <a name="how-to-connect"></a><span data-ttu-id="3a492-110">Pour vous connecter</span><span class="sxs-lookup"><span data-stu-id="3a492-110">How to Connect</span></span>
1. <span data-ttu-id="3a492-111">Sélectionnez **Extraire les données** en bas du volet de navigation gauche.</span><span class="sxs-lookup"><span data-stu-id="3a492-111">Select **Get Data** at the bottom of the left navigation pane.</span></span>  
<span data-ttu-id="3a492-112">![Naviguer pour obtenir des données](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span><span class="sxs-lookup"><span data-stu-id="3a492-112">![Navigating to Get Data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span></span>

<span data-ttu-id="3a492-113">Vous pouvez également démarrer à partir de Dynamics 365 Business Edition.</span><span class="sxs-lookup"><span data-stu-id="3a492-113">You may also get starting from within Dynamics 365 Business Edition.</span></span> <span data-ttu-id="3a492-114">Dans le Tableau de bord, accédez à **Sélection des états** dans le composant du Tableau de bord Power BI.</span><span class="sxs-lookup"><span data-stu-id="3a492-114">From the role center, navigate to **Report Selection** in the Power BI Role Center part.</span></span> <span data-ttu-id="3a492-115">Sélectionnez **Service** ou **Mon organisation** dans le ruban.</span><span class="sxs-lookup"><span data-stu-id="3a492-115">Select either **Service** or **My Organization** from the ribbon.</span></span> <span data-ttu-id="3a492-116">Lorsque l'une de ces actions est sélectionnée, vous arrivez dans la galerie Organisation de Power BI ou dans la bibliothèque des services de Power BI, qui sera également filtrée pour afficher uniquement les packs de contenu associés à [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="3a492-116">When either of these actions are selected, you will be taken to either the Organization gallery in Power BI or to the services library in Power BI, which will also be filtered to only display content packs related to [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span>

2. <span data-ttu-id="3a492-117">Dans la zone **Services**, sélectionnez **Extraire**.</span><span class="sxs-lookup"><span data-stu-id="3a492-117">In the **Services** box, select **Get**.</span></span> <span data-ttu-id="3a492-118">Une fenêtre s'ouvre alors, elle contient **AppSource** et **Applications pour applications Power BI**.</span><span class="sxs-lookup"><span data-stu-id="3a492-118">This will open a window with the **AppSource** and **Apps for Power BI apps**.</span></span>  
<span data-ttu-id="3a492-119">![Choisir des packs de contenu à partir des services en ligne](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span><span class="sxs-lookup"><span data-stu-id="3a492-119">![Choose content packs from online services](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span></span>
3. <span data-ttu-id="3a492-120">Sélectionnez **Applications** dans l'onglet **Applications pour applications Power BI** et choisissez le pack de contenu **Microsoft Dynamics 365 Business Central** à utiliser, puis cliquez sur **Obtenir maintenant**.</span><span class="sxs-lookup"><span data-stu-id="3a492-120">Select **Apps** from the **Apps for Power BI apps** tab, choose the **Microsoft Dynamics 365 Business Central** content pack that you want to use, and then select **Get it now**.</span></span>  
<span data-ttu-id="3a492-121">![Sélectionner Dynamics 365 Business Central et sélectionner Obtenir maintenant](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span><span class="sxs-lookup"><span data-stu-id="3a492-121">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span></span>
4. <span data-ttu-id="3a492-122">Quand on vous le demande, indiquez le nom de *votre société* dans [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="3a492-122">When prompted, enter the name of *your company* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="3a492-123">Il ne s'agit pas du nom complet.</span><span class="sxs-lookup"><span data-stu-id="3a492-123">This is not the display name.</span></span> <span data-ttu-id="3a492-124">Le nom de la société se trouve dans la page Sociétés de votre instance [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="3a492-124">The company name can be found on the 'Companies' page within your [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] instance.</span></span> 
<span data-ttu-id="3a492-125">![Sélectionner Dynamics 365 Business Central et sélectionner Obtenir maintenant](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span><span class="sxs-lookup"><span data-stu-id="3a492-125">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span></span>
5. <span data-ttu-id="3a492-126">Une fois connecté, un tableau de bord, un état et un ensemble de données sont automatiquement chargés dans votre espace de travail Power BI.</span><span class="sxs-lookup"><span data-stu-id="3a492-126">Once connected, a dashboard, report and dataset will automatically be loaded into your Power BI workspace.</span></span> <span data-ttu-id="3a492-127">Une fois terminé, les mosaïques sont mises à jour avec les données de votre société [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="3a492-127">When completed, the tiles will update with data from your [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] company.</span></span>
<span data-ttu-id="3a492-128">![Sélectionner Dynamics 365 Business Central et sélectionner Obtenir maintenant](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span><span class="sxs-lookup"><span data-stu-id="3a492-128">![Select Dynamics 365 Business Central  and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span></span>

## <a name="what-now"></a><span data-ttu-id="3a492-129">Et ensuite ?</span><span class="sxs-lookup"><span data-stu-id="3a492-129">What Now?</span></span>

- <span data-ttu-id="3a492-130">Cliquez sur [poser une question dans la zone Q&R](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) en haut du tableau de bord.</span><span class="sxs-lookup"><span data-stu-id="3a492-130">Try [asking a question in the Q&A box](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) at the top of the dashboard.</span></span>
- <span data-ttu-id="3a492-131">[Modifiez les mosaïques](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) du tableau de bord.</span><span class="sxs-lookup"><span data-stu-id="3a492-131">[Change the tiles](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) in the dashboard.</span></span>  
- <span data-ttu-id="3a492-132">[Sélectionnez une mosaïque](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) pour ouvrir l'état sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="3a492-132">[Select a tile](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) to open the underlying report.</span></span>  
- <span data-ttu-id="3a492-133">Il est prévu que votre ensemble de données soit actualisé quotidiennement, vous pouvez toutefois modifier la planification de l'actualisation ou essayer de l'actualiser à la demande en sélectionnant **Actualiser maintenant**.</span><span class="sxs-lookup"><span data-stu-id="3a492-133">While your dataset will be scheduled to refreshed daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="3a492-134">Configuration système requise</span><span class="sxs-lookup"><span data-stu-id="3a492-134">System Requirements</span></span>
<span data-ttu-id="3a492-135">Pour importer les données [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] dans Power BI, vous devez disposer des autorisations sur les services Web utilisés pour récupérer les données.</span><span class="sxs-lookup"><span data-stu-id="3a492-135">To import your [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data into Power BI, you need to have permissions to the web services used to retrieve data.</span></span> <span data-ttu-id="3a492-136">Les services Web obligatoires pour chaque pack de contenu incluent :</span><span class="sxs-lookup"><span data-stu-id="3a492-136">The web services required for each content pack include:</span></span>

## <a name="role-center-reports"></a><span data-ttu-id="3a492-137">États du Tableau de bord</span><span class="sxs-lookup"><span data-stu-id="3a492-137">Role Center Reports</span></span>

<span data-ttu-id="3a492-138">**Microsoft Dynamics 365 Business Central – CRM**</span><span class="sxs-lookup"><span data-stu-id="3a492-138">**Microsoft Dynamics 365 Business Central – CRM**</span></span>
- <span data-ttu-id="3a492-139">Opportunités ventes</span><span class="sxs-lookup"><span data-stu-id="3a492-139">Sales Opportunities</span></span>
- <span data-ttu-id="3a492-140">Modèle Excel Afficher Société</span><span class="sxs-lookup"><span data-stu-id="3a492-140">Excel Template View Company</span></span>
- <span data-ttu-id="3a492-141">Étiquettes d'état Power BI</span><span class="sxs-lookup"><span data-stu-id="3a492-141">Power BI Report Labels</span></span>

<span data-ttu-id="3a492-142">**Microsoft Dynamics 365 Business Central – Finance**</span><span class="sxs-lookup"><span data-stu-id="3a492-142">**Microsoft Dynamics 365 Business Central – Finance**</span></span>
- <span data-ttu-id="3a492-143">PowerBIFinance</span><span class="sxs-lookup"><span data-stu-id="3a492-143">PowerBIFinance</span></span>
- <span data-ttu-id="3a492-144">Modèle Excel Afficher Société</span><span class="sxs-lookup"><span data-stu-id="3a492-144">Excel Template View Company</span></span>
- <span data-ttu-id="3a492-145">Étiquettes d'état Power BI</span><span class="sxs-lookup"><span data-stu-id="3a492-145">Power BI Report Labels</span></span>

<span data-ttu-id="3a492-146">**Microsoft Dynamics 365 Business Central – Jobs**</span><span class="sxs-lookup"><span data-stu-id="3a492-146">**Microsoft Dynamics 365 Business Central – Jobs**</span></span>
- <span data-ttu-id="3a492-147">Liste des projets</span><span class="sxs-lookup"><span data-stu-id="3a492-147">Job List</span></span>
- <span data-ttu-id="3a492-148">Lignes planning projet</span><span class="sxs-lookup"><span data-stu-id="3a492-148">Job Planning Lines</span></span>
- <span data-ttu-id="3a492-149">Lignes tâche projet</span><span class="sxs-lookup"><span data-stu-id="3a492-149">Job Task Lines</span></span>
- <span data-ttu-id="3a492-150">Étiquettes d'état Power BI</span><span class="sxs-lookup"><span data-stu-id="3a492-150">Power BI Report Labels</span></span>
- <span data-ttu-id="3a492-151">Modèle Excel Afficher Société</span><span class="sxs-lookup"><span data-stu-id="3a492-151">Excel Template View Company</span></span>

<span data-ttu-id="3a492-152">**Microsoft Dynamics 365 Business Central - Sales**</span><span class="sxs-lookup"><span data-stu-id="3a492-152">**Microsoft Dynamics 365 Business Central - Sales**</span></span>
- <span data-ttu-id="3a492-153">Tableau de bord ventes</span><span class="sxs-lookup"><span data-stu-id="3a492-153">Sales Dashboard</span></span>
- <span data-ttu-id="3a492-154">Modèle Excel Afficher Société</span><span class="sxs-lookup"><span data-stu-id="3a492-154">Excel Template View Company</span></span>
- <span data-ttu-id="3a492-155">Étiquettes d'état Power BI</span><span class="sxs-lookup"><span data-stu-id="3a492-155">Power BI Report Labels</span></span>

## <a name="list-page-reports"></a><span data-ttu-id="3a492-156">États Page de liste</span><span class="sxs-lookup"><span data-stu-id="3a492-156">List Page Reports</span></span> 

<span data-ttu-id="3a492-157">**Microsoft Dynamics 365 Business Central – Customers List**</span><span class="sxs-lookup"><span data-stu-id="3a492-157">**Microsoft Dynamics 365 Business Central – Customers List**</span></span>
- <span data-ttu-id="3a492-158">Ventes d'articles par client</span><span class="sxs-lookup"><span data-stu-id="3a492-158">Item Sales by Customer</span></span>
- <span data-ttu-id="3a492-159">Liste des achats d'articles Power BI</span><span class="sxs-lookup"><span data-stu-id="3a492-159">Power BI Item Purchase List</span></span>
- <span data-ttu-id="3a492-160">Liste des ventes d'articles Power BI</span><span class="sxs-lookup"><span data-stu-id="3a492-160">Power BI Item Sales List</span></span>
- <span data-ttu-id="3a492-161">Tableau de bord ventes</span><span class="sxs-lookup"><span data-stu-id="3a492-161">Sales Dashboard</span></span>
- <span data-ttu-id="3a492-162">Liste des clients Power BI</span><span class="sxs-lookup"><span data-stu-id="3a492-162">Power BI Customer List</span></span>
- <span data-ttu-id="3a492-163">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="3a492-163">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="3a492-164">Étiquettes d'état Power BI</span><span class="sxs-lookup"><span data-stu-id="3a492-164">Power BI Report Labels</span></span> 

<span data-ttu-id="3a492-165">**Microsoft Dynamics 365 Business Central - General Ledger Entries List**</span><span class="sxs-lookup"><span data-stu-id="3a492-165">**Microsoft Dynamics 365 Business Central - General Ledger Entries List**</span></span>
- <span data-ttu-id="3a492-166">Liste des montants Power BI GL</span><span class="sxs-lookup"><span data-stu-id="3a492-166">Power BI GL Amount List</span></span>
- <span data-ttu-id="3a492-167">Montant budgété Power BI GL</span><span class="sxs-lookup"><span data-stu-id="3a492-167">Power BI GL Budgeted Amount</span></span>
- <span data-ttu-id="3a492-168">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="3a492-168">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="3a492-169">Étiquettes d'état Power BI</span><span class="sxs-lookup"><span data-stu-id="3a492-169">Power BI Report Labels</span></span>

<span data-ttu-id="3a492-170">**Microsoft Dynamics 365 Business Central – Items List**</span><span class="sxs-lookup"><span data-stu-id="3a492-170">**Microsoft Dynamics 365 Business Central – Items List**</span></span>
- <span data-ttu-id="3a492-171">Ventes d'articles par client</span><span class="sxs-lookup"><span data-stu-id="3a492-171">Item Sales by Customer</span></span>
- <span data-ttu-id="3a492-172">Liste des achats d'articles Power BI</span><span class="sxs-lookup"><span data-stu-id="3a492-172">Power BI Item Purchase List</span></span>
- <span data-ttu-id="3a492-173">Liste des ventes d'articles Power BI</span><span class="sxs-lookup"><span data-stu-id="3a492-173">Power BI Item Sales List</span></span>
- <span data-ttu-id="3a492-174">Tableau de bord ventes</span><span class="sxs-lookup"><span data-stu-id="3a492-174">Sales Dashboard</span></span>
- <span data-ttu-id="3a492-175">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="3a492-175">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="3a492-176">Étiquettes d'état Power BI</span><span class="sxs-lookup"><span data-stu-id="3a492-176">Power BI Report Labels</span></span>

<span data-ttu-id="3a492-177">**Microsoft Dynamics 365 Business Central – Jobs List**</span><span class="sxs-lookup"><span data-stu-id="3a492-177">**Microsoft Dynamics 365 Business Central – Jobs List**</span></span>
- <span data-ttu-id="3a492-178">Liste des projets Power BI</span><span class="sxs-lookup"><span data-stu-id="3a492-178">Power BI Jobs List</span></span>
- <span data-ttu-id="3a492-179">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="3a492-179">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="3a492-180">Étiquettes d'état Power BI</span><span class="sxs-lookup"><span data-stu-id="3a492-180">Power BI Report Labels</span></span>

<span data-ttu-id="3a492-181">**Microsoft Dynamics 365 Business Central – Purchase Invoices List**</span><span class="sxs-lookup"><span data-stu-id="3a492-181">**Microsoft Dynamics 365 Business Central – Purchase Invoices List**</span></span>
- <span data-ttu-id="3a492-182">Liste des achats Power BI</span><span class="sxs-lookup"><span data-stu-id="3a492-182">Power BI Purchase List</span></span>
- <span data-ttu-id="3a492-183">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="3a492-183">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="3a492-184">Étiquettes d'état Power BI</span><span class="sxs-lookup"><span data-stu-id="3a492-184">Power BI Report Labels</span></span>

<span data-ttu-id="3a492-185">**Microsoft Dynamics 365 Business Central – Sales Orders List**</span><span class="sxs-lookup"><span data-stu-id="3a492-185">**Microsoft Dynamics 365 Business Central – Sales Orders List**</span></span>
- <span data-ttu-id="3a492-186">Liste des ventes Power BI</span><span class="sxs-lookup"><span data-stu-id="3a492-186">Power BI Sales List</span></span>
- <span data-ttu-id="3a492-187">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="3a492-187">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="3a492-188">Étiquettes d'état Power BI</span><span class="sxs-lookup"><span data-stu-id="3a492-188">Power BI Report Labels</span></span>


<span data-ttu-id="3a492-189">**Microsoft Dynamics 365 Business Central – Vendors List**</span><span class="sxs-lookup"><span data-stu-id="3a492-189">**Microsoft Dynamics 365 Business Central – Vendors List**</span></span>
- <span data-ttu-id="3a492-190">Liste des achats d'articles Power BI</span><span class="sxs-lookup"><span data-stu-id="3a492-190">Power BI Item Purchase List</span></span>
- <span data-ttu-id="3a492-191">Liste des ventes d'articles Power BI</span><span class="sxs-lookup"><span data-stu-id="3a492-191">Power BI Item Sales List</span></span>
- <span data-ttu-id="3a492-192">Liste des fournisseurs Power BI</span><span class="sxs-lookup"><span data-stu-id="3a492-192">Power BI Vendor List</span></span>
- <span data-ttu-id="3a492-193">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="3a492-193">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="3a492-194">Étiquettes d'état Power BI</span><span class="sxs-lookup"><span data-stu-id="3a492-194">Power BI Report Labels</span></span>

## <a name="web-services"></a><span data-ttu-id="3a492-195">Services web</span><span class="sxs-lookup"><span data-stu-id="3a492-195">Web Services</span></span>
<span data-ttu-id="3a492-196">Pour trouver facilement les services Web, il suffit de les chercher dans [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="3a492-196">An easy way to find the web services is to search for web services in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="3a492-197">Dans la liste, assurez-vous que la case Publier est cochée pour les services Web répertoriés ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="3a492-197">In the list make sure the Publish box is marked for the web services listed above.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="3a492-198">Incident</span><span class="sxs-lookup"><span data-stu-id="3a492-198">Troubleshooting</span></span>
<span data-ttu-id="3a492-199">Le tableau de bord Power BI s'appuie sur les services Web publiés qui sont répertoriés ci-dessus. Il affichera les données de la société de démonstration ou de votre propre société si vous importez les données de votre solution financière actuelle.</span><span class="sxs-lookup"><span data-stu-id="3a492-199">The Power BI dashboard relies on the published web services that are listed above, and it will show data from the demonstration company or your own company if you import data from your current finance solution.</span></span> <span data-ttu-id="3a492-200">Toutefois, si une erreur se produit, cette section fournit une solution de rechange pour les problèmes les plus courants.</span><span class="sxs-lookup"><span data-stu-id="3a492-200">However, if something goes wrong, this section provides a workaround for the most typical issues.</span></span>

### <a name="incorrect-company-name"></a><span data-ttu-id="3a492-201">Nom de société incorrect</span><span class="sxs-lookup"><span data-stu-id="3a492-201">Incorrect Company Name</span></span>  
<span data-ttu-id="3a492-202">Une erreur commune consiste à entrer le nom complet de la société au lieu du nom de la société.</span><span class="sxs-lookup"><span data-stu-id="3a492-202">A common mistake is to enter the company display name instead of the company name.</span></span> <span data-ttu-id="3a492-203">Pour trouver le nom de la société, cherchez dans **Sociétés**.</span><span class="sxs-lookup"><span data-stu-id="3a492-203">To find the company name search for **Companies**.</span></span> <span data-ttu-id="3a492-204">Utilisez ensuite le champ **Nom** au moment de saisir le nom de votre société.</span><span class="sxs-lookup"><span data-stu-id="3a492-204">Then use the **Name** field when entering your company name.</span></span>

### <a name="incorrect-user-name-and-password"></a><span data-ttu-id="3a492-205">Nom d'utilisateur et mot de passe incorrects</span><span class="sxs-lookup"><span data-stu-id="3a492-205">Incorrect User Name and Password</span></span>  
<span data-ttu-id="3a492-206">Le nom d'utilisateur et le mot de passe utilisés pour la connexion sont identiques à ceux utilisés pour la connexion à votre compte Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="3a492-206">The user name and password used to connect will be the same as what is used to connect to your Microsoft Office 365 account.</span></span>  

<span data-ttu-id="3a492-207">Les packs de contenu nécessitent également que vous ayez un compte [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3a492-207">The content packs also require that you have a Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account.</span></span> <span data-ttu-id="3a492-208">Une fois les informations d'identification saisies, tous les abonnés [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Microsoft accessibles seront détectés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="3a492-208">Once you enter your credentials, we will auto discover any Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] tenants you have access to.</span></span> <span data-ttu-id="3a492-209">Si vous n'avez pas de compte Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] sous licence ou d'essai, vous recevrez un message d'erreur.</span><span class="sxs-lookup"><span data-stu-id="3a492-209">If you do not have a licensed or trial Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account, you will receive an error message.</span></span>

### <a name="the-key-didnt-match-any-rows-in-the-table"></a><span data-ttu-id="3a492-210">La clé ne correspond à aucune ligne de la table</span><span class="sxs-lookup"><span data-stu-id="3a492-210">The Key Didn't Match Any Rows in the Table</span></span>
<span data-ttu-id="3a492-211">Si vous entrez un nom de société non valide pendant le processus de connexion, le message d'erreur suivant « La clé ne correspond à aucune ligne de la table » peut s'afficher.</span><span class="sxs-lookup"><span data-stu-id="3a492-211">If you enter a non-valid company name during the connection process, you may get the error message "The key didn't match any rows in the table".</span></span> <span data-ttu-id="3a492-212">Indiquez le nom de société correct, puis reconnectez-vous.</span><span class="sxs-lookup"><span data-stu-id="3a492-212">Provide the correct company name and try connecting again.</span></span>

## <a name="see-also"></a><span data-ttu-id="3a492-213">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a492-213">See Also</span></span>
[<span data-ttu-id="3a492-214">Mise en route de Power BI</span><span class="sxs-lookup"><span data-stu-id="3a492-214">Get started with Power BI</span></span>](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[<span data-ttu-id="3a492-215">Power BI - Concepts de base</span><span class="sxs-lookup"><span data-stu-id="3a492-215">Power BI - Basic Concepts</span></span>](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)  
[<span data-ttu-id="3a492-216">Veille économique</span><span class="sxs-lookup"><span data-stu-id="3a492-216">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="3a492-217">Mise en route</span><span class="sxs-lookup"><span data-stu-id="3a492-217">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="3a492-218">Importation des données métier à partir d'autres systèmes financiers</span><span class="sxs-lookup"><span data-stu-id="3a492-218">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="3a492-219">[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="3a492-219">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="3a492-220">Finances</span><span class="sxs-lookup"><span data-stu-id="3a492-220">Finance</span></span>](finance.md)  
<span data-ttu-id="3a492-221">[Configuration de la génération d'états [!INCLUDE[d365fin](includes/d365fin_md.md)] dans Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="3a492-221">[Setup Reporting for [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span></span>  

