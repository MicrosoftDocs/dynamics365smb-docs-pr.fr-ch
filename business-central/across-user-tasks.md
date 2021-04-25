---
title: Affectation et gestion des tâches
description: Découvrez comment attribuer des tâches aux utilisateurs, y compris votre comptable, dans Business Central, et comment vous choisissez et effectuez des tâches.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: tasks, work
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 71e9c93eede8b39561dc78ff61732273003ce8de
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786997"
---
# <a name="define-user-tasks"></a><span data-ttu-id="8ec5f-103">Définir les tâches utilisateur</span><span class="sxs-lookup"><span data-stu-id="8ec5f-103">Define User Tasks</span></span>

<span data-ttu-id="8ec5f-104">Dans [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez créer des tâches pour vous rappeler le travail à faire.</span><span class="sxs-lookup"><span data-stu-id="8ec5f-104">In [!INCLUDE[prod_short](includes/prod_short.md)], you can create tasks to remind you of work to be done.</span></span> <span data-ttu-id="8ec5f-105">Vous pouvez créer des tâches pour vous-même, mais vous pouvez également affecter des tâches à d’autres personne ou avoir une tâche affectée à vous-même par une autre personne de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8ec5f-105">You can create tasks for yourself, but you can also assign tasks to others or be assigned a task by someone else in your organization.</span></span>  

## <a name="managing-user-tasks"></a><span data-ttu-id="8ec5f-106">Gestion des tâches utilisateur</span><span class="sxs-lookup"><span data-stu-id="8ec5f-106">Managing User Tasks</span></span>

<span data-ttu-id="8ec5f-107">La page **Tâches utilisateur** affiche toutes les tâches, et vous pouvez facilement créer et affecter de nouvelles tâches.</span><span class="sxs-lookup"><span data-stu-id="8ec5f-107">The **User Tasks** page shows all tasks, and you can easily create and assign new tasks.</span></span> <span data-ttu-id="8ec5f-108">Lorsque vous créez une tâche, vous pouvez spécifier la date de début et la date d’échéance, et vous pouvez ajouter un lien vers la page ou l’état dans [!INCLUDE[prod_short](includes/prod_short.md)] où l’utilisateur doit effectuer le travail.</span><span class="sxs-lookup"><span data-stu-id="8ec5f-108">When you create a task, you can specify the start date and due date, and you can add a link to the page or report in [!INCLUDE[prod_short](includes/prod_short.md)] where the user must do the work.</span></span>  

<span data-ttu-id="8ec5f-109">Par exemple, vous pouvez créer une tâche pour vous-même ou un collège pour afficher toutes les factures vente enregistrées.</span><span class="sxs-lookup"><span data-stu-id="8ec5f-109">For example, you can create a task for yourself or a coworker to view all posted sales invoices.</span></span> <span data-ttu-id="8ec5f-110">Dans ce cas, vous liez la tâche à la page 143, **Factures vente enregistrées**.</span><span class="sxs-lookup"><span data-stu-id="8ec5f-110">In that case, you link the task to page 143, **Posted Sales Invoices**.</span></span> <span data-ttu-id="8ec5f-111">Dans la capture d’écran suivante, quelqu’un crée une tâche pour MeganB pour consulter les factures vente enregistrées.</span><span class="sxs-lookup"><span data-stu-id="8ec5f-111">In the following screenshot, someone is creating a task for MeganB to review the posted sales invoices.</span></span>  

:::image type="content" source="media/across-user-tasks/sample-user-task.png" alt-text="Exemple de tâche utilisateur":::

> [!TIP]  
> <span data-ttu-id="8ec5f-113">Utilisez la recherche dans le champ **Page**, puis utilisez le champ **Rechercher** pour trouver la page souhaitée.</span><span class="sxs-lookup"><span data-stu-id="8ec5f-113">Use the look-up in the **Page** field and then use the **Search** field to find the page that you want.</span></span>  
>
> <span data-ttu-id="8ec5f-114">Vous pouvez créer un lien vers n’importe quelle page, mais vous ne pouvez pas créer de lien vers des écritures individuelles. La description doit donc être aussi explicite que possible, par exemple en écrivant « Veuillez consulter le numéro de client</span><span class="sxs-lookup"><span data-stu-id="8ec5f-114">You can link to any page, but you cannot link to individual entries, so make the description as explicit as possible, such as writing "Please take a look at customer no.</span></span> <span data-ttu-id="8ec5f-115">10000 et vérifier qu’il n’a pas d’impayés. »</span><span class="sxs-lookup"><span data-stu-id="8ec5f-115">10000 and make sure they don't have overdue payments.".</span></span>

### <a name="picking-up-user-tasks"></a><span data-ttu-id="8ec5f-116">Sélectionner des tâches d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="8ec5f-116">Picking Up User Tasks</span></span>

<span data-ttu-id="8ec5f-117">Dans les Tableaux de bord Gestionnaire d’activité, Aide-comptable et Comptable, une mosaïque affiche les tâches en attente affectées à ces utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="8ec5f-117">In the Business Manager, Bookkeeper, and Accountant Role Centers, a tile shows pending tasks that are assigned to that user.</span></span> <span data-ttu-id="8ec5f-118">Pour sélectionner une tâche, il suffit de cliquer dessus dans la liste des tâches utilisateur en attente.</span><span class="sxs-lookup"><span data-stu-id="8ec5f-118">To pick up a task, simply choose it from the list of pending user tasks.</span></span> <span data-ttu-id="8ec5f-119">Dans le ruban, le lien **Atteindre l’élément de tâche** ouvre la page sur laquelle vous pouvez effectuer le travail.</span><span class="sxs-lookup"><span data-stu-id="8ec5f-119">In the ribbon, the link **Go to Task Item** opens the page where you can do the work.</span></span>  

<span data-ttu-id="8ec5f-120">Lorsque vous avez terminé une tâche, marquez-la simplement comme terminée.</span><span class="sxs-lookup"><span data-stu-id="8ec5f-120">When you have completed a task, simply mark it as completed.</span></span>  

### <a name="deleting-user-tasks"></a><span data-ttu-id="8ec5f-121">Suppression de tâches utilisateur</span><span class="sxs-lookup"><span data-stu-id="8ec5f-121">Deleting User Tasks</span></span>

<span data-ttu-id="8ec5f-122">Si vous souhaitez supprimer des tâches en bloc ou individuellement, vous pouvez utiliser l’état **Supprimer les tâches utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="8ec5f-122">If you want to bulk delete all or some user tasks, you can use the **Delete User Tasks** report.</span></span> <span data-ttu-id="8ec5f-123">Dans la page de demande, vous pouvez définir des filtres pour déterminer les tâches à supprimer.</span><span class="sxs-lookup"><span data-stu-id="8ec5f-123">In the request page, you can set filters to determine which tasks must be deleted.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8ec5f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ec5f-124">See Also</span></span>

[<span data-ttu-id="8ec5f-125">Recherche d’une page ou d’un état</span><span class="sxs-lookup"><span data-stu-id="8ec5f-125">Searching for a Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="8ec5f-126">[Expériences de comptable dans [!INCLUDE[prod_short](includes/prod_short.md)]](finance-accounting.md)</span><span class="sxs-lookup"><span data-stu-id="8ec5f-126">[Accountant Experiences in [!INCLUDE[prod_short](includes/prod_short.md)]](finance-accounting.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]