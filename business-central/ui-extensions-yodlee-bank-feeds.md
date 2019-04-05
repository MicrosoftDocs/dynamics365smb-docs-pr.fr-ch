---
title: Rapprochement de paiement avec l'extension Envestnet Yodlee Bank Feeds | Microsoft Docs
description: Décrit l'extension Envestnet Yodlee Bank Feeds, qui établit des liaisons avec les comptes bancaires afin que vous puissiez rapidement rapprocher les paiements.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 02/26/2019
ms.author: sgroespe
ms.openlocfilehash: 36400b3265517c29f68f7eb59d17d968334e0fb1
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "821584"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="d2938-103">L'extension Envestnet Yodlee Bank Feeds</span><span class="sxs-lookup"><span data-stu-id="d2938-103">The Envestnet Yodlee Bank Feeds Extension</span></span>
<span data-ttu-id="d2938-104">Pour rapprocher rapidement des paiements effectués sur vos comptes bancaires, le service Envestnet Yodlee Bank Feeds vous permet de lier votre compte bancaire système à votre compte bancaire en ligne.</span><span class="sxs-lookup"><span data-stu-id="d2938-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="d2938-105">Cela signifie que le dernier relevé bancaire est automatiquement ou manuellement entré dans votre feuille rapprochement, garantissant que vous traitez toujours les derniers paiements avec un risque minimal d'erreurs.</span><span class="sxs-lookup"><span data-stu-id="d2938-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

> [!NOTE]
> <span data-ttu-id="d2938-106">Cette fonctionnalité est seulement prise en charge dans la version en ligne de Business Central.</span><span class="sxs-lookup"><span data-stu-id="d2938-106">This functionality is only supported in the online version of Business Central.</span></span> <span data-ttu-id="d2938-107">Pour utiliser cette fonctionnalité sur site, vous devez obtenir un compte de cobrand d'Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="d2938-107">To use this functionality on-premise, you must obtain a cobrand account from Envestnet Yodlee.</span></span>

<span data-ttu-id="d2938-108">Le service Envestnet Yodlee Bank Feeds fournit les avantages suivants :</span><span class="sxs-lookup"><span data-stu-id="d2938-108">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="d2938-109">Supprime les besoins de saisie manuelle.</span><span class="sxs-lookup"><span data-stu-id="d2938-109">Removes the need for manual entry.</span></span>
* <span data-ttu-id="d2938-110">Améliore l'efficacité et la précision lors des rapprochements de paiements.</span><span class="sxs-lookup"><span data-stu-id="d2938-110">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="d2938-111">Prend en charge un grand nombre de banques.</span><span class="sxs-lookup"><span data-stu-id="d2938-111">Supports a large number of banks.</span></span>
* <span data-ttu-id="d2938-112">Permet de bénéficier d'informations à jour relatives aux transactions bancaires au sein de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d2938-112">Allows up-to-date information about bank transactions from within [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
* <span data-ttu-id="d2938-113">Prend en charge les flux bancaires manuels comme automatiques.</span><span class="sxs-lookup"><span data-stu-id="d2938-113">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="d2938-114">Permet la sous-traitance des rapprochements de paiement à un comptable en donnant l'accès aux relevés bancaires.</span><span class="sxs-lookup"><span data-stu-id="d2938-114">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

<span data-ttu-id="d2938-115">Pour plus d'informations, voir [Configurer le service de flux de la Envestnet Yodlee Bank](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="d2938-115">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d2938-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2938-116">See Also</span></span>
<span data-ttu-id="d2938-117">[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide des extensions ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="d2938-117">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="d2938-118">Lettrage automatique des paiements et rapprochement des comptes bancaires</span><span class="sxs-lookup"><span data-stu-id="d2938-118">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="d2938-119">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d2938-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
