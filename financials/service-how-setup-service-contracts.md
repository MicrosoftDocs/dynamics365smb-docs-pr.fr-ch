---
title: Configurer des contrats de service | Microsoft Docs
description: "Découvrez comment configurer des contrats de service."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 203f6ef7f156bdccaa491fdac761711fd32c317e
ms.contentlocale: fr-ch
ms.lasthandoff: 12/14/2017

---

# <a name="how-to-set-up-service-contracts"></a><span data-ttu-id="8f9bc-103">Procédure : configurer des contrats de service</span><span class="sxs-lookup"><span data-stu-id="8f9bc-103">How to: Set Up Service Contracts</span></span>
<span data-ttu-id="8f9bc-104">Avant de pouvoir utiliser les contrats, vous devez définir les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="8f9bc-104">Before you can work with contracts, you must set up the following:</span></span> 

* <span data-ttu-id="8f9bc-105">**Groupes contrats de service** : regroupent les contrats de service liés, quelle que soit la nature de cette relation.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-105">**Service contract groups**, which gather service contracts that are related in some way.</span></span>
* <span data-ttu-id="8f9bc-106">**Groupes comptes contrat de service** : permettent de regrouper les comptes contrat de service pour les factures service créées pour les contrats de service.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-106">**Service contract account groups**, which are used to group the service contract accounts together for service invoices created for service contracts.</span></span> <span data-ttu-id="8f9bc-107">Vous affectez ces groupes aux contrats de service.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-107">You assign these groups to service contracts.</span></span>  
* <span data-ttu-id="8f9bc-108">**Modèles contrat** : définissent les présentations des contrats incluant les détails de contrat de service les plus couramment utilisés.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-108">**Contract templates** that define contract layouts of contracts that include the most commonly used service contract details.</span></span> <span data-ttu-id="8f9bc-109">Vous pouvez créer des devis contrat de service à l'aide de modèles.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-109">When you create service contract quotes, you can create them by using templates.</span></span> <span data-ttu-id="8f9bc-110">Lorsque vous créez un devis contrat, les champs contiennent automatiquement la valeur des champs du modèle.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-110">When you create a contract quote, the fields automatically contain the contents of the template fields.</span></span>
* <span data-ttu-id="8f9bc-111">**Modèles client** : permettent de créer des devis pour les contacts ou les clients potentiels qui ne sont pas enregistrés comme clients dans [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8f9bc-111">**Customer templates** that let you create quotes for contacts or potential customers who are not registered as customers in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-set-up-a-service-contract-group"></a><span data-ttu-id="8f9bc-112">Pour configurer un groupe de contrats de service</span><span class="sxs-lookup"><span data-stu-id="8f9bc-112">To set up a service contract group</span></span>  
1. <span data-ttu-id="8f9bc-113">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Groupes contrats de service**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Contract Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8f9bc-114">Renseignez les champs selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="8f9bc-115">Activez la case à cocher **Remise sur cdes contrat seulement** si vous souhaitez que les remises contrat ou service ne soient valides que pour les commandes contrat de service, tels que de maintenance.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-115">Choose the **Disc. on Contr. Orders Only** check box if you want contract or service discounts to be valid only for contract service orders, such as maintenance.</span></span>  

## <a name="to-set-up-a-service-contract-account-group"></a><span data-ttu-id="8f9bc-116">Pour configurer un groupe comptes contrats de service</span><span class="sxs-lookup"><span data-stu-id="8f9bc-116">To set up a service contract account group</span></span>  
1. <span data-ttu-id="8f9bc-117">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Groupes comptes contrat serv.**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Serv. Contract Account Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8f9bc-118">Créez un groupe comptes contrat de service.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-118">Create a new service contract account group.</span></span>   
3. <span data-ttu-id="8f9bc-119">Renseignez les champs **Code** et **Désignation**.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-119">Fill in the **Code** and **Description** fields.</span></span> <span data-ttu-id="8f9bc-120">Ces champs décrivent le groupe compte service.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-120">These fields describe the service account group.</span></span>  
4. <span data-ttu-id="8f9bc-121">Renseignez le champ **Compte contrat non prépayé**, puis sélectionnez le numéro de compte général du compte non prépayé.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-121">Fill in the **Non-Prepaid Contract Acc.** field, choose general ledger account number for the non-prepaid account.</span></span>  
5. <span data-ttu-id="8f9bc-122">Dans le champ **Compte contrat non prépayé**, sélectionnez le numéro de compte général du compte non prépayé.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-122">In the **Prepaid Contract Acc.** field, choose the general ledger account number for the prepaid account.</span></span>  

## <a name="to-set-up-a-contract-template"></a><span data-ttu-id="8f9bc-123">Pour configurer un modèle de contrat</span><span class="sxs-lookup"><span data-stu-id="8f9bc-123">To set up a contract template</span></span>  
1. <span data-ttu-id="8f9bc-124">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Modèle contrat de service**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Contract Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8f9bc-125">Créez un modèle contrat de service.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-125">Create a new service contract template.</span></span>  
3. <span data-ttu-id="8f9bc-126">Dans le champ **N°**,</span><span class="sxs-lookup"><span data-stu-id="8f9bc-126">In the **No.**</span></span> <span data-ttu-id="8f9bc-127">saisissez le numéro du modèle de contrat.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-127">field, enter a number for the contract template.</span></span>  
  
     <span data-ttu-id="8f9bc-128">Si vous avez configuré une souche de numéros pour les modèles contrat dans la fenêtre **Paramètres Gestion des services**, vous pouvez appuyer sur la touche Entrée pour que le programme saisisse le numéro modèle contrat suivant.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-128">Alternatively, if you have set up number series for contract templates in the **Service Mgt. Setup** window, you can press the Enter key to enter the next available contract template number.</span></span> <span data-ttu-id="8f9bc-129">Renseignez les autres champs, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-129">Fill in the other fields if appropriate.</span></span>  
  
4. <span data-ttu-id="8f9bc-130">Dans le raccourci **Facture**, renseignez les champs **Code gpe cptes contrat serv.**, **Période de facturation**, etc.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-130">On the **Invoice** FastTab, fill in the **Serv. Contract Acc. Group Code** field, the **Invoice Period**, and so on.</span></span> <span data-ttu-id="8f9bc-131">Renseignez les autres champs, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-131">Fill in the other fields if appropriate.</span></span>  
5. <span data-ttu-id="8f9bc-132">Sélectionnez l'action **Remises service** pour ajouter des remises contrat.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-132">Choose the **Service Discounts** action to add contract discounts.</span></span>  

## <a name="to-set-up-a-customer-template"></a><span data-ttu-id="8f9bc-133">Pour configurer un modèle client</span><span class="sxs-lookup"><span data-stu-id="8f9bc-133">To set up a customer template</span></span>  
1. <span data-ttu-id="8f9bc-134">Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), saisissez **Modèles client**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-134">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customer Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8f9bc-135">Créez une fiche modèle client.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-135">Create a new customer template card.</span></span>  
3. <span data-ttu-id="8f9bc-136">Sur le raccourci **Général**, tapez un code et une description pour le modèle client respectivement dans les champs **Code** et **Désignation**.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-136">On the **General** FastTab, enter a code and a description for the customer template in the **Code** and **Description** fields respectively.</span></span> 
4. <span data-ttu-id="8f9bc-137">Pour définir les critères de recherche, renseignez les autres champs tels que **Code pays/région**, **Code secteur** et **Code langue**.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-137">To define search criteria, fill in the other fields, such as **Country/Region Code**, **Territory Code**, and **Language Code**.</span></span>  
5. <span data-ttu-id="8f9bc-138">Renseignez les champs **Groupe compta. marché** et **Groupe compta. client**.</span><span class="sxs-lookup"><span data-stu-id="8f9bc-138">Fill in the **Gen. Bus. Posting Group** and **Customer Posting Group** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8f9bc-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f9bc-139">See Also</span></span>
[<span data-ttu-id="8f9bc-140">Paramétrage de la gestion des services</span><span class="sxs-lookup"><span data-stu-id="8f9bc-140">Setting Up Service Management</span></span>](service-setup-service.md)
