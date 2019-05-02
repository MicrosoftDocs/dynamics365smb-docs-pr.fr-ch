---
title: Procédure de vérification et de personnalisation des données existantes de base de données | Microsoft Docs
description: Lors de la création d’un package configuration pour une solution, vous pouvez consulter et personnaliser les données de base de données disponibles pour les adapter aux besoins de votre client. La table de base de données doit être associée à une page.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: admin-how-to-create-custom-company-configuration-packages
ms.openlocfilehash: 1f49d437e03ecf45a234574530f1e65d93584dea
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 03/08/2019
ms.locfileid: "820609"
---
# <a name="review-and-customize-existing-database-data"></a><span data-ttu-id="ba9db-104">Vérifier et personnaliser les données existantes de base de données</span><span class="sxs-lookup"><span data-stu-id="ba9db-104">Review and Customize Existing Database Data</span></span>
<span data-ttu-id="ba9db-105">Lors de la création d’un package configuration pour une solution, vous pouvez consulter et personnaliser les données de base de données disponibles pour les adapter aux besoins de votre client.</span><span class="sxs-lookup"><span data-stu-id="ba9db-105">As you create a configuration package for a solution, you can view and customize the available database data to suit your customer needs.</span></span> <span data-ttu-id="ba9db-106">La table de base de données doit être associée à une page.</span><span class="sxs-lookup"><span data-stu-id="ba9db-106">The database table has to have an associated page.</span></span>  

### <a name="to-customize-data-in-the-database"></a><span data-ttu-id="ba9db-107">Pour personnaliser des données dans la base de données</span><span class="sxs-lookup"><span data-stu-id="ba9db-107">To customize data in the database</span></span>  

1.  <span data-ttu-id="ba9db-108">Dans la feuille configuration, identifiez les tables dont vous souhaitez afficher ou personnaliser les données.</span><span class="sxs-lookup"><span data-stu-id="ba9db-108">In the configuration worksheet, identify the tables whose data that you want to view or customize.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="ba9db-109">Assurez-vous que chaque table dispose d’un ID page qui lui est affecté.</span><span class="sxs-lookup"><span data-stu-id="ba9db-109">Make sure that each table has a page ID assigned to it.</span></span> <span data-ttu-id="ba9db-110">Pour les tables [!INCLUDE[d365fin](includes/d365fin_md.md)] standard, cette valeur est automatiquement insérée.</span><span class="sxs-lookup"><span data-stu-id="ba9db-110">For standard [!INCLUDE[d365fin](includes/d365fin_md.md)] tables, this value is automatically filled in.</span></span> <span data-ttu-id="ba9db-111">Pour les tables personnalisées, vous devez fournir l'ID.</span><span class="sxs-lookup"><span data-stu-id="ba9db-111">For custom tables, you have to provide the ID.</span></span>  

2.  <span data-ttu-id="ba9db-112">Sous l’onglet **Actions**, dans le groupe **Afficher**, choisissez **Données de base de données**.</span><span class="sxs-lookup"><span data-stu-id="ba9db-112">On the **Actions** tab, in the **Show** group, choose **Database Data**.</span></span>  

     <span data-ttu-id="ba9db-113">La page [!INCLUDE[d365fin](includes/d365fin_md.md)] pour la page s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="ba9db-113">The [!INCLUDE[d365fin](includes/d365fin_md.md)] page for the page opens.</span></span>  

3.  <span data-ttu-id="ba9db-114">Révisez les informations disponibles.</span><span class="sxs-lookup"><span data-stu-id="ba9db-114">Review the available information.</span></span> <span data-ttu-id="ba9db-115">Modifiez-les selon vos besoins en supprimant les enregistrements qui ne sont pas appropriés ou en ajoutant de nouveaux enregistrements.</span><span class="sxs-lookup"><span data-stu-id="ba9db-115">Modify it as necessary by deleting records that are not relevant or by adding new ones.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ba9db-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba9db-116">See Also</span></span>  
 [<span data-ttu-id="ba9db-117">Gérer la configuration de la société dans une feuille</span><span class="sxs-lookup"><span data-stu-id="ba9db-117">Manage Company Configuration in a Worksheet</span></span>](admin-how-to-manage-company-configuration-in-a-worksheet.md)