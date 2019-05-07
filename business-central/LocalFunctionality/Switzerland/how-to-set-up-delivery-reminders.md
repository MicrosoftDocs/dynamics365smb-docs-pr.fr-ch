---
title: 'Procédure : Paramétrer des relances livraison'
description: Dans Business Central, vous pouvez utiliser des relances livraison pour rappeler aux fournisseurs les livraisons en retard.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 07677a711bcc153da7933e42ec80e67a0d50eb35
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "923099"
---
# <a name="set-up-delivery-reminders"></a><span data-ttu-id="2923c-103">Configurer des relances livraison</span><span class="sxs-lookup"><span data-stu-id="2923c-103">Set Up Delivery Reminders</span></span>
<span data-ttu-id="2923c-104">Dans [!INCLUDE[d365fin](../../includes/d365fin_md.md)], vous pouvez utiliser des relances livraison pour rappeler aux fournisseurs les livraisons en retard.</span><span class="sxs-lookup"><span data-stu-id="2923c-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can use purchase delivery reminders to remind vendors about overdue deliveries.</span></span> <span data-ttu-id="2923c-105">Pour créer des relances livraison pour les fournisseurs, vous devez configurer des données de base pour la création de relances livraison et des souches de numéros pour les relances livraison dans la page **Paramètres achats**.</span><span class="sxs-lookup"><span data-stu-id="2923c-105">To create delivery reminders for vendors, you must set up base data for delivery reminder creation and number series for the delivery reminders on the **Purchases & Payables Setup** page.</span></span>  

## <a name="to-set-up-delivery-reminders"></a><span data-ttu-id="2923c-106">Pour paramétrer des relances livraison</span><span class="sxs-lookup"><span data-stu-id="2923c-106">To set up delivery reminders</span></span>  

1.  <span data-ttu-id="2923c-107">Sélectionnez l'icône ![Page ou état pour la recherche](../../media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Paramètres achats**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="2923c-107">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2923c-108">Dans le raccourci **Général**, dans le champ **Champ date rel. livr. par défaut**, spécifiez une des options suivantes comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2923c-108">On the **General** FastTab, in the **Default Del. Rem. Date Field** field, specify one of the following options as described in the following table.</span></span>  

    |<span data-ttu-id="2923c-109">Option</span><span class="sxs-lookup"><span data-stu-id="2923c-109">Option</span></span>|<span data-ttu-id="2923c-110">Désignation</span><span class="sxs-lookup"><span data-stu-id="2923c-110">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="2923c-111">**Date réception demandée**</span><span class="sxs-lookup"><span data-stu-id="2923c-111">**Requested Receipt Date**</span></span>|<span data-ttu-id="2923c-112">Pour indiquer que la valeur de date dans le champ **Date réception demandée** sur la ligne commande achat est utilisée comme date par défaut pour créer des relances livraison.</span><span class="sxs-lookup"><span data-stu-id="2923c-112">To specify that the date value in the **Requested Receipt Date** field on the purchase order line will be used as the default date for creating delivery reminders.</span></span>|  
    |<span data-ttu-id="2923c-113">**Date réception confirmée**</span><span class="sxs-lookup"><span data-stu-id="2923c-113">**Promised Receipt Date**</span></span>|<span data-ttu-id="2923c-114">Pour indiquer que la valeur de date dans le champ **Date réception confirmée** sur la ligne commande achat est utilisée comme date par défaut pour créer des relances livraison.</span><span class="sxs-lookup"><span data-stu-id="2923c-114">To specify that the date value in the **Promised Receipt Date** field on the purchase order line will be used as the default date for creating delivery reminders.</span></span>|  
    |<span data-ttu-id="2923c-115">**Date réception prévue**</span><span class="sxs-lookup"><span data-stu-id="2923c-115">**Expected Receipt Date**</span></span>|<span data-ttu-id="2923c-116">Pour indiquer que la valeur de date dans le champ **Date réception prévue** sur la ligne commande achat est utilisée comme date par défaut pour créer des relances livraison.</span><span class="sxs-lookup"><span data-stu-id="2923c-116">To specify that the date value in the **Expected Receipt Date** field on the purchase order line will be used as the default date for creating delivery reminders.</span></span>|  

3.  <span data-ttu-id="2923c-117">Sur le raccourci **Numérotation**, renseignez les champs comme indiqué dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="2923c-117">On the **Numbering** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="2923c-118">Champ</span><span class="sxs-lookup"><span data-stu-id="2923c-118">Field</span></span>|<span data-ttu-id="2923c-119">Désignation</span><span class="sxs-lookup"><span data-stu-id="2923c-119">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="2923c-120">**Numéros relances livraison**</span><span class="sxs-lookup"><span data-stu-id="2923c-120">**Delivery Reminder Nos.**</span></span>|<span data-ttu-id="2923c-121">Code souche de numéros pour les relances livraison.</span><span class="sxs-lookup"><span data-stu-id="2923c-121">The number series code for delivery reminders.</span></span>|  
    |<span data-ttu-id="2923c-122">**Numéros relances livraison émis**</span><span class="sxs-lookup"><span data-stu-id="2923c-122">**Issued Delivery Reminder Nos.**</span></span>|<span data-ttu-id="2923c-123">Code souche de numéros pour les relances livraison émises.</span><span class="sxs-lookup"><span data-stu-id="2923c-123">The number series code for issued delivery reminders.</span></span>|  

4.  <span data-ttu-id="2923c-124">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="2923c-124">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2923c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2923c-125">See Also</span></span>  
 <span data-ttu-id="2923c-126">[relances livraison](delivery-reminders.md) </span><span class="sxs-lookup"><span data-stu-id="2923c-126">[Delivery Reminders](delivery-reminders.md) </span></span>  
 <span data-ttu-id="2923c-127">[Configurer les conditions, niveaux et textes de relance livraison.](how-to-set-up-delivery-reminder-terms-levels-and-text.md) </span><span class="sxs-lookup"><span data-stu-id="2923c-127">[Set Up Delivery Reminder Terms, Levels, and Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md) </span></span>  
 <span data-ttu-id="2923c-128">[Affecter des codes de relance livraison à des fournisseurs](how-to-assign-delivery-reminder-codes-to-vendors.md) </span><span class="sxs-lookup"><span data-stu-id="2923c-128">[Assign Delivery Reminder Codes to Vendors](how-to-assign-delivery-reminder-codes-to-vendors.md) </span></span>  
 [<span data-ttu-id="2923c-129">Créer manuellement des relances livraison</span><span class="sxs-lookup"><span data-stu-id="2923c-129">Create Delivery Reminders Manually</span></span>](how-to-create-delivery-reminders-manually.md)
