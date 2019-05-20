---
title: Paramétrer la maintenance des immobilisations| Microsoft Docs
description: Pour gérer les réparations et la maintenance des immobilisations, spécifiez les informations de maintenance générale, les codes du type de travail, et un compte de validation pour les coûts.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: ba01ccb88349a1f1943655949a36e2a21f3ae2de
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244522"
---
# <a name="set-up-fixed-asset-maintenance"></a><span data-ttu-id="53e0e-103">Configurer la maintenance d'une immobilisation</span><span class="sxs-lookup"><span data-stu-id="53e0e-103">Set Up Fixed Asset Maintenance</span></span>
<span data-ttu-id="53e0e-104">Pour gérer la maintenance des immobilisations, vous devez configurer tout d'abord certaines informations générales de maintenance, un compte de validation pour les coûts de maintenance et les codes de maintenance pour les types de travaux, tels que le service de routine ou la réparation.</span><span class="sxs-lookup"><span data-stu-id="53e0e-104">To manage fixed asset maintenance, you must first set up some general maintenance information, a posting account for maintenance costs, and maintenance codes for types of work, such as Routine Service or Repair.</span></span>

## <a name="to-set-up-general-maintenance-information"></a><span data-ttu-id="53e0e-105">Pour configurer les informations générales de maintenance</span><span class="sxs-lookup"><span data-stu-id="53e0e-105">To set up general maintenance information</span></span>
<span data-ttu-id="53e0e-106">Si vous configurez les champs pour la maintenance, vous pouvez valider des frais de maintenance à partir d'une feuille immobilisation.</span><span class="sxs-lookup"><span data-stu-id="53e0e-106">If you set up the fields for maintenance, you can post maintenance expenses from the fixed asset journal.</span></span>

1. <span data-ttu-id="53e0e-107">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Immobilisations**, puis choisissez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="53e0e-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="53e0e-108">Sélectionnez l'immobilisation pour laquelle vous souhaitez définir la couverture d'assurance, puis sélectionnez l'action **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="53e0e-108">Select the fixed asset that you to define insurance coverage for, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="53e0e-109">Sur le raccourci **Maintenance**, complétez les champs, comme nécessaire.</span><span class="sxs-lookup"><span data-stu-id="53e0e-109">On the **Maintenance** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a><span data-ttu-id="53e0e-110">Pour configurer des codes maintenance</span><span class="sxs-lookup"><span data-stu-id="53e0e-110">To set up maintenance codes</span></span>
<span data-ttu-id="53e0e-111">Lorsque vous validez des coûts de maintenance à partir d'une feuille comptabilité, vous renseignez le champ **Code maintenance** pour enregistrer le type de maintenance effectuée, telle qu'un service de routine ou une réparation.</span><span class="sxs-lookup"><span data-stu-id="53e0e-111">When you post maintenance costs from a general journal, you fill in the **Maintenance Code** field to record what kind of maintenance has been performed, such as routine service or repair.</span></span>

1. <span data-ttu-id="53e0e-112">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Maintenance**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="53e0e-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Maintenance**, and then choose the related link.</span></span>
2. <span data-ttu-id="53e0e-113">Sur la page **Maintenance**, configurez les codes pour les différents types de travaux de maintenance.</span><span class="sxs-lookup"><span data-stu-id="53e0e-113">On the **Maintenance** page, set up codes for different types of maintenance work.</span></span>

## <a name="to-set-up-maintenance-expense-accounts"></a><span data-ttu-id="53e0e-114">Pour configurer des comptes frais de maintenance</span><span class="sxs-lookup"><span data-stu-id="53e0e-114">To set up maintenance expense accounts</span></span>
<span data-ttu-id="53e0e-115">Pour valider les coûts de maintenance, vous devez tout d'abord saisir un numéro de compte sur la page **Groupes compta. immo**.</span><span class="sxs-lookup"><span data-stu-id="53e0e-115">To post maintenance costs, you must first enter an account number on the **FA Posting Groups** page.</span></span>

1. <span data-ttu-id="53e0e-116">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Groupes compta. immo.**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="53e0e-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **FA Posting Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="53e0e-117">Renseignez le champ **Compte frais maintenance** pour chaque groupe comptabilisation.</span><span class="sxs-lookup"><span data-stu-id="53e0e-117">Fill in the **Maintenance Expense Account** field for each posting group.</span></span>

> [!NOTE]  
>   <span data-ttu-id="53e0e-118">Pour définir que les coûts de maintenance sont attribués aux départements ou projets, configurez une clé d'allocation.</span><span class="sxs-lookup"><span data-stu-id="53e0e-118">To define that maintenance costs are allocated to departments or projects, set up an allocation keys.</span></span> <span data-ttu-id="53e0e-119">Pour en savoir plus, voir [Configurer des fonctionnalités d'immobilisations](fa-how-setup-general.md).</span><span class="sxs-lookup"><span data-stu-id="53e0e-119">For more information, see [Set Up General Fixed Assets Features](fa-how-setup-general.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="53e0e-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53e0e-120">See Also</span></span>
[<span data-ttu-id="53e0e-121">Paramétrage d'immobilisations</span><span class="sxs-lookup"><span data-stu-id="53e0e-121">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="53e0e-122">COMPTES D'IMMOBILISATIONS</span><span class="sxs-lookup"><span data-stu-id="53e0e-122">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="53e0e-123">Finances</span><span class="sxs-lookup"><span data-stu-id="53e0e-123">Finance</span></span>](finance.md)  
[<span data-ttu-id="53e0e-124">Mise en route</span><span class="sxs-lookup"><span data-stu-id="53e0e-124">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="53e0e-125">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="53e0e-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
