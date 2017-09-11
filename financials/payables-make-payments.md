---
title: "Aperçu des tâches permettant de gérer les paiements aux fournisseurs| Microsoft Docs"
description: "Décrit les tâches permettant de gérer les paiements aux fournisseurs ou aux créditeurs, y compris la validation de lignes paiement et d'obtenir un aperçu du solde échu."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d0b9020596484a8910db2f5720adfe159ad96fe7
ms.contentlocale: fr-ch
ms.lasthandoff: 07/07/2017


---
# <a name="make-payments"></a><span data-ttu-id="77b56-103">Exécuter des paiements</span><span class="sxs-lookup"><span data-stu-id="77b56-103">Make Payments</span></span>
<span data-ttu-id="77b56-104">Lorsque vous effectuez des paiements aux fournisseurs, vous validez les lignes paiement associées dans la fenêtre **Feuille paiement**.</span><span class="sxs-lookup"><span data-stu-id="77b56-104">When you make payments to vendors, you post the related payment lines in the **Payment Journal** window.</span></span> <span data-ttu-id="77b56-105">Vous pouvez utiliser la fonction **Proposer paiements fournisseur** pour rechercher les paiements échus.</span><span class="sxs-lookup"><span data-stu-id="77b56-105">You can use the **Suggest Vendor Payments** function to find payments that are due.</span></span> <span data-ttu-id="77b56-106">Vous pouvez également utiliser l'état **Fourn. : Échéancier** pour obtenir un aperçu des paiements échus.</span><span class="sxs-lookup"><span data-stu-id="77b56-106">You can also use the **Vendor - Summary Aging** report to get an overview of due payments.</span></span>

<span data-ttu-id="77b56-107">À partir de la feuille de paiements, vous pouvez imprimer des chèques informatiques ou effectuer un enregistrement lorsque les chèques sont rédigés.</span><span class="sxs-lookup"><span data-stu-id="77b56-107">From the payment journal, you can print computer checks or record when checks are written.</span></span> <span data-ttu-id="77b56-108">Si vous sélectionnez **Informatique** dans le champ **Mode émission paiement**, toutes les lignes représentant des chèques doivent être imprimées avant que les lignes feuille puissent être validées.</span><span class="sxs-lookup"><span data-stu-id="77b56-108">If you select **Computer Check** in the **Bank Payment Type** field, then any lines representing checks must be printed before the payment journal can be posted.</span></span>

<span data-ttu-id="77b56-109">Lorsque les paiements sont validés, vous pouvez les exporter-vers un fichier bancaire à télécharger vers votre banque pour traitement.</span><span class="sxs-lookup"><span data-stu-id="77b56-109">When the payments are posted, you can export them to a bank file for upload to your bank for processing.</span></span>

<span data-ttu-id="77b56-110">Une fois les paiements effectués au niveau de votre banque, vous devez les lettrer avec les écritures comptables fournisseur ouvertes correspondantes.</span><span class="sxs-lookup"><span data-stu-id="77b56-110">After the payments are made at your bank, you must apply them to their related open vendor ledger entries.</span></span> <span data-ttu-id="77b56-111">Vous pouvez le faire manuellement ou en important un fichier de relevé bancaire et en lettrant les paiements automatiquement.</span><span class="sxs-lookup"><span data-stu-id="77b56-111">You can do this manually or by importing a bank statement file and applying the payments automatically.</span></span> <span data-ttu-id="77b56-112">Pour plus d'informations, reportez-vous à [Lettrage automatique des paiements et rapprochement des comptes bancaires](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="77b56-112">For more information, see [Apply Payments Automatically and Reconcile Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span>

<span data-ttu-id="77b56-113">Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.</span><span class="sxs-lookup"><span data-stu-id="77b56-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="77b56-114">Pour</span><span class="sxs-lookup"><span data-stu-id="77b56-114">To</span></span> | <span data-ttu-id="77b56-115">Voir</span><span class="sxs-lookup"><span data-stu-id="77b56-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="77b56-116">Utiliser une fonction pour proposer des paiements fournisseur en fonction de critères sélectionnés, tels que la date d'échéance, la possibilité d'escompte et vos liquidités.</span><span class="sxs-lookup"><span data-stu-id="77b56-116">Use a function to suggest vendor payments according to selected criteria, such as due date, discount eligibility, and your liquidity.</span></span> |[<span data-ttu-id="77b56-117">Procédure : proposer des paiements fournisseur</span><span class="sxs-lookup"><span data-stu-id="77b56-117">How to: Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md) |
| <span data-ttu-id="77b56-118">Émettre des chèques pour les paiements, sous forme de documents imprimés ou de chèques informatiques.</span><span class="sxs-lookup"><span data-stu-id="77b56-118">Issue checks for payments, either as print-outs or as computer checks.</span></span> <span data-ttu-id="77b56-119">Annuler des chèques avant ou après la validation.</span><span class="sxs-lookup"><span data-stu-id="77b56-119">Void checks before or after posting.</span></span> |[<span data-ttu-id="77b56-120">Procédure : utilisation des chèques</span><span class="sxs-lookup"><span data-stu-id="77b56-120">How to: Work with Checks</span></span>](payables-how-work-checks.md) |
| <span data-ttu-id="77b56-121">Assurez-vous que la banque efface uniquement les chèques et les montants validés en envoyant un fichier contenant des informations de paiement, du chèque et du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="77b56-121">Make sure that your bank only clears validated checks and amounts by sending them a file that contains vendor, check, and payment information.</span></span> |[<span data-ttu-id="77b56-122">Procédure : exporter des fichiers Positive Pay</span><span class="sxs-lookup"><span data-stu-id="77b56-122">How to: Export a Positive Pay file</span></span>](finance-how-positive-pay.md) |
|<span data-ttu-id="77b56-123">Exporter des paiements à partir de la fenêtre **Feuille paiement** vers un fichier bancaire que vous téléchargez vers votre banque pour traitement, y compris un transfert électronique de fond (EFT) en Amérique du Nord.</span><span class="sxs-lookup"><span data-stu-id="77b56-123">Export payments from the **Payment Journal** window to a bank file that you upload to your bank for processing, including EFT (electronic funds transfer) in North America.</span></span> |[<span data-ttu-id="77b56-124">Procédure : exportation de paiements vers un fichier bancaire</span><span class="sxs-lookup"><span data-stu-id="77b56-124">How to: Export Payments to a Bank File</span></span>](payables-how-export-payments-bank-file.md)|  

## <a name="see-also"></a><span data-ttu-id="77b56-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77b56-125">See Also</span></span>
[<span data-ttu-id="77b56-126">Gestion des comptes fournisseur</span><span class="sxs-lookup"><span data-stu-id="77b56-126">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="77b56-127">Achats</span><span class="sxs-lookup"><span data-stu-id="77b56-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="77b56-128">Gestion des comptes client</span><span class="sxs-lookup"><span data-stu-id="77b56-128">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="77b56-129">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="77b56-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

