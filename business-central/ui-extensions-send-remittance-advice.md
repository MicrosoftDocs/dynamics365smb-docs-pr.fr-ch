---
title: Extension Envoyer un avis de remise | Microsoft Docs
description: Décrit l'extension Envoyer un avis de remise, qui permet d'envoyer par e-mail un avis de remise à partir de la feuille paiement et et de le renvoyer à partir des écritures comptables fournisseur.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, remittance, advice
ms.date: 05/05/2020
ms.author: edupont
ms.openlocfilehash: 236cb83e99c2385edc09622255037a152bf41e6e
ms.sourcegitcommit: 57e31a8b92feeaf8c6c63eba147f36b38eee7679
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 05/06/2020
ms.locfileid: "3339937"
---
# <a name="send-remittance-advice"></a><span data-ttu-id="29328-103">Envoyer un avis de remise</span><span class="sxs-lookup"><span data-stu-id="29328-103">Send Remittance Advice</span></span>

<span data-ttu-id="29328-104">Lorsqu'un avis de remise est utilisé pour informer les fournisseurs des paiements effectués, vous pouvez désormais envoyer par e-mail un avis de remise en bloc à partir de la feuille paiement et le renvoyer une fois les paiements effectués à partir des écritures comptables fournisseur à l'aide de profils d'envoi de documents.</span><span class="sxs-lookup"><span data-stu-id="29328-104">Where remittance advice is used to notify vendors of payments being made, you can now email remittance advice in bulk from the payment journal as well as resend after payments are made from vendor ledger entries by using document sending profiles.</span></span>

> [!NOTE]
> <span data-ttu-id="29328-105">Cette fonctionnalité est uniquement prise en charge dans Business Central en ligne et local dans les pays suivants : Royaume-Uni, États-Unis, Canada, Australie, Nouvelle-Zélande et Afrique du Sud.</span><span class="sxs-lookup"><span data-stu-id="29328-105">This functionality is only supported in Business Central online and on-premises in following countries: United Kingdom, United States, Canada, Australia, New Zealand, and South Africa.</span></span>  

<span data-ttu-id="29328-106">Vous pouvez envoyer des avis de remise de deux manières différentes :</span><span class="sxs-lookup"><span data-stu-id="29328-106">You can send remittance advice in two different ways:</span></span>

* <span data-ttu-id="29328-107">Dans la page **Feuille paiement**, choisissez **Naviguer**, **Paiements**, **Envoyer un avis de paiement** pour envoyer un avis de remise pour une ou plusieurs lignes feuille paiement</span><span class="sxs-lookup"><span data-stu-id="29328-107">In the **Payment Journal** page, choose **Navigate**, **Payments**, **Send Remittance Advice** to email remittance advice for one or multiple payment journal lines</span></span>
* <span data-ttu-id="29328-108">Dans la page **Écritures comptables fournisseur**, sélectionnez **Actions**, **Fonctions**, **Envoyer un avis de remise** pour envoyer par e-mail un avis de remise après validation des paiements fournisseur, pour une ou plusieurs écritures comptables fournisseur</span><span class="sxs-lookup"><span data-stu-id="29328-108">In the **Vendor Ledger Entries** page, choose **Actions**, **Functions**, **Send Remittance Advice** to email remittance advice after posting of vendor payments, for one or multiple vendor ledger entries</span></span>

## <a name="see-also"></a><span data-ttu-id="29328-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29328-109">See Also</span></span>

[<span data-ttu-id="29328-110">Proposer paiements fournisseur</span><span class="sxs-lookup"><span data-stu-id="29328-110">Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md)  
<span data-ttu-id="29328-111">[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide des extensions ](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="29328-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  
<span data-ttu-id="29328-112">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="29328-112">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="29328-113">Envoyer des documents par e-mail</span><span class="sxs-lookup"><span data-stu-id="29328-113">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
