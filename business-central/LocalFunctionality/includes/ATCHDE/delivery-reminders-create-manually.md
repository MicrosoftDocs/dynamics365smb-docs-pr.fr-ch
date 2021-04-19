---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5060724f27f842e06a2e8641605c1c3011d0cd9c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774418"
---
<span data-ttu-id="f8e89-101">Dans [!INCLUDE[prod_short](../../../includes/prod_short.md)], vous pouvez créer des relances livraison lorsqu'un achat n'a pas été livré comme prévu.</span><span class="sxs-lookup"><span data-stu-id="f8e89-101">In [!INCLUDE[prod_short](../../../includes/prod_short.md)], you can create delivery reminders when a purchase has not been delivered as expected.</span></span> <span data-ttu-id="f8e89-102">Vous pouvez créer une relance livraison unique manuellement, ou vous pouvez générer des relances livraison pour toutes les livraisons échues.</span><span class="sxs-lookup"><span data-stu-id="f8e89-102">You can create a single delivery reminder manually, or you can generate delivery reminders for all overdue deliveries.</span></span>  

> [!NOTE]
> <span data-ttu-id="f8e89-103">Pour créer des relances livraison, vous devez avoir configuré les conditions, les niveaux et les textes des relances livraison.</span><span class="sxs-lookup"><span data-stu-id="f8e89-103">To create delivery reminders, you must have set up the delivery reminder terms, levels, and texts.</span></span>

## <a name="to-create-a-delivery-reminder-manually"></a><span data-ttu-id="f8e89-104">Pour créer une relance livraison manuellement</span><span class="sxs-lookup"><span data-stu-id="f8e89-104">To create a delivery reminder manually</span></span>  

1. <span data-ttu-id="f8e89-105">Choisissez l'icône ![Icône Ampoule qui ouvre la fonction Tell Me](../../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Relance livraison**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="f8e89-105">Choose the ![The lightbulb icon that opens the Tell Me feature](../../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delivery Reminder**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f8e89-106">Sélectionnez l'action **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="f8e89-106">Choose the **New** action.</span></span>  
3. <span data-ttu-id="f8e89-107">Sur la page **Relance livraison**, renseignez les champs comme décrit dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="f8e89-107">On the **Delivery Reminder** page, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="f8e89-108">Champ</span><span class="sxs-lookup"><span data-stu-id="f8e89-108">Field</span></span>|<span data-ttu-id="f8e89-109">Désignation</span><span class="sxs-lookup"><span data-stu-id="f8e89-109">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="f8e89-110">**N°**</span><span class="sxs-lookup"><span data-stu-id="f8e89-110">**No.**</span></span>|<span data-ttu-id="f8e89-111">Numéro d'identification unique de la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="f8e89-111">The unique identification number for the delivery reminder.</span></span>|  
    |<span data-ttu-id="f8e89-112">**N° fournisseur**</span><span class="sxs-lookup"><span data-stu-id="f8e89-112">**Vendor No.**</span></span>|<span data-ttu-id="f8e89-113">Numéro du fournisseur pour lequel vous souhaitez publier la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="f8e89-113">The number of the vendor for whom you want to post the delivery reminder.</span></span><br /><br /> <span data-ttu-id="f8e89-114">Lorsque vous sélectionnez le numéro de fournisseur, les champs **Nom**, **Adresse**, **CP/Ville** et **Contact** sont renseignés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="f8e89-114">When you select the vendor number, the **Name**, **Address**, **Post Code/City**, and **Contact** fields are filled in automatically.</span></span>|  
    |<span data-ttu-id="f8e89-115">**Date de validation**</span><span class="sxs-lookup"><span data-stu-id="f8e89-115">**Posting Date**</span></span>|<span data-ttu-id="f8e89-116">Date de validation de la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="f8e89-116">The posting date for the delivery reminder.</span></span> <span data-ttu-id="f8e89-117">Cette date est copiée dans toutes les écritures comptables de la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="f8e89-117">This date is copied to all of the delivery reminder ledger entries.</span></span>|  
    |<span data-ttu-id="f8e89-118">**Date document**</span><span class="sxs-lookup"><span data-stu-id="f8e89-118">**Document Date**</span></span>|<span data-ttu-id="f8e89-119">Date du document de la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="f8e89-119">The document date for the delivery reminder.</span></span> <span data-ttu-id="f8e89-120">Cette date est également utilisée pour calculer la date d'échéance pour la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="f8e89-120">This date is also used to calculate the due date for the delivery reminder.</span></span> <span data-ttu-id="f8e89-121">Vous pouvez modifier la date de validation, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="f8e89-121">You can modify the posting date if required.</span></span>|  
    |<span data-ttu-id="f8e89-122">**Niveau relance**</span><span class="sxs-lookup"><span data-stu-id="f8e89-122">**Reminder Level**</span></span>|<span data-ttu-id="f8e89-123">Niveau de relance livraison.</span><span class="sxs-lookup"><span data-stu-id="f8e89-123">The delivery reminder level.</span></span> <span data-ttu-id="f8e89-124">Cette valeur est basée sur le nombre de relances livraison déjà envoyées.</span><span class="sxs-lookup"><span data-stu-id="f8e89-124">This value is based on the number of delivery reminders that have already been sent.</span></span>|  
    |<span data-ttu-id="f8e89-125">**Code condition relance**</span><span class="sxs-lookup"><span data-stu-id="f8e89-125">**Reminder Terms Code**</span></span>|<span data-ttu-id="f8e89-126">Spécifiez le code condition relance livraison qui est paramétré pour le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f8e89-126">Specify the delivery reminder terms code that is set up for the vendor.</span></span>|  
    |<span data-ttu-id="f8e89-127">**Date d'échéance**</span><span class="sxs-lookup"><span data-stu-id="f8e89-127">**Due Date**</span></span>|<span data-ttu-id="f8e89-128">Date d'échéance de la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="f8e89-128">The due date for the delivery reminder.</span></span>|  

4. <span data-ttu-id="f8e89-129">Choisissez l'action **Proposer lignes relance**.</span><span class="sxs-lookup"><span data-stu-id="f8e89-129">Choose the **Suggest Reminder Lines** action.</span></span>  

    <span data-ttu-id="f8e89-130">S'il existe des livraisons échues du fournisseur spécifié, ces dernières sont ajoutées à la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="f8e89-130">If there are overdue deliveries from the specified vendor, these are added to the delivery reminder.</span></span>  

5. <span data-ttu-id="f8e89-131">Cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="f8e89-131">Choose the **OK** button.</span></span>  

    <span data-ttu-id="f8e89-132">La relance livraison est créée.</span><span class="sxs-lookup"><span data-stu-id="f8e89-132">The delivery reminder is created.</span></span> <span data-ttu-id="f8e89-133">Vous pouvez alors émettre et imprimer la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="f8e89-133">You can now issue and print the delivery reminder.</span></span>  
