---
title: "Choisir le mode de paiements électroniques | Microsoft Docs"
description: "Traitez les paiements à vos fournisseurs en exportant un fichier avec les informations de paiement provenant des lignes feuille."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: bbb38f7d4a4b7d1b63cfceef2640172d7b69e364
ms.contentlocale: fr-ch
ms.lasthandoff: 09/22/2017

---
# <a name="make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer"></a><span data-ttu-id="7093d-103">Exécuter les paiements avec le service de conversion de données bancaires ou un virement SEPA</span><span class="sxs-lookup"><span data-stu-id="7093d-103">Make Payments with Bank Data Conversion Service or SEPA Credit Transfer</span></span>
<span data-ttu-id="7093d-104">Dans la fenêtre **Feuille paiement**, vous pouvez traiter les paiements à vos fournisseurs en exportant un fichier avec les informations de paiement provenant des lignes feuille.</span><span class="sxs-lookup"><span data-stu-id="7093d-104">In the **Payment Journal** window, you can process payments to your vendors by exporting a file together with the payment information from the journal lines.</span></span> <span data-ttu-id="7093d-105">Vous pouvez ensuite télécharger le fichier vers votre banque électronique, où sont traités les transferts d'argent associés.</span><span class="sxs-lookup"><span data-stu-id="7093d-105">You can then upload the file to your electronic bank where the related money transfers are processed.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="7093d-106"> prend en charge le format de virement SEPA, mais dans votre pays/région, d'autres formats de paiements électroniques peuvent être disponibles.</span><span class="sxs-lookup"><span data-stu-id="7093d-106"> supports the SEPA Credit Transfer format, but in your country/region, other formats for electronic payments may be available.</span></span>   

 <span data-ttu-id="7093d-107">Pour activer les virements SEPA, vous devez d'abord créer un compte bancaire, un fournisseur, et le lot de feuille général sur laquelle la feuille de paiements est basée.</span><span class="sxs-lookup"><span data-stu-id="7093d-107">To enable SEPA credit transfers, you must first set up a bank account, a vendor, and the general journal batch that the payment journal is based on.</span></span> <span data-ttu-id="7093d-108">Vous préparez ensuite les paiements aux fournisseurs en renseignant automatiquement la fenêtre **Feuille paiement** avec les paiements dus aux dates comptabilisation spécifiées.</span><span class="sxs-lookup"><span data-stu-id="7093d-108">You then prepare payments to vendors by automatically filling the **Payment Journal** window with due payments with specified posting dates.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="7093d-109">Lorsque vous avez vérifié que les paiements sont traités avec succès par la banque, vous pouvez passer aux lignes feuille paiement.</span><span class="sxs-lookup"><span data-stu-id="7093d-109">When you have verified that the payments are successfully processed by the bank, you can proceed to post the payment journal lines.</span></span>  

 <span data-ttu-id="7093d-110">Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.</span><span class="sxs-lookup"><span data-stu-id="7093d-110">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="7093d-111">**Pour**</span><span class="sxs-lookup"><span data-stu-id="7093d-111">**To**</span></span>|<span data-ttu-id="7093d-112">**Voir**</span><span class="sxs-lookup"><span data-stu-id="7093d-112">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="7093d-113">Activez la fonctionnalité du service de conversion de données bancaires pour convertir les fichiers de relevé bancaire dans un format que vous pouvez importer, ou pour convertir les fichiers de paiement exportés au format imposé par votre banque.</span><span class="sxs-lookup"><span data-stu-id="7093d-113">Activate the Bank Data Conversion Service feature to have any bank statement file converted to a format that you can import or to have your exported payment files converted to the format that your bank requires.</span></span>|[<span data-ttu-id="7093d-114">Procédure : configurer le service de conversion de données bancaires</span><span class="sxs-lookup"><span data-stu-id="7093d-114">How to: Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)|  
|<span data-ttu-id="7093d-115">Configurez un compte bancaire, un fournisseur et une feuille paiement pour le virement SEPA.</span><span class="sxs-lookup"><span data-stu-id="7093d-115">Set up a bank account, a vendor, and a payment journal for SEPA credit transfer.</span></span>|[<span data-ttu-id="7093d-116">Procédure : configurer des virements SEPA</span><span class="sxs-lookup"><span data-stu-id="7093d-116">How to: Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)|  
|<span data-ttu-id="7093d-117">Renseignez la feuille paiement avec des lignes pour les paiements dus aux fournisseurs, avec la possibilité d'insérer des dates comptabilisation sur la base de la date d'échéance des documents achat associés.</span><span class="sxs-lookup"><span data-stu-id="7093d-117">Fill the payment journal with lines for due payments to vendors, with the option to insert posting dates based on the due date of the related purchase documents.</span></span>|[<span data-ttu-id="7093d-118">Gestion des comptes fournisseur</span><span class="sxs-lookup"><span data-stu-id="7093d-118">Manage Payables</span></span>](payables-manage-payables.md)|  
|<span data-ttu-id="7093d-119">Exportez les lignes feuille paiement dans un fichier au format virement SEPA.</span><span class="sxs-lookup"><span data-stu-id="7093d-119">Export payment journal lines to a file in the SEPA Credit Transfer format.</span></span>|[<span data-ttu-id="7093d-120">Procédure : exportation de paiements vers un fichier bancaire</span><span class="sxs-lookup"><span data-stu-id="7093d-120">How to: Export Payments to a Bank File</span></span>](payables-how-export-payments-bank-file.md)|  
|<span data-ttu-id="7093d-121">Examinez quels les paiements ont été exportés et dans quels fichiers.</span><span class="sxs-lookup"><span data-stu-id="7093d-121">Review which payments have been exported and into which files.</span></span>|<span data-ttu-id="7093d-122">Registres virement</span><span class="sxs-lookup"><span data-stu-id="7093d-122">Credit Transfer Registers</span></span>|  
|<span data-ttu-id="7093d-123">Lorsque le paiement électronique est traité avec succès par la banque, validez les paiements.</span><span class="sxs-lookup"><span data-stu-id="7093d-123">When the electronic payment is successfully processed by the bank, post the payments.</span></span>|[<span data-ttu-id="7093d-124">Utilisation de feuilles comptabilité</span><span class="sxs-lookup"><span data-stu-id="7093d-124">Working with General Journals</span></span>](ui-work-general-journals.md)|  

## <a name="see-also"></a><span data-ttu-id="7093d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7093d-125">See Also</span></span>  
[<span data-ttu-id="7093d-126">Procédure : configurer le service de conversion de données bancaires</span><span class="sxs-lookup"><span data-stu-id="7093d-126">How to: Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)  
[<span data-ttu-id="7093d-127">Procédure : configurer des virements SEPA</span><span class="sxs-lookup"><span data-stu-id="7093d-127">How to: Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)  
<span data-ttu-id="7093d-128">[Gestion des comptes fournisseur](payables-manage-payables.md) </span><span class="sxs-lookup"><span data-stu-id="7093d-128">[Manage Payables](payables-manage-payables.md) </span></span>  
[<span data-ttu-id="7093d-129">Utilisation de feuilles comptabilité</span><span class="sxs-lookup"><span data-stu-id="7093d-129">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="7093d-130">Recouvrement de paiements par prélèvement automatique SEPA</span><span class="sxs-lookup"><span data-stu-id="7093d-130">Collect Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)   

