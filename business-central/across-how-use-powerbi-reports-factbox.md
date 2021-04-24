---
title: Afficher les états Power BI personnalisés pour les données Business Central | Microsoft Docs
description: Vous pouvez utiliser des états Power BI pour obtenir des informations supplémentaires sur les données dans les listes.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: a600b24e16172134d4f8e78cf47efa4e262cac09
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777531"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prod_short"></a><span data-ttu-id="9e7f6-103">Création d’états Power BI pour afficher les données de liste dans [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="9e7f6-103">Creating Power BI Reports for Displaying List Data in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

[!INCLUDE[prod_long](includes/prod_long.md)] <span data-ttu-id="9e7f6-104">comprend un élément de contrôle Récapitulatif Power BI sur plusieurs pages de liste clé.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-104">includes a Power BI FactBox control element on many key list pages.</span></span> <span data-ttu-id="9e7f6-105">Le but de ce Récapitulatif est d'afficher des états Power BI liés aux enregistrements dans les listes, fournissant des informations supplémentaires sur les données.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-105">The purpose of this FactBox is to display Power BI reports that are related to records in the lists, providing extra insight into the data.</span></span> <span data-ttu-id="9e7f6-106">L'idée est que lorsque vous vous déplacez entre les lignes de la liste, l’état est mis à jour et filtré pour l’écriture sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-106">The idea is that as you move between rows in the list, the report is updated and filtered for the selected entry.</span></span>

[!INCLUDE[prod_long](includes/prod_long.md)] <span data-ttu-id="9e7f6-107">est livré avec certains de ces états.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-107">comes ready with some of these reports.</span></span> <span data-ttu-id="9e7f6-108">Vous pouvez également créer vos propres rapports personnalisés qui s'affichent dans ce Récapitulatif.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-108">You can also create your own custom reports that display in this FactBox.</span></span> <span data-ttu-id="9e7f6-109">La création de ces rapports est similaire à d'autres rapports.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-109">Creating these reports is similar to other reports.</span></span> <span data-ttu-id="9e7f6-110">Mais il y a quelques règles de conception que vous devrez suivre pour vous assurer que les rapports s'affichent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-110">But there are a few design rules you'll have to follow to make sure the reports display as expected.</span></span> <span data-ttu-id="9e7f6-111">Ces règles sont expliquées dans cet article.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-111">These rules are explained in this article.</span></span>

> [!NOTE]
> <span data-ttu-id="9e7f6-112">Pour des informations générales sur la création et la publication des états Power BI pour Business Central, voir [Création d'états Power BI pour afficher des données [!INCLUDE [prod_long](includes/prod_long.md)]](across-how-use-financials-data-source-powerbi.md).</span><span class="sxs-lookup"><span data-stu-id="9e7f6-112">For general information about creating and publishing Power BI reports for Business Central, see [Building Power BI Reports to Display [!INCLUDE [prod_long](includes/prod_long.md)] Data](across-how-use-financials-data-source-powerbi.md).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="9e7f6-113">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="9e7f6-113">Prerequisites</span></span>

- <span data-ttu-id="9e7f6-114">Un compte Power BI.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-114">A Power BI account.</span></span>
- <span data-ttu-id="9e7f6-115">Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-115">Power BI Desktop.</span></span>

<!-- 
For more information about getting started, see [Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).-->

## <a name="create-a-report-for-a-list-page"></a><span data-ttu-id="9e7f6-116">Créer un rapport pour une page de liste</span><span class="sxs-lookup"><span data-stu-id="9e7f6-116">Create a report for a list page</span></span>

1. <span data-ttu-id="9e7f6-117">Lancez Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-117">Start Power BI Desktop.</span></span>
2. <span data-ttu-id="9e7f6-118">Sélectionnez **Obtenir des données** et commencez à choisir la source de données pour le rapport.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-118">Select **Get Data**, and start choosing the data source for the report.</span></span>

    <span data-ttu-id="9e7f6-119">Dans cette étape, vous spécifiez les pages de liste Business Central qui contiennent les données souhaitées dans le rapport.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-119">In this step, you specify the Business Central list pages that contain the data that you want in the report.</span></span> <span data-ttu-id="9e7f6-120">Par exemple, pour créer un état pour la liste Ventes, assurez-vous que l’ensemble des données contient les informations liées aux ventes.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-120">For example, to create a report for the Sales List, ensure the data set contains information related to sales.</span></span>

    <span data-ttu-id="9e7f6-121">Pour plus d'informations, suivez les instructions [Ajouter[!INCLUDE[prod_short](includes/prod_short.md)] comme source de données dans Power BI Desktop](across-how-use-financials-data-source-powerbi.md#getdata).</span><span class="sxs-lookup"><span data-stu-id="9e7f6-121">For more information, follow the instructions [Add [!INCLUDE[prod_short](includes/prod_short.md)] as a data source in Power BI Desktop](across-how-use-financials-data-source-powerbi.md#getdata).</span></span>

3. <span data-ttu-id="9e7f6-122">Définissez le filtre d’état.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-122">Set the report filter.</span></span>

    <span data-ttu-id="9e7f6-123">Pour mettre à jour les données de l’enregistrement sélectionné dans la liste, vous ajoutez un filtre à l’état.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-123">To make the data update to the selected record in the list, you add a filter to the report.</span></span> <span data-ttu-id="9e7f6-124">Le filtre doit inclure un champ de la source de données utilisé pour identifier de manière unique chaque enregistrement de la liste.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-124">The filter must include a field of the data source that's used to uniquely identify each record in the list.</span></span> <span data-ttu-id="9e7f6-125">En termes de développeur, ce champ est la *clé primaire*.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-125">In developer terms, this field is the *primary key*.</span></span> <span data-ttu-id="9e7f6-126">Dans la plupart des cas, la clé primaire de la liste est **N°**</span><span class="sxs-lookup"><span data-stu-id="9e7f6-126">In most cases, the primary key for a list is the **No.**</span></span> <span data-ttu-id="9e7f6-127">.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-127">field.</span></span>

    <span data-ttu-id="9e7f6-128">Pour définir le filtre, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="9e7f6-128">To set the filter, do the following steps:</span></span>

    1. <span data-ttu-id="9e7f6-129">Dans les **Filtres**, sélectionnez le champ de clé primaire dans la liste des champs disponibles.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-129">In the **Filters**, select the primary key field from the list of available fields.</span></span>
    2. <span data-ttu-id="9e7f6-130">Faites glisser le champ vers le volet **Filtres** et déposez-le dans le zone **Filtres sur toutes les pages**.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-130">Drag the field to **Filters** pane and drop it in the **Filters on all pages** box.</span></span>
    3. <span data-ttu-id="9e7f6-131">Définissez le **Type de filtre** sur **Filtrage de base**.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-131">Set the **Filter type** to **Basic filtering**.</span></span> <span data-ttu-id="9e7f6-132">Il ne peut pas s’agir d’un filtre de page, visuel ou avancé.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-132">It can't be page, visual, or advanced filter.</span></span>

    ![Définition du filtre d’état pour l’état Activités Facture vente](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)
4. <span data-ttu-id="9e7f6-134">Concevez la disposition du rapport.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-134">Design the report layout.</span></span>

    <span data-ttu-id="9e7f6-135">Créez la disposition en faisant glisser des champs et en ajoutant des visualisations.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-135">Create the layout by dragging fields and adding visualizations.</span></span> <span data-ttu-id="9e7f6-136">Pour plus d'informations, voir [Utiliser la vue Rapport dans Power BI Desktop](/power-bi/create-reports/desktop-report-view) dans la documentation Power BI.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-136">For more information, see, [Work with Report view in Power BI Desktop](/power-bi/create-reports/desktop-report-view) in the Power BI documentation.</span></span>

5. <span data-ttu-id="9e7f6-137">Consultez les sections suivantes sur le dimensionnement du rapport et l'utilisation de plusieurs pages.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-137">See the next sections about sizing the report and using multiple pages.</span></span>

6. <span data-ttu-id="9e7f6-138">Enregistrez et nommez le rapport.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-138">Save and name the report.</span></span>

    <span data-ttu-id="9e7f6-139">Il est important de donner à l’état un nom contenant le nom de la page de liste associée à l’état.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-139">It's important to give the report a name that contains the name of the list page associated with the report.</span></span> <span data-ttu-id="9e7f6-140">Par exemple, si l’état concerne la page de liste **Articles**, incluez le mot *articles* quelque part dans le nom.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-140">For example, if the report is for the **Items** list page, include the word *items* somewhere in the name.</span></span>  

    <span data-ttu-id="9e7f6-141">Cette convention de désignation de nom n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-141">This naming convention isn't a requirement.</span></span> <span data-ttu-id="9e7f6-142">Cependant, il permet de sélectionner plus rapidement des états dans [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="9e7f6-142">However, it makes selecting reports in [!INCLUDE[prod_short](includes/prod_short.md)] quicker.</span></span> <span data-ttu-id="9e7f6-143">Lorsque la page de sélection de l’état s’ouvre à partir d’une page de liste, elle est automatiquement filtrée en fonction du nom de la page.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-143">When the report selection page opens from a list page, it's automatically filtered based on the page name.</span></span> <span data-ttu-id="9e7f6-144">Ce filtrage est effectué pour limiter les états affichés.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-144">This filtering is done to limit the reports that are displayed.</span></span> <span data-ttu-id="9e7f6-145">Vous pouvez aussi effacer le filtre pour obtenir la liste complète des états disponibles dans Power BI.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-145">Users can clear the filter to get a full list of reports available in Power BI.</span></span>

7. <span data-ttu-id="9e7f6-146">Lorsque vous avez terminé, publiez le rapport comme d'habitude.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-146">When you're done, publish the report as usual.</span></span>

    <span data-ttu-id="9e7f6-147">Pour en savoir plus, consultez [Publication d’un état](across-how-use-financials-data-source-powerbi.md#publish-reports).</span><span class="sxs-lookup"><span data-stu-id="9e7f6-147">For more information, see [Publishing a Report](across-how-use-financials-data-source-powerbi.md#publish-reports).</span></span>

8. <span data-ttu-id="9e7f6-148">Testez le rapport.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-148">Test the report.</span></span>

    <span data-ttu-id="9e7f6-149">Une fois les rapports publiés dans votre espace de travail, ils devraient être disponibles à partir du Récapitulatif Power BI sur la page de liste dans [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="9e7f6-149">Once the reports been published to your workspace, it should be available from the Power BI FactBox on the list page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

    <span data-ttu-id="9e7f6-150">Pour le tester, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-150">To test it, do the following steps.</span></span>

    1. <span data-ttu-id="9e7f6-151">Ouvrez [!INCLUDE[prod_short](includes/prod_short.md)] et allez à la page de liste.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-151">Open [!INCLUDE[prod_short](includes/prod_short.md)] and go to the list page.</span></span>
    2. <span data-ttu-id="9e7f6-152">Si vous ne voyez pas le Récapitulatif Power BI, dans la barre d’action, sélectionnez **Actions** > **Afficher** > **Afficher/Masquer les états Power BI**.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-152">If you don't see the Power BI FactBox, go the action bar, then select **Actions** > **Display** > **Show/Hide Power BI Reports**.</span></span>
    3. <span data-ttu-id="9e7f6-153">Dans le Récapitulatif Power BI, sélectionnez **Sélectionner des rapports**, cochez la case **Activer** pour le rapport, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-153">In the Power BI FactBox, select **Select Reports**, select the **Enable** box for the report, then select **OK**.</span></span>

    <span data-ttu-id="9e7f6-154">S'il est correctement conçu, le rapport s'affiche.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-154">If designed correctly, the report displays.</span></span>  

## <a name="set-the-report-size-and-color"></a><span data-ttu-id="9e7f6-155">Définissez la taille et la couleur de l’état</span><span class="sxs-lookup"><span data-stu-id="9e7f6-155">Set the report size and color</span></span>

<span data-ttu-id="9e7f6-156">La taille de l’état doit être configurée sur 325 pixels par 310 pixels.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-156">The size of the report must be set to 325 pixels by 310 pixels.</span></span> <span data-ttu-id="9e7f6-157">Cette taille offre une mise à l’échelle appropriée de l’état dans l’espace disponible du contrôle Récapitulatif Power BI dans [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="9e7f6-157">This size provides the proper scaling of the report in the available space of the Power BI FactBox control in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="9e7f6-158">Pour définir la taille de l’état, placez le focus en dehors de la zone de présentation d’état, puis choisissez l’icône en forme de rouleau de peinture.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-158">To define the size of the report, place focus outside of the report layout area, and then choose the paint roller icon.</span></span>

![Définition de la largeur et de la hauteur de l’état pour l’état Activités Facture vente](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

<span data-ttu-id="9e7f6-160">Vous pouvez modifier la largeur et la hauteur de l’état en choisissant **Personnalisé** dans le champ **Type**.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-160">You can change the width and height of the report by choosing **Custom** in the **Type** field.</span></span>

<span data-ttu-id="9e7f6-161">Si vous souhaitez que l’arrière-plan de l’état se fonde avec la couleur de l’arrière-plan du contrôle Récapitulatif Power BI, définissez une couleur d’arrière-plan d’état personnalisé de *#FFFFFF* (blanc).</span><span class="sxs-lookup"><span data-stu-id="9e7f6-161">If you want the background of the report to blend with the background color of the Power BI FactBox control, set report background color to *#FFFFFF* (white).</span></span> 

> [!TIP]
> <span data-ttu-id="9e7f6-162">Utilisez le fichier de thème [!INCLUDE [prod_short](includes/prod_short.md)] pour créer des rapports avec le même style de couleur que les applications [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="9e7f6-162">Use the [!INCLUDE [prod_short](includes/prod_short.md)] theme file to build reports with the same color styling as the [!INCLUDE [prod_short](includes/prod_short.md)] apps.</span></span> <span data-ttu-id="9e7f6-163">Pour plus d’informations, consultez [Utilisation du thème de l’état [!INCLUDE [prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-powerbi.md#theme).</span><span class="sxs-lookup"><span data-stu-id="9e7f6-163">For more information, see [Using the [!INCLUDE [prod_short](includes/prod_short.md)] report theme](across-how-use-financials-data-source-powerbi.md#theme).</span></span>

## <a name="reports-with-multiple-pages"></a><span data-ttu-id="9e7f6-164">États avec plusieurs pages</span><span class="sxs-lookup"><span data-stu-id="9e7f6-164">Reports with multiple pages</span></span>

<span data-ttu-id="9e7f6-165">Avec Power BI, vous pouvez créer un seul état avec plusieurs pages.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-165">With Power BI, you can create a single report with multiple pages.</span></span> <span data-ttu-id="9e7f6-166">Cependant, pour les états qui s’affichent avec des pages de liste, nous recommandons une seule page.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-166">However, for reports that will display with list pages, we don't recommend that they have more than one page.</span></span> <span data-ttu-id="9e7f6-167">Le Récapitulatif Power BI n’affiche que la première page de votre état.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-167">The Power BI FactBox will only show the first page of your report.</span></span>

## <a name="fixing-problems"></a><span data-ttu-id="9e7f6-168">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="9e7f6-168">Fixing problems</span></span>

<span data-ttu-id="9e7f6-169">Cette section fournit des instructions sur la façon de résoudre les problèmes que vous pourriez rencontrer en essayant d'afficher un état Power BI pour une page de liste dans [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="9e7f6-169">This section provides instructions about how to fix problems that you might run into when trying to view a Power BI report for a list page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

### <a name="you-cant-see-the-power-bi-factbox-on-a-list-page"></a><span data-ttu-id="9e7f6-170">Vous ne pouvez pas voir le Récapitulatif Power BI sur une page de liste</span><span class="sxs-lookup"><span data-stu-id="9e7f6-170">You can't see the Power BI FactBox on a list page</span></span>

<span data-ttu-id="9e7f6-171">Par défaut, le Récapitulatif Power BI est caché de la vue.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-171">By default, the Power BI FactBox is hidden from view.</span></span> <span data-ttu-id="9e7f6-172">Pour afficher le Récapitulatif sur une page, dans la barre d’action, sélectionnez **Actions** > **Afficher** > **Afficher/Masquer les états Power BI**.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-172">To show the FactBox on a page, from the action bar, select **Actions** > **Display** > **Show/Hide Power BI Reports**.</span></span>

### <a name="you-cant-see-the-report-in-the-select-report-pane"></a><span data-ttu-id="9e7f6-173">Vous ne pouvez pas voir l’état sur le volet Sélectionner un état</span><span class="sxs-lookup"><span data-stu-id="9e7f6-173">You can't see the report in the Select Report pane</span></span>

<span data-ttu-id="9e7f6-174">C’est probablement parce que le nom de l’état ne contient pas le nom de la page de liste affichée.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-174">It's probably because the report's name doesn't contain the name of the list page that's being shown.</span></span> <span data-ttu-id="9e7f6-175">Effacez le filtre pour obtenir la liste complète des états disponibles dans Power BI.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-175">Clear the filter to get a full list of Power BI reports available.</span></span>  

### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a><span data-ttu-id="9e7f6-176">L’état est chargé, mais vide, non filtré ou filtré incorrectement</span><span class="sxs-lookup"><span data-stu-id="9e7f6-176">Report is loaded but blank, not filtered, or filtered incorrectly</span></span>

<span data-ttu-id="9e7f6-177">Vérifiez que le filtre de l’état contient la bonne clé primaire.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-177">Verify that the report filter contains the right primary key.</span></span> <span data-ttu-id="9e7f6-178">Dans la plupart des cas, il s’agit du champ **N°**,</span><span class="sxs-lookup"><span data-stu-id="9e7f6-178">In most cases, this field is the **No.**</span></span> <span data-ttu-id="9e7f6-179">mais dans la table **Écriture comptable**, vous devez utiliser le champ **N° écriture**.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-179">field, but in the **G/L Entry** table, for example, you must use the **Entry No.** field.</span></span>

### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a><span data-ttu-id="9e7f6-180">L’état est chargé, mais il affiche une page à laquelle vous ne vous attendiez pas.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-180">Report is loaded, but it shows a page you didn't expect</span></span>

<span data-ttu-id="9e7f6-181">Vérifiez que la page que vous souhaitez afficher est la première page de votre état.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-181">Verify that the page you want displayed is the first page in your report.</span></span>  

### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a><span data-ttu-id="9e7f6-182">L’état apparaît avec des bordures grises non désirées, il est trop petit ou trop grand.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-182">Report appears with an unwanted gray boarder, or it's too small or too large</span></span>

<span data-ttu-id="9e7f6-183">Vérifiez que la taille de l’état est configurée sur 325 pixels x 310 pixels.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-183">Verify that the report size is set to 325 pixels x 310 pixels.</span></span> <span data-ttu-id="9e7f6-184">Enregistrez l’état, puis actualisez la page de liste.</span><span class="sxs-lookup"><span data-stu-id="9e7f6-184">Save the report, and then refresh the list page.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="9e7f6-185">Voir la formation associée sur [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="9e7f6-185">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="9e7f6-186">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e7f6-186">See Also</span></span>

[<span data-ttu-id="9e7f6-187">Activation de vos données métier pour Power BI</span><span class="sxs-lookup"><span data-stu-id="9e7f6-187">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
<span data-ttu-id="9e7f6-188">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)] comme source de données Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="9e7f6-188">[Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
[<span data-ttu-id="9e7f6-189">Préparation aux activités commerciales</span><span class="sxs-lookup"><span data-stu-id="9e7f6-189">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
<span data-ttu-id="9e7f6-190">[Configuration de [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="9e7f6-190">[Setting Up [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span></span>  
[<span data-ttu-id="9e7f6-191">Finances</span><span class="sxs-lookup"><span data-stu-id="9e7f6-191">Finance</span></span>](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]