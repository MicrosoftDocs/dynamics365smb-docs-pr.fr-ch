---
title: "Résolution des problèmes : Intégration à Microsoft Flow | Microsoft Docs"
description: "Vous pouvez modifier la façon de rendre vos données Business Central disponibles sous forme de source de données et spécifier une URL OData de vos services Web pour générer un flux de travail automatisé."
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: e3917573a912a4e51416c4e926443c87513728fe
ms.openlocfilehash: 80bc35f6ea8c4264c2cd8960be3370e5966b88e3
ms.contentlocale: fr-ch
ms.lasthandoff: 06/01/2018

---
# <a name="troubleshooting-integration-with-microsoft-flow---request-url-too-long"></a><span data-ttu-id="4d3af-103">Résolution des problèmes : Intégration à Microsoft Flow - URL de demande trop longue</span><span class="sxs-lookup"><span data-stu-id="4d3af-103">Troubleshooting Integration with Microsoft Flow - Request URL Too Long</span></span>
<span data-ttu-id="4d3af-104">Vous pouvez utiliser vos données [!INCLUDE[d365fin](includes/d365fin_md.md)] en tant que partie du flux de travail dans Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="4d3af-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="4d3af-105">Vous devez disposer d'un compte valide avec [!INCLUDE[d365fin](includes/d365fin_md.md)] et avec Flow.</span><span class="sxs-lookup"><span data-stu-id="4d3af-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

<span data-ttu-id="4d3af-106">Si vous créez un Microsoft Flow à l'aide du connecteur [!INCLUDE[d365fin](includes/d365fin_md.md)], vous risquez de recevoir un message d'erreur indiquant que l'URL demandée est trop longue après avoir créé le flux, comme par exemple : **RequestUriTooLong**.</span><span class="sxs-lookup"><span data-stu-id="4d3af-106">If you are creating a Microsoft Flow using the [!INCLUDE[d365fin](includes/d365fin_md.md)] connector, you may receive an error message stating that the requsted URL is too long after creating the flow, such as the following: **RequestUriTooLong**.</span></span>

## <a name="cause"></a><span data-ttu-id="4d3af-107">Motif</span><span class="sxs-lookup"><span data-stu-id="4d3af-107">Cause</span></span>
<span data-ttu-id="4d3af-108">Pour déclencher un flux, les modifications apportées à vos données font l'objet d'une recherche.</span><span class="sxs-lookup"><span data-stu-id="4d3af-108">For a flow to trigger, it looks for changes in your data.</span></span> <span data-ttu-id="4d3af-109">Quand les connecteurs déterminent si vos données ont été modifiées, ils comparent les données mises en cache aux données aux nouvelles données demandées à partir du document origine.</span><span class="sxs-lookup"><span data-stu-id="4d3af-109">When determining if your data has changed, the connectors compare the cached data to the new data requested from the source.</span></span>  

<span data-ttu-id="4d3af-110">Si la demande de données crée une URL qui est trop longue, elle échouera.</span><span class="sxs-lookup"><span data-stu-id="4d3af-110">If the data request creates a URL that is too long, it will fail.</span></span> <span data-ttu-id="4d3af-111">Parmi les causes courantes on trouve :</span><span class="sxs-lookup"><span data-stu-id="4d3af-111">Common causes may include:</span></span>
- <span data-ttu-id="4d3af-112">En général, toutes les tables source contenant plus de 250 lignes</span><span class="sxs-lookup"><span data-stu-id="4d3af-112">Generally, any source table with over 250 rows</span></span>
- <span data-ttu-id="4d3af-113">Les tables source contenant plusieurs milliers d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="4d3af-113">Source tables containing multiple thousands of records</span></span>

## <a name="workaround"></a><span data-ttu-id="4d3af-114">Solution de contournement</span><span class="sxs-lookup"><span data-stu-id="4d3af-114">Workaround</span></span>
<span data-ttu-id="4d3af-115">Suivez ces étapes pour résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="4d3af-115">Follow these steps as a workaround.</span></span>
1. <span data-ttu-id="4d3af-116">Modifiez le flux qui échoue.</span><span class="sxs-lookup"><span data-stu-id="4d3af-116">Choose to edit the flow that is failing.</span></span>
2. <span data-ttu-id="4d3af-117">Développez **Afficher les options avancées** dans le déclencheur de flux.</span><span class="sxs-lookup"><span data-stu-id="4d3af-117">Expand the **Show advanced options** on the flow trigger.</span></span>
3. <span data-ttu-id="4d3af-118">Dans le champ **Ignorer le nombre**, indiquez le nombre d'enregistrements à ignorer.</span><span class="sxs-lookup"><span data-stu-id="4d3af-118">In the **Skip Count** field, enter the number of records to skip.</span></span>  
<span data-ttu-id="4d3af-119">Par exemple, si la table que vous utilisez comme source de données contient 4 000 enregistrements, saisissez 4 000 comme nombre d'enregistrements à ignorer.</span><span class="sxs-lookup"><span data-stu-id="4d3af-119">For example, if the table that you are using as a data source has 4,000 records, enter 4,000 as the number of records to skip.</span></span>
4. <span data-ttu-id="4d3af-120">Mettez votre flux à jour.</span><span class="sxs-lookup"><span data-stu-id="4d3af-120">Update your flow.</span></span>

> [!NOTE]  
> <span data-ttu-id="4d3af-121">Le connecteur est actuellement en version Bêta.</span><span class="sxs-lookup"><span data-stu-id="4d3af-121">The connector is currently in Beta.</span></span> <span data-ttu-id="4d3af-122">Des mises à jour sur la façon dont les modifications sont apportées aux données sont prévues dans une prochaine version.</span><span class="sxs-lookup"><span data-stu-id="4d3af-122">Updates to how data changes are targeted for a future release.</span></span>


## <a name="see-also"></a><span data-ttu-id="4d3af-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d3af-123">See Also</span></span>
<span data-ttu-id="4d3af-124">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] dans un flux automatisé](across-how-use-financials-data-source-flow.md)</span><span class="sxs-lookup"><span data-stu-id="4d3af-124">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow](across-how-use-financials-data-source-flow.md)</span></span>  
[<span data-ttu-id="4d3af-125">Mise en route</span><span class="sxs-lookup"><span data-stu-id="4d3af-125">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="4d3af-126">Importation des données métier à partir d'autres systèmes financiers</span><span class="sxs-lookup"><span data-stu-id="4d3af-126">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="4d3af-127">[Gérer les utilisateurs et les autorisations](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="4d3af-127">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="4d3af-128">[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="4d3af-128">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="4d3af-129">Finances</span><span class="sxs-lookup"><span data-stu-id="4d3af-129">Finance</span></span>](finance.md)  

