---
title: "Gérer des comptes bancaires| Microsoft Docs"
description: "Vous devez régulièrement rapprocher les écritures comptables bancaires avec les transactions bancaires associées à vos comptes bancaires."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: f3733c3ec0048171294aae51dcfac0c2ecdc9e72
ms.contentlocale: fr-ch
ms.lasthandoff: 09/28/2018

---
# <a name="managing-bank-accounts"></a><span data-ttu-id="5fc6a-103">Gestion des comptes bancaires</span><span class="sxs-lookup"><span data-stu-id="5fc6a-103">Managing Bank Accounts</span></span>
<span data-ttu-id="5fc6a-104">Vous devez rapprocher régulièrement vos écritures comptables banque dans [!INCLUDE[d365fin](includes/d365fin_md.md)] avec les transactions bancaires associées dans les comptes bancaires de votre banque, puis valider le solde sur votre compte bancaire.</span><span class="sxs-lookup"><span data-stu-id="5fc6a-104">At regular intervals, you must reconcile your bank ledger entries in [!INCLUDE[d365fin](includes/d365fin_md.md)] with the related bank transactions in bank accounts at your bank, and then post the balance to your bank account.</span></span> <span data-ttu-id="5fc6a-105">Vous pouvez effectuer cette tâche soit dans le cadre du traitement des paiements représentés sur un relevé bancaire dans la **Feuille rapprochement bancaire**.</span><span class="sxs-lookup"><span data-stu-id="5fc6a-105">You can perform this task either as part of processing the payments represented on a bank statement in the **Payment Reconciliation Journal**.</span></span> <span data-ttu-id="5fc6a-106">Vous pouvez également effectuer la tâche séparément du traitement des paiements, dans la fenêtre **Rapprochement bancaire**, où vous mettez en correspondance (rapprochez) les lignes de relevé bancaire dans le volet gauche avec vos écritures comptables compte bancaire internes dans le volet droit.</span><span class="sxs-lookup"><span data-stu-id="5fc6a-106">Alternatively, you can perform the task separately from payment processing, in the **Bank Acc. Reconciliation** window where you match (reconcile) bank statement lines in the left-hand pane with your internal bank account ledger entries in the right-hand pane.</span></span> <span data-ttu-id="5fc6a-107">Dans les deux fenêtres, vous pouvez renseigner les informations de relevé bancaire en important un fichier ou un flux, et vous pouvez utiliser les suggestions de correspondance automatique.</span><span class="sxs-lookup"><span data-stu-id="5fc6a-107">In both windows, you can fill in the bank statement information by importing a file or feed and you can use automatic matching suggestions.</span></span>

> [!NOTE]  
> <span data-ttu-id="5fc6a-108">Dans les versions nord-américaines, vous pouvez également effectuer le rapprochement bancaire dans la fenêtre **Feuille rapprochement bancaire**, qui est mieux adaptée pour les chèques et les acomptes, mais ne prend pas en charge l'importation de fichiers de relevé bancaire.</span><span class="sxs-lookup"><span data-stu-id="5fc6a-108">In North American versions, you can also perform bank reconciliation in the **Bank Rec. Worksheet** window, which is better suited for checks and deposits but does not offer import of bank statement files.</span></span> <span data-ttu-id="5fc6a-109">Pour utiliser cette fenêtre à la place de la fenêtre **Rapprochement bancaire**, désélectionnez le champ **Rapprochement bancaire avec correspondance auto.** dans la fenêtre **Paramètres comptabilité**.</span><span class="sxs-lookup"><span data-stu-id="5fc6a-109">To use this window instead of the **Bank Acc. Reconciliation** window, deselect the **Bank Recon. with Auto. Match** field in the **General Ledger Setup** window.</span></span> <span data-ttu-id="5fc6a-110">Pour plus d'informations, voir la section « Rapprocher des comptes bancaires » sous Fonctionnalité locale, États-Unis.</span><span class="sxs-lookup"><span data-stu-id="5fc6a-110">For more information, see the "Reconcile Bank Accounts" section under United States Local Functionality.</span></span>

<span data-ttu-id="5fc6a-111">Parfois, vous devez transférer les montants entre comptes bancaires dans [!INCLUDE[d365fin](includes/d365fin_md.md)] pour refléter les transferts effectués au niveau de votre banque.</span><span class="sxs-lookup"><span data-stu-id="5fc6a-111">Sometimes, you need to transfer amounts between bank account in [!INCLUDE[d365fin](includes/d365fin_md.md)] to reflect transfers at your bank.</span></span> <span data-ttu-id="5fc6a-112">Vous effectuez cette tâche dans la fenêtre **Feuille comptabilité**, de différentes manières en fonction de la devise des fonds.</span><span class="sxs-lookup"><span data-stu-id="5fc6a-112">You perform this task in the **General Journal** window, in different ways depending on the currency of the funds.</span></span>

<span data-ttu-id="5fc6a-113">Avant de pouvoir gérer des comptes bancaires, vous devez configurer chaque compte bancaire en tant que fiche compte bancaire.</span><span class="sxs-lookup"><span data-stu-id="5fc6a-113">Before you can manage bank accounts, you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="5fc6a-114">En outre, vous devez configurer les services électroniques que vous pouvez utiliser pour l'importation de relevés bancaires et l'exportation de fichiers de paiement.</span><span class="sxs-lookup"><span data-stu-id="5fc6a-114">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="5fc6a-115">Pour plus d'informations, reportez vous à [Configuration de comptes bancaires](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="5fc6a-115">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="5fc6a-116">Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.</span><span class="sxs-lookup"><span data-stu-id="5fc6a-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="5fc6a-117">Pour</span><span class="sxs-lookup"><span data-stu-id="5fc6a-117">To</span></span> | <span data-ttu-id="5fc6a-118">Voir</span><span class="sxs-lookup"><span data-stu-id="5fc6a-118">See</span></span> |
| --- | --- |
| <span data-ttu-id="5fc6a-119">Rapprocher des comptes bancaires en relation avec le traitement des paiements dans la fenêtre **Feuille rapprochement bancaire**.</span><span class="sxs-lookup"><span data-stu-id="5fc6a-119">Reconcile bank accounts in connection with payment processing in the **Payment Reconciliation Journal** window.</span></span> |[<span data-ttu-id="5fc6a-120">Lettrage automatique des paiements et rapprochement des comptes bancaires</span><span class="sxs-lookup"><span data-stu-id="5fc6a-120">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="5fc6a-121">Rapprocher des comptes bancaires, y compris les écritures comptables chèque, en tant que tâche distincte dans la fenêtre **Rapprochement bancaire**.</span><span class="sxs-lookup"><span data-stu-id="5fc6a-121">Reconcile bank accounts, including check ledger entries, as a separate task in the **Bank Acc. Reconciliation** window.</span></span> |[<span data-ttu-id="5fc6a-122">Rapprocher des comptes bancaires séparément</span><span class="sxs-lookup"><span data-stu-id="5fc6a-122">Reconcile Bank Accounts Separately</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="5fc6a-123">Valider des transferts entre comptes bancaires dans la même devise ou dans des devises différentes.</span><span class="sxs-lookup"><span data-stu-id="5fc6a-123">Post transfers between bank accounts in the same currency or in different currencies.</span></span> |[<span data-ttu-id="5fc6a-124">Transfert de fonds à la banque</span><span class="sxs-lookup"><span data-stu-id="5fc6a-124">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a><span data-ttu-id="5fc6a-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fc6a-125">See Also</span></span>
[<span data-ttu-id="5fc6a-126">Paramétrage des opérations bancaires</span><span class="sxs-lookup"><span data-stu-id="5fc6a-126">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="5fc6a-127">Gestion des comptes client</span><span class="sxs-lookup"><span data-stu-id="5fc6a-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="5fc6a-128">[Gestion des comptes fournisseur](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="5fc6a-128">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="5fc6a-129">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5fc6a-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="5fc6a-130">Fonctionnalités marché</span><span class="sxs-lookup"><span data-stu-id="5fc6a-130">General Business Functionality</span></span>](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

