---
title: Importer les transactions de paie| Microsoft Docs
description: Pour gérer les paies, vous importez et validez des transactions financières de votre fournisseur de paie dans la comptabilité, en utilisant une extension de paie telle que Ceridian ou Quickbooks.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2fde597db9f5889678c5501bfdcc5f2412ec47cc
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3917016"
---
# <a name="import-payroll-transactions"></a><span data-ttu-id="2a99d-103">Importer les transactions de paie</span><span class="sxs-lookup"><span data-stu-id="2a99d-103">Import Payroll Transactions</span></span>
<span data-ttu-id="2a99d-104">Pour tenir compte des paiements des salaires et des transactions associées, vous devez importer et valider des transactions financières effectuées par votre fournisseur de paie dans la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="2a99d-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span> <span data-ttu-id="2a99d-105">Pour cela, vous devez commencer par importer un fichier que vous recevez du fournisseur de paie sur la page **Feuille comptabilité** .</span><span class="sxs-lookup"><span data-stu-id="2a99d-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** page.</span></span> <span data-ttu-id="2a99d-106">Vous devez ensuite mapper les comptes externes du fichier de paie aux comptes généraux appropriés.</span><span class="sxs-lookup"><span data-stu-id="2a99d-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="2a99d-107">Enfin, vous devez valider les transactions de paie en fonction du mappage de compte.</span><span class="sxs-lookup"><span data-stu-id="2a99d-107">Lastly, you post the payroll transactions according to the account mapping.</span></span>

> [!NOTE]  
>   <span data-ttu-id="2a99d-108">Pour utiliser cette fonctionnalité, une extension pour l’importation de la paie doit être installée et activée.</span><span class="sxs-lookup"><span data-stu-id="2a99d-108">To use this functionality, an extension for payroll import must be installed and enabled.</span></span> <span data-ttu-id="2a99d-109">Les extensions Salaire de Ceridian et Importer le fichier de paie de Quickbooks sont préinstallées dans [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="2a99d-109">The Ceridian Payroll and the Quickbooks Payroll File Import extensions are pre-installed in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="2a99d-110">Pour plus d’informations, voir [Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l’aide des extensions](ui-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="2a99d-110">For more information, see [Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md).</span></span>

## <a name="to-import-a-payroll-file"></a><span data-ttu-id="2a99d-111">Pour importer un fichier de paie</span><span class="sxs-lookup"><span data-stu-id="2a99d-111">To import a payroll file</span></span>
1. <span data-ttu-id="2a99d-112">Choisissez l’icône ![Ampoule qui ouvre la fonction Tell Me](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire"), saisissez **Feuilles comptabilité** , puis sélectionnez le lien associé.</span><span class="sxs-lookup"><span data-stu-id="2a99d-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals** , and then choose the related link.</span></span>
2. <span data-ttu-id="2a99d-113">Dans le nom feuille comptabilité pertinent, sélectionnez l’action **Importer les transactions de paie** .</span><span class="sxs-lookup"><span data-stu-id="2a99d-113">In the relevant general journal batch, choose the **Import Payroll Transactions** action.</span></span> <span data-ttu-id="2a99d-114">Un guide d’installation assisté s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="2a99d-114">An assisted setup guide opens.</span></span>
3. <span data-ttu-id="2a99d-115">Suivez les étapes de la page **Importer les transactions de paie** .</span><span class="sxs-lookup"><span data-stu-id="2a99d-115">Follow the steps on the **Import Payroll Transactions** page.</span></span>

    > [!TIP]  
    >   <span data-ttu-id="2a99d-116">Dans l’étape à propos du mappage des enregistrements de paie externes dans les comptes généraux, les mappages que vous effectuez seront reconnus la prochaine fois que les mêmes enregistrements seront importés.</span><span class="sxs-lookup"><span data-stu-id="2a99d-116">In the step about mapping the external payroll records to your G/L accounts, the mappings that you make will be remembered next time the same records are imported.</span></span> <span data-ttu-id="2a99d-117">Cela vous permettra d’économiser du temps car vous n’avez pas à remplir manuellement le champ **N° compte** dans la feuille comptabilité à chaque importation de transactions de paie récurrentes.</span><span class="sxs-lookup"><span data-stu-id="2a99d-117">This will save you time as you do not have to manually fill in the **Account No.** field in the general journal every time you have imported recurring payroll transactions.</span></span>   

    <span data-ttu-id="2a99d-118">Lorsque vous cliquez sur le bouton **OK** dans le guide de configuration assistée, la page **Feuille comptabilité** est complétée par des lignes représentant les transactions contenues dans le fichier de paie et par les comptes appropriés des champs **Compte général** en fonction des mappages effectués dans le guide.</span><span class="sxs-lookup"><span data-stu-id="2a99d-118">When you choose the **OK** button in the assisted setup guide, the **General Journal** page is filled with lines representing the transactions that the payroll file contains and with the relevant accounts prefilled in the **G/L Account** fields according to mappings you made in the guide.</span></span>
4. <span data-ttu-id="2a99d-119">Modifiez ou validez les lignes feuille comme pour toute autre transaction comptable générale.</span><span class="sxs-lookup"><span data-stu-id="2a99d-119">Edit or post the journal lines as for any other general ledger transactions.</span></span> <span data-ttu-id="2a99d-120">Pour plus d’informations, reportez-vous à [Valider les transactions directement vers la comptabilité](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="2a99d-120">For more information, see [Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>   

## <a name="see-also"></a><span data-ttu-id="2a99d-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a99d-121">See Also</span></span>
[<span data-ttu-id="2a99d-122">Finances</span><span class="sxs-lookup"><span data-stu-id="2a99d-122">Finance</span></span>](finance.md)  
<span data-ttu-id="2a99d-123">[Personnalisation de [!INCLUDE[d365fin](includes/d365fin_md.md)] à l’aide d’extensions](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="2a99d-123">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="2a99d-124">Utilisation de feuilles comptabilité</span><span class="sxs-lookup"><span data-stu-id="2a99d-124">Working with General Journals</span></span>](ui-work-general-journals.md)  
