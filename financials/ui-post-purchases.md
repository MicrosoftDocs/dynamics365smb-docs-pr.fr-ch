---
title: Familiarisation avec la validation des documents achat | Microsoft Docs
description: "En savoir plus sur les différentes fonctions de validation pour valider des documents achat."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/12/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 06c22658518d504c80a5a379d579cf7f7e8a0757
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="posting-purchases"></a><span data-ttu-id="68cc4-103">Validation des achats</span><span class="sxs-lookup"><span data-stu-id="68cc4-103">Posting Purchases</span></span>
<span data-ttu-id="68cc4-104">Dans le groupe **Validation** sur un document achat, vous pouvez faire votre choix parmi les fonctions de validation suivantes :</span><span class="sxs-lookup"><span data-stu-id="68cc4-104">In the **Posting group** on a purchase document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="68cc4-105">**Valider**</span><span class="sxs-lookup"><span data-stu-id="68cc4-105">**Post**</span></span>
* <span data-ttu-id="68cc4-106">**Aperçu compta.**</span><span class="sxs-lookup"><span data-stu-id="68cc4-106">**Preview Posting**</span></span>
* <span data-ttu-id="68cc4-107">**Valider et Imprimer**</span><span class="sxs-lookup"><span data-stu-id="68cc4-107">**Post and Print**</span></span>
* <span data-ttu-id="68cc4-108">**Impression test**</span><span class="sxs-lookup"><span data-stu-id="68cc4-108">**Test Report**</span></span>
* <span data-ttu-id="68cc4-109">**Valider par lot**</span><span class="sxs-lookup"><span data-stu-id="68cc4-109">**Post Batch**</span></span>

<span data-ttu-id="68cc4-110">Lorsque vous avez renseigné toutes les lignes et saisi toutes les informations de la commande achat, vous pouvez la valider, c'est-à-dire, créer une réception et une facture.</span><span class="sxs-lookup"><span data-stu-id="68cc4-110">When you have completed all the lines and entered all the information on the purchase order, you can post it, that is, create a receipt and an invoice.</span></span>

<span data-ttu-id="68cc4-111">Lorsqu’une commande achat est validée, le compte du fournisseur, les écritures comptables et les écritures comptables article sont mis à jour.</span><span class="sxs-lookup"><span data-stu-id="68cc4-111">When a purchase order is posted, the vendor's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="68cc4-112">Pour chaque commande achat, une écriture achat est créée dans la table **Ecriture comptable**.</span><span class="sxs-lookup"><span data-stu-id="68cc4-112">For each purchase order, a purchase entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="68cc4-113">Une écriture est également créée dans le compte fournisseur de la table **Ecriture fournisseur** et une autre dans le compte fournisseur approprié.</span><span class="sxs-lookup"><span data-stu-id="68cc4-113">An entry is also created in the vendor's account in the **Vendor Ledger Entry** table and a G/L entry is created in the relevant payables account.</span></span> <span data-ttu-id="68cc4-114">De plus, la validation de la commande peut avoir pour résultat la création d'une écriture TVA et d'une écriture comptable pour le montant de la remise.</span><span class="sxs-lookup"><span data-stu-id="68cc4-114">In addition, posting the order may result in a VAT entry and a G/L entry for the discount amount.</span></span> <span data-ttu-id="68cc4-115">La validation d'une écriture pour la remise dépend de la valeur du champ **Comptabilisation remise** de la fenêtre **Paramètres achats**.</span><span class="sxs-lookup"><span data-stu-id="68cc4-115">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field in the **Purchases & Payables Setup** window.</span></span>

<span data-ttu-id="68cc4-116">Pour chaque ligne commande achat, une écriture comptable article est créée dans la table **Écriture comptable article** (si les lignes achat contiennent des numéros d'article) ou une écriture est créée dans la table **Écriture comptable** (si les lignes achat contiennent un compte général).</span><span class="sxs-lookup"><span data-stu-id="68cc4-116">For each purchase order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the purchase lines contain item numbers) or a G/L entry will be created in the **G/L Entry** table (if the purchase lines contain a G/L account).</span></span> <span data-ttu-id="68cc4-117">En outre, les commandes achat sont toujours enregistrées dans les tables **En-tête réception achat** et **En-tête facture achat**.</span><span class="sxs-lookup"><span data-stu-id="68cc4-117">In addition, purchase orders are always recorded in the **Purch. Recpt. Header** and **Purch. Inv. Header** tables.</span></span>

<span data-ttu-id="68cc4-118">Avant de commencer à valider, vous pouvez effectuer une impression test qui contient toutes les informations de la commande achat et indique les erreurs afférentes.</span><span class="sxs-lookup"><span data-stu-id="68cc4-118">Before you start to post, you can print a test report that contains all the information in the purchase order and indicates any errors there.</span></span> <span data-ttu-id="68cc4-119">Pour imprimer l’état, sélectionnez **Validation**, puis **Impression test**.</span><span class="sxs-lookup"><span data-stu-id="68cc4-119">To print the report, choose **Posting**, and then choose **Test Report**.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="68cc4-120">Lorsque vous validez une commande, vous pouvez créer une réception et une facture.</span><span class="sxs-lookup"><span data-stu-id="68cc4-120">When you post an order, you can create both a receipt and an invoice.</span></span> <span data-ttu-id="68cc4-121">Celles-ci peuvent être faites simultanément ou séparément.</span><span class="sxs-lookup"><span data-stu-id="68cc4-121">These can be done simultaneously or independently.</span></span> <span data-ttu-id="68cc4-122">Vous pouvez également créer une réception partielle et une facture partielle en renseignant les champs **Qté à recevoir** et **Qté à facturer** sur chaque ligne commande achat avant la validation.</span><span class="sxs-lookup"><span data-stu-id="68cc4-122">You can also create a partial receipt and a partial invoice by completing the **Qty. to Receive** and **Qty. to Invoice** fields on the individual purchase order lines before you post.</span></span> <span data-ttu-id="68cc4-123">Remarquez que vous ne pouvez pas créer de facture pour un article qui n'a pas été reçu.</span><span class="sxs-lookup"><span data-stu-id="68cc4-123">Note that you cannot create an invoice for something that has not been received.</span></span> <span data-ttu-id="68cc4-124">C'est-à-dire que, avant de pouvoir facturer, vous devez avoir validé une réception, ou vous devez choisir de réceptionner et de facturer en même temps.</span><span class="sxs-lookup"><span data-stu-id="68cc4-124">That is, before you can invoice, you must have recorded a receipt, or you must choose to receive and invoice at the same time.</span></span>

<span data-ttu-id="68cc4-125">Vous pouvez soit valider, soit valider et imprimer.</span><span class="sxs-lookup"><span data-stu-id="68cc4-125">You can either post, or post and print.</span></span> <span data-ttu-id="68cc4-126">Si vous choisissez de valider et d’imprimer, un rapport est imprimé lorsque la commande est validée.</span><span class="sxs-lookup"><span data-stu-id="68cc4-126">If you choose to post and print, a report is printed when the order is posted.</span></span> <span data-ttu-id="68cc4-127">Vous pouvez aussi choisir la fonction **Valider par lot**, qui vous permet de valider plusieurs commandes en même temps.</span><span class="sxs-lookup"><span data-stu-id="68cc4-127">You can also choose the **Post Batch** function, which lets you post several orders at the same time.</span></span>

<span data-ttu-id="68cc4-128">Lorsque la validation est terminée, les lignes achat validées sont supprimées de la commande.</span><span class="sxs-lookup"><span data-stu-id="68cc4-128">When the posting is completed, the posted purchase lines are removed from the order.</span></span> <span data-ttu-id="68cc4-129">Un message vous indique lorsque la validation est terminée.</span><span class="sxs-lookup"><span data-stu-id="68cc4-129">A message tells you when the posting is completed.</span></span> <span data-ttu-id="68cc4-130">Vous pouvez ensuite afficher les écritures validées dans les diverses fenêtres qui contiennent les écritures validées, comme les fenêtres **Écritures comptable fournisseur**, **Écritures comptable**, **Écritures comptable article**, **Réceptions achat enreg.** et **Factures achat enregistrées**.</span><span class="sxs-lookup"><span data-stu-id="68cc4-130">After this, you will be able to see the posted entries in the various windows that contain posted entries, such as the **Vendor Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Purchase Receipts**, and **Posted Purchase Invoices** windows.</span></span>

## <a name="see-also"></a><span data-ttu-id="68cc4-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68cc4-131">See Also</span></span>
[<span data-ttu-id="68cc4-132">Achats</span><span class="sxs-lookup"><span data-stu-id="68cc4-132">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="68cc4-133">Valider des documents et des feuilles</span><span class="sxs-lookup"><span data-stu-id="68cc4-133">Post Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="68cc4-134">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="68cc4-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


