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
ms.date: 03/16/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 315d4b188cdd834e82676a0c5ef77272ad873eb7
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="connecting-power-bi-to-business-central-content-packs"></a><span data-ttu-id="ed579-103">Connexion de Power BI aux packs de contenu Business Central</span><span class="sxs-lookup"><span data-stu-id="ed579-103">Connecting Power BI to Business Central Content Packs</span></span>
<span data-ttu-id="ed579-104">Il est facile d'obtenir des informations exploitables de vos données [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Microsoft grâce à Power BI et aux packs de contenu [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ed579-104">Getting insights into your Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data is easy with Power BI and the Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] content packs.</span></span> <span data-ttu-id="ed579-105">Power BI extrait vos données, puis génère un tableau de bord prêt à l'emploi et des états basés sur ces données.</span><span class="sxs-lookup"><span data-stu-id="ed579-105">Power BI retrieves your data then builds an out-of-the-box dashboard and reports based on that data.</span></span>

> [!NOTE]  
>  <span data-ttu-id="ed579-106">Vous devez disposer d'un compte valide avec [!INCLUDE[d365fin](includes/d365fin_md.md)] et avec Power BI.</span><span class="sxs-lookup"><span data-stu-id="ed579-106">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Power BI.</span></span> <span data-ttu-id="ed579-107">En outre, vous devez télécharger [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span><span class="sxs-lookup"><span data-stu-id="ed579-107">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span></span>  
>  <span data-ttu-id="ed579-108">Les packs de contenu Power BI nécessitent des autorisations vers les tables d'où sont extraites les données.</span><span class="sxs-lookup"><span data-stu-id="ed579-108">Power BI content packs require permissions to the tables where data is retrieved from.</span></span> <span data-ttu-id="ed579-109">Vous trouverez plus d'informations sur les besoins ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="ed579-109">More details on the requirements are described below.</span></span>  

## <a name="how-to-connect"></a><span data-ttu-id="ed579-110">Pour vous connecter</span><span class="sxs-lookup"><span data-stu-id="ed579-110">How to Connect</span></span>
1. <span data-ttu-id="ed579-111">Sélectionnez **Extraire les données** en bas du volet de navigation gauche.</span><span class="sxs-lookup"><span data-stu-id="ed579-111">Select **Get Data** at the bottom of the left navigation pane.</span></span>  
<span data-ttu-id="ed579-112">![Naviguer pour obtenir des données](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span><span class="sxs-lookup"><span data-stu-id="ed579-112">![Navigating to Get Data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span></span>
2. <span data-ttu-id="ed579-113">Dans la zone **Services**, sélectionnez **Extraire**.</span><span class="sxs-lookup"><span data-stu-id="ed579-113">In the **Services** box, select **Get**.</span></span> <span data-ttu-id="ed579-114">Une fenêtre s'ouvre alors, elle contient **AppSource** et **Applications pour applications Power BI**.</span><span class="sxs-lookup"><span data-stu-id="ed579-114">This will open a window with the **AppSource** and **Apps for Power BI apps**.</span></span>  
<span data-ttu-id="ed579-115">![Choisir des packs de contenu à partir des services en ligne](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span><span class="sxs-lookup"><span data-stu-id="ed579-115">![Choose content packs from online services](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span></span>
3. <span data-ttu-id="ed579-116">Sélectionnez **Applications** dans l'onglet **Applications pour applications Power BI** et choisissez le pack de contenu **Microsoft Dynamics 365 Business Central** à utiliser, puis cliquez sur **Obtenir maintenant**.</span><span class="sxs-lookup"><span data-stu-id="ed579-116">Select **Apps** from the **Apps for Power BI apps** tab, and choose the **Microsoft Dynamics 365 Business Central** content pack that you want to use, and then select **Get it now**.</span></span>  
<span data-ttu-id="ed579-117">![Sélectionner Dynamics 365 Business Central et sélectionner Obtenir maintenant](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span><span class="sxs-lookup"><span data-stu-id="ed579-117">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span></span>
4. <span data-ttu-id="ed579-118">Quand on vous le demande, indiquez le nom de *votre société* dans [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ed579-118">When prompted, enter the name of *your company* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="ed579-119">Il ne s'agit pas du nom complet.</span><span class="sxs-lookup"><span data-stu-id="ed579-119">This is not the display name.</span></span>  
<span data-ttu-id="ed579-120">![Sélectionner Dynamics 365 Business Central et sélectionner Obtenir maintenant](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span><span class="sxs-lookup"><span data-stu-id="ed579-120">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span></span>
5. <span data-ttu-id="ed579-121">Une fois connecté, un tableau de bord, un état et un ensemble de données sont automatiquement chargés dans votre espace de travail Power BI.</span><span class="sxs-lookup"><span data-stu-id="ed579-121">Once connected, a dashboard, report and dataset will automatically be loaded into your Power BI workspace.</span></span> <span data-ttu-id="ed579-122">Une fois terminé, les mosaïques sont mises à jour avec les données de votre compte.</span><span class="sxs-lookup"><span data-stu-id="ed579-122">When completed, the tiles will update with data from your account.</span></span>
<span data-ttu-id="ed579-123">![Sélectionner Dynamics 365 Business Central et sélectionner Obtenir maintenant](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span><span class="sxs-lookup"><span data-stu-id="ed579-123">![Select Dynamics 365 Business Central  and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span></span>

## <a name="what-now"></a><span data-ttu-id="ed579-124">Et ensuite ?</span><span class="sxs-lookup"><span data-stu-id="ed579-124">What Now?</span></span>

- <span data-ttu-id="ed579-125">[Modifiez les mosaïques](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) du tableau de bord.</span><span class="sxs-lookup"><span data-stu-id="ed579-125">[Change the tiles](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) in the dashboard.</span></span>  
- <span data-ttu-id="ed579-126">[Sélectionnez une mosaïque](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) pour ouvrir l'état sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="ed579-126">[Select a tile](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) to open the underlying report.</span></span>  
- <span data-ttu-id="ed579-127">Il est prévu que votre ensemble de données soit actualisé quotidiennement, vous pouvez toutefois modifier la planification de l'actualisation ou essayer de l'actualiser à la demande en sélectionnant **Actualiser maintenant**.</span><span class="sxs-lookup"><span data-stu-id="ed579-127">While your dataset will be scheduled to refreshed daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="ed579-128">Configuration système requise</span><span class="sxs-lookup"><span data-stu-id="ed579-128">System Requirements</span></span>
<span data-ttu-id="ed579-129">Pour importer les données [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] dans Power BI, vous devez disposer des autorisations sur les services Web utilisés pour récupérer les données.</span><span class="sxs-lookup"><span data-stu-id="ed579-129">To import your [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data into Power BI, you need to have permissions to the web services used to retrieve data.</span></span> <span data-ttu-id="ed579-130">Les services Web obligatoires pour chaque pack de contenu incluent :</span><span class="sxs-lookup"><span data-stu-id="ed579-130">The web services required for each content pack include:</span></span>

<span data-ttu-id="ed579-131">**Microsoft Dynamics 365 Business Central – CRM**</span><span class="sxs-lookup"><span data-stu-id="ed579-131">**Microsoft Dynamics 365 Business Central – CRM**</span></span>
- <span data-ttu-id="ed579-132">SalesOpportunities</span><span class="sxs-lookup"><span data-stu-id="ed579-132">SalesOpportunities</span></span>
- <span data-ttu-id="ed579-133">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="ed579-133">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="ed579-134">**Microsoft Dynamics 365 Business Central – Ventes**</span><span class="sxs-lookup"><span data-stu-id="ed579-134">**Microsoft Dynamics 365 Business Central – Sales**</span></span>
- <span data-ttu-id="ed579-135">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="ed579-135">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="ed579-136">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="ed579-136">SalesDashboard</span></span>
- <span data-ttu-id="ed579-137">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="ed579-137">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="ed579-138">**Microsoft Dynamics 365 Business Central – Finance**</span><span class="sxs-lookup"><span data-stu-id="ed579-138">**Microsoft Dynamics 365 Business Central – Finance**</span></span>
- <span data-ttu-id="ed579-139">PowerBIFinance</span><span class="sxs-lookup"><span data-stu-id="ed579-139">PowerBIFinance</span></span>
- <span data-ttu-id="ed579-140">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="ed579-140">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="ed579-141">**Microsoft Dynamics 365 Business Central – Projets**</span><span class="sxs-lookup"><span data-stu-id="ed579-141">**Microsoft Dynamics 365 Business Central – Jobs**</span></span>
- <span data-ttu-id="ed579-142">Liste des projets</span><span class="sxs-lookup"><span data-stu-id="ed579-142">Job List</span></span>
- <span data-ttu-id="ed579-143">Lignes planning projet</span><span class="sxs-lookup"><span data-stu-id="ed579-143">Job Planning Lines</span></span>
- <span data-ttu-id="ed579-144">Lignes tâche projet</span><span class="sxs-lookup"><span data-stu-id="ed579-144">Job Task Lines</span></span>

<span data-ttu-id="ed579-145">**Microsoft Dynamics 365 Business Central – Liste des clients**</span><span class="sxs-lookup"><span data-stu-id="ed579-145">**Microsoft Dynamics 365 Business Central – Customers List**</span></span>
- <span data-ttu-id="ed579-146">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="ed579-146">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="ed579-147">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="ed579-147">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="ed579-148">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="ed579-148">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="ed579-149">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="ed579-149">SalesDashboard</span></span>
- <span data-ttu-id="ed579-150">Power_BI_Customer_List</span><span class="sxs-lookup"><span data-stu-id="ed579-150">Power_BI_Customer_List</span></span>
- <span data-ttu-id="ed579-151">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="ed579-151">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="ed579-152">**Microsoft Dynamics 365 Business Central – Liste des articles**</span><span class="sxs-lookup"><span data-stu-id="ed579-152">**Microsoft Dynamics 365 Business Central – Items List**</span></span>
- <span data-ttu-id="ed579-153">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="ed579-153">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="ed579-154">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="ed579-154">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="ed579-155">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="ed579-155">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="ed579-156">Articles</span><span class="sxs-lookup"><span data-stu-id="ed579-156">Items</span></span>
- <span data-ttu-id="ed579-157">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="ed579-157">SalesDashboard</span></span>
- <span data-ttu-id="ed579-158">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="ed579-158">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="ed579-159">**Microsoft Dynamics 365 Business Central – Liste des fournisseurs**</span><span class="sxs-lookup"><span data-stu-id="ed579-159">**Microsoft Dynamics 365 Business Central – Vendors List**</span></span>
- <span data-ttu-id="ed579-160">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="ed579-160">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="ed579-161">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="ed579-161">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="ed579-162">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="ed579-162">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="ed579-163">Articles</span><span class="sxs-lookup"><span data-stu-id="ed579-163">Items</span></span>
- <span data-ttu-id="ed579-164">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="ed579-164">SalesDashboard</span></span>
- <span data-ttu-id="ed579-165">Power_BI_Customer_List</span><span class="sxs-lookup"><span data-stu-id="ed579-165">Power_BI_Customer_List</span></span>
- <span data-ttu-id="ed579-166">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="ed579-166">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="ed579-167">Power_BI_Vendor_List</span><span class="sxs-lookup"><span data-stu-id="ed579-167">Power_BI_Vendor_List</span></span>
- <span data-ttu-id="ed579-168">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="ed579-168">ExcelTemplateViewCompany</span></span>

## <a name="web-services"></a><span data-ttu-id="ed579-169">Services web</span><span class="sxs-lookup"><span data-stu-id="ed579-169">Web Services</span></span>
<span data-ttu-id="ed579-170">Pour trouver facilement les services Web, il suffit de les chercher dans [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ed579-170">An easy way to find the web services is to search for web services in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="ed579-171">Dans la liste, assurez-vous que la case Publier est cochée pour les services Web répertoriés ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="ed579-171">In the list make sure the Publish box is marked for the web services listed above.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="ed579-172">Incident</span><span class="sxs-lookup"><span data-stu-id="ed579-172">Troubleshooting</span></span>
<span data-ttu-id="ed579-173">Le tableau de bord Power BI s'appuie sur les services Web publiés qui sont répertoriés ci-dessus. Il affichera les données de la société de démonstration ou de votre propre société si vous importez les données de votre solution financière actuelle.</span><span class="sxs-lookup"><span data-stu-id="ed579-173">The Power BI dashboard relies on the published web services that are listed above, and it will show data from the demonstration company or your own company if you import data from your current finance solution.</span></span> <span data-ttu-id="ed579-174">Toutefois, si une erreur se produit, cette section fournit une solution de rechange pour les problèmes les plus courants.</span><span class="sxs-lookup"><span data-stu-id="ed579-174">However, if something goes wrong, this section provides a workaround for the most typical issues.</span></span>

### <a name="incorrect-company-name"></a><span data-ttu-id="ed579-175">Nom de société incorrect</span><span class="sxs-lookup"><span data-stu-id="ed579-175">Incorrect Company Name</span></span>  
<span data-ttu-id="ed579-176">Une erreur commune consiste à entrer le nom complet de la société au lieu du nom de la société.</span><span class="sxs-lookup"><span data-stu-id="ed579-176">A common mistake is to enter the company display name instead of the company name.</span></span> <span data-ttu-id="ed579-177">Pour trouver le nom de la société, cherchez dans **Sociétés**.</span><span class="sxs-lookup"><span data-stu-id="ed579-177">To find the company name search for **Companies**.</span></span> <span data-ttu-id="ed579-178">Utilisez ensuite le champ **Nom** au moment de saisir le nom de votre société.</span><span class="sxs-lookup"><span data-stu-id="ed579-178">Then use the **Name** field when entering your company name.</span></span>

### <a name="incorrect-user-name-and-password"></a><span data-ttu-id="ed579-179">Nom d'utilisateur et mot de passe incorrects</span><span class="sxs-lookup"><span data-stu-id="ed579-179">Incorrect User Name and Password</span></span>  
<span data-ttu-id="ed579-180">Le nom d'utilisateur et le mot de passe utilisés pour la connexion sont identiques à ceux utilisés pour la connexion à votre compte Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="ed579-180">The user name and password used to connect will be the same as what is used to connect to your Microsoft Office 365 account.</span></span>  

<span data-ttu-id="ed579-181">Les packs de contenu nécessitent également que vous ayez un compte [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ed579-181">The content packs also require that you have a Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account.</span></span> <span data-ttu-id="ed579-182">Une fois les informations d'identification saisies, tous les abonnés [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Microsoft accessibles seront détectés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="ed579-182">Once you enter your credentials, we will auto discover any Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] tenants you have access to.</span></span> <span data-ttu-id="ed579-183">Si vous n'avez pas de compte Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] sous licence ou d'essai, vous recevrez un message d'erreur.</span><span class="sxs-lookup"><span data-stu-id="ed579-183">If you do not have a licensed or trial Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account, you will receive an error message.</span></span>

### <a name="the-key-didnt-match-any-rows-in-the-table"></a><span data-ttu-id="ed579-184">La clé ne correspond à aucune ligne de la table</span><span class="sxs-lookup"><span data-stu-id="ed579-184">The Key Didn't Match Any Rows in the Table</span></span>
<span data-ttu-id="ed579-185">Si vous entrez un nom de société non valide pendant le processus de connexion, le message d'erreur suivant « La clé ne correspond à aucune ligne de la table » peut s'afficher.</span><span class="sxs-lookup"><span data-stu-id="ed579-185">If you enter a non valid company name during the connection process, you may get the error message "The key didn't match any rows in the table".</span></span> <span data-ttu-id="ed579-186">Indiquez le nom de société correct, puis reconnectez-vous.</span><span class="sxs-lookup"><span data-stu-id="ed579-186">Provide the correct company name and try connecting again.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed579-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed579-187">See Also</span></span>
[<span data-ttu-id="ed579-188">Mise en route de Power BI</span><span class="sxs-lookup"><span data-stu-id="ed579-188">Get started with Power BI</span></span>](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
<span data-ttu-id="ed579-189">[Power BI - Concepts de base](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Veille économique](bi.md)</span><span class="sxs-lookup"><span data-stu-id="ed579-189">[Power BI - Basic Concepts](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Business Intelligence](bi.md)</span></span>  
<span data-ttu-id="ed579-190">[Bienvenue dans [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="ed579-190">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="ed579-191">Importation des données métier à partir d'autres systèmes financiers</span><span class="sxs-lookup"><span data-stu-id="ed579-191">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="ed579-192">[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="ed579-192">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="ed579-193">Finances</span><span class="sxs-lookup"><span data-stu-id="ed579-193">Finance</span></span>](finance.md)  
<span data-ttu-id="ed579-194">[Configuration de la génération d'états [!INCLUDE[d365fin](includes/d365fin_md.md)] dans Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="ed579-194">[Setup Reporting for [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span></span>  

