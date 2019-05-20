---
title: Résolution des problèmes liés à l'intégration de Microsoft Flow | Microsoft Docs
description: Vous pouvez modifier la façon de rendre vos données Business Central disponibles sous forme de source de données et spécifier une URL OData de vos services Web pour générer un flux de travail automatisé.
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: 8a43df89261867f80ba16782cde92b040ce180c8
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 04/29/2019
ms.locfileid: "1240249"
---
# <a name="troubleshooting-integration-with-microsoft-flow---request-url-too-long"></a><span data-ttu-id="c25fb-103">Résolution des problèmes : Intégration à Microsoft Flow - URL de demande trop longue</span><span class="sxs-lookup"><span data-stu-id="c25fb-103">Troubleshooting Integration with Microsoft Flow - Request URL Too Long</span></span>
<span data-ttu-id="c25fb-104">Vous pouvez utiliser vos données [!INCLUDE[d365fin](includes/d365fin_md.md)] en tant que partie du flux de travail dans Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="c25fb-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="c25fb-105">Vous devez disposer d'un compte valide avec [!INCLUDE[d365fin](includes/d365fin_md.md)] et avec Flow.</span><span class="sxs-lookup"><span data-stu-id="c25fb-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

<span data-ttu-id="c25fb-106">Si vous créez un Microsoft Flow à l'aide du connecteur [!INCLUDE[d365fin](includes/d365fin_md.md)], vous risquez de recevoir un message d'erreur indiquant que l'URL demandée est trop longue après avoir créé le flux, comme par exemple : **RequestUriTooLong**.</span><span class="sxs-lookup"><span data-stu-id="c25fb-106">If you are creating a Microsoft Flow using the [!INCLUDE[d365fin](includes/d365fin_md.md)] connector, you may receive an error message stating that the requsted URL is too long after creating the flow, such as the following: **RequestUriTooLong**.</span></span>

## <a name="cause"></a><span data-ttu-id="c25fb-107">Motif</span><span class="sxs-lookup"><span data-stu-id="c25fb-107">Cause</span></span>
<span data-ttu-id="c25fb-108">Pour déclencher un flux, les modifications apportées à vos données font l'objet d'une recherche.</span><span class="sxs-lookup"><span data-stu-id="c25fb-108">For a flow to trigger, it looks for changes in your data.</span></span> <span data-ttu-id="c25fb-109">Quand les connecteurs déterminent si vos données ont été modifiées, ils comparent les données mises en cache aux données aux nouvelles données demandées à partir du document origine.</span><span class="sxs-lookup"><span data-stu-id="c25fb-109">When determining if your data has changed, the connectors compare the cached data to the new data requested from the source.</span></span>  

<span data-ttu-id="c25fb-110">Si la demande de données crée une URL qui est trop longue, elle échouera.</span><span class="sxs-lookup"><span data-stu-id="c25fb-110">If the data request creates a URL that is too long, it will fail.</span></span> <span data-ttu-id="c25fb-111">Parmi les causes courantes on trouve :</span><span class="sxs-lookup"><span data-stu-id="c25fb-111">Common causes may include:</span></span>
- <span data-ttu-id="c25fb-112">En général, toutes les tables source contenant plus de 250 lignes</span><span class="sxs-lookup"><span data-stu-id="c25fb-112">Generally, any source table with over 250 rows</span></span>
- <span data-ttu-id="c25fb-113">Les tables source contenant plusieurs milliers d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="c25fb-113">Source tables containing multiple thousands of records</span></span>

## <a name="workaround"></a><span data-ttu-id="c25fb-114">Solution de contournement</span><span class="sxs-lookup"><span data-stu-id="c25fb-114">Workaround</span></span>
<span data-ttu-id="c25fb-115">Suivez ces étapes pour résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="c25fb-115">Follow these steps as a workaround.</span></span>
1. <span data-ttu-id="c25fb-116">Modifiez le flux qui échoue.</span><span class="sxs-lookup"><span data-stu-id="c25fb-116">Choose to edit the flow that is failing.</span></span>
2. <span data-ttu-id="c25fb-117">Développez **Afficher les options avancées** dans le déclencheur de flux.</span><span class="sxs-lookup"><span data-stu-id="c25fb-117">Expand the **Show advanced options** on the flow trigger.</span></span>
3. <span data-ttu-id="c25fb-118">Dans le champ **Ignorer le nombre**, indiquez le nombre d'enregistrements à ignorer.</span><span class="sxs-lookup"><span data-stu-id="c25fb-118">In the **Skip Count** field, enter the number of records to skip.</span></span>  
<span data-ttu-id="c25fb-119">Par exemple, si la table que vous utilisez comme source de données contient 4 000 enregistrements, saisissez 4 000 comme nombre d'enregistrements à ignorer.</span><span class="sxs-lookup"><span data-stu-id="c25fb-119">For example, if the table that you are using as a data source has 4,000 records, enter 4,000 as the number of records to skip.</span></span>
4. <span data-ttu-id="c25fb-120">Mettez votre flux à jour.</span><span class="sxs-lookup"><span data-stu-id="c25fb-120">Update your flow.</span></span>

> [!NOTE]  
> <span data-ttu-id="c25fb-121">Le connecteur est actuellement en version Bêta.</span><span class="sxs-lookup"><span data-stu-id="c25fb-121">The connector is currently in Beta.</span></span> <span data-ttu-id="c25fb-122">Des mises à jour sur la façon dont les modifications sont apportées aux données sont prévues dans une prochaine version.</span><span class="sxs-lookup"><span data-stu-id="c25fb-122">Updates to how data changes are targeted for a future release.</span></span>


## <a name="see-also"></a><span data-ttu-id="c25fb-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c25fb-123">See Also</span></span>
<span data-ttu-id="c25fb-124">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] dans un flux automatisé](across-how-use-financials-data-source-flow.md)</span><span class="sxs-lookup"><span data-stu-id="c25fb-124">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow](across-how-use-financials-data-source-flow.md)</span></span>  
[<span data-ttu-id="c25fb-125">Mise en route</span><span class="sxs-lookup"><span data-stu-id="c25fb-125">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="c25fb-126">Importation des données métier à partir d'autres systèmes financiers</span><span class="sxs-lookup"><span data-stu-id="c25fb-126">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="c25fb-127">[Gestion des utilisateurs et des autorisations](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="c25fb-127">[Managing Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="c25fb-128">[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="c25fb-128">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="c25fb-129">Finances</span><span class="sxs-lookup"><span data-stu-id="c25fb-129">Finance</span></span>](finance.md)  
