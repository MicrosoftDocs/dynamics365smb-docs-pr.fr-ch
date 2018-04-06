---
title: "Connecter vos données avec Flow| Microsoft Docs"
description: "Vous pouvez rendre vos données Financials disponibles sous forme de données sources et spécifier une URL OData de vos services Web pour générer un flux de travail automatisé."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: b4e2e7bc1c2622d329c73ae5bf47b4accff10aa8
ms.openlocfilehash: dde99e50c6984a7ec162b4047e8640e6affb3f25
ms.contentlocale: fr-ch
ms.lasthandoff: 03/22/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a><span data-ttu-id="2b121-103">Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] dans un flux automatisé</span><span class="sxs-lookup"><span data-stu-id="2b121-103">Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow</span></span>
<span data-ttu-id="2b121-104">Vous pouvez utiliser vos données [!INCLUDE[d365fin](includes/d365fin_md.md)] en tant que partie du flux de travail dans Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="2b121-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="2b121-105">Vous devez disposer d'un compte valide avec [!INCLUDE[d365fin](includes/d365fin_md.md)] et avec Flow.</span><span class="sxs-lookup"><span data-stu-id="2b121-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a><span data-ttu-id="2b121-106">Pour ajouter [!INCLUDE[d365fin](includes/d365fin_md.md)] comme source de données dans Flow</span><span class="sxs-lookup"><span data-stu-id="2b121-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in Flow</span></span>
1. <span data-ttu-id="2b121-107">Dans votre navigateur, accédez à [flow.microsoft.com](https://flow.microsoft.com/en-us/), puis connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="2b121-107">In your browser, navigate to [flow.microsoft.com](https://flow.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="2b121-108">Choisissez **Mes flux** dans le ruban en haut de la page.</span><span class="sxs-lookup"><span data-stu-id="2b121-108">Choose **My Flows** from the ribbon at the top of the page.</span></span>
3. <span data-ttu-id="2b121-109">Dans la fenêtre **Mes flux**, cliquez sur l'option **Créer à partir de rien**.</span><span class="sxs-lookup"><span data-stu-id="2b121-109">In the **My Flows** window, choose the **Create from blank** option.</span></span>
4. <span data-ttu-id="2b121-110">Dans la liste des déclencheurs disponibles, sélectionnez l'un des déclencheurs [!INCLUDE[d365fin](includes/d365fin_md.md)] disponibles :</span><span class="sxs-lookup"><span data-stu-id="2b121-110">From the list of available triggers, select one of the [!INCLUDE[d365fin](includes/d365fin_md.md)] triggers available:</span></span>  
    <span data-ttu-id="2b121-111">*Lorsque l'approbation d'un client est exigée*,</span><span class="sxs-lookup"><span data-stu-id="2b121-111">*When a customer approval is requested*,</span></span>  
    <span data-ttu-id="2b121-112">*Lorsque l'approbation d'un nom feuille comptabilité est exigée*,</span><span class="sxs-lookup"><span data-stu-id="2b121-112">*When a general journal batch approval is requested*,</span></span>  
    <span data-ttu-id="2b121-113">*Lorsque l'approbation d'une ligne feuille comptabilité est exigée*,</span><span class="sxs-lookup"><span data-stu-id="2b121-113">*When a general journal line approval is requested*,</span></span>  
    <span data-ttu-id="2b121-114">*Lorsque l'approbation d'un article est exigée*,</span><span class="sxs-lookup"><span data-stu-id="2b121-114">*When an item approval is requested*,</span></span>  
    <span data-ttu-id="2b121-115">*Lorsque l'approbation d'un document achat est exigée*,</span><span class="sxs-lookup"><span data-stu-id="2b121-115">*When a purchase document approval is requested*,</span></span>  
    <span data-ttu-id="2b121-116">*Lorsque l'approbation d'un document vente est exigée*, ou</span><span class="sxs-lookup"><span data-stu-id="2b121-116">*When a sales document approval is requested*, or</span></span>  
    <span data-ttu-id="2b121-117">*Lorsque l'approbation d'un fournisseur est exigée*.</span><span class="sxs-lookup"><span data-stu-id="2b121-117">*When a vendor aproval is requested*.</span></span>
5. <span data-ttu-id="2b121-118">Flow vous invite à sélectionner une société dans votre abonné [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="2b121-118">Flow will prompt you to select a company within your [!INCLUDE[d365fin](includes/d365fin_md.md)] tenant.</span></span> <span data-ttu-id="2b121-119">Comme chaque étape de Flow est indépendante de la suivante, vous devrez peut-être définir plusieurs fois la société lorsque vous utilisez un modèle [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="2b121-119">Because each step in the Flow is independent of the next, you may be required to define the company multiple times when using a [!INCLUDE[d365fin](includes/d365fin_md.md)] template.</span></span>

<span data-ttu-id="2b121-120">À ce stade, vous êtes connecté à vos données Finance and Operations, Business edition et vous êtes prêt à générer votre flux.</span><span class="sxs-lookup"><span data-stu-id="2b121-120">At this point, you have successfully connected to your Finance and Operations, Business edition data and are ready to begin building your flow.</span></span> <span data-ttu-id="2b121-121">Pour plus d'informations, voir [Documentation Flow](https://flow.microsoft.com/documentation/getting-started/).</span><span class="sxs-lookup"><span data-stu-id="2b121-121">For more information, see the [Flow documentation](https://flow.microsoft.com/documentation/getting-started/).</span></span>

<span data-ttu-id="2b121-122">Pour résoudre les problèmes avec Microsoft Flow, voir [Résolution des problèmes : Intégration à Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="2b121-122">For troubleshooting your Microsoft Flow, see [Troubleshooting Integration with Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="2b121-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b121-123">See Also</span></span>
<span data-ttu-id="2b121-124">[Bienvenue dans [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="2b121-124">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="2b121-125">Importation des données métier à partir d'autres systèmes financiers</span><span class="sxs-lookup"><span data-stu-id="2b121-125">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="2b121-126">[Gérer les utilisateurs et les autorisations](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="2b121-126">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="2b121-127">[Configuration de [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="2b121-127">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="2b121-128">Finances</span><span class="sxs-lookup"><span data-stu-id="2b121-128">Finance</span></span>](finance.md)  

