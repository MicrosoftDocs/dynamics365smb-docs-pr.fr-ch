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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: d79ef7c076ec3a529aeb0c679b8b61658ef65af5
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315363"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="c1e88-103">Extension Envestnet Yodlee Bank Feeds</span><span class="sxs-lookup"><span data-stu-id="c1e88-103">The Envestnet Yodlee Bank Feeds Extension</span></span>
<span data-ttu-id="c1e88-104">Pour rapprocher rapidement des paiements effectués sur vos comptes bancaires, le service Envestnet Yodlee Bank Feeds vous permet de lier votre compte bancaire système à votre compte bancaire en ligne.</span><span class="sxs-lookup"><span data-stu-id="c1e88-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="c1e88-105">Cela signifie que le dernier relevé bancaire est automatiquement ou manuellement entré dans votre feuille rapprochement, garantissant que vous traitez toujours les derniers paiements avec un risque minimal d'erreurs.</span><span class="sxs-lookup"><span data-stu-id="c1e88-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

<span data-ttu-id="c1e88-106">Le service Envestnet Yodlee Bank Feeds n'est pris en charge qu'aux États-Unis et au Canada.</span><span class="sxs-lookup"><span data-stu-id="c1e88-106">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>

> [!NOTE]
> <span data-ttu-id="c1e88-107">Cette fonctionnalité est seulement prise en charge dans la version en ligne de Business Central.</span><span class="sxs-lookup"><span data-stu-id="c1e88-107">This functionality is only supported in the online version of Business Central.</span></span> <span data-ttu-id="c1e88-108">Pour utiliser cette fonctionnalité sur site, vous devez obtenir un compte de cobrand d'Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="c1e88-108">To use this functionality on-premise, you must obtain a cobrand account from Envestnet Yodlee.</span></span><br /><br />

> [!IMPORTANT]
> <span data-ttu-id="c1e88-109">En raison de la nouvelle directive sur les services de paiement en Europe (PSD2), après le 14 septembre 2019, vous ne pourrez plus importer automatiquement des relevés bancaires de banques du Royaume-Uni vers [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c1e88-109">Due to the new Payment Services Directive in Europe (PSD2), after September 14, 2019, you will no longer be able to automatically import bank statements from banks in the United Kingdom into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="c1e88-110">Nous étudions la possibilité de proposer cette fonctionnalité à l'avenir.</span><span class="sxs-lookup"><span data-stu-id="c1e88-110">We are looking into the possibility of offering this feature again in the future.</span></span>

<span data-ttu-id="c1e88-111">Le service Envestnet Yodlee Bank Feeds offre les avantages suivants :</span><span class="sxs-lookup"><span data-stu-id="c1e88-111">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="c1e88-112">Supprime les besoins de saisie manuelle.</span><span class="sxs-lookup"><span data-stu-id="c1e88-112">Removes the need for manual entry.</span></span>
* <span data-ttu-id="c1e88-113">Améliore l'efficacité et la précision lors des rapprochements de paiements.</span><span class="sxs-lookup"><span data-stu-id="c1e88-113">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="c1e88-114">Prend en charge un grand nombre de banques.</span><span class="sxs-lookup"><span data-stu-id="c1e88-114">Supports a large number of banks.</span></span>
* <span data-ttu-id="c1e88-115">Permet de bénéficier d'informations à jour relatives aux transactions bancaires au sein de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c1e88-115">Allows up-to-date information about bank transactions from within [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
* <span data-ttu-id="c1e88-116">Prend en charge les flux bancaires manuels comme automatiques.</span><span class="sxs-lookup"><span data-stu-id="c1e88-116">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="c1e88-117">Permet la sous-traitance des rapprochements de paiement à un comptable en donnant l'accès aux relevés bancaires.</span><span class="sxs-lookup"><span data-stu-id="c1e88-117">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

<span data-ttu-id="c1e88-118">Pour plus d'informations, voir [Configurer le service Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="c1e88-118">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c1e88-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1e88-119">See Also</span></span>
<span data-ttu-id="c1e88-120">[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l'aide des extensions ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="c1e88-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="c1e88-121">Lettrage automatique des paiements et rapprochement des comptes bancaires</span><span class="sxs-lookup"><span data-stu-id="c1e88-121">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="c1e88-122">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c1e88-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
