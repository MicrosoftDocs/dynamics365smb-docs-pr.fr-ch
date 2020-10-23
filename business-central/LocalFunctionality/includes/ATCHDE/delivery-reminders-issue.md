---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: fa5b2fd51f222988254a4ffe5da6600eafa5dd56
ms.sourcegitcommit: 428f180604e5afcf94fa0e92a0615f58c88e13cd
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/02/2020
ms.locfileid: "3959650"
---
<span data-ttu-id="401e6-101">Après avoir créé des relances livraison, vous devez les émettre et les imprimer afin de pouvoir les envoyer aux fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="401e6-101">After you have created delivery reminders, you must issue and print them so that you can send reminders to vendors.</span></span> <span data-ttu-id="401e6-102">Avant d'émettre les relances livraison, vous pouvez imprimer un rapport de test.</span><span class="sxs-lookup"><span data-stu-id="401e6-102">Before you issue the delivery reminders, you can print a test report.</span></span>  

<span data-ttu-id="401e6-103">Lorsque vous émettez les relances livraison, des écritures comptables de relance livraison sont créées.</span><span class="sxs-lookup"><span data-stu-id="401e6-103">When you issue the delivery reminders, delivery reminder ledger entries are created.</span></span> <span data-ttu-id="401e6-104">Vous pouvez afficher les écritures comptables créées dans la page **Écritures comptables relance livraison**.</span><span class="sxs-lookup"><span data-stu-id="401e6-104">You can view the created ledger entries on the **Deliv. Reminder Ledger Entries** page.</span></span>  

## <a name="to-issue-delivery-reminders"></a><span data-ttu-id="401e6-105">Pour émettre des relances livraison</span><span class="sxs-lookup"><span data-stu-id="401e6-105">To issue delivery reminders</span></span>  

1. <span data-ttu-id="401e6-106">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](../../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Relance livraison**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="401e6-106">Choose the ![Lightbulb that opens the Tell Me feature](../../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delivery Reminder**, and then choose the related link.</span></span>  
2. <span data-ttu-id="401e6-107">Dans la page **Relance livraison**, sélectionnez la relance livraison que vous souhaitez émettre, puis choisissez l'action **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="401e6-107">On the **Delivery Reminder** page, select the delivery reminder that you want to issue, and then choose the **Edit** action.</span></span>  
3. <span data-ttu-id="401e6-108">Sélectionnez l'action **Émettre**.</span><span class="sxs-lookup"><span data-stu-id="401e6-108">Choose the **Issue** action.</span></span>  
4. <span data-ttu-id="401e6-109">Sur la page **Émettre relance livraison**, renseignez les champs comme décrit dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="401e6-109">On the **Issue Delivery Reminder** page, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="401e6-110">Champ</span><span class="sxs-lookup"><span data-stu-id="401e6-110">Field</span></span>|<span data-ttu-id="401e6-111">Désignation</span><span class="sxs-lookup"><span data-stu-id="401e6-111">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="401e6-112">**Imprimer**</span><span class="sxs-lookup"><span data-stu-id="401e6-112">**Print**</span></span>|<span data-ttu-id="401e6-113">Sélectionnez cette option pour imprimer les relances livraison lorsqu'elles sont émises.</span><span class="sxs-lookup"><span data-stu-id="401e6-113">Select to print the delivery reminders when they are issued.</span></span>|  
    |<span data-ttu-id="401e6-114">**Remplacer date comptabilisation**</span><span class="sxs-lookup"><span data-stu-id="401e6-114">**Replace Posting Date**</span></span>|<span data-ttu-id="401e6-115">Sélectionnez cette option pour remplacer la date de comptabilisation existante pour la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="401e6-115">Select to replace the existing posting date for the delivery reminder.</span></span>|  
    |<span data-ttu-id="401e6-116">**Date de validation**</span><span class="sxs-lookup"><span data-stu-id="401e6-116">**Posting Date**</span></span>|<span data-ttu-id="401e6-117">Date de validation de la relance livraison.</span><span class="sxs-lookup"><span data-stu-id="401e6-117">The posting date for the delivery reminder.</span></span><br /><br /> <span data-ttu-id="401e6-118">Cette date de comptabilisation est utilisée pour toutes les relances livraison si vous avez sélectionné la case à cocher **Remplacer date comptabilisation**.</span><span class="sxs-lookup"><span data-stu-id="401e6-118">This posting date is used for all delivery reminders if you have selected the **Replace Posting Date** check box.</span></span> <span data-ttu-id="401e6-119">Si la case à cocher **Remplacer date comptabilisation** est effacée, cette date ne sera utilisée que pour les relances livraison pour lesquelles une date de comptabilisation n'est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="401e6-119">If the **Replace Posting Date** check box is cleared, this date will be used for only those delivery reminders for which a posting date is not available.</span></span>|  

5. <span data-ttu-id="401e6-120">Éventuellement, dans le raccourci **En-tête de relance livraison**, sélectionnez les filtres appropriés.</span><span class="sxs-lookup"><span data-stu-id="401e6-120">Optionally, on the **Delivery Reminder Header** FastTab, select the appropriate filters.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="401e6-121">Vous pouvez supprimer les filtres et émettre à nouveau les relances livraison en même temps.</span><span class="sxs-lookup"><span data-stu-id="401e6-121">You can remove filters and issue all delivery reminders at the same time.</span></span>  

6. <span data-ttu-id="401e6-122">Choisissez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="401e6-122">Choose the **OK** button.</span></span>  

<span data-ttu-id="401e6-123">Vous pouvez afficher les relances émises dans la page **Relances livraison émises**.</span><span class="sxs-lookup"><span data-stu-id="401e6-123">You can view the issued reminders on the **Issued Delivery Reminder** page.</span></span> <span data-ttu-id="401e6-124">En option, vous pouvez maintenant imprimer une relance livraison.</span><span class="sxs-lookup"><span data-stu-id="401e6-124">Optionally, you can now print a delivery reminder.</span></span>  

## <a name="to-view-delivery-reminder-ledger-entries"></a><span data-ttu-id="401e6-125">Pour afficher des écritures comptables de relance livraison</span><span class="sxs-lookup"><span data-stu-id="401e6-125">To view delivery reminder ledger entries</span></span>  

1. <span data-ttu-id="401e6-126">Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me](../../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Commandes achat**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="401e6-126">Choose the ![Lightbulb that opens the Tell Me feature](../../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="401e6-127">Sélectionnez la commande achat pour laquelle vous souhaitez afficher le statut de relance, puis choisissez l'action **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="401e6-127">Select the purchase order for which you want to view the reminder status, and then choose the **Edit** action.</span></span>  
3. <span data-ttu-id="401e6-128">Sélectionnez l'action **Écritures comptables de relance livraison**.</span><span class="sxs-lookup"><span data-stu-id="401e6-128">Choose the **Deliv. Reminder Ledger Entries** action.</span></span>  

<span data-ttu-id="401e6-129">Sur la page **Écritures comptables de relance livraison**, vous pouvez afficher les écritures comptables de relance livraison pour la commande achat sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="401e6-129">On the **Deliv. Reminder Ledger Entries** page, you can view the delivery reminder ledger entries for the selected purchase order.</span></span>  
