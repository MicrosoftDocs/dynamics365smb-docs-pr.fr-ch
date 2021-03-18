---
title: Configuration du plan comptable
description: Vous modifiez les comptes par défaut dans le plan comptable, et vous pouvez ajouter de nouveaux comptes.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f14859a641ddf6368a213f396a111a3423f49c4a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fr-CH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377127"
---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a><span data-ttu-id="fa98f-103">Configuration ou modification du plan comptable</span><span class="sxs-lookup"><span data-stu-id="fa98f-103">Setting Up or Changing the Chart of Accounts</span></span>
<span data-ttu-id="fa98f-104">Le plan comptable affiche les comptes généraux qui stockent vos données financières.</span><span class="sxs-lookup"><span data-stu-id="fa98f-104">The chart of accounts shows the ledger accounts that store your financial data.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="fa98f-105">inclut un plan comptable standard prêt à prendre en charge votre société.</span><span class="sxs-lookup"><span data-stu-id="fa98f-105">includes a standard chart of accounts that is ready to support your business.</span></span>
<span data-ttu-id="fa98f-106">Cependant, vous pouvez modifier les comptes par défaut, et vous pouvez ajouter de nouveaux comptes.</span><span class="sxs-lookup"><span data-stu-id="fa98f-106">However, you can change the default accounts, and you can add new accounts.</span></span>
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]


## <a name="adding-or-changing-accounts"></a><span data-ttu-id="fa98f-107">Ajout ou modification de comptes</span><span class="sxs-lookup"><span data-stu-id="fa98f-107">Adding or Changing Accounts</span></span>
<span data-ttu-id="fa98f-108">À partir du plan comptable, vous pouvez ouvrir chaque compte général et ajouter ou modifier des paramètres.</span><span class="sxs-lookup"><span data-stu-id="fa98f-108">From the chart of accounts, you can open each G/L account and add or change settings.</span></span>

> [!NOTE]  
>   <span data-ttu-id="fa98f-109">Vous pouvez supprimer un compte général.</span><span class="sxs-lookup"><span data-stu-id="fa98f-109">You can delete a general ledger account.</span></span> <span data-ttu-id="fa98f-110">Toutefois, avant que de le supprimer, les conditions suivantes doivent être réunies :</span><span class="sxs-lookup"><span data-stu-id="fa98f-110">However, before you delete it, the following must be true:</span></span>  
>  
>   * <span data-ttu-id="fa98f-111">Le solde du compte doit être nul.</span><span class="sxs-lookup"><span data-stu-id="fa98f-111">The balance on the account must be zero.</span></span>  
>   * <span data-ttu-id="fa98f-112">Le champ **Autoriser suppr. cpte gén. av.** doit être défini sur la page **Paramètres comptabilité**, et le compte ne doit pas comporter d’écritures comptables à cette date ou après celle-ci.</span><span class="sxs-lookup"><span data-stu-id="fa98f-112">The **Allow G/L Acc. Deletion Before** field must be set on the **General Ledger Setup** page, and the account must not have ledger entries on or after that date.</span></span>  
>   * <span data-ttu-id="fa98f-113">Si le champ **Vérifier activité cpte général** de la page **Paramètres comptabilité** est sélectionné, le compte ne doit pas être utilisé dans les groupes comptabilisation ni dans une configuration de la validation.</span><span class="sxs-lookup"><span data-stu-id="fa98f-113">If the **Check G/L Account Usage** field on the **General Ledger Setup** page is selected, then the account must not be used in any posting groups or posting setup.</span></span>  

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="fa98f-114">vous empêchera de supprimer un compte général qui stocke les données nécessaires au plan comptable.</span><span class="sxs-lookup"><span data-stu-id="fa98f-114">will prevent you from deleting a general ledger account that stores data that is needed in the chart of accounts.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="fa98f-115">Voir la formation associée sur [Microsoft Learn](/learn/modules/chart-accounts-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="fa98f-115">See Related Training at [Microsoft Learn](/learn/modules/chart-accounts-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="fa98f-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa98f-116">See Also</span></span>
[<span data-ttu-id="fa98f-117">Comptabilité et plan comptable</span><span class="sxs-lookup"><span data-stu-id="fa98f-117">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
[<span data-ttu-id="fa98f-118">Rapprochement de comptes bancaires</span><span class="sxs-lookup"><span data-stu-id="fa98f-118">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="fa98f-119">Utilisation des axes analytiques</span><span class="sxs-lookup"><span data-stu-id="fa98f-119">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="fa98f-120">Importation des données à partir d’autres systèmes financiers</span><span class="sxs-lookup"><span data-stu-id="fa98f-120">Importing Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="fa98f-121">Utilisation des tableaux d’analyse</span><span class="sxs-lookup"><span data-stu-id="fa98f-121">Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
<span data-ttu-id="fa98f-122">[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fa98f-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]