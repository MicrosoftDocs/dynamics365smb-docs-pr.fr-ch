---
title: Configurer le reporting panne dans la Gestion des services | Microsoft Docs
description: Découvrez comment configurer les processus de reporting panne.
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
ms.openlocfilehash: 7c25c4858600d959024dcbdba2ce5d0f7e3ad4c8
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820836"
---
# <a name="set-up-fault-reporting"></a><span data-ttu-id="2fa05-103">Configurer le reporting panne</span><span class="sxs-lookup"><span data-stu-id="2fa05-103">Set Up Fault Reporting</span></span>
<span data-ttu-id="2fa05-104">Le reporting panne permet d'établir des normes d'enregistrement des informations de panne pour les articles de service.</span><span class="sxs-lookup"><span data-stu-id="2fa05-104">Fault reporting lets you establish standards for recording fault information for service items.</span></span> <span data-ttu-id="2fa05-105">Par exemple, vous pouvez spécifier la nature du problème, les symptômes visibles, le motif du problème et la solution pour le résoudre.</span><span class="sxs-lookup"><span data-stu-id="2fa05-105">For example, you can specify what the problem is, the symptoms you see, the reason for the problem, and how to resolve it.</span></span>  

<span data-ttu-id="2fa05-106">Les codes panne décrivent les pannes article de service courantes ou les actions effectuées au niveau des articles de service.</span><span class="sxs-lookup"><span data-stu-id="2fa05-106">Fault codes describe the typical service item faults or the actions taken on service items.</span></span> <span data-ttu-id="2fa05-107">En fonction du niveau de reporting panne de votre société, il peut être nécessaire de configurer les codes zone panne et symptôme avant les codes panne.</span><span class="sxs-lookup"><span data-stu-id="2fa05-107">Depending on the level of fault reporting in your company, you might need to set up fault area codes and symptom codes before you set up fault codes.</span></span> <span data-ttu-id="2fa05-108">Les zones panne décrivent les zones de pannes article de service.</span><span class="sxs-lookup"><span data-stu-id="2fa05-108">Fault areas descrive areas of service item faults.</span></span> <span data-ttu-id="2fa05-109">Les codes motif panne décrivent le motif des pannes article de service et, si nécessaire, indiquent si les remises garantie et contrat doivent être exclues.</span><span class="sxs-lookup"><span data-stu-id="2fa05-109">Fault reason codes describe the reason for service item faults and, if needed, whether to exclude warranty and contract discounts.</span></span> <span data-ttu-id="2fa05-110">Par exemple, vous pouvez être amené à exclure les remises garantie et contrat si le client est responsable de la panne de l'article de service.</span><span class="sxs-lookup"><span data-stu-id="2fa05-110">For example, you might want to exclude warranty and contract discounts if the customer was somehow responsible for the fault in the service item.</span></span> <span data-ttu-id="2fa05-111">Vous affectez des codes motif panne aux commandes service.</span><span class="sxs-lookup"><span data-stu-id="2fa05-111">You assign fault reason codes to service orders.</span></span> <span data-ttu-id="2fa05-112">Pour plus d'informations, voir [Travailler sur des tâches service](service-how-to-work-on-service-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="2fa05-112">For more information, see [Work on Service Tasks](service-how-to-work-on-service-tasks.md).</span></span>  

## <a name="to-specify-the-overall-level-of-fault-reporting-to-use"></a><span data-ttu-id="2fa05-113">Pour spécifier le niveau global du reporting panne à utiliser</span><span class="sxs-lookup"><span data-stu-id="2fa05-113">To specify the overall level of fault reporting to use</span></span>
1. <span data-ttu-id="2fa05-114">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Paramètres service**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="2fa05-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="2fa05-115">Dans le champ **Niveau reporting panne**, sélectionnez l'une des options décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2fa05-115">In the **Fault Reporting Level** field, choose one of the options described in the following table.</span></span>  

    |<span data-ttu-id="2fa05-116">**Niveau de panne**</span><span class="sxs-lookup"><span data-stu-id="2fa05-116">**Fault Level**</span></span>|<span data-ttu-id="2fa05-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="2fa05-117">**Description**</span></span>|  
    |------------|-------------|  
    |<span data-ttu-id="2fa05-118">Aucun</span><span class="sxs-lookup"><span data-stu-id="2fa05-118">None</span></span> | <span data-ttu-id="2fa05-119">Aucun code reporting n'est utilisé.</span><span class="sxs-lookup"><span data-stu-id="2fa05-119">No reporting codes are used.</span></span>|  
    |<span data-ttu-id="2fa05-120">Panne</span><span class="sxs-lookup"><span data-stu-id="2fa05-120">Fault</span></span> | <span data-ttu-id="2fa05-121">Les codes sont répertoriés dans la table **Codes panne**.</span><span class="sxs-lookup"><span data-stu-id="2fa05-121">Codes are listed in the **Fault Codes** table.</span></span> <span data-ttu-id="2fa05-122">Ils identifient les pannes d'articles de service ou les actions à effectuer sur ces dernières.</span><span class="sxs-lookup"><span data-stu-id="2fa05-122">These codes identify service item faults or actions to take on service items.</span></span> <span data-ttu-id="2fa05-123">Vous pouvez regrouper les codes associés en groupements **Code zone panne**.</span><span class="sxs-lookup"><span data-stu-id="2fa05-123">You can cluster related codes into **Fault Area Code** groupings.</span></span>|  
    |<span data-ttu-id="2fa05-124">Panne + Symptôme</span><span class="sxs-lookup"><span data-stu-id="2fa05-124">Fault + Symptom</span></span> | <span data-ttu-id="2fa05-125">Vous entrez une combinaison de codes dans les tables **Codes panne** et **Codes symptôme**.</span><span class="sxs-lookup"><span data-stu-id="2fa05-125">You provide a combination of codes in the **Fault Codes** and **Symptom Codes** tables.</span></span> <span data-ttu-id="2fa05-126">Les codes symptôme courants incluent des indicateurs qu'un client peut utiliser pour décrire un problème (bruit, qualité, etc).</span><span class="sxs-lookup"><span data-stu-id="2fa05-126">Typical symptom codes include indicators that a customer might use to describe a problem, such as a noise or a quality.</span></span>|  
    |<span data-ttu-id="2fa05-127">Panne + Symptôme + Zone.</span><span class="sxs-lookup"><span data-stu-id="2fa05-127">Fault + Symptom + Area</span></span> | <span data-ttu-id="2fa05-128">Vous utilisez les codes Panne, Symptôme et Zone panne dans le cadre de la mise en œuvre du système International Repair Coding System (IRIS).</span><span class="sxs-lookup"><span data-stu-id="2fa05-128">You use fault, symptom, and fault area codes as an implementation of the International Repair Coding System (IRIS).</span></span>|  

<span data-ttu-id="2fa05-129">Pour terminer la configuration du reporting panne, vous pouvez également spécifier les réparations ou solutions associées à une panne ou un défaut.</span><span class="sxs-lookup"><span data-stu-id="2fa05-129">To complete the setup of fault reporting, you can also specify what repairs or resolutions are associated with a fault or defect.</span></span> <span data-ttu-id="2fa05-130">Pour ce faire, utilisez la page **Relations codes panne/solution**, qui vous permet de configurer des combinaisons de codes pour le groupe d'articles de service de l'article de service à partir duquel vous accédez à la fenêtre, ainsi que le nombre d'occurrences de chacune d'elles.</span><span class="sxs-lookup"><span data-stu-id="2fa05-130">You set that up on the **Fault/Resolution Code Relationships** page, where you set up combinations of codes for the service item group of the service item from which you accessed the witndow and the number of occurrences for each one.</span></span>

## <a name="to-create-fault-and-resolution-code-relationships"></a><span data-ttu-id="2fa05-131">Pour créer des relations codes panne/solution</span><span class="sxs-lookup"><span data-stu-id="2fa05-131">To create fault and resolution code relationships</span></span>
<span data-ttu-id="2fa05-132"><!--this needs to go in a working with topic--> Pour pouvoir visualiser, lors de la maintenance des articles, les modes de réparation les plus courants se rapportant à des pannes article particulières, vous devez regrouper des informations sur les relations codes panne/solution.</span><span class="sxs-lookup"><span data-stu-id="2fa05-132"><!--this needs to go in a working with topic--> To be able to see the most common methods of repair for particular item faults when you are servicing the items, you need to build up information on fault/resolution codes relationships.</span></span> <span data-ttu-id="2fa05-133">Utilisez le traitement par lots **Insérer relations codes P/S** pour rechercher toutes les combinaisons de codes panne/solution dans des commandes service validées et les enregistrer dans la page **Relations codes panne/solution**.</span><span class="sxs-lookup"><span data-stu-id="2fa05-133">Use the **Insert Fault/Resol. Codes Relationships** batch job to find all the combination of fault and resolution codes in posted service orders and record them on the **Fault/Resol. Codes Relationships** page.</span></span>

1. <span data-ttu-id="2fa05-134">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Insérer relations codes P/S**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="2fa05-134">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Insert Fault/Resol. Codes Relationships**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2fa05-135">Saisissez des dates pour définir la période à inclure dans le traitement par lots.</span><span class="sxs-lookup"><span data-stu-id="2fa05-135">Enter dates to define the period you want to include in the batch job.</span></span>  
3. <span data-ttu-id="2fa05-136">Pour regrouper les relations par groupe d'articles de service, activez la case à cocher **Relations définies à partir des groupes articles de service**.</span><span class="sxs-lookup"><span data-stu-id="2fa05-136">To group the relationships by service item group, choose the **Relation Based on Service Item Group** check box.</span></span>  
4. <span data-ttu-id="2fa05-137">Pour conserver les enregistrements que vous avez déjà insérés manuellement sur la page **Relations codes panne/solution**, activez la case à cocher **Conserver enreg. insérés manuellement**.</span><span class="sxs-lookup"><span data-stu-id="2fa05-137">To retain the records that you have already inserted manually on the **Fault/Resol. Codes Relationships** page, choose the **Retain Manually Inserted Rec.** check box.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2fa05-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fa05-138">See Also</span></span>
[<span data-ttu-id="2fa05-139">Paramétrage de la gestion des services</span><span class="sxs-lookup"><span data-stu-id="2fa05-139">Setting Up Service Management</span></span>](service-setup-service.md)  
[<span data-ttu-id="2fa05-140">Gestion des services</span><span class="sxs-lookup"><span data-stu-id="2fa05-140">Service Management</span></span>](service-service.md)  