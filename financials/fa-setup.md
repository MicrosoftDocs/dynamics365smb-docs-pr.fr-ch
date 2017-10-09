---
title: "Paramétrer les immobilisations| Microsoft Docs"
description: "En savoir plus sur la série de tâches que vous devez effectuer pour configurer les immobilisations, telles que les machines ou les bâtiments."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 9dea8be0f5b0200f97082dc25dbaa2483ad6c735
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-fixed-assets"></a><span data-ttu-id="97d5f-103">Paramétrage d'immobilisations</span><span class="sxs-lookup"><span data-stu-id="97d5f-103">Setting Up Fixed Assets</span></span>
<span data-ttu-id="97d5f-104">Avant de pouvoir utiliser les immobilisations, vous devez définir les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="97d5f-104">Before you can work with Fixed Assets, you need to define a few things:</span></span>  

* <span data-ttu-id="97d5f-105">Comment assurer, maintenir et amortir les immobilisations.</span><span class="sxs-lookup"><span data-stu-id="97d5f-105">How you insure, maintain, and depreciate fixed assets.</span></span>  
* <span data-ttu-id="97d5f-106">La manière dont vous enregistrez les coûts et d'autres valeurs dans le grand livre.</span><span class="sxs-lookup"><span data-stu-id="97d5f-106">How you record costs and other values in the general ledger.</span></span>  

<span data-ttu-id="97d5f-107">Le tableau ci-dessous contient des liens vers des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="97d5f-107">The table below has links to more information.</span></span> <span data-ttu-id="97d5f-108">Après avoir défini ces éléments, vous pouvez démarrer diverses activités.</span><span class="sxs-lookup"><span data-stu-id="97d5f-108">After you set those things up, you can start various activities.</span></span> <span data-ttu-id="97d5f-109">Pour plus d'informations, reportez-vous à [Immobilisations](fa-manage.md).</span><span class="sxs-lookup"><span data-stu-id="97d5f-109">For more information, see [Fixed Assets](fa-manage.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="97d5f-110">Vous pouvez enregistrer les transactions immobilisation dans les fenêtres **Feuille compta. immo.** ou **Feuille immo.**, selon que les transactions sont destinées pour des rapports financiers ou pour la gestion interne.</span><span class="sxs-lookup"><span data-stu-id="97d5f-110">You can record fixed asset transactions in the **Fixed Asset G/L Journal** or **Fixed Asset Journal** windows, depending on whether the transactions are for financial reporting or for internal management.</span></span> <span data-ttu-id="97d5f-111">L'aide pour les immobilisations décrit uniquement la procédure d'utilisation de la fenêtre **Feuille compta. immo.**.</span><span class="sxs-lookup"><span data-stu-id="97d5f-111">Help for Fixed Assets only describes how to use the **Fixed Asset G/L Journal** window.</span></span>  

<span data-ttu-id="97d5f-112">Lorsque vous activez une activité immobilisation dans la section **Intégration compta.** de la fenêtre **Fiche loi d'amortissement**, la fenêtre **Feuille compta. immo.** sera utilisée pour valider les transactions pour l'activité.</span><span class="sxs-lookup"><span data-stu-id="97d5f-112">When you enable a fixed asset activity in the **G/L Integration** section in the **Depreciation Book Card** window, the **Fixed Asset G/L Journal** window is used to post transactions for the activity.</span></span>

> [!NOTE]  
>  <span data-ttu-id="97d5f-113">Cette fonctionnalité nécessite que l'expérience soit définie sur **Suite**.</span><span class="sxs-lookup"><span data-stu-id="97d5f-113">This functionality requires that the experience is set to **Suite**.</span></span> <span data-ttu-id="97d5f-114">Pour plus d'informations, voir [Personnalisation de votre expérience Financials](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="97d5f-114">For more information, see [Customizing Your Financials Experience](ui-experiences.md).</span></span>  

<span data-ttu-id="97d5f-115">Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.</span><span class="sxs-lookup"><span data-stu-id="97d5f-115">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

| <span data-ttu-id="97d5f-116">Pour</span><span class="sxs-lookup"><span data-stu-id="97d5f-116">To</span></span> | <span data-ttu-id="97d5f-117">Voir</span><span class="sxs-lookup"><span data-stu-id="97d5f-117">See</span></span> |
| --- | --- |
| <span data-ttu-id="97d5f-118">Configurer les comptes généraux par défaut, les clés de ventilation, les modèles feuille et les lots pour la validation des immobilisations et configurer les catégories et sous-catégories d'immobilisation, telles que Corporelles et Incorporelles.</span><span class="sxs-lookup"><span data-stu-id="97d5f-118">Set up default G/L accounts, allocation keys, journal templates and batches for fixed asset posting, and set up fixed asset classes and subclasses, such as Tangible and Intangible.</span></span> |[<span data-ttu-id="97d5f-119">Procédure : configurer des informations générales pour les immobilisations</span><span class="sxs-lookup"><span data-stu-id="97d5f-119">How to: Set Up General Fixed Assets Information</span></span>](fa-how-setup-general.md) |
| <span data-ttu-id="97d5f-120">Créer des lois d'amortissement, définir différentes méthodes d'amortissement, procéder à l'intégration en comptabilité et activer la duplication d'écritures dans plusieurs lois d'amortissement.</span><span class="sxs-lookup"><span data-stu-id="97d5f-120">Create depreciation books, define various depreciation methods, integrate with the general ledger, and enable duplication of entries in several depreciation books.</span></span> |[<span data-ttu-id="97d5f-121">Procédure : configurer un amortissement immobilisation</span><span class="sxs-lookup"><span data-stu-id="97d5f-121">How to: Set Up Fixed Asset Depreciation</span></span>](fa-how-setup-depreciation.md) |
| <span data-ttu-id="97d5f-122">Activer l'assurance des immobilisations, configurer les informations générales d'assurance, une fiche assurance par police et préparer les feuilles pour valider les coûts d'assurance.</span><span class="sxs-lookup"><span data-stu-id="97d5f-122">Enable insurance of fixed assets, set up general insurance information, an insurance card per policy, and prepare journals to post insurance costs.</span></span> |[<span data-ttu-id="97d5f-123">Procédure : configurer une assurance immobilisation</span><span class="sxs-lookup"><span data-stu-id="97d5f-123">How to: Set Up Fixed Asset Insurance</span></span>](fa-how-setup-insurance.md) |
| <span data-ttu-id="97d5f-124">Activer la maintenance des immobilisations, configurer les informations générales propres à la maintenance, configurer les comptes de validation de la maintenance et définir les types de travaux de maintenance.</span><span class="sxs-lookup"><span data-stu-id="97d5f-124">Enable maintenance of fixed assets, set up general maintenance information, set up maintenance posting accounts, and define types of maintenance work.</span></span> |[<span data-ttu-id="97d5f-125">Procédure : configurer une maintenance d'immobilisation</span><span class="sxs-lookup"><span data-stu-id="97d5f-125">How to: Set Up Fixed Asset Maintenance</span></span>](fa-how-setup-maintenance.md) |
| <span data-ttu-id="97d5f-126">En savoir plus sur les différentes méthodes d'amortissement des immobilisations.</span><span class="sxs-lookup"><span data-stu-id="97d5f-126">Learn about different fixed asset depreciation methods.</span></span> |[<span data-ttu-id="97d5f-127">Méthodes d'amortissement</span><span class="sxs-lookup"><span data-stu-id="97d5f-127">Depreciation Methods</span></span>](fa-depreciation-methods.md) |

## <a name="see-also"></a><span data-ttu-id="97d5f-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97d5f-128">See Also</span></span>
[<span data-ttu-id="97d5f-129">Immobilisations</span><span class="sxs-lookup"><span data-stu-id="97d5f-129">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="97d5f-130">Finances</span><span class="sxs-lookup"><span data-stu-id="97d5f-130">Finance</span></span>](finance.md)  
<span data-ttu-id="97d5f-131">[Bienvenue dans [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="97d5f-131">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="97d5f-132">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="97d5f-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

