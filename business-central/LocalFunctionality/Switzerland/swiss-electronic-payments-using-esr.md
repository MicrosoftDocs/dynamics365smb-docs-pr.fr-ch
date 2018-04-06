---
title: "Paiements électroniques à l'aide de ESR+, Suisse"
description: "La méthode de paiement électronique Einzahlungsschein mit Referenznummer (ESR) est un service de prélèvement électronique qui permet au client de facturer les factures ouvertes en francs suisses (CHF) et en euros (EUR), et de comptabiliser efficacement les paiements entrants."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: dbd03106bca19c2b6d19fc92d36b839ea856acd1
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="swiss-electronic-payments-using-esr"></a><span data-ttu-id="68bcf-103">Paiements électroniques à l'aide de ESR+, Suisse</span><span class="sxs-lookup"><span data-stu-id="68bcf-103">Swiss Electronic Payments Using ESR</span></span>
<span data-ttu-id="68bcf-104">La méthode de paiement électronique Einzahlungsschein mit Referenznummer (ESR) est un service de prélèvement électronique qui permet au client de facturer les factures ouvertes en francs suisses (CHF) et en euros (EUR), et de comptabiliser efficacement les paiements entrants.</span><span class="sxs-lookup"><span data-stu-id="68bcf-104">The Einzahlungsschein mit Referenznummer (ESR) electronic payment method is an electronic debtor service that allows the customer to bill open invoices in Swiss Francs (CHF) and Euros (EUR), and to post incoming payments efficiently.</span></span> <span data-ttu-id="68bcf-105">Le numéro de référence, ou la ligne de code, contient toutes les données de comptabilité pertinentes.</span><span class="sxs-lookup"><span data-stu-id="68bcf-105">The reference number, or code line, contains all relevant bookkeeping data.</span></span>  

<span data-ttu-id="68bcf-106">Avec les paiements électroniques ESR, vous pouvez effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="68bcf-106">With ESR electronic payments, you can do the following:</span></span>  

- <span data-ttu-id="68bcf-107">Envoyez les bordereaux de paiement ESR avec des numéros de référence uniques sur les factures.</span><span class="sxs-lookup"><span data-stu-id="68bcf-107">Send ESR payment slips with unique reference numbers on the invoices.</span></span> <span data-ttu-id="68bcf-108">En raison des numéros de référence ESR uniques, les paiements pour règlement sont automatiquement appliqués aux factures correspondantes.</span><span class="sxs-lookup"><span data-stu-id="68bcf-108">Because of the unique ESR reference numbers, the payments for settlement are automatically applied to the related invoices.</span></span> <span data-ttu-id="68bcf-109">Pour plus d'informations, reportez-vous à [Imprimer des factures ESR](how-to-print-esr-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="68bcf-109">For more information, see [Print ESR Invoices](how-to-print-esr-invoices.md).</span></span>  

- <span data-ttu-id="68bcf-110">Téléchargez quotidiennement les fichiers ESR de la banque.</span><span class="sxs-lookup"><span data-stu-id="68bcf-110">Download the ESR files from the bank daily.</span></span> <span data-ttu-id="68bcf-111">Les fichiers contiennent des informations sur toutes les factures payées.</span><span class="sxs-lookup"><span data-stu-id="68bcf-111">The files contain information about all paid invoices.</span></span>  

- <span data-ttu-id="68bcf-112">Importez les fichiers ESR et créez des lignes de paiement automatiquement pour chaque paiement.</span><span class="sxs-lookup"><span data-stu-id="68bcf-112">Import the ESR files and create payment lines automatically for each payment.</span></span> <span data-ttu-id="68bcf-113">Pour plus d'informations, reportez-vous à [Importer des paiements ESR](how-to-import-esr-payments.md).</span><span class="sxs-lookup"><span data-stu-id="68bcf-113">For more information, see [Import ESR Payments](how-to-import-esr-payments.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="68bcf-114">Avant de pouvoir utiliser le module ESR, vous devez configurer la banque, le compte bancaire et le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="68bcf-114">Before you can use the ESR module, you must set up the bank, bank account, and file name.</span></span> <span data-ttu-id="68bcf-115">Vous devez également spécifier si ESR ou ESR+ doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="68bcf-115">You must also specify whether ESR or ESR+ should be used.</span></span>

<span data-ttu-id="68bcf-116">Lorsque vous avez évalué les informations de configuration, vous pouvez ajuster le formulaire de facture et créer une série de tests que vous pouvez demander à votre banque ou à votre service postal de valider.</span><span class="sxs-lookup"><span data-stu-id="68bcf-116">When you have evaluated the setup information, you can adjust the invoice form, and you can create a test series that you can ask your bank or postal service to validate.</span></span>  

<span data-ttu-id="68bcf-117">Lorsque vous configurez des souches de numéros pour les factures, vous devez suivre les instructions suivantes :</span><span class="sxs-lookup"><span data-stu-id="68bcf-117">When you set up number series for invoices, you must follow these guidelines:</span></span>  

- <span data-ttu-id="68bcf-118">Utilisez un maximum de huit chiffres.</span><span class="sxs-lookup"><span data-stu-id="68bcf-118">Use a maximum of eight digits.</span></span>  
- <span data-ttu-id="68bcf-119">Utilisez uniquement des caractères numériques.</span><span class="sxs-lookup"><span data-stu-id="68bcf-119">Use only numeric characters.</span></span>  
- <span data-ttu-id="68bcf-120">Ne précédez pas les nombres de zéros.</span><span class="sxs-lookup"><span data-stu-id="68bcf-120">Do not precede numbers with zeros.</span></span>  

## <a name="see-also"></a><span data-ttu-id="68bcf-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68bcf-121">See Also</span></span>  
 <span data-ttu-id="68bcf-122">[Paiements électroniques, Suisse](swiss-electronic-payments.md) </span><span class="sxs-lookup"><span data-stu-id="68bcf-122">[Swiss Electronic Payments](swiss-electronic-payments.md) </span></span>  
 <span data-ttu-id="68bcf-123">[Imprimer des factures ESR](how-to-print-esr-invoices.md) </span><span class="sxs-lookup"><span data-stu-id="68bcf-123">[Print ESR Invoices](how-to-print-esr-invoices.md) </span></span>  
 <span data-ttu-id="68bcf-124">[Importation de paiements ESR](how-to-import-esr-payments.md) </span><span class="sxs-lookup"><span data-stu-id="68bcf-124">[Import ESR Payments](how-to-import-esr-payments.md) </span></span>  
 <span data-ttu-id="68bcf-125">[Paiements électroniques à l'aide de LSV+, Suisse](swiss-electronic-payments-using-lsv-.md) </span><span class="sxs-lookup"><span data-stu-id="68bcf-125">[Swiss Electronic Payments Using LSV+](swiss-electronic-payments-using-lsv-.md) </span></span>  
 [<span data-ttu-id="68bcf-126">Effectuer des paiements</span><span class="sxs-lookup"><span data-stu-id="68bcf-126">Making Payments</span></span>](../../payables-make-payments.md)

