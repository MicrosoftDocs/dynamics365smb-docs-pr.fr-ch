---
title: Configuration du plan comptable
description: "Vous modifiez les comptes par défaut dans le plan comptable, et vous pouvez ajouter de nouveaux comptes."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 04/16/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 9f84af8bb4ac3be9132ab621906c463cfc9b91ff
ms.contentlocale: fr-ch
ms.lasthandoff: 05/17/2018

---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a><span data-ttu-id="f052e-103">Configuration ou modification du plan comptable</span><span class="sxs-lookup"><span data-stu-id="f052e-103">Setting Up or Changing the Chart of Accounts</span></span>
<span data-ttu-id="f052e-104">Le plan comptable affiche les comptes généraux qui stockent vos données financières.</span><span class="sxs-lookup"><span data-stu-id="f052e-104">The chart of accounts shows the ledger accounts that store your financial data.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="f052e-105"> inclut un plan comptable standard prêt à prendre en charge votre société.</span><span class="sxs-lookup"><span data-stu-id="f052e-105"> includes a standard chart of accounts that is ready to support your business.</span></span>
<span data-ttu-id="f052e-106">Cependant, vous pouvez modifier les comptes par défaut, et vous pouvez ajouter de nouveaux comptes.</span><span class="sxs-lookup"><span data-stu-id="f052e-106">However, you can change the default accounts, and you can add new accounts.</span></span>  

## <a name="adding-or-changing-accounts"></a><span data-ttu-id="f052e-107">Ajout ou modification de comptes</span><span class="sxs-lookup"><span data-stu-id="f052e-107">Adding or Changing Accounts</span></span>
<span data-ttu-id="f052e-108">À partir du plan comptable, vous pouvez ouvrir chaque compte général et ajouter ou modifier des paramètres.</span><span class="sxs-lookup"><span data-stu-id="f052e-108">From the chart of accounts, you can open each G/L account and add or change settings.</span></span>

> [!NOTE]  
>   <span data-ttu-id="f052e-109">Vous pouvez supprimer un compte général.</span><span class="sxs-lookup"><span data-stu-id="f052e-109">You can delete a general ledger account.</span></span> <span data-ttu-id="f052e-110">Toutefois, avant que de le supprimer, les conditions suivantes doivent être réunies :</span><span class="sxs-lookup"><span data-stu-id="f052e-110">However, before you delete it, the following must be true:</span></span>  

* <span data-ttu-id="f052e-111">Le solde du compte doit être nul.</span><span class="sxs-lookup"><span data-stu-id="f052e-111">The balance on the account must be zero.</span></span>  
* <span data-ttu-id="f052e-112">Le champ **Autoriser suppr. cpte gén. av.** doit être défini dans la fenêtre **Paramètres comptabilité**, et le compte ne doit pas comporter d'écritures comptables à cette date ou après celle-ci.</span><span class="sxs-lookup"><span data-stu-id="f052e-112">The **Allow G/L Acc. Deletion Before** field must be set in the **General Ledger Setup** window, and the account must not have ledger entries on or after that date.</span></span>  
* <span data-ttu-id="f052e-113">Si le champ **Vérifier activité cpte général** de la fenêtre **Paramètres comptabilité** est sélectionné, le compte ne doit pas être utilisé dans les groupes comptabilisation ni dans une configuration de la validation.</span><span class="sxs-lookup"><span data-stu-id="f052e-113">If the **Check G/L Account Usage** field in the **General Ledger Setup** window is selected, then the account must not be used in any posting groups or posting setup.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="f052e-114"> vous empêchera de supprimer un compte général qui stocke les données nécessaires au plan comptable.</span><span class="sxs-lookup"><span data-stu-id="f052e-114"> will prevent you from deleting a general ledger account that stores data that is needed in the chart of accounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f052e-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f052e-115">See Also</span></span>
[<span data-ttu-id="f052e-116">Les écritures comptables et le plan comptable</span><span class="sxs-lookup"><span data-stu-id="f052e-116">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
[<span data-ttu-id="f052e-117">Gestion des comptes bancaires</span><span class="sxs-lookup"><span data-stu-id="f052e-117">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="f052e-118">Utilisation des axes analytiques</span><span class="sxs-lookup"><span data-stu-id="f052e-118">Working with Dimensions</span></span>](finance-dimensions.md)  
<span data-ttu-id="f052e-119">[Importation de données à partir d'autres systèmes financiers](across-import-data-configuration-packages.md)(across-import-data-configuration-packages.md)</span><span class="sxs-lookup"><span data-stu-id="f052e-119">[Importing Data from Other Finance Systems](across-import-data-configuration-packages.md)(across-import-data-configuration-packages.md)</span></span>  
[<span data-ttu-id="f052e-120">Utilisation des tableaux d'analyse</span><span class="sxs-lookup"><span data-stu-id="f052e-120">Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
<span data-ttu-id="f052e-121">[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f052e-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

