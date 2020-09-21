---
title: Afficher les états Power BI personnalisés pour les données Business Central | Microsoft Docs
description: Vous pouvez utiliser des états Power BI pour obtenir des informations supplémentaires sur les données dans les listes.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 5d3acaf05952a61845eb8bb72b2556f2e54f8208
ms.sourcegitcommit: aeaa0dc64e54432a70c4b0e1faf325cd17d01389
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697713"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prodshort"></a><span data-ttu-id="52065-103">Création d’états Power BI pour afficher les données de liste dans [!INCLUDE[prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="52065-103">Creating Power BI Reports for Displaying List Data in [!INCLUDE[prodshort](includes/prodshort.md)]</span></span>

[!INCLUDE[prodlong](includes/prodlong.md)] <span data-ttu-id="52065-104">inclut un élément de contrôle Récapitulatif sur un certain nombre de pages Liste des clés fournissant des informations supplémentaires sur les données de la liste.</span><span class="sxs-lookup"><span data-stu-id="52065-104">includes a FactBox control element on a number of key list pages that provide additional insight into the data in the list.</span></span> <span data-ttu-id="52065-105">Lorsque vous vous déplacez entre les lignes de la liste, l’état est mis à jour et filtré pour l’écriture sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="52065-105">As you move between rows in the list, the report is updated and filtered for the selected entry.</span></span> <span data-ttu-id="52065-106">Vous pouvez créer des états personnalisés à afficher dans ce contrôle.</span><span class="sxs-lookup"><span data-stu-id="52065-106">You can create custom reports to display in this control.</span></span> <span data-ttu-id="52065-107">Cependant, il y a quelques règles à suivre pour s’assurer que les états fonctionnent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="52065-107">However, there are a few rules to follow to ensure that reports work as expected.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="52065-108">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="52065-108">Prerequisites</span></span>

- <span data-ttu-id="52065-109">Un compte Power BI.</span><span class="sxs-lookup"><span data-stu-id="52065-109">A Power BI account.</span></span>
- <span data-ttu-id="52065-110">Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="52065-110">Power BI Desktop.</span></span>

<span data-ttu-id="52065-111">Pour plus d’informations sur la mise en route, voir [Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] comme source de données Power BI](across-how-use-financials-data-source-powerbi.md).</span><span class="sxs-lookup"><span data-stu-id="52065-111">For more information about getting started, see [Using [!INCLUDE[d365fin](includes/d365fin_md.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).</span></span>

## <a name="defining-the-report-data-set"></a><span data-ttu-id="52065-112">Définition de l’ensemble de données d’état</span><span class="sxs-lookup"><span data-stu-id="52065-112">Defining the report data set</span></span>

<span data-ttu-id="52065-113">Spécifiez la source de données qui contient les données liées à la liste.</span><span class="sxs-lookup"><span data-stu-id="52065-113">Specify the data source that contains the data related to the list.</span></span> <span data-ttu-id="52065-114">Par exemple, pour créer un état pour la liste Ventes, assurez-vous que l’ensemble des données contient les informations liées aux ventes.</span><span class="sxs-lookup"><span data-stu-id="52065-114">For example, to create a report for the Sales List, ensure the data set contains information related to sales.</span></span>  

## <a name="defining-the-report-filter"></a><span data-ttu-id="52065-115">Définition du filtre d’état</span><span class="sxs-lookup"><span data-stu-id="52065-115">Defining the report filter</span></span>

<span data-ttu-id="52065-116">Pour mettre à jour les données de l’enregistrement sélectionné dans la liste, vous ajoutez un filtre à l’état.</span><span class="sxs-lookup"><span data-stu-id="52065-116">To make the data update to the selected record in the list, you add a filter to the report.</span></span> <span data-ttu-id="52065-117">Le filtre doit inclure un champ de la source de données utilisée comme *clé primaire*.</span><span class="sxs-lookup"><span data-stu-id="52065-117">The filter must include a field of the data source that's used as the *primary key*.</span></span> <span data-ttu-id="52065-118">Dans la plupart des cas, la clé primaire de la liste est **N°**</span><span class="sxs-lookup"><span data-stu-id="52065-118">In most cases, the primary key for a list is the **No.**</span></span> <span data-ttu-id="52065-119">.</span><span class="sxs-lookup"><span data-stu-id="52065-119">field.</span></span>

<span data-ttu-id="52065-120">Pour définir un filtre pour l'état, sélectionnez la clé primaire dans la liste des champs disponibles, puis faites glisser ce champ dans la section **Filtre d'état**.</span><span class="sxs-lookup"><span data-stu-id="52065-120">To define a filter for the report, select the primary key from the list of available fields, and then drag and drop that field into the **Report Filter** section.</span></span> <span data-ttu-id="52065-121">Le filtre doit être un filtre d’état de base.</span><span class="sxs-lookup"><span data-stu-id="52065-121">The filter must be basic report filter.</span></span> <span data-ttu-id="52065-122">Il ne peut pas s’agir d’un filtre de page, visuel ou avancé.</span><span class="sxs-lookup"><span data-stu-id="52065-122">It can't be page, visual, or advanced filter.</span></span> 

![Définition du filtre d'état pour l'état Activités Facture vente](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter.png)

## <a name="setting-the-report-size-and-color"></a><span data-ttu-id="52065-124">Définition de la taille et de la couleur de l’état</span><span class="sxs-lookup"><span data-stu-id="52065-124">Setting the report size and color</span></span>

<span data-ttu-id="52065-125">La taille de l'état doit être configurée sur 325 pixels par 310 pixels.</span><span class="sxs-lookup"><span data-stu-id="52065-125">The size of the report must be set to 325 pixels by 310 pixels.</span></span> <span data-ttu-id="52065-126">Cette taille offre une mise à l’échelle appropriée de l’état dans l’espace disponible du contrôle Récapitulatif Power BI dans [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="52065-126">This size provides the proper scaling of the report in the available space of the Power BI FactBox control in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="52065-127">Pour définir la taille de l'état, placez le focus en dehors de la zone de présentation d'état, puis choisissez l'icône en forme de rouleau de peinture.</span><span class="sxs-lookup"><span data-stu-id="52065-127">To define the size of the report, place focus outside of the report layout area, and then choose the paint roller icon.</span></span>

![Définition de la largeur et de la hauteur de l'état pour l'état Activités Facture vente](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing.png)

<span data-ttu-id="52065-129">Vous pouvez modifier la largeur et la hauteur de l'état en choisissant **Personnalisé** dans le champ **Type**.</span><span class="sxs-lookup"><span data-stu-id="52065-129">You can change the width and height of the report by choosing **Custom** in the **Type** field.</span></span>

<span data-ttu-id="52065-130">Si vous souhaitez que l’arrière-plan de l’état se fonde avec la couleur de l’arrière-plan du contrôle Récapitulatif Power BI, définissez une couleur d’arrière-plan d’état personnalisé de *#FFFFFF*.</span><span class="sxs-lookup"><span data-stu-id="52065-130">If you want the background of the report to blend with the background color of the Power BI FactBox control, set report background color to *#FFFFFF*.</span></span> 

## <a name="using-reports-with-multiple-pages"></a><span data-ttu-id="52065-131">Utilisation des états avec plusieurs pages</span><span class="sxs-lookup"><span data-stu-id="52065-131">Using reports with multiple pages</span></span>

<span data-ttu-id="52065-132">Avec Power BI, vous pouvez créer un seul état avec plusieurs pages.</span><span class="sxs-lookup"><span data-stu-id="52065-132">With Power BI, you can create a single report with multiple pages.</span></span> <span data-ttu-id="52065-133">Cependant, pour les états qui s’affichent avec des pages de liste, nous recommandons une seule page.</span><span class="sxs-lookup"><span data-stu-id="52065-133">However, for reports that will display with list pages, we don't recommend that they have more than one page.</span></span> <span data-ttu-id="52065-134">Le Récapitulatif Power BI n’affiche que la première page de votre état.</span><span class="sxs-lookup"><span data-stu-id="52065-134">The Power BI FactBox will only show the first page of your report.</span></span>

## <a name="naming-the-report"></a><span data-ttu-id="52065-135">Définition du nom de l’état</span><span class="sxs-lookup"><span data-stu-id="52065-135">Naming the report</span></span>

<span data-ttu-id="52065-136">Donnez à l’état un nom contenant le nom de la page de liste associée à l’état.</span><span class="sxs-lookup"><span data-stu-id="52065-136">Give the report a name that contains the name of the list page associated with the report.</span></span> <span data-ttu-id="52065-137">Par exemple, si l’état concerne la page de liste **Fournisseur**, incluez le mot *fournisseur* quelque part dans le nom.</span><span class="sxs-lookup"><span data-stu-id="52065-137">For example, if the report is for the **Vendor** list page, include the word *vendor* somewhere in the name.</span></span>  

<span data-ttu-id="52065-138">Cette convention de désignation de nom n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="52065-138">This naming convention isn't a requirement.</span></span> <span data-ttu-id="52065-139">Cependant, il permet de sélectionner plus rapidement des états dans [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="52065-139">However, it makes selecting reports in [!INCLUDE[d365fin](includes/d365fin_md.md)] quicker.</span></span> <span data-ttu-id="52065-140">Lorsque la page de sélection de l’état s’ouvre à partir d’une page de liste, elle est automatiquement filtrée en fonction du nom de la page.</span><span class="sxs-lookup"><span data-stu-id="52065-140">When the report selection page opens from a list page, it's automatically filtered based on the page name.</span></span> <span data-ttu-id="52065-141">Ce filtrage est effectué pour limiter les états affichés.</span><span class="sxs-lookup"><span data-stu-id="52065-141">This filtering is done to limit the reports that are displayed.</span></span> <span data-ttu-id="52065-142">Vous pouvez aussi effacer le filtre pour obtenir la liste complète des états disponibles dans Power BI.</span><span class="sxs-lookup"><span data-stu-id="52065-142">Users can clear the filter to get a full list of reports available in Power BI.</span></span>  

## <a name="fixing-problems"></a><span data-ttu-id="52065-143">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="52065-143">Fixing problems</span></span>

<span data-ttu-id="52065-144">Cette section fournit une solution de rechange pour les problèmes les plus courants qui apparaissent lorsque vous créez l’état Power BI.</span><span class="sxs-lookup"><span data-stu-id="52065-144">This section provides a workaround for the most typical problems that can occur when you create the Power BI report.</span></span>  

#### <a name="you-cant-see-a-report-on-the-select-report-page"></a><span data-ttu-id="52065-145">Vous ne pouvez pas voir d’état sur la page Sélectionner un état.</span><span class="sxs-lookup"><span data-stu-id="52065-145">You can't see a report on the Select Report page</span></span>

<span data-ttu-id="52065-146">C’est probablement parce que le nom de l’état ne contient pas le nom de la page de liste.</span><span class="sxs-lookup"><span data-stu-id="52065-146">It's probably because the report's name doesn't contain the name of the list page.</span></span> <span data-ttu-id="52065-147">Effacez le filtre pour obtenir la liste complète des états disponibles dans Power BI.</span><span class="sxs-lookup"><span data-stu-id="52065-147">Clear the filter to get a full list of Power BI reports available.</span></span>  

#### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a><span data-ttu-id="52065-148">L’état est chargé, mais vide, non filtré ou filtré incorrectement.</span><span class="sxs-lookup"><span data-stu-id="52065-148">Report is loaded but blank, not filtered or filtered incorrectly</span></span>

<span data-ttu-id="52065-149">Vérifiez que le filtre de l’état contient la bonne clé primaire.</span><span class="sxs-lookup"><span data-stu-id="52065-149">Verify that the report filter contains the right primary key.</span></span> <span data-ttu-id="52065-150">Dans la plupart des cas, il s’agit du champ **N°**,</span><span class="sxs-lookup"><span data-stu-id="52065-150">In most cases, this field is the **No.**</span></span> <span data-ttu-id="52065-151">mais dans la table **Écriture comptable**, vous devez utiliser le champ **N° écriture**.</span><span class="sxs-lookup"><span data-stu-id="52065-151">field, but in the **G/L Entry** table, for example, you must use the **Entry No.** field.</span></span>

#### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a><span data-ttu-id="52065-152">L’état est chargé, mais il affiche une page à laquelle vous ne vous attendiez pas.</span><span class="sxs-lookup"><span data-stu-id="52065-152">Report is loaded, but it shows a page you didn't expect</span></span>

<span data-ttu-id="52065-153">Vérifiez que la page que vous souhaitez afficher est la première page de votre état.</span><span class="sxs-lookup"><span data-stu-id="52065-153">Verify that the page you want displayed is the first page in your report.</span></span>  

#### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a><span data-ttu-id="52065-154">L’état apparaît avec des bordures grises non désirées, il est trop petit ou trop grand.</span><span class="sxs-lookup"><span data-stu-id="52065-154">Report appears with an unwanted gray boarder, or it's too small or too large</span></span>

<span data-ttu-id="52065-155">Vérifiez que la taille de l'état est configurée sur 325 pixels x 310 pixels.</span><span class="sxs-lookup"><span data-stu-id="52065-155">Verify that the report size is set to 325 pixels x 310 pixels.</span></span> <span data-ttu-id="52065-156">Enregistrez l'état, puis actualisez la page de liste.</span><span class="sxs-lookup"><span data-stu-id="52065-156">Save the report, and then refresh the list page.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="52065-157">Voir la formation associée sur [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="52065-157">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="52065-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52065-158">See Also</span></span>

[<span data-ttu-id="52065-159">Activation de vos données métier pour Power BI</span><span class="sxs-lookup"><span data-stu-id="52065-159">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
<span data-ttu-id="52065-160">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] comme source de données Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="52065-160">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
[<span data-ttu-id="52065-161">Mise en route</span><span class="sxs-lookup"><span data-stu-id="52065-161">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="52065-162">[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="52065-162">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="52065-163">Finances</span><span class="sxs-lookup"><span data-stu-id="52065-163">Finance</span></span>](finance.md)  
