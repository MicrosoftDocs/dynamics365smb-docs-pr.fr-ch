---
title: Afficher les verrouillages base de données
description: Découvrez comment afficher des informations sur les verrouillages de base de données directement depuis l’interface client de Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: b53677ab57d6c48b015bb0dd47ea6e315f8e80c3
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776931"
---
# <a name="viewing-database-locks"></a><span data-ttu-id="c3eb3-103">Affichage des verrouillages base de données</span><span class="sxs-lookup"><span data-stu-id="c3eb3-103">Viewing Database Locks</span></span>

<span data-ttu-id="c3eb3-104">Les verrouillages base de données contrôlent l’accès simultané de plusieurs utilisateurs aux mêmes données.</span><span class="sxs-lookup"><span data-stu-id="c3eb3-104">Database locking controls access by multiple users to the same data at the same time.</span></span> <span data-ttu-id="c3eb3-105">Pour protéger une transaction contre d’autres transactions modifiant les mêmes données, la première transaction met un verrouillage sur les données.</span><span class="sxs-lookup"><span data-stu-id="c3eb3-105">To protect a transaction against other transactions modifying the same data, the first transaction puts a lock on the data.</span></span> <span data-ttu-id="c3eb3-106">Le verrouillage reste en place jusqu’à la fin de la transaction.</span><span class="sxs-lookup"><span data-stu-id="c3eb3-106">The lock remains until the transaction's done.</span></span>

<span data-ttu-id="c3eb3-107">Les utilisateurs peuvent être empêchés d’effectuer des transactions sur les données verrouillées.</span><span class="sxs-lookup"><span data-stu-id="c3eb3-107">Users may be blocked from completing transactions on the locked data.</span></span> <span data-ttu-id="c3eb3-108">Ils reçoivent généralement un message indiquant la condition de verrouillage.</span><span class="sxs-lookup"><span data-stu-id="c3eb3-108">They'll typically get a message that indicates the lock condition.</span></span>

## <a name="to-view-database-locks"></a><span data-ttu-id="c3eb3-109">Pour afficher les verrouillages base de données</span><span class="sxs-lookup"><span data-stu-id="c3eb3-109">To view database locks</span></span>

<span data-ttu-id="c3eb3-110">Sélectionnez l’icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), saisissez **Verrouillages base de données**, puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="c3eb3-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Database Locks**, and then choose the related link.</span></span>

<span data-ttu-id="c3eb3-111">La page **Verrouillages base de données** affiche un aperçu de tous les verrouillages base de données actuels.</span><span class="sxs-lookup"><span data-stu-id="c3eb3-111">The **Database Locks** page gives snapshot of all current database locks.</span></span>

<span data-ttu-id="c3eb3-112">Pour en savoir plus sur les verrouillages base de données, consultez [Surveillance des verrouillages base de données](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) dans l’aide Business Central sur Developer and IT Pro.</span><span class="sxs-lookup"><span data-stu-id="c3eb3-112">For more information about database locking, see [Monitoring Database Locks](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) in the Business Central Developer and IT Pro help.</span></span>

## <a name="see-also"></a><span data-ttu-id="c3eb3-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3eb3-113">See Also</span></span>

[<span data-ttu-id="c3eb3-114">Surveiller les verrouillages base de données</span><span class="sxs-lookup"><span data-stu-id="c3eb3-114">Monitor Database Locks</span></span>](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 


[!INCLUDE[footer-include](includes/footer-banner.md)]