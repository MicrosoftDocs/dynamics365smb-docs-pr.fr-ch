---
title: 'Procédure : travailler sur des tâches service | Microsoft Docs'
description: Après avoir créé une commande ou devis service, enregistré des lignes article de service, et affecté des ressources aux articles de service de la commande ou du devis, vous pouvez commencer la réparation et la maintenance des articles de service.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 973bc19e9d6e2efd28c56b0db70e4f53148f636e
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820744"
---
# <a name="work-on-service-tasks"></a><span data-ttu-id="22757-103">Travailler sur des tâches service</span><span class="sxs-lookup"><span data-stu-id="22757-103">Work on Service Tasks</span></span>
<span data-ttu-id="22757-104">Après avoir créé une commande ou devis service, enregistré des lignes article de service, et affecté des ressources aux articles de service de la commande ou du devis, vous pouvez commencer la réparation et la maintenance des articles de service.</span><span class="sxs-lookup"><span data-stu-id="22757-104">After you have created a service order or service quote, registered service item lines, and allocated resources to the service items in the order or quote, you can start repairing and maintaining the service items.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="22757-105">inclut une page **Tâches service** qui offre un aperçu de tous les articles de service nécessitant une attention particulière.</span><span class="sxs-lookup"><span data-stu-id="22757-105">features a **Service Tasks** page that gives an overview of all the service items that need attention.</span></span> <span data-ttu-id="22757-106">Considérez-le comme votre tableau de bord de service : où vous pouvez consulter les commandes en attente, recherchez et enregistrez les pièces de rechange et mettez votre stock à jour.</span><span class="sxs-lookup"><span data-stu-id="22757-106">Think of it as your service dashboard where you can see what orders are pending, look for and register spare parts, and keep your inventory up-to-date.</span></span>  

<span data-ttu-id="22757-107">Pour assurer le suivi des modifications et obtenir une vue graphique de vos activités de service, utilisez les outils de statistiques de [!INCLUDE[d365fin](includes/d365fin_md.md)] pour obtenir des diagrammes et analyses rapides générés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="22757-107">To track changes and get a graphical view of your service business, use [!INCLUDE[d365fin](includes/d365fin_md.md)] statistics tools for quick, automatically generated charting and analysis.</span></span>  

## <a name="to-work-on-a-service-task"></a><span data-ttu-id="22757-108">Pour travailler sur une tâche service</span><span class="sxs-lookup"><span data-stu-id="22757-108">To work on a service task</span></span>  
1. <span data-ttu-id="22757-109">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Tâches service**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="22757-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Tasks**, and then choose the related link.</span></span>
2. <span data-ttu-id="22757-110">Pour obtenir la liste des tâches service auxquelles une ressource ou un groupe de ressources est affecté, renseignez le champ **Filtre ressources** ou **Filtre groupe ressources** et appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="22757-110">If you want a list of service tasks a certain resource or resource group is allocated to, fill in the **Resource Filter** or **Resource Group Filter** field and press Enter.</span></span>  
3. <span data-ttu-id="22757-111">Pour obtenir la liste des tâches service ayant certaines dates réponse sur une période de temps donnée, renseignez le champ **Filtre date réponse** et appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="22757-111">If you want a list of service tasks with a certain response date or response dates within a certain time period, fill in the **Response Date Filter** field and press Enter.</span></span>  
4. <span data-ttu-id="22757-112">Pour obtenir la liste des tâches service ayant un certain état affectation ou réparation, renseignez le champ **Filtre état affectation** ou **Filtre code état réparation** et appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="22757-112">If you want a list of service tasks with a certain allocation status or repair status, fill in the **Allocation Status Filter** or **Repair Status Code Filter** field and press Enter.</span></span>  
5. <span data-ttu-id="22757-113">Sélectionnez la tâche service que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="22757-113">Select the service task you want to work on.</span></span> <span data-ttu-id="22757-114">Sous l'onglet **Naviguer**, dans le groupe **Tâches service**, choisissez **Feuille activité article**.</span><span class="sxs-lookup"><span data-stu-id="22757-114">On the **Navigate** tab, in the **Service Tasks** group, choose **Item Worksheet**.</span></span> <span data-ttu-id="22757-115">La page **Feuille activité article de service** s'ouvre.</span><span class="sxs-lookup"><span data-stu-id="22757-115">The **Service Item Worksheet** page opens.</span></span>  
6. <span data-ttu-id="22757-116">Enregistrez les textes standard, les pièces de rechange, les heures ressource et les coûts à l'aide des options correspondantes dans le champ **Type** : <Blank>, **Article**, **Ressource** et **Coût**.</span><span class="sxs-lookup"><span data-stu-id="22757-116">Register standard texts, spare parts, resource hours, and costs as appropriate using the corresponding options in the **Type** field:  <Blank>, **Item**, **Resource**, and **Cost**.</span></span>  
7. <span data-ttu-id="22757-117">Dans le champ **Statut réparation**, sélectionnez le statut approprié.</span><span class="sxs-lookup"><span data-stu-id="22757-117">In the **Repair Status** field, select the appropriate status.</span></span>  

   > [!NOTE]  
   >  <span data-ttu-id="22757-118">Renseignez le champ **État de la réparation** en indiquant le statut **Terminé** ou **Service en partie réalisé** si la maintenance de l'article de service est terminée ou si une autre ressource est encore en service.</span><span class="sxs-lookup"><span data-stu-id="22757-118">Fill in the **Repair Status** field with the **Finished** or **Partly Serviced** status if the service item has been completely serviced or another resource will continue servicing.</span></span> <span data-ttu-id="22757-119">Le programme sélectionne automatiquement le statut **Terminé** ou **Réaffectation nécessaire** pour l'écriture affectation correspondant à l'article de service.</span><span class="sxs-lookup"><span data-stu-id="22757-119">The **Finished** or **Reallocation Needed** status is specified automatically for the allocation entry corresponding to the service item.</span></span>  

## <a name="to-register-service-operations"></a><span data-ttu-id="22757-120">Pour enregistrer des opérations de service</span><span class="sxs-lookup"><span data-stu-id="22757-120">To register service operations</span></span>  
<span data-ttu-id="22757-121">Lors de l'exécution d'un service sur une commande service, vous pouvez enregistrer les détails spécifiant les articles utilisés, les coûts exposés et le temps passé.</span><span class="sxs-lookup"><span data-stu-id="22757-121">When performing a service on a service order, you can register the details specifying the items used, costs incurred, and the time spent.</span></span> <span data-ttu-id="22757-122">Les données que vous spécifiez sont stockées sur la page **Feuille activité article de service**.</span><span class="sxs-lookup"><span data-stu-id="22757-122">The data you specify is stored on the **Service Item Worksheet** page.</span></span> <span data-ttu-id="22757-123">Vous pouvez mettre à jour les données si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="22757-123">You can update the data when necessary.</span></span>

1. <span data-ttu-id="22757-124">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Commandes service**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="22757-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="22757-125">Ouvrez la commande service pour laquelle vous voulez enregistrer le service, puis choisissez la ligne article.</span><span class="sxs-lookup"><span data-stu-id="22757-125">Open the service order to register the service for, and choose the item line.</span></span>  
3. <span data-ttu-id="22757-126">Choisissez **Actions**, sélectionnez **Ligne**, puis **Feuille activité article de service**.</span><span class="sxs-lookup"><span data-stu-id="22757-126">Choose **Actions**, choose **Line**, and then choose **Service Item Worksheet.**</span></span>  
4. <span data-ttu-id="22757-127">Dans les lignes, spécifiez les articles utilisés, les coûts exposés et le temps passé au service.</span><span class="sxs-lookup"><span data-stu-id="22757-127">On the lines, specify the items used, costs incurred, and the time spent on the service.</span></span>  

   > [!NOTE]  
   >  <span data-ttu-id="22757-128">Vous pouvez également enregistrer un service directement dans les lignes service liées à la commande service.</span><span class="sxs-lookup"><span data-stu-id="22757-128">You can also register service directly on the service lines linked to the service order.</span></span>  

## <a name="to-register-spare-parts"></a><span data-ttu-id="22757-129">Pour enregistrer les pièces de rechange</span><span class="sxs-lookup"><span data-stu-id="22757-129">To register spare parts</span></span>  
<span data-ttu-id="22757-130">Lorsque vous travaillez sur des articles de service de commandes service, vous pouvez être amené à utiliser des pièces de rechange pour la maintenance.</span><span class="sxs-lookup"><span data-stu-id="22757-130">When working on service items in service orders, you may need to use spare parts for the service.</span></span> <span data-ttu-id="22757-131">La procédure suivante vous montre comment enregistrer les pièces de rechange utilisées sur la page **Feuille activité article de service**.</span><span class="sxs-lookup"><span data-stu-id="22757-131">The following procedure shows how to register the spare parts you use on the **Service Item Worksheet** page.</span></span>  

1. <span data-ttu-id="22757-132">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Tâches service**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="22757-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Tasks**, and then choose the related link.</span></span>
2. <span data-ttu-id="22757-133">Choisissez la ligne comprenant l'article de service approprié, puis sélectionnez l'action **Feuille activité article**.</span><span class="sxs-lookup"><span data-stu-id="22757-133">Choose the line that includes the relevant service item, and then choose the **Item Worksheet** action.</span></span>  
3. <span data-ttu-id="22757-134">Entrez une nouvelle ligne service.</span><span class="sxs-lookup"><span data-stu-id="22757-134">Enter a new service line.</span></span>  
4. <span data-ttu-id="22757-135">Dans le champ **Type**, choisissez **Article**.</span><span class="sxs-lookup"><span data-stu-id="22757-135">In the **Type** field, choose **Item**.</span></span>  
5. <span data-ttu-id="22757-136">Dans le champ **N°**,</span><span class="sxs-lookup"><span data-stu-id="22757-136">In the **No.**</span></span> <span data-ttu-id="22757-137">choisissez la pièce de rechange appropriée.</span><span class="sxs-lookup"><span data-stu-id="22757-137">field, choose the relevant spare part.</span></span>  
6. <span data-ttu-id="22757-138">Dans le champ **Quantité**, saisissez la quantité d'articles que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="22757-138">In the **Quantity** field, enter the quantity of items you want to use.</span></span>  

 <span data-ttu-id="22757-139">Vous pouvez utiliser une procédure similaire pour enregistrer les pièces de rechange dans la page **Lignes service** que vous pouvez ouvrir dans la page **Commande de service**.</span><span class="sxs-lookup"><span data-stu-id="22757-139">You can use a similar procedure to register the spare parts on the **Service Lines** page, which you can open from the **Service Order** page.</span></span>  

## <a name="to-register-spare-parts-from-a-service-order"></a><span data-ttu-id="22757-140">Pour enregistrer des pièces de rechange à partir d'une commande service</span><span class="sxs-lookup"><span data-stu-id="22757-140">To register spare parts from a service order</span></span>  
1. <span data-ttu-id="22757-141">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Commandes service**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="22757-141">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="22757-142">Ouvrez la commande service pour laquelle vous voulez enregistrer des pièces de rechange.</span><span class="sxs-lookup"><span data-stu-id="22757-142">Open the service order you want to register spare parts for.</span></span>  
3. <span data-ttu-id="22757-143">Choisissez la ligne comportant l'article de service approprié.</span><span class="sxs-lookup"><span data-stu-id="22757-143">Choose the line that includes the relevant service item.</span></span> <span data-ttu-id="22757-144">Sélectionnez **Actions**, **Commande**, puis **Lignes service**.</span><span class="sxs-lookup"><span data-stu-id="22757-144">Choose **Actions**, choose **Order**, and then choose **Service Lines**.</span></span>  
4. <span data-ttu-id="22757-145">Entrez une nouvelle ligne service.</span><span class="sxs-lookup"><span data-stu-id="22757-145">enter a new service line.</span></span>  

## <a name="to-replace-a-service-item-or-a-service-item-component"></a><span data-ttu-id="22757-146">Pour remplacer un article de service ou un composant article de service</span><span class="sxs-lookup"><span data-stu-id="22757-146">To replace a service item or a service item component</span></span>  
<span data-ttu-id="22757-147">La maintenance d'un article de service constitué de plusieurs composants peut nécessiter le remplacement d'un composant défectueux.</span><span class="sxs-lookup"><span data-stu-id="22757-147">When you service a service item that is composed of components, you may need to replace a faulty component with a new one.</span></span> <span data-ttu-id="22757-148">Chaque fois que vous saisissez une pièce de rechange pour un article de service constitué de plusieurs composants, vous pouvez remplacer un composant ou en créer un nouveau.</span><span class="sxs-lookup"><span data-stu-id="22757-148">Every time that you enter a spare part for a service item with components, you have the option of replacing a component or creating a new one.</span></span> <span data-ttu-id="22757-149">Le nouvel article n'est enregistré comme composant de l'article de service qu'après validation de cette ligne service ou de la commande service.</span><span class="sxs-lookup"><span data-stu-id="22757-149">The new item is not registered as a component of the service item until you post this service line or the service order.</span></span>

1. <span data-ttu-id="22757-150">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Tâches service**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="22757-150">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Tasks**, and then choose the related link.</span></span>
2. <span data-ttu-id="22757-151">Choisissez la ligne comprenant l'article de service, puis sélectionnez l'action **Feuille activité article**.</span><span class="sxs-lookup"><span data-stu-id="22757-151">Choose the line that includes the service item, and then choose the **Item Worksheet** action.</span></span>  
3. <span data-ttu-id="22757-152">Entrez une nouvelle ligne service.</span><span class="sxs-lookup"><span data-stu-id="22757-152">Enter a new service line.</span></span>  
4. <span data-ttu-id="22757-153">Dans le champ **Type**, choisissez **Article**.</span><span class="sxs-lookup"><span data-stu-id="22757-153">In the **Type** field, choose **Item**.</span></span>  
5. <span data-ttu-id="22757-154">Dans le champ **N°**,</span><span class="sxs-lookup"><span data-stu-id="22757-154">In the **No.**</span></span> <span data-ttu-id="22757-155">le champ, sélectionnez le composant à remplacer.</span><span class="sxs-lookup"><span data-stu-id="22757-155">field, choose the component to replace.</span></span>  
6. <span data-ttu-id="22757-156">Appuyez sur **Entrée**.</span><span class="sxs-lookup"><span data-stu-id="22757-156">Press **Enter**.</span></span> <span data-ttu-id="22757-157">La boîte de dialogue qui s'ouvre contient les trois champs suivants : **Remplacer composant**, **Nouveau composant** et **Ignorer**.</span><span class="sxs-lookup"><span data-stu-id="22757-157">A dialog box opens with three options: **Replace Component**, **New Component**, and **Ignore**.</span></span> <span data-ttu-id="22757-158">Le tableau suivant décrit les options.</span><span class="sxs-lookup"><span data-stu-id="22757-158">The following table describes the options.</span></span>  

    |<span data-ttu-id="22757-159">Option</span><span class="sxs-lookup"><span data-stu-id="22757-159">Option</span></span> | <span data-ttu-id="22757-160">Désignation</span><span class="sxs-lookup"><span data-stu-id="22757-160">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="22757-161">**Remplacement composant**</span><span class="sxs-lookup"><span data-stu-id="22757-161">**Replace Component**</span></span>|<span data-ttu-id="22757-162">Fait passer le statut du composant que vous remplacez sur inactif et le composant s'affiche dans la liste des composants remplacés de l'article de service.</span><span class="sxs-lookup"><span data-stu-id="22757-162">Changes the status of the component you are replacing to not active, and it will appear on the replaced component list for the service item.</span></span>|  
    |<span data-ttu-id="22757-163">**Nouveau composant**</span><span class="sxs-lookup"><span data-stu-id="22757-163">**New Component**</span></span>|<span data-ttu-id="22757-164">Insère le nouveau composant dans la liste des composants de l'article de service.</span><span class="sxs-lookup"><span data-stu-id="22757-164">Enters the new component in the component list of the service item.</span></span>|  
    |<span data-ttu-id="22757-165">**ignorer**</span><span class="sxs-lookup"><span data-stu-id="22757-165">**Ignore**</span></span>|<span data-ttu-id="22757-166">N'apporte aucune modification à la liste des composants de l'article de service.</span><span class="sxs-lookup"><span data-stu-id="22757-166">Does nothing to the component list of the service item.</span></span>|  

7. <span data-ttu-id="22757-167">Cliquez sur **Remplacer composant**.</span><span class="sxs-lookup"><span data-stu-id="22757-167">Choose **Replace Component**.</span></span>  
8. <span data-ttu-id="22757-168">Choisissez le composant à remplacer, puis choisissez **OK**.</span><span class="sxs-lookup"><span data-stu-id="22757-168">Choose the component to replace, and then choose **OK**.</span></span>  

## <a name="to-change-the-response-time-for-a-service-item-line"></a><span data-ttu-id="22757-169">Pour modifier le délai de réponse pour une ligne article de service</span><span class="sxs-lookup"><span data-stu-id="22757-169">To change the response time for a service item line</span></span>  
<span data-ttu-id="22757-170">Lorsque vous enregistrez des lignes article de service dans une commande ou un devis service, selon que l'article de service se trouve sur un contrat de service, le temps de réponse en heures est automatiquement saisi et la date et l'heure de réponse sont calculées en conséquence.</span><span class="sxs-lookup"><span data-stu-id="22757-170">When you register a service item line in a service order or quote, depending on whether the service item is on a service contract the response time in hours is automatically entered and the response date and time are calculated accordingly.</span></span> <span data-ttu-id="22757-171">Vous pouvez modifier le délai de réponse en heures, la date et le délai de réponse, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="22757-171">You can change the response time in hours and the response date and time if you need to.</span></span>  

1. <span data-ttu-id="22757-172">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Commandes service** ou **Devis de service**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="22757-172">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Orders** or **Service Quotes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="22757-173">Choisissez la commande ou le devis service pour ouvrir la fiche.</span><span class="sxs-lookup"><span data-stu-id="22757-173">Choose the service order or quote to open the card.</span></span>  
3. <span data-ttu-id="22757-174">Sur la ligne d'élément de service pour lequel vous souhaitez modifier le temps de réponse, dans le champ **Délai de réponse (heures)**, ou dans les champs **Date de réponse** et **Délai de réponse**, saisissez les nouvelles heures de réponse ou la date et le délai de réponse souhaités.</span><span class="sxs-lookup"><span data-stu-id="22757-174">On the service item line you want to change the response time for, either in the **Response Time (Hours)** field or in the **Response Date** and **Response Time** fields, enter the new response hours or response date and time.</span></span>  

## <a name="to-register-faultresolution-codes"></a><span data-ttu-id="22757-175">Pour enregistrer des codes panne/solution</span><span class="sxs-lookup"><span data-stu-id="22757-175">To register fault/resolution codes</span></span>  
<span data-ttu-id="22757-176">Après avoir réparé un article de service, vous pouvez enregistrer le code panne et le code solution de l'article en sélectionnant une combinaison à partir des relations codes panne/solution existantes.</span><span class="sxs-lookup"><span data-stu-id="22757-176">After repairing a service item, you can register both the fault code and the resolution code for the item by selecting a combination from the existing fault/resolution codes relationships.</span></span> <span data-ttu-id="22757-177">Les codes panne et solution s'affichent dans les champs correspondants de la page **Feuille activité article de service**.</span><span class="sxs-lookup"><span data-stu-id="22757-177">The fault and resolution codes will appear in the corresponding fields on the **Service Item Worksheet** page.</span></span> <span data-ttu-id="22757-178">Vous pouvez également enregistrer les codes sur cette page.</span><span class="sxs-lookup"><span data-stu-id="22757-178">You can also register the codes directly in this page.</span></span>  

1. <span data-ttu-id="22757-179">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Tâches service**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="22757-179">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Tasks**, and then choose the related link.</span></span>
2. <span data-ttu-id="22757-180">Choisissez la ligne comprenant l'article de service approprié, puis sélectionnez l'action **Feuille activité article**.</span><span class="sxs-lookup"><span data-stu-id="22757-180">Choose the line that includes the relevant service item, and then choose the **Item Worksheet** action.</span></span>  
3. <span data-ttu-id="22757-181">Sur la page **Feuille activité article de service**, sélectionnez **Relations codes panne/solution**.</span><span class="sxs-lookup"><span data-stu-id="22757-181">On the **Service Item Worksheet** page, choose **Fault/Resol. Codes Relationships**.</span></span> <span data-ttu-id="22757-182">La page **Relations codes panne/solution** s'ouvre.</span><span class="sxs-lookup"><span data-stu-id="22757-182">The **Fault/Resolution Codes Relationships** page opens.</span></span>  

  >  [!Note]
  >  <span data-ttu-id="22757-183">Des filtres sont automatiquement positionnés sur les relations affichées sur la page en copiant le groupe articles de service et les codes panne de la page **Feuille activité article de service**.</span><span class="sxs-lookup"><span data-stu-id="22757-183">Filters are set on the relationships that are shown on the page by copying the service item group and the fault codes from the **Service Item Worksheet** page.</span></span>  

4. <span data-ttu-id="22757-184">Renseignez la ligne complètement.</span><span class="sxs-lookup"><span data-stu-id="22757-184">Fill out the line.</span></span> <span data-ttu-id="22757-185">Choisissez la combinaison de codes panne/solution, puis choisissez **OK** pour la copier sur l'article de service.</span><span class="sxs-lookup"><span data-stu-id="22757-185">Choose the combination of fault and resolution codes, and then choose **OK** to copy it to the service item.</span></span> <span data-ttu-id="22757-186">Si une combinaison appropriée est introuvable, vous pouvez créer une combinaison sur la page.</span><span class="sxs-lookup"><span data-stu-id="22757-186">If an appropriate combination cannot be found, you can create a new combination on the page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="22757-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22757-187">See Also</span></span>  
<span data-ttu-id="22757-188">[Configurer le reporting panne](service-how-setup-fault-reporting.md)
[Statut affectation et statut réparation](service-allocation-status-and-repair-status.md)</span><span class="sxs-lookup"><span data-stu-id="22757-188">[Set Up Fault Reporting](service-how-setup-fault-reporting.md)
[Allocation Status and Repair Status](service-allocation-status-and-repair-status.md)</span></span>  
[<span data-ttu-id="22757-189">Validation de service</span><span class="sxs-lookup"><span data-stu-id="22757-189">Service Posting</span></span>](service-service-posting.md)  