---
title: Paramétrer les feuilles de temps et leur approbation| Microsoft Docs
description: Vous paramétrez des feuilles de temps pour suivre le temps consacré aux projets et l'utilisation des ressources, vous aider à gérer des projets, à recruter du personnel, et à anticiper vos capacités
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 057497cfee69ed91c5d37828ea290749585f93d8
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820742"
---
# <a name="set-up-time-sheets"></a><span data-ttu-id="9b787-103">Paramétrer des feuilles de temps</span><span class="sxs-lookup"><span data-stu-id="9b787-103">Set Up Time Sheets</span></span>
<span data-ttu-id="9b787-104">Dans [!INCLUDE[d365fin](includes/d365fin_md.md)], les feuilles de temps gèrent l'enregistrement des heures sur une base hebdomadaire par incrément de sept jours.</span><span class="sxs-lookup"><span data-stu-id="9b787-104">Time sheets in [!INCLUDE[d365fin](includes/d365fin_md.md)] handle time registration in weekly increments of seven days.</span></span> <span data-ttu-id="9b787-105">Elles permettent de suivre le temps consacré à des projets, et vous pouvez les utiliser pour enregistrer les heures ressource.</span><span class="sxs-lookup"><span data-stu-id="9b787-105">You use them to track the time used on jobs, and you can use them to record simple resource time registration.</span></span> <span data-ttu-id="9b787-106">Avant de pouvoir utiliser des feuilles de temps, vous devez les configurer.</span><span class="sxs-lookup"><span data-stu-id="9b787-106">Before you can use time sheets, you must specify how you want them to be set up and configured.</span></span>

<span data-ttu-id="9b787-107">Une fois l'utilisation des feuilles de temps au sein de votre organisation configurée, vous pouvez indiquer si et comment les feuilles de temps sont approuvées.</span><span class="sxs-lookup"><span data-stu-id="9b787-107">After you have set up how your organization will use time sheets, you can specify if and how time sheets are approved.</span></span> <span data-ttu-id="9b787-108">Selon les besoins de votre organisation, vous pouvez désigner :</span><span class="sxs-lookup"><span data-stu-id="9b787-108">Depending on the needs of your organization, you can designate:</span></span>

* <span data-ttu-id="9b787-109">un ou plusieurs utilisateurs en tant qu'administrateur et approbateur de feuille de temps pour toutes les feuilles de temps ;</span><span class="sxs-lookup"><span data-stu-id="9b787-109">One or more users as the time sheet administrator and approver for all time sheets.</span></span>
* <span data-ttu-id="9b787-110">un approbateur de feuille de temps pour chaque ressource.</span><span class="sxs-lookup"><span data-stu-id="9b787-110">A time sheet approver for each resource.</span></span>

<span data-ttu-id="9b787-111">Lorsque vous créez des feuilles de temps, vous pouvez créer des feuilles de temps pour les ressources, les affecter aux lignes planning projet, et valider les lignes de feuille de temps.</span><span class="sxs-lookup"><span data-stu-id="9b787-111">When you have set up time sheets, you can create time sheets for resources, assign them to job planning lines, and post time sheet lines.</span></span> <span data-ttu-id="9b787-112">Pour plus d'informations, voir [Utiliser des feuilles de temps](projects-how-use-time-sheets.md).</span><span class="sxs-lookup"><span data-stu-id="9b787-112">For more information, see [Use Time Sheets](projects-how-use-time-sheets.md).</span></span>

## <a name="to-set-up-general-information-for-time-sheets"></a><span data-ttu-id="9b787-113">Pour configurer des informations générales pour les feuilles de temps</span><span class="sxs-lookup"><span data-stu-id="9b787-113">To set up general information for time sheets</span></span>
1. <span data-ttu-id="9b787-114">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres ressources**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="9b787-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resources Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9b787-115">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="9b787-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="9b787-116">Sélectionnez l'une des options suivantes pour le champ **Feuille de temps par approbation de projet**.</span><span class="sxs-lookup"><span data-stu-id="9b787-116">For the **Time Sheet by Job Approval** field, select one of the following options.</span></span>

| <span data-ttu-id="9b787-117">Option</span><span class="sxs-lookup"><span data-stu-id="9b787-117">Option</span></span> | <span data-ttu-id="9b787-118">Désignation</span><span class="sxs-lookup"><span data-stu-id="9b787-118">Description</span></span> |
| --- | --- |
| <span data-ttu-id="9b787-119">**Jamais**</span><span class="sxs-lookup"><span data-stu-id="9b787-119">**Never**</span></span> |<span data-ttu-id="9b787-120">L'utilisateur du champ **ID utilisateur de l'approbateur de la feuille de temps** de la fiche ressource approuve la feuille de temps.</span><span class="sxs-lookup"><span data-stu-id="9b787-120">The user in the **Time Sheet Approver User ID** field on the resource card approves the time sheet.</span></span> |
| <span data-ttu-id="9b787-121">**Toujours**</span><span class="sxs-lookup"><span data-stu-id="9b787-121">**Always**</span></span> |<span data-ttu-id="9b787-122">L'utilisateur du champ **Responsable** de la fiche projet approuve la feuille de temps.</span><span class="sxs-lookup"><span data-stu-id="9b787-122">The user in the **Person Responsible** field on the job card approves the time sheet.</span></span> |
| <span data-ttu-id="9b787-123">**Poste uniquement**</span><span class="sxs-lookup"><span data-stu-id="9b787-123">**Machine Only**</span></span> |<span data-ttu-id="9b787-124">Si la feuille de temps poste est liée à un projet, alors l'utilisateur du champ **Responsable** spécifié sur la fiche projet approuve la feuille de temps.</span><span class="sxs-lookup"><span data-stu-id="9b787-124">If the machine time sheet is linked with a job, then the user in the **Person Responsible** field on the job card approves the time sheet.</span></span> <span data-ttu-id="9b787-125">Si la feuille de temps poste est liée à une ressource, alors l'utilisateur du champ **ID utilisateur de l'approbateur de la feuille de temps** spécifié sur la fiche ressource approuve la feuille de temps.</span><span class="sxs-lookup"><span data-stu-id="9b787-125">If the machine time sheet is linked with a resource, then the user in the **Time Sheet Approver User ID** field on the resource card approves the time sheet.</span></span> |

## <a name="to-assign-a-time-sheet-administrator"></a><span data-ttu-id="9b787-126">Pour affecter un administrateur de feuille de temps</span><span class="sxs-lookup"><span data-stu-id="9b787-126">To assign a time sheet administrator</span></span>
1. <span data-ttu-id="9b787-127">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres utilisateur**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="9b787-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **User Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9b787-128">Ajoutez un nouvel utilisateur (si la personne que vous souhaitez désigner en tant qu'administrateur de feuille de temps ne figure pas dans la liste des utilisateurs).</span><span class="sxs-lookup"><span data-stu-id="9b787-128">Add a new user if the user list does not include the person who you want to be the time sheet administrator.</span></span> <span data-ttu-id="9b787-129">Pour plus d'informations, voir [Gestion des utilisateurs et des autorisations](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="9b787-129">For more information, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>
3. <span data-ttu-id="9b787-130">Sélectionnez l'utilisateur qui deviendra l'administrateur de feuille de temps et sélectionnez la case à cocher **Admin. feuille de temps**.</span><span class="sxs-lookup"><span data-stu-id="9b787-130">Select a user to be a time sheet administrator, and then select the **Time Sheet Admin.** check box.</span></span>  

> [!TIP]  
>   <span data-ttu-id="9b787-131">Il est recommandé de ne désigner qu'un seul utilisateur en tant qu'administrateur de feuille de temps dans une société.</span><span class="sxs-lookup"><span data-stu-id="9b787-131">It is recommended that you designate only one user to be the time sheet administrator for a company.</span></span> <span data-ttu-id="9b787-132">Dans la procédure suivante, vous devez configurer un propriétaire et un approbateur de feuille de temps et affecter l'approbateur à chaque ressource.</span><span class="sxs-lookup"><span data-stu-id="9b787-132">In the following procedure, you set up a time sheet owner and approver where the time sheet approver is assigned for each resource.</span></span>  

## <a name="to-assign-a-time-sheets-owner-and-approver"></a><span data-ttu-id="9b787-133">Pour affecter un propriétaire et un approbateur de feuille de temps</span><span class="sxs-lookup"><span data-stu-id="9b787-133">To assign a time sheets owner and approver</span></span>
1. <span data-ttu-id="9b787-134">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Ressources**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="9b787-134">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resources**, and then choose the related link.</span></span>
2. <span data-ttu-id="9b787-135">Sélectionnez la ressource pour laquelle vous souhaitez configurer la capacité d'utiliser des feuilles de temps, puis sélectionnez la case à cocher **Utiliser la feuille de temps**.</span><span class="sxs-lookup"><span data-stu-id="9b787-135">Select the resource for which you want to set up the ability to use time sheets, and then select the **Use Time Sheet** check box.</span></span>  
3. <span data-ttu-id="9b787-136">Entrez l'ID du propriétaire de la feuille de temps dans le champ **ID utilisateur du propriétaire de la feuille de temps**.</span><span class="sxs-lookup"><span data-stu-id="9b787-136">In the **Time Sheet Owner User ID** field, enter the ID of the owner of the time sheet.</span></span> <span data-ttu-id="9b787-137">Le propriétaire peut entrer le temps d'utilisation dans une feuille de temps et la soumettre pour approbation.</span><span class="sxs-lookup"><span data-stu-id="9b787-137">The owner can enter time usage on a time sheet and submit it for approval.</span></span> <span data-ttu-id="9b787-138">En règle générale, lorsque la ressource est une personne, cette personne est également le propriétaire.</span><span class="sxs-lookup"><span data-stu-id="9b787-138">In general, when the resource is a person, that person is also the owner.</span></span>  
4. <span data-ttu-id="9b787-139">Entrez l'ID de l'approbateur de la feuille de temps dans le champ **ID utilisateur de l'approbateur de la feuille de temps**.</span><span class="sxs-lookup"><span data-stu-id="9b787-139">In the **Time Sheet Approver User ID** field, enter the ID of the approver of the time sheet.</span></span> <span data-ttu-id="9b787-140">L'approbateur peut approuver, rejeter ou rouvrir une feuille de temps.</span><span class="sxs-lookup"><span data-stu-id="9b787-140">The approver can approve, reject, or reopen a time sheet.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="9b787-141">Vous ne pouvez pas modifier l'ID de l'approbateur de feuille de temps s'il existe des feuilles de temps qui n'ont pas encore été traitées et dont le statut est **Soumis** ou **En cours**.</span><span class="sxs-lookup"><span data-stu-id="9b787-141">You cannot change the ID of the time sheet approver if there are time sheets that have not yet been processed and have the status of **Submitted** or **Open**.</span></span>

## <a name="see-also"></a><span data-ttu-id="9b787-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b787-142">See Also</span></span>
[<span data-ttu-id="9b787-143">Configuration de la gestion de projet</span><span class="sxs-lookup"><span data-stu-id="9b787-143">Setting Up Project Management</span></span>](projects-setup-projects.md)  
[<span data-ttu-id="9b787-144">Gestion de projets</span><span class="sxs-lookup"><span data-stu-id="9b787-144">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="9b787-145">Finances</span><span class="sxs-lookup"><span data-stu-id="9b787-145">Finance</span></span>](finance.md)  
<span data-ttu-id="9b787-146">[Achats](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="9b787-146">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="9b787-147">[Ventes](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="9b787-147">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="9b787-148">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9b787-148">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  