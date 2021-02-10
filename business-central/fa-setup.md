---
title: Paramétrer les immobilisations| Microsoft Docs
description: En savoir plus sur la série de tâches que vous devez effectuer pour configurer les immobilisations, telles que les machines ou les bâtiments.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7a5230f26b3e0db8896125d1a8dbf2d8ff322777
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751170"
---
# <a name="setting-up-fixed-assets"></a><span data-ttu-id="dc652-103">Paramétrage d’immobilisations</span><span class="sxs-lookup"><span data-stu-id="dc652-103">Setting Up Fixed Assets</span></span>
<span data-ttu-id="dc652-104">Avant de pouvoir utiliser les immobilisations, vous devez définir les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="dc652-104">Before you can work with Fixed Assets, you need to define a few things:</span></span>  

* <span data-ttu-id="dc652-105">Comment assurer, maintenir et amortir les immobilisations.</span><span class="sxs-lookup"><span data-stu-id="dc652-105">How you insure, maintain, and depreciate fixed assets.</span></span>  
* <span data-ttu-id="dc652-106">La manière dont vous enregistrez les coûts et d’autres valeurs dans le grand livre.</span><span class="sxs-lookup"><span data-stu-id="dc652-106">How you record costs and other values in the general ledger.</span></span>  

<span data-ttu-id="dc652-107">Le tableau ci-dessous contient des liens vers des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="dc652-107">The table below has links to more information.</span></span> <span data-ttu-id="dc652-108">Après avoir défini ces éléments, vous pouvez démarrer diverses activités.</span><span class="sxs-lookup"><span data-stu-id="dc652-108">After you set those things up, you can start various activities.</span></span> <span data-ttu-id="dc652-109">Pour plus d’informations, reportez-vous à [Immobilisations](fa-manage.md).</span><span class="sxs-lookup"><span data-stu-id="dc652-109">For more information, see [Fixed Assets](fa-manage.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="dc652-110">Vous pouvez enregistrer les transactions immobilisation sur les pages **Feuille compta. immo.** ou **Feuille immo.**, selon que les transactions sont destinées pour des rapports financiers ou pour la gestion interne.</span><span class="sxs-lookup"><span data-stu-id="dc652-110">You can record fixed asset transactions in the **Fixed Asset G/L Journal** or **Fixed Asset Journal** pages, depending on whether the transactions are for financial reporting or for internal management.</span></span> <span data-ttu-id="dc652-111">L’aide pour les immobilisations décrit uniquement la procédure d’utilisation de la page **Feuille compta. immo.**.</span><span class="sxs-lookup"><span data-stu-id="dc652-111">Help for Fixed Assets only describes how to use the **Fixed Asset G/L Journal** page.</span></span>  

<span data-ttu-id="dc652-112">Lorsque vous activez une activité immobilisation dans la section **Intégration compta.** sur la page **Fiche loi d’amortissement**, la page **Feuille compta. immo.** sera utilisée pour valider les transactions pour l’activité.</span><span class="sxs-lookup"><span data-stu-id="dc652-112">When you enable a fixed asset activity in the **G/L Integration** section on the **Depreciation Book Card** page, the **Fixed Asset G/L Journal** page is used to post transactions for the activity.</span></span>

<span data-ttu-id="dc652-113">Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.</span><span class="sxs-lookup"><span data-stu-id="dc652-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

| <span data-ttu-id="dc652-114">Pour</span><span class="sxs-lookup"><span data-stu-id="dc652-114">To</span></span> | <span data-ttu-id="dc652-115">Voir</span><span class="sxs-lookup"><span data-stu-id="dc652-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="dc652-116">Configurer les comptes généraux par défaut, les clés de ventilation, les modèles feuille et les lots pour la validation des immobilisations et configurer les catégories et sous-catégories d’immobilisation, telles que Corporelles et Incorporelles.</span><span class="sxs-lookup"><span data-stu-id="dc652-116">Set up default G/L accounts, allocation keys, journal templates and batches for fixed asset posting, and set up fixed asset classes and subclasses, such as Tangible and Intangible.</span></span> |[<span data-ttu-id="dc652-117">Configurer des informations générales pour les immobilisations</span><span class="sxs-lookup"><span data-stu-id="dc652-117">Set Up General Fixed Assets Information</span></span>](fa-how-setup-general.md) |
| <span data-ttu-id="dc652-118">Créer des lois d’amortissement, définir différentes méthodes d’amortissement, procéder à l’intégration en comptabilité et activer la duplication d’écritures dans plusieurs lois d’amortissement.</span><span class="sxs-lookup"><span data-stu-id="dc652-118">Create depreciation books, define various depreciation methods, integrate with the general ledger, and enable duplication of entries in several depreciation books.</span></span> |[<span data-ttu-id="dc652-119">Configurer un amortissement immobilisation</span><span class="sxs-lookup"><span data-stu-id="dc652-119">Set Up Fixed Asset Depreciation</span></span>](fa-how-setup-depreciation.md) |
| <span data-ttu-id="dc652-120">Activer l’assurance des immobilisations, configurer les informations générales d’assurance, une fiche assurance par police et préparer les feuilles pour valider les coûts d’assurance.</span><span class="sxs-lookup"><span data-stu-id="dc652-120">Enable insurance of fixed assets, set up general insurance information, an insurance card per policy, and prepare journals to post insurance costs.</span></span> |[<span data-ttu-id="dc652-121">Configurer une assurance immobilisation</span><span class="sxs-lookup"><span data-stu-id="dc652-121">Set Up Fixed Asset Insurance</span></span>](fa-how-setup-insurance.md) |
| <span data-ttu-id="dc652-122">Activer la maintenance des immobilisations, configurer les informations générales propres à la maintenance, configurer les comptes de validation de la maintenance et définir les types de travaux de maintenance.</span><span class="sxs-lookup"><span data-stu-id="dc652-122">Enable maintenance of fixed assets, set up general maintenance information, set up maintenance posting accounts, and define types of maintenance work.</span></span> |[<span data-ttu-id="dc652-123">Configurer la maintenance d’une immobilisation</span><span class="sxs-lookup"><span data-stu-id="dc652-123">Set Up Fixed Asset Maintenance</span></span>](fa-how-setup-maintenance.md) |
| <span data-ttu-id="dc652-124">En savoir plus sur les différentes méthodes d’amortissement des immobilisations.</span><span class="sxs-lookup"><span data-stu-id="dc652-124">Learn about different fixed asset depreciation methods.</span></span> |[<span data-ttu-id="dc652-125">Méthodes d’amortissement</span><span class="sxs-lookup"><span data-stu-id="dc652-125">Depreciation Methods</span></span>](fa-depreciation-methods.md) |

## <a name="see-also"></a><span data-ttu-id="dc652-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc652-126">See Also</span></span>
[<span data-ttu-id="dc652-127">COMPTES D’IMMOBILISATIONS</span><span class="sxs-lookup"><span data-stu-id="dc652-127">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="dc652-128">Finances</span><span class="sxs-lookup"><span data-stu-id="dc652-128">Finance</span></span>](finance.md)  
[<span data-ttu-id="dc652-129">Mise en route</span><span class="sxs-lookup"><span data-stu-id="dc652-129">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="dc652-130">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dc652-130">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
