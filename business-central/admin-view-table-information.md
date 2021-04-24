---
title: Afficher les informations sur les tables
description: Découvrez comment afficher des informations sur les tables de base de données directement depuis l’interface client de Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 7a01143dd7928d5996c1620676a758ea634bdf5d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776906"
---
# <a name="viewing-table-information"></a><span data-ttu-id="4d965-103">Affichage d’informations sur les tables</span><span class="sxs-lookup"><span data-stu-id="4d965-103">Viewing Table Information</span></span>

<span data-ttu-id="4d965-104">La page **Informations sur les tables 8700** fournit des informations sur toutes les tables système et métier d’une solution Business Central.</span><span class="sxs-lookup"><span data-stu-id="4d965-104">The page **8700 Table Information** provides information about all system and business tables in a Business Central solution.</span></span> <span data-ttu-id="4d965-105">En particulier, la page affiche des informations sur la quantité de données contenues dans les tables.</span><span class="sxs-lookup"><span data-stu-id="4d965-105">In particular, the page displays information about the amount of data the tables contain.</span></span>

<span data-ttu-id="4d965-106">Ces informations sont utiles pour résoudre les problèmes de performances, car nous allons voir la répartition de la taille des données entre les tables.</span><span class="sxs-lookup"><span data-stu-id="4d965-106">This information is useful for troubleshooting performance problems, because let's you see the distribution of data size across tables.</span></span>

## <a name="viewing-table-information"></a><span data-ttu-id="4d965-107">Affichage d’informations sur les tables</span><span class="sxs-lookup"><span data-stu-id="4d965-107">Viewing table information</span></span>

<span data-ttu-id="4d965-108">Pour ouvrir cette page, sélectionnez l’icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Icône Page ou état pour la recherche"), entrez **Informations sur les tables**, puis sélectionnez le lien connexe.</span><span class="sxs-lookup"><span data-stu-id="4d965-108">To open this page, select the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Table Information**, and then choose the related link.</span></span>

<span data-ttu-id="4d965-109">Le tableau suivant décrit les informations fournies pour chaque table :</span><span class="sxs-lookup"><span data-stu-id="4d965-109">The following table describes the information provided for each table:</span></span>

|<span data-ttu-id="4d965-110">Colonne</span><span class="sxs-lookup"><span data-stu-id="4d965-110">Column</span></span>|<span data-ttu-id="4d965-111">Description</span><span class="sxs-lookup"><span data-stu-id="4d965-111">Description</span></span>|
|------|-----------|
|<span data-ttu-id="4d965-112">Nom de la société</span><span class="sxs-lookup"><span data-stu-id="4d965-112">Company Name</span></span>|<span data-ttu-id="4d965-113">Nom de la société, si existant, à laquelle appartient la table.</span><span class="sxs-lookup"><span data-stu-id="4d965-113">The name of the company, if any, that the table belongs to.</span></span>|
|<span data-ttu-id="4d965-114">Nom de la table</span><span class="sxs-lookup"><span data-stu-id="4d965-114">Table Name</span></span>|<span data-ttu-id="4d965-115">Nom de la table.</span><span class="sxs-lookup"><span data-stu-id="4d965-115">The name of the table.</span></span>|
|<span data-ttu-id="4d965-116">Numéro table</span><span class="sxs-lookup"><span data-stu-id="4d965-116">Table No.</span></span>|<span data-ttu-id="4d965-117">ID unique de la table</span><span class="sxs-lookup"><span data-stu-id="4d965-117">The ID of the table</span></span>|
|<span data-ttu-id="4d965-118">Non.</span><span class="sxs-lookup"><span data-stu-id="4d965-118">No.</span></span> <span data-ttu-id="4d965-119">d’enregistrements</span><span class="sxs-lookup"><span data-stu-id="4d965-119">of Records</span></span>|<span data-ttu-id="4d965-120">Nombre total d’enregistrements stockés dans la table.</span><span class="sxs-lookup"><span data-stu-id="4d965-120">The total number of records stored in the table.</span></span>|
|<span data-ttu-id="4d965-121">Taille enregistrement</span><span class="sxs-lookup"><span data-stu-id="4d965-121">Record Size</span></span>|<span data-ttu-id="4d965-122">La taille d’enregistrement moyenne en Ko/enregistrement.</span><span class="sxs-lookup"><span data-stu-id="4d965-122">The average record size in KB/record.</span></span> <span data-ttu-id="4d965-123">La valeur est calculée à l’aide de la formule suivante : 1024 (Taille)/N°</span><span class="sxs-lookup"><span data-stu-id="4d965-123">The value is calculated using the following formula: 1024(Size)/(No.</span></span> <span data-ttu-id="4d965-124">d’enregistrements)\`.</span><span class="sxs-lookup"><span data-stu-id="4d965-124">of Records)\`.</span></span> |

## <a name="see-also"></a><span data-ttu-id="4d965-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d965-125">See Also</span></span>

[<span data-ttu-id="4d965-126">Inspection des pages</span><span class="sxs-lookup"><span data-stu-id="4d965-126">Inspecting Pages</span></span>](across-inspect-page.md)  
[<span data-ttu-id="4d965-127">Articles sur les performances pour les développeurs</span><span class="sxs-lookup"><span data-stu-id="4d965-127">Performance Articles For Developers</span></span>](/dynamics365/business-central/dev-itpro/performance/performance-developer)  


[!INCLUDE[footer-include](includes/footer-banner.md)]