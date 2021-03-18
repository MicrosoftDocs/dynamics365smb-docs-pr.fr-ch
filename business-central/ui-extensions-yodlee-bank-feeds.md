---
title: Rapprochement de paiement avec l’extension Envestnet Yodlee Bank Feeds
description: Décrit l’extension Envestnet Yodlee Bank Feeds, qui établit des liaisons avec les comptes bancaires afin que vous puissiez rapidement rapprocher les paiements.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 946958669f4554869e171286927bf498fe62a7ed
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5394039"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="22a85-103">Extension Envestnet Yodlee Bank Feeds</span><span class="sxs-lookup"><span data-stu-id="22a85-103">The Envestnet Yodlee Bank Feeds Extension</span></span>

<span data-ttu-id="22a85-104">Pour rapprocher rapidement des paiements effectués sur vos comptes bancaires, le service Envestnet Yodlee Bank Feeds vous permet de lier votre compte bancaire système à votre compte bancaire en ligne.</span><span class="sxs-lookup"><span data-stu-id="22a85-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="22a85-105">Cela signifie que le dernier relevé bancaire est automatiquement ou manuellement entré dans votre feuille rapprochement, garantissant que vous traitez toujours les derniers paiements avec un risque minimal d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="22a85-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

<span data-ttu-id="22a85-106">Le service Envestnet Yodlee Bank Feeds n’est pris en charge qu’aux États-Unis et au Canada.</span><span class="sxs-lookup"><span data-stu-id="22a85-106">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>

> [!NOTE]
> <span data-ttu-id="22a85-107">Le service Envestnet Yodlee Bank Feeds est uniquement pris en charge dans la version en ligne de Business Central.</span><span class="sxs-lookup"><span data-stu-id="22a85-107">The Envestnet Yodlee Bank Feeds service is only supported in the online version of Business Central.</span></span> <span data-ttu-id="22a85-108">Pour utiliser cette fonctionnalité sur site, vous devez obtenir un compte de cobrand d’Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="22a85-108">To use this functionality on-premises, you must obtain a cobrand account from Envestnet Yodlee.</span></span><br /><br />
> <span data-ttu-id="22a85-109">Le service Envestnet Yodlee Bank Feeds n’est pris en charge qu’aux États-Unis et au Canada.</span><span class="sxs-lookup"><span data-stu-id="22a85-109">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>
> <span data-ttu-id="22a85-110">Seules les banques résidant dans ces pays sont prises en charge, même si des banques d’autres pays peuvent apparaître dans la fenêtre de sélection des banques Envestnet Yodlee Bank Feeds dans [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="22a85-110">Only banks residing in these countries are supported, even though banks from other countries may appear in the Envestnet Yodlee Bank Feeds bank selection window in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

> [!IMPORTANT]
> <span data-ttu-id="22a85-111">En raison de la nouvelle directive sur les services de paiement en Europe (PSD2), après le 14 septembre 2019, vous ne pourrez plus importer automatiquement des relevés bancaires de banques du Royaume-Uni vers [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="22a85-111">Due to the new Payment Services Directive in Europe (PSD2), after September 14, 2019, you will no longer be able to automatically import bank statements from banks in the United Kingdom into [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="22a85-112">Nous étudions la possibilité de proposer cette fonctionnalité à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="22a85-112">We are looking into the possibility of offering this feature again in the future.</span></span>

<span data-ttu-id="22a85-113">Le service Envestnet Yodlee Bank Feeds offre les avantages suivants :</span><span class="sxs-lookup"><span data-stu-id="22a85-113">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="22a85-114">Supprime les besoins de saisie manuelle.</span><span class="sxs-lookup"><span data-stu-id="22a85-114">Removes the need for manual entry.</span></span>
* <span data-ttu-id="22a85-115">Améliore l’efficacité et la précision lors des rapprochements de paiements.</span><span class="sxs-lookup"><span data-stu-id="22a85-115">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="22a85-116">Prend en charge un grand nombre de banques.</span><span class="sxs-lookup"><span data-stu-id="22a85-116">Supports a large number of banks.</span></span>
* <span data-ttu-id="22a85-117">Permet de bénéficier d’informations à jour relatives aux transactions bancaires au sein de [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="22a85-117">Allows up-to-date information about bank transactions from within [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>
* <span data-ttu-id="22a85-118">Prend en charge les flux bancaires manuels comme automatiques.</span><span class="sxs-lookup"><span data-stu-id="22a85-118">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="22a85-119">Permet la sous-traitance des rapprochements de paiement à un comptable en donnant l’accès aux relevés bancaires.</span><span class="sxs-lookup"><span data-stu-id="22a85-119">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

## <a name="available-bank-feeds"></a><span data-ttu-id="22a85-120">Flux bancaires disponibles</span><span class="sxs-lookup"><span data-stu-id="22a85-120">Available Bank Feeds</span></span>
<span data-ttu-id="22a85-121">Vous pouvez vérifier si une banque est prise en charge en configurant et en vous connectant au service Envestnet Yodlee Bank Feeds.</span><span class="sxs-lookup"><span data-stu-id="22a85-121">You can check whether a bank is supported by setting up and connecting to the Envestnet Yodlee Bank Feeds service.</span></span> <span data-ttu-id="22a85-122">La banque s’affiche sur la liste si elle est prise en charge par Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="22a85-122">The bank will appear on the list if it is supported by Envestnet Yodlee.</span></span>

<span data-ttu-id="22a85-123">Pour plus d’informations, voir [Configurer le service Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="22a85-123">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="22a85-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22a85-124">See Also</span></span>
<span data-ttu-id="22a85-125">[Personnalisation de [!INCLUDE[prod_short](includes/prod_short.md)] à l’aide des extensions ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="22a85-125">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="22a85-126">Lettrage automatique des paiements et rapprochement des comptes bancaires</span><span class="sxs-lookup"><span data-stu-id="22a85-126">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="22a85-127">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="22a85-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]